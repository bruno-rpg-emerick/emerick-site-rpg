---
layout: default
title: Galeria de Provas
permalink: /provas/
---

<h2 class="section-header">EVIDÊNCIAS MATERIAIS: PROVAS</h2>

<div class="alert-box">
  REGISTROS FOTOGRÁFICOS E ÁUDIOS
  <small>Eles dizem que é montagem. Nós sabemos a verdade.</small>
</div>

{% for post in site.posts %}
  {% if post.categories contains 'provas' %}
    <div class="post-card">
      <div class="post-meta">
        <span class="post-date">▶ {{ post.date | date: "%d/%m/%Y" }}</span> 
        <span class="tag">PROVA</span>
      </div>
      <h2 class="post-title"><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
      <p class="post-excerpt">{{ post.excerpt | strip_html | truncatewords: 25 }}</p>
      <a href="{{ post.url | relative_url }}" class="read-more">[ ANALISAR EVIDÊNCIA _ ]</a>
    </div>
  {% endif %}
{% endfor %}
