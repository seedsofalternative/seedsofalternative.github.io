---
layout: page
title: Getting to know yourself
permalink: /introspection
comments: false
---

<div class="row justify-content-between">
<div class="col-md-8 pr-5">


<p>Posts in category "introspection" are:</p>

<ul>
  {% for post in site.categories.introspection %}
    {% if post.url %}
        <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endif %}
  {% endfor %}
</ul>


</div>
</div>
