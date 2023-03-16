---
layout: page
permalink: /teaching/
title: Teaching
description: My teaching
nav: true
nav_order: 2
display_categories: [Teaching Experience]
horizontal: false

---

<strong>Teaching Interests:</strong> Management Information Systems, AI Applications in Business, Machine Learning, Text Mining, Business Applications Programming (e.g., Python, R, Java, VBA)

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


<strong>The Hong Kong Polytechnic University</strong>

<i>Textual Analysis in Business (MM5427)</i> <br>
<strong>• Teaching period:</strong> Spring 2023 <br>
<strong>• Teaching responsibilities:</strong> Course and Lab Instructor <br>
<strong>• Class size:</strong> 19 <br>

This course covers the concepts and techniques for applying textual analytics in processing unstructured text data in the business domain. Python programming language will be the primary implementation tool for data analysis and model development. An extended lab session intends to train students with good knowledge and skills for solving practical problems, such as sentiment analysis, document classification, word embedding, and topic modeling.

<br>

<i>Business Forecasting (MM5413)</i> <br>
<strong>• Teaching period:</strong> Spring 2022, Spring 2023 <br>
<strong>• Teaching responsibilities:</strong> Course and Lab Instructor <br>
<strong>• Class size:</strong> 42 (Spring 2022), 46 (Spring 2023) <br>
<strong>• Instructor Evaluation:</strong> 4.4/5 (Spring 2022) <br>

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




