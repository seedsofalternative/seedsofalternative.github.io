---
layout: page
title: Book Summaries
permalink: /books
comments: false
---

<div class="row justify-content-between">
<div class="col-md-8 pr-5">


<p>The posts in category "books" are:</p>

<ul>
  {% for post in site.categories.books %}
    {% if post.url %}
        <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endif %}
  {% endfor %}
</ul>


</div>
</div>
