---
layout: page
permalink: /service/
title: Service
description: My academic service
nav: false
nav_order: 2
display_categories: [Services to the University/Community, Ad Hoc Reviewer]
horizontal: false
---

<!-- pages/projects.md -->
<div class="projects">
{%- if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  <h2 class="category">{{ page.display_categories[0]}}</h2>
• Associate Editor, <i>Pacific Asia Conference on Information Systems (PACIS)</i> <float style="display:inline-block; float:right;">2023</float><br>
• Coordinator, <i>Management Information Systems Speaker Series</i> <float style="display:inline-block; float:right;">2023</float><br>
• Panel Member, <i>NON-JEE Interviews</i> <float style="display:inline-block; float:right;">2023</float><br>
• Committee Member, <i>International Conference on Information Systems (ICIS)</i> <float style="display:inline-block; float:right;">2022 – 2023</float><br>
• Associate Editor, <i>International Conference on Information Systems (ICIS)</i> <float style="display:inline-block; float:right;">2022 – 2023</float><br>
• Thesis Proposal Assessment Panelist, <i>DFinTech Residential 2 2022</i> <float style="display:inline-block; float:right;">2022 – 2023</float><br>
• Panel Member, <i>MPhil Confirmation of Registration</i> <float style="display:inline-block; float:right;">2022 – 2023</float><br>
• Supervisor, <i>Marketing Capstone Project (MM4942)</i> <float style="display:inline-block; float:right;">2022 – 2023</float>


<h2 class="category">{{ page.display_categories[1]}}</h2>
<strong>Journals:</strong> <br><br>
• Management Information Systems Quarterly (MISQ)<br>• Information Systems Research (ISR)<br>• Journal of Management Information Systems (JMIS)<br> • Information and Management (I&M)<br>• International Journal of Information Management (IJIM)<br>• International Journal of Electronic Commerce (IJEC)<br> • Journal of Electronic Commerce Research (JECR)<br><br>
<strong>Conferences:</strong> <br><br>
• Pacific Asia Conference on Information Systems (PACIS)<br>• International Conference on Information Systems (ICIS)<br>• China Summer Workshop on Information Management (CSWIM)<br>• Workshop on Information Technologies and Systems (WITS)<br>• Wuhan International Conference on E-business (WHICEB)

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




