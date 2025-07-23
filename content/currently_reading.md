---
title: Reading
eleventyNavigation:
  key: Reading
  order: 5
---

# Have a look at what I am reading: 

<ul>
  {% for book in collections.currentReads %}
    <li>
      <strong>{{ book.data.title }}</strong> by {{ book.data.author }}
      {% if book.data.genre %}
        <em>({{ book.data.genre | join(", ") }})</em>
      {% endif %}
    </li>
  {% endfor %}
</ul>