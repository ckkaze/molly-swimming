# Molly Swimming 專案開發紀錄 (GEMINI.md)

## 📌 專案概觀
本專案為「梓嫣 (Molly) 的游泳紀錄站」，旨在取代原本的 Google Sites，提供更美觀、自主性更高且具備資料管理功能的網頁。

## 🛠️ 技術規格
- **前端架構**: 純 HTML5 / CSS3 / Vanilla JavaScript。
- **樣式框架**: Tailwind CSS (透過 CDN)。
- **託管平台**: GitHub Pages (網址: https://ckkaze.github.io/molly-swimming/)。
- **後端 API**: Google Apps Script (GAS)。
- **資料庫**: Google Sheets (試算表 ID: `1bahk0hVUzXh6eZ70Dc0PeYi3dPUGX1EEJbGMJOxW4IY`)。

## 🔗 關鍵連結
- **GAS 執行網址**: `https://script.google.com/macros/s/AKfycbzHyxGXTpoxYrQP_wwOBj15-LmMJ9P-Esh15MROo3yiD6yCm8H2BwkmxK4mJ4pT9PnU/exec`
- **本地路徑**: `D:\Work\GeminiSpace\molly-swimming`

## 📁 檔案結構與規則
- `/assets/images/`: 存放賽事照片。子資料夾命名規則為 `event_YYYY_名稱_季節`。
- `/css/styles.css`: 客製化樣式。
- `/js/app.js`: 全域邏輯。
- `Code.gs`: 存放於根目錄，但已加入 `.gitignore`，僅供本地備份，不上傳 GitHub。
- `.gitignore`: 已設定排除 `*.mp4`, `*.mov` 等影片大檔及 `Code.gs`。

## 🚀 已完成功能
1. **首頁 (index.html)**: 響應式 Hero 區塊、教練的話、最新摘要。
2. **賽事紀錄 (events.html)**: 2024-2026 各大賽事藝廊排版，直接連結本地圖檔。
3. **成績查詢 (records.html)**: 
    - 串接 GAS API 取得試算表即時資料。
    - **篩選功能**: 支援賽事、項目的模糊查詢。
    - **排序功能**: 支援日期（智慧排序）、賽事、項目、成績的遞增/遞減。
    - **新增功能**: 內建表單可直接寫入 Google Sheets，且已修正「時間格式」在 Sheet 中被誤轉的問題。

## 📝 後續維護提醒
- 修改 `Code.gs` 後，必須在 Google 網頁端選擇「新版本」部署，否則 API 不會生效。
- 新增照片後，使用 GitHub Desktop 進行 Commit & Push 即可更新網站。
- 影片檔建議上傳至雲端後以 `iframe` 嵌入，不要直接放入專案目錄上傳。
