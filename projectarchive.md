---
layout: page
title: Projects
---
-----

{% for post in site.posts %}

[ **{{ **post.title** }}** ]({{ site.url }}{{ post.url }}) » [{% capture category_name %}{{ post.category }}{% endcapture %} <a href="/category/{{ category_name }}">{{ category_name }}</a> ]

<!-- Excerpt -->

{{ post.content | split:"<!-- more -->" | first }}

-----

{% endfor %}