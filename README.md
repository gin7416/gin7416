### 高凱伶 Kai-Ling Kao

陽明交通大學生物資訊及系統生物研究所碩士（2026）。專長是把雜亂的多來源資料整理成可信任的分析結果，並用可重現、可量化評估的方式把研究模型與 LLM 應用做成軟體服務。

Bioinformatics MS (NYCU, 2026) working on data pipelines, local-LLM applications and evaluation.

---

#### 作品

**[ERP AI Copilot](https://github.com/gin7416/erp-ai-copilot)**：用中文查詢企業資料與公司 SOP 的地端 LLM 系統（模擬資料）
- Airflow ＋ dbt 資料管線（45 項資料測試，被剔除的資料都記錄原因）；以 dbt 欄位說明作語意層的 Text-to-SQL，兩層唯讀 SQL 防護；中文 BM25 ＋ bge-m3 的 SOP 檢索；FastAPI 與 MCP server。
- 評測：36 題中文資料查詢與 26 題 SOP 檢索測試題。筆電上的 3B 地端模型加入語意層與錯誤修正迴圈後，準確率 22.2% → 66.7%（嚴格計分 38.9%）；向量檢索使 SOP 第 1 名命中率 84.6% → 88.5%。完整報告：[EVAL_REPORT](https://github.com/gin7416/erp-ai-copilot/blob/main/results/EVAL_REPORT.md)。
- CI：66 項測試、實際執行 Airflow DAG、Docker 與 Kubernetes（kind）部署驗證。

**[PathwayScore API](https://github.com/gin7416/pathwayscore-api)**：把碩論的癌症預後模型做成可測試的服務
- FastAPI 提供五種癌症的固定 Cox 評分、欄位規格與特徵貢獻；錯誤輸入回傳 HTTP 422。
- 31 項 pytest（覆蓋率 93%），自動比對 5 種癌症、24 項特徵的係數與標準化參數和原研究設定一致；GitHub Actions 與 Docker。

**[碩士論文研究程式](https://github.com/ICLab-pathway-level-risk-scores/pathway-level-risk-scores)**：跨來源癌症基因體資料整合與預後模型（實驗室 repo）
- 整合 MSK-CHORD 19,905 名患者的臨床、突變、拷貝數與結構變異資料，彙整為 pathway 特徵；IBCGA 30 次特徵選擇，每癌別精簡至 4–5 項特徵。
- 內部測試 C-index 較臨床基準提升 0.025–0.094，並以 2,607 名獨立患者外部驗證。
- 2026 年 6 月起開發，[完整 commit 紀錄](https://github.com/ICLab-pathway-level-risk-scores/pathway-level-risk-scores/commits/main)。IEEE CIBCB 2026 第一作者海報；期刊投稿審查中。

---

#### 技術

Python · pandas · SQL（DuckDB）· dbt · Airflow · FastAPI · pytest · GitHub Actions · Docker · Kubernetes · Ollama · RAG · MCP · Linux · Git

開發時會與 AI 工具協作，並以自動化測試與量化評測驗證結果。
