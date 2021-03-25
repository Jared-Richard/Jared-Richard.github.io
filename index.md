---
layout: default
title: Home
---

<h1>Welcome</h1>

-----

My name is <a href="{{ site.url }}/about">Jared Richard</a>, a Physics Undergraduate at the University of Oxford. 

You've reached my academic website. Check out some of the <a href="{{ site.url }}/projectarchive">projects</a> / <a href="{{ site.url }}/postarchive">posts</a> and feel free to <a href="{{ site.url }}/about">let me know</a> any of your thoughts or ideas.

Thank you for your visit and I hope you enjoy your stay.

-----

<h2>Recent Posts</h2>

-----

{% for post in site.posts %}

  [ **{{ post.title }}** ]({{ site.url }}{{ post.url }}) » [{% capture category_name %}{{ post.category }}{% endcapture %} <a href="/category/{{ category_name }}">{{ category_name }}</a> ]

 <!-- Excerpt -->

- {{ post.content | split:"<!-- more -->" | first }}

{% endfor %}

-----




