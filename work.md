---
layout: page
permalink: /work/
title: 'Работа'
---
<div class='row'>
{% for post in site.works %}
    <div class="col-md-6 col-12">
        <small>{{ post.year }}</small>
        <h4 class='mb-1' style='margin-top: 0.5rem;'>{{ post.title }}</h4>
        <p>{{post.description}}</p>
    </div>
{% endfor %}
</div>