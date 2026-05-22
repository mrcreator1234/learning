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
  {% comment %}Get all pages in the learning folder{% endcomment %}
  {% for page in site.pages %}
    {% if page.dir == "/learning/" and page.name != "index.md" and page.extname == ".html" %}
      
      <a href="{{ page.name }}" class="btn-link">
        {% if page.title %}
          {{ page.title }}
        {% else %}
          📝 {{ page.basename | replace: "_", " " | replace: "-", " " }}
        {% endif %}
      </a>
      
    {% endif %}
  {% endfor %}
</div>
