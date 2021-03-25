---
layout: default
title: Home
---

<h1>Welcome</h1>

-----

My name is <a href="{{ site.url }}/about">Jared Richard</a>, a Physics Undergraduate at the University of Oxford. 

You've reached my academic website. Check out some of the <a href="{{ site.url }}/projectarchive">projects</a> / <a href="{{ site.url }}/postarchive">posts</a> and feel free to <a href="{{ site.url }}/about">let me know</a> any of your thoughts or ideas.

Thank you for your visit and I hope you enjoy your stay.

-----

<h2>Recent Posts</h2>

{% for post in site.posts limit:3 %}

{{ post.date | date_to_string }} » [{% capture category_name %}{{ post.category }}{% endcapture %} <a href="/category/{{ category_name }}">{{ category_name }}</a> ] » [ **{{ post.title }}** ]({{ site.url }}{{ post.url }}) 

{% endfor %}


<div class="posts">

  {% for post in site.posts %}

  <div class="post">

    <h1 class="post-title">
      <a href="{{ post.url }}">
        {{ post.title }}
      </a>
    </h1>

    <div class="metadata">
      <span style="display: inline" class="post-date" title="Estimated read time">
        {{ post.date | date_to_string }} &middot; 
         {% assign words = post.content | number_of_words %}{{ words | divided_by:200 | at_most:25 }} min read
      </span>

     &emsp;

      <span style="display: inline">[
         {% capture category_name %}{{ post.category }}{% endcapture %}
         <a href="/category/{{ category_name }}">{{ category_name }}</a> ]
      </span>
      
    </div>

    <div>
      {% if post.content contains "<!-- more -->" %}
      {{ post.content | split:"<!-- more -->" | first % }}
      <div style="text-align: left;">
        <a href="{{ post.url }}" style="font-weight: bold; color:#383fc7;">Read More...</a>
      </div>
      {% else %}
        {{ post.content }}
     {% endif %}
    </div>
  </div>

  {% endfor %}

</div>



{% for post in site.categories[physics ] %}
{{ post.title }}
{{ post.date | date_to_string }} · {% assign words = post.content | number_of_words %}{{ words | divided_by:200 | at_most:25 }} min read
{% if post.content contains "" %} {{ post.content | split:"" | first }}
Read More...
{% else %} {{ post.content }} {% endif %}
{% endfor %}