---
layout: default
title: IT_case
---

# IT_case

{% for post in site.posts %}
- [{{ post.title }}]({{ post.url | relative_url }}) ({{ post.date | date: "%Y-%m-%d" }})
{% endfor %}

pyff-ny/pyff-ny.github.io/_posts/2026-01-20-case-n1-dns.md