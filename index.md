---
layout: page
permalink: /
body_class: home
og_title: "Vera｜用 AI，陪伴成長"
description: "沒有技術背景，也可以開始把 AI 用進真實工作。Vera 記錄與 AI 一起拆解問題、嘗試、驗證與修正的真實過程。"
---

<section class="home-hero">
  <div class="home-hero-copy">
    <p class="eyebrow">從真實問題開始，慢慢找到自己的方法</p>
    <h1>沒有技術背景，<br>也可以開始把 AI 用進真實工作。</h1>
    <p class="hero-lead">我是 Vera。我從不懂 AI 開始，透過一個個工作問題，學著與 AI 一起拆解、嘗試、驗證與修正。</p>
    <p>這裡沒有標準答案，只有真實的使用過程，以及過程中形成的判斷。</p>
    <div class="button-row">
      <a class="button button-primary" href="{{ '/ai-practice/' | relative_url }}">從實踐案例開始</a>
      <a class="button button-secondary" href="{{ '/ai-thinking/' | relative_url }}">了解我的 AI 協作方式</a>
    </div>
  </div>
  <img src="{{ '/assets/images/homepage-illustration.jpg' | relative_url }}" alt="Vera 用 AI 陪伴自己思考與成長的插畫" class="home-hero-image">
</section>

<section class="home-section problem-section" aria-labelledby="problems-title">
  <p class="eyebrow">從你現在遇到的問題開始</p>
  <h2 id="problems-title">你也有這些問題嗎？</h2>
  <div class="problem-grid">
    <a class="problem-card" href="{{ '/ai-practice/' | relative_url }}#工作流程與自動化">
      <span class="card-index">01</span><h3>想用 AI 處理工作，卻不知道怎麼開始？</h3>
      <span class="text-link">看工作實踐案例 <span aria-hidden="true">→</span></span>
    </a>
    <a class="problem-card" href="{{ '/ai-thinking/' | relative_url }}#怎麼判斷-ai-的答案">
      <span class="card-index">02</span><h3>AI 給了答案，但不知道能不能相信？</h3>
      <span class="text-link">看判斷與驗證方法 <span aria-hidden="true">→</span></span>
    </a>
    <a class="problem-card" href="{{ '/ai-tools/' | relative_url }}">
      <span class="card-index">03</span><h3>工具很多，不知道哪一個適合自己？</h3>
      <span class="text-link">看工具使用筆記 <span aria-hidden="true">→</span></span>
    </a>
  </div>
</section>

<section class="home-section" aria-labelledby="featured-title">
  <div class="section-heading-row">
    <div><p class="eyebrow">真實案例，不只展示成果</p><h2 id="featured-title">從這三篇開始</h2></div>
    <a class="text-link desktop-link" href="{{ '/ai-practice/' | relative_url }}">查看所有案例 <span aria-hidden="true">→</span></a>
  </div>
  <p class="section-intro">保留問題怎麼發生、中間怎麼調整，以及最後如何判斷。</p>
  <div class="featured-grid">
    {% assign featured_slugs = "payroll-skill-development,attendance-exception-automation,labor-cost-scheduling-failure" | split: "," %}
    {% for slug in featured_slugs %}
      {% assign post = site.posts | where: "slug", slug | first %}
      {% if post %}
      <article class="article-card">
        <div class="article-meta"><span>{{ post.topic }}</span><time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%Y.%m.%d" }}</time></div>
        <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
        <p>{{ post.description }}</p>
        <a class="text-link" href="{{ post.url | relative_url }}">閱讀案例 <span aria-hidden="true">→</span></a>
      </article>
      {% endif %}
    {% endfor %}
  </div>
  <a class="text-link mobile-link" href="{{ '/ai-practice/' | relative_url }}">查看所有案例 <span aria-hidden="true">→</span></a>
</section>

<section class="home-section principles-section" aria-labelledby="principles-title">
  <div class="principles-intro">
    <p class="eyebrow">不是請 AI 替我決定</p><h2 id="principles-title">我怎麼與 AI 一起工作</h2>
    <p>AI 可以協助整理資訊、拆解問題與提供不同角度，但判斷與決定仍然在自己手上。</p>
    <a class="button button-light" href="{{ '/ai-thinking/' | relative_url }}">閱讀完整協作思維</a>
  </div>
  <ol class="principle-list">
    <li><strong>把真實情境說清楚</strong><span>除了問題，也提供背景、限制及真正想完成的事。</span></li>
    <li><strong>不把答案直接當成事實</strong><span>AI 提供的是方向，仍要回到自己的情境判斷。</span></li>
    <li><strong>能驗證，就不要只靠猜</strong><span>找出可以比較的基準，實際檢查輸入與結果。</span></li>
    <li><strong>方法能用，不代表最適合</strong><span>依實際需求調整工具，不要求自己一次選對。</span></li>
  </ol>
</section>

<section class="home-section" aria-labelledby="latest-title">
  <p class="eyebrow">持續累積中的真實紀錄</p><h2 id="latest-title">最近記錄</h2>
  <div class="latest-list">
    {% for post in site.posts limit: 4 %}
    <a class="latest-item" href="{{ post.url | relative_url }}">
      <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%Y.%m.%d" }}</time>
      <span class="latest-topic">{{ post.topic | default: "實踐案例" }}</span><strong>{{ post.title }}</strong><span class="latest-arrow" aria-hidden="true">→</span>
    </a>
    {% endfor %}
  </div>
</section>

<section class="home-section about-strip" aria-labelledby="about-title">
  <img src="{{ '/assets/images/profile-photo.jpg' | relative_url }}" alt="Vera" class="about-photo">
  <div><p class="eyebrow">關於 Vera</p><h2 id="about-title">我也曾經因為不懂，不知道該從哪裡開始。</h2>
    <p>我沒有 IT 或程式背景。真正帶來改變的，不是等到全部學會，而是先動手做，在過程中遇到問題、提出問題，再一步一步找到方法。</p>
    <a class="text-link" href="{{ '/about/' | relative_url }}">認識 Vera <span aria-hidden="true">→</span></a>
  </div>
</section>
