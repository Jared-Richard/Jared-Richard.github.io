---
layout: page
title: "Physics"
---

-----
<div style="text-align:left">

{% for post in site.categories[physics, ] %}

- [ **{{ post.title }}** ]({{ site.url }}{{ post.url }}) &middot; {{ post.date | date_to_string }} 

{% endfor %}

</div>

<!-- 
{% for post in site.categories[physics, ] %}

{{ post.date | date_to_string }} » [{% capture category_name %}{{ post.category }}{% endcapture %} <a href="/category/{{ category_name }}">{{ category_name }}</a> ] » [ **{{ post.title }}** ]({{ site.url }}{{ post.url }}) 

{% endfor %}
 -->