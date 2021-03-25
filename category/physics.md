---
layout: page
title: "Physics"
---

-----

{% for post in site.categories[ physics ] %}

{{ post.date | date_to_string }} » [ **{{ post.title }}** ]({{ site.url }}{{ post.url }}) 

{% endfor %}


{% for post in site.categories[ physics ] %}

[ **{{ post.title }}** ]({{ site.url }}{{ post.url }}) » 
[{% capture category_name %}{{ post.category }}{% endcapture %} <a href="/category/{{ category_name }}">{{ category_name }}</a> ]

{% endfor %}



{% for post in site.categories[ physics ] %}
{{ post.title }}
{{ post.date | date_to_string }} · {% assign words = post.content | number_of_words %}{{ words | divided_by:200 | at_most:25 }} min read   [ {% capture category_name %}{{ post.category }}{% endcapture %} {{ category_name }} ]
{% if post.content contains "" %} {{ post.content | split:"" | first % }}
Read More...
{% endif %}
{% endfor %}
