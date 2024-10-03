---
layout: page
title: Hikes and Treks in Nepal
permalink: /trek-reports/nepal
comments: false
---

<div class="row justify-content-between">
<div class="col-md-8 pr-5">


<p>Posts in category "nepal" are:</p>

<ul>
  {% for post in site.categories.nepal %}
    {% if post.url %}
        <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endif %}
  {% endfor %}
</ul>


</div>
</div>