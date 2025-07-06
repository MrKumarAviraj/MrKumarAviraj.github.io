---
layout: page
title: Tech News
permalink: /tech-news/
---

<h2>📰 Tech News Articles</h2>

<ul class="post-list">
  {% assign tech_posts = site.posts | where: "category", "Tech News" %}
  {% for post in tech_posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
      <span> — {{ post.date | date: "%B %d, %Y" }}</span>
    </li>
  {% endfor %}
</ul>
