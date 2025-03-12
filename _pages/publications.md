---
layout: page
permalink: /publications/
title: publications
page-title: Publications
description: Here's the full list of publications and preprints  from the lab
nav: true
nav_order: 4
---
<!-- _pages/publications.md -->
<div class="publications">

{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography %}
{% endfor %}

</div>
