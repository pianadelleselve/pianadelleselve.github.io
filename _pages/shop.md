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

<p><a href="/{{ item.title | slugify }}.html" class="read-more">Read more about {{ item.title }}</a></p>
</article>
{% endfor %}
