---
layout: page
title: Projects
permalink: /projects/
---

<style>
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

<div class="project-grid">

  <a class="project-card" href="/project1-details">
    <img src="https://via.placeholder.com/400x180?text=Project+1" alt="Project 1">
    <h3>Smart Light Control with ESP32</h3>
  </a>

  <a class="project-card" href="/project2-details">
    <img src="https://via.placeholder.com/400x180?text=Project+2" alt="Project 2">
    <h3>AI Quiz Bot for Students</h3>
  </a>

  <!-- Add more projects below by duplicating the block above -->

</div>

