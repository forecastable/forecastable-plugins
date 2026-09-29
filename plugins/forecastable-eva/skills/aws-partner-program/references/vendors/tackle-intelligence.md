# Tackle content intelligence
Built 2026-09-26. VENDOR source: operational detail, labeled; official pages win on conflicts.

Scope: Tackle (tackle.io, "an AppDirect company" since December 2025), maker of the Tackle Cloud GTM Platform (Offers, Co-Sell, Prospect), Tackle for Salesforce, the Cloud GTM Coach agent and Strategic Services. Tags `TK1` onward resolve in Sources. Cross-reference tags point to our files: `A` = aws-intelligence.md, `M` = microsoft-intelligence.md, `G` = google-cloud-intelligence.md, `X` = cross-cloud-intelligence.md.

Coverage achieved: full Yoast sitemap index walked on 2026-09-26 (158 blog URLs, 9 report, 35 news, 36 video, 41 webinar, 65 page URLs) [TK111]; every blog URL modified since 2025-07-01 fetched (51 posts, 48 published in window) plus 3 reports, 3 product-news items, the three cloud hubs and 8 product and company pages; 54 help center articles read from the help.tackle.io sitemap (189 URLs), prioritizing hyperscaler rules [TK65 to TK93]; the State of Cloud GTM 2025 microsite's chart data extracted from its JavaScript bundle (n = 83) [TK49]; YouTube @tackleio (184 videos) listed via TranscriptAPI and 11 transcripts pulled (all 10 program-relevant Cloud GTM XP 2026 sessions plus one 2025 channel session) [TK94 to TK104]. Author and team pages returned HTTP 403. No 2026 State of Cloud GTM report is published as of 2026-09-26, although Tackle's CEO said in May 2026 it would come out in June [TK100].

Label key: every TK fact is VENDOR unless marked. Where a hyperscaler employee speaks on Tackle's channel, the fact is marked "VENDOR channel, AWS/Microsoft/Google speaker": treat it as stronger than Tackle copy, weaker than a published official page.

---

## Ten takeaways that change how Alex or Eva advise

1. **Tackle is a Salesforce company, and its HubSpot story is thin.** Tackle for Salesforce is the product center of gravity (v2.5 February, v2.6 April, v2.7 May, v2.8 June 2026) [TK92]. Tackle for HubSpot, launched spring 2026, syncs only AWS ACE co-sells, one way (Tackle to HubSpot), into a custom CO_SELL object on a deal whose ID a user types into the Tackle form; no Microsoft, no Google, no private offers, and the HubSpot marketplace listing was still awaiting approval when announced [TK65][TK94]. For a HubSpot-run ISV, Tackle is a transaction and ACE tool with a HubSpot mirror, not a CRM-native co-sell workflow.

2. **The "20% to 32% of revenue through marketplace" headline is a mean from 83 respondents, and the median ISV is at 0 to 10%.** In Tackle's own chart data, 53 of 83 respondents (64%) put past-12-month marketplace revenue at 0 to 10%, and 19 of 83 still expected 0 to 10% the next year [TK49]. The sample skews large (27 of 83 at USD 501M to 1B+ ARR) and toward alliance roles (42 of 82 in Cloud Alliances) [TK49]. Use Tackle's averages as "top-heavy" signals, never as a peer benchmark for a Series B ISV.

3. **Tackle's respondents say marketplace is a commit-drawdown and speed tool, not a lead source.** 61 of 83 (73%) rate access to committed spend a significant or major benefit; 62 of 83 (75%) rate lead generation as no or minimal benefit; only 11 of 83 (13%) see significant lead-gen value [TK49]. Hyperscaler field engagement is the top blocker: 46 of 83 (55%) call engaging field sellers very or extremely challenging and 38 of 83 (46%) say the same of PDM attention, while only 15 of 83 (18%) find marketplace fees very or extremely challenging [TK49]. The advisory frame for a "no pipeline" ISV: fix field engagement, stop expecting the listing to generate demand.

4. **Tackle's AWS co-sell advice is now "triage, do not maximize the score."** Its Investment Checkpoint: extra effort only when the deal's segment and size justify it and it grows AWS service consumption; split "Collaboration Driven" deals (real better-together story, earn full sharpening) from "Program Driven" deals (credits or Marketplace transaction, baseline only) [TK1]. Partner-led is "the correct outcome for the majority" [TK1]. This matches our OQS read [A3][A87][A88] and gives Eva a two-question filter before rewriting ACE records.

5. **AWS ACE eligibility: Tackle's help center gives a different count than our file.** Tackle (updated 2026-01-21): Validated status, at least one solution with approved FTR, "ten submitted and validated co-sell opportunities in ACE," an active Partner Solutions Finder listing, ACE terms accepted [TK67]. Our file cites Labra's summary of a 2023 FAQ: 15 validated opportunities for Software [A108]. Both are vendors paraphrasing a login-gated FAQ; the Tackle page is newer. Tell customers "10 to 15, confirm in the ACE FAQ in Partner Central."

6. **MPOPP has an operational trap Tackle has automated: link the accepted offer at launch.** Tackle says offer association at the moment the ACE opportunity moves to Launched "is critical for qualification" and now auto-links the last accepted offer; it also surfaces the MPOPP wallet balance and one-click MPOPP applications from Salesforce via the Partner Central Benefits API [TK14][TK18][TK94]. CrowdStrike's alliance lead calls MPOPP a time-bound "compelling event" and negotiating chip for sellers [TK99]. Add "offer linked before Launched" to Eva's close checklist [A31][A95].

7. **Several Tackle pages still teach retired rules; do not let customers copy them.** Google: the May 2026 guides say register in "Partner Advantage" under the "Build Engagement model" [TK7][TK8], and the help center says Google Marketplace SaaS counts toward commit "up to 50% of their total commit" [TK73], against the official 25% cap [G22]. Microsoft: "IP Co-sell Incentivized," "Partner Sales Connect" and Marketplace Rewards as a live program [TK11][TK22][TK3], all pre-FY27 language [M30]. AWS: ACE via S3 buckets "remains widely used" [TK38] (S3 is deprecated [A47]); ISV Accelerate gives "reduced listing fees" [TK35] (fees are tiered by TCV for everyone [A24]); each help FAQ says marketplace fees depend on "the seller's relationship" [TK73][TK78][TK80].

8. **Microsoft and Google executives used Tackle's stage to preview program changes.** Google's Dai Vu (May 2026): Google is redesigning its deal registration platform for co-sell across ISVs, channel partners and Google; MCCP will add variable credits and pay-as-you-go contracts; a distributor channel private offer pilot (DCPO) is running; AI-category GTV grew 18x year over year and total GTV doubled 2024 to 2025 [TK97]. Microsoft's channel speaker (May 2026): roughly 40,000 MACC-eligible solutions, channelled Marketplace sales up 3x in a year, Marketplace revenue doubled three years running [TK96]. None of these are on official pages we hold; treat as announced, not live.

9. **The operating model that works at scale is rep-led co-sell inside the CRM, with alliances as enablers.** Datadog: a "co-sell with cloud provider" button on every Salesforce account page (AWS, Azure or Google) produced the first year with more partner-originated than AWS-originated opportunities; KPIs are sourced opportunities to stage 2, new logos with "active influence," and sourced net-new ARR; cloud alliances sits inside MEDDPICC as the "partner champion" [TK98]. CrowdStrike: sellers tag AWS on an opportunity exactly like CDW or SHI, and automation creates the ACE record; nobody logs into ACE [TK99]. Honeycomb: CRO declared "marketplace first" at SKO with propensity scores in hand [TK102].

10. **Tackle is being folded into a bigger AppDirect distribution play; watch roadmap focus.** AppDirect announced the Tackle acquisition on 2025-12-01 (price undisclosed; Tackle then cited USD 20B+ processed, 150 staff) [TK105][TK23], bought PartnerStack on 2026-04-14 (reported at upwards of USD 150M) [TK106][TK107], and Tackle now pitches syndication to about 400 AppDirect marketplaces, Firstbase storefronts, PartnerStack affiliates and devs.ai agents [TK94][TK100]. Its public AWS Marketplace listing prices the Platform from USD 22,500, Co-Sell from USD 20,000 and Prospect from USD 12,750 per 12 months, plus services [TK64]. Stated agent strategy is "headless" (APIs, SDKs, MCP servers) but no public Tackle MCP server was found as of 2026-09-26 [TK94].

---

## 1. Vendor profile (VENDOR throughout)

| Dimension | Detail | Source |
|---|---|---|
| Company | Founded 2016 (Boise); founders Dillon Woods (Founder/CTO), Brian Denker (Founder/COO); CEO John Jahnke ("GM of Tackle" in September 2026 release); CRO Jake Simpson; VP Product Adam Boyle | [TK19][TK59][TK2] |
| Ownership | Acquired by AppDirect: announced 2025-12-01, "expected to close within 7 days," price not disclosed. Tackle describes itself as "an AppDirect company." AppDirect then acquired PartnerStack (2026-04-14; 138,000+ partners; BetaKit reports upwards of USD 150M). Earlier VC backers named on YouTube: a16z, Bessemer, Coatue | [TK105][TK19][TK106][TK107][TK110] |
| Scale claims | USD 20B+ marketplace transactions processed; "hundreds of thousands of AWS co-sell submissions"; 52,000+ accepted offers; 450 customers; 150 staff (November 2025). "Over 400 APN members" supported (September 2026) | [TK23][TK59][TK2] |
| AWS relationship | Strategic Collaboration Agreement with AWS (2025-11-07); AWS Marketplace co-launch partner for Concurrent Agreements, Self-Service Billing Adjustments and Cancellations, AI Agents and Tools; launch 3rd Party Integrator in AWS's 3PI PDM pilot (2026-09-02); offers Partner Central migration services | [TK23][TK13][TK10][TK54][TK2][TK18] |
| Clouds | AWS, Microsoft, Google Cloud (listings, private offers, co-sell). AppDirect network adds about 400 non-hyperscaler marketplaces and Firstbase storefronts | [TK60][TK94] |
| Products | Tackle Offers (listings, direct and partner private offers, amendments, bookable artifacts, Contracts); Tackle Co-Sell (ACE, Partner Center Referrals, Google Partner Network Hub registrations); Tackle Prospect ("Cloudographic" propensity data, 150+ factors, High/Medium/Low by marketplace); Revenue Insights (in Salesforce, from December 2025); Payments, Data Feeds and Insights; APIs (Invoicing, Disbursement, Subscription, Metering); Cloud GTM Coach (formerly GTM Agent) on Salesforce Agentforce, listed on AgentExchange | [TK61][TK60][TK88][TK18][TK52][TK53][TK13] |
| CRM integrations | Salesforce managed package (deep: field mapper, auto-create/sync/close/accept for AWS, Microsoft referral automation, Google co-sell GA June 2026, bulk co-sell, custom objects, report types, OQS fields in v2.8). HubSpot: AWS co-sell only, one-way sync to a CO_SELL object (help article 2026-04-08) | [TK92][TK30][TK4][TK65][TK94] |
| AWS API coverage | Partner Central Selling API (legacy S3 connection upgrade path), Benefits API (MPOPP applications), Partner Central agents (pipeline insights, next steps, funding recommendations for MAP, POC, MPOPP, WMP), Marketplace Catalog API (all listing types in preview: AMI first), SDDS data feeds, Concurrent Agreements, EPO, offer sets |[TK18][TK13][TK68][TK69][TK75] |
| Microsoft API coverage | Partner Center Referrals API (Tackle user needs Referral Admin and Developer roles), MPO create and import, non-USD private offers (June 2026), auto-activation and 1 to 120 month terms (July 2026), bulk co-sell up to 200 opportunities | [TK89][TK84][TK79][TK20] |
| Google API coverage | Partner Network Hub co-sell via the Integrator role (Google's "two-way API"), co-sell GA in Salesforce June 2026; Google direct private offers limited to new, flat-rate, flat-rate-with-usage and installment offers (no consumption-only, no amendments); MCPO associate-only (cannot create from Tackle) | [TK82][TK94][TK4][TK72][TK81] |
| Agentic / MCP | Cloud GTM Coach (Agentforce) live with customers; integrates AWS Partner Central Agent; "headless" strategy to expose features through APIs, SDKs and MCP servers (stated May 2026); devs.ai agent builder free to Tackle customers. No public Tackle MCP server found | [TK94][TK13][TK4] |
| Pricing | Public AWS Marketplace listing: Tackle Platform from USD 22,500 per 12 months "plus services"; Tackle Co-Sell from USD 20,000; Tackle Prospect from USD 12,750; 12, 24, 36 month terms; USD 0.01 per unit overage dimension. Price scales with marketplace revenue, accounts scored and co-sell partners; annual or multi-year, upfront or annual payment. Pre-February 2023 plans were per listing | [TK64][TK87] |
| Services | Advisory Services, Cloud GTM Success (named success manager), Co-Sell Managed Services, PLG Advisory, Launch Services, 24/7 premium support for end-of-quarter | [TK63][TK58][TK87][TK18] |
| Customers named | CrowdStrike, HashiCorp, New Relic, Snyk, Datadog, Salesforce, Redgate, PagerDuty, Asana, Grammarly, Starburst, GitLab, Honeycomb, Seeq, Jamf, Infor, Kasada, ClickHouse, Forter, Fastly, Datometry, Bugcrowd; reseller WWT | [TK2][TK23][TK53][TK98][TK99][TK101][TK102][TK103][TK104] |
| Events and research | Cloud GTM XP (fifth year, virtual, ~May 2026, replays on YouTube); State of Cloud GTM report (sixth edition October 2025); AppDirect Thrive (in person, September 2026, Los Angeles) | [TK10][TK100][TK94][TK29] |

Strengths: deepest AWS co-launch cadence of any vendor we track (Concurrent Agreements, billing adjustments, AI Agents, 3PI pilot); Salesforce-native automation across all three clouds; real transaction volume behind benchmarks; hyperscaler executives appear on its stage; bookable artifacts for finance.

Weaknesses: HubSpot support is minimal; Google private offer creation is partial (no consumption-only, no amendments, MCPO associate-only); Tackle Microsoft checklist predates Frontier Accelerate; several marketing and help pages carry retired program names; no published MCP server; AppDirect integration may pull roadmap toward storefronts and affiliates.

Bias to watch: every benchmark is from Tackle's customer base or its own survey (large, alliance-heavy, already marketplace-committed); "consolidate onto one platform" is the recommended fix in every customer session [TK101][TK102]; case-study numbers (353% growth, 25x ROI, 5x close rate) are single-customer and unaudited [TK33][TK56][TK57].

---

## 2. AWS: extracted substance

| Fact | Status | Our tag | Vendor tag | Date |
|---|---|---|---|---|
| Every submitted ACE opportunity is scored in real time and rescored on meaningful update; lands in Partner-Led (default for most), Agent-Engaged, or AWS Field-Engaged (reserved for highest readiness and strategic value) | CONFIRMS | [A3][A75] | [TK1] | 2026-09-25 |
| OQS, motion and recommendations can reach partners by email and Slack "where connected," not only the console; only after you integrate | NEW (Slack delivery not in our files) | [A3] | [TK1] | 2026-09-25 |
| Baseline submission: business problem naming current environment, problem, impact and the AWS ask; next step with action, owner, named customer contact and date; tag only AWS services the customer is adopting or expanding | CONFIRMS | [A3][A43] | [TK1] | 2026-09-25 |
| Tackle for Salesforce v2.8 shows Co-sell Motion, OQS and OQS Trend on Salesforce opportunity records | CONFIRMS | [A47] | [TK92][TK1] | 2026-06-30 |
| ACE eligibility: Partner Central account, ACE T&C, Validated status, at least one solution with approved FTR, 10 submitted and validated co-sell opportunities, active Partner Solutions Finder listing | CONFLICT (15 per our vendor source) | [A108] | [TK67] | 2026-01-21 |
| ACE requires APN "Standard, Advanced, or Premier tier" and submitted customer reviews | STALE (tiers replaced by Partner Paths in 2022) | [A21] | [TK47] | 2025-07-02 |
| Choosing "Do Not Need Support" (For Visibility Only) "does not trigger AWS incentives"; MRR, SaaS status and marketplace transaction info affect SaaS Co-Sell Benefit eligibility | CONFIRMS (incentive nuance NEW) | [A42][A79] | [TK47] | 2025-07-02 |
| MPOPP: associating the accepted private offer to the opportunity at launch "is critical for qualification"; Tackle auto-links the last accepted offer at launch (February 2026) | NEW (not on AWS MPOPP page we hold) | [A31][A95] | [TK14] | 2026-02-27 |
| Required AWS product associations can be auto-applied at co-sell launch | CONFIRMS | [A95] | [TK14] | 2026-02-27 |
| MPOPP wallet balance per funding account and MPOPP applications submitted from Salesforce via Partner Central Benefits API; Salesforce preview targeted end of Q2 2026 | CONFIRMS (Benefits API) / NEW (wallet mechanics) | [A48][A31] | [TK18][TK94] | 2026-05 |
| Partner Central agent capabilities surfaced in Tackle Coach v1.4: pipeline insights (lost-deal trends, partner history by customer, stale or flagged opportunities), next steps evaluated against AWS standards, funding recommendations for MAP, POC, MPOPP, WMP | CONFIRMS | [A105][A46] | [TK13] | 2026-03-18 |
| AWS Marketplace features 6,000+ unique ISVs and 4,000 channel partners | NEW | none | [TK2] | 2026-09-02 |
| 3PI PDM pilot: AWS uses third-party integrators to give a cohort of ISVs 1:1 onboarding and co-sell guidance; Tackle is a launch 3PI | CONFIRMS | [X33a] | [TK2] | 2026-09-02 |
| Private offers up to 144 months across all product types including SaaS contracts (May 2026) | CONFIRMS | [A57] | [TK79] | 2026-05 |
| Buyer-country restriction on private offers; INR-disbursement accounts locked to India | CONFIRMS | [A52] | [TK79] | 2026-04 |
| Custom net payment terms (Net 15, 30, 45, 60, 90, 120) on offers with a payment schedule (SaaS, ProServe, AMI); resellers can shorten, not extend, ISV terms | CONFIRMS | [A55] | [TK79][TK85] | 2026-08 |
| Self-service billing adjustments: approved adjustments issued as AWS credit; PENDING up to 72 hours; credit memo invoice generated | NEW (not in our files; unverified on AWS docs) | none | [TK79] | 2026-08 |
| Seller-initiated contract cancellation: buyer has 7 days to respond; auto-accepted if no action; seller can withdraw before response | NEW (unverified on AWS docs) | none | [TK79] | 2026-08 |
| Refunds and cancellations now go through AWS Marketplace > Sell > Agreements; requests via the Marketplace Support Center console are rejected | NEW | none | [TK80] | 2026-06-10 |
| Concurrent Agreements opt-in path: AMMP Contact Us > Commercial Marketplace > Product Configuration / Integration > Concurrent Agreement Opt-in; test with $0 private offers on named buyer accounts; test metering if listing meters; capture LicenseARN and Agreement ID; enabling "cannot be rolled back" | CONFIRMS (feature) / NEW (steps) | [A101] | [TK74] | 2026-03-03 |
| Express Private Offers: stacked rate-card discounts multiply (10% TCV and 5% buyer-profile = 14.5%, not 15%); buyer-profile answers are self-reported and not verified by AWS; consumption portion of contract-with-consumption products is not discounted; typical validity 7 to 14 days; rate card edits apply only to new requests; 0% max discount allowed for speed-only | NEW (detail beyond our A54) | [A54] | [TK68] | 2026-08-12 |
| Offer sets: 2 to 7 private offers, one per product; SaaS, AMI, containers, professional services, AI/ML; excludes public, amendment/replacement and free-trial offers; same buyer account, currency and expiration; each product becomes its own agreement; seller of record is whoever assembles the set (the reseller in resale); one resale authorization per product; ISV-distributor-reseller-buyer (four-party) deals fall outside offer sets | NEW (detail beyond our A60) | [A60] | [TK69] | 2026-08-12 |
| Private offer currencies USD, AUD, GBP, CAD, EUR, INR, JPY when enabled in disbursement preferences; each currency to a single bank account; reseller must have the same currency configured to create an offer from a resale authorization | CONFLICT on CAD (official list has no CAD); rest CONFIRMS | [A56] | [TK70] | 2026-01-09 |
| Contract-with-consumption and usage offers in EUR, GBP, AUD, JPY for direct and partner offers | CONFIRMS | [A56] | [TK27] | 2025-10-29 |
| Buyers are invoiced on the 3rd of the following month unless a flexible payment schedule applies; monthly disbursement covers payments made in the prior month, "the 20th is the cut-off date" | NEW (unverified) | [A56] | [TK80] | 2026-06-10 |
| AWS disbursement is "a monthly cycle" issued as "a single payout" | CONFLICT (AWS offers daily or monthly) | [A56] | [TK52] | 2026-09-23 |
| Private offers cannot be auto-renewed; public subscriptions default to auto-renew | NEW | none | [TK80] | 2026-06-10 |
| Future-dated agreement private offers: no integrated AWS notification until the agreement start date; for reseller FDAs Tackle cannot confirm acceptance before start | NEW | none | [TK80] | 2026-06-10 |
| Professional services and BYOL listings do not count toward commit drawdown; SaaS does | CONFIRMS | [A38][A60] | [TK80] | 2026-06-10 |
| EDP "customers typically need to commit at least $1M annually" | NEW (VENDOR; contract term, unverified) | [A38] | [TK26] | 2025-10-28 |
| Marketplace fees "can be dependent on the seller's relationship" with AWS | STALE (fee schedule is published) | [A24] | [TK80] | 2026-06-10 |
| ISV Accelerate brings "reduced listing fees on AWS Marketplace" | CONFLICT (fees tiered by TCV for all sellers) | [A24][A1] | [TK35] | 2025-09-11 |
| MDF "typically AWS matches 50%" / reimburses "up to 50% of eligible spend"; Well-Architected ISV funding for FTR completers who address at least 25% of high-risk items; POA funding for strategic deals | NEW, `[UNVERIFIED, VENDOR, source dated 2025-09]` | [A65][A68] | [TK35][TK32] | 2025-09 |
| ACE data exchange via S3 buckets "remains widely used" | STALE (S3 deprecated, closed to new users) | [A47] | [TK38] | 2025-08-20 |
| CPPO expanded as "Consulting Partner Private Offer" | STALE (now Channel Partner Private Offers) | [A53] | [TK38] | 2025-08-20 |
| CPPO money flow: ISV sets wholesale price, partner adds markup, AWS bills, collects tax and disburses to both; supported for SaaS; accepted CPPOs cannot be canceled; only "Offer created" CPPOs can be canceled and only by the partner before extension | CONFIRMS (flow) / NEW (cancel rules) | [A53] | [TK40][TK85] | 2026-09-24 |
| Tackle creates and imports only single-use resale authorizations; multi-use authorizations must be managed in AMMP; renewal flag on partner offers qualifies for reduced renewal fees | CONFIRMS (renewal fee) / NEW (tool limit) | [A24][A53] | [TK85] | 2026-09-24 |
| Dimensions added in a private offer are added to the product permanently; up to 200 dimensions per product; new usage dimensions only via listing edit | CONFIRMS | [A57] | [TK85] | 2026-09-24 |
| AI Agents and Tools listing paths (July 2025): add AI categorization to existing listing, new API-based SaaS listing, or container-based listing in the buyer's account; launch partners reviewed "within hours" | CONFIRMS | [A27][A58] | [TK54] | 2025-07-16 |
| AWS Marketplace Seller Prime exists as an AWS PLG program (named by AWS Marketplace PLG lead) | CONFIRMS existence of [A86]; amounts still UNVERIFIED | [A86] | [TK95] | 2026-05 |
| Successful PLG ISVs on AWS Marketplace see 40%+ free-to-paid conversion; one self-service buyer grew into a private offer over USD 20M | NEW (AWS speaker, VENDOR channel) | none | [TK95] | 2026-05 |
| Forrester TEI of AWS Marketplace: deals 81% larger, 27% more likely to close, 40% faster than direct; nearly 80% of partners view AWS Marketplace as critical to co-sell; 40% of ISVs struggle to communicate joint value proposition | NEW (study not in our files; our A5 cites a different Forrester channel study) | [A5] | [TK15] | 2026-01-27 |
| Honeycomb's AWS SCA (signed Q4 2025) bundled MDF, POC credits and MPOPP; WWT's AWS SCA includes an ACE opportunity creation metric | CONFIRMS (SCA negotiated) / NEW (contents) | [A46][A71] | [TK102][TK104] | 2026-05 / 2025-05 |
| AWS-originated referrals (AOs) at Datadog were largely logged renewals under the SaaS revenue program; value comes from converting them into expansion, not from volume | NEW (practitioner) | [A79] | [TK98] | 2026-05 |
| PSMs are goaled on getting partners to the right AWS people and on Marketplace; ask each PSM for territory and account list; engage PSM groups for reputation, not deals | NEW (tactic) | none | [TK45] | 2025-07-10 |
| AWS support tickets for ACE CRM issues: Partner Central Contact Support > ACE Leads and Opportunities > CRM Integration (Alliance Lead role) | NEW (menu path) | none | [TK67] | 2026-01-21 |

---

## 3. Microsoft: extracted substance

| Fact | Status | Our tag | Vendor tag | Date |
|---|---|---|---|---|
| Co-sell ready: PartnerID, business profile per region under Referrals, Co-sell > Solutions configured (needs Co-sell solutions administrator), sales contact per geography. Azure IP co-sell eligible: USD 100K ACR trailing 12 months or USD 100K billed revenue for transactable offers; primarily platformed on Azure; reference architecture diagram; new offers transactable since 2023-07-11 | CONFIRMS; STALE by omission (no Frontier Accelerate enrollment prerequisite) | [M1][M30] | [TK66] | 2025-09-15 |
| Co-sell eligibility is "$100,000 in trailing 12 months in marketplace billed sales or Azure consumed revenue" | CONFIRMS | [M1] | [TK96] | 2026-05 |
| Tackle Microsoft blogs describe "IP Co-sell Incentivized" status, "Partner Sales Connect" and Marketplace Rewards as current | STALE | [M30][M44] | [TK11][TK22][TK3] | 2026-04 / 2025-11 / 2026-09 |
| Only listings showing "MACC Enrolled" burn down commitment; the invoice date decides which calendar year a purchase counts toward | CONFIRMS (per-offer enrollment) / NEW (invoice-date rule) | [M43] | [TK78] | 2026-01-27 |
| About 40,000 eligible solutions with a 100% match to MACC, "no limit" | CONFIRMS (100% no cap) / NEW (count) | [M36][M94] | [TK96] | 2026-05 |
| Unspent MACC concentrates in Microsoft Q4 (April to June); confirm MACC eligibility with the PDM before procurement | CONFIRMS | [M13] | [TK22] | 2025-11-12 |
| Microsoft Marketplace: 140+ geographies, 17 currencies, tax managed in 50+ geographies, 500,000 partners; channelled sales up 3x in the past year; Marketplace revenue doubled each of the past three years and on pace to triple; 75% of software companies report larger deals; Omdia forecasts over 50% of marketplace revenue channelled by 2030 and a USD 300B partner opportunity | NEW (Microsoft speaker, VENDOR channel); Omdia 50% CONFIRMS | [X40] | [TK96] | 2026-05 |
| Resale enabled offers announced at Ignite November 2025; ISV enrolls, publishes, selects channel partner | CONFIRMS | [M37] | [TK96] | 2026-05 |
| Private offers: custom durations 1 to 120 months (or 1 to 10 years), auto-activation, renewal settings (July 2026 API update) | CONFIRMS | [M13][M34][M17] | [TK79] | 2026-07 |
| Payment schedule: 1 to 70 payments; an initial charge is required at subscription (can be $0); flat-rate only (not per-user); terms over 1 month; per-year model only for multiples of 12 months; "Renew into private offer" unavailable when a payment schedule is used | NEW | [M34] | [TK71] | 2026-07-20 |
| Non-USD private offers: currencies limited to markets on the public plan; Microsoft requires local-currency pricing for each configured market | NEW | none | [TK71][TK79] | 2026-06 |
| Buyer acceptance needs EA Admin or Billing Account Owner to accept terms and Owner or Contributor on the Azure subscription to subscribe; plan must exist in buyer's market; retired plan greys out Purchase; advise buyers to set Recurring Billing Off unless agreed | NEW (vendor paraphrase of Microsoft docs) | none | [TK78] | 2026-01-27 |
| CSP-managed buyer accounts may be unable to buy a SaaS listing; fixes: separate non-CSP account (re-target the offer), customer-led CSP offer with owner permission, or go direct | CONFIRMS (CSP limits) / NEW (fix paths) | [M93][M36] | [TK78] | 2026-01-27 |
| Buyer's remorse: full refund within 72 hours (weekends count), usage charges excluded | CONFIRMS (official page) | none in our file; [TK109] | [TK78] | 2026-01-27 |
| After 72 hours the buyer must file a Microsoft Support refund request | CONFLICT (Microsoft: buyer contacts the publisher, who files the ticket) | none | [TK78] vs [TK109] | 2026-01-27 vs 2025-04-09 |
| Tackle does not mark a Microsoft offer accepted until the subscription is activated and billing starts (pre auto-activation behavior) | NEW | [M17] | [TK78] | 2026-01-27 |
| Microsoft closes deal registration in Partner Center each year during fiscal year-end accounting; submissions fail with "Deal Registration functionality is currently closed" | NEW | [M6] | [TK91][TK90] | 2026-06-25 |
| Partner Center integration permissions for a co-sell tool: Global Admin and Owner to create the app registration; tool user invited with Referral Admin and Developer roles; app assigned Manager (Windows) for offers; up to 24 hours to propagate; a co-sell eligible solution is needed before co-sell setup | NEW (menu-level) | none | [TK89] | 2026-09-16 |
| MPO via Tackle: customized plans only ("customize public plan pricing" no longer supported); pricing end date always last day of month; only single-product, single-plan offers importable; accepted MPOs cannot be canceled, partner cancels unextended offers | NEW | [M39] | [TK84] | 2026-08-19 |
| Microsoft marketplace fee "can be dependent on the seller's relationship" | STALE (3% standard, 1.5% renewals) | [M34][M42] | [TK78] | 2026-01-27 |
| Microsoft Bulk Co-sell drafts up to 200 Salesforce opportunities at once; account matching reuses previously accepted co-sells to find the right Microsoft customer record (controlled availability, November 2025) | NEW (tool) | none | [TK20] | 2025-11-20 |
| AppSource and Azure Marketplace converged into one Microsoft Marketplace in September 2025 | CONFIRMS | [M4 scope] | [TK96] | 2026-05 |
| Enabling a second marketplace "just like AWS" failed at CrowdStrike: legal terms, accounts receivable and seller enablement differ by cloud | NEW (practitioner) | none | [TK99] | 2026-05 |

---

## 4. Google Cloud: extracted substance

| Fact | Status | Our tag | Vendor tag | Date |
|---|---|---|---|---|
| Register and progress Google co-sell "inside Partner Advantage"; ISVs list "under the Build Engagement model" | STALE (Partner Network replaced Partner Advantage 2026-01-15) | [G1][G4] | [TK7][TK8][TK57] | 2026-05 |
| Select, Premier and new Diamond tiers; competencies measured on capacity and capability, independent of tier; rolled out Q1 2026 with a transition period | CONFIRMS | [G1][G2] | [TK8] | 2026-05-07 |
| Hub co-sell setup: Partner Network Hub > Your company > Users > Assign Roles; add the tool's service account with the Integrator role; copy Company Name and Partner ID from Account; about 10 minutes | CONFIRMS | [G72] | [TK82] | 2026-05-22 |
| Google co-sell from Salesforce: early access March 2026, GA June 2026; bulk registration; required legal acknowledgments cannot change after Google accepts; some fields lock after acceptance; Google returns deal number and Google seller owner; only Google can mark closed won or lost (partner requests) | CONFIRMS (G73) / NEW (field behavior) | [G73] | [TK13][TK4][TK83] | 2026-06 |
| Google's new co-sell APIs are two-way; Tackle co-launched | NEW | [G72] | [TK94] | 2026-05 |
| Google is redesigning its deal registration platform to support co-selling across ISVs, channel partners and Google | NEW (Google speaker, VENDOR channel) | none | [TK97] | 2026-05 |
| MCCP will expand to variable credits and pay-as-you-go contracts; propensity-to-buy tooling adds channel support and Gemini Enterprise paid-seat signals | NEW (announced, not live on our pages) | [G45][G46] | [TK97] | 2026-05 |
| Distributor channel private offer pilot (DCPO) running to improve channel onboarding | NEW | none | [TK97] | 2026-05 |
| New private offer APIs in preview (May 2026) | CONFIRMS (Producer API GA 2026-07-24) | [G26] | [TK97] | 2026-05 |
| 2,000+ AI agents and tools in Marketplace; backlog USD 462B (from 240B); GTV doubled 2024 to 2025; AI-category GTV up 18x year over year; 8M paid Gemini Enterprise seats; 11M paying Workspace organizations | CONFIRMS (2,000; 462B) / NEW (GTV, 18x, seats) | [G64][G8] | [TK97] | 2026-05 |
| USD 750M partner fund covers agent build support, FDEs with SIs, deployment and usage incentives, training | CONFIRMS | [G6] | [TK97] | 2026-05 |
| SaaS purchases count 100% toward the Google commit "up to 50% of their total commit amount" | CONFLICT (official cap 25%) | [G22] | [TK73] | 2025-11-05 |
| Multi-payment schedules need at least one payment per contract year; each payment may decrease "to a minimum of 70% value" per day | CONFLICT on 70% (official: each installment's per-day value at least 50% of prior) / NEW (one per year) | [G28] | [TK72] | 2025-11-05 |
| Custom billing terms 1 to 84 months; future-dated offers need listing auto-approval enabled | CONFIRMS | [G26][G47][G30][G32] | [TK72][TK73] | 2025-11-05 |
| Amendments must keep the same pricing and payment option (prepay with prepay); a second agreement for the same buyer and product is not allowed, amend instead | NEW (vendor) / partial CONFIRMS | [G29] | [TK86] | 2025-12-15 |
| MCPO reselling needs organization-level roles Commerce Business Enablement Configuration Admin and Commerce Business Enablement Reseller Discount Admin; deal types New, Channel shift, Migration, Native renewal drive revenue share | CONFIRMS (deal types) / NEW (role names) | [G26][G34] | [TK81] | 2025-11-05 |
| Payouts typically on the 21st; Detailed Disbursement report arrives by the 10th business day for disbursements through the 21st of the prior month; no historical import on connection | CONFIRMS (21st) / NEW (report timing) | [G24] | [TK73][TK77] | 2025-10 / 2025-11 |
| Cancellation and refund: seller files in Service Desk Portal (Billing Administrator); buyer gets 30 days to approve, reminder 7 days before expiry | NEW | none | [TK73] | 2025-11-05 |
| Sellers outside the US may need to charge Google VAT or GST on Google's revenue-share payment and invoice Google | NEW | [G24] | [TK73] | 2025-11-05 |
| Public orders auto-renew by default and cannot be changed; private offers optional | CONFIRMS | [G31] | [TK73] | 2025-11-05 |
| If a buyer never completes registration, Google provides no buyer identity, Tackle sends nothing and the buyer is not billed | NEW | none | [TK86] | 2025-12-15 |
| Google Marketplace fees "depend on the seller's history and relationship" | STALE (Vendor Net Revenue Schedule 3/2/1.5%) | [G18] | [TK73] | 2025-11-05 |
| Tackle creates Google direct private offers only for new, flat-rate, flat-rate-with-usage and installment offers; consumption-only and amendments must be created in Producer Portal and imported | NEW (tool limit) | none | [TK72] | 2025-11-05 |

---

## 5. Cross-cloud playbooks and benchmarks worth reusing

1. **Investment Checkpoint before any co-sell rewrite.** Ask two questions per opportunity: does segment and deal size justify the effort, and does it grow the cloud's own consumption? If yes, classify Collaboration Driven (full sharpening, seller assignment check, use the agent feedback loop as a working session) or Program Driven (baseline only) [TK1]. Transferable to Microsoft and Google triage.
2. **Rep-led co-sell button.** Put a "co-sell with cloud" action on every CRM opportunity or account; route it to automation, not to a Slack channel the alliance manager works by hand. Datadog's shift made partner-originated opportunities exceed AWS-originated for the first time [TK98]; CrowdStrike tags AWS exactly like a reseller so automation creates the ACE record [TK99].
3. **Three alliance KPIs that a CRO accepts.** Sourced opportunities reaching stage 2 per quarter; new logos closed with "active influence" (co-selling across the cycle, not one call); sourced net-new ARR per alliance rep [TK98].
4. **Put the cloud into the sales methodology.** Add a "partner champion" field to MEDDPICC, a cloud slot in every QBR, co-sell modules in new-hire onboarding, and small-group enablement (Datadog ran 17 sessions in a week for one segment) [TK98][TK103].
5. **Map your territories to the cloud's verticals.** AWS fields by industry; CrowdStrike named its central-region lead as the counterpart to AWS auto manufacturing and reviews pipeline with that team [TK99].
6. **Search "company + AWS" before every QBR.** Public press releases reveal strategic cloud agreements; bring the AWS team into accounts where one exists [TK99].
7. **Use MPOPP (and MCCP on Google) as a dated compelling event.** Credits tied to a private offer give sellers a time-bound reason to close; link the offer before the opportunity reaches Launched [TK99][TK14].
8. **Set marketplace targets at the company growth rate, not 60 to 80%.** Seeq kept executive trust by matching marketplace growth goals to overall revenue goals and then beating them [TK103].
9. **Position marketplace 4 to 6 weeks before close, not at stage 6.** Late marketplace requests create the 11th-hour mess resellers and ISVs both describe [TK103][TK104]; Grammarly educated sellers six weeks before launch and recorded an AWS co-sell training for reuse [TK42].
10. **PSM ladder.** One-off rescue (learn territory, ask for account list), repeat engagement (run the list against your pipeline), group engagement (team meetings and kickoffs for reputation, not deals) [TK45].
11. **Marketplace-first SKO.** Honeycomb's CRO declared "marketplace first" at SKO with Tackle and AWS present and propensity scores per rep; wins were fed back as win wires [TK102].
12. **Treat finance as a first-class stakeholder.** Payouts can land 60 to 120 days after acceptance; forecast expected versus actual disbursement, book fees as COGS, suppress normal invoicing for cloud deals [TK28]. Get bookable artifacts at acceptance [TK61][TK14].
13. **Do not let AI rewrite the evaluation list without you.** AWS's PLG lead cited G2 data: 51% of B2B buyers start research in AI chatbots (29% in 2025) and 69% chose a different vendor on AI guidance; keep listings, reviews and structured evaluation content machine-readable [TK95].
14. **PLG through marketplace needs pricing redesign.** A USD 12,000 or 100,000 annual SKU will not self-serve; design a sub-USD 100 monthly entry and mine usage signals for private-offer upgrades (examples: near-zero usage to USD 15K a month to a USD 500K private offer) [TK95][TK16].
15. **Commit discussions and GTM incentives are now one negotiation.** Tackle's CEO: tie your cloud commit, your co-sell incentives and your product strategy together in any strategic agreement (SCA) [TK100]; Honeycomb's SCA carried MDF, POC credits and MPOPP [TK102].
16. **One platform, one DRI per step.** GitLab: name owners for offer creation, offer approval, co-sell registration; hold weekly or biweekly vendor check-ins; embed cloud expertise in deal desk, AR and product [TK101].
17. **Prospect score plus cloud score, read together.** High AWS engagement with low marketplace propensity usually means legacy procurement or a mid-migration buyer; high propensity with low AWS engagement usually means EDP burn-down buyers or line-of-business pilots [TK88].

---

## 6. Survey and benchmark data

State of Cloud GTM 2025 (sixth annual; fielded mid-2025; published 2025-10-08 webinar, blogs 2025-10-21 to 2025-12-17). Sample n = 83 (derived: every chart series sums to 83; Tackle does not state n) [TK49]. Respondents: ARR USD 501M to 1B+ 27, 101 to 500M 20, 11 to 50M 10, undisclosed 9, 51 to 100M 6, under 1M 6, 1 to 10M 5; roles Cloud Alliances 42 of 82, Channel/Partner Management 20 [TK49]. All VENDOR.

| Figure | Sample | Date | Label |
|---|---|---|---|
| Mean marketplace share of revenue 20% past year, 32% expected next year ("60% increase") | n = 83 | 2025-10 | VENDOR [TK29][TK49] |
| 53 of 83 (64%) had 0 to 10% of revenue via marketplace; 19 of 83 expect 0 to 10% next year | n = 83 | 2025-10 | VENDOR, derived [TK49] |
| Co-sell influenced 22% of net-new deals, expected 30%; 96% expect more co-sell deals | n = 83 | 2025-10 | VENDOR [TK29] |
| Active co-sell: AWS 69 (83%), Microsoft 42 (51%), Google 29 (35%); 28% co-sell with all three; 80% multi-cloud or planning | n = 83 | 2025-10 | VENDOR [TK29][TK49] |
| Active marketplace listing: AWS 74 (89%), Microsoft 48 (58%), Google 34 (41%) | n = 83 | 2025-10 | VENDOR, derived [TK49] |
| Benefit rated significant or major: committed spend 61 (73%, reported as 74% and 75%); deal acceleration 39 (47%); deal conversion 35 (42%); lead generation 11 (13%); lead gen no or minimal 62 (75%) | n = 83 | 2025-10 | VENDOR, derived [TK49] |
| Very or extremely challenging: engaging field sellers 46 (55%); PDM attention 38 (46%); culture and change management 42 (51%); business model alignment 37 (45%); manual processes 31 (37%); exec sponsorship 26 (31%); sales comp 23 (28%); referral quality 20 (24%); forecasting 20 (24%); cost 16 (19%); marketplace fees 15 (18%) | n = 83 | 2025-10 | VENDOR, derived [TK49] |
| "92% rate getting attention from providers as challenging" (only 8% "not at all") | n = 83 | 2025-10 | VENDOR [TK49] |
| Channel partners in 27% of marketplace transactions, expected 37%; 59% expect more channel influence; channel "mission critical" 33%, "critical" 27% | n = 83 | 2025-10 | VENDOR [TK17][TK49] |
| Multi-cloud (all three) sellers: 29% of revenue via marketplace vs 3% single-cloud; 39% vs 18% of deals co-sell influenced | subgroup, n not given | 2025-11 | VENDOR [TK24] |
| Data users: 36% of sellers closed at least one marketplace deal vs 24% for non-users (average 28%) | n = 83 | 2025-11 | VENDOR [TK24] |
| GenAI users expect 33% of deals co-sell assisted vs 27% for non-users; 12 of 83 use GenAI extensively in partner selling | n = 83 | 2025-10 | VENDOR [TK49] |
| Executive sponsor is CRO for 35 of 82 (43%, reported 40%); partner or channel team 24 (29%) | n = 82 | 2025-10 | VENDOR [TK49] |
| Current Cloud GTM team 0 to 5 FTE for 38 of 83 (46%); 52% expect to hire; "37% team growth" | n = 83 | 2025-10 | VENDOR [TK49] |
| Top 10% of companies: 50% of revenue via marketplace, 58% influenced by co-sell | not stated | 2025-10 | VENDOR [TK49][TK12] |
| Cloud commitments above USD 460B in 2025 (Canalys, quoted) | analyst | 2025 | INDEPENDENT via VENDOR [TK17] |
| Cloud commits about USD 1T, heading to USD 2T to 3T (CEO estimate) | none | 2026-05 | VENDOR [TK100] |
| Q4 2025 was the largest booking quarter in Tackle's history (most unique buyers, transactions, global transactions, channel deals) | Tackle platform | 2026-05 | VENDOR [TK100] |
| Canalys: USD 85B through cloud marketplaces by 2028, over 50% via channel | analyst | 2025-05 | INDEPENDENT via VENDOR [TK104] (outside window) |
| AWS Marketplace deals 81% larger, 27% more likely to close, 40% faster (Forrester TEI); ~80% of partners see AWS Marketplace as critical to co-sell | Forrester, n not given | cited 2026-01 | INDEPENDENT (AWS-commissioned) via VENDOR [TK15] |
| 64% of CIOs prefer buying through existing cloud relationships | not given | 2026-05 | VENDOR, source not named [TK6] |
| 58% of SaaS companies have some PLG motion; 61% use or test usage-based pricing | not given | 2026-02 / 2026-03 | VENDOR [TK16][TK12] |
| G2: 51% of B2B buyers start research in AI chatbots (29% in 2025); 54% use it to shortlist; 69% chose a different vendor on AI guidance | G2 study | 2026-05 | INDEPENDENT via AWS speaker [TK95] |
| Prospect "High" accounts over 500x more likely to close on marketplace than Low/Medium | Tackle platform | 2024-12, updated 2025-11 | VENDOR [TK113] |
| Customer results: Jamf close rate 5% to 20% with 4x marketplace deal volume; work-management ISV +1,022% deals shared with AWS, +92% closed-won marketplace deals after 4 months of managed services; CrowdStrike USD 1.5B through marketplaces in a year and 50% faster private-offer workflow; Grammarly first listing 10 months, second 18 days, USD 1M closed, USD 5M+ projected | single customers | 2024-12 to 2026-05 | VENDOR [TK113][TK48][TK99][TK42][TK14] |

---

## 7. Conflicts with our intelligence files

| Topic | Tackle says | Our file says | Which wins and why |
|---|---|---|---|
| Google commit drawdown cap | 100% of SaaS counts "up to 50% of their total commit amount" [TK73] (help article updated 2025-11-05) | 25% cap on combined eligible marketplace spend [G22] (Google terms, modified 2025-05-27) | Official terms win. Tackle's FAQ predates or ignores the May 2025 policy. Flag to any customer quoting Tackle |
| Google installment decrease floor | Payments may decrease to a minimum of 70% per-day value [TK72] (2025-11-05) | Each installment's per-day value at least 50% of prior [G28] (updated 2026-09-24) | Official doc wins (newer, primary) |
| AWS ACE eligibility count | 10 submitted and validated opportunities, plus Validated, FTR, PSF listing [TK67] (2026-01-21) | 15 validated opportunities for Software, Labra paraphrase of 2023 FAQ [A108] | Neither is official; Tackle is newer. Record both, verify in ACE FAQ (login-gated) |
| AWS private offer currencies | Includes CAD [TK70] (2026-01-09) | USD, EUR, GBP, AUD, JPY, INR only [A56]; confirmed again on the AWS page 2026-09-26 [TK108] | Official wins; CAD unverified |
| AWS disbursement cadence | "Monthly cycle," "single payout" [TK52] (2026-09-23) | Daily or monthly (day 1 to 28) [A56][TK108] | Official wins |
| ISV Accelerate and fees | ISVA brings "reduced listing fees" [TK35] (2025-09-11) | Fees tiered by TCV and renewal for all sellers [A24] | Official wins; Tackle post conflates |
| ACE prerequisites | APN Standard, Advanced or Premier tier plus customer reviews [TK47] (2025-07-02) | Partner Paths since 2022; Registered, Validated, Differentiated [A21] | Official wins; Tackle FAQ is stale |
| ACE data exchange | S3 buckets "remain widely used" [TK38] (2025-08-20) | S3 deprecated, closed to new users [A47] | Official wins |
| Microsoft post-72-hour refund | Buyer files Microsoft Support request [TK78] | Microsoft: buyer contacts the publisher, who files the ticket [TK109] (2025-04-09) | Official wins |
| Microsoft program names | "IP Co-sell Incentivized," "Partner Sales Connect," Marketplace Rewards as live [TK11][TK22][TK3] | Frontier Accelerate for Marketplace consolidated these in September 2026 [M30] | Official wins; Tackle copy predates FY27 |
| Google program | Partner Advantage and Build engagement model [TK7][TK8][TK57] (May 2026) | Partner Network since 2026-01-15 [G1] | Official wins (our file already flags [G74]) |
| Marketplace fees in help FAQs (all three clouds) | Fee "depends on the seller's relationship" [TK73][TK78][TK80] | Published schedules: AWS [A24], Microsoft [M34][M42], Google [G18] | Official wins |
| State of Cloud GTM "PDM access" stat | Blog: "46% rated access to PDMs extremely challenging"; "31% rated provider engagement extremely challenging" [TK17] | Our X-file repeats the 46% "extremely" wording [X42] | Tackle's own chart data: 46% is "very or extremely" (38 of 83); "extremely" alone is 21 of 83 (25%); the 31% could not be reproduced from any series [TK49]. Correct X42 wording |
| Microsoft MACC-eligible count | ~40,000 eligible solutions [TK96] (Microsoft speaker, May 2026) | No count in our file | Not a conflict; NEW, unverified on official page |

---

## 8. Content inventory (published or updated since 2025-07-01, plus older items still cited)

Substance rating: 3 = program rules or hard numbers; 2 = useful tactics or partial rules; 1 = product marketing.

| Date | Type | Title | Cloud | URL | Rating |
|---|---|---|---|---|---|
| 2026-09-25 | Blog | The New Math of AWS Co-Sell: OQS | AWS | https://tackle.io/blog/aws-opportunity-quality-score/ | 3 |
| 2026-09-24 | Help | AWS partner private offers | AWS | https://help.tackle.io/en/articles/10707700-aws-partner-private-offers | 3 |
| 2026-09-23 | Report (updated) | The Alliance Leader's Cloud Co-sell Playbook | All | https://tackle.io/resources/report/isv-cloud-co-sell-strategy-playbook/ | 1 |
| 2026-09-23 | Blog (updated) | Should You Build or Buy Your Cloud GTM? | All | https://tackle.io/blog/build-or-buy-cloud-marketplace/ | 1 |
| 2026-09-23 | News (updated) | Marketplace revenue reconciliation | All | https://tackle.io/resources/news/marketplace-revenue-reconciliation/ | 2 |
| 2026-09-17 | Hub | Tackle for AWS / Microsoft / Google | All | https://tackle.io/aws/ ; https://tackle.io/microsoft/ ; https://tackle.io/google/ | 1 |
| 2026-09-16 | Help | Connect to Microsoft | Microsoft | https://help.tackle.io/en/articles/10509617-connect-to-microsoft | 3 |
| 2026-09-02 | Blog | Tackle selected for AWS 3PI PDM Pilot | AWS | https://tackle.io/blog/tackle-3pi-pdm-pilot/ | 2 |
| 2026-08-26 | Help | What's new 2026 | All | https://help.tackle.io/en/articles/13675718-what-s-new-2026 | 3 |
| 2026-08-19 | Help | Microsoft partner private offers | Microsoft | https://help.tackle.io/en/articles/11371959-microsoft-partner-private-offers | 3 |
| 2026-08-12 | Help | Express Private Offers (EPO) and Tackle FAQs | AWS | https://help.tackle.io/en/articles/16351548-express-private-offers-epo-and-tackle-faqs | 3 |
| 2026-08-12 | Help | Multi-product solutions and offer sets FAQ | AWS | https://help.tackle.io/en/articles/16351721 | 3 |
| 2026-07 (event ~2026-05) | Video | Cloud GTM XP 2026: 11 sessions (keynote, CrowdStrike, Datadog, Microsoft, Google, AWS PLG, GitLab, Seeq, Honeycomb, PartnerStack, Automation) | All | https://www.youtube.com/@tackleio ; https://tackle.io/cloud-gtm-xp/ | 3 |
| 2026-07-20 | Help | Pricing and payments for Microsoft | Microsoft | https://help.tackle.io/en/articles/10535445 | 3 |
| 2026-06-30 | Help | What's new Tackle for Salesforce 2026 | All | https://help.tackle.io/en/articles/13675811 | 2 |
| 2026-06-25 | Help | Manage Microsoft co-sell referrals from Salesforce; automate referrals | Microsoft | https://help.tackle.io/en/articles/11395356 ; https://help.tackle.io/en/articles/11760081 | 2 |
| 2026-06-17 | Blog | Tackle Reel: June 2026 | All | https://tackle.io/blog/the-tackle-reel-june-product-updates-2/ | 2 |
| 2026-06-10 | Help | AWS Marketplace private offers FAQs | AWS | https://help.tackle.io/en/articles/10504181 | 3 |
| 2026-05-22 | Help | Connect to Google Cloud for co-sell; manage Google co-sell from Salesforce | Google | https://help.tackle.io/en/articles/15217465 ; https://help.tackle.io/en/articles/15217622 | 3 |
| 2026-05-20 | Blog | What a Successful B2B SaaS Sales Strategy Looks Like | All | https://tackle.io/blog/b2b-saas-sales-strategy-success/ | 1 |
| 2026-05-19 | Blog | Benefits of Selling SaaS on Cloud Marketplaces | All | https://tackle.io/blog/benefits-of-selling-saas-on-cloud-marketplaces/ | 1 |
| 2026-05-07 | Blog | How to Sell on Google Cloud Marketplace | Google | https://tackle.io/blog/how-to-sell-on-google-cloud-marketplace/ | 1 (stale) |
| 2026-05-04 | Blog | A Guide to AWS Co-selling | AWS | https://tackle.io/blog/how-to-cosell-with-aws/ | 1 |
| 2026-05-01 | Blog | Co-sell in the Google Cloud Partner Program | Google | https://tackle.io/blog/co-sell-in-google-cloud-partner-program/ | 1 (stale) |
| 2026-04-16 | Blog | Tackle Reel: April 2026 | All | https://tackle.io/blog/tackle-reel-april/ | 2 |
| 2026-04-08 | Help | Tackle HubSpot integration | AWS | https://help.tackle.io/en/articles/14486577-tackle-hubspot-integration | 3 |
| 2026-04-06 | Blog | How to Co-Sell With Microsoft Azure | Microsoft | https://tackle.io/blog/co-selling-with-microsoft/ | 1 (stale) |
| 2026-03-31 | Blog | ISV Revenue Growth Strategies | All | https://tackle.io/blog/isv-revenue-growth-strategies/ | 1 |
| 2026-03-18 | Blog | Tackle Reel: March 2026 | All | https://tackle.io/blog/cloud-gtm-product-updates-march-2026-tackle/ | 3 |
| 2026-03-03 | Help | How to opt in for AWS Concurrent Agreements | AWS | https://help.tackle.io/en/articles/13908272 | 3 |
| 2026-02-27 | Blog | Tackle Reel: February 2026 | AWS | https://tackle.io/blog/cloud-gtm-product-updates-february-2026-tackle/ | 2 |
| 2026-02-17 | Blog | Product Led Growth in SaaS | All | https://tackle.io/blog/product-led-growth-in-saas/ | 2 |
| 2026-01-27 | Blog | Driving Marketplace Revenue Begins at SKO | AWS | https://tackle.io/blog/driving-meaningful-marketplace-revenue-begins-at-sales-kick-off/ | 2 |
| 2026-01-27 | Help | Microsoft commercial marketplace FAQs | Microsoft | https://help.tackle.io/en/articles/10542353 | 3 |
| 2026-01-21 | Help | AWS Co-Sell FAQs (ACE eligibility) | AWS | https://help.tackle.io/en/articles/10514011-aws-co-sell-faqs | 3 |
| 2026-01-09 | Help | Pricing and payments for AWS | AWS | https://help.tackle.io/en/articles/10447246 | 2 |
| 2025-12-17 | Blog | State of Cloud GTM 2025: Learnings 5 to 7 | All | https://tackle.io/blog/state-of-cloud-gtm-2025-committed-spend-engagement-and-the-new-marketplace-landscape/ | 3 |
| 2025-12-02 | Blog | New Tackle capabilities at re:Invent 2025 | AWS | https://tackle.io/blog/cloud-gtm-success-starts-here-tackle-aws-unveil-the-next-generation-of-cloud-selling/ | 2 |
| 2025-12-01 | Blog | Tackle + AppDirect | All | https://tackle.io/blog/tackle-appdirect-accelerating-the-future-of-cloud-gtm/ | 2 |
| 2025-11-24 | Blog | Planning your week at re:Invent | AWS | https://tackle.io/blog/planning-your-cloud-gtm-week-at-aws-reinvent/ | 1 |
| 2025-11-20 | Blog | The New Standard for Selling with Microsoft | Microsoft | https://tackle.io/blog/the-new-standard-for-selling-with-microsoft-faster-smarter-and-fully-connected/ | 2 |
| 2025-11-12 | Blog | Breaking Down MACC | Microsoft | https://tackle.io/blog/breaking-down-the-microsoft-azure-consumption-commitment-macc/ | 2 (partly stale) |
| 2025-11-07 | Blog | Tackle signs SCA with AWS | AWS | https://tackle.io/blog/tackle-signs-strategic-collaboration-agreement-with-aws/ | 2 |
| 2025-11-06 | Blog | SoCGTM 2025: Multi-cloud 10x | All | https://tackle.io/blog/state-of-cloud-gtm-2025-why-multi-cloud-companies-see-10x-more-revenue-with-data/ | 3 |
| 2025-11-05 | Help | Google PO FAQs; pricing and payment; associate MCPO | Google | https://help.tackle.io/en/articles/10509098 ; https://help.tackle.io/en/articles/10504368 ; https://help.tackle.io/en/articles/11898587 | 3 |
| 2025-10-30 | Blog / Help | Why PLG wins on marketplaces; About marketplace scoring | All | https://tackle.io/blog/why-plg-ready-companies-win-on-cloud-marketplaces/ ; https://help.tackle.io/en/articles/10471584 | 2 |
| 2025-10-29 | Blog | Tackle Reel: October 2025 | All | https://tackle.io/blog/the-tackle-reel-october-product-updates/ | 2 |
| 2025-10-28 | Blog | Leveraging committed spend | All | https://tackle.io/blog/leveraging-committed-spend-on-cloud-marketplaces/ | 1 |
| 2025-10-22 | Blog | How RevOps Leaders Orchestrate Cloud GTM | All | https://tackle.io/blog/how-revops-leaders-orchestrate-predictable-growth-through-cloud-gtm/ | 2 |
| 2025-10-21 | Blog | SoCGTM 2025: Marketplaces and co-sell | All | https://tackle.io/blog/state-of-cloud-gtm-2025-why-marketplaces-and-co-sell-cant-be-ignored/ | 3 |
| 2025-10-17 | Report | 2025 State of Cloud GTM Report (landing and microsite) | All | https://tackle.io/resources/report/2025-state-of-cloud-gtm-report-2/ ; https://state-of-cloud-gtm-report-2025.tackle.io/ | 3 |
| 2025-10-15 | News | GTM Agent on Agentforce | AWS | https://tackle.io/resources/news/tackle-introduces-gtm-agent-to-power-cloud-co-selling-with-salesforces-agentforce/ | 2 |
| 2025-10-15 | Help | Reconcile AWS / Microsoft / Google payments | All | https://help.tackle.io/en/articles/10535499 ; https://help.tackle.io/en/articles/10535672 ; https://help.tackle.io/en/articles/10535660 | 2 |
| 2025-10-08 | Blog | 4 Cloud GTM Challenges Tackle for Salesforce Solves | All | https://tackle.io/blog/4-cloud-gtm-challenges-tackle-for-salesforce-solves/ | 1 |
| 2025-09-30 | Blog | Tackle Reel: September 2025 | All | https://tackle.io/blog/the-tackle-reel-september-updates/ | 2 |
| 2025-09-26 | Blog | Engaging Marketing Teams in Cloud GTM | All | https://tackle.io/blog/engage-marketing-cloud-gtm-strategy/ | 1 |
| 2025-09-25 | Blog | 353% AWS Marketplace growth with Tackle for Salesforce | AWS | https://tackle.io/blog/aws-marketplace-353-growth-tackle-for-salesforce/ | 1 |
| 2025-09-24 | Blog | SoCGTM 2025 preview | All | https://tackle.io/blog/state-of-cloud-gtm-report-2025-preview/ | 1 |
| 2025-09-15 | Help | Microsoft Azure IP Co-sell requirements checklist | Microsoft | https://help.tackle.io/en/articles/12295218 | 2 (pre-FY27) |
| 2025-09-11 | Blog | What You Need to Know About the AWS ISV Partner Path | AWS | https://tackle.io/blog/what-you-need-to-know-about-the-aws-isv-partner-path/ | 1 (errors) |
| 2025-09-04 | Blog | Why Private Offers and Private Plans Matter | All | https://tackle.io/blog/private-offers-and-private-plans-2/ | 1 |
| 2025-08-21 | Blog | Tackle Reel: August 2025 | All | https://tackle.io/blog/the-tackle-reel-august-product-updates/ | 2 |
| 2025-08-20 | Blog | AWS Alphabet Soup (acronyms) | AWS | https://tackle.io/blog/aws-acronym-cheat-sheet-2/ | 1 (stale) |
| 2025-08-13 | Blog | How Kasada built Cloud GTM around AWS Marketplace | AWS | https://tackle.io/blog/how-kasada-made-aws-marketplace-the-center-of-its-cloud-gtm-strategy/ | 1 |
| 2025-08-12 (updated 2026-03-05) | Blog | 5 Things to Know About AWS CPPO | AWS | https://tackle.io/blog/guide-to-aws-cppo/ | 1 |
| 2025-08-07 | Blog | How to Leverage Co-sell with Cloud Providers | All | https://tackle.io/blog/how-to-leverage-co-sell-with-cloud-providers-to-scale-revenue-and-boost-efficiency/ | 2 |
| 2025-07-30 | Blog | How Grammarly jumpstarted its marketplace motion | AWS | https://tackle.io/blog/how-grammarly-jumpstarted-its-marketplace-motion-with-one-leader-and-a-plan/ | 2 |
| 2025-07-28 | Blog | Grading our 2025 GTM predictions | All | https://tackle.io/blog/state-of-cloud-gtm-grading-our-2025-gtm-predictions/ | 1 |
| 2025-07-17 | Blog | Tackle Reel: July 2025 | All | https://tackle.io/blog/the-tackle-reel-july-product-updates/ | 2 |
| 2025-07-16 | News | Day 1 AI Agent and Tools in AWS Marketplace | AWS | https://tackle.io/resources/news/powering-day-1-partner-success-with-ai-agent-and-tools-in-aws-marketplace/ | 2 |
| 2025-07-10 | Blog | Building AWS PSM relationships | AWS | https://tackle.io/blog/how-to-build-lasting-relationships-with-aws-partner-sales-managers-to-drive-co-sell-success/ | 2 |
| 2025-07-09 | Blog | ClickHouse PLG automation | AWS | https://tackle.io/blog/driving-product-led-growth-through-automation/ | 1 |
| 2025-07-02 | Blog | Basics of AWS Co-sell: ACE Portal | AWS | https://tackle.io/blog/the-basics-of-aws-co-sell-how-to-get-started-with-the-ace-portal/ | 2 (FAQ stale) |
| 2025-07-01 | Blog | Why Companies Are Turning to Co-sell Managed Services | AWS | https://tackle.io/blog/why-companies-are-turning-to-co-sell-managed-services/ | 1 |
| 2025-05 (outside window) | Video | Co-Building What's Next: Channels and Global Expansion (WWT, Google, Microsoft) | All | https://www.youtube.com/watch?v=bAFT9xz4W2Y | 2 |
| 2024-12-10 (updated 2025-11-13) | Blog | Data-Driven Strategies for Cloud GTM Success | All | https://tackle.io/blog/data-driven-strategies-for-cloud-gtm-success/ | 2 |

Webinar sitemap: no webinar pages published since 2025-07-25; events moved to Cloud GTM XP on YouTube and in-person AppDirect Thrive [TK111]. No podcast feed found on the channel (search for "podcast" and "Tackle Cast" returned nothing) [TK110].

---

## 9. Registry rows (people and channels to track monthly) and discovery queries

| Name | Role | Where to look | Good for | Last new item |
|---|---|---|---|---|
| Tackle blog and sitemap | Company content | https://tackle.io/blog-sitemap.xml (lastmod per URL); RSS https://tackle.io/feed/ | AWS OQS and co-launch explainers, State of Cloud GTM series | 2026-09-25 (OQS) |
| Tackle Help "What's new 2026" | Release notes | https://help.tackle.io/en/articles/13675718-what-s-new-2026 ; help sitemap https://help.tackle.io/sitemap.xml | Earliest signal of new hyperscaler transaction features (billing adjustments, net terms, currencies, EPO, offer sets) | 2026-08-26 |
| Tackle YouTube (Cloud GTM XP) | Event replays | https://www.youtube.com/@tackleio | Hyperscaler executives previewing roadmap; practitioner operating models | ~2026-07 (XP 2026 uploads) |
| Alex Murdoch | Content lead (22 bylines since 2025-07) | tackle.io/blog (author pages 403); LinkedIn | OQS, State of Cloud GTM series, 3PI and SCA announcements | 2026-09-25 |
| Ashley Stachura | Product marketing lead; "The Tackle Reel" monthly | tackle.io/blog Reel posts; hosts Datadog session | Monthly feature log that maps to AWS, Microsoft, Google launches | 2026-06-17 (updated 2026-07-31) |
| John Jahnke | CEO / GM of Tackle | Cloud GTM XP keynote; LinkedIn; quoted | Market sizing, predictions, State of Cloud GTM | 2026-09-02 (3PI quote) |
| Dillon Woods | Founder / CTO | Cloud GTM XP closing session | Agent, API, MCP and HubSpot roadmap | ~2026-05 |
| Adam Boyle | VP Product | re:Invent and Agentforce announcements | AWS Benefits API and funding in CRM | 2025-12-02 |
| Liam Savage | Cloud GTM Advisor | Blog (PSM relationships); XP sessions (GitLab, Seeq) | Practitioner operating models for lean alliance teams | ~2026-05 |
| Kevin Idol | Customer success (CrowdStrike, Honeycomb) | XP sessions | Enterprise-scale ops (billion-dollar sellers) | ~2026-05 |
| Vathsalya Senapathi | Manager, Partner and Cloud GTM | GTM Agent release; Google Marketplace event (March 2026) | Google co-sell and agent guidance | 2026-03-18 |
| Michael Crane | Help center author (EPO, Concurrent Agreements, offer sets) | help.tackle.io | Precise AWS transaction mechanics | 2026-08-12 |
| Jason Matthew Smith | Tackle (per our Microsoft registry) | tackle.io/blog | Microsoft co-sell primer | No bylined item found since 2025-07; Microsoft post (2026-04-06, no author metadata) is the latest attributed |
| Kaley Edmonds | Cloud GTM Coach | tackle.io/blog; LinkedIn https://www.linkedin.com/in/kmedmonds | SaaS Co-Sell Benefit steps | No new item found since 2025-04-24; move to Dormant check next pass |
| State of Cloud GTM report | Annual survey | https://state-of-cloud-gtm-report-2025.tackle.io/ ; watch for a 2026 microsite | Benchmarks (read chart data, not headlines) | 2025-10 (2026 edition promised for June 2026, not found) |
| AppDirect press releases | Parent company | https://www.appdirect.com/releases | Ownership, bundling, pricing changes affecting Tackle | 2026-04-14 (PartnerStack) |
| Tackle AWS Marketplace listing | Public pricing | https://aws.amazon.com/marketplace/pp/prodview-cfofnlysi75ug | List price changes | fetched 2026-09-26 |

Discovery queries (run monthly, last 45 days):
1. `site:tackle.io/blog OR site:tackle.io/resources 2026` then diff against blog-sitemap.xml lastmod.
2. `site:help.tackle.io "what's new"` and the help sitemap sorted by lastmod (new articles on AWS, Microsoft, Google transaction rules).
3. YouTube: TranscriptAPI `list_channel_videos @tackleio` (no sort) for uploads after last check; search `"Cloud GTM XP" 2026` and `"Tackle" "AWS Marketplace" webinar`.
4. `"State of Cloud GTM" 2026` and `state-of-cloud-gtm-report-2026.tackle.io` (check whether the 2026 report launched).
5. `Tackle HubSpot co-sell` OR `"Tackle for HubSpot"` (watch for Microsoft or Google support and HubSpot marketplace listing), plus `Tackle MCP server` (headless roadmap).

---

## Sources

| Tag | Title | Date | URL |
|---|---|---|---|
| TK1 | The New Math of AWS Co-Sell: What the Opportunity Quality Score Actually Means for You (Alex Murdoch) | 2026-09-25 | https://tackle.io/blog/aws-opportunity-quality-score/ |
| TK2 | Tackle Selected to Support ISV Onboarding Through AWS 3PI PDM Pilot | 2026-09-02 | https://tackle.io/blog/tackle-3pi-pdm-pilot/ |
| TK3 | Should You Build or Buy Your Cloud GTM? | 2021-03-02, updated 2026-09-23 | https://tackle.io/blog/build-or-buy-cloud-marketplace/ |
| TK4 | The Tackle Reel: June Product Updates (Ashley Stachura) | 2026-06-17, updated 2026-07-31 | https://tackle.io/blog/the-tackle-reel-june-product-updates-2/ |
| TK5 | What a Successful B2B SaaS Sales Strategy Looks Like | 2026-05-20 | https://tackle.io/blog/b2b-saas-sales-strategy-success/ |
| TK6 | The Benefits of Selling SaaS on Cloud Marketplaces | 2026-05-19 | https://tackle.io/blog/benefits-of-selling-saas-on-cloud-marketplaces/ |
| TK7 | How to Co-sell Successfully Through the Google Cloud Partner Program | 2026-05-01 | https://tackle.io/blog/co-sell-in-google-cloud-partner-program/ |
| TK8 | How to Sell on Google Cloud Marketplace: The Complete Guide for ISVs | 2026-05-07 | https://tackle.io/blog/how-to-sell-on-google-cloud-marketplace/ |
| TK9 | A Guide to AWS Co-selling | 2026-05-04 | https://tackle.io/blog/how-to-cosell-with-aws/ |
| TK10 | The Tackle Reel: April Product Updates (Ashley Stachura) | 2026-04-16 | https://tackle.io/blog/tackle-reel-april/ |
| TK11 | How to Co-Sell With Microsoft Azure: A Complete Guide | 2026-04-06, updated 2026-04-17 | https://tackle.io/blog/co-selling-with-microsoft/ |
| TK12 | ISV Revenue Growth Strategies | 2026-03-31 | https://tackle.io/blog/isv-revenue-growth-strategies/ |
| TK13 | The Tackle Reel: March Product Updates (Ashley Stachura) | 2026-03-18 | https://tackle.io/blog/cloud-gtm-product-updates-march-2026-tackle/ |
| TK14 | The Tackle Reel: February 2026 Product Updates (Ashley Stachura) | 2026-02-27 | https://tackle.io/blog/cloud-gtm-product-updates-february-2026-tackle/ |
| TK15 | Driving Meaningful Marketplace Revenue Begins at Sales Kick-Off (Ashley Stachura) | 2026-01-27 | https://tackle.io/blog/driving-meaningful-marketplace-revenue-begins-at-sales-kick-off/ |
| TK16 | Product Led Growth in SaaS (Ashley Stachura) | 2026-02-17 | https://tackle.io/blog/product-led-growth-in-saas/ |
| TK17 | State of Cloud GTM 2025: Committed Spend, Engagement, and the New Marketplace Landscape (Ashley Stachura) | 2025-12-17 | https://tackle.io/blog/state-of-cloud-gtm-2025-committed-spend-engagement-and-the-new-marketplace-landscape/ |
| TK18 | Cloud GTM Success Starts Here: Tackle + AWS Unveil the Next Generation of Cloud Selling (re:Invent 2025) | 2025-12-02 | https://tackle.io/blog/cloud-gtm-success-starts-here-tackle-aws-unveil-the-next-generation-of-cloud-selling/ |
| TK19 | Tackle + AppDirect: Accelerating the Future of Cloud GTM (Dillon Woods) | 2025-12-01 | https://tackle.io/blog/tackle-appdirect-accelerating-the-future-of-cloud-gtm/ |
| TK20 | The New Standard for Selling with Microsoft (Ashley Stachura) | 2025-11-20 | https://tackle.io/blog/the-new-standard-for-selling-with-microsoft-faster-smarter-and-fully-connected/ |
| TK21 | Your Guide to Marketplace and Co-Sell at re:Invent | 2025-11-24 | https://tackle.io/blog/planning-your-cloud-gtm-week-at-aws-reinvent/ |
| TK22 | Breaking Down the Microsoft Azure Consumption Commitment (MACC) (Alex Murdoch) | 2025-11-12 | https://tackle.io/blog/breaking-down-the-microsoft-azure-consumption-commitment-macc/ |
| TK23 | Tackle.io Signs Strategic Collaboration Agreement with AWS | 2025-11-07 | https://tackle.io/blog/tackle-signs-strategic-collaboration-agreement-with-aws/ |
| TK24 | State of Cloud GTM 2025: Why Multi-Cloud Companies See 10x More Revenue with Data | 2025-11-06 | https://tackle.io/blog/state-of-cloud-gtm-2025-why-multi-cloud-companies-see-10x-more-revenue-with-data/ |
| TK25 | Why PLG-Ready Companies Win on Cloud Marketplaces | 2025-10-30 | https://tackle.io/blog/why-plg-ready-companies-win-on-cloud-marketplaces/ |
| TK26 | How to Leverage Committed Spend on Cloud Marketplaces | 2025-10-28 | https://tackle.io/blog/leveraging-committed-spend-on-cloud-marketplaces/ |
| TK27 | The Tackle Reel: October Product Updates | 2025-10-29 | https://tackle.io/blog/the-tackle-reel-october-product-updates/ |
| TK28 | How RevOps Leaders Orchestrate Predictable Growth Through Cloud GTM | 2025-10-22 | https://tackle.io/blog/how-revops-leaders-orchestrate-predictable-growth-through-cloud-gtm/ |
| TK29 | State of Cloud GTM 2025: Why Marketplaces and Co-Sell Can't Be Ignored | 2025-10-21 | https://tackle.io/blog/state-of-cloud-gtm-2025-why-marketplaces-and-co-sell-cant-be-ignored/ |
| TK30 | 4 Cloud GTM Challenges Tackle for Salesforce Solves | 2025-10-08 | https://tackle.io/blog/4-cloud-gtm-challenges-tackle-for-salesforce-solves/ |
| TK31 | The Tackle Reel: September Product Updates | 2025-09-30 | https://tackle.io/blog/the-tackle-reel-september-updates/ |
| TK32 | Engaging Marketing Teams in Your Cloud GTM Strategy | 2025-09-26 | https://tackle.io/blog/engage-marketing-cloud-gtm-strategy/ |
| TK33 | Driving 353% AWS Marketplace Growth with Tackle for Salesforce | 2025-09-25 | https://tackle.io/blog/aws-marketplace-353-growth-tackle-for-salesforce/ |
| TK34 | The 2025 State of Cloud GTM Report Preview | 2025-09-24 | https://tackle.io/blog/state-of-cloud-gtm-report-2025-preview/ |
| TK35 | What You Need to Know About the AWS ISV Partner Path | 2025-09-11 | https://tackle.io/blog/what-you-need-to-know-about-the-aws-isv-partner-path/ |
| TK36 | Why Private Offers and Private Plans Matter for Marketplace Sellers | 2025-09-04 | https://tackle.io/blog/private-offers-and-private-plans-2/ |
| TK37 | The Tackle Reel: August Product Updates | 2025-08-21 | https://tackle.io/blog/the-tackle-reel-august-product-updates/ |
| TK38 | AWS Alphabet Soup: A Cheat Sheet of Amazon Acronyms | 2025-08-20 | https://tackle.io/blog/aws-acronym-cheat-sheet-2/ |
| TK39 | How Kasada Built Its Cloud GTM Around AWS Marketplace | 2025-08-13 | https://tackle.io/blog/how-kasada-made-aws-marketplace-the-center-of-its-cloud-gtm-strategy/ |
| TK40 | 5 Things to Know About the AWS CPPO Program in 2026 | 2025-08-12, updated 2026-03-05 | https://tackle.io/blog/guide-to-aws-cppo/ |
| TK41 | How to Leverage Co-sell with Cloud Providers to Scale Revenue | 2025-08-07 | https://tackle.io/blog/how-to-leverage-co-sell-with-cloud-providers-to-scale-revenue-and-boost-efficiency/ |
| TK42 | How Grammarly Jumpstarted Its Marketplace Motion with One Leader and a Plan | 2025-07-30 | https://tackle.io/blog/how-grammarly-jumpstarted-its-marketplace-motion-with-one-leader-and-a-plan/ |
| TK43 | State of Cloud GTM: Grading Our 2025 GTM Predictions (Liam Savage) | 2025-07-28 | https://tackle.io/blog/state-of-cloud-gtm-grading-our-2025-gtm-predictions/ |
| TK44 | The Tackle Reel: July Product Updates | 2025-07-17 | https://tackle.io/blog/the-tackle-reel-july-product-updates/ |
| TK45 | How to Build Lasting Relationships with AWS Partner Sales Managers (Liam Savage) | 2025-07-10 | https://tackle.io/blog/how-to-build-lasting-relationships-with-aws-partner-sales-managers-to-drive-co-sell-success/ |
| TK46 | Driving Product-Led Growth Through Automation: ClickHouse | 2025-07-09 | https://tackle.io/blog/driving-product-led-growth-through-automation/ |
| TK47 | The Basics of AWS Co-sell: How to Get Started with the ACE Portal (Josh Abrahams) | 2025-07-02 | https://tackle.io/blog/the-basics-of-aws-co-sell-how-to-get-started-with-the-ace-portal/ |
| TK48 | Why Companies Are Turning to Co-sell Managed Services | 2025-07-01 | https://tackle.io/blog/why-companies-are-turning-to-co-sell-managed-services/ |
| TK49 | The 2025 State of Cloud GTM Report microsite (chart data from site bundle) | 2025-10 | https://state-of-cloud-gtm-report-2025.tackle.io/ |
| TK50 | 2025 State of Cloud GTM Report (landing page) | 2025-10-17 | https://tackle.io/resources/report/2025-state-of-cloud-gtm-report-2/ |
| TK51 | The Alliance Leader's Cloud Co-sell Playbook | 2023-05-16, updated 2026-09-23 | https://tackle.io/resources/report/isv-cloud-co-sell-strategy-playbook/ |
| TK52 | Marketplace revenue reconciliation (product news) | 2022-03-01, updated 2026-09-23 | https://tackle.io/resources/news/marketplace-revenue-reconciliation/ |
| TK53 | Tackle Introduces GTM Agent to Power Cloud Co-selling with Salesforce's Agentforce | 2025-10-15 | https://tackle.io/resources/news/tackle-introduces-gtm-agent-to-power-cloud-co-selling-with-salesforces-agentforce/ |
| TK54 | Powering Day 1 Partner Success with AI Agent and Tools in AWS Marketplace | 2025-07-16 | https://tackle.io/resources/news/powering-day-1-partner-success-with-ai-agent-and-tools-in-aws-marketplace/ |
| TK55 | Tackle for AWS (hub) | updated 2026-09-17 | https://tackle.io/aws/ |
| TK56 | Tackle for Microsoft (hub) | updated 2026-09-17 | https://tackle.io/microsoft/ |
| TK57 | Tackle for Google Cloud (hub) | updated 2026-09-17 | https://tackle.io/google/ |
| TK58 | Tackle platform overview ("pricing" URL, no prices) | updated 2025-12-16 | https://tackle.io/pricing/ |
| TK59 | Company | updated 2026-08-13 | https://tackle.io/company/ |
| TK60 | Tackle Co-Sell | updated 2026-09-17 | https://tackle.io/tackle-platform/tackle-co-sell/ |
| TK61 | Tackle Offers | updated 2026-09-17 | https://tackle.io/tackle-platform/tackle-offers/ |
| TK62 | Salesforce Integration | updated 2025-09-24 | https://tackle.io/tackle-platform/salesforce-integration/ |
| TK63 | Strategic Services | updated 2026-08-13 | https://tackle.io/strategic-services/ |
| TK64 | Tackle Cloud GTM Platform, AWS Marketplace listing (public pricing) | fetched 2026-09-26 | https://aws.amazon.com/marketplace/pp/prodview-cfofnlysi75ug |
| TK65 | Tackle - HubSpot integration (Help) | 2026-04-08 | https://help.tackle.io/en/articles/14486577-tackle-hubspot-integration |
| TK66 | Microsoft Azure IP Co-sell requirements checklist (Help) | 2025-09-15 | https://help.tackle.io/en/articles/12295218-microsoft-azure-ip-co-sell-requirements-checklist |
| TK67 | AWS Co-Sell FAQs (Help) | 2026-01-21 | https://help.tackle.io/en/articles/10514011-aws-co-sell-faqs |
| TK68 | Express Private Offers (EPO) and Tackle FAQs (Help, Michael Crane) | 2026-08-12 | https://help.tackle.io/en/articles/16351548-express-private-offers-epo-and-tackle-faqs |
| TK69 | Selling Multiple Products Through a Reseller: Multi-Product Solutions and Offer Sets FAQs (Help) | 2026-08-12 | https://help.tackle.io/en/articles/16351721-selling-multiple-products-through-a-reseller-multi-product-solutions-and-offer-sets-on-aws- |
| TK70 | Pricing and payments for AWS (Help) | 2026-01-09 | https://help.tackle.io/en/articles/10447246-pricing-and-payments-for-aws |
| TK71 | Pricing and payments for Microsoft commercial marketplace (Help) | 2026-07-20 | https://help.tackle.io/en/articles/10535445-pricing-and-payments-for-microsoft-commercial-marketplace |
| TK72 | Pricing and payment for Google Cloud (Help) | 2025-11-05 | https://help.tackle.io/en/articles/10504368-pricing-and-payment-for-google-cloud |
| TK73 | Google Cloud Marketplace private offers FAQs (Help) | 2025-11-05 | https://help.tackle.io/en/articles/10509098-google-cloud-marketplace-private-offers-faqs |
| TK74 | How to opt-in for AWS concurrent agreements (Help, Michael Crane) | 2026-03-03 | https://help.tackle.io/en/articles/13908272-how-to-opt-in-for-aws-concurrent-agreements |
| TK75 | Reconcile AWS Marketplace payments (Help) | 2025-10-15 | https://help.tackle.io/en/articles/10535499-reconcile-aws-marketplace-payments |
| TK76 | Reconcile Microsoft payments (Help) | 2025-10-15 | https://help.tackle.io/en/articles/10535672-reconcile-microsoft-payments |
| TK77 | Reconcile Google Cloud payments (Help) | 2025-10-15 | https://help.tackle.io/en/articles/10535660-reconcile-google-cloud-payments |
| TK78 | Microsoft commercial marketplace FAQs (Help) | 2026-01-27 | https://help.tackle.io/en/articles/10542353-microsoft-commercial-marketplace-faqs |
| TK79 | What's new 2026 (Help) | 2026-08-26 | https://help.tackle.io/en/articles/13675718-what-s-new-2026 |
| TK80 | AWS Marketplace private offers FAQs (Help) | 2026-06-10 | https://help.tackle.io/en/articles/10504181-aws-marketplace-private-offers-faqs |
| TK81 | Associate Google Cloud partner private offers (Help) | 2025-11-05 | https://help.tackle.io/en/articles/11898587-associate-google-cloud-partner-private-offers |
| TK82 | Connect to Google Cloud for co-sell registration (Help) | 2026-05-22 | https://help.tackle.io/en/articles/15217465-connect-to-google-cloud-for-co-sell-registration |
| TK83 | Manage Google co-sell registrations from Salesforce (Help) | 2026-05-22 | https://help.tackle.io/en/articles/15217622-manage-google-co-sell-registrations-from-salesforce |
| TK84 | Microsoft partner private offers (Help) | 2026-08-19 | https://help.tackle.io/en/articles/11371959-microsoft-partner-private-offers |
| TK85 | AWS partner private offers (Help) | 2026-09-24 | https://help.tackle.io/en/articles/10707700-aws-partner-private-offers |
| TK86 | About Google Cloud private offers (Help) | 2025-12-15 | https://help.tackle.io/en/articles/10504349-about-google-cloud-private-offers |
| TK87 | Your Tackle subscription (Help) | 2025-09-29 | https://help.tackle.io/en/articles/10439728-your-tackle-subscription |
| TK88 | About marketplace scoring (Help) | 2025-10-30 | https://help.tackle.io/en/articles/10471584-about-marketplace-scoring |
| TK89 | Connect to Microsoft (Help) | 2026-09-16 | https://help.tackle.io/en/articles/10509617-connect-to-microsoft |
| TK90 | Automate your Microsoft co-sell referral workflows (Help) | 2026-06-25 | https://help.tackle.io/en/articles/11760081-automate-your-microsoft-co-sell-referral-workflows |
| TK91 | Manage Microsoft co-sell referrals from Salesforce (Help) | 2026-06-25 | https://help.tackle.io/en/articles/11395356-manage-microsoft-co-sell-referrals-from-salesforce |
| TK92 | What's new: Tackle for Salesforce 2026 (Help) | 2026-06-30 | https://help.tackle.io/en/articles/13675811-what-s-new-tackle-for-salesforce-2026 |
| TK93 | About AWS private offers (Help) | 2025-08-15 | https://help.tackle.io/en/articles/10447202-about-aws-private-offers |
| TK94 | Inside Tackle's Automation Everywhere Strategy: Agents, Workflows, and HubSpot (Dillon Woods), Cloud GTM XP | ~2026-05 (uploaded ~2026-07) | https://www.youtube.com/watch?v=1QWBGIkGtvA |
| TK95 | Marketplace PLG and the Agentic Future of Co-Sell for ISVs on AWS (AWS: Reagan, Vinod Nair), Cloud GTM XP | ~2026-05 | https://www.youtube.com/watch?v=tGnzjugokW0 |
| TK96 | How the Microsoft Marketplace Drives Channel-Led Cloud Growth (Microsoft speaker), Cloud GTM XP | ~2026-05 | https://www.youtube.com/watch?v=k1iyBo4leLc |
| TK97 | Building and Monetizing AI Agents on Google Cloud Marketplace (Dai Vu, Google), Cloud GTM XP | ~2026-05 | https://www.youtube.com/watch?v=TC0e0KdeSlg |
| TK98 | How Datadog Scaled Co-Sell Into a Growth Engine (Adam Clair Cooper), Cloud GTM XP | ~2026-05 | https://www.youtube.com/watch?v=c4dWmbecUhw |
| TK99 | How CrowdStrike Scaled Cloud GTM to Billions in Marketplace Transactions, Cloud GTM XP | ~2026-05 | https://www.youtube.com/watch?v=NTX9f5ZEMWI |
| TK100 | The Future of Cloud GTM in the AI Era, Cloud GTM XP Opening Keynote (John Jahnke; Salesforce's Tyler Carlson) | ~2026-05 | https://www.youtube.com/watch?v=cADMxRJjlU8 |
| TK101 | How GitLab Consolidated Its Multi-Hyperscaler Marketplace Motion, Cloud GTM XP | ~2026-05 | https://www.youtube.com/watch?v=unvFJr6WdJw |
| TK102 | Honeycomb's Guide for Evaluating a Cloud GTM Partner, Cloud GTM XP | ~2026-05 | https://www.youtube.com/watch?v=bWbT9nrAAn4 |
| TK103 | How Seeq Runs a Multi-Cloud Marketplace Strategy as a Team of One, Cloud GTM XP | ~2026-05 | https://www.youtube.com/watch?v=30Bckf4K0EI |
| TK104 | Co-Building What's Next: Scaling Cloud GTM Through Channels and Global Expansion (WWT, Google, Microsoft), Cloud GTM XP 2025 | 2025-05 | https://www.youtube.com/watch?v=bAFT9xz4W2Y |
| TK105 | AppDirect and Tackle.io to Unite (Business Wire) | 2025-12-01 | https://www.businesswire.com/news/home/20251201840606/en/AppDirect-and-Tackle.io-to-Unite-to-Extend-Leadership-in-B2B-Subscription-Commerce-with-Native-Hyperscaler-Marketplace-Integration |
| TK106 | AppDirect acquires PartnerStack in sixth deal in 12 months (The Next Web, INDEPENDENT) | 2026-04-14 | https://thenextweb.com/news/appdirect-acquires-partnerstack-partner-led-growth-b2b-commerce |
| TK107 | AppDirect acquires PartnerStack for upwards of $150 million USD (BetaKit headline, INDEPENDENT, not fetched) | 2026-04 | https://betakit.com/appdirect-acquires-partnerstack-to-build-unified-platform-for-partner-led-growth/ |
| TK108 | Managing disbursements (AWS Marketplace Seller Guide, OFFICIAL) | fetched 2026-09-26 | https://docs.aws.amazon.com/marketplace/latest/userguide/managing-disbursements.html |
| TK109 | Refund policy for Microsoft Marketplace (Microsoft Learn, OFFICIAL) | 2025-04-09 | https://learn.microsoft.com/en-us/marketplace/refund-policies |
| TK110 | Tackle YouTube channel (@tackleio; 184 videos, 283 subscribers) | fetched 2026-09-26 | https://www.youtube.com/@tackleio |
| TK111 | Tackle sitemap index and help center sitemap | fetched 2026-09-26 | https://tackle.io/sitemap_index.xml ; https://help.tackle.io/sitemap.xml |
| TK112 | 4 Challenges Your Tackle Coach Can Help You Overcome | 2025-05-20, updated 2025-09-16 | https://tackle.io/blog/4-challenges-your-tackle-coach-can-help-you-overcome/ |
| TK113 | Data-Driven Strategies for Cloud GTM Success (Alex Murdoch) | 2024-12-10, updated 2025-11-13 | https://tackle.io/blog/data-driven-strategies-for-cloud-gtm-success/ |
