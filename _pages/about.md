---
title: "About"
layout: gridlay
permalink: /about/
seo_title: "About SIEAL - measurement infrastructure for marine habitats and biodiversity"
description: "SIEAL is a research group at JKUAT that builds and operates measurement infrastructure for marine habitats and biodiversity, from the deep sea to Kenya's mangroves and coastal waters."
---

## About SIEAL

<div class="section-card" markdown="1">
The **Spatial Intelligence and Environmental Analytics Lab** is a research group in the Department of Geomatic
Engineering and Geospatial Information Systems at Jomo Kenyatta University of Agriculture and Technology, Nairobi.

We build and operate measurement infrastructure for marine habitats and biodiversity. Imagery and Earth
observation data go in &mdash; satellite optical, spaceborne LiDAR, towed camera systems, underwater stereo-video
&mdash; and out come habitat classifications, standardised biodiversity metrics, spatial distribution and hotspot
analyses, and mapped outputs with documented provenance and stated uncertainty. The pipeline was built and
published on deep-sea imagery from the Pacific and the tropical Atlantic; it is now being applied to Kenya's
mangroves and coastal waters. The deep-sea and coastal lines are two applications of one method, not two
unrelated projects.

We design our outputs to meet the reporting standards that carbon and biodiversity markets actually run on, and
we are positioned as a methodology and data provider &mdash; including upstream of the accredited bodies that
carry out validation and verification.

The lab exists because of a specific gap. Biodiversity credit and disclosure frameworks were largely built for
terrestrial ecosystems, and marine and coastal systems remain underrepresented in them. Kenya's mangroves are
among the most carbon-dense ecosystems on Earth and among the least well measured. Carbon finance already reaches
coastal communities here through community-led mangrove conservation; biodiversity finance for the same ecosystems
has no equivalent pathway, because there is no established way to measure it. Our aim over the coming years
is to make SIEAL a leading source of GeoAI-based blue carbon and marine biodiversity intelligence for the
Western Indian Ocean.
</div>

<div class="section-card" markdown="1">
### Infrastructure

The lab operates its own stack rather than borrowing one project by project. A GeoNode instance, backed by
PostGIS and GeoServer, is our data-publishing portal, so that datasets and map services can be released with
metadata and served to collaborators rather than emailed as files. Model training runs on an NVIDIA A30 GPU
provided by the Kenya Education Network (KENET), with further capacity available on KENET's Chui
high-performance computing facility subject to allocation.

This is what separates an operating lab from an individual researcher, and it is the honest answer to the
capacity question any funder or client will ask of a group this size. It is also a fair statement of the
limits: present capacity supports model development, and scaling to repeat inference across multiple sites
is something we would size and cost as part of an engagement rather than assume.
</div>

{% comment %}
TODO: link the portal (portal.sieal.org) from here once the first dataset is
published on it. Pointing a funder or procurement reader at an empty portal
costs more credibility than the link gains.

Liquid comment, not an HTML one: HTML comments are served to the browser and
show up in view-source on a public page.
{% endcomment %}

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
marine and coastal ecosystems in the Western Indian Ocean, and with intergovernmental, regional and
development-finance bodies procuring technical input on habitat mapping, biodiversity measurement and area-based
management &mdash; see
[Partner with us]({{ site.url }}{{ site.baseurl }}/partner)
for what that can look like in practice. If you are looking to work *in* the lab,
see [Join us]({{ site.url }}{{ site.baseurl }}/join). Otherwise our
[contact details]({{ site.url }}{{ site.baseurl }}/contact) are here.
</div>
