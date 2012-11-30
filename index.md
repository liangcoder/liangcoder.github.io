---
layout    : page
title     : 学的是技术 写的是思想
tagline   : programmer
---
{% include JB/setup %}

### Blog List
  
<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>

### 学技术

    public class Programmer {

      private String name;
      private int age;
      private char sex;

      public Programmer(){
        name = "David Liang";
        age = 28;
        sex = 'M';
      }

      public void post(String content){
        System.out.println(String.format("%s is posed by %s", content, name));
      }
    }

### 写思想

缩进格式还好，但没有语法高亮，很遗憾。


