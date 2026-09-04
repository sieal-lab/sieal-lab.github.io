---
title: "Home"
layout: homelay
permalink: /
seo_title: "SIEAL — Spatial Intelligence and Environmental Analytics Lab, JKUAT"
---

<h2 class="home-hero">Spatial Intelligence and Environmental Analytics Lab</h2>
<p class="home-hero-sub">Department of Geomatic Engineering &amp; Geospatial Information Systems, JKUAT &mdash; Nairobi, Kenya</p>

<div class="chip-container" markdown="0">
<a href="{{ site.url }}{{ site.baseurl }}/research" class="chip">Habitat classification</a>
<a href="{{ site.url }}{{ site.baseurl }}/research" class="chip">Underwater computer vision</a>
<a href="{{ site.url }}{{ site.baseurl }}/research" class="chip">Biodiversity integrity</a>
<a href="{{ site.url }}{{ site.baseurl }}/research" class="chip">Blue carbon</a>
<a href="{{ site.url }}{{ site.baseurl }}/research" class="chip">Deep-sea imagery</a>
<a href="{{ site.url }}{{ site.baseurl }}/research" class="chip">GeoAI</a>
</div>

**SIEAL builds and operates measurement infrastructure for marine habitats and biodiversity.**
Imagery and Earth observation data go in. Habitat classifications, standardised biodiversity metrics,
spatial distribution and hotspot analyses come out &mdash; as maps, with documented provenance and
stated uncertainty. The pipeline was built and published on deep-sea imagery from the Pacific and the
tropical Atlantic. We are now applying it to Kenya's mangroves and coastal waters.

<div class="callout callout-success" markdown="0">
<div class="callout-title"><i class="fa-solid fa-leaf callout-icon"></i> Why we are pointing it at the coast</div>
<p>Carbon finance already reaches Kenya's mangroves; biodiversity finance does not. The credit and disclosure
frameworks were largely designed for forests on land, and marine and coastal systems have no established way to be
measured against them. That measurement is what we build. We structure our outputs to meet Verra VM0033, TNFD, the
GRI Biodiversity Standard and CSRD, so that what we measure can be used in practice &mdash; not just published.</p>
</div>

### What the record looks like

- **Four first-author papers in Nature Portfolio journals** &mdash; *Scientific Reports* (2022, 2023, 2025) and *Scientific Data* (2023) &mdash; on automated seafloor classification, megabenthic fauna detection and analysis-ready underwater imagery
- **Two ocean basins.** The workflows were built in the Clarion&ndash;Clipperton Zone in the Pacific and shown to transfer to the tropical Atlantic, a different basin and geological setting
- **Open methods.** Classification and detection pipelines released as software; the underlying image dataset archived at PANGAEA
- **Operating infrastructure.** A GeoNode data portal, PostGIS and GeoServer services, and GPU compute for model training

This work was carried out by the lab's director at GEOMAR Helmholtz Centre for Ocean Research Kiel, before SIEAL was
established. It is the technical foundation the lab now builds on. See
[Publications]({{ site.url }}{{ site.baseurl }}/publications).

<div class="banner-frame" markdown="0">
<img src="{{ site.url }}{{ site.baseurl }}/images/banner.jpg" alt="Sentinel-2 satellite composite of Mwache Creek and Mombasa, Kenya" loading="lazy">
<div class="banner-caption">Mwache Creek, Mombasa &mdash; Sentinel-2 tidal composite, 2025. Our primary field site.</div>
</div>

### Two settings, one pipeline

**Coastal &mdash; Blue-BII.** Above- and below-ground carbon across mangrove extents, from Sentinel-2 optical
imagery, NASA GEDI spaceborne LiDAR and field allometry; and a biodiversity integrity index derived from
below-water stereo-video, so that a mangrove's ecological condition can be reported alongside the tonnes of
CO<sub>2</sub> it holds. Funded by KENET and by the AIMS Research and Innovation Centre with the Carnegie
Corporation of New York.

**Deep sea &mdash; Deep-BII.** The same integrity approach below 200 m, developed with the Ocean Discovery
League's Western Indian Ocean cohort. Deep-sea habitats are the least surveyed and least protected part of the
ocean, and the BBNJ Treaty creates an immediate need for methods that can assess them from sparse imagery.

<div class="banner-frame" markdown="0">
<img src="{{ site.url }}{{ site.baseurl }}/images/mwache-carbon.jpg" alt="Preliminary estimate of carbon stored in Mwache Creek mangroves" loading="lazy">
<div class="banner-caption">Preliminary carbon stock estimate for 2,890 ha of mangrove forest at Mwache Creek, from combined satellite and LiDAR analysis.</div>
</div>

<p markdown="0"><a href="{{ site.url }}{{ site.baseurl }}/research" class="btn-pill btn-website">Explore our research &rarr;</a>
<a href="{{ site.url }}{{ site.baseurl }}/partner" class="btn-pill btn-doi">Work with us &rarr;</a>
<a href="{{ site.url }}{{ site.baseurl }}/join" class="btn-pill btn-git">We are hiring &rarr;</a></p>
