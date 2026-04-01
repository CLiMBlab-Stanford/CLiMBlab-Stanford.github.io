---
layout: page
permalink: /publications/
title: publications
page-title: Publications
description: Here's the full list of publications and preprints  from the lab
start_year: 2010
nav: true
nav_order: 4
---
<!-- _pages/publications.md -->
<div class="publications">
  {%- assign current_year = "now" | date: "%Y" | plus: 0 -%}

  {%- for y in (page.start_year..current_year) reversed -%}
    {%- capture year_query -%}@*[year={{ y }}]*{%- endcapture -%}
    {%- capture year_count -%}{% bibliography_count -f papers -q {{ year_query }} %}{%- endcapture -%}
    {%- assign year_count = year_count | strip | plus: 0 -%}

    {%- if year_count > 0 -%}
      <h2 class="year">{{ y }}</h2>
      {% bibliography -f papers -q {{ year_query }} %}
    {%- endif -%}
  {%- endfor -%}
</div>
