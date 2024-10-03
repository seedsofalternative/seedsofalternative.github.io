---
layout: page
title: Hikes in Romania
permalink: /trek-reports/romania
comments: false
---

<div class="row justify-content-between">
<div class="col-md-8 pr-5">


<p>Posts in category "romania" are:</p>

<ul>
  {% for post in site.categories.romania %}
    {% if post.url %}
        <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endif %}
  {% endfor %}
</ul>


</div>
</div>
