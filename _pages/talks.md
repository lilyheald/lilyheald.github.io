---
title: "Presentations"
layout: page
permalink: /talks/
---

# Presentations

{% assign invited = site.data.talks | where: "type", "invited" %}
{% assign contributed = site.data.talks | where_exp: "t", "t.type != 'invited'" %}

{% if invited.size > 0 %}
<div class="section-card" markdown="0">
<h2>Invited Talks</h2>
{% for talk in invited %}{% include talk.html talk=talk %}{% endfor %}
</div>
{% endif %}

{% if contributed.size > 0 %}
<div class="section-card" markdown="0">
<h2>Conference Presentations</h2>
{% for talk in contributed %}{% include talk.html talk=talk %}{% endfor %}
</div>
{% endif %}

{% unless site.data.talks.size > 0 %}
<p class="text-muted">No presentations listed yet. Add entries to <code>_data/talks.yml</code>.</p>
{% endunless %}
