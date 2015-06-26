---
layout: page
title: Work
permalink: /work/
weight: 2
---

{% for post in site.tags[portfolio] %}
<a href="{{ post.url | prepend: site.baseurl }}"><h1>{{ post.title}}</h1></a>
{% endfor %}
