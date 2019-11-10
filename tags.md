---
layout: page
title: Tags
permalink: /tags/
---

{% for tag in site.tags %}
<h2>{{ tag | first }}</h2>
<ul class="arc-list">
    {% for post in tag.last %}
        <li>{{ post.date | date:"%d/%m/%Y "}}<a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
</ul>
{% endfor %}
