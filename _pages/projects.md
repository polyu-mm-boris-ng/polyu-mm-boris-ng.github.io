---
layout: page
permalink: /projects/
title: Projects
nav: true
description: My research projects
nav_order: 0
display_categories: [My Research Projects]
horizontal: false
---

Artificial intelligence (AI) is an unlimited tool that transforms the way of data collection, data analysis, and decision-making in financial services. Deep learning combined with natural language processing (NLP) techniques enables promising automatic and real-time information processing that supports financial technology (FinTech). However, the uprising of AI also opens a new avenue for cyberterrorists to craft fake and misleading news with high perceived trustworthiness to promote false sites and clickbait. Therefore, it is crucial to safeguard clean information pathways and regulate suspicious accounts on online platforms and social media to manage content quality and strengthen personal protection. In the meantime, text mining methods enable researchers and practitioners to leverage social media data in analyzing important FinTech-related problems, such as AI and Big Data workforce dynamics and decentralized finance (DeFi) platform development. Advanced machine learning also facilitates the holistic adoption and implementation of regulatory technology (RegTech) and legal technology (LegalTech). Lastly, cybersecurity remains one of the big challenges for FinTech. It is of great interest to study how to enhance individuals’ cybersecurity awareness and motivate them to take action against cybersecurity threats.

In brief, I work on three interrelated research areas at the interface of AI and business. I will elaborate further on my research projects in these areas in the following.


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