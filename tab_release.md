---

title: Release
displaytext: Release
layout: col-sidebar
tab: true
tags: Nightingale
order: 4
level: 2
type: tool

---
<h2>Nightingale Releases</h2>
<ul id="release-list"></ul>
<div id="release-container"></div>

<script>
// Fetch releases from GitHub and store them in a CSV file
async function fetchReleases() {
    try {
        const response = await fetch("https://api.github.com/repos/RAJANAGORI/Nightingale/releases");
        const data = await response.json();
        
        // Convert JSON to CSV format
        let csvContent = "tag_name,published_at,html_url\n";
        data.forEach(release => {
            csvContent += `${release.tag_name},${release.published_at},${release.html_url}\n`;
        });
        
        // Store in local storage (or backend API if needed)
        localStorage.setItem("github_releases", csvContent);
        
        displayReleases(csvContent);
    } catch (error) {
        console.error("Error fetching releases:", error);
    }
}

// Display data from CSV in a table
function displayReleases(csvData) {
    let rows = csvData.split("\n").filter(row => row.trim() !== "");
    if (rows.length <= 1) return; // No valid data to display
    
    let table = `<table border='1'><tr><th>Tag</th><th>Published Date</th><th>URL</th></tr>`;
    
    rows.slice(1).forEach(row => {
        let cols = row.split(",");
        if (cols.length < 3) return; // Skip malformed rows
        table += `<tr><td>${cols[0]}</td><td>${new Date(cols[1]).toDateString()}</td><td><a href='${cols[2]}' target='_blank'>Link</a></td></tr>`;
    });
    table += "</table>";
    
    document.getElementById("release-container").innerHTML = table;
}

// Load data when the page loads
window.onload = () => {
    let storedData = localStorage.getItem("github_releases");
    if (storedData) {
        displayReleases(storedData);
    } else {
        fetchReleases();
    }
};
</script>
