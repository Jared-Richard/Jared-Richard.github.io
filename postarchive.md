---
layout: page
title: Post Archive
---

<h2>Categories</h2>

[Link to a category]({{ site.baseurl }}{% link category/physics.md %})
[Link to a file]({{ site.baseurl }}{% link /assets/files/doc.pdf %})

category 1
category 2
category 3
category 4

<h2>All Posts</h2>

{% for post in site.posts %}

{{ post.date | date_to_string }} » [{% capture category_name %}{{ post.category }}{% endcapture %} <a href="/category/{{ category_name }}">{{ category_name }}</a> ] » [ {{ post.title }} ]({{ site.url }}{{ post.url }}) » {% assign words = post.content | number_of_words %}{% if words < 360 %} 1 min {% else %} {{ words | divided_by:200 | at_most:25 }} mins {% endif %} {% endfor %}
