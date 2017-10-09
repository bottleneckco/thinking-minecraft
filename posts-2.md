---
id: 71
title: Posts
date: 2014-07-24T10:05:53+00:00
author: Duncan Leo
layout: page

---

<div class="home">
  <ul class="post-list">
    {% for post in site.posts %}
      <li>
        {% assign date_format = site.minima.date_format | default: "%b %-d, %Y" %}
        <span class="post-meta">{{ post.date | date: date_format }}</span>

        <h2>
          <a class="post-link" href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
        </h2>
      </li>
    {% endfor %}
  </ul>

  <a href="{{ "/feed.xml" | relative_url }}">RSS feed</a>

</div>  