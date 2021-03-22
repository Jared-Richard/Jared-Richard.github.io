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

{% for post in site.posts[physics, finance] %}

{{ post.date | date_to_string }} » [{% capture category_name %}{{ post.category }}{% endcapture %} <a href="/category/{{ category_name }}">{{ category_name }}</a> ] » [ **{{ post.title }}** ]({{ site.url }}{{ post.url }}) 

{% endfor %}



TEST

<div class="posts">

  {% for post in site.categories[physics, finance] %}

  <div class="post">

    <h3 class="post-title">
      <a href="{{ post.url }}">
        {{ post.title }}
      </a>
    </h3>

    <div class="metadata">
      <span style="display: inline" class="post-date" title="Estimated read time">
        {{ post.date | date_to_string }} &middot; 
         {% assign words = post.content | number_of_words %}{{ words | divided_by:200 | at_most:25 }} min read
      </span>
    </div>

      {% if post.content contains "<!-- more -->" %}
      {{ post.content | split:"<!-- more -->" | first % }}
      <div style="text-align: left;">
        <a href="{{ post.url }}" style="font-weight: bold; color:#383fc7;">Read More...</a>
      </div>
    {% else %}
      {{ post.content }}
    {% endif %}
  </div>
  {% endfor %}
</div>