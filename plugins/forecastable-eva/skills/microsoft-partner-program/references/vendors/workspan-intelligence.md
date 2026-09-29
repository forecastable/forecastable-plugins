# WorkSpan content intelligence
Built 2026-09-26. VENDOR source: operational detail, labeled; official pages win on conflicts.

Scope: WorkSpan (workspan.com), maker of WorkSpan Hyperscaler Edition, Ecosystem Edition and WorkSpan AI. Tags `WS1` onward resolve in Sources. Cross-reference tags point to our files: `A` = aws-intelligence.md, `M` = microsoft-intelligence.md, `G` = google-cloud-intelligence.md, `X` = cross-cloud-intelligence.md. Everything WorkSpan says is VENDOR unless a row says OFFICIAL confirmation was found.

Coverage achieved: full sitemap walked (400 URLs, 2026-09-26) [WS73]; 16 public help center articles read in full through the Zendesk API (the rest of the help center, including field-mapping and post-deployment guides, is login-gated) [WS2 to WS16]; 67 marketing, blog, event and resource pages fetched; 14 pages of the May 2026 "Running AI-Native Partnerships" report and research hub read [WS47 to WS54]; YouTube uploads list (262 videos) walked and 7 transcripts pulled (about 7.5 hours of content) [WS55 to WS61, WS67]; third-party pricing, reviews and funding checked [WS62 to WS65]. About 60 items read end to end.

---

## Ten takeaways that change how Alex or Eva advise

1. **The AWS S3-based CRM integration has a hard stop date, per WorkSpan: 2026-09-30.** WorkSpan's July 2026 customer notice says S3 inbound processing stops and outbound opportunity and lead sync ends on 2026-09-30, AWS revokes S3 bucket access on 2026-10-30, and begins decommissioning buckets on 2026-12-31 (download history before October 30) [WS2]. AWS docs say only that S3 integrations stopped accepting new requests in 2024; no end date is published [WS69][A47]. Today is 2026-09-26. Eva: any customer whose ACE sync still runs on S3 (any vendor, or homegrown) must be asked this week. Anyone who went live on WorkSpan's AWS integration after January 2025 is already on the API [WS2]. The API migration and the console (APN) migration are separate workstreams; do the API one first [WS2][WS3].

2. **The console migration has two dates in the field, and neither is on an AWS page.** WorkSpan's March 2026 webinar says AWS notification emails set **2026-09-30** as the final date to migrate Partner Central into the AWS console, while PDMs and PSMs pushed **2026-06-30** because that date is tied to having at least one listing PRM-tagged to stay eligible for funding requests [WS55]. WorkSpan's own blog and help center said June 30, 2026 was the shutdown date [WS1][WS3]. Our AWS file records no official deadline [A8][A11]. Advice stays the same: an unmigrated account is the first fix, and PRM tagging should be done in parallel [WS55][A12].

3. **Microsoft's Americas partner chief says out loud that sellers are paid on Marketplace.** Nina Harding (CVP, Americas Enterprise Partner Solutions, Microsoft), April 2026: "Marketplace is becoming the commercial backbone of co-sell. It's not an optional channel anymore, and our field is paid off of Marketplace transactions" and "the way that we pay the field on co-sell is all through Marketplace" [WS56][WS34]. This confirms our FY27 read [M13]. She also named what partners get wrong operationally: PRACR and PAL tagging ("the plumbing") that unlocks funding and visibility [WS56][M61].

4. **Microsoft now feeds partner success stories into its field AI.** Harding: partners can write AI-assisted success stories and use cases in Partner Center, which are "piped all over Microsoft and right into our sales agent tools" in MSX, and Microsoft uses AI to recommend partners into deals at industry, sub-industry and persona granularity [WS56]. NEW. Eva action: every Microsoft ISV customer should publish use-case stories in Partner Center, framed by industry and persona, not generic capability [WS56][WS36].

5. **The AWS seller comp number an ISV customer quoted: 42% quota retirement, only on Marketplace.** Qualtrics' AWS alliance leads (February 2025) said that under SRRP "AWS reps ... get 42% of our deal as quota retirement," that from 2025 this credit applies only when the deal transacts through Marketplace (in 2024 an ACE-registered deal the rep knew about was enough), and that they used MPOPP to give first-time Marketplace buyers 1% to 2% of TCV back [WS60]. AWS publishes no percentage [A84]. Treat 42% as one partner's figure for its own deals, from before SRRP was folded into the SaaS Co-Sell Benefit [A79]. Useful for Alex's business-case framing only if it's labeled.

6. **The best benchmark WorkSpan offers is the win-rate lift: 22% to 47%.** Across WorkSpan's customer base, win rates move from 22% to 47% when the cloud field rep is actually activated on an ISV opportunity rather than logged as "influence" [WS48][WS49]. That's WorkSpan's own customer data, with no sample size or method published. Pair it with the AWS-commissioned Canalys figures WorkSpan cites (frequent co-sellers: 51% higher revenue growth, 65% higher close rates, 54% larger deals) [WS48]. The operational point for Eva: activation means the ISV seller knows the covering AWS, Microsoft or Google rep, briefs them, and gets a meeting on both calendars before the architecture review [WS48].

7. **HubSpot: WorkSpan has a real native app for referrals on all three clouds. Private offers are still Salesforce-first.** Released 2024-08-12. You embed it in the HubSpot deal page. A native referral object lets you create, edit, accept, reject, launch and close referrals to AWS ACE, Microsoft Partner Center and Google. Deals can auto-create referrals, workflow triggers update referrals when deals change, and sync runs both ways [WS23][WS9]. An AWS VP (Matt Yanchyshyn) is quoted endorsing "WorkSpan's HubSpot connector" [WS24]. The catch: every private offer, CPQ and "Marketplace managed from your CRM" description names Salesforce only [WS18][WS19][WS24][WS25]. Value mapping for HubSpot is manual copy of picklist values from Settings > Data Management > Objects > Deals > Manage deal properties [WS10]. Alex's recommendation for a HubSpot customer: WorkSpan covers co-sell referrals both ways on all three clouds. Get private-offer creation from HubSpot demonstrated before signing.

8. **WorkSpan's ACE error catalog is a ready-made pre-submission checklist for Eva.** 56 ACE rejection messages with fixes [WS4]. The ones that bite most often: description under 50 characters; Next Step and Additional Comments over 255; contact title over 80; customer website equal to partner domain; zero or blank Expected Monthly AWS Revenue; target close date not in the future; US state spelled in full (no two-letter codes); Contract Vehicle and RFx number required for Government or Education ("Unknown" accepted); Closed Lost can't be the first sync; opportunity owner email must be an active ACE user. Duplicate detection keys on name, use case, expected MRR, customer website and close date. ISVA and SaaS revenue recognition launches need Customer Software Value, Procurement Type, contract start and end dates, plus "AWS field engaged", "Is this for Marketplace" and "net new business" [WS4]. CONFIRMS and extends our ACE field guidance [A43][A3].

9. **WorkSpan is priced for the enterprise, and it says it never taxes transactions.** "No transaction pricing ... not a toll collector": no charges based on referral volume, private offers or transacted revenue [WS17][WS21][X57]. Buyer-reported pricing (Vendr): median USD 48,000 a year (range 20,000 to 64,000); Hyperscaler Edition Pro about USD 72,000 a year for three clouds; AI Teammates add-on USD 10,000 a year; buyers report 17% to 31% discounts; Clazar's median is USD 13,560 [WS63]. Public AWS Marketplace listing for advisory work: USD 10,000 advisory, USD 4,500 listing support, USD 30,000 AI Sales Partnering Assistant plus USD 6,000 implementation (12 months) [WS62]. Listing-service calculator example: USD 9,000 setup for 4 listings, about USD 6,000 a year per private-offer listing and USD 9,000 a year per metered listing [WS21]. Hyperscaler Edition includes one managed listing [WS17][WS21].

10. **Read WorkSpan's copy with three known errors in mind.** (a) It says professional-services private offers on Microsoft Marketplace "count toward customer MACC" [WS25]; Microsoft says they don't [M34][M60]. (b) Its Google pages, support page (August 2026) and implementation guides still say "Google Partner Advantage" and ask for a Partner Advantage "Vector ID" [WS20][WS14][WS7]; Partner Advantage ended 2026-01-15 [G1]. (c) Its Google product page lists Google private-offer management as "in roadmap" [WS20], while an April 2025 post and the current use-case page say private offers from CRM are live [WS44][WS26]. Its scale claims also vary a lot across pages (see section 6). WorkSpan is also the most AWS-endorsed of the vendors: an AWS Launch Partner for the console migration, AWS-funded migration advisory, and named with Hyland in AWS's Partner Central agents launch post [WS1][WS24][WS68]. And Microsoft's venture arm M12 is an investor [WS65].

---

## 1. Vendor profile (VENDOR throughout)

| Item | Detail | Source |
|---|---|---|
| Company | Founded 2015; co-founders Mayank Bawa (CEO), Amit Sinha (President; ex-SAP HANA ecosystem), Milind Joshi (CTO). One April 2026 blog calls Amit Sinha "CEO" while the About page lists Bawa as CEO | [WS29][WS35][WS65] |
| Funding | About USD 66M total; Series C USD 30M (Insight Partners lead); Series D announced 2025-03-24, amount undisclosed. Investors include Mayfield, **M12 (Microsoft's venture fund)**, Insight Partners, Redline, Nautilus | [WS42][WS65] |
| Momentum claims | "Record quarter" for new business in Q1 2025 (11-year history); "15,000 companies on the WorkSpan network" | [WS43][WS29] |
| Products | **Hyperscaler Edition** (Starter, Pro, Premium, Enterprise; one or several clouds): co-sell automation, marketplace listing management, private-offer management, planning and reporting. **Ecosystem Edition** (ISV, GSI, reseller co-sell, CRM to CRM). **WorkSpan AI** (AI Teammates per partnership, "Partner Advantage card" in Salesforce, MCP orchestrator). **Marketplace Accelerator / Listing Service** (turnkey or fully managed listings, create or migrate in 2 to 4 weeks) | [WS17][WS21][WS22][WS16][WS57] |
| Clouds | AWS (ACE, Marketplace, Partner Central APIs), Microsoft (Partner Center Referrals API, Marketplace), Google (Partner Network Hub API "v2", Marketplace). Also Oracle for some customers (NVIDIA lead exchange) and SAP co-sell | [WS17][WS32][WS11] |
| CRMs | Salesforce (managed package "WorkSpan Ecosystem Cloud", v1.40.3 current), **HubSpot (native public app)**, Dynamics 365, ServiceNow CRM (NOW Assist agent, May 2026). Integrations directory also lists Freshworks, Pipedrive, SugarCRM, Zoho, Crossbeam, Reveal, Slack | [WS11][WS9][WS28][WS31] |
| AWS API coverage | Selling API (ACE bidirectional, "Launch in ACE"); Benefits API (funding eligibility at opportunity level: built December 2025, usable from April 2026); Solutions API and Partner Profile API (January 2026); Leads API (April 2026); all need console migration plus an updated CloudFormation template in WorkSpan's ACE setup. Private offers, CPPO, ISVA and SRRP fields, multi-product Solution Marketplace Offerings, Express Private Offers | [WS3][WS24][WS31][WS4] |
| Microsoft API coverage | Referrals API via OAuth, using a Referral Admin service account; replaces Power Automate flows (disable them first to avoid duplicates); fuzzy account matching to Microsoft-managed accounts; MPO, professional-services private offers, multi-currency | [WS5][WS25][WS11] |
| Google API coverage | "Google v2" Partner Network Hub API: allowlisting through WorkSpan with Partner ID, plus Integrator role for a WorkSpan service account; "ISV Deal Registration API" integration (April 2025); SaaS listings; private offers and MCPO lifecycle (see conflict in takeaway 10) | [WS7][WS8][WS44][WS26] |
| Agentic and MCP | AI Teammates (GA 2025); listed on AWS AI Agent Marketplace at launch (2025-07-17); MCP Orchestrator behind a ServiceNow NOW Assist agent, with optional enrichment from the AWS Partner Central MCP (2026-05-04); named with Hyland in AWS's Partner Central agents launch (funding-eligibility pilot) | [WS30][WS31][WS53][WS68] |
| Pricing | Flat annual, no transaction fees; see takeaway 9 | [WS17][WS63][WS62][WS21] |
| Named customers (public) | AWS: Boomi, Qualtrics, Hyland, Deepwatch, Tealium, Wipro, ClearScale, Deloitte, Datastax, MongoDB, Mindtickle. Microsoft: Abnormal Security, Avanade, Capgemini, DocuSign. Google: Palo Alto Networks, Databricks, SAP, MongoDB, Reltio. Multi-cloud: NVIDIA, Cisco, Red Hat | [WS17][WS25][WS26][WS32][WS70] |
| Support model | Follow-the-sun (APJ, CET, EST, PST); P0 24x7 phone, P1 1-hour target (24x5), P2 next business day | [WS14] |
| Third-party reviews | G2 4.3 of 5 (29 reviews). Pros: co-sell efficiency, reporting, responsive support. Cons: confusing UI for new users, slow page loads, Salesforce package setup gaps | [WS64] |
| Strengths | Deepest enterprise references on AWS co-sell volume (AWS execs quoted calling WorkSpan the "#1 provider of ACE referrals ... volume and value" [WS24]); only vendor we found with native HubSpot, Dynamics and ServiceNow co-sell apps; multi-partner and GSI orchestration beyond hyperscalers; flat pricing; strong Microsoft sponsorship (Project Ascend) | [WS24][WS56][WS23][WS31] |
| Weaknesses | Enterprise price point; Salesforce-first private offers; stale Google naming; inconsistent headline metrics; heavy dependence on Professional Services for setup (Microsoft and Google steps end with "WorkSpan PS will complete the rest"); much of the help center is login-gated | [WS63][WS5][WS7][WS20] |
| Bias to watch | Frames Tackle, Clazar and Suger as "legacy" connectors that "move data" [WS30]. Its research concludes that a "partner revenue platform" is required [WS47]. AWS funds its migration advisory (about USD 3,000 per partner) [WS24]. M12 is an investor [WS65]. Customer numbers are self-reported | [WS30][WS47][WS24][WS65] |
| Community content | Ecosystem Aces podcast **dormant** (215 episodes, last 2025-02-02). Replaced by the "Partners in Revenue" interview blog and short-video series (March to August 2026), quarterly **Partner Signal Live** (April 2, 2026), Sales Partnership Summit (January 22, 2026), and the May 2026 "Running AI-Native Partnerships" report with BlueThread | [WS66][WS67][WS72][WS47] |

---

## 2. AWS: extracted substance

| Fact | Status | Our tag | Vendor tag | Date |
|---|---|---|---|---|
| S3-based CRM integration: inbound stops and outbound sync ends 2026-09-30; bucket access revoked 2026-10-30; decommissioning starts 2026-12-31. AWS docs give no date (only "stopped accepting new requests" in 2024). Could not confirm officially | NEW (UNVERIFIED) | [A47] says EOL not published | [WS2][WS69] | 2026-07-01 |
| API (S3 to Selling API) migration and console/APN migration are separate; do API first; WorkSpan estimates 2 to 4 hours including testing; customers live after January 2025 already on API | NEW | [A47] | [WS2][WS3] | 2026-07-01 |
| Console migration final date 2026-09-30 per AWS emails; 2026-06-30 pushed by PDMs because it aligns with PRM tagging for funding eligibility | CONFLICT | [A8][A11][A102] | [WS55] | 2026-03-11 |
| Console migration downtime 30 minutes to about 6 hours depending on opportunity volume; WorkSpan's own took 4.5 to 5 hours | CONFIRMS (range) | [A8] (2 to 6 h) | [WS55] | 2026-03-11 |
| Link the **primary Marketplace seller account** (where private offers transact and disbursements land), not the org management account; linked account cannot be free tier, org management, or sandbox or developer | NEW (detail) | [A8] | [WS55] | 2026-03-11 |
| Business verification needs Alliance Lead name and email, legal business name, tax ID matching registration jurisdiction, government photo ID plus selfie via QR code | NEW (detail) | [A8] | [WS55] | 2026-03-11 |
| User onboarding: download partner user CSV first; IAM option for fewer than 20 users; IAM Identity Center for org setups; external IdP (for example Okta) supported; Skill Builder-only "technical staff" users need no console access | NEW | [A8] | [WS55] | 2026-03-11 |
| Migration moves profile, solutions, leads, fund requests and alliance lead contact; no partner activity (opportunities, fund requests) during window; warn ACE users in advance | CONFIRMS | [A8] | [WS55][WS3] | 2026-03-11 |
| New PC 3.0 APIs: Leads (ingest, qualify, convert), Solutions (single and multi-product), Benefits (eligibility, apply, status, claimable amounts at opportunity level), Partner Profile; "PC 3.0 is a UX change, not a new API version" | CONFIRMS | [A48] | [WS3] | 2025-12-22, upd 2026-06-18 |
| Partner Central agents MCP server exposes "eight agent-callable tools" (pipeline insights, opportunity summary, sales play, customer profile, solution recommendation, funding recommendation, next steps, opportunity progression) at partnercentral-agents-mcp.us-east-1.api.aws/mcp | CONFLICT (framing) | [A48] lists MCP tools `sendMessage` and `getSession`; the eight are agent capabilities reached through chat | [WS53] | 2026-05 |
| WorkSpan and Hyland named in AWS's Partner Central agents launch as a funding-program pilot | CONFIRMS (OFFICIAL) | [A78] | [WS53][WS68] | 2026-03-16 |
| Free migration advisory funded by AWS, "about USD 3,000 per partner," open to non-customers (advisory@workspan.com) | NEW | none | [WS24][WS1][WS55] | 2026-07-01 | <!-- VALIDATE-OK[person-address]: published role mailbox, not a person -->
| ACE validation catalog: 56 messages with fixes (see takeaway 8), including duplicate keys, 255 and 80 character limits, 50-character minimum description, US state spelled out, Government and Education fields, Consulting partners must add 12-digit AWS Account ID to Launch | NEW (detail) | [A43][A47] | [WS4] | 2024-06-28, upd 2025-05-21 |
| ISVA and SaaS revenue recognition launch fields: Customer Software Value (number and currency), Procurement Type, Contract Start and Expiration; plus AWS field engaged, Is Marketplace, net new | NEW (detail) | [A43] | [WS4] | 2025-05-21 |
| To close an opportunity as Closed Lost it must first sync at an earlier stage and get an APN ID | NEW | [A43] | [WS4] | 2025-05-21 |
| "Unable to obtain exclusive access to this record" errors come from ACE congestion; resubmit | NEW | none | [WS4] | 2025-05-21 |
| SRRP quota retirement: AWS reps get "42% of our deal"; from 2025 only on Marketplace-transacted deals, in 2024 ACE-registered deals counted too | NEW (UNVERIFIED, customer statement, source dated 2025-02) | [A84] says not published; [A79] | [WS60] | 2025-02-25 |
| MPOPP gave first-time Marketplace buyers 1% to 2% of TCV "every other quarter"; one ISV returned over USD 3.5M in AWS credits to customers in 2024 | STALE (MPOPP relaunched self-service, year-round, August 2025) | [A31][A7] | [WS60] | 2025-02-25 |
| Low propensity-to-buy accounts can unlock more AWS funding; high-propensity accounts are where you burn EDP | NEW (practitioner) | none | [WS60] | 2025-02-25 |
| Propensity-to-Buy = AWS "Marketplace Engagement Score," surfaced on outgoing ACE referrals via ACE plus AMMP integration | NEW (source dated 2024-05) | none | [WS45] | 2024-05-03 |
| "AWS uses your recommendation score to decide who they sell with"; every referral builds or damages it | CONFIRMS (vendor framing) | [A47][A71] | [WS24] | 2026-07-01 |
| Brian Bohan (AWS consulting partner CoE): show up in AWS's AI recommendation engines by sharing every opportunity through ACE and your wins by industry; Pattern Partner program with "SWAT teams" for AI-native services firms; Marketplace is one of five strategic pillars for 2026 | NEW | none | [WS61][WS37] | 2026-01-22 |
| Deloitte: ACE bulk functionality "going away" later in 2026 | NEW (UNVERIFIED) | none | [WS61] | 2026-01-22 |
| Seller Prime (per an AWS Marketplace BD speaker): USD 40K MDF per ISV (not per listing) once a PLG-ready product is listed; List and Sell credits quoted as both 5K and 15K in the same session | CONFIRMS $40K; CONFLICT on credits | [A86][A30] ($10K VENDOR) | [WS59] | 2025-09-04 |
| AWS Marketplace: over 90% of transactions self-service; 99% of top 10,000 AWS customers transact on Marketplace; 90% of self-service buyers expect a free trial and 25% will not consider a product without one | CONFLICT (80%+ in [A93]); rest NEW | [A93][X49] | [WS59] | 2025-09-04 |
| Link Marketplace account to ACE so private offers can be linked to co-sell opportunities | CONFIRMS | [A43][A95] | [WS59] | 2025-09-04 |
| Boomi: 3,000% YoY Marketplace growth; 1,200 co-sell opportunities in six months; referrals out +146%, referrals in +119%, ACE launches +67%, Marketplace TCV 6.5x; 400 to 500 renewals through Marketplace renew earlier with less negotiation | NEW (case study) | none | [WS50][WS70] | 2026-05 |
| Stack AWS programs: Workload Migration Program (rebate) plus Marketplace promotions plus Gen AI competency | CONFIRMS | [A68] | [WS50] | 2026-05 |
| Multi-product solutions let services partners bundle SI services, ISV software and AWS into one purchasable offer | CONFIRMS | [A60][A29] | [WS37][WS1] | 2026-01-27 |
| November 2023 ACE V2 change: referrals default to co-sell and net new until V2; V2 adds For Visibility Only and renewal types | STALE (historic) | [A42] | [WS46] | 2023-11-22 |

---

## 3. Microsoft: extracted substance

| Fact | Status | Our tag | Vendor tag | Date |
|---|---|---|---|---|
| "Our field is paid off of Marketplace transactions"; co-sell and Marketplace are one motion; Marketplace sits inside the partner org | CONFIRMS (Microsoft executive, on vendor stage) | [M13] | [WS56][WS34] | 2026-04-02 |
| PRACR and PAL tagging is the "plumbing" partners most often get wrong; it unlocks funding, visibility and field traction | CONFIRMS | [M61][M13] | [WS56] | 2026-04-02 |
| Partners can publish AI-drafted success stories and use cases in Partner Center; these feed MSX and field sales agents; Microsoft uses AI to recommend partners into deals | NEW | none | [WS56] | 2026-04-02 |
| Microsoft maps partners by industry, sub-industry and persona value propositions to make them available to the field | NEW | none | [WS56][WS36] | 2026-04-02 |
| Project Ascend (FY24 to FY26): 45,000 opportunities shared with Microsoft through WorkSpan, USD 27B pipeline, USD 5.2B revenue for partners; Microsoft sponsored API automation for its software development companies | NEW (VENDOR figures on stage) | none | [WS56] | 2026-04-02 |
| WorkSpan claims over USD 1B in Microsoft co-sell pipeline processed | NEW; inconsistent with the USD 27B figure above | none | [WS25] | 2026-04-22 |
| Referrals API setup: service account with Referral Admin (guide also says log in with Partner Center Admin); OAuth; select the company name exactly as shown in Partner Center Account settings > Company details | CONFIRMS | [M10][M11] | [WS5] | 2025-07-10, upd 2026-06-18 |
| **Disable Power Automate co-sell flows before enabling API integration** or referrals duplicate | NEW | [M11] | [WS5] | 2026-06-18 |
| Personal accounts break integrations when the person leaves (refresh token invalid); use a service account | NEW | none | [WS5] | 2026-06-18 |
| FY26 Solution Areas (AI Business Solutions, Cloud and AI Platforms, Security, Microsoft Unified) and 17 Solution Plays; mandatory in Partner Center from **2025-08-09** (moved from July 31) | CONFLICT (date) | [M7] (July 31, 2025) | [WS6] | 2025-07-28 |
| Salesforce users must deactivate old Solution Play and Area picklists, add new values, set field dependencies and a temporary validation rule; WorkSpan CRM users get it automatically | NEW (runbook) | [M11] | [WS6] | 2025-07-28 |
| WorkSpan auto-matches CRM accounts to Microsoft-managed accounts (fuzzy match) before submission; Salesforce field "MPC Account Match Status" | CONFIRMS need | [M6][M7] | [WS25][WS11] | 2026-04-22 |
| Partner Center tracks response times, referral quality, account-match accuracy and close rates; clean execution gets more inbound | CONFIRMS | [M8][M9] | [WS25] | 2026-04-22 |
| **Professional-services private offers count toward customer MACC** | CONFLICT (vendor wrong) | [M34][M60] | [WS25] | 2026-04-22 |
| Multi-currency Marketplace transactions (India, Germany, Japan) with local tax handled | NEW (vendor capability) | none | [WS25] | 2026-04-22 |
| Abnormal Security with WorkSpan: 60% to 70% higher acceptance of co-sell referrals, 80% to 97% less time per submission, 15x referrals per month | NEW (case study) | none | [WS29][WS19] | 2025 |
| Microsoft "40K partners" (ISV page framing) | NEW (unsourced) | none | [WS19] | 2026-04-22 |

---

## 4. Google Cloud: extracted substance

| Fact | Status | Our tag | Vendor tag | Date |
|---|---|---|---|---|
| Co-sell API access ("Google v2") requires **allowlisting**: submit Partner name, type (ISV or SI), Partner ID (10-character alphanumeric, Hub > Account) to the vendor | NEW | [G72] | [WS7][WS8] | 2025-05-20 |
| Grant access: Hub > Users (partners.cloud.google.com/users) > Assign roles > service account `google-cosell-client-prod@workspan-app.iam.gserviceaccount.com` > Integrator | CONFIRMS | [G72] | [WS7][WS8] | 2025-08-25 | <!-- VALIDATE-OK[person-address]: published role mailbox, not a person -->
| New customers also supply an 18-digit "Vector ID" (starts 0014) from Partner Advantage > My Account > Account ID | STALE (portal retired 2026-01-15) | [G1] | [WS7] | 2025-05-20 |
| WorkSpan product, support and integration pages still say "Google Partner Advantage" (including an August 2026 support page) | STALE | [G1][G70] | [WS20][WS14][WS28] | 2026-08-27 |
| WorkSpan integrated Google's "Deal Registration API" for ISV deal registration from CRM (Google Next 2025) | NEW | google file 6.6: public API not documented | [WS44] | 2025-04-10 |
| Private offers for SaaS listings from CRM; MCPO authorization lifecycle | CONFLICT (vendor internal: product page says "in roadmap") | [G26] | [WS44][WS26][WS20] | 2025-04 to 2026-04 |
| Referrals sync both ways (CRM to Hub when criteria met; Google referrals land as new CRM opportunities); "works with Salesforce, Dynamics and HubSpot" | NEW (claim) | google file 6.4 | [WS26] | 2026-04-22 |
| Manual flow without tooling: Hub for referrals, CRM for opportunity, Marketplace console for private offer, back to Hub to link; "45 minutes per deal" | NEW (vendor estimate) | none | [WS26] | 2026-04-22 |
| Google Marketplace listings: flat fee or usage-based SaaS pricing, hybrid and custom terms; expiration and publishing alerts | CONFIRMS | [G26] | [WS26] | 2026-04-22 |
| Palo Alto Networks: joint pipeline with Google "almost a billion dollars"; WorkSpan is system of record for joint pipeline reviews | NEW (customer quote) | none | [WS32] | 2026-01-23 |
| "Coming July 2025" partner communication tools for MCPO | STALE (undated follow-up) | none | [WS26] | 2026-04-22 |

---

## 5. Cross-cloud playbooks and benchmarks worth reusing

1. **Sequence AWS migrations: S3 to API first, then console, then PRM tagging in parallel.** Confirm whether the ACE integration is S3 or API; schedule the console migration off-hours after exporting the user CSV and mapping roles to IAM policies; tag one primary listing for PRM so funding requests keep working [WS2][WS3][WS55][A12].
2. **Pre-submission ACE checklist (Eva).** Before any submit: description 50 or more characters and customer-specific; Next Step and Comments at or under 255; contact title at or under 80; customer domain differs from yours; positive MRR; future close date; state spelled out; Government or Education fields filled ("Unknown" works); owner email is an active ACE user; not a duplicate on name, use case, MRR, website and close date [WS4].
3. **Qualtrics' AWS vertical sprint.** One AWS vertical per month (Healthcare, then Travel and Hospitality, then Financial Services, then Public Sector). List existing contracts and upsells in that vertical, check propensity-to-buy, move renewals onto Marketplace ("lift and shift looks net new to AWS"), and register everything in ACE [WS60].
4. **Be ruthless about introductions.** Qualtrics set up AE-to-AWS intro calls in fewer than 50% of cases where AWS asked, to "stack successes"; one alliance lead ran 560 rep alignment calls in a year [WS60].
5. **"Landing zones" when your buyer is not AWS's buyer.** Ask the AWS rep to have their champion (often the CIO or procurement) pull your deal onto Marketplace for PPA burn-down and credits. Procurement then contacts you proactively [WS60].
6. **Attach early to reserve commit.** Send new opportunities to AWS at creation to get propensity data and relationship context. Ten months later AWS has carved budget inside the customer's private pricing agreement for your deal [WS60].
7. **Formal private-offer delivery beats a bare link.** Customers ignored raw private-offer emails from an unknown sender; a formatted, CRM-generated notification raised acceptance before expiry [WS60].
8. **Kyle Hayes' marketplace ops checklist.** (a) Build a full-year plan with the PDM on their priorities and commit targets, with pre-built joint messaging; (b) a seller qualification checklist that captures the customer's billing account ID, partner involved, and net new vs upsell up front (a missing billing ID stalls private offers); (c) document how your quote, contract and approval steps map to the hyperscaler transaction flow; (d) a standing line between PDM, alliances, ops and CRO; (e) short internal and customer-facing "do these four things" guides [WS33].
9. **Four misconceptions that stall listings:** storefront mentality, commit-spend tunnel vision, misunderstanding that you are a partner inside the hyperscaler's ecosystem, and comp that doesn't reward (or penalizes) routing deals through Marketplace [WS33].
10. **Microsoft field attention.** Lead with an industry, sub-industry and persona use case, not "we can do anything"; tell the rep their economics and how you transact; publish success stories in Partner Center; capture wins with named reps as internal references (sellers are "coin operated and ego-driven") [WS56].
11. **Pre-pipeline deliverable per strategic partner:** persona-level joint value proposition, seller-to-seller introductions before a deal exists, account priority mapping, and transaction mechanics. Test: can a new partner seller co-sell with you within days? [WS34]
12. **Triple play for enterprise deals.** Assign distinct roles (hyperscaler = platform, Marketplace and commit burn-down; ISV = core capability; SI = industry delivery and change management) and build one customer narrative. Avoid role overlap or the customer cuts a partner [WS35].
13. **JBP template (5 to 15 pages):** thesis (why this year), 3 to 5 targets (sourced pipeline, attached pipeline, Marketplace consumption, logos, seller activation rate), 5 to 8 motions each with an owner pair on both sides, funding matched to motions (MDF, MAP, SAF, ISVA, technical hours), and a rhythm (weekly motion review, monthly pipeline sync, QBR, half-year reset). Failure mode: motions that assume funding the hyperscaler hasn't committed [WS52].
14. **SI accelerator math (services partners).** One USD 100K accelerator deliverable in 8 weeks, pitched to 8 to 10 hyperscaler AEs with 8 to 10 accounts each, gives your real pipeline; expect to close about 10% with disciplined follow-up. Narrowing to 2 industries and 3 products drove 300% pipeline growth for one SI [WS41].
15. **PLG on AWS Marketplace:** list a PLG-ready product (self-serve signup, entitlement and metering integrated, free trial), add "Try free with AWS" and Buy with AWS CTAs, use Seller Prime MDF for top-of-funnel campaigns, and track in Seller Prime marketing dashboards [WS59][A61].
16. **Resellers and MSPs now co-sell too.** Bring PRM deal registrations into the co-sell platform to run CPPO or MPO with the ISV and hyperscaler together; for MSPs, co-sell against pre-bought inventory burn-down [WS58][WS27].

---

## 6. Survey and benchmark data

| Figure | Sample / basis | Date | Label |
|---|---|---|---|
| Win rate 22% without vs 47% with activated cloud field rep | WorkSpan customer base; no n or method | 2026-05 | VENDOR [WS48] |
| Frequent co-sellers: 51% higher revenue growth, 65% higher close rates, 54% larger deals | Canalys study commissioned by AWS, cited by WorkSpan | undated in source | INDEPENDENT, commissioned [WS48] |
| AWS Marketplace sellers close 27% more deals, 40% shorter cycles | Forrester TEI commissioned by AWS, cited | undated in source | INDEPENDENT, commissioned [WS49] |
| 6.3 partners in the average enterprise deal; over 10 on large deals; 2/3 of tech sold on subscription or consumption | Jay McBain (Canalys/Omdia) interview in WorkSpan report | 2026-04-23 | INDEPENDENT via VENDOR [WS47] |
| "90% of partner sellers stay dormant" | Seller-activation research "underway with the AWS Marketplace Center of Excellence" | 2026-06 | VENDOR, preliminary [WS71] |
| Two-thirds of B2B leaders expect partner-influenced revenue to grow over 30% YoY; 67% name alliances top 2026 priority | Forrester, cited | 2025 to 2026 | INDEPENDENT via VENDOR [WS48][WS39] |
| Shared pipeline: 350K cloud referrals, USD 50B referral pipeline under management | Product page | lastmod 2026-04-22 | VENDOR [WS17] |
| 1,000,000 co-selling opportunities synced | Same product page | 2026-04 | VENDOR [WS17] |
| 578K opportunities shared, USD 78B pipeline exchanged | Homepage and About | 2026-08 | VENDOR [WS29] |
| About 500K partner opportunities across 100+ partners (AWS page); "#1 referrer of private offers by volume and value" | AWS use-case page | 2026-07 | VENDOR [WS24] |
| USD 513B shared joint pipeline, USD 196B closed (April 2026); USD 542B shared (May 2026) | Blog and research hub | 2026-04 to 05 | VENDOR [WS40][WS54] |
| Microsoft Project Ascend FY24 to FY26: 45,000 opportunities, USD 27B pipeline, USD 5.2B revenue | WorkSpan slide presented with a Microsoft CVP | 2026-04-02 | VENDOR [WS56] |
| Platform outcomes: 20%+ more pipeline shared, 27%+ higher partner win rates, up to 90% less manual effort, 84% larger deals; 40% faster deal cycles | WorkSpan customers | 2024 to 2026 | VENDOR [WS16][WS23][WS39] |
| DIY CRM connectors: "about 30% of opportunities need manual fixes" | WorkSpan claim | 2026-04 | VENDOR [WS28] |
| Committed spend "flowing through marketplaces" USD 450B; marketplace "a USD 150B channel" | WorkSpan blogs | 2026-04 | VENDOR, conflicts with Omdia (USD 30B 2024 sales; about USD 470B committed spend total) [WS38][WS39][X40] |
| Seller Prime stats: over 90% self-service transactions; 99% of top 10,000 AWS customers transact; 90% expect trials, 25% won't consider without | AWS Marketplace BD speaker | 2025-09-04 | OFFICIAL speaker on VENDOR webinar [WS59] |
| Qualtrics: seven to nine figures on Marketplace in one year; 700% growth in shared referrals; USD 50M+ through Marketplace in a year; about 20 hours a week saved on ACE entry | Customer webinar | 2025-02-25 | VENDOR [WS60] |
| Demandbase: partner share of new-logo revenue 2% to 3% rising to 23% in two years | Customer interview | 2026-07-06 | VENDOR [WS53a] |
| KGAM SI client: USD 9M ecosystem revenue, then 300% pipeline increase after focusing | Consultant interview | 2026-08-11 | VENDOR [WS41] |

Data-quality note for Alex: WorkSpan's headline scale numbers are not one consistent series (350K referrals vs 578K opportunities vs 1M synced; USD 50B vs 78B vs 542B). Quote a figure only with its page and date.

---

## 7. Conflicts with our intelligence files

| # | Topic | Our value (source) | WorkSpan value (source) | Which wins and why |
|---|---|---|---|---|
| 1 | AWS console migration deadline | No official date [A8][A11]; WorkSpan June 30, 2026 [A102]; Suger no date [A9] | 2026-09-30 final per AWS emails; 2026-06-30 tied to PRM tagging for funding [WS55]; blog FAQ even says "June 30, 2025" (typo) [WS1] | Unresolved. No AWS page states either. Keep "no published date" and add the 09-30 email claim as UNVERIFIED |
| 2 | S3 CRM integration end of life | Not published [A47][WS69] | 2026-09-30 stop, 10-30 access revoked, 12-31 decommission [WS2] | Official silence; WorkSpan's is a customer notice citing AWS sunset dates. Act on it (low cost) but label UNVERIFIED |
| 3 | Partner Central MCP tools | Two MCP tools, `sendMessage` and `getSession` [A48] | "Eight agent-callable tools" [WS53] | Official docs win. The eight are agent capabilities reached through the two tools |
| 4 | Microsoft professional services and MACC | Professional services excluded from MACC and CSD MBS [M34][M60] | "Services revenue counts toward customer MACC" [WS25] | Microsoft wins. Vendor error; don't repeat to customers |
| 5 | Microsoft FY26 Solution Play mandatory date | API compliance by July 31, 2025 [M7] | Moved to August 9, 2025 [WS6] | Historic; both dated 2025. Microsoft doc governs; WorkSpan may reflect a later Microsoft notice. Irrelevant for FY27 except as a precedent that deadlines slip |
| 6 | Google portal naming | Partner Network Hub; Partner Advantage ended 2026-01-15 [G1] | Partner Advantage and Vector ID still used [WS7][WS14][WS20] | Google wins; WorkSpan copy is stale |
| 7 | AWS Marketplace self-service share | "More than 80%" (VENDOR quoting AWS) [A93] | "Over 90%" (AWS speaker, 2025-09) [WS59] | Neither official in print; use "80% to 90%" with source |
| 8 | List and Sell credits | USD 10K (VENDOR) [A25]; official page no amount [A30] | 5K and 15K both said in one session [WS59] | Unverified; keep "amount not published" |
| 9 | Marketplace market size | Omdia USD 30B sales 2024; about USD 470B committed spend across the three clouds [X40] | "USD 450B committed spend flowing through marketplaces"; "USD 150B channel" [WS38][WS39] | Omdia wins; WorkSpan conflates commitments with marketplace flow |
| 10 | SaaS Co-Sell Benefit percentage | Not published [A84] | 42% quota retirement (one ISV, early 2025) [WS60] | Keep "not published"; cite 42% only as a labeled anecdote |
| 11 | MPOPP mechanics | Self-service, year-round, next-business-day credits (from August 2025) [A31] | "Every other quarter," 1% to 2% of TCV [WS60] | Official wins; WorkSpan source predates the relaunch (STALE) |

---

## 8. Content inventory (published or updated since 2025-07-01, plus older items still cited)

| Date | Type | Title | Cloud | URL | Substance (1 to 3) |
|---|---|---|---|---|---|
| 2026-09-17 | Help center | WS SFDC App Installation Guide (v1.40.3) | All | https://support.workspan.com/hc/en-us/articles/18749778537491 | 2 |
| 2026-09-17 | Help center | Salesforce App Package Upgrade Guide | All | https://support.workspan.com/hc/en-us/articles/44524164267283 | 2 |
| 2026-08-27 | Help center | WorkSpan Support (SLAs) | All | https://support.workspan.com/hc/en-us/articles/54846043383187 | 1 |
| 2026-08-11 | Blog | From One Win to a Revenue Engine: KGAM Playbook for SIs | All | https://www.workspan.com/blog/from-one-win-to-a-revenue-engine-the-kgam-playbook-for-system-integrators | 2 |
| 2026-08-11 | Blog | Franz-Josef Schrepf's Playbook for Scaling a Partner Desk With AI | None | https://www.workspan.com/blog/franz-josef-schrepfs-playbook-for-scaling-a-partner-desk-with-ai | 1 |
| 2026-08 | Blog | Maurits Pieper's Playbook for Starting a Partner Program | None | https://www.workspan.com/blog/maurits-piepers-playbook-for-starting-a-partner-program-the-right-way | 1 |
| 2026-07-06 | Blog | How Kim Tremblay Grew Partner Revenue from 2% to 23% | None | https://www.workspan.com/blog/how-kim-tremblay-grew-partner-revenue-from-2-to-23 | 1 |
| 2026-07-06 | Blog | How Tom Gavenonis Makes Partners a Pillar of Top-Line Revenue | None | https://www.workspan.com/blog/how-tom-gavenonis-makes-partners-a-pillar-of-top-line-revenue | 1 |
| 2026-07-01 | Help center | WorkSpan AWS Partner Central API Migration (S3 sunset dates) | AWS | https://support.workspan.com/hc/en-us/articles/53078418454675 | 3 |
| 2026-07-01 | Web page | WorkSpan for AWS Partnerships (use case) | AWS | https://www.workspan.com/use-case/aws-partnership | 2 |
| 2026-06-18 | Help center | AWS Partner Central 3.0 API Guide (upd) | AWS | https://support.workspan.com/hc/en-us/articles/47607948575379 | 3 |
| 2026-06 | Event | Strategy Salon (seller-activation research with AWS Marketplace CoE) | AWS | https://www.workspan.com/events-and-webinar/strategy-salon----an-afternoon-for-partner-leaders-at-the-heart-of-data-ai | 1 |
| 2026-06-16 | Blog | The Partner Manager's Job Has Split in Two | All | https://www.workspan.com/blog/the-partner-managers-job-has-split-in-two | 1 |
| 2026-05 | Report | Running AI-Native Partnerships (WorkSpan and BlueThread) | All | https://www.workspan.com/ai-native-partnerships/ | 2 |
| 2026-05 | Research | How much does partner activation lift win rates? | All | https://www.workspan.com/ai-native-partnerships/research/how-much-does-partner-activation-lift-win-rates | 2 |
| 2026-05 | Research | What is the AWS Partner Central MCP server | AWS | https://www.workspan.com/ai-native-partnerships/research/what-is-aws-partner-central-mcp-server | 2 |
| 2026-05 | Research | How to write a JBP with AWS or Microsoft | AWS, MS | https://www.workspan.com/ai-native-partnerships/research/how-to-write-a-joint-business-plan-with-aws-or-microsoft | 2 |
| 2026-05 | Research | How did Boomi grow 30x on AWS Marketplace | AWS | https://www.workspan.com/ai-native-partnerships/research/how-did-boomi-grow-on-aws-marketplace | 2 |
| 2026-05 | Research | Seller Activation Gap | All | https://www.workspan.com/ai-native-partnerships/research/seller-activation-gap | 2 |
| 2026-05 | Research | ClearScale with AWS Partner Central | AWS | https://www.workspan.com/ai-native-partnerships/research/how-clearscale-uses-workspan-with-aws-partner-central | 1 |
| 2026-05 | Research | Who uses WorkSpan and what results | All | https://www.workspan.com/ai-native-partnerships/research/who-uses-workspan-and-what-results | 1 |
| 2026-05-08 | Blog | How Wayne Li Closes Deals 40% Faster (APAC) | None | https://www.workspan.com/blog/how-wayne-li-closes-deals-40-faster-through-partner-trust | 1 |
| 2026-05-08 | Blog | How Chris Saam Turns First Partner Wins into Compounding Revenue | None | https://www.workspan.com/blog/how-chris-saam-turns-first-partner-wins-into-compounding-revenue | 1 |
| 2026-05-04 | Blog | WorkSpan Launches NOW Assist Agent for ServiceNow CRM (MCP) | AWS, All | https://www.workspan.com/blog/workspan-launches-now-assist-agent-servicenow-crm | 2 |
| 2026-04-22 | Web page | WorkSpan for Microsoft Partnerships | MS | https://www.workspan.com/use-case/microsoft-partnership | 2 |
| 2026-04-22 | Web page | WorkSpan for Google Partnerships | Google | https://www.workspan.com/use-case/google-partnership | 2 |
| 2026-04-22 | Web page | The New Channel Economics (CPPO, MPO, MCPO) | All | https://www.workspan.com/use-case/the-new-channel-economics | 1 |
| 2026-04-22 | Web page | Hyperscaler Edition product overview | All | https://www.workspan.com/solutions/hyperscalers/product-overview | 2 |
| 2026-04-21 | Event | WorkSpan at Google Cloud Next '26 | Google | https://www.workspan.com/events-and-webinar/workspan-at-google-cloud-next-26 | 1 |
| 2026-04-16 | Blog | Pre-Pipeline: The Work That Keeps Co-Sell Deals from Dying | MS | https://www.workspan.com/blog/pre-pipeline-the-work-that-keeps-co-sell-deals-from-dying | 2 |
| 2026-04-16 | Blog | Triple Play: The Multi-Partner Advantage | All | https://www.workspan.com/blog/triple-play-the-multi-partner-advantage-in-todays-enterprise-co-sell | 2 |
| 2026-04-16 | Blog | AI for Partnerships: Don't Share Your Data, Share Your Context | All | https://www.workspan.com/blog/ai-for-partnerships-dont-share-your-data-share-your-context | 1 |
| 2026-04-15 | Blog | The New AI Operating Model for Partner Revenue | All | https://www.workspan.com/blog/the-new-ai-operating-model-for-partner-revenue | 1 |
| 2026-04-03 | Blog | How Elite Alliance Leaders from Microsoft and DocuSign Design Joint Value | MS | https://www.workspan.com/blog/how-elite-alliance-leaders-from-microsoft-and-docusign-design-joint-value | 2 |
| 2026-04-02 | Event/video | Partner Signal Live April 2026 (Nina Harding, David Meyer, Bron Hastings) | AWS, MS | https://www.workspan.com/partner-signal-live/april-2026 | 3 |
| 2026-03-16 | Blog | How Kyle Hayes Turns Marketplace Listings into Revenue | All | https://www.workspan.com/blog/how-kyle-hayes-turns-marketplace-listings-into-marketplace-revenue | 3 |
| 2026-03-16 | Blog | Partners in Revenue series (Alex Richards, Amanda Nielsen, Rob Moyer, Antonio Caridad, Barrett King, Dan Taylor and others) | None | https://www.workspan.com/blog | 1 |
| 2026-03-11 | Webinar | Navigating Your AWS Partner Central Migration with Confidence | AWS | https://www.youtube.com/watch?v=Ztg5NIfYxb4 | 3 |
| 2026-01-27 | Blog | The Billion-Dollar Blueprint (AWS, Deloitte, Cisco) | AWS | https://www.workspan.com/blog/the-billion-dollar-blueprint | 2 |
| 2026-01-23 | Blog | The 2026 Co-Stars of Co-Sell Award Winners | All | https://www.workspan.com/blog/the-2026-co-stars-of-co-sell-award-winners | 2 |
| 2026-01-22 | Summit video | Sales Partnership Summit: The Tres Commas Club (Brian Bohan, AWS) | AWS | https://www.youtube.com/watch?v=mBz1KoGGNw0 | 2 |
| 2025-12-22 | Help center | AWS Partner Central 3.0 API Guide (created) | AWS | https://support.workspan.com/hc/en-us/articles/47607948575379 | 3 |
| 2025-12-04 | Help center | Locating Values for Automated Value Mapping (SFDC, HubSpot, Dynamics) | All | https://support.workspan.com/hc/en-us/articles/47083532264211 | 2 |
| 2025-11-30 | Blog | Free AWS Partner Console Migration (Amit Sinha) | AWS | https://www.workspan.com/blog/free-aws-partner-console-migration | 3 |
| 2025-11-17 | Event | Exec Roundtable at Microsoft Ignite | MS | https://www.workspan.com/events-and-webinar/exec-rountable-at-microsoft-ignite | 1 |
| 2025-09-08 | Help center | Salesforce Connected App Usage Restrictions | All | https://support.workspan.com/hc/en-us/articles/44432397224851 | 1 |
| 2025-09-04 | Webinar | Product-Led Growth on AWS Marketplace (with AWS) | AWS | https://www.youtube.com/watch?v=6HiwsHhEUTk | 3 |
| 2025-08-28 | Help center | What is WorkSpan | All | https://support.workspan.com/hc/en-us/articles/44240205455123 | 1 |
| 2025-08-25 | Help center | Google v2 Implementation Guide (existing customers) | Google | https://support.workspan.com/hc/en-us/articles/44153432584979 | 2 |
| 2025-08-05 | Blog | Databricks AI partnerships | All | https://www.workspan.com/blog/databricks-ai-partnerships | 1 |
| 2025-07-28 | Help center | Microsoft Co-sell Updates: Solution Areas and Plays Migration | MS | https://support.workspan.com/hc/en-us/articles/43363210015507 | 2 |
| 2025-07-25 | Blog | Frontline AI: Leading Partnerships Through the AI Shift | None | https://www.workspan.com/blog/frontline-ai-leading-partnerships-through-the-ai-shift | 1 |
| 2025-07-22 | Help center | Pricing Models for AWS Marketplace Listings | AWS | https://support.workspan.com/hc/en-us/articles/43201089364883 | 1 |
| 2025-07-17 | Blog | WorkSpan AI Launches on AWS Agent Marketplace | AWS | https://www.workspan.com/blog/aws-agent-marketplace-launch | 1 |
| 2025-07-10 | Help center | Microsoft Partner Center APIs Implementation Guide (upd 2026-06-18) | MS | https://support.workspan.com/hc/en-us/articles/42871496915347 | 2 |
| 2025-05-20 | Help center | Google v2 Implementation Guide (new customers) | Google | https://support.workspan.com/hc/en-us/articles/41434754775187 | 2 |
| 2025-05-21 | Help center | AWS ACE Integration Messages (56 validations) | AWS | https://support.workspan.com/hc/en-us/articles/30798917226643 | 3 |
| 2025-04-10 | Blog | How WorkSpan AI Drives Successful Google Cloud Partnerships | Google | https://www.workspan.com/blog/how-workspan-ai-drives-successful-google-cloud-partnerships | 2 |
| 2025-02-25 | Webinar | Aligning Cloud Partner Incentives: How Qualtrics Hit USD 100M+ | AWS | https://www.youtube.com/watch?v=8bP75QefR1Y | 3 |
| 2024-09-10 | Help center | Hyperscaler Edition with HubSpot Installation Guide (upd 2025-10-24) | All | https://support.workspan.com/hc/en-us/articles/33247557683347 | 2 |
| 2024-08-12 | Blog | WorkSpan Hyperscaler Edition with HubSpot | All | https://www.workspan.com/blog/workspan-hyperscaler-edition-with-hubspot | 2 |
| 2024-05-03 | Blog | Succeeding at AWS Marketplace Sales with Propensity-to-Buy Scores | AWS | https://www.workspan.com/blog/succeeding-at-aws-marketplace-sales-with-propensity-to-buy-scores | 2 |
| Gated | Ebook / report | Mastering Co-Sell with AWS; Ultimate Guide to Partnering with Cloud Providers; Canalys Co-Sell Leadership Matrix (2023); Cloud Sales Revenue Worksheet | All | https://www.workspan.com/e-book-mastering-co-sell-with-aws-an-essential-playbook-for-partnering-with-aws | not read (form-gated) |

---

## 9. Registry rows (monthly) and discovery queries

| Name | Role | Where to look | Good for | Last new item |
|---|---|---|---|---|
| WorkSpan help center (public API) | Vendor docs | https://support.workspan.com/api/v2/help_center/en-us/articles.json (sort by updated_at; only about 16 public) | Hyperscaler API deadlines and migrations (S3 sunset, PC 3.0, Microsoft API, Google allowlisting) | 2026-09-17 |
| WorkSpan sitemap | Change feed | https://www.workspan.com/sitemap.xml (lastmod is a CMS date, not publish date; research hub /ai-native-partnerships/ is not in it) | New blog, use-case and event pages | 2026-08-24 |
| Amit Sinha | President and co-founder, WorkSpan | https://www.workspan.com/blog (author), Partner Signal Live, LinkedIn | AWS migration, Microsoft co-sell automation, launch announcements | 2026-05-04 |
| Mayank Bawa | CEO and co-founder | Blog, /ai-native-partnerships/research/mayank-bawa | Strategy thesis (low tactical value) | 2026-05 |
| Sam Gong | SVP Marketing / AI GTM | Blog, summits | Report framing, award posts | 2026-05 |
| Richard Gene Felix and Travis Katona | WorkSpan marketplace and advisory team | YouTube webinars; advisory@workspan.com | AWS console migration mechanics, Seller Prime, private-offer ops | 2026-03-11 | <!-- VALIDATE-OK[person-address]: published role mailbox, not a person -->
| Partner Signal Live | Quarterly summit | https://www.workspan.com/partner-signal-live/april-2026 ; YouTube @WorkSpan | Hyperscaler executives on record (Microsoft CVP Nina Harding, April 2026) | 2026-04-02 |
| Sales Partnership Summit / Co-Stars of Co-Sell | Semiannual summit and awards | YouTube @WorkSpan | AWS partner org speakers (Brian Bohan); customer case numbers | 2026-01-22 |
| WorkSpan YouTube | Channel | https://www.youtube.com/@WorkSpan (262 uploads; mostly 1 to 2 minute "Partners in Revenue" clips since March 2026) | Transcripts of webinars and summits | 2026-08 |
| Ecosystem Aces podcast | Podcast | https://podcasts.apple.com/us/podcast/ecosystem-aces/id1376113326 | Back catalogue only | DORMANT since 2025-02-02 |
| Kyle Hayes | CEO, Ecosystem Revenue Dynamics (CREATOR, guest) | WorkSpan blog and YouTube; LinkedIn | Marketplace ops playbooks for ISVs | 2026-03-16 |
| Rob Moyer | Founder, BlueThread (co-author of WorkSpan report) | /ai-native-partnerships/research/rob-moyer ; LinkedIn | Partnership Operator and Co-Sell Engine frameworks, attribution | 2026-05 |

Discovery queries (run monthly, last 45 days):
1. `site:support.workspan.com AWS OR Microsoft OR Google` and the help center API sorted by `updated_at`.
2. `WorkSpan "Partner Central" OR "ACE" OR "S3" 2026` (deadline changes and AWS API releases).
3. YouTube search: `WorkSpan webinar` and `Partner Signal Live` (upload date: month).
4. `"WorkSpan" HubSpot co-sell OR "private offer" HubSpot` (whether HubSpot private offers ship).
5. `WorkSpan "Partner Network Hub" OR "Google Cloud" co-sell 2026` (Google naming fix, private offers GA).

---

## Sources

| Tag | Title | Date | URL |
|---|---|---|---|
| WS1 | Navigate AWS Partner Central Migration to Your AWS Console with Free Support (Amit Sinha) | 2025-11-30 | https://www.workspan.com/blog/free-aws-partner-console-migration |
| WS2 | WorkSpan AWS Partner Central API Migration (help center) | 2026-07-01 | https://support.workspan.com/hc/en-us/articles/53078418454675-WorkSpan-AWS-Partner-Central-API-Migration |
| WS3 | AWS Partner Central 3.0 API Guide (help center) | 2025-12-22, upd 2026-06-18 | https://support.workspan.com/hc/en-us/articles/47607948575379-AWS-Partner-Central-3-0-API-Guide |
| WS4 | AWS ACE Integration Messages (help center) | 2024-06-28, upd 2025-05-21 | https://support.workspan.com/hc/en-us/articles/30798917226643-AWS-ACE-Integration-Messages |
| WS5 | Microsoft Partner Center APIs: Implementation Guide | 2025-07-10, upd 2026-06-18 | https://support.workspan.com/hc/en-us/articles/42871496915347-Microsoft-Partner-Center-APIs-Implementation-Guide |
| WS6 | Microsoft Co-sell Updates: Solution Areas and Plays Migration Guide | 2025-07-28, upd 2026-06-18 | https://support.workspan.com/hc/en-us/articles/43363210015507-Microsoft-Co-sell-Updates-Solution-Areas-and-Plays-Migration-Guide |
| WS7 | Google v2 Implementation Guide for New Customers | 2025-05-20, upd 2025-08-25 | https://support.workspan.com/hc/en-us/articles/41434754775187-Google-v2-Implementation-Guide-for-New-Customers |
| WS8 | Google v2 Implementation Guide for Existing Customers | 2025-08-25 | https://support.workspan.com/hc/en-us/articles/44153432584979-Google-v2-Implementation-Guide-for-Existing-Customers |
| WS9 | WorkSpan Hyperscaler Edition with HubSpot Application Installation Guide | 2024-09-10, upd 2025-10-24 | https://support.workspan.com/hc/en-us/articles/33247557683347 |
| WS10 | Locating Values for Automated Value Mapping (SFDC, HubSpot and Dynamics) | 2025-12-04 | https://support.workspan.com/hc/en-us/articles/47083532264211 |
| WS11 | WorkSpan Salesforce App Package Upgrade Guide | 2025-09-08, upd 2026-09-17 | https://support.workspan.com/hc/en-us/articles/44524164267283 |
| WS12 | WorkSpan Salesforce Connected App Usage Restrictions | 2025-09-04, upd 2026-01-05 | https://support.workspan.com/hc/en-us/articles/44432397224851 |
| WS13 | WorkSpan Salesforce App (WS SFDC App) Installation Guide | 2023-07-21, upd 2026-09-17 | https://support.workspan.com/hc/en-us/articles/18749778537491 |
| WS14 | WorkSpan Support | 2026-08-27 | https://support.workspan.com/hc/en-us/articles/54846043383187-WorkSpan-Support |
| WS15 | Pricing Models for AWS Marketplace Listings | 2025-07-22 | https://support.workspan.com/hc/en-us/articles/43201089364883 |
| WS16 | What is WorkSpan and How Do We Accelerate Co-selling? | 2025-08-28 | https://support.workspan.com/hc/en-us/articles/44240205455123 |
| WS17 | WorkSpan Hyperscaler Edition product overview | lastmod 2026-04-22, fetched 2026-09-26 | https://www.workspan.com/solutions/hyperscalers/product-overview |
| WS18 | Hyperscaler Edition for AWS | lastmod 2026-07-01 | https://www.workspan.com/solutions/hyperscalers/hyperscaler-edition-for-aws |
| WS19 | Hyperscaler Edition for Microsoft | lastmod 2026-04-22 | https://www.workspan.com/solutions/hyperscalers/hyperscaler-edition-for-microsoft |
| WS20 | Hyperscaler Edition for Google | lastmod 2026-04-22 | https://www.workspan.com/solutions/hyperscalers/hyperscaler-edition-for-google |
| WS21 | Marketplace Listing (service, quote calculator) | lastmod 2026-07-01 | https://www.workspan.com/solutions/hyperscalers/marketplace-listing |
| WS22 | WorkSpan Marketplace Accelerator for AWS / for Microsoft | lastmod 2026-04-22 | https://www.workspan.com/solutions/hyperscalers/workspan-marketplace-accelerator-for-aws |
| WS23 | WorkSpan Hyperscaler Edition with HubSpot (blog) | 2024-08-12 | https://www.workspan.com/blog/workspan-hyperscaler-edition-with-hubspot |
| WS24 | WorkSpan for AWS Partnerships (use case) | lastmod 2026-07-01 | https://www.workspan.com/use-case/aws-partnership |
| WS25 | WorkSpan for Microsoft Partnerships (use case) | lastmod 2026-04-22 | https://www.workspan.com/use-case/microsoft-partnership |
| WS26 | WorkSpan for Google Partnerships (use case) | lastmod 2026-04-22 | https://www.workspan.com/use-case/google-partnership |
| WS27 | The New Channel Economics (use case) | lastmod 2026-04-22 | https://www.workspan.com/use-case/the-new-channel-economics |
| WS28 | Integration Platform; Integrations directory | lastmod 2026-04-22 | https://www.workspan.com/platform/integration-platform |
| WS29 | WorkSpan homepage and About (leadership, network size) | 2026-08-24 / 2026-08-13 | https://www.workspan.com/company/about |
| WS30 | WorkSpan AI Launches on AWS Agent Marketplace (Amit Sinha) | 2025-07-17 | https://www.workspan.com/blog/aws-agent-marketplace-launch |
| WS31 | WorkSpan Launches the First NOW Assist Agent for ServiceNow CRM | 2026-05-04 | https://www.workspan.com/blog/workspan-launches-now-assist-agent-servicenow-crm |
| WS32 | The 2026 Co-Stars of Co-Sell Award Winners | 2026-01-23 | https://www.workspan.com/blog/the-2026-co-stars-of-co-sell-award-winners |
| WS33 | How Kyle Hayes Turns Marketplace Listings into Marketplace Revenue | 2026-03-16 | https://www.workspan.com/blog/how-kyle-hayes-turns-marketplace-listings-into-marketplace-revenue |
| WS34 | Pre-Pipeline: The Work That Keeps Co-Sell Deals from Dying | 2026-04-16 | https://www.workspan.com/blog/pre-pipeline-the-work-that-keeps-co-sell-deals-from-dying |
| WS35 | Triple Play: The Multi-Partner Advantage in Today's Enterprise Co-Sell | 2026-04-16 | https://www.workspan.com/blog/triple-play-the-multi-partner-advantage-in-todays-enterprise-co-sell |
| WS36 | How Elite Alliance Leaders from Microsoft and Docusign Design Joint Value (Amit Sinha) | 2026-04-03 | https://www.workspan.com/blog/how-elite-alliance-leaders-from-microsoft-and-docusign-design-joint-value |
| WS37 | The Billion-Dollar Blueprint | 2026-01-27 | https://www.workspan.com/blog/the-billion-dollar-blueprint |
| WS38 | The Partner Manager's Job Has Split in Two | 2026-04-16 | https://www.workspan.com/blog/the-partner-managers-job-has-split-in-two |
| WS39 | The New AI Operating Model for Partner Revenue (Mayank Bawa) | 2026-04-15 | https://www.workspan.com/blog/the-new-ai-operating-model-for-partner-revenue |
| WS40 | AI for Partnerships: Don't Share Your Data, Share Your Context | 2026-04-16 | https://www.workspan.com/blog/ai-for-partnerships-dont-share-your-data-share-your-context |
| WS41 | From One Win to a Revenue Engine: The KGAM Playbook for System Integrators | 2026-08-11 | https://www.workspan.com/blog/from-one-win-to-a-revenue-engine-the-kgam-playbook-for-system-integrators |
| WS42 | WorkSpan's Next Chapter: AI-Powered Partnerships and Series D Funding | 2025-03-24 | https://www.workspan.com/blog/workspan-ai-launch-series-d-funding |
| WS43 | WorkSpan Reports Record Quarter | 2025-05-09 | https://www.workspan.com/blog/workspan-reports-record-quarter-accelerates-growth-with-workspan-ai-launch |
| WS44 | How WorkSpan AI Drives Successful Google Cloud Partnerships (Amit Sinha) | 2025-04-10 | https://www.workspan.com/blog/how-workspan-ai-drives-successful-google-cloud-partnerships |
| WS45 | Succeeding at AWS Marketplace Sales with Propensity-to-Buy Scores | 2024-05-03 | https://www.workspan.com/blog/succeeding-at-aws-marketplace-sales-with-propensity-to-buy-scores |
| WS46 | WorkSpan: Your Partner for Transition to Enhanced AWS Partner Central | 2023-11-22 | https://www.workspan.com/blog/workspan-your-partner-for-transition-to-enhanced-aws-partner-central |
| WS47 | Running AI-Native Partnerships (WorkSpan and BlueThread report) | 2026-05-04 | https://www.workspan.com/ai-native-partnerships/ |
| WS48 | How much does partner activation lift win rates? | 2026-05 | https://www.workspan.com/ai-native-partnerships/research/how-much-does-partner-activation-lift-win-rates |
| WS49 | Seller Activation Gap | 2026-05 | https://www.workspan.com/ai-native-partnerships/research/seller-activation-gap |
| WS50 | How did Boomi grow 30x on AWS Marketplace? | 2026-05 | https://www.workspan.com/ai-native-partnerships/research/how-did-boomi-grow-on-aws-marketplace |
| WS51 | How ClearScale uses WorkSpan with AWS Partner Central | 2026-05 | https://www.workspan.com/ai-native-partnerships/research/how-clearscale-uses-workspan-with-aws-partner-central |
| WS52 | How to write a joint business plan (JBP) with AWS or Microsoft | 2026-05 | https://www.workspan.com/ai-native-partnerships/research/how-to-write-a-joint-business-plan-with-aws-or-microsoft |
| WS53 | What is the AWS Partner Central MCP server | 2026-05 | https://www.workspan.com/ai-native-partnerships/research/what-is-aws-partner-central-mcp-server |
| WS53a | How Kim Tremblay Grew Partner Revenue from 2% to 23% | 2026-07-06 | https://www.workspan.com/blog/how-kim-tremblay-grew-partner-revenue-from-2-to-23 |
| WS54 | Who uses WorkSpan, and what results have they seen? | 2026-05 | https://www.workspan.com/ai-native-partnerships/research/who-uses-workspan-and-what-results |
| WS55 | Navigating Your AWS Partner Central Migration with Confidence (webinar transcript) | 2026-03-11 | https://www.youtube.com/watch?v=Ztg5NIfYxb4 |
| WS56 | Partner Signal Live: Nina Harding (Microsoft) (transcript) | 2026-04-02 | https://www.youtube.com/watch?v=lFOBDw8oadE |
| WS57 | Partner Signal Live: David Meyer (Qualtrics) (transcript) | 2026-04-02 | https://www.youtube.com/watch?v=LhmY5YPMHqg |
| WS58 | Partner Signal Live: Amit Sinha (transcript) | 2026-04-02 | https://www.youtube.com/watch?v=HuA83LHdkZ4 |
| WS59 | Product-Led Growth on AWS Marketplace: What, Why and How (with AWS; transcript) | 2025-09-04 | https://www.youtube.com/watch?v=6HiwsHhEUTk |
| WS60 | Aligning Cloud Partner Incentives: How Qualtrics Hit USD 100M+ in One Year (transcript) | 2025-02-25 | https://www.youtube.com/watch?v=8bP75QefR1Y |
| WS61 | Sales Partnership Summit: The Tres Commas Club (transcript) | 2026-01-22 | https://www.youtube.com/watch?v=mBz1KoGGNw0 |
| WS62 | WorkSpan AWS Advisory Services (AWS Marketplace listing) | fetched 2026-09-26 | https://aws.amazon.com/marketplace/pp/prodview-y2ncie33gmrse |
| WS63 | WorkSpan Software Pricing and Plans (Vendr) | data circa 2025-02, fetched 2026-09-26 | https://www.vendr.com/marketplace/workspan |
| WS64 | WorkSpan Reviews (G2) | fetched 2026-09-26 | https://www.g2.com/products/workspan/reviews |
| WS65 | WorkSpan company profile (CB Insights) | fetched 2026-09-26 | https://www.cbinsights.com/company/workspan |
| WS66 | Ecosystem Aces podcast (Apple Podcasts) | last episode 2025-02-02 | https://podcasts.apple.com/us/podcast/ecosystem-aces/id1376113326 |
| WS67 | WorkSpan YouTube channel uploads | fetched 2026-09-26 | https://www.youtube.com/@WorkSpan |
| WS68 | Introducing AWS Partner Central agents (AWS APN Blog, OFFICIAL; same as A78) | 2026-03-16 | https://aws.amazon.com/blogs/apn/introducing-aws-partner-central-agents/ |
| WS69 | Using an earlier CRM with Amazon S3 integration (AWS docs, OFFICIAL) | fetched 2026-09-26 | https://docs.aws.amazon.com/partner-central/latest/crm/custom-integration-using-amazon-s3.html |
| WS70 | Boomi's Partnership with AWS and WorkSpan (customer story) | fetched 2026-09-26 | https://www.workspan.com/customers/boomi-aws |
| WS71 | Strategy Salon (June 2026) and Exec Roundtable at Microsoft Ignite (2025-11-17) event pages | 2025-11 to 2026-06 | https://www.workspan.com/events-and-webinar/strategy-salon----an-afternoon-for-partner-leaders-at-the-heart-of-data-ai |
| WS72 | Partner Signal Live April 2026 agenda | 2026-04-02 | https://www.workspan.com/partner-signal-live/april-2026 |
| WS73 | WorkSpan sitemap | fetched 2026-09-26 | https://www.workspan.com/sitemap.xml |
