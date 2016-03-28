---
layout: default
title: "Inverse Dynamics Research"
---
<div class="research" id="research">
  <h1 class="pageTitle">Inverse Dynamics Research</h1>
  <ul class="posts noList">
    {% for post in site.posts %}
      {% if post.category contains 'idyn' %}
        <li>
          <span class="date">{{ post.date | date: '%B %d, %Y' }}</span>
          <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
          <p class="description">{% if post.description %}{{ post.description | strip_html | strip_newlines | truncate: 250 }}{% else %}{{ post.content | strip_html | strip_newlines | truncate: 250 }}{% endif %}</p>
        </li>
      {% endif %}
    {% endfor %}
  </ul>
</div>
