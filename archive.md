---
layout: page
title: Archive
permalink: /archive/
---

<div class="archive">
  {% for post in site.posts %}
    {% assign current_date = post.date | date: "%Y" %}
    {% if current_date != date %}
      {% unless forloop.first %}</ul>{% endunless %}
      <h2 id="{{ current_date }}">{{ current_date }}</h2>
      <ul>
      {% assign date = current_date %}
    {% endif %}
    <li>
      <span class="post-date">{{ post.date | date: "%m-%d" }}</span>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </li>
    {% if forloop.last %}</ul>{% endif %}
  {% endfor %}
</div>