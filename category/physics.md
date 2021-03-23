---
layout: page
title: "Physics"
---

-----

{% for post in site.categories[physics, ] %}

{{ post.date | date_to_string }} » [ **{{ post.title }}** ]({{ site.url }}{{ post.url }}) 

{% endfor %}

<!-- 
{% for post in site.categories[physics, ] %}

{{ post.date | date_to_string }} » [{% capture category_name %}{{ post.category }}{% endcapture %} <a href="/category/{{ category_name }}">{{ category_name }}</a> ] » [ **{{ post.title }}** ]({{ site.url }}{{ post.url }}) 

{% endfor %}
 -->