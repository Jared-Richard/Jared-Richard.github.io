---
layout: page
title: Post Archive
---



-----

<!-- CATEGORIES -->

<h2>Categories</h2>

* ### [Physics]({{ site.url }}/category/physics)
* ### [Coding]({{ site.url }}/category/coding)
* ### [Finance]({{ site.url }}/category/finance)
* ### [Book Reviews]({{ site.url }}/category/book-reviews)
* ### [General]({{ site.url }}/category/general)

-----

<!-- PROJECTS -->



-----  

<!-- POSTS -->

<h2>Posts</h2>

{% for post in site.posts %}

{{ post.date | date_to_string }} » [{% capture category_name %}{{ post.category }}{% endcapture %} <a href="/category/{{ category_name }}">{{ category_name }}</a> ] » [ **{{ post.title }}** ]({{ site.url }}{{ post.url }}) 

{% endfor %}
