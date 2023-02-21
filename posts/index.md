---
layout: layouts/base.njk
title: Posts
templateClass: tmpl-post
permalink: /blogposts/
eleventyNavigation:
  key: Posts
  order: 2
---

<ul>
{% for post in postslist | reverse %}
  <li>
    <a href="{{ post.url | url }}">{% if post.data.title %}{{ post.data.title }}{% else %}<code>{{ post.url }}</code>{% endif %}</a>
    <time  datetime="{{ post.date | htmlDateString }}">{{ post.date | readableDate }}</time>
  </li>
{% endfor %}
</ul>