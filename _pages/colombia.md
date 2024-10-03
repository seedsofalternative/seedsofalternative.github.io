---
layout: page
title: Treks and Hikes in Colombia
permalink: /trek-reports/colombia
comments: false
---

<div class="row justify-content-between">
<div class="col-md-8 pr-5">


<p>Posts in category "colombia" are:</p>

<ul>
  {% for post in site.categories.colombia %}
    {% if post.url %}
        <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endif %}
  {% endfor %}
</ul>


</div>
</div>