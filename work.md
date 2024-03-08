---
layout: page
permalink: /work/
title: 'Работа'
---
<div class='row par-exbig'>
    {% for post in site.works %}
        {% if post.link != "" %}
            <a href="{{ post.permalink }}" target="_blank" class="col-md-6 col-12" >
        {% else%}
            <div class="col-md-6 col-12">
        {% endif %}
            <small>{{ post.year }}</small>
            <h3 style='margin-bottom: 0rem; margin-top: 0.1rem;'>{{ post.title }}</h3>
            <p class='par-big'>{{post.description}}</p>
        {% if post.link != "" %}
            </a>
        {% else%}
            </div>
        {% endif %}
    {% endfor %}
    </div>