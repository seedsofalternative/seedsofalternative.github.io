---
layout: page
title: Hikes in Ireland
permalink: /trek-reports/ireland
comments: false
---

<div class="row justify-content-between">
<div class="col-md-8 pr-5">


<p>Posts in category "ireland" are:</p>

<ul>
  {% for post in site.categories.ireland %}
    {% if post.url %}
        <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endif %}
  {% endfor %}
</ul>


</div>
</div>
