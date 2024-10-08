---
layout: page
title: Treks and Hikes in Australia
permalink: /trek-reports/australia
comments: false
---

<div class="row justify-content-between">
<div class="col-md-8 pr-5">


<p>Posts in category "australia" are:</p>

<ul>
  {% for post in site.categories.australia %}
    {% if post.url %}
        <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endif %}
  {% endfor %}
</ul>


</div>
</div>