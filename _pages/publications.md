---
layout: page
permalink: /publications/
title: publications
page-title: Publications
description: Sample citations stole from your website.
years: [2024, 2023]
nav: true
nav_order: 4
---
<!-- _pages/publications.md -->
<div class="publications">

{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>
