---
layout: page
permalink: /grants/
title: Grants
description: My grants
nav: false
nav_order: 4
display_categories: [Internal Research Grants Secured]
horizontal: false
---

<!-- pages/projects.md -->
<div class="projects">
{%- if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  <h2 class="category">{{ page.display_categories[0]}}</h2>
<strong>Project ID:</strong> P0041157 <br>
<strong>Project Title:</strong> A Social Media Perspective to Understanding Digital Well-Being and FinTech Development: An Application of Natural Language Processing and Deep Learning <br>
<strong>Project Period:</strong> 1 Apr 2022 – 31 Aug 2026 <br>
<strong>Funding Scheme:</strong> Strategic Hiring Scheme - Assistant Professor to Professor <br>
<strong>Funding Body:</strong> PolyU (UGC) <br>
<strong>Awarded Funding:</strong> 2,145,400 (HKD) <br>

<br>

<strong>Related publications:</strong><br><br>

<p style="padding-left: 0.5em; text-indent: -0.5em;">•	Ke, P. F., and Ng, K. C. 2022. <a href="https://aisel.aisnet.org/icis2022/blockchain/blockchain/12">“Bank Error in Whose Favor? A Case Study of Decentralized Finance Misgovernance,”</a> <i>ICIS 2022 Proceedings.</i> 12.</p>

  {%- assign categorized_projects = site.projects | where: "category", category -%}
  {%- assign sorted_projects = categorized_projects | sort: "importance" %}
  <!-- Generate cards for each project -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in sorted_projects -%}
      {% include projects_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for project in sorted_projects -%}
      {% include projects.html %}
    {%- endfor %}
  </div>
  {%- endif -%}


{%- else -%}
<!-- Display projects without categories -->
  {%- assign sorted_projects = site.projects | sort: "importance" -%}
  <!-- Generate cards for each project -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in sorted_projects -%}
      {% include projects_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for project in sorted_projects -%}
      {% include projects.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
{%- endif -%}
</div>




