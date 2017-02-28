---
layout: default
title: blog
---
<div class="container">
<h1 class="post-title">Welkom bij mijn blog</h1>
<div class="home pull-left">

  <ul class="post-list">
    {% for post in site.posts %}
      <li>
        <h2>
           <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }} <small class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</small></a>
        </h2>
      {% if post == site.posts.first %}
        {{ post.content }}
      {% else %}
        {% if post.excerpt %}
            {% if post.image %}
            <img src="{{ post.image | prepend: site.baseurl }}" class="project-image-small rounded" style="float: left; margin-right: 20px">
            {% endif %}
            {{ post.excerpt }} <a href="{{ post.url | prepend: site.baseurl }}">read more</a>
        {% endif %}
      {% endif %}
      </li>
    {% endfor %}
  </ul>
  </div>
