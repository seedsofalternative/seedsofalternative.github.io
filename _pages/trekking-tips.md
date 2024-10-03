---
layout: page
title: Trekking tips
permalink: /trek-reports/trekking-tips
comments: false
---

<div class="row justify-content-between">
<div class="col-md-8 pr-5">


<p>Posts in category "trekking-tips" are:</p>

<ul>
  {% for post in site.categories.trekking-tips %}
    {% if post.url %}
        <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endif %}
  {% endfor %}
</ul>


</div>
</div>
