---
layout: page
title: 木有意思
tagline: 思考•阅读•生活•苹果•心情•Web
---
{% include JB/setup %}

> If you wish to succeed, you should use persistence as your good friend, experience as your reference, prudence as your brother and hope as your sentry.

> Life is like a wheel, sometimes you're up, sometimes you're down.

> 一切都是命运 一切都是烟云 一切都是没有结局的开始 一切都是稍纵即逝的追寻 一切欢乐都没有微笑 一切苦难都没有泪痕 一切语言都是重复 一切交往都是初逢 一切爱情都在心里 一切往事都在梦中 一切希望都带着注释 一切信仰都带着呻吟 一切爆发都有片刻的宁静 一切死亡都有冗长的回声

> A great obstacle to happiness is to anticipate too great a happiness.

**最近发布的文章**:

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>



