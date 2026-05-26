# Paperclip: Hire AI Agents Like Employees (Live Demo)
## 影片逐字稿

**來源**：https://www.youtube.com/watch?v=C3-4llQYT8o
**主持**：Greg（採訪者）+ Dota（Paperclip 創辦人）
**擷取日期**：2026-05-25
**說明**：逐字稿由 NotebookLM 從影片字幕擷取，為主要段落節錄，非逐句完整版本。

---

## 開場介紹

how do you turn a group of AI agents into a company that actually runs itself you know with org charts roles goals budgets and agents working around the clock 24/7 there's this project called Paperclip maybe you've seen it because it just blew up it got 30,000 GitHub stars in the last 3 weeks and it's an open-source project that's building the orchestration layer for exactly that hiring a team of AI agents so I sat down with Dota he's the creator and it's one of the first times he's publicly talked about how to use his product we broke down exactly how to use paperclip in practice and what a zero human company could actually look like using paperclip enjoy the episode.

dota is here well his AI avatar is here and we're going to be going through paperclip the viral you know what are you calling it yeah so it's a uh agent orchestrator for uh zero human companies so it's a tool that you can use to put in your ideas and uh manage a company of agents okay and by the end of this episode what.

---

## Paperclip 是什麼

...so let me talk about Paperclip so Paperclip um here I can show you this dashboard this would be the dashboard that I use to manage PaperClip itself which is pretty involved so let's take a step back so um the idea with paperclip is it is a tool for um the tagline is zero human companies now um I think that is maybe a bit aspirational i'm sure you guys have seen tools like Pulsia where you uh you you give it your credit card it creates um business ideas for you and um paperclip is designed to be have a little bit more control right now because it's designed for um work that you're really accountable for doing um the idea behind paperclip is that you're really managing your business goals so it's not you know on one end you might have something like pulsey that's totally automatic on the other hand you might...

---

## STEP 1：選擇商業點子（Idea Browser）

...nto the system so yeah Greg one of the things I thought we could do was we could go to uh your idea browser and we could look here and we could try just try to decide something from the idea browser that we could try to use uh as as a case study so I don't know what's what's one of these that you think might be a good uh a good option m if you I mean there's a few really interesting ones like I like the you tell me I'll give you two and you pick so scroll up yep so if you go down there was a finance finance app that builds money habits in 3 minutes a day okay that's one option and then the other option if you scroll down Yep the uh flight compensation recovery agent for frequent flyers both of those I think would are great ideas okay nice yeah let's try let's try a finance app that builds money habits so one of the things I noticed actually when I was testing this out if you just right-click you can copy like pretty much a good description from this more than more than this um so here w...

---

## STEP 2：建立公司名稱與第一個 Agent（CEO）

...e can come in here like what do we want to name our app we'll name it um moola moola okay great and what is this company trying to achieve right so this text box I suppose is a little small but um we'll just paste it in we'll come back and we'll look at this in a second um after you write down what you want your company to do you create your first agent so Paperclip right now um best works when it's on your local machine and especially if you already have something like Claude Code or Codeex installed i think these tools are really important for really any agent-driven entrepreneur i'm guessing pretty much everyone in your audience has at least like cloud code or codeex installed right um we recommend that you use one of these two for your CEO which would be your first agent but we do support other agent types right you can use open code which means you could use really any model that you have um on uh open router so you've probably seen open router um they have like uh what is it lead...

...erboard that kind of shows the most popular yeah the rankings they have the AI model rankings so you can use any of these models um with paperclip i think you're going to get the best results with paperclip if you use a frontier model for your CEO but then maybe for other you know tasks you can get away with a cheaper model a hot tip is Open Router actually often has free models um so there's been this Hunter Alpha model was free for a couple of weeks the step flash free so if you have work that can be accomplished by a free model right which would be sort of uh you know not all work can you can use it and and get free tokens um also the pi coding agent whatever so it basically depends on some of these existing agents um to to operate this one's actually going to run on my local machine so um we'll just go next and and do you recommend you know doing local or how how should people think about this yeah so right now um Paperclip mostly works when you run it locally we're working on...

---

## STEP 3：給 CEO 第一個任務

...doing a cloud deployment so either you can self-host it yourself um because it is open source or eventually we'll provide a hosted solution for people that want to do that um but I think local is really how most people are doing a lot everything with paperclip right now yeah cool so the first thing we want to do is uh give our agent something to do **hire your first engineer and create a hiring plan so you are the CEO you set the direction for the company hire a founding engineer write a hiring plan break the road map into concrete tasks and start delegating work** so you can edit this if you want um you know maybe your business doesn't need an engineer maybe you're um like doing marketing sales you can sort of adjust this depending on what you want that u you know having a founding engineer is helpful because almost every sort of online business needs to do a bit of coding so we'll click next here okay we've got our company our plan and uh it kicks off so what you have here is um along...

---

## STEP 4：Dashboard 與花費追蹤

...g this sidebar we've got different companies paperclip is made to run as many companies as you want to so I'm running Paperclip itself in here um I'm running Forgotten Runes from here i've got a couple other companies that I'm like you know different apps that I'm working on um and here we've got our new uh entry for the Moola company you can see right here we've got this dashboard um part of the thing with Paperclip is that it will track the monthly spend um and it tracks all of the work your agents do i mean **I built paperclip because I was uh using cloud code to build my companies and I would have 20 or 30 cla code windows open all at once and I couldn't remember what any of them were working on i would set them to run over the weekend and I'd come back and I had no idea what anyone did i couldn't remember what they were supposed to do and they had spent all my money on all their tokens my budget was busted** and I didn't know what was actually accomplished and so paperclip is desi...

---

## STEP 5：Inbox 與雇用批准

...gned to solve those problems it actually um tracks your monthly spend that you have in tokens um everything that it happens is done through issues so right now we have this first project here um and it hires our first engineer you know these things sort of take a while uh here we go we can see we've already got our founding uh our hiring plan installed so immediate hire founding engineer you know a roadmap breakdown etc etc you know what it actually is for this call doesn't really matter but you could look in here you could edit it give it feedback give it comments so um what happens in paperclip is your agents um have tasks that get created and then um they work on them i mean that's it's as simple as that right and uh Paperclip sort of orchestrates this idea that each agent uh each task can only be handled by one agent at a time so you're not going to get this kind of uh conflict of agents stepping on top of each other um okay look here we've got something in our inbox okay hire agent...

...our first engineer uh there's a request from our CEO to hire an engineer now as you get more comfortable with paperclip and how your agents are acting you can um turn this off and let your agents hire agents automatically but for sort of these like defaults we've said you know a lot of people are getting started their first time we want to approve this manually so we just approved that our CEO uh can hire his first engineer so is that sort of the big mindset shift with paperclip instead of you know thinking of jobs to be done you think of hiring agents yeah **i think one of the things instead of thinking about like the the details the goal of paperclip is that you're thinking at a higher level like you think of yourself as like the the board or and you should be talking to the CEO and saying here are high-level goals here's the MRR that we want to reach here's like what we want to achieve now I'm asking you to make a plan and institute what needs to happen**...

---

## STEP 6：工程師上工，任務即時出現

...e here we've hired this engineer and now we've got uh like five live tasks actually happening here so let's look in a bit more deeply and see what's going on so if we click on the issues you can see we've got um more issues um set up the scaffolding continuous integration do progress tracking the user off and onboarding build a core daily loop right so the agent right now is uh working on these things the engineer is um now I can see right now that the engineer is actually just working on one of these um so I might go in here and I can up the concurrency so whatever there's advanced settings in here where you could say you know run four engineers at once and it's a bit in the weeds but uh so wait going back to that because I you know I know it's the weeds but the configuration yeah like should the should we spend any time in here sure how how should we be thinking about this yeah so one of the key things that you want to be able to do with your agents is you need to configure them...

---

## STEP 7：Agent 記憶系統與 Heartbeat 設定

...with um a bit of persona so the uh paperclip right now gives you a default uh persona for your CEO so if you look here it says you know you are the CEO here's how we expect you to use memory um we use a memory system by default that just stores your memory in files um that that was designed it's it's using like the parah memory system which is like uh I think Diego Forte's invention that um this skill is from Nat Elias he runs the Felix bot um so it it it gives your your CEO a default memory now um agent memory is a really involved topic um there are a lot of different choices which I'm happy to talk about um but this is gives you a a simple default and then you give it some safety considerations right don't exfiltrate my secrets here are some other things that I want you to look at one of the key things that you want to look at is the heartbeat and here's the the the CEO's heartbeat checklist so when you think about AI agents here's a tip about using AI agents with paperclip or or an...

---

## 🎯 最重要段落：Memento 比喻（Agent 記憶的本質）

...ything um have you ever seen the movie Momento it's like of course yeah yeah so so if for people who haven't momento the momento man he wakes up every morning and he is like um really capable but he can't remember where he's at or where he's doing and he has to leave himself little notes right **your AI agents are memento man they wake up they know how to fight they know how to drive they know how to like just take care of themselves and spend money but they don't know who they are they don't know where they are they don't know what they're supposed to be doing and so what you need to do is actually write down uh you know give them little polaroids or write tattoos on their arm on what who you are and what you're supposed to be doing** and so the heartbeat basically means like when you wake up as an agent what are you supposed to do and and this gives you these instructions so so fetch agents me confirm that you who you are learn who you are um read today's plan look for your assignment...

---

## STEP 8：Heartbeat 執行步驟

...s check out the work and then break it down into tasks and extract your memory and then you're done right so these are your responsibilities i would say that um you know Paperclip has been out about 3 weeks and we are already um improving on this on a daily basis you know one of the key things that um you always have to do with your agents is you really want to set up a way to kind of evaluate the quality of the prompts that you're giving them and this is really like a new field that a lot of people haven't it hasn't been figured out yet we'll be building more tools in Paperclip for helping you do that um but really how a lot of people just do it practically is when it does something you don't like you come in here and you say rule like like make sure you remember to set you know like if if it's forgetting to set like a a win condition like **make sure you set like a success condition for every task and ask the developer uh to have QA review it** right like I might I might be using this an...

---

## STEP 9：加入 QA 角色 + Rules 改善

...d I realize he never defines what success looks like and he never asks QA to review it and I'll literally just like add that line in here and then save it and then you know typically you you'll get a bit better results which by the way I think is something that we should have our CEO do so I'm going to ask him to hire uh a QA uh person to help review the work so um that's another thing like so this is another way that you use paperclip is whenever you have an idea for something just ask the CEO knows how to use paperclip um very very well and I if you're having trouble if you want to set up a new project you want to set up you improve your organization you want to make a plan you don't you you need advice you just ask your CEO to do it um so I'll create this issue let him work on that another key way that you might want to configure your agent would be with skills so um you know if you've tried to use uh you know open claw for example okay so let me talk about openclaw for for...

---

## STEP 10：安裝 Skills（技能）

...e you a bit more accountability into what everyone's doing you can break your agents up into different um personas and you can also give them different skills um the best way to find skills would be uh skills.sh maybe not the best way but it's one of the most popular have you used this before yeah I my my question here is how do you know you're not installing skills that are you know have bad stuff in it it's a problem yeah it's it's a it's a real problem and it's something you have to be careful with i don't think anyone solved that um one of the things that skills.sh has is they do have um some degree of security audits yep so they have um these these badges so I think that that's that's as best as you can do probably for now and I mean you can just because it has a lot of GitHub stars doesn't mean it's you know 100% secure but it does give you directional kind of it's a data point right if if it has if the remotion you know skill has 100 plus thousand stars for example chances are i...

...t's likely that there's value there that's right that's right so what we can do if we wanted to if we did want to make a video about this right we can uh copy this here and we can go to paperclip there's a couple things that you could do you can um your skills are organized by uh company so we should be able to paste this here or if you can't remember that you can just ask your CEO like add the remotion skill or whatever but you know we don't need to do that right here we can just click add um yeah there we go so we've now we've got the Remotion skill installed into our company okay and um this actually keeps track of um like you can check for updates if the skill gets updated etc etc you know something that I might often do like I might do is I might say you know hire a video editor and give them the remotion skill and I would paste the URL and the CEO knows if you sign the CEO he knows how to do this um for the sake of demo we'll just wait because we don't need to do that this second...

---

## STEP 11：指派影片製作任務給 CEO

...r job at like organizing the documents organizing the artifacts that you have within Paperclip we'll do that but of course your agents are able to access um pages anywhere you want so for example on the paperclip website um I have a brand guide yeah the brand identity so when we're asking this question which is like how do I make sure that my agent makes a video that's good one piece of that is like do you have a brand guide yet um and you can ask your agent to do this right so I would say for kind of moola we haven't necessarily gotten there yet right our agents are still kind of working but eventually what you would do is you would create an issue create me a brand guide and it would give you the URL and you would look at it um then the other part would be is I might say um well why don't we do this right let's say um uh let's plan a 60 second remotion video um about moola showing the key pitch um that we could share on Twitter and we'll assign this to the CEO for now because we don...

...'t have a CMO but maybe we should maybe it should be in another project but whatever we'll we'll get there so um I would say make a plan for this don't uh make it yet but we need uh a video demoing the product and showing the pitch it needs to be animated needs to be animated and pretty agents don't really like care about typos so you don't have to care that much about it so whatever we'll let that we'll let that run and we'll come back a bit later um one of the things you'll notice is that our monthly spend right now is $0 even though we've been doing all this work um part of that is because I'm using my codeex subscription or claude code subscription actually I'm not even sure which model we're using for these might be Claude um oh yeah look at this our agent Yeah so our our our our CEO is using the uh Claude Opus and it's you are able to use your subscription um as well as API credits if you want and that's why you're seeing here that the costs are zero...

---

## STEP 12：Bug 修復示範（截圖 → Agent → QA）

...o like click on something and make sure that it actually works so for example um you know in here you can like at-mention um the CEO or at-mention a project you know like the onboarding project and this was like a really um you know you see it all the time but it for whatever reason my agents had a hard time coding this funny I can even see here that the that the pills have a different height and that really annoys me um so like what I might do is I would go into paperclip and I would actually post this screenshot here and I would say um the agent mentions pill is misaligned with the like uh project mention pill fix it right and I'm going to assign this to uh the cloud coder for the paperclip app and I'll say **you know when you're done pass it to QA uh to get eyes on it and verify it works here with a screenshot** now listen if you're going to run a zero human company you cannot be managing your apps at that level right like I I'm actually acting not even as a C a board member or CEO i'...

---

## STEP 13：Routines 功能（定時自動任務）

...ht now as I would say uh you know uh create a discord message on everything that uh that was merged into the main branch uh uh yeah into the like master branch of the code today so is this uh is this interesting to work through oh 100% okay great so we'll give this to I don't know the content strategist I suppose and this will be for the paperclip app uh app here we go so here's how I would actually do this i would say um every day we put work uh put work into paperclip um we're merging pull requests um from the community and adding features we want to have a discord channel where we post the updates um in a community like in a community formatted uh like form um we especially uh want to celebrate our community members who contribute so make sure you call out everyone who um added something that was merged we do take the weekends off sometimes so if there isn't anything you can just do nothing okay um uh read the GitHub changes for the last uh last 24 hours for this okay I know tha...

...t took a little bit of bit of time um but you know the repo is here so you can find the paperclip repo here it's all open source we've got um yeah 500 pull requests we're working on we've got um 30,000 stars so there's a lot of like motion happening in this repo that we want to be able to kind of celebrate on every day so uh fine i think this is good good enough like oh this is what I would say is um eventually we'll post it uh will post direct to Discord but for now just post in your issue okay so I'm going to create this routine then from there I can do a trigger i can say you know every day at 10 a.m i add a trigger here um we can uh run it right now and we can see what was actually run now this uh a routine right is actually almost like a template of an issue it's an issue that you're going to like rerun over and over and every day um but you still with paperclip get that same kind of tracking where you can see um for this particular day when we uh decided to run this what...

---

## STEP 14：雇用影片剪輯師 + Terminate 功能

...u know it's you're still using your kind of inference for your subscription but if you hooked it into something like open code or we're using like pure uh pay per token values you'd get kind of real dollars here okay we've hired our video editor um and let's check and see if he was given the skills yeah so there you go he has the Remotion best practices skills enabled our CEO is still working on uh planning the video so we'll just let him kind of kind of work doesn't seem like you have the context of firing a CEO firing an engineer firing a QA agent is that correct no so yeah you you can yeah you can come in here to configuration and uh let's see oh where's Oh let's see here i mean I hate to be that guy but Oh right here we got terminate you can terminate yeah okay well don't don't do it but you know he has had a chance yeah yeah give him a shot give him a give him a 30-day cure period at least right yeah so um some of the other things that you uh can do with paperclip is this idea o...

---

## 結語：你是老闆，不是在管細節

...nd find out how to communicate them um back which is even in a pre-AI era the the concept of a good leader of a good manager of a good CEO of a good founder is very much someone who can clearly communicate their values and taste right that's right that's right so **not much has changed except the vehicle to to doing it has changed instead of hiring employees you're hiring agents**.

---

## Paperclip Org Chart（組織架構）

...i had a question before before we move on now I had a question if if you you know if you go back to the paperclip uh project which by the way it's so cool that you use paperclip to build paperclip i expect nothing less from you obviously but you know you were talking about you know it's important to hire you know an agent for this and an agent for that how many agents do you have for the paperclip project like we're talking not that many actually um so this would be the org it's actually a little hard to see here um and yeah I would say that it is growing all the time um so we've got the CEO reporting to him would...

...be a CMO a UX designer and a CTO and I use different agents for um different reasons i would say that the cursor coder and the claude coder would be my kind of workhorse they're using the frontier models on my subscriptions um then I have a QA engineer who has um both the claude browser installed as well as there is a skill called agent browser which is it basically gives your agent uh access to a web browser in a way that is um a little bit faster than using Chrome like if you've used Chrome with clawed code before I'm sure you've seen it like pops up a Chrome window and like takes over your computer and if you click on it you mess it up and so that's the QA um I also have am starting an eval engineer so eval would be basically just a way saying like how do we start to um kind of like how do we do performance reviews on our agents and and be able to go back and reflect on what they did paperclip is going to be building tools where you can look at your past um issues look at the fee...

---

*逐字稿擷取來源：NotebookLM 從影片字幕處理，為主要段落節錄。完整影片：https://www.youtube.com/watch?v=C3-4llQYT8o*
