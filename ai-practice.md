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
<nav class="topic-nav" aria-label="篩選案例主題">
  <button type="button" data-topic-filter="所有案例" aria-pressed="true">所有案例</button>
  <button type="button" data-topic-filter="工作流程與自動化" aria-pressed="false">工作流程與自動化</button>
  <button type="button" data-topic-filter="人資與資料處理" aria-pressed="false">人資與資料處理</button>
  <button type="button" data-topic-filter="AI 專案與內容製作" aria-pressed="false">AI 專案與內容製作</button>
  <button type="button" data-topic-filter="排錯與踩坑" aria-pressed="false">排錯與踩坑</button>
</nav>
<section class="case-section" id="所有案例">
  <h2 id="case-list-title" aria-live="polite">所有案例</h2><div class="case-list">
  {% for post in site.posts %}
    <article class="case-card" data-case-topics="{{ post.topic | default: '實踐案例' }}{% if post.tags contains '踩坑紀錄' %}|排錯與踩坑{% endif %}"><div class="article-meta"><span>{{ post.topic | default: "實踐案例" }}</span><time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%Y.%m.%d" }}</time></div><h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3><p>{{ post.description | default: post.excerpt | strip_html | truncate: 110 }}</p>{% if post.tools %}<p class="tool-line">使用工具：{{ post.tools | join: "、" }}</p>{% endif %}<a class="text-link" href="{{ post.url | relative_url }}">閱讀案例 <span aria-hidden="true">→</span></a></article>
  {% endfor %}
  </div>
</section>
<script>
  (() => {
    const filters = document.querySelectorAll('[data-topic-filter]');
    const cards = document.querySelectorAll('[data-case-topics]');
    const title = document.getElementById('case-list-title');

    filters.forEach((filter) => {
      filter.addEventListener('click', () => {
        const selectedTopic = filter.dataset.topicFilter;

        filters.forEach((item) => item.setAttribute('aria-pressed', String(item === filter)));
        cards.forEach((card) => {
          const topics = card.dataset.caseTopics.split('|');
          card.hidden = selectedTopic !== '所有案例' && !topics.includes(selectedTopic);
        });
        title.textContent = selectedTopic;
      });
    });
  })();
</script>
