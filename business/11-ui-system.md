---
updated: 2026-07-31T18:07:00 （新增 Wordmark 特別條款，反映手動調整版官方標準字與系統字體規則之區隔）
---
# Picnic Attack Brand System

## Overview

Picnic Attack 是一個台灣獨立配件品牌，定位為 Editorial Minimalism。設計語言以克制、靜謐、精準為核心，拒絕促銷色彩與過度動態。

**Keywords**: picnic attack, PA, jewelry, accessories, editorial, minimal, taiwan, fragment mono, libre baskerville, stillness, moment

---

## Brand Colors

### Core Palette（僅此兩色）

|Role|Hex|用途|
|---|---|---|
|Background|`#FAFAF8`|全站底色|
|Foreground|`#1E1C1A`|主文字、按鈕填色、標題、邊框|

### Forbidden Colors（禁止使用）

- ❌ 任何第三色、accent 色
- ❌ Success green
- ❌ Urgency red / orange
- ❌ AI purple / pink gradients
- ❌ Pure white `#FFFFFF` 作為頁面背景
- ❌ `#C8C5C0`、`#7A7670`、`#F5F0E8`、`#5C6B6B`（舊版 pa-brand.md 遺留，已廢棄）

### Button Rules

- **Primary CTA**：背景 `#1E1C1A`，文字 `#FAFAF8`，hover 反轉為線框
- **Secondary / Ghost**：線框 `0.5px solid #1E1C1A`，背景透明，hover 填色
- 禁止使用色彩填充按鈕（除 Primary CTA）

---

## Typography

### Font Stack

css

```css
/* Heading — Display / H1 / H2 / H3 */
font-family: 'Libre Baskerville', Georgia, serif;
font-style: normal !important; /* 全站無 italic，無例外 */
font-weight: 400;

/* Body / UI / Labels / Tags / 中文 */
font-family: 'Fragment Mono', 'PingFang TC', 'Microsoft JhengHei', monospace;
```

### Wordmark 特別條款

品牌標準字（wordmark，如「Picnic Attack」全名 lockup）為**手動調整版本**，
非直接套用 Libre Baskerville 原始字重輸出。字母連筆與收筆方式經過手動修改，
與下方 Type Scale 中其他層級（H1/H2/H3/Display）的標準 Libre Baskerville
渲染結果不完全一致。

- **適用範圍**：僅限官方 wordmark 圖檔本身（品牌 logo、商標送件圖樣）
- **不適用於**：網站內文標題、Section 標題、商品名稱等其他 Libre Baskerville
  使用場景——這些仍必須是**未經修改**的標準字重，維持 `font-style: normal !important`
- **檔案來源**：官方 wordmark 圖檔以 `picnicattack-wordmark.png` 為準
  （或後續更新之正式版本檔名）
- **理由**：wordmark 屬於一次性設計定案的品牌識別資產，其筆畫調整是刻意的
  設計決策，不代表全站排版規則放寬。其餘所有 Libre Baskerville 使用情境
  仍受本文件 Typography Rules 約束，無例外。

### Google Fonts Import

css

```css
@import url('https://fonts.googleapis.com/css2?family=Fragment+Mono&family=Libre+Baskerville&display=swap');
```

> ⚠️ 注意：只載入 `Libre Baskerville` 正體，不載入 italic 字重。

### Type Scale

|層級|字族|字級|用途|
|---|---|---|---|
|Display|Libre Baskerville|clamp(32px, 5vw, 52px)|品牌宣言、About 大標|
|H1|Libre Baskerville|48px|頁面主標題|
|H2|Libre Baskerville|36px / 3.6rem|Section 標題|
|H3|Libre Baskerville|28px|商品名稱|
|Body|Fragment Mono|11–12px|品牌故事、商品描述|
|UI Label|Fragment Mono uppercase|10px / ls 0.12em|導覽、標籤、按鈕|
|Micro|Fragment Mono uppercase|8–9px / ls 0.1em|系列標籤、圖片 caption|

### Typography Rules

- `font-style: normal !important` 全站強制，**無任何例外**
- Fragment Mono 用於所有 UI 元素（按鈕、標籤、價格、meta）
- `text-transform: uppercase` 用於 10px 以下的 label
- 禁止使用 Inter、Roboto、Arial

---

## Spacing System（8pt Grid 強制執行）

所有間距**必須**是 8 的倍數（4px 次間距僅在有充分理由時使用）：

|Token|px|用途|
|---|---|---|
|xs|4px|最小間距（需有理由）|
|sm|8px|元素內部 gap|
|md|16px|組件內距|
|lg|24px|Card padding、按鈕水平|
|xl|32px|小 section 間距|
|2xl|48px|手機版 section gap|
|3xl|64px|桌機版 section gap|
|section|80–96px|頁面 section 間距|

### Spacing Rules（強制）

- Hero 左右留白：`8%`
- Section 間距：最小 `64px`，建議 `80px`
- Card 內距：`24px`
- 按鈕高度：`40px`，水平 padding `24px`
- **禁止**使用非 8 倍數間距（如 15px、25px、35px）

---

## Layout System

### Editorial Grid（桌機 ≥1024px）

- 12 col / 16px gap / 40px padding
- Tablet：8 col
- Mobile <768px：4 col / 8px gap / 16px padding

### PDP 分割

```
圖片區：60%  |  文字區：40%
```

- 禁止對稱分割（50/50）
- 右欄只用 `0.5px border #1E1C1A`，不用 shadow

### Border Radius

- **全站統一：`0px`（方角）**
- 唯一例外：input focus ring 可用 `2px`

---

## Image Treatment

css

```css
filter: saturate(0.82);
```

- 所有情境圖統一降飽和度 `0.82`
- 禁止使用白底去背商品圖作為主視覺
- Hero 圖使用 `fetchpriority="high"`，移除 `loading="lazy"`
- 非 Hero 圖使用 `loading="lazy"`

---

## Animation Rules

- Transition 統一：`0.3s linear`
- Hover 只允許：`opacity` 或 `translate ≤ 4px`
- **禁止**：bounce、ease、ease-in-out、parallax、decorative effects

css

```css
@media (prefers-reduced-motion: no-preference) {
  .pa-element {
    transition: opacity 0.3s linear;
  }
}
```

---

## Components

### Border

css

```css
border-width: 0.5px;
border-radius: 0;
```

### Cards

css

```css
.card, .card__inner, .button, input, textarea, select {
  border-radius: 0 !important;
}
```

---

## Collections

|系列|特色|
|---|---|
|Ground|靜謐、極簡|
|Picnic|日常、輕盈|
|Attack|態度、俐落|
|Moment|當下、內斂|
|Allover|日常款|

> ⚠️ 舊版 pa-brand.md 的 Moment Accent `#5C6B6B` 已廢棄，全系列統一使用 `#1E1C1A`。

---

## Shopify Implementation Notes

- **CSS 策略**：全站樣式 `base.css`，Product 頁獨立 `pa-product.css`
- **Section 樣式**：寫在各 `.liquid` 檔案內的 `<style>` 標籤（scoped，不污染全域）
- **字體載入**：在 `theme.liquid` `<head>` 內用 `<link>` 載入 Google Fonts
- **Dawn Theme 覆蓋**：使用 `!important` 蓋掉 Dawn 原生樣式
- **OS 2.0 架構**：Sections / Blocks，Mobile-first

---

## Brand Voice

||English|中文|
|---|---|---|
|Hero Tagline|World comes undone. You don't.|—|
|About H1|Panic lingers. You remain.|—|
|About sub-tagline|loud world. quiet you.|—|
|密碼頁標題|Picnic preparing.|—|
|密碼頁副標|Leave your email. You'll know when it's ready.|—|
|密碼頁折扣文字|EARLY ACCESS · NT$100 · BY INVITATION|—|
|Brand description|Refined accessories shaped by restraint and detail|以克制與細節構築的配件語言|
|Email|[pa@picnicattack.com](mailto:pa@picnicattack.com)|—|
|Meta title|Picnic Attack — Accessories for the moment you choose to stay|—|
|Meta description|Refined accessories shaped by restraint and detail. 以克制與細節構築的配件語言，呈現內斂而精準的風格。|—|

---

## Password Page

- 背景：`#FAFAF8`
- 標題字體：Libre Baskerville，`font-style: normal`
- 副標字體：Fragment Mono，`font-size: 11px`，`letter-spacing: 0.12em`，`color: #1E1C1A`
- 實作位置：`layout/password.liquid`

---

## About Page（手機版）

- 圖片：`order: 1`，靠右 `margin-right: -8%`，`margin-bottom: -40px`
- 文字卡片：`order: 2`，`max-width: 100%`，`margin-left: 0`
- Label（`— picnic attack`）：手機版 `display: none`
- Footer 分隔線距離：`margin-top: 40px`，`padding-top: 24px`，`padding-bottom: 24px`
- Tagline 字體（手機版）：Fragment Mono，`font-size: 13px`，`letter-spacing: 0.12em`，`color: #1E1C1A`

---

> **版本說明**：此為 v2，對齊對話規範。舊版 pa-brand.md 的 italic、多色系、ease animation 設定已全數廢棄。