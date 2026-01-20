---
layout: default
title: IT case collection and study
---

# IT case collection and study

{% assign net = site.categories.network | sort: "date" | reverse %}
{% if net and net.size > 0 %}
## Network
{% for post in net %}
- [{{ post.title }}]({{ post.url | relative_url }}) ({{ post.date | date: "%Y-%m-%d" }})
{% endfor %}
{% endif %}

{% assign net = site.categories.hardware | sort: "date" | reverse %}
{% if net and net.size > 0 %}
## Hardware
{% for post in net %}
- [{{ post.title }}]({{ post.url | relative_url }}) ({{ post.date | date: "%Y-%m-%d" }})
{% endfor %}
{% endif %}

{% assign net = site.categories.os | sort:"date" | reverse %}
{% if net and net.size > 0 %}
## Operating Systems
{% for post in net %}
- [{{ post.title }}]({{ post.url | relative_url }}) ({{ post.date | date: "%Y-%m-%d" }})
{% endfor %}
{% endif %}

{% assign net = site.categories.user | sort: "date" | reverse %}
{% if net and net.size > 0 %}
## User/Process
{% for post in net %}
- [{{ post.title }}]({{ post.url | relative_url }}) ({{ post.date | date: "%Y-%m-%d" }})
{% endfor %}
{% endif %}
