---
layout: default
title: Arquivos Confidenciais
permalink: /arquivos/
---

<h2 class="section-header">VAZAMENTOS: ARQUIVOS</h2>

<div class="alert-box">
  NÍVEL DE AMEAÇA: ALTO
  <small>Mantenha sua VPN ativada durante o download.</small>
</div>

{% for post in site.posts %}
  {% if post.categories contains 'arquivos' %}
    <div class="post-card">
      <div class="post-meta">
        <span class="post-date">▶ {{ post.date | date: "%d/%m/%Y" }}</span> 
        <span class="tag">ARQUIVO</span>
      </div>
      <h2 class="post-title"><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
      <p class="post-excerpt">{{ post.excerpt | strip_html | truncatewords: 25 }}</p>
      <a href="{{ post.url | relative_url }}" class="read-more">[ ACESSAR REGISTRO _ ]</a>
    </div>
  {% endif %}
{% endfor %}
