---
layout    : page
---
{% include JB/setup %}

### 0. 学技术

{% highlight java linenos %}

    public class Programmer {

      private String name;
      private int age;
      private char sex;

      public Programmer() {
        name = "David Liang";
        age = 28;
        sex = 'M';
      }

      public void post(String content) {
        System.out.println(String.format("%s is posed by %s", content, name));
      }

      @Override
      public String toString() {
        return String.format("name=[%s], age=[%s], sex=[%s]", name, age, sex);
      }
    }

{% endhighlight %}

### 1. 写思想

缩进格式还好，语法高亮和行数搞定，很8错，very nice!  
加了一个return-top button 这个，还是很重要滴哦！  
但，真的是不敢在windows平台下看，可能会很糟糕。  

**最重要的是：右上角的[fork me on GitHub](https://github.com/liangcoder/liangcoder.github.com)!**

### 2. 博客列表

<ul class="posts" style="margin-top:10px;">
  {% for post in site.posts %}
    <li style="font-size:110%;">
      <span>{{ post.date | date: "%Y-%m-%d" }}</span> &raquo; 
      <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>

