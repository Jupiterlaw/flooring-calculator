# 地板材料計算器 · Flooring Material Calculator

戶外/室內地板材料估算工具：輸入地板規格與各施工區域尺寸，即時計算總面積、加損耗後面積、每包覆蓋面積，以及所需包數（向上取整）。

A flooring-material estimator: enter plank specs and per-area dimensions to instantly get total area, area with waste, pack coverage, and required pack count (rounded up).

## 使用方法 · How to use
1. 填寫「地板產品資料」：單片長度、單片闊度、每包片數（毫米 / 片）。
2. 設定「損耗百分比」（裁邊預留，預設 0%）。
3. 在「施工區域」新增多個區域（長 × 闊，單位公尺），可個別命名與刪除。
4. 結果即時更新，無需按計算鍵。

1. Fill in plank length / width (mm) and pieces per pack.
2. Set the waste percentage (default 0%).
3. Add areas (length × width in metres); rename or remove as needed.
4. Results update live — no Calculate button.

## 計算公式 · Formula
- 單片面積 = 長(mm) ÷ 1000 × 闊(mm) ÷ 1000 （m²）
- 每包覆蓋 = 單片面積 × 每包片數
- 加損耗面積 = 總面積 × (1 + 損耗% ÷ 100)
- 所需包數 = ⌈加損耗面積 ÷ 每包覆蓋⌉
- 換算：1 m² = 10.7639 ft²

## 特性 · Notes
- 手機優先（375px），系統字型，高對比，戶外強光可讀。
- 純單一 `index.html`，無外部依賴、無建置步驟，直接以瀏覽器開啟即可。
- 支援深淺色（`prefers-color-scheme`）。

## 本套件成員 · Part of the Jupiterlaw calculator suite
- [flooring-calculator](https://github.com/Jupiterlaw/flooring-calculator) — 本工具（地板材料）
- [ourdoor_flooring_material_calculator](https://github.com/Jupiterlaw/ourdoor_flooring_material_calculator) — 戶外木地板 + 面通/底通/鋁角
- [joist_calculater](https://github.com/Jupiterlaw/joist_calculater) — 龍骨（joist）佈局位置

© Jupiter's Design Limited
