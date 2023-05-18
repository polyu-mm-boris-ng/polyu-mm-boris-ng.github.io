---
layout: page
permalink: /students/
title: Students
description: 
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

<strong>Research Postgraduate Programme</strong><br>
<p style="padding-left: 0.5em; text-indent: -0.5em;">• <a href="https://zhe-wang0018.github.io/">Zhe Wang</a> <br>
MPhil - Ph.D. Student in Management Information Systems<br>
<i>Supervisor.</i> 2023 – Present</p>
<br>

<strong>Taught Postgraduate Programme</strong><br>
<p style="padding-left: 0.5em; text-indent: -0.5em;">• Kit Kwan Mak<br>
MSc in Business Analytics<br>
<i>Co-supervisor</i> w/ Yue Feng. 2022 – 2023<br>
<strong>Dissertation:</strong> The Effect of Contract-based Referral on Post-Campaign Consumption: Empirical Evidence from a Chinese Social Commerce Platform</p>


<p style="padding-left: 0.5em; text-indent: -0.5em;">• Xiaoxiu Fu<br>
MSc in Business Analytics<br>
<i>Supervisor.</i> 2022 – Present<br>
<strong>Dissertation:</strong> The Impact of Fake News Engagement on Digital Well-Being During the Pandemic: A Text Analytics Approach</p>
<br>

<strong>Undergraduate Research and Innovation Scheme (URIS)</strong><br>
<p style="padding-left: 0.5em; text-indent: -0.5em;">• Yifeng Wang and Haoxin Wang<br>
<i>Supervisor.</i> 2022 – 2023<br>
<strong>Project Title:</strong> Adversarial Attacks on Financial Sentiment Analysis</p>

<p style="padding-left: 0.5em; text-indent: -0.5em;">• Zhinan Zhang, Yichi Zhang, and Xiaoyu Chen<br>
<i>Supervisor.</i> 2022 – 2023<br>
<strong>Project Title:</strong> It Is Money 2.0: A Machine-learning Approach to Predicting Cryptocurrency Price Using Social Media Data</p>

<p style="padding-left: 0.5em; text-indent: -0.5em;">• Jiayun Pei, Wenhao Li, and Qiuhao Xie<br>
<i>Supervisor.</i> 2022 – 2023<br>
<strong>Project Title:</strong> Promoting Green and Socially Responsible Investments in Robo-Advisors: A Natural Language Processing Approach</p>

<p style="padding-left: 0.5em; text-indent: -0.5em;">• Yaming Jin, Yingkai Hua, Kefan Wu, and Zitong Yue<br>
<i>Supervisor.</i> 2022 – 2023<br>
<strong>Project Title:</strong> Understanding the Role of Image and Language in Fake Marketing Information on Consumer Behavior</p>
