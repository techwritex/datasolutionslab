---
layout: default
title: Заметки
permalink: /notes/
---

<section class="notes-section">
  <h2>ls ./notes</h2>
  <div class="notes-container">
    <ul class="notes-list">
      {% for post in site.posts %}
        <li class="note-item">
          <span class="note-date">{{ post.date | date: "%Y-%m-%d" }}</span>
          <span class="note-pointer"> >> </span>
          <a href="{{ post.url | relative_url }}" class="note-link">{{ post.title }}</a>
        </li>
      {% endfor %}
    </ul>
  </div>
  <p class="terminal-footer">[system]: найдено записей: {{ site.posts | size }}</p>
</section>