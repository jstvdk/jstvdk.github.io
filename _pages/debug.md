---
layout: single
title: DEBUG
permalink: /debug/
---

**Total posts:** {{ site.posts | size }}

{% for post in site.posts %}
- {{ post.date | date: "%Y-%m-%d" }} — [{{ post.title }}]({{ post.url }})
{% endfor %}