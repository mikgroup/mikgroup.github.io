---
layout: page
title: research
permalink: /research/
description:
nav: true
nav_order: 2
display_categories: [Advanced Acquisition Methods, Advanced reconstruction methods + Computational MRI, Advancements in MRI Hardware, Motion sensing and correction in MRI, Anatomy-mimicking quantitative phantoms, Wearable & Implantable Sensors within the MRI]
horizontal: false
---
<!-- pages/projects.md -->
<div class="projects">
{% if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  {% for category in page.display_categories %}
  <a id="{{ category }}" href=".#{{ category }}">
    <h2 class="category">{{ category }}</h2>
  </a>
  {% assign categorized_projects = site.projects | where: "category", category %}
  {% assign sorted_projects = categorized_projects | sort: "importance" %}
  <!-- Generate cards for each project -->
  {% if page.horizontal %}
  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_projects %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endif %}
  {% endfor %}

{% else %}

<!-- Display projects without categories -->

{% assign sorted_projects = site.projects | sort: "importance" %}

  <!-- Generate cards for each project -->

{% if page.horizontal %}

  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_projects %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endif %}
{% endif %}
</div>



### Lecture videos
- NIBIB New Horizon Lecture, ["When Fast is not Fast Enough: The Challenging Path Towards Pediatric MRI Without Anesthesia](https://www.ismrm.org/18/plenaryvideos/04-Tuesday/), ISMRM 2018
- New Horizons Workshop, EPFL, [“Current Status and Future Horizon in (Pediatric) MRI”](https://www.youtube.com/watch?v=bd0PJ1qDwuE), 2021
- International Workshop‚ MR yesterday, today, and tomorrow, [“The Never Ending Adventures in Computational MRI”](https://www.youtube.com/watch?v=4Yha1Lc0oDo&feature=youtu.be), 2022
- IPAM Multi-Modal Imaging Workshop, [“Multi-Modal Imaging using Microwave Tones in an MRI Scanner”](https://www.youtube.com/watch?v=bx66hVdqlg0), 2022
