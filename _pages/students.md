---
layout: page
permalink: /students/
title: Students
description: Students under supervison
nav: false
nav_order: 2
display_categories: [Research Team, Research Supervison]
horizontal: false
---

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

<strong>Research Postgraduate Programme</strong><br><br>
• <a href="https://zhe-wang0018.github.io/">Zhe Wang</a> <br>
&nbsp; MPhil - Ph.D. Student in Management Information Systems<br>
&nbsp; <i>Supervisor.</i> 2023 – Present

<strong>Taught Postgraduate Programme</strong><br><br>
• Kit Kwan Mak<br>
&nbsp; MSc in Business Analytics<br>
&nbsp; <i>Co-supervisor</i> w/ Yue Feng. 2022 – 2023<br>
&nbsp; Dissertation: <br>
• The Effect of Contract-based Referral on Post-Campaign Consumption: Empirical Evidence from a Chinese &nbsp; Social Commerce Platform

• Xiaoxiu Fu<br>
&nbsp; MSc in Business Analytics<br>
&nbsp; <i>Supervisor.</i> 2022 – Present<br>

<strong>Undergraduate Research and Innovation Scheme (URIS)</strong><br><br>
• Yifeng Wang and Haoxin Wang<br>
&nbsp; <i>Supervisor.</i> 2022 – 2023<br>
&nbsp; Project Title: <br>
• Adversarial Attacks on Financial Sentiment Analysis

• Zhinan Zhang, Yichi Zhang, and Xiaoyu Chen<br>
&nbsp; <i>Supervisor.</i> 2022 – 2023<br>
&nbsp; Project Title: <br>
• It Is Money 2.0: A Machine-learning Approach to Predicting Cryptocurrency Price Using Social Media Data

• Jiayun Pei, Wenhao Li, and Qiuhao Xie<br>
&nbsp; <i>Supervisor.</i> 2022 – 2023<br>
&nbsp; Project Title: <br>
• Promoting Green and Socially Responsible Investments in Robo-Advisors: A Natural Language Processing Approach

• Yaming Jin, Yingkai Hua, Kefan Wu, and Zitong Yue<br>
&nbsp; <i>Supervisor.</i> 2022 – 2023<br>
&nbsp; Project Title: <br>
• Understanding the Role of Image and Language in Fake Marketing Information on Consumer Behavior
