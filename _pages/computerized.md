---
layout: page
title: Computerized Textual Analysis of Fake News
permalink: /computerized/
description: Overview of Computerized Textual Analysis of Fake News
nav: false
nav_order: 2
display_categories: [work, fun]
horizontal: false
---

Fake news is capturing attention worldwide and severely impacting our society. Intervention strategies such as labeling to curb the transmission of fake content on social media at scale need to be built on computational models that can assess information content in real time. Other applications, such as robo-advising in FinTech and online product reviews that rely on trustworthy information, also benefit from effective machine learning methods to detect and filter fake content. My research contributes to this area by applying computerized textual analysis to examine three important aspects of fake news: detection method, societal impact, and mitigation strategy.

<!-- pages/projects.md -->
<div class="projects">
{%- if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  {%- for category in page.display_categories %}
  <h2 class="category">{{ category }}</h2>
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
  {% endfor %}

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
