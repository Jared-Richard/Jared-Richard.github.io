---
layout: page
title: "Coding"
---

-----

{% for post in site.categories[coding, ] %}

{{ post.date | date_to_string }} » [ **{{ post.title }}** ]({{ site.url }}{{ post.url }}) 

{% endfor %}
