# Google Cloud partner program intelligence
Version: 2026.09 (built 2026-09-26). Refreshed monthly. Facts carry source tags; see Sources.

Scope: Google Cloud Partner Network (the program that replaced Partner Advantage on 2026-01-15), Partner Network Hub, Google Cloud Marketplace (Producer Portal, Partner Sales Console), co-sell, incentives and funding, AI agent programs (Agent Marketplace, Agent Gallery in Gemini Enterprise). Written for B2B SaaS ISVs first, then services firms, agencies and resellers.

Label key used in text: OFFICIAL (Google docs, blogs, terms), INDEPENDENT (press, analysts), VENDOR (Tackle, Clazar, Suger, Invisory, Labra, WorkSpan), CREATOR (practitioner newsletters and podcasts). A fact tagged only with a VENDOR or INDEPENDENT source is not confirmed by Google; treat it as directional.

---

## The twelve things that matter right now

1. **Partner Advantage is dead; Google Cloud Partner Network is the program.** Announced 2025-12-16 by Colleen Kapase, kicked off 2026-01-15 (Partner Advantage terminated that day), with a six-month transition window that ran to about mid-July 2026 [G1][G4][G5]. Tiers are **Select, Premier, Diamond** (Diamond is new and "intentionally selective") [G1][G2]. Partner "paths" replaced the old Build / Sell / Service engagement models: **co-selling, services, technology** [G3][G4]. Any web content, vendor guide or rep deck still saying "Partner Advantage portal", "Build engagement model", "Specialization", "Expertise" or "Premier Partner in the Build Engagement Model" is stale (even vendor guides dated May 2026 still say it) [G70][G74].

2. **Tiers and competencies are now computed automatically from registered outcomes, not paperwork.** "We will automatically apply every successful customer engagement toward a partner's progress in all eligible tiers and competencies" [G1]. No business plans or customer stories; the metrics are co-sell, workshops/assessments/pilots, closed SOWs and certifications ("book smarts" and "street smarts") [G4][G92]. Implication: an unregistered deal does not exist for tiering. Registration hygiene in Partner Network Hub is now the program.

3. **Tier thresholds reported by CRN Australia (not published publicly by Google):** Select USD 250K partner co-sell ACV, Premier USD 2M, Diamond USD 20M plus 20 partner-implemented workloads, 30 partner co-sell influenced opportunities and 200 professional certifications [G5]. Google's public pages give descriptions only, and one vendor explicitly says Google publishes no number [G2][G66]. Treat as the best available figure; verify in the login-gated program guide in Partner Network Hub before committing a plan to it.

4. **21 competencies replaced Specializations, independent of tier.** 6 solution (AI, Application Modernization, Data & Analytics, Databases, Infrastructure, Security), 10 industry, and 5 product per CRN (Apigee, Chrome, Gemini Enterprise, Maps, Looker) though Google's own page lists 4 product competencies (no Apigee) [G2][G4]. Two levels each: Competency and Advanced Competency. Measured on capacity (certifications and sales credentials) and capability (pre-sales and post-sales contributions to validated closed/won opportunities) [G1][G84].

5. **Leadership turned over in 2026; update your contact map.** Colleen Kapase (VP Channels and Partner Programs, author of the Partner Network launch) left Google Cloud in March 2026 and joined OpenAI [G11][G12]. David Smith (27 years at Microsoft, former VP Worldwide Channel Sales) is now Head of Global Partner Program / channel chief, reporting to Kevin Ichhpurani, President Global Ecosystem [G11][G14]. Philip Larson (MD, Google Cloud Partner Network, the program's architect and Next '26 spokesperson) left and in July 2026 joined OpenAI to run its partner network [G13]. Dai Vu (MD, Marketplace and ISV GTM) is still in role as of May 2026 [G64]. <!-- VALIDATE-OK[customer-name]: substring of spokesperson or salesperson, not a customer -->

6. **The $750M partner innovation fund (Next '26, 2026-04-22)** covers: hands-on support for software companies to build agents on Gemini Enterprise Agent Platform and sell them through Agent Marketplace and Agent Gallery; forward deployed engineers (FDEs) embedded with major SIs; deployment and usage incentives for services partners; training and workshops [G6]. Larson's breakdown: sandbox credits for workshops, assessments and pilots; demand gen; deployment vouchers; FDEs; services funding to production [G92]. Google has not published per-partner amounts or an application form; access runs through your partner manager and Partner Network Hub.

7. **Marketplace economics are the best of the three clouds for large private offers.** Vendor Net Revenue Schedule effective 2025-04-21: 3% fee for standard (public) offers and new private offers under USD 1M TCV; 2% for new private offers USD 1M to under 10M; 1.5% for new private offers at or above USD 10M and for channel shifts, migrations and native renewals at any TCV [G18][G21]. Deal type is a field you must set correctly on the private offer (New, Migration, Native renewal, Channel shift) [G26]. Usage-only offers compute TCV as zero and sit at 3%; use CUD pricing to earn the lower rates [G20]. Professional services are excluded from the schedule [G19].

8. **Commit drawdown: 100% rate, 25% cap, and a specific exclusions list.** 100% of Marketplace spend can count toward a customer's Google Cloud Minimum Commitment, except Google Maps, Google Ads, products not running on Google Cloud, resold purchases where the ISV has not opted into the resale program, products owned by the purchaser, and professional services [G23]. All eligible Marketplace spend combined can retire at most 25% of a given commitment; excess does not roll over [G22]. Reseller-transacted purchases count for new purchases and renewals after 2025-06-08 if the reseller and the Google rep associate the purchase with the customer and it is not inside a reseller-held commitment [G22]. There is no "eligible for commit" badge program to earn; eligibility is set by hosting on Google Cloud (the listing requirement) plus the exclusions.

9. **Hosting on Google Cloud is the gating requirement to list.** You must verify during onboarding that the product is hosted primarily on Google Cloud, via one of nine approved hosting patterns (fully hosted; compute or data plane on GCP; storage/backup to GCP; migration tooling with GCP as sole destination; agent data analysis on GCP; datasets; Google Distributed Cloud; AI agents fully on GCP; AI agents hybrid) and the listing "must result in meaningful Google Cloud consumption" [G17]. An AWS-hosted SaaS generally cannot list without architecture work. Decide this before spending on Google marketplace.

10. **Co-sell = registration in Partner Network Hub + a Marketplace transaction + a named Google seller.** Google sellers are incentivized on marketplace deals: Google's own April 2026 copy says "Google sales reps incentivized to work with you" [G8]; Dai Vu has said most marketplace solutions are eligible for quota attainment plus SPIFFs on closed co-sell deals [G71]; Google's ISV sales leaders now carry a target to source opportunities for ISVs [G77]. The customer's commit drawdown is the reason the field leans in [G68]. Off-marketplace deals lose the drawdown and weaken credit.

11. **Buyer incentive levers exist and are underused.** Marketplace Customer Credit Program (MCCP): up to 3% of annualized GTV back to the customer as Google Cloud credits on a first-time private-offer purchase of an eligible ISV, min USD 100K annualized GTV, max USD 250K credit, paid in 4 quarterly disbursements [G45][G46]. Partner eligibility is gated (ISV Solution Connect enrollment, 25 registered deals or USD 5M pipeline, 10 private offers or USD 1M GTV in 12 months) [G45]. RaMP 2026 gives migration customers service credits (25% to 65% of incremental spend, capped) and Partner Services Funds up to USD 2M per workload [G55].

12. **Agents are the new listing type and a new designation.** Marketplace supports "AI agent as a service" listings built on an A2A Agent Card; agents validated for Gemini Enterprise earn "Google Cloud Ready - Gemini Enterprise" after a four-step evaluation and appear in the Agent Gallery inside the Gemini Enterprise app (70+ partner agents at Next '26 launch) [G7][G8][G39][G61]. Google Cloud's backlog (USD 460B+ quoted in April 2026, USD 514B reported after Q2 2026) is the pool partners are told to tap [G8][G65].

---

## 0. Program map and vocabulary

### 0.1 What replaced what

| Retired name (still on the web) | Current name or mechanic | Notes | Source |
|---|---|---|---|
| Google Cloud Partner Advantage (program) | Google Cloud Partner Network | Terminated 2026-01-15; six-month transition | [G1][G4] |
| Partner Advantage portal (partneradvantage.goog) | Partner Network Hub (partners.cloud.google.com) | Same hub hosts Earnings Hub, SOW Analyzer, Partner Agent, Marketplace Vendor Agreement, onboarding tasks | [G1][G16][G52] |
| Tiers: Member (older), Partner, Premier | Tiers: Select, Premier, Diamond | CRN AU: former "Partner" is the Select equivalent | [G5][G87] |
| Engagement models: Build, Sell, Service | Partner paths: co-selling, services, technology | Diamond exists per track (co-sell, services, technology) | [G3][G4] |
| Product-specific Premier badges (2023, e.g. "Premier Partner for Google Cloud in the Build Engagement Model") | Tier plus competencies | Premier badges launched 2023-08-01, now superseded | [G87] |
| Specializations (highest achievement, 3+ customer stories) and Expertise | Competency and Advanced Competency (21 areas) | No customer-story requirement; outcomes tracked automatically | [G1][G4][G88] |
| Delivery Readiness Index (DRI) | Still feeds capacity data; Hub pulls "delivery readiness portal data" | [G4][G87] |
| Agentspace (Google's agent product, 2024-2025) | Gemini Enterprise (launched 2025-10-09) and Gemini Enterprise Agent Platform (Next '26) | Agents list via Agent Marketplace, surface in Agent Gallery | [G6][G61] |
| AI Agent Marketplace (Next '25) | Agent Marketplace plus Agent Gallery in Gemini Enterprise | 70+ agents at Next '26 launch | [G7][G21] |
| Flat 3% marketplace fee | Vendor Net Revenue Schedule (1.5% to 3%) | Effective 2025-04-21 | [G18] |
| "Google Cloud Build partner" (marketplace docs 2022-2025) | Technology Partner in Partner Network (authorization via Hub) | Docs now say "authorized as a Google Cloud Technology Partner" | [G16][G26] |
| Partner Advantage "Partner tier" as prerequisite (e.g. Google Cloud Ready - AlloyDB page) | Unclear; page still says "registered Google Cloud partner at Partner Tier" | Stale wording on an official page | [G59] |

### 0.2 The layered model (how to think about Google Cloud as an ISV)

| Layer | Google mechanism | Owner at the ISV | What "done" looks like |
|---|---|---|---|
| 1. Org membership | Partner Network enrollment, Partner Network Hub account, Partner Admin assigned | Alliances lead | Company profile live in Hub; at least 2 Partner Admins |
| 2. Path and authorization | Technology partner authorization (for marketplace), co-selling path, services path, Resale Subprogram (resellers) | Alliances + legal | Marketplace Vendor Agreement accepted in Hub |
| 3. Listing status | Producer Portal product, pricing review, technical integration, published listing | Product + eng + alliances | Transactable listing, test purchase done |
| 4. Technical validation | Hosting pattern approval; Google Cloud Ready designations (BigQuery, AlloyDB, Gemini Enterprise); A2A validation for agents | Eng + partner engineer | Designation badge; listed on product partner page |
| 5. Co-sell eligibility | Registrations in Partner Network Hub; ISV Solution Connect (invite-only directory for field) | Alliances + sales ops | Every qualified deal registered; field can find you |
| 6. Opportunity execution | Named FSR, CE, ISV specialist; account mapping; joint pitch | AEs + alliance managers | Google seller attached and active on the opportunity |
| 7. Incentives and funding | MCCP, partner funding via SOW (Earnings Hub), $750M fund, RaMP, credits | Alliances + finance | Claims submitted; Earnings Hub shows payments |
| 8. Transaction | Private offer, reseller private offer plan (MCPO), commit drawdown | Deal desk | Offer accepted; approved; disbursement received ~21st |

### 0.3 Glossary

| Term | Meaning | Source |
|---|---|---|
| Partner Network Hub | The partner portal at partners.cloud.google.com. Enrollment, user management, Marketplace Vendor Agreement, onboarding tasks, registrations, Earnings Hub, SOW Analyzer, Partner Agent, program progress dashboards | [G1][G3][G16] |
| Partner Admin | Hub role that can accept agreements (Marketplace Vendor Agreement) and sign terms (Delivery Navigator) for the org | [G16][G63] |
| Integrator role | Hub role assigned to a third-party service account (e.g. Tackle) so it can register co-sell opportunities on your behalf | [G72] |
| Partner Agent | Agent inside Partner Network Hub (Next '26) that guides next steps, summarizes assets, coaches registrations and SOWs | [G6] |
| Agentic Earnings Hub | Earnings Hub with agentic features: auto-draft SOWs, monitor consumption milestones and auto-generate claim requests; paired with Earnings Potential Modeler | [G6] |
| Earnings Hub | Dashboard of rebates, discounts, funds and credits earned; launched 2024-10-17 | [G53] |
| Earnings Potential Modeler | Tool forecasting incentive earnings for a deal and mapping incentives to client level | [G6][G54] |
| SOW Analyzer | Gemini-based review of partner SOWs submitted for Google funding; Hub path Earnings > Funds Details > SOW Documents | [G52] |
| Partner Finder | Customer-facing, conversational partner search (Next '26) | [G6] |
| Producer Portal | Console tool for marketplace listings, pricing, private offers, reseller management | [G27] |
| Partner Sales Console | Reseller tool to accept ISV private offer plans and create resold private offers | [G36][G37] |
| Private offer | Customer-specific marketplace offer tied to the customer's Cloud Billing account ID | [G27] |
| MCPO | Marketplace Channel Private Offer: reseller-led private offer built from an ISV's reseller private offer plan; reseller bills customer | [G21][G37] |
| Private offer plan | ISV-defined wholesale plan (single-use or multi-use) that a reseller uses to create MCPOs | [G34][G20] |
| Vendor Net Revenue Schedule (VNRS) | Deal-type and TCV-based revenue share, effective 2025-04-21 | [G18] |
| Deal type | Field on a private offer: New, Migration, Native renewal, Channel shift | [G26] |
| Minimum Commitment | The customer's committed spend obligation with Google Cloud (often called "commit") | [G22] |
| MCCP | Marketplace Customer Credit Program, up to 3% credits to first-time buyers | [G45] |
| ISV Solution Connect | Invitation-only co-sell program and internal directory seen by Google field sellers | [G45][G75] |
| Google Cloud Ready - X | Product-team validation designations: BigQuery, AlloyDB, Gemini Enterprise (and historically Sustainability) | [G58][G59][G61] |
| A2A / Agent Card | Agent2Agent protocol; JSON Agent Card stored in Cloud Storage defines a marketplace agent listing | [G39] |
| Agent Gallery | Catalog inside the Gemini Enterprise app where employees request partner agents and IT approves | [G8] |
| RaMP | Rapid Migration and Modernization Program; 2026 terms with credits and partner services funds | [G55] |
| PSF / GSF | Partner Services Funds (paid to partner for approved SOW) / Google Cloud Consulting Services Funds | [G55] |
| DAF | Deal acceleration fund(s) for workshops and POCs referenced by Google leaders and analysts; no public program page found | [G54][G78] |
| FSR | Field Sales Representative (Google account executive) | [G70][G81] |
| CE | Customer Engineer (Google pre-sales technical) | [G70][G81] |
| PDM | Partner Development Manager (partner-side relationship owner) | [G51][G81] |
| FDE | Forward deployed engineer, embedded with select SIs under the $750M fund | [G6] |
| Agency model / Merchant of Record | Marketplace transaction models; agency model means ISV is merchant of record and customer may get split invoices | [G25] |

---

## 1. Fiscal calendar, org and where decisions get made

### 1.1 Fiscal year and planning moments

| Item | Detail | Source |
|---|---|---|
| Fiscal year | Alphabet reports on the calendar year (Q1 Jan-Mar, Q2 Apr-Jun, Q3 Jul-Sep, Q4 Oct-Dec). Google Cloud seller quotas follow the calendar year. | [G90] |
| Quarter ends that matter | Mar 31, Jun 30, Sep 30, Dec 31. Customer commit-consumption pressure peaks before a customer's own commit anniversary, not Google's quarter end. | [G22][G70] |
| Program year | Partner Network kicked off 2026-01-15; Google calls program-year guides "Y26" (a "Program Guide - Y26" circulates, login-gated) | [G4][G5] |
| Partner Kickstart | Regional January/February partner kickoffs (North America Kickstart 2026 held; event pages now 404) | search results only |
| Google Cloud Next '26 | 2026-04-22 to 04-24, Las Vegas, 32,000+ attendees, Partner Summit and Partners of the Year | [G7] |
| Google Cloud Next '27 | 2027-04-13 to 04-15, Mandalay Bay, Las Vegas (select programming 04-12) | [G89] |
| Earnings | Q2 2026 reported 2026-07-22: Google Cloud revenue USD 24.8B, +82% YoY, backlog USD 514B (INDEPENDENT) | [G65] |
| Scale claims | May 2026: USD 80B annual run rate and USD 462B committed-spend backlog (Dai Vu) | [G64] |

**Planning rhythm to use with Google:** Q4 (Oct-Dec) is when Google's FY plans, territory assignments and account plans are built. Get into account plans in Nov/Dec; land joint business plans in Jan/Feb after Kickstart; use Next (April) for announcements and executive access; push marketplace closes into Q2 and Q4 ends.

### 1.2 Who's who (partner-relevant leaders, as of 2026-09)

| Person | Role | Status | Source |
|---|---|---|---|
| Kevin Ichhpurani | President, Global Ecosystem, Google Cloud | Active; owns $750M fund announcement | [G6][G14] |
| David Smith | Head of Global Partner Program / channel chief (ex-Microsoft VP WW Channel Sales); reports to Ichhpurani; mandate "agentic transformation" of the channel | Since March 2026 | [G11][G14] |
| Colleen Kapase | Former VP Channels and Partner Programs; authored Partner Network launch | Left March 2026; now VP Strategic Global Partnerships, OpenAI | [G11][G12] |
| Philip Larson | Former MD, Google Cloud Partner Network | Left; joined OpenAI July 2026 | [G13] |
| Dai Vu | MD, Google Cloud Marketplace and ISV GTM Initiatives | Active (May 2026) | [G64] |
| Satish Thomas | VP, Applied AI and Platform Ecosystem (agents in Gemini Enterprise) | Active (Apr 2026) | [G8] |
| Shobana Shankar | Head of ISV Sales, Data Analytics | Active (Mar 2026) | [G77] |
| Samrah Khan | Director, SI partnerships NA (earlier Head of Strategic SaaS Partnerships) | Active (Feb 2026) | [G78][G80] |
| Rajiv Batra | Head of GSI Sales and GTM | Active (Mar 2026) | [G79] |
| Mike Shea | Head of partner co-sell, U.S. enterprise | Active (Feb 2026) | [G80] |
| Shelby Johnston | Channel sales leader, North America partner ecosystem | Active (Feb 2026) | [G80] |
| Lakshmi Saranath / Arjun Lahiri | Global Directors, partner programs strategy and incentives | Active (Jun 2025) | [G52] |
| Sandy Janes | Head of Partner Program Communications (Canalys study) | Active (Jun 2025) | [G51] |
| Oliver Schulz | BDM, Google Cloud Marketplace (AI agents) | Active (Oct 2025) | [G62][G76] |
| Marc Harpster | Resell Strategic Initiatives Lead (launched MCPO) | 2025 | [G76] |
| Gary Denman | Head of Partnerships and Alliances, ANZ | Jan 2026 | [G5] |

### 1.3 Field roles a partner deals with

| Role | Side | What they care about | How to use them | Source |
|---|---|---|---|---|
| Field Sales Rep (FSR) / account executive | Customer-facing | Consumption growth, commit consumption, marketplace attainment, AI wins, net-new logos | Bring a named account, a commit-drawdown angle and a GCP consumption story | [G70][G78][G81] |
| Customer Engineer (CE) | Customer-facing technical | Architecture, POCs, consumption | Give a 5-minute technical brief, reference architecture, integration docs | [G70][G81] |
| Specialist sellers (data/AI, infra, security, app mod) | Customer-facing | Workload-specific quota | Align your product to their workload (BigQuery, Vertex, AlloyDB, SecOps) | [G81] |
| ISV sales specialist (e.g. ISV Sales, Data Analytics) | Partner-facing but quota-carrying | Marketplace revenue, Google-sourced ISV opps (they carry a target to source opps for ISVs), 3x pipeline coverage | Treat as an embedded seller; run JBP and pipeline reviews with them | [G77] |
| Partner Development Manager (PDM) / partner manager | Partner-facing | Program progression, JBP, funding, registrations | Owner of tier/competency progress and funding asks | [G51][G81] |
| Partner Engineer | Partner-facing technical | Integration quality, validations | Needed for Google Cloud Ready validations; also resolves pricing-plan deletions | [G40][G58] |
| Marketplace team (BDMs, onboarding) | Marketplace | Listings, private offers, channel resale | Onboarding form, Project Info Form, MCCP pre-approval (mccp@google.com) | [G16][G45] | <!-- VALIDATE-OK[person-address]: published role mailbox, not a person -->
| Sub-regional co-sell teams | Customer-facing coordination | Partner-attached pursuits | Under-used channel per practitioner report | [G81] (CREATOR) |
| Forward deployed engineers | Google engineering | Production agent deployments at select SIs | Only via $750M fund with select GSIs | [G6] |

Practitioner note (CREATOR): Google's customer-facing org (FSR, CE, specialists) and partner-facing org (PDM, ISV specialists) are more visibly separate than at AWS or Microsoft. A PDM cannot "bring deals" from an org they are not embedded in; mature ISVs name counterparts on both sides [G81].

### 1.4 Why a Google seller cares (compensation and incentives)

| Claim | Evidence | Label |
|---|---|---|
| Google reps are incentivized to work with marketplace partners | "With Google sales reps incentivized to work with you, and Marketplace vendors closing deals 112% larger" (Google blog, 2026-04-23) | OFFICIAL [G8] |
| Most marketplace solutions are eligible for quota attainment; SPIFFs on closed co-sell deals | Dai Vu on Clazar podcast, 2024-04-03 | VENDOR-hosted, Google speaker [G71] `[UNVERIFIED, source dated 2024-04]` |
| ISV sales team comp includes a target to source opportunities for ISVs | Shobana Shankar, 2026-03-06 | CREATOR-hosted, Google speaker [G77] |
| Partners are in every account plan and business plan of direct sellers | Shobana Shankar, 2026-03-06 | [G77] |
| Google measures partners on net-new logos, AI revenue and consumption growth | Samrah Khan, 2025-09-02 | [G78] |
| Upper-enterprise customers increasingly contract directly with Google; resale "still has a place" but co-sell is key | Kapase to CRN, 2026-01-13; Omdia 2026-05-11 notes hyperscalers "taking large enterprise resell deals directly" | [G4][G82] |
| Internal lead scoring ranks incoming co-sell and services registrations to share them more broadly internally | Larson to CRN, 2026-01-13 | [G4] |

**The "why would a seller care" answer:** a marketplace private offer (a) retires the customer's Google commitment (up to the 25% cap), (b) counts toward the seller's attainment on most listings, (c) shows up as a registered, outcome-linked co-sell that Google's own program now measures, and (d) can drag Google consumption (the listing requirement is "meaningful Google Cloud consumption") [G8][G17][G22][G71].

---

## 2. Navigating the portal(s)

### 2.1 Portal inventory

| Portal | URL | Used for | Who needs access |
|---|---|---|---|
| Partner Network Hub | https://partners.cloud.google.com | Enrollment, company profile, users and roles, Marketplace Vendor Agreement, "View tasks > Partner tasks", program progress (tiers, competencies), registrations, Earnings Hub, SOW Analyzer, Partner Agent, Bot-Assisted Live Chat, MCCP Credits Request Form, Partner Support Desk | Alliances, sales ops, finance, partner admins |
| Enrollment | https://partners.cloud.google.com/enrollment | New company enrollment (login required) | First admin |
| Producer Portal | https://console.cloud.google.com/producer-portal?project=PUBLIC_PROJECT_ID | Listings, pricing, technical integration, private offers, reseller settings, reseller discounts, reports, analytics | Product, eng, deal desk |
| Private Offers page | https://console.cloud.google.com/producer-portal/private-offers | Create/manage offers; Settings for multiple orders and account approval | Deal desk |
| Marketplace payments | https://console.cloud.google.com/partner/payments | Payments profile, bank, tax forms, transactions, payouts | Finance |
| Solution analytics | Producer Portal analytics (console.cloud.google.com/partner/analytics) | Listing traffic and campaigns | Marketing |
| Partner Sales Console | Linked from reseller docs | Resellers: private offer plans, resold private offers, discounts acceptance, alerts | Resellers |
| Delivery Navigator | https://deliverynavigator.cloud.google.com | Services partners: delivery methodology and tools; requires Hub-registered users and Partner Admin ToS | Services delivery |
| Partner Support Desk | https://g.co/cloud/psd-partner (via Producer Portal Overview > Contact Marketplace support) | Marketplace and program support; include the word "Marketplace" | Everyone |
| Marketplace Vendor Agreement | https://partners.cloud.google.com/marketplace-vendor-agreement (accepted version); public: https://cloud.google.com/terms/marketplace-vendor-agreement | Legal | Partner Admin |

Sources: [G15][G16][G24][G27][G32][G36][G44][G63].

### 2.2 Menu paths that are documented publicly

| Task | Path | Source |
|---|---|---|
| Start marketplace onboarding | Partner Network Hub > View tasks > Partner tasks > Initiate onboarding your product to Marketplace | [G16] |
| Accept Marketplace Vendor Agreement | Partner Network Hub (Partner Admin only) > agreement task | [G16] |
| Upload SOW for funding review | Partner Network Hub > Earnings > Funds Details > SOW Documents | [G52] |
| Create private offer | Producer Portal > Private Offers > Create offer | [G27] |
| Extend offer acceptance deadline | Producer Portal > Private Offers > Manage your offers (more_vert) > new date (within 3 months) > Save | [G29] |
| Turn on multiple orders (SaaS flat fee) | Producer Portal > Private Offers > Settings > Multiple Orders > select products > confirm Procurement API update > Enable multiple orders (irreversible) | [G32] |
| Turn on account approval (SaaS) | Producer Portal > Private Offers > Settings > Account approval > select products > Activate account approval (irreversible) | [G32] |
| Manage allowed resellers | Producer Portal > Account management > Settings > Reseller management > Manage reseller network (toggle "Auto allow new resellers to resell my products") | [G35] |
| Configure a reseller discount | Producer Portal > Reseller discounts > choose org and billing account > Configure reseller discount | [G34] |
| Add AI agent product | Producer Portal > Add product > Product type: AI agent as a service > name > Create | [G41] |
| Add pricing (agents) | Producer Portal > product Overview > Pricing > Edit > define structures > Set up > add details > Submit | [G40] |
| Update price after launch (30+ days after approval) | Producer Portal > product > pricing section > Edit content > Submit price model | [G40] |
| Contact marketplace support | Producer Portal > Overview > Contact Marketplace support | [G44] |
| Payments profile and bank | Payments page > Manage payment methods > Add payment method > Set as primary > Save; verify test deposits | [G24] |
| Payments users | Payments page > Manage settings > Payments Users > Manage payments users > Add new user | [G24] |
| Tax forms | Payments page > Manage settings > Payments profile > United States tax info (W-9 or W-8BEN-E; treaty rate under "Other Copyright Royalties") | [G24] |
| Reseller accepts private offer plan | Partner Sales Console > Private offer plans (or Alerts) > Pending acceptance > Accept > Confirm acceptance | [G36] |
| Reseller creates resold private offer | Partner Sales Console > Customers > [customer] > Private offers > Create private offer > Use this plan | [G37] |
| Connect a co-sell tool | Partner Network Hub > user management > add tool's service account with Integrator role; copy Company name and Partner ID from Hub Account page | [G72] |

### 2.3 IAM roles you will need

| Role | Needed for | Source |
|---|---|---|
| Partner Admin (Hub) | Accept Marketplace Vendor Agreement, Delivery Navigator ToS, manage users | [G16][G63] |
| Integrator (Hub) | Third-party co-sell sync | [G72] |
| Project Editor (roles/editor) on the marketplace project | Payments, multiple orders, account approval | [G24][G32] |
| Commerce Producer Viewer + Commerce Price Management Private Offers Admin | Create private offers without Project Editor; custom EULA needs Private Offers Admin | [G27] |
| Project Viewer + payments profile Read access | View payment reports | [G24] |
| Billing Account Administrator (org level) + Google Cloud Reseller Admin (Partner Sales Console) | Resellers | [G36] |
| Customer side: Billing Administrator, or Billing User + Consumer Procurement Order Administrator | Customer accepting your private offer | [G30] |

Recommended project ID convention for marketplace: `PARTNER_NAME-public` [G41].

---

## 3. Registration: step by step

### 3.1 Prerequisites
- A Google account on your corporate domain (Google Workspace or Cloud Identity) for every user; users must be registered in Partner Network Hub to reach tools like Delivery Navigator and Partner Support Desk [G44][G63].
- For marketplace: organization incorporated in a supported region; a payments profile whose legal entity name matches the entity that signs the Marketplace Vendor Agreement and whose address is in the country of incorporation [G17][G24].
- For listing: product production-ready (not alpha/beta), enterprise-ready (professional online presence, defined sales motion, support, security practices), hosted primarily on Google Cloud per an approved pattern [G17].

### 3.2 Steps (zero to enrolled and listed)

| # | Step | Where | Time (published or observed) | Done when | Source |
|---|---|---|---|---|---|
| 1 | Enroll the company in Google Cloud Partner Network | partners.cloud.google.com > Become a partner / enrollment | Not published | Company account exists; you can log into Partner Network Hub | [G3][G16] |
| 2 | Register additional users ("Register as a user" / User Registration Form); assign at least 2 Partner Admins | Hub | Minutes | Colleagues can log in; admins can accept agreements | [G3][G44] |
| 3 | Choose partner path(s): co-selling, services, technology (ISVs selling on marketplace need Technology Partner authorization) | Hub | Not published | Path shows in profile | [G3][G16][G45] |
| 4 | Complete profile and link certifications and delivery-readiness data (Hub pulls these automatically) | Hub | Ongoing | Program progress dashboard populates | [G4] |
| 5 | Start marketplace onboarding: View tasks > Partner tasks > Initiate onboarding your product to Marketplace; submit architecture diagrams and business inputs (Onboarding/Solution Validation form) | Hub | Varies; VENDOR estimate 1-4 weeks for enrollment + agreement | Product approved against listing requirements | [G16][G42][G67] |
| 6 | Accept Marketplace Vendor Agreement (Partner Admin) | Hub | Minutes once legal clears | Accepted version visible at partners.cloud.google.com/marketplace-vendor-agreement | [G16] |
| 7 | Create a Google Cloud project for listings (`PARTNER_NAME-public`) | Console | Minutes | Project exists | [G16][G41] |
| 8 | Complete the Cloud Marketplace Project Info Form | Link from marketplace team | Not published | Producer Portal access | [G16] |
| 9 | Set up payments profile, bank account, tax form (only after agreement is final) | Payments page | Test-deposit verification days | Primary bank verified | [G24] |
| 10 | Configure Producer Portal access control | Producer Portal | Minutes | Team roles set | [G16] |
| 11 | Submit pricing model | Producer Portal | Up to 4 business days review | Pricing approved | [G16][G40] |
| 12 | Integrate (SaaS: Procurement API, Pub/Sub, SSO/account linking; agents: Agent Card; VM/K8s: packages) | Eng | VENDOR: 8-16 weeks end to end for SaaS | Technical integration approved | [G39][G67] |
| 13 | Test with a Test Billing Account (100% discount "Marketplace Partner Testing") | Console | Days | Test purchase and entitlement flow work | [G43] |
| 14 | Publish | Producer Portal submissions; agents get a gcloud command to make listing public | Days | Listing public | [G39] |
| 15 | Prepare GTM (Hub GTM benefits page) | Hub | Ongoing | JBP drafted with PDM | [G16] |

### 3.3 Common blockers

| Blocker | Symptom | Fix | Source |
|---|---|---|---|
| Product hosted mainly on AWS/Azure | Onboarding validation stalls | Re-architect to an approved pattern (e.g. Pattern 2: data plane on GCP) or do not list | [G17] |
| Payments legal-entity mismatch | Payment setup errors | Match MVA entity name and country | [G24] |
| Single payments admin | Profile closed when person leaves | Add at least one more admin | [G24] |
| Google Payments disabled for Workspace account | OR-DDUH-01 | Workspace admin turns on Google Payments | [G24] |
| Wrong project selected | "Unable to find the resource" | Select the project with Producer Portal access | [G24][G41] |
| Can't reach Partner Support Desk | Access denied | Register user in Partner Network (User Registration Form); else public form | [G44] |
| Using stale Partner Advantage guides | Wrong portal, wrong tier names | Use docs.cloud.google.com/marketplace and Hub | [G70][G74] |
| Pricing names or plans rejected | Review loops | Names under 58 characters, no $0 private plans, no POC free plans, at least one feature per plan, no pro-services line items | [G40] |

---

## 4. Tiers, paths, designations, competencies, badges: exact qualification criteria

### 4.1 Tiers (Partner Network, 2026)

| Tier | Google's description | Reported thresholds (CRN AU, INDEPENDENT) | Measured how | What it unlocks |
|---|---|---|---|---|
| Select | "Foundational knowledge and successful client engagements" | USD 250K partner co-sell ACV | Automatic from registered co-sell and services outcomes across Google Cloud and Google Workspace | Program participation, visibility; unlocks not itemized publicly |
| Premier | "Significant investment in certified technical resources and consistent history of driving customer outcomes at scale" | USD 2M partner co-sell ACV | Same | Higher standing with field; incentives not published publicly |
| Diamond | "Highest partnership level... deepest global commitment... large-scale, complex deployments"; "intentionally selective" | USD 20M partner co-sell ACV + 20 partner-implemented workloads + 30 partner co-sell influenced opportunities + 200 professional certifications | Same; tiers exist per track (co-sell, services, technology) | Top visibility; "the first call a salesperson or customer is going to make" per Kapase | <!-- VALIDATE-OK[customer-name]: substring of spokesperson or salesperson, not a customer -->

Sources: descriptions [G1][G2]; thresholds [G5] (INDEPENDENT; Suger states Google publishes none [G66]); per-track Diamond [G4].

Notes and conflicts:
- A practitioner guide (flashdba, CREATOR) describes Select as "marketplace listing live, basic profile, competency activity initiated" and Premier as 12-18 months from Select [G81]. This conflicts with the CRN AU dollar thresholds and is not sourced to Google. Prefer [G5] pending the program guide.
- Existing partners were "not guaranteed to retain their current tier" at transition [G85]. Former Partner Advantage "Partner" maps to Select [G5].
- Tiering considers outcomes "across Google Cloud and Google Workspace" [G1].

### 4.2 Partner paths

| Path | Who | What Google measures | Source |
|---|---|---|---|
| Co-selling | ISVs and partners who co-sell with Google field (including resale business per one practitioner) | Registered co-sell influence, partner co-sell ACV | [G3][G4][G81] |
| Services | SIs, consultancies, MSPs | Workshops, assessments, pilots; closed SOWs; delivery capacity (certified people per solution area) | [G4][G92] |
| Technology | ISVs building products that integrate with Google; marketplace vendors must be authorized as Technology Partner | Co-innovation, marketplace, integrations | [G3][G16][G45] |

A partner can hold more than one path (practitioner report) [G81].

### 4.3 Competencies (21 areas, two levels)

| Category | Areas | Source |
|---|---|---|
| Product (5 per CRN; 4 on Google's page) | Apigee (CRN only), Chrome, Gemini Enterprise, Google Maps Platform, Looker | [G2][G4] |
| Solution (6) | Artificial Intelligence, Application Modernization, Data & Analytics, Databases, Infrastructure, Security | [G2][G4] |
| Industry (10) | Business & Professional Services; Consumer Packaged Goods; Financial Services; Healthcare & Life Sciences; Logistics; Manufacturing & Industrial; Public Sector & Education; Retail & Consumer; Software & Internet; Telecom, Media & Gaming | [G2][G4] |

| Level | Criteria (published at framework level only) | Source |
|---|---|---|
| Competency | Capacity (technical certifications, sales credentials) + capability (pre-sales and post-sales contributions to validated closed/won opportunities) | [G1] |
| Advanced Competency | "Same measuring metrics, but who's doing it at a broader scale" (Larson) | [G4] |

Exact certification counts and opportunity counts per competency: not published publicly (login-gated program guide). Competencies do not depend on tier [G1].

### 4.4 Subprograms

| Subprogram | What | Source |
|---|---|---|
| Resale Subprogram | Authorization to resell Google Cloud and marketplace products (MCPO via Partner Sales Console) | [G33][G36] |
| Managed services | "Ongoing managed services" subprogram | [G2] |
| Product capacity programs | Gemini Enterprise, Google Maps Platform | [G2] |

### 4.5 Technical designations (ISV)

| Designation | Minimum criteria | Process | Benefits | Source |
|---|---|---|---|---|
| Google Cloud Ready - BigQuery | Production-quality BigQuery integration; at least 5 customers in production with BigQuery; 1 public case study | Evaluate (Google runs integration tests in sandboxed production), Enhance, Enable; category-specific tests (BI/ML; connectors and dev tools; governance/security/MDM; quality/observability/FinOps; ETL/integration); no charge | Badge; priority placement on BigQuery partner page; extra GTM (blogs, PR, workshops, webinars); partner engineering and product team roadmap access; quarterly feature previews | [G58] |
| Google Cloud Ready - AlloyDB | Production-quality AlloyDB integration or willingness to build one; "registered Google Cloud partner at Partner Tier" (stale wording) | Apply via Hub or interest form; Evaluate/Enhance/Enable; categories (BI; governance/modeling/security; integration/migration; quality/observability) | Badge; AlloyDB partner page placement; GTM; early access | [G59] |
| Google Cloud Ready - Gemini Enterprise | Agent passes four-step evaluation: basic functionality, output accuracy, autonomous execution, enterprise standards; A2A + Gemini/Model Garden model | Via AI Agent Ecosystem Program / AI Agents Program application | Featured in Agent Gallery inside Gemini Enterprise app | [G8][G60][G61] |

Other historic Google Cloud Ready tracks (e.g. Sustainability) were referenced in 2023 [G87]; current status not verified.

### 4.6 ISV Solution Connect (co-sell directory)

| Item | Detail | Source |
|---|---|---|
| Nature | Invitation-only co-sell program; members appear in an internal ISV Solution Connect Partner Directory used by field sellers | [G75] (VENDOR, 2025-02) |
| Reported eligibility | Build-authorized (now Technology), product mostly on Google Cloud, 2+ marketplace deals of USD 10K+, paid listing, categories data/analytics, security, dev tools, networking, AI/ML, Partner or Premier level | [G75] `[UNVERIFIED, source dated 2025-02]` |
| Registration | First-year contract value (USD 10K minimum), expected close date, support needs | [G75] `[UNVERIFIED, source dated 2025-02]` |
| Assets | Sales card with three customer stories, competitive insights, objection handling; better-together solution brief | [G75] |
| Official confirmation | Google's MCCP brief uses ISV Solution Connect to register MCCP opportunities and mark them won | [G45] |

---

## 5. Marketplace

### 5.1 Eligibility (organization and product)

- Join and maintain good standing in Partner Network; incorporated in a supported region; marketplace vendor account and payment profile in good standing [G17].
- Production-ready, enterprise-ready, no malicious code, hosted primarily on Google Cloud via an approved pattern; same features as off-marketplace versions; data products must not contain PII as defined in the Protecting Americans' Data from Foreign Adversaries Act of 2024; customer-deployed components must implement tenant consumption tracking; "must result in meaningful Google Cloud consumption" [G17].
- Standard revenue share applies only to products that meet requirements and "pass a business case review"; otherwise Google "might offer you an adjusted revenue share" [G17].

**Nine approved hosting patterns** [G17]:

| # | Pattern | Key test |
|---|---|---|
| 1 | Fully hosted on Google Cloud | Everything on GCP |
| 2 | Compute or data plane on GCP | GCP resource must be the fastest-growing with usage; small control planes elsewhere OK |
| 3 | Storage and backup on GCP | Must replicate all data to GCP |
| 4 | Migration to GCP | GCP is the only destination |
| 5 | Agent data analysis on GCP | Agents anywhere, data sent to GCP for storage/analysis |
| 6 | Datasets hosted on GCP | Delivered through GCP |
| 7 | Google Distributed Cloud | VM/K8s on GDC devices |
| 8 | AI agents hosted on GCP | AI Agent as a Service via Gemini Enterprise, fully on GCP |
| 9 | AI agents with hybrid infrastructure | Core on GCP using Google or Model Garden models; GCP agent resource fastest-growing |

### 5.2 Listing types

| Type | Notes | Source |
|---|---|---|
| SaaS billed by Google (Integrated SaaS) | Runs on your infrastructure; billed by Google; Procurement API + Pub/Sub; subscription, usage, combined pricing | [G16] |
| VM products | Compute Engine images; trials supported | [G16][G26] |
| Kubernetes apps (GKE, GKE Enterprise), incl. Terraform K8s apps with usage-based GKE pricing (Dec 2025) | [G16][G26] |
| Container images | Open source containers | [G16] |
| Dataset / data products | Delivered via GCP (Analytics Hub/BigQuery) | [G15][G16] |
| AI agents | A2A "AI agent as a service" (Gemini Enterprise), or SaaS, K8s, or professional services for agents | [G39] |
| Professional services | Only via private offer; must link to a commercial third-party listing; US vendor and US customer only; agency model; categories Assessment, Implementation, Premium support, Managed services (and others) | [G42] |
| Free container images | Free listings | [G15] |
| Standalone SaaS (not billed by Google) | Deprecated since 2019 | [G26] |

### 5.3 Fees (revenue share)

**Vendor Net Revenue Schedule**, effective 2025-04-21 (schedule page last modified 2025-03-10) [G18]:

| Deal type | TCV (USD) | Google fee | Vendor keeps |
|---|---|---|---|
| Private offer, New | < 1M | 3% | 97% |
| Private offer, New | >= 1M and < 10M | 2% | 98% |
| Private offer, New | >= 10M | 1.5% | 98.5% |
| Channel shift, Migration, Native renewal | Any | 1.5% | 98.5% |
| Standard (public, non-private-offer) | Any | 3% | 97% |

Definitions [G18]:
- **Channel shift:** new private offer replacing an existing non-marketplace deal with the same customer for the same product, workload already on GCP.
- **Migration:** same, but the old workload was not on GCP and the new one is on GCP from the start date.
- **Native renewal:** auto-renewal of a marketplace private offer, or a new private offer replacing a prior marketplace transaction for the same product where both workloads are on GCP, the original ran at least 9 months, the new offer starts within 90 days of expiry, or an amendment increases both duration and TCV by at least 60%.

Rules that change the money [G19][G20]:
- Applies to new transactions and auto-renewals from 2025-04-21; installments of deals whose terms started earlier keep old terms until renewal.
- Requires current Marketplace Vendor Agreement and compliance with listing and operational requirements; **transactions that include professional services are excluded**.
- TCV is taken from the private offer at publish time. Usage-only pricing has TCV zero, so it stays at 3%; CUD commitments count toward TCV (overage does not).
- Native renewal above USD 10M TCV requires Google review before customer acceptance.
- Multi-use reseller private offer plans default deal type to "new"; use single-use plans to set migration, channel shift or native renewal.
- Usage after a private offer ends reverts to 97% (3%).
- Mis-labelling deal type: "Google reserves the right to make adjustments."
- Resold deals: ISV sees an estimated revenue share in Producer Portal; reseller and customer do not.

Before 2025-04-21 the fee was a flat 3% [G21].

Channel/MCPO fee: Google docs apply the reseller discount before revenue share (example: USD 100 list, 10% reseller discount, 3% fee, vendor nets USD 87.30) [G34]. Suger claims "no incremental ISV fee" on MCPO versus an AWS CPPO uplift (VENDOR) [G67]; Google does not publish a separate MCPO fee line, consistent with that claim.

### 5.4 Private offers (ISV-direct)

| Parameter | Rule | Source |
|---|---|---|
| Prereqs | Listed, integrated product; customer's Cloud Billing account ID; IAM roles above; SaaS entitlements configured | [G27] |
| Steps | Create offer > product and customer details > pricing (model, billing frequency, auto-renew) > EULA (Google standard or custom) > review and publish > send URL | [G27] |
| Pricing models | Usage only with discount; CUD (commitment with overage at list, or commitment with all usage discounted); flat fee; flat fee with usage; provisioned throughput for models | [G29][G47] |
| Billing frequency | Monthly, quarterly, annually, custom; Brazil billing accounts must be monthly | [G28] |
| Installments | Each installment's per-day value must be >= 50% of the previous one | [G28] |
| Term | Up to 5-year upfront payments with annual amortized drawdown (June 2024); contract lengths up to 7 years (Oct 2024) | [G26][G47] |
| CUD balances | Released at start of each installment; choose expire vs roll over; partner-sponsored one-time credits allowed | [G26][G29] |
| Acceptance deadline | Offer expires 11:45 PM Pacific on deadline date; extendable to within 3 months without new URL | [G26][G29] |
| Amendments | Create a new offer on the same billing account; can change end date, remaining installments, future installments; cannot change paid installments or billing frequency; amended TCV >= 50% of current TCV; no changes within 24 hours of expiry | [G29] |
| Auto-renew | Opt-in by ISV; customer can toggle; not supported with custom billing frequency; max renewals depend on remaining installments | [G31] |
| Customer purchase | One-time purchase per offer; customer needs Billing Admin, or Billing User + Consumer Procurement Order Administrator | [G30] |
| SaaS approval | ISV must approve accepted SaaS offers (or enable auto approval for scheduled start dates) | [G30][G32] |
| Multiple orders | Flat-fee SaaS; one entitlement per accepted offer; irreversible to enable | [G32] |
| API | Cloud Commerce Producer API can create, manage and publish private offers, attach EULA/SOW, pick offer to amend (2026-07-24) | [G26] |
| Status "Pending Google Approval" | Offer auto-sent after Google approves | [G30] |
| Download | PDF export with internal notes and EULA | [G26] |

### 5.5 Channel and reseller offers (MCPO / resale)

**ISV side** [G33][G34][G35][G38]:
1. Confirm your Marketplace Vendor Agreement includes resale terms (may require an amendment; ask your Business Development rep).
2. Turn on reselling for all your marketplace products. When first turned on, all current resellers are allowed and new ones auto-added (toggle in Manage reseller network).
3. Create private offer plans (single-use for one customer/product/time, or multi-use for many customers via one reseller) with the reseller discount baked in; reseller must accept in Partner Sales Console.
4. Or configure a standing reseller discount on a resold customer subaccount (percent, start date, optional end date); reseller must accept before the start date or you resubmit; if accepted on the start date it takes effect next day.
5. Since 2024-05-20, discount changes do not apply to active commitment or flat-fee purchases unless you amend or renew them; usage charges pick up changes at invoicing.
6. Customer Insights reports for resold customers show reseller name/address, not end-customer identity.

**Reseller side** [G36][G37]:
- Must be accepted in Partner Network and authorized in the Resale Subprogram.
- Cannot buy with the reseller parent billing account; must use resold customer subaccounts.
- Creates offers in Partner Sales Console; Google invoices the reseller for the plan amount (invoice visible by the 5th business day of the following month) and disburses to the ISV; reseller bills and invoices the end customer and recognizes topline revenue [G21][G37].
- Reseller purchases retire the customer's commit only if associated with the customer by the reseller and the Google rep and not inside a reseller-held commitment [G22].
- Channel momentum: third-party GTV resold through channel partners grew 170% from 2023 to 2024 [G21][G49].

### 5.6 Committed-spend drawdown: exactly what counts

| Question | Answer | Source |
|---|---|---|
| Rate | 100% of eligible marketplace spend | [G23] |
| Cap | Combined eligible marketplace amounts retire at most 25% of a given Minimum Commitment; excess neither counts nor rolls over | [G22] |
| Direct purchases | Count if the service is deployed on Google Cloud Platform | [G22] |
| Reseller purchases | Count for new purchases/renewals after 2025-06-08 if reseller and Google rep associate the purchase with the customer, and not part of a reseller-held commitment | [G22] |
| Exclusions | All Google Maps offerings; Google Ads; services not running on Google Cloud; resold services where vendor has not opted into resale; services owned by purchaser or its affiliate; professional services | [G23] |
| Multi-year upfront | Installments longer than 12 months apply pro rata per year (e.g. USD 4,500 over 3 years = USD 1,500/yr) | [G22] |
| Rate lock | Rate applied is the one in effect when the customer procures or renews | [G22] |
| "Google Cloud Ready" and commit | No link: Google Cloud Ready is a technical validation badge, not a commit-eligibility label. Commit eligibility follows the hosting requirement and exclusions above | [G17][G23][G58] |
| MCCP credits vs commit | MCCP credits are on top of drawdown | [G45] |
| RaMP service credits | Do not count toward Minimum Commitment | [G55] |

**Sales talk track:** "Buying us on Google Cloud Marketplace spends money you already committed to Google, up to a quarter of your commit, with one bill." Ask every prospect: commit size, anniversary date, how much of the 25% marketplace headroom is used.

### 5.7 Payments and disbursement

| Item | Detail | Source |
|---|---|---|
| Cadence | Google computes monthly; payouts typically on the 21st of each month; you never invoice Google | [G24] |
| Usage reporting deadline | Report usage by 6 AM Pacific on the 1st to appear on the prior month's invoice | [G24] |
| Currency | Prices set in USD; customers pay in local currency; payouts in supported currencies (AUD, EUR, CAD, USD, HKD, ILS, JPY, NOK, PLN, SEK, CHF, GBP; India and Saudi Arabia in USD) | [G24] |
| Tax | W-9 (US) or W-8BEN-E; merchant-of-record transactions may need Singapore (APAC) or Ireland (EMEA) tax info | [G24] |
| Transaction models | Agency model (ISV is merchant of record; split invoicing in UK, DE, FR from 2025-02-01; Israel 2025-06-01; BE, IT, LU, NL, PL, ES, SE 2025-09-01; Switzerland 2026-06-01 with three documents; Australia 2026-08-01 with up to four documents and domestic sellers invoicing GST themselves) vs Google as merchant of record | [G25] |
| Reports | Customer Insights, Detailed Disbursements, Charges and Usage, Disbursement; BigQuery delivery (2025-07-17); D+1 delivery from 2026-05-27; city field added 2026-07-30; marketplace_fee_amount and fee_percent fields since 2024-07 | [G26] |
| Refunds | Partner-processed customer refunds supported | [G15] |
| Support | Partner Support Desk with "Marketplace" in description | [G24] |

VENDOR claim: cash lands 45-60 days after customer billing cycle [G67].

### 5.8 Listing operations and optimization

- Pricing review up to 4 business days; price decreases immediate after review; price increases take an extra 45 days (15 days to notify users + 30 days notice); price updates only 30+ days after last approval [G40].
- Pricing plan deletion impossible once purchased; contact your Partner Engineer [G40].
- Up to two Category IDs per solution for console filtering [G26].
- Free trials supported for VM, K8s and SaaS (historical feature) [G26].
- Solution analytics and campaign tracking in Producer Portal [G26].
- Sales lead management lets customers message you (needed for professional services) [G42].
- VENDOR guidance: keyword-specific titles and descriptions; Google field reps look at your listing before engaging [G67].

### 5.9 Buyer procurement angle and incentives

| Lever | Detail | Source |
|---|---|---|
| Single bill, existing agreement | Customers use existing Google Cloud billing and agreement | [G15][G48] |
| Commit drawdown | See 5.6 | [G22][G23] |
| MCCP | Up to 3% credits on first-time eligible purchase via private offer or MCPO | [G45][G46] |
| Private Marketplace | Customer governance of what employees can buy | [G46] |
| Standard terms | Industry-standard partner agreements with consistent terms across hyperscalers; vendors may use Google's or their own | [G46] |
| Agent Gallery procurement | Employees request agents; IT approves; purchase via marketplace | [G8][G62] |

**MCCP details** (program brief created 2025-01-08; program reconfirmed in Dec 2025 and on the sell page in Sep 2026) [G45][G46][G48]:

| Criterion | Value |
|---|---|
| Credit | Up to 3% of annualized GTV, general-use Google Cloud credits, 4 quarterly disbursements in arrears |
| Minimum deal | USD 100K annualized GTV |
| Maximum credit | USD 250K per qualifying ISV purchase (reached at ~USD 8.3M annualized GTV) |
| Eligible | First-time purchases of that ISV via private offer or MCPO; new or existing Google customers; with or without commit |
| Ineligible | Renewals, channel shifts from direct, public offers, pay-as-you-go |
| Partner eligibility | Technology partner; MVA 3.x+; business case validated; transactable listing; enrolled in ISV Solution Connect; 25 registered deals or USD 5M pipeline in last 12 months; 10 private offers or USD 1M GTV in last 12 months |
| Process | Register in ISV Solution Connect + MCCP Credits Request Form in Partner Network Hub (pre-approval) > eligibility email > customer buys via private offer, partner marks won > partner enters private offer ID and end customer ID in Hub > MCCP team disburses to customer billing ID. Contact: mccp@google.com | <!-- VALIDATE-OK[person-address]: published role mailbox, not a person -->
| Example | USD 15M over 3 years = USD 5M annualized GTV = USD 150K credit |

Thresholds `[UNVERIFIED, source dated 2025-01]`: re-confirm with your partner manager.

### 5.10 What makes a listing produce pipeline

1. **Private offers, not public listings, drive revenue.** VENDOR claim: most ISVs see more than 70% of marketplace revenue via private offers at enterprise scale [G67]. Public PAYG works for PLG: Databricks reports 500+ marketplace signups a month and 2x higher conversion from Google traffic because buyers arrive with billing IDs [G76].
2. **Alignment inside your company first.** Glean grew marketplace transactions 42x YoY by enabling its own sellers, finding a talk track that resonated with Google FSRs through hundreds of calls, and joining co-sell calls ("what dollars are you making Google sellers?") [G76].
3. **Comp neutrality for your sellers.** 96% of partners in the Futurum study had compensation-neutral programs; one applies a 15% over-base kicker [G49].
4. **Channel.** Canalys forecasts more than 50% of marketplace sales via channel partners by 2027 [G76]; WWT reports 40% of its marketplace business is net new [G76].
5. **Label deals correctly** (deal type, CUD vs usage) to capture 1.5-2% fees [G20].
6. **Be findable by the field:** ISV Solution Connect directory, Google Cloud Ready badges, competency, Agent Gallery [G45][G58][G8].

Published outcome benchmarks (Google-commissioned Futurum study of 705 partners, June 2025): 112% larger deals, 70% cite more multi-year deals, deals close 2-4 weeks faster (up to 50% time saved), 14% better retention, 90% grew marketplace revenue in 2024 [G49].

---

## 6. Co-sell

### 6.1 Eligibility ladder

| Level | Requirement | Effect | Source |
|---|---|---|---|
| Member of Partner Network | Enrolled, users registered | Can register opportunities in Hub | [G1][G3] |
| Transactable listing | Marketplace live | Deal can close on marketplace, retire commit, count for seller | [G68] |
| ISV Solution Connect | Invite-only; directory visible to field | Field can discover and engage; MCCP eligibility | [G45][G75] |
| Google Cloud Ready / competency / Agent Gallery | Validation | Priority placement, stronger field trust | [G58][G8] |
| Tier (Select/Premier/Diamond) | Outcome thresholds | Partner Finder and field ranking weight; "Diamond matters" | [G4][G5] |

### 6.2 How to share and register opportunities

- **Where:** Partner Network Hub (Kapase: "every single partner is out there registering their co-sell opportunities and services registrations") [G4]. Two registration families exist: co-sell registrations and services registrations [G4]. The exact Hub menu path for registration is login-gated and not documented publicly.
- **What to include (VENDOR guidance):** customer account details, deal size, timeline, GCP services involved, stakeholders, buyer stage, marketplace eligibility [G70][G74].
- **When:** during discovery or qualification, not after close; late registration loses co-sell value and, now, tier credit [G70].
- **Automation:** CRM sync via Tackle (Salesforce-native Google co-sell, bulk registrations, writeback, launched March 2026), Clazar, Suger, Labra; these connect with an Integrator-role service account in Hub [G72][G73][G70][G68].
- **What Google does with it:** internal AI lead scoring ranks co-sell and services registrations and shares them more broadly internally [G4]. Partner Agent coaches registrations [G6].
- **Credit:** Suger's framing: sourcing (who brought it) differs from credit (whether the closed, marketplace-transacted deal is recognized as a joint win); an off-marketplace close has no transaction to anchor credit [G68].

Stale-content alert: Clazar (2026 guide) and Tackle (May 2026 blog) still say "register in the Partner Advantage portal" and Clazar lists tiers as "Member, Partner, Premier plus Diamond"; both are wrong for 2026 [G70][G74].

### 6.3 What the field sees and responds to

| Google side | Responds to | Source |
|---|---|---|
| Customer-facing (FSR, CE, specialists, industry) | Consumption uplift, named-customer outcomes, commit drawdown, AI wins | [G78][G81] |
| Partner-facing (PDM, ISV specialists) | Marketplace transaction volume, tier progression, partner-attached pipeline, 3x pipeline coverage | [G77][G81] |
| Google leadership | Net-new logos, AI revenue, consumption growth | [G78] |

### 6.4 Referral flows both directions

- **Partner to Google:** registration in Hub; account mapping; JBP pipeline reviews.
- **Google to partner:** ISV sales specialists carry a target to source opportunities for ISVs; ISV Solution Connect directory; Partner Finder for customers; field referrals via account plans [G6][G77].
- GSIs: "There is nothing called partner source, Google source... it's truly about co-selling to the end customer together" (Rajiv Batra) [G79].

### 6.5 Opportunity quality, acceptance, SLAs

Not published: no public acceptance SLA, no published quality score. Google ranks registrations with internal AI lead scoring [G4]. Treat any SLA claim as unverified.

### 6.6 CRM integration and APIs

| Integration | What | Source |
|---|---|---|
| Hub co-sell registration via partners | Integrator role, Company name + Partner ID | [G72] |
| Cloud Commerce Partner Procurement API | Accounts, entitlements, Pub/Sub events (e.g. ENTITLEMENT_OFFER_ACCEPTED) | [G26][G62] |
| Cloud Commerce Producer API | Private offer create/manage/publish (2026-07-24) | [G26] |
| BigQuery reports | Detailed Disbursements, Customer Incremental Insights | [G26] |
| Public Google API for co-sell registration | Not documented publicly | none |

### 6.7 Seller engagement playbook that works (synthesized; sources per line)

1. Name one owner of the Google relationship with a Google-specific quota or MBO [G81].
2. Build a better-together narrative naming the GCP services you pull (BigQuery, Vertex AI/Gemini, GKE, AlloyDB) and a consumption number [G70][G75].
3. Map accounts quarterly with territory teams; bring target lists with context [G70].
4. Register every qualified deal at discovery with a specific ask of the Google seller [G76].
5. Ask about commit size and anniversary in discovery; route through private offer [G70].
6. Use MCCP where eligible for first-time buyers [G45].
7. Keep Google sellers updated after registration; share win wires [G70][G76].
8. Close on marketplace; set deal type correctly [G20].
9. For GSIs: industry-first joint solutions and live demos, not decks [G79].
10. Run monthly or bi-monthly channel pipeline reviews six months out with resellers [G76].

---

## 7. Incentives, funding and benefits (current published amounts)

| Program | What / amount | Who | How to claim | Status / date | Source |
|---|---|---|---|---|---|
| $750M partner innovation fund | Agent build support for ISVs, FDEs for SIs, deployment and usage incentives for services partners, training/workshops; sandbox credits, demand gen, deployment vouchers, services funding | GSIs, ISVs, channel | Through partner manager / Hub; no public form | Announced 2026-04-22 | [G6][G92][G10] |
| Partner funding via SOW (services funding, "multibillion-dollar funding program") | Google funds a portion of partner SOWs ("customer has skin in the game, we have skin in the game") | Services partners | Upload SOW in Hub > Earnings > Funds Details > SOW Documents; SOW Analyzer pre-check; human final approval | Live; SOW Analyzer at 90% of funded SOWs within six months | [G4][G52][G92] |
| Deal acceleration funds (DAF) | Funding for workshops and POCs pre-sale; Techaisle reports higher close probability when used | Services partners | Via partner manager / Earnings Hub | Amounts not published | [G54][G78] |
| Post-sales incentives, rebates, discounts, credits | Viewable in Earnings Hub by product family, customer, country, period; CSV export | Resellers and services partners | Earnings Hub | Amounts login-gated | [G53] |
| Agentic Earnings Hub | Auto-draft SOWs; monitor consumption milestones; auto-generate claim requests; Earnings Potential Modeler maps incentives to client level | All partners | Hub | Announced 2026-04-22 | [G6] |
| RaMP 2026 (migration) | Service credits (customer): General/VMware/Database/Data Analytics 25% of incremental TTM spend per quarter up to lesser of 30% of projected annual run rate or USD 3M; Oracle 65% up to lesser of 70% or USD 3M; Windows 35% up to lesser of 40% or USD 3M; Modern Infra (GKE, Cloud Run, ARM/Axion) 30% up to lesser of 35% or USD 3M. Partner Services Funds per workload: General lesser of 20% or USD 2M; VMware 45%/USD 2M; Database, Data Analytics, Oracle, Modern Infra 30%/USD 2M; SAP Partner Services Funds lesser of 100% or USD 1M | Customers and PF partners | RaMP Agreement; tag projects with workload ID in Admin Console; partner SOW pre-approved under Partner Funding Program | Terms last modified 2026-05-18; RaMP Period 3 years; unused incentives expire 12 months after issuance; first credits deposited by 2026-08-15 for agreements through 2026-06-30 | [G55] |
| MCCP | Up to 3% customer credits, max USD 250K | ISVs meeting gates | Hub form + ISV Solution Connect | Live; thresholds dated 2025-01 | [G45][G46] |
| Marketplace fee reductions | 1.5-2% for large/renewal/migration deals | Marketplace vendors | Set deal type on private offer | Since 2025-04-21 | [G18] |
| Google for Startups Cloud Program | Pre-funded USD 2K; Seed to Series A USD 200K; AI-first Seed to Series A up to USD 350K; Series B+ custom | Startups | cloud.google.com/startup | Current (page accessed 2026-09) | [G56] |
| ISV Startup Springboard | 12-week program for AI and cybersecurity startups to become co-sell ready with GTM assets | Startups | Register-interest form | Current | [G57] |
| Google for Startups AI Agents Challenge | Includes a track for agents primed for Gemini Enterprise | Startups | Launched 2026-04-23 | [G8] |
| AI Agent Ecosystem Program / AI Agents Program | Product/eng access, early tech access, GTM and co-sell for agents, marketing features; Google Cloud Ready - Gemini Enterprise path | ISVs and SIs with agents using Gemini or Model Garden models | Apply via AI Agents Program page | Current (docs updated 2026-09-25) | [G60][G8] |
| Early model access | Accenture, Bain, BCG, Deloitte, McKinsey | Select GSIs | Invitation | 2026-04 | [G6] |
| FDE partnership | Accenture, Capgemini, Cognizant, Deloitte, HCLTech, PwC, TCS | Select GSIs | Invitation | 2026-04 | [G6] |
| Google Cloud Ready validations | No-charge validation and GTM support | ISVs | Hub or forms | Current | [G58][G59] |
| MDF / co-op | Not published publicly under Partner Network; Earnings Hub lists "funds" | Unknown | Ask partner manager | Unverified | [G53] |
| Competitive displacement funds | Not published publicly; RaMP Oracle/VMware/Windows rates are the closest public equivalent | | | | [G55] |

---

## 8. What changed in 2025 to 2026 and what is announced next (newest first)

| Date | Change | Source |
|---|---|---|
| 2026-09-24 | Marketplace partner docs refreshed site-wide (no new release note since 2026-07-30) | [G26] |
| 2026-08-01 | Australia agency-model split invoicing (up to four documents; domestic sellers invoice GST) | [G25] |
| 2026-07-30 | City field added to Customer Insights and Detailed Disbursements reports | [G26] |
| 2026-07-24 | Cloud Commerce Producer API supports programmatic private offers and amendments | [G26] |
| 2026-07-22 | Q2 2026: Google Cloud revenue USD 24.8B (+82%), backlog USD 514B (INDEPENDENT) | [G65] |
| 2026-07-15 | Philip Larson (Partner Network MD) joins OpenAI | [G13] |
| ~2026-07-15 | Partner Network six-month transition window ends (Jan 15 + 6 months) | [G4] |
| 2026-07-07 | Omdia names Google Cloud a Champion in 2026 Cloud & Data Center Ecosystem Leadership Matrix | [G83] |
| 2026-06-01 | Switzerland split invoicing (three documents) | [G25] |
| 2026-05-27 | Marketplace reports move from D+2 to D+1 | [G26] |
| 2026-05-18 | RaMP terms updated (RaMP 2026 SKU group, new workload types incl. Modern Infra) | [G55] |
| 2026-05-12 | Dai Vu: USD 80B run rate, USD 462B backlog; Gemini Enterprise Agent Platform hosts 2,000+ agents | [G64] |
| 2026-05-11 | Omdia: hyperscalers shifting partners to services, taking large enterprise resell direct | [G82] |
| 2026-04-23 | Partner agents in Agent Gallery inside Gemini Enterprise app; AI Agents Program apply; Google for Startups AI Agents Challenge | [G8] |
| 2026-04-22 | Next '26: $750M fund; Gemini Enterprise Agent Platform; Agent Marketplace with 70+ agents; Partner Agent; Agentic Earnings Hub; Partner Finder; FDEs; early model access | [G6][G7] |
| 2026-03 (announced 2026-03-24) | David Smith named Head of Global Partner Program; Colleen Kapase departs (joins OpenAI, announced April) | [G11][G12][G14] |
| 2026-03 | Tackle ships Google co-sell from Salesforce (VENDOR) | [G73] |
| 2026-01-15 | Partner Network live globally; Partner Advantage terminated; 21 competencies launched; six-month transition begins | [G4][G5] |
| 2025-12-16 | Partner Network announced (Select/Premier/Diamond, competencies, automated tracking, Hub for Q1 2026) | [G1] |
| 2025-12-11 | IDC MarketScape names Google a Leader in hyperscaler marketplaces; 65 countries, 30 currencies | [G46] |
| 2025-12-04 | Terraform K8s apps with usage-based GKE pricing | [G26] |
| 2025-10-14 | Agent Card onboarding, outcome-based pricing for agents, AI agent finder | [G62] |
| 2025-10-09 | Gemini Enterprise launch; Google Cloud Ready - Gemini Enterprise designation | [G61] |
| 2025-10-06 | Procurement API returns reseller parent billing account ID | [G26] |
| 2025-09-01 | Split invoicing for BE, IT, LU, NL, PL, ES, SE | [G25] |
| 2025-07-17 | Detailed Disbursements and Customer Incremental Insights in BigQuery | [G26] |
| 2025-06-26 | SOW Analyzer and Bot-Assisted Live Chat in Hub; Earnings Hub AI features | [G52] |
| 2025-06-25 | Canalys PEM study published (USD 7.05 per USD 1) | [G51] |
| 2025-06-09 | Reseller (MCPO) purchases count 100% toward commit (policy text: after 2025-06-08) | [G21][G22] |
| 2025-05-27 | Commit drawdown policy updated (25% cap) | [G22] |
| 2025-05-15 | Variable revenue share, MCCP GA, MCPO expansion announced | [G21] |
| 2025-04-21 | Vendor Net Revenue Schedule and deal types live | [G18][G26] |

**Announced, not yet dated or not yet live:**
- Partner Agent maturing toward "partner agents talking to our agents" (agent-to-agent partner operations) [G92].
- Improved deal telemetry to predict MCPO opportunities [G46].
- Next '27: 2027-04-13 to 04-15 [G89].

---

## 9. Diagnostics: why partners get zero pipeline, and the fix

| # | Failure mode | How to detect (what to check) | Fix |
|---|---|---|---|
| 1 | Product can't list (not GCP-hosted) | Onboarding validation stalled; no approved hosting pattern | Decide: re-architect data/compute plane to GCP (Pattern 2) or deprioritize Google [G17] |
| 2 | Still operating as a Partner Advantage partner | Team uses partneradvantage links, old tier names; no Hub program-progress data | Re-onboard users to Hub; brief sales on Partner Network; re-map goals to tiers/competencies [G1] |
| 3 | Deals not registered, so tier and competencies stall | Hub program dashboard shows little co-sell ACV vs CRM partner pipeline | Register every qualified deal at discovery; automate via Integrator-role tool [G1][G72] |
| 4 | Listing live but nobody in the field knows you | No ISV Solution Connect invite; no Google-sourced opps | Ask PDM for ISV Solution Connect; get Google Cloud Ready badge; JBP with ISV specialist [G45][G58][G77] |
| 5 | Only a PDM relationship, no FSR/CE relationships | PDM "doesn't bring deals" | Build named FSR/CE/specialist counterparts per target account; split alliance roles [G81] |
| 6 | Closing off-marketplace | Deals won with Google help but paper is direct | Route through private offer; explain commit drawdown and MCCP [G22][G68] |
| 7 | Paying 3% when you could pay 1.5% | Customer Insights marketplace_fee_percent at 3 on renewals/migrations | Set deal type (Native renewal, Migration, Channel shift); use CUDs not usage-only [G20][G26] |
| 8 | Customer's 25% marketplace headroom already used | Customer says commit "won't count" | Check with Google rep; position for next commit or renewal; still sell on procurement speed [G22] |
| 9 | Weak better-together story | FSRs don't respond | Quantify GCP consumption your product drives; name services [G70] |
| 10 | Resellers can't sell you | Resellers report product not eligible | Turn on reselling; amend MVA; create private offer plans [G33] |
| 11 | Services partner unfunded | Earnings Hub shows missed incentives | Submit SOWs through SOW Analyzer; claim via Agentic Earnings Hub [G52][G6] |
| 12 | Selling agents without Gemini Enterprise validation | Not in Agent Gallery | Apply to AI Agents Program; build A2A Agent Card; pass four-step evaluation [G8][G39] |
| 13 | Wrong internal contacts after 2026 exec turnover | Emails to former leaders bounce, escalations stall | Re-map to David Smith's org under Ichhpurani; confirm PDM [G11][G14] |
| 14 | Sales comp not neutral | AEs avoid marketplace | Make marketplace comp-neutral or add a kicker [G49] |
| 15 | Treating Google as the third cloud with no owner | No Google quota owner | Named owner with Google quota; review ROI at 12 and 24 months [G81] |

---

## 10. KPIs and operating cadence

### 10.1 KPIs

| KPI | Definition | Benchmark (label) | Source |
|---|---|---|---|
| Partner co-sell ACV (Google's measure) | ACV of registered co-sell deals recognized in Hub | Tier gates USD 250K / 2M / 20M (INDEPENDENT) | [G5] |
| Registration rate | Qualified opps registered / total qualified | Target near 100% | [G70] |
| Google-sourced opportunities | Opps sourced by Google sellers | Tracked by Google ISV sales | [G77] |
| Pipeline coverage | Joint pipeline vs target | 3x minimum for ISVs (Google ISV sales) | [G77] |
| Marketplace GTV and marketplace % of ARR | Revenue through marketplace | VENDOR: mature programs 20-30%+ of revenue | [G70] |
| Effective fee rate | Weighted fee across deals | 1.5-3% | [G18] |
| Private offer cycle time | Create to accept | Futurum: 2-4 weeks faster than direct | [G49] |
| Deal size uplift | Marketplace vs direct | Futurum: +112% | [G49] |
| Commit-eligible pipeline | Opps where customer has commit headroom | Internal | [G22] |
| Certifications (for services) | Certified individuals | Diamond gate: 200 (INDEPENDENT) | [G5] |
| Partner-implemented workloads / influenced opps | Services and co-sell counts | Diamond gates: 20 / 30 | [G5] |
| Incentive capture | Earned vs eligible in Earnings Hub | Earnings Hub shows missed incentives | [G54] |
| Services multiplier | Partner services revenue per USD 1 of GCP | Up to USD 7.05 (Canalys, Jan 2025): Y1 2.05, Y2 3.64, Y3 1.36; Advise 0.75, Design 1.75, Procure 0.39, Build 1.72, Adopt 1.20, Manage 1.24 | [G50][G51] |

Canalys note: Google's blog calls Build "the single biggest segment" but the factsheet shows Design (USD 1.75) slightly above Build (USD 1.72) [G50]. No 2026 update to the PEM study found as of 2026-09-26 (Canalys is now Omdia).

### 10.2 Cadence

| Cadence | Activity |
|---|---|
| Weekly | Register new qualified opps; update Google seller on active deals; check Producer Portal offer statuses and pending approvals |
| Monthly | Reconcile disbursement (21st) and Customer Insights; review Hub program progress (tier/competency gaps via Partner Agent); Earnings Hub claims; check marketplace release notes feed |
| Quarterly | Account mapping with territory teams; JBP review with PDM and ISV specialist; pipeline 3x check; validate commit anniversaries of top accounts |
| Annually (Nov-Jan) | Get into Google account plans; renew JBP; plan Next (April) presence; re-verify thresholds in new program-year guide |

---

## 11. By partner type

| Type | Path | First moves | Watch-outs |
|---|---|---|---|
| ISV SaaS, GCP-hosted | Technology + co-selling | Enroll; list SaaS with CUD-capable private offers; register all deals; seek ISV Solution Connect; Google Cloud Ready badge for your integration; MCCP | Deal type labeling; comp neutrality; name FSR counterparts |
| ISV SaaS, AWS/Azure-hosted | Technology (limited) | Assess hosting patterns (2, 3, 5, 9); if none fit, run co-sell-only or deprioritize | Cannot list, so no commit drawdown, weak field pull |
| ISV with agents | Technology + AI Agents Program | Build A2A Agent Card; list as AI agent as a service; pursue Google Cloud Ready - Gemini Enterprise; Agent Gallery | Pricing rules (no POC free plans, no $0 private plans) |
| Data/analytics ISV | Technology + co-selling | Google Cloud Ready - BigQuery (5 prod customers + 1 case study); work with ISV Sales, Data Analytics | Category test prep |
| Services / SI / consultancy | Services | Certifications; register services opps; SOW funding via Hub; RaMP PSF; competencies (industry + solution); Delivery Navigator | 200-cert Diamond gate; audit-free but data-driven |
| Reseller / MSP | Services and/or co-selling + Resale Subprogram | Resale authorization; Partner Sales Console; request private offer plans and reseller discounts from ISVs; associate purchases for commit | Enterprise resale being taken direct; margin compression | <!-- VALIDATE-OK[economics]: public hyperscaler or vendor reseller economics, not Forecastable's -->
| Startup | Google for Startups Cloud Program; ISV Startup Springboard | Credits up to USD 350K (AI); co-sell readiness | Marketplace listing still requires production-ready product |
| Agency (marketing/creative) | Services | Gemini Enterprise and Workspace competencies; partner-built agents | Limited marketplace angle unless productized |

---

## 12. Strategic decision points (for Alex)

### 12.1 Invest in Google Cloud at all?
- **Yes if:** product runs on GCP (or can move a data/compute plane), target buyers have Google commits, product drives BigQuery/Vertex/Gemini/GKE consumption, or you sell agents that fit Gemini Enterprise [G17][G8].
- **No (or co-sell only) if:** hosted elsewhere with no viable pattern; ICP overlap with Google customers is thin.
- **Flip condition:** a top-10 target account has a large Google commit and wants to buy through it; or Google offers FDE/fund support for your agent.
- Practitioner view: Google gets less partner competition and a more accessible field, often better ROI per alliance headcount than AWS/Microsoft (CREATOR) [G81].

### 12.2 Which tier to chase this program year?
- ISVs: tier matters less than listing, registration and ISV Solution Connect. Aim for Select via USD 250K registered co-sell ACV (reported) [G5]; competencies and Google Cloud Ready carry more field signal for ISVs (partner quote: "competencies will hopefully be more important than tiers") [G5].
- Services firms: Premier (USD 2M) is the realistic target; Diamond requires 200 certified people and USD 20M [G5].
- **Flip:** if the program guide shows tier-linked incentive multipliers you can capture, move tier up the list.

### 12.3 Marketplace-first or not?
- Marketplace-first when buyers have commits and procurement friction is the bottleneck; fee is 1.5-3% [G18]; deals 112% larger and 2-4 weeks faster per Google-commissioned study [G49].
- Keep direct paper when the customer's 25% marketplace headroom is used, for professional-services-heavy deals (excluded from drawdown and VNRS), or non-US pro services (pro services listings are US-only) [G22][G23][G42].

### 12.4 When private offers beat direct
- Any deal where the customer has uncommitted Google spend; any renewal or migration (1.5%); any deal over USD 1M (2% or 1.5%); first-time buyers eligible for MCCP [G18][G45].
- Direct can win when the deal is mostly services, when the buyer is not on Google billing, or when your fee math on usage-only PAYG is poor [G20].

### 12.5 How to fund the motion
- Services partners: SOW funding, DAF, RaMP PSF (up to USD 2M per workload), $750M fund [G55][G6].
- ISVs: MCCP (buyer side), Google Cloud Ready GTM support, AI Agents Program, $750M fund agent-building support, startup credits [G45][G58][G60][G6].
- Marketplace fee savings (vs 3%) on large and renewal deals can fund a deal desk.

### 12.6 Business-case inputs
- Google commit overlap in your pipeline (count and USD); average deal size and renewal mix (fee blend); share of revenue hosted on GCP; expected uplift (Futurum: +112% deal size, 2-4 weeks faster); alliance headcount (1 owner minimum); tool cost (Tackle/Clazar/Suger); incentive capture (MCCP up to USD 250K per new logo credit to customer).
- For services firms: Canalys PEM up to USD 7.05 services revenue per USD 1 of Google Cloud over three years, 51.6% in year one [G50].

### 12.7 Read the current Google priorities
Google is rewarding: agents on Gemini Enterprise, co-sell and services outcomes (not paperwork), consumption growth, net-new logos, AI revenue [G1][G6][G78]. Leadership turnover (Kapase, Larson out; Smith in) means program details may shift in 2027; re-verify at Kickstart 2027 [G11][G13].

---

## 13. Tactical runbooks (for Eva)

### R1. Enroll in Google Cloud Partner Network
1. Confirm corporate Google accounts exist for all users. Done when: each user can sign into Google with a company email.
2. Go to partners.cloud.google.com > Become a partner; complete enrollment. Done when: Partner Network Hub loads with your company.
3. Invite users (Register as a user) and assign at least two Partner Admins. Done when: two admins listed in Hub user management.
4. Select paths (technology for marketplace ISVs; services for SIs; co-selling). Done when: profile shows paths.
5. Connect certifications and delivery data (automatic ingest). Done when: program progress dashboard shows data.
6. Log the Partner ID and company name from the Hub Account page for integrations. Done when: stored in CRM admin notes.

### R2. Get co-sell ready
1. Confirm marketplace listing is transactable (see R3). Done when: public or private-offer-ready product exists.
2. Write the better-together one-pager (GCP services used, consumption impact, 3 customer stories). Done when: approved by PDM.
3. Ask PDM for ISV Solution Connect invitation. Done when: enrolled.
4. Apply for the relevant Google Cloud Ready designation (BigQuery: 5 prod customers + 1 public case study). Done when: validation scheduled.
5. Connect CRM co-sell sync (Integrator role in Hub). Done when: test registration syncs.
6. Build target-account list with commit anniversaries; request mapping session with territory team. Done when: session on calendar.

### R3. Publish a listing
1. Hub > View tasks > Partner tasks > Initiate onboarding your product to Marketplace; submit architecture and business inputs. Done when: validation approved.
2. Partner Admin accepts Marketplace Vendor Agreement in Hub. Done when: accepted version visible.
3. Create project `COMPANY-public`; complete Project Info Form. Done when: Producer Portal accessible.
4. Payments page: region/currency, profile, second admin, bank (verify test deposits), W-9/W-8BEN-E. Done when: primary bank verified.
5. Producer Portal: add product; submit pricing (up to 4 business days). Done when: pricing approved.
6. Integrate (SaaS Procurement API + Pub/Sub + SSO; agents: Agent Card). Done when: technical review approved.
7. Create Test Billing Account; run purchase end to end. Done when: entitlement created and approved; invoice shows 100% "Marketplace Partner Testing" discount.
8. Submit remaining reviews; publish. Done when: listing public (agents: run the gcloud command Google provides).

### R4. Create a private offer
1. Get customer's Cloud Billing account ID and confirm who on their side has Billing Admin (or Billing User + Consumer Procurement Order Administrator). Done when: ID and approver named.
2. Check deal type: New / Migration / Native renewal / Channel shift, and TCV band. Done when: expected fee rate recorded in CRM.
3. Producer Portal > Private Offers > Create offer; enter customer, billing account, offer name, sales contact. Done when: saved draft.
4. Pricing: choose CUD or flat fee (avoid usage-only if you want TCV credit); billing frequency (monthly for Brazil); installments each >= 50% of prior per-day value; auto-renew if desired (not with custom frequency). Done when: pricing section complete.
5. EULA: Google standard or custom (needs Private Offers Admin role). Done when: EULA attached.
6. Review and publish; send URL with Google's "accept a private offer" doc and a note that it can be purchased once. Done when: customer confirms receipt.
7. After acceptance (SaaS): approve account/entitlement. Done when: entitlement active.
8. If Pending Google Approval (e.g. native renewal over USD 10M), wait; Google sends it automatically. Done when: status Published.

### R5. Create a channel (reseller) offer
1. Confirm MVA includes resale terms; turn on reselling for products. Done when: reselling on.
2. Producer Portal > Account management > Settings > Reseller management > Manage reseller network; allow the reseller's billing account. Done when: reseller shows as allowed.
3. Create a private offer plan (single-use to set deal type other than New). Done when: plan created.
4. Reseller accepts in Partner Sales Console > Private offer plans. Done when: plan status accepted.
5. Reseller creates the offer: Partner Sales Console > Customers > [customer] > Private offers > Create private offer > Use this plan. Done when: offer Published.
6. Reseller and Google rep associate purchase to the end customer for commit drawdown. Done when: Google rep confirms association.

### R6. Register or share an opportunity
1. Qualify: named customer, GCP footprint or commit, product-GCP link, stage at discovery or later. Done when: meets criteria.
2. Register in Partner Network Hub (co-sell registration; services registration for services partners) with customer, deal size, close date, GCP services, marketplace plan, specific ask of Google. Done when: registration ID in CRM.
3. Use Partner Agent for registration coaching if fields are unclear. Done when: no validation errors.
4. Email the ISV specialist/PDM with the registration ID and the ask; request the FSR name. Done when: FSR identified.
5. Update Google monthly until close; close via marketplace. Done when: won in Hub and private offer accepted.

### R7. Request or claim funding
1. Services SOW funding: draft SOW; run it through SOW Analyzer (Hub > Earnings > Funds Details > SOW Documents); fix flagged gaps. Done when: submitted for human approval.
2. RaMP: confirm customer RaMP Agreement; ensure workload ID tagging in Admin Console; submit partner SOW for PSF pre-approval. Done when: funds approved.
3. MCCP: confirm partner gates; submit MCCP Credits Request Form in Hub and register in ISV Solution Connect; after close, enter private offer ID and end customer ID. Done when: MCCP team confirms disbursement to customer billing ID.
4. $750M fund / AI Agents Program: ask PDM which component applies; apply via AI Agents Program page. Done when: written confirmation.
5. Track everything in (Agentic) Earnings Hub; download CSV monthly. Done when: reconciled.

### R8. Audit current status
1. Hub: tier, paths, competencies and gaps (ask Partner Agent "what do I need for X competency"). 
2. Hub: users, admins (>=2), Integrator connections.
3. Producer Portal: products, pricing status, open offers and expirations, reseller settings.
4. Payments: profile admins (>=2), bank verified, tax form current.
5. Reports: last 3 months fee percent by deal (Customer Insights marketplace_fee_percent).
6. Earnings Hub: earned vs missed incentives.
7. CRM: registration rate, Google-sourced opps, co-sell win rate.
Done when: a one-page status with red/amber/green per line exists.

### R9. Prep for a Google field seller meeting
1. Identify seller role (FSR, CE, specialist, ISV specialist) and their quota lens. 
2. Bring: 3 named overlapping accounts with commit info, the GCP services you drive, one customer story, the marketplace path (private offer, MCCP eligibility), and a specific ask.
3. Keep materials under 5 minutes to consume.
4. After: register opportunities discussed within 24 hours; send recap.
Done when: at least one registered opp with a named Google owner.

### R10. Monthly program health check
1. Registrations this month vs qualified opps (target near 100%).
2. Marketplace GTV, effective fee rate, offers expiring in 30 days.
3. Disbursement reconciled (21st).
4. Tier/competency progress delta.
5. Incentives claimed vs available.
6. Check Tier 0 feeds (marketplace release notes RSS, partner blog) for changes.
7. Leadership/contact changes at Google.
Done when: health report filed and actions assigned.

---

## 14. Unverified, conflicting or login-gated

| Item | Status | Detail |
|---|---|---|
| Tier dollar thresholds (USD 250K / 2M / 20M ACV) and Diamond gates (20 workloads, 30 influenced opps, 200 certs) | INDEPENDENT only | CRN Australia "understands" [G5]; Suger says Google publishes none [G66]; flashdba gives different, non-dollar criteria [G81] |
| Competency-level requirements (counts of certs and opps) | Login-gated | Program guide "Y26" in Hub; a copy exists on Scribd but could not be read |
| Number of product competencies | Conflict | CRN: 5 incl. Apigee [G4]; Google page: 4, no Apigee [G2] |
| Tier benefits by tier (discounts, rebates, MDF) | Login-gated | Not public |
| Co-sell registration menu path, fields, SLAs | Login-gated | Only vendor descriptions [G70][G72][G74] |
| ISV Solution Connect criteria | `[UNVERIFIED, source dated 2025-02]` | Invisory [G75] |
| MCCP thresholds | `[UNVERIFIED, source dated 2025-01]` | Program brief [G45]; program still promoted 2025-12 and 2026-09 [G46][G48] |
| Seller quota eligibility and SPIFFs on marketplace | `[UNVERIFIED, source dated 2024-04]` for detail | Dai Vu via Clazar podcast [G71]; Google 2026 copy confirms reps are "incentivized" without specifics [G8] |
| $750M fund per-partner amounts and application | Not published | [G6] |
| DAF, MDF, POC credit amounts | Not published | Mentioned by Samrah Khan and Techaisle [G54][G78] |
| "Marketplace Consumption Partner Offer" program | Unverified | Only in Suger guide [G67]; no Google source found |
| MCPO "no incremental ISV fee" | VENDOR claim, consistent with Google docs | [G67][G34] |
| Canalys PEM 2026 refresh | None found | Latest is January 2025 study [G50] |
| Google Cloud Ready - AlloyDB prerequisite "Partner Tier" | Stale wording on official page | [G59] |
| Clazar and Tackle 2026 guides reference Partner Advantage | Stale | [G70][G74] |
| Suger claim "All renewals 1.5%" | Imprecise | Official: native renewals only, meeting criteria [G18] |
| Kickstart 2026 event details | Pages removed (404) | |
| Q2 2026 Google Cloud figures | INDEPENDENT recap | Verify against Alphabet release at abc.xyz [G65] |
| Colleen Kapase OpenAI move date | INDEPENDENT | Left March 2026; OpenAI role announced April 2026 [G11][G12] |

---


### 14.V Vendor-sourced items to verify (Tackle, Clazar, Suger, WorkSpan; added 2026-09-26)

All VENDOR. Detail and sources in `vendors/{vendor}-intelligence.md`. Official pages win on conflict.

| Item | Vendor claim | Official status | Action |
|---|---|---|---|
| Commit cap | 50% (Tackle page) | 25% per commit policy | Official wins |
| Payment schedule step-down | Each payment can drop to 70% of prior (Tackle) | Google doc says 50% | Official wins |
| Deal registration API access | Needs a support case to switch on (Clazar); Tackle's May 2026 guide does not mention it | Not documented publicly | Ask the Google partner team |
| Upcoming changes previewed on stage | Deal registration redesign, MCCP variable credits, distributor private offer pilot (Google speakers at Tackle Cloud GTM XP 2026) | Not on official pages yet | Watch release notes; do not promise |
| MCCP $8.3M | Suger calls it a per-ISV cap | Official brief: annualized deal value at which the $250K per-transaction maximum is reached | Official wins |
| Private offer failures | Free-trial billing accounts and self-serve account limits block acceptance (Suger) | Consistent with docs | Add to M4 pre-flight |
| Hosting patterns | "Six" (Suger), "Partner Advantage" naming (WorkSpan, Clazar, Tackle pages in 2026) | Nine patterns; Partner Network | Treat vendor pages as stale on names |

## Sources

| Tag | Title | Publisher | Date | Label | URL |
|---|---|---|---|---|---|
| G1 | Introducing Google Cloud Partner Network and three pillars for meaningful business (Colleen Kapase) | Google Cloud Blog | 2025-12-16 | OFFICIAL | https://cloud.google.com/blog/topics/partners/introducing-google-cloud-partner-network |
| G2 | Google Cloud Partner Network (program page) | Google Cloud | accessed 2026-09-26 | OFFICIAL | https://cloud.google.com/partners |
| G3 | Unlock your growth: Join the Google Cloud Partner Network (Hub landing) | Google Cloud | accessed 2026-09-26 | OFFICIAL | https://partners.cloud.google.com/?hl=en |
| G4 | Google Cloud's New Partner Network Is Here: 12 Huge AI, Features And Changes To Know (Mark Haranas) | CRN | 2026-01-13 | INDEPENDENT | https://www.crn.com/news/cloud/2026/google-cloud-s-new-partner-network-is-here-12-huge-ai-features-and-changes-to-know |
| G5 | Google Cloud's new three-tiering system brings mixed reviews from partners (Athina Mallis) | CRN Australia | 2026-01-22 | INDEPENDENT | https://www.crn.com.au/news/2026/cloud/google-partner-program-tiering-system-changes |
| G6 | Building the Agentic Enterprise with Google Cloud partners and a $750M innovation fund (Kevin Ichhpurani) | Google Cloud Blog | 2026-04-22 | OFFICIAL | https://cloud.google.com/blog/topics/partners/how-google-cloud-partner-ecosystem-is-building-the-agentic-enterprise |
| G7 | 260 things we announced at Google Cloud Next '26 | Google Cloud Blog | 2026-04-25 | OFFICIAL | https://cloud.google.com/blog/topics/google-cloud-next/google-cloud-next-2026-wrap-up |
| G8 | Enabling the agentic enterprise: business and industry agents arrive in Gemini Enterprise (Satish Thomas) | Google Cloud Blog | 2026-04-23 | OFFICIAL | https://cloud.google.com/blog/products/ai-machine-learning/partner-built-agents-available-in-gemini-enterprise |
| G9 | Google Cloud puts $750M behind partner ecosystem (Larson on theCUBE) | SiliconANGLE | 2026-04-22 | INDEPENDENT | https://siliconangle.com/2026/04/22/google-cloud-invests-750m-fuel-agentic-enterprise-googlecloudnext/ |
| G10 | Google Cloud carves out $750M AI fund for partners (Matt Ashare) | Channel Dive | 2026-04-22 | INDEPENDENT | https://www.channeldive.com/news/google-cloud-750-million-partner-fund-agentic-ai/818125/ |
| G11 | March 2026 Leadership Moves: Google Cloud Partner Chief Departs (Jordan Smith) | Channel Insider | 2026-04-03 | INDEPENDENT | https://www.channelinsider.com/channel-business/vendor-leadership-and-partner-programs/march-2026-leadership-recap/ |
| G12 | OpenAI Taps Former Google Cloud Lead for Partnerships Role | Channel Insider | 2026-04 | INDEPENDENT | https://www.channelinsider.com/ai/openai-colleen-kapase-global-partnerships/ |
| G13 | OpenAI hires Google Cloud's Larson to lead partner network | ScanX News | 2026-07-15 | INDEPENDENT | https://scanx.trade/stock-market-news/startups/openai-hires-google-cloud-s-philip-larson-to-lead-partner-network/45607388 |
| G14 | David Smith leidt AI-transformatie partnerkanaal Google Cloud | Dutch IT Channel | 2026-03-24 | INDEPENDENT | https://www.dutchitchannel.nl/people/727885/david-smith-leidt-ai-transformatie-partnerkanaal-google-cloud |
| G15 | Google Cloud Marketplace partners documentation (overview) | Google Cloud Docs | updated 2026-09-24 | OFFICIAL | https://docs.cloud.google.com/marketplace/docs/partners |
| G16 | Offer software on Google Cloud Marketplace | Google Cloud Docs | updated 2026-09-24 | OFFICIAL | https://docs.cloud.google.com/marketplace/docs/partners/offer-products |
| G17 | Requirements for Google Cloud Marketplace | Google Cloud Docs | updated 2026-09-24 | OFFICIAL | https://docs.cloud.google.com/marketplace/docs/partners/get-started |
| G18 | Vendor Net Revenue Schedule | Google Cloud Terms | effective 2025-04-21 (modified 2025-03-10) | OFFICIAL | https://cloud.google.com/terms/marketplace-revenue-share-schedule |
| G19 | Overview of the Vendor Net Revenue Schedule | Google Cloud Docs | updated 2026-09-24 | OFFICIAL | https://docs.cloud.google.com/marketplace/docs/partners/migrations/variable-revenue-share |
| G20 | Sample revenue share calculations for Google Cloud Marketplace | Google Cloud Docs | updated 2026-09-24 | OFFICIAL | https://docs.cloud.google.com/marketplace/docs/partners/revenue-share-scenarios |
| G21 | Upgrades to Google Cloud Marketplace for partners (Dai Vu) | Google Cloud Blog | 2025-05-15 | OFFICIAL | https://cloud.google.com/blog/topics/partners/upgrades-to-google-cloud-marketplace-for-partners |
| G22 | Google Cloud Marketplace Commitment Drawdown Policy | Google Cloud Terms | modified 2025-05-27 | OFFICIAL | https://cloud.google.com/terms/marketplace/commit-policy |
| G23 | Google Cloud Marketplace commitment drawdown rates | Google Cloud Docs | updated 2026-09-24 | OFFICIAL | https://docs.cloud.google.com/marketplace/docs/commit-drawdown |
| G24 | Receiving payments from Google | Google Cloud Docs | updated 2026-09-24 | OFFICIAL | https://docs.cloud.google.com/marketplace/docs/partners/receive-payments |
| G25 | Transaction models | Google Cloud Docs | updated 2026-09-24 | OFFICIAL | https://docs.cloud.google.com/marketplace/docs/partners/transaction-models |
| G26 | Cloud Marketplace Partners release notes (feed: https://docs.cloud.google.com/feeds/gcpmarketplacepartners-release-notes.xml) | Google Cloud Docs | latest entry 2026-07-30 | OFFICIAL | https://docs.cloud.google.com/marketplace/docs/partners/release-notes |
| G27 | Create a private offer for a customer | Google Cloud Docs | updated 2026-09-24 | OFFICIAL | https://docs.cloud.google.com/marketplace/docs/partners/create-offers |
| G28 | Billing frequency for private offers | Google Cloud Docs | updated 2026-09-24 | OFFICIAL | https://docs.cloud.google.com/marketplace/docs/partners/offers/select-payment-schedule |
| G29 | Modify a published offer | Google Cloud Docs | updated 2026-09-24 | OFFICIAL | https://docs.cloud.google.com/marketplace/docs/partners/offers/modify-offer |
| G30 | Send a private offer to a customer | Google Cloud Docs | updated 2026-09-24 | OFFICIAL | https://docs.cloud.google.com/marketplace/docs/partners/offers/send-offer |
| G31 | Automatic renewal for private offers | Google Cloud Docs | updated 2026-09-24 | OFFICIAL | https://docs.cloud.google.com/marketplace/docs/partners/offers/auto-renew |
| G32 | Turn on account approval / multiple orders for SaaS products | Google Cloud Docs | updated 2026-09-24 | OFFICIAL | https://docs.cloud.google.com/marketplace/docs/partners/offers/account-approval ; https://docs.cloud.google.com/marketplace/docs/partners/offers/multiple-offers |
| G33 | Set up your Cloud Marketplace products for resale | Google Cloud Docs | updated 2026-09-24 | OFFICIAL | https://docs.cloud.google.com/marketplace/docs/partners/resell/set-up-reselling |
| G34 | Configure discounts for resellers | Google Cloud Docs | updated 2026-09-24 | OFFICIAL | https://docs.cloud.google.com/marketplace/docs/partners/resell/reseller-incentives |
| G35 | Manage allowed resellers for your products | Google Cloud Docs | updated 2026-09-24 | OFFICIAL | https://docs.cloud.google.com/marketplace/docs/partners/resell/manage-allowed-resellers |
| G36 | Resell Cloud Marketplace products from ISVs / Private offer plans for resellers | Google Cloud Docs | updated 2026-09-24 | OFFICIAL | https://docs.cloud.google.com/marketplace/docs/partners/resellers/resell |
| G37 | Create private offers as a Cloud Marketplace reseller | Google Cloud Docs | updated 2026-09-24 | OFFICIAL | https://docs.cloud.google.com/marketplace/docs/partners/resellers/create-private-offers |
| G38 | Changes to reseller discounts (2024-05-20) | Google Cloud Docs | updated 2026-09-24 | OFFICIAL | https://docs.cloud.google.com/marketplace/docs/partners/migrations/reseller-discount-changes |
| G39 | Offer AI agents through Google Cloud Marketplace | Google Cloud Docs | updated 2026-09-24 | OFFICIAL | https://docs.cloud.google.com/marketplace/docs/partners/ai-agents |
| G40 | Add your AI agent's pricing information | Google Cloud Docs | updated 2026-09-24 | OFFICIAL | https://docs.cloud.google.com/marketplace/docs/partners/ai-agents/choose-pricing |
| G41 | Add your AI agent in Producer Portal | Google Cloud Docs | updated 2026-09-24 | OFFICIAL | https://docs.cloud.google.com/marketplace/docs/partners/ai-agents/add-product |
| G42 | Offer professional services | Google Cloud Docs | updated 2026-09-24 | OFFICIAL | https://docs.cloud.google.com/marketplace/docs/partners/professional-services |
| G43 | Testing your published Google Cloud Marketplace products | Google Cloud Docs | updated 2026-09-24 | OFFICIAL | https://docs.cloud.google.com/marketplace/docs/partners/testing-products |
| G44 | Request assistance with Google Cloud Marketplace | Google Cloud Docs | updated 2026-09-24 | OFFICIAL | https://docs.cloud.google.com/marketplace/docs/partners/get-support |
| G45 | Marketplace Customer Credit Program: Program Brief | Google (services.google.com PDF) | created 2025-01-08 | OFFICIAL | https://services.google.com/fh/files/misc/google_cloud_marketplace_customer_credit_program_brief.pdf |
| G46 | Google named a Leader in the 2025 IDC MarketScape for Worldwide Hyperscaler Marketplaces (Dai Vu, Denis Morentsov) | Google Cloud Blog | 2025-12-11 | OFFICIAL | https://cloud.google.com/blog/topics/partners/google-leader-idc-marketscape-hyperscaler-marketplaces |
| G47 | Google Cloud Marketplace private offer enhancements unlock enterprise and AI use cases | Google Cloud Blog | 2024-10-16 | OFFICIAL | https://cloud.google.com/blog/topics/partners/enhancing-google-cloud-marketplace-private-offers |
| G48 | Why sell on Google Cloud Marketplace | Google Cloud | accessed 2026-09-26 | OFFICIAL | https://cloud.google.com/marketplace/sell |
| G49 | Scaling Smarter: How Google Cloud Marketplace Is Reshaping Partner Sales (Futurum, Google-commissioned) | Futurum / Google | 2025-06 | INDEPENDENT | https://services.google.com/fh/files/misc/futurum_whitepaper_partners_scaling_smarter_google_cloud_marketplace_june_2025.pdf |
| G50 | Google Cloud Partner Ecosystem Multiplier Factsheet (Canalys study, January 2025) | Google / Canalys | 2025-01 | OFFICIAL | https://services.google.com/fh/files/misc/gcp_partner_ecosystem_multiplier_factsheet.pdf |
| G51 | Partner growth with Google Cloud: A strategy for maximized and sustained earnings (Sandy Janes) | Google Cloud Blog | 2025-06-25 | OFFICIAL | https://cloud.google.com/blog/topics/partners/new-study-on-maximizing-partner-growth-with-google-cloud |
| G52 | New AI tools help partners increase efficiency and growth (SOW Analyzer) | Google Cloud Blog | 2025-06-26 | OFFICIAL | https://cloud.google.com/blog/topics/partners/new-ai-tools-for-google-cloud-partners |
| G53 | Accelerating partner growth with Earnings Hub and new AI resources | Google Cloud Blog | 2024-10-17 | OFFICIAL | https://cloud.google.com/blog/topics/partners/track-and-optimize-incentives-with-earnings-hub/ |
| G54 | Google Cloud's Earnings Hub: A New Benchmark (Anurag Agrawal) | Techaisle | 2025-05-27 | INDEPENDENT | https://www.techaisle.com/blog/617-google-cloud-earnings-hub-a-new-benchmark-for-partner-enablement-and-profitability |
| G55 | Rapid Migration and Modernization Program Terms | Google Cloud Terms | modified 2026-05-18 | OFFICIAL | https://cloud.google.com/terms/ramp |
| G56 | Google for Startups Cloud Program | Google Cloud | accessed 2026-09-26 | OFFICIAL | https://cloud.google.com/startup |
| G57 | ISV Startup Springboard | Google Cloud | accessed 2026-09-26 | OFFICIAL | https://cloud.google.com/resources/isv-startup-springboard-register-interest-form-page |
| G58 | Google Cloud Ready - BigQuery | Google Cloud Docs | updated 2026-09-24 | OFFICIAL | https://docs.cloud.google.com/bigquery/docs/bigquery-ready-overview |
| G59 | Google Cloud Ready - AlloyDB | Google Cloud Docs | updated 2026-09-24 | OFFICIAL | https://docs.cloud.google.com/alloydb/docs/cloud-ready/overview |
| G60 | Overview of the Google Cloud AI Agent Ecosystem Program | Google Cloud Docs | updated 2026-09-25 | OFFICIAL | https://docs.cloud.google.com/vertex-ai/docs/ai-agent-ecosystem-overview |
| G61 | Partners powering the Gemini Enterprise agent ecosystem (Kevin Ichhpurani) | Google Cloud Blog | 2025-10-09 | OFFICIAL | https://cloud.google.com/blog/topics/partners/partners-powering-the-gemini-enterprise-agent-ecosystem/ |
| G62 | Scaling AI agents with Google Cloud Marketplace and Gemini Enterprise (Pritish Sinha, Oliver Schulz) | Google Cloud Blog | 2025-10-14 | OFFICIAL | https://cloud.google.com/blog/topics/partners/google-cloud-ai-agent-marketplace |
| G63 | Onboarding your organization (Delivery Navigator Help) | Google Support | accessed 2026-09-26 | OFFICIAL | https://support.google.com/delivery-navigator/answer/14728909?hl=en |
| G64 | Google Cloud sees its marketplace as the launchpad for the agentic enterprise (Dai Vu on theCUBE) | SiliconANGLE | 2026-05-12 | INDEPENDENT | https://siliconangle.com/2026/05/12/embracing-agentic-reality-cloud-marketplaces-rhsummit/ |
| G65 | Alphabet Q2 2026 Earnings Show Cloud Surge | InsiderFinance | 2026-07-22 | INDEPENDENT | https://www.insiderfinance.io/news/alphabet-q2-2026-earnings-show-cloud-surge |
| G66 | Google Cloud Partner Network Tiers Explained (Samantha Ho) | Suger | 2026-08-20 | VENDOR | https://www.suger.io/resources/blog/google-cloud-partner-network-tiers/ |
| G67 | Selling on Google Cloud Marketplace: 2026 Guide | Suger | 2026-08 | VENDOR | https://www.suger.io/resources/guides/google-cloud-marketplace/ |
| G68 | Co-selling with Google Cloud (Sabrina Xie) | Suger | verified 2026-08-20 | VENDOR | https://www.suger.io/resources/blog/co-selling-with-google-cloud/ |
| G69 | Google Cloud Commitments and Marketplace Drawdown | Suger | 2026 | VENDOR | https://www.suger.io/resources/blog/gcp-commitments-and-marketplace-drawdown/ |
| G70 | A Complete Guide to Co-Selling with Google (2026) | Clazar | 2026 | VENDOR | https://clazar.io/guides/co-selling-with-google |
| G71 | The opportunity and economics of Google Cloud Marketplace with Dai Vu (podcast) | Clazar | 2024-04-03 | VENDOR | https://clazar.io/podcasts/the-opportunity-and-economics-of-google-cloud-marketplace-with-dai-vu |
| G72 | Connect to Google Cloud for co-sell registration | Tackle Help | 2026-05-22 | VENDOR | https://help.tackle.io/en/articles/15217465-connect-to-google-cloud-for-co-sell-registration |
| G73 | March 2026 Product Updates (Ashley Stachura) | Tackle | 2026-03 | VENDOR | https://tackle.io/blog/cloud-gtm-product-updates-march-2026-tackle/ |
| G74 | Co-sell in the Google Cloud Partner Program (Jason Matthew Smith) | Tackle | 2026-05-01 | VENDOR | https://tackle.io/blog/co-sell-in-google-cloud-partner-program/ |
| G75 | Google Cloud Marketplace's ISV Solution Connect: The Ultimate Guide (Alex Torres) | Invisory | 2025-02-25 | VENDOR | https://invisory.co/resources/blog/google-cloud-marketplaces-isv-solution-connect-the-ultimate-guide/ |
| G76 | How Top ISVs and Partners Turn Cloud Marketplaces into Net New Revenue Engines (Roman Kirsanov) | Partner Insight | 2025-03-18 | CREATOR | https://partnerinsight.substack.com/p/how-top-isvs-and-partners-turn-cloud |
| G77 | Shobana Shankar: Inside Google Cloud's Playbook for ISV Partnerships (Chip Rodgers) | Inside Partnering | 2026-03-06 | CREATOR | https://insidepartnering.substack.com/p/shobana-shankar-inside-google-clouds |
| G78 | Samrah Khan: How Google and Services Partners Co-Sell and Win in AI | Inside Partnering | 2025-09-02 | CREATOR | https://insidepartnering.substack.com/p/samrah-khan-how-google-and-services |
| G79 | Rajiv Batra: From Industry Insight to Scalable Partner Solutions | Inside Partnering | 2026-03-31 | CREATOR | https://insidepartnering.substack.com/p/rajiv-batra-turning-partner-collaboration |
| G80 | 5 ways Google Cloud partners are driving the next phase of enterprise AI (Partner AI Series) | SiliconANGLE | 2026-02-23 | INDEPENDENT | https://siliconangle.com/2026/02/23/google-cloud-partners-drive-enterprise-outcomes-googlecloudpartneraiseries/ |
| G81 | How to Co-Sell With Google Cloud: The Partner Network and the Co-Sell/Services/Technology Model | flashdba | 2026 | CREATOR | https://flashdba.com/hyperscaler-gtm/co-sell/google-cloud/ |
| G82 | Cloud hyperscalers reshuffle cloud channel economics and competitive landscape for 2026 (Sharon Hiu) | Omdia | 2026-05-11 | INDEPENDENT | https://omdia.tech.informa.com/om145061/cloud-hyperscalers-reshuffle-cloud-channel-economics-and-competitive-landscape-for-2026 |
| G83 | Omdia unveils Champions in the 2026 Cloud & Data Center Ecosystem Leadership Matrix (Alastair Edwards) | Omdia | 2026-07-07 | INDEPENDENT | https://omdia.tech.informa.com/blogs/2026/july/omdia-unveils-champions-in-the-2026-cloud-and-data-center-ecosystem-leadership-matrix |
| G84 | Google Cloud Set to Launch Partner Program Updates in 2026 (Jordan Smith) | Channel Insider | 2025-12-30 | INDEPENDENT | https://www.channelinsider.com/channel-business/vendor-leadership-and-partner-programs/google-cloud-partner-program-2026/ |
| G85 | Google Cloud reveals all-new channel program (Craig Hale) | TechRadar Pro | 2025-12-23 | INDEPENDENT | https://www.techradar.com/pro/google-cloud-reveals-all-new-channel-program-heres-all-the-key-details |
| G86 | Google Cloud to Launch New Partner Program in 2026 (Tony Jones) | ChannelVision | 2025-12-17 | INDEPENDENT | https://channelvisionmag.com/google-cloud-to-launch-new-partner-program-in-2026/ |
| G87 | New ways for Google Cloud partners to develop and demonstrate deep product expertise (Premier badges, legacy) | Google Cloud Blog | 2023-07-11 | OFFICIAL | https://cloud.google.com/blog/topics/partners/new-product-specific-premier-badges-and-incentives-for-partners |
| G88 | Updates to our Partner Advantage program (Expertise and Specialization, legacy) | Google Cloud Blog | 2020-07-15 | OFFICIAL | https://cloud.google.com/blog/topics/partners/differentiate-yourself-as-a-google-cloud-partner-and-grow-your-customer-base/ |
| G89 | Partner Summit: Google Cloud Next (Next '27 dates) | Google Cloud Events | accessed 2026-09-26 | OFFICIAL | https://www.googlecloudevents.com/next-vegas/partner-summit |
| G90 | Alphabet Q2 2026 10-Q (fiscal year = calendar year) | Stock Titan (SEC filing mirror) | 2026-07 | INDEPENDENT | https://www.stocktitan.net/sec-filings/GOOG/10-q-alphabet-inc-quarterly-earnings-report-8ffb92bbee5d.html |
| G91 | (reserved) | | | | |
| G92 | Philip Larson, Google Cloud, Google Cloud Next 2026 (video transcript) | SiliconANGLE theCUBE (YouTube) | 2026-04-22 | INDEPENDENT | https://www.youtube.com/watch?v=bs3AvAtXs-U |
