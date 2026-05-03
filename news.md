---
title: News
layout: page
---

## News Archive

<ul class="academic-home__news">
  {% for item in site.data.news %}
    <li><span>{{ item.date_label }}</span>{{ item.text | markdownify | remove: '<p>' | remove: '</p>' }}</li>
  {% endfor %}
</ul>
