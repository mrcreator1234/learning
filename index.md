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
      
      <a href="{{ file.name }}" class="btn-link">
        {% assign title = file.basename | replace: "_", " " | replace: "-", " " %}
        📝 {{ title }}
      </a>
      
    {% endif %}
  {% endfor %}
</div>
