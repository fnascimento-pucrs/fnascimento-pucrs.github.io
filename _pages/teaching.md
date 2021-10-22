---
layout: page
permalink: /teaching/
title: teaching
description: Materials for courses I taught.
years: [2021,2020,2019]
nav: true
horizontal: true
---


<div class="teaching">

{% for y in page.years %}
  <h2 class="year">{{y}}</h2>
      {% assign selected_ones = site.teaching | where: "year", y %}
      {% if page.horizontal %}
        <div class="container">
          <div class="row row-cols-2">
          {% for teach in selected_ones %}
                    {% include teach_horizontal.html %}
          {% endfor %}
          </div>
        </div>
      {% else %}
        <div class="grid">
          {% for teach in selected_ones %}
                    {% include teach.html %}
          {% endfor %}
        </div>
      {% endif %}
{% endfor %}

</div>

<!--
For now, this page is assumed to be a static description of your courses. You can convert it to a collection similar to `_projects/` so that you can have a dedicated page for each course.

Organize your courses by years, topics, or universities, however you like!
-->
