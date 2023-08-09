---
layout: page
permalink: /teaching/
title: Teaching
description: 
nav: true
nav_order: 2
display_categories: [Teaching Experience]
horizontal: false

---

<strong>Teaching Interests:</strong> Management Information Systems, AI Applications in Business, Machine Learning, Text Mining, Business Applications Programming (e.g., Python, R, Java, VBA)

As a passionate and meticulous researcher, I find immense satisfaction in teaching and mentoring students, considering these roles integral to my academic career. In response to the rapid technological advancements and the digital transformation challenges confronting academia, I have adopted a variety of teaching methods. These methods are designed to support undergraduate and graduate students in their learning journeys, with a focus on three key objectives: (1) gaining a deep comprehension of the content, (2) developing a genuine interest in the subject matter, and (3) mastering strategic communication skills.

To ensure a profound understanding of the subject, I employ an ability-based teaching approach combined with experiential learning strategies. To foster enthusiasm, I introduce cutting-edge knowledge and stimulate curiosity, encouraging students to delve deeper into the subjects they are studying. Effective communication is critical in this context; it involves the ability to articulate concepts to diverse audiences (professionals, novices), and in various settings (formal business discussions or casual coffee chat). This can be achieved by skilfully reframing knowledge and ideas, an aspect I promote by facilitating interactive learning environments through knowledge exchange, group dialogues, and classroom presentations. I undertake these responsibilities with immense dedication and great enthusiasm, confident that my personal experiences and academic qualifications will contribute to the realization of my teaching philosophy.

My teaching portfolio is extensive, primarily in the fields of business analytics and information systems. I am equipped to teach a range of subjects that include business analytics, text mining, and machine learning, along with courses related to information systems. Further, my technical proficiency enables me to guide students through technical courses like business programming in Java/R/Python, database management, and the implementation of deep learning.



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


<strong>The Hong Kong Polytechnic University</strong>

<i>Textual Analysis in Business (MM5427)</i> <br>
<strong>• Teaching period:</strong> Spring 2023 <br>
<strong>• Teaching responsibilities:</strong> Course and Lab Instructor <br>
<strong>• Class size:</strong> 19 <br>
<strong>• Instructor Evaluation:</strong> 4.5/5 <br>

This course covers the concepts and techniques for applying textual analytics in processing unstructured text data in the business domain. Python programming language will be the primary implementation tool for data analysis and model development. An extended lab session intends to train students with good knowledge and skills for solving practical problems, such as sentiment analysis, document classification, word embedding, and topic modeling.

<br>

<i>Business Forecasting (MM5413)</i> <br>
<strong>• Teaching period:</strong> Spring 2022, Spring 2023 <br>
<strong>• Teaching responsibilities:</strong> Course and Lab Instructor <br>
<strong>• Class size:</strong> 42 (Spring 2022), 46 (Spring 2023) <br>
<strong>• Instructor Evaluation:</strong> 4.4/5 (Spring 2022), 4.2/5 (Spring 2023) <br>

This course is developed to introduce both conventional and advanced models in business forecasting, with a specific focus on the application of deep learning. This course includes lectures (×10) and lab sessions (×4) intended to train students with good knowledge and skills to solve practical problems. Python programming language will be the primary tool for data analysis and model development.

<br><br>

<strong>The Hong Kong University of Science and Technology</strong>

<i>Natural Language Processing in Business Using Deep Learning (ISOM4000B)</i> <br>
<strong>• Teaching period:</strong> Fall 2021 <br>
<strong>• Teaching responsibilities:</strong> Course and Lab Instructor <br>
<strong>• Class size:</strong> 18 <br>
<strong>• Instructor Evaluation:</strong> 4.8/5 <br>

This course covers the concepts and techniques for applying natural language processing and deep learning in processing text data in the business domain. Python programming language is the primary implementation tool for data analysis and model development. An extended lab session intends to train students with good knowledge and skills for solving practical problems, such as document classification, word embedding, topic modeling, and financial news analysis.

<br>

<i>Data Mining for Business Analytics (ISOM3360)</i> <br>
<strong>• Teaching period:</strong> Summer 2020 <br>
<strong>• Teaching responsibilities:</strong> Course and Lab Instructor <br>
<strong>• Class size:</strong> 21 <br>
<strong>• Instructor Evaluation:</strong> 87.5/100 <br>

This course covers the fundamental concepts, technologies, and applications of business analytics to help firms gain a competitive advantage in the era of Big Data. Topics include text mining, predictive analytics, search engine strategy, social network analysis, cloud computing, etc. Students will gain hands-on experience with popular data analytical tools.

<br>

<i>Big Data Analytics (ISOM5270)</i> <br>
<strong>• Teaching period:</strong> Fall 2019 <br>
<strong>• Teaching responsibilities:</strong> Teaching Assistant <br>
<strong>• Class size:</strong> 68 <br>

This course introduces the key concepts and applications of business analytics in the world of Big Data. Examples of business problems to be solved analytically include customer relationship management, financial trading, social media marketing, search engine strategy, etc. Hands-on experience with popular data analytical tools is included.

<br>

<i>Introduction to Information Systems (ISOM2010)</i> <br>
<strong>• Teaching period:</strong> Fall 2016 – Fall 2019 <br>
<strong>• Teaching responsibilities:</strong> Lab Instructor <br>
<strong>• Class size:</strong> ~56 <br>

This course introduces Information Systems (IS), which is about managing the applications of IT to create business values. Topics include fundamental concepts of IS, e-commerce, digital and the Internet economy, Web 2.0 and social networks, online advertising, personalization and privacy, digital rights management and piracy, business intelligence and decision-making, how organizations harness IS for innovative business strategies, and the socio-economic impact of IS on organizations and societies. The labs cover business problem-solving skills.




