---
layout: page
title: Blog
permalink: /blog/
---

<h1>📝 Blog Posts</h1>

<!-- 🔖 Tag Cloud -->
<h3>🏷️ Browse by Tag</h3>
<ul class="tag-cloud">
  {% for tag in site.tags %}
    <li style="display:inline-block; margin: 4px 8px;">
      <a href="{{ site.baseurl }}/tag/{{ tag[0] | slugify }}/">{{ tag[0] }} ({{ tag[1].size }})</a>
    </li>
  {% endfor %}
</ul>

<hr>

<!-- 📚 List of Blog Posts -->
<ul class="post-list">
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
      <span> — {{ post.date | date: "%B %d, %Y" }}</span>
    </li>
  {% endfor %}
</ul>
