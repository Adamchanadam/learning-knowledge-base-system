# PUBLIC 發佈邊界

本工作區只承載可公開使用的產品版本內容。它與 OPS 工作區分離。

## 核心原則

PUBLIC 可以使用與 OPS 一致的 Agent Handoff Kit 底層機制；不可接入 OPS 的資料層。

這代表：

- 可以公開：安裝方式、升級方式、AI agent 操作入口、公開版交接機制、公開文件索引、清理後的產品示例與套件內容。
- 不可公開：OPS 的交接歷史、session log、內部研發輸出、私人 Notion 資料、本機私人路徑、憑證或未清理素材。

## OPS 與 PUBLIC 的關係

| 工作區 | 功能 | 發佈角色 |
|---|---|---|
| OPS | 私有研發、驗收、內部治理、證據沉澱 | 產生候選成果，不直接公開 |
| PUBLIC | 公眾 GitHub / npm 產品發佈面 | 承接清理後內容，服務公眾安裝、升級與使用 |

同步只允許由 OPS 到 PUBLIC 的受控單向流程。PUBLIC 不自動同步 OPS，也不作為 OPS 的備份或鏡像。

## 從 OPS 到 PUBLIC 的同步流程

當 OPS 開發完成並通過驗收後，PUBLIC 發佈前必須完成：

1. 在 OPS 列明候選成果與驗收證據。
2. 將候選成果分類為可公開、需改寫、不可公開。
3. 移除 OPS 交接紀錄、研發證據、私人 Notion 資料、本機私人路徑、憑證和未授權素材。
4. 把可公開內容轉化為 PUBLIC 產品材料，例如 README、公開文件、示例、技能封裝或 npm package 檔案。
5. 在 PUBLIC 執行健康檢查、私隱掃描、差異檢查與必要產品測試。
6. 檢查通過後才可提交 PUBLIC。
7. push、tag、release、package publish 或部署必須另行取得明確授權。

## 可公開

- 產品用途、安裝方式、升級方式、操作流程和限制。
- 已清理的公開示例。
- 不依賴 Adam 私人 Notion 或本機路徑的通用文件。
- 經確認可公開授權的程式碼、技能檔和模板。
- Agent Handoff Kit 的公開操作規則。

## 不可公開

- OPS 治理檔、交接紀錄、session log、內部研發輸出。
- 私人 Notion database/page ID、本機絕對路徑、個人資料、未清理截圖。
- 憑證、token、API key、OAuth secret、refresh token 或任何可還原機密。
- 未確認授權的第三方全文、圖片、PDF 或資料集。

## 更新紀錄規則

PUBLIC 每次面向公眾的提交，都應同步更新 CHANGELOG.md。更新紀錄必須用繁體中文、非開發者可理解的固定格式；不要只寫 commit 訊息或技術差異。

## 發佈前檢查

每次公開發佈前至少確認：

- 沒有 OPS 私人資料被搬入。
- 沒有 credential 或可還原機密。
- README 沒有宣稱未完成能力。
- 安裝與升級說明仍指向目前可用的 Agent Handoff Kit 官方入口或產品自身 package 入口。
- 示例可由公眾理解，不需要 Adam 私人環境。
- GitHub repo、tag、release、package publish 另行取得明確授權。
