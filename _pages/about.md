---
title: "About"
layout: gridlay
sitemap: false
permalink: /about/
---

## About SIEAL

<div class="section-card" markdown="1">
The **Spatial Intelligence and Environmental Analytics Lab** is a research group in the Department of Geomatic
Engineering and Geospatial Information Systems at Jomo Kenyatta University of Agriculture and Technology, Nairobi.

We develop GeoAI pipelines that measure carbon storage and biodiversity in blue carbon ecosystems &mdash; mangroves,
seagrass and the coastal waters around them. Our work combines satellite remote sensing, spaceborne LiDAR,
underwater stereo-video, computer vision and geostatistical modelling, and we design our outputs to meet the
reporting standards that carbon and biodiversity markets actually run on.

The lab exists because of a specific gap. Biodiversity credit and disclosure frameworks were largely built for
terrestrial ecosystems, and marine and coastal systems remain underrepresented in them. Kenya's mangroves are
among the most carbon-dense ecosystems on Earth and among the least well measured. Our aim over the coming years
is to make SIEAL a leading source of GeoAI-based blue carbon and marine biodiversity intelligence for the
Western Indian Ocean.
</div>

{% if site.data.grants %}
<div class="section-card">
<h3>Funding</h3>
<ul>
{% for grant in site.data.grants %}
<li style="margin-bottom: var(--space-3);">{{ grant.name }}</li>
{% endfor %}
</ul>
</div>
{% endif %}

{% if site.data.funders and site.data.funders.size > 0 %}
<div class="section-card">
<h4>Our funders</h4>
<div class="sponsor-logos" style="display: flex; flex-wrap: wrap; align-items: center; justify-content: center; gap: var(--space-6);">
{% for funder in site.data.funders %}
<a href="{{ funder.url }}" target="_blank" rel="noopener"><img src="{{ site.url }}{{ site.baseurl }}/images/{{ funder.image }}" alt="Funder logo" style="max-height: 80px; max-width: 200px; border-radius: 0;" loading="lazy"></a>
{% endfor %}
</div>
</div>
{% endif %}

<div class="section-card" markdown="1">
### Get in touch

We welcome collaboration with conservation organisations, carbon project developers and researchers working on
coastal ecosystems in the Western Indian Ocean. See [Contact]({{ site.url }}{{ site.baseurl }}/contact), or
[Join us]({{ site.url }}{{ site.baseurl }}/join) if you are looking to work in the lab.
</div>
