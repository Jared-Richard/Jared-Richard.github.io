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

<h2>Project Archive</h2>

{% for post in site.posts %}

{{ post.date | date_to_string }} » [{% capture category_name %}{{ post.category }}{% endcapture %} <a href="/category/{{ category_name }}">{{ category_name }}</a> ] » [ **{{ post.title }}** ]({{ site.url }}{{ post.url }}) 

{% endfor %}



TEST 1

{% for post in site.categories[physics, finance] %}

{{ post.date | date_to_string }} » [{% capture category_name %}{{ post.category }}{% endcapture %} <a href="/category/{{ category_name }}">{{ category_name }}</a> ] » [ **{{ post.title }}** ]({{ site.url }}{{ post.url }}) 

{% endfor %}


TEST 2

{% for post in site.categories["physics", "finance"] %}
  {% if post.categories contains "physics" or post.categories contains "finance" or post.categories contains "coding" %}

    {{ post.date | date_to_string }} » [{% capture category_name %}{{ post.category }}{% endcapture %} <a href="/category/{{ category_name }}">{{ category_name }}</a> ] » [ **{{ post.title }}** ]({{ site.url }}{{ post.url }}) 

  {% endif %}
{% endfor %}



TEST 3

{% for post in site.categories[ physics, finance ] %}
  {% if post.categories contains "physics" or post.categories contains "finance" %}

    {{ post.date | date_to_string }} » [{% capture category_name %}{{ post.category }}{% endcapture %} <a href="/category/{{ category_name }}">{{ category_name }}</a> ] » [ **{{ post.title }}** ]({{ site.url }}{{ post.url }}) 

  {% endif %}
{% endfor %}


TEST 4

{% for post in site.categories %}
  {% if post.categories contains "physics" and post.categories contains "finance" %}

    {{ post.date | date_to_string }} » [{% capture category_name %}{{ post.category }}{% endcapture %} <a href="/category/{{ category_name }}">{{ category_name }}</a> ] » [ **{{ post.title }}** ]({{ site.url }}{{ post.url }}) 

  {% endif %}
{% endfor %}

TEST 5

{% for post in site.categories[physics, finance] %}
  {% if post.categories contains "physics" or post.categories contains "finance" or post.categories contains "coding" %}

    {{ post.date | date_to_string }} » [{% capture category_name %}{{ post.category }}{% endcapture %} <a href="/category/{{ category_name }}">{{ category_name }}</a> ] » [ **{{ post.title }}** ]({{ site.url }}{{ post.url }}) 

  {% endif %}
{% endfor %}






