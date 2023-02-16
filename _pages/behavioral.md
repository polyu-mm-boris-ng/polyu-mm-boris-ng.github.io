---
layout: page
title: Behavioral Aspects of Cybersecurity
permalink: /behavioral/
description: Overview of Behavioral Aspects of Cybersecurity
nav: false
nav_order: 2
display_categories: [work, fun]
horizontal: false
---

The uprising of FinTech is associated with a critical challenge - cybersecurity. Many security applications, such as two-factor authentication (2FA), were developed to secure online transactions and mobile payments. Such technologies always offer good security, but many users are unaware of it. For this reason, individuals’ weak and insufficient security awareness will be a big vulnerability in FinTech development. In this regard, one stream of my research examines how to enhance individuals’ cybersecurity awareness and motivate them to take action against cybersecurity threats. My studies enrich the current research on fear appeal and provide a pathway to improve its design to persuade individuals to take cybersecurity precautions.

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
