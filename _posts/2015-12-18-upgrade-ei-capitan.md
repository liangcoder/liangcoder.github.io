---
layout      : post
title       : EI Capitan Upgrade
description : upgrade Mac OS X to EI Capitan
category    : daily
tags        : [macos, jdk, daily]
---
{% include JB/setup %}

大约三天前，2015-12-15， 我升级了Mac OS X到最新版本10.11, 代号EI Captan。

虽然之前有听说升级后会导致CPU变成烽火轮等诸多副作用，但，还是没忍住点击了升级按钮，唯一的依仗就是机器比较新，相信Apple的兼容性！

升级过程耗时大约20分钟，完成后的第一感觉是字体显示效果提升显著，这个特性是相当棒！去官网了解下其它众新特性，说是Notes有显著提升，果断用起来记日常笔记。

与大约一年前[升级Yosemite](http://liangcoder.github.io/daily/2014/11/01/yosemite-install-jdk/)时遇到的场景一样，升级EI Capitan后，JDK6又不见了。只好翻出[博客](http://liangcoder.github.io/daily/2014/11/01/yosemite-install-jdk/)中的链接[Java for OS X 2015-001](http://support.apple.com/kb/DL1572?viewlocale=en_US&locale=en_US "Java for OS X 2015-001")重新下载安装，Apple做事还是很棒的，时隔一年虽然下载内容变更了（2014-001变更为了2015-001）但是下载链接还保持一致！

安装完成后运行以下命令确认JDK HOME位置：

{% highlight console %}

$ /usr/libexec/java_home -v 1.6
/Library/Java/JavaVirtualMachines/1.6.0.jdk/Contents/Home

$ /usr/libexec/java_home -v 1.7
/Library/Java/JavaVirtualMachines/jdk1.7.0_75.jdk/Contents/Home

{% endhighlight %}

这一点就更靠谱了，Apple终于把不同版本的JDK安装在了统一的/Library/Java/JavaVirtualMachines目录下，值得表扬！
