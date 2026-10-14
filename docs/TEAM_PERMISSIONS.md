# MewtopiaStudio Teams 與最小權限規範

> 本文件是建議設定；**不代表 GitHub Team 或組織 Settings 已經自動設定完成**。

| 團隊／角色 | `.github`（Public） | `CatDownstairs`（Private） | `CatGameFramework`（Private） |
| --- | --- | --- | --- |
| Organization Owners | Admin | Admin | Admin |
| `game-dev` | 可讀 | Write | Read |
| `framework-maintainers` | 可讀 | Read | Write |
| `reviewers` | 可讀 | Read | Read |

## 組織設定建議

1. 到 **Organization Settings → Member privileges**，若允許請將 Base permissions 設成 **None**，避免成員自動讀取私人 Repo。
2. 只保留少數 Owner；一般協作者是 Member。
3. 新增團隊：**Organization → Teams → New team**。僅在有實際成員時建立，免得增加空團隊管理負擔。
4. 在 Repo 的 Collaborators and teams 針對團隊授權。需 Review 的使用者也可能需要 Write 才能核准合併，依實際工作流程再提高權限。
5. 不要把 AI 助理當成 GitHub 組織成員。ChatGPT 使用 GitHub App 授權。
6. 每次新增人員及對外公開前，重新確認私人 Repo、Fork、第三方授權的設定。

**注意：** GitHub Free 與 Private Repo 的分支保護強制執行功能可能有限；以實際設定頁面是否允許 Enforcement 為準。
