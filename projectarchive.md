---
layout: page
title: Projects
---
-----

<h2>Categories</h2>

* #### [Coding]({{ site.url }}/category/coding)
* #### [Physics]({{ site.url }}/category/physics)
* #### [Finance]({{ site.url }}/category/finance)

-----  

{% for post in site.posts %}

{{ post.date | date_to_string }} » [{% capture category_name %}{{ post.category }}{% endcapture %} <a href="/category/{{ category_name }}">{{ category_name }}</a> ] » [ **{{ post.title }}** ]({{ site.url }}{{ post.url }}) 

{% endfor %}


-----  

<h2>Coding</h2>

{% for post in site.categories[ "coding" ] %}

{{ post.date | date_to_string }} » [{% capture category_name %}{{ post.category }}{% endcapture %} <a href="/category/{{ category_name }}">{{ category_name }}</a> ] » [ **{{ post.title }}** ]({{ site.url }}{{ post.url }}) 

{% endfor %}

-----  

<h2>Physics</h2>

{% for post in site.categories[physics, finance] %}

{{ post.date | date_to_string }} » [{% capture category_name %}{{ post.category }}{% endcapture %} <a href="/category/{{ category_name }}">{{ category_name }}</a> ] » [ **{{ post.title }}** ]({{ site.url }}{{ post.url }}) 

{% endfor %}

-----  

<h2>Finance</h2>

{% for post in site.categories[finance ] %}

{{ post.date | date_to_string }} » [{% capture category_name %}{{ post.category }}{% endcapture %} <a href="/category/{{ category_name }}">{{ category_name }}</a> ] » [ **{{ post.title }}** ]({{ site.url }}{{ post.url }}) 

{% endfor %}