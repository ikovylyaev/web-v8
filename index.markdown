---
layout: default
---
<div class='container-fluid'>
    <div class='row'>
        <div class='col-md-8 col-12'>
            <h1 class='main-color'>Иван Ковыляев</h1>
            <h2 class='h1'>Дизайнер дизайн-систем, интерфейсов, продуктов</h2>
        </div>
        <div class='col-md-4 col-12'>
            <a href='{{site.url}}/projects'>Проекты</a><br>
            <a href='{{site.url}}/work'>Работа</a><br>
            <a href='{{site.url}}/photo'>Фотография</a>
        </div>
    </div>
    <div class='row'>   
        <div class='col-md-4'>
        <h3>Проекты</h3>
        {% for post in site.project %}
        post
            {% if post.link != "" %}
                <a href="{{ post.link }}" target="blank">
            {% else%}
                <div>
            {% endif %}
                <h4>{{ post.title }} 
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
    </div>
</div>
