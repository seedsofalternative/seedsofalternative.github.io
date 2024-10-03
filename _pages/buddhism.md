---
layout: page
title: Buddhism
permalink: /philosophy/buddhism
comments: false
---

<div class="row justify-content-between">
<div class="col-md-8 pr-5">


<p>Posts in category "buddhism" are:</p>

<ul>
  {% for post in site.categories.buddhism %}
    {% if post.url %}
        <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endif %}
  {% endfor %}
</ul>


</div>
</div>