---
layout: page
title: "Archive"
description: "独木亦成林"
header-img: "img/black.jpg"
---

<center>
    <p><img src="http://otsp9u9u8.bkt.clouddn.com/17-7-28/46064042.jpg" align="center"></p>
</center>

<ul class="listing">
{% for post in site.posts %}
  {% capture y %}{{post.date | date:"%Y"}}{% endcapture %}
  {% if year != y %}
    {% assign year = y %}
    <li class="listing-seperator">{{ y }}</li>
  {% endif %}
  <li class="listing-item">
    <time datetime="{{ post.date | date:"%Y-%m-%d" }}">{{ post.date | date:"%Y-%m-%d" }}</time>
    <a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>
  </li>
{% endfor %}
</ul>
