---
layout: page
permalink: /teaching/
title: Teaching
description: Teaching Interests:Management Information Systems, AI Applications in Business, Machine Learning, Text Mining, Business Applications Programming (e.g., Python, R, Java, VBA)
nav: true
nav_order: 2
display_categories: [PolyU, HKUST]
horizontal: false
---

Besides being an enthusiastic and methodical researcher, I enjoy teaching and mentoring students, which I perceive as essential for my academic career. Responding to the fast-growing technological development and the challenge of the digital transformation faced by the university, I employ several teaching methods to help undergraduate and graduate students learn efficiently and meaningfully with three associated goals: (1) a thorough understanding of what they learned, (2) enthusiasm for the subject, and (3) strategic communication. 

I apply aptitude-based teaching and learning-by-doing approaches to achieve the first teaching goal. To raise students’ enthusiasm for what they learned, I deliver pioneer knowledge and motivate their curiosity to explore new information about the subjects they learned. Lastly, strategic communication means that students can communicate well with different audiences (e.g., professionals or laypersons) and under various circumstances (e.g., business talk or coffee break), which can be achieved by efficiently reformulating knowledge and ideas. I help students achieve this goal by ensuring a highly interactive study environment through knowledge sharing, group discussions, and in-class presentations. In sum, I assume these responsibilities with great passion and commitment, and I believe my personal experience and academic background will pave the way for achieving my teaching philosophy. 

I have a lot of teaching experience in business analytics and information systems. I can teach business analytics, text mining, machine learning, and information systems-related courses. Besides, I can teach technical courses such as business programming in Java/R/Python, database management, and deep learning implementations.



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

