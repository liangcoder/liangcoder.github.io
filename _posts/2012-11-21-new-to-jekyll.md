---
layout      : post
title       : Learn Jekyll
description : Try to learn the jekyll
category    : thinking
tags        : [Jekyll Bootstrap, learning]
comments    : false
---
{% include JB/setup %}

Jekyll is a popular tools for transforming the plain text into static HTML based site, the Home pages of which can be accessed on [Jekyll](http://jekyllrb.com/).

## Basic steps to use Jekyll

- Install the Jekyll: gem install jekyll
- Enter the local web site directory.
- Start up the Jekyll server locally: jekyll serve

Access url locally is [http://localhost:4000](http://localhost:4000)

### Code Sample

Here is a "Hello world" program in Java.

{% highlight java linenos %}

for(int i = 0; i < 100; i++){
	Sysout.out.println("Hello, world.");
}

{% endhighlight %}

### Text Sample

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

### Image Sample

博客中使用的图片，实例如下  

thumb
![chair](/assets/storage/image/thumb/chair.jpg "chair")

原图
![chair][chairImage]  

### Hyperlink Sample

这是一本很棒的书
[Java语言精粹](http://www.oreilly.com.cn/index.php?func=book&isbn=978-7-121-13309-1 "Java语言精粹")  
我喜欢的网站[Google][1] [GitHub][2]

[1]: http://www.google.com "google"
[2]: http://github.com "github"

[chairImage]: /assets/storage/image/chair.jpg "chair"
