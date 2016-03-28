---
layout: default
title: Research
---
<div class="research" id="research">
  <h1 class="pageTitle">Research</h1>
  
<ul>
  <li><h4><a href='simulation'>Simulation</a></h4>
    <ul>
{% for node in site.posts %}
  {% if node.category contains 'simulation' %}
      <li><a href='{{node.url}}'>{{node.title}}</a></li>
  {% endif %}
{% endfor %}
    </ul>
  </li>
  <li><h4><a href='idyn'>Inverse Dynamics</a></h4>
    <ul>
{% for node in site.posts %}
  {% if node.category contains 'idyn' %}
      <li><a href='{{node.url}}'>{{node.title}}</a></li>
  {% endif %}
{% endfor %}
    </ul>
  </li>
  <li><h4><a href='locomotion'>Legged Locomotion</a></h4>
    <ul>
{% for node in site.posts %}
  {% if node.category contains 'locomotion' %}
      <li><a href='{{node.url}}'>{{node.title}}</a></li>
  {% endif %}
{% endfor %}
    </ul>
  </li>
  <li><h4><a href='manipulation'>Human Manipulation</a></h4>
    <ul>
{% for node in site.posts %}
  {% if node.category contains 'manipulation' %}
    <li><a href='{{node.url}}'>{{node.title}}</a></li>
  {% endif %}
{% endfor %}
    </ul>
  </li>
</ul>
</div>
