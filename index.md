---
layout: default
---

<ul>
{% for post in site.posts %}
  <li>
    <span style="display: flex; flex-direction: column; justify-content: space-between;">
      <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
      <h4>{{ post.date | date_to_string }}</h4>
    </span>    
    <h4>{{ post.content | strip_html | truncatewords: 20 }}</h4>
  </li>
{% endfor %}
</ul>
