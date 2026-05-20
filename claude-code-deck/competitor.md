# Claude Code 卡牌專案 — 競品研究

> **建立日期**：2026-05-19
> **主責**：教學設計師 + 產品企劃主管（共讀）
> **整合範圍**：5/14 啟動以來所有競品研究（英文圈 / 中文台灣 / 跨領域借鏡）
> **定位**：**Single source of truth** — 競品數據以本檔為準。instruction-design.md 是教學設計法庫，這檔是市場 / 競品 / 定價庫。
> **核心問題**：「**台灣 / 英文圈，現在有多少人在教 agent team？以什麼方式？定價多少？智谷的縫隙在哪？**」

---

## 📑 目錄

- [A. 全球地圖 — agent team × 卡牌交集分析](#a)
- [B. 英文市場 — Claude Code / GenAI 教學玩家](#b)
- [C. 台灣繁中市場 — 30 家完整盤點](#c)
- [D. 標竿競品深挖（5 家）](#d)
- [E. 台灣 multi-agent 公開課定價 survey](#e)
- [F. 教學法借鏡（非競品但機制可移植）](#f)
- [G. 智谷戰略結論](#g)

---

<a id="a"></a>
## A. 全球地圖 — agent team × 卡牌交集分析

### A1. 核心發現（最重要）

**「agent team × 實體卡牌」這個交集，全球零競品**。智谷護城河成立。

兩條主流路線各自存在，但**沒人把兩條路合起來**：

| 維度 | 代表玩家 | 形態 | agent team? | 實體卡? |
|------|---------|------|------------|--------|
| **英文教 GenAI 卡牌的最強玩家** | [AI Tinkerers' Cards](https://ai-tinkerers.cards/)（Alex Eisenchteter / Stormz 創辦人 / 5/14 v0.1 逆向工程 source）| 81 張卡，€1 起 / €49 進階 | ❌ Generic GenAI / Prompt 工程 | ✅ 實體 |
| **英文教 agent team 的最強玩家** | [DigitalApplied AI Virtual Team Playbook](https://www.digitalapplied.com/blog/ai-virtual-team-specialist-agent-squad-playbook) | 10 agents 完整角色 + system prompts + 委派矩陣 + orchestration workflow | ✅ 學員定位「non-technical founders」（**跟智谷一模一樣**） | ❌ 純文字 blog playbook |
| **兩者的交集（agent team × 實體卡）** | **不存在** | — | — | — |

### A2. 智谷剛好填中間真空

- AI Tinkerers' Cards 已經把「**卡牌教 AI**」走通 → 沒擴展到 agent team
- DigitalApplied 已經把「**10 個 virtual specialist agent**」走通 → 沒做成實體卡
- **智谷把兩條路的優點合起來** = 卡牌實體 × C-suite 6 角色 agent team × 老闆視角

### A3. 三大市場 segment 對位

| Segment | 英文圈代表 | 中文圈代表 | 智谷對位 |
|--------|----------|----------|--------|
| **工程師派**（教框架 / 寫代碼 / Dify）| Coursera / Frontend Masters / Code with Antonio | 天地人 AutoGen / iSpan / 台大 / HiSKIO / 工研院 | ❌ 不打 |
| **工作者派**（個人生產力 / 單 agent）| CC for Everyone / Claude Quest / KDnuggets | 雷蒙 / Hahow / PressPlay / 新商業學校 | ❌ 不打 |
| **老闆論壇派**（趨勢 / 視野 / 不動手）| Mastercard Virtual C-Suite / AI 治理 cards | 商周 CEO 學院 / 經理人年會 / BCG / airabbi | ❌ 不打 |
| **🎯 智谷的金礦**：老闆視角 × **動手做 agent team** × **卡牌實體** | **空白** | **空白** | ✅ 唯一 |

---

<a id="b"></a>
## B. 英文市場 — Claude Code / GenAI 教學玩家

### B1. Claude Code 教學玩家盤點（9 家）

| # | 玩家 | 形態 | 定位 | 對智谷威脅 |
|---|------|------|------|--------|
| 1 | [Claude Quest (SeanZoR)](https://github.com/SeanZoR/claude-quest) | 90 成就 / 8 大類遊戲化外掛 | 線上單人 / 中初學員 / 系統化探索 | 🟢 低（線上單人，非老闆視角）|
| 2 | [CC for Everyone](https://ccforeveryone.com/) | Learn Claude Code IN Claude Code / no videos no docs | 非技術 / 零基礎 | 🟡 中（敘事力高，但 slash 引導與 Jimmy 偏好相反）|
| 3 | [Anthropic Code with Claude](https://claude.com/code-with-claude) | SF / London / Tokyo 三城實體 conf | 開發者社群 | 🟢 低（市場層級不同）|
| 4 | [Frontend Masters Deep Dive](https://frontendmasters.com/workshops/advanced-claude-code/) (Lydia Hallie) | mental model first → CLAUDE.md → MCP | 工程師 / 進階 | 🟢 低（工程師取向）|
| 5 | [Code with Antonio](https://www.codewithantonio.com/cohorts/build-your-own-claude-code-2026-05) | 6 天 cohort 從零做 Claude Code CLI | 工程師逆向工程 | 🟢 低 |
| 6 | [KDnuggets 5 Fun Projects](https://www.kdnuggets.com/5-fun-projects-using-claude-code) | 5 個趣味 coding 專案 | 開發者 | 🟢 低（全 coding，老闆 0 個能跑）|
| 7 | [claude.nagdy.me](https://www.blocktempo.com/learn-claude-code-interactive-browser-terminal-simulator-free-no-install/) | 瀏覽器 terminal 模擬器 11 堂 | 免安裝免 key | 🟢 低 |
| 8 | [Anthropic Skilljar](https://anthropic.skilljar.com/claude-code-in-action) + 13 堂官方課 | 官方證書 / B2C | 線上自學 | 🟡 中（官方品牌，但無 B2B 動能）|
| 9 | [Coursera: Claude Code](https://www.coursera.org/learn/claude-code) | Software Engineering with Generative AI Agents | 學術 / 工程師 | 🟢 低 |

### B2. 教 GenAI 通用卡牌（非 Claude Code 但同形態 = 卡牌）

| # | 玩家 | 形態 | 對智谷威脅 |
|---|------|------|--------|
| 10 | [AI Tinkerers' Cards](https://ai-tinkerers.cards/)（Alex / Stormz） | 81 張：Starter Kit 24 張 €1 / Base Deck 37 張 €49 / Prompt Engineering 20 張 €49 | 🟡 中（同卡牌形態的標竿，但教 generic GenAI 非 agent team）|
| 11 | [Thoughtworks "Singularity"](https://www.thoughtworks.com/en-us/insights/blog/generative-ai/lets-play-singularity-ai-governance-card-game) | AI 治理風險卡牌 / 腦力激盪 | 🟢 低（AI 倫理，主題不同）|
| 12 | [In The Pocket AI Card Game](https://www.inthepocket.com/blog/get-inspired-with-ai-by-playing-our-card-game) | 探索 GenAI 卡牌 | 🟢 低 |
| 13 | [Trustworthy AI Cards](https://www.aiethicist.org/trustworthy-ai-cards) | AI 倫理 / 治理用 | 🟢 低 |
| 14 | [Workshops & Wizards](https://www.sessionlab.com/blog/facilitation-cards/) | D&D 風工作坊技巧卡 | 🟢 低（教 facilitation 非 AI）|

### B3. 教 agent team 但無卡牌

| # | 玩家 | 形態 | 對智谷威脅 |
|---|------|------|--------|
| 15 | [DigitalApplied AI Virtual Team Playbook](https://www.digitalapplied.com/blog/ai-virtual-team-specialist-agent-squad-playbook) | 10 specialist agents + role cards 模板 + 委派矩陣 + orchestration workflow / non-technical founders | 🔴 高（**學員定位最像智谷**，但純文字 blog 無卡牌）|

---

<a id="c"></a>
## C. 台灣繁中市場 — 30 家完整盤點

### C1. 核心圈🎯（真在教 multi-agent / agent team）— 6 家

**重點**：**0 家是「老闆視角 × C-suite 6 角色 × 桌面卡牌」**。最接近的都是工程框架 / Dify / IT 取向。

| # | 玩家 | 路線 | 主力課程 | 學員定位 |
|---|------|------|--------|--------|
| 1 | **天地人學堂** | AutoGen 開發框架 | c1534 多代理人實作課（3hr 線上 NT$3,890）/ c1589 工作坊（6hr 實體 NT$3,880-10,000）| 開發者 / AI 初學者 |
| 2 | **iSpan 資展國際** | Agentic AI 企業 workflow | AIA / AIB / AIAGENT 三班（21hr 三日 NT$12,000-21,000）| IT / PM / 技術中高 |
| 3 | **CPC 中國生產力中心** | Dify + 地端 LLM + RAG | AI Agent 地端實戰（12hr 兩日 NT$8,550-9,000）| 數位轉型負責人 / IT |
| 4 | **台大資訊系統訓練班** | LLM → Multi-Agent 工程實作 | AI Agent 開發與多智能體實作（12hr 兩日 NT$4,500）| 技術背景 |
| 5 | **工研院產業學院** | 流程自動化 / 服務業導入 | AI Agent 流程自動化實作 / 智慧轉型實戰班（補助免費）| 零售 / 餐飲 / 物流業主 |
| 6 | **雷蒙三十** | 個人生產力 KOL | 24 小時 Claude Code 迷你課 NT$2,000-6,000 | 一人公司 / 上班族 |

### C2. 中外圈🟡🔵 — 24 家簡表

| 玩家 | 平台 | 主力課程 | 層 | 定價 NTD | Agent Team? |
|------|------|--------|---|---------|------------|
| 黃琇琳 | 天下學習 | 打造 AI Agent 應用藍圖 | 🟡 | 3,200 | 🟡 部分 |
| 黃琇琳 | 天下學習 | AI Agent 零基礎個人工作流 | 🟡 | ~3,000 | 🟡 |
| 新商業學校 | biz-online | 激增十倍工作效率的 AI 工作流 | 🟡 | 3,000-5,000 | ❌ |
| 燒賣研究所 | 自架 | 商業 Prompt 優化班 / n8n 電商自動化 | 🟡 | 4,000-8,000 | ❌ |
| TBR.Digital | 自架 | n8n / Make 場景 | 🟡 | ~5,000+ | ❌ |
| HiSKIO | 自架 | n8n + AI Agent + MCP 實戰 | 🟡 | ~3,000-5,100 | 🟡 |
| 大人提（Value Chain）| 自架 | AI Agent 一日開發實戰營 | 🟡 | 6,000（4hr）| ❌ |
| 恆逸 | 自架 | 零程式碼 AI Agent Dify/n8n | 🟡 | 24,000（14hr）| 🟡 |
| Hahow（多講師）| Hahow | ChatGPT 升級工作流 | 🔵 | 1,500-3,000 | ❌ |
| PressPlay Academy | PressPlay | 1000 個 ChatGPT 指令 / 行銷 AI | 🔵 | 1,500-3,000 | ❌ |
| 商周 CEO 學院 | 商周 | CEO 經營策略含 AI 模組 | 🟡 | 數十萬 / 年 | ❌ |
| 商周學院 | 商周 | AI 新領導力論壇 | 🟡 | 5,000-20,000 | ❌ |
| 經理人月刊 | managertoday | 未來經理人年會 | 🟡 | ~5,000+ | ❌ |
| 天下學習（其他）| cwlearning | AI 素養認證 / Agent 系列 | 🟡 | 1,500-5,000 | 🟡 |
| 台灣人工智慧學校 AIA | 自架 | LLM 中階班（14hr）| 🟡 | 15,000（13,500 校友/團報）| 🟡（含 Agentic Workflow 3hr）|
| 台灣人工智慧學校 AIA | 自架 | LLM 高階班（30hr 4 週）| 🟡 | 40,000（32,000 校友）| 🟡（LangChain Agent + Memory）|
| 台灣人工智慧學校 AIA | 自架 | 經理人 / 技術領袖 cohort | 🟡 | 48,000 | ❌（非 multi-agent 專班）|
| airabbi 瑞比智慧 | 自架 | 企業主必修 AI 經營管理學 | 🟡 | 客製 | ❌（老闆視角 ✅ 但偏報表 / 流程）|
| 永旭顧問 | 自架 | 中小企業 AI 賦能 | 🟡 | 客製 | ❌ |
| 田中系統（GWS）| 自架 | 企業 AI 半天內訓 | 🟡 | 2.5 萬-6 萬 / 班 | ❌ |
| 鄭緯筌 Vista | 自架 / 講座 | 行銷 AI / Prompt 入門 | 🔵 | 1,000-3,000 | ❌ |
| 林長揚 | 自架 | 簡報 + AI | 🔵 | 5,000+ | ❌ |
| 邱奕霖 | 自架 | 圖像思考 + AI | 🔵 | 5,000+ | ❌ |
| 葛如鈞 | 偶爾講座 | AI 趨勢演講 | 🔵 | 不公開 | ❌ |
| BCG / 麥肯錫台灣 | 顧問 | AI 轉型導入 | 🟡 | 數百萬起 | 🟡（客製 GPT 工廠）|
| 資策會 | 自架 | 各類 Agent 補助班 | 🟡 | 政府補助多 | 🟡 |
| 黃敬峰（AI 峰哥）| 自架 | 企業 AI 內訓 | 🟡 | 客製 | ❌ |
| Build School | 自架 | AI Agent Bootcamp | 🟡 | 2,800（7.5hr）| ❌（未明寫 multi-agent）|

### C3. 沒查到具體公開班 multi-agent 報價的玩家（標 ❓）

- 工研院產業學院《AI Agent 流程自動化實作》— 線上洽詢
- 工研院《AI Agent 驅動服務業智慧轉型實戰班》— 經濟部補助合格者全免
- TibaMe 緯育 — 一般實作課 10,000-20,000，多走政府補助
- AppWorks Aiworks — 走企業培訓 / RPA 為主
- AICEAN / Skiclex — 無台灣公開班報價資訊

---

<a id="d"></a>
## D. 標竿競品深挖（5 家）

### D1. 天地人學堂（台灣最直接的核心競品）

#### D1-a. c1534《多代理人工具與工作流程開發實作課》

| 項目 | 內容 |
|------|------|
| 講師 | 張書豪（數位科技課程研發業師） |
| 形式 | 線上影音 3hr / 14 天觀看權 |
| 定價 | NT$3,890（原 7,200）|
| 技術棧 | **AutoGen 框架**（Microsoft Python multi-agent framework） |
| 三大主軸 | ① 基礎定義 + 應用場景 ② AutoGen 框架實作多代理 ③ 未來趨勢 |
| 學員定位 | 「AI 初學者、開發者、智慧決策 / 自動化技術專業人士」 |

→ **本質「3 小時線上自學包」**，價格錨點是「試水溫」不是「帶回家用」。

#### D1-b. c1589《AI Agent 實戰應用工作坊》

| 項目 | 內容 |
|------|------|
| 講師 | 楊傑年（泛亞數位科技執行長，輔導 100+ 家企業數位轉型）|
| 形式 | **實體 1 天 6 小時**（IEAT 會議中心，台北中山） |
| 定價 | 兩方案 — NT$3,880（基礎）/ NT$10,000（進階，限量名額） |
| 核心動線 | 基礎概念 → AI Agent 原理 → 整合企業流程 → 自動化串接 → 部署優化 |
| 學員定位 | 想把 AI 導入企業流程的人（偏 IT 主管 / 顧問） |

→ **這才是天地人對外的主推門面**，但定價 10,000 才是真實「全套帶回去」價位。

#### D1-c. 平台定位

- **本質**：跨界教育百貨（年 600+ 堂課）— AI 只是 1/10
- **講師制**：業師制（外聘總經理 / 總監 / 律師 / 會計師）— **流動性高**
- **規模**：服務 1000+ 公司企業培訓
- **AI 不是護城河，是流量入口**

#### D1-d. vs 智谷 9 維對位

| 維度 | 天地人 | 智谷 |
|------|--------|------|
| 平台性質 | 跨界教育百貨 | 專精企業 AI 訓練 |
| 品牌年資 | 不確定 | **26 年 / 3000+ 客戶 / 30,000+ 學員** |
| 講師制 | 業師外聘（流動） | Jimmy 主帶 + 400+ 夥伴（穩定） |
| **教 agent 的方式** | **AutoGen Python 框架** | **C-suite 6 幕僚 × 卡牌指揮** |
| 學員定位 | 開發者 / AI 初學者 / IT 主管 | 老闆 / 中高主管 / 中小企業主 |
| 形式 | 3hr 線上 or 6hr 單日實體 | 半天 / 全天 / 多日 cohort + 卡牌組 |
| 定價區間 | 3,880-10,000 NTD | 預計 15,000-25,000 NTD |
| 學員產出 | 跑得起 AutoGen demo（電腦上）| 帶走 6 個 agent + 一組卡牌 |
| Agent team 敘事 | 技術框架 | 「複製一個部門」（口語） |

### D2. AI Tinkerers' Cards（英文圈卡牌最強競品）

| 項目 | 內容 |
|------|------|
| 設計者 | Alex Eisenchteter（Stormz 創辦人）— 20 年工作坊資歷 |
| 規模 | Starter Kit 24 張 €1 / Base Deck (Modern AI Assistants) 37 張 €49 / Prompt Engineering Expansion 20 張 €49 |
| 形式 | SVG / 高解析度 PDF / 列印友善 + Miro 模板 + Custom GPT |
| 卡牌結構 | LLM board / Input / Output / **Capability cards** / Term cards / **DREAMS cards**（腦力激盪）|
| 學員定位 | 「非技術團隊」(non-tech teams) — 通用培訓師 / facilitator |
| 主題 | **GenAI 入門 + Prompt 工程**（**不是 agent team**） |
| 社群 | AI Trainers' Guild + AI Tinkerers' Club 兩個社群 |
| 語言 | 英文 |
| 教學資源 | step-by-step instructions / timing / group sizes / variations |

**對智谷的啟發**：
- ✅ €1 → €49 的「**引流款 + 旗艦款**」分層策略可借鏡
- ✅ 「SVG + 高解析度 PDF + Miro 模板」**多載體分發**可借鏡（智谷可做：實體卡 + Miro 模板 + 印刷 PDF）
- ✅ 「**培訓師為培訓師而設計**」的社群打法可借鏡（智谷可建「企業 AI 教練 club」）
- ❌ 沒擴展到 agent team → **智谷的縫隙**

### D3. DigitalApplied AI Virtual Team Playbook（英文圈 agent team 最強競品）

| 項目 | 內容 |
|------|------|
| 形式 | **純文字 blog playbook**（無實體卡牌）|
| 規模 | **10 specialist agents** |
| 角色 | Research Analyst / Content Writer / Data Analyst / Creative Director / Financial Assistant / Support Specialist / Sales Rep / Operations Coordinator / QA Editor / Social Media Strategist |
| 提供物 | role cards（文字模板）+ system prompts + task delegation matrix + orchestration workflow + quality gates + performance scorecard |
| 學員定位 | **non-technical founders / solo operators**（**跟智谷一模一樣**） |
| 定價 | **免費 blog**（背後賣 AI Digital Transformation Services）|
| 平台 | Claude Opus 4.6 / GPT-5.2 / Gemini 3.1 Pro 三模型並存 |

**對智谷的差異化**：
- 智谷打 **C-suite 6 角色（CEO/CMO/CFO/CSO/CPO/特助）**，他們打 **10 個營運角色**（內容 / 資料 / 業務 / 客服等）→ **智谷敘事更高階**（戰略決策層）
- 他們純文字模板 → **智谷實體卡牌 = 體感記憶 + 中年主管不怕**
- 他們免費 + 後端賣顧問 → **智谷收公開班學費 + 後端內訓**（兩種獲利模式都成立）

### D4. airabbi 瑞比智慧（台灣老闆視角最像但偏報表）

- 課程：《企業主必修 AI 經營管理學》
- 形式：內訓 + 顧問（客製定價）
- 學員定位：**老闆視角 ✅** 但偏報表 / 流程數據
- 對智谷站位：「**不是給你儀表板，是給你部屬**」

### D5. 商周 CEO 學院（頂級老闆社群但不教動手）

- 形式：實體 cohort（半年制）/ 年費數十萬
- 學員定位：頂級老闆 / 圈子 + 方向感
- 弱點：**動嘴不動手**
- 對智谷站位：「**不只給你方向感，給你回家就能複製的 6 個分身**」

---

<a id="e"></a>
## E. 台灣 multi-agent 公開課定價 survey

### E1. 聚焦表 — 13 家真在教 multi-agent 的台灣公開班（依定價低到高）

| # | 單位 | 課程 | 時數 | 形式 | 定價 NTD | 學員定位 | 真在教 agent team? |
|---|------|------|------|------|---------|---------|---------------------|
| 1 | 天地人文創 | AI Agent 多代理人實作課 c1534 | 3hr | 線上影音（14 天）| **3,890**（原 7,200）| 初學/開發者 | ✅ AutoGen 多代理協作 |
| 2 | 天下學習 | 打造 AI Agent 應用藍圖（黃琇琳）| 線上 | 線上影音 | **3,200** | 通用上班族 | 🟡 部分（未深入 multi-agent）|
| 3 | 天地人文創 | AI Agent 實戰應用工作坊 c1589 | 6hr | 實體一日（台北 IEAT）| **3,880**（原 7,200）| 通用 | ✅ AutoGen 多代理協作 |
| 4 | 台大資訊系統訓練班 | AI Agent 開發與多智能體實作 | 12hr | 實體兩日 | **4,500** | 技術背景 | ✅ 明寫多智能體 |
| 5 | 大人提（Value Chain）| AI Agent 一日開發實戰營 | 4hr | 實體半日 | **6,000** | 中小企業主 / 行政 | ❌ 單 agent |
| 6 | CPC 中國生產力中心 | AI Agent 地端實戰 TC7499 | 12hr | 實體兩日（台北）| **8,550-9,000** | IT / 應用設計師 | 🟡 含 A2A + MCP，偏單 agent 多應用 |
| 7 | iSpan 資展國際 AIA | Agentic AI 與企業 workflow 自動化基礎架構 | 21hr | 實體三日（北桃中高）| **12,000**（早鳥）/ 15,000 | IT / PM | ✅ agent orchestration |
| 8 | AIA 台灣人工智慧學校 | 大型語言模型實作中階班 | 14hr | 實體兩日 | **15,000**（13,500 校友 / 團報）| 技術中階 | ✅ Agentic Workflow 3hr 實作 |
| 9 | iSpan 資展國際 AIB | Agentic AI Framework 與 LLM 應用安全 | 21hr | 實體三日（台北）| **16,800**（早鳥）/ 21,000 | 技術中高 | ✅ multi-agent framework |
| 10 | iSpan 資展國際 AIAGENT | AI Multi-Agent 實戰班 | 21hr | 實體（北桃中高）| ❓ ~16,800-21,000（同級估）| 技術中高 | ✅ LangGraph 多角色（研究員 / 規劃師 / 執行者）|
| 11 | 恆逸 | 零程式碼 AI Agent Dify / n8n | 14hr | 實體（北竹中高）| **24,000** | 通用無程式 | 🟡 多 Agent 串接 |
| 12 | AIA 台灣人工智慧學校 | 大型語言模型實作高階班 | 30hr（4 週）| 實體 | **40,000**（32,000 校友 / 團報）| 技術高階 | 🟡 LangChain Agent + Memory，非 multi-agent focus |
| 13 | AIA 台灣人工智慧學校 | 經理人周末研修 / 技術領袖 cohort | 數週 | 實體 cohort | **48,000** | 主管 / 技術領袖 | ❌ 非 multi-agent 專班 |

### E2. 定價區間分布

| 帶 | 區間 NTD | 玩家數 | 形態 |
|---|---------|------|------|
| 線上影音 | 3,000 以下 | 3 | 試水溫 |
| 半日 / 單日入門 | 3,000-10,000 | 5 | **最擁擠** — 12-14hr 兩日為主 |
| **中高（multi-agent 主流）** | **12,000-24,000** | **4** | 14-21hr / 技術背景 |
| 超高 / cohort | 30,000+ | 3 | AIA cohort 名校品牌 |

### E3. 三個關鍵發現

1. **「全天 6-8h multi-agent 專班」是市場空缺** — 半日（6,000）與兩日（8,550+）中間沒人做
2. **NT$15,000+ 的 multi-agent 課，學員 100% 是技術背景** → 智谷打「非技術主管 + 15,000+」是真空地帶
3. **AIA 是價格錨點不是學員對手** — 智谷借錨點 / 搶他們搶不到的非技術主管

---

<a id="f"></a>
## F. 教學法借鏡（非競品但機制可移植）

### F1. Magic: The Gathering 入門卡牌教學法

- 來源：[Oreate AI Blog](https://www.oreateai.com/blog/practical-insights-and-reflections-on-offline-magic-the-gathering-beginner-teaching-activities-an-immersive-card-game-introduction-experience/4e8b61a043b6fa3bc6246ce0aa9e4d28)（410 Gone，僅留摘要）
- 機制：**沉浸式 immersive** — 先玩起來邊玩邊教規則，不是看規則書
- 借鏡：分層揭露規則（第一輪只 3 卡 → 第二輪加限制 → 第三輪完整）

### F2. AI Agents 教學模擬（arxiv 2407.12796）

- 機制：直接教學 + 教練 + 模擬練習 + 回饋四步循環
- 借鏡：智谷卡牌 = 離線版 simulated practice

### F3. 卡牌桌面練習 × 混合教學（臨床醫療 NCT07189611）

- 機制：**case 庫 + 卡牌 + 場景模擬**三件套
- 借鏡：智谷已對應 — 任務卡（case）+ 能力 / 資料 / 產出 / 心法（卡牌）+ 互評（場景）

---

<a id="g"></a>
## G. 智谷戰略結論

### G1. 護城河四點

1. **C-suite 6 角色具象化**（CEO/CMO/CFO/CSO/CPO/特助）→ 老闆秒懂
2. **桌面卡牌實體** → 體感記憶 + 中年主管不怕（不需打字示範）
3. **自然語言主導**（Claude Code 而非 n8n / Dify / AutoGen）→ 老闆能自己改
4. **中文 B2B 教學 26 年品牌** → 比 KOL 個人課可信

### G2. 三句反差敘事（行銷可直用）

- **vs 天地人**：「不是給你框架，是給你**部門**」
- **vs airabbi**：「不是給你儀表板，是給你**部屬**」
- **vs 商周 CEO 學院**：「不只給你方向感，給你**回家就能複製的 6 個分身**」

### G3. 定價戰略三檔（對應 v0.8 量級拍板）

| v0.8 方案 | 卡牌規模 | 時數 | 建議定價 | 對標 | 差異化 |
|---------|---------|------|---------|------|----------|
| **B 骨架** | 30 張 | 4hr 半天 | **NT$6,800-7,800** | 大人提 6,000 / 天地人 3,880 | 「多 6 個角色 + 帶卡牌回家」 |
| **A 完整（旗艦）** | 108 張 | 6-8hr 全天 | **NT$16,800-18,800** ⭐ | iSpan 12-15k / AIA 中階 15k | 「全部門 virtual team + 課後支援 + 卡牌」**市場甜蜜空缺** |
| **A 旗艦 cohort** | 108 張 | 2 天 cohort | **NT$32,000-38,000** | AIA 校友 32k / 高階 40k | 「做出自己的 C-suite + 同梯社群 + Jimmy office hour」|

### G4. 一句話戰略

**主推 A 全天版 NT$18,000** — 台灣 multi-agent 公開班的「市場空缺」：有人在這價位，但**沒人用「卡牌 × 部門級 virtual team × 非技術主管」這三角組合**。

- 半天版做引流（讓對方體驗卡牌）
- 2 天 cohort 做毛利

### G5. 不能做的（避雷）

- ❌ 不要定 8,000-10,000：被 CPC / 台大 / 天地人錨在「兩日才這個價」
- ❌ 不要定 12,000：跟 iSpan 21h 撞，時數比輸
- ❌ 不要走 AutoGen / LangGraph 路線：等於放棄非技術主管市場
- ❌ 不要主打官方證書：B2B 不買單，這條路 Anthropic Skilljar 已經佔了
- ❌ 不要打 BCG / 麥肯錫的 CXO 客戶：不是同檔次，會被笑

### G6. 量級拍板對應市場（給 v0.8）

| 方案 | 卡牌 | 對應市場 | 建議定價 |
|------|------|--------|---------|
| B（30 張 / 4hr）| 骨架 | 半天引流 | 6,800-7,800 |
| C（61 張 / 4hr）| MVP | 半天升級或全天簡版 | 8,800-12,800 |
| A（108 張 / 8-12hr）| 完整 | 全天旗艦 / 2 天 cohort | 16,800-18,800（全天）/ 32,000-38,000（2 天） |

---

## 📅 更動紀錄

### 2026-05-19
- **建檔**：整合自 5/14 啟動以來所有競品研究
- 來源：
  - instruction-design.md E 區（30 家中文市場掃描）
  - 5/19 英文圈搜尋（9 家 Claude Code 玩家 + AI Tinkerers' Cards + DigitalApplied）
  - 5/19 天地人深挖（c1534 + c1589 + 平台定位 9 維對位）
  - 5/19 台灣 multi-agent 公開課定價 survey（13 家聚焦表）
  - 5/19 全球 agent team × 卡牌交集分析（結論：全球零交集，智谷護城河成立）
- **下一步**：建議精簡 instruction-design.md E 區為一行 pointer 指向本檔，避免雙處維護 drift
