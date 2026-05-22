---
layout: default
title: Laman Utama
---

<h1>📚 Laman Pembelajaran</h1>
<p>Selamat datang! 🌟</p>

<h2>🔗 Pautan Berguna</h2>
<a href="https://ekamus.dbp.gov.my" class="btn-link" target="_blank">📖 Kamus DBP</a>

<hr>

<h2>📂 Semua Kuiz & Latihan</h2>
<div class="file-list">
  {% for file in site.static_files %}
    {% if file.extname == ".html" and file.name != "index.html" %}
      
      <!-- Try to read front matter, fallback to filename -->
      {% assign quiz_page = site.pages | where: "path", file.path | first %}
      {% if quiz_page.title %}
        {% assign title = quiz_page.title %}
      {% else %}
        {% assign title = file.basename | replace: "_", " " | replace: "-", " " %}
      {% endif %}
      
      <a href="{{ file.path }}" class="btn-link">
        {{ title }}
      </a>
    {% endif %}
  {% endfor %}
</div>
