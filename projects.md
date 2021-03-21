---
layout: project
title: Projects
---

<div class="posts">

  {% for post in site.category.physics %}

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




<div class="pagination">
  {% if paginator.next_page %}
    <a class="pagination-item older" href="{{ site.url }}/page{{paginator.next_page}}">Older</a>
  {% else %}
    <span class="pagination-item older">Older</span>
  {% endif %}
  {% if paginator.previous_page %}
    {% if paginator.page == 2 %}
      <a class="pagination-item newer" href="{{ site.url }}">Newer</a>
    {% else %}
      <a class="pagination-item newer" href="{{ site.url }}/page{{paginator.previous_page}}">Newer</a>
    {% endif %}
  {% else %}
    <span class="pagination-item newer">Newer</span>
  {% endif %}
</div>

