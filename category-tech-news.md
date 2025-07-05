---
layout: page
title: Tech News
permalink: /category/tech-news/
---

<h2>📰 Tech News Articles</h2>

<ul>
  {% for post in site.posts %}
    {% if post.category == "Tech News" %}
      <li><a href="{{ post.url }}">{{ post.title }}</a> — {{ post.date | date: "%b %d, %Y" }}</li>
    {% endif %}
  {% endfor %}
</ul>
