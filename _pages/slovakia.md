---
layout: page
title: Hikes in Slovakia
permalink: /trek-reports/slovakia
comments: false
---

<div class="row justify-content-between">
<div class="col-md-8 pr-5">


<p>Posts in category "slovakia" are:</p>

<ul>
  {% for post in site.categories.slovakia %}
    {% if post.url %}
        <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endif %}
  {% endfor %}
</ul>


</div>
</div>