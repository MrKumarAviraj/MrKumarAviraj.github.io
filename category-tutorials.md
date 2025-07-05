---
layout: page
title: Tutorials
permalink: /category/tutorials/
---

<h2>📚 All Tutorials</h2>

<ul>
  {% for post in site.posts %}
    {% if post.category == "Tutorials" %}
      <li><a href="{{ post.url }}">{{ post.title }}</a> — {{ post.date | date: "%b %d, %Y" }}</li>
    {% endif %}
  {% endfor %}
</ul>
