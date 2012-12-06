---
layout      : post
title       : 学习jekyll
description : Try to learn the jekyll
category    : thinking
tags        : [Jekyll Bootstrap, learning]
comments    : true
---
{% include JB/setup %}

### 标题3 heading 3


段落  
还又点晕，先借助Jekyll Bootstrap开始起步，发第一篇post,确实很晕。增加一个超连接[我的主页](http://liangcoder.github.com)测试长度 测试长度 测试长度 测试长度 测试长度 测试长度 测试长度 测试长度 测试长度 测试长度  
return  

Sometimes APNs might attempt to deliver notifications for an application on a device, but the device may repeatedly refuse delivery because there is no target application. This often happens when the user has uninstalled the application. In these cases, APNs informs the provider through a feedback service that the provider connects with. The feedback service maintains a list of devices per application for which there were recent, repeated failed attempts to deliver notifications. The provider should obtain this list of devices and stop sending notifications to them

### 1. 代码

Here is a "Hello world" program in Java.

{% highlight java linenos %}

	for(int i = 0; i < 100; i++){
		Sysout.out.println("Hello, world.");
	}

{% endhighlight %}

### 2. 文字

文字在这里here is string *em文字* **strong文字**

1. 列表1
2. 列表2

* 列表3
* 列表4

> java
>
> ruby
>
> scala
>
> lua

### 3. 图片

博客中使用的图片，实例如下  

thumb
![chair](/assets/storage/image/thumb/chair.jpg "chair")

原图
![chair][chairImage]  

### 4. 超链接

这是一本很棒的书
[Java语言精粹](http://www.oreilly.com.cn/index.php?func=book&isbn=978-7-121-13309-1 "Java语言精粹")  
我喜欢的网站[Google][1] [GitHub][2]

[1]: http://www.google.com "google"
[2]: http://github.com "github"

[chairImage]: /assets/storage/image/chair.jpg "chair"

