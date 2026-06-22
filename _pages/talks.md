---
title: "Talks"
layout: gridlay
sitemap: false
permalink: /talks/
---

## Talks

<div class="section-card" id="pubList">
<h3>Oral presentations</h3>

{% bibliography --query @incollection[keywords != poster] %}


<h3>Posters presentations</h3>

{% bibliography --query @incollection[keywords ^= poster] %}
</div>
