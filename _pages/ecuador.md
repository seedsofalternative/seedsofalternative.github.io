---
layout: page
title: Treks and Hikes in Ecuador
permalink: /trek-reports/ecuador
comments: false
---

<div class="row justify-content-between">
<div class="col-md-8 pr-5">


<p>Posts in category "ecuador" are:</p>

<ul>
  {% for post in site.categories.ecuador %}
    {% if post.url %}
        <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endif %}
  {% endfor %}
</ul>


</div>
</div>
