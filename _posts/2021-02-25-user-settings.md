---
layout      : post
title       : User Settings
description : user settings.
category    : daily
tags        : [daily]
---
{% include JB/setup %}


## 1. Java Development Enviroment Settings

安装 JDK8 之后发现其命令行提示信息都按照用户环境语言做了适配，而不是熟悉的英文，故特作以下配置保证其使用英文作为命令行提示信息，目标文件：.zshrc

{% highlight shell %}

export JAVA_TOOL_OPTIONS="-Duser.language=en"

{% endhighlight %}

## 2. iTerms2 

日常工具箱离不开 iTerms2，发现一篇不错的快捷键总结：[iTerms 快捷键](https://cnbin.github.io/blog/2015/06/20/iterm2-kuai-jie-jian-da-quan/)

## 3. JetBrains Mono

安装了新的编程字体：JetBrains Mono，并在 Sublime Text 和 iTerms 中使用：

{% highlight shell %}

"font_face": "JetBrains Mono"

{% endhighlight %}





