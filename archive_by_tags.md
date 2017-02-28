---
layout: page
title: Archive
permalink: /archive_by_tags/
---

<h2>Archives by Tags</h2>
{% for tag in site.tags %}
  {% assign t = tag | first %}
  {% assign posts = tag | last %}

<a name="{{#t | slugify}}">{{ t | downcase }}</a>

<ul>
  {% for post in site.posts %}
    {% if post.tags contains t %}
        {% unless post.next %}
          <h3>{{ post.date | date: '%Y' }}</h3>
        {% else %}
          {% capture year %}{{ post.date | date: '%Y' }}{% endcapture %}
          {% capture nyear %}{{ post.next.date | date: '%Y' }}{% endcapture %}
          {% if year != nyear %}
            <h3>{{ post.date | date: '%Y' }}</h3>
          {% endif %}
        {% endunless %}

        <li>{{ post.date | date:"%b" }} <a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endif %}
  {% endfor %}
</ul>
{% endfor %}
