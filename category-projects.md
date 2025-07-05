---
layout: page
title: Projects
permalink: /category/projects/
---

<h2>🧰 All Project Tutorials</h2>

<ul>
  {% for post in site.posts %}
    {% if post.category == "Projects" %}
      <li><a href="{{ post.url }}">{{ post.title }}</a> — {{ post.date | date: "%b %d, %Y" }}</li>
    {% endif %}
  {% endfor %}
</ul>
