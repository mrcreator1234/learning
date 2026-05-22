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
  {% assign pages_sorted = site.pages | sort: "title" %}
  {% for page in pages_sorted %}
    {% if page.path contains ".html" and page.name != "index.html" and page.layout != "default" %}
      <a href="{{ page.url }}" class="btn-link">
        📝 {{ page.title }}
      </a>
    {% endif %}
  {% endfor %}
</div>
