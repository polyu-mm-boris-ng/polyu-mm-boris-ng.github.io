---
layout: page
title: Strategic Manipulation in Machine Learning
permalink: /strategic/
description: Overview of Strategic Manipulation in Machine Learning
nav: false
nav_order: 2
display_categories: [strategic]
horizontal: false
---

Machine learning is widely used for decision-making in many business contexts. Although machine learning has been well recognized for identifying meaningful patterns from massive data, they are vulnerable to input manipulation, as agents may strategically behave or manipulate their characteristics to obtain the desired inference from machine learning models. Therefore, one stream of my research works on solutions to address this problem. Specifically, my ongoing works propose a human-AI hybrid approach that utilizes the complementarity of human knowledge and AI to improve the information processing of firm disclosures. In this context, adversarial behaviors can be observed as managers strategically adjust language and information content to mitigate unfavorable investor perceptions.

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
