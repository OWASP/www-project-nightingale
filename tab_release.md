<script>
// Fetch releases from local CSV file and display them
async function fetchReleases() {
    try {
        const response = await fetch('/releases.csv');
        const csvText = await response.text();
        displayReleases(csvText);
    } catch (error) {
        console.error('Error fetching releases CSV:', error);
    }
}

function displayReleases(csvData) {
    const rows = csvData.trim().split('\n');
    if (rows.length === 0) return;

    let table = `<table border="1"><tr><th>Tag</th><th>Published Date</th><th>URL</th></tr>`;

    rows.forEach(row => {
        const cols = row.split(',');
        if (cols.length < 3) return;

        // Remove surrounding quotes
        const tag = cols[0].replace(/^"|"$/g, '');
        const published = cols[1].replace(/^"|"$/g, '');
        const url = cols.slice(2).join(',').replace(/^"|"$/g, '');

        const dateStr = new Date(published).toDateString();
        table += `<tr>` +
                 `<td>${tag}</td>` +
                 `<td>${dateStr}</td>` +
                 `<td><a href="${url}" target="_blank">${url}</a></td>` +
                 `</tr>`;
    });

    table += `</table>`;
    document.getElementById('release-container').innerHTML = table;
}

// Load CSV and render on page load
window.onload = fetchReleases;
</script>
