---
layout: post
title: "告别iTunes歌曲导入乱码"
description: ""
category: 苹果
tags: [OSX]
---
{% include JB/setup %}

## 导入mp3出现????.mp3乱码时

下载「mutagen」，在按照readme里的提示安装.
然后使用:
        <pre><code>
        mid3iconv -e gbk *.mp3 //转换当前目录不包括子目录
        find .-iname "*.mp3" -execdir mid3iconv -e gbk{}\ //转换当前目录含子目录
        </code></pre>
在实际操作时，会遇到ID3V1不支持中文的Unicode编码,转换后的ID3V1就是会全是问号
此时可以用:
        <pre><code>
        mid3iconv -e gbk --remove-v1 *.mp3 //加上--remove-v1参数的方式转换
        </code></pre>