---
layout: page
title: Blog Archive
---

{% for tag in site.tags %}
  <h3>{{ tag[0] }}</h3>
  <h3>"I have no idea waht im doing"</h3>
  <ul>
    {% for post in tag[1] %}
      <li><a href="{{ post.url }}">{{ post.date | date: "%B %Y" }} - {{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}