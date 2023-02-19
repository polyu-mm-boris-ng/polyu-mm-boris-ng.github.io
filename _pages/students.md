---
layout: page
permalink: /students/
title: Students
description: Students under supervison
nav: false
nav_order: 2
display_categories: [Research Team, Reserch Supervison]
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
Ph.D. Student in Management Information Systems<br>
<i>Supervisor.</i> 2023 – Present

<strong>Taught Postgraduate Programme</strong><br><br>
• Kit Kwan Mak<br>
MSc in Business Analytics<br>
<i>Co-supervisor</i> w/ Yue Feng. 2022 – 2023<br>
Dissertation: <br>
• The Effect of Contract-based Referral on Post-Campaign Consumption: Empirical Evidence from a Chinese Social Commerce Platform

• Xiaoxiu Fu<br>
MSc in Business Analytics<br>
<i>Supervisor.</i> 2022 – Present<br>

<strong>Undergraduate Research and Innovation Scheme (URIS)</strong><br><br>
• Yifeng Wang and Haoxin Wang<br>
Project Title: Adversarial Attacks on Financial Sentiment Analysis<br>
<i>Supervisor.</i> 2022 – 2023

• Zhinan Zhang, Yichi Zhang, and Xiaoyu Chen<br>
Project Title: It Is Money 2.0: A Machine-learning Approach to Predicting Cryptocurrency Price Using Social Media Data<br>
<i>Supervisor.</i> 2022 – 2023

• Jiayun Pei, Wenhao Li, and Qiuhao Xie<br>
Project Title: Promoting Green and Socially Responsible Investments in Robo-Advisors: A Natural Language Processing Approach<br>
<i>Supervisor.</i> 2022 – 2023

• Yaming Jin, Yingkai Hua, Kefan Wu, and Zitong Yue<br>
Project Title: Understanding the Role of Image and Language in Fake Marketing Information on Consumer Behavior<br>
<i>Supervisor.</i> 2022 – 2023
