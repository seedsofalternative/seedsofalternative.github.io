---
layout: page
title: Treks and Hikes in India
permalink: /trek-reports/india
comments: false
---

<div class="row justify-content-between">
<div class="col-md-8 pr-5">


<p>Posts in category "india" are:</p>

<ul>
  {% for post in site.categories.india %}
    {% if post.url %}
        <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endif %}
  {% endfor %}
</ul>


</div>
</div>
