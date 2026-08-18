# Vera 個人網站 — 使用說明

這份說明是給 Vera 自己看的操作指南，不會出現在網站上。

## 這是什麼

這是用 Jekyll 建立的個人網站專案，設計給 GitHub Pages 免費上線。妳不需要自己安裝任何東西、也不需要自己「build」網站——只要把檔案放到 GitHub 上，GitHub 會自動幫妳把這些檔案變成真正的網站。

## 第一次上線的步驟

1. 到 GitHub 建立一個新的 repository（專案空間），名稱必須完全是：`WS-Vera.github.io`
2. 把這個資料夾裡的所有檔案上傳到那個 repository（可以直接在 GitHub 網頁上用「Upload files」拖曳上傳，不需要用指令）
3. 到 repository 的 Settings → Pages，確認 Source 設定為 `Deploy from a branch`，Branch 選 `main`，資料夾選 `/ (root)`，儲存
4. 等 1～2 分鐘，網站就會自動在 https://ws-vera.github.io 上線

## 之後要新增一篇「我的AI實踐」文章

1. 打開 `_templates/post-template.md`，複製一份
2. 把複製的檔案放到 `_posts/` 資料夾裡
3. 檔名改成：`YYYY-MM-DD-文章標題.md`（例如：`2026-08-20-第一次用AI整理出勤異常.md`）
4. 打開檔案，把最上面的 title、date、tags 改成這篇的內容，下面開始寫真實內容
5. 存檔，上傳到GitHub（覆蓋/新增這個檔案），等1～2分鐘網站會自動更新

## 之後要新增一個「AI工具」介紹

1. 打開 `_templates/tool-template.md`，複製一份
2. 把複製的檔案放到 `_tools/` 資料夾裡，檔名用工具名稱（例如：`claude-code.md`）
3. 打開檔案，依照裡面的六個小標題填寫內容
4. 存檔上傳，等網站自動更新

## 之後要調整首頁／關於Vera等文字

直接打開對應的檔案修改文字：

- 首頁 → `index.md`
- 關於Vera → `about.md`
- AI思維 → `ai-thinking.md`
- AI工具介紹頁 → `ai-tools.md`
- 我的AI實踐列表頁 → `ai-practice.md`

## 網站視覺風格在哪裡調

`assets/css/style.css` 檔案最上面有幾個顏色設定（--bg背景色、--accent重點色等），要換顏色改這裡就好，不用動其他檔案。

## 目前是V1範圍

這個版本刻意先不做：AI即時聊天、自動回答訪客問題、會員系統、複雜自動化、個人化推薦、大量AI工具比較。這些之後有需要再逐步加入。
