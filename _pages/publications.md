---
title: "Publications"
layout: page
permalink: /publications/
---

# Publications

<div class="section-card" id="pubList">
<h2>Under Review</h2>

{% bibliography --query @*[status=review] %}

<h2>In Preparation</h2>

{% bibliography --query @*[status=prep] %}
</div>

<div class="section-card" markdown="0">
<h2>Conference Presentations</h2>
<p>Posters and papers presented at conferences and symposia are listed on the <a href="{{ '/talks' | relative_url }}">Presentations</a> page.</p>
</div>
