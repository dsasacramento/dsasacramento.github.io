---
layout: page
title: "California Chapters"
permalink: /resources/chapters/
---
<style>ul {list-style: circle} </style> 
Find local California Democratic Socialists of America (DSA) and Young Democratic Socialists of America (YDSA) chapters in your area. DSA and YDSA chapters are starting up across the country to democratically build power in our communities.

### DSA California Chapters
<ul>
{% for item in site.data.dsa-chapters.dsa %}
    {% assign start = 6 %}
    <li>
    {{ item.label }}: 
    {% if item.phone %}
        {{ item.phone }}
        {% assign start = 1 %}
    {% elsif item.email %}
        <a href="mailto:{{ item.email }}">Email</a> 
        {% assign start = 2 %}
    {% elsif item.website %}
        <a href="{{ item.website }}">Website</a>
        {% assign start = 3 %}
    {% elsif item.facebook %}
        <a href="{{ item.facebook }}">Facebook</a>
        {% assign start = 4 %}
    {% elsif item.twitter %}
        <a href="{{ item.twitter }}">Twitter</a>
        {% assign start = 5 %}
    {% endif %}

    {% if item.email and start < 2 %}
        | <a href="mailto:{{ item.email }}">Email</a> 
    {% endif %}
    {% if item.website and start < 3 %}
        | <a href="{{ item.website }}">Website</a>
    {% endif %}
    {% if item.facebook and start < 4 %}
        | <a href="{{ item.facebook }}">Facebook</a>
    {% endif %}
    {% if item.twitter and start < 5 %}
        | <a href="{{ item.twitter }}">Twitter</a>
    {% endif %}
    </li>
{% endfor %}
</ul>


### YDSA California Chapters
<ul>
{% for item in site.data.dsa-chapters.ydsa %}
    {% assign start = 6 %}
    <li>
    {{ item.label }}: 
    {% if item.phone %}
        {{ item.phone }}
        {% assign start = 1 %}
    {% elsif item.email %}
        <a href="mailto:{{ item.email }}">Email</a> 
        {% assign start = 2 %}
    {% elsif item.website %}
        <a href="{{ item.website }}">Website</a>
        {% assign start = 3 %}
    {% elsif item.facebook %}
        <a href="{{ item.facebook }}">Facebook</a>
        {% assign start = 4 %}
    {% elsif item.twitter %}
        <a href="{{ item.twitter }}">Twitter</a>
        {% assign start = 5 %}
    {% endif %}

    {% if item.email and start < 2 %}
        | <a href="mailto:{{ item.email }}">Email</a> 
    {% endif %}
    {% if item.website and start < 3 %}
        | <a href="{{ item.website }}">Website</a>
    {% endif %}
    {% if item.facebook and start < 4 %}
        | <a href="{{ item.facebook }}">Facebook</a>
    {% endif %}
    {% if item.twitter and start < 5 %}
        | <a href="{{ item.twitter }}">Twitter</a>
    {% endif %}
    </li>
{% endfor %}
</ul>