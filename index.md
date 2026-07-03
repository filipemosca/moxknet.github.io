---
layout: index
title: "Blog do Mosca"
---

<img src="/blog-do-mosca.png" alt="" style="max-width: 500px;">

Olá, eu sou Filipe! Sou médico,  atualmente realizando a residência (especialização) de clínica médica. Esse é meu espaço na internet para compartilhar meus hobbies e escrever sobre a medicina.

- [Jogos de tabuleiro](/boardgames/jogos-tabuleiro)
- [Jogos de baralho](/boardgames/baralho)
- Aprendendo a digitar mais rápido: [TypingClub](https://www.edclub.com/sportal/program-21.game)

## Todas as postagens

<ul>
  {% for post in site.posts %}
    {% unless post.path contains "medruas" %}
      <li>
        <span>{{ post.date | date: "%d/%m/%Y" }}</span>
        <a href="{{ post.url }}">{{ post.title }}</a>
        <span style="font-size: 0.8em; color: gray">
          {% for tag in post.tags %}#{{ tag }} {% endfor %}
        </span>
      </li>
    {% endunless %}
  {% endfor %}
</ul>