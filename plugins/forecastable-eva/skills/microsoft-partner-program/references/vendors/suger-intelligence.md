# Suger content intelligence
Built 2026-09-26. VENDOR source: operational detail, labeled; official pages win on conflicts.

Scope of this pass: Suger's sitemap (356 URLs, 265 blog posts, 19 guides) was fully enumerated on 2026-09-26; 185 blog, guide and case-study items dated 2025-07-01 or later were inventoried (section 8). 48 items were read in full, about 25 more were scanned for rule and number lines, plus the pricing, platform, API, MCP, about and changelog pages, one docs page (doc.suger.io), and 4 YouTube transcripts. Three NEW claims carrying numbers were checked against official AWS and Google pages (SG85 to SG87). Every fact below is VENDOR unless tagged with one of our OFFICIAL tags ([A..], [M..], [G..], [X..]) or SG85 to SG87.

How to read Suger: since August 2026 almost every post ends with a "Sources" list of primary AWS, Microsoft and Google docs plus a "Last verified" date, and marks which rules are the cloud's and which are Suger's. That makes the August and September 2026 blog the most rule-dense vendor content we have found. The April to June 2026 pillar guides and the February 2026 "101" posts are much weaker: they carry stale program language and unsourced benchmarks (section 7).

## Ten takeaways that change how Alex or Eva advise

1. **The AWS Opportunity Quality Score is failed by paperwork, not by deal size.** Suger's analysis of scored referrals: every referral in AWS's lowest bucket scored exactly 0; the highest bucket landed at 50 to 75; deal size, expected AWS revenue, industry and region did not correlate. Nearly half of the zeros still had template text in the field, a third had no customer context, a third described the ISV's product instead of the customer's problem [SG13]. An AWS PDM on Suger's August 2026 webinar said the score uses a version of MEDDPICC, rewards a specific ask, and that "10 opportunities of very high quality" beat 100 generic ones [SG75]. Eva's rule: no ACE submission leaves with template text, a product pitch, or no dated next step with a named customer contact. (Sample size not published; treat the distribution as directional.)

2. **Two AWS inboxes, one five-business-day clock.** Since 2026-09-09, a Marketplace "Request private offer" or "Request demo" arrives either as an Opportunity Invitation (Sell > Opportunities > Opportunity Invitations, title "[Company] AWS Marketplace [Request Demo | Request Private Offer]") or, when the buyer gave only contact details, as a Lead Invitation (Sell > Leads > Lead Invitations, Lead Source "AWS Marketplace"). Both expire or must be answered within 5 business days, and AWS expects buyer follow-up in the same window. Contact details appear only after acceptance [SG6] (CONFIRMS [A96][A43]). Name an owner and a backup per queue before turning the buttons on.

3. **Partner-created AWS leads are now a prospecting tool, and enrichment is a separate step.** ACE-eligible partners can import 1 to 100 leads per CSV (or via API) and then ask AWS to enrich them: a readiness call (Contact Ready, Nurture Lead, Limited Potential, each High/Medium/Low confidence), a Marketplace engagement score, a Marketplace solution score, eligibility checks for Partner Greenfield Program, Pioneer Credits and Partner-Led Sales Motion, and firmographics. Lead Prospecting plays only unlock on enriched leads. Error PARTNER_LEAD_CREATION_NOT_ENABLED means AWS must switch it on for your account [SG4]. This is the cheapest way for a Forecastable customer to test which target accounts AWS thinks will buy through Marketplace.

4. **"Deployed on AWS" answers where you run, not whether a buyer's EDP draws down.** AWS's only drawdown wording is that deployed-on-AWS products "typically qualify" and eligibility is "determined separately for each product" [SG5] (CONFIRMS [A60]). The badge requires application and control planes on AWS; third-party services touching buyer data must also run on AWS except CDN, DNS and corporate IdP [SG5]. Our AWS file's twelve-things line "only SaaS hosted entirely on AWS counts" is stronger than any official text (section 7). Advice: get the badge, then get the buyer to confirm drawdown in writing with their AWS account team, per product.

5. **Microsoft channel choice is really a "who pays you" choice.** In a resale enabled offer (REO) Microsoft pays the reseller, the reseller pays the ISV outside Marketplace, the ISV sets no wholesale price in Partner Center, gets no notice of partner-created offers, and sees sales only in Insights under a "Resale partner" filter; the authorization never expires until revoked, and markets can be added but not removed. In an MPO Microsoft pays the ISV, the fee applies only to the ISV's partner price, and the ISV sees each deal [SG29] (CONFIRMS [M36][M39]). Any REO needs a reseller contract covering wholesale price, payment timing, the partner's fee, and a per-offer report.

6. **Most private-offer failures are buyer-side and predictable.** AWS: offers expire at 23:59:59 UTC but can be extended back to Active if only one charge date falls on or before the new expiry; buyer account IDs cannot be changed after release (clone and cancel); "You already have an active contract" means amend with an agreement-based offer carrying pending payments; accept-then-cancel emails mean missing AWSMarketplaceManageSubscriptions permission, a declined card (private offers are typically paid in full at acceptance unless financed) or an unpaid AWS bill, and the buyer can re-accept the same link [SG7]. Google: free-trial billing accounts cannot accept, prepay is unavailable to Brazil billing accounts, and large offers can fail on self-serve/Online billing accounts with no published threshold [SG42]. Eva's pre-flight checklist should ask these before building the offer.

7. **AWS moved several money rules in mid-2026 that most ISVs have not priced in.** Professional services private offers 0.5% (from 2.5%, new offers only, 2026-06-16) [SG19]; CPPO uplift of 0.5% is computed on the ISV's discounted price to the partner [SG18]; seller-set net payment terms on private offers, with an ISV ceiling on CPPO (official docs list Customer default, Net 15, 30, 45, 60, 90, 120; Suger lists only 30 to 90) [SG22][SG86]; self-service refunds and cancellations (2026-03-31), with adjustments on KYC-country invoices needing a KYC-verified secondary user with MFA and, on a CPPO, only the channel partner can adjust [SG2]; pre-authorized auto-renewal for direct contract private offers (GA 2026-09-01) with fixed or ranged uplift [SG85][SG69]. Worked example worth reusing: one $2M private offer costs $40,000 in fees, four $500K offers cost $60,000 [SG18].

8. **AWS is telling partners that data, not relationships, now routes them.** The AWS PDM on Suger's webinar: an internal Solution Matching Engine (replacing the old field "discovery portal") recommends partners to sellers using ACE pipeline, leads, competencies, program status and reviews, and the same data feeds Marketplace agent-mode recommendations; AWS SMB sellers get about 6 new partner-originated opportunities a day and some enterprise sellers hold 100 to 200 live partner opportunities in one account; AWS saw its first purely agent-led Marketplace purchase in mid-2026 [SG75] (NEW, unofficial). Implication for Alex: registering every real deal and closing on Marketplace is now how an ISV gets recommended, even when no human seller engages.

9. **Partner Revenue Measurement ends the "30% of TCV is AWS consumption" era.** The same PDM said AWS historically granted incentives such as ISV Accelerate seller SPIFFs, "30% SaaS revenue recognition" and full EDP burn-down for products not built on AWS, and approved funding largely on partner attestation; PRM exists to measure real consumption and automate funding approvals beyond the top 20 to 30 partners, and 2027 is the year to operationalize attribution with RA IDs [SG75] (NEW, unofficial; our file says credit percentages are not published [A84]). Low-consumption business apps should sell downstream consumption and access to non-IT buyers instead.

10. **Suger is the strongest CRM-agnostic option for HubSpot shops, with limits.** Suger connects Salesforce, HubSpot and Dynamics 365 to AWS ACE, Microsoft Partner Center co-sell and Google Cloud Partner Network, one active configuration per cloud [SG79]; the HubSpot deal card creates private, amendment and reseller offers, co-sell referrals per cloud, and AWS MDF/POC funding requests [SG64][SG68]. But AWS lead creation and enrichment sync reads Salesforce only [SG4], HubSpot funding is AWS only and fails on the legacy S3 integration [SG68], custom object mapping is Salesforce only [SG79], and co-sell and HubSpot need the Growth tier [SG61][SG63]. No list prices are published; pricing is usage-based with no revenue share [SG61].

## 1. Vendor profile (products, clouds, CRM and API coverage, pricing, ownership, strengths, bias)

All VENDOR unless noted.

| Dimension | Detail | Tag |
|---|---|---|
| Company | Founded 2022 by Jon Yoo (CEO) and Chengjun Yuan (CTO); HQ 637 Howard St, San Francisco, second office Vancouver; YC company | [SG65][SG8] |
| Funding and ownership | About $20M raised; investors Y Combinator, Intel Capital, Craft Ventures, Threshold Ventures; a $15M Series A was discussed on a Q1 2025 podcast; independent (no acquisition news, unlike AppDirect acquiring Tackle [X56]) | [SG65][SG78] |
| Scale claims | 300+ software companies; "~$10 billion" processed (press release 2026-09-02); "$6B+" still on the About page; $6B and 17x YoY in September 2025; 52 employees in September 2025 | [SG8][SG65][SG60] |
| Named customers | Intel, Snowflake, Notion, Airtable, Webflow, Glean, ContentSquare, Fivetran, Fireblocks, Aikido Security, NinjaOne, Simpplr, Ona, Securiti AI, Kong, Workday and "the AI labs" (webinar) | [SG60][SG52][SG75][SG76] |
| AWS status | AWS ISV Accelerate member; launch Third Party Integrator (3PI) in AWS's 3PI PDM Pilot for early-stage ISV onboarding (2026-09-02), delivered by a new Cloud GTM Practice led by Juston Salcido; launch partner for AWS Self-Service Cancellations and Billing Adjustments (SCABA) | [SG8][SG72] |
| Marketplaces | AWS, Microsoft, Google Cloud, Snowflake, Alibaba Cloud, Oracle; plus AWS Bedrock, Google Vertex AI and Azure AI Foundry distribution (June 2026) | [SG65][SG70] |
| Products | Cloud GTM platform: listings, private and resale offers, agreements, co-sell, billing and metering, disbursement reconciliation, revenue recognition, reporting, workflows; PRM (launched 2026-06-24: deal registration without portal login, multi-partner attribution, commissions and SPIFFs pushed to AP, white-label portal live in under 5 days with no implementation fee, LMS with SCORM, per-partner pricing); Insulin (general agent platform, private beta Q3 2026); Buyer Service (AWS buyer-side procurement); Chrome extension | [SG61][SG67][SG62] |
| CRM integrations | Salesforce (managed package, widget with Marketplace, Co-Sell, Funding, Insights tabs), HubSpot (deal card with Offers, Entitlements, Co-Sell, Funding, Insights; separate Co-sell Insights company card), Dynamics 365 for co-sell | [SG72][SG68][SG79] |
| HubSpot vs Salesforce gaps | Salesforce only: AWS lead creation/enrichment from Accounts, custom object mapping, predicted AWS account owner on the account record. HubSpot: funding AWS only, REO partner and markets not shown, needs Growth tier | [SG4][SG79][SG71][SG29][SG64] |
| Co-sell API coverage | AWS Partner Central Selling API (API integration, not legacy S3; EventBridge-triggered sync plus about 10-minute polling; leads swept every 3 hours); Microsoft Partner Center referrals including multi-partner Referral Sets (January 2026); Google Cloud Partner Network. One active config per cloud | [SG6][SG74][SG79] |
| Funding automation | AWS fund requests from Salesforce or console: MAP Cash Claim, POC, ISV Workload Migration, MDF, PIF SCA GenAI POC, PIF SCA GenAI MDF, MPOPP Grow; AWS Partner Central agents surfaced in the Salesforce widget | [SG71][SG72] |
| AI and agentic | Remote MCP server at apiv2.suger.cloud/mcp, 163 tools in 17 categories, OAuth 2.1 with PKCE, works with Claude, ChatGPT, Cursor, VS Code, Windsurf, included in Cloud GTM (launched April 2026 with 120+ tools); Co-Sell MCP (June 2026); predicted AWS quality score with ranked fixes; AI-generated Customer Business Problem from CRM fields; predicted AWS/Azure/GCP account owners from a cloud-rep database; Collaboration Score per cloud rep; AI field mapping (Direct, Expression, Default Value, AI Generate) | [SG62][SG70][SG71][SG13] |
| API | REST at api.suger.cloud, OAuth 2.0 client credentials (API keys deprecated), SDKs for Node.js, Python, Go, Java, HMAC-signed webhooks, breaking changes only on a new host with 12 months notice; rate limits not published | [SG66] |
| Pricing | Usage-based, "no rev share". Professional: up to 3 listings, 5 users, private offers, no resale offers, basic CRM, limited API. Growth: unlimited listings, resale offers, all CRM and ERP integrations, co-sell intelligence, SSO, 20 users, 99.9% SLA. Enterprise: AI recommendations, custom reports, dedicated CSM. No dollar amounts published. Buyable on AWS Marketplace | [SG61] | <!-- VALIDATE-OK[economics]: public hyperscaler or vendor reseller economics, not Forecastable's -->
| Implementation claims | Net-new listing about 3 weeks on AWS and Azure, about 4 weeks on Google, about 5 days to migrate an existing listing; "5 to 10 business days" from submission elsewhere | [SG81][SG52] |
| Named-customer results | Fireblocks 3x co-sell volume, 70% less offer time; Securiti AI 40% faster closure in 6 months; Kong: win rate 1.5x and deals 4x larger when AWS influences (customer's own figures, podcast) | [SG63][SG76] |
| Strengths | Most rule-precise public content in the category (dated, sourced, cloud rules separated from Suger rules); broad marketplace coverage; genuine HubSpot and Dynamics support; MCP and funding automation ahead of most peers; honest evaluation framework that admits build-in-house is sometimes right [SG50] |  |
| Weaknesses | Several key features are Salesforce-first; co-sell locked to Growth tier; small YouTube presence (about 50 subscribers); older guides carry stale and wrong program facts; scale claims inconsistent across pages ($6B+ vs about $10B) | [SG65][SG88] |
| Bias to watch | Everything funnels to "reconcile in one system" and "offers from the CRM"; benchmark tables mix vendor-commissioned and unsourced figures; Google drawdown post omits the 25% cap; hyperscaler seller comp described as minimal in February 2026 (contradicts our files). Suger openly states it has not tested Tackle, Clazar or Labra [SG50] | [SG39][SG57] |

## 2. AWS: extracted substance

Status key: CONFIRMS (matches our file), NEW (not in our files), CONFLICT (differs), STALE (describes a retired rule). "Our tag" is from aws-intelligence.md unless noted.

| Fact | Status | Our tag | Vendor tag | Date |
|---|---|---|---|---|
| OQS: lowest-bucket referrals all scored 0; highest bucket 50 to 75; deal size, AWS revenue, industry, region uncorrelated; ~half of zeros had template text, a third no customer context, a third a product pitch (sample size not stated) | NEW | cf. [A87][A88] | [SG13] | 2026-07-29 |
| Suger's predicted-score dimensions include Customer situation (20 pts), Next steps (15), Competition (8); example fixes +25 business problem, +15 dated next step with contact, +8 named competitors | NEW (vendor model) | | [SG13] | 2026-07-29 |
| AWS PDM: score uses a version of MEDDPICC; generic copy-pasted descriptions score low; scoring FAQ released August 2026; engineering prefers 10 quality opps to 100; partner org still goaled on volume | NEW (unofficial) | [A3] | [SG75] | 2026-08 |
| AWS SMB sellers receive about 6 new partner-originated opps per day; enterprise sellers can hold 100 to 200 live partner opps in one account | NEW (unofficial) | | [SG75] | 2026-08 |
| Solution Matching Engine replaces internal discovery portal; fed by ACE data, leads, competencies, programs, reviews; also informs Marketplace agent-mode discovery; first purely agent-led Marketplace purchase mid-2026 | NEW (unofficial) | cf. [A62] | [SG75] | 2026-08 |
| Suger data: 51% of APN launches held by the top 100 partners | NEW (VENDOR) | | [SG75] | 2026-08 |
| Historic incentives included ISV Accelerate seller SPIFFs, "30% SaaS revenue recognition" and full EDP burn-down for non-AWS-built products; funding approvals were attestation based; PRM automates them | NEW (unofficial) | [A84][A12] | [SG75] | 2026-08 |
| Competency bar rising, fewer competencies rolled out; two SCA types (customer SCA, highly negotiated, 1 to 2 years; scale SCA, repeatable) | NEW (unofficial) | cf. [A20] | [SG75] | 2026-08 |
| Private offer/demo requests: agentic evaluation since 2026-09-09; opportunity vs lead routing; titles truncated at 40 chars; 5-business-day windows; buttons appear only after the biweekly ACE status update following enrollment; requires linked accounts incl. CreatePartnerCentralCloudAdminRole; AMI, SaaS, container, CloudFormation; public pricing can be removed | CONFIRMS (detail NEW) | [A96][A43] | [SG6] | 2026-09-19 |
| Lead import 1 to 100 rows per CSV; same-day re-upload creates no duplicates; enrichment is an async task of up to 100 leads; readiness Contact Ready / Nurture Lead / Limited Potential; insights incl. eligibility for Partner Greenfield Program, Pioneer Credits, Partner-Led Sales Motion; only Qualified leads convert | NEW (detail) | [A43][A97] | [SG4] | 2026-09-24 |
| ACE ReviewStatus: Pending Submission, Submitted, In-Review, Action Required, Approved, Disqualified; CreateOpportunity does not submit (associate 1 to 10 solutions, then StartEngagementFromOpportunityTask); Action Required unlocks only 11 fields; watch "Opportunity Updated" EventBridge event | NEW (detail) | [A95][A48] | [SG44] | 2026-08-10 |
| Launched stage means "billing for the solution has begun" | CONFIRMS | [A43] | [SG44] | 2026-08-10 |
| Partner Central migration: 4 steps; linked account becomes primary and pays the APN fee; 2 to 6 hours blocked; S3 CRM integration deprecated and closed to new users, no EOL date; API upgrade needs only account linking; soln- IDs not yet supported by the CRM connector | CONFIRMS | [A8][A9][A47] | [SG12] | 2026-08-24 |
| CRM connector cutover: retire "Sync with AWS"/"Has Updates for AWS", delete old APN scheduled jobs (duplicate opps), backfill Last Modified Date | CONFIRMS | [A47] | [SG12] | 2026-08-24 |
| Software Path is one of five paths (Software, Hardware, Services, Training, Distribution); removing a path requires APN Support | NEW | [A21] | [SG15] | 2026-08-09 |
| FTR via SOC 2 Type II or WAFR (zero high-risk issues in Security, Operational Excellence, Reliability); reports under 1 year old; approval valid 2 years; renew before due date or lose Validated | CONFIRMS (report-age detail NEW) | [A19][A49] | [SG15] | 2026-08-09 |
| Marketplace seller registration does not require APN membership | NEW | | [SG15] | 2026-08-09 |
| Deployed on AWS: both planes on AWS; 3rd-party services handling app data on AWS except CDN, DNS, corporate IdP; agents/gateways off AWS allowed if data goes only to AWS; diagram PNG/JPG, not published; submit via AMMP Build > SaaS > Request changes > Update architecture details; "Succeeded" is not the verdict; no review time published | NEW (detail) | [A38][A49] | [SG5] | 2026-09-19 |
| Drawdown: products deployed on AWS "typically qualify", eligibility per product; AMI/container deployed into the buyer account must be a separate add-on product | CONFIRMS | [A60] | [SG5] | 2026-09-19 |
| Fees: public SaaS 3%, server 20%, ADX 3%; private <$1M 3%, $1M to <$10M 2%, >=$10M 1.5%, renewals 1.5%; CPPO +0.5% on the ISV's discounted price; South Korea +1% additive (4% on a small SaaS PO) | CONFIRMS | [A24] | [SG18] | 2026-08-06 |
| Professional services 0.5% (from 2.5%), new offers only, existing subscriptions keep 2.5%; 0% in qualifying multi-product offer set | CONFIRMS | [A28][A29] | [SG19][SG52] | 2026-08-18 |
| Net payment terms seller-set per private offer, one term for all charges, buyer sees it pre-acceptance, CPPO ceiling set by ISV | CONFIRMS | [A55] | [SG22] | 2026-08-19 |
| Net payment term options are Net 30/45/60/90 only | CONFLICT | [A55] | [SG22] | 2026-08-19 |
| Express private offers: SaaS contract and contract-with-consumption only; dimension descriptions >= 250 characters; rate cards dimension-, TCV- or buyer-profile-based; global max TCV guardrail; "Get Express Private Offer" button | CONFIRMS (detail NEW) | [A54] | [SG20] | 2026-08-05 |
| Concurrent Agreements: PS on by default 2026-02-26; SaaS default after 2026-06-01; older SaaS opt in via Contact Us > Concurrent Agreements Support and must justify not relisting; no deadline; SNS to EventBridge; LicenseArn in ResolveCustomer/GetEntitlements/BatchMeterUsage; ProductCode + LicenseArn same customer same hour bills twice; 1 hour to report final usage after License Deprovisioned (2026-09-11); container products break metering on opt-in (Suger docs) | CONFIRMS (detail NEW) | [A101] | [SG3] | 2026-09-24 |
| KYC: AWS EMEA SARL invoices EMEA buyers only after seller KYC; CPPO needs both parties KYC-verified or AWS Inc. invoices; Turkey and South Africa always AWS Inc.; business verification ~24h, bank verification 1 to 5 business days, secondary users ~24h; UK bank account requires KYC; two disbursements (EMEA SARL and AWS Inc.) | NEW (detail) | [A51][A56] | [SG2][SG28] | 2026-09-24 |
| AWS EMEA SARL excludes professional services purchases | CONFLICT | [A119] | [SG2] | 2026-09-24 |
| Self-service refunds and cancellations (What's New 2026-03-31); KYC only triggered for invoices needing compliance validation; adjustments on KYC-country invoices need a KYC-verified secondary user with MFA; CPPO adjustments only by the channel partner; irreversible; billing adjustments process in 5 to 10 minutes; buyer has 7 days to deny a cancellation before auto-approval | NEW | | [SG2][SG72] | 2026-03 to 2026-09 |
| Private offer errors: expiry 23:59:59 UTC; extend expired offers back to Active if only one charge date on or before expiry; buyer accounts fixed at release; linked accounts judged by own Tax Address location; accept-then-cancel causes; AWSMarketplaceRead-only cannot subscribe | NEW | | [SG7] | 2026-09-19 |
| Pre-authorized auto-renewal for direct contract private offers (GA 2026-09-01): no change, fixed change or ranged uplift; either party can opt out before the renewal decision deadline; POs can map to renewals | NEW (verified official) | | [SG85][SG69] | 2026-09-01 |
| Multi-currency private offers (EUR, GBP, AUD, JPY; INR for India sellers) for contract, CCP and PAYG since 2025-10-07; containers contract-only; US ACH and Hyperwallet receive USD only; non-USD needs SWIFT | NEW | cf. [A56] | [SG28] | 2025-04, updated 2026-09-19 |
| Commerce surfaces: Buy with AWS (Dec 2024), Discovery API read-only (2026-04-09; us-east-1, us-west-2, eu-west-1), Agreements API (2026-05-06, us-east-1), Storefront GA 2026-06-16 with Salesforce and HubSpot connectivity | CONFIRMS | [A99][A118] | [SG25] | 2026-08-24 |
| Vendor Insights automated (Audit Manager) assessments no longer available to new sellers; Audit Manager maintenance mode 2026-04-30 | CONFLICT (our file STALE) | [A59] | [SG26] | 2026-08-20 |
| AI Agents & Tools category: 1 to 3 categories with at least one from AI Agents & Tools; attest reasoning models and autonomous capability; API or container deployment; pricing model frozen at Limited | NEW (detail) | [A62] | [SG27] | 2026-08-12 |
| Managed entitlements: subscription belongs to buying account; enable subscription sharing, create License Manager grants, recipients accept/activate; Bedrock entitlement setup in us-east-1 | NEW | | [SG10] | 2026-08-27 |
| Purchase orders: buyer sets PO at acceptance (up to 200 chars, per charge); management account can make PO mandatory; auto-renewal carries PO | NEW | | [SG47] | 2026-09-19 |
| Usage records cannot be negative or amended; window under 24h, previous month until 06:00 UTC on the 1st; AWS may refund metering errors itself | NEW | | [SG46] | 2026-09-24 |
| Retiring a SaaS listing: Restricted keeps subscribers until contract end; visibility change up to 37 days with a 24h cancel window; replacement must be an existing Limited/Public product; AMI removal requires 90 days support | NEW | | [SG48] | 2026-09-24 |
| Annual price changes on server products every 90 days with 90 days notice; reach auto-renewal only if changed 90+ days before | NEW | | [SG82] | 2026-08-12 |
| Disbursement default monthly 7th to 10th, daily option; ACH 1 to 3 business days to land | CONFIRMS (detail) | [A56] | [SG80] | 2026-08-19 |
| Competency benefits per AWS: badges, priority PSF placement, improved co-sell score, AWS Sales access, MDF and MAP eligibility; no cost or timeline published; Service Delivery and Service Ready deprecated 2027-06-01 | CONFIRMS | [A20] | [SG24] | 2026-08-19 |
| Funding programs in Suger: MAP Cash Claim, POC, ISV WMP, MDF, PIF SCA GenAI POC, PIF SCA GenAI MDF, MPOPP Grow | NEW (names) | [A7][A31] | [SG71][SG72] | 2026-03 to 2026-04 |
| List and Sell $10K credits (qualify $65K TCV or 10 private offers in 12 months; PLG $5,500 revenue or 10 active monthly subs); Seller Prime up to $40K reimbursable marketing funds; ACE-CRM Integration Credits $10K | CONFIRMS (VENDOR only, still unverified officially) | [A25][A86] | [SG52] | 2026-04 |
| ACE entry criteria "Advanced tier APN + active marketplace listing" | STALE | [A1] | [SG49] | 2026-04 |
| "AWS 3% base, up to 5% on some categories; ISV Accelerate qualifying deals drop to 1.5%" | STALE / CONFLICT | [A24] | [SG56] | 2026-04 |
| AWS Marketplace listings from 6,000+ unique ISVs and 4,000 channel partners | NEW | | [SG8] | 2026-09-02 |
| re:Invent 2026 Nov 30 to Dec 4, Las Vegas | CONFIRMS | | [SG9] | 2026-08-27 |

## 3. Microsoft: extracted substance

| Fact | Status | Our tag | Vendor tag | Date |
|---|---|---|---|---|
| IP co-sell deal registration: won, eligible solution, partner-led or co-sell, Microsoft accepted, >= USD 25,000 (Reuters monthly rate), Microsoft-managed account; 72h gap before Won; terminal states immutable | CONFIRMS | [M6] | [SG1][SG44] | 2026-08-18 |
| Six deal types (IP co-sell, Services co-sell, P2P, Solution assessments, Partner-led, Private), set by two form questions; answering no to both creates a private deal no seller sees | CONFIRMS (detail) | [M7] | [SG44] | 2026-08-10 |
| Account search tabs Microsoft Managed / Unmanaged / Other (Moody's); wrong tab can only be changed via support | CONFIRMS | [M7] | [SG1][SG44] | 2026-08-18 |
| Microsoft sellers have 14 days to decide; inbound opps expire on the same clock; stages 10/20/40/60/80/100% | CONFIRMS | [M7] | [SG44] | 2026-08-10 |
| FY27: PRACR no longer a broad co-sell mechanism; credit via Marketplace Billed Sales; Frontier Accelerate for Marketplace consolidates ISV Success, Marketplace Rewards, Azure IP co-sell, CSD | CONFIRMS | [M13][M30] | [SG1][SG34] | 2026-08-18 |
| Commercial Cloud local-currency pricing updates annually every January from FY27 | NEW | | [SG34] | 2026-08-18 |
| REO: SaaS, VM software reservations, Dragon Copilot; excluded markets Belarus, Brazil, China, India, Mexico, Russia, Singapore, South Korea; Microsoft pays partner, partner pays ISV outside Marketplace; no wholesale price field; no notice; Insights "Resale partner" filter only; no expiry until revoked; markets added not removed; revoking stops only new offers; 100% MACC if co-sell eligible | CONFIRMS (detail NEW) | [M36][M37] | [SG29] | 2026-09-19 |
| MPO in 36 markets (Australia, Japan, South Africa announced 2026-07-16); fee only on ISV's partner price | CONFIRMS | [M38][M39] | [SG29] | 2026-09-19 |
| CSP private offers: margin off list for up to 50 CSP tenants, month-end end date, ISV paid wholesale less agency fee, no MACC | CONFIRMS | [M40] | [SG29] | 2026-09-19 | <!-- VALIDATE-OK[economics]: public hyperscaler or vendor reseller economics, not Forecastable's -->
| Updated MPA and CSP Program Guide effective 2026-12-01 automatically; CSP direct bill and distributor partners in France must accept 2026-12-01 to 2027-02-28; 180 days notice; Global admin only; check Settings > Account settings > Agreements ("N/A" means nothing pending) | CONFIRMS (France window NEW) | [M17] | [SG30] | 2026-08-30 |
| Request private offer toggle (2026-07-20) for SaaS, Azure app, container, VM; lands as a Marketplace lead in the referrals workspace | CONFIRMS | [M13] | [SG31] | 2026-08-24 |
| Custom contract lengths 1 to 120 months for SaaS and PS private offers (GA 2026-07-06); annual billing only if months divisible by 12; accepted offers cannot be edited self-serve | CONFIRMS (billing rule NEW) | [M34] | [SG32] | 2026-08-24 |
| SaaS auto-renew off by default (customer chooses); renew into private vs public offer; public fallback term mandatory; flexible-schedule offers cannot renew into private term; renewal fee attestation only at creation, 50% store fee | CONFIRMS (detail NEW) | [M42] | [SG33] | 2026-08-18 |
| 141 geographies with fixed currencies; USD converted once at first save then static; export/import pricing sheet; price increases take at least 90 days; hidden or government-cloud plans cannot be repriced | NEW (detail) | [M33] | [SG36] | 2026-08-19 |
| Private plan is tenant-ID scoped; private offer billing-account scoped; only private offers accept a contract PDF; no private plans for consulting, "Contact me" or free offers | NEW | | [SG37] | 2026-08-06 |
| Metered billing: one event per resource/dimension/hour (409 on duplicate), past 24h only, quantity must be > 0, send only usage above base fee; "Refunds aren't granted for metered usage" | NEW | | [SG46] | 2026-09-24 |
| Stop distribution of a SaaS offer: gone within hours, customers keep using and can renew; VM offer deprecation scheduled 90 days out; removing access needs customer consent and refund amount | NEW | | [SG48] | 2026-09-24 |
| PO mapping in Azure portal announced to partners 2026-09-01, still "gradually rolling out" per customer docs (updated 2026-08-06); needs publisher ID and offer ID; reapply reaches back 3 months | CONFLICT (minor, GA status) | [M15] | [SG47] | 2026-09-19 |
| AI Apps and Agents is a first-class offer type; SaaS pricing model (flat rate or per user) frozen at publish | CONFIRMS | [M34] | [SG27] | 2026-08-12 |
| Multi-partner Azure referrals via a Microsoft Referral Set (each invited partner gets its own copy) | NEW | cf. [M7] | [SG74] | 2026-01-26 |
| IP Co-Sell Ready requires "at least one successful marketplace transaction" and "regional availability" | CONFLICT | [M1] | [SG51] | 2026-04 |
| Azure private offer contract duration "up to 3 years" | STALE | [M34] | [SG51] | 2026-04 |
| Azure Marketplace and AppSource described as separate storefronts | STALE | [M73] | [SG51] | 2026-04 |
| Listing 3 to 6 weeks manual; MACC "typically 3 years"; marketplace skips "4 to 8 weeks" of vendor onboarding | NEW (unsourced) | | [SG51][SG54] | 2026-04 |
| Ignite 2026 is Nov 17 to 20 | CONFIRMS | | [SG34] | 2026-08-18 |

## 4. Google Cloud: extracted substance

| Fact | Status | Our tag | Vendor tag | Date |
|---|---|---|---|---|
| Partner Network tiers Select, Premier, Diamond; competencies at Competency and Advanced Competency levels, independent of tier; thresholds not published | CONFIRMS | [G1][G2][G66] | [SG40] | 2026-08-20 |
| Selling on Marketplace requires Partner Network good standing, vendor account and payment profile, no minimum tier | CONFIRMS | [G16] | [SG40][SG41] | 2026-08-20 |
| Google publishes no partner-facing co-sell opportunity lifecycle; the private offer carries the deal | CONFIRMS | [X22][X24] | [SG44] | 2026-08-10 |
| SaaS listing needs approved Product details, Pricing and Technical integration reviews; product types include AI agents | CONFIRMS | [G7] | [SG41] | 2026-08-20 |
| Drawdown works across CUDs, usage-based discounts and provisioned throughput; multi-year upfront deals draw down annually amortized; spend-based CUDs sit at billing-account level and cannot be cancelled | CONFIRMS | [G26] | [SG39] | 2026-08-20 |
| Drawdown post omits the 25% cap and the exclusions list | CONFLICT (omission) | [G22][G23] | [SG39] | 2026-08-20 |
| MCPO 100% drawdown capped at 25% of commitment "since June 9, 2025" | CONFIRMS (date differs by a day) | [G22] | [SG53] | 2026-06-30 |
| Private offers cannot be accepted on free-trial billing accounts; hidden listings cannot carry offers; SaaS entitlements required; prepay unavailable to Brazil billing accounts; large offers can fail on self-serve/Online accounts with no threshold published; custom EULA needs Commerce Price Management Private Offers Admin | NEW (free trial, self-serve) / CONFIRMS (roles, Brazil) | [G27][G28] | [SG42] | 2026-08-06 |
| Reselling must be turned on for all Marketplace products (may need a vendor agreement amendment); allowed-resellers list separate; single-use plan targets customer billing subaccount, multi-use targets reseller main billing account; statuses draft, ready to accept, accepted, ready to use, used, expired/completed/rejected | NEW (all-products rule, statuses) / CONFIRMS (plan types) | [G34] | [SG43] | 2026-08-06 |
| No incremental ISV fee on MCPO | CONFIRMS | [G67] | [SG53] | 2026-06-30 |
| Fees 3% (public and new private <$1M), 2% ($1M to <$10M), 1.5% (>= $10M, renewals, migrations, channel shifts) | CONFIRMS | [G18][G21] | [SG53] | 2026-06-30 |
| MCCP "caps at approximately $8.3M annualized GTV in credits per eligible ISV" | CONFLICT | [G45] | [SG53] | 2026-06-30 |
| Hosting requirement accepts "six architecture patterns" | CONFLICT | [G17] | [SG53] | 2026-06-30 |
| "$240B committed-spend backlog" | STALE | [G8][G65] | [SG53] | 2026-06-30 |
| "ISVs enroll under the Build engagement model" | STALE | [G1][G3] | [SG53] | 2026-06-30 |
| ACE-style entry criteria "Build or Premier tier + marketplace listing" | STALE | [G1] | [SG49] | 2026-04 |
| Payouts on the 21st of the following month, 45 to 60 days after customer billing | CONFIRMS | [G24] | [SG53][SG56] | 2026-06-30 |
| Listing timeline 8 to 16 weeks; pricing review up to 4 business days; some component reviews up to 2 weeks; MVA 1 to 4 weeks | NEW (VENDOR estimate) | | [SG53] | 2026-06-30 |
| Usage within 1 hour; month-end usage by 1 AM Pacific next day; refunds via Partner Support Desk, offset against future payments | NEW | | [SG46] | 2026-09-24 |
| PO number is per invoiced Cloud Billing account (not per purchase); moving an active order to another billing account is an entitlement transfer, not guaranteed, a week or more; split invoicing for agency-model transactions (Australia added 2026-08-01) | NEW | | [SG47] | 2026-09-19 |
| Deprecation date at least 180 days out; review up to 5 business days; listing permanently deleted; SaaS plan deletable only with no entitlements ever | NEW | | [SG48] | 2026-09-24 |
| Futurum (Google-commissioned, June 2025): see section 6 | NEW | | [SG53] | 2026-06-30 |
| Google sellers get quota attainment on most Marketplace deals plus SPIFFs on co-sell | CONFIRMS | [G71] | [SG53] | 2026-06-30 |

## 5. Cross-cloud playbooks and benchmarks worth reusing

1. **Referral quality gate (Eva, every submission).** Customer named; business problem in the customer's words, about the customer not the product; one concrete ask of the cloud; dated next step with a named customer contact; competitors named; no template text. Suger's scoring shows the gate, not deal size, decides the AWS motion [SG13][SG75]. Event variant: capture name, problem in their words and agreed next step the same day; submit within one week [SG11].
2. **Own-ID discipline.** Populate AWS PartnerOpportunityIdentifier and Microsoft's CRM ID on every record; never map one generic "Closed Won" to both clouds because AWS Launched means billing started and Microsoft Won is terminal and gates registration [SG44].
3. **Inbound SLA.** One named owner plus backup per queue (AWS Opportunity Invitations, AWS Lead Invitations, Microsoft Marketplace leads); accept and route on day one, reach the buyer before day five [SG6][SG31]. Suger's own guide target: respond to cloud-rep referrals within 24 hours [SG49].
4. **Pre-flight before any private offer.** Buyer account/billing ID in writing; account location and invoicing entity (AWS KYC tab, Google billing account type and free-trial status); buyer permissions (AWS AWSMarketplaceManageSubscriptions); payment by invoice or card; PO process and who raises it; renewal attestation checkbox on Microsoft; expiry and first charge dates [SG7][SG42][SG2][SG47][SG33].
5. **Fee modeling.** Model the software and services lines separately (AWS PS 0.5%); consolidate into one contract to hit lower TCV tiers; price CPPO margin on the ISV's discounted price; add the regional fee; treat discount, channel margin and disbursement lag as larger costs than the fee [SG18][SG19]. <!-- VALIDATE-OK[economics]: public hyperscaler or vendor reseller economics, not Forecastable's -->
6. **Renewal calendar.** AWS renewal milestones at T-120, T-90, T-60, T-45, T-30 days [SG90]; Microsoft renewal behavior is fixed at offer creation (auto-renew off by default, public fallback mandatory) [SG33]; AWS pre-authorized auto-renewal now removes re-papering for direct contract offers [SG85].
7. **SCA as a management system.** Decompose every SCA commitment into a record a system emits (ACE referrals accepted, opps with an AWS seller, agreements and disbursements, funding claims, certifications); agree in writing whether revenue means bookings, billed or disbursed; review monthly, not only quarterly [SG23]. The AWS PDM view: an SCA accelerates a motion that already works and does not create one [SG75].
8. **Three metrics AWS scores a partner on.** Kong's cloud alliances lead: the ISV's own AWS consumption, pipeline TCV shared and launched, and Marketplace gross sales; share renewals too, because an unshared renewal looks like new business for a competitor [SG76].
9. **CFO expectation setting.** Expected AWS-sourced new business in year one is "probably zero", with a 2 to 3 year payoff; pitch instead win-rate and deal-size lift on AWS-influenced deals, local-currency and in-country transacting via partners, and flexible payment schedules. "Co-sell is free. Marketplace is 3%." [SG76].
10. **Internal enablement first.** Lead the first co-sold deal personally to create one believing AE; repeat the story about seven times; hire a partner engineer to build first-party integrations and a reference architecture that feeds product and field marketing [SG77].
11. **Comp neutrality, then comp positive.** Reps paid the same on marketplace deals; some teams pay 1.1x to 1.25x for 2 to 4 quarters; start with renewals of customers who have commitments (3 to 5 renewal wins before net-new) [SG55][SG58].
12. **Business-app ISVs with low consumption.** Sell downstream consumption and the relationships you hold with non-IT buyers the cloud field lacks; expect influence, not sourced pipeline [SG75].
13. **Usage over-report playbook.** Stop the emitter, size from what the marketplace accepted per buyer/dimension/hour, tell the buyer before the invoice, use one remedy: usage credit before invoicing; after invoicing AWS billing adjustment, Microsoft support ticket (no refunds on metered usage), Google refund request [SG46].
14. **Retiring a listing.** Set the date from the longest applicable clock (Google 180 days minimum, Microsoft VM 90 days, AWS visibility change up to 37 days) against contract end dates; stand up the replacement first [SG48].
15. **Tooling decision (for Alex).** One cloud and under about 10 offers a year: start in the consoles. Two or more clouds, usage pricing or a resale motion: buy. Ask every vendor for a live listing they created, the field-level CRM mapping, metering retry behavior and a reconciliation export checked against a real disbursement; model platform cost at 3x current volume because percentage-of-GMV pricing scales against you [SG50].

## 6. Survey and benchmark data

| Figure | Sample / basis | Date | Label |
|---|---|---|---|
| OQS: lowest bucket all 0; highest 50 to 75; ~50% of zeros had template text | Suger analysis of referrals, n not published | 2026-07-29 | VENDOR [SG13] |
| 51% of APN launches held by top 100 partners | Suger slide, basis not published | 2026-08 | VENDOR [SG75] |
| AWS SMB sellers ~6 partner-originated opps per day; enterprise sellers 100 to 200 live partner opps in one account | One AWS PDM, anecdotal | 2026-08 | VENDOR-hosted, unofficial [SG75] |
| AWS Marketplace: 6,000+ unique ISVs, 4,000 channel partners listed | Suger press release | 2026-09-02 | VENDOR [SG8] |
| Suger volume ~$10B processed; $6B with 17x YoY a year earlier | Suger | 2026-09 / 2025-09 | VENDOR [SG8][SG60] |
| Win rate 1.5x and deal size 4x on AWS-influenced deals | Kong, one company | ~2026-04 | VENDOR-hosted [SG76] |
| Futurum "Scaling Smarter": 100% of ISVs say Marketplace shortens cycles; 2 to 4 weeks compression; deal size +112%; 70% report more multi-year deals; 90% grew Marketplace revenue in 2024 (65% high double digit); retention +14% | Google-commissioned study as cited by Suger | 2025-06 | INDEPENDENT, commissioned, via VENDOR [SG53] |
| Google channel GTV +170% 2023 to 2024 | As cited by Suger | 2025 | VENDOR citing Google [SG53] |
| Marketplace sales $30B (2024) to $163B (2030), 29.1% CAGR; agentic AI $24.4B; ~$470B committed cloud spend | Omdia as cited by Suger | 2025-10 | INDEPENDENT via VENDOR [SG52][SG84] (CONFIRMS [X40]) |
| 27% to 50% faster close (Forrester); 65% higher close rate and 51% higher revenue growth with co-sell (Canalys 2024); up to 140% larger deals (CrowdStrike); 5x higher average subscription price (AppDynamics); CrowdStrike $1B+ transacted on AWS Marketplace | Suger compilation, secondary citations | 2026-02 to 2026-05 | VENDOR citing third parties [SG55][SG58] |
| 64% of ISVs comp neutral, up from 54% | Tackle 2024 as cited by Suger | 2024 | VENDOR citing VENDOR [SG55] |
| "62% say marketplaces are their largest source of net-new revenue" and elsewhere "62% say co-sell is their largest source" | Partner Insight 2025 as cited by Suger | 2025 | VENDOR, misquoted (section 7) [SG55][SG58] |
| ~85% of enterprise marketplace ARR via private offers | Partner Insight 2025 as cited by Suger | 2025 | VENDOR, unverified [SG55] |
| 58% of companies say sales teams are unwilling or unprepared for marketplace deals | Source not named | 2026-02 | VENDOR, unsourced [SG58] |
| Marketplace share of revenue 5% to 10% early, 20% to 30%+ mature; offer acceptance 3 to 7 days; co-sell win-rate lift 50% to 70% (below 20% signals a referral-only motion); org redesign at $10M to $25M marketplace ARR (Bessemer); offers expire 60 to 180 days | Suger guides, mostly unsourced | 2026-04 to 2026-05 | VENDOR [SG54][SG55] |
| Targets: partner-sourced pipeline 20% to 30% at scale; co-sell win-rate lift 40% to 60%; cycle 30% to 40% faster; manual ops break at ~15% of ARR | Suger blog, unsourced; conflicts with the 50% to 70% lift above | 2026-02 | VENDOR [SG57] |
| Co-sell pipeline appears in 3 to 6 months; ops pain at 15 to 20 active deals; ISVs without co-sell discipline leave 30% to 50% of marketplace pipeline | Suger guide, unsourced | 2026-04 | VENDOR [SG49] |
| Confluent ran 40% to 50% of revenue through hyperscaler marketplaces | Podcast anecdote | 2025-Q1 | VENDOR-hosted [SG78] |

## 7. Conflicts with our intelligence files

| Topic | Suger says | Our file says | Which wins and why |
|---|---|---|---|
| AWS net payment terms | Net 30, 45, 60, 90 (launch 2026-08-06) [SG22] | Customer default, Net 15, 30, 45, 60, 90, 120 [A55] | Ours. Re-fetched the AWS docs page on 2026-09-26: options are Customer's AWS default, Net 15, 30, 45, 60, 90, 120; not available for ADX, AWS 1P/2P or Bedrock [SG86]. |
| AWS EMEA SARL and professional services | "AWS also excludes purchases of professional services from AWS EMEA SARL" [SG2], citing the AWS Europe FAQ | Localized billing for professional services from AWS EMEA with SEPA (What's New 2026-02-03) [A119] | Ours: dated official announcement is newer than the FAQ line Suger quoted. Flag to re-check the AWS Europe FAQ at next refresh. |
| Vendor Insights | Automated Audit Manager assessments no longer available to new sellers (maintenance mode 2026-04-30) [SG26] | Lists live Audit Manager / Config evidence as a source [A59] | Suger, which quotes the current AWS docs. Our AWS file should be patched. |
| Deployed on AWS and EDP drawdown | Badge is evidence, not the answer; AWS only says "typically qualify", per product [SG5] | Twelve-things line 8: "only SaaS hosted entirely on AWS counts toward EDP/PPA" (INDEPENDENT/VENDOR sourced) [A38][A39] | Suger is closer to the official text [A60]. Soften our line to "typically qualify, per product; confirm per buyer". |
| Google MCCP cap | "caps at approximately $8.3M annualized GTV in credits per eligible ISV" [SG53] | Max USD 250K credit per transaction [G45] | Ours. The official brief says the $250K per-transaction maximum "is achieved at $8.3M annualized gross transaction value" [SG87]; $8.3M is not a per-ISV cap. |
| Google hosting patterns | Six accepted architecture patterns [SG53] | Nine approved hosting patterns [G17] | Ours (official page); Suger's June guide predates the agent patterns. |
| Google backlog | $240B [SG53] | $460B+ (April 2026), $514B after Q2 2026 [G8][G65] | Ours; Suger figure is stale. |
| Google program language | "Build engagement model", "Build or Premier tier" [SG53][SG49] | Engagement models and Partner Advantage retired 2026-01-15 [G1] | Ours; Suger's own August posts use current terms [SG40]. |
| Google drawdown cap | Drawdown post states no cap or exclusions [SG39] | 25% cap per commitment, exclusions list [G22][G23] | Ours (official). Suger's guide does state the 25% cap for MCPO [SG53], so the omission is inconsistency, not disagreement. |
| Azure IP co-sell eligibility | Requires "at least one successful marketplace transaction" and "regional availability" [SG51] | USD 100K TTM ACR or MBS, technical validation, RAD, transactable offer [M1] | Ours (official). Suger's August post uses the correct co-sell-ready gate [SG1]. |
| Azure private offer term | "Contract duration up to 3 years" [SG51] | 1 to 120 months [M34] | Ours; Suger's own August post agrees with ours [SG32]. |
| AWS fee structure in billing guide | "3% base, up to 5% on some categories; ISV Accelerate qualifying deals drop to 1.5%" [SG56] | TCV-tiered schedule, 20% server, CPPO +0.5% [A24] | Ours; Suger's later posts agree with ours [SG18]. |
| AWS ACE eligibility | "Advanced tier APN + active marketplace listing" [SG49] | Tiers retired; ACE eligibility and ISVA criteria as in [A1] | Ours. |
| Hyperscaler seller comp | AWS AEs earn "minimal compensation on marketplace... maybe a small SPIFF" (February 2026) [SG57] | SaaS Co-Sell Benefit quota retirement for ISVA partners [A79]; MBS co-sell credit [M13]; Google quota eligibility [G71] | Ours (official program pages). Suger's own co-sell guide says the opposite of its February post [SG49]. |
| Partner Insight 2025 "62%" | "Largest source of net-new revenue" and, in another guide, "co-sell is their largest source of net-new revenue" [SG55] | "62% report net-new revenue" via marketplaces [X44] | Ours (closer to the report); Suger overstates the statistic two different ways. |
| Microsoft PO mapping status | Rolling out, GA "expected soon" (customer doc updated 2026-08-06) [SG47] | GA September 2026 [M15] | Unresolved; both cite Microsoft. Treat as "announced 2026-09-01, may not be live in every buyer tenant". |
| Google MCPO drawdown start date | June 9, 2025 [SG53] | 2025-06-08 [G22] | Immaterial; keep ours. |
| Committed-spend total | $348B in one guide, $470B in others [SG55][SG84] | ~$470B (Omdia) [X40] | Ours; Suger internal inconsistency. |

## 8. Content inventory

Items published 2025-07-01 to 2026-09-24 from https://www.suger.io/sitemap-0.xml (publish dates from each page's datePublished). Rating: 3 = rule or number dense and read in full or scanned for rules; 2 = operational but generic or not read in full; 1 = product marketing, case study or company news. Guides with no author carry the guide's own publish date.

| Date | Type | Title | Cloud | URL | Substance |
|---|---|---|---|---|---|
| 2026-09-24 | blog | Upgrading to AWS Marketplace Concurrent Agreements | AWS | https://www.suger.io/resources/blog/aws-marketplace-concurrent-agreements-opt-in-or-relist/ | 3 |
| 2026-09-24 | blog | Retire a Marketplace Listing: What Buyers Keep | Cross-cloud | https://www.suger.io/resources/blog/retire-marketplace-listing/ | 3 |
| 2026-09-24 | blog | Marketplace Usage Correction: What Each Cloud Allows | Cross-cloud | https://www.suger.io/resources/blog/marketplace-usage-correction/ | 3 |
| 2026-09-24 | blog | AWS Partner Central Leads from Salesforce Accounts | AWS | https://www.suger.io/resources/blog/aws-partner-central-leads-from-salesforce/ | 3 |
| 2026-09-24 | blog | AWS EMEA SARL and Seller KYC on AWS Marketplace | AWS | https://www.suger.io/resources/blog/aws-emea-sarl-marketplace-kyc/ | 3 |
| 2026-09-19 | blog | Microsoft Resale Enabled Offers vs MPO: Who Pays You | Microsoft | https://www.suger.io/resources/blog/microsoft-resale-enabled-offers-vs-mpo/ | 3 |
| 2026-09-19 | blog | Deployed on AWS Badge: How to Qualify and Submit | AWS | https://www.suger.io/resources/blog/deployed-on-aws-badge/ | 3 |
| 2026-09-19 | blog | Cloud Marketplace Purchase Orders: Who Sets the PO | Cross-cloud | https://www.suger.io/resources/blog/purchase-order-numbers-on-cloud-marketplaces/ | 3 |
| 2026-09-19 | blog | AWS Private Offer Errors: Why a Buyer Can't Accept | AWS | https://www.suger.io/resources/blog/buyer-cannot-accept-aws-private-offer/ | 3 |
| 2026-09-19 | blog | AWS Marketplace Request Private Offer: Who Answers? | AWS | https://www.suger.io/resources/blog/aws-marketplace-private-offer-requests/ | 3 |
| 2026-09-13 | blog | What Syncs to HubSpot from Your Marketplace Deals | Cross-cloud | https://www.suger.io/resources/blog/marketplace-data-in-hubspot/ | 2 |
| 2026-09-13 | blog | Sync Partners From Salesforce Into a Partner Program | Cross-cloud | https://www.suger.io/resources/blog/partners-already-in-salesforce/ | 2 |
| 2026-09-13 | blog | Partner Discovery: Start With Data You Already Have | Cross-cloud | https://www.suger.io/resources/blog/finding-partners-you-already-have/ | 2 |
| 2026-09-13 | blog | Partner Commission Types: Which One Fits Which Deal | Cross-cloud | https://www.suger.io/resources/blog/partner-commission-plans/ | 2 |
| 2026-09-13 | blog | Partner Certifications: Validity and Renewal Rules | Cross-cloud | https://www.suger.io/resources/blog/partner-certifications-that-expire/ | 2 |
| 2026-09-02 | blog | Suger Joins AWS 3PI PDM Pilot for ISV Onboarding | AWS | https://www.suger.io/resources/blog/suger-selected-aws-3pi-pdm-pilot/ | 1 |
| 2026-08-30 | blog | The Updated Microsoft Partner Agreement, Explained | Microsoft | https://www.suger.io/resources/blog/updated-microsoft-partner-agreement/ | 3 |
| 2026-08-27 | blog | Turning re:Invent Conversations Into ACE Referrals | AWS | https://www.suger.io/resources/blog/reinvent-conversations-to-ace-referrals/ | 2 |
| 2026-08-27 | blog | Planning Your 2027 Cloud GTM Strategy: A Framework | Cross-cloud | https://www.suger.io/resources/blog/planning-your-2027-cloud-gtm-strategy/ | 2 |
| 2026-08-27 | blog | Instrumenting Your Marketplace Motion for 2027 | Cross-cloud | https://www.suger.io/resources/blog/instrumenting-your-marketplace-motion-for-2027/ | 2 |
| 2026-08-27 | blog | Getting Your Listing Ready for Event Traffic | Cross-cloud | https://www.suger.io/resources/blog/listing-ready-for-event-traffic/ | 2 |
| 2026-08-27 | blog | AWS re:Invent 2026: A Marketplace Prep Checklist | AWS | https://www.suger.io/resources/blog/aws-reinvent-2026-marketplace-prep/ | 2 |
| 2026-08-27 | blog | AWS Managed Entitlements for Foundation Models | Cross-cloud | https://www.suger.io/resources/blog/managed-entitlements-for-foundation-models/ | 3 |
| 2026-08-24 | blog | Your Year-End Marketplace Reporting Checklist | Cross-cloud | https://www.suger.io/resources/blog/year-end-marketplace-reporting-checklist/ | 2 |
| 2026-08-24 | blog | Setting Cloud Marketplace Targets You Can Defend | Cross-cloud | https://www.suger.io/resources/blog/setting-cloud-marketplace-targets/ | 2 |
| 2026-08-24 | blog | Security Questions Buyers Ask About Your Ops | Cross-cloud | https://www.suger.io/resources/blog/security-questions-buyers-ask/ | 2 |
| 2026-08-24 | blog | Migrating to the New AWS Partner Central (ACE) | AWS | https://www.suger.io/resources/blog/migrating-to-aws-partner-central/ | 3 |
| 2026-08-24 | blog | Microsoft Marketplace Request Private Offer | Microsoft | https://www.suger.io/resources/blog/microsoft-marketplace-request-private-offer/ | 3 |
| 2026-08-24 | blog | Microsoft Marketplace Custom Contract Lengths | Microsoft | https://www.suger.io/resources/blog/microsoft-marketplace-custom-contract-lengths/ | 3 |
| 2026-08-24 | blog | How to Cut Security Questionnaire Cycle Time | Cross-cloud | https://www.suger.io/resources/blog/cutting-security-questionnaire-cycles/ | 2 |
| 2026-08-24 | blog | Closing Cloud Marketplace Deals Before Year-End | Cross-cloud | https://www.suger.io/resources/blog/closing-marketplace-deals-before-year-end/ | 2 |
| 2026-08-24 | blog | Alibaba Marketplace: Private Offers vs Promotions | Other marketplaces | https://www.suger.io/resources/blog/alibaba-marketplace-private-offers-vs-promotions/ | 2 |
| 2026-08-24 | blog | AWS Marketplace Storefront vs Buy with AWS | AWS | https://www.suger.io/resources/blog/aws-marketplace-storefront-vs-buy-with-aws/ | 3 |
| 2026-08-21 | guide | Multi-Channel SaaS Monetization: A Playbook | Cross-cloud | https://www.suger.io/resources/guides/multi-channel-saas-monetization/ | 2 |
| 2026-08-21 | guide | How to Sell on Snowflake Marketplace: ISV Guide | Other marketplaces | https://www.suger.io/resources/guides/how-to-sell-on-snowflake-marketplace/ | 2 |
| 2026-08-21 | guide | How to Sell SaaS on Oracle Cloud Marketplace | Other marketplaces | https://www.suger.io/resources/guides/how-to-sell-on-oracle-cloud-marketplace/ | 2 |
| 2026-08-21 | guide | How to Build and Scale a B2B SaaS Partner Program | Cross-cloud | https://www.suger.io/resources/guides/how-to-build-a-b2b-saas-partner-program/ | 2 |
| 2026-08-20 | blog | Selling to Government Through Marketplaces | Cross-cloud | https://www.suger.io/resources/blog/selling-to-government-through-marketplaces/ | 3 |
| 2026-08-20 | blog | Selling Internationally on Cloud Marketplaces | Cross-cloud | https://www.suger.io/resources/blog/selling-internationally-on-cloud-marketplaces/ | 2 |
| 2026-08-20 | blog | Selling Data Products on Cloud Marketplaces | Cross-cloud | https://www.suger.io/resources/blog/selling-data-products-on-a-marketplace/ | 2 |
| 2026-08-20 | blog | Migrate Marketplace Metering Without Downtime | Cross-cloud | https://www.suger.io/resources/blog/migrating-without-breaking-metering/ | 2 |
| 2026-08-20 | blog | Google Cloud Partner Network Tiers Explained | Google | https://www.suger.io/resources/blog/google-cloud-partner-network-tiers/ | 3 |
| 2026-08-20 | blog | GCP Commitments and Marketplace Drawdown for Sellers | Google | https://www.suger.io/resources/blog/gcp-commitments-and-marketplace-drawdown/ | 3 |
| 2026-08-20 | blog | FedRAMP and Your Cloud Marketplace Listing | Cross-cloud | https://www.suger.io/resources/blog/fedramp-and-your-marketplace-listing/ | 3 |
| 2026-08-20 | blog | Co-Selling with Google Cloud: How It Works | Google | https://www.suger.io/resources/blog/co-selling-with-google-cloud/ | 3 |
| 2026-08-20 | blog | Alibaba Cloud Marketplace for APAC Sellers | Other marketplaces | https://www.suger.io/resources/blog/alibaba-cloud-marketplace-for-apac-sellers/ | 2 |
| 2026-08-20 | blog | AWS Vendor Insights: What Sellers Should Know | AWS | https://www.suger.io/resources/blog/aws-vendor-insights-what-sellers-should-know/ | 3 |
| 2026-08-19 | blog | What to Alert On in Marketplace Operations | Cross-cloud | https://www.suger.io/resources/blog/what-to-alert-on-in-marketplace-operations/ | 2 |
| 2026-08-19 | blog | What Moves When You Switch Marketplace Platforms | Cross-cloud | https://www.suger.io/resources/blog/what-moves-when-you-switch-platforms/ | 2 |
| 2026-08-19 | blog | Public Sector vs Commercial Marketplace Deals | Cross-cloud | https://www.suger.io/resources/blog/public-sector-vs-commercial-marketplace-deals/ | 2 |
| 2026-08-19 | blog | Per-Market Pricing on Azure Marketplace, Explained | Microsoft | https://www.suger.io/resources/blog/per-market-pricing-on-azure-marketplace/ | 3 |
| 2026-08-19 | blog | Monthly Marketplace Close Checklist for Billing Ops | Cross-cloud | https://www.suger.io/resources/blog/the-monthly-marketplace-close-checklist/ | 2 |
| 2026-08-19 | blog | Is the AWS Competency Program Worth the Work? | AWS | https://www.suger.io/resources/blog/aws-competencies-worth-the-work/ | 3 |
| 2026-08-19 | blog | How to List AI Models on Cloud Marketplaces | Cross-cloud | https://www.suger.io/resources/blog/listing-ai-models-on-cloud-marketplaces/ | 2 |
| 2026-08-19 | blog | How Fast Can a Marketplace Deal Actually Close? | Cross-cloud | https://www.suger.io/resources/blog/how-fast-can-a-marketplace-deal-actually-close/ | 3 |
| 2026-08-19 | blog | Cloud Marketplace Operations: The Runbook & Cadence | Cross-cloud | https://www.suger.io/resources/blog/the-cloud-marketplace-operations-runbook/ | 2 |
| 2026-08-19 | blog | AWS Marketplace Net Payment Terms for Private Offers | AWS | https://www.suger.io/resources/blog/aws-marketplace-net-payment-terms-for-private-offers/ | 3 |
| 2026-08-18 | blog | Where a Signed AWS Marketplace Agreement Lives | Cross-cloud | https://www.suger.io/resources/blog/where-the-signed-marketplace-agreement-lives/ | 2 |
| 2026-08-18 | blog | Usage-Based Renewal Risk: The Leading Signals | Cross-cloud | https://www.suger.io/resources/blog/renewal-risk-signals-usage-based-deals/ | 2 |
| 2026-08-18 | blog | Snowflake Marketplace for Data and AI Products | Other marketplaces | https://www.suger.io/resources/blog/snowflake-marketplace-for-data-and-ai-products/ | 2 |
| 2026-08-18 | blog | Microsoft IP Co-Sell: How It Actually Works | Microsoft | https://www.suger.io/resources/blog/microsoft-ip-co-sell-how-it-works/ | 3 |
| 2026-08-18 | blog | Measuring Partner Influence Without Bad Data | Cross-cloud | https://www.suger.io/resources/blog/measuring-partner-influence-without-bad-data/ | 2 |
| 2026-08-18 | blog | Marketplace Credit Request: Bulk Adjustments | Cross-cloud | https://www.suger.io/resources/blog/credits-at-scale-bulk-adjustments/ | 2 |
| 2026-08-18 | blog | Cloud Marketplace Platform Migration: A Checklist | Cross-cloud | https://www.suger.io/resources/blog/cloud-marketplace-platform-migration/ | 2 |
| 2026-08-18 | blog | Azure Marketplace Renewals and Offer Transitions | Microsoft | https://www.suger.io/resources/blog/azure-renewals-and-offer-transitions/ | 3 |
| 2026-08-18 | blog | Azure Marketplace Changes 2026: What's New for ISVs | Microsoft | https://www.suger.io/resources/blog/azure-marketplace-fy27-changes-for-isvs/ | 3 |
| 2026-08-18 | blog | AWS Marketplace Professional Services Fee Cut | AWS | https://www.suger.io/resources/blog/aws-marketplace-professional-services-fee-cut/ | 3 |
| 2026-08-16 | blog | Your AWS SCA Is Signed. Now Operationalize It | AWS | https://www.suger.io/resources/blog/aws-sca-operating-plan/ | 3 |
| 2026-08-16 | blog | When Usage Records Fail: Batching and Retries | Cross-cloud | https://www.suger.io/resources/blog/when-usage-records-fail/ | 2 |
| 2026-08-16 | blog | What Buy with AWS Does to Your Website Funnel | AWS | https://www.suger.io/resources/blog/buy-with-aws-funnel/ | 2 |
| 2026-08-16 | blog | Selling on Snowflake, Oracle and Alibaba Cloud | Other marketplaces | https://www.suger.io/resources/blog/selling-on-snowflake-oracle-and-alibaba-cloud/ | 2 |
| 2026-08-16 | blog | Packaging Software and Services in One Offer | Cross-cloud | https://www.suger.io/resources/blog/packaging-software-and-services-in-one-offer/ | 2 |
| 2026-08-16 | blog | One GTM Motion Across AWS, Azure and Google Cloud | AWS | https://www.suger.io/resources/blog/one-gtm-motion-across-aws-azure-google-cloud/ | 2 |
| 2026-08-16 | blog | MCP for Cloud GTM: Connecting Agents to Data | Cross-cloud | https://www.suger.io/resources/blog/mcp-for-cloud-gtm/ | 2 |
| 2026-08-16 | blog | How Security Reviews Shape Marketplace Deals | Cross-cloud | https://www.suger.io/resources/blog/security-reviews-in-marketplace-deals/ | 2 |
| 2026-08-16 | blog | How Enterprise Buyers Buy Through a Marketplace | Cross-cloud | https://www.suger.io/resources/blog/how-enterprise-buyers-buy-through-a-marketplace/ | 2 |
| 2026-08-16 | blog | Creating Private Offers Without the Console | Cross-cloud | https://www.suger.io/resources/blog/creating-private-offers-without-the-console/ | 2 |
| 2026-08-16 | blog | Co-Terming and Expanding Marketplace Agreements | Cross-cloud | https://www.suger.io/resources/blog/co-terming-and-expanding-marketplace-agreements/ | 3 |
| 2026-08-14 | blog | What Should Happen When a Marketplace Trial Ends | Cross-cloud | https://www.suger.io/resources/blog/what-happens-when-a-marketplace-trial-ends/ | 2 |
| 2026-08-14 | blog | The First Marketplace Hire: What to Look For | Cross-cloud | https://www.suger.io/resources/blog/the-first-marketplace-hire/ | 2 |
| 2026-08-14 | blog | Tax and Withholding on Marketplace Revenue | Cross-cloud | https://www.suger.io/resources/blog/tax-and-withholding-on-marketplace-revenue/ | 2 |
| 2026-08-14 | blog | Running Cloud Marketplace Operations API-First | Cross-cloud | https://www.suger.io/resources/blog/running-marketplace-operations-api-first/ | 2 |
| 2026-08-14 | blog | Marketplace Setup Steps Teams Skip and Regret | Cross-cloud | https://www.suger.io/resources/blog/marketplace-setup-steps-teams-skip/ | 2 |
| 2026-08-14 | blog | Marketplace Events and Webhooks: A Practical Guide | Cross-cloud | https://www.suger.io/resources/blog/marketplace-events-and-webhooks/ | 2 |
| 2026-08-14 | blog | Marketplace Data in Salesforce: What to Sync | Cross-cloud | https://www.suger.io/resources/blog/marketplace-data-in-salesforce/ | 2 |
| 2026-08-14 | blog | How Authentication Works for Marketplace APIs | Cross-cloud | https://www.suger.io/resources/blog/authentication-for-marketplace-apis/ | 2 |
| 2026-08-14 | blog | Exporting Marketplace Data to Your Warehouse | Cross-cloud | https://www.suger.io/resources/blog/exporting-marketplace-data-to-your-warehouse/ | 2 |
| 2026-08-14 | blog | Designing Metering Dimensions You Won't Regret | Cross-cloud | https://www.suger.io/resources/blog/designing-metering-dimensions/ | 2 |
| 2026-08-12 | blog | What It Takes to Get Listed: A Readiness Checklist | Cross-cloud | https://www.suger.io/resources/blog/marketplace-listing-readiness-checklist/ | 2 |
| 2026-08-12 | blog | The AWS Standard Contract, or Your Own Paper? | AWS | https://www.suger.io/resources/blog/aws-standard-contract-or-your-own-paper/ | 2 |
| 2026-08-12 | blog | Seller of Record: Why It Changes Your Books | Cross-cloud | https://www.suger.io/resources/blog/marketplace-seller-of-record/ | 2 |
| 2026-08-12 | blog | Marketplace Access: Who Should Have Which Role | Cross-cloud | https://www.suger.io/resources/blog/marketplace-access-roles/ | 2 |
| 2026-08-12 | blog | How to Run a Paid POC Through a Marketplace | Cross-cloud | https://www.suger.io/resources/blog/paid-poc-through-a-marketplace/ | 2 |
| 2026-08-12 | blog | Entitlement Management on Cloud Marketplaces | Cross-cloud | https://www.suger.io/resources/blog/marketplace-entitlement-management/ | 2 |
| 2026-08-12 | blog | EULAs and Custom Terms in Marketplace Deals | Cross-cloud | https://www.suger.io/resources/blog/marketplace-eulas-and-custom-terms/ | 2 |
| 2026-08-12 | blog | Connecting Your CRM to Cloud Marketplace Data | Cross-cloud | https://www.suger.io/resources/blog/connect-crm-to-cloud-marketplace-data/ | 2 |
| 2026-08-12 | blog | Changing Your Marketplace Price After Launch | Cross-cloud | https://www.suger.io/resources/blog/change-marketplace-price-after-launch/ | 3 |
| 2026-08-12 | blog | AI Agents on AWS Marketplace: A Seller's Guide | AWS | https://www.suger.io/resources/blog/ai-agents-on-aws-marketplace/ | 3 |
| 2026-08-10 | blog | Your First 90 Days Selling on a Cloud Marketplace | Cross-cloud | https://www.suger.io/resources/blog/first-90-days-cloud-marketplace/ | 2 |
| 2026-08-10 | blog | Why Your Marketplaces Report Different Numbers | Cross-cloud | https://www.suger.io/resources/blog/marketplace-revenue-reconciliation/ | 2 |
| 2026-08-10 | blog | When a Buyer Pays but Provisioning Never Happens | Cross-cloud | https://www.suger.io/resources/blog/marketplace-provisioning-failures/ | 2 |
| 2026-08-10 | blog | Offer vs Entitlement: What's the Difference? | Cross-cloud | https://www.suger.io/resources/blog/offer-vs-entitlement/ | 2 |
| 2026-08-10 | blog | How Long Does a Marketplace Integration Take? | Cross-cloud | https://www.suger.io/resources/blog/how-long-marketplace-integration-takes/ | 3 |
| 2026-08-10 | blog | How Co-Sell Works on AWS, Azure, and Google Cloud | Cross-cloud | https://www.suger.io/resources/blog/how-co-sell-works/ | 3 |
| 2026-08-10 | blog | Four Metrics to Watch After You Add Buy with AWS | AWS | https://www.suger.io/resources/blog/buy-with-aws-metrics/ | 2 |
| 2026-08-10 | blog | Connect Dynamics 365 to Your Marketplace Pipeline | Microsoft | https://www.suger.io/resources/blog/dynamics-365-marketplace-integration/ | 2 |
| 2026-08-10 | blog | Channel Partner Relationship Management, Explained | Cross-cloud | https://www.suger.io/resources/blog/channel-partner-relationship-management/ | 1 |
| 2026-08-10 | blog | Attribution Rules That Stop Channel Conflict | Cross-cloud | https://www.suger.io/resources/blog/deal-registration-conflict-rules/ | 2 |
| 2026-08-09 | blog | Who Should Own Cloud Marketplace Revenue at an ISV? | Cross-cloud | https://www.suger.io/resources/blog/who-owns-cloud-marketplace-revenue/ | 2 |
| 2026-08-09 | blog | What AWS Marketplace Seller Insights Actually Show | AWS | https://www.suger.io/resources/blog/aws-marketplace-seller-insights/ | 2 |
| 2026-08-09 | blog | The AWS ISV Partner Path Is Now the Software Path | AWS | https://www.suger.io/resources/blog/aws-isv-partner-path/ | 3 |
| 2026-08-09 | blog | Partner-Sourced vs Partner-Influenced Revenue | Cross-cloud | https://www.suger.io/resources/blog/partner-sourced-vs-partner-influenced/ | 2 |
| 2026-08-09 | blog | Marketplace vs Direct Sales: When Each Wins | Cross-cloud | https://www.suger.io/resources/blog/marketplace-vs-direct-sales/ | 2 |
| 2026-08-09 | blog | How to Cancel an AWS Marketplace Subscription | AWS | https://www.suger.io/resources/blog/cancel-aws-marketplace-subscription/ | 2 |
| 2026-08-09 | blog | Cloud Marketplace Pricing Models: How to Choose | Cross-cloud | https://www.suger.io/resources/blog/cloud-marketplace-pricing-models/ | 2 |
| 2026-08-09 | blog | Cloud Marketplace Metrics Worth a Dashboard | Cross-cloud | https://www.suger.io/resources/blog/cloud-marketplace-metrics/ | 2 |
| 2026-08-09 | blog | AWS Marketplace Renewals: An Operating Playbook | AWS | https://www.suger.io/resources/blog/aws-marketplace-renewals/ | 3 |
| 2026-08-09 | blog | AWS Marketplace Contract Pricing vs Usage Pricing | AWS | https://www.suger.io/resources/blog/aws-marketplace-contract-vs-usage-pricing/ | 2 |
| 2026-08-06 | guide | Cloud GTM Platform Evaluation: A Buyer's Framework | Cross-cloud | https://www.suger.io/resources/guides/cloud-gtm-platform-comparison/ | 2 |
| 2026-08-06 | blog | What a Marketplace Dollar Actually Costs You | Cross-cloud | https://www.suger.io/resources/blog/what-a-marketplace-dollar-costs-you/ | 3 |
| 2026-08-06 | blog | Refunds and Cancellations on AWS Marketplace | AWS | https://www.suger.io/resources/blog/aws-marketplace-refunds-and-cancellations/ | 2 |
| 2026-08-06 | blog | Oracle Cloud Marketplace: A Guide for ISV Sellers | Other marketplaces | https://www.suger.io/resources/blog/oracle-cloud-marketplace-guide-for-isv-sellers/ | 2 |
| 2026-08-06 | blog | Google Cloud Private Offers: Setup and Pitfalls | Google | https://www.suger.io/resources/blog/google-cloud-private-offers-setup-and-pitfalls/ | 3 |
| 2026-08-06 | blog | Free Trials on Cloud Marketplaces: An ISV Guide | Cross-cloud | https://www.suger.io/resources/blog/free-trials-on-cloud-marketplaces/ | 2 |
| 2026-08-06 | blog | Cloud GTM Glossary: 40 Marketplace Terms Defined | Cross-cloud | https://www.suger.io/resources/blog/cloud-gtm-glossary/ | 2 |
| 2026-08-06 | blog | CPPO vs MPO: Reselling on the Cloud Marketplaces | Cross-cloud | https://www.suger.io/resources/blog/cppo-vs-mpo-multiparty-private-offers/ | 3 |
| 2026-08-06 | blog | Bringing Resellers Into Google Cloud Marketplace | Google | https://www.suger.io/resources/blog/resellers-on-google-cloud-marketplace/ | 3 |
| 2026-08-06 | blog | Azure Marketplace Private Offers vs Private Plans | Microsoft | https://www.suger.io/resources/blog/azure-private-offers-vs-private-plans/ | 3 |
| 2026-08-06 | blog | AWS Partner Funding: POC, MDF, ISV Workload, PIF | AWS | https://www.suger.io/resources/blog/aws-partner-funding-programs/ | 2 |
| 2026-08-05 | blog | What Is a MACC? Azure Committed Spend, Explained | Microsoft | https://www.suger.io/resources/blog/what-is-a-macc-azure-committed-spend-explained/ | 2 |
| 2026-08-05 | blog | What Buyers See When You Send a Private Offer | Cross-cloud | https://www.suger.io/resources/blog/what-buyers-see-when-you-send-a-private-offer/ | 2 |
| 2026-08-05 | blog | Selling Professional Services on AWS Marketplace | AWS | https://www.suger.io/resources/blog/selling-professional-services-on-aws-marketplace/ | 2 |
| 2026-08-05 | blog | How to Sell on Azure Marketplace: An ISV Guide | Microsoft | https://www.suger.io/resources/blog/how-to-sell-on-azure-marketplace-isv-guide/ | 2 |
| 2026-08-05 | blog | How to Choose the Right Cloud Marketplace Platform | Cross-cloud | https://www.suger.io/resources/blog/how-to-choose-a-cloud-marketplace-platform/ | 2 |
| 2026-08-05 | blog | Google Cloud Marketplace: The ISV Seller Guide | Google | https://www.suger.io/resources/blog/google-cloud-marketplace-isv-seller-guide/ | 2 |
| 2026-08-05 | blog | AWS Marketplace for Sellers: The Complete Guide | AWS | https://www.suger.io/resources/blog/aws-marketplace-for-sellers-complete-guide/ | 2 |
| 2026-08-05 | blog | AWS Marketplace Express Private Offers, Explained | AWS | https://www.suger.io/resources/blog/aws-marketplace-express-private-offers/ | 3 |
| 2026-08-05 | blog | AWS EDP: What Marketplace Sellers Need to Know | AWS | https://www.suger.io/resources/blog/aws-edp-what-sellers-need-to-know/ | 2 |
| 2026-08-05 | blog | AWS ACE: A Practical Co-Sell Guide for ISVs | AWS | https://www.suger.io/resources/blog/aws-ace-guide-for-isv-sellers/ | 2 |
| 2026-08-03 | blog | Partner Relationship Management Software for ISVs | Cross-cloud | https://www.suger.io/resources/blog/partner-relationship-management-software-for-isvs/ | 1 |
| 2026-08-03 | blog | Deal Registration Software: A Guide for ISVs | Cross-cloud | https://www.suger.io/resources/blog/deal-registration-software-for-isvs/ | 2 |
| 2026-07-29 | blog | AWS Co-Sell Quality Score: What Actually Moves It | AWS | https://www.suger.io/resources/blog/aws-decides-whether-you-get-a-rep/ | 3 |
| 2026-07-15 | blog | PRM Journeys: Keep Partners Engaged and Active | Cross-cloud | https://www.suger.io/resources/blog/prm-journeys-keep-partners-engaged/ | 1 |
| 2026-06-30 | guide | Selling on Google Cloud Marketplace: 2026 Guide | Google | https://www.suger.io/resources/guides/google-cloud-marketplace/ | 2 |
| 2026-06-26 | product update | Product Updates: June 2026 | Cross-cloud | https://www.suger.io/resources/blog/product-updates-june-2026/ | 1 |
| 2026-06-24 | blog | Launching a new path for partnerships | Cross-cloud | https://www.suger.io/resources/blog/partner-relationship-management/ | 1 |
| 2026-06-12 | case study | How Ona Turned AWS Marketplace Into Its Primary Channel | Cross-cloud | https://www.suger.io/resources/customer-stories/ona/ | 2 |
| 2026-06-01 | case study | How Aikido Security Tripled AWS Marketplace Revenue | Cross-cloud | https://www.suger.io/resources/customer-stories/aikido-security/ | 2 |
| 2026-05-22 | guide | AI Opportunity Insights for AWS Co-Sell Referrals | Cross-cloud | https://www.suger.io/resources/guides/ai-opportunity-insights/ | 2 |
| 2026-05-22 | guide | AI Field Mapping & Prompt Templates for CRM Sync | Cross-cloud | https://www.suger.io/resources/guides/ai-field-mapping-prompts/ | 2 |
| 2026-05-22 | guide | AI Diagnose: Fix Failed Marketplace Offers | Cross-cloud | https://www.suger.io/resources/guides/ai-diagnose-offer-failures/ | 2 |
| 2026-05-22 | guide | AI Diagnose: Fix Failed Co-Sell Referrals | Cross-cloud | https://www.suger.io/resources/guides/ai-diagnose-cosell-failures/ | 2 |
| 2026-05-22 | blog | Suger AI: In-Product Copilot for Marketplace Ops | Cross-cloud | https://www.suger.io/resources/blog/meet-suger-ai-the-in-product-copilot/ | 1 |
| 2026-05-15 | guide | How to Sell on Cloud Marketplaces: The 2026 Guide | Cross-cloud | https://www.suger.io/resources/guides/cloud-marketplaces/ | 2 |
| 2026-05-11 | guide | How Suger Uses AI for Cloud Marketplace Automation | Cross-cloud | https://www.suger.io/resources/guides/suger-ai/ | 2 |
| 2026-05-11 | guide | Cloud GTM Sales: A Playbook for Marketplace Teams | Cross-cloud | https://www.suger.io/resources/guides/cloud-gtm-sales/ | 2 |
| 2026-05-01 | case study | How Simpplr Drove $2M on AWS Marketplace in Year One | Cross-cloud | https://www.suger.io/resources/customer-stories/simpplr/ | 2 |
| 2026-04-30 | product update | Product Updates: April 2026 | Cross-cloud | https://www.suger.io/resources/blog/product-updates-april-2026/ | 1 |
| 2026-04-27 | case study | How NinjaOne Built a Cloud GTM Motion in 18 Months | Cross-cloud | https://www.suger.io/resources/customer-stories/ninjaone/ | 2 |
| 2026-04-23 | guide | The Co-Sell Playbook for Cloud GTM Teams (2026) | Cross-cloud | https://www.suger.io/resources/guides/co-sell/ | 2 |
| 2026-04-23 | guide | Selling on Azure Marketplace: The 2026 ISV Guide | Microsoft | https://www.suger.io/resources/guides/azure-marketplace/ | 2 |
| 2026-04-23 | guide | Selling on AWS Marketplace: The Complete 2026 Guide | AWS | https://www.suger.io/resources/guides/aws-marketplace/ | 2 |
| 2026-04-23 | guide | Marketplace Billing & Revenue Operations (2026) | Cross-cloud | https://www.suger.io/resources/guides/marketplace-billing/ | 2 |
| 2026-04-20 | guide | The Complete Guide to Cloud GTM for ISVs (2026) | Cross-cloud | https://www.suger.io/resources/guides/cloud-gtm/ | 2 |
| 2026-03-26 | product update | Product Updates: March 2026 | Cross-cloud | https://www.suger.io/resources/blog/product-updates-march-2026/ | 1 |
| 2026-02-19 | product update | Product Updates: February 2026 | Cross-cloud | https://www.suger.io/resources/blog/product-updates-february-2026/ | 1 |
| 2026-02-11 | blog | Sales 101: Close Deals on AWS, Azure & GCP | AWS | https://www.suger.io/resources/blog/sales-101-how-to-close-deals-faster-on-aws-azure-gcp/ | 2 |
| 2026-02-05 | blog | Partnerships 101: Co-Sell on AWS, Azure & GCP | AWS | https://www.suger.io/resources/blog/partnerships-101-build-a-winning-co-sell-motion-with-aws-azure-gcp/ | 2 |
| 2026-01-27 | blog | Finance 101: GAAP for Marketplace Revenue | Cross-cloud | https://www.suger.io/resources/blog/finance-101-bridging-the-gaap-on-marketplace-revenue/ | 2 |
| 2026-01-26 | product update | Product Updates: January 2026 | Cross-cloud | https://www.suger.io/resources/blog/product-updates-january-2026/ | 1 |
| 2026-01-13 | blog | RevOps 101: Governing Cloud Marketplace Deals | Cross-cloud | https://www.suger.io/resources/blog/revops-cloud-gtm-playbook-101/ | 2 |
| 2026-01-12 | product update | Product Updates: Winter 2025 | Cross-cloud | https://www.suger.io/resources/blog/product-updates-winter-2025/ | 1 |
| 2026-01-05 | blog | AWS re:Invent 2025 Recap: Cloud GTM for 2026 | AWS | https://www.suger.io/resources/blog/your-cloud-gtm-strategy-for-2026-post-aws-reinvent/ | 2 |
| 2025-12-22 | blog | Buyer Intent Signals for Cloud Marketplaces | Cross-cloud | https://www.suger.io/resources/blog/buyer-intent-signals/ | 2 |
| 2025-10-06 | product update | Product Updates: September 2025 | Cross-cloud | https://www.suger.io/resources/blog/product-updates-september-2025/ | 1 |
| 2025-09-30 | blog | Cloudelligent Cuts Co-Sell Time to a Few Clicks | Cross-cloud | https://www.suger.io/resources/blog/cloudelligent-cuts-co-sell-submission-time-to-a-few-clicks-with-suger/ | 1 |
| 2025-09-16 | blog | Suger Passes $6B in Cloud Marketplace Volume | Cross-cloud | https://www.suger.io/resources/blog/suger-surpasses-6-billion-in-cloud-marketplace-transactions/ | 1 |
| 2025-09-02 | product update | Product Updates: August 2025 | Cross-cloud | https://www.suger.io/resources/blog/product-updates-august-2025/ | 1 |
| 2025-08-16 | blog | How Glean Expands Co-Sell Pipeline with Suger | Cross-cloud | https://www.suger.io/resources/blog/glean-expands-co-sell-pipeline-and-automates-operations-with-suger/ | 1 |
| 2025-08-13 | blog | FusionAuth Scales to 300 AWS Co-Sell Referrals | Cross-cloud | https://www.suger.io/resources/blog/fusionauth-scales-to-300-referrals-submits-5x-faster-with-suger/ | 1 |
| 2025-08-08 | blog | Do Cloud Marketplace Deals Need a Signature? | Cross-cloud | https://www.suger.io/resources/blog/when-do-you-need-a-signature-on-legal-documents-in-cloud-marketplace-deals/ | 2 |
| 2025-08-04 | product update | Product Updates: July 2025 | Cross-cloud | https://www.suger.io/resources/blog/product-updates-july-2025/ | 1 |
| 2025-07-14 | blog | Fireblocks Scales Co-Sell 3x, Cuts Offer Time 70% | Cross-cloud | https://www.suger.io/resources/blog/fireblocks-scales-co-sell-3x-and-cuts-offer-time-70-with-suger/ | 1 |
| 2025-07-11 | blog | Suger Data Export: Reports and Raw Data Hub | Cross-cloud | https://www.suger.io/resources/blog/data-export-hub/ | 1 |
| 2025-07-11 | blog | More Flexibility for GCP Marketplace Offers | Google | https://www.suger.io/resources/blog/product-update-for-gcp-marketplace/ | 2 |

YouTube (channel @suger-io, 68 videos, about 50 subscribers; items since 2025-07 plus the one older long-form interview used):

| Date (approx.) | Type | Title | Cloud | URL | Substance |
|---|---|---|---|---|---|
| ~2026-08 | webinar | The Future of Co-Sell: AI, Marketplace, and the End of Manual GTM (with AWS) | AWS | https://www.youtube.com/watch?v=yKxd8U_nw-A | 3 |
| ~2026-04 | podcast | Apple Trees, AWS, and Reality: Michael Musselman on Long-Term Partner Growth (Kong x Sugerpod) | AWS | https://www.youtube.com/watch?v=AWg_9G_g56M | 3 |
| ~2026-03 | podcast | From Zero to Scale: Derrick Roberts on Marketplace and Partner Strategy (NinjaOne x SugerPod) | Cross-cloud | https://www.youtube.com/watch?v=TLA31Yj0E_k | 2 |
| ~2026-05 | case study | NinjaOne, Suger Case Study | Cross-cloud | https://www.youtube.com/watch?v=ocjW55yUPnA | 1 |
| ~2026-05 | shorts (8) | "Newsflash AWS Will Compete With You", "The Starbucks Rule for Enterprise Marketplace Sales", "The Greatest Myth in Alliance", "If You Need Apples Today..." and others (clips of the two podcasts) | AWS | https://www.youtube.com/@suger-io/videos | 1 |
| ~2026-07 to 2026-08 | product shorts | Insulin Inbox, Suger AI Knowledge Base, Cloud Marketplace Billing explained | n/a | https://www.youtube.com/@suger-io/videos | 1 |
| 2025-Q1 | podcast | The Future of B2B Sales on Marketplaces and AI, with Vince Menzione (before window; used for funding and anecdotes only) | Cross-cloud | https://www.youtube.com/watch?v=8ANFr3p9JL0 | 1 |

Not found: a Suger research report or survey, a webinar series page, or a standalone podcast feed. The "Sugerpod" podcast exists only as YouTube uploads (two episodes in 2026).

## 9. Registry rows and discovery queries

| Name | Role | Where to look | Good for | Last new item |
|---|---|---|---|---|
| Sabrina Xie | Suger content author, listed as Head of QA [SG65] | https://www.suger.io/resources/blog/author/sabrina-xie/ | Co-sell mechanics on all three clouds, AWS OQS, leads, Microsoft REO/MPA, SCA | 2026-09-24 "AWS Partner Central Leads from Salesforce Accounts" |
| Stacy Wu | Head of Solution [SG65] | https://www.suger.io/resources/blog/author/stacy-wu/ | AWS Marketplace mechanics: Concurrent Agreements, Deployed on AWS, offer errors, express offers, agents | 2026-09-24 "Upgrading to AWS Marketplace Concurrent Agreements" |
| Shirley Guo | Suger author (billing, finance) | https://www.suger.io/resources/blog/author/shirley-guo/ | Fees, KYC, usage correction, POs, net terms, reconciliation | 2026-09-24 "AWS EMEA SARL and Seller KYC" |
| Samantha Ho | Suger author (Microsoft, Google, APAC marketplaces) | https://www.suger.io/resources/blog/author/samantha-ho/ | Azure renewals, per-market pricing, custom terms, Google drawdown and tiers | 2026-08-24 "Microsoft Marketplace Custom Contract Lengths" |
| Chloe Wu | Suger author (buyer journey, lifecycle) | https://www.suger.io/resources/blog/author/chloe-wu/ | Listing retirement, deal timelines, targets, repricing | 2026-09-24 "Retire a Marketplace Listing" |
| Gabriel Paiva | Product Lead | https://www.suger.io/resources/blog/author/gabriel-paiva/ and https://www.suger.io/resources/changelog/ | Monthly product updates, HubSpot app scope, which cloud features are automatable | 2026-09-13 "What Syncs to HubSpot from Your Marketplace Deals" |
| Chengjun Yuan | Co-founder, CTO | https://www.suger.io/resources/blog/author/chengjun-yuan/ | Marketplace APIs, security reviews, FedRAMP | 2026-08-24 |
| Jon Yoo | Co-founder, CEO | YouTube @suger-io (webinars, Sugerpod), LinkedIn | AWS field and program commentary with AWS PDMs | ~2026-08 webinar |
| Juston Salcido | Head of GTM / Sr Director, Cloud GTM Practice | https://www.suger.io/resources/blog/ (press), LinkedIn | AWS 3PI PDM Pilot, early-stage ISV onboarding | 2026-09-02 |
| Suger changelog | Product release notes | https://www.suger.io/resources/changelog/ | Earliest signal of new cloud features being automated (for example AWS pre-authorized auto-renewal) | 2026-09-14 |
| Suger docs | Product docs | https://doc.suger.io/ | Where cloud rules end and Suger rules begin; CRM coverage limits | fetched 2026-09-26 |
| Suger YouTube | Channel | https://www.youtube.com/@suger-io (RSS https://www.youtube.com/feeds/videos.xml?channel_id=UCwyfpzgKY9lrVqCEO3drzWw) | Sugerpod interviews, AWS PDM webinars | ~2026-08 |
| Michael Musselman (NEW, CREATOR) | Global cloud alliances, Kong; co-founder of Pecan partner community (500+ members); co-hosts "Beyond Co-Sell" YouTube with Andrew Morris | LinkedIn; YouTube "Beyond Co-Sell" | Practitioner view of AWS scorecards and CFO expectation setting | ~2026-04 on Sugerpod [SG76] |
| Derrick Roberts (Watchlist, CREATOR) | Sr Director BD and Alliances, NinjaOne | LinkedIn | Internal enablement playbook | ~2026-03 [SG77] |

Monitoring method: the sitemap at https://www.suger.io/sitemap-0.xml lists every post and each page's JSON-LD carries datePublished and author, so a monthly diff of the sitemap against this inventory is the cheapest refresh.

Discovery queries (run monthly, last 45 days):
1. `site:suger.io/resources/blog "Last verified"` plus the month name, to catch newly sourced rule posts.
2. `site:suger.io "What's New" 2026` (Suger posts that cite fresh AWS What's New items often precede our own capture).
3. YouTube: `"Sugerpod"` and `"Suger" AWS PDM webinar co-sell`.
4. LinkedIn: `"Suger" "Cloud GTM Practice" OR "3PI" AWS` for pilot and PDM-program news.
5. `"Suger" (acquisition OR raises OR "Series B")` for ownership and funding changes.

## Sources

| Tag | Title | Date | URL |
|---|---|---|---|
| SG1 | Microsoft IP Co-Sell: How It Actually Works (Sabrina Xie) | 2026-08-18 | https://www.suger.io/resources/blog/microsoft-ip-co-sell-how-it-works/ |
| SG2 | AWS EMEA SARL and Seller KYC on AWS Marketplace (Shirley Guo) | 2026-09-24 | https://www.suger.io/resources/blog/aws-emea-sarl-marketplace-kyc/ |
| SG3 | Upgrading to AWS Marketplace Concurrent Agreements (Stacy Wu) | 2026-09-24 | https://www.suger.io/resources/blog/aws-marketplace-concurrent-agreements-opt-in-or-relist/ |
| SG4 | AWS Partner Central Leads from Salesforce Accounts (Sabrina Xie) | 2026-09-24 | https://www.suger.io/resources/blog/aws-partner-central-leads-from-salesforce/ |
| SG5 | Deployed on AWS Badge: How to Qualify and Submit (Stacy Wu) | 2026-09-19 | https://www.suger.io/resources/blog/deployed-on-aws-badge/ |
| SG6 | AWS Marketplace Request Private Offer: Who Answers? (Sabrina Xie) | 2026-09-19 | https://www.suger.io/resources/blog/aws-marketplace-private-offer-requests/ |
| SG7 | AWS Private Offer Errors: Why a Buyer Can't Accept (Stacy Wu) | 2026-09-19 | https://www.suger.io/resources/blog/buyer-cannot-accept-aws-private-offer/ |
| SG8 | Suger Joins AWS 3PI PDM Pilot for ISV Onboarding (press release) | 2026-09-02 | https://www.suger.io/resources/blog/suger-selected-aws-3pi-pdm-pilot/ |
| SG9 | AWS re:Invent 2026: A Marketplace Prep Checklist (Stacy Wu) | 2026-08-27 | https://www.suger.io/resources/blog/aws-reinvent-2026-marketplace-prep/ |
| SG10 | AWS Managed Entitlements for Foundation Models (Stacy Wu) | 2026-08-27 | https://www.suger.io/resources/blog/managed-entitlements-for-foundation-models/ |
| SG11 | Turning re:Invent Conversations Into ACE Referrals (Sabrina Xie) | 2026-08-27 | https://www.suger.io/resources/blog/reinvent-conversations-to-ace-referrals/ |
| SG12 | Migrating to the New AWS Partner Central (ACE) (Sabrina Xie) | 2026-08-24 | https://www.suger.io/resources/blog/migrating-to-aws-partner-central/ |
| SG13 | AWS Co-Sell Quality Score: What Actually Moves It (Sabrina Xie) | 2026-07-29 | https://www.suger.io/resources/blog/aws-decides-whether-you-get-a-rep/ |
| SG14 | AWS ACE: A Practical Co-Sell Guide for ISVs (Sabrina Xie) | 2026-08-05 | https://www.suger.io/resources/blog/aws-ace-guide-for-isv-sellers/ |
| SG15 | The AWS ISV Partner Path Is Now the Software Path (Sabrina Xie) | 2026-08-09 | https://www.suger.io/resources/blog/aws-isv-partner-path/ |
| SG16 | AWS Partner Funding: POC, MDF, ISV Workload, PIF (Sabrina Xie) | 2026-08-06 | https://www.suger.io/resources/blog/aws-partner-funding-programs/ |
| SG17 | AWS EDP: What Marketplace Sellers Need to Know (Stacy Wu) | 2026-08-05 | https://www.suger.io/resources/blog/aws-edp-what-sellers-need-to-know/ |
| SG18 | What a Marketplace Dollar Actually Costs You (Shirley Guo) | 2026-08-06 | https://www.suger.io/resources/blog/what-a-marketplace-dollar-costs-you/ |
| SG19 | AWS Marketplace Professional Services Fee Cut (Shirley Guo) | 2026-08-18 | https://www.suger.io/resources/blog/aws-marketplace-professional-services-fee-cut/ |
| SG20 | AWS Marketplace Express Private Offers, Explained (Stacy Wu) | 2026-08-05 | https://www.suger.io/resources/blog/aws-marketplace-express-private-offers/ |
| SG21 | Selling Professional Services on AWS Marketplace (Stacy Wu) | 2026-08-05 | https://www.suger.io/resources/blog/selling-professional-services-on-aws-marketplace/ |
| SG22 | AWS Marketplace Net Payment Terms for Private Offers (Shirley Guo) | 2026-08-19 | https://www.suger.io/resources/blog/aws-marketplace-net-payment-terms-for-private-offers/ |
| SG23 | Your AWS SCA Is Signed. Now Operationalize It (Sabrina Xie) | 2026-08-16 | https://www.suger.io/resources/blog/aws-sca-operating-plan/ |
| SG24 | Is the AWS Competency Program Worth the Work? (Stacy Wu) | 2026-08-19 | https://www.suger.io/resources/blog/aws-competencies-worth-the-work/ |
| SG25 | AWS Marketplace Storefront vs Buy with AWS (Stacy Wu) | 2026-08-24 | https://www.suger.io/resources/blog/aws-marketplace-storefront-vs-buy-with-aws/ |
| SG26 | AWS Vendor Insights: What Sellers Should Know (Stacy Wu) | 2026-08-20 | https://www.suger.io/resources/blog/aws-vendor-insights-what-sellers-should-know/ |
| SG27 | AI Agents on AWS Marketplace: A Seller's Guide (Stacy Wu) | 2026-08-12 | https://www.suger.io/resources/blog/ai-agents-on-aws-marketplace/ |
| SG28 | Multi-currency transactions on AWS Marketplace (Gabriel Paiva; FAQ updated 2026-09-19) | 2025-04-11 | https://www.suger.io/resources/blog/multi-currency-transactions-on-aws-marketplace/ |
| SG29 | Microsoft Resale Enabled Offers vs MPO: Who Pays You (Sabrina Xie) | 2026-09-19 | https://www.suger.io/resources/blog/microsoft-resale-enabled-offers-vs-mpo/ |
| SG30 | The Updated Microsoft Partner Agreement, Explained (Sabrina Xie) | 2026-08-30 | https://www.suger.io/resources/blog/updated-microsoft-partner-agreement/ |
| SG31 | Microsoft Marketplace Request Private Offer (Samantha Ho) | 2026-08-24 | https://www.suger.io/resources/blog/microsoft-marketplace-request-private-offer/ |
| SG32 | Microsoft Marketplace Custom Contract Lengths (Samantha Ho) | 2026-08-24 | https://www.suger.io/resources/blog/microsoft-marketplace-custom-contract-lengths/ |
| SG33 | Azure Marketplace Renewals and Offer Transitions (Samantha Ho) | 2026-08-18 | https://www.suger.io/resources/blog/azure-renewals-and-offer-transitions/ |
| SG34 | Azure Marketplace Changes 2026: What's New for ISVs (Samantha Ho) | 2026-08-18 | https://www.suger.io/resources/blog/azure-marketplace-fy27-changes-for-isvs/ |
| SG35 | What Is a MACC? Azure Committed Spend, Explained (Samantha Ho) | 2026-08-05 | https://www.suger.io/resources/blog/what-is-a-macc-azure-committed-spend-explained/ |
| SG36 | Per-Market Pricing on Azure Marketplace, Explained (Samantha Ho) | 2026-08-19 | https://www.suger.io/resources/blog/per-market-pricing-on-azure-marketplace/ |
| SG37 | Azure Marketplace Private Offers vs Private Plans (Samantha Ho) | 2026-08-06 | https://www.suger.io/resources/blog/azure-private-offers-vs-private-plans/ |
| SG38 | How to Sell on Azure Marketplace: An ISV Guide (Samantha Ho) | 2026-08-05 | https://www.suger.io/resources/blog/how-to-sell-on-azure-marketplace-isv-guide/ |
| SG39 | GCP Commitments and Marketplace Drawdown for Sellers (Samantha Ho) | 2026-08-20 | https://www.suger.io/resources/blog/gcp-commitments-and-marketplace-drawdown/ |
| SG40 | Google Cloud Partner Network Tiers Explained (Samantha Ho) | 2026-08-20 | https://www.suger.io/resources/blog/google-cloud-partner-network-tiers/ |
| SG41 | Co-Selling with Google Cloud: How It Works (Sabrina Xie) | 2026-08-20 | https://www.suger.io/resources/blog/co-selling-with-google-cloud/ |
| SG42 | Google Cloud Private Offers: Setup and Pitfalls (Samantha Ho) | 2026-08-06 | https://www.suger.io/resources/blog/google-cloud-private-offers-setup-and-pitfalls/ |
| SG43 | Bringing Resellers Into Google Cloud Marketplace (Sabrina Xie) | 2026-08-06 | https://www.suger.io/resources/blog/resellers-on-google-cloud-marketplace/ |
| SG44 | How Co-Sell Works on AWS, Azure, and Google Cloud (Sabrina Xie) | 2026-08-10 | https://www.suger.io/resources/blog/how-co-sell-works/ |
| SG45 | CPPO vs MPO: Reselling on the Cloud Marketplaces (Sabrina Xie) | 2026-08-06 | https://www.suger.io/resources/blog/cppo-vs-mpo-multiparty-private-offers/ |
| SG46 | Marketplace Usage Correction: What Each Cloud Allows (Shirley Guo) | 2026-09-24 | https://www.suger.io/resources/blog/marketplace-usage-correction/ |
| SG47 | Cloud Marketplace Purchase Orders: Who Sets the PO (Shirley Guo) | 2026-09-19 | https://www.suger.io/resources/blog/purchase-order-numbers-on-cloud-marketplaces/ |
| SG48 | Retire a Marketplace Listing: What Buyers Keep (Chloe Wu) | 2026-09-24 | https://www.suger.io/resources/blog/retire-marketplace-listing/ |
| SG49 | The Co-Sell Playbook for Cloud GTM Teams (guide; reviewed 2026-08-06) | 2026-04-23 | https://www.suger.io/resources/guides/co-sell/ |
| SG50 | Cloud GTM Platform Evaluation: A Buyer's Framework (guide) | 2026-08-06 | https://www.suger.io/resources/guides/cloud-gtm-platform-comparison/ |
| SG51 | Selling on Azure Marketplace: The 2026 ISV Guide (guide; reviewed 2026-08-02) | 2026-04-23 | https://www.suger.io/resources/guides/azure-marketplace/ |
| SG52 | Selling on AWS Marketplace: The Complete 2026 Guide (guide; reviewed 2026-08-02) | 2026-04-23 | https://www.suger.io/resources/guides/aws-marketplace/ |
| SG53 | Selling on Google Cloud Marketplace: 2026 Guide (guide) | 2026-06-30 | https://www.suger.io/resources/guides/google-cloud-marketplace/ |
| SG54 | The Complete Guide to Cloud GTM for ISVs (guide) | 2026-04-20 | https://www.suger.io/resources/guides/cloud-gtm/ |
| SG55 | Cloud GTM Sales: A Playbook for Marketplace Teams (guide) | 2026-05-11 | https://www.suger.io/resources/guides/cloud-gtm-sales/ |
| SG56 | Marketplace Billing and Revenue Operations (guide) | 2026-04-23 | https://www.suger.io/resources/guides/marketplace-billing/ |
| SG57 | Partnerships 101: Co-Sell on AWS, Azure and GCP (Sabrina Xie) | 2026-02-05 | https://www.suger.io/resources/blog/partnerships-101-build-a-winning-co-sell-motion-with-aws-azure-gcp/ |
| SG58 | Sales 101: Close Deals on AWS, Azure and GCP (Chloe Wu) | 2026-02-11 | https://www.suger.io/resources/blog/sales-101-how-to-close-deals-faster-on-aws-azure-gcp/ |
| SG59 | AWS re:Invent 2025 Recap: Cloud GTM for 2026 (Qiuyang Luo) | 2026-01-05 | https://www.suger.io/resources/blog/your-cloud-gtm-strategy-for-2026-post-aws-reinvent/ |
| SG60 | Suger Passes $6B in Cloud Marketplace Volume (Qiuyang Luo) | 2025-09-16 | https://www.suger.io/resources/blog/suger-surpasses-6-billion-in-cloud-marketplace-transactions/ |
| SG61 | Suger Pricing | fetched 2026-09-26 | https://www.suger.io/pricing/ |
| SG62 | Suger MCP Server | fetched 2026-09-26 | https://www.suger.io/platform/mcp/ |
| SG63 | Co-Sell Automation (platform page) | fetched 2026-09-26 | https://www.suger.io/platform/cosell/ |
| SG64 | HubSpot Marketplace Integration (platform page) | fetched 2026-09-26 | https://www.suger.io/platform/integrations/hubspot/ |
| SG65 | About Suger | fetched 2026-09-26 | https://www.suger.io/about/ |
| SG66 | Suger API Reference (landing page) | fetched 2026-09-26 | https://www.suger.io/resources/apis/ |
| SG67 | Launching a new path for partnerships (Jon Yoo, PRM launch) | 2026-06-24 | https://www.suger.io/resources/blog/partner-relationship-management/ |
| SG68 | What Syncs to HubSpot from Your Marketplace Deals (Gabriel Paiva) | 2026-09-13 | https://www.suger.io/resources/blog/marketplace-data-in-hubspot/ |
| SG69 | Suger Changelog (entries 2026-08-31 to 2026-09-14) | 2026-09-14 | https://www.suger.io/resources/changelog/ |
| SG70 | Product Updates: June 2026 (Gabriel Paiva) | 2026-06-26 | https://www.suger.io/resources/blog/product-updates-june-2026/ |
| SG71 | Product Updates: April 2026 (Gabriel Paiva) | 2026-04-30 | https://www.suger.io/resources/blog/product-updates-april-2026/ |
| SG72 | Product Updates: March 2026 (Gabriel Paiva) | 2026-03-26 | https://www.suger.io/resources/blog/product-updates-march-2026/ |
| SG73 | Product Updates: February 2026 (Gabriel Paiva) | 2026-02-19 | https://www.suger.io/resources/blog/product-updates-february-2026/ |
| SG74 | Product Updates: January 2026 (Gabriel Paiva) | 2026-01-26 | https://www.suger.io/resources/blog/product-updates-january-2026/ |
| SG75 | The Future of Co-Sell: AI, Marketplace, and the End of Manual GTM (with AWS), Suger webinar with an AWS PDM (transcript) | ~2026-08 | https://www.youtube.com/watch?v=yKxd8U_nw-A |
| SG76 | Apple Trees, AWS, and Reality: Michael Musselman (Kong x Sugerpod) (transcript) | ~2026-04 | https://www.youtube.com/watch?v=AWg_9G_g56M |
| SG77 | From Zero to Scale: Derrick Roberts (NinjaOne x SugerPod) (transcript) | ~2026-03 | https://www.youtube.com/watch?v=TLA31Yj0E_k |
| SG78 | The Future of B2B Sales on Marketplaces and AI, with Vince Menzione (transcript) | 2025-Q1 | https://www.youtube.com/watch?v=8ANFr3p9JL0 |
| SG79 | Suger docs: Co-sell Configuration | fetched 2026-09-26 | https://doc.suger.io/cosell/cosell-configuration/ |
| SG80 | How Fast Can a Marketplace Deal Actually Close? (Chloe Wu) | 2026-08-19 | https://www.suger.io/resources/blog/how-fast-can-a-marketplace-deal-actually-close/ |
| SG81 | How Long Does a Marketplace Integration Take? (Max Ma) | 2026-08-10 | https://www.suger.io/resources/blog/how-long-marketplace-integration-takes/ |
| SG82 | Changing Your Marketplace Price After Launch (Chloe Wu) | 2026-08-12 | https://www.suger.io/resources/blog/change-marketplace-price-after-launch/ |
| SG83 | FedRAMP and Your Cloud Marketplace Listing (Chengjun Yuan) | 2026-08-20 | https://www.suger.io/resources/blog/fedramp-and-your-marketplace-listing/ |
| SG84 | How to Sell on Cloud Marketplaces: The 2026 Guide (guide) | 2026-05-15 | https://www.suger.io/resources/guides/cloud-marketplaces/ |
| SG85 | AWS Marketplace now supports auto-renewals for private offers (AWS What's New, OFFICIAL, verification) | 2026-09-01 | https://aws.amazon.com/about-aws/whats-new/2026/09/aws-marketplace-auto-renewals-for-private-offers/ |
| SG86 | Configuring net payment terms for private offers (AWS docs, OFFICIAL, verification) | fetched 2026-09-26 | https://docs.aws.amazon.com/marketplace/latest/userguide/seller-net-payment-terms.html |
| SG87 | Marketplace Customer Credit Program brief (Google, OFFICIAL, verification) | fetched 2026-09-26 | https://services.google.com/fh/files/misc/google_cloud_marketplace_customer_credit_program_brief.pdf |
| SG88 | Suger YouTube channel (@suger-io) | fetched 2026-09-26 | https://www.youtube.com/@suger-io |
| SG89 | Suger sitemap (enumeration source) | fetched 2026-09-26 | https://www.suger.io/sitemap-0.xml |
| SG90 | AWS Marketplace Renewals: An Operating Playbook (Stacy Wu) | 2026-08-09 | https://www.suger.io/resources/blog/aws-marketplace-renewals/ |
