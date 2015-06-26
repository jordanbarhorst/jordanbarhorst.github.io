---
layout: page
title: Work
permalink: /work/
weight: 2

heroimage: work/featured.jpg
headline: My Work
subline: Below you'll find a collection of design work I've done for previous employers, freelance clients, and just for fun. 

---

{% for post in site.tags['portfolio'] %}
<a href="{{ post.url | prepend: site.baseurl }}"><h1>{{ post.title}}</h1></a>
{% endfor %}
