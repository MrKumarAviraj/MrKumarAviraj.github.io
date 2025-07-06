---
layout: page
title: Tutorials
permalink: /tutorials/
---

<h2>📘 Tutorials & Guides</h2>

<ul class="post-list">
  {% assign tutorial_posts = site.posts | where: "category", "Tutorial" %}
  {% for post in tutorial_posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
      <span> — {{ post.date | date: "%B %d, %Y" }}</span>
    </li>
  {% endfor %}
</ul>
