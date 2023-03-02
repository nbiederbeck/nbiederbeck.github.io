---
title: Blog
layout: page
permalink: /blog/
---

{% for post in site.posts %}
- [{{ post.title }}]({{ post.url }})
{% endfor %}
