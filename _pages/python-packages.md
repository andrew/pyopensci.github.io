---
layout: splash
permalink: /python-packages.html
title: "pyOpenSci Open Peer Review & Accepted Packages"
classes:
header:
    overlay_image: images/header.jpg
    overlay_filter: 0.6
intro:
    - excerpt: "The scientific Python packages below have
    been accepted into the pyOpenSci ecosystem through our [open peer review process](/about-peer-review/)."
toc: false
classes: wide
redirect_from:
  - /python-packages/
---

{% include feature_row id="intro" type="center" %}

{% assign packages_sorted = site.data.packages | sort_natural: 'date_accepted' | reverse %}
{% assign total_packages = packages_sorted | size %}

## Explore our accepted scientific Python open source packages

To date, {{ total_packages }} packages have been accepted into the pyOpenSci
ecosystem. [Click here to check out packages that are currently under review.](https://github.com/pyOpenSci/software-submission/issues)

<p><input type="text" id="quicksearch" placeholder="Search" /></p>

<div id="filters" class="button-group">
  <button class="button is-checked" data-filter="*">show all</button>
  <button class="button" data-filter=".data-munging">data munging</button>
  <button class="button" data-filter=".data-extraction">data extraction</button>
  <button class="button" data-filter=".data-retrieval">data retrieval</button>
  <button class="button" data-filter=".data-visualization">data-visualization</button>
  <button class="button" data-filter=".education">education</button>

<button class="button" data-filter=".geospatial">geospatial</button>
<button class="button" data-filter=".reproducibility">reproducibility</button>

  <!-- <button class="button" data-filter=":not(.transition)">not transition</button>
  <button class="button" data-filter=".metal:not(.transition)">metal but not transition</button> -->
</div>

<div class="grid-isotope">
{% for apackage in packages_sorted %}
  {% include package-grid.html %}
{% endfor %}
</div>

<hr style="clear:both;">
<br clear="both">
