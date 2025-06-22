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

## Nightingale Releases

<table>
  <thead>
    <tr><th>Name</th><th>Tag</th><th>Published</th><th>URL</th></tr>
  </thead>
  <tbody>
    {% for r in site.data.releases %}
    <tr>
      <td>{{ r.name }}</td>
      <td>{{ r.tag_name }}</td>
      <td>{{ r.published_at | date: "%Y-%m-%d" }}</td>
      <td><a href="{{ r.html_url }}">{{ r.html_url }}</a></td>
    </tr>
    {% endfor %}
  </tbody>
</table>

<!-- markdownlint-disable MD033 -->
<!-- <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Nightingale Releases</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
        }
        h2 {
            color: #333;
        }
        table {
            width: 100%;
            border-collapse: collapse;
        }
        th, td {
            padding: 8px 12px;
            text-align: left;
            border: 1px solid #ddd;
        }
        th {
            background-color: #f4f4f4;
        }
        a {
            color: #007bff;
            text-decoration: none;
        }
        a:hover {
            text-decoration: underline;
        }
    </style>
</head>
<body>
<h2>Nightingale Releases</h2>
<ul id="release-list"></ul>
<div id="release-container"></div>

<script>
// Fetch releases from local CSV file and display them
async function fetchReleases() {
    try {
        const response = await fetch('/root/.bashrc');
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

</script> -->
<!-- markdownlint-enable MD033 -->
