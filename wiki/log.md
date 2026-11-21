# 動漫文化科普 Wiki 異動日誌（Log）

> 本檔為 **Append-only（只追加不改寫）** 時間軸紀錄。
> 標題格式固定為 `## [YYYY-MM-DD] <operation> | <簡短標題>`，支援操作類型：`init`、`ingest`、`query`、`slide`、`lint`、`schema`。

---

## [2026-11-21] init | 初始化動漫文化科普 LLM Wiki 骨架

- **完成項目**：
  - 建立核心作業手冊 [Agent.md](../Agent.md)
  - 初始化三層目錄架構：`raw/`（`sources/`、`assets/`）、`wiki/`（五大分類與 `syntheses/`）、`presentations/`
  - 建立 [index.md](./index.md)、[log.md](./log.md) 與頁面範本（[card-template.md](./_templates/card-template.md)、[synthesis-template.md](./_templates/synthesis-template.md)）
- **核心設定確認**：
  - 範疇：綜合動漫文化科普（面向普羅大眾、台灣繁體中文）
  - 條目形態：30 秒輕量圖鑑卡片（深度情境故事留待 `.html` 簡報展開）
  - 連結規範：標準相對路徑 Markdown 連結（純 VS Code 友善）
  - 簡報規格：單檔獨立 16:9 深色劇院沈浸風（Cinema Dark），原創 Inline SVG 圖解優先

---

## [2026-11-21] ingest | 建置日本異世界演進與《無職轉生》首批 6 張科普卡片

- **參考來源（`raw/sources/`）**：
  - [2026-11-21-moegirl-mushoku-tensei.md](../raw/sources/2026-11-21-moegirl-mushoku-tensei.md)
  - [2026-11-21-tnl-isekai-history-analysis.md](../raw/sources/2026-11-21-tnl-isekai-history-analysis.md)
  - [2026-11-21-ann-mushoku-tensei-isekai-web-novels.md](../raw/sources/2026-11-21-ann-mushoku-tensei-isekai-web-novels.md)
  - [2026-11-21-ann-the-state-of-isekai-anime-2025.md](../raw/sources/2026-11-21-ann-the-state-of-isekai-anime-2025.md)
  - [2026-11-21-isekai-evolution-works-and-reference-dossier.md](../raw/sources/2026-11-21-isekai-evolution-works-and-reference-dossier.md)
- **新增卡片（6 張，均採 30 秒輕量格式＋雙向標準 Markdown 連結＋無劇透）**：
  - [《無職轉生～到了異世界就拿出真本事～》](./works/mushoku-tensei.md)（貫穿主軸與主要例子）
  - [異世界（Isekai）](./genres/isekai.md)
  - [異世界轉生 vs. 轉移與召喚](./terms/tensei-vs-summoning.md)
  - [成為系（なろう系）與「成為小說家吧」](./culture/narou-kei.md)
  - [貨車君（卡車君／Truck-kun）](./terms/truck-kun.md)
  - [現代異世界四大變體（惡役千金、慢活、退隊流、逆異世界）](./genres/isekai-subgenres.md)
- **同步更新**：[index.md](./index.md)
- **備註**：這 6 張卡片已構成完整的「異世界風格演進」知識網，隨時可啟動 **Export Slide** 流程組裝成 16:9 深色劇院風 `.html` 簡報。

---

## [2026-11-21] slide | 產出「日本異世界 40 年演進（主軸：《無職轉生》）」16:9 Cinema Dark .html 簡報

- **輸出簡報**：[2026-11-21-isekai-evolution-mushoku-tensei.html](../presentations/2026-11-21-isekai-evolution-mushoku-tensei.html)（10 頁、16:9 自動縮放、100% 離線單檔、原創 Inline SVG 圖解、附每頁講者口播稿）
- **專題腳本沉澱**：[isekai-evolution-mushoku-tensei-deck.md](./syntheses/isekai-evolution-mushoku-tensei-deck.md)
- **引用卡片**：`mushoku-tensei`、`isekai`、`tensei-vs-summoning`、`narou-kei`、`truck-kun`、`isekai-subgenres`
- **同步更新**：[index.md](./index.md)

---

## [2026-11-22] schema | 同步反思改進至 Agent.md 並建立 WORKFLOW_GRAPH.md

- **異動動機**：首輪實作發現「外部資料取得與格式清理」最易發生憑證受阻、結構差異與 HTML 雜訊問題，因此將檢查與容錯機制正式前移並固化進 Schema。
- **更新檔案**：
  - [Agent.md](../Agent.md)：
    - 流程一（Ingest）新增「Step 0：Fetch & Sanitize 前置預檢與分層降級備援子迴圈」與「Step 4：建卡後自動連結完整性檢查（0 斷鏈）」
    - 流程三（Export Slide）新增「Step 4：產出後自動離線與結構驗證（頁數／0 外部 URL／Inline SVG）」
    - 更新第 7 節 Schema Changelog
  - [WORKFLOW_GRAPH.md](../WORKFLOW_GRAPH.md)：新增完整系統 Loop & Graph 設計文件與 Mermaid 流程圖（含修正前後對照圖）
