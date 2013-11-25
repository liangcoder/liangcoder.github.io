---
layout    : page
---
{% include JB/setup %}

<div class="blogrss">
  <a target="_blank" href="{{ BASE_PATH }}atom.xml"><img width="32" height="32" src="/assets/storage/image/rss.png"/></a>
</div>

### 博客列表

<ul>
  {% for post in site.posts %}
    <li>
      <span>{{ post.date | date: "%Y-%m-%d" }}</span> &raquo; 
      <a target="_blank" href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>

### 1. 博客分类
<ul>
  {% for category in site.categories %} 
    <li>
      <a target="_blank" href="{{ BASE_PATH }}categories.html#{{ category[0] }}-ref">{{ category[0] }}</a>
    </li>
  {% endfor %}
</ul>

### 2. 博客标签
<ul class="tag_box inline">
  {% for tag in site.tags %} 
    <li>
      <a target="_blank" href="{{ BASE_PATH }}tags.html#{{ tag[0] }}-ref">{{ tag[0] }}</a>
    </li>
  {% endfor %}
</ul>

### 3. 学技术

{% highlight java linenos %}

    public class Programmer {

      private String name;

      public Programmer() {
        name = "David Liang";
      }

      public void post(String content) {
        System.out.println(String.format("%s is posted by %s", content, name));
      }

      @Override
      public String toString() {
        return String.format("name=[%s]", name);
      }
    }

{% endhighlight %}

### 4. 写思想

代码不仅是解决问题的工具，而且是代码编写人员思想的表达。  

