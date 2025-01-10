---
layout: page
permalink: /projects/
title: Projects
description: 
nav: true
nav_order: 0
display_categories: [FinTech & AI, Computational Social Science]
horizontal: false

---

These two research streams converge at the intersection of AI, business studies, and social science, creating a comprehensive framework for understanding and addressing contemporary challenges. The following paragraphs detail my specific research projects within these areas.

<!-- pages/projects.md -->
<div class="projects">
{%- if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  <h2 class="category">{{ page.display_categories[0]}}</h2>
In the domain of FinTech & AI, my research examines how AI transforms financial services through advanced data collection, analysis, and decision-making processes. The integration of deep learning and natural language processing (NLP) enables efficient, automatic, and real-time information processing, which is fundamental to FinTech innovation. However, these advancements have inadvertently created opportunities for cyber threats, particularly AI-generated fake news and misleading content with heightened perceived credibility that distorts investor behavior and undermines financial market efficiency. My work investigates critical aspects of information integrity, platform governance, and security measures to maintain content quality. Besides, I develop innovative approaches to enhance cybersecurity awareness and promote proactive defense against emerging threats. Additionally, I leverage AI to analyze unstructured data, employing NLP techniques and large language models (LLMs) for corporate disclosures and financial texts, and multimodal analysis for executive interviews. This approach generates actionable insights that enhance the efficiency and decision-making capabilities of investors and regulators.

<br><br>
<strong>Related publications:</strong>

<p style="padding-left: 0.5em; text-indent: -0.5em;">• Zheng, J., <u>Ng, K. C.</u>, Zheng, R., and Tam, K. Y. 2023. <a href="">“The Effects of Sentiment Evolution in Financial Texts: A Word Embedding Approach,”</a> <i>Journal of Management Information Systems.</i> (41:1), pp. 178-205.<br></p>

<p style="padding-left: 0.5em; text-indent: -0.5em;">•   Ke, P. F., and <u>Ng, K. C.</u> 2022. <a href="https://aisel.aisnet.org/icis2022/blockchain/blockchain/12">“Bank Error in Whose Favor? A Case Study of Decentralized Finance Misgovernance,”</a> <i>ICIS 2022 Proceedings.</i> 12. <br></p>

<p style="padding-left: 0.5em; text-indent: -0.5em;">•	<u>Ng, K. C.</u>, Zhang, X., Thong, J. Y. L., and Tam, K. Y. 2021. <a href="https://www.tandfonline.com/doi/full/10.1080/07421222.2021.1962601">“Protecting Against Threats to Information Security: An Attitudinal Ambivalence Perspective,”</a> <i>Journal of Management Information Systems.</i> (38:3), pp. 732–764.<br></p>

<p style="padding-left: 0.5em; text-indent: -0.5em;">•   Zhou, J., and <u>Ng, K. C.</u> 2020. <a href="https://aisel.aisnet.org/icis2020/social_media/social_media/3">“Online Media Causes Biased Stock Investment: Evidence from a Regression-Discontinuity Design,”</a> <i>ICIS 2020 Proceedings.</i> 3. </p>


<h2 class="category">{{ page.display_categories[1]}}</h2>
In the realm of Computational Social Science, my research leverages advanced NLP methods, network analysis techniques, and machine learning models to analyze crucial societal issues through social media and online data. By employing cutting-edge deep learning techniques and LLMs, I examine complex social phenomena including fake news propagation, deepfake detection, substance abuse patterns, and digital behavioral influences. This computational approach enables systematic analysis of large-scale social data, providing insights into human behavior and social dynamics in the digital age. I also investigate the vulnerability of AI-mediated social interactions and decision-making processes to strategic manipulation. From a methodological perspective, I have developed several AI-based tools and models that advance the study of social phenomena and corporate relationships. In sum, my research in this area contributes to both theoretical understanding and practical solutions for pressing social challenges.

<br><br>
<strong>Related publications:</strong>

<p style="padding-left: 0.5em; text-indent: -0.5em;">•  Ke, P. F., and<u>Ng, K. C. </u> 2024. <a href="https://www.tandfonline.com/doi/full/10.1080/07421222.2023.2301176">Human-AI Synergy in Survey Development: Implications from Large Language Models in Business and Research</a>
<i>ACM Transactions on Management Information Systems,</i> forthcoming.</p>

<p style="padding-left: 0.5em; text-indent: -0.5em;">•   <u>Ng, K. C.</u>, Ke, P. F., So, M. K. P., and Tam, K. Y. 2023. <a href="https://onlinelibrary.wiley.com/doi/abs/10.1111/poms.13959">“Augmenting Fake Content Detection in Online Platforms: A Domain Adaptive Transfer Learning via Adversarial Training Approach,”</a> <i>Production and Operations <br>
Management.</i> (32:7), pp. 2101–2022.<br></p>

<p style="padding-left: 0.5em; text-indent: -0.5em;">•   <u>Ng, K. C.</u>, Tang, J., and Lee, D. 2021. <a href="https://www.tandfonline.com/doi/full/10.1080/07421222.2021.1990612">“The Effect of Platform Intervention Policies on Fake News Dissemination and Survival: An Empirical Examination,”</a> <i>Journal of Management Information Systems</i> (38:4), pp. 898–930.<br></p>

<p style="padding-left: 0.5em; text-indent: -0.5em;">•   Tang, J., and <u>Ng, K. C.</u> 2019. <a href="https://aisel.aisnet.org/icis2019/crowds_social/crowds_social/13">“Reposts Influencing the Effectiveness of Social Reporting System: An Empirical Study from Sina Weibo,”</a> <i>ICIS 2019 Proceedings.</i>13. </p>

<p style="padding-left: 0.5em; text-indent: -0.5em;">•   <u>Ng, K. C.</u>, So, M. K. P., and Tam, K. Y. 2021. <a href="https://dl.acm.org/doi/10.1145/3424240">“A Latent Space Modeling Approach to Interfirm Relationship Analysis,”</a> <i>ACM Transactions on Management Information Systems</i> (12:2), 10. <br></p>

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





