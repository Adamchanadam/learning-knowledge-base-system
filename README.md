# 學習型知識庫系統 PUBLIC

這個 repo 是面向公眾的 GitHub / npm 產品發佈面。它不是 OPS 工作區的鏡像，也不是私人 Notion、治理紀錄、研發證據或 session log 的發佈出口。

目前版本：v0.1.0。公開發佈骨架已接入 Agent Handoff Kit 底層機制；尚未是可正式使用的完整產品版本。

## 更新紀錄

- 最新版本：v0.1.0
- 面向非開發者的更新紀錄：[CHANGELOG.md](CHANGELOG.md)

## 產品入口

這個產品的主要使用入口是 agentic AI。用戶應可用自然語言要求 AI agent 安裝、升級和接續工作，而不是先理解內部治理文件。

首次安裝或升級 Agent Handoff Kit：

```text
請讀取 https://adamchanadam.github.io/agent-handoff-kit/agent-handoff-kit-ai-install.html，並在這個資料夾安裝或升級 Agent Handoff Kit。
```

日常接續工作：

```text
Start Agent Handoff
```

中文可說：

```text
開工
```

結束本輪工作並保存交接：

```text
收工
```

若 AI agent 尚未指向本資料夾，才使用帶路徑啟動句：

```text
Work in <你的專案資料夾>. Read AGENTS.md first, then Start Agent Handoff. Before changing anything, tell me the current state and your recommended next step.
```

## 安裝與升級原則

安裝與升級是 PUBLIC 產品的基本能力，主真源放在本 README，而不是拆成額外安裝文件。

- 安裝與升級均使用 [`Adamchanadam/agent-handoff-kit`](https://github.com/Adamchanadam/agent-handoff-kit)。
- PUBLIC 採用與 OPS 一致的 Agent Handoff Kit 底層機制。
- PUBLIC 不接入 OPS 的資料、交接歷史或內部研發內容。
- 未來若加入 npm package，`package.json`、CLI 命令、版本策略、健康檢查與升級預演才是安裝／升級的產品實作層。
- README 只保留公眾用戶需要知道的最短入口與驗收原則。

升級必須先預演，無衝突才正式升級：

```text
npx --yes @adamchanadam/agent-handoff-kit@latest upgrade --dry-run --root .
```

```text
npx --yes @adamchanadam/agent-handoff-kit@latest upgrade --yes --root .
```

安裝或升級後必須通過健康檢查：

```text
npx --yes @adamchanadam/agent-handoff-kit@latest doctor --root .
```

## OPS 與 PUBLIC 的角色

| 目錄 | 角色 | 可包含 | 不可包含 |
|---|---|---|---|
| OPS | 私有研發、驗收、治理和內部證據工作區 | 研發輸出、實驗紀錄、內部交接、驗收證據、私人資料來源 | 不能直接作為公眾發佈面 |
| PUBLIC | 公眾 GitHub / npm 產品發佈面 | README、公開文件、清理後示例、可公開技能或套件內容、PUBLIC 專用 Agent Handoff Kit 狀態 | OPS 的 `dev/`、`outputs/`、session log、內部決策紀錄、私人 Notion 資料、憑證、本機私人路徑 |

兩者的關係是「OPS 產出候選內容，PUBLIC 承接清理後的產品發佈內容」。同步方向只應由 OPS 到 PUBLIC，且每次都要經過人工或 AI 明確審核；PUBLIC 不反向污染 OPS，也不自動吸收 OPS 全量內容。

## 從 OPS 同步到 PUBLIC 的發佈流程

當 OPS 開發完成並通過驗收後，不能直接複製整個資料夾到 PUBLIC。正確流程是：

1. 在 OPS 確認候選成果已完成驗收，列出要公開的能力、文件、示例或套件內容。
2. 判斷每項內容是否可公開；剔除私人資料、內部交接、研發證據、本機路徑、未授權第三方素材和憑證。
3. 把可公開內容改寫成 PUBLIC 產品語言：README、公開文件、示例、技能封裝或 npm package 結構。
4. 在 PUBLIC 更新對應文件與產品檔案，不搬入 OPS 的 `dev/`、`outputs/` 或 session log。
5. 在 PUBLIC 跑健康檢查、私隱掃描、差異檢查與必要產品測試。
6. 檢查通過後才可提交 PUBLIC 變更。
7. GitHub push、tag、release、npm publish 或部署，都需要另行明確授權。

## 邊界

可放入這裡的內容：

- 面向公眾的產品說明。
- 可公開的安裝、升級、使用和示例內容。
- 經清理後的技能、工具或本地代理封裝。
- 不含私人資料、Notion 路徑、憑證、內部治理紀錄的示例。
- Agent Handoff Kit 的公開操作機制。

不可放入這裡的內容：

- OPS 工作區的 `dev/`、`outputs/`、session log 或內部決策紀錄。
- Adam 個人 Notion 資料、資料庫 ID、頁面 ID、私人本機路徑或截圖。
- API key、token、credential、個人設定或可還原機密的片段。
- 尚未清理來源權限的文章全文、圖片或第三方內容。

## 目錄

- `AGENTS.md`：AI agent 的公開倉庫操作入口。
- `START_NEXT_SESSION_PROMPT.txt`：下一次接續工作的便利提示副本。
- `dev/`：Agent Handoff Kit 的 PUBLIC 專用治理狀態。
- `docs/`：未來公開文件入口；目前不承擔安裝／升級主真源。
- `examples/`：公開示例入口。
- `skill/`：未來技能或本地代理封裝入口。
- `PUBLICATION_BOUNDARY.md`：公開發佈邊界。

## 下一步

先補齊最小可用產品說明、可清理示例和未來 npm package 結構；本次公開倉庫提交只包含 Git commit 與 push；任何 GitHub tag、GitHub release、package publish 或正式部署，都需要另行明確確認。
