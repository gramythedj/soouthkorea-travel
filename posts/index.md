---
layout: layouts/base.njk
title: Posts
templateClass: tmpl-post
permalink: /blogposts/
eleventyNavigation:
  key: Posts
  order: 2
---

<div id="posts">
  <h2>Posts</h2>
  {% set postslist = collections.posts %}
  {% include "postslist.njk" %}
</div>


