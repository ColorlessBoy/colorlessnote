---
layout: page
title: Categories
permalink: /categories/
---
{% for category in site.categories %}
<h2>{{ category | first }}</h2>
<ul class="arc-list">
    {% for post in category.last %}
        <li>{{ post.date | date:"%d/%m/%Y "}}<a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
</ul>
{% endfor %}
