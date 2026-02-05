---
layout: page
permalink: /publications/
title: publications
description: † denotes equal contribution | * denotes corresponding authorship
nav: true
nav_order: 1
---
<!-- _pages/publications.md -->
<div class="publications">

  <div id="pub-filters" class="pub-filters" style="margin-bottom: 1rem;">
    <button class="btn btn-sm z-depth-0 active" data-filter="all">
      All
    </button>
    <button class="btn btn-sm z-depth-0" data-filter="selected">
      Selected only
    </button>
    <button class="btn btn-sm z-depth-0" data-filter="review">
      Review
    </button>
    <button class="btn btn-sm z-depth-0" data-filter="boride">
      Boride
    </button>
    <button class="btn btn-sm z-depth-0" data-filter="restructuring">
      Restructuring
    </button>
  </div>

{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>

