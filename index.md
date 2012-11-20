---
layout: page
title: 木有意思
tagline: 思考•阅读•生活•苹果•心情•Web
---
{% include JB/setup %}

> If you wish to succeed, you should use persistence as your good friend, experience as your reference, prudence as your brother and hope as your sentry.

> Life is like a wheel, sometimes you're up, sometimes you're down.

> The future is already here. It's just unevenly distributed.

> A great obstacle to happiness is to anticipate too great a happiness.

**最近发布的文章**:

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>



