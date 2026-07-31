---
type: brand-element
sync_status: active
priority: high
updated: 2026-07-31T15:30:00
version: 2
created: 2026-04-22T15:29
---
---
Type: brand-element
Sync_status: active
Priority: high
Updated: 2026-07-31
Version: 2

# decisions-summary

## 現況一句話
Picnic Attack 全面收斂為單一品牌架構，廢止子品牌。營運中樞現階段由 **Brand Brain** 統籌全域決策，並已完成核心 AI 幕僚（Creative Studio, Sourcing & Finance）的指令模塊化，隨時可拆分部署。

## 2026-07-31 重大轉向摘要
原「串聯雙賣場（子品牌測款 → 主品牌承接）」策略經完整覆核，判定客源轉移路徑結構性不可行，予以廢止。
*   **品牌與產品：** 改採單一品牌直接經營。材質主力由鈦鋼轉為 925 純銀（佔比 80%），產品線由四線並行收斂為兩線雙軌（`picnic` 主力／`allover` 入口），`ground` 與 `moment` 無限期凍結。
*   **通路架構：** 收斂為「蝦皮＋實體寄賣＋官網靜態本館」，無限期排除 Pinkoi 且官網現階段不開啟交易金流。
*   **鐵律升級：** 品牌最高指導原則 `99-rules.md` 同步修訂至 v3.3 終極版。
*(完整決策脈絡與辯論理由見 `_decisions-log.md`)*

---

## 專案架構現況 (AI 幕僚陣列)
原規劃的「七專案分工」已依據一人公司的產能極限進行收斂。目前以 Brand Brain 為核心，但已為未來擴張準備好模塊化指令。

| 專案模塊 | 主要職掌 | 當前狀態 |
| :--- | :--- | :--- |
| **Brand Brain** | 戰略決策、SKU 追蹤、財務守門、Hub 同步 | ✅ **運作中** (核心大腦) |
| **Creative Studio** | 創意方向、雙語文案、品牌聲音守門員 | ✅ **指令已完備** (待部署為獨立 GPT) |
| **Sourcing & Finance**| 採購把關、成本結構、定價策略、毛利試算 | ✅ **指令已完備** (待部署為獨立 GPT) |
| **AI Gen** | Nano Banana 圖像、Veo 影片、提示詞 | ⏳ 尚未建立獨立專案 |
| **Launch Ops** | 內容排程、發布、資產確認 | ⏳ 尚未建立獨立專案 |
| **Website** | Shopify UI/UX、CRO、頁面結構 | 🛑 **不適用** (官網現為靜態頁，無限期擱置) |
| **Business Ops** | 行政、法務、物流、客服 | 🔄 **整合** (內容已併入 `10-operations.md`) |

**【一人公司現況判斷】**
現階段以 Brand Brain 單一專案通盤處理最符合實際運作規模。待業務量成長到需要精細分工時，直接套用已寫好的 System Prompts 拆出 Creative Studio 與 Sourcing & Finance。

---

## Hub 檔案同步狀態（2026-07-31 檢核）

| 檔案名稱 | 狀態 | 備註說明 |
| :--- | :--- | :--- |
| `99-rules.md` | ✅ 已同步 | 更新至 v3.3，整合定價、營運與文案紅線。 |
| `00-brand-core.md` | ✅ 已同步 | 確認核心精神不變，無需修改。 |
| `01-product-lines.md`| ✅ 已同步 | 重寫完成，確立 picnic / allover 雙線架構。 |
| `03-pricing.md` | ✅ 已同步 | 載入 34.8% 毛利試算與 V2 漲價防呆機制。 |
| `04-finance.md` | ✅ 已同步 | 確立 87K 資金分配與 45% COGS 紅線。 |
| `05-channels.md` | ✅ 已同步 | 廢除子品牌與 Pinkoi，建立蝦皮防作弊 SOP。 |
| `06-content-strategy.md`| ✅ 已同步 | 調整完畢。 |
| `10-operations.md` | ✅ 已同步 | 確立客訴三級補償與全面現貨制出貨紀律。 |
| `02-visual-system.md`| ⏳ **待補** | 需加註 Grasspath 視覺系統封存說明，並補入 925/鈦鋼 的視覺區隔規範。 |
| `07-customer-journey.md`| ➖ 維持原狀 | 本次未涉及修改。 |
| `08-email-flows.md` | ➖ 維持原狀 | 本次未涉及修改。 |
| `09-ugc-kol.md` | ➖ 維持原狀 | 本次未涉及修改。 |
| `11-ui-system.md` | ➖ 維持原狀 | 本次未涉及修改。 |