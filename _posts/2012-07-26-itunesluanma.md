---
layout: post
title: "告别iTunes歌曲导入乱码"
description: ""
category: 苹果
tags: [OSX]
---
{% include JB/setup %}

这篇文章来自于我开始接触使用MBP后的一点心得，如果你正在看这篇文章，那么希望能对你有所帮助:)  － 悠木

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
       
当碰见需要转换APE或是FLAC此类的高音质无损音乐文档时， 用XLD是一个不错的选择，不过通过终端用其它方法该怎么做呢？

## 通过终端转换APE/FLAC无损音频文档

下载并编译安装「ffmpeg」.
OSX上用macport搞定就可以了，然后使用：
        <pre><code>
         1. ffmpeg -i  x.ape x.wav //转换APE/FLAC为wav格式
         2. lame -b 320  x.wav x.mp3 //将转换好的wav再转为mp3格式
        </code></pre>

通常情况下就做到这里就转好了，但是此时的音频文件是一个整的，APE与FLAC文档其实都伴随有cue文档，cue文档里存放着歌曲的信息，利用这个文档，通过终端，就可以对之前转好的mp3文档进行分割。

## 通过终端切割x.mp3文档
下载并编译安装「mp3splt」.
然后使用:
       <pre><code>
         mp3splt  -c x.cue x.mp3 //分割x.mp3文档
       </code></pre>

这步完成之后，我们的音乐文件名与歌曲就自动的一首首的被分割好了，赶快打开iTunes:)吧

BTW，偶尔，我们会遇见被分割出来的mp3文件也是乱码，但正如这篇文章的标题所诉，我们旨在告别iTunes歌曲里的乱码，所以接下来...

## 通过终端转码x.cue文档
最后使用：
       <pre><code>
       enconv -L zh_CN -x UTF-8 x.cue //将cue文档格式转换为UTF-8后再进行分割
       </code></pre>

到此，就大功告成拉！
PS: 一般情况下，别忘了iTunes自带的 'Convert ID3 Tags'，虽然这不是特别的好使。