# Vera 個人網站 — 使用說明

這份說明是給 Vera 自己看的操作指南，不會出現在網站上。專案全貌與目前狀態見[_docs/網站全景架構.md](_docs/網站全景架構.md)；後續工作見[_docs/網站任務清單.md](_docs/網站任務清單.md)；重要修改見[_docs/網站工作日誌.md](_docs/網站工作日誌.md)。

## 這是什麼

這是用 Jekyll 建立的個人網站專案，設計給 GitHub Pages 免費上線。妳不需要自己安裝任何東西、也不需要自己「build」網站——只要把檔案放到 GitHub 上，GitHub 會自動幫妳把這些檔案變成真正的網站。

## 目前網站怎麼更新

網站專案已連到 GitHub repository `Vera-With-AI/Vera-With-AI.github.io`。修改本機檔案後，需要將變更提交並推送到 GitHub；GitHub Pages 建置成功後，再到 https://vera-with-ai.github.io 檢查實際頁面。預排文章另有每日重新建置設定；是否如期顯示，仍以公開頁面與 GitHub Actions 紀錄為準。

## 之後要新增一篇「我的AI實踐」文章

1. 打開 `_templates/post-template.md`，複製一份
2. 把複製的檔案放到 `_posts/` 資料夾裡
3. 檔名改成：`YYYY-MM-DD-文章標題.md`（例如：`2026-08-20-第一次用AI整理出勤異常.md`）
4. 打開檔案，把最上面的 title、date、tags 改成這篇的內容，下面開始寫真實內容
5. 檢查文章日期、摘要、圖片、內部連結及隱私內容，存檔後提交並推送到 GitHub；確認建置成功與公開頁面內容

## 之後要補充「工具使用筆記」

目前保留公開的 `ai-tools.md` 總覽頁，工具經驗主要記錄在相關實踐文章中；不規劃 ChatGPT、Claude、Gemini 的獨立介紹頁。若有新的實際經驗，優先更新相關文章或總覽頁。

## 之後要調整首頁／關於Vera等文字

直接打開對應的檔案修改文字：

- 首頁 → `index.md`
- 關於Vera → `about.md`
- AI思維 → `ai-thinking.md`
- AI工具介紹頁 → `ai-tools.md`
- 我的AI實踐列表頁 → `ai-practice.md`
- 聯絡頁 → `contact.md`
- 隱私與網站說明 → `privacy.md`

搜尋引擎與錯誤頁相關檔案：

- 搜尋引擎檢索規則 → `robots.txt`
- 網站地圖 → `sitemap.xml`
- 找不到頁面 → `404.md`

## 網站視覺風格在哪裡調

`assets/css/style.css` 檔案最上面有幾個顏色設定（--bg背景色、--accent重點色等），要換顏色改這裡就好，不用動其他檔案。

## 目前是V1範圍

這個版本刻意先不做：AI即時聊天、自動回答訪客問題、會員系統、複雜自動化、個人化推薦、大量AI工具比較。這些之後有需要再逐步加入。
