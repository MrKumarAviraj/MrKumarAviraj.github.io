---
layout: page
title: Home
permalink: /
---


<style>
.banner-img {
  width: 100%;
  border-radius: 6px;
  margin-bottom: 10px;
}

.section-title {
  font-size: 24px;
  margin-top: 40px;
  margin-bottom: 10px;
  border-bottom: 2px solid #ccc;
  padding-bottom: 5px;
}

.blog-list li {
  margin-bottom: 10px;
}

.project-grid {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
  justify-content: center;
}

.project-card {
  width: 45%;
  border: 1px solid #ccc;
  border-radius: 12px;
  overflow: hidden;
  box-shadow: 2px 2px 10px rgba(0,0,0,0.1);
  text-align: center;
  text-decoration: none;
  color: inherit;
  background: #fff;
  transition: transform 0.2s ease;
}

.project-card:hover {
  transform: scale(1.02);
}

.project-card img {
  width: 100%;
  height: 180px;
  object-fit: cover;
}

.project-card h3 {
  margin: 15px 0;
  padding: 0 10px;
}
</style>

<!-- 🔹 Banner -->
<img class="banner-img" src="/images/banner.png" alt="The MakersRoom Banner">


<!-- 🔹 Latest Blogs -->
<h2 class="section-title">📝 Latest Blog Posts</h2>
<ul class="blog-list">
  {% for post in site.posts limit:3 %}
    <li><a href="{{ post.url }}">{{ post.title }}</a> — {{ post.date | date: "%b %-d, %Y" }}</li>
  {% endfor %}
</ul>

<!-- 🔹 Featured Projects -->
<h2 class="section-title">🛠️ Featured Projects</h2>

<div class="project-grid">

{% assign latest_projects = site.posts | where_exp:"post", "post.tags contains 'Project'" | slice: 0, 3 %}
{% for post in latest_projects %}
  <a class="project-card" href="{{ post.url }}">
    <img src="{{ post.image | default: '/images/default-thumb.jpg' }}" alt="{{ post.title }}">
    <h3>{{ post.title }}</h3>
  </a>
{% endfor %}

</div>

