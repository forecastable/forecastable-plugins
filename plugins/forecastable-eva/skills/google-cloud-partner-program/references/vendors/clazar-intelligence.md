# Clazar content intelligence
Built 2026-09-26. VENDOR source: operational detail, labeled; official pages win on conflicts.

Scope: everything Clazar (clazar.io) published or updated since 2025-07-01 across blog, guides, the 2025 State of Cloud Marketplace & Co-Sell report (co-authored with Roman Kirsanov / Partner Insight), help center (help.clazar.io, 161 articles in sitemap), events, podcast and YouTube, plus the Clazar MCP server (2026-08-21). 58 items read in full or in substance, 11 YouTube transcripts pulled. Every Clazar claim is VENDOR unless a row says it was confirmed on an official page. Tags `[CZn]` resolve in Sources; tags `[A..]`, `[M..]`, `[G..]`, `[X..]` point to our existing intelligence files.

Reading rule for Eva: Clazar's help center is the most useful part (portal mechanics, field lists, gotchas). Clazar's long-form guides are the least reliable part: several 2026-dated guides still use retired Microsoft and Google program names (see section 7). Never quote a Clazar program name without checking our cloud file first.

## Ten takeaways that change how Alex or Eva advise

1. **Clazar is the strongest HubSpot option among Cloud GTM vendors, but HubSpot is second-class inside Clazar.** Clazar ships a HubSpot app with a deal card for private offers and co-sell on AWS, Microsoft and Google [CZ4][CZ18], and Supabase runs its AWS ACE pipeline from HubSpot on it [CZ4][CZ77]. But co-sell sync to HubSpot runs "on a daily cycle" while Salesforce syncs "bidirectionally in real time" [CZ4], and the AWS ACE auto-update job runs twice daily [CZ9]. Advice for HubSpot-first Forecastable customers: Clazar is a first-look candidate; set expectations that ACE stage and Quality Score changes land in HubSpot next day, not live.

2. **Some AWS money only flows if you use a participating integrator, and Clazar sells that as "free for the first year."** Clazar pricing is public: QuickStart USD 799/month and Growth USD 1,499/month billed annually, Enterprise custom, no revenue share, each tier marked "Free for First year*" with "up to $10k" or "$20k cloud credits back" [CZ31][CZ33]. The credits are AWS programs: List & Sell (USD 10,000 credits once a new SaaS listing reaches USD 65K TCV or 10+ private offers in 12 months; PLG products USD 5,500 or 10+ active monthly subscriptions) and ACE-CRM Integration Credits (USD 10,000; net-new integration, one private offer accepted from the CRM or one co-sell submission, no double dipping with other credits) [CZ22][CZ79]. AWS confirms List & Sell exists and requires an integrator found in Partner Central but publishes no thresholds or amounts [CZ87][A30]. Business-case rule for Alex: net tool cost in year one can be near zero on AWS, but only if the customer actually transacts USD 65K in year one.

3. **A new, vendor-only AWS incentive: USD 5,000 in credits for 10+ co-sell opportunities updated through the Partner Central MCP Server, fund requests close December 1, 2026** [CZ37]. Not found on AWS's public MCP docs, which mention no credits [CZ88]. Treat as UNVERIFIED; ask the PDM. If real, it pays any partner who routes ACE updates through an agent before December 1.

4. **Partner Revenue Measurement has an ecosystem deadline our AWS file lacks: July 31, 2026, and May 31, 2026 for AI Competency holders.** Clazar calls PRM compliance "required to remain eligible for AWS funding benefits" from July 31, 2026 [CZ39], then in a later article says these are "widely-cited planning dates rather than a formal AWS commitment" [CZ40]; an independent vendor says the same and ties the risk to co-sell visibility and MDF [CZ89]. Tag rules worth adding to Eva's runbook: one `aws-apn-id` tag per resource (only one partner can claim it), customer consent before tagging in customer accounts, tag running resources not the listing ARN or AMI, a free listing is enough to get a product code, and no Marketplace transaction is required for attribution [CZ39].

5. **All three clouds now charge 1.5% on migrating an existing direct customer onto the marketplace at renewal, and AWS confirms it.** Clazar says the AWS renewal rate applies when the private offer renews a Marketplace agreement "or extend[s] a previous off-Marketplace contract" if you link the preceding agreement in AMMP [CZ1]; the AWS fee page confirms renewals can come "from a previous agreement outside of AWS Marketplace" [CZ84]. Microsoft needs the renewal self-attested at creation [M42][CZ2]; Google needs deal type set to Migration or Channel shift [G18][CZ3]. Clazar's fee math also shows that on AWS, three one-year USD 500K offers (3% then 1.5% renewals) cost the same USD 30,000 as one USD 1.5M three-year offer at 2% [CZ1]. Alex's rule: the cheapest first marketplace deal is a renewal of an existing direct customer, correctly flagged.

6. **ISV Accelerate is invitation-based after you hit the numbers, and Clazar documents operating SLAs the official page does not publish.** AWS's page confirms the ISVA team "will send you an invitation" once requirements are met [CZ85]. Clazar adds: accept or reject AWS-sourced opportunities within 72 hours (3 business days), update every active ACE opportunity every 14 days (stage, next steps, close date, MRR, blockers), more than 30 days without updates triggers a program review [CZ36]. Our official source says 5 business days for referral acceptance [A43] (conflict, official wins); use the 14-day update cadence as Eva's default anyway.

7. **Clazar's survey is the most cited ISV marketplace benchmark, and it is thin.** 100+ SaaS companies [CZ30], co-authored with Partner Insight [CZ29]. Headline: 89% transact on a marketplace, 22% get over 20% of revenue there, 41% get under 5% [CZ28]. The "22% Club" reports 75% higher win rates versus 47% for others, 94% versus 77% consistent field engagement, and 63% automated submissions, more than double the rest [CZ28]. Clazar's own pages disagree on two headline numbers (structured cadences 32% versus 40%; higher co-sell win rates 54%, 58% or 59%) [CZ28][CZ29][CZ17]. Use for direction, never as a forecast.

8. **Clazar's 2026 content is stale on Microsoft and Google program names; Eva must not echo it.** The Google marketplace guide updated 2026-09-22 still says to enroll in "Partner Advantage" [CZ24]; the Azure guides updated August 2026 still describe ISV Success, "App Accelerate coming in 2026", "Partner Sales Connect" and Marketplace Rewards rebates [CZ6][CZ20]; a June 2026 help article still sells PRACR as a co-sell benefit [CZ58b]. Our files say Google Partner Network replaced Partner Advantage [G1], Frontier Accelerate for Marketplace replaced ISV Success and Marketplace Rewards in September 2026 [M30], and PRACR stopped being a broad co-sell mechanism on July 1, 2026 [M13].

9. **Microsoft deal registration is now automatable from the CRM, with the official gates enforced before the form opens.** Clazar's Register Deal action checks: marked Won, co-sell or partner-led, Microsoft accepted or won, Azure IP co-sell eligible solution, at least USD 25,000, Microsoft-managed customer; signed date within 60 days, start date within 90 days; one registration per deal, no edits after filing [CZ56], matching Microsoft's rules [M6]. Clazar also exposes a per-country "Microsoft Managed" account flag to target field-covered accounts [CZ11][CZ47]. Eva: register every won IP co-sell deal inside 60 days; a missed or wrong registration cannot be fixed later.

10. **Google co-sell API access and Clazar's MCP server are the two agent-era plumbing items to know.** Clazar's GCP co-sell setup requires a Google Cloud support case to enable "Deal Registration API" access (V2, 18-character Partner Advantage account ID) plus the Integrator role for a service account in Partner Hub [CZ62]; Tackle's May 2026 guide shows only the Integrator role step [CZ90] (vendor conflict; our Google file says no public co-sell API is documented [G72]). Clazar's MCP server (https://mcp.clazar.io, OAuth 2.1 with PKCE) lets Claude, ChatGPT, Cursor or Windsurf read offers, contracts, co-sell pipeline, metering and disbursements across AWS, Microsoft, Google and Snowflake, and create or update AWS co-sell opportunities only after user confirmation [CZ5][CZ67]. For a Forecastable customer on Clazar, Eva can read marketplace state through that server instead of asking for exports.

## 1. Vendor profile (products, clouds, CRM and API coverage, pricing, ownership, strengths, bias)

All rows VENDOR unless stated.

| Dimension | What Clazar says (VENDOR) | Source |
|---|---|---|
| Company | "Cloud sales acceleration platform"; founded 2023 by Trunal Bhanse (CEO; ex head of engineering for marketplaces at Confluent, Airbnb 2013 to 2018, LinkedIn) and Aayush Bahuguna (CTO; ex Airbnb, Zenefits). Advisors include Neha Narkhede (Confluent co-founder) and Lenny Rachitsky | [CZ32][CZ80] |
| Funding and ownership | Seed May 2023 (Twin Ventures, The General Partnership); USD 10M Series A April 2024 led by Ridge Ventures and Ensemble VC with DST's Saurabh Gupta. Independent and private; no newer round found on 2026-09-26 (unlike Tackle, which AppDirect agreed to acquire [X56]) | [CZ35] |
| Scale claims | "250+ market leaders" (site), "300+ customers" (November 2025 and June 2026), "USD 2 billion plus of transactions" supported (about November 2025), relationships with "at least 1,000" AWS account managers; Clazar says AWS referrals are 45% to 50% of its own opportunities | [CZ33][CZ79][CZ80] |
| Clouds | AWS, Microsoft, Google Cloud; Snowflake Marketplace listings read-only (July 2025) | [CZ16][CZ5] |
| Marketplace products | Listings (SaaS, AMI, container, AI agents and tools API listings on AWS, GCP VM from December 2025), private offers, AWS ABOs, reseller offers (AWS CPPO, Microsoft MPO, Google MCPO), express private offer tracking, contracts, metering (incl. AWS concurrent agreements by agreement ID), Buyer 360, disbursement and future-billings analytics, fee visibility | [CZ7][CZ9][CZ12][CZ42][CZ45] |
| Co-sell products | Auto-create and auto-update of co-sell opportunities from CRM triggers or SOQL filters on AWS, Microsoft and Google; inbound referral routing (Microsoft inbound from December 2025); Microsoft deal registration (about August 2026); partner contacts directory; co-sell dashboards | [CZ13][CZ7][CZ56][CZ18] |
| AWS intelligence surfaced | Opportunity Quality Score, trend, recommendation and co-sell motion in Salesforce package v1.67+; AWS Solution Score, category and Eligible Programs per company from Lead Prospecting, run through Clazar's own Partner Central account | [CZ46][CZ47] |
| Funding workflow | December 2025: create AWS MDF requests in Clazar; about August 2026 help: funding requests across all programs shown read-only, creation happens in Partner Central (Clazar's own docs changed) | [CZ7][CZ41] |
| CRM coverage | Salesforce managed package (widgets, custom objects, multi-account, real-time sync); HubSpot app (deal card, daily co-sell sync); Microsoft Dynamics for co-sell | [CZ4][CZ11][CZ13] |
| Co-sell API coverage | AWS: Partner Central Selling API, "official launch partner", S3 path retired; AWS Partner Central 3.0 launch partner and free migration service. Microsoft: Partner Center Referrals API (Referrals admin role). Google: Partner Network Hub Integrator role plus Deal Registration API V2 | [CZ10][CZ58][CZ62] |
| Agentic and MCP | Clazar MCP server (2026-08-21, OAuth 2.1 PKCE, read across clouds, AWS co-sell writes with confirmation); Clazar AI assistant; routes updates through AWS Partner Central MCP server; P2B (propensity to buy) score from AWS and Azure signals; AI dashboard query generator | [CZ5][CZ37][CZ16][CZ12] |
| Data and integrations | API and webhooks (Svix), Airbyte and Fivetran (40+ destinations), Workato, Orb and Metronome metering, Slack, SSO, SCIM | [CZ12][CZ34b] |
| Pricing (public) | QuickStart USD 799/month (1 marketplace, 10 private offers per year); Growth USD 1,499/month (1 marketplace, 50 private offers, 50 reseller offers, 1 co-sell integration, 200 co-sell opportunities per year, CRM with 3 seats); Enterprise custom (all clouds, unlimited, API, automation, 24x7). Add-ons on Growth: extra marketplace or co-sell integration USD 6,000, listing USD 3,000. Support response 72 h, 12 h, 4 h by tier. "Clazar does not do rev-share" | [CZ31][CZ33] | <!-- VALIDATE-OK[economics]: public hyperscaler or vendor reseller economics, not Forecastable's -->
| Named customers (their customers, not Forecastable's) | Supabase, Vectra AI, Verint, Sisense (former), Honeycomb, Rootly, Atlan, Facets, Momento, Pinecone, Perplexity, Groundcover, UserTesting, VulnCheck, Confluent, Couchbase | [CZ34][CZ4][CZ79][CZ30] |
| Claimed outcomes | Supabase 350% YoY AWS co-sell growth and 80% less marketplace ops effort; Vectra AWS Marketplace 2.5x and Azure 6x YoY, ACE registrations "in the thousands"; Sisense AWS revenue share tripled; Honeycomb doubled submissions in 11 days | [CZ34][CZ78][CZ28][CZ15] |
| Content cadence | Blog: 6 posts in 2026 (fee explainers, CRM, MCP, Azure co-sell); monthly release notes stopped after December 2025; podcast last episode 2025-03-25; YouTube channel mostly re-uploads, last new video about February 2026; help center is the active surface (articles updated days ago) | [CZ94][CZ76] |

**Strengths (for Alex's tooling call):** public flat pricing with no revenue share (a Vectra executive says it switched from a competitor whose pricing "shifted to a percentage of aggregate marketplace volume" [CZ78]); real HubSpot support; AWS launch-partner depth (Partner Central 3.0, Selling API, MCP); deal-level Microsoft registration; detailed, current help center; MCP server for agent access.

**Weaknesses:** long-form guides lag Microsoft and Google program changes by months; Google co-sell is the least mature piece (auto-create arrived August 2025, HubSpot June 2025); HubSpot sync is daily; content output fell sharply after mid-2025; survey sample small.

**Bias to watch:** ranks itself "#1" against Tackle, Suger and Labra in its own guides [CZ19][CZ21][CZ22]; frames AWS incentives that require a participating integrator as making the tool "free" [CZ79]; attributes "40 to 60% faster sales cycles" and "25 to 40% larger deals" to "AWS reports" without a citation [CZ36]; quotes a customer saying legacy vendors cost "$50K per marketplace" [CZ8]; DIY cost figures (400 to 700 hours, USD 35K to 82K, 13 to 24 weeks, 20% rejection rate) are unsourced and self-serving [CZ15].

## 2. AWS: extracted substance

| Fact | Status | Our tag | Vendor tag | Date |
|---|---|---|---|---|
| No fee to list; fee only on settled transactions, deducted before disbursement, on pre-tax TCV | CONFIRMS | A24 | CZ1 | 2026-08-11 |
| Public SaaS 3%, server 20%, Data Exchange 3%; private offers 3% under USD 1M, 2% USD 1M to under 10M, 1.5% at 10M+; all renewals 1.5% | CONFIRMS | A24 | CZ1 | 2026-08-11 |
| 1.5% renewal also applies when the private offer extends an off-Marketplace contract; link the preceding agreement in AMMP at creation | NEW (official page confirms the off-Marketplace source; the "link in AMMP" step is VENDOR) | A24 | CZ1, CZ84 | 2026-08-11 |
| Multi-year: three one-year USD 500K offers (USD 30,000 total) cost the same as one USD 1.5M three-year offer at 2%; banding up only beats a series of new offers | NEW (arithmetic on official rates) | A24, A26 | CZ1 | 2026-08-11 |
| CPPO adds 0.5% charged on the ISV-to-partner (discounted) price; worked example USD 640K partner price: USD 19,200 + 3,200 = 22,400 | CONFIRMS | A24, A53 | CZ1 | 2026-08-11 |
| Professional services 0.5% | CONFIRMS, but STALE by omission: no mention of 0% in qualifying multi-product sets from 2026-09-01 | A28, A29 | CZ1 | 2026-08-11 |
| South Korea buyers +1% from 2025-04-01 (SaaS PO under USD 1M = 4%) | CONFIRMS | A24 | CZ1 | 2026-08-11 |
| AWS guide FAQ: marketplace fee "typically 3 to 5 percent" | CONFLICT (wrong: range is 1.5% to 20% plus add-ons) | A24 | CZ22 | 2026-08-21 |
| Seller registration timeline: account setup 1 to 3 days, tax interview 2 to 10 business days, bank verification 2 to 5 business days, KYC 5 to 15 business days | NEW | A51 | CZ8 | 2026-01-01 |
| Use a dedicated seller-of-record AWS account, role-based monitored email, tax location must match Billing console | CONFIRMS (and note: after Partner Central migration the linked account is permanent, so choose it once) | A51, A8 | CZ8 | 2026-01-01 |
| Listing review: 3 to 10 business days SaaS, 5 to 14 business days AMI and container; most SaaS listings 3 to 6 weeks end to end | NEW (VENDOR; AWS states 7 to 10 business days per our file) | A44 | CZ22 | 2026-08-21 |
| AWS Marketplace discontinued Quick Launch for Helm chart deployments on EKS on 2026-03-01; existing deployments keep running | NEW (not verified on AWS pages) | none | CZ22 | 2026-08-21 |
| List & Sell: USD 10,000 promotional credits via participating integrators; eligibility USD 65K TCV or 10+ private offers in 12 months (contract products), USD 5,500 or 10+ active monthly subscriptions (PLG) | CONFIRMS existence and USD 10K (VENDOR A25); thresholds NEW, UNVERIFIED (AWS page publishes none) | A30, A25 | CZ22, CZ79, CZ87 | 2026-08-21 |
| ACE-CRM Integration Credits: USD 10,000; net-new integration to Marketplace or co-sell portal; one private offer accepted from CRM or one co-sell submission; no double dipping | CONFIRMS amount (VENDOR A25); conditions NEW, UNVERIFIED | A25 | CZ22 | 2026-08-21 |
| Seller Prime: up to USD 40,000 reimbursable marketing funds; start with a strategy document | CONFIRMS (VENDOR, still unverified on AWS pages) | A86 | CZ22 | 2026-08-21 |
| USD 5,000 AWS credits once 10+ co-sell opportunities are updated via the Partner Central MCP Server; fund requests close 2026-12-01 | NEW, UNVERIFIED (not on AWS MCP docs) | A48 | CZ37 | about 2026-08 |
| Partner Central MCP server requires SigV4 on every request, so it cannot connect directly to Claude | CONFLICT (AWS What's New 2026-08-20 added OAuth with AWS Sign-In; AWS dev guide still describes SigV4) | A100, A48 | CZ37, CZ88 | about 2026-08 |
| Partner Central 3.0 migration: irreversible; old portal inaccessible during migration; 15 minutes minimum, "30 to 40 minutes" typical, several hours maximum | CONFLICT on duration (our file: 2 to 6 hours) | A8 | CZ38 | about 2026-08 |
| IAM replaces the legacy 20-user ACE cap; map APN roles to managed policies (ACE Manager to AWSPartnerCentralOpportunityManagement); Skill Builder switches to Builder ID login on migration or 2026-01-29; S3 CRM integration and Tasks removed | NEW (20-user cap, Skill Builder date); CONFIRMS policies and S3 removal | A47, A112 | CZ38 | about 2026-08 |
| Account linking required to confirm and renew APN membership from November 2025 | CONFIRMS | A112 | CZ38, CZ10 | 2025-12-01 |
| "Incentive-related" migration deadline June 30, 2026 | CONFLICT (AWS publishes no cutoff; our file already records the vendor claim) | A8, A9, A102 | CZ10 | 2025-12-01 |
| PRM tag `aws-apn-id` = `pc:<product-code>` on running resources in partner and customer accounts | CONFIRMS | A12, A13 | CZ39 | 2026-04-10 |
| PRM: one partner tag per resource; customer consent required in customer accounts; attribution continues until tag removed or resource terminated; free listing suffices (not bound by paid-seller country rules); no Marketplace transaction needed; AWS shares only aggregated data monthly above customer thresholds | NEW | A12 to A14 | CZ39 | 2026-04-10 |
| PRM compliance "required to remain eligible for AWS funding benefits" from 2026-07-31; AI Competency holders earlier (2026-05-31 per independent source) | NEW, UNVERIFIED (Clazar later calls it a planning date, not formal policy) | A6 | CZ39, CZ40, CZ89 | 2026-04 to 2026-06 |
| ISVA requirements (GA listing, ACE eligible, Validated or Differentiated, Payee Central, 5 launched and 15 qualified not-FVO in 12 months, 1 person trained, USD 2,000 AWS revenue) | CONFIRMS | A1 | CZ36 | about 2026-08 |
| ISVA is invitation-only after meeting requirements | CONFIRMS (official: ISVA team "will send you an invitation") | A1 | CZ36, CZ85 | about 2026-08 |
| Accept or reject AWS-sourced opportunities within 72 hours (3 business days); after 5 days inactive they leave the dashboard | CONFLICT (official: 5 business days) | A43 | CZ36 | about 2026-08 |
| Update active ACE opportunities every 14 days; over 30 days without updates triggers ISVA program review; possible suspension | NEW, UNVERIFIED | none | CZ36 | about 2026-08 |
| AWS seller incentives for ISVA: ACE opportunity credits, enhanced rates for ISVA partners, SCB as primary quota retirement, Marketplace transaction bonuses with multi-year multipliers | NEW, UNVERIFIED (our file: SCB percentages not published) | A79, A84 | CZ36 | about 2026-08 |
| Legacy ISVA requirements (2 public references, business plan, field-ready kit, NDA) and "reduced listing fees" benefit | STALE (help article last updated about 2025) | A1 | CZ55 | about 2025 |
| Payee Central: request by Partner Central support case; invitation within 2 business days from amazon-payee-central@amazon.com; after a cash claim is approved AWS issues a PO; invoice against it in Payee Central; paid Net 30 | NEW | A46 | CZ53 | about 2026-08 | <!-- VALIDATE-OK[person-address]: published role mailbox, not a person -->
| Funding programs visible to partners: MDF, Partner Initiative Funding, POC, MAP, Innovation Sandbox, ISV Workload Migration; types Cash, Credit, Discount, Access, Recognition, Resource, Combo; Partner Central's list view does not show amounts; returned requests show as Draft | NEW (detail); CONFIRMS stages | A46 | CZ41 | about 2026-08 |
| ACE field "Project Description" is labeled "Customer Business Problem" in Partner Central; API name still `project_description` | NEW | A43 | CZ44 | about 2026-08-31 |
| ACE required and conditional fields: Partner Specific Needs mandatory when Co-Sell with AWS selected; Marketing Fund Used mandatory when Marketing Originated = Yes; Industry Other text required if Industry = Other; Partner CRM Unique Identifier required; opportunity owner must be a Partner Central user (defaults to Alliance Lead); SaaS contract start, end, customer software value and procurement type fields for SCB-eligible sellers | NEW (field-level) | A43 | CZ48 | about 2026-04 |
| OQS 0 to 100, trend, recommendation, motion (Partner-led, AWS Field-engaged, Agent-engaged) | CONFIRMS | A3 | CZ46 | about 2026-08 |
| AWS Solution Score comes from Lead Prospecting, reflects the account's need, not your positioning; cannot be improved by messaging; separate from OQS | NEW | A97 | CZ46 | about 2026-08 |
| Manual ACE entry takes 10 to 15 minutes (Vectra) or 20 to 30 minutes (Clazar demo) per opportunity | NEW (practitioner estimates) | none | CZ78, CZ79 | about 2025-11 |
| Express private offers: rate cards in Partner Central; supported only for SaaS Contract and SaaS Contract with Consumption listings | CONFIRMS and adds product-type limit | A54 | CZ42 | about 2026-08-31 |
| Private and reseller offers: up to 12 years (144 months, 4,380 days) for SaaS, AMI, container and professional services; payment schedules up to 86 installments; previously 5 years SaaS and PS, 3 years AMI and container | CONFIRMS 144 months; NEW 86 installments and prior limits | A57 | CZ43 | about 2026-09-16 |
| Concurrent agreements: meter each active agreement by agreement ID (`agmt-...`) | CONFIRMS concurrent agreements; NEW metering mechanic | A101 | CZ45 | about 2026-09-25 |
| Published private offers cannot be edited; withdraw (before acceptance only) and recreate; after acceptance use an ABO; price-only ABO keeps contract value USD 0 to avoid double billing; offers cannot move between listings | NEW | A52 | CZ52 | about 2025-10 |
| Metering: whole units only, no proration, cannot backdate; new dimensions can be added (review 24 to 48 h) but existing ones cannot change; existing private offers need an ABO to use a new dimension | NEW (dimension immutability CONFIRMS A57) | A57 | CZ51 | about 2026-08 |
| Self-serve cancellation in Agreements: reason required; buyer confirmation link; auto-cancels if not approved within 7 days; cancellation does not refund; billing adjustment refunds an invoice while keeping the agreement; refunds show in buyer billing in 24 to 48 h, bank up to 5 business days | NEW | none | CZ49, CZ50 | about 2026-06 |
| AWS pauses disbursements for invalid bank details and emits no "resumed" signal | NEW | A56 | CZ2x (help disbursement events) | about 2026-09 |
| Private offer generation in AWS takes about 45 minutes after submission | NEW (VENDOR) | A52 | CZ52b | about 2025 |
| Linking the AWS listing to Partner Central is "now mandatory" for co-sell setup | CONFIRMS (solution or product association required) | A43, A95 | CZ62b | about 2026-06 |
| From 2025-05-01 SaaS hosted anywhere can list; only "Deployed on AWS" (application and control planes on AWS, AWS-only migration or replication targets) counts toward PPA commitments; submit architecture diagram in AMMP | CONFIRMS | A38, A60 | CZ54, CZ68 | 2025-02-28 |
| ACE engagement shows who the AWS AM is and a customer "engagement score" (commit signal) | CONFIRMS (customer contacts and AWS contacts visible) | A43 | CZ79 | about 2025-11 |
| AWS Marketplace Distribution Seller program lets ISVs keep distributors in Marketplace deals; CPPO supported worldwide | CONFIRMS | A53 | CZ78 | about 2025-11 |
| AWS "10,000 plus account managers"; ISVA gives access to "more than 10,000 account managers, solution architects, and specialists" | NEW (VENDOR sizing) | none | CZ79, CZ36 | 2025 to 2026 |

## 3. Microsoft: extracted substance

| Fact | Status | Our tag | Vendor tag | Date |
|---|---|---|---|---|
| Standard 3% on transactable offers including private offers (on negotiated price), Dynamics 365 and Power BI apps, transacted professional services; zero on Contact Me, free, BYOL | CONFIRMS | M34 | CZ2 | 2026-09-11 |
| MPO fee 3% on the ISV wholesale price, not the customer price; worked example USD 75K wholesale, USD 2,250 fee | CONFIRMS | M39 | CZ2 | 2026-09-11 |
| Renewal discount to 1.5% for the whole term; self-attest "Customer Renewal" at creation; covers renewals, off-Marketplace migrations and upsells classified as renewal; offers created after 2024-10-01; cannot be added later; worth USD 7,500 on a USD 500K three-year deal | CONFIRMS (USD figure is arithmetic) | M42 | CZ2, CZ16 | 2026-09-11 |
| Co-sell ready and Azure IP co-sell eligible requirements (USD 100K TTM ACR or MBS at org level, credits and ACO excluded, technical validation, RAD not required for Azure App, Container, VM, transactable since 2023-07-11, solution type IP) | CONFIRMS | M1 | CZ6, CZ20 | 2026-08-28 |
| Contact Me (non-transactable) offers can still reach co-sell ready | CONFIRMS | M4 | CZ6 | 2026-08-28 |
| Revenue threshold monitored at publisher level since July 2024, so multiple listings pool | NEW (consistent with "organization level" in M1) | M1 | CZ20 | 2026-08-04 |
| Marketplace Intent mandatory for API co-sell referrals from January 2026; Estimated ACR field GA; QRP retired Q3 FY26 | CONFIRMS | M21, M19, M18 | CZ6 | 2026-08-28 |
| "App Accelerate" coming in 2026 with a nomination-based early co-sell route (MACC traction, pipeline, readiness) | STALE name (became Frontier Accelerate for Marketplace, GA September 2026); early route CONFIRMS emerging criteria | M30, M27 | CZ6, CZ20 | 2026-08 |
| ISV Success "free for 12 months with a USD 1,500 per year renewal" | STALE (FAM Premium USD 1,500 list replaced ISV Success) | M22, M30 | CZ6 | 2026-08-28 |
| Marketplace Rewards: USD 20,000 rebate at USD 100K eligible ACR in a fiscal year, extra USD 50,000 at USD 4M; activate by assigning a marketing contact | CONFLICT and STALE (not in our official sources; Marketplace Rewards now inside FAM) | M44, M29 | CZ20 | 2026-08-04 |
| "Partner Sales Connect" is Microsoft's co-sell referral system | STALE (Partner Center Referrals) | M10 | CZ20 | 2026-08-04 |
| Co-sell benefits include eligibility for partner-reported ACR (PRACR); Business Applications co-sell needs ISV Connect | STALE (PRACR no longer a broad co-sell mechanism from 2026-07-01; ISV Success, now FAM) | M13, M4 | CZ58b | about 2026-06 |
| MACC timing: target accounts in Microsoft fiscal Q4 (April to June) when customers push to burn commit; most large MACC deals close via private offers | NEW (tactic) | M89 | CZ20 | 2026-08-04 |
| MACC "Enrolled" state needed per offer; primarily platformed on Azure | CONFIRMS | M43 | CZ20 | 2026-08-04 |
| "Close to USD 900 billion in enterprise cloud commitments" across hyperscalers | CONFLICT (definition: Partner Insight sums RPO/backlog including OpenAI-related Azure RPO; our Omdia figure is about USD 470B committed spend) | X40, X49 | CZ20, CZ83 | 2026-02-13 |
| Deal registration gates and form: Won, co-sell or partner-led, Microsoft accepted or won, IP co-sell eligible solution, USD 25K, Microsoft-managed; signed within 60 days, start within 90 days; solution value not above contract value; ACV below USD 25K warning; one registration, no edits; statuses Approved, Action Required, Review or Validation Required, Passed, Failed | CONFIRMS | M6 | CZ56 | about 2026-08 |
| Azure co-sell field list: required Location, Company Name, Microsoft Account ID, Opportunity Name, Type (Partner-led or Co-sell), Assistance Type (six options), Solution, Estimated Value, Close Date, Buyer Purchase Intent, Solution Area, Solution Play, Notes to Microsoft (mandatory for co-sell), buyer and team contacts; stage to MCEM mapping 10/20/40/60/80/100 | CONFIRMS | M7 | CZ57 | about 2026-08 |
| Integration roles: Referrals admin (authorizes Referral APIs) and Co-sell solutions admin; solution ID from Partner Center URL | CONFIRMS | M11 | CZ58 | about 2026-08 |
| Per-country "Microsoft Managed" status and Azure score by account country | NEW (tooling; underlying rule CONFIRMS M6 managed-account gate) | M6 | CZ11, CZ47 | 2025-11 to 2026-08 |
| Microsoft now requires "supplemental content" on SaaS listings with a hosting classification: fully, partially or not hosted in Azure | CONFLICT (official page 2026-06-01 lists five approved hosting categories and requires Azure subscription IDs) | M1 | CZ60, CZ86 | about 2026-05 |
| Account verification: legal name and address must match registration docs, no P.O. boxes; up to three appeals; editing legal info triggers re-vetting per program | NEW | M62 | CZ59 | about 2026-03 |
| Tax and payout: Incentives Admin or Owner role; every seller files a US form (W-9, W-8BEN-E, W-8BEN); 30% default withholding reducible by treaty; tax validation up to 48 h; payout profile only after tax approved; payout validation up to 48 h; bank must be in account country; bank change can delay one payment cycle | NEW (our file: W-9/W-8 only) | M45 | CZ59 | about 2026-03 |
| SaaS private offer purchase: accept does not start billing; buyer must subscribe then "Configure Account Now"; buyer needs Owner or Contributor on the subscription | CONFIRMS | M39 | CZ61 | about 2025 |
| MPO: partner sees offer within 15 minutes; ISV can withdraw only in "Pending partner action"; if the partner acted, partner withdraws first then ISV ("double withdrawal"); upgrades cannot overlap existing dates; SaaS stuck in PendingFulfillmentStart is auto-cancelled after 30 days, forcing a new MPO | NEW (gotchas) | M38, M39 | CZ69 | 2025-02-05, page updated 2026-02-23 |
| MPO channel partners need US or UK tax profile; AppSource products not eligible for private offers; "over 1 million" monthly visitors | STALE (37 customer countries, unified marketplace, 6M+ visitors) | M38, M73 | CZ69 | 2025-02-05 |
| Azure guide describes MPO as buying Azure via CSP or Open Licensing | CONFLICT (MPO excludes CSP-billed customers) | M93 | CZ23 | 2026-08-04 |
| Clazar reports Microsoft inbound referral response target under 4 hours | CONFIRMS (already cited in our file as VENDOR) | M102 | CZ20 | 2026-08-04 |
| Microsoft Marketplace unified 2025-09-25, AI apps and agents category, 6M+ monthly visitors | CONFIRMS | M73 | CZ20 | 2026-08-04 |

## 4. Google Cloud: extracted substance

| Fact | Status | Our tag | Vendor tag | Date |
|---|---|---|---|---|
| Variable revenue share since April 2025: 3% standard and new POs under USD 1M, 2% USD 1M to under 10M, 1.5% at 10M+ and for renewals, migrations, channel shifts; BYOL 0% | CONFIRMS | G18 | CZ3 | 2026-08-28 |
| "All renewals, any TCV, 1.5%" | CONFLICT by omission (native renewal needs prior term of at least 9 months, restart within 90 days, or amendment raising duration and TCV 60%+) | G18 | CZ3 | 2026-08-28 |
| Usage-only offers have TCV zero and pay 3%; use CUD to reach lower bands | CONFIRMS | G20 | CZ3 | 2026-08-28 |
| MCPO: no separate surcharge; fee on the ISV-to-reseller price (USD 80K example, USD 2,400) | CONFIRMS | G34, G67 | CZ3 | 2026-08-28 |
| Fee FAQ: USD 1M offer at 10% discount (USD 900K paid) billed at 2% | CONFLICT (internal error: USD 900K TCV sits in the 3% band) | G18 | CZ3 | 2026-09-05 |
| Fee FAQ: marketplace purchases "draw down Committed Use Discounts" | CONFLICT (confuses CUD pricing with the customer's Google Cloud commitment; drawdown is 100% to a 25% cap) | G22, G23 | CZ3 | 2026-09-05 |
| Payouts typically on the 21st; net of fee | CONFIRMS | G24 | CZ3 | 2026-08-28 |
| Commit drawdown for qualifying purchases 100% capped at 25% of commitment (effective June 2025, citing ChannelE2E); MCPO purchases count from June 2025 | CONFIRMS | G22, G23 | CZ21, CZ25 | 2026-04 to 2026-08 |
| Register in "Partner Advantage portal"; tiers "Member, Partner, Premier plus Diamond"; enroll in "Build" track | STALE (Partner Network, Select, Premier, Diamond; paths co-selling, services, technology) | G1, G70 | CZ21, CZ24 | 2026-08-04 and 2026-09-22 |
| MCCP up to 3% credits on first eligible purchase; GA May 2025; ISVs "must register opportunities in Partner Advantage" | CONFIRMS credit; STALE portal name; registration actually via ISV Solution Connect | G45, G46 | CZ21 | 2026-08-04 |
| Futurum: 112% larger deals on GCP Marketplace (June 2025) | CONFIRMS | G49 | CZ21 | 2026-08-04 |
| Co-sell setup: sign current Marketplace Vendor Agreement; open a Google Cloud support case (Issue type Google Cloud Marketplace, Category "Deal Registration API Error") to enable Deal Registration API V2 access with the 18-character Partner Advantage account ID and Partner Hub ID; then give a service account the Integrator role in Partner Hub > Users and enter Partner ID | NEW (VENDOR); CONFLICT with Tackle (May 2026: Integrator role only, no support case) | G72, G73 | CZ62, CZ90 | about 2026-06 |
| Private offers need the customer's direct billing account, not a reseller billing account (error otherwise); cannot change after submission; customer accepts under Billing > Private Offers | NEW (consistent with G36 reseller subaccounts) | G27, G30 | CZ66, CZ66b | about 2025-10 |
| Free trials self-serve in Producer Portal since 2025-08-15 (no intake form); set trial days and USD credit amount; must republish listing for changes | NEW | G26 | CZ63 | about 2025 |
| Making a listing live: after Publish, Google support provides gcloud commands (servicemanagement.serviceConsumer binding) that an Owner or Editor with Service Management Administrator runs in Cloud Shell | NEW | G26 | CZ65 | about 2025 |
| AI agent listings: SaaS flow in Producer Portal, A2A protocol, Gemini or Vertex-hosted models, agent-specific validation form, MVA 3.0+, approval and ingestion up to 2 days, customer registers the agent manually with a curl command | NEW detail; STALE naming (AgentSpace is now Gemini Enterprise; "Partner Advantage Build Track") | G8, G39, G61 | CZ64 | about 2025 |
| GCP does not support invoice-level reporting; disbursements reported monthly | NEW (VENDOR) | G26 | CZ9, CZ2x | 2025-12 to 2026-09 |
| Google Cloud closed more billion-dollar deals in the first three quarters of 2025 than in 2023 and 2024 combined | NEW (Google earnings remark, VENDOR relay) | G8 | CZ21 | 2026-08-04 |
| Cloud Next '26 USD 750M partner fund for agentic AI | CONFIRMS | G6 | CZ24 | 2026-09-22 |

## 5. Cross-cloud playbooks and benchmarks worth reusing

1. **Price the first marketplace deal as a migration, not a new logo.** Move an existing direct customer onto the marketplace at renewal and flag it: AWS link the prior agreement (1.5%), Microsoft tick Customer Renewal (1.5%), Google set Migration or Channel shift (1.5%) [CZ1][CZ2][CZ3][A24][M42][G18].
2. **Model multi-year packaging both ways on AWS.** Annual offers with renewals and one multi-year offer often land at the same blended 2%; a series of new offers is the only structure that costs more [CZ1].
3. **On Google, add a CUD commitment to usage-priced deals** so TCV is non-zero and eligible for 2% or 1.5% [CZ3][G20].
4. **Auto-register at a fixed CRM stage with filters.** Vectra registers nearly all SaaS deals at the qualified stage via CRM filters and runs "thousands" of ACE registrations [CZ78]; Verint adds a two-step draft then alliance-owner review before submission [CZ14].
5. **Automate the first touch to the hyperscaler rep.** On ACE acceptance send the AWS seller a tailored message immediately; alert reps in Slack when AWS or Microsoft sellers engage [CZ14]. Microsoft inbound: respond in under 4 hours [CZ20].
6. **Track the relationship, not just the deal.** Keep a partner-contacts register of AWS, Microsoft and Google reps per opportunity with active and total co-sold deals; report seller-level engagement [CZ18][CZ17]. Clazar says it built relationships with at least 1,000 AWS AMs by registering volume [CZ79].
7. **Ask two commit questions in discovery:** which cloud holds the commitment and when it expires; Microsoft Q4 (April to June) is the burn window [CZ20][CZ21]. CyberArk's version: ask the technical champion who owns the cloud provider relationship and spend agreement, then go to that executive [CZ81].
8. **Register and launch everything you close, even off-marketplace.** Hyperscaler sellers pick ISVs with strong registration and launch ratios because variable comp increasingly rewards marketplace transactions (CyberArk practitioner, February 2025) [CZ81].
9. **PRM tagging at scale:** Terraform `default_tags` or CloudFormation StackSets so every new resource carries `aws-apn-id`; confirm customer consent for customer-account resources; keep three screenshots (listing public, account linked, resource tag with ARN) for troubleshooting [CZ39].
10. **Private offer lifecycle rules for Eva (AWS):** withdraw and recreate before acceptance; ABO after; USD 0 contract value on price-only ABOs; a new metering dimension needs an ABO for existing customers; meter overages monthly in whole units against a monthly dimension, never backdated [CZ52][CZ51].
11. **Refund versus cancel (AWS):** billing adjustment for refunds, cancellation to end the agreement; share the buyer confirmation link; auto-cancel after 7 days [CZ49][CZ50].
12. **MPO hygiene (Microsoft):** make sure the customer clicks Configure Account and the ISV activates within 30 days, or the MPO dies and must be recreated; never plan an upgrade that overlaps current dates [CZ69].
13. **Prioritize accounts with hyperscaler signals, not gut feel.** Use AWS Solution Score and Eligible Programs (from Lead Prospecting) and Microsoft-managed status by country to choose co-sell targets [CZ46][CZ47]; the 22% Club qualifies commit and engagement score before the first discovery call [CZ71].
14. **Internal enablement before field enablement.** Sales comp neutrality (56% of respondents), AE marketplace training (58%), clean CRM attribution (33%) separate performers from listers [CZ28]. Datadog's advice: find early allies in sales and get early wins [CZ28].
15. **Stage the journey and expect 6 to 12 months:** list, transact one or two deals, become co-sell eligible (FTR, ISVA), then automate registration volume [CZ79]. Clazar's customer-success KPI is "transacted at least one deal in the first three months live" [CZ79], a good leading indicator for Forecastable too.

## 6. Survey and benchmark data

| Figure | Value | Sample | Date | Label |
|---|---|---|---|---|
| Transact on at least one hyperscaler marketplace | 89% | 100+ SaaS companies [CZ30] | 2025-04-24 | VENDOR [CZ28] |
| Share of revenue via marketplace | 22% over 20%; 41% at 0 to 5% | same | 2025 | VENDOR [CZ28] |
| Net-new revenue vs shifted | 62% net-new; 30% mostly shifted direct deals | same | 2025 | VENDOR [CZ28] |
| Outcomes | 54% higher win rates; 50% larger deal values; 48% more new customers (page); 63% acquire new customers (press release) | same | 2025 | VENDOR [CZ28][CZ30] |
| 22% Club vs rest | Win rates 75% vs 47%; larger deals 50% vs 42%; new-customer acquisition 48% vs 44%; automated workflows 63% (more than double); field engagement 94% vs 77% | same | 2025 | VENDOR [CZ28][CZ71] |
| Co-sell | 71% co-sell; 51% too complex to scale; 32% structured cadences (page) or 40% (blog); 81% some field engagement; 19% struggle; 57% of non-proactive cite resources or enablement | same | 2025 | VENDOR [CZ28][CZ29] |
| Motivations | 65% customer preference or contract simplicity; 56% co-sell or co-marketing; 55% broader reach | same | 2025 | VENDOR [CZ28] |
| Internal alignment | Partnerships 84% aligned; sales 75% some buy-in, 22% fully; RevOps 58% support, 38% neutral, 29% fully; 42% RevOps unconvinced | same | 2025 | VENDOR [CZ28] |
| Enablement | 60% in hyperscaler programs such as ISVA; 58% started AE training; 56% comp neutral or better; 37% automated usage tracking; 33% track attribution in CRM | same | 2025 | VENDOR [CZ28] |
| Automation maturity | Reporting 72% started, 21% high; usage tracking 62%, 15% high; attribution 60%, 20% high | same | 2025 | VENDOR [CZ28] |
| Tooling | 62% run workflows in CRM; 41% third-party platform; 40% in-house build | same | 2025 | VENDOR [CZ28] |
| Channel | 31% say channel influences over 20% of marketplace deals; 64% win-rate lift with strong partner involvement; 63% say channel partners becoming critical; 27% pursue multi-cloud | same | 2025 | VENDOR [CZ28] |
| Plans | 51% more training; 49% more channel; 40% automation investment | same | 2025 | VENDOR [CZ28] |
| Pre-committed budgets | USD 419B (press release 2025-04); USD 340B (2024); USD 380B (2025-02); USD 370B (guide); "close to USD 900B" (2026, RPO-based) | varies | 2024 to 2026 | VENDOR, inconsistent [CZ30][CZ35][CZ26][CZ20][CZ83] |
| Canalys co-sell | Partners that co-sell frequently: 51% higher revenue growth, 65% higher close rates, 54% larger deals | Canalys, undated in guide | cited 2026 | VENDOR relay of INDEPENDENT [CZ19] |
| ISVA effect "AWS reports" | 40% to 60% faster cycles; 25% to 40% larger deals | none cited | about 2026-08 | VENDOR, UNVERIFIED [CZ36] |
| List & Sell participants vs non (Sept 2023 to Dec 2024) | 97% higher TCV; nearly 1.5x more private offers; 28% faster publication | AWS | 2025-03-25 | OFFICIAL [CZ87] |
| Procurement cycle | reduced "at least 30 to 40%" via marketplace | Clazar customers | about 2025-11 | VENDOR [CZ79] |
| DIY listing | 400 to 700 hours, USD 35K to 82K, 13 to 24 weeks; 20% of manual submissions rejected; 10 to 15 minutes per offer or opportunity | none cited | 2025-08-20 | VENDOR, self-serving [CZ15] |
| Marketplace ARR target | "Mature programs" 20% to 30%+ of ARR through marketplace | none cited | 2026 | VENDOR [CZ19][CZ20][CZ21] |
| AWS Marketplace catalog | about 22,000 solutions | Clazar demo | about 2025-11 | VENDOR [CZ79] |

## 7. Conflicts with our intelligence files

| # | Topic | Clazar says | Our file says | Which wins and why |
|---|---|---|---|---|
| 1 | AWS referral acceptance window | 72 hours (3 business days) for ISVA partners [CZ36] | 5 business days, then the invitation disappears [A43] | Official Sales Guide [A43]. Clazar may be quoting an internal ISVA expectation; brief Eva to aim for 72 h, but the system limit is 5 business days |
| 2 | Partner Central MCP auth | SigV4 on every request, cannot connect directly to Claude [CZ37] | OAuth with AWS Sign-In added 2026-08-20 [A100] | AWS What's New [A100] is newer and official; AWS dev guide still only documents SigV4 [CZ88], so test before promising direct Claude connection |
| 3 | Partner Central migration duration | 15 minutes to several hours; typically 30 to 40 minutes [CZ38] | 2 to 6 hours [A8] | Official [A8] for planning; Clazar's figure reflects small accounts |
| 4 | Migration deadline | "Incentive-related deadline June 30, 2026" [CZ10] | No published cutoff [A8][A11] | Official. Date has passed with no public enforcement |
| 5 | PRM funding deadline | Required for funding eligibility from 2026-07-31 [CZ39]; later "planning dates, not formal" [CZ40] | Not in file; PRM gates FTR and new ISVA MDF [A49][A6] | Neither official; add as UNVERIFIED ecosystem date |
| 6 | Microsoft program names | ISV Success, App Accelerate "coming", Marketplace Rewards rebates USD 20K at USD 100K ACR and USD 50K at USD 4M, Partner Sales Connect [CZ6][CZ20] | Frontier Accelerate for Marketplace replaced ISV Success, Marketplace Rewards, IP co-sell packaging, CSD in September 2026 [M30]; Referrals in Partner Center [M10] | Official Microsoft [M30][M22]. Clazar content is stale; the rebate figures have no official source |
| 7 | PRACR | Listed as a co-sell financial incentive (June 2026 article) [CZ58b] | No longer a broad co-sell mechanism from 2026-07-01; MBS recognized [M13] | Official [M13] |
| 8 | Microsoft supplemental content | Three classes: fully, partially, not hosted [CZ60] | IP co-sell needs "primarily platformed on Azure" [M1] | Official Learn page (2026-06-01) has five approved hosting categories plus Azure subscription IDs [CZ86]; add to Microsoft file |
| 9 | MPO scope | Channel partner tax profile US or UK only; describes MPO as CSP or Open Licensing purchasing [CZ69][CZ23] | 37 customer countries; MPO excludes CSP customers [M38][M93] | Official [M38][M93] |
| 10 | Google program | "Partner Advantage portal", tiers Member/Partner/Premier plus Diamond, Build track (guide updated 2026-09-22) [CZ24][CZ21] | Partner Network, Select/Premier/Diamond, paths [G1][G2] | Official [G1]; already flagged as stale for [G70] |
| 11 | Google renewal fee | 1.5% on all renewals at any TCV [CZ3] | Native renewal conditions (9 months, 90 days, 60% amendment) [G18] | Official [G18] |
| 12 | Google fee FAQ math | USD 900K deal billed at 2% [CZ3] | 3% below USD 1M TCV [G18] | Official; vendor arithmetic error |
| 13 | Google commit vs CUD | Purchases "draw down Committed Use Discounts" [CZ3] | Drawdown counts against the Google Cloud Minimum Commitment, 100% to a 25% cap; CUD is a private offer pricing model [G22][G29] | Official |
| 14 | Google co-sell API | Support case to enable Deal Registration API V2, then Integrator role [CZ62] | Integrator role in Hub; no public co-sell API [G72] | Unresolved vendor disagreement (Tackle, 2026-05-22, shows no support case [CZ90]); treat support case as possibly required for Clazar's API version |
| 15 | AWS fee range | "Typically 3 to 5 percent" [CZ22] | 1.5% to 20% plus CPPO and regional add-ons [A24] | Official |
| 16 | AWS professional services fee | 0.5% [CZ1] | 0.5%, and 0% in qualifying multi-product sets from 2026-09-01 [A29] | Official, Clazar incomplete |
| 17 | Cloud commitment pool | "Close to USD 900B" [CZ20][CZ83] | About USD 470B committed spend (Omdia) and over USD 500B (Partner Insight 2026-06) [X40][X49] | Different definitions: USD 900B sums hyperscaler RPO/backlog including OpenAI-linked Azure RPO. Use Omdia for marketplace-addressable commit |
| 18 | ISVA requirements | Legacy list (2 public references, business plan, field kit, NDA, reduced fees) in older help article [CZ55] | Current eight requirements [A1] | Official; Clazar's newer article [CZ36] matches official |
| 19 | Survey internals | Structured cadences 32% vs 40%; win-rate uplift 54%, 58%, 59% [CZ28][CZ29][CZ17] | Our file cites 59% and 32% to 40% [X44] | Keep as a range; cite the report page [CZ28] as primary |
| 20 | Clazar's own funding workflow | December 2025: create AWS MDF requests in Clazar [CZ7]; August 2026: funding requests read-only, create in Partner Central [CZ41] | n/a | Newer help article [CZ41] |

## 8. Content inventory (since 2025-07-01, plus older items still live and cited)

| Date | Type | Title | Cloud | URL | Substance (1 to 3) |
|---|---|---|---|---|---|
| 2026-09-25 (upd) | Help | Metering support for AWS concurrent agreements | AWS | https://help.clazar.io/articles/5426414470-support-metering-for-aws-concurrent-agreements-and-link-orb-to-the-contract | 2 |
| 2026-09-22 (upd) | Guide | Google Cloud Marketplace guide | Google | https://clazar.io/guides/google-marketplace | 1 |
| 2026-09-17 (upd) | Help | Enter a reseller's 12-digit AWS account ID | AWS | https://help.clazar.io/articles/4950135784-enter-a-reseller-s-12-digit-aws-account-id-on-aws-reseller-offers | 1 |
| 2026-09-16 (upd) | Help | Contract durations up to 12 years on AWS private and reseller offers | AWS | https://help.clazar.io/articles/9727208766-set-contract-durations-up-to-12-years-on-aws-private-and-reseller-offers | 3 |
| 2026-09-11 | Blog | Microsoft Marketplace Fees in 2026 | Microsoft | https://clazar.io/blog/microsoft-marketplace-fees | 3 |
| 2026-09-04 (upd) | Help | Marketplace disbursement events for AWS, Azure and GCP | All | https://help.clazar.io/articles/2797953734-marketplace-disbursement-events-for-aws-azure-and-gcp | 2 |
| 2026-09-07 | Blog | How to Integrate Your CRM with Cloud Marketplaces | All | https://clazar.io/blog/crm-cloud-marketplace-integration | 2 |
| 2026-08-31 (upd) | Help | Track AWS Express Private Offers | AWS | https://help.clazar.io/articles/3760620196-track-aws-express-private-offers-in-clazar | 2 |
| 2026-08-31 (upd) | Help | Customer Business Problem field in AWS co-sell | AWS | https://help.clazar.io/articles/4442170685-project-description-field-name-changed-to-customer-business-problem-in-aws-cosell-opportunity | 2 |
| 2026-08-28 | Blog | Google Cloud Marketplace Fees in 2026 | Google | https://clazar.io/blog/google-cloud-marketplace-fees | 3 |
| 2026-08-28 (upd) | Blog | Azure Co-Sell vs IP Co-Sell Eligible (orig 2026-02-12) | Microsoft | https://clazar.io/blog/azure-co-sell-vs-ip-co-sell-eligible-guide | 2 |
| 2026-08-21 | Blog | Clazar MCP Server | All | https://clazar.io/blog/clazar-mcp-server | 2 |
| 2026-08-21 (upd) | Guide | How to Sell on AWS Marketplace (2026) | AWS | https://clazar.io/guides/aws-marketplace | 3 |
| about 2026-08 | Help | AWS ISV Accelerate Program Guide | AWS | https://help.clazar.io/articles/8525930522-aws-isv-accelerate-program-guide | 3 |
| about 2026-08 | Help | AWS USD 5,000 Funding via Partner Central MCP Server | AWS | https://help.clazar.io/articles/5579664708-aws-5-000-funding-via-partner-central-mcp-server | 3 |
| about 2026-08 | Help | AWS Partner Central Migration Guide | AWS | https://help.clazar.io/articles/2549501160-aws-partner-central-migration-guide | 3 |
| about 2026-08 | Help | Added AWS funding requests across every program | AWS | https://help.clazar.io/articles/8210389206-added-aws-funding-requests-to-clazar-across-every-funding-program | 2 |
| about 2026-08 | Help | FAQ: AWS insights fields (OQS, Solution Score) | AWS | https://help.clazar.io/articles/9241413489-faq-aws-insights-fields-in-the-clazar-salesforce-package-solution-score-prospecting-insights | 3 |
| about 2026-08 | Help | AWS intelligence on companies; country-level Microsoft matching | AWS, Microsoft | https://help.clazar.io/articles/6964200916-adding-aws-intelligence-to-companies-and-enabling-country-level-microsoft-matching | 2 |
| about 2026-08 | Help | How to set up Amazon Payee Central | AWS | https://help.clazar.io/articles/8406421781-how-to-set-up-your-amazon-payee-central-account | 3 |
| about 2026-08 | Help | FAQ: charging customer overages (user-based billing) | AWS | https://help.clazar.io/articles/1707377340-faq-charging-customer-overages-on-aws-marketplace-user-based-billing | 3 |
| about 2026-08 | Help | Added deal registration for Azure co-sell | Microsoft | https://help.clazar.io/articles/4915534810-added-deal-registration-for-azure-cosell-opportunities | 3 |
| about 2026-08 | Help | Azure co-sell field mapping | Microsoft | https://help.clazar.io/articles/8069734262-azure-co-sell-field-mapping | 2 |
| about 2026-08 | Help | Azure co-sell setup guide | Microsoft | https://help.clazar.io/articles/8949894897-azure-co-sell-setup-guide | 2 |
| about 2026-08 | Help | Clazar MCP Server setup guide | All | https://help.clazar.io/articles/4639208093-clazar-mcp-server-setup-guide | 2 |
| 2026-08-11 | Blog | AWS Marketplace Fees in 2026 | AWS | https://clazar.io/blog/aws-marketplace-fees | 3 |
| 2026-08-04 (upd) | Guide | A Complete Guide to Co-Selling with Azure (2026) | Microsoft | https://clazar.io/guides/co-selling-with-azure | 2 (stale names) |
| 2026-08-04 (upd) | Guide | A Complete Guide to Co-Selling with Google (2026) | Google | https://clazar.io/guides/co-selling-with-google | 1 (stale) |
| 2026-08-04 (upd) | Guide | Sell on Azure Marketplace: The Complete 2026 Guide | Microsoft | https://clazar.io/guides/azure-marketplace | 1 |
| 2026-08-04 (upd) | Guide | How to Sell on Cloud Marketplaces | All | https://clazar.io/guides/cloud-marketplace | 1 |
| about 2026-07 | Help | AWS PRM Resource Tagging Guide (content dated 2026-04-10) | AWS | https://help.clazar.io/articles/3878307567-aws-prm-resource-tagging-guide | 3 |
| about 2026-06 | Help | Tag your AWS resources for PRM with Claude | AWS | https://help.clazar.io/articles/9203440346-tag-your-aws-resources-for-prm-automatically-with-claude | 2 |
| about 2026-06 | Help | Self-serve cancellation on AWS | AWS | https://help.clazar.io/articles/7914177068-self-serve-cancellation-on-aws | 3 |
| about 2026-06 | Help | Self-serve billing adjustment on AWS | AWS | https://help.clazar.io/articles/5218731876-self-serve-billing-adjustment-on-aws | 3 |
| about 2026-06 | Help | GCP co-sell setup | Google | https://help.clazar.io/articles/7551597013-gcp-co-sell-setup | 3 |
| about 2026-06 | Help | AWS co-sell setup | AWS | https://help.clazar.io/articles/7351812102-aws-co-sell-setup-steps | 1 |
| about 2026-06 | Help | What is Azure co-sell? (stale PRACR) | Microsoft | https://help.clazar.io/articles/9797712448-azurecosell | 1 |
| about 2026-06 | Podcast (external) | The Customer Wins: Transforming Cloud Marketplace Sales With AI (Trunal Bhanse) | All | https://www.youtube.com/watch?v=AwYokfCEsNQ | 1 |
| about 2026-05 | Help | Prerequisites for Azure Marketplace listing | Microsoft | https://help.clazar.io/articles/2300588509-prerequisites-for-azure-marketplace-listing | 2 |
| about 2026-04 | Help | [Salesforce] AWS co-sell field mapping | AWS | https://help.clazar.io/articles/5877532302-aws-co-sell-field-mapping | 3 |
| 2026-04-16 (upd) | Guide | A Complete Guide on Co-selling (2026) | All | https://clazar.io/guides/co-selling | 1 |
| about 2026-03 | Help | Microsoft Partner Center account verification, tax and payout | Microsoft | https://help.clazar.io/articles/3350322513-microsoft-partner-center-account-setup | 3 |
| 2026-02-24 | Webinar (Partner Insight, Trunal speaker) | Converting cloud commits into marketplace revenue (AWS, Qlik, Supabase templates) | AWS | http://partnerinsight.io/webinar-aws-marketplace-revenue-playbook-feb-24 | not watched |
| 2026-02-24 (upd) | Blog | State of cloud marketplace and co-sell today (orig 2025-04-24) | All | https://clazar.io/blog/state-of-cloud-marketplace-and-co-sell-report-insights | 2 |
| 2026-02-17 (upd) | Guide | A Complete Guide to Co-Selling with AWS | AWS | https://clazar.io/guides/co-selling-with-aws | 1 |
| about 2026-02 | YouTube | How Supabase Scales AWS Marketplace Revenue with Clazar | AWS | https://www.youtube.com/watch?v=HJ3dRtCBtyM | 2 |
| 2026-01-07 | Blog | December 2025 Product Release | All | https://clazar.io/blog/clazar-december-2025-release | 2 |
| 2026-01-01 | Blog | How to register as a seller on AWS Marketplace | AWS | https://clazar.io/blog/how-to-register-as-a-seller-on-aws-marketplace | 2 |
| 2025-12-15 | Blog | November 2025 Product Release | All | https://clazar.io/blog/clazar-november-2025-release | 1 |
| 2025-12-01 | Blog | The new AWS Partner Central experience | AWS | https://clazar.io/blog/the-new-aws-partner-central-experience-what-is-changing-and-how-clazar-helps-you-migrate-for-free | 2 |
| 2025-12-01 (page) | Report | 2025 State of Cloud Marketplace & Co-Sell (full web version) | All | https://clazar.io/reports/state-of-cloud-marketplace-cosell | 3 |
| 2025-11-17 | Blog | October 2025 Product Release | All | https://clazar.io/blog/clazar-october-2025-release | 1 |
| about 2025-11 | YouTube (AWS Events) | Clazar: Supercharge your GTM with AWS Marketplace (Let's Build a Startup) | AWS | https://www.youtube.com/watch?v=cmT2H1hVqV4 | 3 |
| about 2025-11 | YouTube | How Vectra doubled AWS Marketplace volume | AWS, Microsoft | https://www.youtube.com/watch?v=qaJFcRvZrKw | 2 |
| about 2025-11 | YouTube | Six Trunal Bhanse explainers (fees, private offers, eligibility, visibility, mistakes, publishing) | AWS | https://www.youtube.com/@GetClazar | 1 |
| about 2025-10 | Help | Managing AWS private offers: amendments, rebuys, listing migrations | AWS | https://help.clazar.io/articles/5584662554-managing-aws-marketplace-private-offers-amendments-rebuys-and-listing-migrations | 3 |
| about 2025-10 | Help | Custom private offer in Google Cloud Marketplace | Google | https://help.clazar.io/articles/9030433614-how-to-create-a-custom-private-offer-in-google-cloud-marketplace | 2 |
| 2025-09-22 | Blog | Combined cloud analytics | All | https://clazar.io/blog/clazar-enhanced-analytics | 1 |
| 2025-09-16 | Webinar | The marketplace multiplier: co-sell, automation, agentic AI (AWS, Wiz, Confluent) | AWS | https://clazar.io/events/growing-marketplace-revenue-with-agentic-ai | not transcribed (recording gated) |
| 2025-09-15 | Blog | August release (GCP co-sell automation, CUD offers) | Google | https://clazar.io/blog/august-release | 2 |
| 2025-08-29 | Blog | From referrals to revenue: co-sell automation (Verint, Vectra) | AWS, Microsoft | https://clazar.io/blog/cloud-marketplace-co-sell-automation | 2 |
| 2025-08-20 | Blog | True cost of DIY cloud marketplace management | All | https://clazar.io/blog/the-hidden-costs-of-diy-cloud-marketplace-management | 1 |
| 2025-08-15 | Blog | July release (Azure renewal field, AWS offer description, Snowflake) | All | https://clazar.io/blog/july-release | 1 |
| about 2025 | Help | GCP Producer Portal self-serve free trials | Google | https://help.clazar.io/articles/3371480084-GCP+Free+Trials | 2 |
| about 2025 | Help | GCP AI Agent Marketplace explainer | Google | https://help.clazar.io/articles/9441774242-GCP+AI+Agent+Marketplace | 2 |
| about 2025 | Help | Making your GCP listing live | Google | https://help.clazar.io/articles/9836165497-making-your-gcp-listing-live | 2 |
| about 2025 | Help | AWS Marketplace SaaS policy update | AWS | https://help.clazar.io/articles/4668266154-AWS-SaaS-Policy-Update | 2 |
| about 2025 | Help | AWS co-sell (legacy ISVA requirements) | AWS | https://help.clazar.io/articles/7993651896-awsco-sell | 1 (stale) |
| 2025-07-22 | Blog | How to scale co-sell without chaos | All | https://clazar.io/blog/co-sell-at-scale-without-chaos | 2 |
| 2025-07-10 | Blog | June release (partner contacts, GCP co-sell in HubSpot) | All | https://clazar.io/blog/june-release-partner-contratcs-future-billings | 1 |
| 2025-06-26 | Webinar | Scaling co-sell from referral to revenue (Verint, Vectra) | AWS | https://clazar.io/events/scaling-cosell-with-automation | 2 |
| 2025-05-08 | Blog | Inside the 22% Club | All | https://clazar.io/blog/inside-the-22-percent-club-marketplace-leaders | 2 |
| 2025-04-24 | Report launch webinar and press release | 2025 State of Cloud Marketplace & Co-Sell | All | https://clazar.io/events/state-of-cloud-marketplace-and-cosell-launch | 2 |
| 2025-03-25 | Podcast | Last Clazar Podcast episode (adaptive marketplace strategy, Andre King) | All | https://clazar.io/podcasts | 1 |
| 2025-02-28 | Blog | How AWS' new SaaS policy reshapes the marketplace | AWS | https://clazar.io/blog/aws-new-saas-policy | 2 |
| 2025-02-05 | Blog (upd 2026-02-23) | Microsoft Marketplace Multiparty Private Offers | Microsoft | https://clazar.io/blog/azure-marketplace-mpo-channel-sales | 2 |
| 2025-02-05 | Podcast | Behind-the-deal dynamics with Brennan Lynch (CyberArk) | All | https://www.youtube.com/watch?v=mr0sbLmf2Qk | 2 |

## 9. Registry rows and discovery queries

| Name | Role | Where to look | Good for | Last new item |
|---|---|---|---|---|
| Clazar help center (Changelog and Cloud Sales collections) | VENDOR, product docs | https://help.clazar.io (sitemap https://help.clazar.io/sitemap.xml) | Fastest-moving surface: AWS portal field changes, ISVA hygiene, PRM tagging, Microsoft deal registration, GCP co-sell setup, funding program lists | 2026-09-25 (concurrent agreements metering) |
| Clazar blog | VENDOR | https://clazar.io/blog ; sitemap https://clazar.io/sitemap.xml | Fee explainers per cloud with worked examples; CRM integration; MCP | 2026-09-11 |
| Trunal Bhanse | Co-founder and CEO, Clazar | LinkedIn (profile URL not verified this pass); YouTube explainers @GetClazar; guest spots (The Customer Wins 2026-06; Partner Insight webinar 2026-02-24) | Report narrative, AWS marketplace basics; low on program detail | about 2026-06 (podcast guest) |
| Lalit Aggarwal | Clazar, author of 2026 fee and MCP posts; ran AWS "Let's Build a Startup" demo | https://clazar.io/blog (author byline) | Fee math, AWS incentive mechanics (List & Sell, ACE-CRM) | 2026-09-11 |
| Mani Makkar | Clazar product marketing, release notes and Azure co-sell guide | https://clazar.io/blog ; help center changelog | Feature-level changes that mirror hyperscaler portal changes | 2026-08-28 |
| Roman Kirsanov, Partner Insight | CREATOR; co-author of the 2025 report | https://newsletter.partnerinsight.io (RSS /feed) | Commit-pool sizing, co-sell tactics, joint webinars with Clazar | 2026-02-13 (USD 900B commits post) |
| Clazar YouTube | VENDOR | https://www.youtube.com/@GetClazar (channel UC_CSjI-uqbp1-OHl9b-a8Lw) | Customer testimonials; mostly re-uploads | about 2026-02 (Supabase). Candidate for Dormant |
| Clazar Podcast | VENDOR | https://clazar.io/podcasts | Older AWS co-sell and Google economics episodes | 2025-03-25. Dormant |
| Clazar events | VENDOR | https://clazar.io/events | Report launches, customer panels with AWS staff | 2025-09-16; no upcoming on 2026-09-26 |

Discovery queries (run monthly, last 45 days):
1. `site:help.clazar.io AWS OR Azure OR GCP` sorted by newest (or diff the help sitemap for new article IDs).
2. `"Clazar" "State of Cloud Marketplace" 2026 report` (watch for a 2026 edition with Partner Insight).
3. `"Trunal Bhanse" podcast OR webinar 2026`.
4. `"Clazar" MCP OR "Partner Central MCP" credits`.
5. YouTube search `Clazar` with upload date "month", plus `@GetClazar` RSS.

## Sources

| Tag | Title | Date | URL |
|---|---|---|---|
| CZ1 | AWS Marketplace Fees in 2026: Private Offers, CPPO Uplift, and More (Lalit Aggarwal) | 2026-08-11, updated 2026-08-25 | https://clazar.io/blog/aws-marketplace-fees |
| CZ2 | Microsoft Marketplace Fees in 2026: What You Pay by Offer Type (Lalit Aggarwal) | 2026-09-11 | https://clazar.io/blog/microsoft-marketplace-fees |
| CZ2x | Marketplace disbursement events for AWS, Azure and GCP (help) | about 2026-09-04 | https://help.clazar.io/articles/2797953734-marketplace-disbursement-events-for-aws-azure-and-gcp |
| CZ3 | Google Cloud Marketplace Fees in 2026: Rates by Offer Type (Siddhartha Jain) | 2026-08-28, updated 2026-09-05 | https://clazar.io/blog/google-cloud-marketplace-fees |
| CZ4 | How to Integrate Your CRM with Cloud Marketplaces (AWS, Microsoft and Google Cloud) | 2026-09-07 | https://clazar.io/blog/crm-cloud-marketplace-integration |
| CZ5 | Clazar MCP Server: Query Your Cloud Partnerships Data Wherever You Work | 2026-08-21, updated 2026-08-28 | https://clazar.io/blog/clazar-mcp-server |
| CZ6 | Azure Co-Sell vs. IP Co-Sell Eligible: The Complete Guide for ISVs (Mani Makkar) | 2026-02-12, updated 2026-08-28 | https://clazar.io/blog/azure-co-sell-vs-ip-co-sell-eligible-guide |
| CZ7 | December 2025 Product Release | 2026-01-07 | https://clazar.io/blog/clazar-december-2025-release |
| CZ8 | How to register as a seller on AWS Marketplace (Aakash Sinha) | 2026-01-01, updated 2026-02-11 | https://clazar.io/blog/how-to-register-as-a-seller-on-aws-marketplace |
| CZ9 | November 2025 Product Release | 2025-12-15 | https://clazar.io/blog/clazar-november-2025-release |
| CZ10 | The new AWS Partner Central experience and free migration | 2025-12-01, updated 2026-01-05 | https://clazar.io/blog/the-new-aws-partner-central-experience-what-is-changing-and-how-clazar-helps-you-migrate-for-free |
| CZ11 | October 2025 Product Release | 2025-11-17 | https://clazar.io/blog/clazar-october-2025-release |
| CZ12 | Clazar's combined cloud analytics | 2025-09-22 | https://clazar.io/blog/clazar-enhanced-analytics |
| CZ13 | What's new in Clazar this August | 2025-09-15 | https://clazar.io/blog/august-release |
| CZ14 | From referrals to revenue: co-sell automation (Samhita Suresh) | 2025-08-29, updated 2026-03-27 | https://clazar.io/blog/cloud-marketplace-co-sell-automation |
| CZ15 | The true cost of DIY cloud marketplace management (Aakash Sinha) | 2025-08-20 | https://clazar.io/blog/the-hidden-costs-of-diy-cloud-marketplace-management |
| CZ16 | What's new in Clazar this July | 2025-08-15 | https://clazar.io/blog/july-release |
| CZ17 | How to scale co-sell without chaos (Shikhar Jaiswal) | 2025-07-22, updated 2026-02-17 | https://clazar.io/blog/co-sell-at-scale-without-chaos |
| CZ18 | What's new in Clazar this June | 2025-07-10 | https://clazar.io/blog/june-release-partner-contratcs-future-billings |
| CZ19 | A Complete Guide to Co-Selling with AWS | page updated 2026-02-17 | https://clazar.io/guides/co-selling-with-aws |
| CZ20 | A Complete Guide to Co-Selling with Azure (2026) | page updated 2026-08-04 | https://clazar.io/guides/co-selling-with-azure |
| CZ21 | A Complete Guide to Co-Selling with Google (2026) | page updated 2026-08-04 | https://clazar.io/guides/co-selling-with-google |
| CZ22 | How to Sell on AWS Marketplace: A Complete Guide (2026) | page updated 2026-08-21 | https://clazar.io/guides/aws-marketplace |
| CZ23 | Sell on Azure Marketplace: The Complete 2026 Guide | page updated 2026-08-04 | https://clazar.io/guides/azure-marketplace |
| CZ24 | Google Cloud Marketplace guide | page updated 2026-09-22 | https://clazar.io/guides/google-marketplace |
| CZ25 | A Complete Guide On Co-selling (2026) | page updated 2026-04-16 | https://clazar.io/guides/co-selling |
| CZ26 | A Complete Guide On How To Sell on Cloud Marketplaces | page updated 2026-08-04 | https://clazar.io/guides/cloud-marketplace |
| CZ27 | A Complete Guide To Cloud GTM | page updated 2026-01-20 | https://clazar.io/guides/cloud-gtm |
| CZ28 | 2025 State of Cloud Marketplace & Co-Sell (report web edition, with Partner Insight) | 2025-04-24; page 2025-12-01 | https://clazar.io/reports/state-of-cloud-marketplace-cosell |
| CZ29 | The state of cloud marketplace and co-sell today (Trunal Bhanse) | 2025-04-24, updated 2026-02-24 | https://clazar.io/blog/state-of-cloud-marketplace-and-co-sell-report-insights |
| CZ30 | In the AI Era, Cloud Marketplaces Are Reshaping How Software Gets Sold (press release, Clazar with Partner Insight) | 2025-04-24 | https://www.prnewswire.com/news-releases/in-the-ai-era-cloud-marketplaces-are-reshaping-how-software-gets-sold-302437474.html |
| CZ31 | Pricing | fetched 2026-09-26 (page updated 2026-09-15) | https://clazar.io/pricing |
| CZ32 | About us | fetched 2026-09-26 | https://clazar.io/about-us |
| CZ33 | Co-Sell Automation (platform page) | fetched 2026-09-26 | https://clazar.io/platform/co-sell-automation |
| CZ34 | Customer Stories | fetched 2026-09-26 | https://clazar.io/customers |
| CZ34b | Integrations; API | fetched 2026-09-26 | https://clazar.io/integrations ; https://clazar.io/api |
| CZ35 | Announcing Clazar's USD 10M Series A (Trunal Bhanse) | 2024-04-18 | https://clazar.io/blog/series-a-announcement |
| CZ36 | AWS ISV Accelerate Program Guide (help) | about 2026-08 | https://help.clazar.io/articles/8525930522-aws-isv-accelerate-program-guide |
| CZ37 | AWS USD 5,000 Funding via Partner Central MCP Server (help) | about 2026-08 | https://help.clazar.io/articles/5579664708-aws-5-000-funding-via-partner-central-mcp-server |
| CZ38 | AWS Partner Central Migration Guide (help; same as our A10) | about 2026-08 | https://help.clazar.io/articles/2549501160-aws-partner-central-migration-guide |
| CZ39 | AWS PRM Resource Tagging Guide (help) | content 2026-04-10, updated about 2026-07 | https://help.clazar.io/articles/3878307567-aws-prm-resource-tagging-guide |
| CZ40 | Tag Your AWS Resources for PRM Automatically with Claude (help) | about 2026-06 | https://help.clazar.io/articles/9203440346-tag-your-aws-resources-for-prm-automatically-with-claude |
| CZ41 | Added AWS funding requests to Clazar, across every funding program (help) | about 2026-08 | https://help.clazar.io/articles/8210389206-added-aws-funding-requests-to-clazar-across-every-funding-program |
| CZ42 | Track AWS Express Private Offers in Clazar (help) | about 2026-08-31 | https://help.clazar.io/articles/3760620196-track-aws-express-private-offers-in-clazar |
| CZ43 | Set contract durations up to 12 years on AWS private and reseller offers (help) | about 2026-09-16 | https://help.clazar.io/articles/9727208766-set-contract-durations-up-to-12-years-on-aws-private-and-reseller-offers |
| CZ44 | Project Description renamed Customer Business Problem (help) | about 2026-08-31 | https://help.clazar.io/articles/4442170685-project-description-field-name-changed-to-customer-business-problem-in-aws-cosell-opportunity |
| CZ45 | Metering support for AWS concurrent agreements (help) | about 2026-09-25 | https://help.clazar.io/articles/5426414470-support-metering-for-aws-concurrent-agreements-and-link-orb-to-the-contract |
| CZ46 | FAQ: AWS insights fields (Solution Score, Prospecting, OQS) (help) | about 2026-08 | https://help.clazar.io/articles/9241413489-faq-aws-insights-fields-in-the-clazar-salesforce-package-solution-score-prospecting-insights |
| CZ47 | AWS intelligence on companies; country-level Microsoft matching (help) | about 2026-08 | https://help.clazar.io/articles/6964200916-adding-aws-intelligence-to-companies-and-enabling-country-level-microsoft-matching |
| CZ48 | [Salesforce] AWS Co-Sell Field Mapping (help) | about 2026-04 | https://help.clazar.io/articles/5877532302-aws-co-sell-field-mapping |
| CZ49 | Self-serve cancellation on AWS (help) | about 2026-06 | https://help.clazar.io/articles/7914177068-self-serve-cancellation-on-aws |
| CZ50 | Self-serve billing adjustment on AWS (help) | about 2026-06 | https://help.clazar.io/articles/5218731876-self-serve-billing-adjustment-on-aws |
| CZ51 | FAQ: Charging customer overages on AWS Marketplace (help) | about 2026-08 | https://help.clazar.io/articles/1707377340-faq-charging-customer-overages-on-aws-marketplace-user-based-billing |
| CZ52 | Managing AWS private offers: amendments, rebuys, listing migrations (help) | about 2025-10 | https://help.clazar.io/articles/5584662554-managing-aws-marketplace-private-offers-amendments-rebuys-and-listing-migrations |
| CZ52b | AWS Private Offers (help) | about 2025 | https://help.clazar.io/articles/5206586827-awsprivateoffers |
| CZ53 | How to set up your Amazon Payee Central account (help) | about 2026-08 | https://help.clazar.io/articles/8406421781-how-to-set-up-your-amazon-payee-central-account |
| CZ54 | AWS Marketplace SaaS Policy Update (help) | about 2025 | https://help.clazar.io/articles/4668266154-AWS-SaaS-Policy-Update |
| CZ55 | AWS Co-Sell (help, legacy ISVA requirements) | about 2025 | https://help.clazar.io/articles/7993651896-awsco-sell |
| CZ56 | Added deal registration for Azure co-sell opportunities (help) | about 2026-08 | https://help.clazar.io/articles/4915534810-added-deal-registration-for-azure-cosell-opportunities |
| CZ57 | Azure Co-Sell Field Mapping (help) | about 2026-08 | https://help.clazar.io/articles/8069734262-azure-co-sell-field-mapping |
| CZ58 | Azure Co-Sell Setup Guide (help) | about 2026-08 | https://help.clazar.io/articles/8949894897-azure-co-sell-setup-guide |
| CZ58b | What is Azure Co-Sell? (help) | about 2026-06 | https://help.clazar.io/articles/9797712448-azurecosell |
| CZ59 | Microsoft Partner Center account verification, tax and payout (help) | about 2026-03 | https://help.clazar.io/articles/3350322513-microsoft-partner-center-account-setup |
| CZ60 | Prerequisites for Azure Marketplace Listing (help) | about 2026-05 | https://help.clazar.io/articles/2300588509-prerequisites-for-azure-marketplace-listing |
| CZ61 | How to Purchase SaaS Private Offers in the Azure Marketplace (help) | about 2025 | https://help.clazar.io/articles/9760487722-purchase-saas-private-offers-in-azure-marketplace |
| CZ62 | GCP Co-Sell Setup (help) | about 2026-06 | https://help.clazar.io/articles/7551597013-gcp-co-sell-setup |
| CZ62b | AWS Co-sell Setup (help) | about 2026-06 | https://help.clazar.io/articles/7351812102-aws-co-sell-setup-steps |
| CZ63 | GCP Producer Portal: Self-Serve Free Trials (help) | about 2025 | https://help.clazar.io/articles/3371480084-GCP+Free+Trials |
| CZ64 | GCP AI Agent Marketplace Explainer (help) | about 2025 | https://help.clazar.io/articles/9441774242-GCP+AI+Agent+Marketplace |
| CZ65 | Making Your GCP Listing Live (help) | about 2025 | https://help.clazar.io/articles/9836165497-making-your-gcp-listing-live |
| CZ66 | How to Create a Custom Private Offer in Google Cloud Marketplace (help) | about 2025-10 | https://help.clazar.io/articles/9030433614-how-to-create-a-custom-private-offer-in-google-cloud-marketplace |
| CZ66b | How to Share Private Offers on GCP Marketplace (help) | about 2025 | https://help.clazar.io/articles/4670125070-how-to-create-and-share-private-offers-on-gcp-marketplace |
| CZ67 | Clazar MCP Server setup guide (help) | about 2026-08 | https://help.clazar.io/articles/4639208093-clazar-mcp-server-setup-guide |
| CZ68 | How AWS' new SaaS policy reshapes the marketplace (Samhita Suresh) | 2025-02-28 | https://clazar.io/blog/aws-new-saas-policy |
| CZ69 | Maximize channel sales with Multiparty Private Offers (Arijit Bose) | 2025-02-05, page updated 2026-02-23 | https://clazar.io/blog/azure-marketplace-mpo-channel-sales |
| CZ70 | Ten steps to grow revenue by aligning with hyperscaler priorities | 2025-03-20 | https://clazar.io/blog/aligning-with-hyperscaler-priorities |
| CZ71 | Inside the 22% club (Samhita Suresh) | 2025-05-08 | https://clazar.io/blog/inside-the-22-percent-club-marketplace-leaders |
| CZ72 | Cracking the co-sell code (Samhita Suresh) | 2025-05-13 | https://clazar.io/blog/cracking-the-co-sell-code |
| CZ73 | Events and Webinars | fetched 2026-09-26 | https://clazar.io/events |
| CZ74 | The marketplace multiplier webinar (AWS, Wiz, Confluent, Clazar) | 2025-09-16 | https://clazar.io/events/growing-marketplace-revenue-with-agentic-ai |
| CZ75 | Scaling co-sell from referral to revenue with automation (webinar) | 2025-06-26 | https://clazar.io/events/scaling-cosell-with-automation |
| CZ76 | The Clazar Podcast index | last episode 2025-03-25 | https://clazar.io/podcasts |
| CZ77 | How Supabase Scales AWS Marketplace Revenue with Clazar (YouTube) | about 2026-02 | https://www.youtube.com/watch?v=HJ3dRtCBtyM |
| CZ78 | How Vectra doubled AWS Marketplace volume with Clazar (YouTube) | about 2025-11 | https://www.youtube.com/watch?v=qaJFcRvZrKw |
| CZ79 | Clazar: Supercharge your go-to-market strategy with AWS Marketplace (AWS Events, Let's Build a Startup) | about 2025-11 | https://www.youtube.com/watch?v=cmT2H1hVqV4 |
| CZ80 | Transforming Cloud Marketplace Sales With AI With Trunal Bhanse (The Customer Wins) | about 2026-06 | https://www.youtube.com/watch?v=AwYokfCEsNQ |
| CZ81 | Uncovering behind-the-deal dynamics of marketplace success with Brennan Lynch (Clazar podcast) | 2025-02-05 | https://www.youtube.com/watch?v=mr0sbLmf2Qk |
| CZ82 | Trunal Bhanse AWS Marketplace explainers (six shorts) | about 2025-11 | https://www.youtube.com/@GetClazar |
| CZ83 | USD 531B to USD 900B in One Quarter: The Cloud Commit Jump (Partner Insight, CREATOR) | 2026-02-13 | https://newsletter.partnerinsight.io/p/531b-900b-in-one-quarter-the-cloud |
| CZ84 | Understanding listing fees for AWS Marketplace sellers (OFFICIAL, verification) | fetched 2026-09-26 | https://docs.aws.amazon.com/marketplace/latest/userguide/listing-fees.html |
| CZ85 | AWS ISV Accelerate Program (OFFICIAL, verification) | fetched 2026-09-26 | https://aws.amazon.com/partners/programs/isv-accelerate/ |
| CZ86 | Supplemental content for a SaaS offer (Microsoft Learn, OFFICIAL, verification) | 2026-06-01 | https://learn.microsoft.com/en-us/partner-center/marketplace-offers/create-new-saas-offer-supplemental |
| CZ87 | AWS Marketplace List & Sell Incentive page and launch blog (OFFICIAL, verification) | blog 2025-03-25; page fetched 2026-09-26 | https://aws.amazon.com/partners/saas-on-aws/mpls/ ; https://aws.amazon.com/blogs/awsmarketplace/winning-in-aws-marketplace-introducing-aws-marketplace-list-sell-program/ |
| CZ88 | Connect AI agents to AWS Partner Central with the MCP Server (OFFICIAL, verification) | fetched 2026-09-26 | https://docs.aws.amazon.com/partner-central/latest/developer-guide/partner-central-mcp-server.html |
| CZ89 | AWS PRM Deadline: What Partners Need to Know Before July 31, 2026 (MontyCloud, VENDOR) | 2026-05-22 | https://montycloud.com/blog-aws-prm-deadline-2026-partner-guide/ |
| CZ90 | Connect to Google Cloud for co-sell registration (Tackle Help, VENDOR) | 2026-05-22 | https://help.tackle.io/en/articles/15217465-connect-to-google-cloud-for-co-sell-registration |
| CZ91 | Customer Office Hours (Clazar event page) | 2025-06-05 | https://clazar.io/events/customer-office-hours/automation |
| CZ92 | 2025 State of Cloud Marketplace & Co-Sell launch webinar (with Zoom, UserTesting, NetApp, Partner Insight) | 2025-04-24 | https://clazar.io/events/state-of-cloud-marketplace-and-cosell-launch |
| CZ93 | Five barriers to marketplace scale (Samhita Suresh) | 2025-05-03 | https://clazar.io/blog/five-barriers-to-marketplace-scale |
| CZ94 | Clazar sitemap and paginated blog index (inventory basis) | fetched 2026-09-26 | https://clazar.io/sitemap.xml ; https://clazar.io/blog |
| CZ95 | Supabase case study | fetched 2026-09-26 | https://clazar.io/case-studies/supabase |
