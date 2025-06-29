---
layout: page
title: Projects
permalink: /projects/
---

<h2>🚀 My Projects</h2>

<div class="projects-grid">

{% assign project_posts = site.posts | where_exp:"post", "post.tags contains 'Project'" %}
{% for post in project_posts %}
  <a class="project-card" href="{{ post.url }}">
    <img src="{{ post.image | default: '/images/default-thumb.jpg' }}" alt="{{ post.title }}">
    <h3>{{ post.title }}</h3>
    <p>{{ post.description | default: post.excerpt }}</p>
  </a>
{% endfor %}

</div>


