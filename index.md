---
layout    : page
---
{% include JB/setup %}

## 学技术

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

## 写思想

缩进格式还好，但没有语法高亮，很遗憾。

### 博客列表

<ul class="posts">
  {% for post in site.posts %}
    <li style="font-size:110%;">
      <span>{{ post.date | date: "%Y-%m-%d" }}</span> &raquo; 
      <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>

