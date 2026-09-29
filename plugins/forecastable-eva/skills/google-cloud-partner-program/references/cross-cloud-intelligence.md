# Cross-cloud partner program intelligence (AWS vs Microsoft vs Google Cloud)
Version: 2026.09 (built 2026-09-26). Refreshed monthly. Facts carry source tags; see Sources.
Scope: the layer that sits above the three per-cloud files (`aws/`, `microsoft/`, `google-cloud/`). Use this file to compare, prioritize and run one operating cadence across clouds. For portal menu paths and per-cloud runbooks, go to the per-cloud file. Where this file and a per-cloud file disagree, the per-cloud file wins for that cloud's mechanics; flag the conflict in section 14.

Label key: OFFICIAL (hyperscaler or Crossbeam product docs), VENDOR (marketplace ops vendors, consultancies, anyone selling into this motion), INDEPENDENT (analysts, press), CREATOR (individual publishers). Analyst studies commissioned by a hyperscaler are marked "commissioned".

---

## The twelve things that matter right now

1. **All three marketplaces now charge the same headline fee: 3%, falling to 1.5% on renewals.** AWS: 3% SaaS public and private under $1M TCV, 2% at $1M to under $10M, 1.5% at $10M+, 1.5% on all renewals [X1]. Google: identical TCV ladder since 2025-04-21 plus 1.5% for renewals, migrations and channel shifts [X5]. Microsoft: flat 3% on all transactable offer types, 1.5% on attested renewals of private offers created on or after 2024-10-01 [X2][X3]. Fees are no longer a reason to pick one cloud over another. The real cost is the ops work around the listing [X58].

2. **Committed spend is the prize, and each cloud now gates it by where your product runs.** Microsoft counts 100% of the pretax purchase toward MACC, but only for "Azure benefit eligible" offers, which requires Azure IP co-sell eligible status and Azure-exclusive licenses [X8][X14]. Google counts 100% toward commit for services actively running on Google Cloud, professional services excluded [X7]. AWS opened the catalog to SaaS hosted anywhere on 2025-05-01, but only products 100% deployed on AWS get the "Deployed on AWS" badge and keep customer-commitment benefits [X9]; independent reporting puts EDP/PPA marketplace drawdown at 100% of qualifying spend capped at 25% of the annual commitment [X10] (unverified against an official page, see section 14). **Where you host decides where you can draw down.**

3. **The market is big and growing fast, but most ISVs do not see much of it yet.** Omdia (Canalys) sized hyperscaler marketplace sales at $30B in 2024, forecast $163B by 2030 (29.1% CAGR), against about $470B in committed cloud spend across the three [X40]. In the Clazar and Partner Insight survey, 89% of companies transact on a marketplace, but only 22% get more than 20% of revenue there and 41% get under 5% [X44].

4. **Channel partners are moving onto the marketplace.** Omdia expects at least 50% of marketplace transactions to flow through channel partners by 2027 [X41] and nearly 60% by 2030 [X40]. Tackle's respondents reported 27% of marketplace deals involving a channel partner, expected to reach 37% within 12 months [X42]. All three clouds now support channel private offers: AWS CPPO at a 0.5% uplift [X1], Microsoft MPO with no fee to the channel partner in 36 markets [X4][X15], and Google reseller private offers through the Partner Network Resale Subprogram [X11]. An ISV without a reseller-offer motion is leaving the fastest-growing slice of marketplace volume to competitors.

5. **Microsoft made marketplace its co-sell engine for FY27.** Partner Reported ACR no longer works as a broad co-sell mechanism, and Marketplace Billed Sales is the recognized path (announced 2026-07-10) [X15]. ISV Success, Marketplace Rewards, Azure IP co-sell and certified software designations were folded into **Frontier Accelerate for Marketplace**, launched September 2026, with existing partners moving over automatically at renewal [X15][X16]. Azure IP co-sell eligibility still requires $100K of ACR or Marketplace Billed Sales over the trailing 12 months plus Azure technical validation [X14].

6. **AWS now scores every co-sell opportunity by machine.** Since 2026-06-16, Partner Central agents assign an **Opportunity Quality Score** and route each deal to one of three motions: AWS field-engaged, agent-engaged or partner-led [X30][X33]. Since 2026-07-01, an opportunity cannot reach Committed or Launched unless an AWS Marketplace solution, marketplace product or partner solution is attached [X31]. Low-quality ACE submissions do not reach sellers any more. Data quality now decides whether AWS engages at all.

7. **Google rebuilt its partner program around measured outcomes.** Partner Advantage gave way to **Google Cloud Partner Network** (announced 2025-12-16, launched Q1 2026 with a 6-month transition): tiers Select, Premier and Diamond; Competency and Advanced Competency replace specializations; tier and competency progress is tracked automatically from closed-won pre-sales and post-sales contributions [X26]. Tier thresholds are not published [X25]. Google's co-sell registration is the lightest of the three: no published opportunity lifecycle, and the private offer does most of the coordinating [X22][X24].

8. **Seller compensation is the "why would a rep care" answer, and it runs through the marketplace on all three clouds.** AWS sellers get quota retirement on partner SaaS sold as marketplace private offers (the SaaS Co-Sell Benefit, live since January 2025, for SaaS running 100% on AWS) [X20][X21]. Microsoft recognizes Marketplace Billed Sales [X15], and one partner reported FY27 marketplace seller incentives up 55% year over year [X18]. Google has described quota attainment for most marketplace solutions plus SPIFFs on closed co-sell deals [X65] (source dated 2024-04, unverified). **A direct-billed deal gives the hyperscaler rep nothing.**

9. **Each cloud's funding is now tied to the marketplace or to AI workloads.** AWS: Marketplace Private Offer Promotion Program (customer credits based on TCV, self-service, next-business-day approval) [X29], ISV Workload Migration Program credits paid through Marketplace, an extra $25K MDF for agentic AI categories, and the new Partner Greenfield Program [X28]. Microsoft: Frontier Accelerate engagements of up to $250K for migration and up to $100K for AI build-and-publish on the marketplace path (both VENDOR-reported), with $30K in Azure credits in the premium tier [X16][X17]. Google: MCCP customer credits of 3% of annualized GTV, capped at $250K per transaction, for first-time purchases [X13], plus a $750M agentic AI partner fund announced at Next 2026 [X27].

10. **Each hyperscaler returns several dollars of partner revenue per dollar of its own, per studies each one commissioned.** AWS: up to $7.13 per $1 for "Expert" partners (Omdia PEM 2025) [X45]. Microsoft: $8.45 for services partners and $10.93 for software partners (IDC) [X46]. Google: $7.05 (Canalys, January 2025) [X47]. All three were commissioned by the hyperscaler, so use them to frame an opportunity, not to forecast.

11. **Multi-cloud companies do far better on marketplace than single-cloud companies.** Tackle reports marketplace transactions at 29% of revenue for multi-cloud organizations versus 3% for single-cloud [X43] (VENDOR, and the causation likely runs both ways). The practical point: one listing in one cloud with no co-sell cadence is the most common zero-pipeline pattern, and a second cloud on the same weak process will not fix it.

12. **The ops tooling is consolidating and adding AI agents, so pick for CRM fit and roadmap stability.** AppDirect agreed to acquire Tackle (announced 2025-12-01) [X56]. Clazar shipped an MCP server (2026-08-21) [X67a]. AWS exposes Partner Central through five APIs (Selling, Account, Benefits, Channel, Revenue Measurement) [X34] and an MCP server for its agents [X30]. Microsoft exposes a Partner Center agent endpoint [X15]. Google added programmatic private offers to the Cloud Commerce Producer API on 2026-07-24 [X37]. Crossbeam's Open Data Partners now include AWS, GCP and Microsoft as mappable "is a customer of" populations with product-level detail, built from public signals [X52].

---

## 0. Program map and vocabulary

### 0.1 The layered model, side by side

| Layer | AWS | Microsoft | Google Cloud |
|---|---|---|---|
| Org membership | AWS Partner Network (APN), Partner Central now inside the AWS Management Console with IAM access [X28] | Microsoft AI Cloud Partner Program (MAICPP), Partner Center [X14] | Google Cloud Partner Network (from Q1 2026; replaced Partner Advantage) [X26] |
| Path / status | Software Path: Registered > Validated > Differentiated (renamed from "ISV Partner Path") [X39]; Services Path tiers | Solutions Partner designations; FY27 simplified to Cloud and AI Platform, AI Business Solutions, Security; "Solutions Partner with certified software" for ISVs [X18][X15] | Tiers Select > Premier > Diamond; paths co-sell, services, technology [X26][X25] |
| Technical validation | Foundational Technical Review (FTR), valid 2 years, via SOC 2 Type II report or Well-Architected review [X39] | Azure technical validation for IP co-sell; "primarily platformed in Azure" [X14] | Architecture review for co-sell path (per flashdba) [X23]; Competency "Capacity" plus "Capability" [X26] |
| Co-sell eligibility | ACE eligibility; ISV Accelerate (5 launched plus 15 qualified ACE opps in 12 months, GA marketplace listing, Validated or Differentiated) [X19][X21] | Co-sell ready > Azure IP co-sell eligible ($100K ACR or MBS trailing 12 months, transactable offer, technical validation) [X14] | Marketplace listing live; Partner Network membership; no published gate [X22][X24] |
| Opportunity execution | ACE in Partner Central; Selling API; Opportunity Quality Score [X30][X34] | Partner Center Referrals; co-sell connectors for Salesforce and Dynamics [X36] | Partner Network Hub opportunity registration [X38] |
| Incentives and funding | MDF, MAP, MPOPP, ISV WMP, BOX, Partner Greenfield Program [X28][X29] | Frontier Accelerate for Marketplace; Frontier Accelerate for Azure (formerly Azure Accelerate) [X16][X64] | MCCP, Partner funding, $750M agentic AI fund [X13][X27] |
| Channel execution | CPPO (Channel Partner Private Offer) [X1] | MPO (Multiparty Private Offer) [X4] | Reseller private offers, called MCPO (Marketplace Channel Private Offers) in partner comms [X11][X13] |

### 0.2 Retired or renamed names that still show up on the web

| Old name | Current name | Cloud | Source |
|---|---|---|---|
| Partner Advantage (tiers Partner, Premier; "specializations") | Google Cloud Partner Network (Select, Premier, Diamond; Competency, Advanced Competency) | Google | [X26] |
| ISV Partner Path | Software Path | AWS | [X39] |
| Azure Marketplace + AppSource | Microsoft Marketplace (launched September 2025) | Microsoft | [X59] |
| ISV Success, Marketplace Rewards, Azure IP co-sell (as separate offerings) | Frontier Accelerate for Marketplace (September 2026) | Microsoft | [X15][X16] |
| Azure Accelerate (FY26) | Frontier Accelerate for Azure (FY27) | Microsoft | [X64] |
| SaaS Revenue Recognition Program | Folded into the SaaS Co-Sell Benefit (January 2025) | AWS | [X20] |
| EDP (Enterprise Discount Program) | Often called PPA (Private Pricing Agreement) now; both terms in use | AWS | [X10][X68] |
| Microsoft "Copilot" specialization | Microsoft 365 Copilot specialization, measured on paid MAU | Microsoft | [X15] |
| Partner Reported ACR as a broad co-sell mechanism | Marketplace-first co-sell, Marketplace Billed Sales | Microsoft | [X15] |

### 0.3 Cross-cloud glossary

| Term | Meaning | Cloud |
|---|---|---|
| ACE | APN Customer Engagements, AWS co-sell opportunity program in Partner Central | AWS |
| OQS | Opportunity Quality Score, automated AI score on each ACE submission; drives engagement motion | AWS [X30] |
| ISVA | ISV Accelerate, AWS flagship ISV co-sell program | AWS [X19] |
| SCB | SaaS Co-Sell Benefit, AWS seller quota retirement on partner SaaS private offers | AWS [X20] |
| CPPO | Channel Partner Private Offer, ISV authorizes a reseller to sell its listing via private offer | AWS [X1] |
| EDP / PPA | Customer's committed-spend agreement with AWS | AWS |
| MPOPP | Marketplace Private Offer Promotion Program, AWS credits to buyers of participating ISVs | AWS [X29] |
| MACC | Microsoft Azure Consumption Commitment | Microsoft [X8] |
| Azure benefit eligible | Badge marking offers whose purchase decrements MACC 100% | Microsoft [X8] |
| IPCS / IP co-sell eligible | Status above co-sell ready; prerequisite for MACC eligibility | Microsoft [X14] |
| MBS | Marketplace Billed Sales | Microsoft [X14][X15] |
| ACR | Azure Consumed Revenue | Microsoft [X14] |
| MPO | Multiparty Private Offer (ISV > channel partner > customer) | Microsoft [X4] |
| SDC | Software Development Company, Microsoft's current term for ISV | Microsoft [X15] |
| MCPO | Marketplace Channel Private Offer | Google [X12][X13] |
| MCCP | Marketplace Customer Credit Program, up to 3% credits on first-time ISV purchases | Google [X13] |
| Vendor Net Revenue Schedule | Google's TCV-based fee schedule, effective 2025-04-21 | Google [X5] |
| Native renewal / migration / channel shift | Google deal types that earn the 1.5% fee | Google [X5] |
| Commit drawdown | Marketplace purchase decrementing a customer's cloud commitment | All |
| Cloud GTM platform | Third-party software that automates listings, offers, co-sell sync (Tackle, Clazar, Suger, Labra, WorkSpan and others) | All |

---

## 1. Fiscal calendar, org and where decisions get made

### 1.1 Fiscal years and planning moments

| | AWS | Microsoft | Google Cloud |
|---|---|---|---|
| Fiscal year | Calendar year (Amazon reports Jan to Dec) [X70] | July 1 to June 30; FY27 runs 2026-07-01 to 2027-06-30 [X15][X17] | Calendar year (Alphabet reports Jan to Dec) [X71] |
| Planning / kickoff | Program changes announced at re:Invent (Dec) for the next calendar year [X28] | MCAPS Start (July) sets FY priorities and incentives [X18] | Partner program changes announced at Next (April) and year-end blog posts [X26][X27] |
| Flagship event | re:Invent 2026: Nov 30 to Dec 4, Las Vegas [X60] | Ignite 2026: Nov 17 to 20 [X61] | Next 2027: Apr 13 to 15, Mandalay Bay, Las Vegas [X62] (Next 2026 was Apr 22 to 24 per coverage [X27]) |
| Quarter-end pressure | Mar, Jun, Sep, Dec | Sep, Dec, Mar, Jun (Q4 = Apr to Jun) | Mar, Jun, Sep, Dec |
| Best window to pitch a joint plan | Oct to Nov (before re:Invent and annual account planning) | May to June (before MCAPS Start) and early July | Jan to Mar (before Next) |

Independent channel events: Canalys Forums EMEA 2026, Oct 6 to 8, Barcelona [X63]; the Americas and APAC 2026 dates were not confirmed (section 14).

### 1.2 Field roles a partner meets

| Function | AWS | Microsoft | Google Cloud |
|---|---|---|---|
| Your partner manager | PDM (Partner Development Manager); Tackle reports an AWS "3PI PDM pilot" using third parties for ISV onboarding [X33a] | PDM / Partner Development Manager; ISV engagement via Frontier Accelerate engagement managers [X16] | Partner Account Manager / Partner Engineer (names vary) [UNVERIFIED] |
| Field seller | AM / AE (account manager) | AE / Account Executive, Specialist | FSR / Customer Engineer |
| Co-sell routing | Partner Sales Manager plus Partner Central agents (OQS) [X30] | Partner Development / co-sell desk (IPCosellDesk@microsoft.com) [X15] | Partner team plus Partner Network Hub | <!-- VALIDATE-OK[person-address]: published role mailbox, not a person -->
| Marketplace BD | AWS Marketplace BD / Channel team | Marketplace team (Commercial Marketplace) | Cloud Marketplace ISV GTM team [X65] |

### 1.3 How sellers are paid on partner and marketplace deals

| | AWS | Microsoft | Google Cloud |
|---|---|---|---|
| Mechanism | SaaS Co-Sell Benefit: AWS sellers get quota retirement when they co-sell partner SaaS/PaaS through AWS Marketplace private offers (live January 2025) [X20][X21]; ISVA page lists "seller incentives for Private Offers" [X19] | Marketplace Billed Sales recognized for IP co-sell; MACC decremented 100% on Azure benefit eligible offers [X15][X8]; FY27 marketplace seller incentives reported up 55% YoY, Azure up 35% [X18] | Quota attainment on most marketplace solutions; SPIFFs on closed co-sell deals [X65, UNVERIFIED, source dated 2024-04] |
| Hosting condition | Solution runs 100% on AWS [X20] | Primarily platformed in Azure; Azure-exclusive license for MACC [X14][X8] | Running on Google Cloud for commit drawdown [X7] |
| What kills it | Direct-billed deal; product not Deployed on AWS | Offer not transactable; not IP co-sell eligible; hybrid or on-prem license | Not on marketplace; not running on GCP |

**Rule of thumb for Alex:** the seller's reason to care, in order, is (1) the deal retires the customer's commit, (2) it retires the seller's quota, (3) it lands a workload. Build the pitch to the seller in that order.

---

## 2. Navigating the portal(s): surface comparison

| Need | AWS | Microsoft | Google Cloud |
|---|---|---|---|
| Partner portal | AWS Partner Central, now in the AWS Management Console with IAM roles [X28] | Partner Center (partner.microsoft.com) | Partner Network Hub [X38] |
| Marketplace seller portal | AWS Marketplace Management Portal | Partner Center > Marketplace offers | Producer Portal [X37] |
| Opportunity API | Partner Central Selling API (`CreateOpportunity`, `StartEngagementFromOpportunityTask`, `ListEngagementInvitations`, EventBridge events) [X34][X24] | Partner Center Referrals API with webhooks [X36] | No public co-sell opportunity API found; integrators get an "Integrator" role on Partner Network Hub via service account [X38] |
| Other APIs | Account, Benefits, Channel, Revenue Measurement APIs [X34]; AWS Marketplace Catalog API | Partner Center agent endpoint (June 2026) [X15]; MPO API [X4] | Cloud Commerce Producer API (private offers since 2026-07-24); Partner Procurement API [X37] |
| Native CRM connector | AWS Partner CRM Connector on Salesforce AppExchange, uses Partner Central API [X35] | Partner Center Referrals Connector for Salesforce and for Dynamics 365, built on Power Automate [X36] | None found; use a Cloud GTM platform [X22] |
| AI agent | Partner Central agents, Partner Central MCP server; usable from Amazon Quick, Kiro or your CRM [X30] | Partner Center AI assistant across 12 workspaces; agent endpoint for integration [X15] | AI-powered automatic tier and competency tracking; Earnings Hub; SOW Analyzer [X26] |
| Change feed | What's New RSS, APN blog RSS, Marketplace blog RSS (registry Tier 0) | Monthly Partner Center announcements page; Tech Community RSS | Marketplace partner release notes RSS; Cloud blog partners RSS |

---

## 3. Registration: cross-cloud sequencing

Per-cloud steps live in the per-cloud files. Cross-cloud rules:

1. **Run membership and marketplace seller registration in parallel, not in sequence.** On AWS they are separate processes that should run in parallel [X39]; the same holds on Microsoft (MAICPP plus Marketplace enrollment) [X16] and Google (Partner Network plus vendor account plus payment profile) [X25].
2. **Start the long-lead item first.** AWS: the FTR, which needs a SOC 2 Type II report or a Well-Architected review [X39]. Microsoft: the $100K trailing ACR or MBS for IP co-sell eligibility [X14]. Google: the marketplace listing, which is the prerequisite for co-sell, private offers, commit drawdown and MCCP [X25].
3. **Decide hosting before you apply.** Drawdown and seller benefits require your workload to run on that cloud [X7][X8][X9][X20]. A product hosted on AWS can list on Microsoft and Google, but it will not retire a MACC or a Google commit.
4. **Use one legal entity and one tax/banking setup across clouds where possible.** Microsoft MPO and AWS EMEA invoicing entities add KYC work (Suger covered AWS EMEA SARL KYC on 2026-09-24) [X67b].

| Milestone | AWS typical | Microsoft typical | Google typical |
|---|---|---|---|
| Membership | Days | Days | Days |
| Transactable listing live | Weeks (vendor-reported) | Weeks | Weeks |
| Co-sell eligible | Months: ISVA needs 5 launched plus 15 qualified ACE opps in trailing 12 months [X19] | Co-sell ready in weeks; IP co-sell eligible once $100K ACR or MBS in trailing 12 months [X14] | At listing; no published gate [X24] |
| Committed-spend eligible | Deployed on AWS badge [X9] | Azure benefit eligible badge (requires IP co-sell eligible) [X8][X14] | Running on GCP; resale only if the vendor opts into resale [X7] |

Timings marked "weeks" and "months" are practitioner estimates, not published SLAs.

---

## 4. Tiers and co-sell eligibility gates (side by side)

### 4.1 Program name and tiers

| | AWS | Microsoft | Google Cloud |
|---|---|---|---|
| Program | AWS Partner Network | Microsoft AI Cloud Partner Program | Google Cloud Partner Network |
| ISV track | Software Path: Registered, Validated (FTR passed), Differentiated [X39] | Solutions Partner with certified software designations; Frontier Accelerate for Marketplace stages Build and Publish > Grow > Differentiate [X16] | Technology and co-sell paths within Select, Premier, Diamond [X25][X26] |
| Services track | Services Path tiers (see aws file) | Solutions Partner designations (FY27: Cloud and AI Platform, AI Business Solutions, Security) plus specializations; new Frontier Partner Specialization [X18][X15] | Services path; Competency and Advanced Competency [X26] |
| Top distinction | Differentiated / Premier-tier services | Frontier Partner Specialization (FY27) [X18] | Diamond (new, intentionally selective) [X26] |
| Thresholds published? | Yes, in Partner Central docs (see aws file) | Yes, on Learn (specializations have ACR thresholds, e.g. $15K ACR across 3 customers for the merged Analytics specialization) [X15] | No: Google does not publish tier thresholds [X25] |

### 4.2 Entry requirements

| | AWS | Microsoft | Google Cloud |
|---|---|---|---|
| To join | Partner Central registration (console-based, IAM) [X28] | MAICPP enrollment, PartnerID [X14] | Partner Network application [X25] |
| To sell on marketplace | Marketplace seller registration; public SaaS listing no longer requires AWS hosting since 2025-05-01 [X9] | Marketplace enrollment in Partner Center; transactable offer [X14] | Partner Network membership in good standing, vendor account, valid payment profile; no tier needed [X25] |
| Fee to join | Not published on the official pages fetched. Tackle cites a $2,500 onboarding fee with a $3,500 credit offset [X20] (VENDOR, UNVERIFIED) | Frontier Accelerate standard tier no cost; premium tier fee-based, amount not published on the fetched page [X16] | Not published |

### 4.3 Co-sell eligibility gates

| Gate | AWS (ISV Accelerate) [X19][X21] | Microsoft (Azure IP co-sell eligible) [X14] | Google (co-sell path) [X22][X24] |
|---|---|---|---|
| Listing | At least one GA product in AWS Marketplace | Offer live and transactable (required for new offers since 2023-07-11) | Marketplace listing live |
| Technical | Validated or Differentiated (FTR) | Azure technical validation; primarily platformed in Azure; reference architecture diagram for SaaS | Architecture review per practitioner guides; not published officially |
| Revenue | About $2K recognized AWS account revenue at enrollment | $100K ACR or MBS over trailing 12 months (org level; credits and ACO excluded) | None published |
| Pipeline | 5 launched plus 15 qualified ACE opps in trailing 12 months (For Visibility Only excluded) [X21] | None for status; per-deal registration minimum $25K for IP co-sell deals and 72 hours between create and mark won [X24] | None published |
| Other | ACE eligibility; Payee Central account; "Co-Selling with AWS" module [X19][X21] | Sales contact per geography; complete business profile | Basic profile complete; competency activity initiated [X22] |

---

## 5. Marketplace (side by side)

### 5.1 Fees, standard and reduced

| Deal type | AWS [X1] | Microsoft [X2][X3] | Google [X5] |
|---|---|---|---|
| Public SaaS | 3% | 3% | 3% (standard offer) |
| Private offer, new, TCV under $1M | 3% | 3% | 3% |
| Private offer, new, $1M to under $10M | 2% | 3% | 2% |
| Private offer, new, $10M+ | 1.5% | 3% | 1.5% |
| Renewal | 1.5% (all renewals) | 1.5% (50% discount; private offers created on or after 2024-10-01; attested at creation, not retroactive) | 1.5% (native renewal: prior term at least 9 months, restart within 90 days; amendments must raise duration and TCV by at least 60%) |
| Migration from off-marketplace / channel shift | Standard ladder | 1.5% if attested as renewal of an existing paid agreement or upsell to an existing paid customer [X3] | 1.5% (migration or channel shift) |
| Server / AMI / container | 20% public [X1] | 3% VM, container, managed app [X2] | Usage-only post-offer shown at 97% vendor net in Google scenarios [X6] |
| Professional services | 0.5% on private offers; 0% base when part of a qualifying multi-product solution [X1] | 3% [X2] | Excluded from commit drawdown [X7]; fee not confirmed in fetched pages |
| Channel / reseller uplift | CPPO +0.5% on top of the standard fee [X1] | MPO: no fee to the channel partner; ISV pays the standard fee [X4] | ISV sets the reseller discount; fee schedule treats channel shifts at 1.5% [X5][X11] |
| Regional add-on | South Korea +1% from 2025-04-01 [X1] | None found | None found |
| Effective since | 2024-01-05 | Renewal discount from 2024-10-01; page updated 2026-03-25 | 2025-04-21 (offers created before keep legacy terms until term end) |

### 5.2 Private offer and channel offer models

| | AWS CPPO | Microsoft MPO | Google reseller private offers (MCPO) |
|---|---|---|---|
| Flow | ISV authorizes reseller; reseller creates private offer to buyer | ISV creates MPO and sends it to a channel partner; partner adds margin and extends it to the customer; customer accepts in the Azure portal [X4] | ISV turns on reselling and issues a private offer plan to the reseller; reseller creates the customer private offer in Partner Sales Console [X11] | <!-- VALIDATE-OK[economics]: public hyperscaler or vendor reseller economics, not Forecastable's -->
| Who can resell | AWS channel partners authorized by ISV | Authorized channel partners in MAICPP | Partners in the Resale Subprogram of Partner Network [X11] |
| Geography | Per aws file | 36 markets as of 2026-07-16 (added Australia, Japan, South Africa; Canada customers only) [X15][X4] | Not specified on fetched page [X11] |
| Commit drawdown | Per EDP terms; see section 5.3 | Counts toward MACC if the product is IP co-sell eligible / Azure benefit eligible [X4] | Resale purchases excluded unless the vendor opts into the resale program [X7]; 100% drawdown for MCPO announced 2025 [X13] (conflict, see section 14) |
| Recent additions | Express private offers: pre-set pricing rules so AWS sellers can route customers who get offers in minutes (2026-06-16) [X32] | Customer "Request private offer" button (2026-07-20); custom contract terms up to 10 years (GA 2026-07-06); amendable offers [X15] | Programmatic private offers via Cloud Commerce Producer API (2026-07-24) [X37] |

### 5.3 Committed spend drawdown: exactly what counts

| | AWS EDP / PPA | Microsoft MACC | Google commit |
|---|---|---|---|
| Rate | 100% of qualifying SaaS spend, capped at 25% of annual commitment [X10] (INDEPENDENT, 2025-02; EDP terms are private contracts, so confirm per customer) | 100% of pretax purchase [X8] | 100% of spend on eligible Marketplace services [X7] |
| Product must | Be 100% deployed on AWS (Deployed on AWS badge) from 2025-05-01; application and control planes on AWS [X9][X10] | Carry the Azure benefit eligible badge (requires Azure IP co-sell eligible) [X8][X14] | Be actively running on Google Cloud infrastructure [X7] |
| Buyer must | Buy via AWS Marketplace under the account tied to the agreement | Buy via Azure portal with an Azure subscription tied to the MACC agreement; license used exclusively in Azure [X8] | Buy directly, or via reseller only if the vendor opted into resale [X7] |
| Excluded | Professional services [X10] | Purchases with Azure prepayment; credit-card purchases on Microsoft Marketplace; hybrid or on-prem licenses; some pre-benefit agreements [X8] | Professional services; Google Maps, Google Ads; non-Google-Cloud-based services; certain reseller purchases; products owned by the purchaser or affiliates [X7] |
| Channel purchase | CPPO: follow EDP terms [UNVERIFIED specifics] | MPO counts when co-sell eligible [X4] | See conflict in section 14 |

**What to tell a customer's procurement team:** ask three questions. (1) Which cloud holds your largest commit, and how much is unburned? (2) Does your agreement cap marketplace drawdown? (3) Will you buy through the portal account tied to the commit? The answer decides which marketplace to transact on, whatever the ISV's default cloud is.

### 5.4 What makes a listing produce pipeline (cross-cloud)

1. Transactable plus private-offer-ready, not "contact me" [X14][X25].
2. Commit-eligible (badge) on the cloud where the customer's money sits [X8][X9].
3. Attached to every co-sell opportunity: AWS now blocks Committed or Launched stages without it [X31].
4. Priced for private offers first: most volume is private [X58].
5. Trials: Microsoft expanded trials to 1 to 180 days with badges and filters (2026-07-24) [X15].
6. A channel-offer motion: see truth 4.

---

## 6. Co-sell (side by side)

| | AWS | Microsoft | Google Cloud |
|---|---|---|---|
| System | ACE in Partner Central [X24] | Partner Center Referrals [X24] | Partner Network Hub [X38] |
| Published status model | Yes: ReviewStatus plus sales stages [X24] | Yes: deal types plus numeric sales stages [X24] | Not published [X24] |
| Submission prerequisite | At least one associated solution or product; submitting takes `StartEngagementFromOpportunityTask` after create [X24] | At least one co-sell-ready solution [X24] | Marketplace listing and offer capability [X24] |
| Quality gate | Opportunity Quality Score routes to AWS field-engaged, agent-engaged or partner-led [X30] | Eligibility rules; 14-day window for seller decision [X24] | Not published |
| Deal minimum | None published [X24] | $25K for IP co-sell registration [X24] | None published |
| Editability | Locked during submission; only 11 fields editable in Action Required [X24] | Terminal states cannot be modified [X24] | Offer amendment rules apply [X24] |
| Stage rule | Marketplace solution, product or partner solution must be attached to reach Committed or Launched (from 2026-07-01) [X31] | Co-sell engagement moved to Stage 1 (pre-requirements) in FY27 GTM [X18] | Private offer is the coordination vehicle [X24] |
| Inbound referrals | Engagement invitations via API [X34] | Referrals from Microsoft sellers and marketplace leads; "Request private offer" requests flow into lead management [X15] | Via Partner Network Hub |

**Cross-cloud engagement playbook that works (synthesis):** lead with the customer's commit position and the seller's comp mechanism, bring a named account list built from overlap data (section 9 below), register only deals you can describe with the customer's pain, the hyperscaler services consumed and a next step, and close through a private offer on the cloud that holds the commit.

---

## 7. Incentives and funding (side by side, current published amounts)

| Category | AWS | Microsoft | Google Cloud |
|---|---|---|---|
| Flagship ISV program | ISV Accelerate [X19] | Frontier Accelerate for Marketplace (Sept 2026; replaces ISV Success, Marketplace Rewards, Azure IP co-sell packaging) [X15][X16] | No separate ISV program found; ISVs run on co-sell and technology paths [X26] |
| Buyer credits on marketplace deals | MPOPP: AWS Promotional Credits to buyers based on TCV and program rates; self-service via Partner Funding Portal; automated next-business-day approval (2025-08-12) [X29] | Not a direct equivalent found; Azure sponsorship for trials in Frontier Accelerate standard [X16] | MCCP: 3% of annualized GTV in credits, paid quarterly, capped at $250K per transaction, first-time purchase, deal registration required [X13] |
| Migration / workload funds | MAP (now covering digital transformation and generative/agentic AI); ISV Workload Migration Program with credits paid through Marketplace [X28] | Frontier Accelerate engagements: assessment up to $25K; migration up to $250K (High Value Migration tier above $500K ACR); up to $275K per project combined [X17] | Rapid migration programs (see google-cloud file) |
| AI build funds | Additional $25K MDF for Agentic AI categories (on top of existing $50K MDF) [X28] | AI Build and Publish: up to $100K on the marketplace path, up to $125K for the Copilot Agent Store [X17] | $750M partner fund of credits, co-investment, training subsidies and GTM funding for agentic AI (Next 2026) [X27] |
| Build credits | POC credits (see aws file) | $30K in Azure credits in the Frontier Accelerate premium tier [X16] | Not confirmed in fetched pages |
| MDF | Up to $50K industry MDF in BOX; $50K MDF for Amazon Connect implementations [X28] | See microsoft file | See google-cloud file |
| New co-investment | Partner Greenfield Program: multi-year co-investment for Migration/Modernization, GenAI, Security practices [X28] | Frontier Accelerate for Azure (Cloud Accelerate Factory, zero-cost deployment support for 30+ Azure services) [X64] | Diamond tier benefits (not published) |
| Where the guide lives | AWS Partner Funding Benefits Guide, login-gated in Partner Central [X29] | Partner Center and partner.microsoft.com; Frontier Accelerate resources collection [X16] | Partner Network Hub, login-gated |

Microsoft amounts marked [X17] are from a VENDOR summary (Noteworthy, 2026-09-08). The official Frontier Accelerate page confirms the structure and the $30K premium credit, not every engagement cap [X16].

---

## 8. What changed in 2025 to 2026 and what is announced next (cross-cloud, newest first)

| Date | Cloud | Change | Source |
|---|---|---|---|
| 2026-09-25 | AWS | Tackle explains Opportunity Quality Score economics (VENDOR) | [X33] |
| 2026-09 | Microsoft | Frontier Accelerate for Marketplace launches | [X15][X16] |
| 2026-08-21 | Vendor | Clazar ships MCP server for cloud partnerships data | [X67a] |
| 2026-08-19 | Crossbeam | Managed Offline Partners (AWS, Microsoft, Google Cloud, Salesforce, SAP) stop receiving data updates; Open Data Partners recommended | [X53] |
| 2026-07-24 | Google | Cloud Commerce Producer API supports programmatic private offers | [X37] |
| 2026-07-24 | Microsoft | Marketplace trials expanded (1 to 180 days, badges, analytics) | [X15] |
| 2026-07-20 | Microsoft | "Request private offer" on listings; Partner Center agent endpoint | [X15] |
| 2026-07-16 | Microsoft | MPO adds Australia, Japan, South Africa (36 markets) | [X15] |
| 2026-07-10 | Microsoft | Azure IP co-sell goes marketplace-first; PRACR no longer a broad co-sell mechanism | [X15] |
| 2026-07-06 | Microsoft | Custom contract lengths up to 10 years GA (SaaS, professional services) | [X15] |
| 2026-07-01 | AWS | Marketplace listings linkable to co-sell opportunities; attachment required for Committed or Launched | [X31] |
| 2026-06-16 | AWS | Partner Central agents: OQS and three engagement motions; MCP server | [X30] |
| 2026-06-16 | AWS | Express private offers for partners | [X32] |
| 2026-04-22 | Google | $750M agentic AI partner fund at Next 2026 | [X27] |
| 2026 Q1 | Google | Google Cloud Partner Network live; 6-month transition | [X26] |
| 2025-12-16 | Google | Partner Network announced (Select, Premier, Diamond) | [X26] |
| 2025-12-01 | Vendor | AppDirect to acquire Tackle | [X56] |
| 2025-12-01 | AWS | 2026 partner innovations: Partner Central in console, APIs, Greenfield Program, agentic MDF | [X28] |
| 2025-11-06 | Crossbeam | Managed Offline Partners for AWS, Google Cloud, Microsoft; MCP server; Smarter Matching using marketplace attributes | [X54] |
| 2025-10-06 | Analyst | Omdia: $163B marketplace sales by 2030 | [X40] |
| 2025-09 | Microsoft | Microsoft Marketplace replaces Azure Marketplace and AppSource | [X59] |
| 2025-08-12 | AWS | MPOPP launched | [X29] |
| 2025-06-09 | Google | MCPO commit drawdown simplification effective (per ChannelInsider) | [X12] |
| 2025-05-01 | AWS | SaaS catalog opens to all hosting; Deployed on AWS badge; commitment benefits limited to 100% AWS-deployed | [X9][X10] |
| 2025-04-21 | Google | Vendor Net Revenue Schedule (3% / 2% / 1.5%) | [X5] |
| 2025-04-01 | AWS | South Korea +1% regional fee | [X1] |
| 2025-01 | AWS | SaaS Co-Sell Benefit live (quota retirement on marketplace private offers) | [X20] |

**Announced next:** CSP growth margins for select AI workloads go live 2026-10-01 (Microsoft) [X15]; Agentic Security specialization (Microsoft, FY27, design phase) [X15]; AWS Marketing Central agents during 2026 [X28]; re:Invent (Nov 30 to Dec 4) will carry AWS's 2027 program changes [X60]. <!-- VALIDATE-OK[economics]: public hyperscaler or vendor reseller economics, not Forecastable's -->

---

## 9. Diagnostics: common cross-cloud failure modes and the fix

| # | Failure mode | How to detect | Fix |
|---|---|---|---|
| 1 | Listed on the cloud where the product runs, not where the customers' commits sit | Map top 50 target accounts to their primary cloud using Crossbeam Open Data Partners (AWS, GCP, Microsoft populations) [X52]; compare to your listing footprint | Prioritize the cloud that holds the most target-account overlap and where you can meet the hosting rule; see section 12 |
| 2 | Listing not commit-eligible | No Deployed on AWS badge [X9]; no Azure benefit eligible badge [X8]; workload not on GCP [X7] | Either host a deployment on that cloud or stop pitching drawdown there |
| 3 | Direct-billed deals, so the hyperscaler seller gets no credit | Share of hyperscaler-influenced deals closed off-marketplace | Default every co-sell deal to a private offer; seller comp only moves on marketplace transactions [X20][X15] |
| 4 | Low-quality ACE submissions die at OQS | Share of opps routed "partner-led"; OQS trend (surfaced in some GTM platforms) [X30][X33] | Submit fewer, richer opportunities: customer pain, AWS services consumed, next step, attached marketplace listing [X31] |
| 5 | Microsoft: co-sell ready but not IP co-sell eligible | Trailing 12-month ACR plus MBS under $100K [X14] | Route early deals through marketplace so MBS accrues; enroll in Frontier Accelerate [X16] |
| 6 | Microsoft: registrations rejected | Deals under $25K; marked won within 72 hours of creation [X24] | Register earlier (Stage 1) and only at $25K+ [X18][X24] |
| 7 | Google: no motion because there is no gate | No private offers issued; no MCCP registrations | Treat the private offer as the co-sell object; register for MCCP on first-time buyers [X13][X24] |
| 8 | No channel-offer path | Zero CPPO/MPO/reseller offers while resellers touch deals | Turn on resale on all three; set standard reseller discount bands [X1][X4][X11] |
| 9 | Three clouds, three processes, no owner | Separate spreadsheets per cloud; no weekly review | One cadence (section 10) and one system of record in CRM through a Cloud GTM platform or native connectors |
| 10 | RevOps blocks marketplace | Finance cannot reconcile disbursements; 42% of RevOps teams remain unconvinced [X44] | Put disbursement reports into the data warehouse (Google disbursement reports in BigQuery [X37]); agree on revenue recognition before launch |
| 11 | Funding left unclaimed | No MPOPP, MCCP or Frontier Accelerate claims in the last quarter | Build claims into the private-offer checklist: every eligible first-time deal gets its credit program attached [X29][X13][X17] |
| 12 | Chasing tier badges instead of pipeline | Hours spent on designations vs pipeline created | Google now measures outcomes automatically [X26]; Microsoft moved to audits and usage-based metrics [X15]. Pursue tiers only when they unlock a named benefit you will use |

---

## 10. KPIs and one operating cadence across three clouds

### 10.1 KPIs (same definitions on all three clouds)

| KPI | Definition | Benchmark (label) |
|---|---|---|
| Marketplace share of new bookings | Marketplace-transacted bookings / total new bookings | 22% of ISVs above 20% of revenue; 41% below 5% [X44] (VENDOR survey) |
| Co-sell influenced share | Deals with hyperscaler engagement / total deals | Multi-cloud firms expect 39% of next year's deals co-sell influenced vs 18% for single-cloud [X43] (VENDOR) |
| Seller activation | % of your AEs who closed at least 1 marketplace deal in 12 months | 28% average; 36% where market intelligence data is used heavily [X43] (VENDOR) |
| Channel share of marketplace | Deals via CPPO/MPO/MCPO / all marketplace deals | 27% now, 37% expected in 12 months [X42] (VENDOR) |
| Commit coverage | % of target accounts whose largest commit is on a cloud where you are commit-eligible | No benchmark published |
| OQS mix (AWS) | Share of submitted opps in field-engaged vs agent-engaged vs partner-led | No benchmark published [X30] |
| Win rate lift | Win rate with partner overlap vs without | Crossbeam: 53% more deals closed and 27% shorter cycles when sales and partnerships collaborate [X55] (VENDOR, undated); computable per org in Crossbeam Performance Dashboard [X66] |

### 10.2 The cadence (one rhythm, three clouds)

| Rhythm | What happens | Inputs | Output |
|---|---|---|---|
| Weekly (30 min) | Pipeline review of all co-sell opps across ACE, Partner Center and Partner Network Hub in one CRM view; decide which to register, which to convert to private offers, which need seller outreach | Cloud GTM platform or native connector sync; Crossbeam Deal Navigator overlap on open opps | Registrations submitted; private offers requested; 3 seller asks |
| Biweekly | Seller touchpoints per cloud: bring 5 named accounts with overlap evidence and commit position | Crossbeam Open Data Partner lists (AWS, GCP, Microsoft) with product-level data [X52] | Account plans shared with hyperscaler reps |
| Monthly | Program health: eligibility status (ISVA thresholds, IP co-sell $100K, Google tier progress), fee tier outcomes, funding claims, change-feed review (registry Tier 0) | Portal scorecards; this file's section 8 | Health report; funding claims filed |
| Quarterly | Cloud mix decision: shift effort to the cloud with best pipeline per hour; align to hyperscaler quarter-end | KPIs above; hyperscaler fiscal calendar (Microsoft Q4 = Apr to Jun) | Reallocation; QBR with each PDM |
| Annually | Plan to each hyperscaler's planning moment: re:Invent (AWS), MCAPS Start (Microsoft), Next (Google) | Section 1.1 | Joint business plans |

---

## 11. By partner type (cross-cloud priority)

| Partner type | First cloud | Why | First move |
|---|---|---|---|
| ISV SaaS, single-cloud hosted | The cloud you run on | Only that cloud gives commit drawdown and seller comp [X7][X8][X9][X20] | Transactable listing plus private offers; co-sell eligibility on that cloud |
| ISV SaaS, multi-cloud hosted | The cloud holding most target-account commits | Drawdown follows hosting on each cloud | Overlap-map targets by cloud; list on the top two |
| ISV, not hosted on any hyperscaler | AWS for listing reach only (open catalog since 2025-05-01) [X9] | No drawdown anywhere; marketplace is procurement convenience only | Decide whether a hosted deployment is worth it for drawdown |
| Services / SI | The cloud whose funding matches your practice | Funding is richest for migration and agentic AI on all three [X28][X17][X27] | Chase the designation or competency that unlocks the fund you will use |
| Reseller / MSP | Microsoft first (MPO, CSP growth margins from 2026-10-01) then AWS CPPO | Channel is the fastest-growing slice of marketplace [X41] | Get authorized for MPO, CPPO and Google Resale Subprogram | <!-- VALIDATE-OK[economics]: public hyperscaler or vendor reseller economics, not Forecastable's -->
| Startup ISV | Whichever cloud gave your credits; then add marketplace | Credits create hosting lock-in, and hosting drives drawdown | List early; private offers from the first enterprise deal |

---

## 12. Which hyperscaler to prioritize: the decision framework (for Alex)

### 12.1 The seven factors

Score each cloud 1 to 5 on each factor, multiply by weight, and total. Default weights suit a Series B to public B2B SaaS ISV. Reweight for services firms (funding and seller density count for more).

| # | Factor | Weight | How to measure | Where the data comes from |
|---|---|---|---|---|
| 1 | Customers' committed spend | 25% | Share of top-100 target accounts whose primary cloud is X; size of commits | Crossbeam Open Data Partners (AWS, GCP, Microsoft) with product-level adoption [X52]; customer procurement interviews; ask the PDM |
| 2 | Product architecture / hosting | 20% | Can you meet the hosting rule (100% on AWS, Azure-platformed, running on GCP)? Cost to add a deployment | Engineering; [X7][X8][X9][X14] |
| 3 | ICP overlap | 15% | Overlap of your ICP with the cloud's customer base, by segment and industry | Crossbeam overlaps; closed-won analysis; Partner Score (win rate, deal size, cycle vs baseline) [X66] |
| 4 | Seller density in your segment | 10% | Number of hyperscaler reps covering your ICP accounts; do they carry quota that your deal retires? | PDM; seller comp in section 1.3 |
| 5 | Program maturity for your type | 10% | Published gates, API surface, CRM connectors, funding clarity | Sections 2, 4, 7 |
| 6 | Time to co-sell eligible | 10% | Months from today to eligibility, given your current revenue and pipeline | Section 3; ISVA 5 plus 15 opps [X19]; IPCS $100K [X14]; Google at listing [X24] |
| 7 | Cost | 10% | Fees (now roughly equal) plus ops cost (tooling, headcount, listing engineering) plus hosting change cost | [X1][X2][X5][X58] |

### 12.2 Default tendencies (use to sanity-check the score, not to replace it)

| Situation | Usual answer | Condition that flips it |
|---|---|---|
| Enterprise ICP, product on AWS | AWS first | Target accounts are mostly Microsoft-committed (common in regulated, public sector, Microsoft 365-heavy enterprises) and you can run on Azure |
| Product built on Azure or sold alongside Microsoft 365 / Dynamics | Microsoft first | Deals under $25K cannot be registered for IP co-sell [X24]; you will not hit $100K MBS/ACR soon [X14] |
| Data, AI or analytics product on GCP; ICP digital-native | Google first | Need structured co-sell routing, which Google does not publish [X24] |
| Heavy reseller or MSP route to market | Microsoft (MPO, CSP) then AWS CPPO | Resellers in your market are AWS-aligned |
| Early stage (under about $5M ARR) | One cloud only, marketplace-first on the hosting cloud | Anchor customer demands another marketplace to burn a commit |
| Already strong on one cloud, pipeline plateaued | Add the second cloud with the highest commit overlap | First cloud's failure modes (section 9) are not fixed yet: fix those first |

### 12.3 Business-case inputs (per cloud)

- Target accounts with commit on this cloud x win-rate lift from co-sell x average deal size.
- Marketplace fee (3% new, 1.5% renewal) plus CPPO uplift if channel [X1][X2][X5].
- Ops cost: Cloud GTM platform subscription, 0.5 to 1 FTE partner ops (practitioner estimate), listing engineering.
- Hosting cost if a new deployment is needed to be commit-eligible.
- Offsets: funding programs in section 7; MCCP or MPOPP credits used as deal accelerants.
- Time to first co-sell-eligible quarter (section 3).
- Payback test: fees plus ops cost recovered by incremental deals in 4 quarters.

### 12.4 When private offers beat direct

Private offers beat direct when any of these holds: the customer has unburned commit on a cloud where you are eligible; a hyperscaler seller is engaged (their comp moves only on marketplace); procurement needs a pre-approved vendor path; or a reseller is in the deal (CPPO/MPO/MCPO keeps the reseller and still decrements the commit where eligible) [X4][X8][X20]. Direct wins when none of these holds and the 3% fee plus ops friction is pure cost.

---

## 13. Multi-cloud operations: tools, Crossbeam and runbooks

### 13.1 Marketplace and co-sell automation vendors (all VENDOR)

| Vendor | What it does | Clouds | Notes and currency |
|---|---|---|---|
| Tackle (AppDirect) | Cloud GTM platform: listings, private offers, co-sell sync to Salesforce, surfaces AWS OQS in Salesforce [X33]; Google co-sell via Partner Network Hub Integrator role [X38] | AWS, Microsoft, Google | AppDirect acquisition announced 2025-12-01 [X56]; selected for AWS 3PI PDM pilot [X33a]; publishes State of Cloud GTM report [X42][X43] |
| Clazar | Listings, private offers, bidirectional CRM sync for co-sell across three clouds; MCP server (2026-08-21) [X67a][X67c] | AWS, Microsoft, Google | Co-publishes State of Cloud Marketplace & Co-Sell report with Partner Insight [X44]; active blog (2026-09-11) |
| Suger | Listing, co-sell, billing and metering automation; very active technical blog on marketplace edge cases [X67b] | AWS, Microsoft, Google | Blog posts daily in Sept 2026 |
| Labra | Cloud GTM platform; AWS partner program guides [X72] | AWS, Microsoft, Google | Blog last item 2026-08-07 |
| WorkSpan (Hyperscaler Edition) | Co-sell referral workflows with bidirectional CRM and AWS ACE sync; transactable listing management; Salesforce, HubSpot, Dynamics 365 [X57] | AWS, Microsoft, Google | Claims 350K+ cloud referrals processed, $50B referral pipeline under management [X57] |
| Impartner HyperscalerGTM | PRM-linked partner-to-marketplace automation [X69] | Multi | Published hyperscaler marketplace guide January 2026 [X69] |
| Invisory, Automatum, Stactize, SaaSify, Noteworthy | Managed services / platforms and guides; Noteworthy tracks Microsoft funding [X17] | Varies | Useful explainers; verify against official pages |
| Native: AWS Partner CRM Connector | Salesforce AppExchange package syncing ACE opportunities and marketplace data via Partner Central API [X35] | AWS | Free; Salesforce only |
| Native: Partner Center Referrals Connector | Power Automate-based co-sell sync for Salesforce and Dynamics 365 via Referrals API [X36] | Microsoft | Needs Power Automate license; referrals admin role |
| Native: Google | No native CRM connector found; Producer API for offers [X37] | Google | Use a Cloud GTM platform for co-sell [X22] |

**How to choose:** (1) the CRM you run (HubSpot support is thinner among native connectors: AWS and Microsoft connectors are Salesforce and Dynamics first [X35][X36]; WorkSpan lists HubSpot [X57]); (2) the clouds you need now vs in 12 months; (3) whether the platform exposes AWS OQS and Microsoft deal-eligibility checks; (4) pricing model (WorkSpan advertises no transaction pricing [X57]); (5) roadmap stability after consolidation [X56].

### 13.2 Where Crossbeam and account mapping fit

Crossbeam (Forecastable's key partner) does not register co-sell opportunities with hyperscalers. It answers the question that comes before registration: which of my accounts are the hyperscaler's customers, on which products, and which of my partners (SIs, resellers, ISVs) are already in those accounts.

| Crossbeam capability | Hyperscaler relevance | Source |
|---|---|---|
| **Open Data Partners (ODPs)** | AWS, GCP and Microsoft available as partners without an invite; "is a customer of" signals from public sources (partner directories, tech stack listings, vendor marketplaces, case studies); product-level detail (for example, accounts running a specific AWS service); filter "contains" to find all accounts using a product | [X52] |
| Managed Offline Partners (legacy) | AWS, Microsoft, Google Cloud, Salesforce, SAP customer populations; stopped receiving updates from 2026-08-19; no new adds; move to ODPs | [X53] |
| Smarter Matching | Matches on DUNS, phone and marketplaces beyond domain | [X54] |
| Deal Navigator | Open opportunities overlapping partner customers, in Crossbeam or Salesforce; signals such as recent wins and long-term relationships | [X66b] |
| Partner Score | Win rate, deal size, time to close on a partner's customers vs baseline; High / Medium / Low | [X66] |
| MCP server, API and webhooks | Feed overlap data to agents and CRM (API and signals on Supernode and Enterprise) | [X54] |
| Crossbeam on AWS Marketplace | Crossbeam itself sells via AWS Marketplace | [X73] |
| Crossbeam Insider marketplace content | "What it actually takes to win on cloud marketplaces in 2026" (Juhi Saha, 2026-05-13) | [X51] |

No native Crossbeam integration with ACE, Partner Center Referrals or Partner Network Hub was found (section 14). Crossbeam's integration list covers CRMs, PRMs (PartnerStack, Impartner), Clay and others, so the hyperscaler link runs through CRM fields.

**The cross-cloud account-mapping play (Eva runbook, summary):**
1. Add AWS, GCP and Microsoft as Open Data Partners. Done when all three show under Partner List [X52].
2. Build an account-mapping list per cloud against your Prospects and Open Opportunities populations; filter Products "contains" the services your product pairs with. Done when each list has product-level columns [X52].
3. Score each cloud on factor 1 (commit / primary cloud) and factor 3 (ICP overlap) in section 12. Done when the scores are in the prioritization sheet.
4. For the chosen cloud, push "is a customer of" fields into Salesforce or HubSpot via Partner Field Mapping or custom object so the Cloud GTM platform can tag co-sell candidates [X66b].
5. Layer SI and reseller overlap from Crossbeam network partners on the same accounts to pick the CPPO / MPO / MCPO channel partner.
6. Take 5 named accounts per cloud to the biweekly seller touchpoint (section 10.2).

### 13.3 Tactical runbooks (cross-cloud)

**R1. Cross-cloud status audit (monthly, 60 minutes)**
1. AWS: Partner Central scorecard; check Software Path stage, FTR expiry (2-year validity), ISVA counts (5 launched, 15 qualified, trailing 12 months). Done when all three are recorded [X19][X39].
2. Microsoft: Partner Center co-sell solutions; confirm co-sell ready, IP co-sell eligible, Azure benefit eligible badge, trailing ACR plus MBS vs $100K. Done when all are recorded [X14][X8].
3. Google: Partner Network Hub tier and competency progress; listing live; resale enabled; MCCP eligibility. Done when recorded [X25][X13].
4. Fees: confirm renewal attestations were used on Microsoft private offers created this month; check Google deal type classification. Done when exceptions are listed [X3][X5].
5. Feeds: walk registry Tier 0 and log changes into section 8. Done when the changelog is updated.

**R2. Choose the transacting cloud for a specific deal**
1. Ask the buyer which cloud holds their largest unburned commit and whether it caps marketplace drawdown. Done when the answer is written down.
2. Check your eligibility on that cloud (badge and hosting). Done when yes or no.
3. If a reseller is involved, check your authorization on that cloud's channel offer (CPPO / MPO / reseller plan). Done when yes or no.
4. Pick the cloud: eligible plus commit available beats everything; then seller engagement; then lowest fee (TCV tier). Done when the private offer is requested.
5. Attach the credit program: MPOPP (AWS), MCCP (Google, first-time buyer, deal registered), Frontier Accelerate engagement (Microsoft). Done when the claim is filed [X29][X13][X17].

**R3. Register a co-sell deal on the right system**
1. AWS: create in ACE; associate a marketplace solution or product; submit via StartEngagementFromOpportunityTask; watch OQS [X24][X30][X31].
2. Microsoft: create referral in Partner Center with an IP co-sell eligible solution; value at least $25K; do not mark won within 72 hours [X24].
3. Google: register in Partner Network Hub; issue private offer as the coordination object [X24][X38].
Done when each system shows the deal with a status and the CRM holds the external ID.

**R4. Launch a channel offer on all three**
1. AWS: authorize reseller for CPPO; price with the 0.5% uplift in mind [X1].
2. Microsoft: create MPO, send to channel partner; confirm the market is one of the 36 supported [X4][X15].
3. Google: turn on reselling; issue a private offer plan to a Resale Subprogram partner [X11].
Done when each partner confirms they can see the offer.

**R5. Prep for a hyperscaler seller meeting (any cloud)**
1. Pull 5 overlapping accounts from Crossbeam ODP lists with product-level signals [X52].
2. For each: customer pain, hyperscaler services consumed, commit position if known, the seller's comp hook (section 1.3).
3. Bring a ready private offer structure and the credit program you can attach.
Done when the seller agrees to one next step per account.

---

## 14. Unverified, conflicting or login-gated

| Item | Status | Detail |
|---|---|---|
| AWS EDP/PPA marketplace drawdown 25% cap | UNVERIFIED on an official page; source dated 2025-02 [X10] | EDP/PPA terms are private contracts. AWS's official post says Deployed on AWS products "continue to count towards additional customer benefits" without stating the rate [X9]. Suger's 2026-08-05 article gives no cap [X68]. |
| Google MCPO commit drawdown | CONFLICT | Official page: reseller purchases excluded unless the vendor opts into resale [X7]. Invisory: 100% drawdown for MCPO [X13]. ChannelInsider: 100% drawdown effective 2025-06-09 plus a confusing "up to 25% of the qualifying amount" [X12]. Read as: 100% when the ISV has enabled resale; confirm per deal. |
| Google seller compensation on marketplace | UNVERIFIED, source dated 2024-04 [X65] | No current official statement found. |
| Google co-sell gates and architecture review | Practitioner-reported [X22][X23] | Google does not publish tier thresholds [X25]. |
| AWS onboarding fee ($2,500 with $3,500 credit) | VENDOR claim [X20] | Not found on official pages fetched. |
| Microsoft Frontier Accelerate engagement caps ($25K / $250K / $100K / $125K) | VENDOR [X17] | Official page confirms stages and $30K premium credits only [X16]; guide likely login-gated. |
| Microsoft FY27 seller incentive percentages (+55% marketplace, +35% Azure) | VENDOR [X18] | From MCAPS Start coverage; internal comp plans are not public. |
| ISVA criteria | Official page fetched 2026-09-26 [X19] and practitioner (verified June 2026) [X21] agree on 5 launched plus 15 qualified opps; the "$2,000 recognized revenue" line was garbled in the fetch | Recheck in Partner Central. |
| Crossbeam native hyperscaler co-sell integration | Not found | Crossbeam help center shows ODPs and legacy Managed Offline Partners for hyperscalers; no ACE / Referrals / Partner Network Hub connector found (2026-09-26). |
| Canalys Forums Americas and APAC 2026 dates | Not found | Only EMEA 2026 confirmed (Oct 6 to 8, Barcelona) [X63]. |
| IDC, Gartner, Forrester marketplace-size forecasts | No current public forecast found | IDC MarketScape on marketplaces is 2023 and paywalled; Forrester TEI of Microsoft commercial marketplace (587% ROI) is 2023 and Microsoft-commissioned [X50] (UNVERIFIED, source dated 2023). |
| Omdia "at least 50% via channel by 2027" | Date of the insight page not shown [X41] | Consistent with the October 2025 release (nearly 60% by 2030) [X40]. |
| Login-gated | AWS Partner Funding Benefits Guide; Partner Central scorecards; Partner Center benefits workspace; Google Partner Network Hub tier criteria | Eva must check in-portal. |

---

## 15. Market data (labelled)

| Metric | Value | Source | Label | Date |
|---|---|---|---|---|
| Hyperscaler marketplace sales 2024 | $30B | Omdia [X40] | INDEPENDENT | 2025-10-06 |
| Forecast 2030 | $163B, 29.1% CAGR 2025 to 2030 | Omdia [X40] | INDEPENDENT | 2025-10-06 |
| Committed cloud spend across AWS, Azure, GCP | about $470B; about $30B new commitments in Q2 2025 | Omdia [X40] | INDEPENDENT | 2025-10-06 |
| Cloud commitments | "crossed $500B last year"; AWS commitments $364B; 99% of top 1,000 AWS customers have at least 1 active Marketplace subscription | Partner Insight (Roman Kirsanov) citing company disclosures [X49] | CREATOR | 2026-06-08 |
| Commitments projected | above $460B in 2025 | Tackle [X42] | VENDOR | 2025-12-17 |
| Marketplace sales via channel partners | at least 50% by 2027; nearly 60% by 2030 | Omdia [X41][X40] | INDEPENDENT | 2025 |
| Category sizes 2025 | Infrastructure software $10.5B; DevOps $9.1B; Business apps $9.1B; AI marketplace $24.4B by 2030 (37% CAGR); cybersecurity $31B by 2030 (31% CAGR) | Omdia [X40] | INDEPENDENT | 2025-10-06 |
| ISVs transacting on at least one marketplace | 89% | Clazar / Partner Insight [X44] | VENDOR | 2025-04-24, updated 2026-02-24 |
| Share of revenue via marketplace | 22% get over 20%; 41% under 5%; 62% report net-new revenue; 30% move direct deals | Clazar / Partner Insight [X44] | VENDOR | 2025 |
| Co-sell | 71% co-sell with hyperscalers; 51% say too complex to scale; 59% higher win rates; 32% to 40% have structured cadences | Clazar / Partner Insight [X44] | VENDOR | 2025 |
| Multi-cloud vs single-cloud | 29% vs 3% of revenue via marketplace; 39% vs 18% of deals co-sell influenced | Tackle [X43] | VENDOR | 2025-11-06 |
| Committed spend as benefit | 74% cite access to committed spend; 46% rate access to PDMs "very or extremely challenging" (25% "extremely"; corrected from Tackle chart data, see vendors/tackle-intelligence.md) | Tackle [X42] | VENDOR | 2025-12-17 |
| Expected marketplace revenue growth | 60% increase in 2026 | Tackle [X42] | VENDOR | 2025-12-17 |
| Partner revenue per $1 of hyperscaler | AWS up to $7.13 (Expert partners; $1.26 Focused, $3.26 Multi-category, $5.78 Progressive) | Omdia PEM 2025 via AWS [X45] | INDEPENDENT, commissioned | 2025-12-01 |
| | Microsoft $8.45 services, $10.93 software | IDC via Microsoft [X46] | INDEPENDENT, commissioned | 2025-03-24 |
| | Google $7.05 | Canalys via Google [X47] | INDEPENDENT, commissioned | 2025-01 / 2025-06-25 |
| Partner share of IT spend | Partner-delivered only 61% of North America IT spend in 2026 (over 70% four years prior); 81% of partners expect to underperform market | Omdia / Jay McBain via Channel Dive [X48] | INDEPENDENT | 2026-02-06 |
| Partner-attached lift | 53% more deals, 27% shorter cycles when sales and partnerships collaborate; deals close 46% faster with a partner involved | Crossbeam [X55] | VENDOR | undated |
| Marketplace procurement ROI | 587% ROI, payback under 6 months (composite of 10 customers) | Forrester TEI, Microsoft-commissioned [X50] | INDEPENDENT, commissioned | 2023 (UNVERIFIED, source dated 2023) |
| Gartner / IDC current marketplace forecasts | Not published publicly | Section 14 | n/a | checked 2026-09-26 |

---

## Sources

| Tag | Title | Publisher | Date | Label | URL |
|---|---|---|---|---|---|
| X1 | Understanding listing fees for AWS Marketplace sellers | AWS | effective 2024-01-05; fetched 2026-09-26 | OFFICIAL | https://docs.aws.amazon.com/marketplace/latest/userguide/listing-fees.html |
| X2 | Commercial marketplace transaction capabilities (store service fee) | Microsoft Learn | 2026-07-23 | OFFICIAL | https://learn.microsoft.com/en-us/partner-center/marketplace-offers/marketplace-commercial-transaction-capabilities-and-considerations |
| X3 | Agency fee discount for renewals | Microsoft Learn | 2026-03-25 | OFFICIAL | https://learn.microsoft.com/en-us/partner-center/marketplace-offers/agency-fee-discount-for-renewals |
| X4 | Multiparty private offers overview | Microsoft Learn | 2026-07-22 | OFFICIAL | https://learn.microsoft.com/en-us/partner-center/marketplace-offers/multiparty-private-offers-overview |
| X5 | Vendor Net Revenue Schedule | Google Cloud | effective 2025-04-21 | OFFICIAL | https://cloud.google.com/terms/marketplace-revenue-share-schedule |
| X6 | Sample revenue share calculations for Google Cloud Marketplace | Google Cloud | 2026-09-24 | OFFICIAL | https://docs.cloud.google.com/marketplace/docs/partners/revenue-share-scenarios |
| X7 | Google Cloud Marketplace commitment drawdown rates | Google Cloud | 2026-09-24 | OFFICIAL | https://docs.cloud.google.com/marketplace/docs/commit-drawdown |
| X8 | Azure consumption commitment benefit | Microsoft Learn | 2025-09-25 | OFFICIAL | https://learn.microsoft.com/en-us/marketplace/azure-consumption-commitment-benefit |
| X9 | AWS Marketplace announces upcoming expansion to SaaS product catalog | AWS Marketplace blog | 2025-02-25 | OFFICIAL | https://aws.amazon.com/blogs/awsmarketplace/aws-marketplace-announces-upcoming-expansion-to-saas-product-catalog/ |
| X10 | AWS Tightens the Reins: New AWS SaaS Marketplace Rules Will Impact Your Commitments | Duckbill | 2025-02-06 | INDEPENDENT | https://www.duckbillhq.com/blog/new-aws-marketplace-rules/ |
| X11 | Resell Cloud Marketplace products from ISVs | Google Cloud | 2026-09-18 | OFFICIAL | https://docs.cloud.google.com/marketplace/docs/partners/resellers/resell |
| X12 | Google Cloud Marketplace Moves to Incentivize Partner Growth | Channel Insider | 2025-05 | INDEPENDENT | https://www.channelinsider.com/tech-companies/google-cloud-marketplace-partner-commit/ |
| X13 | New Google Cloud Marketplace Incentives for 2025: MCPO, MCCP, and More | Invisory | 2025 | VENDOR | https://invisory.co/resources/blog/new-gcm-google-cloud-marketplace-incentives-for-2025-mcpo-mccp-and-more/ |
| X14 | Co-sell requirements | Microsoft Learn | 2025-09-25 | OFFICIAL | https://learn.microsoft.com/en-us/partner-center/referrals/co-sell-requirements |
| X15 | July 2026 announcements (Partner Center) | Microsoft Learn | 2026-07 | OFFICIAL | https://learn.microsoft.com/en-us/partner-center/announcements/2026-july |
| X16 | Frontier Accelerate for Marketplace | Microsoft | 2026 (fetched 2026-09-26) | OFFICIAL | https://partner.microsoft.com/en-us/partnership/frontier-accelerate-for-marketplace |
| X17 | Marketplace funding, explained: what Frontier Accelerate means for you in FY27 | Noteworthy (Sian Herrington) | 2026-09-08 | VENDOR | https://noteworthy.support/news-and-insights/marketplace-funding-frontier-accelerate-fy27 |
| X18 | MCAPS Start 2026: what Microsoft's FY27 updates mean for partners | Partner1 | 2026-07-22 | VENDOR | https://www.partner1.io/partner-blog/mcaps-start-2026-fy27-microsoft |
| X19 | AWS ISV Accelerate Program | AWS | fetched 2026-09-26 | OFFICIAL | https://aws.amazon.com/partners/programs/isv-accelerate/ |
| X20 | How to Achieve AWS SaaS Co-Sell Benefit and Maximize Co-Sell Success | Tackle | 2025 | VENDOR | https://tackle.io/blog/how-to-achieve-aws-saas-co-sell-benefit-and-maximize-co-sell-success/ |
| X21 | How to Co-Sell With AWS: ACE, ISV Accelerate and the Path to Partner-Led Growth | flashdba (Chris Buckel) | 2026-06 | CREATOR | https://flashdba.com/hyperscaler-gtm/co-sell/aws/ |
| X22 | How to Co-Sell With Google Cloud | flashdba (Chris Buckel) | 2026-06-17, reviewed 2026-07-06 | CREATOR | https://flashdba.com/hyperscaler-gtm/co-sell/google-cloud/ |
| X23 | Hyperscaler Co-Sell: The Complete Guide | flashdba (Chris Buckel) | 2026-06-17, reviewed 2026-07-01 | CREATOR | https://flashdba.com/hyperscaler-gtm/co-sell/ |
| X24 | How Co-Sell Works on AWS, Azure, and Google Cloud | Suger | 2026-08-10 | VENDOR | https://www.suger.io/resources/blog/how-co-sell-works/ |
| X25 | Google Cloud Partner Network Tiers Explained | Suger | 2026 | VENDOR | https://www.suger.io/resources/blog/google-cloud-partner-network-tiers/ |
| X26 | Introducing Google Cloud Partner Network | Google Cloud blog (Colleen Kapase) | 2025-12-16 | OFFICIAL | https://cloud.google.com/blog/topics/partners/introducing-google-cloud-partner-network |
| X27 | Google launches $750M partner fund at Cloud Next 2026 | The Next Web | 2026-04-22 | INDEPENDENT | https://thenextweb.com/news/google-cloud-750m-partner-fund-agentic-ai |
| X28 | Powering Next-Level Partner Success: Innovations for Growth and Scale in 2026 | AWS APN blog | 2025-12-01, modified 2026-03-25 | OFFICIAL | https://aws.amazon.com/blogs/apn/powering-partner-success-2026-innovations/ |
| X29 | Announcing new incentives for ISVs selling in AWS Marketplace (MPOPP) | AWS What's New | 2025-08-12 | OFFICIAL | https://aws.amazon.com/about-aws/whats-new/2025/08/aws-marketplace-private-offer-promotions/ |
| X30 | AWS Partner Central agents now accelerate co-selling on every deal | AWS What's New | 2026-06-16 | OFFICIAL | https://aws.amazon.com/about-aws/whats-new/2026/06/accelerate-co-selling-with-agents/ |
| X31 | AWS Partner Central now supports AWS Marketplace listings for co-selling | AWS What's New | 2026-07-01 | OFFICIAL | https://aws.amazon.com/about-aws/whats-new/2026/07/aws-marketplace-co-selling-support/ |
| X32 | AWS Partners can now accelerate co-sell deals with express private offers | AWS What's New | 2026-06-16 | OFFICIAL | https://aws.amazon.com/about-aws/whats-new/2026/06/aws-partners-express-private-offers/ |
| X33 | The New Math of AWS Co-Sell: What the Opportunity Quality Score Actually Means for You | Tackle | 2026-09-25 | VENDOR | https://tackle.io/blog/aws-opportunity-quality-score/ |
| X33a | Tackle Selected to Support ISV Onboarding Through AWS 3PI PDM Pilot | Tackle | 2026 | VENDOR | https://tackle.io/blog/tackle-3pi-pdm-pilot/ |
| X34 | AWS Partner Central API Reference (Welcome) | AWS | fetched 2026-09-26 | OFFICIAL | https://docs.aws.amazon.com/partner-central/latest/APIReference/Welcome.html |
| X35 | What is AWS Partner CRM integration? | AWS | fetched 2026-09-26 | OFFICIAL | https://docs.aws.amazon.com/partner-central/latest/crm/aws-partner-crm-integration.html |
| X36 | The co-sell connector for Salesforce CRM | Microsoft Learn | 2026-01-07 | OFFICIAL | https://learn.microsoft.com/en-us/partner-center/referrals/connector-salesforce |
| X37 | Cloud Marketplace Partners release notes | Google Cloud | 2026-07-30 latest entry | OFFICIAL | https://docs.cloud.google.com/marketplace/docs/partners/release-notes |
| X38 | Connect to Google Cloud for co-sell registration | Tackle Help | 2026-05-22 | VENDOR | https://help.tackle.io/en/articles/15217465-connect-to-google-cloud-for-co-sell-registration |
| X39 | The AWS ISV Partner Path Is Now the Software Path | Suger | 2026-08-09 | VENDOR | https://www.suger.io/resources/blog/aws-isv-partner-path/ |
| X40 | Hyperscaler cloud marketplace sales to hit $163 billion by 2030 | Omdia | 2025-10-06 | INDEPENDENT | https://omdia.tech.informa.com/pr/2025/oct/hyperscaler-cloud-marketplace-sales-to-hit-us-163-billion-us-dollars-by-2030 |
| X41 | Now and Next for Hyperscaler Marketplaces | Canalys (Omdia) | 2025 | INDEPENDENT | https://omdia.tech.informa.com/insights/2025/now-and-next-for-hyperscaler-marketplaces |
| X42 | State of Cloud GTM 2025: committed spend, engagement and the new marketplace landscape | Tackle | 2025-12-17 | VENDOR | https://tackle.io/blog/state-of-cloud-gtm-2025-committed-spend-engagement-and-the-new-marketplace-landscape/ |
| X43 | State of Cloud GTM 2025: Why Multi-Cloud Companies See 10x More Revenue with Data | Tackle | 2025-11-06 | VENDOR | https://tackle.io/blog/state-of-cloud-gtm-2025-why-multi-cloud-companies-see-10x-more-revenue-with-data/ |
| X44 | State of Cloud Marketplaces & Co-Sell: From Adoption to Acceleration (2025 report) | Clazar with Partner Insight | 2025-04-24, updated 2026-02-24 | VENDOR | https://clazar.io/blog/state-of-cloud-marketplace-and-co-sell-report-insights |
| X45 | AWS Partner profitability: revenue multiplier (Omdia PEM 2025) | AWS APN blog | 2025-12-01 | INDEPENDENT, commissioned | https://aws.amazon.com/blogs/apn/aws-partner-profitability-revenue-multiplier |
| X46 | Microsoft at 50: The journey and future of the partner ecosystem | Official Microsoft Blog | 2025-03-24 | INDEPENDENT, commissioned (IDC data) | https://blogs.microsoft.com/blog/2025/03/24/microsoft-at-50-the-journey-and-future-of-the-partner-ecosystem/ |
| X47 | New study on maximizing partner growth with Google Cloud (Canalys) | Google Cloud blog | 2025-06-25 | INDEPENDENT, commissioned | https://cloud.google.com/blog/topics/partners/new-study-on-maximizing-partner-growth-with-google-cloud/ |
| X48 | The IT boom is real but the channel's share is shrinking | Channel Dive | 2026-02-06 | INDEPENDENT | https://www.channeldive.com/news/partners-expect-to-lag-it-boom-as-hyperscalers-dominate-infrastructure/811627/ |
| X49 | One Chart Shows Cloud Marketplaces Going Mainstream | Partner Insight (Roman Kirsanov) | 2026-06-08 | CREATOR | https://newsletter.partnerinsight.io/p/one-chart-shows-cloud-marketplaces |
| X50 | The Total Economic Impact of the Microsoft commercial marketplace | Microsoft Azure blog (Forrester, commissioned) | 2023 | INDEPENDENT, commissioned | https://azure.microsoft.com/en-us/blog/the-total-economic-impact-of-the-microsoft-commercial-marketplace/ |
| X51 | What It Actually Takes to Win on Cloud Marketplaces in 2026 and Beyond | Crossbeam Insider (Juhi Saha) | 2026-05-13 | VENDOR | https://insider.crossbeam.com/entry/what-it-actually-takes-to-win-on-cloud-marketplaces-in-2026-and-beyond |
| X52 | Understanding Open Data Partners | Crossbeam Help Center | fetched 2026-09-26 | VENDOR | https://help.crossbeam.com/en/articles/15453957-understanding-open-data-partners |
| X53 | Managed Offline Partners | Crossbeam Help Center | fetched 2026-09-26 (sunset notice 2026-08-19) | VENDOR | https://help.crossbeam.com/en/articles/11730520-managed-offline-partners |
| X54 | Crossbeam Product Release Notes 11/6/2025 | Crossbeam Help Center | 2025-11-06 | VENDOR | https://help.crossbeam.com/en/articles/12674444-crossbeam-product-release-notes-11-6-2025 |
| X55 | When sales and partnerships partner up | Crossbeam Insider | undated | VENDOR | https://insider.crossbeam.com/resources/when-sales-and-partnerships-partner-up |
| X56 | AppDirect and Tackle.io to Unite | Business Wire | 2025-12-01 | VENDOR | https://www.businesswire.com/news/home/20251201840606/en/AppDirect-and-Tackle.io-to-Unite-to-Extend-Leadership-in-B2B-Subscription-Commerce-with-Native-Hyperscaler-Marketplace-Integration |
| X57 | WorkSpan Hyperscaler Edition | WorkSpan | fetched 2026-09-26 | VENDOR | https://www.workspan.com/solutions/hyperscalers/product-overview |
| X58 | Cloud Marketplace fees compared: what Microsoft, AWS and Google Cloud actually charge | Partner1 | 2026-07 | VENDOR | https://www.partner1.io/partner-blog/cloud-marketplace-fees-compared |
| X59 | Microsoft Unifies Azure Marketplace and AppSource Into New AI-Focused Marketplace | WinBuzzer | 2025-09-26 | INDEPENDENT | https://winbuzzer.com/2025/09/26/microsoft-unifies-azure-marketplace-and-appsource-into-new-ai-focused-marketplace-xcxwbn/ |
| X60 | AWS re:Invent 2026 | AWS | fetched 2026-09-26 | OFFICIAL | https://aws.amazon.com/events/reinvent/ |
| X61 | Microsoft Ignite 2026 | Microsoft | fetched 2026-09-26 | OFFICIAL | https://ignite.microsoft.com/en-US/home |
| X62 | FAQ: Google Cloud Next | Google Cloud | fetched 2026-09-26 | OFFICIAL | https://www.googlecloudevents.com/next-vegas/faq |
| X63 | Canalys Forums EMEA 2026 in Barcelona | Dutch IT Channel | 2026 | INDEPENDENT | https://www.dutchitchannel.nl/event/725448/canalys-forums-emea-2026-in-barcelona |
| X64 | Azure Accelerate Is Now Frontier Accelerate for Azure | Maven Collective Marketing | 2025-07-31, modified 2026-08-18 | VENDOR | https://mavencollectivemarketing.com/insights/blog/what-is-microsoft-azure-accelerate/ |
| X65 | The Opportunity and Economics of the Google Cloud Marketplace with Dai Vu | Clazar podcast | 2024-04-03 | VENDOR (UNVERIFIED, source dated 2024-04) | https://clazar.io/podcasts/the-opportunity-and-economics-of-google-cloud-marketplace-with-dai-vu |
| X66 | Understanding Partner Score in Crossbeam | Crossbeam Help Center | fetched 2026-09-26 | VENDOR | https://help.crossbeam.com/en/articles/9204052-understanding-partner-score-in-crossbeam |
| X66b | Crossbeam Deal Navigator | Crossbeam Help Center | fetched 2026-09-26 | VENDOR | https://help.crossbeam.com/en/articles/10844915-crossbeam-deal-navigator |
| X67a | Clazar MCP Server: Query Your Cloud Partnerships Data Wherever You Work | Clazar | 2026-08-21 | VENDOR | https://clazar.io/blog/clazar-mcp-server |
| X67b | Suger blog index (AWS EMEA SARL and KYC, 2026-09-24, and others) | Suger | 2026-09-24 | VENDOR | https://www.suger.io/resources/blog/ |
| X67c | How to Integrate Your CRM with Cloud Marketplaces (AWS, Microsoft and Google Cloud) | Clazar | 2026-09-07 | VENDOR | https://clazar.io/blog/crm-cloud-marketplace-integration |
| X68 | AWS EDP: What Marketplace Sellers Need to Know | Suger | 2026-08-05 | VENDOR | https://www.suger.io/resources/blog/aws-edp-what-sellers-need-to-know/ |
| X69 | Leading Growth in Partner Ecosystems: Hyperscaler Marketplaces Insights Guide 2026 | Impartner | 2026-01 | VENDOR | https://impartner.com/wp-content/uploads/2026/01/Impartner-Hyperscaler-Marketplaces-Insights-Guide-2026.pdf |
| X70 | Amazon investor relations (annual reports, calendar fiscal year) | Amazon | annual | OFFICIAL | https://ir.aboutamazon.com/annual-reports-proxies-and-shareholder-letters/default.aspx |
| X71 | Alphabet investor relations (calendar fiscal year) | Alphabet | annual | OFFICIAL | https://abc.xyz/investor/ |
| X72 | The Complete Guide to AWS Partner Programs in 2026 | Labra | 2026 | VENDOR | https://labra.io/aws-partner-programs-guide/ |
| X73 | AWS Marketplace: Crossbeam seller profile | AWS Marketplace | fetched 2026-09-26 | OFFICIAL | https://aws.amazon.com/marketplace/seller-profile?id=seller-lwthae66p4uwq |
