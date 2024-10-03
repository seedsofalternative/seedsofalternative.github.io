---
layout: page
title: Non-Violent Communication
permalink: /communication
comments: false
---

<div class="row justify-content-between">
<div class="col-md-8 pr-5">


<p>Posts in category "communication" are:</p>

<ul>
  {% for post in site.categories.communication %}
    {% if post.url %}
        <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endif %}
  {% endfor %}
</ul>


</div>
</div>
