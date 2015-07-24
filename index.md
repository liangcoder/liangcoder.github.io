---
layout    : page
---
{% include JB/setup %}

<div class="blogrss">
  <a target="_blank" href="{{ BASE_PATH }}atom.xml"><img width="32" height="32" src="/assets/storage/image/rss.png"/></a>
</div>

### Posts

<ul>
  {% for post in site.posts %}
    <li>
      <span>{{ post.date | date: "%Y-%m-%d" }}</span> &raquo; 
      <a target="_blank" href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>

### Categories
<ul>
  {% for category in site.categories %} 
    <li>
      <a target="_blank" href="{{ BASE_PATH }}categories.html#{{ category[0] }}-ref">{{ category[0] }}</a>
    </li>
  {% endfor %}
</ul>

### Tags
<ul class="tag_box inline">
  {% for tag in site.tags %} 
    <li>
      <a target="_blank" href="{{ BASE_PATH }}tags.html#{{ tag[0] }}-ref">{{ tag[0] }}</a>
    </li>
  {% endfor %}
</ul>
