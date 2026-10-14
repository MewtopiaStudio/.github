# GitHub 組織初始化 SOP

> 2026-10-14 初始原始碼與 Issue 已提交。以下標示「待操作」的項目，不代表已在 GitHub 設定完成。

## 已完成

- [x] 建立公開 `.github` Repo，並提交 `profile/README.md`
- [x] 建立私人 `CatDownstairs` Repo，提交 Cocos Creator 操作原型
- [x] 建立私人 `CatGameFramework` Repo，提交純 TypeScript 共用核心、測試及 Workflow
- [x] 建立首波 GitHub Issues 與管理政策文件

## 待人工完成

### 1. 上傳 Logo PNG

進入 [組織資產目錄](https://github.com/MewtopiaStudio/.github/tree/main/assets)，選 **Add file → Upload files**，上傳：

- `mewtopia-emblem.png`（圓形圖章）
- `mewtopia-wordmark.png`（文字 Logo）

精確的圖片位元資料在 Starter Pack 的 `.github/assets/` 目錄；完成後檢查 [組織首頁](https://github.com/MewtopiaStudio) 圖片顯示。

**組織大頭貼**：需另至 Organization Settings 的 Profile/General（介面依 GitHub 版本為準）上傳圓形圖章，README 內的圖片不會自動取代組織頭像。

### 2. 組織 Team 與基礎權限

參照 [TEAM_PERMISSIONS.md](./TEAM_PERMISSIONS.md)：

- 在 Organization Settings → Member privileges 檢查 Base permissions，優先考慮 None。
- 有實際協作者時，在 Organization → Teams → New team 新增 `game-dev`、`framework-maintainers`、`reviewers`。
- 到各 Repository 的 Settings → Collaborators and teams 進行最小權限授權。
- 確認私人 Repo 不會因設定而意外公開。

### 3. GitHub Project

在 Organization → Projects 建立 `Mewtopia Roadmap`：

- Status：Backlog / Ready / In progress / In review / Done
- 建議欄位：Priority（P0/P1/P2）、Phase、Repository、Assignee
- 連結 `CatDownstairs` 的 Issues #1–#6 與 `.github` 的設定類 Issues。

### 4. 分支與合併

- `main` 為穩定基線，功能開發使用 `feature/*`，修正使用 `fix/*`。
- 修改經 Pull Request 與驗收後合併，不直接 force push main。
- 到每個 Repo 的 Settings → Rules（或 Branches）確認分支保護功能是否可用、能否強制執行。
- 免費方案私人 Repo 的相關保護設定可能受限制，應以實際 UI/方案為準。

### 5. 開發驗收

- 於 CatGameFramework → Actions 確認 Core checks 的執行結果。
- 在實際 Cocos Creator 3.8.x 編輯器建立 `Game.scene` 和 Node 綁定後驗收。
- 只有正式驗收 PASS 才標示相應里程碑完成。
