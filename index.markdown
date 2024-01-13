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
        <div class='col-md-4 col-12'>
        <h3>Проекты</h3>
        {% for post in site.projects %}
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
        <div class='col-md-4 col-12'>
        <h3>Работа</h3>
        {% for post in site.works %}
            <div>
                <small>{{ post.year }}</small>
                <h4>{{ post.title }}</h4>
                <p>{{post.description}}</p>
            </div>
        {% endfor %}
        </div>
        <div class='col-md-4 col-12'>
        <h3>Контакты</h3>
        <a class='mt-3 par' href='mailto:hi@ikovylyaev.com' target="_blank">Почта hi@ikovylyaev.com</a><br>
        <a class='par' href='https://figma.com/@ikovylyaev' target="_blank">Figma @ikovylyaev</a><br>
        <a class='par' href='https://behance.net/ikovylyaev' target="_blank">Behance @ikovylyaev</a><br>
        <a class='par' href='https://dprofile.ru/ikovylyaev' target="_blank">DProfile @ikovylyaev</a><br>
        <a class='par' href='https://t.me/ikovylyaev' target="_blank">Tg @ikovylyaev</a><br>
        <a class='mt-5 secondary-link' href='{{site.url}}/policy' target="">Политика конфиденциальности</a>
        </div>
    </div>
</div>
