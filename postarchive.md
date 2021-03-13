---
layout: page
title: Post Archive
---

{% for post in site.posts %}
  * {{ post.date | date_to_string }} &raquo;   [{% capture category_name %}{{ post.category }}{% endcapture %}
        <a style="white-space: nowrap" href="/category/{{ category_name }}">{{ category_name }}</a>
    ]
    &raquo;
    [ {{ post.title }} ]({{ site.url }}{{ post.url }}) &raquo; {% assign words = post.content | number_of_words %}{% if words < 360 %}
    1 min {% else %}
    {{ words | divided_by:200 | at_most:25 }} mins
  {% endif %} 
{% endfor %}


{% for post in site.posts %}

{{ post.date | date_to_string }} » [{% capture category_name %}{{ post.category }}{% endcapture %} {{ category_name }} ] » [ {{ post.title }} ]({{ site.url }}{{ post.url }}) » {% assign words = post.content | number_of_words %}{% if words < 360 %} 1 min {% else %} {{ words | divided_by:200 | at_most:25 }} mins {% endif %} {% endfor %}
