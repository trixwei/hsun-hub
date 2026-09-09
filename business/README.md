# Picnic Attack — business hub

# Picnic Attack — business hub

單一品牌線的營運知識庫。衝突時的判定依據在下方「管轄權」表，不看各檔文末的自我聲明。

## 一、檔案編號體系
| 編號 | 檔案 | 管轄主題 | 備註 |
| :--- | :--- | :--- | :--- |
| _decisions-log | 決策流水帳 | 待定義邊界 | |
| 00 | 00-brand-core | 品牌核心 | — |
| 01 | 01-product-lines | 產品線與 SKU | 款式、材質、首批規模 |
| 02 | 02-visual-system | 視覺系統 | — |
| 03 | 03-pricing | 定價 | 價位帶、首發區間、階段性天花板 |
| 04 | 04-finance | 財務 | 資金配置、COGS 紅線、毛利試算、現金流 |
| 05 | 05-channels | 通路 | — |
| 06 | 06-content-strategy | 內容策略 | Panic/Picnic 分工 |
| 07 | 07-customer-journey | 顧客旅程 | — |
| 08 | 08-email-flows | EDM | 由 GPS 主筆 |
| 09 | 09-ugc-kol | UGC / KOL | 由 GPS 主筆，Rolling Stone 協同 0 元單 |
| 10 | 10-operations | 營運 | 現貨制、供應鏈驗證、蝦皮參數、客訴 SOP、法遵標示 |
| 11 | 11-ui-system | UI 系統 | — |
| 12 | 12-engine-log | 引擎日誌 | 各引擎執行回報寫入目標 |
| 13 | 13-engine-protocol | 引擎協定 | 跨專案派工、五引擎邊界、回報格式與退件迴圈 |
| 14 | 14-campaign-calendar | 行銷日曆 | GPS 專屬工作區（檔期與漏斗策略） |
| decisions-summary | 決策摘要 | 待定義邊界 | |

index.base：Obsidian Bases 視圖自動彙整，非手寫檔。新增檔案須先在本表登記。編號一經佔用不重複使用。

## 二、管轄權（衝突判定）
規則：同一個數字只在一個檔案裡定義，其他檔案只連結、不複製。

| 主題 | 說了算的檔案 | 其他檔案作法 |
| :--- | :--- | :--- |
| 價格能否變動、折扣、語彙禁區、F4 | 99-rules | 只引用條號，不複述條文 |
| 價位帶、首發區間、天花板 | 03-pricing | 只連結 |
| COGS 紅線、資金配置、毛利試算、包材成本 | 04-finance | 只連結 |
| 蝦皮費率與營運參數、供應鏈驗證、法遵標示 | 10-operations | 只連結 |
| 款式、SKU、首批件數 | 01-product-lines | 只連結 |
| 引擎派工與邊界、退件機制 | 13-engine-protocol | 只連結 |
| 行銷檔期規劃、受眾定位、漏斗策略 | 14-campaign-calendar | 只連結 |

禁止： 任何檔案整段複製他檔管轄的數字。需要引用時寫 `[[04-finance#二、貨成本紅線]]`。

 附註：流水帳與決策摘要的協同邊界（_decisions-log vs decisions-summary）
* **`_decisions-log`（決策流水帳）：** 
  * **性質：** 原始異動 Append-only 檔案（類似 Git Commit History）。
  * **規則：** 任何引擎完成重要任務或主理人執行 F4 覆寫時，由 The Engine 依時間軸**逐筆追加**。只增不減，忠實記錄歷史。
* **`decisions-summary`（決策摘要）：** 
  * **性質：** 衍生性共識快照（Executive Summary）。
  * **規則：** 濃縮當前仍然有效的核心結論與現行紅線。定期或重大里程碑時由 The Engine 根據 log 提煉更新。
* **協同原則：** 歷史查閱看 log，當前有效共識看 summary。禁止兩者內容互相矛盾。

## 三、frontmatter 樣板 (Obsidian Properties)
---
type: spec | rule | log
version: x.y
created: YYYY-MM-DD
updated: YYYY-MM-DD
sync_status: active | draft | pending-sync
authority: [此檔說了算的主題]
depends_on: ["[[04-finance]]", "[[99-rules]]"]
---

sync_status 定義：
* **active**：已寫回 GitHub / 系統定案，可直接採信
* **draft**：對話中生成、尚未寫回，不可作為決策依據
* **pending-sync**：內容已定案，等待同步

## 四、index.base 建議欄位
index.base 目前只顯示 name。到右上「屬性」加入以下欄位，index 就變成同步狀態儀表板，不需另外手寫索引檔：
* `sync_status`：最重要——一眼看出哪幾份還是 draft 沒寫回
* `updated`：找出最久沒維護的檔案
* `version`：判斷是否為最新版
* `authority`：忘記哪個數字歸誰管時直接查
* `type`：區分 spec / rule / log

建議排序：sync_status 遞減 → updated 遞增（沒同步的、最舊的排最上面）。
index.base 的 YAML 設定見 `index-base-config.md`。

## 五、正文結構規範
* ## 本版變動（三行內）
* 主體分節：`## 一、標題`（頓號後不空格，全 hub 統一；99-rules 保留字母制）
* `## 待確認`（統一 `- [ ]`）
* `## 變更紀錄`（表格：日期｜版本｜變動摘要｜影響檔案）
* 引用一律 wikilink：`[[99-rules#B2]]`。
* 不用 emoji 作狀態標記，改文字標籤：[待核實]、[新增]、[待裁決]。

## 六、待處理
- [ ] _decisions-log 與 decisions-summary 邊界未定義——是「流水帳 vs 摘要」還是新舊版本？兩份並存是下一個不同步點
- [ ] 00-brand-core、02、05–09、11-ui-system 尚未完全對齊五引擎架構與 Obsidian Properties 規範。
- [x] 全 hub frontmatter 補齊 version / authority / depends_on