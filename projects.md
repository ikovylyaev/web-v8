---
layout: page
permalink: /projects/
title: 'Проекты'
---
<div class='row'>
{% for post in site.projects %}
    {% if post.link != "" %}
        <a href="{{ post.link }}" target="_blank" class="col-md-6 col-12" >
    {% else%}
        <div class="col-md-6 col-12">
    {% endif %}
    <h4 class='mb-1'>{{ post.title }} 
        {% if post.link == "" %}
            <p class='badge'>Скоро</p>
        {% endif %}
    </h4>
    <p>{{post.description}}</p>
    {% if post.link != "" %}
        </a>
    {% else %}
        </div>
    {% endif %}
{% endfor %}
</div>
