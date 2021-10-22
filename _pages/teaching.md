---
layout: page
permalink: /teaching/
title: teaching
description: Materials for courses I taught.
years: [2021,2020]
nav: true
---


<div class="teaching">
  {% for y in page.years %} 
  <h2 class="year">{{y}}</h2>
  <!-- Display classes-->
      <!-- Generate cards for each class-->
	  {% assign selected_classes = site.teaching | where: "year", y %}
          {% for teach in selected_classes %}
                    {% include class.html %}
          {% endfor %}

 {% endfor %}
</div>

	  

For now, this page is assumed to be a static description of your courses. You can convert it to a collection similar to `_projects/` so that you can have a dedicated page for each course.

Organize your courses by years, topics, or universities, however you like!
