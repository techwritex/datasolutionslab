---
layout: default
title: Заметки
---

<section class="notes-section">
  <h2>> ls -la ./notes</h2>
  
  <div class="notes-container">
    <div class="notes-list">
      {% for post in site.posts %}
        <article class="note-item">
          <time class="note-date" datetime="{{ post.date | date_to_xmlschema }}">
            {{ post.date | date: "%Y-%m-%d" }}
          </time>
          <span class="note-pointer"></span>
          <a href="{{ post.url | relative_url }}" class="note-link">{{ post.title }}</a>
        </article>
      {% endfor %}
    </div>
  </div>
  
  <p class="terminal-footer">[system]: общее количество нод в директории: {{ site.posts | size }}</p>
</section>