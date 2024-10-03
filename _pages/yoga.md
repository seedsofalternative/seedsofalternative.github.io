---
layout: page
title: Yoga
permalink: /philosophy/yoga
comments: false
---

<div class="row justify-content-between">
<div class="col-md-8 pr-5">


<p>Posts in category "yoga" are:</p>

<ul>
  {% for post in site.categories.yoga %}
    {% if post.url %}
        <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endif %}
  {% endfor %}
</ul>


</div>
</div>
