---
layout: page
title: Treks and Hikes in Pakistan
permalink: /trek-reports/pakistan
comments: false
---

<div class="row justify-content-between">
<div class="col-md-8 pr-5">


<p>Posts in category "pakistan" are:</p>

<ul>
  {% for post in site.categories.pakistan %}
    {% if post.url %}
        <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endif %}
  {% endfor %}
</ul>


</div>
</div>
