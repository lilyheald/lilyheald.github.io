---
title: "Home"
layout: homelay
permalink: /
---

<h1 class="home-hero">{{ site.name }}</h1>
<p class="home-hero-sub">{{ site.title }}, <a href="https://nielsen-lab.github.io/">Nielsen Lab</a>, UC Berkeley</p>

<div class="chip-container" markdown="0">
<a href="{{ '/research' | relative_url }}" class="chip">Population &amp; Evolutionary Genetics</a>
<a href="{{ '/research' | relative_url }}" class="chip">Ancient DNA</a>
<a href="{{ '/research' | relative_url }}" class="chip">Computational &amp; Statistical Genetics</a>
<a href="{{ '/research' | relative_url }}" class="chip">Human Evolutionary History</a>
<a href="{{ '/research' | relative_url }}" class="chip">Machine Learning</a>
</div>

I am a Research Data Analyst in the [Nielsen Lab](https://nielsen-lab.github.io/) in the Department of Integrative Biology at UC Berkeley, working with Dr. Rasmus Nielsen.
I use statistical and computational methods on modern and ancient genomes to study human evolutionary history, with a particular focus on how natural selection has shaped traits such as pigmentation.

Right now I am developing inference for a structured Wright–Fisher model that jointly estimates selection coefficients, migration rates, and effective population sizes from allele-frequency time series sampled across multiple populations.
I am applying it to the Allen Ancient DNA Resource to study the evolution of pigmentation and lactase persistence in ancient Eurasian populations.

{% capture selected %}{% bibliography --query @*[selected=true] %}{% endcapture %}
{% if selected contains "pub-entry" %}
## Selected publications

<div class="section-card selected-pubs" markdown="0">
{{ selected }}
<p style="margin: var(--space-4) 0 0;"><a href="{{ '/publications' | relative_url }}">All publications &rarr;</a></p>
</div>
{% endif %}

## About me

I graduated from the University of Michigan in 2026 with a B.S. in Statistics and in Human Origins, Biology, and Behavior, with Highest Honors.
For my honors thesis with [Dr. Tina Lasisi](https://www.lasisilab.com/), I evaluated how reliably pigmentation phenotypes can be predicted from low-coverage Neanderthal and Denisovan genomes ([project site](https://lilyheald.github.io/PAINT/)).
In the Lasisi Lab I also contributed to a review of the genetics of human pigmentation and hair morphology and analyzed genetic, survey, and skin-reflectance data to test assumptions behind pigmentation measurements.

Before turning to genetics, I worked in zooarchaeology with the [Ancient Protein and Isotope Laboratory Group](https://sites.lsa.umich.edu/ancient-protein-isotope-lab/), using stable isotopes in animal tooth enamel to reconstruct ancient herding practices. I wrote the R package [isotopeTools](https://github.com/lilyheald/isotopeTools) to automate that analysis.
I have also excavated at Hohle Fels in Germany and Tell el-Hesi in the Negev.
