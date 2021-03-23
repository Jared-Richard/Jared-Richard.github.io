---
layout: page
title: "Finance"
---

Through reading “The Physics of Wall Street” by James Weatherall, I was first introduced to the subtle yet elegant relationship between financial markets and physical theories.

I intend to harness the analytical skills from my Physics degree and technical skills from self-teaching Python to understand market behaviour on a deeper level. An exploration into predicting the unpredictable.

-----

{% for post in site.categories[finance, ] %}

{{ post.date | date_to_string }} » [ **{{ post.title }}** ]({{ site.url }}{{ post.url }}) 

{% endfor %}