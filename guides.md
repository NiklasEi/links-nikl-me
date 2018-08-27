---
layout: default
title: Guides
description: Links to all guides on this website.
permalink: /guides
---
{% for item in site.guides %}
  <h2><a href="{{ item.url }}">{{ item.title }}</a></h2>
  <p>{{ item.description }}</p>
  <br>
{% endfor %}