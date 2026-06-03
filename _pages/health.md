---
layout: page
title: Physical Wellbeing
permalink: /wellbeing
comments: false
---

<div class="row justify-content-between">
<div class="col-md-8 pr-5">


<p>The posts in category "wellbeing" are:</p>

<ul>
  {% for post in site.categories.wellbeing %}
    {% if post.url %}
        <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endif %}
  {% endfor %}
</ul>


</div>
</div>
