---
title: Tags
pagination:
  data: collections
  size: 1
  alias: tag
  filter: tag => !["all", "nav", "post", "posts"].includes(tag)
permalink: /tags/{{ tag | slug }}/index.html
eleventyComputed:
  title: "Posts tagged with {{ tag }}"
eleventyNavigation:
    key: Tags
    order: 2
    
---

<h1>Posts tagged with "{{ tag }}"</h1>

<ul>
  {% for post in collections[tag] %}
    <li>
      <a href="{{ post.url }}">{{ post.data.title }}</a>
      ({{ post.date | readableDate }})
    </li>
  {% endfor %}
</ul>