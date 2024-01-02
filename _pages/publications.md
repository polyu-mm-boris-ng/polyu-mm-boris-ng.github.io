---
layout: page
permalink: /publications/
title: Publications
description: 
sections:
  - bibquery: "@article"
    text: "Journal Publications"
  - bibquery: "@inproceedings"
    text: "Conference Papers"
nav: false
nav_order: 1
display_categories: [Journal Publications, Conference Papers, Conference Presentations, Research in Progress, Working Papers, Works In Progress]
years: [2023, 2022, 2021, 2020, 2019]
horizontal: false
---

<div class="publications">
{%- for section in page.sections %}
  <a id="{{section.text}}"></a>
  <h2 class="bibtitle">{{section.text}}</h2>
  {%- for y in page.years %}

    {%- comment -%}  Count bibliography in actual section and year {%- endcomment -%}
    {%- capture citecount -%}
    {%- bibliography_count -f {{site.scholar.bibliography}} -q {{section.bibquery}}[year={{y}}] -%}
    {%- endcapture -%}

    {%- comment -%} If exist bibliography in actual section and year, print {%- endcomment -%}
    {%- if citecount !="0" %}

      <h2 class="year">{{y}}</h2>
      {% bibliography -f {{site.scholar.bibliography}} -q {{section.bibquery}}[year={{y}}] %}

    {%- endif -%}

  {%- endfor %}

{%- endfor %}

<!--</div>



<div class="projects">
{%- if site.enable_project_categories and page.display_categories %}-->

<!--pages/projects.md-->

  <!-- Display categorized projects -->
<!--<h2 class="bibtitle">{{ page.display_categories[0]}}</h2>

<p style="padding-left: 0.5em; text-indent: -0.5em;">• <a href="https://onlinelibrary.wiley.com/doi/abs/10.1111/poms.13959">Augmenting Fake Content Detection in Online Platforms: A Domain Adaptive Transfer Learning via Adversarial Training Approach</a><br>
<u>Ka Chung Ng</u>, Ping Fan Ke, Mike K. P. So, and Kar Yan Tam<br>
<i>Production and Operations Management.</i> Forthcoming.<br><br>
<strong>[Github]</strong> <a href="https://github.com/polyu-mm-boris-ng/Adversarial-Domain-Adaptation-for-Fake-Content">Adversarial Domain Adaptation for Fake Content</a></p>
<br>

<p style="padding-left: 0.5em; text-indent: -0.5em;">•	<a href="https://www.tandfonline.com/doi/full/10.1080/07421222.2021.1990612">The Effect of Platform Intervention Policies on Fake News Dissemination and Survival: An Empirical Examination</a><br>
<u>Ka Chung Ng</u>, Tang Jie, and Dongwon Lee<br>
<i>Journal of Management Information Systems.</i> 2021. <br><br>
<strong>Media Coverage: </strong>
<a href="https://dbr.donga.com/article/view/1202/article_no/10562/ac/magazine">Dong-A Business Review</a> (Sep 2022, Issue 1, No. 352),
<a href="https://www.donga.com/news/Economy/article/all/20220913/115435247/1">Dong-A ILBO</a> (Sep 14, 2022)</p>
<br>

<p style="padding-left: 0.5em; text-indent: -0.5em;">•	<a href="https://www.tandfonline.com/doi/full/10.1080/07421222.2021.1962601">Protecting Against Threats to Information Security: An Attitudinal Ambivalence Perspective</a><br>
<u>Ka Chung Ng</u>, Xiaojun Zhang, James Y. L. Thong, and Kar Yan Tam<br>
<i>Journal of Management Information Systems.</i> 2021.</p>
<br>
<p style="padding-left: 0.5em; text-indent: -0.5em;">•	<a href="https://dl.acm.org/doi/10.1145/3424240">A Latent Space Modeling Approach to Interfirm Relationship Analysis</a><br>
<u>Ka Chung Ng</u>, Mike K. P. So, and Kar Yan Tam<br>
<i>ACM Transactions on Management Information Systems.</i> 2021.</p>



<h2 class="bibtitle">{{ page.display_categories[1]}}</h2>

<p style="padding-left: 0.5em; text-indent: -0.5em;">•	<a href="https://aisel.aisnet.org/icis2022/blockchain/blockchain/12">Bank Error in Whose Favor? A Case Study of Decentralized Finance Misgovernance</a><br>
Ping Fan Ke and <u>Ka Chung Ng</u><br>
<i>ICIS 2022 Proceedings.</i> 2022.</p>
<br>

<p style="padding-left: 0.5em; text-indent: -0.5em;">•	<a href="https://aisel.aisnet.org/icis2020/social_media/social_media/3">Online Media Causes Biased Stock Investment: Evidence from a Regression-Discontinuity Design</a><br>
Jiali Zhou and <u>Ka Chung Ng</u><br>
<i>ICIS 2020 Proceedings.</i> 2020.</p>
<br>

<p style="padding-left: 0.5em; text-indent: -0.5em;">•	<a href="https://aisel.aisnet.org/icis2019/crowds_social/crowds_social/13">Reposts Influencing the Effectiveness of Social Reporting System: An Empirical Study from Sina Weibo</a><br>
Tang Jie and <u>Ka Chung Ng</u><br>
<i>ICIS 2019 Proceedings.</i> 2019.</p>-->



<h2 class="bibtitle">{{ page.display_categories[2]}}</h2>
<h2 class="year">{{page.years[1]}}</h2>
<p style="padding-left: 0.5em; text-indent: -0.5em;">•	A Hybrid Human-AI Approach to Capturing Disclosure Sentiment<br>
<a href="https://polyu-mm-boris-ng.github.io/"><u>Ka Chung Ng</u></a>, Jiexin Zheng, and Rong Zheng <br>
<i>The 32nd Workshop on Information Technologies and Systems (WITS).</i> 2022.</p>

<h2 class="year">{{page.years[2]}}</h2>
<p style="padding-left: 0.5em; text-indent: -0.5em;">•	Applying Domain Adaptive Transfer Learning in Fake Financial News Analysis<br>
<a href="https://polyu-mm-boris-ng.github.io/"><u>Ka Chung Ng</u></a>, Ping Fan Ke, Mike K. P. So, and Kar Yan Tam<br>
<i>The 2021 NSFC-HKUST FinTech Symposium.</i> 2021.</p>

<h2 class="year">{{page.years[3]}}</h2>
<p style="padding-left: 0.5em; text-indent: -0.5em;">•	Distillation of News Deception into Textual Analysis Using Domain Adaptation Learning<br>
<a href="https://polyu-mm-boris-ng.github.io/"><u>Ka Chung Ng</u></a>, Ping Fan Ke, and Kar Yan Tam<br>
<i>The INFORMS 2020 Annual Meeting.</i> 2020.</p>

<p style="padding-left: 0.5em; text-indent: -0.5em;">•	Inferring Deceptive Cues in Financial News: An Application of Domain Adaptation Learning<br>
<a href="https://polyu-mm-boris-ng.github.io/"><u>Ka Chung Ng</u></a>, Ping Fan Ke, Mike K. P. So, and Kar Yan Tam<br>
<i>2020 Pre-AMCIS SIGBPS Workshop on Blockchain and Financial Analytics.</i> 2020.</p>

<p style="padding-left: 0.5em; text-indent: -0.5em;">•	Will Fake News Survive Platform Intervention? Examining the Impact of Forwarding Restriction on Fake News Survival <br>
<a href="https://polyu-mm-boris-ng.github.io/"><u>Ka Chung Ng</u></a>, Tang Jie, and Dongwon Lee<br>
<i>The 6th Symposium on Statistical Challenges in Electronic Commerce Research (SCECR).</i> 2020.</p>

<h2 class="year">{{page.years[4]}}</h2>
<p style="padding-left: 0.5em; text-indent: -0.5em;">•	Financial News Credibility Measurement and Analysis <br>
<a href="https://polyu-mm-boris-ng.github.io/"><u>Ka Chung Ng</u></a>, Ping Fan Ke, Mike K. P. So, and Kar Yan Tam<br>
<i>The 11th International Association for Statistical Computing (IASC-ARS) 2019 Conference.</i> 2019.</p>

<p style="padding-left: 0.5em; text-indent: -0.5em;">•	Interfirm Relationship Analysis for Dynamic and Dual-View Company Networks: A Latent Space Modeling Approach<br>
<a href="https://polyu-mm-boris-ng.github.io/"><u>Ka Chung Ng</u></a>, Mike K. P. So, and Kar Yan Tam<br>
<i>The 3rd International Conference on Econometrics and Statistics (EcoSta).</i> 2019.</p>


<!--<br>

<div class="projects">

<h2 class="bibtitle">{{ page.display_categories[3]}}</h2>
<br>
<h2 class="category">{{ page.display_categories[6]}}</h2>
<strong>Working Papers</strong><br><br>
<p style="padding-left: 0.5em; text-indent: -0.5em;">•	Analyzing Word Sentiment Evolution in Financial Text: A Word Embedding Approach <br>
w/ Jiexin Zheng, Rong Zheng, and Kar Yan Tam<br>
<i>Journal of Management Information Systems.</i> Under 2nd Round Review.</p>
<br>

<p style="padding-left: 0.5em; text-indent: -0.5em;">•	Market Reactions to Fake Financial News: Perspectives of Humans, Machines, and Regulators <br>
w/ Ping Fan Ke, Mike K. P. So, and Kar Yan Tam<br>
<i>Information Systems Research.</i> Under 1st Round Review.</p>
<br>

<p style="padding-left: 0.5em; text-indent: -0.5em;">•	A Man with a Machine: Human-AI Augmentation for Sentiment Extraction from Firm Disclosure <br>
w/ Jiexin Zheng and Rong Zheng<br>
<i>Management Science.</i> Under 1st Round Major Revision.</p>-->

<!--<br><br>
<h2 class="category">{{ page.display_categories[5]}}</h2>
<p style="padding-left: 0.5em; text-indent: -0.5em;">•	Robo-Advisor, Financial Inclusion, and Human-Robo Interaction<br>
w/ Weiyin Hong and Kar Yan Tam</p>
<br>

<p style="padding-left: 0.5em; text-indent: -0.5em;">•	Direct and Spillover Effects of Exploits on DeFi Platform Development<br>
w/ Ping Fan Ke and Dongwon Lee</p>
<br>

<p style="padding-left: 0.5em; text-indent: -0.5em;">•	Effect of Referral Marketing on Post-Campaign Consumption<br>
w/ Yue Feng and Kit Kwan Mak</p>
<br>

<p style="padding-left: 0.5em; text-indent: -0.5em;">•	LinkedIn FinTech Talent Analysis<br>
w/ Mike K. P. So and Kar Yan Tam</p>
<br>

<p style="padding-left: 0.5em; text-indent: -0.5em;">•	Strategic Behaviors, Financial News, and Market Reaction<br>
w/ Kar Yan Tam and Cui Jie</p>-->

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






