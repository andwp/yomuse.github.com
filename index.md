---
layout: page
title: 木有意思
tagline: 思考•阅读•生活•苹果•心情•Web
---
{% include JB/setup %}

> If you wish to succeed, you should use persistence as your good friend, experience as your reference, prudence as your brother and hope as your sentry.
> 如果你希望成功，当以恒心为良友，以经验为参谋，以谨慎为兄弟，以希望为哨兵。

> 乃问于天师日：余闻上古之人，春秋皆度百岁，而动作不衰；今时之人，年半百而动作皆衰者，时世异耶？人将失之耶？岐伯对日：上古之人，其知道者，法于阴阳，和于术数，食饮有节，起居有常，不妄作劳，故能形与神俱，而尽终其天年，度百岁乃去。今时之人不然也，以酒为浆，以妄为常，醉以入房，以欲竭其精，以耗散其真，不知持满，不时御神，务快其心，逆于生乐，起居无节，故半百而衰也。

**最近发布的博文**:

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>



