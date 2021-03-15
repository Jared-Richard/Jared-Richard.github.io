---
layout: page
title: Post Archive
---

<h2>Categories</h2>

[Physics]({{ site.url }}/category/physics)

<h3>[Life]({{ site.url }}/category/life)</h3>

<h2>[Life]({{ site.url }}/category/book-reviews)</h2>

category 1
category 2
category 3
category 4

<h2>All Posts</h2>

{% for post in site.posts %}

{{ post.date | date_to_string }} » [{% capture category_name %}{{ post.category }}{% endcapture %} <a href="/category/{{ category_name }}">{{ category_name }}</a> ] » [ {{ post.title }} ]({{ site.url }}{{ post.url }}) » {% assign words = post.content | number_of_words %}{% if words < 360 %} 1 min {% else %} {{ words | divided_by:200 | at_most:25 }} mins {% endif %} {% endfor %}
