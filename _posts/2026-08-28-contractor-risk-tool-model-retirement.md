---
layout: post
title: "打開才發現，模型被下架了：承攬情境風險評估器的真實記錄"
date: 2026-08-28 12:00:00 +0800
tags: [AI工具, 踩坑紀錄]
---

## 起點不是計畫，是一個錯誤訊息

今天想起之前做的承攬情境風險評估器，重新打開測試，畫面卻顯示：「AI分析服務暫時無法使用。」

這個工具之前可以正常使用，我也沒有調整設定，卻突然無法運作。

## 查出原因：模型被下架了

去 Netlify 的 Function log 查錯誤訊息，看到這行：

```text
The model llama-3.3-70b-versatile does not exist or you do not have access to it.
```

原來Groq在2026年6月17日將這個模型下架了。我沒有注意到相關通知，直到工具報錯才發現底層模型已經無法使用。

這類服務變動不容易從網站畫面提前發現，通常要等工具出現錯誤後，再進一步查找原因。

## 換模型，遇到新問題

把模型名稱換成 Groq 建議的替代版本之後，錯誤訊息換了一個：

```text
SyntaxError: Unexpected token '<', "<think> He"... is not valid JSON
```

新模型的回應包含`<think>...</think>`標記，之後才接著輸出JSON結果；原本的程式只接受純JSON，因此解析失敗。

我嘗試修改幾個版本仍未解決，後來改由Cowork協助檢查實際輸出與解析流程，才排除問題。

## Netlify 額度用完

因為今天反覆測試與部署，Netlify的免費部署額度在下午用完。

畫面出現：「Production deploys are paused because your team has used all of its available credits for this billing cycle.」

當下無法繼續在原平台部署，我評估後決定改用另一個平台。

## 換到 Cloudflare Pages

Cloudflare Pages（一種免費的網站部署服務）同樣提供免費服務，而且這次沒有遇到部署次數限制。平台切換也透過Cowork完成，包括把程式碼從Netlify格式改成Cloudflare格式。

工具最後在這裡上線：[contractor-risk-tool.pages.dev](https://contractor-risk-tool.pages.dev)

這件事讓我體會到：工具完成後，不代表它會一直維持原狀。服務會更新、模型會停用，免費額度也可能改變。問題發生時，我能做的是逐步排查，再依實際狀況調整。
