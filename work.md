---
layout: page
title: Work
permalink: /work/
weight: 2

heroimage: work/featured.jpg
headline: My Work
subline: Below you'll find a collection of design work I've done for previous employers, freelance clients, and just for fun. 

---

<div class="work wrapper">
    {% for post in site.tags['portfolio'] %}
        <div class="work-portfolio-item">
           <img src="/assets/img/portfolio-items/{{ post.portfolio-grid-photo }}" alt="{{post.title}}">
            <span class="portfolio-overlay" style="background-color:#{{ post.color }};">
                <span class="post-meta">{{ post.categories }}</span>
                <h3>{{ post.title }}</h3>

                {% if post.alt-button-link %}
                <a class="white hollow-button" target="_blank" href=" {{ post.alt-button-link }}" onMouseOver="this.style.color='#{{ post.color }}'" onMouseOut="this.style.color='#ffffff'">{{ post.alt-button-text }}</a>
                {% else %}
                <a class="white hollow-button" href="{{ post.url | prepend: site.baseurl }}" onMouseOver="this.style.color='#{{ post.color}}'" onMouseOut="this.style.color='#ffffff'">View Case Study</a>
                {% endif %}

            </span>
        </div>
    {% endfor %}
</div>
