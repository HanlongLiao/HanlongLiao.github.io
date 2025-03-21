---
layout: page
title: Categories
permalink: /categories/
---

<div class="categories">
  {% for category in site.categories %}
    <div class="category">
      <h2 id="{{ category[0] }}">{{ category[0] }}</h2>
      <ul>
        {% for post in category[1] %}
          <li>
            <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
            <small>{{ post.date | date: "%Y-%m-%d" }}</small>
          </li>
        {% endfor %}
      </ul>
    </div>
  {% endfor %}
</div>