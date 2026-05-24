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

### 待收清單（claude-code-deck 專案內已存在的 md）

- `WORKING_MEMORY.md` — 內有「桌面玩法 6 步」、「12 條上機前挑戰」、「翻譯層類比清單」、「卡牌正反面設計」等多段教學設計線索，待 Jimmy 指示後逐段收進
- `claude-code-deck-design.md` — v0.1 三層結構（工具 / 場景 / 心法）+ 工作坊操作流程 5 步
- `claude-code-knowledge-100.md` — 知識點，非教學設計（不收）
- `pain-points-100.md` — 痛點素材，非教學設計（不收）
- `use-cases-35.md` — 含「Use Case 自然展開後就是工作流」、「進工作坊個案實戰卡 10 個候選」等設計觀察

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

### 2026-05-24
- **Batch B 企業案例**：D 區新增 4 個實戰個案（ai-c-suite / AI Chief of Staff / CFO+Xero MCP / HumanLayer CLAUDE.md 指南），含課堂引用建議與智谷卡牌對應點

### 2026-05-19
- **Clear cut（夜）**：E 區內容全段搬遷至 `competitor.md`（single source of truth），本檔 E 區僅留 pointer。檔案分工乾淨：教學法 vs 競品定價。
- **第三次更新（晚）**：E 區增建 — 台灣繁中市場競品掃描（已搬遷至 competitor.md）
- **第二次更新**：A 區補完 + 目錄校準
- **建檔（傍晚）**：A 區 9 個來源 + B 區 3 個借鏡案例 + C 區差異化盤點 + D 區待收結構
