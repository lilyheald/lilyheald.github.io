---
title: "About"
layout: page
permalink: /about/
---

# About

<div class="section-card">
<div class="pi-card">
<img src="{{ site.photo | prepend: '/images/' | relative_url }}" class="pi-photo" alt="{{ site.name }}" width="160" height="160">
<div>
<h2 class="pi-name">{{ site.name }}</h2>
<p style="font-style: italic; color: var(--text-secondary);">{{ site.title }}, {{ site.institution }}</p>
<div class="pi-links">
{% if site.email %}<a href="mailto:{{ site.email }}" class="icon-link" title="Email" aria-label="Email">{% include icon.html name="envelope" %}</a>{% endif %}
{% if site.links.cv and site.links.cv != "" %}<a href="{{ site.links.cv | prepend: '/' | relative_url }}" class="icon-link" title="CV" aria-label="CV">{% include icon.html name="cv" %}</a>{% endif %}
{% if site.links.google_scholar and site.links.google_scholar != "" %}<a href="{{ site.links.google_scholar }}" class="icon-link" title="Google Scholar" aria-label="Google Scholar">{% include icon.html name="google-scholar" %}</a>{% endif %}
{% if site.links.github and site.links.github != "" %}<a href="{{ site.links.github }}" class="icon-link" title="GitHub" aria-label="GitHub">{% include icon.html name="github" %}</a>{% endif %}
{% if site.links.researchgate and site.links.researchgate != "" %}<a href="{{ site.links.researchgate }}" class="icon-link" title="ResearchGate" aria-label="ResearchGate">{% include icon.html name="researchgate" %}</a>{% endif %}
{% if site.links.linkedin and site.links.linkedin != "" %}<a href="{{ site.links.linkedin }}" class="icon-link" title="LinkedIn" aria-label="LinkedIn">{% include icon.html name="linkedin" %}</a>{% endif %}
</div>
{% if site.data.pi[0].education %}
<ul style="margin-top: var(--space-4);">
{% for education in site.data.pi[0].education %}
<li>{{ education | replace: "-","&#8211;" }}</li>
{% endfor %}
</ul>
{% endif %}
</div>
</div>
</div>

<div class="section-card" markdown="0">
<h3>Research Experience</h3>
<ul>
<li><strong>Research Data Analyst</strong>, <a href="https://nielsen-lab.github.io/">Nielsen Lab</a>, UC Berkeley (2026&#8211;present). Advisor: Dr. Rasmus Nielsen.
<ul>
<li>Developing and optimizing inference for a computational method under a structured Wright&#8211;Fisher model that jointly infers selection coefficients, migration rates, and effective population sizes from serial allele-frequency time series across multiple structured populations.</li>
<li>Built an HPC pipeline applying the method to the Allen Ancient DNA Resource 2M SNP panel to study the evolution of pigmentation and lactase persistence in ancient Eurasian populations.</li>
</ul></li>
<li><strong>Undergraduate Honors Thesis</strong>, University of Michigan (2025&#8211;2026). Advisor: Dr. Tina Lasisi.
<ul>
<li>Independently designed and carried out the thesis <a href="https://lilyheald.github.io/PAINT/"><em>Pigmentation Genetics in Archaic Hominins: Evaluating DNA Phenotyping in Neanderthal and Denisovan Genomes</em></a>, using public ancient genomic data from the Simons Genome Diversity Project and the Max Planck Institute for Evolutionary Anthropology.</li>
<li>Performed genetic PCA and genotype-reliability assessment in low-coverage archaic genomes with PLINK and samtools in Linux and HPC environments.</li>
</ul></li>
<li><strong>Research Assistant</strong>, <a href="https://www.lasisilab.com/">Lasisi Lab</a>, University of Michigan (2024&#8211;2026). Advisor: Dr. Tina Lasisi.
<ul>
<li>Contributed literature searches, synthesis, and drafting to a co-authored review on the genetics of human pigmentation and hair morphology.</li>
<li>Analyzed a high-dimensional dataset of genetic, survey, and reflectance measures to test assumptions behind constitutive and facultative skin pigmentation metrics.</li>
<li>Built a literature-derived reference database of pigmentation-associated genes and SNPs in the modern human genome for lab-wide use.</li>
</ul></li>
<li><strong>Undergraduate Research Assistant</strong>, <a href="https://sites.lsa.umich.edu/ancient-protein-isotope-lab/">Ancient Protein and Isotope Laboratory Group</a> (Near Eastern Archaeology subgroup), University of Michigan (2022&#8211;2024). PI: Dr. Alicia Ventresca-Miller; Mentor: Kara Larson.
<ul>
<li>Developed and published the open-source R package <a href="https://github.com/lilyheald/isotopeTools">isotopeTools</a> to automate stable isotope analysis of sequential enamel samples.</li>
<li>Sequentially sampled and analyzed enamel from 21 molars of sheep, goats, and cattle to reconstruct diet and mobility as proxies for economic specialization.</li>
<li>Integrated survey and stable isotope data to evaluate herd management practices.</li>
</ul></li>
</ul>
</div>

<div class="section-card" markdown="0">
<h3>Field Experience</h3>
<ul>
<li><strong>Crew</strong>, University of T&uuml;bingen Excavations at Hohle Fels, Blaubeuren, Germany (2024). Excavated Middle Paleolithic layers at this UNESCO World Heritage site, contributing to research on early human and Neanderthal material culture; prepared microfauna for paleoecological reconstruction and archived excavated materials, including lithic artifacts.</li>
<li><strong>Undergraduate Member</strong>, Renewed Archaeological Excavations at Tell el-Hesi, Negev (2023). Excavated Early Bronze Age layers, contributing to research on the rise of urbanism in the southern Levant, and managed and documented recovered pottery and faunal remains.</li>
</ul>
</div>

{% if site.data.awards %}
<div class="section-card">
<h3>Awards &amp; Honors</h3>
<ul>
{% for award in site.data.awards %}
<li>{{ award.name }}</li>
{% endfor %}
</ul>
</div>
{% endif %}

<div class="section-card" markdown="0">
<h3>Skills</h3>
<ul>
<li><strong>Programming languages:</strong> R, Python, Bash</li>
<li><strong>Bioinformatics &amp; ML:</strong> PLINK, samtools, PyTorch</li>
<li><strong>Developer tools:</strong> Git, Linux, Slurm</li>
<li><strong>Languages:</strong> English (fluent); Chinese (reading and oral comprehension)</li>
</ul>
</div>

<div class="section-card" markdown="0">
<h3>Relevant Coursework</h3>
<ul>
<li>Statistical Machine Learning (Datasci 415)</li>
<li>Introduction to the Design of Experiments (Datasci 470)</li>
<li>Statistics and AI (Datasci 315)</li>
<li>Introduction to Theoretical Probability (Stats 426)</li>
<li>Introduction to Probability (Math 425)</li>
<li>Genetics (Biology 305)</li>
<li>Molecular Anthropology (Anthrbio 469)</li>
<li>Introduction to Biochemistry (MCDB 310)</li>
</ul>
</div>
