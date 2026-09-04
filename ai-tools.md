---
layout: page
title: 工具使用筆記
hide_title: true
permalink: /ai-tools/
description: "Vera 實際使用過的 AI 工具與工作方式：為什麼使用、拿來做什麼、遇過哪些限制，以及現在如何選擇。"
---
<header class="page-intro"><div><p class="eyebrow">不是排行榜，是實際使用紀錄</p><h1>工具使用筆記</h1><p class="page-lead">我不比較哪個工具一定最好，而是記錄自己為什麼使用、拿它完成什麼、遇過哪些限制，以及後來如何調整。</p></div><img src="{{ '/assets/images/ai-tools-illustration.jpg' | relative_url }}" alt="Vera 使用 AI 工具的插畫" class="page-intro-image"></header>
<section class="tool-guidance"><h2>我選工具時在意的事</h2><div class="mini-grid"><p><strong>任務適不適合</strong><span>能完成不代表流程最省力。</span></p><p><strong>結果能不能驗證</strong><span>重要資料不能只看表面成功。</span></p><p><strong>限制能不能接受</strong><span>包含權限、額度、模型與平台變動。</span></p></div></section>
<section class="tool-status" aria-labelledby="tool-note-title"><p class="eyebrow">第一篇工具筆記</p><h2 id="tool-note-title">ChatGPT：先把情境說清楚，再一起拆解</h2><p>我使用 ChatGPT，不只是為了快速取得答案，更常把它當成整理資訊、釐清問題與檢查盲點的協作夥伴。這篇記錄我怎麼開始、怎麼判斷，以及哪些事仍然要由自己負責。</p><a class="button button-primary" href="{{ '/ai-tools/chatgpt/' | relative_url }}">閱讀 ChatGPT 使用筆記</a></section>
<section class="tool-status" aria-labelledby="related-cases-title"><p class="eyebrow">工具放回真實情境</p><h2 id="related-cases-title">相關實踐案例</h2><p>工具本身不是主角。以下案例保留我為什麼選擇它、遇過哪些限制，以及最後如何調整。</p><div class="case-list compact">{% for post in site.posts %}{% if post.tools %}<article class="case-card"><div class="article-meta"><span>{{ post.tools | join: "、" }}</span><time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%Y.%m.%d" }}</time></div><h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3><p>{{ post.description }}</p></article>{% endif %}{% endfor %}</div></section>
