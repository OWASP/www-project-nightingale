---

title: Release
displaytext: Release
layout:  col-sidebar
tab: true
tags: Nightingale
order: 4
level: 2
type: tool

---
<h2>Nightingale Releases</h2>
<ul id="release-list"></ul>

<script>
fetch("https://api.github.com/repos/RAJANAGORI/Nightingale/releases")
  .then(response => response.json())
  .then(data => {
    let list = document.getElementById("release-list");
    data.forEach(release => {
      let li = document.createElement("li");
      li.innerHTML = `<a href="${release.html_url}">${release.tag_name}</a> - ${new Date(release.published_at).toDateString()}`;
      list.appendChild(li);
    });
  })
  .catch(error => console.error("Error fetching releases:", error));
</script>