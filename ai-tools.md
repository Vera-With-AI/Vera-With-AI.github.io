---
layout: page
title: AI工具
permalink: /ai-tools/
accent: caramel
description: "介紹 Vera 實際使用過的 AI 工具，不是排行榜，只是紀錄為什麼用、實際怎麼用、遇過什麼問題與踩坑心得。"
---

<img src="{{ '/assets/images/ai-tools-illustration.jpg' | relative_url }}" alt="AI工具插畫" class="hero-image">

介紹我實際使用過的 AI 工具——不是排行榜，只是紀錄我為什麼用、實際怎麼用、遇過什麼問題。

{% if site.tools.size > 0 %}
{% for tool in site.tools %}
- [{{ tool.title }}]({{ tool.url | relative_url }}){% if tool.last_reviewed %}（最後確認日期：{{ tool.last_reviewed }}）{% endif %}
{% endfor %}
{% else %}
目前還沒有工具介紹，敬請期待。
{% endif %}
