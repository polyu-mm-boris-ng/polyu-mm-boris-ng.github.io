---
layout: page
permalink: /projects/
title: Projects
nav: true
description: 
nav_order: 0
display_categories: [My Research Projects]
horizontal: false
---

Artificial Intelligence (AI) is a boundless tool that revolutionizes the way we collect, analyze data, and make decisions in financial services. The amalgamation of deep learning and natural language processing (NLP) techniques paves the way for efficient, automatic, and real-time information processing, which is vital to the evolution of financial technology (FinTech). Nonetheless, the rise of AI has also inadvertently provided cyber terrorists with a fresh avenue to craft and disseminate fake and misleading news with a high degree of perceived trustworthiness, thereby promoting false sites and clickbait. Consequently, it is critical to ensure the integrity of information pathways, regulate suspicious accounts on online platforms and social media, and strengthen personal protection measures to maintain content quality.

Simultaneously, text mining methods empower researchers and practitioners to harness social media data in analyzing essential FinTech-related issues, such as AI and Big Data workforce dynamics and the development of decentralized finance (DeFi) platforms. Advanced machine learning further facilitates the comprehensive adoption and implementation of regulatory technology (RegTech) and legal technology (LegalTech). Nevertheless, cybersecurity continues to pose significant challenges for FinTech. It is compelling to explore ways to enhance individual cybersecurity awareness and motivate proactive actions against cybersecurity threats.

In essence, my work navigates three interconnected research areas at the nexus of AI and business. I will provide a more detailed exploration of my research projects in these domains as we go along.

<strong>The images below are AI-generated based on keywords!</strong>

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