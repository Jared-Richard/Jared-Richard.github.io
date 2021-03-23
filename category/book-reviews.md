---
layout: page
title: "Book Reviews"
---

All my book reviews and then a <a href="">link</a> to all books I've read.

-----

{% for post in site.categories[book-reviews, ] %}

{{ post.date | date_to_string }} » [ **{{ post.title }}** ]({{ site.url }}{{ post.url }}) 

{% endfor %}

