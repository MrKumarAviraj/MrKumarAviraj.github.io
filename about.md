---
layout: page
title: About
permalink: /about/
---

Some information about you!

### More Information

A place to include any other types of information that you'd like to include about yourself.

### Contact me
<style>
form {
  max-width: 500px;
}
input, textarea {
  width: 100%;
  padding: 8px;
  border-radius: 6px;
  border: 1px solid #ccc;
  margin-top: 4px;
}
button {
  padding: 10px 20px;
  border: none;
  border-radius: 6px;
  background-color: #007ACC;
  color: white;
  cursor: pointer;
}
button:hover {
  background-color: #005FA3;
}
</style>

<h2>Contact Me</h2>
<form action="https://formspree.io/f/mnnvlgzq" method="POST">
  <label>
    Your Name:<br>
    <input type="text" name="name" required>
  </label><br><br>

  <label>
    Your Email:<br>
    <input type="email" name="email" required>
  </label><br><br>

  <label>
    Your Message:<br>
    <textarea name="message" rows="5" required></textarea>
  </label><br><br>

  <button type="submit">Send Message</button>
</form>


