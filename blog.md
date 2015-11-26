---
layout: default
title: Blog
permalink: /blog/
---
<div class="posts">
  {% for post in site.posts %}
    <article class="post">

      <h1><a class="blog-link"href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h1>

      <div class="entry">
        {{ post.excerpt }}
      </div>

      <a class="blog-link" href="{{ site.baseurl }}{{ post.url }}" class="read-more">Read More</a>
    </article>
  {% endfor %}
</div>