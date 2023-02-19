---
layout: page
title: teaching
permalink: /teaching/
description: the knowledge that I have learned and would like to share.
nav: true
nav_order: 3
display_categories: [undergraduate, graduate, bud]
horizontal: false
---

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="https://cdn.pixabay.com/photo/2020/10/01/11/07/hands-5618240_1280.jpg" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<!-- <div class="caption">
    "The second brain is a magic kitchen for me to cook delicious foods for thoughts!" ~ I-Te Lu (the picture from <a href="https://unsplash.com/photos/DcIZJsskTfg">unsplash</a>)
</div> -->

The mateial is grouped into 1) undergraduate, 2) graduate, and 3) bud. Here "bud" with a symbol 🚧 means that the relevant course material is under construction, and that it is not complete yet but I will regularly update it.  

> 🏗️ I am still constructing the website, so I will add more...stay tuned

<!-- For now, this page is assumed to be a static description of your courses. You can convert it to a collection similar to `_projects/` so that you can have a dedicated page for each course. -->

<!-- Organize your courses by years, topics, or universities, however you like! -->

<!-- pages/projects.md -->
<div class="projects">
{%- if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  {%- for category in page.display_categories %}
  <h2 class="category">{{ category }}</h2>
  {%- assign categorized_projects = site.teaching | where: "category", category -%}
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

