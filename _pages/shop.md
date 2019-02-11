---
title: Shop
layout: default
permalink: /shop
---
{% assign items = site.shop | sort: 'weight' %}
{% for item in items %}
<article>
  <h2>{{ item.title }}</h2>

  {% include thumbnail.html item=item %}
  {% include values.html item=item %}

<a href="/{{ item.title | slugify }}.html">Read more</a>
</article>
{% endfor %}
