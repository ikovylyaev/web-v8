---
layout: page
permalink: /photo/
title: 'Фотография'
---
<div class="row">
    {% for counter in (1..48) %}
    <div class='col-md-4 col-sm-6 col-12 photo' style='background: url({{site.url}}/img/photo/{{ counter }}.webp);background-size: cover; background-position: center;'></div>
{% endfor %}
</div>
<style>
  .photo{
    aspect-ratio: 1/1;
    border: 8px solid #FFFFFF;
  }
</style>