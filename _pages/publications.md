---
title: "Publications"
layout: gridlay
sitemap: false
permalink: /publications/
---

## Publications

<input type="text" class="pub-search" id="pubSearch" placeholder="Filter by title, author, or year...">

<div class="section-card" id="pubList">

<h3>In preparation</h3>

{% bibliography --query @unpublished %}

<h3>Journal articles</h3>

{% bibliography --query @article %}

<h3>Datasets and research software</h3>

{% bibliography --query @misc %}

<h3>Thesis</h3>

{% bibliography --query @phdthesis %}

</div>
