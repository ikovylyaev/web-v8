---
layout: page
permalink: /projects/
title: 'Проекты'
---
<div class='row'>
{% for post in site.projects %}
    {% if post.link != "" %}
        <a href="{{ post.link }}" target="_blank" class="col-md-4 col-sm-6 col-12" >
    {% else%}
        <div class="col-md-4 col-sm-6 col-12">
    {% endif %}
    <img src='{{ site.url }}/img/projects/{{ post.image }}.webp' alt='{{ post.title }}' style='width: 100%; border-radius: 16px; margin-bottom: 0.5rem;'>
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
{% for post in site.projectsmore %}
    {% if post.link != "" %}
        <a href="{{ post.link }}" target="_blank" class="col-md-4 col-sm-6 col-12" >
    {% else%}
        <div class="col-md-4 col-sm-6 col-12">
    {% endif %}
    <img src='{{ site.url }}/img/projects/{{ post.image }}.webp' alt='{{ post.title }}' style='width: 100%; border-radius: 16px; margin-bottom: 0.5rem;'>
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
