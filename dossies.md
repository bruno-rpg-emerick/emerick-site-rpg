---
layout: default
title: Dossiês Investigativos
permalink: /dossies/
---

<h2 class="section-header">ARQUIVO MORTO: DOSSIÊS</h2>

<div class="alert-box">
  ACESSO RESTRITO
  <small>Credenciais verificadas. Acesso concedido.</small>
</div>

{% for post in site.posts %}

  {% if post.categories contains 'dossies' %}
  
    <div class="post-card">
      <div class="post-meta">
        <span class="post-date">▶ {{ post.date | date: "%d/%m/%Y" }}</span> 
        <span class="tag">DOSSIÊ</span>
      </div>
      
      <h2 class="post-title">
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      </h2>
      
      <p class="post-excerpt">{{ post.excerpt | strip_html | truncatewords: 25 }}</p>
      
      <a href="{{ post.url | relative_url }}" class="read-more">[ LER DOSSIÊ COMPLETO _ ]</a>
    </div>

  {% endif %}
  
{% endfor %}
