---
layout: default
---

<ul>
  {% for post in site.posts %}
    <li>
        <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
        <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date_to_string }}</time>
        <p>{{ post.content | strip_html | truncatewords:20 }}</p>
    </li>
  {% endfor %}
</ul>
