---
type: spec
created: 2026-08-13
updated: 2026-08-13
sync_status: active
---

**版本 2026-08-13**｜首版。定位依 08-06「七併四」決議：本檔案為跨引擎流程分工地圖，記錄客戶在各接觸點時，哪個引擎負責什麼、由誰交棒給誰，不是行銷內容或文案產出（內容產出屬 Windshield 職掌，見 06-content-strategy.md）。

## 一、客戶旅程階段與引擎對應總覽

| 階段 | 客戶行為 | 主責引擎 | 涉及檔案 |
|---|---|---|---|
| 1. 觸及 | 在 Threads/IG 滑到品牌內容 | Windshield（內容）→ Gas Pedal（發布） | 06-content-strategy.md |
| 2. 搜尋進站 | 蝦皮搜尋關鍵字進入賣場 | Gas Pedal（廣告與陳列） | 05-channels.md |
| 3. 瀏覽決策 | 看商品頁、比價、猶豫 | Windshield（文案與商品頁素材）→ Gas Pedal（落地執行） | 11-ui-system.md、02-visual-system.md |
| 4. 下單 | 蝦皮結帳 | Gas Pedal（營運參數）、Rolling Stone（現貨與出貨） | 10-operations.md |
| 5. 到貨與開箱 | 收到包裹、拆封 | Rolling Stone（品管、包裝） | 10-operations.md、04-finance.md |
| 6. 售後 | 客訴、退換、留評 | Rolling Stone（執行 SOP）→ The Engine（若觸及補償上限需裁決） | 99-rules.md（D2）、10-operations.md |
| 7. 回購/推薦 | UGC、二次購買 | Windshield（UGC 內容）、Rolling Stone（送禮物流） | 09-ugc-kol.md、06-content-strategy.md |

## 二、階段一：觸及（Threads / IG）

**客戶狀態：** 陌生受眾，第一次看到品牌內容，尚未產生購買意圖。

**分工：**
- Windshield 依 `00-brand-core.md` 語氣與 `02-visual-system.md` 視覺座標產出雙語文案與圖像/影像 prompt。
- Gas Pedal 依 `06-content-strategy.md` 排程頻率（約三天一則）執行發布，Threads 為主力、IG 為次要。

**交棒節點：** Windshield 完成內容與參數化語氣座標後，交給 Gas Pedal 執行，Gas Pedal 不做美學判斷，僅核對技術規格是否符合。

**The Engine 介入時機：** 僅在 Windshield 三份提案皆未達標，或觸及 99-rules A4/B4 禁用詞時介入裁決或退回。

## 三、階段二：搜尋進站（蝦皮）

**客戶狀態：** 已有明確購買意圖或比價意圖，主動搜尋關鍵字。

**分工：**
- Gas Pedal 負責蝦皮站內關鍵字廣告操作（廣泛比對起跑、依報表收斂精準比對），受 The Engine 核准之預算上限與時間範圍約束。
- Rolling Stone 於此階段不涉入，僅在廣告財務讀數需要週期分析時被動接手 Gas Pedal 提供的原始數據。

**紅線提醒：** 零評價階段禁止投放廣告（依 05-channels.md 廣告凍結條款）；廣告即時燒錢警示為 Gas Pedal 職責，超支立即回報 The Engine，不等待 Rolling Stone 週期分析。

## 四、階段三：瀏覽決策（商品頁）

**客戶狀態：** 已進站，在比較商品細節、材質說明、評價，猶豫是否下單。

**分工：**
- Windshield 產出商品文案（材質判斷、選品邏輯，依 06-content-strategy.md 「做東西的過程與判斷」原則）。
- Gas Pedal 依 `11-ui-system.md` 技術規格（8pt grid、Fragment Mono、border-radius: 0 等）落地執行，僅核對規格，不做美學判斷。

**交棒節點：** 官網若已開通交易（依 05-channels.md 三選一觸發條件），Gas Pedal 同時負責官網 UI 落地；現階段官網為靜態頁，此節點僅適用蝦皮商品頁與 IG Highlights。

## 五、階段四：下單（蝦皮結帳）

**客戶狀態：** 已決定購買，進入結帳流程。

**分工：**
- Gas Pedal 確保蝦皮營運參數正確（免運方案一、隔日到貨 19:00 截止）。
- Rolling Stone 確保現貨在庫、品管已完成（磁鐵初篩、925 驗真、連戴測試皆於到貨階段完成，非下單當下）。

**紅線提醒：** 隔日到貨截止 19:00 為 Gas Pedal 不可違反之紅線；休假模式絕對禁止輕易開啟，缺貨時改標「較長備貨」。

## 六、階段五：到貨與開箱

**客戶狀態：** 收到包裹，第一次實際接觸商品與包裝。

**分工：**
- Rolling Stone 負責出貨品質（包材、小卡內容需符合 99-rules C2 蝦皮零導外規範）。
- 包裹小卡內容文案由 Windshield 產出，但實際包裝執行與寄送屬 Rolling Stone。

**紅線提醒：** 包裹小卡嚴禁任何離站購買明示或暗示；QR code 僅導向蝦皮「關注禮」功能。

## 七、階段六：售後（客訴／退換／留評）

**客戶狀態：** 商品有問題，或主動想留評價。

**分工：**
- Rolling Stone 依 `10-operations.md` 三級 SOP 執行（輕微/中度/重度），使用固定話術模板。
- 若情節超出既定補償上限，或客戶要求現金折扣/購物金（違反 99-rules D2），Rolling Stone 不得自行決定，必須回報 The Engine 裁決。

**紅線提醒：** 一律禁止現金折扣碼或購物金補償，無例外。

## 八、階段七：回購與推薦（UGC/KOL）

**客戶狀態：** 已是回購客或滿意客戶，可能產生自發分享或接受品牌邀請合作。

**分工：**
- Windshield 依 `09-ugc-kol.md`（延伸 06-content-strategy.md 種子創作者段落）產出 UGC 徵集與呈現邏輯。
- Rolling Stone 負責微型創作者送禮的實際物流執行（成本估算 NT$4,000，依 D1 給予類原則，不涉及對價條件）。

**交棒節點：** Windshield 決定「找誰、怎麼呈現」，Rolling Stone 執行「寄什麼、寄給誰」，兩者資訊皆經 The Engine 派工銜接，不互相直接聯繫。

## 九、與其他 hub 檔案的關聯

本檔案為流程分工地圖，不重複定義各階段的具體規則數字（定價、紅線、話術模板），這些定義權威一律以對應來源檔案為準：`99-rules.md`（促銷與補償鐵律）、`04-finance.md`（COGS 紅線）、`05-channels.md`（通路參數）、`06-content-strategy.md`（內容策略）、`10-operations.md`（營運 SOP）、`11-ui-system.md`（視覺規格）。若本檔案的階段描述與來源檔案數字衝突，一律以來源檔案為準，並回頭修正本檔案。

---

_本檔案由 The Engine 撰寫維護，非任何執行引擎的內容產出物。若客戶旅程階段因通路變動（如官網交易開通）需調整，須同步檢查本檔案是否仍準確反映流程現況。_