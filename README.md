# 宅宅勇者大冒險 RPG 遊戲官方網站

一個以 Vanilla HTML / CSS / JavaScript 建構的 RPG 遊戲主題宣傳網站。

**Live Demo：** [zu109520-arch.github.io/irasutoya-rpg](https://zu109520-arch.github.io/irasutoya-rpg)
[![宅宅勇者大冒險](https://github.com/user-attachments/assets/58bffdc0-82a5-47bb-b867-36613cd3e724)](https://zu109520-arch.github.io/irasutoya-rpg/)

---

## 設計理念

本專案刻意不使用任何前端框架，目的是展示在沒有 React 的情況下，運用原生 JavaScript 處理 DOM 操作、事件監聽、表單驗證與互動動畫的基礎能力。

---

## 專案特色

- 以原生 HTML / CSS / JavaScript 實作，不依賴任何前端框架
- 角色補血互動功能，點擊飯糰回復 HP，搭配動態血條動畫
- Toast 通知系統取代瀏覽器原生 alert，提升使用者體驗
- Email 格式驗證（Regex）結合事前登錄表單，模擬實際互動流程
- RWD 響應式設計，支援手機與桌機瀏覽
- 平滑滾動導覽列，提升頁面操作流暢度

---

## 技術亮點

**DOM 操作與動態樣式**
- 點擊飯糰時透過 `getElementById` 取得血條元素，動態更新 `style.width`
- 使用 `Math.min` 確保 HP 不超過 100%，滿血時觸發 Toast 提示

**Toast 通知系統**
- 用 CSS class 切換搭配 `opacity` 與 `transform` 製作淡入淡出動畫
- 取代會中斷使用者操作的原生 `alert`，2.5 秒後自動消失

**平滑滾動導覽**
- 透過 `querySelectorAll` 抓取所有錨點連結並批次綁定事件
- 使用 `e.preventDefault()` 阻止預設跳轉，改以 `scrollIntoView({ behavior: 'smooth' })` 實現平滑滾動

**Regex 表單驗證**
- 使用 `/^[^\s@]+@[^\s@]+\.[^\s@]+$/` 驗證 Email 格式
- 成功 / 失敗即時顯示對應訊息，提升使用者操作回饋

**RWD 響應式設計**
- 使用 CSS Grid 排列角色卡與平台卡，搭配 `@media (max-width: 768px)` 自動切換為單欄
- 確保跨裝置瀏覽體驗一致

---

## 技術架構

| 類別 | 技術 |
|------|------|
| 結構 | HTML5 |
| 樣式 | CSS3（Flexbox / Grid / CSS 變數） |
| 互動 | Vanilla JavaScript |

---

## 主要功能

**導覽列**
- 固定式導覽連結，點擊平滑滾動至對應區塊

**劇情介紹**
- 遊戲世界觀與故事背景說明

**登場人物**
- 三位角色卡片展示，各有獨立 HP 血條
- 點擊飯糰圖示補血，血條動態更新，滿血時顯示 Toast 提示

**遊戲動畫**
- PV 預告片佔位區塊，含 hover 互動效果

**販售資訊**
- PS5 / Nintendo Switch 雙平台封面展示

**事前登錄**
- Email 格式 Regex 驗證，成功 / 失敗即時回饋

---

## 本機執行

下載後直接用瀏覽器開啟 `index.html` 即可。