---
title: "Team"
layout: gridlay
permalink: /team/
description: "The people behind SIEAL: Dr. Benson Mbani, Ruth Mellanie Adhiambo and Orado Wiseman Safa, at JKUAT in Nairobi, Kenya."
---

## Team

## Principal Investigator

<div class="section-card">
<div class="pi-card">
<img src="{{ site.url }}{{ site.baseurl }}/images/team/benson-mbani.jpg" class="pi-photo" alt="Benson Mbani" loading="lazy">
<div>
<h3 class="pi-name">Dr. Benson Mbani</h3>
<p style="font-style: italic; color: var(--text-secondary);">Lecturer, Department of Geomatic Engineering &amp; Geospatial Information Systems, JKUAT &mdash; Founder, SIEAL</p>
<div class="pi-links">
{% if site.email and site.email != "" %}<a href="mailto:{{ site.email }}" class="icon-link" title="Email"><i class="fa-solid fa-envelope"></i></a>{% endif %}
{% if site.links.google_scholar and site.links.google_scholar != "" %}<a href="{{ site.links.google_scholar }}" class="icon-link" title="Google Scholar"><i class="ai ai-google-scholar"></i></a>{% endif %}
{% if site.links.orcid and site.links.orcid != "" %}<a href="{{ site.links.orcid }}" class="icon-link" title="ORCID"><i class="ai ai-orcid"></i></a>{% endif %}
{% if site.links.linkedin and site.links.linkedin != "" %}<a href="{{ site.links.linkedin }}" class="icon-link" title="LinkedIn"><i class="fa-brands fa-linkedin"></i></a>{% endif %}
{% if site.links.github and site.links.github != "" %}<a href="{{ site.links.github }}" class="icon-link" title="GitHub"><i class="fa-brands fa-github"></i></a>{% endif %}
</div>
<ul style="margin-top: var(--space-4);">
{% for education in site.data.pi[0].education %}
<li>{{ education | replace: "-","&#8211;" }}</li>
{% endfor %}
</ul>
</div>
</div>

<div markdown="1" style="margin-top: var(--space-5);">
Benson holds a PhD in Marine Data Science from GEOMAR Helmholtz Centre for Ocean Research and Kiel University,
where his doctoral work with Prof. Dr. Jens Greinert focused on automated deep-sea image analysis. That work
produced first-author papers in *Scientific Reports* and *Scientific Data* on seafloor classification in the
Clarion&ndash;Clipperton Zone, the FaunD-Fast model for megabenthic fauna detection, and sediment and megafauna
distribution in the tropical Atlantic.

He returned to Kenya to establish SIEAL, where his research centres on the Blue Biodiversity Integrity Index &mdash;
a dual-arm GeoAI pipeline pairing satellite-based carbon stock mapping with a below-water integrity index derived
from stereo-video and computer vision, designed to produce compliance-grade outputs for carbon and biodiversity
disclosure frameworks.
</div>
</div>

{% if site.data.team_members.size > 0 %}
## Lab members

<div class="team-grid">
{% for member in site.data.team_members %}
<div class="team-card">
<img src="{{ site.url }}{{ site.baseurl }}/images/{{ member.photo }}" class="team-photo" alt="{{ member.name }}" loading="lazy">
<h4 class="team-name">{{ member.name }}</h4>
<p class="team-info">{{ member.info }}</p>
<div class="team-links">
{% if member.email %}<a href="mailto:{{ member.email }}" class="icon-link" title="Email"><i class="fa-solid fa-envelope"></i></a>{% endif %}
{% if member.website %}<a href="{{ member.website }}" class="icon-link" title="Website"><i class="fa-solid fa-house"></i></a>{% endif %}
{% if member.scholar %}<a href="{{ member.scholar }}" class="icon-link" title="Google Scholar"><i class="ai ai-google-scholar"></i></a>{% endif %}
{% if member.github %}<a href="{{ member.github }}" class="icon-link" title="GitHub"><i class="fa-brands fa-github"></i></a>{% endif %}
{% if member.linkedin %}<a href="{{ member.linkedin }}" class="icon-link" title="LinkedIn"><i class="fa-brands fa-linkedin"></i></a>{% endif %}
</div>
</div>
{% endfor %}
</div>
{% endif %}

{% if site.data.alumni and site.data.alumni.size > 0 %}
## Alumni

<div class="section-card">
<table class="alumni-table">
<thead>
<tr><th>Name</th><th>Years in the lab</th><th>Now</th></tr>
</thead>
<tbody>
{% for member in site.data.alumni %}
<tr>
<td>{{ member.name }}</td>
<td>{{ member.duration }}</td>
<td>{{ member.info }}</td>
</tr>
{% endfor %}
</tbody>
</table>
</div>
{% endif %}
