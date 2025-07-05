---
layout: page
title: Projects
permalink: /projects/
---

<h1>🚀 My Projects</h1>

<!-- 🔖 Project Tag Filter -->
<h3>🏷️ Browse by Tag</h3>
<ul class="tag-cloud">
  {% assign all_project_posts = site.posts | where_exp:"post", "post.tags contains 'project'" %}
  {% assign all_tags = all_project_posts | map: 'tags' | uniq | join: ',' | split: ',' | uniq %}
  {% for tag in all_tags %}
    <li style="display:inline-block; margin: 4px 8px;">
      <a href="{{ site.baseurl }}/tag/{{ tag | slugify }}/">{{ tag }}</a>
    </li>
  {% endfor %}
</ul>

<hr>

<!-- 📦 Project Cards -->
<div class="project-grid">
  {% assign project_posts = site.posts | where: "category", "Projects" %}
  {% for post in project_posts %}
    <a class="project-card" href="{{ post.url }}">
      <img src="{{ post.image }}" alt="{{ post.title }}">
      <h3>{{ post.title }}</h3>
      <p>{{ post.description }}</p>
    </a>
  {% endfor %}
</div>




