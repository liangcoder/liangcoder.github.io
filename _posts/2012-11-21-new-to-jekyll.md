---
layout      : post
title       : 学习jekyll
description : Try to learn the jekyll
category    : thinking
tags        : [Jekyll Bootstrap, learning]
comments    : true
---
{% include JB/setup %}

### 0. 段落

还又点晕，先借助Jekyll Bootstrap开始起步，发第一篇post,确实很晕。增加一个超连接[我的主页](http://liangcoder.github.com)  
测试长度 测试长度 测试长度 测试长度 测试长度 测试长度 测试长度 测试长度 测试长度 测试长度  
return

### 1. 代码

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

暂时使用[photry.com](http://www.photry.com/ "photry.com")保存博客中使用的所有图片，实例如下  

![chair](http://photry-production-singapore.s3.amazonaws.com/743/954/35678/large.jpeg?AWSAccessKeyId=AKIAIFWXMUQTJZO2WGXA&Expires=1354591988&Signature=xzyLyn4amuRSx%2BGRj7CyS%2BUoWYA%3D "chair") 
![chair][chairImage]  

### 4. 超链接

这是一本很棒的书
[Java语言精粹](http://www.oreilly.com.cn/index.php?func=book&isbn=978-7-121-13309-1 "Java语言精粹")  
我喜欢的网站[Google][1] [GitHub][2]

[1]: http://www.google.com "google"
[2]: http://github.com "github"

[chairImage]: http://photry-production-singapore.s3.amazonaws.com/743/954/35678/large.jpeg?AWSAccessKeyId=AKIAIFWXMUQTJZO2WGXA&Expires=1354591988&Signature=xzyLyn4amuRSx%2BGRj7CyS%2BUoWYA%3D "chair"

