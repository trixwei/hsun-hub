---
type: brand-element
created: 2026-04-22
updated: 2026-09-03
sync_status: active
version: 2
---
### 2026-09-03｜99-rules 修法：v3.5 → v3.6（C1 明確化、C2 拆軌、新增 D3）

- **決策：** 99-rules.md 由 v3.5 修訂至 v3.6，取代所有先前版本。
- **理由：** 三項變動，兩項實質、一項明確化：①C1「NT$680 以上」明確為**含本數**，解除原「待釐清」清單中的邊界爭點，公版首發上限保守抓 679 之做法予以確認；②C2 由單軌「一律導向蝦皮關注禮、全程零導外」拆分為**數位／實體雙軌**——數位端（商品頁、聊聊）維持零導外不變，實體端（包裹小卡 QR code）改導向品牌自有社群/官網，以保養指南／圖鑑為由建立私域流量；③新增 D3，禁止親友與 KOL 公關贈禮以系統折扣碼形式呈現，一律採 0 元公關單實物給予。
- **風險揭露（不可省略）：** C2 實體端開放**非零風險判定**。依 `10-operations.md` 第十一節，蝦皮導外管制範圍明文包含「包裹內容物」，稽查手段不限於系統自動偵測，買家截圖檢舉與客服人工抽查皆可能觸發計分或凍結賣場，代價是優選資格喪失，賭注不對稱。此變動由 The Engine（品牌負責人）在明確知悉上述風險後主動承擔並拍板，非引擎自行認定為安全動作。日後若觸發稽查後果，待釐清清單已列入 C2 監測項，由 Rolling Stone 追蹤，不得回頭視為執行疏失。
- **影響範圍：** `99-rules.md` 全文（frontmatter version 3.5 → 3.6，新增 D3、待釐清清單更新 C1 結案並新增 C2 監測項）、`decisions-summary.md`（本次新增段落與同步狀態表更新）、`10-operations.md`（第十一節導外規範與包裹小卡技術敘述須改為雙軌，派工 Gas Pedal）、`05-channels.md`（包裹小卡段落須同步，派工 Gas Pedal）、`07-customer-journey.md`（階段五至七之導外敘述、階段七公關贈禮流程須更新，派工 Rolling Stone／The Engine）。

---

### 2026-08-05｜99-rules 修法：v3.3 → v3.4（論述強化，非數字變動）

- **決策：** 99-rules.md 由 v3.3 修訂至 v3.4，取代所有先前版本。
- **理由：** 三項論述強化：①判準節承認Brand Guideline有多個根，不再宣稱單一判準涵蓋全部條文（尤其 C 段定價正當性、平台存活另有保護對象）；②B2 蝦幣回饋改採「平台歸屬」定性，明確與 A2 的區隔依據；③B1 停產出清條款增列「受控例外聲明」，承認此條確實可能讓原價買家看到更低價，以三重不可逆柵欄（停產不可逆、售完不補、SKU 上限 20%）換取死庫存出口，不假裝無傷。三項修訂均不涉及任何價格判定或數字變動。
- **影響範圍：** `99-rules.md` 全文（frontmatter version 3.3 → 3.4）、`decisions-summary.md`（同步狀態表與重大轉向摘要文字更新）。

## 現況一句話

Picnic Attack 為單一品牌，不設子品牌。營運中樞由七專案收斂為四引擎（The Engine 決策／Windshield 感官輸出／Gas Pedal 發布陳列／Rolling Stone 現實基底），否決權集中於 The Engine。

---

## 2026-07-31 重大轉向摘要

原「串聯雙賣場（子品牌測款 → 主品牌承接）」策略經完整覆核，判定客源轉移路徑結構性不可行，予以廢止。

- **品牌與材質：** 改採單一品牌直接經營，材質主力由鈦鋼轉為 925 純銀。
- **產品線收斂：** 由四線並行收斂為兩線（`picnic` 主力／`allover` 入口；`ground`／`moment` 凍結）。
- **通路收斂：** 收斂為「蝦皮＋實體寄賣＋官網本館」三者，明確排除 Pinkoi。
- **Brand Guideline升級：** `99-rules` 同步修訂至 v3.4。 _(完整決策脈絡與理由見 `_decisions-log.md`)_

---

## 專案架構現況（四引擎，2026-08-06 七併四生效）

原七專案矩陣收斂為四引擎。The Engine 為唯一決策/否決節點，其餘三者只執行不裁決。

|引擎|前身|主要職掌|否決權/執行權|狀態|
|---|---|---|---|---|
|**The Engine**|Brand Brain|拆解任務、守底線、彙整回報；持有全 16 檔 hub 主本|**唯一否決權**|✅ 運作中|
|**Windshield**|Creative Studio + AI Gen|雙語文案、圖像/影像 prompt、字體排版技術指令|執行（只提案不拍板）|✅ 已建立|
|**Gas Pedal**|Launch Ops + Website|IG/Threads 排程、種子單錯開、官網 UI 實作、廣告後台操作、即時止血|執行（無裁決權）|✅ 已建立|
|**Rolling Stone**|Sourcing & Finance + Business Ops|1688 議價、品管、淨利精算、廣告週期財務分析、客訴與行政|執行（只算不判）|✅ 已建立|

> **【否決權集中防呆】** The Engine 保留對 COGS 45%／淨利 30%／促銷Brand Guideline的唯一否決權。三執行引擎只接受 The Engine 派工、不與 peer 協商邊界，回報採固定格式（Task ID／Result／Red line touched／Needs Engine decision）。

> **【廣告回報分工】** Gas Pedal 握即時後台、負責即時止血；Rolling Stone 用 Gas Pedal 提供的原始數字做週期財務分析。

> **【空白檔案歸屬】** 07-customer-journey → The Engine；08-email-flows、09-ugc-kol → Windshield。

---

## Hub 檔案同步狀態（2026-09-03）

|檔案名稱|狀態|備註說明|
|---|---|---|
|`99-rules.md`|✅ 已同步|更新至 v3.6（C1 含本數結案、C2 拆數位/實體雙軌、新增 D3）|
|`00-brand-core.md`|✅ 已同步|已確認無需修改|
|`01-product-lines.md`|✅ 已同步|已重寫同步|
|`03-pricing.md`|✅ 已同步|已更新同步|
|`04-finance.md`|⏳ 待寫回|未確認同步|
|`05-channels.md`|⏳ 待寫回|包裹小卡段落須反映 C2 雙軌，派工 Gas Pedal 執行中|
|`06-content-strategy.md`|✅ 已同步|已更新同步|
|`10-operations.md`|⏳ 待寫回|第十一節導外規範須反映 C2 雙軌，派工 Gas Pedal 執行中|
|`02-visual-system.md`|🔍 已草擬・待核准||
|`07-customer-journey.md`|⏳ 待寫回|階段五至七敘述與 D3 公關贈禮流程須更新|
|`08-email-flows.md`|📝 未撰寫|架構已規劃，內容尚未產出|
|`09-ugc-kol.md`|📝 未撰寫|架構已規劃，內容尚未產出|
|`11-ui-system.md`|🔍 已草擬・待核准||