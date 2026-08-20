---
layout: page
title: 我的AI實踐
permalink: /ai-practice/
accent: navy
---

<img src="{{ '/assets/images/ai-practice-illustration.jpg' | relative_url }}" alt="我的AI實踐插畫" class="hero-image">

真實事件、真實嘗試、踩坑紀錄與思考過程。

## 全部文章

{% if site.posts.size > 0 %}
{% for post in site.posts %}
- [{{ post.title }}]({{ post.url | relative_url }}) — {{ post.date | date: "%Y-%m-%d" }}
{% endfor %}
{% else %}
目前還沒有文章，敬請期待。
{% endif %}

## 依標籤瀏覽

{% for tag in site.tags %}
### {{ tag[0] }}

{% for post in tag[1] %}
- [{{ post.title }}]({{ post.url | relative_url }})
{% endfor %}

{% endfor %}
