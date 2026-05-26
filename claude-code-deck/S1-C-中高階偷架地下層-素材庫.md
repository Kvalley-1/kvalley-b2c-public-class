# S1-C：中高階主管偷架 Agent Team 案例庫（地下層）

> **用途**：B2C 公開班 Section 1「老闆要佔住哪一層」的「地下層 / 同行壓力」結構 C，**也是 S2.1「好的 AGT TEAM 指揮範例」的主要素材**。
> **建立**：2026-05-26（sub-agent 平行 web 深挖；20+ 來源驗證；NotebookLM deep research 補強仍在跑，預計 18:00 出爐再合併）
> **狀態**：素材厚版（尚未進教案 L3）

---

## Part A：半公開人物的真實 stack 細節（9 位）

### 1. Garry Tan — Y Combinator President & CEO
**Stack**：開源 `gstack`（github.com/garrytan/gstack），把 Claude Code 包成 23 個 slash command，每個 command 等於一個「組織角色」：CEO/Founder（`/office-hours`、`/plan-ceo-review`）、Eng Manager（`/plan-eng-review`）、Designer（`/plan-design-review`）、Staff Engineer（`/review`）、QA Lead（`/qa`）、Release Engineer（`/ship`）、Security Officer（`/cso`）、Debugger（`/investigate`）、Technical Writer（`/document-release`）、Retro Facilitator（`/retro`）等。流程是 think → plan → build → review → test → ship → reflect，每個 skill output 餵下一個。
**組織腦概念**：跨職能 hand-off、process 治理（避免 chaos）、role separation、parallel execution。
**金句**：
> "The point isn't who typed it, it's what shipped." — Garry Tan, gstack README
> "Ten agents is ten sources of chaos. With a process … each agent knows exactly what to do and when to stop."
> 自報「過去 60 天 3 個 production service、40+ feature、part-time 同時跑 YC，2026 run rate 約是 2013 年的 810 倍程式碼產出。」
**來源**：https://github.com/garrytan/gstack ; https://news.ycombinator.com/item?id=47418576 ; https://www.ycombinator.com/library/OW-inside-garry-tan-s-ai-coding-setup

### 2. Lenny Rachitsky — 前 Airbnb PM lead, Lenny's Newsletter（260K 訂閱）
**Stack**：自報「**9 個 AI agent 跑我的工作和生活**」；公開推 Tal Raviv 的「Personal AI Copilot」三件套（Projects + project knowledge + custom instructions），覆蓋 ChatGPT/Claude/Gemini/M365 Copilot。長期專訪 Claire Vo（9 agent on 3 Mac Mini）、Wade Foster（Zapier CEO）、Michael Leibovich（Adobe GM）三人完整 stack。
**組織腦概念**：copilot onboarding（像新員工要 onboard）、role-based instructions、knowledge base 當 shared context。
**金句**：
> "Lenny built a team of 9 AI agents that run his work and life."
> Tal Raviv: "Use instructions to set your copilot's role, personality, and behaviors … fill out the project knowledge with company and org-level documents that act as shared context."
**來源**：https://www.lennysnewsletter.com/p/build-your-personal-ai-copilot ; https://x.com/lennysan/status/1948121027571318973

### 3. Claire Vo — 三度 CPO、ChatPRD 創辦人（半地下→公開）
**Stack**：**9 個 OpenClaw agent，跑在 3 台 Mac Mini 上**，外加 Obsidian 當記憶/知識庫、Loom 做 transcription。9 個 agent 各有名字、角色：
- **Polly** — 工作 Chief of Staff / EA
- **Finn** — 家庭 & 家務 manager（**獨立 Mac Mini 跟工作隔離**）
- **Sam** — proactive SDR（每天掃 CRM、Exa people search、寫 outreach）
- **Howie** — Podcast producer & 研究助理
- **Sage** — 線上課程 project manager
- **Q** — 小孩功課輔導
- Max / Kelly / Holly

**組織腦概念**：data boundary（work vs family 物理隔離）、agent specialization、span of control（一個人管 9 個 24/7 agent）、把過去 10 hr/週的 contractor 工作 outsource 給 Sam。
**金句**：
> Vo 描述 OpenClaw 是「我自 ChatGPT 之後最重要的 AI 體驗。」
> 第一次裝 OpenClaw 它「把我家庭行事曆全清掉了」，她還是堅持下去 → 轉信徒。
**來源**：https://www.lennysnewsletter.com/p/openclaw-the-complete-guide-to-building ; https://www.lennysnewsletter.com/p/how-openclaw-changed-my-life-claire-vo ; https://finance.biggo.com/podcast/4b5de34271d86f70

### 4. Wade Foster — Zapier CEO & 共同創辦人
**Stack**：Zapier (Zaps / AI by Zapier / Agents / Tables / Interfaces) + Granola（會議 transcript）+ Grok（人才挖角）+ Cursor（個人腳本）+ MCP。**有一隻名叫「Scout」的 agent**——每週讀他的 Gmail、Granola notes、Slack、Calendar、Cursor transcripts，找自動化機會。
**組織腦概念**：「small, focused agent for one specific task」（窄 scope 才好用）、agent fleet 治理、approval workflow。
**金句**：
> "I get about 100 emails and it gives me 10 to look at." — Wade Foster
> "Build small, focused agents for one specific task." 他用 Granola 做企業文化 transcript 萃取，再給 agent 評估面試候選人。
**來源**：https://www.lennysnewsletter.com/p/zapiers-ceo-shares-his-personal-ai-stack ; https://zapier.com/blog/humans-managing-agent-teams/

### 5. Tyler Cowen — 經濟學家、Marginal Revolution（半公開的 stack 細節最完整）
**Stack**：o1 Pro（podcast prep、reliably 深度 research）+ Claude（philosophical writing、graph 視覺化）+ DeepSeek（替代閱讀）。**「把整疊書換成 LLM」**——以前每月買 20-30 本書，現在「拷問」LLM。
**組織腦概念**：tool specialization by use-case、不用 AI 寫 draft（保留 voice）但用 AI 評論 draft、AI 是「main secondary source」。
**金句**：
> "Claude is a wonderful mix of thoughtful, philosophical, dreamy, flexible, versatile—it's the best writer."
> "ChatGPT is better for tables, but Claude is really good for graphs."
**來源**：https://linesofdefence.com/note/how-tyler-cowen-uses-ai-2025/ ; https://every.to/podcast/economist-tyler-cowen-on-how-chatgpt-is-changing-your-job

### 6. Aaron Levie — Box CEO
**Stack**：刻意「model-agnostic」——同時用 Claude 和 ChatGPT（在 Box AI 平台），把合約丟進 GPT-4 抓法律錯誤、用 Box AI 自寫 PRD、訓練業務新人。
**組織腦概念**：avoid lock-in、agent workflow design 是「企業科技最高槓桿技能」。
**金句**：
> "Agent workflow design is the highest-leverage skill in enterprise tech right now." — Levie
> 「在最 agentic 的系統（如 Claude Code）裡，總有一刻 context window 跑完，model 就做不出好決策。」
**來源**：https://techcrunch.com/2025/09/11/box-ceo-aaron-levie-on-ais-era-of-context/ ; https://every.to/podcast/transcript-box-ceo-aaron-levie-on-why-ai-agents-won-t-take-your-job

### 7. Brian Balfour — Reforge CEO
**Stack**：Reforge 內部「Build Agent」（Slack-native，描述要做什麼 → prototype 回傳 thread）+「Discovery Agent」（建之前先問清楚），分成 4-7 人 squad，40 人 / 5 個產品同時跑。
**組織腦概念**：AI-Native squad、避免「Frankenstein workflows」、shipping vs learning balance。
**金句**：
> 「9 個月內 ship 5 個 AI 產品 with just 25 people」——squad 結構讓他們能快速 ship。
**來源**：https://blog.brianbalfour.com/p/ai-native-product-teams-how-they ; https://suprainsider.substack.com/p/84-how-reforge-launched-5-ai-products

### 8. Sam Lessin — Slow Ventures GP / Fin 創辦人
**Stack**：async email worker、photo AI、email-to-action pipeline；推 human-in-the-loop（不全自動）。文件在 wlessin.com/tools（需登入，刻意半私）。
**組織腦概念**：knowledge work instrumentation、human-AI 分工。
**來源**：https://wlessin.com/

### 9. David Sacks — Craft Ventures GP / 美國 AI Czar
**Stack**：與 Justin Reidy 合提「The AI Simple Stack」概念（model + vector DB + retrieval = 每個員工自己的 personal AI assistant）；自己創 Glue（從 Slack/Zoom 對話 invoke AI）。
**組織腦概念**：把 AI assistant 當 employee equipment，不是 tool。
**來源**：https://www.craftventures.com/team/david-sacks

---

## Part B：匿名 / 半地下案例（12 個）

### B1. Michael Leibovich — Adobe GM, Behance + Adobe Portfolio
**身份**：Adobe 商務單位主管，**非工程背景**，paternity leave 期間建出 chief of staff。
**Stack**：純 Claude Code + 資料夾 + Markdown 檔。三層架構：(1) **Identity Context** — 寫他自己的 mental model、價值觀、什麼讓他「stop reading」；(2) **People File** — 每個碰過面的人一檔，自動 update；(3) **Market Intelligence digest** — 每週自動跑、依他定義的策略優先序過濾訊號。
**關鍵設計**：「Claude reads it at the start of every session.」（每 session 都重 load identity）
**為什麼**：「把 Claude Code 變成 personal operating system，用的是組織共享雲端硬碟的技能。」
**來源**：https://michaelleibovich.substack.com/p/how-i-built-my-ai-chief-of-staff

### B2. Doneyli De Jesus — Snowflake Principal Solutions Engineer / Substack「Signal Over Noise」
**身份**：Principal Solutions Engineer（資深個人貢獻者，非經理），但管 18 個個人專案像管組織。
**Stack**：自架的 **head-of-ai** repo（已開源 head-of-ai-template）：
- `portfolio.yaml` — 18 個 project 分 Tier 1/2/3（revenue / product bet / infra）
- **Personal Control Plane** — 4 層：Registry、Scoring、Dispatch、Scope（162 行 YAML）
- Dispatch + Scope hook + Vacation mode + Cost ceiling 連 Langfuse
- **24/7 跑在 Mac Studio 上**
- 子系統：AI Chief of Staff（7 agent）、Local Infra（9 agent）、Content & Research（10 agent）
**組織腦**：明確 portfolio prioritization、「from 114 things, which 5 should run tonight while I sleep?」
**來源**：https://doneyli.substack.com/p/i-hired-a-head-of-ai-to-run-my-agents ; https://doneyli.substack.com/p/i-built-an-ai-chief-of-staff-that

### B3. Barbara Bermes — Engineering 主管
**身份**：Medium 上自述「為什麼你也想要 chief of staff」
**Stack**：Claude Cowork 10 分鐘快速架；session memory、mental models、people file（自動從會議 transcript 更新）、knowledge graph（隨時間長大）。
**為什麼半隱身**：以「10-minute quickstart」框架介紹，強調**任何 non-coder 都能架**——暗示這正是低調入門點。
**來源**：https://bbinto.medium.com/building-my-own-ai-chief-of-staff-and-why-you-might-want-one-too-7e862a052a85

### B4. Cesar R.G. — 個人 chief of staff（半匿名 personal blog）
**Stack**：Claude Code + folder structure，重點在 session 之間的 continuity，每週 digest 跑在 schedule 上。
**來源**：https://www.cesarrg.com/how-i-built-my-ai-chief-of-staff/

### B5. Alex Honchar — Neurons Lab Co-founder
**Stack**：Claude Code 為中樞，三層整合：
1. claude.ai/settings/integrations 內建 connector
2. **Native MCP**：Google MCP / Slack / Notion / Apple Notes / Remarkable / 自己寫的 Rize connector
3. **Chrome Extension** 處理沒 MCP 的 LinkedIn / WhatsApp / X / Instagram / Telegram
**金句**：「skills for my Claude Chief of Staff 會放在一個 'work' plugin 裡，work 是獨立的人生範疇。」（人生模組化）
**來源**：https://medium.com/data-science-collective/claude-code-for-life-2-a-personal-ai-chief-of-staff-for-daily-work-357b6c35573f

### B6. razbakov（DEV Community）— 一人 15 個 side project
**Stack**：「Executive Team of 6 AI Agents」 manage 15 side projects。每個 agent 有自己的 domain、personality、skill set。橫跨 code review / content / strategy / coaching / community。
**來源**：https://dev.to/razbakov/i-built-an-executive-team-of-6-ai-agents-to-manage-my-15-side-projects-4k0i

### B7. Liam Darmody（GitHub Gist）— 非技術用戶 24/7 personal agent guide
**身份**：明標「Step-by-step guide for **non-technical users**」
**Stack**：Mac Mini + Claude Code，always-on，每天定時自動跑 task。
**來源**：https://gist.github.com/liamdarmody/4aba083c26ccb1b3b0f1068ec185ef66

### B8. Peter Steinberger — 退休 iOS 工程師（PSPDFKit 創辦人）→ Clawdbot
**Stack**：Vienna 寫 2025 workflow 改造文，自承「The most profound change this year is that I almost never read code anymore.」開源 Clawdbot 24/7 個人 AI（locally running，permanent memory）。直接帶起 Silicon Valley Mac Mini 賣到斷貨。
**來源**：https://eu.36kr.com/en/p/3655411080568966 ; https://www.bloomberg.com/news/articles/2026-05-11/why-claude-ai-agents-are-driving-record-mac-mini-demand

### B9. Nabila Ismail（Substack）— solo business owner
**標題就是**：「I run My Entire Business Alone. How I'm Using AI to Be The Team I Never Hired.」 220K+ follower 個人品牌、旅遊社群、多個產品全靠 AI agent 跑營運。
**來源**：https://thenabilaismail.substack.com/p/i-run-my-entire-business-alone-because

### B10. 「26 agent on 2022 MacBook Pro」匿名 Substack 作者
**Stack**：repurposed 2022 MacBook Pro + launchd + Docker + Python + Claude Max，跑 26 個 agent。屬於明顯**怕同事知道**的 setup——舊筆電當 home server，不過公司 IT。
**來源**：https://excellentprompts.substack.com/p/ai-agent-stack-mcp-canvas（引用）

### B11. HN Show HN 系列（多個匿名）
- **Nerve**（Dec 2025）：「AI Chief of Staff that does your actual work」
- **HNSignals**（Jan 2026）：「a Chief of Staff who reads the entire thread for you and hands you a one-page executive brief」
- 其他「I built an AI chief of staff to stop drowning in email and meetings」
**用途**：經理人想處理 email/會議淹沒，自己默默架。
**來源**：https://news.ycombinator.com/item?id=46137854 ; https://news.ycombinator.com/item?id=46765448 ; https://news.ycombinator.com/item?id=44401674

### B12. The Digital Runway（匿名 Substack）— 「8 Roles + 15 Tools = My AI Tech Stack」
作者自定義 8 個 agent role（不只是 prompt，是「organizational role」），跨 15 個工具串起來。屬於完整的「組織腦」搬到 AI agent 設計。
**來源**：https://thedigitalrunway.substack.com/p/whats-in-my-ai-tech-stack

---

## Part C：中文圈案例（5 個）

### C1. B 站 30 集系列：「我用 Claude Code 給我的一人公司搭了 11 人 AI 團隊」
**身份**：一人公司老闆，**用中文公開連載 30 集**（這在華語圈非常罕見，多數華人創業者只在小圈內分享）。
**Stack**：Claude Code + orchestrator 串 11 個 agent 跑 11 階段，47 秒內 4 個功能上線實測。
**組織腦**：把研發團隊（PM、設計、工程、QA、Ops）全擬人化成 agent，老闆只下需求。
**來源**：https://www.bilibili.com/video/BV1pFRgBvEgT/

### C2. V2EX 開發者 Elvis — 「一人軍團」實戰手冊
**Stack**：Codex + Claude Code + orchestrator，把多個 coding agent 串起來，自己變「**提需求的人**而不是寫代碼的人」（這句話對中高管最有共鳴——他們本來就只下需求）。
**來源**：https://zhuanlan.zhihu.com/p/2009932247780836380

### C3. 即刻 App — Claude Cowork 討論社群
即刻上多位產品經理、創業者分享 Claude Cowork 是「超級同事」、「智能空間」、「無限自主性」。但**完整 stack 細節通常只在私訊或付費社群裡分享**（典型半地下）。
**來源**：https://m.okjike.com/originalPosts/6965c1e8cc10407bef8505de

### C4. 知乎付費專欄 — Claude Code Agent Teams 完整上手攻略
**Stack 共識**：Team Lead 模式（主 session 用 TeamCreate / Task / SendMessage），按 Shift+Tab 切到 delegate 模式強制只管不寫。**完美對應「主管/高管」工作場景**——只指揮、不執行。
**來源**：https://zhuanlan.zhihu.com/p/2004878637753730888 ; https://zhuanlan.zhihu.com/p/2004486603343671752

### C5. 騰訊雲開發者社群 — 「一個人就是一個團隊」深度教學
**標題即定位**——個人變團隊。教 PM / 全棧 / QA / DevOps 四角色 agent 分工。
**來源**：https://cloud.tencent.com/developer/article/2631985

---

## Part D：3 條「為什麼保密」的精彩 quote / 案例（直接用在 S1「地下層」）

### D1. Fortune 報導：員工偷用 AI 為的就是 secret advantage
> "Nearly one-third of workers keep their AI use a secret from their employer. The biggest reason workers choose not to disclose using the tech tool is because they want a **'secret advantage' over their peers (36%)**, while employees also fear that revealing their reliance on this technology will lead to losing their job (30%)."
**用法**：證明「他不會告訴你」是普遍現象，36% 為的是個人競爭優勢，30% 怕被當「想取代」。
**來源**：https://fortune.com/2025/05/29/employees-secretly-using-ai-hiding-bosses-secret-advantage-peers/

### D2. EY 2026 Technology Pulse Poll（500 位 tech executive）
> **「52% of department-level AI initiatives 在沒有正式批准下運作。」**
> **「93% 高管和資深經理人說自己用 shadow AI tool。」**
**用法**：地下層不是現象，是常態。中高管自己就是最大宗 shadow user。
**來源**：https://www.cio.com/article/4083473/shadow-ai-the-hidden-agents-beyond-traditional-governance/ ; https://www.secondtalent.com/resources/shadow-ai-stats/

### D3. Garry Tan 在 gstack README 的潛台詞
> 「Ten agents is ten sources of chaos. With a process … each agent knows exactly what to do and when to stop.」
**用法**：這句話對著「想學的中高管」是一記 hook ——他們最害怕的不是 AI，是失控。Garry Tan（YC CEO）親口說：**有組織腦的人，agent 才不會變混亂**。這就是「為什麼你的下屬學不會，但你會」。
**來源**：https://github.com/garrytan/gstack

---

## Part E：🎯 對「智谷 B2C 公開班學員」最有共鳴的 8 個案例小傳

**學員輪廓**：台灣 30-55 歲中小企業老闆 / 部門主管，業務/行銷/營運/HR/財務出身，**不是工程師**。挑「角色 / 規模 / 痛點」最對應的案例。**這是 S2.1「好的 AGT TEAM 指揮範例」的核心素材庫。**

### E1. Adobe GM Michael Leibovich（**最對應「部門主管」**）
40 歲商務單位主管（非工程），**用 paternity leave 自己一個人架出 chief of staff**。Stack 是「資料夾 + Markdown 檔」就這麼簡單——這正是給「不會寫程式但會用 Google Drive / Notion 的部門主管」最直接的證明。他建了一個「People File」每個會面者一檔自動 update——這對台灣業務主管管客戶關係、HR 主管管下屬，**完全可以照抄**。
> **講課切入點**：「他不寫 code、不是工程師，他用的就是各位都會的『建資料夾、寫 markdown』，但他每週讓 AI 自動跑出市場情報 digest——你的競爭對手已經在這樣管自己的部門了。」

### E2. Claire Vo（**最對應「身兼數職的女性老闆/主管」**）
3 度 CPO + 創業者 + 媽媽，9 個 agent 跨工作家庭，工作 agent 跟家庭 agent **物理隔離在不同 Mac Mini**——這對台灣女性主管（30-50 歲被工作家庭兩頭燒）超有共鳴。她的 Sam（SDR agent）取代過去每週 10 hr / 月幾萬的 contractor。
> **講課切入點**：「她每週省下 10 小時、原本付給人的錢，現在給一台 Mac Mini。你的 saas / 業務出身的學員一聽就懂這筆帳。」

### E3. razbakov 一人 15 個 side project（**最對應「中小企業老闆」**）
一個人用 6 個 AI agent 管 15 個專案——這是台灣中小企業老闆的真實人生（一個老闆同時管業務、製造、會計、行銷、人事、廠務 6 條線）。
> **講課切入點**：「你不需要 6 個經理，你需要 6 個 agent + 一張對的指揮圖。razbakov 就是這樣做的。」

### E4. Doneyli De Jesus 的「Personal Control Plane」（**最對應「想系統化的主管」**）
他不是經理，但用了一套「**從 114 件可能的事，今晚我睡覺時跑哪 5 件最該跑？**」的決策框架——這就是台灣中小企業主每天早上煩的事。他把它 codify 成 YAML、自動跑。
> **講課切入點**：「你每天早上花 30 分鐘排今日工作？他用 YAML 寫一次，AI 每晚自動排好給他看。」

### E5. Wade Foster 的 Scout agent（**最對應「業務出身老闆」**）
Zapier CEO 養了一隻 agent 名叫 Scout，**每週讀他自己的 Gmail、會議筆記、Slack、行事曆**，找下週可以自動化的事。台灣業務主管最痛點就是「我的時間被會議和 email 吃掉，沒空看大局」。
> **講課切入點**：「Scout 不取代你，它幫你看你自己看不見的時間黑洞。每個學員回家當天就能架。」

### E6. B 站「一人公司 11 人 AI 團隊」連載（**最對應「準備創業 / 接班的中階主管」**）
**中文、華人、一人公司**，30 集連載手把手教——這對台灣聽眾沒有語言/文化隔閡。Stack 是 Claude Code + orchestrator + 11 個 agent 分工，**47 秒上線 4 個功能**。
> **講課切入點**：「不需要看英文資料，B 站有人在做華人一人公司 11 人 AI 團隊。你的 30 歲下屬可能已經偷偷在學了。」

### E7. Peter Steinberger（PSPDFKit 創辦人退休）的 Clawdbot（**最對應「快 50 歲想轉型的老闆」**）
他退休之後用 Mac Mini 跑 24/7 personal AI，直接帶起 Silicon Valley Mac Mini 賣到斷貨。**他不是為了工作，是為了過更好的生活**——這對 40-55 歲台灣老闆「想退、想輕、想自由」直擊。
> **講課切入點**：「他退休了，但他比上班的時候做的事更多。他用一台 Mac Mini 跑 24 小時 AI 員工——這不是科技問題，是生活設計問題。」

### E8. EY 2026 Survey + Fortune 報導的「shadow AI 統計」（**最對應「焦慮的中階主管」**）
不是案例，是**警鐘**。給學員的衝擊：93% 高管已經偷用、52% 部門 AI 計畫沒批准、36% 員工為了 secret advantage 不告訴老闆。
> **講課切入點**：「你問你下屬有沒有用 AI？他說『偶爾用一下 ChatGPT』。**真實數字是 93%**。他不是沒在用，是不告訴你。今天課程結束你回去，要嘛你也學會自己架一套，要嘛你是辦公室裡唯一沒架的人。」

---

## 對 S2.1「HOW TO BECOME U」+「互動 HTML 產 CLAUDE.md」的設計啟發

從案例提煉出**「好 agent team 指揮範例」的 5 個共通元素**（可直接做成 S2.1 教學活動的盤點欄位）：

1. **Identity / 你是誰**（Leibovich 的 Identity Context、Cowen 的 "voice"）
   — 寫下你做決定的 mental model、什麼讓你 stop reading / 立刻 reply
2. **People / 你關心誰**（Leibovich People File、Vo 的家庭/工作隔離）
   — 列你的客戶、下屬、合作夥伴前 N 名 + 每位的偏好/禁忌
3. **Mission / 你的優先序**（Doneyli portfolio.yaml）
   — 你的 Tier 1 / 2 / 3 — 什麼絕對要做、什麼可以放手
4. **Trigger / 什麼時候啟動**（Wade Foster Scout 每週掃、Leibovich 每週 digest）
   — 每天/每週/事件觸發 — agent 主動 vs 被動
5. **Boundary / 邊界**（Vo 物理隔離、Doneyli vacation mode、Levie human-in-the-loop）
   — 哪些事絕對不能碰、哪些事要先問再做

→ **互動 HTML 設計建議**：5 個欄位填空 → 即時生成 CLAUDE.md（每個欄位學員邊填邊看 markdown 即時更新）

---

## 主要 Sources（核心）

- [Garry Tan gstack](https://github.com/garrytan/gstack) / [HN discussion](https://news.ycombinator.com/item?id=47418576)
- [Michael Leibovich AI Chief of Staff](https://michaelleibovich.substack.com/p/how-i-built-my-ai-chief-of-staff)
- [Claire Vo OpenClaw guide on Lenny's](https://www.lennysnewsletter.com/p/openclaw-the-complete-guide-to-building)
- [Wade Foster on Lenny's](https://www.lennysnewsletter.com/p/zapiers-ceo-shares-his-personal-ai-stack)
- [Tal Raviv Personal AI Copilot](https://www.lennysnewsletter.com/p/build-your-personal-ai-copilot)
- [Tyler Cowen AI usage 2025](https://linesofdefence.com/note/how-tyler-cowen-uses-ai-2025/)
- [Aaron Levie / Box](https://techcrunch.com/2025/09/11/box-ceo-aaron-levie-on-ais-era-of-context/)
- [Brian Balfour AI-Native Product Teams](https://blog.brianbalfour.com/p/ai-native-product-teams-how-they)
- [Doneyli De Jesus Head of AI](https://doneyli.substack.com/p/i-hired-a-head-of-ai-to-run-my-agents)
- [Alex Honchar Claude Code for Life](https://medium.com/data-science-collective/claude-code-for-life-2-a-personal-ai-chief-of-staff-for-daily-work-357b6c35573f)
- [razbakov 6 agents 15 projects](https://dev.to/razbakov/i-built-an-executive-team-of-6-ai-agents-to-manage-my-15-side-projects-4k0i)
- [Liam Darmody non-technical 24/7 guide](https://gist.github.com/liamdarmody/4aba083c26ccb1b3b0f1068ec185ef66)
- [Peter Steinberger Clawdbot / Mac Mini surge](https://www.bloomberg.com/news/articles/2026-05-11/why-claude-ai-agents-are-driving-record-mac-mini-demand)
- [Fortune: Workers hide AI for secret advantage](https://fortune.com/2025/05/29/employees-secretly-using-ai-hiding-bosses-secret-advantage-peers/)
- [CIO: Shadow AI beyond governance](https://www.cio.com/article/4083473/shadow-ai-the-hidden-agents-beyond-traditional-governance/)
- [Shadow AI stats 2026](https://www.secondtalent.com/resources/shadow-ai-stats/)
- [Bilibili 一人公司 11 人 AI 團隊](https://www.bilibili.com/video/BV1pFRgBvEgT/)
- [知乎 Claude Code Agent Teams](https://zhuanlan.zhihu.com/p/2004878637753730888)
- [V2EX 一人軍團 Codex+Claude+Orchestrator](https://zhuanlan.zhihu.com/p/2009932247780836380)
