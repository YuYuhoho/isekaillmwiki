# 動漫文化科普 LLM Wiki（Isekai LLM Wiki）

面向普羅大眾的日本動漫文化科普知識庫，採用「**不可變原始資料（`raw/`）→ 30 秒輕量圖鑑卡片（`wiki/`）→ 16:9 深色劇院風互動簡報（`presentations/`）**」三層架構，並透過 [Agent.md](./Agent.md) 與 [WORKFLOW_GRAPH.md](./WORKFLOW_GRAPH.md) 規範完整的人機協作與自動化檢查流程。

---

## 線上預覽 `.html` 教學簡報（GitHub Pages）

- **直接開啟簡報**：https://yuyuhoho.github.io/isekaillmwiki/
- **簡報直連路徑**：https://yuyuhoho.github.io/isekaillmwiki/presentations/2026-11-21-isekai-evolution-mushoku-tensei.html

> **操作快捷鍵**：`←` / `→`（或空白鍵）翻頁｜`S` 開關講者口播備忘錄｜`G`（或點頁碼）開啟縮圖總覽｜`F` 全螢幕

---

## 專案導覽

| 檔案 / 目錄 | 說明 |
| :--- | :--- |
| [Agent.md](./Agent.md) | 知識庫最高作業手冊與 Schema（含四大流程、去黑話／防雷規範與 Cinema Dark 簡報規格） |
| [WORKFLOW_GRAPH.md](./WORKFLOW_GRAPH.md) | Loop 與 Graph 系統設計說明、Mermaid 流程圖與實際執行反思 |
| [wiki/index.md](./wiki/index.md) | 全站知識卡片目錄（6 張 30 秒輕量卡片＋1 篇簡報腳本合成） |
| [wiki/log.md](./wiki/log.md) | Append-only 異動時間軸紀錄 |
| [raw/sources/](./raw/sources/) | 5 篇不可變原始參考資料（關鍵評論網、ANN 2021/2025、萌娘百科《無職轉生》、年表總整理） |
| [presentations/](./presentations/) | 單檔離線 16:9 互動 `.html` 簡報（內嵌原創 Inline SVG，零外部相依） |
