# Claude Code 教學設計收集庫

> **建立日期**：2026-05-19
> **主責**：教學設計師
> **目的**：
> 1. 蒐集市面上現有的 Claude Code「趣味教學法」/ 工作坊 / 體驗式教學設計，作為智谷卡牌玩法的借鏡與差異化參照
> 2. 隨專案推進，**收納所有專案 md 內出現的「教學設計片段」**（任何提到玩法、引導、學員體驗、講師動作、互動機制的段落）統一沉澱到這裡
> **使用**：本檔不是 LOG，是**設計參考庫**。卡牌玩法 SOP / 講師手冊 / 工作坊腳本動工時，從這裡找彈藥。

---

## 📑 目錄

- [A. 市面現有的 Claude Code 教學法盤點（含趣味化）](#a)
- [B. 教學法借鏡（非 Claude Code 本體，但機制可移植）](#b)
- [C. 對智谷卡牌的設計啟發（差異化 vs 可借鏡）](#c)
- [D. 從專案 md 收進來的教學設計片段（持續累積）](#d)
- E. 競品 / 市場 / 定價 → 已搬至獨立檔 [`competitor.md`](competitor.md)

---

<a id="a"></a>
## A. 市面現有的 Claude Code 教學法盤點（含趣味化）

> 2026-05-19 第一波 sweep。後續看到新案例就追加。

### A1. Claude Quest — 純遊戲化外掛層（最直接對應「趣味教學法」）

**來源**：[GitHub SeanZoR/claude-quest](https://github.com/SeanZoR/claude-quest)

**核心設計哲學**：「**正常使用 Claude Code，遊戲自己進行**」—— 零額外指令，背景監測使用行為自動解鎖成就，避免學習負擔。

**結構**：
- **90 個成就** × 8 大類：記憶守護者（CLAUDE.md）/ 命令工匠（slash）/ 技能編織者（Skills）/ 鉤子大師（Hooks）/ 整合者（MCP）/ 工具使用者（內建 tools）/ 工作流精靈 / 冠軍（meta 成就）
- **4 階段漸進**：新手 L1-4（50 XP）→ 學徒 L5-9（100 XP）→ 專家 L10-14 → 冠軍 L15+（500 XP）
- **ASCII Dashboard** 四層回饋：進度條 / 統計 / 近期解鎖 / 下一目標
- **任務模式**：`/quest learn N` 提供逐步教學

**對智谷卡牌的啟發**：
- ✅ **8 大類分類法** 跟我們 v0.5 五類（任務 / 能力 / 資料 / 產出 / 心法）邏輯接近，但他們更偏「Claude Code 元件清單」，我們偏「老闆視角任務」 → **差異化清楚**
- ✅ **背景監測自動解鎖** = 學員零學習壓力 → 智谷卡牌玩法可借鏡：**「不需要記規則」是趣味化的核心**
- ⚠️ **單人線上模式** → 智谷是團班桌面互動，玩法形態完全不同（這是我們的差異化）
- ⚠️ Claude Quest 服務「想系統化探索功能」的中初學員 → **不是老闆 / 主管的視角**

### A2. CC for Everyone（ccforeveryone.com）— 沉浸式做中學

**來源**：[ccforeveryone.com](https://ccforeveryone.com/)

**核心哲學**：**「Learn Claude Code IN Claude Code」** — no videos, no docs, no coding experience required. 只要會對話就能用。

**學習機制**：
1. 安裝 Claude Code（15 min）
2. 下載課程素材
3. 在 Claude Code 內輸入 `/start-1-1` → **Claude 自己引導互動式課程**

**模組設計**：
- 模組 1（3 hr）：檔案操作 / 視覺工作區 / 平行代理 / 自訂 subagent / 專案記憶 / 快捷指令
- 模組 2（1-2 hr）Vibe Coding：需求規劃 → 建構 → 版控 → 部署上線

**趣味元素**：
- **角色扮演**：Custom Sub-agents 創造「擁有不同觀點的 AI 顧問」
- **真實成果**：學員能實際部署到 Vercel 拿到真實 URL（即時成就感）
- **視覺反饋**：分割螢幕工作流 → 即時看到改變
- **敘事化**：「Vibe Coding」概念化成「你描述、Claude 建」的對話體驗

**對智谷卡牌的啟發**：
- ✅ **「if you can have a conversation, you can use Claude Code」** 跟 Jimmy「討厭 slash、要人話」直接對齊 → 卡牌背面範本要做到這個感覺
- ✅ **真實 URL = 即時成就感** → 工作坊終點如果能讓學員「離開時帶走一個真的會跑的 agent」，學習動機飆升
- ⚠️ 該課用 slash command 引導 → 跟 Jimmy 偏好衝突，但**「Claude 引導學員」的元設計可借鏡**：卡牌背面範本可以做成「跟 Claude 對話的開場句」

### A3. Anthropic 官方 Code with Claude 系列 — 三城市開發者大會

**來源**：[Code with Claude — Anthropic Developer Conference](https://claude.com/code-with-claude) / [London May 19](https://claude.com/code-with-claude/london) / [SF Extended May 7](https://claude.com/code-with-claude/san-francisco-extended)

**形式**：一天的 hands-on workshops + live demos + 開發團隊對談（SF / London / Tokyo 三城）

**借鏡點**：
- **Live Demo + Workshop** 並進是業界主流，純講師單向講課已被淘汰
- 「跟開發團隊對談」是價格錨點（無法被線上錄影課取代）→ 智谷對應的差異化 = **「Jimmy 的實戰系統」**（一人公司 6 個 C-level 幕僚）

### A4. Frontend Masters: Claude Code Deep Dive（Lydia Hallie）

**來源**：[Frontend Masters Workshop](https://frontendmasters.com/workshops/advanced-claude-code/) / [blog](https://frontendmasters.com/blog/free-claude-workshop/)

**主題**：harness vs model 心智模型 → CLAUDE.md → plan mode → permissions → Skills → 從零寫 MCP server

**借鏡點**：
- **「mental model first」是進階教學的金線**：先建心智模型，再展開工具
- 智谷對應 = 「老闆視角的 C-suite 心智模型」（你已經會帶部門，現在帶 agent 部門）

> ⚠️ 該頁僅推廣文，未披露具體教學動作細節，需要錄影釋出後再回填。

### A5. Code with Antonio: Build Your Own Claude Code（cohort）

**來源**：[Build Your Own Claude Code](https://www.codewithantonio.com/cohorts/build-your-own-claude-code-2026-05)

**形式**：6 天 cohort + Discord + 辦公時間，學員「從零做出 Claude Code CLI 本體」（逆向工程法）

**借鏡點**：
- **逆向工程法**（從零做一遍 = 真懂）對工程師有效，但**對老闆無效**（老闆不會寫 CLI）
- 智谷對應 = 「**從零做一個自己**」（個人分身）+「從零做一個部門」（6 個幕僚）→ 老闆視角的逆向工程

### A6. KDnuggets: 5 Fun Projects — 趣味專案清單

**來源**：[5 Fun Projects Using Claude Code](https://www.kdnuggets.com/5-fun-projects-using-claude-code)

| # | 專案 | 趣味點 | 程度 | 教到的 Claude Code 能力 |
|---|------|--------|------|----------------------|
| 1 | 第一個 web app | 一個 idea → 可用程式 | 入門 | App prototyping |
| 2 | Retro 2D 太空射擊遊戲 | 即時看到結果、改 prompt 調難度 | 入門-中級 | 互動前端 + 遊戲機制 |
| 3 | React Native + Expo 行動 App | 比靜態網頁更吸睛、裝置上即時回饋 | 中級 | Mobile prototyping |
| 4 | Full-stack（DB + Auth + 部署） | 跨層 debug 真實感 | 進階 | Production-level |
| 5 | 自製 MCP Server | **不是寫 app，是擴展 Claude Code 本身** | 進階 | Custom tool / agent 能力 |

**對智谷卡牌的啟發**：
- 5 個全是「coding 性質」，**老闆 / 主管 0 個能跑** → 智谷的差異化 = 5 個「老闆能跑的 fun projects」（建分身 / 做週報 hook / 提案語氣 review / 跨主管協調 / 客戶 LINE 仿寫）
- 「即時看到結果」是趣味化關鍵 → 卡牌玩法的「翻牌看背面 = 自然語言指令」就是即時回饋

### A7. claude.nagdy.me — 瀏覽器 terminal 模擬器（11 堂課）

**來源**：透過 [動區動趨報導](https://www.blocktempo.com/learn-claude-code-interactive-browser-terminal-simulator-free-no-install/) 提到

**設計亮點**：**免安裝、免 API key、瀏覽器內模擬 terminal** → 完全沒有上機門檻

**對智谷卡牌的啟發**：
- 跟 Jimmy「上機前 12 條挑戰，卡牌處理掉 10 條」直接對齊 → **「降低上機門檻」是業界共通方向**
- 但他們的解法是「模擬器」，智谷的解法是「**桌面卡牌離線推演**」 → **比模擬器更低門檻**（連螢幕都不用）

### A8. Anthropic Skilljar: Claude Code in Action + 13 堂免費官方課

**來源**：[Anthropic Skilljar](https://anthropic.skilljar.com/claude-code-in-action) / 2026/3/6 推出 13 堂課含官方證書（涵蓋 Agent Skills + Claude Code 實作）

**借鏡點**：**官方證書**是 B2C 端的學習動機 → 智谷 B2B 不打這條路（智谷的學習動機 = 「主管帶 AI 部門」的競爭力）

### A9. Coursera: Claude Code — Software Engineering with Generative AI Agents

**來源**：[Coursera](https://www.coursera.org/learn/claude-code)

**形式**：學術線上課 → 完全偏工程師 → 跟智谷無重疊

---

<a id="b"></a>
## B. 教學法借鏡（非 Claude Code 本體，但機制可移植）

### B1. Magic: The Gathering 入門卡牌教學法（沉浸式體驗）

**來源**：[Oreate AI Blog](https://www.oreateai.com/blog/practical-insights-and-reflections-on-offline-magic-the-gathering-beginner-teaching-activities-an-immersive-card-game-introduction-experience/4e8b61a043b6fa3bc6246ce0aa9e4d28)（連結 410 Gone，僅留搜尋摘要）

**摘要可知方向**：**沉浸式（Immersive）卡牌入門教學**，不是看規則書，是先玩起來，邊玩邊教規則。

**對智谷卡牌的啟發**（待補實際內容）：
- 卡牌教學的核心：**不要讓學員先讀規則書**
- 講師當 DM（地下城主），先給簡化版玩起來，5 分鐘有第一輪「啊哈」
- 規則複雜度應分層揭露（第一輪只用核心 3 卡，第二輪加入限制條件）

### B2. AI Agents 教學模擬（Simulated Practice at Scale, arxiv 2024）

**來源**：[arxiv 2407.12796](https://arxiv.org/pdf/2407.12796)

**核心機制**：用 AI agent 模擬學員互動對象 → 大量練習 + 直接教學 + 教練 + 模擬 + 回饋四步循環

**對智谷卡牌的啟發**：
- 智谷卡牌 = **離線版的「Simulated Practice」**：上機前用桌面卡牌模擬 agent 行為，避免直接在線上摸索浪費 token + 心智負擔
- 「直接教學 → 模擬練習 → 回饋」的三步可作為**講師動作骨架**

### B3. 卡牌桌面練習 × 混合教學（臨床醫療領域，NCT07189611）

**來源**：[ClinicalTrials NCT07189611](https://clinicaltrials.gov/study/NCT07189611)

**機制**：GAI 優化的臨床案例庫 + 虛擬模擬平台 + **卡牌桌面練習** + 場景模擬

**對智谷卡牌的啟發**：
- 「**case 庫 + 卡牌 + 場景模擬**」三件套是醫療臨床教學驗證過的組合
- 智谷對應 = 任務卡（case 庫）+ 能力 / 資料 / 產出 / 心法（卡牌）+ 互評（場景模擬）

---

<a id="c"></a>
## C. 對智谷卡牌的設計啟發（差異化 vs 可借鏡）

### C1. 差異化護城河（不要做別人做的）

| 別人在做 | 智谷不做 | 智谷做什麼 |
|--------|--------|---------|
| Claude Quest 90 成就 / 8 大類 | ❌ 線上單人遊戲化 | ✅ 桌面團班互評 |
| CC for Everyone slash 引導 | ❌ slash 主導 | ✅ 自然語言主導（卡牌背面範本） |
| Frontend Masters mental model（harness vs model） | ❌ 工程師心智模型 | ✅ 老闆心智模型（C-suite + 部門） |
| Antonio Build Your Own CLI | ❌ 從零做 CLI | ✅ 從零做一個自己 / 一個部門 |
| KDnuggets 5 fun projects（全 coding） | ❌ coding projects | ✅ 老闆能跑的 5 個（建分身 / 週報 hook 等） |
| nagdy.me 瀏覽器模擬器 | ❌ 線上模擬 | ✅ 桌面實體卡牌（更低門檻） |

### C2. 可借鏡的趣味化機制（要做的）

1. **「不需要記規則」是趣味化的核心**（Claude Quest 啟發）→ 卡牌的玩法 SOP 要做到「玩 1 局自然會」
2. **即時成就感**（CC for Everyone Vercel URL 啟發）→ 工作坊終點讓學員帶走一個「真的會跑的卡牌組合」
3. **「跟 Claude 對話的開場句」當卡牌背面範本**（CC for Everyone 啟發）→ 翻牌 = 學會講第一句話
4. **分層揭露規則**（MTG 啟發）→ 第一輪只玩任務 + 能力（2 類），第二輪加資料 + 產出（4 類），第三輪加心法（5 類完整）
5. **case 庫 + 卡牌 + 場景模擬三件套**（醫療臨床啟發）→ 智谷已有對應結構，只需確認三件套都有
6. **mental model first**（Frontend Masters 啟發）→ 開場 5 分鐘必教翻譯層（CLAUDE.md = 職務說明書，subagent = 派同仁⋯）才開始抽牌

### C3. 我們的「啊哈」時刻設計（要刻意打造的學員情緒高峰）

借鏡 Claude Quest 的「自動解鎖成就」、CC for Everyone 的「真實 URL」、KDnuggets 的「即時看結果」，智谷卡牌的「啊哈」時刻候選：

| 時刻 | 卡牌玩法對應 | 學員感受 |
|------|------------|--------|
| 翻牌看背面 | 正面物理推演 → 背面自然語言指令 | 「原來這就叫『派同仁』」 |
| 互評組合「少什麼」 | 同組找出對方缺資料卡 / 缺心法卡 | 「啊我忘了給它脈絡」 |
| 任務卡 vs ChatGPT 弱項 | 對照「ChatGPT 做不來的理由」 | 「原來這種事才用 Claude Code」 |
| 終場展示組合 | 把組合念出來「總工程師，請幫我⋯」 | 「我會用人話下指令了」 |

---

<a id="d"></a>
## D. 從專案 md 收進來的教學設計片段（持續累積）

> 待 Jimmy 投放 / 我從各 md 收進來。預留結構如下，每筆收進來時加日期 + 來源檔案 + 原文摘錄 + 適用情境。

### 📥 收納格式範本

```
### [YYYY-MM-DD] [來源 md 檔名] [一句話主題]

**原文段落**：
> ⋯（從來源 md 引用）⋯

**教學設計性質**：
（玩法 / 引導 / 講師動作 / 學員體驗 / 互評機制 / 引導問句 / ⋯）

**可套用情境**：
（卡牌哪一輪？哪段時序？哪類學員？）

---
```

### [2026-05-19] 對話內提出 — KPI for Agent（老闆/主管最愛的 hook）

**原始 idea（Jimmy 對話內）**：
> 「我突然想到有一個東西很重要，幫 agent 設定 KPI」
> 「這是老闆們喜歡的或者部門主管喜歡的」

**教學設計性質**：
- **雙落地點機制**：
  1. **養成 Canvas 必填項** — agent 設定時填 3-5 個 KPI（屬 Canvas，非卡牌）
  2. **任務卡背面標 KPI 對應** — 跑完任務知道動了哪個主管的哪個 KPI
- **老闆語言 hook**：KPI 是老闆 / 主管母語，不是工程師詞
- **跨 session 累積 ROI 證據**：寫進 WORKING_MEMORY → 3 個月後可看「請了這 AI 團隊有差嗎」
- **升級為課程第二大賣點**：
  - 賣點 1：「指揮虛擬團隊」
  - 賣點 2：**「用 KPI 追蹤 AI 團隊的價值」**

**可套用情境**：
- **卡牌哪一輪**：第三輪揭露之後（進階階段才出現，避免一開始嚇到學員）
- **哪段時序**：(1) 養成 Canvas 填空階段 (2) 每張任務卡背面對應
- **哪類學員**：老闆 / 中高階主管（製造業 50+ 主管尤其有感；純工程師興趣低）

**具體 KPI 範例**（給講師手冊 / Canvas 範本用）：

| 角色 | KPI 範例 |
|------|---------|
| 產品主管 | 新課提案週期 / 定價準確度（實際 vs 預估） |
| 行銷主管 | content / 週 / CTR / SEO 排名 |
| 銷售主管 | 提案勝率 / follow-up 響應率 |
| 財務主管 | 報價準確率（實際成本 vs 預估） |
| 策略幕僚 | 決策落地率 |
| 特別助理 | 跨主管協作效率 / 會議紀錄完成度 |
| 總工程師 | agent 上線時間 / 鐵律一致性稽核率 |

**差異化敘事**（給開場 5 分 / 文宣 / 招生頁用）：
> 「上完課你會知道**怎麼幫虛擬團設 KPI**，並用 Claude Code **跨 session 持久追蹤** — ChatGPT 用完丟，沒法持久 KPI 比較。」

**為什麼這個 idea 是 ROI 證據**（給老闆級行銷用）：
- 學員回家可以跟老闆 / 同事解釋：「我裝了這套 AI 團隊，過去 3 個月 KPI 達成率 X%」
- 直接回應老闆級 hidden question：「請了這團隊有差嗎？」

---

### [2026-05-19] 外部素材 — DigitalApplied AI Virtual Team Playbook（最完整 agent team 教學框架）

**原始來源**：[DigitalApplied — AI Virtual Team Specialist Agent Squad Playbook](https://www.digitalapplied.com/blog/ai-virtual-team-specialist-agent-squad-playbook)

**Jimmy 評**：「我覺得這篇講得很好」

**為什麼這篇是金礦**：英文圈唯一「**non-technical founders × 10 agents × 完整教學框架**」的免費素材，學員定位跟智谷一模一樣，但他們是純文字 blog，智谷可以「**抽精華 + 用卡牌實體化**」。

---

#### 🎯 抽出的 7 個教學設計核心點（按對 v0.8 戰術價值排序）

##### #1 Task Delegation Matrix（三軸評分法）— 直接進任務卡背面

**原文設計**：每個任務用三軸評分（各 1-5 分）：
- **Frequency**（月→日 = 1→5）
- **Time Cost**（<15min → 2hr+ = 1→5）
- **AI Suitability**（差→極佳 = 1→5）
- 三軸相加 ≥ 12 = 「應該派 agent 做」；≤ 8 = 「保留人做」

**智谷怎麼用**：
- **任務卡背面**新增一欄「該不該派 agent」三軸圖示（頻率 / 耗時 / AI 適配度）
- 學員拿到任務卡時自評三軸 → 訓練老闆「哪些事才該丟給 agent」直覺
- 對應 v0.8：**任務卡 10 張的卡背標準欄位**

##### #2 Role Card 五欄結構 — 直接成為角色卡規格

**原文設計**：每張 role card 含：
```
Title / Responsibilities / Tools / Success Metrics / Best For
```
+ 隱含的「邊界」欄（如 Researcher「不做內容製作」、Writer「不做事實查證」）

**智谷怎麼用**：
- **v0.8 角色卡 7 張**直接套這 6 欄結構（Title / 職責 / 配備 / KPI / 適用場景 / **不做的事**）
- 「不做的事」欄是關鍵 — 強化**角色互不重疊原則**，避免老闆「全交給特助」的誘惑
- 對應 v0.8：**角色卡 7 張的卡面標準欄位**

##### #3 5-Gate Quality Check System — 升級鐵律卡 6 張的內涵

**原文設計**：每個 agent 產出都過 5 個品質閘：
1. **Factual Accuracy**（事實準確）
2. **Brand Voice**（品牌語氣）
3. **Legal & Compliance**（法律合規）
4. **Technical Quality**（技術品質）
5. **Business Logic**（商業邏輯）

**智谷怎麼用**：
- **鐵律卡 6 張**對應這 5 個 gate（智谷已有「自尊測試」「不編造」「商業機密」「客戶禁忌」「不上雲」「人工驗收」→ 跟 5-Gate 高度重疊但用詞更老闆友善）
- 每張鐵律卡的卡背加「對應 DigitalApplied 哪個 gate」當技術錨點
- 對應 v0.8：**鐵律卡 6 張的內涵深化**

##### #4 Orchestration Workflow 4 個範例 — 任務卡示範組合直接借鏡

**原文設計**：4 個完整多 agent 串接流程：
- **內容管線**：Researcher → Writer → QA → Social（35 min vs 手工 6-8 hr）
- **銷售管線**：Researcher → Sales → QA → Sales（31 min vs 3-4 hr）
- **客服升級**：Support → QA → Analyst（4 min/ticket vs 15-20 min）
- **週間 BI**：Analyst → Researcher → PM（25 min vs 3-4 hr）

**智谷怎麼用**：
- **任務卡背面**標「示範組合」（範例：任務 #4 合興提案 → Researcher 卡 → Writer 卡 → QA 卡 → Sales 卡）
- 講師手冊每張任務卡配 1 個「典型正確組合」+ 1 個「常見學員錯法」
- **時序卡 6 張**（v0.8 新增）的「串行」「平行」直接呼應 orchestration 邏輯
- 對應 v0.8：**任務卡示範組合 + 時序卡實戰應用**

##### #5 5 週漸進部署順序 — 完美對齊 MTG 三輪分層揭露

**原文設計**：絕不一次部署 10 個 agents，按週疊加：
- Week 1：Writer + QA（內容引擎）→ 立即有可見輸出
- Week 2：+ Researcher + Analyst（情報層）
- Week 3：+ Support + Sales（營收驅動）
- Week 4：+ Social + Designer（品牌存在感）
- Week 5：+ PM + Bookkeeper（操作主幹）

**智谷怎麼用**：
- **MTG 三輪揭露玩法**（v0.8 已拍板）可直接借這個漸進順序：
  - 第一輪 20 min：任務 + 角色（2 類 / 對應 Writer + QA 引擎）
  - 第二輪 40 min：+ 技能 + 知識（4 類 / 對應加 Researcher + Analyst）
  - 第三輪 20 min：+ MCP（5 類完整 / 對應全 10 個 agent）
- **講師可發「課後 5 週執行卡」**：每週解鎖一個新角色 → 學員回家照表操課
- 對應 v0.8：**整體教學時序 + 課後延續手冊**

##### #6 30 分鐘 Daily Standup 結構 — 學員「課後執行」核心儀式

**原文設計**：每日 30 min 三塊結構：
- **檢查昨日輸出**（10 min）— 跑過 QA 的逐項核准/修訂
- **派遣今日任務**（15 min）— 按 agent 分類派遣（「研究員幫我...」）
- **週一/週五加碼**（5 min）— 績效記分卡 / 設優先級

**智谷怎麼用**：
- 工作坊「**結尾儀式**」直接示範這 30 min Standup → 學員當場演練一次
- 講師發「**每日 30 分鐘行事曆模板**」讓學員回家貼在桌面
- 對應 v0.8：**講師手冊的工作坊結尾 + 課後延續 deliverable**

##### #7 6 個雷區（Don't 清單）— 開場踩雷預警 + 鐵律卡背面

**原文警告**：
1. ❌ 不要一次部署全部（品質失控）
2. ❌ 不要跳過手動編排階段（至少手動跑 2 週才自動化）
3. ❌ 不要跳過品質把關（**non-negotiable**）
4. ❌ 不要自動化所有任務（策略 / 客戶關係 / 高風險決策保留人做）
5. ❌ 不要忽視 prompt 細節（[COMPANY NAME] [INDUSTRY] 客製化）
6. ❌ 不要假設 AI 不會出錯（hallucination / miss context / off-brand）

**智谷怎麼用**：
- **開場 15 分鐘**插入「6 個常見雷區」當 mental model 預警 → 降低學員「AI 萬能」幻想
- 每個鐵律卡背面標「對應雷區 #N」做技術錨點
- 對應 v0.8：**開場鋪墊 + 鐵律卡 6 張的卡背**

---

#### 📊 教學設計性質總覽

- **覆蓋層級**：L0 學習目標 → L7 PPT 全包（罕見的「全棧素材」）
- **可借鏡的工法**：完整 SOP（task delegation / role card / quality gate / orchestration / standup / scorecard / phased rollout）
- **可帶走物件**：5 個檔（task matrix / role cards / quality checklist / workflow templates / daily routine）
- **真實範例**：4 個工作流範例 + 完整 system prompt 範例（Researcher）

---

#### 🎯 可套用情境

| 智谷工作坊段落 | 借鏡點 |
|--------------|--------|
| 開場 15 min mental model | 6 個雷區 + 經濟學對比敘事（10 agents $200-400 vs 5 人團隊 $25,000）|
| 第一輪揭露 20 min | 對應 Writer + QA「內容引擎」最小可用組合 |
| 第二輪揭露 40 min | 對應 Task Delegation Matrix 三軸評分 + 4 個 orchestration 範例 |
| 第三輪揭露 20 min | 對應 5-Gate Quality Check + 績效記分卡 |
| 結尾儀式 | Daily Standup 30 min 演練 |
| 課後執行手冊 | 5 週漸進部署順序 |

---

#### 💡 三句差異化敘事（行銷文宣可直用）

1. 「**DigitalApplied 給你 blog 模板，智谷給你卡牌組 + 講師當場帶 + 5 週漸進落地手冊**」
2. 「**他們的 10 個 agent 是營運導向（內容 / 客服 / 業務），智谷的 6 個是 C-suite 戰略導向（CEO/CMO/CFO/CSO/CPO/特助）**」
3. 「**他們純英文，學員定位非技術 founder；智谷繁中 + 製造業 / 服務業 / 教育訓練業情境，台灣老闆秒懂**」

---

#### 🔴 為什麼這個 idea 對招生很關鍵

- 「DigitalApplied 認證」可變成**社會證明**：「英文圈最完整的 agent team playbook 學員定位跟我們一樣，他們收費 $0 賣後端 AI 顧問，智谷收 $18,000 但**當場帶你做完 + 帶卡牌組回家 + 5 週執行手冊**」
- 老闆會接受「**比英文免費版貴，但省 5 週自學摸索的學費**」的敘事
- 對應到 competitor.md G4「**主推 A 全天版 NT$18,000 市場甜蜜空缺**」的價值錨點

---

---

### [2026-05-24] Batch A 研究 — Anthropic 官方文件（架構機制層）

> 目的：課程的「技術依據層」，幫助老闆學員理解幕僚系統的四個機制，並對應到老闆語言。

---

#### A-1. CLAUDE.md — 幕僚的員工手冊

**來源**：[Anthropic 官方 Memory 文件](https://code.claude.com/docs/en/memory)

**核心機制**：
- CLAUDE.md 是 AI 每次上工前自動讀的「入職文件」，確保它記住你的角色、規則、公司脈絡
- 放置位置決定作用範圍：全局（`~/.claude/CLAUDE.md`）→ 個人（主資料夾）→ 單一專案（可 git commit 讓團隊共享）→ 本地私人（加進 .gitignore）
- Auto memory：Claude 自己學到的偏好會自動寫進 `MEMORY.md`，下次自動帶入
- `@import` 語法：可引用其他檔案讓記憶模組化（例如 `@README` / `@docs/SOP.md`）
- 有效寫法：**200 行以內**、用 markdown 結構化、指令要具體可查驗

**可直接引用的官方語句**：
> "Treat CLAUDE.md as the place you write down what you'd otherwise re-explain. Add to it when Claude makes the same mistake a second time."

**課程用途**：
- ✅ **S1 心智模型鋪墊**：CLAUDE.md = 員工手冊，每次上工前自動讀
- ✅ **bs 指令 / 訪談五要素**的官方依據
- ✅ 解釋「為何 Claude Code 記得你，ChatGPT 不記得」

---

#### A-2. Subagents — 給幕僚設定角色邊界

**來源**：[Anthropic 官方 Sub-agents 文件](https://code.claude.com/docs/en/sub-agents)

**核心機制**：
- Subagent = 一個 `.md` 檔案放在 `.claude/agents/`，定義角色名稱、職責說明、工具清單、使用模型
- 建立方式：`/agents` 指令 → Create new agent → 描述用途 → Claude 自動生成系統 prompt
- 每個 subagent 有**獨立 context window**，主 agent 只收「結論摘要」（節省 context，降低成本）
- 可為不同 subagent 指定不同模型：研究型用 Haiku（快省）、決策型用 Opus（強）
- 可精確鎖定權限：「只能讀不能寫」的 subagent 就算指令出錯也不會動到系統

**可直接引用的官方語句**：
> "Control costs by routing tasks to faster, cheaper models like Haiku."

**課程用途**：
- ✅ **S2 卡牌模擬**的技術底層：每張角色卡 = 一個 subagent 定義
- ✅ 說明「幕僚只回報結論」的架構邏輯
- ✅ 「指定模型」 = Token 效率競賽的官方依據

---

#### A-3. Hooks — SOP 的自動執法層

**來源**：[Anthropic 官方 Hooks 文件](https://code.claude.com/docs/en/hooks)

**核心機制**：
- Hooks 寫在 `settings.json`，格式：**事件 → 篩選條件 → 執行動作**
- 14 種時間點：`SessionStart`（啟動時）/ `PreToolUse`（工具執行前）/ `PostToolUse`（執行後）/ `Stop`（回應完畢）等
- **守門員邏輯**：Exit code 2 = 強制阻止 Claude 執行；Exit code 0 = 正常通過
- 常見用途：完成任務後自動記錄 log / 自動通知 Slack / 阻擋危險指令（如 `rm -rf`）
- 全程不需人工轉手，流程自動跑

**可直接引用的官方語句**：
> "If an instruction is something that must run at a specific point—such as before every commit or after each file edit—write it as a hook instead."

**課程用途**：
- ✅ **進階學員**（有 IT 背景）的延伸知識
- ✅ 解釋「幕僚如何自動跑 SOP」而不是「每次要提醒它」
- ✅ **Hooks 心法卡**的官方依據

---

#### A-4. Agent Teams — 幕僚之間互相 review 的架構

**來源**：[Anthropic 官方 Agent Teams 文件](https://code.claude.com/docs/en/agent-teams)

**核心機制**：
- 架構：Team Lead（主 session）+ Teammates（獨立 Claude instances）+ 共用 Task List + Mailbox 訊息系統
- **與 Subagent 最大差異**：Teammate 之間可以直接互傳訊息、互相質疑；Subagent 只能回報主 agent
- 建立方式：用自然語言告訴 Lead 要什麼架構，Claude 自動生成（`~/.claude/teams/`）
- 建議規模：**3-5 個 Teammate**，每人 5-6 個任務（超過後協調成本抵消效益）
- 目前狀態：實驗性功能，需在 settings.json 開啟 `CLAUDE_CODE_EXPERIMENTAL_AGENT_TEAMS`

**可直接引用的官方語句**：
> "Spawn 5 agent teammates to investigate different hypotheses. Have them talk to each other to try to disprove each other's theories, like a scientific debate."

**課程用途**：
- ✅ **S4 進階演示**：讓老闆看到「幕僚開會辯論」的實際效果
- ✅ 說明「單一幕僚 vs 幕僚團隊」的差異
- ✅ **課程最高潮**的技術亮點（實驗性 = 搶先看）

---

#### 📐 四機制學習梯度（Batch A 最終結論）

| 層次 | 機制 | 老闆動作 | 對應課程段落 |
|------|------|---------|-------------|
| 基礎 | CLAUDE.md | 寫員工手冊 | S1 |
| 中階 | Subagents | 定義幕僚角色邊界 | S2-S3 |
| 進階 | Hooks | 建 SOP 自動執法 | S3 選修 |
| 最高 | Agent Teams | 讓幕僚互相辯論協作 | S4 演示 |

> 這個梯度剛好是「老闆從零到一打造 AI 幕僚系統」的完整學習路徑。

---

### [2026-05-24] Batch B 研究 — 企業 Agent Team 實戰個案庫（4 個驗證來源）

> 本批研究聚焦：**真實企業如何架設 agent team + 實際落地的架構與經驗**，作為課程「個案庫」素材與教學設計依據。
> 課堂用途：開場佐證（「別人都在做」）+ S2 抽牌模擬參照 + 課後個案閱讀

---

#### B-1. ai-c-suite（GitHub）— 開源 C-suite Agent 五人組

**來源**：[github.com/one-personcompany/ai-c-suite](https://github.com/one-personcompany/ai-c-suite)

**架構一覽**：

| Agent | 職責定義 |
|-------|---------|
| CEO | 戰略方向、重大決策 |
| CTO | 技術架構、技術選型 |
| COO | 營運效率、流程優化 |
| CFO | 財務分析、成本控制 |
| CMO | 品牌策略、市場推廣 |

**技術實作**：
- 每個 agent 一個資料夾，內含 `AGENTS.md` 角色定義檔
- 統一用 shell script（`c-suite-communicate.sh`）切換 agent 溝通
- 支援 Codex、Claude Code、Qwen 三種後端（環境變數切換）

**對智谷課程的用途**：
- ✅ **S1 開場佐證**：「開源社群早就在做 C-suite agent，智谷幫你做繁中 + 製造業版本」
- ✅ **角色卡設計驗證**：跟智谷 6 幕僚（CPO/CMO/CFO/CSO/特助/工程師）比較，讓學員理解「幕僚組合沒有標準答案」
- ⚠️ 純 shell / 工程師底層，**老闆無法直接用** → 正好凸顯智谷 Claude Code + CLAUDE.md 路線的易用差異
- ✅ **任務卡 #6「建立幕僚角色」** 對照案例

---

#### B-2. AI Chief of Staff — 個人 AI 幕僚長實作（Barbara Bermes）

**來源**：[Medium — Building My Own AI Chief of Staff](https://bbinto.medium.com/building-my-own-ai-chief-of-staff-and-why-you-might-want-one-too-7e862a052a85)

**核心設計**：
- 每週自動產出「主管週報」，回答三個問題：①這週交付了什麼？②跨產品/團隊出現什麼模式？③還沒浮現的訊號是什麼？
- 資料整合：Slack、Jira、Calendar（MCP 直連）+ CSV/JSON 手動丟入資料夾
- 架構四層：Orchestrator → MCP 資料源 → Claude API Loop → 報告輸出

**成本 & 時間**：
- 一次性建置：12-15 小時
- 月費：Claude Pro $24 + API ~$15-20 ≒ $40/月（NT$1,200）
- 效益：消除手動合成，主管時間回歸高層決策

**作者關鍵話語**（可直接引用於課堂）：
> "The plumbing is generic. I only need to plug in different instructions and data sources."
> （管線是通用的，我只需要換上不同指令和資料源）

**對智谷課程的用途**：
- ✅ **S4 實作參考**：學員「幕僚週報」任務卡的真實版本
- ✅ **CLAUDE.md 訓練類比**：「你只要寫清楚給幕僚的指令，它就會跑」
- ✅ **ROI 敘事**：$40/月 vs 人力時間，製造業老闆能算帳
- ✅ **MCP 說明**：最直觀的 MCP = 幫 Claude 接公司系統的橋

---

#### B-3. CFO Agent + Xero MCP — 財務 AI 幕僚 20 分鐘上線

**來源**：[Medium — How I Turned AI Into My CFO Assistant](https://medium.com/vibe-coders/how-i-turned-ai-into-my-cfo-assistant-with-xero-mcp-f89eef186ff5)

**核心設計**：
- 透過 Xero MCP，Claude 直接查詢會計系統 → 回答「2025 年我們的毛利是多少？」
- Claude Desktop 自動獲得約 40 個財務指令
- 設定流程：建 Xero Custom App（API 憑證）→ 安裝 MCP → 重啟 Claude Desktop = 完成

**真實應用情境**：
- 「哪些訂閱超過 £50/月？」
- 「沒有分類的交易有哪些？」
- 「VAT 負債 + 毛利趨勢 → 生成含互動圖表的 HTML 報告」

**資安設計**：唯讀 API 憑證、存在本機、不上雲 = 跟智谷課程資安原則一致

**對智谷課程的用途**：
- ✅ **MCP 能力卡最佳示範**：從「用自然語言查財務」具體說明 MCP 是什麼
- ✅ **S3「MCP 連結外部世界」段落**直接引用：「20 分鐘，CFO 幕僚能看你的財務系統了」
- ✅ **B2B 採購說服素材**：「這不是工程師玩具，財務主管當天用得上」
- ✅ 資安疑慮化解：唯讀 + 本機的設計同步照應「資安政策卡」

---

#### B-4. HumanLayer — 寫好 CLAUDE.md 的實用指南

**來源**：[humanlayer.dev/blog/writing-a-good-claude-md](https://www.humanlayer.dev/blog/writing-a-good-claude-md)

**核心原則**：

| 原則 | 說明 |
|------|------|
| LLM 是無狀態的 | CLAUDE.md = 每次 session 重新上工的「員工入職文件」 |
| WHAT / WHY / HOW 三層 | 是什麼（架構）/ 為什麼（目的）/ 怎麼做（工作流程）|
| 少即是多 | Claude Code 系統 prompt 已含 ~50 條指令；你的 CLAUDE.md 目標 < 300 行，HumanLayer 自己只用 60 行 |
| 用 reference，不貼程式碼 | 指向檔案:行號，不要貼 code snippet（會過時） |
| 不要寫 linter | 格式/排版由工具管，別塞進 CLAUDE.md |

**對智谷課程的用途**：
- ✅ **S1「CLAUDE.md = 職務說明書」** 類比的技術依據 — 「無狀態」是直白解釋為何要寫 CLAUDE.md
- ✅ **「三層問法」** 可直接成為學員 bs 指令訪談的引導框架（幕僚是誰 / 做什麼 / 怎麼做）
- ✅ **防學員塞太多**：開場明確說「60 行夠用，不要塞整個 SOP 進去」
- ✅ **心法卡「精準 ≠ 長」** 的設計依據

---

#### 📊 Batch B 關鍵數據（課堂引用可直接使用）

| 數據 | 來源 | 備注 |
|------|------|------|
| $40/月 → 消除主管手動整合工時 | Bermes AI Chief of Staff | 個人實測，非大型調研 |
| 20 分鐘設定 CFO Agent | Xero MCP 文章 | 需有 Xero 訂閱（£5/月） |
| ~40 個財務指令自動化 | Xero MCP 文章 | Claude Desktop 環境 |
| 開源 5-agent C-suite | ai-c-suite GitHub | Shell-based，非 Claude Code 原生 |

> ⚠️ Klarna $60M / 73% SMB 生產力等廣泛流傳的數字尚未找到一手來源，**不建議課堂直接引用**，待 Batch A 補核實。

---

---

### [2026-05-24] Batch C 研究 — Claude Code vs 替代品工具比較

> 目的：幫學員回答「為何選 Claude Code 而非 ChatGPT / Cursor / Copilot？」

---

#### C-1. Claude Code vs ChatGPT：老闆最該知道的 3 件差異

**來源**：[IntuitionLabs 企業比較](https://intuitionlabs.ai/articles/claude-vs-chatgpt-vs-copilot-vs-gemini-enterprise-comparison) / [Mobikasa](https://www.mobikasa.com/blog/claude-vs-chatgpt-for-business-key-differences-pricing-and-which-use-case)

| | ChatGPT | Claude Code |
|---|---|---|
| 記憶 | 每次對話歸零 | CLAUDE.md 永久記住你的公司脈絡 |
| 能力 | 給建議、回答問題 | 執行任務、操作你的系統（MCP）|
| 定位 | 萬用但分心 | 專精業務自動化 |

**可直接用於課堂的比喻**：
> 「ChatGPT 是臨時工，Claude Code 是記得你規矩的正職員工。」

**課程用途**：
- ✅ **S1 差異化說明**：讓老闆 30 秒懂為何要換工具
- ✅ **S3 CLAUDE.md 段落**鋪墊：「你在 CLAUDE.md 寫的，就是讓 Claude 記住的」

---

#### C-2. Claude Code vs Cursor vs Copilot（開發者生態）

**來源**：[NxCode 比較](https://www.nxcode.io/resources/news/cursor-vs-claude-code-vs-github-copilot-2026-ultimate-comparison) / [CosmicJS](https://www.cosmicjs.com/blog/claude-code-vs-github-copilot-vs-cursor-which-ai-coding-agent-should-you-use-2026)

| | Copilot | Cursor | Claude Code |
|---|---|---|---|
| 性質 | IDE 外掛（補全建議）| AI-native IDE | 終端機 Agent |
| 任務規模 | 單行/函數 | 單檔/小專案 | 整個 repo / 跨任務 |
| 非技術老闆能用？ | ❌ | ❌ | ✅ |
| 2026 開發者喜好 | 9% | 19% | 46% |

**課程用途**：
- ✅ 對有 IT 部門的 B2B 學員：讓他們理解 Copilot≠Claude Code
- ✅ **鐵律卡「交辦任務，不是補全建議」**的技術依據

---

#### C-3. MCP：Claude Code 連接公司系統的橋

**來源**：[Nimbalyst — Best Claude Code MCP Servers](https://nimbalyst.com/blog/best-claude-code-mcp-servers/) / [Data-Mania 行銷應用](https://www.data-mania.com/blog/top-10-claude-mcp-servers-for-marketing/)

**關鍵數據**：
- 2025 年初：幾十個 MCP server
- 2026 年 4 月：已超過 **10,000 個**公開 server
- 2025 年 12 月：Anthropic 將 MCP 捐給 Linux Foundation，ChatGPT / Gemini / Copilot **全部採用**此標準

**老闆語言解釋**：MCP = 讓 Claude 從「聊天機器人」變成「能動你公司系統的員工」

**可串接的商業工具**（老闆聽得懂的）：
Google Sheets / Notion / Slack / HubSpot / Stripe / Xero / GitHub

**課程用途**：
- ✅ **S3「MCP 連結外部世界」**的核心素材
- ✅ 用「10,000 個外掛」讓老闆感受生態系的爆發

---

#### C-4. 非技術主管如何用 CLAUDE.md

**來源**：[PM 使用指南 Medium](https://medium.com/product-powerhouse/claude-code-for-product-managers-complete-setup-guide-real-pm-workflows-2026-c94ec7087b6f) / [Techsy — Claude for Small Business](https://techsy.io/en/blog/claude-for-small-business-review)

**2026-05-13 重要消息**：Anthropic 推出 **Claude for Small Business**
- 15 個預建工作流
- 15 個可重用技能
- 10+ 個商業 connector
- 定位：不需 IT 部門即可部署

**CLAUDE.md 能寫什麼（非技術主管版）**：
- 公司術語 / 客戶偏好 / 禁用詞
- 工作流程 SOP
- 客戶禁忌 / 公司規矩

**課程用途**：
- ✅ **bs 指令 / 訪談 5 要素**的直接支撐
- ✅ 「Claude for Small Business」可當智谷課程的市場驗證佐證

---

#### 📊 Batch C 關鍵數據（課堂可直接引用）

| 數據 | 來源 | 信心 |
|------|------|------|
| 開發者工具偏好：Claude Code 46% > Cursor 19% > Copilot 9% | NxCode 2026 | 中 |
| MCP server 數量：2026/4 已超過 10,000 個 | Nimbalyst | 高 |
| MCP 已成跨廠商開放標準（Linux Foundation）| Anthropic 官方 | 高 |
| Fortune 500 中 92% 用 ChatGPT（因 Microsoft 生態）| IntuitionLabs | 中 |

---

### [2026-05-24] Batch D 研究 — AI Agent Team 成熟度模型個案庫

> 目的：讓學員能回答「我現在在哪個階段，下一步去哪」，設計課堂自我定位活動用。

---

#### D-1. Kellogg 4-Stage AI Adoption Model（最適合非技術老闆）

**來源**：[Kellogg School of Management](https://insight.kellogg.northwestern.edu/article/4-stages-ai-adoption)

| 階段 | 比喻 | 定義 |
|------|------|------|
| Stage 1 | Cog（齒輪）| 替換人工重複任務 |
| Stage 2 | Intern（工讀生）| 替換較複雜任務 |
| Stage 3 | Collaborator（同事）| AI 與人平行工作 |
| Stage 4 | Agent（負責人）| AI 作為專案負責人 |

**課程用途**：
- ✅ **S1 開場自我定位活動**：5 分鐘讓學員討論「你的公司現在在哪一關」
- ✅ 比喻完全不需要技術背景（工讀生 → 同事 → Agent = 老闆直覺語言）
- ✅ 智谷課程目標 = 帶學員從 Stage 2 跨到 Stage 3-4

---

#### D-2. Salesforce Agentic Maturity Model（企業市場共識）

**來源**：[Salesforce News](https://www.salesforce.com/news/stories/agentic-maturity-model/)

4 個層級，從個人 AI Copilot 到跨組織自主 Multi-Agent。

**課程用途**：
- ✅ 對「我們用 Salesforce / ChatGPT」的學員，直接對應「你現在在第幾層」
- ✅ 全球最大 CRM 廠商出品 = 業界共識背書，不需要解釋為何這個框架可信

---

#### D-3. ServiceNow Enterprise AI Maturity Index 2025（最震撼的開場數據）

**來源**：[ServiceNow Enterprise AI Maturity Index](https://www.servicenow.com/workflow/ai/enterprise-ai-maturity-index-2025.html)

**關鍵數據**：
- 全球企業 AI 成熟度平均分：35 / 100（2025）
- **全球不到 1% 的企業超過 50 分**

**課程用途**：
- ✅ **S1 開場投影片**：「全球 99% 的企業還沒過一半，現在跟上是分水嶺」
- ✅ 讓老闆不覺得自己落後（大家都還在早期），同時建立緊迫感

---

#### D-4. HyScaler 30-Day Agentic AI Quickstart for SMBs

**來源**：[HyScaler](https://hyscaler.com/insights/agentic-ai-implementation-for-smb/)

30 天快速啟動路線圖，適合資源有限的中小企業。

**課程用途**：
- ✅ **S4 課後行動計劃**：學員帶走「接下來 30 天做什麼」的具體清單
- ✅ 不需要工程師就能照著做

---

#### D-5. Multi-Agent Orchestration 老闆語言解釋

**來源**：[Kore.ai](https://www.kore.ai/blog/what-is-multi-agent-orchestration) / [MindStudio](https://www.mindstudio.ai/blog/multi-agent-orchestration-patterns)

**Kore.ai 可直接用的比喻**：
> 「Orchestrator = 總指揮，各 Agent = 專職部門，共同完成一件複雜任務」

**MindStudio 三種架構模式**：主管型（Supervisor）/ 分散協作型（Adaptive Network）/ 客製型（Custom）

**課程用途**：
- ✅ **S1 心智模型**：老闆聽得懂「總指揮 + 專職部門」的類比
- ✅ **S3 進階**：讓老闆對應「我的組織結構像哪種 Agent 架構」
- ✅ 可直接做投影片圖示（三種模式 = 三張卡）

---

#### 📊 Batch D 關鍵數據（課堂可直接引用）

| 數據 | 來源 | 信心 |
|------|------|------|
| 全球 AI 成熟度平均 35/100，<1% 超過 50 分 | ServiceNow 2025 | 高 |
| 小企業 AI 採用率 39%→55%（2024→2025） | JP Morgan Chase | 高 |
| 56% 組織導入 orchestration 後提升可擴展性 | Hubstic 2026 | 中 |
| 61% 企業主已在部署 AI Agent | Hubstic 2026 | 中 |
| SMB Agentic AI 月費：$100–500（標準工作量） | HyScaler | 中 |

> ⚠️ Gartner「40% 企業應用將內建 AI Agent（2026）」等預測數字需自行核實一手報告後才引用。

---

#### 🎯 三框架課堂組合建議（D 批最終結論）

| 時序 | 框架 | 用途 |
|------|------|------|
| S1 開場 5 min | Kellogg 4-Stage | 自我定位活動（你在哪一關）|
| S1 數據震撼 | ServiceNow <1% | 建立緊迫感 + 降低自我落後感 |
| S3 中段 | Salesforce 4 Level | 說明「升一級要什麼條件」 |
| S3 進階 | Kore.ai 總指揮比喻 | Orchestration 直觀說明 |
| S4 收尾 | HyScaler 30-Day | 課後行動計劃 |

---

---

### [2026-05-24] Batch B2 — 企業 Agent 實作 Writeup（5 個深度案例）

---

#### B2-1. claude-chief-of-staff（GitHub 開源，最完整 CLAUDE.md 範本）

**來源**：[github.com/mimurchison/claude-chief-of-staff](https://github.com/mimurchison/claude-chief-of-staff)

**建了什麼**：單一 Chief of Staff，6 種操作模式：Prioritize / Decide / Draft / Coach / Synthesize / Explore。Claude 根據對話內容**自動判斷**現在該用哪個模式，不需手動切換。

**架構**：
```
~/.claude/CLAUDE.md          ← 角色定義 + 6 個模式 + 鐵律
~/.claude/goals.yaml         ← 優先目標
~/.claude/contacts/          ← 人際關係追蹤（三層重要度，14/30/60 天 flag）
~/.claude/my-tasks.yaml      ← 任務清單
```

**鐵律設計（直接可借鑑）**：
- 任何訊息發送前必須等 user 明確批准（`Never send any message without explicit approval`）
- 出現 fundraising / litigation / termination 關鍵字 → 觸發警告

**課程用途**：CLAUDE.md 鐵律設計示範、邊界保護機制、bs 指令範本參照

---

#### B2-2. 37 個 Agent 自主新創系統（DEV Community）

**來源**：[dev.to/asklokesh — How I Built an Autonomous AI Startup System with 37 Agents](https://dev.to/asklokesh/how-i-built-an-autonomous-ai-startup-system-with-37-agents-using-claude-code-2p79)

**建了什麼**：7 個 Swarm，共 37 個 agent：工程（8）/ 營運（8）/ 業務（8）/ 資料 / 產品 / 成長 / 審查

**Code Review Pipeline（平行協作範例）**：
```
IMPLEMENT → REVIEW（3 個 reviewer 並行）→ AGGREGATE → FIX → RE-REVIEW → COMPLETE
```
3 個 reviewer 同時跑（code quality / business logic / security），severity-tagged 問題決定是否 block。

**實作亮點**：每個 agent 有獨立 state 檔案 → rate limit 後能自動恢復，不會整個任務斷掉。

**課程用途**：大型多 agent 架構概念、平行協作演示、「agent 越多不一定越好」的對話起點

---

#### B2-3. 26 個 Agent Chief of Staff 系統（Substack，最完整實作）

**來源**：[doneyli.substack.com — I Built an AI Chief of Staff That Actually Works](https://doneyli.substack.com/p/i-built-an-ai-chief-of-staff-that)

**建了什麼**：26 個 agent 三組：幕僚長子系統（7）/ 本地基礎設施（9）/ 內容研究（10）

**硬體**：一台閒置 M1 MacBook Pro，用 `caffeinate` 永不睡眠，macOS launchd 排程（重開機後仍存活）

**兩層成本控制架構**：
- Tier 1：每 30 分鐘規則跑 → **不花 token**
- Tier 2：每天下午 5 點累積約 50 封 email → 才用 Claude 分類起草

**信任量化門檻（關鍵設計）**：
自動發信條件 = `edit distance < 10%` + `confidence > 0.9` + `每小時 < 5 封` + `非受保護聯絡人`
→ 把信任量化成**可測量指標**，不是模糊的「AI 判斷」

**每日成本**：約 $3 美元（分類用 Haiku，起草用 Sonnet）

**課程用途**：token 成本分層策略、信任量化設計、「從玩具到真實系統」的距離說明

---

#### B2-4. lst97/claude-code-sub-agents（GitHub，33 個 agent 範本庫）

**來源**：[github.com/lst97/claude-code-sub-agents](https://github.com/lst97/claude-code-sub-agents)

**建了什麼**：33 個 agent，8 大類，每個是一個 Markdown 檔（YAML frontmatter + 系統 prompt）。含一個 `agent-organizer` 作為 meta orchestrator。

**Agent MD 檔案格式**：
```yaml
---
name: kebab-case-name
description: 自動觸發條件與關鍵字（這欄決定 Claude 何時 invoke 這個 agent）
tools: [可選，預設全部]
---
# 角色名稱
**Role**: 職責與邊界
**Expertise**: 核心技術領域
```

**關鍵設計**：description 欄位寫清楚關鍵字 → Claude Code 自動判斷要 invoke 哪個 agent，不需 user 手動指定。

**課程用途**：Agent MD 格式示範、description 欄位設計練習、subagent 資料夾架構參照

---

#### B2-5. Paperclip 行銷公司（MindStudio）

**來源**：[mindstudio.ai — Build a Multi-Agent Company with Paperclip + Claude Code](https://www.mindstudio.ai/blog/build-multi-agent-company-paperclip-claude-code)

**建了什麼**：4 個角色組成 AI 行銷公司：CEO（Opus）/ Researcher（Sonnet）/ Marketer（Sonnet）/ Designer（Sonnet）

**模型分層策略**：CEO 用 Opus 做複雜推理，其他用 Sonnet → 依認知複雜度選模型，不統一用最貴的

**Agent 間溝通**：file-based messaging（寫入共用目錄，polling 2000ms）

**每個 agent 的 prompt 必備四元素**：
1. 職責描述
2. 明確列出不該做什麼
3. 指定輸出格式（Markdown / JSON / 結構化文字）
4. 至少一個具體行為範例

**啟動**：`paperclip start --all` → 把目標丟給 CEO → 後續全程自動委派

**課程用途**：agent prompt 四元素設計、模型分層選型、老闆視角「一句話啟動整個團隊」演示

---

### [2026-05-24] Batch B3 — 各行業 Agent 落地案例（10 個，有數字）

---

#### 行銷

**Harley-Davidson 紐約店 × Albert.ai**
URL: https://hbr.org/2017/05/how-harley-davidson-used-predictive-analytics-to-increase-new-york-sales-leads-by-2930
AI 廣告 agent 發現「Call now」比「Buy now」效果好 447%，自動全線換詞，人沒介入。
→ 3 個月潛在客戶 +2,930%，每日詢問 1 通 → 40 通
**課程用途**：行銷主管開場震撼數據，「AI 自己發現規律、自己改」

**屈臣氏（A.S. Watson）AI 購物顧問**
URL: https://superagi.com/ai-powered-marketing-automation-case-studies-on-how-ai-agents-boost-efficiency-and-roi-in-2025/
→ 使用 AI 顧問的顧客轉換率高 396%，消費金額高 4 倍

---

#### 業務／CRM

**Salesforce 自家 SDR Agent**
URL: https://www.salesforce.com/news/stories/agentforce-customer-success-stories/
追蹤 43,000 筆沉睡名單自動挖掘 → 挖出 170 萬美元新案源

**1-800Accountant 稅季客服 Agent**
URL: https://www.salesforce.com/news/stories/agentforce-customer-success-stories/
→ 稅季高峰期 70% 對話 AI 自主解決，不轉人工

---

#### 財務

**金融服務公司財報 Agent**
URL: https://www.accelirate.com/agentforce-case-studies/
→ 報表生成：15 天 → 35 分鐘；每份成本：$2,200 → $9；錯誤率 -90%

**Wiley 出版商 Agentforce**
URL: https://www.salesforce.com/agentforce/metrics/
→ ROI 213%；自助服務效率 +40%

---

#### 客服

**Vodafone AI 客服**
URL: https://www.sobot.io/article/ai-customer-service-case-studies-2025-support-satisfaction-cost/
→ 每次對話成本 -70%

**Klarna AI 客服**
URL: https://www.nexgencloud.com/blog/case-studies/how-ai-and-rag-chatbots-cut-customer-service-costs-by-millions
→ 處理 230 萬對話，等於 700 名全職客服工作量

---

#### 營運

**大型零售商庫存調配 Agent**
URL: https://www.accelirate.com/agentforce-case-studies/
→ 調配決策：10 天 → 1 小時；季虧損：$540 萬 → $160 萬

**Quickbooks 中小企業財務 Agent**
URL: https://quickbooks.intuit.com/r/running-a-business/agentic-ai-for-business/
→ 發票處理：20 分鐘 → 2 分鐘；每月省 10 小時行政時間

---

### [2026-05-24] DigitalApplied — Agentic AI Executive Team Playbook 2026

**來源**：[DigitalApplied — Agentic AI Executive Team Playbook: Decision Support 2026](https://www.digitalapplied.com/blog/agentic-ai-executive-team-playbook-decision-support-2026)

> ⭐ Demo 候選：架構清晰，可用 Jimmy 現有幕僚系統（特助 + 財務主管 + 策略幕僚）當場演示「3 個 agent 協作完成一份決策簡報」。

---

#### 核心架構：5 個角色，分工不合並

| 角色 | 職責 | 觸發頻率 |
|------|------|---------|
| CEO | 董事會報告合成（60-80 頁彙整）| 每季 |
| CFO | 情境模擬器（what-if 模型）| 隨需 + 常設庫 |
| COO | 綜合儀表板（ERP + BI）| 每週 + 異常觸發 |
| CSO | 競品情報簡報（財報 / 法說會 / 新聞）| 每月 + 事件觸發 |
| **Chief of Staff** | 日常運作 / 範本維護 / 紀律把關 | 日常 |

**作者最強論點（課堂必引）**：
> "Programs that try to consolidate the four into a single unified executive agent typically produce a system that does none of the four well."
> 把四個塞成一個 super agent → 四個都做不好。**分工才是對的。**

---

#### 三層資料骨幹（data backbone）

| 資料源 | 負責人 | 用途 |
|--------|--------|------|
| ERP | CFO | 財務 / 結帳資料，每次跑前留不可變快照 |
| CRM | CSO | 管線 / 客戶健康 / 勝負分析 |
| BI | COO | KPI + 營運指標（接語意層，不接原始資料）|

---

#### 90 天落地時程（直接可變課後行動計劃）

| 時程 | 任務 | 關卡（Gate）|
|------|------|------------|
| Day 1-30 | 簽 AI 憲章、接通 ERP、確立 attestation 範本 | ERP 端對端 + 稽核 log 可跑 |
| Day 31-60 | 上線第一個用途（COO 儀表板）、建立評估基線 | 主管確認採用 |
| Day 61-90 | 建立月度例會、上線第二個用途 | 兩個用途上線，準備 Q2 |

> 董事會用途刻意延到 Q2，等「整季的實際運作證據」再推。

---

#### 鐵律：每個產出必須有 attestation（簽署確認）

每份 agent 輸出必須標注：
1. 用了哪個模型
2. 資料快照時間點
3. 使用的 synthesis prompt
4. 人工審核者簽名

---

#### 三個可直接用於課堂的金句

1. > "Decision support, not decision-delegation — agent 出分析，老闆做決定。"
2. > "The source-integration discipline is the constraint. The agent is only as trustworthy as the data it reads."
3. > "Programs without a named chief of staff collapse the load onto the CEO and stall by month four."（沒有特助幕僚長，第四個月就垮了）

---

#### 對智谷課程的用途

| 課程段落 | 用法 |
|---------|------|
| S1 開場心智模型 | 「4 個平行 agent 不能合成一個」= 分工比合併強 |
| S2 卡牌模擬 | 4 個用途 × 觸發頻率 = 任務卡設計參照 |
| S3 Chief of Staff 段落 | 「最高槓桿的單一決策」直接引用 |
| S4 Demo | 特助 + 財務主管 + 策略幕僚 → 當場跑一份決策簡報 |
| 課後行動計劃 | 90 天時程表直接給學員帶走 |

---

---

### [2026-05-25] Operations Agent 協作模式庫（11 種）— 課堂視覺化素材

**來源**：NotebookLM 雙 notebook 深挖（Paperclip 官方文件 + AI Agent 趨勢企業案例）
**教學設計性質**：視覺化圖解 × 真實 ops 案例 × 學員討論觸發
**可套用情境**：「Agent Team」單元核心素材；每種模式一張視覺圖 + 一個 30 秒口頭舉例

> **視覺化設計原則**：每種模式用「方框 + 箭頭」示意圖，搭配 1 個台灣企業可對應的場景說明。學員看圖 → 猜適用情境 → 講師揭曉 → 問「你的公司哪個部門最像這種？」

---

#### 模式 1：Sequential Pipeline 流水線
```
觸發 → [Agent A] → [Agent B] → [Agent C] → [Agent D] → 交付
        資料蒐集   業務分析    財務建模    報告送出
```
**嚴格順序，每人只做一段，不跳步驟。**

真實案例：Fortune 500 房地產公司租約更新——Property Data Agent → Business Analyst Agent → Portfolio Advisor Agent → Coordinator Agent（發 Slack/Email）。原本 3 天 → 數小時。

課堂問法：「如果你的採購流程有 5 個審核關卡，你會怎麼用這個？」

---

#### 模式 2：Hub-and-Spoke 統一指揮
```
            [專家A]
           ↗
[中央指揮] → [專家B] → 中央指揮統整結果 → 交付
           ↘
            [專家C]
```
**一個 orchestrator 分發任務給多個專家，再把結果統整回來。**

真實案例：L'Oréal 客戶數據分析——主 Agent 收到問題，分給語意/地理/產品/計算 4 個子 Agent 並行查詢，主 Agent 合成最終答案，準確率從 90% → 99.9%。

課堂問法：「你公司的月報需要跨幾個系統拉數據？每個系統給一個 agent，最後一個 agent 組裝報告。」

---

#### 模式 3：Parallel Broadcast 同時廣播
```
[觸發事件] ──→ [IT Agent]（裝機）
            ├──→ [HR Agent]（設薪）
            ├──→ [法務 Agent]（合規）
            └──→ [設施 Agent]（門禁）
```
**一個事件同時觸發多條獨立流程，互不等待。**

真實案例：ServiceNow 新員工入職——HR 系統偵測到新進人員，同時觸發 IT 設備、薪資設定、合規訓練、辦公室門禁 4 條線，全部並行，員工第一天到職時全部就緒。

課堂問法：「你們新人入職需要跑幾個部門？每個部門同時跑，人到了才不需要等。」

---

#### 模式 4：Event-Driven 監控觸發
```
[Agent 待機] ──── 一般情況不動 ────
     ↓ 異常事件發生
[Agent 醒來] → 分析 → 行動 → 通報
```
**Agent 平時沉睡，只有「事件」才觸發。省資源，反應快。**

真實案例：FedEx 物流——Agent 持續監看路況/天氣，只有偵測到延誤才自動重排路線。企業 KPI 監控——每天掃財務/庫存指標，只有偏離閾值才發警報 + 自動找根因。

課堂問法：「你有沒有哪個數字，你希望它一偏掉就自動叫你？那就是 event-driven 的用法。」

---

#### 模式 5：Human Gate 強制人工關卡
```
[Agent 跑完] → [人工審查點] → ✅ 通過才繼續 → 執行
                              ❌ 退回修改
```
**Agent 做好準備工作，但某個節點 100% 等人類決定，不能自動跳過。**

真實案例：金融合規——Agent 5 分鐘做完客戶盡職調查（CDD）研究，但最終核准必須合規官人工簽字。金融業 0% 完全自主決策，永遠有 Human Gate。高額匯款場景：Agent 備好 $500 萬匯款資料，暫停等 CFO 點擊確認才執行銀行 API。

課堂問法：「你公司有沒有哪些動作，就算 AI 做得再好，還是要蓋章才行？那就是你的 Human Gate。」

---

#### 模式 6：Peer Review Loop 互審循環
```
[執行 Agent] → 提交 done
                 ↓（系統攔截）
             [審查 Agent] → ✅ 通過 → 真正完成
                          ↓ ❌ 打回
             [執行 Agent] → 修正 → 再提交 → 回到審查
```
**不靠 Agent 記得要 review，系統強制攔截轉手，循環直到通過。**

真實案例：財務月結——帳務 Agent 出對帳報告 → 稽核 Agent 發現少憑證 → 打回 → 補完 → 再審。製造業品管——產線異常 Agent 寫報告 → 品管主管 Agent 審核 → 有問題退回重寫 → 迴圈直到品質符合。

課堂問法：「你們有沒有哪個流程，一定要過兩關才能出去？那就是 Peer Review Loop。」

---

#### 模式 7：Guardian Agent 監控者
```
[Agent 1] [Agent 2] [Agent 3]（各自工作）
         ↑   ↑   ↑
    [Guardian Agent]（24 小時監控所有 agent 行為）
         ↓ 發現異常
    自動隔離 + 通報人類
```
**一個 agent 的任務只有一件事：盯著其他 agent，防止出包、越權、錯誤。**

真實案例：ServiceNow AI Control Tower——獨立合規/風險 Agent 監看全公司所有 AI 工作流，一旦偵測到合規風險或異常行為，主動隔離並通知管理層。Gartner 預測：2028 年 40% 的 CIO 都會部署 Guardian Agent。

課堂問法：「你把 5 個 agent 同時派出去工作，你怎麼知道他們有沒有亂來？答案就是再派一個 Guardian。」

---

#### 模式 8：Silo Independence 各管各的
```
[客服 Agent]   [退款 Agent]   [調查 Agent]
   （獨立）        （獨立）        （獨立）
  不互相溝通，各自擁有完整的業務線
```
**多個 agent 完全不交流，每個人各自負責一整條業務流程。**

真實案例：N26 數位銀行——客服 Agent（5 語言 24 小時）、退款處理 Agent（翻譯 + 分析索賠文件）、金融犯罪調查 Agent（草擬調查報告）三條線完全獨立，共 15+ 個 agent，整體自動化率達 70%。

課堂問法：「如果你的業務部門彼此完全不需要溝通，各自跑各自的——那就可以用 Silo，最好部署最少互依賴。」

---

#### 模式 9：Closed-Loop Self-Correction 自我修正
```
[Agent 執行] → 測試失敗 → 自動分析錯誤 → 修正 → 再測試
     ↑_______________________________________________|
     直到成功，不找人，自己跑完整個修正迴圈
```
**Agent 自己執行、自己測試、自己找錯、自己修正，人類只看最後結果。**

真實案例：Palantir AI FDE——資料倉儲遷移，Agent 寫轉換腳本 → 執行 → 抓到錯誤 → 自動重寫 → 再跑 → 迴圈。原本需要 2 年的工作，壓縮到 5 天。

課堂問法：「你有沒有哪種工作，失敗了就要一直重試改參數？這種最適合自我修正迴圈。」

---

#### 模式 10：Human Co-Pilot 人主機副
```
[人類決策者] ←→ [Agent 做記憶/調閱/整理]
   人發號施令，Agent 擴充記憶與搜尋範圍
   最終判斷在人，Agent 是「超強外掛腦」
```
**人類是主角，Agent 是輔助者。Agent 做的是「記住跨文件脈絡 + 快速查閱 + 整理」。**

真實案例：NBIM 挪威主權基金——分析師主導 ESG 研究，AI Agent 跨 9000 家公司的文件維持長時間 context，讓分析師不用自己找資料、不用重複閱讀，每週省下 20% 工時。

課堂問法：「你有沒有需要長期追蹤大量文件的工作？不是要 AI 幫你決定，只是要它幫你記得？那就是 Co-Pilot 模式。」

---

#### 模式 11：Decentralized Swarm 去中心群體
```
[Node A] ←→ [Node B] ←→ [Node C]
   ↕              ↕              ↕
[Node D] ←→ [Node E] ←→ [Node F]
   各節點自主決策 + 互相協商，無中央指揮
```
**沒有 orchestrator，多個 agent 各自感知局部環境，互相協商，共同達成目標。**

真實案例：Google DeepMind + Duke Energy 智慧電網——各節點 Agent 監控當地電力供需，偵測故障後去中心化協商重新路由電力，防止大規模停電。適合「太大、太快、中央算不過來」的場景。

課堂問法：（進階，一般班可跳過）「當你的規模大到一個中央 orchestrator 處理不完，才考慮 Swarm。這是 AI agent 的終極形態，但也最難控制。」

---

**11 種模式速查表（課堂發的參考卡）**

| # | 模式 | 核心結構 | 最適合的 ops 場景 | 人類參與度 |
|---|------|---------|-----------------|-----------|
| 1 | Sequential Pipeline | A→B→C→D | 採購審核、合約簽核 | 低（全自動） |
| 2 | Hub-and-Spoke | 中央+多專家 | 跨系統報表、客戶詢問 | 中 |
| 3 | Parallel Broadcast | 一觸發多線 | 入職流程、緊急通報 | 低 |
| 4 | Event-Driven | 異常才醒 | KPI 監控、庫存警報 | 中（接通報） |
| 5 | Human Gate | 關卡等人 | 法規合規、高額審批 | **高（必須）** |
| 6 | Peer Review Loop | 提交→審→退→改 | 財務對帳、品管報告 | 中 |
| 7 | Guardian | 監控其他 agent | 風控、合規稽核 | 低 |
| 8 | Silo Independence | 各跑各的 | 獨立部門流程 | 低 |
| 9 | Closed-Loop | 自測自修 | 資料處理、腳本執行 | **極低** |
| 10 | Human Co-Pilot | 人主 AI 副 | 研究分析、長文件追蹤 | **高（人主導）** |
| 11 | Decentralized Swarm | 無中心協商 | 大規模分散式決策 | 極低（進階） |

---

### 待收清單（claude-code-deck 專案內已存在的 md）

- `WORKING_MEMORY.md` — 內有「桌面玩法 6 步」、「12 條上機前挑戰」、「翻譯層類比清單」、「卡牌正反面設計」等多段教學設計線索，待 Jimmy 指示後逐段收進
- `claude-code-deck-design.md` — v0.1 三層結構（工具 / 場景 / 心法）+ 工作坊操作流程 5 步
- `claude-code-knowledge-100.md` — 知識點，非教學設計（不收）
- `pain-points-100.md` — 痛點素材，非教學設計（不收）
- `use-cases-35.md` — 含「Use Case 自然展開後就是工作流」、「進工作坊個案實戰卡 10 個候選」等設計觀察

### [2026-05-26] Cadbury 5 Star "Make AI Mediocre Again" — 課堂開場引子（指令品質破冰）

**來源**：Cadbury 5 Star 廣告活動（2025）
**影片搜尋關鍵字**：`Cadbury 5 Star Make AI Mediocre Again`
**TrendHunter 介紹**：https://www.trendhunter.com/trends/make-ai-mediocre-again

**廣告原意**：諷刺 AI 炫耀文化——Cadbury 設立「垃圾資料農場」主動餵給 AI 訓練資料庫廢話，宣稱要讓 AI「再次平庸」，鼓吹慢生活與不完美。

**Jimmy 的課堂 Reframe**（核心教學轉折）：

> 廣告說的是外部破壞 AI。但真正讓 AI 平庸的，是你自己每次下了爛指令。
> **你下什麼水準的指令，AI 就給你什麼水準的輸出。**
> 不需要有人來「Make AI Mediocre Again」——你自己就在做這件事。

**教學設計性質**：開場破冰 × 認知衝擊 × 指令品質引入

---

#### 課堂播放流程（建議時序）

```
① 播放廣告（60–90 秒）— 讓學員笑完
② 講師問：「他們要做什麼？」→ 學員：「讓 AI 輸出爛東西」
③ 講師反問：「你上週用 AI，結果讓你滿意嗎？」
   → 等待沉默 3 秒（關鍵時刻）
④ 講師：「讓 AI 平庸的，不是 Cadbury，是你自己給的指令。」
⑤ 帶出核心概念：
   「AI 的上限，是你指令的上限。
    AI 幕僚指揮官的價值，不是會用 AI，是會下最高標準的指令。」
```

**媒介備注**：若當天找不到原版影片，可用標題 + 概念口頭描述替代，效果同樣有力。

---

#### 教學轉接語（講師手冊可直用）

> 「Make AI Mediocre Again」這個廣告是在嘲笑 AI 文化。
> 但今天我們要翻轉它：**「Make AI Great Again」的方法只有一個——你學會下指令。**
> 這就是今天你要帶走的事。

---

#### 可套用情境

| 位置 | 用途 |
|------|------|
| **S1 開場 5–8 分鐘** | 破冰 + 引出「指令品質」主題，取代枯燥自我介紹 |
| **Prompt 設計單元前** | 進入「如何下高標準指令」之前的認知預熱 |
| **Agent 協作單元** | 「你不給清楚任務，agent 團隊只會亂跑」的起手式 |

---

#### 延伸討論問句（可選）

- 「你覺得你自己的 AI 指令，平均幾分（1–10）？」
- 「你上次讓 AI 重做超過 3 次的任務是什麼？是 AI 的問題，還是指令的問題？」

---

### 待收清單（其他專案的可借鏡片段）

- `agents/教學設計師/memory/LOVE-SLJM-teaching-methods.md` — 28 種教學法分類框架（主動/被動 × 吸收/沉浸）
- `agents/教學設計師/memory/教學產出分級標準.md` — L0-L7 八層
- `agents/教學設計師/memory/教學設計原理.md` — Knowles / Bloom / Kolb / Tuckman / SCARF / ADDIE / Kirkpatrick
- `agents/教學設計師/memory/團體活動帶領實務.md` — 課室動力 / SPECTRUM/SAP / PA50
- `agents/教學設計師/memory/教材設計原則.md` — 8 種投影片類型 / 視覺化決策樹
- 各客戶案的工作坊腳本（台水 / 商周 / 南亞 / 華城）— 已驗證的引導問句 / 帶領動作

---

<a id="e"></a>
## E. 競品 / 市場 / 定價（已搬遷）

→ 完整內容（30 家中文盤點 + 英文圈 15 家 + 標竿深挖 5 家 + 台灣 multi-agent 公開課定價 13 家 + 智谷戰略結論）已搬至獨立檔 [`competitor.md`](competitor.md)。

**分工**：
- 本檔（instruction-design.md）= **教學設計法庫**（A-D 區）
- competitor.md = **市場 / 競品 / 定價庫**

---

## 📅 更動紀錄

### 2026-05-26
- **Cadbury "Make AI Mediocre Again"**：D 區新增影片教學導入設計，含 Jimmy reframe（「讓 AI 平庸的是你自己的爛指令」）、完整課堂播放流程、三個可套用情境、講師手冊轉接語

### 2026-05-24
- **Batch A 官方文件**：D 區新增 4 個 Anthropic 官方機制（CLAUDE.md / Subagents / Hooks / Agent Teams），含四層學習梯度整理
- **Batch C 工具比較**：D 區新增 Claude Code vs ChatGPT/Cursor/Copilot 比較 + MCP 生態系數據（10,000+ servers）
- **Batch D 成熟度模型**：D 區新增 5 個框架（Kellogg 4-Stage / Salesforce / ServiceNow / HyScaler / Kore.ai），含三框架課堂組合建議
- **Batch B 企業案例**：D 區新增 4 個實戰個案（ai-c-suite / AI Chief of Staff / CFO+Xero MCP / HumanLayer CLAUDE.md 指南），含課堂引用建議與智谷卡牌對應點

### 2026-05-19
- **Clear cut（夜）**：E 區內容全段搬遷至 `competitor.md`（single source of truth），本檔 E 區僅留 pointer。檔案分工乾淨：教學法 vs 競品定價。
- **第三次更新（晚）**：E 區增建 — 台灣繁中市場競品掃描（已搬遷至 competitor.md）
- **第二次更新**：A 區補完 + 目錄校準
- **建檔（傍晚）**：A 區 9 個來源 + B 區 3 個借鏡案例 + C 區差異化盤點 + D 區待收結構
