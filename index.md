---
layout: page
title: 木有意思
tagline: 思考•阅读•生活•苹果•心情•Web
---
{% include JB/setup %}

> 您好,这里是yomuse的个人网站,无论是什么原因让您看到这个页面,您都会同时收获一份来自我的祝福.
> 虽然有时会觉得这个世界有些糟糕,但是作为立场:"我始终相信这个世界的美好!"
> 所以,我会在空闲的时候把自己的一些心情和关乎其它的东东记录在这里.无论文字风格的严谨或戏谑,愉悦或感怀...
> 我只是以为它们都是关于"美好"的存在.
> 这个网站的"光影境"是记录自己一些习作的地方,使用的工具主要是PS和AI."水清浅"是记录时光的地方,你可以当它是一个相册.
> 另外还有"棱镜π"这样一个关于自己其它习作或是技术类话题分享的地方.
> 这三块栏目的平台目前分别来自Lofter,点点与FarBox.最后感谢您的关注. by yomuse

**最近发布的文章**:

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>



