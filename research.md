---
layout: default
title: Research
---

<div class="research" id="research">
  <h1 class="pageTitle">Research</h1>
  <ul class="posts noList">
    {% for post in site.posts %}
      <li>
        <span class="date">{{ post.date | date: '%B %d, %Y' }}</span>
        <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
        <p class="description">{% if post.description %}{{ post.description | strip_html | strip_newlines | truncate: 250 }}{% else %}{{ post.content | strip_html | strip_newlines | truncate: 250 }}{% endif %}</p>
      </li>
    {% endfor %}
  </ul>
</div>
