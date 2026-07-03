---
layout: default
title: Dossiês e Relatórios
permalink: /dossies/
---

<h2 class="section-header">ARQUIVO MORTO: DOSSIÊS DE MISSÃO</h2>

<div class="alert-box">
  NÍVEL DE ACESSO: MÁXIMO
  <small>Os relatos abaixo contém informações sensíveis sobre a Desconjuração.</small>
</div>

{% for post in site.posts %}
{% if post.categories contains 'dossies' %}
<div class="post-card">
  <div class="post-meta">
    <span class="post-date">▶ {{ post.date | date: "%d/%m/%Y" }}</span> 
    <span class="tag" style="color: #ff3333; border-color: #ff3333;">DOSSIÊ</span>
  </div>
  <h2 class="post-title"><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
  <p class="post-excerpt">{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
  <a href="{{ post.url | relative_url }}" class="read-more">[ DESCRIPTOGRAFAR ARQUIVO _ ]</a>
</div>
{% endif %}
{% endfor %}