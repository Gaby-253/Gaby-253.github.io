---
title: "About"
layout: gridlay
sitemap: false
permalink: /about/
---

## About
<div class="section-card">
<div class="pi-card">
<img src="{{ site.url }}{{ site.baseurl }}/images/{{ site.photo }}" class="pi-photo" alt="{{ site.name }}" loading="lazy">
<div>
<h3 class="pi-name">{{ site.name }}</h3>
<p style="font-style: italic; color: var(--text-secondary);">{{ site.title }}, {{ site.institution }}</p>
<div class="pi-links">
{% if site.email %}<a href="mailto:{{ site.email }}" class="icon-link" title="Email"><i class="fa-solid fa-envelope"></i></a>{% endif %}
{% if site.links.cv and site.links.cv != "" %}<a href="{{ site.url }}{{ site.baseurl }}/{{ site.links.cv }}" class="icon-link" title="CV"><i class="ai ai-cv"></i></a>{% endif %}
{% if site.links.google_scholar and site.links.google_scholar != "" %}<a href="{{ site.links.google_scholar }}" class="icon-link" title="Google Scholar"><i class="ai ai-google-scholar"></i></a>{% endif %}
{% if site.links.github and site.links.github != "" %}<a href="{{ site.links.github }}" class="icon-link" title="GitHub"><i class="fa-brands fa-github"></i></a>{% endif %}
{% if site.links.researchgate and site.links.researchgate != "" %}<a href="{{ site.links.researchgate }}" class="icon-link" title="ResearchGate"><i class="ai ai-researchgate"></i></a>{% endif %}
</div>
{% if site.data.pi[0].education %}
<div class="education-list">
{% for edu in site.data.pi[0].education %}
<div class="education-item">
<span class="edu-year">{{ edu["year"] }}</span>
<div class="edu-content">
<strong>{{ edu["degree"] }}</strong><br>
<span>{{ edu["institution"] }}</span>
</div>
</div>
{% endfor %}
</div>
{% endif %}
</div>
</div>
</div>

{% if site.data.grants %}
<div class="section-card">
<h3>Grants and Fellowships</h3>
<ul>
{% for grant in site.data.grants %}
<li>{{ grant.name }}</li>
{% endfor %}
</ul>
</div>
{% endif %}

{% if site.data.awards %}
<div class="section-card">
<h3>Awards</h3>
<ul>
{% for award in site.data.awards %}
<li>{{ award.name | replace: "-","&#8211;" }}</li>
{% endfor %}
</ul>
</div>
{% endif %}

{% if site.data.people %}
<div class="section-card" markdown="0">
<h3>References</h3>
<div class="reference-grid">
{% for person in site.data.people %}
<div class="reference-card">
<h4>{{ person.name }}</h4>
<p><strong>{{ person.role }}</strong></p>
<p>{{ person.institution }}</p>
<p>{{ person.description }}</p>
</div>
{% endfor %}
</div>
</div>
{% endif %}

{% if site.data.service %}
<div class="section-card">
<h3>Professional Service</h3>

<div class="service-groups">

<div class="service-group">
<h4>Reviewing</h4>
<ul>
{% for item in site.data.service.reviewing %}
<li>{{ item }}</li>
{% endfor %}
</ul>
</div>

<div class="service-group">
<h4>Community</h4>
<ul>
{% for item in site.data.service.community %}
<li>{{ item }}</li>
{% endfor %}
</ul>
</div>

<div class="service-group">
<h4>Organization</h4>
<ul>
{% for item in site.data.service.organization %}
<li>{{ item }}</li>
{% endfor %}
</ul>
</div>

</div>
</div>
{% endif %}

{% if site.data.funders %}
<div class="section-card">
<h4>Affiliations</h4>
<div class="sponsor-logos" style="display: flex; flex-wrap: wrap; align-items: center; justify-content: center; gap: var(--space-6);">
{% for funder in site.data.funders %}
<a href="{{ funder.url }}" target="_blank"><img src="{{ site.url }}{{ site.baseurl }}/images/{{ funder.image }}" alt="Funder logo" style="max-height: 80px; max-width: 200px; border-radius: 0;" loading="lazy"></a>
{% endfor %}
</div>
</div>
{% endif %}
