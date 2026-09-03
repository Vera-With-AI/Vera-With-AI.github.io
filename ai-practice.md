---
layout: page
title: 實踐案例
hide_title: true
permalink: /ai-practice/
description: "Vera 將 AI 用進人資、資料整理與日常工作流程的真實案例，完整記錄問題、嘗試、調整、驗證與最後的判斷。"
---
<header class="page-intro">
  <div><p class="eyebrow">真實事件、真實嘗試</p><h1>實踐案例</h1><p class="page-lead">這裡記錄我在工作與學習中，實際運用 AI 解決問題的過程。不只寫最後完成了什麼，也保留中間的判斷、調整與踩坑。</p></div>
  <img src="{{ '/assets/images/ai-practice-illustration.jpg' | relative_url }}" alt="Vera 的 AI 實踐案例插畫" class="page-intro-image">
</header>
<nav class="topic-nav" aria-label="案例主題"><a href="#所有案例">所有案例</a><a href="#工作流程與自動化">工作流程與自動化</a><a href="#人資與資料處理">人資與資料處理</a><a href="#ai-專案與內容製作">AI 專案與內容製作</a><a href="#排錯與踩坑">排錯與踩坑</a></nav>
<section class="case-section" id="所有案例">
  <h2>所有案例</h2><div class="case-list">
  {% for post in site.posts %}
    <article class="case-card"><div class="article-meta"><span>{{ post.topic | default: "實踐案例" }}</span><time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%Y.%m.%d" }}</time></div><h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3><p>{{ post.description | default: post.excerpt | strip_html | truncate: 110 }}</p>{% if post.tools %}<p class="tool-line">使用工具：{{ post.tools | join: "、" }}</p>{% endif %}<a class="text-link" href="{{ post.url | relative_url }}">閱讀案例 <span aria-hidden="true">→</span></a></article>
  {% endfor %}
  </div>
</section>
<section class="topic-overview" aria-labelledby="topic-title"><h2 id="topic-title">依問題探索</h2><div class="topic-grid">
  <div id="工作流程與自動化"><span>01</span><h3>工作流程與自動化</h3><p>重複性工作、排程與固定流程如何導入 AI，以及上線後才會遇到的真實問題。</p></div>
  <div id="人資與資料處理"><span>02</span><h3>人資與資料處理</h3><p>出勤、薪資、人力成本及 Excel 資料整理等實際工作案例。</p></div>
  <div id="ai-專案與內容製作"><span>03</span><h3>AI 專案與內容製作</h3><p>從工具開發、教材製作到把方法交給別人使用的過程。</p></div>
  <div id="排錯與踩坑"><span>04</span><h3>排錯與踩坑</h3><p>當設定失效、模型變動或結果異常時，如何找出問題並降低風險。</p></div>
</div></section>
