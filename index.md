---
layout: page
title: 木有意思
tagline: 思考•阅读•生活•苹果•心情•Web
---
{% include JB/setup %}

> 您好,这里是yomuse的个人网站.

**最近发布的文章**:

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>



