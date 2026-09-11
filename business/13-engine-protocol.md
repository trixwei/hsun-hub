---
type: spec
version: 2
created: 2026-08-22
updated: 2026-09-09
sync_status: active
authority: "[引擎協作協定, 跨界派工規範, 回報格式, 例外退件機制]"
depends_on: '["[[99-rules]]", "[[12-engine-log]]", "[[14-campaign-calendar]]"]'
---
---
本版變動
自 v1.0 升級至 v2.0。因應五引擎架構（新增 GPS 行銷引擎）正式上線，擴充引擎職掌邊界與派工流程；全面導入 Obsidian Properties 屬性區塊規範；納入下游引擎遇到阻礙時的「例外與退件機制 (Reject & Revise Loop)」；修訂回報格式以支援 YAML 標籤。

一、適用情境
任務橫跨兩個以上引擎職掌邊界時。
典型案例： 新品上市企劃 → GPS 定位受眾與檔期（寫入 14 號檔） → Rolling Stone 給成本紅線 → Windshield 寫文案與小卡規範 → Gas Pedal 落地上架。
單一引擎可獨立完成的任務不走本流程，避免增加無謂的裁決往返。

二、引擎職掌與邊界
## 引擎角色職掌分工表

| 引擎角色                | 職掌範圍                                                                     | 不得越線事項                   |
| ------------------- | ------------------------------------------------------------------------ | ------------------------ |
| **The Engine**      | 決策、任務切割、整合、對外回覆；持有 F4 裁決權之幕僚長。                                           | 不直接執行下游的專業作業。            |
| **GPS (Marketing)** | 行銷檔期、受眾定位、漏斗策略（08、09、14 檔）、促銷與通路導流策略。通路戰場選擇、流量漏斗與導流策略（如 05-channels 策略面） | 不干涉美學設計，不碰底層成本試算。        |
| **Rolling Stone**   | 財務、成本、供應商、實體品質、SKU/庫存監控、D3 零元公關單。                                        | 不做美學判斷，不做商業策略取捨決定（僅出數據）。 |
| **Windshield**      | 品牌語彙、文案、視覺美學、實體工業規格與防護規範。                                                | 不決定價格數字，不碰成本與投放。         |
| **Gas Pedal**       | 頁面落地、後台上架、廣告投放、社群客服、原始成效數據收集。通路後台技術設定、上架與參數落地（如 05-channels 執行面）         | 不做財務解讀，無美學裁決權。           |
三、執行步驟
1. 裁定切割 — The Engine 判斷任務涉及哪些引擎（含 GPS、Windshield、Gas Pedal、Rolling Stone）、切成幾塊、順序為何。
2. 附範圍說明派工 — 每塊任務交付時須附上「僅執行此範圍，不延伸至其他引擎職掌」的說明，避免引擎自行擴權或反向踢回。
3. 逐步回報 — 各引擎完成後以固定格式回報 The Engine，不直接跳過 The Engine 互相交接。
4. 例外與退件機制 (Reject & Revise Loop) — 若 Gas Pedal 遇到平台規格衝突（Technical Error Flag），或 Rolling Stone 算出一筆企劃突破財務紅線（Margin Breach），必須打 Flag 退回給 The Engine；The Engine 須發布帶有 Pros/Cons Analysis 的 Revision Brief 重新指派。
5. 最終整合 — 由 The Engine 彙整所有引擎產出，統一回覆主理人（使用者）。

四、回報固定格式與 Properties 規範
所有引擎之輸出與回報檔案，頂端均須包含 Obsidian Properties 屬性標頭，且內文採用下列格式：

```markdown
---
type: [task / log / spec]
version: 1
created: YYYY-MM-DD
updated: YYYY-MM-DD
sync_status: draft
authority: [任務核心主題]
depends_on: ["[[關聯 Hub 檔案]]"]
---

### 回報欄位清單
* **任務代號：** 由 The Engine 派工時指定
* **結果：** 交付物本體或其在 Hub 中的位置
* **是否觸及紅線：** 是／否；若是，指明條號（如 [[99-rules#C1]]、[[04-finance]]）
* **需 The Engine 裁決的項目：** 逐項列出，無則寫「無」
````

五、範例切割模板（五引擎版）

|**順序**|**引擎**|**任務範圍**|**交付物**|
|---|---|---|---|
|1|GPS|決定受眾、促銷機制、寫入行銷行事曆|檔期策略草案（寫入 14 號檔）|
|2|Rolling Stone|驗證 GPS 之促銷機制是否符合 30% 淨利與 45% 成本紅線|財務驗證讀數|
|3|Windshield|依 GPS 策略與 Rolling Stone 成本限制，撰寫雙語文案與包裹小卡規格|創意資產與技術參數|
|4|Gas Pedal|將文案、商品與小卡落地至頁面與實體包裝，同步監控廣告數據|頁面草稿／投放數據報表|

六、禁止事項

- 引擎間不得跳過 The Engine 直接互相協商任務範圍。
    
- 引擎不得自行擴權至他引擎職掌。
    
- 引擎不得將任務反向踢回而不附具體阻礙原因或技術錯誤標頭（Flag）。
    
- Rolling Stone 不得代替 The Engine 判斷「這筆交易／檔期策略上值不值得」——只出財務與庫存讀數。
    
- 任何引擎不得私自篡改經主理人拍板之 F4 規則或 99-rules 紅線。
    

變更紀錄

|**日期**|**版本**|**變更摘要**|**影響檔案**|
|---|---|---|---|
|2026-08-22|1.0|自 10-operations 第五節抽出獨立成檔；修正表格；補引擎職掌與邊界表|10-operations、README|
|2026-09-09|2.0|升級為五引擎架構（納入 GPS）；全面導入 Obsidian Properties 屬性格式；新增 Reject & Revise 退件迴圈與 F4 邊界規範|99-rules、各引擎 Instruction、14-campaign-calendar|