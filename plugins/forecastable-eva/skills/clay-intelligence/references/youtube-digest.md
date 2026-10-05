# YouTube Digest: Clay and B2B Event Strategy for Eva

Built 2026-10-04 for Eva (Forecastable partner-operations assistant). Source: 44 YouTube transcripts saved in `/home/claude/clay/youtube/transcripts/` (about 192,000 words). Every number below is attributed to the speaker who said it; none are independently verified. Timestamps are mm:ss into the video. Clay plan prices and features change often: treat anything priced as "as stated on that date" and confirm against clay.com before quoting to a customer.

Reading coverage note: 34 transcripts were read in full. For the 10 longest (Crossbeam 4 Wins, Crossbeam partner data webinar, Ring the Gong, Clay experts panel, Xavier Caffrey tutorial, Accelevents 116 meetings, Alison French, Grace Nicklas, Kayla Drake long-form, Nevara) the full text is saved but the digest was built from a keyword and number scan of the whole transcript plus the opening and closing sections, so a few mid-video points may be missing.

Contents
1. Clay fundamentals (13 videos)
2. Clay events workflows (9 videos)
3. Clay + Crossbeam / partners (7 videos)
4. Clay MCP and agents (5 videos)
5. Event strategy: pre, during, post, partner co-hosted, measurement (10 videos)
6. Cross-video patterns (15)
7. Conflicts

---

## 1. Clay fundamentals

### What is Clay? (Clay, official)
https://www.youtube.com/watch?v=v31hKg-WSCc
- Clay frames almost every workflow as four steps: Find, Enrich, Transform, Export ("FETE") (0:39).
- Positioning: "we're not a data provider, we're a data aggregator" plugging into 80+ sources at the time of recording (2:03).
- Waterfall enrichment checks multiple providers in sequence and charges Clay credits only for data successfully returned (2:22).
- Claygent (the AI research agent) covers data no provider has, "turns the entire web into your researching canvas" (2:41).
- Transform step = lead scores, categories, tags, personalized copy; Export = Zapier, Make, CRM, sequencers, dialers (2:58 to 3:14).
- Bring your own provider API key and Clay does not charge for that step of the waterfall (3:39).
- Eva use: explain Clay to a customer in FETE terms, then map their partner list or event list to each step.

### Clay Keynote: 3 Laws of GTM, Sculptor, Audiences, Sequencer (SCULPT 2025, Kareem Amin, Jeff Barg, Abbie Kouzmanoff)
https://www.youtube.com/watch?v=uyOxNMVcB2E
- Kareem's three laws: be unique ("GTM alpha"), anything you scale stops working, so the only sustainable advantage is finding new tactics faster (2:52 to 4:23).
- Examples of alpha data points: Canva messaging a head of design when the brand posts something off-brand; Rudder spotting execs going to a conference; Intercom sizing support docs for Fin (5:00 to 5:35).
- Claygent passed 1 billion runs, expected to double to 2 billion by year end (8:47); 150+ integration partners (9:06).
- Claygent connectors: Claygent can research your own Gong, Salesforce, Google Docs data; custom MCP tools live for enterprise, "later this fall" for others (10:22 to 11:01).
- Claygent Builder: versioned, workspace-level prompts you can iterate on "without spending credits" (11:40 to 12:37).
- Sculptor demo is literally an event workflow: "find VPs of marketing... and invite them to a happy hour this afternoon", refine to tenure over a year, add work email waterfall, recent news, then write the invite email (13:36 to 15:45).
- Signals and Web Intent: track ICP site visits, score accounts, Slack-alert the owner if assigned, else HubSpot nurture with Claygent personalization (ElevenLabs example, 17:57 to 19:20).
- Audiences: import millions of CRM records, merge by email, layer signals, push back to CRM; export rules "always write, never write, write only if empty" (21:14 and 26:36).
- Native Sequencer: inbox warming, rotation, human-in-the-loop AI replies, Slack alerts on replies (24:16 to 25:40).
- Eva use: a "sculpt_attendee" style CRM field plus an Audience is the native way to run event invites and follow-ups inside Clay.

### How Clay uses Clay for CX and Sales (SCULPT 2025, Jess Bergson and Ashley Artrip)
https://www.youtube.com/watch?v=B6hFkgyhNlE
- Stated growth: on track to over 8x revenue, 6x headcount, 0 to 250 enterprise customers (0:24).
- Out-of-home ABM: pulled SF office addresses of target accounts with Claygent, mapped them, placed billboards next to buyer buildings (4:36 to 5:40).
- Social listening: scrape reactions and comments on a LinkedIn post, enrich, ask Sculptor "how many are marketing qualified", Slack only high-propensity target account engagement (5:43 to 7:10).
- Product usage triggers for outreach: same enrichment run 500 times, nearing 50,000 row limit, inefficient credit use, behavior mirroring top GTM teams (8:56 to 9:15).
- CRM hygiene bot: days since last touch from Gong and email, Slack nudge to move the deal stage (10:09).
- Closed-lost analysis and sales-to-CX handoff: deal hits final stage, Clay pulls Salesforce plus Gong, writes a handoff object with use cases, red flags, promises made (11:00 to 14:30).
- Support enrichment: every Intercom ticket enriched with role, tenure as customer, tables live, pushed back as an agent note (15:08).
- Impact reviews (their QBR) drafted from usage data straight into Google Slides via a Slack command (19:24 to 21:10).
- Closing advice: ask "what is one thing my team spends a lot of time on that I can automate" and "one sticking point in my customer journey"; build two things (23:18).
- Eva use: the handoff and QBR patterns map to partner QBRs and partner-to-AE handoffs.

### Clay experts share their secrets (SCULPT 2025, Jordan Crawford, Petra, Patrick Spychalski, Eric Nowoslawski)
https://www.youtube.com/watch?v=ypmCZCsVNHU
- Jordan Crawford: "burn your sequences to the ground"; we design around what reps can do, not why buyers buy (0:21 to 1:43).
- Firmographic lists ("tech companies 50 to 500 employees") are the problem, not the copy (1:43).
- Inversion exercise: "What message would you send if you had unlimited time and perfect information?" then work backwards to the data (5:05).
- Data-led message examples: FAA proposed rule times number of affected engines to a dollar repair figure; idle crane detected from state transport permits (6:11 to 10:02).
- PQS, "pain qualified segment": redescribe the targeting back to the buyer as the reason for the message (12:15).
- Second speaker: a VP of Sales had a 28,000 account list after doing "everything by the book"; the fix was adding situational criteria (product-led, support friction) to prioritize (15:39 to 16:46).
- Eva use: for partner co-sell, the PQS is "you use Partner X and are hitting Y"; build lists from overlap plus a situational signal, not firmographics.

### The signals supercharging Cursor's GTM engine (SCULPT 2025, Jordan Topoleski and Roman Ugarte)
https://www.youtube.com/watch?v=50WD7eJzs34
- Stated: Cursor went from about $10M to $100M ARR in six or seven months in late 2024 with 24 people (3:52).
- More than half the Fortune 1000 already had developers using Cursor, so they went data-driven instead of hiring hundreds of reps first (5:17).
- "Patient zero" pattern: 3 senior engineers in a trial grew to 15, then 200, then 1,500 users within weeks (7:22).
- Thesis: "usage is more important than logos, which is more important than revenue" (14:35).
- TAM board built from Clay data plus job-description language scraping to find early-adopter clusters (for example LatAm neobanks) (12:01 to 13:40).
- Clay used for recruiting: Sales Nav list, enrich, score in Clay; their SF account executive TAM was about 5,000 people (17:20 to 18:43).
- Jordan: a 20% productivity gain equals about 2 hires early but about 15 hires at a 60 to 80 person GTM team, so hire faster (24:17).

### How OpenAI uses OpenAI with Clay (SCULPT 2025, Scotty Huhn and Conor Dragomanovich)
https://www.youtube.com/watch?v=TE-2VznRVjc
- At one point there were three custom GPTs per GTM team member: great energy, not scalable (3:50).
- Model: bottoms-up building plus a tops-down GTM innovation team that graduates the best workflows (5:57 to 6:40).
- Prioritization filter: is it strategic, is it repeatable, is it feasible (including training, QA, change management) (7:17 to 8:20).
- Objective stated: decouple revenue growth from headcount growth (10:35).
- GTM assistant in Slack: daily meeting brief with Clay enrichment, demo plan, recap, follow-up draft; reps say it frees about a full day per week (13:18 to 15:23).
- Support agent results stated: up to 70% ticket deflection, 29% solution rate, 78% positive human evaluation (17:50).
- Four-week sprint: week 1 pick the problem and name the user, metric, finish line; week 2 pair a builder with an operator and ship the smallest unit; week 3 measure and refine; week 4 evaluate (21:38).
- Eva use: this is the operating model for productizing Eva and Alex AI inside a customer.

### How Verkada Scales Outbound with Clay (GTM in GMT '26, Cody Leovic)
https://www.youtube.com/watch?v=z8BnIZwIsy4
- Thesis: the best GTM teams will win "by remembering what their buyers already told them" (first-party signals) (0:57).
- Third-party signals have an arbitrage window then decay through saturation (2:36 to 4:20).
- Stack: Clari transcripts, Salesforce data, email replies piped into Clay, then round-robin to SDRs via Outreach (2:17).
- Audience over copy: "if you need AI to write your email copy, then your message and your audience probably are not specific enough" (7:00 to 9:00).
- Future reach-out workflow: classify "reach back in January" replies, reason the date, sequence with their original email embedded; stated 33% reply rate (9:42 to 12:40).
- No-longer-at-company workflow: classify bounces and OOO replies naming a replacement, then sequence the replacement (12:49 to 15:00).
- Stale lead reactivation: one Clay table per past action (webinar attended, no-show, event attended) feeding one master sequencer table (15:10 to 18:24).
- Messaging rule: "one signal, one message, one reason for reaching out" (18:24).
- Eva use: event no-shows and "talk after the conference" replies are first-party signals to capture the same way.

### The ONLY Clay Tutorial You Need in 2025 (Xavier Caffrey)
https://www.youtube.com/watch?v=kY5E4wl8wlA
- Opens with "1,227 leads enriched in under 6 minutes using just two data sources" (0:00).
- States Clay gives access to 105+ data sources (1:11).
- Plans as stated at recording: Free with 100 credits per month; Starter $149 per month with 2,000 credits; a $349 tier with 10,000 credits he recommends for testing providers; Pro $800 per month with 50,000 credits and CRM integrations; Enterprise adds row limits and SSO (2:48 to 7:50). Verify current pricing.
- Most overlooked feature: testing providers against your own audience before committing (7:15).
- Native company search filters, including AI filters, used to shrink a list (9:34 to 11:13).
- Column types tour: enrichment, waterfall, formula (plain English), AI, HTTP API (13:27 to 15:38).

### Clay.com Beginner Walkthrough (Matt Lucero)
https://www.youtube.com/watch?v=HqdvpIGiOz4
- Typical gap: an Apollo export had emails for about half the people; run a second provider only where email is empty (3:44 to 5:20).
- Merge columns into one "work email" column, then validate via API (he uses a separate validator because it handles catch-alls) (5:20 to 6:20).
- Two-step AI: cheap model writes a long company summary, stronger model makes the fit decision from the summary (7:38 and 18:31).
- He states GPT-4o mini on your own key costs about a tenth of a cent per row (21:47).
- Conditional run formulas ("only run if work email is not empty") prevent wasted credits (15:53).
- Constrain outputs: "only output B2B or B2C, nothing else" so downstream filters work (23:10).
- Run 10 rows first; he made a prompt mistake live and caught it that way (24:00).
- His view: Clay's native "find people" data was weaker than other providers in his testing (9:30).

### I sent 10,000,000 cold emails and learned this (Clay channel, Eric Nowoslawski)
https://www.youtube.com/watch?v=CMndL5hNDbw
- About 30 emails per inbox per day, scale horizontally with more domains (0:21).
- Target 40 to 60% open rate as a deliverability check; under 1% overall reply rate means rebuild domains and copy rather than testing (0:53 to 1:58).
- Max three emails per sequence; email 1 performs best (2:00).
- Reuse the TAM every quarter instead of long sequences (2:40).
- "Golden ICP": waterfall signals in priority order (new company, then funded, then first-time CEO) and change the message by which ones are true (5:02 to 7:00).
- Five offers in the world: save time, make money, save money, raise status, live longer; test offers and the "so what", not CTA wording (7:52 to 8:30).
- Small TAM (under about 20,000): hit everyone on one channel, then the next, then direct mail last; threading gave only marginal lift in their test (8:31 to 10:30). <!-- VALIDATE-OK[economics]: channel-testing term quoted from a public video, not Forecastable economics -->
- "Recently joined company" was the best 2023 trigger; social signals (posted about a topic, engaged with content) were the best of 2024 (10:38 to 13:20).
- Email 1 structure: why you, why now; the offer; social proof; CTA (13:47).
- "Show your work": cite the source (Similarweb, Crunchbase) so wrong data is blamed on the source (19:02).
- Do not let AI write the whole email; keep static text and spend prompting effort on one line (21:10).

### How to use Clay with zero Clay credits (Tim Yakubson)
https://www.youtube.com/watch?v=8SOJiE4zZe0
- As stated: Starter at $149 per month for 2,000 credits works out to almost 8 cents per credit; an email waterfall can cost up to 3 credits, about 21 cents per verified email (0:43 to 1:20).
- Never pay credits for AI columns: add your own OpenAI or Anthropic key and select it in the column (1:45 to 3:40).
- Use an external email finder and validator through their Clay integrations or HTTP API (3:45 to 7:40).
- Use a router (OpenRouter) to pick the cheapest adequate model per prompt (7:40).
- Turn on auto-dedupe on a key column so the same person is never enriched twice (11:19).
- Spend credits intentionally, not by default (1:35).

### How to Enrich HubSpot with Clay Pt 5: Balancing Data Quality and Cost (Jacob Tuwiner)
https://www.youtube.com/watch?v=FFKuHzdVBcI
- Two enrichment models per customer: deep enrich (expensive, many fields, few records) and cost-optimized (few fields, many records) (0:55).
- Use deep enrich for an ICP study on customers; use cost-optimized for a 200,000 record prospect cleanup (1:10 to 3:00).
- Route by a HubSpot property, for example lifecycle stage = customer goes to deep, prospect or MQL goes to light (3:56).
- Clay's native HubSpot integration lacks granular overwrite rules, which is why they built a custom app (3:20).

### When to Use Claygent vs Regular AI (Eric Nowoslawski)
https://www.youtube.com/watch?v=I_F6S_CO5Og
- Claygent has internet access; regular AI columns do not (0:58).
- Never use Claygent to write a sentence that goes into an email, because you cannot train it with examples (1:24).
- Rule: one AI sentence needs at least 2 examples, preferably 3; anything more complex needs 5 to 7 examples (2:42).
- Regular AI fails without context ("Go Tylus" read as a travel site) and nails it when fed the homepage text (3:13).
- Do not ask Claygent to both research and judge "is this B2B SaaS"; research with Claygent, decide with an AI column trained on examples (5:00).

---

## 2. Clay events workflows

### How To Build Clay Table For Effective Event Outreach (vFairs with Patrick Spychalski, The Kiln)
https://www.youtube.com/watch?v=4UQmlUkv3-8
- Patrick: event outreach has been "some of the most successful that we've done", higher response rates and better conversations (1:33).
- Play 1, someone else's event: scrape everyone who posted about Dreamforce in the past two weeks (Apify keyword scraper), narrowed to about 500 ICP people (6:56 to 7:32).
- Use an AI column (Anthropic) to confirm the post implies they are attending, so you never message "I hate Dreamforce" posters (7:40 to 8:20).
- First line: "Saw your post about attending Dreamforce"; rest of the email static, offer was free product use for two months; client "did not have a free moment at Dreamforce" and turned down meetings (8:20 to 9:44).
- Play 2, your own event: 150 Series A companies in SF from Clay company search, find founders, enrich for profile picture URL (13:00 to 15:20).
- Generate a personalized image invitation (their photo on a "special GTM dinner" invite) via an HTTP API call to an image templating service, sent in a LinkedIn campaign (15:52 to 16:30).
- Finding companies and people in Clay is free; credits are spent on enrichment (13:10). Credits act as one currency across providers like HG Insights (17:14).
- Advice: run LinkedIn campaigns for events (higher conversion); in-person dinners with a select peer group get replies; be more creative in event outreach than in normal outbound (19:32 to 21:40).

### How to Fill Your Calendar Before You Even Get to the Conference (TMNKO)
https://www.youtube.com/watch?v=E9mcUH7NbjQ
- Trigify social listener on keywords (example: London Tech Week) fetches about 100 posts per day (1:50 to 2:30).
- AI step classifies whether the poster is attending; attendees are enriched and sent to Clay by webhook (2:35 to 3:15).
- Clay columns: company enrich, B2B/B2C, country, employee band, ICP score, competitor exclusion (5:30 to 6:20).
- Decision-maker check: if poster is a decision maker, find email; if not, search the company for CEO/founder then CMO (6:30 to 7:30).
- Opener branches: "I saw your post about attending London Tech Week" vs "your colleague posted about your team attending" (7:55 to 8:10).
- Runs daily and auto-enrolls new attendees into the campaign (8:12).

### I got 15 meetings after contacting 704 event attendees (Santiago Rojas)
https://www.youtube.com/watch?v=6utQE64RpP8
- Stated result: 15 meetings from 704 attendees contacted, all automated (title).
- Event app directories often list about 6,000 to 7,000 people with name, title, company; scrape with a browser data-scraper extension (0:46 to 1:45).
- Clay: split names with formulas, AI agent to separate title and company, Claygent for LinkedIn URL, website, company LinkedIn, then email (2:00 to 3:20).
- Fit routing: LinkedIn-fit, email-fit, or not a fit; reach out before the event and after to the people you could not meet (3:20 to 4:10, 6:30).
- Luma guest list: use Sculptor to create a column that visits each Luma profile URL and extracts LinkedIn, X, website, title, company where present (4:41 to 6:20).

### How to Extract and Qualify LinkedIn Event Attendees (Zacharias Xiroudakis)
https://www.youtube.com/watch?v=96rAORQLP4Q
- Use PhantomBuster's prebuilt "LinkedIn event guest export" on your own LinkedIn Event (his had 122 interested) (0:40 to 1:20).
- Connect PhantomBuster to Clay by API key as a source table (2:00 to 2:40).
- Formula columns: seniority keyword match (founder, CEO, CMO, head of marketing), function match, and a combined qualified checkbox (3:16 to 4:20).
- Company enrich (size, industry, country), Crunchbase funding, Claygent for B2B vs B2C (4:30 to 5:40).
- Claygent ICP qualifier outputs qualified or not qualified with its reasoning in a separate column so you can audit errors (5:45 to 7:00).
- Work-email waterfall last, only for qualified rows (7:00).
- Eva use: identical flow for a partner co-hosted webinar run as a LinkedIn Event.

### Event Lead Gen Campaign: 9 in-person meetings out of 141 contacted (Jim Ortiz)
https://www.youtube.com/watch?v=eWHSIPwbd1k
- Stated: 141 contacted, 9 in-person meetings at a payments industry event (EMVCo) over 3 weeks; 5 from email, 4 from LinkedIn (0:00 to 0:40).
- Scrape LinkedIn posts by event hashtag with an Apify LinkedIn post scraper (needs your LinkedIn session cookie) (1:00 to 1:55).
- Enrich person from post author URL, AI check that the post relates to the upcoming event, keep only those with email and ICP fit, push to the sequencer (2:00 to 2:50).
- Second table: scrape reactions on the organizer's announcement posts (likely attendees), same qualification (2:55 to 3:40).

### 23 High-Value Meetings Booked Before a Major Industry Event (Jim Ortiz)
https://www.youtube.com/watch?v=FTk5xMhJvHg
- Event-based ABM at Money20/20 (April 2025, Bangkok) for a payments security company (0:55).
- Pulled the exhibitor or attendee company list (available via the event newsletter), intersected with the client's 200 target accounts, kept only attending targets (1:35 to 1:55).
- Also scraped speakers, both as targets and as references for colleagues (2:00).
- Two-step email and LinkedIn sequence, CTA = coffee chat at booth 1018, follow-up 2 to 3 days later (2:36 to 2:50).
- Stated results: 4 meetings in the first three days; 23 over three weeks; 6 from email, 17 from LinkedIn (3:00 to 3:30).

### Turn webinar sign ups into pipeline (Danit Ben Simon)
https://www.youtube.com/watch?v=VL73oY_jOCo
- Luma has no API without a paid plan, so she had Claude Code build a browser automation to copy the guest list into Clay (0:31).
- Enrich LinkedIn URLs in Clay, push to a La Growth Machine campaign via its API key (1:00 to 2:30).
- Message is about the specific webinar by name, with the promised resource link, sent right after the session (1:05 and 2:40).

### Enriching event attendees with Claygent (Nnabuike Okoroafor)
https://www.youtube.com/watch?v=54IfXixLUHw
- Starting point: an attendee list with only first name, last name, company (0:25).
- Four-part Claygent prompt: mission, method, guard rails, benchmark for success (1:08).
- Guard rail: output must start with the LinkedIn URL format, no preamble (2:24).
- Benchmark: "if you're not at least 85% sure of your answer output the word unknown" so the AI does not invent (2:51).
- Stated: about 800 LinkedIn profiles found, down to company domain where the normal enrichment failed (3:30).

### How GTM Teams Turn Events into Pipeline (Bitscale GTM Clinic E2)
https://www.youtube.com/watch?v=bxcDVpQppMY
- Competitor tool, but the frame transfers to Clay: three problems are knowing who is attending, being visible before you meet, and knowing what to say (7:22).
- If the event does not publish attendees, use posts about attending the event as a proxy; schedule the search to rerun monthly as the event approaches (10:00 to 11:40).
- Two-layer qualification: company (US healthcare provider) then person (works in finance or revenue cycle) using LinkedIn profile text and an LLM (12:55 to 15:40).
- Get visible first: comment on target attendees' posts (or on influencer posts they engage with) before asking for a meeting (17:09 to 22:50).
- Know what to say: research signals per account (AI investment announcements, rising claim denial rates) with true/false outputs plus sources for audit (25:43 to 30:40).

---

## 3. Clay + Crossbeam / partners

No video found that demos Clay and Crossbeam together on screen; the closest is Bob Moore describing the integration play (below). This is a content gap worth filling (see creator registry watchlist).

### This CEO Reveals How Partnerships Unlock Growth (Sendspark, Bob Moore of Crossbeam)
https://www.youtube.com/watch?v=ZxJvNH3k42U
- Bob's framing: "partnerships died" and ecosystem-led growth replaced them; strategy must be aware of the whole ecosystem, not one-to-one relationships (0:48 to 6:30).
- At his previous company Stitch, he states 80%+ of revenue would not have existed without a pre-existing partner stack (5:14).
- Readiness 2x2: company scale vs "ecosystem DNA" (how much your core use case depends on other tools); low on both means wait (11:10 to 14:50).
- Free-tier first step: connect with many potential partners and share only rollup overlap stats before sharing names (17:25 to 18:30).
- The Clay play, in his words: use Crossbeam as a data source in Clay, pull only prospects that are customers of partner X, Y, Z (example 720 companies) with a column naming which partner (21:03 to 21:45).
- Then enrich titles and contacts in Clay, personalize by the partner stack (highlight the integration), and use it to qualify or disqualify ABM spend (21:45 to 23:10).
- Sendspark host adds: layer in joint case studies (customer using both tools) for relevance (23:10).

### 4 Easy Account Mapping Wins (Crossbeam, Sean Blanda and Chris Samila)
https://www.youtube.com/watch?v=kfziXln3_Xs
- Checklist: data source connected, standard populations (prospects, opportunities, customers), sharing defaults set (3:17 to 4:55).
- Custom populations are fine (Crossbeam splits free vs paid customers) (4:21).
- When vetting a partner, start by sharing overlap counts only (6:02).
- Get the mutual NDA in place before connecting (9:49).
- Customer-to-customer overlap sizes the integration market and supplies beta testers and case studies (11:27 to 13:20).
- Send overlap lists to HubSpot for integration-adoption campaigns (13:36).
- Eva use: this is the setup gate before any partner co-hosted event list can be built.

### How to Source and Convert Pipeline in HubSpot (Crossbeam Connector Summit '22, Shana Thompson)
https://www.youtube.com/watch?v=sAQqVAuwmsA
- Outbound HubSpot integration available starting at Crossbeam's Connector paid tier (at the time) (1:33).
- List creation needs HubSpot Professional; custom-object enrichment for workflows and reporting needs HubSpot Enterprise (1:51 to 2:29).
- Event play: save a report of "my prospects that are partner's customers" as ecosystem qualified leads, push it as a dynamic HubSpot list, invite them to a co-hosted webinar (2:44 to 3:30).
- Same mechanism for mutual-customer integration announcements, co-marketing webinars, fireside chats, co-sponsored happy hours (3:43 to 4:00).
- Use a HubSpot suppression list to keep the wrong contacts out (3:35).
- Reporting example: partner "Bezala" held 38% of overlaps, 178 accounts, used to justify more resources (5:55).
- Everflow (Ed Ceballos): governance matters, do not invite a client shared with another partner to the wrong partner's campaign; track intro requests per partner (8:35 to 11:30).

### Everything You Didn't Know You Could Do With Partner Data (Crossbeam, Olivia Ramirez and Matt Nicosia)
https://www.youtube.com/watch?v=C7XWgj-j67g
- Partner data must leave the PEP and reach the tools GTM teams already use (0:05 and 5:31).
- Do not ask CSMs to email every overlapping customer; narrow first using product usage plus partner data (4:58).
- Architecture shown: ETL into Snowflake, transform, reverse ETL (Census) back to Salesforce, HubSpot, Intercom (7:13 to 9:30).
- Partner data treated as "second party data" for segmentation (16:35).
- Everflow example: marketing and sales dashboards built on partner data to plan co-marketing (21:01).
- Integration adoption and churn: they cite Freshworks data that customers who adopt five or more integrations are 60 to 80% less likely to churn (25:56).

### Ring the Gong ep. 3: Channel Sales in the Age of Rev AI (Crossbeam and Gong panel)
https://www.youtube.com/watch?v=OQAkfYJYkDQ
- Panel: Chelsea Davis (Crossbeam), Rich Steves (Mountain Branch Consulting), Heatherly Booker (PTC Arena), Mike Davis (Gong).
- Process change lags the technology; reps use AI passively first, skills determine value (6:07 to 9:00).
- Direct sellers' expectations rise for what partners bring that GPT cannot pull off the web: relationships, capabilities, information (9:28).
- Pushback on "AI reps won't need partners": deliver "better together" value you can actually prove, not marketing stories (11:08 to 12:20).
- Let AI do what it does well so partner people spend more time on relationships (12:47).
- Eva use: frame partner events as the relationship layer AI cannot automate.

### Customer Referral Intelligence: Clay Intelligence Table Part 4 (FullFunnel, Matt Iovanni)
https://www.youtube.com/watch?v=wPQynTn15dI
- Pull customers, find all CRM contacts at them, ICP-filter by title (1:00).
- Get each contact's last three past employers (excluding current) (1:25).
- Score those companies hot, warm, cold against the fit rubric; find contacts with target titles at hot ones (1:40 to 2:20).
- Find overlap with your own team (same school, same past company) to choose who makes the ask (2:20).
- Output: Slack notification plus a CRM note with score (example 75 of 100), signal summary, recommended next step; outreach itself is deliberately not automated (2:40 to 3:30).

### heyBTW: Co-Marketing Event Attribution (Ben Roodman)
https://www.youtube.com/watch?v=t5rPVVcJ3CI
- Problem stated: partner co-hosted events, conference parties and multi-sponsor events are run on spreadsheets with no results measurement (0:05).
- Shared workspace per collaboration; each partner sees only its own collab (1:19).
- Sync attendees with HubSpot or Salesforce, enrich, mark MQLs (1:50 to 2:20).
- Multi-touch event attribution example: "took three events to build a relationship with Stripe" (2:30).
- Alert: "94 qualified leads from recent events haven't been contacted by sales" (2:52).
- Eva use: requirements checklist for Forecastable's Events module (per-partner permissions, CRM sync, uncontacted-lead alerts).

---

## 4. Clay MCP and agents

### Clay + Claude Code Now Builds Your Whole Outbound Workflow (Tim Yakubson, 2 months old)
https://www.youtube.com/watch?v=UC-UcXi9G9k
- Official Clay plugin for Claude Code installed from a GitHub marketplace via /plugins, then /reload-plugins (6:25 to 9:00).
- Skills exposed: ideation, setup and API key, CLI "workflows" (create Clay agents, triggers, scheduled runs), Clay API access to 100+ providers, credit optimization, feedback (9:10 to 10:40).
- The beta name was "Terracotta"; it is now called Workflows (11:20).
- Two rules before the first run: make Claude Code ask clarifying questions, and run 10 companies or contacts before the full run (14:10 to 15:00).
- Every run is visible as a Clay table or workbook in the Clay UI afterward (19:20).
- Tell Claude Code which providers to use with your own API keys so it does not spend Clay credits (20:34).

### Claude Code + Clay Makes Lead Generation Actually Fun (Nate Herk)
https://www.youtube.com/watch?v=zyvdl__Ywfk
- Pattern: Claude Code is the orchestrator, Clay is the data layer (0:15 to 1:00).
- Give Claude Code context files first (business profile, case studies, FAQs, offer, website copy) or copy quality suffers (2:00 to 2:40).
- He states a single-provider lookup might find about 30% of emails while the waterfall reaches about 80 to 90% (3:46).
- Install must be done in the Claude Code terminal, then authenticate the Clay workspace (5:10 to 6:50).
- Goal prompt run: 50 enriched HVAC leads with verified emails, pain points, subject and body; six sub-agents by city; took about an hour with verification passes (8:30 to 10:30).
- Stated cost: 172 Clay credits, about $12, for the 50-lead run (11:21).
- Import the CSV back into Clay, use Clay campaigns and buy pre-warmed domains capped around 30 sends per day (13:50 to 16:20).
- At recording the Clay MCP could not yet manage campaigns (17:00).

### How to Connect Clay with Claude Code (Tanay Mishra)
https://www.youtube.com/watch?v=hKFN-1QkG-c
- Connect Clay under Claude.ai Settings, Connectors, then authorize the workspace (1:40 to 2:35).
- Claude Code automatically inherits Claude.ai connectors; /mcp showed the Clay connector without separate setup (2:40 to 3:20).
- Example: "find me all the people who work at [domain]" then "get their emails", spending your Clay credits (3:20 to 4:30).
- Value: Clay lookups become one step inside larger agentic workflows triggered from other systems (0:55 and 4:40).

### You Can Now Use Clay INSIDE Claude (Hlib Storchak)
https://www.youtube.com/watch?v=ko1iHUuk3vA
- Official connector use cases: find email and phone for ICP contacts, research a target account, draft email copy, map buying centers, multi-thread deals (1:16 to 2:40).
- Demo: 10 most recent hires at a company; some results were role changes rather than new joiners, so verify (3:00 to 3:55).
- Copy drafted from a hiring trigger ("17+ sales and GTM roles in July") was usable but needed editing (5:40 to 6:40).
- His view: biggest win for individual SDRs and AEs, less new for agencies already fluent in Clay (7:20).

### Is Claude Code a Threat to Clay? No (Jordan Crawford, Blueprint)
https://www.youtube.com/watch?v=24GnpSB7Ivs
- Agents are powerful and fun but context drifts; you must track down what they did to know if it is right (1:00 to 1:30).
- He lost a database by loose instructions; agent mistakes can be large (3:30).
- Clay's value: you see what it is doing and see the errors; reliable runs across hundreds of thousands of CRM rows need that structure (3:50 to 5:00).
- Production workflow vs vibe-coded workflow is "a world of difference" (6:46).
- Eva use: agent for exploration and drafting, Clay tables for anything writing to a customer CRM.

---

## 5. Event strategy

### From 10x10 Booth to 116 Meetings: Pre-Show Strategy (Accelevents, Jonathan Kazarian and Michael)
https://www.youtube.com/watch?v=dnbla2Ix4VI
- Goal set by working backward from conversion rates and ACV: 100 pre-booked meetings (4:01).
- Result stated: 126 scheduled, about 10 no-shows, 116 held, up from 81 the prior year, in a 10x10 booth at IMEX (6:46).
- Offer drove booking: a Topgolf side event with about 212 to 215 registrants and an approval workflow to keep it ICP (7:20).
- List: event portal attendee export, Clay enrichment and filters; about 14,000 to 15,000 attendees, of which 20 to 25% fit ICP; about 3,200 DMs sent through the event platform (10:08 to 10:45).
- Owned the "ultimate guide to sidecar events" page for the show; it became their highest-traffic page in the 30 days before, with Topgolf pinned at the top (11:44 and 15:03 to 16:09).
- Executive outreach: AEs flag high-value prospects so the CEO and CRO send personal LinkedIn or email notes; test messages on a small batch before scaling (21:38).
- Pre-show timing: start 4 to 6 weeks out (6 for IMEX), warm the list with ads to past attendees (40:27 to 41:00).
- Booth: no demos at the booth, consultative conversation, book the follow-up on the spot; posture matters (standing, facing the aisle) (24:25 to 27:12).
- Every pre-booked contact pre-imported into HubSpot with notes reviewed in advance (49:25).
- Post-show stated: 46 follow-up meetings booked on site, more than half of the roughly 80 follow-ups that occurred (46:37 to 47:10).
- Messaging rule from the host: friendly, concise, relevant (45:30).

### How to launch a high-impact B2B field marketing strategy (Insightly podcast, Jon Kazarian, Accelevents CEO)
https://www.youtube.com/watch?v=OMbq3MhvqdI
- He sees events moving from about 25% to 35 to 40% of marketing budgets (0:55).
- Start with partners: Accelevents did 11 events last year, 9 or 10 so far this year, most co-hosted with 2 to 4 partners sharing cost and invites (6:52).
- Dinner target 25 to 30 prospects; all-in about $8,000 split across partners; cost per head with travel about $300 to $450 (7:20 to 7:40).
- Facilitate the dinner: a printed slip at each plate with one personal and one industry question, 30 seconds each around the table (8:40 to 9:10).
- Show rate for dinners about 90%; sidecar Topgolf at IMEX had about 275 applicants, 215 approved, about 100 showed (10:05 to 10:45).
- Sidecar rules: pick events with a high concentration of your ICP, avoid pulling people out of the main agenda, fill gaps like dinner, make it walkable (11:20 to 13:20).
- Topgolf cost about $52 per attendee plus bays (14:33).
- Make noise: every team member posts learnings on LinkedIn; hire a photographer for about $300 (split with partners); no videographer, people open up less (16:20 to 17:30).

### You're Wasting Money on Events (Sendspark, Kayla Drake, ex-Apollo field marketing)
https://www.youtube.com/watch?v=61cUlf_9ki8
- She usually adds field marketing last in the marketing cascade and joins companies around Series C (1:48).
- Event marketing = brand and net-new leads at scale; field marketing = localized ABM, roadshows, dinners to accelerate pipeline (4:00 to 5:20).
- Low budget: co-host with tech partners, let their field team run it, still get the lead list and floor time (5:44 to 6:20).
- Small dinners rose post-pandemic; executives prefer round tables of five or six over big happy hours (7:30 to 10:00).
- Apollo city selection: tier-one cities by marketable database and active users (11:30).
- Invite math: to get 200 registrations she sent about 6,000 invites, assuming 3 to 5% email open rate (12:26).
- Follow-up rules: one marketing touch to all attendees and no-shows within 24 hours; attended leads to AEs, no-shows to SDRs, sales follows up within the week (12:52 to 14:00).
- Partnered events: be selective, put partners on the mic, co-brand every reminder so leads expect outreach from both; share a follow-up schedule with partners (15:00 to 16:10).
- Quality over quantity: two or three events per month max per field marketer (18:22).
- ROI cadence: check Salesforce at 2 weeks, 1, 3 and 6 months; the 30-day to 3-month mark shows if it worked (21:39).

### How Field Marketing Drives B2B Growth (360 Marketing Show, Kayla Drake)
https://www.youtube.com/watch?v=j8-UPEo1Yx4
- Golden rule: every event should return 3x its cost in closed-won, even if open pipeline is 5 to 10x (7:49).
- Field marketers are "a salesperson without quota", aligned to territories (8:21). <!-- VALIDATE-OK[customer-name]: generic job title quoted from a public video, not a tenant -->
- Send attended leads to AEs and no-shows to SDRs (10:00).
- Attendees often post event photos, giving second-hand promotion before sales follows up (11:39).
- Start with one event marketing lead before field marketing; with low budget, start with partnered events (24:17 to 26:00).
- Apollo's portfolio included hosted series and many partnered events with shared costs (25:56).

### The Conference Playbook: Pipeline, Not Badge Scans (Sell Better)
https://www.youtube.com/watch?v=a_rruTm0Vo4
- Do not pitch early; the person who asks the most questions wins; good openers are about speakers and travel (0:27 to 1:30).
- Set "hats" (specific goals) before the show, for example 10 meetings or 3 new CEOs (1:36).
- Leave the booth; walk the floor for ideas (2:10).
- Capture notes: voice memo right after each good conversation; connect on LinkedIn on the spot and screenshot with notes (2:40 to 4:00).
- Take a photo with strong contacts and use it in follow-up (4:10).
- NFC tags (about 15 cents each) linking to a link page or a booking calendar instead of business cards (5:02).
- Block calendar time before leaving; tier contacts into a personalized tier-one sequence and a lighter tier-two sequence (6:25 to 8:00).

### Trade Show Strategy: Turn Conferences into Pipeline (Burn The Playbook, Alison French, LTO and ShowScout)
https://www.youtube.com/watch?v=8Psyov9MuU8
- Treat the show as a channel and compare it to other channels on qualified ICP contacts (14:54).
- She cites a client with 10 people at the event who walked away with 80 deals in three days after heavy pre-work (14:54).
- Pre-show starts about six weeks out with marketing and sales aligned on message and CTA (16:00).
- Post-show: automate a "sorry we didn't get to meet" note to everyone you did not meet (29:43).
- Arm booth staff with buyer intelligence: target accounts, which prospects from them are attending, head shots (31:20).

### How to Measure Event ROI for B2B SaaS (MyOutreach, Andy)
https://www.youtube.com/watch?v=gIjJtlVHgP4
- Cited stats: GWI says 85% of B2B buyers find events influential when considering a product; Freeman says 77% trust a brand more after an event interaction (1:05).
- Three levels: activity (scans), engagement (qualified conversations), pipeline and revenue; only level three answers "was it worth it" (1:58).
- Five metrics: cost per qualified conversation, pipeline created (30 to 60 days), pipeline influence, deal velocity, revenue closed (2:41 to 5:30).
- He states pipeline influence is typically 3 to 5x pipeline created for exec events (4:20); event-sourced revenue closes 60 to 180 days later (5:20).
- Setup: tag attendees as CRM campaign members before the event, define "qualified" with sales before, log conversations within 24 hours, fix the attribution window in advance, book 60 and 90 day reviews (5:30 to 7:00).
- Benchmarks stated: roundtables of 10 to 20 people, 3 to 5 opportunities, 5 to 8x pipeline to cost; roadshows of 40 to 80, 8 to 15 opportunities, 4 to 6x; 100+ person events, 2 to 4x (7:11).
- Below 3x pipeline to cost within 90 days, change audience, format, follow-up speed or sales engagement (7:39).

### Event Marketing Career Growth, ROI and Partnerships (Popl, Grace Nicklas)
https://www.youtube.com/watch?v=S2PFqMbOHN4
- Moved from content to events to an ecosystem role; events and partnerships "go hand in hand" (1:06 to 1:40).
- Partners are recruited for events because they bring their brands and audiences to the room (10:26).
- Mid-cycle acceleration: use partner relationships and events to move deals already in the sales cycle; that is what led to her partnerships title (10:59 to 11:31).
- Her LinkedIn connection list of brands and partners is her starting invite list (25:40).
- In e-commerce tech, everyone looks out for each other; partners route people to the right event (26:14).

### How Small B2B Brands Win With Community-Led Events (MAN DIGITAL, Shantanu Shekhar, Gong)
https://www.youtube.com/watch?v=vOo53YLWYnQ
- Gong shifted toward exclusive, smaller events and dinners for top accounts, for example RevOps dinners in London (22:50).
- For newer brands: find where the persona already congregates and sponsor that community's mini events; ROI is better because the audience exists (26:18).
- Prioritize mid-funnel over top-of-funnel and focus on customer outcomes rather than attribution (29:04).
- Enterprise: find the actual operator, not the CRO; a burning problem is required (32:00 to 34:30).
- Host suggests pop-up events next to big industry conferences to reach enterprise personas (36:44).

### Trade Shows Don't Generate Pipeline Anymore (Nevara)
https://www.youtube.com/watch?v=0Eg3Bx5wt7s
- Guest's stated example: about $180,000 total for one event (booth, sponsorship, swag, travel for 10 to 15 days) produced about 50 leads, at most 10 qualified, zero closed (3:54 to 4:29).
- Biggest mistake: not knowing what you want from the show; many staff do not know how to network without selling (0:00 and 6:09).
- Drop "sales" from your badge title; nobody wants to talk to a sales rep (9:26).
- Overstaffing is common (12 to 15 people sent when not needed) (11:35).
- Low budget: piggyback on partners and host a private event; have partners share it on LinkedIn (16:34 to 17:39).
- Well-run events release the attendee list one to two months ahead; poorly run ones a week before (20:24).
- Use other attendees' travel budgets: pull them into a side conversation near the conference; co-host with a partner (20:57 to 21:30).

---

## 6. Cross-video patterns (15 most repeated and proven)

1. **The event is won or lost before it starts.** Build the list and start outreach 4 to 6 weeks out (Accelevents, Alison French), run for about 3 weeks (Jim Ortiz twice), and set a meeting goal derived from conversion math (Accelevents: 100).
2. **Get attendees even when the organizer will not give them to you.** Event portal or app directory export (Santiago Rojas, Accelevents), Luma guest list (Santiago, Danit Ben Simon), LinkedIn Event guest export (Zacharias), people posting or reacting about the event (vFairs/Patrick, TMNKO, Jim Ortiz, Bitscale, Accelevents).
3. **Classify intent before you message.** An AI column confirms "this person is attending" (vFairs, TMNKO, Jim Ortiz) so you never message someone who said they are skipping.
4. **Qualify in two layers, company then person, and route.** ICP company fit, then seniority and function formulas or an LLM, then decision-maker fallback search (TMNKO, Zacharias, Bitscale, Santiago); Accelevents found only 20 to 25% of attendees fit ICP.
5. **Intersect the event with a target or partner account list.** Attendee companies x 200 target accounts (Jim Ortiz 23 meetings); prospects that are customers of partner X via Crossbeam as a Clay source (Bob Moore); Crossbeam ecosystem-qualified-lead lists pushed to HubSpot for co-hosted webinars (Crossbeam Connector Summit).
6. **Lead with an offer, not an ask.** Side event (Topgolf), dinner invite, coffee at booth number, free trial, owned guide to sidecar events (Accelevents, Jim Ortiz, vFairs, Jon Kazarian).
7. **Co-host with 2 to 4 partners.** Split cost, double invite reach, co-brand every touch so leads expect both companies' follow-up (Kayla Drake, Jon Kazarian, Nevara, Grace Nicklas, Gong).
8. **Small and intimate beats big and loud for pipeline.** Dinners of 25 to 30 at about $8K (Kazarian), round tables of 5 or 6 (Drake), exclusive dinners (Gong), roundtable benchmark of 5 to 8x pipeline to cost (MyOutreach) vs the $180K booth with zero closed (Nevara).
9. **LinkedIn is the event channel.** LinkedIn produced 17 of 23 meetings (Jim Ortiz), 4 of 9 (Jim Ortiz), platform DMs plus LinkedIn drove 126 bookings (Accelevents), and Patrick Spychalski says LinkedIn event campaigns convert higher.
10. **Short, specific, "why you, why now" messages anchored on the event.** "Saw your post about attending X" (vFairs, TMNKO); why you, why now, offer, proof, CTA (Eric Nowoslawski); friendly, concise, relevant (Accelevents host); one signal, one message (Verkada).
11. **Follow up inside 24 hours to one week, and book the next meeting on site.** 24-hour marketing touch, attended to AEs and no-shows to SDRs (Kayla Drake), 46 follow-ups booked at the booth (Accelevents), tiered post-show sequences (Sell Better), automated note to everyone you did not meet (Alison French).
12. **Instrument the CRM before the event and judge on pipeline at 30, 60, 90 days.** Campaign membership tagged ahead (MyOutreach, Accelevents pre-imported HubSpot), review at 2 weeks, 1, 3, 6 months (Drake), 3x rule (Drake on closed-won; MyOutreach on pipeline).
13. **Claygent researches, AI columns transform, and both need guard rails.** Claygent for live web data only; AI columns with 2 to 7 examples (Eric Nowoslawski); "85% sure or output unknown" (Nnabuike); constrain outputs to fixed labels (Matt Lucero); audit reasoning columns (Zacharias).
14. **Control credit spend structurally.** Test on 10 rows (Matt Lucero, Tim Yakubson in Claude Code), conditional run formulas (Lucero), dedupe (Yakubson), bring your own API keys (Yakubson, Lucero, Xavier), deep vs light enrichment by lifecycle stage (Tuwiner).
15. **First-party and partner data is the moat; third-party signals decay.** First-party reply and transcript signals (Verkada), Clay's own usage plus third-party data (How Clay uses Clay), Cursor's product usage, Crossbeam overlaps as second-party data (Crossbeam webinars, Bob Moore).

---

## 7. Conflicts

1. **Stack signals vs one signal.** Clay's keynote (Abbie Kouzmanoff) says acting on single signals "creates noise, not relevance" and pushes stacking signals in Audiences. Verkada's Cody Leovic says "one signal, one message, one reason for reaching out" and warns more data bloats personalization. Reconcile: stack signals to select and prioritize, mention one in the message.
2. **Should AI write the email?** Clay's Sculptor and Sequencer demos, Nate Herk and Tim Yakubson let AI write full subject and body. Eric Nowoslawski says do not use AI for the whole email, and Cody Leovic says needing AI copy means the audience is not specific enough.
3. **How to judge an event.** Kayla Drake ranks pipeline above brand and wants 3x closed-won per event; Accelevents wants each show "immediately profitable". Jon Kazarian says sidecar events like Topgolf build brand and future funnel, "it's not pipeline", and should not be judged on CPL. MyOutreach splits the difference with pipeline influence and a 3x pipeline (not revenue) bar within 90 days.
4. **When a company should start doing events.** Kayla Drake adds field marketing last and usually joins at Series C. Jon Kazarian, Nevara's guest and Gong's Shantanu Shekhar say early or small companies can start now by co-hosting with partners or sponsoring existing communities at low cost.
5. **Clay's own people data.** Nate Herk says Clay has "the best data" through its own set plus negotiated providers. Matt Lucero found Clay's native find-people data weaker than other providers in his tests, and Tim Yakubson calls the find-people waterfall a cost trap at over 20 cents and recommends an external provider.
6. **Pay Clay credits for AI and enrichment, or not.** Tim Yakubson: never spend Clay credits on AI columns, use your own keys and cheaper external finders. Nate Herk presents 172 credits (about $12) for 50 fully enriched leads as a bargain. Both can be true; volume decides.
7. **Agents vs Clay tables.** Tim Yakubson and Nate Herk show Claude Code building whole Clay workflows from one chat. Jordan Crawford argues agent context drifts and production CRM writes need Clay's visible, structured tables.
8. **Sidecar and side events.** Accelevents, Gong's host and Nevara promote side events next to big conferences; Jon Kazarian's own data shows heavy attrition there (about 215 approved, about 100 attended) versus about 90% show rate for hosted dinners.
9. **Threaded multichannel sequences.** Eric Nowoslawski found perfectly threaded email, call, LinkedIn, mail cadences gave only marginal lift and recommends exhausting one channel at a time. Accelevents and Bitscale run channels concurrently (DMs, LinkedIn, email, ads, social comments) to build presence before the event. <!-- VALIDATE-OK[economics]: channel-testing term quoted from a public video, not Forecastable economics -->
