# Flooring Calculator (地板材料計算器)

[![Calculator Suite](https://img.shields.io/badge/Calculator%20Suite-Flooring%20Calculator-01696F?style=flat-square)](https://github.com/Jupiterlaw/calculator-suite)

地板材料面積計算器 — 支援多區域施工面積輸入、損耗率計算、自動換算包數。

> **現場第一線工具**：專為工地環境設計，大按鈕、大字體、高對比度，即使在陽光直射下也能清晰閱讀。

---

## 功能特色

- **多區域支援** — 動態新增/刪除區域，每個區域可獨立命名與設定尺寸
- **即時計算** — 修改任何數值立即更新結果，無需按按鈕
- **損耗率設定** — 可自訂損耗百分比（%），裁邊預留自動計算
- **包裝計算** — 根據每包片數與單片面積，自動計算所需包數（向上取整）
- **雙單位顯示** — 所有面積同時顯示平方米（m²）與平方呎（ft²）
- **暗色模式** — 跟隨系統設定自動切換亮/暗主題

---

## 快速開始

### 直接在瀏覽器使用

1. 打開 [GitHub Pages 連結](https://jupiterlaw.github.io/flooring-calculator/)（如有啟用）
2. 或直接下載 `index.html` 在瀏覽器開啟

### 本地使用

```bash
# 克隆倉庫
git clone https://github.com/Jupiterlaw/flooring-calculator.git

# 直接在瀏覽器打開 index.html
open index.html        # macOS
start index.html       # Windows
xdg-open index.html    # Linux
```

**無需任何依賴、無需構建、無需後端。** 一個 HTML 檔案，打開即用。

---

## 使用說明

### 基本設定
1. **地板產品資料**：輸入地板長度 (mm)、地板闊度 (mm)、每包片數
2. **損耗設定**：輸入損耗百分比（%），預設 0%

### 施工區域
3. 按 **「＋ 新增區域」** 添加施工區域
4. 每個區域可設定：
   - **區域名稱**（如「客廳」、「主人房」）
   - **長度（米）** 與 **闊度（米）**
5. 即時顯示每個區域的面積（m² 與 ft²）

### 結果
- **總施工面積** — 所有區域的面積總和
- **加損耗後面積** — 總面積 × (1 + 損耗%)
- **每包覆蓋面積** — 單片面積 × 每包片數
- **所需包數** — 加損耗後面積 ÷ 每包覆蓋面積，向上取整

### 計算公式

| 項目 | 公式 |
|------|------|
| 單片面積 (m²) | `(地板長度 mm × 地板闊度 mm) / 1,000,000` |
| 每包覆蓋面積 (m²) | `單片面積 × 每包片數` |
| 加損耗後面積 (m²) | `總施工面積 × (1 + 損耗% / 100)` |
| 所需包數 | `ceil(加損耗後面積 / 每包覆蓋面積)` |

---

## 截圖

| 桌面版 | 手機版 |
|--------|--------|
| *(待添加)* | *(待添加)* |

---

## 瀏覽器支援

| Chrome | Firefox | Safari | Edge | Opera |
|--------|---------|--------|------|-------|
| ✅ 最新 | ✅ 最新 | ✅ 最新 | ✅ 最新 | ✅ 最新 |

亦支援 iOS Safari 及 Android Chrome 等行動瀏覽器。

---

## 開發資訊

### 專案結構

```
flooring-calculator/
├── index.html    # 完整計算器（HTML + CSS + JS 單一檔案）
└── README.md     # 本文件
```

### 技術棧

- 純 HTML5 / CSS3 / JavaScript（ES6）
- CSS Custom Properties 設計系統（支援亮/暗主題）
- 無外部執行時期依賴
- 響應式設計（375px 手機到寬螢幕桌面）

### 設計系統

本計算器是 **Calculator Suite** 的一部分，共享設計語言規範於 [UI-SYSTEM.md](https://github.com/Jupiterlaw/calculator-suite/blob/main/UI-SYSTEM.md)（跨專案文件）。

---

## 相關專案

| 計算器 | 說明 |
|--------|------|
| [Outdoor Flooring Calculator](https://github.com/Jupiterlaw/ourdoor_flooring_material_calculator) | 戶外木地板及面通材料計算（地板分段、等分規則、面通/底通/鋁角） |
| [Joist Calculator](https://github.com/Jupiterlaw/joist_calculater) | 龍骨佈局計算器（等分分段、位置表、CSV 匯出） |

---

## 授權

本專案採用 MIT 授權條款 — 詳見 LICENSE 檔案（如適用）。

---

## 貢獻

歡迎提交 Issue 或 Pull Request。請參閱 [PR-GUIDELINES.md](https://github.com/Jupiterlaw/calculator-suite/blob/main/PR-GUIDELINES.md) 了解分支命名、提交規範與 PR 流程。