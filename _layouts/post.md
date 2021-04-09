---
layout: default
---
<h1>{{ page.title }}</h1>
<p class="view"><small>{{ page.date | date_to_string }}</small> - {{ page.author }}</p>

<p>{{ content }}</p>

{% if page.tags %}
  <small>tags: <em>{{ page.tags | join: "</em> - <em>" }}</em></small>
{% endif %}