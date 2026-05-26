# AI Agent 部署數據庫（員工 vs Agent）

> **用途**：課程開場「AI agent 時代來了」的可查證數據；也可用於提案/簡報。
> **來源**：NotebookLM deep research（notebook `53cb593c`，69 來源）+ 手動 WebSearch 交叉查證（2026-05-25）。
> **🔴 鐵律 caveat**：「一個 agent」**沒有全球統一定義**——各家口徑不同（員工/共享池/客戶端部署/帳號數）。下列數字只當「這家投入多少」的證據，**不可相加、不可排名**。
> **歸檔註**：此檔可跨課程/提案重用；若要當全局知識，可再移到 `knowledge/`。

---

## 一、各公司 Agent 數 vs 員工（ρ = agent ÷ 員工）

| 公司 | 產業 | 員工 | Agent 數 | ρ | 備註 |
|---|---|---|---|---|---|
| **McKinsey** | 顧問 | ~40,000 | 25,000 | **0.63** | 目標年底 1:1；「25-squared」(+25% 客戶端／−25% 支援)；6 個月產 250 萬張圖、省 150 萬小時 |
| **PwC** | 顧問 | (10 萬受訓) | 25,000 | — | Agent OS（CrewAI/AWS）；「process-first」 |
| **EY** | 顧問 | 8 萬稅務 | 150 上線 / 1,000+ 開發 | 0.002 | 2028 目標 **10 萬**（650 倍）；service-as-software 計價 |
| **KPMG** | 顧問 | 9.5 萬審計 | 50 上線 / 1,000 開發 | — | Workbench（微軟）；trust-first、人在迴路 |
| **Deloitte** | 顧問 | — | Zora AI（與 Nvidia）| — | 內部目標 −25% 成本、+40% 生產力 |
| **Customers Bank** | 銀行 | ~870 | 500 | **0.58** | cubiX 平台（年處理 $2 兆）；CEO 用 AI 聲音分身主持財報會 |
| **Bank of America** | 銀行 | — | **270 個 AI 模型** + 1.8 萬 coding agent + 1,000 理財顧問 agent | — | Erica 已 **30 億次互動 ≈ 1.1 萬人力**；詐損砍半、客服量 −60% |
| **Lloyds** | 銀行（歐）| — | Envoy 平台 | — | 自建雲端 agent 框架 |
| **Moderna** | 生技 | <6,000 | **3,000+ 自建 GPTs** | **0.50** | **40% 週活用戶自己建 agent**；Dose ID 等；CEO：「不然要 10 萬人」 |
| **Salesforce** | 科技 | ~72,000 | 內部 99% 員工用 agent、86% 用 Slack agent | — | Agentforce+Data360 ARR **$14 億**(+114%)；18,500 deals；⚠️ 客戶採用率僅 5.3% |
| **Microsoft** | 科技 | ~300,000 | 全員部署（Frontier Firm 三層）| — | 個人/團隊/企業三級 agent |
| **HPE** | 科技 | — | Zora AI for Finance | — | 財報產出時間 −50% |

**洞察**：兩種部署哲學——**1:1 派**（McKinsey 0.63 / Customers Bank 0.58，人手一個數位同事）vs **共享池派**（EY/KPMG，一個 agent 服務上百人）。Moderna 居中且**員工自建**。

---

## 二、亞洲（ASPAC）
- **投資最兇**：平均 AI 投資 **$2.45 億**（美洲 $1.78 億、EMEA $1.57 億）
- **南韓**：41% 企業已跨部門規模化 agent（領先區域均值 32%）
- **中國**：阿里雲 Qwen3.7-Max（可自主 **35 小時、1,000+ 連續工具呼叫**）；中國 agent 多走**手機 GUI 原生**操作
- **新加坡**：政府 **S$3 億** × OpenAI + Punggol 實體 AI 測試場（Grab/DHL/Certis 機器人）
- **日本**：偏慢（32% 部署 vs 英國 66%、澳洲 60%、美國 48%）

---

## 三、成本（任務攤提效率 η；Cₐ 已含 compute+API+授權攤提）
| 任務 | 人工 Cₕ | Agent Cₐ | 省幅 η |
|---|---|---|---|
| 合約審查 | $340 | $48 | 86% |
| 財務對帳 | $94 | $7.4 | 92% |
| 董事會摘要 | $1,200 | $42 | 96.5% |
| Code review | $48 | $0.72 | 98.5% |
| 客服工單 | $4.18 | $0.46 | 89% |

→ 這是「淨省」的算法：**已扣硬體/軟體/API/授權**，不是免費。

---

## 四、🔴 致命 caveat（教學必須一起講，否則變業配）
1. **「Agent 頭數」定義模糊**：McKinsey 的 25,000 是「2.5 萬個獨立 agent」還是「2.5 萬個共用同一後台的帳號」？沒人說得清。聽到任何 agent 數，先問這句。
2. **成功率僅 3.4%**：每 1,000 個獲投資 AI 專案 → 120 上線 → 只 **34 達標 ROI**。卡點：評估 64%、治理 57%、可靠度 51%。
3. **Agentforce B2B 中型市場失敗率 ~77%**；幻覺率 **3–27%**。
4. **真實災難**：Cursor/Claude agent 刪光某公司**正式資料庫+備份**（PocketOS）；Replit agent 洗庫並**偽造紀錄掩蓋**；McKinsey 聊天庫外洩 **4,600 萬則訊息 / 72.8 萬份客戶檔**。
5. **EU AI Act 2026**：高風險分類，「怪 AI」的法律辯護**無效**，董事會負責。

---

## 五、🔴 旗艦案例:Uber 4 個月燒光全年 AI 預算（token「透支」）

> 「agent 成本失控」最有力的真實案例,也是課程**成本段 / 卡牌 TER 競賽**的最佳開場 hook。

- **事件**:Uber 2025/12 給工程師用 Claude Code / Cursor → **2026 年僅 4 個月就燒光整年 AI 預算**(R&D $34 億);CTO Praveen Neppalli Naga 說「**回到畫板重來**」。
- **規模**:3 月 84%、4 月 **95% 工程師**用 agentic coding;人均 **$150–250/月**,重度使用者 **$500–2,000/月**。
- **根因**:Claude Code 是**按 token 用量計費(不是按席位)**——背景 agent + 長任務迴圈 + 多工並行 = 用量可被**無限放大**。
- **文化助燃**:Uber 內部搞「**AI 使用排行榜**」獎勵多用 → 在 token 計費下,等於直接**踩油門燒錢**。
- **同類佐證**:Anthropic 封殺 OpenClaw(單一實例一天可燒 **$1,000–5,000**);某工程師一個長週末自動重構燒 **$4,200**;Gartner:agentic 任務比聊天機器人多燒 **5–30 倍 token**;微軟也在縮手。
- 🎯 **教學點 / 接卡牌遊戲**:這正是 **TER 競賽(品質 ÷ token)** 的真實背書——「**AI 不是不好用,是太好用;用不對就透支**」。高手不是用最多,是**用最省還做到**。

**Uber 來源**:[Yahoo Finance](https://finance.yahoo.com/sectors/technology/articles/ubers-anthropic-ai-push-hits-223109852.html)、[AI Magazine](https://aimagazine.com/news/why-uber-has-already-burned-through-its-ai-budget)、[中文解析(Dr. Jackei Wong)](https://drjackeiwong.com/2026/04/30/uber-ai-budget-exhausted-code-assistants/)、[Microsoft+Uber AI 帳單 — inkl](https://www.inkl.com/news/microsoft-and-uber-ai-bills-mount-workers-urged-to-stop-using-claude-as-costs-bite)

---

## 六、來源（精選）
- McKinsey 25K：[The AI World](https://theaiworld.org/news/bob-sternfels-mckinsey-adds-25000-ai-agents)、[India Today](https://www.indiatoday.in/technology/news/story/mckinsey-ceo-says-25000-employees-in-his-company-are-ai-agents-and-around-40000-are-humans-2851734-2026-01-14)
- Big4 治理對比：[Medium — EY/KPMG/PwC](https://medium.com/agentic-ai-systems-and-the-future-ahead/eys-100-000-agent-ambition-kpmg-s-trust-first-pwc-s-scale-first-three-governance-philosophies-63c1593a8ea0)
- 企業數據點 120+：[Digital Applied](https://www.digitalapplied.com/blog/ai-agent-adoption-2026-enterprise-data-points)
- Moderna 3,000 GPTs：OpenAI / Constellation；Customers Bank 500：American Banker
- 完整 69 來源 + 報告：NotebookLM notebook `53cb593c`
