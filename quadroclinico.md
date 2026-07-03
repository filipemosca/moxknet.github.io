---
title: Quadro Clínico
layout: index
---

<img src="/medicina/quadroclinico.png" alt="" style="max-width: 500px;">

Blog de um clínico para clínicos e estudantes. Escrito por Filipe Mosca, clínico em formação. Esse blog não pretensão de servir como aconselhamento à população geral. O objetivo aqui é contribuir para a educação médica.

<ul class="posts">
  {% for post in site.categories.medicina %}
      {% assign post_time = post.date | date: '%s' %}
      {% assign now = 'now' | date: '%s' %}
      {% assign diff = now | minus: post_time %}
      <li>
        <span class="posts-dates">{{ post.date | date: "%d/%m/%Y" }}</span> <span class="break"></span>
        <a href="{{ post.url }}" class="post-title">{{ post.title }}</a>
          {% if diff < 2592000 %}
          <span class="novo-badge"><i>Novo!</i></span>
          {% endif %}
      </li>
  {% endfor %}
</ul>

## Links úteis

- [Curso de digitação](https://www.edclub.com/pt-BR/library/bosque-da-digitacao) -- acredite, agiliza sua vida (e é gratuito).
- [Criador de acrônimos](https://remember.shinyapps.io/remember_shiny_tool/) -- uso pra criar flashcards.
- [Zbib](https://zbib.org/) -- uso pra formatar referências.