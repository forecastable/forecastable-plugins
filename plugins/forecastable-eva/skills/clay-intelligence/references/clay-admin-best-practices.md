# Clay Admin, Tips and Best Practices (from top YouTube voices)

Built 2026-10-04 for Eva (Forecastable partner-ops assistant). Second pass on the Clay YouTube knowledge base. Source: 30 new transcripts saved in `/home/claude/clay/youtube/transcripts/` (listed at the end) plus a few cross-references to the first-pass digest (`youtube-digest.md`).

How to read this file
- Every bullet is attributed as [creator, video URL @mm:ss]. Timestamps point to the start of the passage, so the exact words may be up to a minute later.
- Every number is what the speaker said on camera. None is independently verified. Do not quote prices or credit costs to a customer without checking clay.com that day.
- Pricing freshness: Clay moved to a new model in March 2026 (Actions plus Data Credits, plan renames). Any video published before that is marked PRE in the transcript header and in the source list below. Treat its prices, plan names, plan gates and "free if you bring your own key" claims as possibly stale.
- Labels: VENDOR = Clay itself. PARTNER = holds a Clay partner credential (Elite Studio, Clay Expert) as stated by the creator or a third-party expert list, or is a data vendor integrated into Clay. INDEPENDENT = no Clay credential found.
- Captions are machine generated: "Claygent" often appears as "cayen", "Cent" or "clent" in the raw transcripts.

---

## 1. Top voices

Ranked on Clay-specific depth (count and quality of admin-relevant videos), recognition by Clay (credential, Clay-hosted appearances, SCULPT) and reach (subscribers, views). Subscriber counts are YouTube display figures read on 2026-10-04.

| Rank | Creator | Channel URL | Subs | Clay credential (source) | Best for | Label |
|---|---|---|---|---|---|---|
| 1 | Eric Nowoslawski (Growth Engine X) | https://www.youtube.com/@ericnowoslawski | 16.7K (293 videos) | One of Clay's earliest employees; says on stage "we're an elite Clay Studio partner" ([kFQfMZBo6Lo @3:14](https://www.youtube.com/watch?v=kFQfMZBo6Lo)); described by Nebor's expert list as a former Clay team member | Table guard rails, credit efficiency, AI prompting rules at very high volume, Clay plus Claude Code architecture | PARTNER |
| 2 | Tim Yakubson (Unlock Clay, B2B Boosted) | https://www.youtube.com/@Tim-Yakubson | 3.84K (236 videos) | "I'm a Clay Expert" (channel description); co-published a 6-hour course with Clay (video 1JiLlbgyVWo, listed as "Tim Yakubson and Clay") | Admin hygiene tips, formulas, Functions, Workflows, Sculptor, honest Clay vs Claude Code takes | PARTNER |
| 3 | Clay official: Clay, SCULPT, Clay University (incl. Yash Tekriwal, then head of education) | https://www.youtube.com/@GrowWithClay, https://www.youtube.com/@SCULPTbyClay, https://www.youtube.com/@ClayUniversity | 17.2K / 818 / 1.04K | Vendor | Feature launches (SCULPT), Claygent prompting method from Clay's education lead. Thin on admin how-tos: @GrowWithClay has 9 uploads, recent ones are Clay Cup streams; Clay University's latest upload is about 1 year old | VENDOR |
| 4 | Matt Lucero (Anevo) | https://www.youtube.com/@matthewlucero | 18K (198 videos) | Affiliate only; no partner credential found | Most current full platform tour after the pricing change (sources, metaprompter, max cost, run conditions, waterfall config, Signals, sequencer, Functions, MCP) | INDEPENDENT |
| 5 | Michel Lieben (ColdIQ) | https://www.youtube.com/@MichLieben | 3.28K (160 videos) | Certified Clay Expert per Nebor's 2026 expert list | Feature tier list (about 95K views, top Clay feature review found), agency operating model after the pricing change, Clay Ads | PARTNER |
| 6 | Patrick Spychalski (The Kiln) | https://www.youtube.com/@Patrick-TheKiln | 503 (3 videos), appears mostly as a guest | The Kiln described as "one of only six Clay Elite Studios" (Finn Thormeier video description); Certified Clay Expert per Nebor list; Clay University webinar guest | CRM cleaning layer pattern, when CRM work must stay in Clay | PARTNER |
| 7 | Jacob Tuwiner (Sculpted) | https://www.youtube.com/@jacobtuwiner | 3.72K (244 videos) | "one of the first five Clay experts" (channel description); presented a partner briefing deck Clay gave him | The March 2026 pricing model explained, CRM cleanup and enrichment plays | PARTNER |
| 8 | Michael Saruggia | https://www.youtube.com/@michaelsaruggia | 3.35K (99 videos) | None found ("The Clay Operator" is self-branding) | When Clay fits in 2026, CRM job-change routines, scheduled reruns | INDEPENDENT |
| 9 | Nathan Lippi (Clay Bootcamp) | https://www.youtube.com/@nathanlippi | 1.29K (42 videos) | None found; runs Clay Bootcamp | GTM engineering principles; host of Joe Rhew's modular function-table session | INDEPENDENT |
| 10 | Joe Rhew (The Workflow Company) | https://www.youtube.com/@workflowcompany | 656 (29 videos) | None found; Clay Bootcamp student number two (per Lippi) | CRM sync design with least-privilege API access, modular "function tables", naming conventions | INDEPENDENT |
| 11 | Xavier Caffrey (OneAway) | https://www.youtube.com/@XaviercaffreyGTM | 1.33K (54 videos) | None found (OneAway appeared on a Clay University fireside chat) | Beginner tutorial already in the first pass (kY5E4wl8wlA) | INDEPENDENT |
| 12 | Nate Herk | https://www.youtube.com/@nateherk | 1.05M (535 videos) | None; his Clay video carries a Clay credits offer link | Reach only: Claude Code orchestrating Clay (first pass, zyvdl__Ywfk). Few Clay admin videos | INDEPENDENT |

Specialist single-topic sources used below (small channels, good for one technique): Stan Stojanovic / frontBrick (2026 features), David Shamula (webhooks and HTTP API), Tanay Mishra (HTTP rate limits; already Tier 2 in the registry), RedHawk BD (Salesforce via HTTP API), Stack & Scale (Sculptor habits), Wiza (waterfall design; a data vendor, so PARTNER and self-interested).

Checked and not used: Kellen Casebeer, Bryan Cooper, Josh Whitfield, Lucas Perret, Alex Vacca: no Clay-specific YouTube channel or video surfaced in searches on 2026-10-04 (they may publish on LinkedIn instead). Yash Tekriwal has no personal channel found; his material is on Clay University and guest webinars.

Gap to know: no video in either pass demonstrates Clay workspace user roles, seat permissions or per-user credit limits. For those, Eva should use Clay's help docs, not YouTube.

---

## 2. Distilled best practices by theme

### 2.1 Admin and governance

- Make "every paid column has a run condition" a team rule, even a trivial one like first name is not empty, so nobody spends credits by habit. [Eric Nowoslawski, https://www.youtube.com/watch?v=kFQfMZBo6Lo @3:50]
- Check where credits went in Settings, Credit usage; it breaks spend down by table so you can find the expensive enrichment (Tim's example: 48,000 credits in one table). [Tim Yakubson, https://www.youtube.com/watch?v=p8I_s91xfmc @24:57]
- Build in Sandbox mode with 5 to 10 imported rows before going live, and switch off auto-update both per column and for the whole table while building. [Tim Yakubson, https://www.youtube.com/watch?v=p8I_s91xfmc @8:51, @21:52, @24:28]
- Name columns by role so any teammate can run a template: "Input" columns, numbered "Step" columns, and labelled outputs (Email 1, Email 2). Color code inputs green, columns that need editing before a run yellow, broken columns red. [Tim Yakubson, https://www.youtube.com/watch?v=p8I_s91xfmc @11:01, @12:39]
- Naming convention for shared modules: mark inputs with "I" and optional inputs "(O)", and give every reusable module a common prefix so it is easy to find from other tables. [Joe Rhew on Nathan Lippi, https://www.youtube.com/watch?v=y8oFBx1MaCA @44:45]
- Put repeated logic (email waterfall, CRM write-back, name cleaning) in a Function so one change updates every table. Eric runs about 400 active tables and says he would otherwise have to edit each one. [Eric Nowoslawski, https://www.youtube.com/watch?v=kFQfMZBo6Lo @4:24]; how to save columns as a Function [Tim Yakubson, https://www.youtube.com/watch?v=6edc4r6bXOI @1:41]; CRM write-back as one shared Function, now on all paid plans per the pricing briefing [Jacob Tuwiner, https://www.youtube.com/watch?v=WAYpwmZ4Agw @5:57]
- Save good prompts and column configs as templates; "Share as template" keeps the column structure and strips the data. [Tim Yakubson, https://www.youtube.com/watch?v=p8I_s91xfmc @7:48]; [Yash Tekriwal, https://www.youtube.com/watch?v=tDHdnCX2_ps @37:57]
- Use other people's templates as inspiration, not as your build; adapting someone else's stack usually takes longer than building your own. [Tim Yakubson, https://www.youtube.com/watch?v=p8I_s91xfmc @30:13]
- Keep a Do Not Contact table (customers, open deals, past proposals) and check it with a free "lookup multiple rows" before any send step. [Tim Yakubson, https://www.youtube.com/watch?v=p8I_s91xfmc @16:46]
- One workspace per client is the post-pricing agency norm: clients pay for their own Clay account, the agency builds inside it and imports its template library. [Michel Lieben with Tim Yakubson, https://www.youtube.com/watch?v=MBrigXBfvHs @13:53]. Clay's own education lead made the same point in 2024 (separate workspaces are easier to manage than a big folder tree). [Yash Tekriwal, https://www.youtube.com/watch?v=tDHdnCX2_ps @33:23]
- Larger companies (roughly 50 plus employees with legal or compliance review) often will not approve Claude Code or OpenClaw on their systems but will approve Clay, so enterprise GTM work tends to stay in Clay. [Tim Yakubson on Michel Lieben, https://www.youtube.com/watch?v=MBrigXBfvHs @15:48]; same view for companies above about 30M ARR: compliance, one central place, a stable platform instead of "15 different Claude licenses" [Michael Saruggia, https://www.youtube.com/watch?v=iHpXv0FmVoY @4:57]
- CRM credentials: when you need API access beyond the native integration, create a dedicated private app with only the scopes you need (read-only if you are only checking), so a leaked token cannot write. [Joe Rhew, https://www.youtube.com/watch?v=qF2WPueIDN4 @1:45]
- Support: paste the table link when you contact Clay support so they can open it; the in-app help agent answers most questions first. [Tim Yakubson, https://www.youtube.com/watch?v=p8I_s91xfmc @29:33]

### 2.2 Table architecture

- Think of Clay as the layer between inputs (lists, CRM, webhooks) and outputs (CRM, sequencers, ads). Decide inputs and outputs before buying a plan. [Tim Yakubson, https://www.youtube.com/watch?v=p8I_s91xfmc @23:20, @31:21]; same framing as "data intermediary" [Patrick Spychalski, https://www.youtube.com/watch?v=YLXzWpknuJk @9:13]
- Split company and contact work: enrich companies once in a deduplicated company table, then pull results into the contact table with a free "lookup single row". Five contacts at one company should not pay five times. [Eric Nowoslawski, https://www.youtube.com/watch?v=tM4nqus2L8w @3:36]
- Start every build from "corner pieces": company website or company LinkedIn URL for accounts; name plus company, or email, for people. Everything else can be derived from those. [Yash Tekriwal, https://www.youtube.com/watch?v=tDHdnCX2_ps @15:10]
- Pick the company identifier deliberately when using Find People: in Tim's test, domain matched 1,848 companies vs 353 via LinkedIn URL. [Tim Yakubson, https://www.youtube.com/watch?v=p8I_s91xfmc @20:25]
- Set column types correctly (URL, number, text); wrong types cause many "bugs". [Tim Yakubson, https://www.youtube.com/watch?v=p8I_s91xfmc @3:03]
- Turn on Auto-dedupe for the key column (full name, domain, email) so re-imports do not double spend. [Tim Yakubson, https://www.youtube.com/watch?v=p8I_s91xfmc @0:50]
- Use Clay as the visible, hosted "final mile" (segmentation, AI copy, push to sequencers) even if upstream list pulling and email finding run elsewhere; visual tables make exceptions easy to spot before bad emails go out. [Eric Nowoslawski, https://www.youtube.com/watch?v=s2hShfYo7Wo @13:37]
- Keep a cache outside Clay for anything you paid for (emails with last-verified date, company data). Clay is middleware, not a database you own. Eric's cache: Supabase, revalidate only if older than 90 days. [Eric Nowoslawski, https://www.youtube.com/watch?v=kFQfMZBo6Lo @6:38]; [https://www.youtube.com/watch?v=s2hShfYo7Wo @7:56]
- For always-on campaigns, use scheduled sources instead of daily CSV uploads (Eric parks a client's TAM in a cheap HubSpot portal and processes an active segment). [Eric Nowoslawski, https://www.youtube.com/watch?v=kFQfMZBo6Lo @7:49]
- Tables vs Workflows: tables remain right for high-volume row by row enrichment of a defined list; Workflows (visual canvas) are for branching, routing and event-driven plays such as inbound lead routing by region and segment. [Tim Yakubson, https://www.youtube.com/watch?v=UvFDcbmzPJQ @3:38]
- Audiences hold CRM, warehouse, CSV and Clay-sourced records in one deduplicated place and are not bound by the 50,000 row table cap Stan cites for tables. [Stan Stojanovic, https://www.youtube.com/watch?v=hXA8RIVfYOI @1:21, @1:44]
- Pre-Functions pattern still worth knowing: a shared "function table" you write rows into and look results back from, with dedupe on so repeats are never re-run. Caveat: there is no native delay between write and lookup, so Joe used an external echo endpoint that waits 10 seconds. Native Functions now cover most of this. [Joe Rhew on Nathan Lippi, https://www.youtube.com/watch?v=y8oFBx1MaCA @41:42, @47:50, @49:22]

### 2.3 Credit efficiency

Post-change model first (March 2026), as explained by a partner Clay briefed:
- Free: finding and importing records, importing first-party (CRM) data, transforming with formulas, CRM lookups. Charged an Action: enriching with third-party data (including LinkedIn and Claygent), and execution steps such as CRM sync, sequencing, ads audience sync and Slack alerts. Data credits are charged on top for paid data. [Jacob Tuwiner, https://www.youtube.com/watch?v=WAYpwmZ4Agw @11:59]
- The Action fee applies even when you bring your own API key; BYO keys no longer make a run free. [Jacob Tuwiner, https://www.youtube.com/watch?v=WAYpwmZ4Agw @4:47]; [Matt Lucero, https://www.youtube.com/watch?v=jEkDgA8hPmo @3:03]
- Data credit prices were cut (examples quoted from the briefing deck: enrich person 1 to 0.5, validate email 1 to 0.1, find work email 2 to 0.8 credits). [Jacob Tuwiner, https://www.youtube.com/watch?v=WAYpwmZ4Agw @8:03]
- AI: most models on flat, lower credit rates; heavier models move to variable pricing, quoted as realized model cost plus 20 percent, visible per row before scaling. [Jacob Tuwiner, https://www.youtube.com/watch?v=WAYpwmZ4Agw @14:15]

Practices that still hold:
- Run conditions on every paid column; chain them so nothing runs downstream of a missing or invalid email. [Eric Nowoslawski, https://www.youtube.com/watch?v=tM4nqus2L8w @1:41]; [Tim Yakubson, https://www.youtube.com/watch?v=p8I_s91xfmc @14:18]
- A filtered view limits runs: columns only run on rows visible in the filtered view. [Michel Lieben, https://www.youtube.com/watch?v=C9aFa9kNENw @24:34]; [Matt Lucero, https://www.youtube.com/watch?v=jEkDgA8hPmo @24:21]
- "Save and don't run", then run one row, then 10, then all. [Tim Yakubson, https://www.youtube.com/watch?v=p8I_s91xfmc @16:22]; [Matt Lucero, https://www.youtube.com/watch?v=jEkDgA8hPmo @17:16]; test AI on 10 diverse rows before scaling [Yash Tekriwal, https://www.youtube.com/watch?v=tDHdnCX2_ps @4:34]
- Set a Max cost on AI columns. [Matt Lucero, https://www.youtube.com/watch?v=jEkDgA8hPmo @16:15]; [Yash Tekriwal, https://www.youtube.com/watch?v=tDHdnCX2_ps @44:01]
- Timestamp what you write to the CRM and only re-enrich when the last update is older than your threshold (Eric suggests two to six months for company data). [Eric Nowoslawski, https://www.youtube.com/watch?v=tM4nqus2L8w @6:13]
- Signals first, bulk enrichment second: monitoring signals on a TAM and enriching only the accounts that fire is more cost-efficient than bulk-scoring every company. [Stan Stojanovic, https://www.youtube.com/watch?v=hXA8RIVfYOI @6:37]
- Native Find People / Find Companies sources do not spend credits. [Tim Yakubson, https://www.youtube.com/watch?v=p8I_s91xfmc @18:53]; [Matt Lucero, https://www.youtube.com/watch?v=jEkDgA8hPmo @9:07]
- Formulas are free; use them before AI for cleaning, combining, if/then logic and scoring. [Eric Nowoslawski, https://www.youtube.com/watch?v=kFQfMZBo6Lo @8:57]
- Know your per-row cost before scaling: Yash's research table cost 13 credits per row, so 10,000 leads is 130,000 credits. [Yash Tekriwal, https://www.youtube.com/watch?v=tDHdnCX2_ps @44:01]. Sculptor-built tables cost Tim about 20 to 30 credits per row. [Tim Yakubson, https://www.youtube.com/watch?v=BpQU9gXYtC0 @19:57]
- Lieben's warning: a new user can burn a whole month's plan in one click by running an untested table. [Michel Lieben, https://www.youtube.com/watch?v=C9aFa9kNENw @7:39]

### 2.4 Waterfalls and data quality

- A waterfall queries providers in order and stops at the first hit; you pay only for the provider that returned data. [Patrick Spychalski, https://www.youtube.com/watch?v=YLXzWpknuJk @21:34]; [Wiza, https://www.youtube.com/watch?v=hY9vKVqptN0 @1:21]
- Configure it: open Full configuration, delete providers you do not want, reorder, set the validation provider; Lucero puts providers he holds API keys for at the front. [Matt Lucero, https://www.youtube.com/watch?v=jEkDgA8hPmo @22:19]
- Aggregator providers (FullEnrich, BetterContact) are themselves waterfalls of many sources, so one column can stand in for a long chain. [Tim Yakubson, https://www.youtube.com/watch?v=p8I_s91xfmc @4:31]; [Michel Lieben, https://www.youtube.com/watch?v=C9aFa9kNENw @8:25]
- Verify after the waterfall, not instead of it; Eric double-verifies "valid" emails with a second verifier and reports bounce rates under 1 percent. [Eric Nowoslawski, https://www.youtube.com/watch?v=cbmZkHF9tfI @6:20]; [Wiza, https://www.youtube.com/watch?v=hY9vKVqptN0 @5:14]
- Confirm the person still works at the company before paying for email finding; third-party list data goes stale. [Eric Nowoslawski, https://www.youtube.com/watch?v=cbmZkHF9tfI @4:05]
- Expect drop-off: Eric says only 50 to 70 percent of pulled contacts end with a validatable email, depending on industry, so forecast list volume on verified emails. [Eric Nowoslawski, https://www.youtube.com/watch?v=s2hShfYo7Wo @3:22]
- Schedule re-enrichment; Wiza cites 2 to 3 percent contact decay per month (vendor figure). [Wiza, https://www.youtube.com/watch?v=hY9vKVqptN0 @0:00, @5:14]
- Watch for "first match" risk (a cheaper, weaker provider answering first) and check every provider in the chain is GDPR and CCPA compliant. [Wiza, https://www.youtube.com/watch?v=hY9vKVqptN0 @5:37, @6:16]
- A generic logo on a source or enrichment usually means LinkedIn-scraped data. [Patrick Spychalski, https://www.youtube.com/watch?v=YLXzWpknuJk @12:18]. Do not trust "find contacts by job title" blindly; Lieben rates its data quality low and double-checks it. [Michel Lieben, https://www.youtube.com/watch?v=C9aFa9kNENw @14:33]

### 2.5 Claygent and AI prompting

Method (Clay's own education lead):
- Claygent is "a really ambitious, all-knowing junior employee" with no context, so prompts must supply it. [Yash Tekriwal, https://www.youtube.com/watch?v=tDHdnCX2_ps @1:32]
- Prompt anatomy: set the task and context; pass the row inputs (company name, domain); give sequential steps that cover edge cases, written as you would instruct a human researcher; then define the output and what to return when nothing is found. [Yash Tekriwal, https://www.youtube.com/watch?v=tDHdnCX2_ps @7:35]
- Structured outputs: name each output field exactly as the prompt names it, and set field types (URL, number, email, true/false, select). For select fields list every allowed option up front or the model invents new ones. More than about five fields degrades results. [Yash Tekriwal, https://www.youtube.com/watch?v=tDHdnCX2_ps @4:34, @6:05, @28:50, @30:21]
- Model choice: cheapest model for simple one or two step lookups, smarter model for open-ended or creative work. [Yash Tekriwal, https://www.youtube.com/watch?v=tDHdnCX2_ps @3:03]. Claygent reads public text and images only: nothing behind logins, no audio or video. [same video @25:45, @37:57]

Rules from the heaviest user:
- 10-minute manual research rule: write down what you would look for if researching by hand for 10 minutes, then automate exactly that. [Eric Nowoslawski, https://www.youtube.com/watch?v=kFQfMZBo6Lo @9:56]
- Only let AI do one thing per column; get website content in one column, then classify in separate downstream columns. [Eric Nowoslawski, https://www.youtube.com/watch?v=kFQfMZBo6Lo @10:41]
- Do not ask Claygent to find information and make the decision in the same column: you cannot give Claygent training examples, so find with Claygent and decide in a separate AI column that has examples. [Eric Nowoslawski, https://www.youtube.com/watch?v=cbmZkHF9tfI @8:07]
- Add an escape value so failures are filterable. Eric's prompt line, quoted: "if you're not at least 99.5% sure of the answer you're going to give just output the word purple instead as I need the answers to be accurate". [Eric Nowoslawski, https://www.youtube.com/watch?v=DJnwrD9-i30 @2:28]. Yash's equivalent: "if I can't find it respond with unable to find". [Yash Tekriwal, https://www.youtube.com/watch?v=tDHdnCX2_ps @9:05]
- Always include three or four hand-written examples of the output you want; fix weak results by changing examples before rewriting the prompt. [Eric Nowoslawski, https://www.youtube.com/watch?v=kFQfMZBo6Lo @12:34]; [https://www.youtube.com/watch?v=cbmZkHF9tfI @8:44]
- For hard classifications (industry), ask for reasoning before the final answer. [Eric Nowoslawski, https://www.youtube.com/watch?v=kFQfMZBo6Lo @13:53]
- Use the metaprompter (write a lazy prompt, click Generate), then ask an LLM "what questions do you have for me to improve this prompt?" (Eric credits the tip to Yash). [Eric Nowoslawski, https://www.youtube.com/watch?v=kFQfMZBo6Lo @13:21]; [Matt Lucero, https://www.youtube.com/watch?v=jEkDgA8hPmo @14:12]
- Pin the source: tell Claygent the only acceptable source is the website in the input, then add a second AI column to confirm the result really came from that company, because Claygent sometimes wanders to other sites. [Eric Nowoslawski, https://www.youtube.com/watch?v=DJnwrD9-i30 @2:02]; [https://www.youtube.com/watch?v=cbmZkHF9tfI @11:06]
- Expect 80 percent of build time to go into tuning AI edge cases and 20 percent into wiring integrations. [Eric Nowoslawski, https://www.youtube.com/watch?v=kFQfMZBo6Lo @14:31]
- Always design a fallback line so leads without a case study or competitor still get a valid first line; merge case-study, competitor and fallback lines into one variable with a formula. [Eric Nowoslawski, https://www.youtube.com/watch?v=cbmZkHF9tfI @2:50, @14:47]

Example prompts quoted from the videos
- Eric's four-step structure: "one, give Claygent a task to do at just a very high level; two, you have to give it all the data that you need to work with; three, you need to explain to it how you would find the data if you were manually doing the task; and then four, you need to put up guard rails". [https://www.youtube.com/watch?v=DJnwrD9-i30 @0:19]
- Eric's case-study prompt opener: "go to the website in the input and find information of up to three case studies that the company mentions on their website". Guard rails used: "the only source that any of these case studies should come from is the website in the input"; "please think thoroughly about your process and take your time"; "it is very important that this is accurate and done well, my job is on the line". [https://www.youtube.com/watch?v=DJnwrD9-i30 @1:39, @2:02, @3:37]
- Tim's no-credit LinkedIn finder (run with your own OpenAI key on a small model): "the input is the person's name; based on the name and the website of their company, find me the person's LinkedIn profile and nothing else". [https://www.youtube.com/watch?v=p8I_s91xfmc @5:50]
- Lucero's B2B check, then improved by the metaprompter: "visit the websites of all the leads in this table and see if they are B2B companies; if they are, output true, and if not output false". [https://www.youtube.com/watch?v=jEkDgA8hPmo @13:11]
- Yash's 10-K finder steps: Google search first; if not in the top results, check the company's investor relations page; then the EDGAR database; then "just try and find it"; return only the URL, else "unable to find". [https://www.youtube.com/watch?v=tDHdnCX2_ps @7:35]

### 2.6 Formulas and conditional runs

- Three formula jobs to master: conditional runs ("only run if status is valid"), data formatting (round 18,xxx,xxx visitors to "18 million"), and conditional outputs (if employee count over 2,000 say "wonderful ICP fit", then only push rows that contain that text). [Tim Yakubson, https://www.youtube.com/watch?v=EiVYuaLpNu0 @1:42, @2:42, @4:10]
- Use the AI formula generator; it costs no credits and shows a preview so you can confirm "output is correct" before saving. [Michel Lieben, https://www.youtube.com/watch?v=C9aFa9kNENw @19:11, @19:57]. Formulas are JavaScript underneath, so paste a screenshot into an LLM when one breaks. [Eric Nowoslawski, https://www.youtube.com/watch?v=kFQfMZBo6Lo @9:46]
- Run conditions need exact column references: Lucero's first condition ("only run for leads that live in New York") skipped a New York row until rewritten as "location contains New York". Check the preview. [Matt Lucero, https://www.youtube.com/watch?v=jEkDgA8hPmo @17:16]
- Filter list fields inside enrichment results with a formula, for example from the experience list "find the first instance where is current is unchecked, then return the URL" to get a prior employer for free. [Tim Yakubson, https://www.youtube.com/watch?v=EiVYuaLpNu0 @18:06]
- Wrap final-output variables in curly brackets in the column name (for example {first name}) so they are easy to find in message templates. [Tim Yakubson, https://www.youtube.com/watch?v=EiVYuaLpNu0 @9:19]
- Use the free "Normalize company name" enrichment before company names go into copy. [Tim Yakubson, https://www.youtube.com/watch?v=EiVYuaLpNu0 @20:09]
- Rule-based "score row" is cheaper and predictable but rigid; AI scoring handles nuance. Lieben ranks AI lead scoring A and score row B. [Michel Lieben, https://www.youtube.com/watch?v=C9aFa9kNENw @34:35]

### 2.7 CRM sync and write-back

- Do not push entire prospect lists into the CRM; push qualified or engaged records only, to avoid clutter. [Patrick Spychalski, https://www.youtube.com/watch?v=YLXzWpknuJk @37:07]
- Use Clay as a CRM cleaning layer: import records (HubSpot lists, Salesforce list views or reports, which can auto-refresh on a schedule), enrich and normalize, write back. [Patrick Spychalski, https://www.youtube.com/watch?v=YLXzWpknuJk @13:52, @38:40]
- Keep CRM-touching work in Clay rather than an autonomous agent: an agent with Salesforce write access has "no guarantee it doesn't just like destroy all the data". Claude Code is fine for one-off list enrichment, not for CRM enrichment or inbound aggregation. [Patrick Spychalski, https://www.youtube.com/watch?v=fHPfuDUiRSw @6:04, @7:34]
- Job-change routine: import Salesforce reports on a monthly schedule, find LinkedIn from email with Claygent, compare current employer to the CRM account, only act on changes in the last three months, use the LinkedIn URL as the stable key (emails change, LinkedIn does not), mark the old contact "left company", look up or create the new lead and account, add to a campaign. [Michael Saruggia, https://www.youtube.com/watch?v=DHX8uoA53OI @5:13 to 10:22]
- Exclude by deal status, not by mere existence in the CRM: look up the company ID natively, then search HubSpot deals by associated company via the API, and only suppress accounts with an active deal. [Joe Rhew, https://www.youtube.com/watch?v=qF2WPueIDN4 @1:20, @2:45]
- Lookup keys differ by CRM: HubSpot contact lookup needs email, Salesforce can match on LinkedIn URL (Eric's experience). [Eric Nowoslawski, https://www.youtube.com/watch?v=tM4nqus2L8w @6:50]
- Native CRM depth: Saruggia says HubSpot and Salesforce are the well-integrated CRMs (lookup, create, update, add to campaign). [Michael Saruggia, https://www.youtube.com/watch?v=QfnNZc5J2mw @14:52]
- Clay Audiences push back to the CRM with write rules "always write, never write, write only if empty" (first pass, SCULPT keynote). [Clay, https://www.youtube.com/watch?v=uyOxNMVcB2E @26:36]

### 2.8 Webhooks and HTTP API

- In: add a "Monitor webhook" source to get an endpoint URL, then POST JSON to it from any tool. Out: add an HTTP API column, method POST, body JSON with column references. [David Shamula, https://www.youtube.com/watch?v=vF6dL-Zdqk4 @6:36, @11:32]
- Webhooks are limited at workspace level; Eric batches about 25 contacts per webhook call and schedules big pushes overnight (2 a.m.) so rate limits do not collide with daytime work. [Eric Nowoslawski, https://www.youtube.com/watch?v=s2hShfYo7Wo @11:51, @2:39]
- An HTTP API column fires across many rows at once and can overrun a third-party rate limit; failed rows are not retried until you rerun them. Fix: send through a queue such as Hookdeck with a max delivery rate and automatic retries. [Tanay Mishra, https://www.youtube.com/watch?v=48IjCJZXRMQ @1:02, @5:08, @5:50]
- Salesforce via HTTP API: per the creator, Salesforce stopped allowing new Connected Apps for new orgs in March 2026, so use an External Client App; in Clay, one HTTP column gets the temporary OAuth token, a second POSTs the record with a "Bearer" authorization header. [RedHawk BD, https://www.youtube.com/watch?v=Omp-obI8rkU @0:53, @5:05]
- HTTP API is where advanced users go "creditless" for providers Clay lacks; powerful but fiddly to get right first time. [Michel Lieben, https://www.youtube.com/watch?v=C9aFa9kNENw @30:42]

### 2.9 Debugging

- When a column misbehaves, check the column type first. [Tim Yakubson, https://www.youtube.com/watch?v=p8I_s91xfmc @3:03]
- Click into a cell to see each waterfall step and which provider returned what, and the AI response cell to read its reasoning. [Michel Lieben, https://www.youtube.com/watch?v=C9aFa9kNENw @9:58]; [Matt Lucero, https://www.youtube.com/watch?v=jEkDgA8hPmo @18:16]
- Keep a test row you already know the answer to and check it first after every change. [Stack & Scale, https://www.youtube.com/watch?v=f-H2kmtZHx4 @3:20]
- "Run condition not met" in a cell means the condition worked; verify that is intended. [Tim Yakubson, https://www.youtube.com/watch?v=p8I_s91xfmc @14:18]
- Rerun only "empty or out-of-date rows" after fixing a column instead of the whole table. [Matt Lucero, https://www.youtube.com/watch?v=jEkDgA8hPmo @25:22]
- Watch structured output hallucinations (blank or invented URLs) and narrow the prompt (for example "not API docs"). [Yash Tekriwal, https://www.youtube.com/watch?v=tDHdnCX2_ps @56:12]

### 2.10 Common mistakes

- Running a whole table before testing: one click can burn a month of credits. [Michel Lieben, https://www.youtube.com/watch?v=C9aFa9kNENw @7:39]
- Pressing "save and run" when importing a CSV into a built table; use "save and don't run". [Tim Yakubson, https://www.youtube.com/watch?v=p8I_s91xfmc @28:24]
- One AI column doing research plus classification plus decision. [Eric Nowoslawski, https://www.youtube.com/watch?v=kFQfMZBo6Lo @10:41]
- No fallback value, so failures come back as many different "not found" sentences you cannot filter. [Eric Nowoslawski, https://www.youtube.com/watch?v=kFQfMZBo6Lo @11:37]
- Enriching company data on every contact row. [Eric Nowoslawski, https://www.youtube.com/watch?v=tM4nqus2L8w @3:36]
- Treating Clay as storage and paying again for the same data. [Eric Nowoslawski, https://www.youtube.com/watch?v=kFQfMZBo6Lo @6:38]
- Over-trusting signals: many custom signals cost effort and money without proven lift. Test them by enriching positive replies (and negatives) with every signal, then target the ones that actually separate them. [Eric Nowoslawski, https://www.youtube.com/watch?v=3THIdISjTkk @3:48]
- Excluding every company that exists in the CRM instead of only those with active deals. [Joe Rhew, https://www.youtube.com/watch?v=qF2WPueIDN4 @0:45]
- Giving Sculptor long multi-step prompts: one step per prompt, roughly 500 characters or less worked best for Brandon. [Stack & Scale, https://www.youtube.com/watch?v=f-H2kmtZHx4 @13:29, @16:28]
- Following old tutorials for plan gates or Salesforce Connected Apps (see section 4).

### 2.11 New 2026 features

- Sculptor (AI co-pilot): good for starting lists and getting unstuck; Tim found end-to-end builds took him as long as building manually and cost about 20 to 30 credits per row, so use it as a "chat for help" while building column by column. [Tim Yakubson, https://www.youtube.com/watch?v=BpQU9gXYtC0 @19:57, @20:34]. Positive beginner view [Matt Lucero, https://www.youtube.com/watch?v=jEkDgA8hPmo @6:05]; Tim rated it "a solid seven out of ten" in the Workflows beta [https://www.youtube.com/watch?v=UvFDcbmzPJQ @7:00]
- Workflows (open beta at recording): visual canvas with triggers (webhook, schedule, manual, CSV upload, segments or audiences on higher plans); buildable from Sculptor or the Clay CLI in Claude Code; Tim also uses it to sketch builds for proposals. [Tim Yakubson, https://www.youtube.com/watch?v=UvFDcbmzPJQ @2:56, @4:41, @7:39]. frontBrick uses Workflows to queue 10 leads a day per rep into Gong instead of n8n or Make. [Stan Stojanovic, https://www.youtube.com/watch?v=hXA8RIVfYOI @11:07]
- Audiences and Signals: unified deduplicated TAM; company signals (topic intent, website visits, new hires, news and fundraising, job posts) and person signals (topic intent, job change, promotion). [Stan Stojanovic, https://www.youtube.com/watch?v=hXA8RIVfYOI @6:37]. Signals can run daily, weekly or monthly and alert Slack or update the CRM. [Matt Lucero, https://www.youtube.com/watch?v=jEkDgA8hPmo @30:28]
- Ads sync (LinkedIn, Meta, Google): segment, enrich work emails and LinkedIn IDs to raise match rates, sync. [Tim Yakubson on Michel Lieben, https://www.youtube.com/watch?v=MBrigXBfvHs @17:21, @21:40]; [Stan Stojanovic, https://www.youtube.com/watch?v=hXA8RIVfYOI @9:49]
- Native Sequencer: per Lucero a white-labelled Smartlead; fine for small account-based sends, use a standalone sequencer above roughly 1,000 emails a day. [Matt Lucero, https://www.youtube.com/watch?v=jEkDgA8hPmo @27:24]; Eric: under 5,000 emails a day, Clay's native tooling is enough [https://www.youtube.com/watch?v=s2hShfYo7Wo @15:21]
- Clay agent upgrade: reusable skills, can find contacts and jobs inside Clay, use business context and files, return many structured fields in one call, and be called from coding agents or Workflows. [Stan Stojanovic, https://www.youtube.com/watch?v=hXA8RIVfYOI @12:56]
- Navigator (browser-acting Claygent, slow and expensive, can fill forms) and Intent (website de-anonymization at company level, higher plan). [Michael Saruggia, https://www.youtube.com/watch?v=QfnNZc5J2mw @9:28, @4:27]
- Scheduled column reruns for signal monitoring (pair with a Google date restriction so only last-week news counts). [Michael Saruggia, https://www.youtube.com/watch?v=QfnNZc5J2mw @11:03]
- API, CLI and MCP: Clay can now be driven from Claude Code, Codex and other agents. [Stan Stojanovic, https://www.youtube.com/watch?v=hXA8RIVfYOI @3:06]; MCP listed in the main menu [Matt Lucero, https://www.youtube.com/watch?v=jEkDgA8hPmo @5:05]. Claude Code plugin install and first-run rules are in the first-pass digest (section 4, Tim Yakubson UC-UcXi9G9k, Nate Herk zyvdl__Ywfk, Tanay Mishra hKFN-1QkG-c).

---

## 3. Top 20 tips Eva should know cold

1. Every paid column gets a run condition, chained so nothing runs after a missing or invalid email. (Nowoslawski, Yakubson)
2. Test on 1 row, then 10 diverse rows, then scale; set Max cost on AI columns. (Yakubson, Tekriwal, Lucero)
3. Build in Sandbox with auto-update off at column and table level. (Yakubson)
4. Since March 2026, every enrichment and every export (CRM, sequencer, ads, Slack) is an Action even with your own API key; imports, formulas and CRM lookups are free. (Tuwiner, Lucero)
5. Read the Credit usage page by table before blaming a feature. (Yakubson)
6. Enrich companies once in a deduplicated company table and look them up from contacts. (Nowoslawski)
7. Auto-dedupe on the key column and correct column types prevent most double spend and odd bugs. (Yakubson)
8. Put shared logic (waterfall, CRM write-back, cleaning) in Functions; one edit updates every table. (Nowoslawski, Tuwiner, Rhew)
9. Name columns Input / Step / Output, color code them, and keep a known-answer test row. (Yakubson, Rhew, Stack & Scale)
10. Cache paid data outside Clay with a last-verified date; revalidate emails older than about 90 days. (Nowoslawski)
11. Verify emails after the waterfall and confirm the person still works there before paying to find them. (Nowoslawski, Wiza)
12. Claygent prompt = context, inputs, step-by-step manual method with edge cases, output plus a "not found" value. (Tekriwal, Nowoslawski)
13. One AI task per column; find with Claygent, decide in a separate AI column that has examples. (Nowoslawski)
14. Name structured output fields exactly as the prompt does, set types, list all select options, keep to about five fields. (Tekriwal)
15. Use formulas (free, AI-generated, preview before save) before reaching for AI. (Nowoslawski, Lieben)
16. Only qualified or engaged records go to the CRM; suppress by active deal, not by existence. (Spychalski, Rhew)
17. Keep CRM-writing and enterprise work in Clay; agents are fine for list enrichment but risky on core systems and often blocked by compliance. (Spychalski, Saruggia, Yakubson on Lieben)
18. Use the LinkedIn URL as the durable person key for job-change routines; run them monthly on imported reports. (Saruggia)
19. HTTP API columns can swamp third-party rate limits; batch webhooks (Eric uses about 25 records per call) and queue outbound calls with retries. (Nowoslawski, Mishra)
20. Use Tables for row-by-row volume, Workflows for branching and routing, Audiences plus Signals for always-on TAM monitoring, and Sculptor as a helper rather than the builder. (Yakubson, Stojanovic)

---

## 4. Conflicts and stale advice

- Credit unit price. Tim says "one clay credit costs 32 cents" at [p8I_s91xfmc @7:34] and "3 cents" later in the same video [@15:27]; elsewhere he says 4 to 7 cents in 2025 [XsfrCYd_dRs @4:12]; Yash said about 7 cents on Starter and about 1.2 to 1.3 cents on Pro in 2024 [tDHdnCX2_ps @44:01]. All pre-change. Do not quote any of these.
- Plan names and gates. Pre-change videos say HTTP API and webhooks need the $314 Explorer plan and CRM integrations need the $720 Pro plan [vF6dL-Zdqk4 @1:39, @14:53]; Eric cites a $350 plan for own API keys [tM4nqus2L8w @10:16]; Lieben quotes 10,000 credits for $349 and 50,000 for $800 [C9aFa9kNENw @6:07]; Tim says Functions need the $800 plan [BpQU9gXYtC0 @22:12]. The post-change briefing says Starter and Explorer merge into Launch (quoted at $185 a month), Pro becomes Growth, and Functions come to all paid plans [WAYpwmZ4Agw @5:46, @5:57]. Treat every gate as unverified until checked on clay.com.
- "Bring your own keys and Clay is free." True in Eric's, Tim's and Tuwiner's pre-change advice [tM4nqus2L8w @7:33; p8I_s91xfmc @15:27; WAYpwmZ4Agw @3:06]; no longer true after March 2026 because Actions are charged regardless [WAYpwmZ4Agw @4:47; jEkDgA8hPmo @3:03]. Own keys still cut data cost, not the platform fee.
- Using HTTP API or Make to skip the native CRM integration to avoid a higher plan [vF6dL-Zdqk4 @14:53; Omp-obI8rkU @0:00]: the cost logic changes under Actions (CRM sync and HTTP calls may both count). Re-check before recommending.
- Clay vs Claude Code. Tim and Lieben cancelled their own agency Clay plans [XsfrCYd_dRs @13:54; MBrigXBfvHs @13:53]; Saruggia, Spychalski and Eric keep Clay for enterprise, CRM-touching and final-mile work [iHpXv0FmVoY @4:57; fHPfuDUiRSw @6:04; s2hShfYo7Wo @13:37]. Tim himself says keep Clay for RevOps and CRM work [XsfrCYd_dRs @11:49]. Reconciled view for Eva: Clay where CRM writes, compliance or visibility matter; agents for one-off list work.
- One AI column, many outputs. Eric's rule is one task per column [kFQfMZBo6Lo @10:41], yet he deliberately outputs four loose qualification checks from one column when precision does not matter [cbmZkHF9tfI @7:40]; Yash allows up to about five structured fields [tDHdnCX2_ps @6:05]. Rule of thumb: one judgment per column; several extractions are fine.
- Model choice. Eric uses the cheapest GPT mini model "for everything" [kFQfMZBo6Lo @14:31]; Yash uses a top model for creative or abstract tasks [tDHdnCX2_ps @47:01]. Model names in all pre-2026 videos are dated.
- Sculptor value. Lucero and Saruggia present it as a fast start [jEkDgA8hPmo @6:05; QfnNZc5J2mw @0:12]; Tim found it slower than manual and expensive per row [BpQU9gXYtC0 @19:57].
- Templates. Tim: do not build from other people's templates [p8I_s91xfmc @30:13]; Yash: Clay's own prompt templates are "relatively subpar", use as starting points [tDHdnCX2_ps @36:27]; Eric and Lieben share templates freely. Treat templates as references.
- Waterfall order. Wiza says put the most accurate provider first, not the cheapest (and names itself) [hY9vKVqptN0 @5:14]; Lucero puts providers he holds keys for first to save cost [jEkDgA8hPmo @22:19]. Choose by the customer's priority (coverage vs cost) and test.
- Functions history. Eric presented Functions as an enterprise beta [kFQfMZBo6Lo @4:24]; Tim later demoed it as shipped [6edc4r6bXOI @0:08]; Joe Rhew's write-to-table function tables with an external delay [y8oFBx1MaCA @49:22] predate native Functions and are now mostly unnecessary.
- Table size. Stan cites a 50,000 row cap per table that Audiences avoid [hXA8RIVfYOI @1:44]. Not confirmed elsewhere in this set; check current limits.
- Salesforce auth. Older tutorials use Connected Apps; per RedHawk BD these were retired for new orgs in March 2026 [Omp-obI8rkU @0:53].
- Clay partner referral terms. Yash (2024) cites 25 percent of a referred account's first-year revenue [tDHdnCX2_ps @33:23]; Lieben's guest (2026) cites a 20 percent affiliate kickback [MBrigXBfvHs @13:53]. Different programs and years; verify before relying on either.
- Native "find contacts by job title". Free and convenient [p8I_s91xfmc @19:48; jEkDgA8hPmo @9:07] but rated low on data quality by Lieben [C9aFa9kNENw @14:33]. Spot-check before outreach.

---

## 5. Sources added in this pass (30)

| File | Creator | Published (approx.) | Pricing freshness |
|---|---|---|---|
| eric-nowoslawski-largest-user-lessons-kFQfMZBo6Lo.md | Eric Nowoslawski | 2025-11 | PRE |
| eric-nowoslawski-save-money-clay-tM4nqus2L8w.md | Eric Nowoslawski | late 2024 to 2025-09 | PRE |
| eric-nowoslawski-8m-emails-claude-clay-s2hShfYo7Wo.md | Eric Nowoslawski | 2026-03 | Around the change |
| eric-nowoslawski-test-signals-3THIdISjTkk.md | Eric Nowoslawski | 2026-04 | Post |
| eric-nowoslawski-prompt-claygent-DJnwrD9-i30.md | Eric Nowoslawski | late 2023 to 2024-09 | PRE |
| eric-nowoslawski-lead-scoring-team-training-cbmZkHF9tfI.md | Eric Nowoslawski | late 2024 to 2025-09 | PRE |
| tim-yakubson-32-clay-tips-p8I_s91xfmc.md | Tim Yakubson | 2025-11 | PRE |
| tim-yakubson-clay-functions-6edc4r6bXOI.md | Tim Yakubson | late 2024 to 2025-09 | PRE |
| tim-yakubson-clay-workflows-UvFDcbmzPJQ.md | Tim Yakubson | 2026-09 | Post |
| tim-yakubson-cancelled-clay-XsfrCYd_dRs.md | Tim Yakubson | 2026-05 | Post |
| tim-yakubson-20-formula-checklist-EiVYuaLpNu0.md | Tim Yakubson | late 2024 to 2025-09 | PRE |
| tim-yakubson-sculptor-tutorial-BpQU9gXYtC0.md | Tim Yakubson | 2026-01 | PRE |
| michel-lieben-clay-feature-tier-list-C9aFa9kNENw.md | Michel Lieben | late 2024 to 2025-09 | PRE |
| michel-lieben-replaced-clay-claude-code-MBrigXBfvHs.md | Michel Lieben with Tim Yakubson | 2026-08 | Post |
| michael-saruggia-700-hours-clay-iHpXv0FmVoY.md | Michael Saruggia | 2026-09 | Post |
| michael-saruggia-5-features-2026-QfnNZc5J2mw.md | Michael Saruggia | 2026-02 | PRE |
| michael-saruggia-crm-job-changes-DHX8uoA53OI.md | Michael Saruggia | late 2024 to 2025-09 | PRE |
| matt-lucero-crash-course-2026-jEkDgA8hPmo.md | Matt Lucero | 2026-06 | Post |
| jacob-tuwiner-clay-pricing-change-WAYpwmZ4Agw.md | Jacob Tuwiner | 2026-04 | Post |
| patrick-spychalski-1-hour-tutorial-YLXzWpknuJk.md | Patrick Spychalski | late 2024 to 2025-09 | PRE |
| patrick-spychalski-gtm-engineering-leading-edge-fHPfuDUiRSw.md | Finn Thormeier / Patrick Spychalski | 2026-09 | Post |
| yash-tekriwal-claygent-neon-deep-dive-tDHdnCX2_ps.md | Clay University / Yash Tekriwal | late 2023 to 2024-09 | PRE |
| david-shamula-http-webhook-vF6dL-Zdqk4.md | David Shamula | late 2024 to 2025-09 | PRE |
| tanay-mishra-http-rate-limiting-48IjCJZXRMQ.md | Tanay Mishra | late 2024 to 2025-09 | PRE |
| joe-rhew-custom-hubspot-integration-qF2WPueIDN4.md | Joe Rhew | late 2024 to 2025-09 | PRE |
| redhawk-salesforce-http-api-Omp-obI8rkU.md | RedHawk BD | 2026-08 | Post |
| nathan-lippi-joe-rhew-function-tables-y8oFBx1MaCA.md | Nathan Lippi with Joe Rhew | late 2024 to 2025-09 | PRE |
| stack-and-scale-sculptor-build-f-H2kmtZHx4.md | Stack & Scale | 2026-01 | PRE |
| stan-stojanovic-clay-2026-updated-hXA8RIVfYOI.md | Stan Stojanovic | 2026-09 | Post |
| wiza-waterfall-enrichment-hY9vKVqptN0.md | Wiza | 2026-09 | Post |

Reading coverage: 28 of the 30 transcripts were read in full. The two long podcasts (fHPfuDUiRSw, Finn Thormeier with Patrick Spychalski; y8oFBx1MaCA, Nathan Lippi with Joe Rhew) were read through a keyword scan of the whole transcript plus the surrounding passages, so a few mid-video points unrelated to Clay administration may be missing. Full text of all 30 is saved.
