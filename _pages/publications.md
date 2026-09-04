---
title: "Publications"
layout: gridlay
permalink: /publications/
description: "Peer-reviewed papers, archived datasets and released research software from SIEAL and its founder Benson Mbani, with DOIs and open-access links."
---

## Publications

Four peer-reviewed articles in Nature Portfolio journals, an archived image dataset and three software releases.
The papers were written by the lab's director at GEOMAR Helmholtz Centre for Ocean Research Kiel between 2022 and
2025, before SIEAL was established; they are the methodological foundation the lab now works from.

The datasets and software below are listed alongside the papers deliberately. A method that has been released and
archived can be inspected, rerun and audited; a citation cannot. For anyone assessing whether this lab can deliver
a piece of work, the released artefacts are the stronger evidence.

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
