---
layout: page
title: "Blog"
permalink: /blog/
---
<h2>News and Updates</h2>

<div class="row my-5">
  {% for post in site.posts %}
    <div class="col-12">
      <h6 class="my-0 text-black-tint-2">{{ post.date | date: "%b %-d, %Y" }}</h6>
      <a class="my-0 article-link" href="{{ post.url }}">{{ post.title }}</a>
      <p>{{ post.short_description }}</p>
    </div>
  {% endfor %}
</div>

