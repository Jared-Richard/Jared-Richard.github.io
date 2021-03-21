---
layout: page
title: Posts
---
-----

<h2>Categories</h2>

* #### [Book Reviews]({{ site.url }}/category/book-reviews)
* #### [General]({{ site.url }}/category/general)

-----  

<h2>Post Archive</h2>

{% for post in site.posts %}

{{ post.date | date_to_string }} » [{% capture category_name %}{{ post.category }}{% endcapture %} <a href="/category/{{ category_name }}">{{ category_name }}</a> ] » [ **{{ post.title }}** ]({{ site.url }}{{ post.url }}) 

{% endfor %}
