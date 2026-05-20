# Claude Code 能力素材庫（供給面總集）

> **整理日期**：2026-05-20（合併原 `claude-code-knowledge-100.md` + `mcp-cards-25-verified.md` + `skill-cards-30-verified.md`）
> **用途**：對應老闆痛點素材庫（pain-points-library.md），篩出卡牌高含金量內容
>
> **三區結構（MECE）**：
> - **A 區 — 100 條 Claude Code 內建能力**（10 大類，工具 / Memory / Agent / Skill 系統等）
> - **B 區 — 26 張 MCP 卡核實清單**（外掛跨系統工具，含雷區）
> - **C 區 — 30 張 Skill 卡核實清單**（可裝 Claude Code 的辦公 SOP 包）

---

# A 區：100 條 Claude Code 內建能力

> 分類：10 大類 × 每類 10 條

## 一、核心工具基礎（10 條）— 不會這些等於沒用 Claude Code

1. **Read**：精準讀檔（含 offset / limit / pages 範圍控制，大檔不爆 context）
2. **Edit**：精準字串取代（含 replace_all，可重命名變數）
3. **Write**：新建或全覆寫檔案（覆寫前必須先 Read）
4. **Bash**：執行 shell 指令（含 timeout / run_in_background）
5. **Grep**：codebase 內容全文搜尋
6. **Glob**：檔名模式搜尋（`**/*.md`）
7. **WebFetch**：抓取單一網頁全文
8. **WebSearch**：上網搜尋取摘要
9. **TodoWrite**：任務追蹤板（in_progress 一次只一條）
10. **Plan Mode**：先產出計畫 → 用戶批准 → 才執行

## 二、Memory 與知識管理（10 條）

11. **CLAUDE.md 三層級**：全域 `~/.claude/` / 專案目錄 / 客戶端附加
12. **MEMORY.md**：記憶索引（一行一筆 pointer 到實際 memory 檔）
13. **memory/ 目錄**：各類記憶檔分類（user / feedback / project / reference）
14. **CONVERSATION_LOG.md**：跨 session catch-up（prepend 結構）
15. **WORKING_MEMORY.md**：專案級流水帳（比 LOG 更詳細）
16. **五象限歸檔**：Knowledge / Agent Memory / Project Memory / Skill / Output
17. **記憶寫入時機**：對話中即時 prepend vs 用戶 say「log」vs 收工時
18. **記憶 vs Plan vs TodoWrite 三分工**：跨 session 保留 / 本次任務對齊 / 步驟追蹤
19. **記憶 stale 處理**：讀 memory 後要交叉驗證實際檔案
20. **CLAUDE.md 改寫鐵律**：規則直接寫進 CLAUDE.md，不開零碎 feedback 檔

## 三、Agent / Subagent 委派（10 條）

21. **Agent 工具**：派遣 subagent 處理獨立任務
22. **subagent_type 選擇**：Explore / general-purpose / Plan / claude / 自訂角色
23. **何時派 subagent**：研究 / 平行任務 / 保護主 context
24. **subagent prompt 設計**：自包含、提供完整 context、要求回報格式與字數
25. **run_in_background**：背景並行多 agent
26. **agent 結果驗證**：trust but verify（讀程式碼 / 檔案確認）
27. **平行多 agent**：同一訊息多個 Agent tool call 並發
28. **SendMessage**：延續同一個 agent（保留 context）
29. **agent isolation = worktree**：隔離 git 環境工作
30. **何時 NOT 派 subagent**：明確路徑 / 單一指令時直接做

## 四、Skill 系統（10 條）

31. **Skill 概念**：可重用的 SOP 包
32. **Skill 三層架構**：系統內建 / agent shared / agent 專屬
33. **SKILL.md 結構**：何時觸發 / 輸入 / 步驟 / 輸出
34. **Skill 觸發雙模式**：用戶 `/skill-name` 主動呼叫 vs CLAUDE.md 條件觸發
35. **Slash command 呼叫語法**：`/<skill-name>` 直接觸發
36. **Skill 觸發判斷表**：寫進 CLAUDE.md 對照表
37. **從重複任務升級為 skill**：第二次做相似事情時主動提議
38. **Skill 內部呼叫其他 skill / agent**：組合式工作流
39. **INDEX.md vs SKILL.md 分工**：人用的索引 vs AI 用的 SOP
40. **Skill 維護**：升級後同步更新 trigger 表

## 五、Hooks 自動化（10 條）

41. **Hook 概念**：事件觸發 shell 指令
42. **6 種事件**：PreToolUse / PostToolUse / Stop / SubagentStop / UserPromptSubmit / Notification
43. **常見用途**：自動 log / format / validate / inject context
44. **settings.json 配置 hook**：寫死自動行為
45. **Hook 訊息來源**：從 AI 角度被視為「來自用戶」的訊息
46. **Hook 阻斷工具呼叫**：exit code 非 0 可擋下動作
47. **Hook vs Skill 差異**：hook 被動觸發（事件）/ skill 主動呼叫（指令）
48. **update-config skill**：協助配置 settings.json 與 hook
49. **Hook 失敗排查**：log 路徑 / permission / sandbox 三層查
50. **Hook 安全**：避免在 hook 跑破壞性指令

## 六、MCP 跨系統整合（10 條，**詳細卡牌清單見 B 區**）

51. **MCP 概念**：Model Context Protocol，跨系統工具連接器
52. **系統內建 MCP**：fetch / nano-banana 等
53. **常用第三方 MCP**：Notion / Google Sheets / Gmail / Drive / Calendar
54. **MCP server resources**：ListMcpResourcesTool / ReadMcpResourceTool 取資源
55. **MCP 工具 namespace**：`mcp__<server>__<tool>` 命名規則
56. **MCP 認證流程**：OAuth / API key / token
57. **ToolSearch**：載入 deferred MCP 工具 schema
58. **MCP 集中管理**：settings.json 或 claude config
59. **MCP 工具的權限管理**：read-only / write 權限分級
60. **自建 MCP server**：mcp-builder skill 協助

## 七、多 Agent 協作架構（10 條）— 智谷的差異化

61. **多 agent 系統設計**：角色分工（C-suite 視角，非技術視角）
62. **Chief of Staff 協調層**：特別助理當主管團 hub（智谷獨家）
63. **shared/ 跨 agent 共用資源**：knowledge / projects / skills / assets 四大區
64. **Symlink 物理連接**：cross-agent visibility（檔案改一次大家共見）
65. **shared/projects**：協作案子只放 README 入口，工作檔在主責 agent
66. **shared/meeting-notes**：跨幕僚交辦事項（最新在最上方）
67. **Handoff 機制**：agent 之間任務交接
68. **Log routing**：本 agent CONV_LOG / shared meeting-notes 分流寫入
69. **Agent-level vs Project-level memory 分層**：跨案 vs 單案
70. **跨 agent 啟動掃描**：`find -L` 含 symlink 找所有 WORKING_MEMORY

## 八、工作流框架(10 條)

71. **Plan Mode 流程**：產 plan → ExitPlanMode → 執行
72. **TodoWrite 規則**：in_progress 一次只一條，完成即標記
73. **Plan vs TodoWrite vs Memory 三分工**
74. **平行工具呼叫**：同訊息多 tool call 並發
75. **鐵律治理**：CLAUDE.md 寫死鐵律，AI 自我校正
76. **啟動程序 SOP**：MEMORY.md → CONVERSATION_LOG（前 500 行）→ meeting-notes
77. **Compaction 後重讀**：MEMORY.md 進行中專案表格逐一讀
78. **建檔三問**：存什麼 / 誰讀 / 不存會怎樣
79. **STRUCTURE.md 歸檔規則**：建檔前必讀
80. **檔案輸出三問**：格式 / 位置 / 檔名

## 九、語氣 / 治理鐵律（10 條）— 智谷獨家

81. **自尊測試三問**（提案語氣鐵律）
82. **製造業 50+ 主管文化敏感性**
83. **用戶視角詞 vs 工程師術語**
84. **社畜口語 vs 書面語**
85. **AI Capability Cards 邊界**（只談痛點卡 + 能力卡）
86. **Symlink ≠ 便條**（物理協作優先）
87. **md 是 source 時直接 parse，不繞 MCP**
88. **改字級只改範圍，不要無腦全改**
89. **印刷品 A4 2×2 = 4 張留邊距**
90. **Design source 留可編輯版本**

## 十、進階機制（10 條）

91. **Permission modes**：read-only / acceptEdits / 自訂
92. **settings.json 三層**：global / project / local
93. **Background process**：Bash run_in_background + Monitor
94. **ScheduleWakeup**：`/loop` 動態節奏自我安排下次喚醒
95. **CronCreate**：定時任務（cron mode 排程）
96. **Worktree isolation**：git worktree 隔離工作環境
97. **Context window 管理**：subagent 切割 / compaction 自動觸發
98. **Slash commands**：`/help` `/clear` `/config` + 自訂指令
99. **Statusline 自訂**：底部狀態列顯示專案資訊
100. **Output styles**：CLI / VS Code / IDE 不同呈現方式

---

# B 區：26 張 MCP 卡核實清單

> **核實日期**：2026-05-19 sub-agent 上網驗證
> **後續補丁**：Telegram 新增 / LINE 改名加警語 / Jimmy 指示卡牌正面不標色標

## B-1. 辦公生產力（9 張）

| # | MCP | 用途 | 來源 | URL |
|---|-----|------|------|-----|
| 1 | **Notion** | 讀寫 workspace | Notion 官方 hosted | [link](https://www.notion.com/help/notion-mcp) |
| 2 | **Gmail / Google Workspace** | Gmail / Drive / Calendar / Sheets / Docs 六合一 | 社群 taylorwilsdon（12 服務） | [link](https://github.com/taylorwilsdon/google_workspace_mcp) |
| 3 | **Google Calendar** | 行事曆（純官方） | Google 官方 Workspace Dev Preview | [link](https://developers.google.com/workspace/calendar/api/guides/configure-mcp-server) |
| 4 | **Microsoft 365** | Outlook / Teams / SharePoint / OneDrive 全家 | Microsoft Work IQ 官方（需 Copilot 授權） | [link](https://learn.microsoft.com/microsoft-agent-365/tooling-servers-overview) |
| 5 | **MS 365 社群版** | 200+ tools 免 Copilot 授權 | Softeria 社群 | [link](https://github.com/softeria/ms-365-mcp-server) |
| 6 | **Slack** | 訊息 / 頻道 | Slack 官方 remote | 透過 Anthropic remote |
| 7 | **Airtable** | 資料表 | 官方 npm | [link](https://www.npmjs.com/package/airtable-mcp-server) |
| 8 | **Atlassian (Jira / Confluence)** | 專案管理 + 知識庫 | Atlassian 官方 remote | mcp.atlassian.com |
| 9 | **Telegram Bot** | 訊息推送 / 內部通知（**免費、無額度限制**） | 社群成熟實作 | [link](https://github.com/chigwell/telegram-mcp) |

## B-2. AI 工具（4 張）

| # | MCP | 用途 | 來源 | URL |
|---|-----|------|------|-----|
| 10 | **nano-banana 生圖** | Gemini Flash Image 生圖 | 社群 zhongweili + Google CLI ext | [link](https://github.com/zhongweili/nanobanana-mcp-server) |
| 11 | **ElevenLabs** | TTS / 語音克隆 / STT | ElevenLabs 官方 | [link](https://github.com/elevenlabs/elevenlabs-mcp) |
| 12 | **Perplexity** | 即時網路搜尋 | Perplexity 官方 | [link](https://github.com/perplexityai/modelcontextprotocol) |
| 13 | **NotebookLM** | 操作 NotebookLM | 社群 PleasePrompto（Playwright 自動化，穩定性差） | [link](https://github.com/PleasePrompto/notebooklm-mcp) |

## B-3. 商業系統（6 張）

| # | MCP | 用途 | 來源 | URL |
|---|-----|------|------|-----|
| 14 | **Stripe** | 金流 | Stripe 官方 remote | stripe.com |
| 15 | **HubSpot** | CRM | HubSpot 官方 remote GA（2026/4） | [link](https://www.mcpbundles.com/blog/best-mcp-servers) |
| 16 | **Salesforce** | CRM | Salesforce 官方 | github.com/salesforcecli/mcp |
| 17 | **Shopify** | 電商 | Shopify 官方 4 個 MCP | shopify.com |
| 18 | **Xero** | 會計 | XeroAPI 官方 | [link](https://github.com/XeroAPI/xero-mcp-server) |
| 19 | **Linear** | 任務管理 | Linear 官方 remote | linear.app |

## B-4. 開發 / 自動化（3 張）

| # | MCP | 用途 | 來源 | URL |
|---|-----|------|------|-----|
| 20 | **GitHub** | repo / issue / PR | GitHub 官方（與 Anthropic 協作） | [link](https://github.com/github/github-mcp-server) |
| 21 | **Zapier** | 接 8000+ apps | Zapier 官方 | zapier.com/mcp |
| 22 | **Playwright** | 瀏覽器自動化 | Microsoft 官方 | [link](https://github.com/microsoft/playwright-mcp) |

## B-5. 設計（2 張）

| # | MCP | 用途 | 來源 | URL |
|---|-----|------|------|-----|
| 23 | **Figma Dev Mode** | 設計稿 | Figma 官方 | fast.io |
| 24 | **Canva** | 模板設計 | Canva 官方（MCP Apps 計畫） | canva.com |

## B-6. 製造業 / ERP（1 張）

| # | MCP | 用途 | 來源 | URL |
|---|-----|------|------|-----|
| 25 | **SAP S/4HANA** | ERP（**只 SAP 有，其他 ERP 多半要自建 wrapper**） | SAP 官方 ABAP add-on | [link](https://community.sap.com/t5/technology-blog-posts-by-members/mcp-server-for-sap-ecc-amp-s-4hana-unlimited-abap-add-on-for-display-create/ba-p/14293485) |

## B-7. 台灣本地（1 張）

| # | MCP | 用途 | 來源 | URL |
|---|-----|------|------|-----|
| 26 | **LINE OA 廣播**（單向推播） | 推給已加 OA 好友的訂閱者 | LINE 官方 preview（v0.4.2, 2025/11） | [link](https://github.com/line/line-bot-mcp-server) |

### ⚠️ LINE OA 廣播使用限制（學員裝前必看）

| 限制 | 細節 |
|------|------|
| 💰 月推送額度 | 免費 200 則 / 月（2026 從 500 降）、輕量 NT$800 / 3,000 則、中量 NT$1,200 / 6,000 則 |
| 🚫 不能讀 / 不能回 | 無 reply / read tool — 做不了自動客服 |
| 👤 不能冷推陌生人 | user 必須先加 OA 為好友才能推 |
| 🛠️ 裝機門檻 | Node v22+（一般 Mac 預設 18/20 會 npx 失敗）|
| 🆔 必備設定 | LINE Developers 帳號 + Channel Access Token + Channel Secret |

→ **適合**：公司有 OA、推促銷 / 出貨通知 / 群發公告
→ **不適合**：個人 LINE 自動化、自動客服、冷推陌生客戶

## ❌ MCP 雷區（瞎列 = 整套被質疑）

| 名稱 | 原因 |
|------|------|
| **eFax** | 只有冷門社群 server，給 OpenText 傳真機解 PDF 用 |
| **LINE Notify** | 2025 年已停止服務 |
| **DALL-E / GPT 繪圖獨立 MCP** | 不存在，靠 nano-banana 或 Zapier 接 |
| **Coda** | 沒有官方，社群也沒像樣版本 |
| **Whisper 官方 MCP** | OpenAI 沒做 |
| **QuickBooks 直連 MCP** | Intuit 無官方，靠 Numeric / Zapier 包 |
| **政府電子採購網「官方」** | 沒有，只有社群封裝 g0v 開源 API |

## MCP 後備清單（如前 26 有變動）

Cloudflare 13 個 / Discord / Asana / Supabase / PostgreSQL / Sentry / YouTube / LinkedIn / X / Reddit / Oracle DB / 政府電子採購網（g0v 社群版）

---

# C 區：30 張 Skill 卡核實清單

> **核實日期**：2026-05-19 sub-agent 上網驗證
> **三大來源**：Anthropic 官方 8 + Corey Haines marketingskills 13（29.4k ★）+ w95 corporate skills 9（36 ★）
> **卡牌正面不分官方 / 社群**（Jimmy 指示，學員不在意誰做的）

## C-1. Anthropic 官方 — 文件處理（8 張）

| # | Skill | 一句話 | URL |
|---|-------|------|-----|
| 1 | **pptx** | 一句話生出乾淨可改的 PPT | [link](https://github.com/anthropics/skills/tree/main/skills/pptx) |
| 2 | **docx** | 零散文字組成正式 Word（含目錄/抬頭） | [link](https://github.com/anthropics/skills/tree/main/skills/docx) |
| 3 | **xlsx** | Excel 公式、樞紐、清髒資料一次到位 | [link](https://github.com/anthropics/skills/tree/main/skills/xlsx) |
| 4 | **pdf** | PDF 合併、拆檔、抓表格、套浮水印 | [link](https://github.com/anthropics/skills/tree/main/skills/pdf) |
| 5 | **internal-comms** | 寫狀態報告、跨部門公告、FAQ、事故報告 | [link](https://github.com/anthropics/skills/tree/main/skills/internal-comms) |
| 6 | **brand-guidelines** | 文件自動套上公司色票 / 字體 | [link](https://github.com/anthropics/skills/tree/main/skills/brand-guidelines) |
| 7 | **doc-coauthoring** | 帶你寫提案 / 規格書 / 決策文件 | [link](https://github.com/anthropics/skills/tree/main/skills/doc-coauthoring) |
| 8 | **canvas-design** | 出海報、卡片、視覺設計（PNG / PDF） | [link](https://github.com/anthropics/skills/tree/main/skills/canvas-design) |

## C-2. Corey Haines marketingskills（13 張，29.4k ★）

| # | Skill | 一句話 | URL |
|---|-------|------|-----|
| 9 | **copywriting** | 寫首頁 / Landing / 產品頁文案 | [link](https://github.com/coreyhaines31/marketingskills/tree/main/copywriting) |
| 10 | **copy-editing** | 把現有文案改得更短更利 | [link](https://github.com/coreyhaines31/marketingskills/tree/main/copy-editing) |
| 11 | **cold-email** | 寫 B2B 開發信 + 多封 follow-up | [link](https://github.com/coreyhaines31/marketingskills/tree/main/cold-email) |
| 12 | **sales-enablement** | 生 pitch deck、One-pager、異議處理稿 | [link](https://github.com/coreyhaines31/marketingskills/tree/main/sales-enablement) |
| 13 | **pricing** | 定價分層 / 包裝 / 漲價策略 | [link](https://github.com/coreyhaines31/marketingskills/tree/main/pricing) |
| 14 | **seo-audit** | 網站 SEO 健檢報告 | [link](https://github.com/coreyhaines31/marketingskills/tree/main/seo-audit) |
| 15 | **emails** | onboarding / nurture / win-back email 序列 | [link](https://github.com/coreyhaines31/marketingskills/tree/main/emails) |
| 16 | **launch** | 產品上市 / 新功能發表 playbook | [link](https://github.com/coreyhaines31/marketingskills/tree/main/launch) |
| 17 | **competitors** | 競品比較頁 / Alternative 頁 | [link](https://github.com/coreyhaines31/marketingskills/tree/main/competitors) |
| 18 | **marketing-psychology** | 70+ 行為心理學原則套到文案 | [link](https://github.com/coreyhaines31/marketingskills/tree/main/marketing-psychology) |
| 19 | **churn-prevention** | 取消挽留流程 / 減少流失 | [link](https://github.com/coreyhaines31/marketingskills/tree/main/churn-prevention) |
| 20 | **cro** | 頁面 / 表單轉換率優化 | [link](https://github.com/coreyhaines31/marketingskills/tree/main/cro) |
| 21 | **social** | LinkedIn / X / IG 社群貼文 + 排程 | [link](https://github.com/coreyhaines31/marketingskills/tree/main/social) |

## C-3. w95 corporate skills（9 張，36 ★，HR/法務/採購類）

| # | Skill | 一句話 | URL |
|---|-------|------|-----|
| 22 | **board-meeting-prep** | 董事會簡報架構 + 預期提問 | [link](https://github.com/w95/awesome-claude-corporate-skills) |
| 23 | **strategic-planning** | OKR / SWOT / 年度策略文件 | 同上 |
| 24 | **business-case-builder** | 寫投資 / 專案商業提案 ROI | 同上 |
| 25 | **incident-postmortem** | 事故覆盤 / 檢討報告 | 同上 |
| 26 | **qbr-builder** | 客戶季度檢討會 QBR 簡報 | 同上 |
| 27 | **job-description-writer** | 寫 JD、面試題庫、Offer Letter | 同上 |
| 28 | **performance-review-assistant** | 員工績效評估 / PIP 草稿 | 同上 |
| 29 | **contract-review** | 合約風險點 / NDA 快速審閱 | 同上 |
| 30 | **theme-factory** | 一鍵幫簡報 / 文件套主題色 | [link](https://github.com/anthropics/skills/tree/main/skills/theme-factory) |

## Skill 後備清單（10 張，前 30 有變動時替換）

competitive-analysis / risk-assessment / change-management / kpi-dashboard / sop-builder / rfp-builder / ad-creative / analytics / onboarding / content-strategy

## ❌ Skill 雷區（避免下游打臉）

- **executive-mentor / scenario-war-room**：Jimmy 自用，不在公認 repo（要保留須標客製版）
- **ppt-build / market-launch / market-audit / market-report**：Jimmy 自製 / 中文社群，學員找不到
- **mcp-builder / claude-md-improver / init / review / security-review**：偏 dev 流，老闆學不到
- **dei-strategy**：台灣中小企業無 fu
- **schema-markup / programmatic-seo / ai-seo**：太技術
- **referral-program / popup-cro / form-cro**：偏 SaaS growth，傳產老闆不會用

## Skill Sources

- [Anthropic Skills 官方](https://github.com/anthropics/skills)（135k ★）
- [Corey Haines marketingskills](https://github.com/coreyhaines31/marketingskills)（29.4k ★）
- [w95 awesome-claude-corporate-skills](https://github.com/w95/awesome-claude-corporate-skills)（36 ★）
- [travisvn awesome-claude-skills](https://github.com/travisvn/awesome-claude-skills)
- [alirezarezvani claude-skills](https://github.com/alirezarezvani/claude-skills)

---

# 用法（給下游卡牌設計）

1. **A 區**作為「Claude Code 能力地圖」— 確認任務卡 / Power 卡覆蓋面（10 大類有沒有漏）
2. **B 區**直接餵進卡牌的 MCP 卡（26 張，含警語 + 雷區避雷）
3. **C 區**直接餵進卡牌的 Skill 卡（30 張）；老闆視角組合：一個任務動作可能要 2-5 張 skill（例：DOCX 製作 = docx + brand-guidelines + theme-factory + doc-coauthoring）
4. **MCP 卡跟 Skill 卡的差異**：MCP = 跨系統工具（連別人系統），Skill = 可裝的 SOP 包（執行特定任務）。學員容易混淆，講師要點明
