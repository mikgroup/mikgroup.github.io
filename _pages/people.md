---
layout: page
horizontal: true
title: people
permalink: /people/
nav: true
nav_order: 5
display_categories: [Principle Investigator, Graduate Students, Postdocs, Undergraduate Students]
---

<!-- pages/projects.md -->
<div class="people">
{% if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  {% for category in page.display_categories %}
  <!-- <a id="{{ category }}" href=".#{{ category }}"> -->
    <h2 class="category">{{ category }}</h2>
  <!-- </a> -->
  {% assign categorized_people = site.people| where: "category", category %}
  {% assign sorted_people = categorized_people | sort: "importance" %}
  <!-- Generate cards for each project -->
  {% if page.horizontal %}
  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for people in sorted_people %}
      {% include people_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for people in sorted_people %}
      {% include people.liquid %}
    {% endfor %}
  </div>
  {% endif %}
  {% endfor %}

{% else %}


  <!-- Generate cards for each project -->

{% if page.horizontal %}

  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for people in sorted_people %}
      {% include people_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for people in sorted_people %}
      {% include people.liquid %}
    {% endfor %}
  </div>
  {% endif %}
{% endif %}
</div>

## Alumni
- Mark Murphy (Ph.D. student with [Kurt Keutzer](https://www2.eecs.berkeley.edu/Faculty/Homepages/keutzer.html), now at GoogleX)
- Sana Vaziri (Undergraduate)
- Dara Bahri (Undergraduate)
- Peter Shin (Ph.D. student)
- [Martin Uecker](https://www.tugraz.at/institute/ibi/home) (Research Associate, now faculty at TU Graz, Austria)
- Mariya Doneva (Research Associate, now at Philips Research, Germany)
- Alina Paechacek (M.S. student)
- Harrison Wang (Undergraduate)
- Harrison Rosenber (Undergraduate)
- Wenwen Jiang (Ph.D. student with [Peder Larson](https://profiles.ucsf.edu/peder.larson), now at Meta)
- Teresa Ou (M.S. student with [Laura Waller](https://www2.eecs.berkeley.edu/Faculty/Homepages/waller.html))
- Siddharth Srinivasan (Undergraduate)
- Joe Corea (Ph.D. student with [Ana Claudia Arias](https://www2.eecs.berkeley.edu/Faculty/Homepages/acarias.html), now at InkSpace Imaging)
- Balthazar Lechene (Ph.D. student primarily with [Ana Claudia Arias](https://www2.eecs.berkeley.edu/Faculty/Homepages/acarias.html), now at InkSpace Imaging)
- Patrick Virtue (Ph.D. student with [Stella Yu](https://midas.umich.edu/directory/stella-yu//), now faculty at Carnegie Mellon University)
- Frank Ong (Ph.D. student, now at Roblox)
- Tao Zhang (Ph.D. student at Stanford University with [John Pauly](https://profiles.stanford.edu/john-pauly) and [Shreyas Vasanawala](https://profiles.stanford.edu/shreyas-vasanawala), now at Apple)
- Arda Sahiner (Undergraduate)
- Zach Stillman (Undergraduate)
- Joseph Cheng (Researcher at Stanford, now at Apple)
- Rahul Tewari (Undergraduate)
- [Jon Tamir](https://users.ece.utexas.edu/~jtamir/) (Ph.D. student, now faculty at UT Austin)
- Volkert Roeloffs (Postdoctoral Researcher, now at Neoscan Solutions GmbH)
- [Zhiyong Zhang](https://bme.sjtu.edu.cn/En/FacultyDetail/615) (Postdoctoral Researcher, now faculty at Shanghai Jiao Tong University, China)
- Michael Kellman (Ph.D. student with [Laura Waller](https://www2.eecs.berkeley.edu/Faculty/Homepages/waller.html), now at Zendar)
- Jacob Sleczkowski (Undergraduate)
- Sukrit Arora (M.S. student)
- Celine Veys (M.S. student)
- Rafael Calleja (M.S. student)
- Maxwell Lin-He (M.S. student)
- Alison Hammerschmidt (Undergraduate)
- Max Litster (Undergraduate)
- Jim Tropp (Research Associate)
- Anita Flynn (Research Associate)
- Han Qi (Undergraduate)
- Han Cui (M.S. student)
- Daniel Abraham (Undergraduate)
- Jordan Grelling (M.S. student)
- Darren Hsu (M.S. student)
- Ke Wang (Ph.D. student with [Stella Yu](https://midas.umich.edu/directory/stella-yu//), now at Adobe)
- Alan Dong (Ph.D. student, now at Apple)
- Katie Lamar (M.S. student)
- Gavin Zhang (Undergraduate)
- Amanda McGraw (M.Des. student)
- Cindy Tung (Undergraduate)
- [Efrat Shimron](https://www.efratshimron.com/) (Postdoctoral Researcher, now faculty at Technion - Israel Institute of Technology)
- Fred Wang (M.S. student)
- Ana Cismaru (M.S. student)
- Robert Peltekov (M.S. student)
- Suma Anand (Ph.D. student)
