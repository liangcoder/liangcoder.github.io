---
layout      : post
title       : 重新上路，从C开始
description : A new step as a coder.
category    : daily
tags        : [daily]
---
{% include JB/setup %}

## 1. 重新上路，从C开始

再次翻开《C Primer Plus》已经是第六版，上一次阅读这本书的时候还是2005年的暑假。那时候大一刚结束，而之前的“C语言程序设计”课程完全没有学明白，勉强考了个及格60分糊弄过去了，考试卷子上涉及指针的题目全都不会的那种。

可是接下来的几门专业课程都是以C语言作为工具，例如数据结构与算法，操作系统还有计算机网络。所以当时趁着暑假的时间啃了这本优秀的书籍，算是亡羊补牢，为时未晚（但依然没有学透）。

在这里要强调一下谭浩强的《C语言程序设计》这本书绝对是垃圾，不接受反驳。

转眼间二十年过去了，情不自禁的又想再读一读这本经典佳作，顺便找回一下作为一名程序员的初心。

## 2. MacOS环境使用iTerm和Visual Studio Code

MacOS环境自带了Apple Clang编译器可以用来编译C语言，其对C标准支持的很好，比如C99和C11。

Visual Studio Code IDE 来自Microsoft，支持多种编程语言的IDE，可以结合iTerm使用同时也提供了丰富的Extensions, 学习C语言需要安装C/C++ Extensions基本就够了，额外再安装一个CodeRunner用来快捷运行C程序，后者输出运行结果更友好一些：

{% highlight shell %}

[Running] cd "/Users/david/workspace/c_primer_plus/chapter_2/" && gcc first.c -o first && "/Users/david/workspace/c_primer_plus/chapter_2/"first
I am a simple computer.
My favorite number is 1, because it is first not.

[Done] exited with code=0 in 0.547 seconds

{% endhighlight %}

![book][c_primer_plus_image] 

## Reference

* [Developing C programs on Mac OS](https://www.cs.auckland.ac.nz/~paul/C/Mac/ "Developing C programs on Mac OS")
* [C language documentation from Visual Studio](https://learn.microsoft.com/en-us/cpp/c-language/?view=msvc-170 "C language documentation from Visual Studio")

[c_primer_plus_image]: /assets/storage/image/c_primer_plus.png "c_primer_plus"
