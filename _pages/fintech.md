---
layout: page
title: FinTech, RegTech, and LegalTech
permalink: /fintech/
description: Overview of FinTech, RegTech, and LegalTech
nav: false
nav_order: 2
display_categories: [fintech, regtech, legaltech]
horizontal: false
---

FinTech, RegTech, and LegalTech are intertwined and serve as the crucial underpinnings of the development of Hong Kong into a global financial center. My research thoroughly investigates various aspects of these three areas and makes efforts to offer implications for academia, industry, and government.

Here I will outline my current focuses and interests. Regarding the FinTech aspect, I am working on (1) understanding how DeFi hacks and exploits affect the development of DeFi platforms and (2) analyzing the FinTech talent growth using social media data with the machine learning approach. Regarding the RegTech aspect, I am working on (1) applying language style migration and speech recognition in improving e-KYC and (2) incorporating federated learning into statistical methods for better policymaking. Regarding the LegalTech aspect, I am working on developing an AI-based Chinese legal document processing tool using machine learning, NLP, and expert-crafted rules. 

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
