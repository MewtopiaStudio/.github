# MewtopiaStudio 專案管理規則（v0.1）

## 方向

- `.github`：公開首頁與協作政策；每款遊戲一個 Repo；`CatGameFramework` 獨立存放共用 TypeScript 核心。
- README、Issue、驗收、SOP 預設使用**繁體中文**；程式識別字與命令維持英文。
- 品牌與商標使用仍待正式查證，不宣稱已註冊或完全沒有撞名風險。

## 工作流程

1. 先建立 Issue：目的、範圍、驗收條件、相關 Repository。
2. 開發使用 `feature/<topic>`、`fix/<topic>` 或 `docs/<topic>` 分支。
3. 以 PR 合併，填寫測試結果與風險。
4. 先完成核心功能 → 盤點缺陷 → 一次性人工情境驗收 → 再處理美工。
5. 重要驗收 PASS 才建立 Tag／Release，不強推或重寫共用 main 歷史。

## 命名與優先度

Issue 前綴：`[Setup]`、`[Game]`、`[Framework]`、`[UI]`、`[Build]`、`[Docs]`、`[Brand]`。

- **P0**：阻斷開發或無法測試；優先處理。
- **P1**：核心功能或重大一致性缺陷。
- **P2**：外觀、體驗、維護性改善。

## GitHub Projects 看板（待建立）

名稱：`Mewtopia Roadmap`。Status：Backlog / Ready / In progress / In review / Done。

建議欄位：Priority、Phase、Repository、Assignee。Issue 先建在對應的 Repo，再匯入 Project。

## 安全與品質

- 禁止提交金鑰、密碼、未授權字型／圖片／第三方素材。
- 框架每次 PR 都須通過 TypeScript 編譯與單元測試。
- Cocos 遊戲需另外驗證場景、觸控、裝置與輸出格式。
- 免費方案私人 Repo 的分支保護是否能強制執行，需以 GitHub 設定頁面為準。
