---
layout: posts
title: IT_case
---

# IT_case

{% for post in site.posts %}
- [{{ post.title }}]({{ posts.url | relative_url }}) ({{ post.date | date: "%Y-%m-%d" }})
{% endfor %}
