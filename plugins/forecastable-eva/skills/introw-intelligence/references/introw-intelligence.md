# Introw Intelligence

Version: 2026-09-29. Next refresh due: 2026-10-29 (monthly). Sections 1 to 11 are public-source research; section 12 is live-tenant observation [L1].

Compiled 2026-09-29 from public sources only (vendor site, docs.introw.io, support.introw.io, marketplaces, review sites, press). Every fact carries a source tag [Sn]; the numbered source list is at the end. Tags used:

- VENDOR = marketing or self-reported claim by Introw, not independently verified.
- COMPETITOR = claim made by a competing vendor about Introw.
- UNVERIFIED = conflicting, inferred, or only partially supported by sources.
- CONFLICT = two Introw sources disagree; both are recorded.

Docs note: Introw runs two documentation properties. docs.introw.io is the newer, much larger product documentation (516+ pages, organized as "feature index + technical page + how-to guides", plus release notes, API reference, OpenAPI spec and an llms.txt index) [S16][S17]. support.introw.io is the older Intercom help center (11 collections, about 234 articles) that still hosts monthly product-update posts and many how-to articles [S15]. When the two disagree, docs.introw.io is generally newer.

---

## 1. Company overview

### 1.1 Identity, HQ, founding
- Legal entity: Introw BV (AppExchange provider name) [S140].
- HQ: Dok-Noord 4E 102, 9000 Ghent, Belgium. US office: 447 Broadway, 2nd FL #378, New York, NY 10013 [S4][S3].
- Founded: May 2023 per About page [S3]; 2023 per press [S5].
- Founders: Andreas Geamanu (Co-founder and CEO), Laurens Lavaert (Co-founder and CTO), Simon Van Den Hende (Co-founder, CPO and Head of AI) [S3][S4]. The 2024 funding post also lists Lorenz Bogaert, Toon Coppens, Nicolas Van Eenaeme and Vincent Verlee in a founders/backers list; their roles are UNVERIFIED (likely angels or founding contributors, not operating founders) [S6].
- Other named staff: Wouter Moyaert (Head of Solutions), Adele Coolens (Partner and Customer Marketing), Peter Vermeulen (Staff Engineer), Janis De Sutter (Software Engineer), Tibo Declerck (Full Stack AI Engineer) [S3].
- Headcount: team grew from 4 to 15 during 2025 [S4][S5]; About page says roughly 30+ employees, fully distributed with HQ in Ghent [S3]. VENDOR.
- Original concept (2024): "Digital Partnership Rooms", shared collaborative spaces where partners work without individual accounts, claiming "up to 80% partner adoption" vs an industry norm of 25% [S6]. VENDOR. This lineage explains Introw's persistent "off-portal / headless" positioning and why some API parameters still use `roomId` [S90].
- Awards: nominated for Deloitte Rising Star 2026 [S147]. HubSpot Certified App Partner since December 2024 [S147][S139].

### 1.2 Funding
| Date | Round | Amount | Investors | Source |
|---|---|---|---|---|
| 26 May 2024 (blog date) | Seed / pre-seed | EUR 1M | Pitchdrive (lead); angels Pieterjan Bouten (ex-Showpad CEO), Ewout Meyns (ex-HubSpot), Dieter De Mesmaeker (DataCamp) | [S6][S4] |
| 13 Nov 2025 | Called "Series A" on About page; press calls it a raise | USD 3M | Visionaries Club (lead), Pitchdrive | [S4][S5][S3] |

CONFLICT: the About page dates the EUR 1M round to October 2023 [S3], while the announcement blog is dated 26 May 2024 [S6]. Treat the round as closed late 2023, announced May 2024 (UNVERIFIED).

### 1.3 Positioning
- Current tagline: "#1 Agentic Partnership Management Platform" / "#1 Agentic PRM"; CRM-native, "headless" PRM that meets partners where they already work (CRM, Slack, Teams, WhatsApp, email, AI assistants) instead of forcing a portal login [S1][S96]. VENDOR.
- Core thesis: the CRM (HubSpot or Salesforce) is the system of record; Introw adds a partner layer on top with two-way sync, so "nothing to migrate and nothing to reconcile later" [S16 why/crm-native][S38].
- Explicitly out of scope per roadmap: "portal-optional architecture" is the direction (partners use native tools), no consultant-dependent implementations, no parallel data systems [S31].
- Marketing metrics (VENDOR): +30% partner pipeline, +50% faster onboarding, under 2 weeks average time to go live, 4.9/5 G2 [S1][S139]; "2,000+ partnership professionals use the platform" [S139]; 100+ B2B customers in 30+ countries, revenue quadrupled in 2025 [S4][S5].

### 1.4 ICP
- B2B SaaS and tech companies running resellers, referral partners, distributors, SIs/implementation partners, agencies, co-sell/tech partners and (since May 2026) affiliates [S1][S98][S26].
- Industry pages: cybersecurity, HR tech, fintech, SaaS, legal tech, manufacturing [S1].
- Third-party framing: "mid-to-upper-market", "not ideal for very small teams seeking budget solutions or enterprises needing deep TCMA and global governance" [S142] (COMPETITOR); "startup-to-growth teams that want a clean partner portal and fast setup" [S155].
- Heavy European footprint (Belgium HQ, EU customers such as Factorial, Personio, Ringover, Quatt, Parloa, Storyblok) [S1][S4].

### 1.5 Notable customers (public)
Logos/case studies: Ringover, Quatt, Factorial, Aikido, Cumulocity, Zenity, Sedai, Epiphan Video, Xelix, WeGive, SafeBreach, Payflip, Cubbit, Coder, Tensis, SANDSIV [S7][S147]; homepage logos also include Sharegate, Archer, Axon, Personio, Parloa, ReversingLabs, Storyblok [S1].

Case-study metrics (all VENDOR):
- Ringover: partner activity 20% to 70%, 25% connect daily, 200+ lead submissions [S1][S7].
- Quatt (heat pumps, HubSpot + Slack): 10 to 200+ installer partners in a year (20x), 1,400+ form submissions year one, 200+ partners submitting outside the portal; built its own AI assistant on the Introw MCP with Claude to pull partner details, check orders and update deals [S9]. Public portal at quatt.introw.io [search result].
- Factorial (HubSpot): go-live March 2025, under 4 weeks to launch; 6x partner-engaged deals, 3x registrations per quarter, active partner users 100+ to 500+/month, partner activity on deals 30% to 80%, partner roster 300+ to 700+ companies; uses the AI agent to fill HubSpot properties on handover [S8].
- Aikido: 500+ partner-sourced deals per quarter; Cumulocity: 20% of revenue via partners in 15 months; Zenity: 2x deal registrations annually; Payflip: 200% partnership revenue increase [S7].


### 1.6 Pricing and plans
Public pricing page lists four tiers with no list prices; "Pricing is tier-based on the number of partners you manage" [S2].

| Plan | Internal users | Key inclusions | Key exclusions | Source |
|---|---|---|---|---|
| Starter (Free) | 3 | 1 partner portal; HubSpot and Salesforce; unlimited forms; deal collaboration; content library; Slack, Zapier, Claude | Custom domain, SSO, custom reports, multi-currency, LMS, Crossbeam | [S2] |
| Pro | 3 | Multiple portals; HubSpot only; 20 custom reports; RBAC; unlimited commission plans; 5 goals; 1 certificate; email/in-app support | Salesforce, Crossbeam, multi-currency, custom domain, SSO | [S2] |
| Scale ("Most Popular") | 5 | 50 custom reports; multi-currency; 10 goals; unlimited certificates; HubSpot and Salesforce; Crossbeam; priority support via shared channel; custom domain, custom font, custom email domain | MDF, CPQ, Affiliate, LMS, Embed are add-ons | [S2] |
| Enterprise | Custom | Custom partners and users; custom-object collaboration; unlimited reports/goals/certificates; dedicated CSM; internal and external SSO; all integrations | n/a | [S2] |

- Add-ons across plans: MDF, CPQ, Affiliate, LMS, Embed, Power BI, API connection, Multi-lingual (30+ languages) [S2]. Docs also list as on/off modules: commissions, courses, certificates, MDF, affiliate campaigns, Power BI, custom domains, portal SSO, WhatsApp; Crossbeam and Deal Coaching are also described as modules/add-ons [S21][S45][S92].
- Metered items: partner portals (consumed when an experience is published to a partner; republishing never consumes), internal seats (partner contacts do not consume seats), saved reports, goals (definitions, not enrollments), active portal languages, API credits. "Nothing is unlimited by default unless explicitly set on your plan." Publishing beyond limit blocks with "Select fewer new partners or upgrade your plan to add more portals" [S21]. CRM-only roles are unlimited seats [S22].
- Free plan per docs: one partner portal; one each of goals, reports, courses, languages, workflows, certificates, deal coaches, commission plans; unlimited partners, forms, announcements, tasks, journeys, assets; pre-seeded demo program (referral and reseller experiences, CRM-mapped forms, tiers, asset folders, journeys, sample reports); "The second partner is the moment the free plan ends" [S20]. CONFLICT: pricing page says free = 5 goals [S2]; docs say 1 [S20].
- Observed price points (third party, may be stale): AWS Marketplace 12-month contracts, Basic USD 5,000/yr, Pro USD 12,000/yr [S141]; Capterra "starting at $299/month" [S138]; Growann "$329/month for up to 10 partners", "Pro from $499/month" [S143]. UNVERIFIED and inconsistent; treat as indicative of a low-thousands to low-tens-of-thousands USD/yr range for SMB/mid-market.
- HubSpot Marketplace lists Free, Pro, Scale, Enterprise with 14-day trials on paid plans [S139]. AppExchange: Freemium, nonprofit discounts available [S140].
- Salesforce is excluded from Pro (HubSpot only) [S2]. This matters when recommending tiers to Salesforce shops.
- Introw Pay is fee-based (percentage of processed transactions), included in all plans; fee either billed to vendor or deducted from partner payout, negotiated with the account manager [S63][S22].

---

## 2. Product architecture and core concepts (admin mental model)

### 2.1 Objects and vocabulary
- Organisation: an Introw tenant. One user can belong to many organisations (multi-tenant access, org switcher in top-left avatar; each org is a walled garden; creator becomes Admin) [S132]. Useful for agencies/consultants managing several clients and for sandbox vs production [S132].
- Partner: a CRM company/account (or custom object record) detected by filters; each partner has People (contacts), a Team (internal owners by role), tier(s), phase, segment memberships, an assigned Experience [S60][S38].
- Experience: a portal template (tabs, sections, forms, pipelines, assets) assigned to partners. Publishing an experience to a partner creates a "portal" and consumes the portal meter [S21][S103]. Experiences have draft/published/preview states and version history with restore [S17].
- Segment: reusable audience (static or dynamic) of partners and contacts. Since June 2026 segments replaced per-contact roles as the audience model for announcements, assets, courses, tabs, permissions and notifications [S25][S56].
- Forms: no-code forms mapped to CRM objects (deal registration, lead share, onboarding, partner application, MDF steps, feedback) with CRM automations and approval gates [S54][S55].
- Shared pipeline / collaboration record: a CRM record (deal, ticket, lead, custom object) attributed or shared to a partner and shown in the portal with field-level visibility/edit controls [S52].
- Journeys and Tasks: onboarding/enablement checklists (formerly task templates) with due dates, flexible or sequential [S29][S23].
- Workflows: no-code automation canvas (Aug 2026, rolled out per org) [S23][S84].
- Partner Connect: partner-side surfaces (partner's own CRM card, AI assistant via MCP, Slack/Teams/WhatsApp) at partners.introw.io [S82][S24].
- Apps/URLs: vendor app at app.introw.io (forms at /forms, submissions at /submissions, internal AI at /agent, Claude connector at /settings/integrations/claude) [S65][S93][S71]; partner-side app at partners.introw.io [S82]; portals on {sub}.introw.io or a custom domain [S59][S77].

### 2.2 CRM sync model (most important for admins)
- Supported CRMs: HubSpot and Salesforce (production or sandbox) are fully documented [S38]. Pipedrive is marketed (OAuth in under 5 minutes, Organizations as partners, dropdown "Linked to Partner(s)" attribution, two-way sync of stage/value/close date/custom fields) [S13] and referenced in docs (disconnect Pipedrive before Salesforce; Aug 2026 Pipedrive record search fix) [S35][S23], but the CRM technical page documents only HubSpot and Salesforce [S38]. Treat Pipedrive as supported but less mature (UNVERIFIED depth).
- Only one CRM can be connected at a time [S32][S35][S38].
- Sync cadence: partner-linked record changes CRM to Introw in about 1 minute; full record import every ~15 minutes; deletions/merges via webhook (immediate); owners/pipelines/stages/currency rates on scheduled import; form-created records Introw to CRM immediately; tier/manager/team roles and contact portal access Introw to CRM real-time where mapped; course enrollments/certificates as CRM records every ~15 minutes; HubSpot timeline activity real-time; comments/tasks/files/field edits on shared records both ways real-time [S38]. The Sync-a-CRM-object API endpoint exists but "You usually do not need this" [S16].
- Write safety: defaults to "Fill if empty" (never overwrite a value your team set); "Overwrite" is opt-in per field; empty/unmapped values are skipped so a submission cannot blank a field; since Aug 2026 an omitted property no longer clears a field, only an explicit empty value does [S54][S23].
- CRM validation rules and picklist values are enforced before writes; picklists inherit live CRM options with opt-out hiding per form [S129][S24].
- Deduplication: companies matched by name + domain (including submitter email domain), contacts by email, deals by associated accounts/contacts within a recent window; match keys tunable, any field can be a match key since Aug 2026 (custom ID keys work) [S54][S23].
- Credentials: CRM tokens stored in a dedicated credential vault outside the app [S38][S72].
- No email alert when a connection breaks; admins must check the Integrations page [S40].

### 2.3 Partner detection (3-question setup)
Same pattern for HubSpot and Salesforce [S32][S35][S60]:
1. Where partners live: HubSpot Company (recommended) or custom object; Salesforce Account (most common) or custom object.
2. Which records are partners: property filters (e.g., Type is Partner or Reseller; record type; checkbox), select all or a pilot subset; toggle "Automatically sync new partners" so new matching records auto-become partners. Default HubSpot filter looks at company type = Partner or Reseller [S133].
3. Object linking and attribution: add Deal/Opportunity attribution first (required), then optional Contact, Company, Ticket, Lead (HubSpot) or Contact, Case, custom (Salesforce). Name each attribution (e.g., "Influencing partner", "Reseller").
- Changing the partner object resets filters and links [S32][S35].
- If "exceeded the maximum number of partners", tighten the filter [S32].
- Account owner is imported as a suggested team member; partner contacts import under People; access starts as "Requested" and must be approved [S60].

---

## 3. CRM integrations in depth

### 3.1 HubSpot
Connect [S32]: Integrations > CRM & Data > HubSpot > Connect; HubSpot user must be able to approve third-party apps and must accept every scope (declining any blocks the connection). Tile shows "Connected" on success.

Scopes [S33]:
- Required: companies read/write + schemas; deals read/write + schemas; owners read; line items read/write + schema + e-commerce; quotes read + schema; tickets full; `settings.currencies.read`.
- Conditional: contacts (partner contacts), custom objects, `files` (uploads), `crm.objects.quotes.write` (partner quoting), orders/invoices/subscriptions (commerce data), `sales-email-read` (email engagement).
- Optional: leads read/write (decline with no cascade failure).
- HubSpot scopes are portal-wide to the app; connecting as a restricted user does not restrict Introw (unlike Salesforce).
- Missing scope: objects not offered, permission notices on screens, read-only properties struck through; "Install update" when new scopes are needed; re-check permissions without reconnecting.

Attribution methods [S34][S133][S134]:
| Method | How | HubSpot plan | Notes |
|---|---|---|---|
| Custom property | Deal dropdown/property holds the partner; Introw can manage dropdown options | All plans | Simplest; weak for multi-partner; values must map to partner companies |
| Association label | Labeled deal-to-company association (e.g., "Partner", "Reseller", "Partner Influenced") | Professional or Enterprise | "Sweet spot"; distinguishes sourced vs influenced; labels need Super Admin to create |
| Custom object | Dedicated Partner object associated to deals | Enterprise | Richest data (tier, region) |
Multiple named attributions can coexist on one object, e.g., "Sourced by" and "Influenced by", each independently used for reporting and commissions [S34][S135]. December 2025 added "multi-attribution for CRM deals" when creating records [S114].

HubSpot app cards [S42]:
- Introw Collaboration card: deal and ticket sidebars; shows linked partner, tier, collaborators, champion/manager; share, comment, register/link deals, Ask AI, open portal. Replaced the legacy "Introw Copilot" card in Aug 2025; admins had to add the new card to all views [S117].
- Introw Partner card: company sidebar and partner objects; show/create partner, invite contacts, open portal.
- Introw Collaboration tab: full record tab for companies, tickets, partner objects.
- Cards must be placed manually (customize record, search "Introw"); app events and app objects deploy automatically.
- Property visibility conditions (Sept 2026) also apply to the HubSpot partner card [S22].

HubSpot workflow actions [S43][S139]: Create partner (company-enrolled workflow; set experience, manager, portal access), Update partner (experience, tier, phase, manager), Enroll partner in journey, Issue certificate (contact or company). Marketplace listing also names "Search partners" and "Update CRM object" [S139].

HubSpot app events [S44]: six event types written to both the partner contact and company timeline: Portal visit, Comment, Asset viewed, Object update (with before/after values), Form submitted, Deal closed won. Usable in reports and as workflow enrollment triggers. Sept 2026 added triggering HubSpot workflows from partner engagement events [S22].

App objects: course enrollments and certificates appear as HubSpot app objects [S17 show-course-progress-in-hubspot][S102 #38].

CRM Users (HubSpot) [S41][S100]: access Introw only via HubSpot cards, no separate Introw login; can see partner on deal/ticket, share records, comment with partners, register/link partner deals, see portal activity; cannot configure, create partners, or get non-CRM notifications. Recommended for sales/support reps. CRM-only roles are unlimited seats [S22]. The support article says CRM User is HubSpot-only [S100]; a Salesforce "CRM users vs Admin users" doc also exists [S18], and the Sept 2026 Salesforce Collaboration panel serves reps without Introw login [S22] (UNVERIFIED whether Salesforce CRM-only role is identical).

Other HubSpot features: create a partner portal from within HubSpot [S18]; capture partner file uploads in HubSpot [S18]; collaborate from HubSpot tickets [S102 #67]; HubSpot Agent Hub use case [S17]; Introw CPQ on HubSpot quotes and line items [S112]; HubSpot CRM-only users see full deal conversations in HubSpot (Sept 2026) [S22]; HubSpot custom objects support board view in shared pipelines (Sept 2026) [S22].

Marketplace listing [S139]: 4.9/5 from 80 reviews (95% five-star), 500+ installs, HubSpot Certified App, languages Dutch/English/French/German/Italian/Spanish, "Rising" tier partner.

### 3.2 Salesforce
Prerequisites [S35][S37]: dedicated integration user (Salesforce or Salesforce Integration license) with a scoped permission set; Introw connected app installed/allowed first; no other CRM connected; decide production (login.salesforce.com) or sandbox (test.salesforce.com); Introw permission to manage integrations.

Managed package: IntrowPRM, contains custom objects, integration permission set, Lightning component for record pages [S35]. Version history seen: v1.10.0 listed (last updated 04/24/2026) [S140]; IntrowPRM 1.15.0 shipped Sept 2026 with the Collaboration Panel; legacy orgs see "Install update" on the integration page [S22]. AppExchange: 5.00/5 from 10 reviews, Lightning Ready, "No Limits" (does not count against org limits), multi-currency, Freemium [S140].

Gotchas [S37][S39]:
- Since September 2025 Salesforce blocks authorization of connected apps not installed in the org unless the user is admin or has "Approve Uninstalled Connected Apps". Flow: attempt connect (fails with OAuth error) > Setup > Connected Apps OAuth Usage > install app or exempt integration user > reconnect.
- Do not give the integration user "Use Any API Client" or "Approve Uninstalled Connected Apps"; install and scope the named Introw app instead.
- Introw runs as the authorizing user and inherits exactly its access (FLS, CRUD, sharing rules). Verify on the Integrations page that the connection is the integration user, not an admin. Since Aug 2026 Introw displays which CRM user the connection authenticates as, plus instance and connection date [S23].
- Salesforce silently omits unwritable fields; check FLS before mapping [S40]. Since Aug 2026 Introw reports per-property limitations (e.g., "Read-only in your CRM") instead of failing the whole connection, and shared deal views omit unreadable fields [S23].
- Sandbox and production are separate connections [S35]. Salesforce always requests sign-in on connect (Sept 2026) [S22].
- The Lightning component must be placed on record layouts manually by an admin [S38].

Permission set baseline [S37]: read Account (Name, Website, Industry, Description, NumberOfEmployees, AnnualRevenue, Phone, billing address, OwnerId, Id), Contact (FirstName, LastName, Email, Title, Phone, MobilePhone, Id), User (Id, FirstName, LastName, Email, SmallPhotoUrl); read on embedded objects and attribution links; create/edit only where forms, partner edits, attribution writes (create on OpportunityPartner) or write-back mappings need it; LMS permissions via package permission set. OAuth scopes: api, refresh_token, lightning.

Attribution methods [S36][S112]:
| Method | Notes |
|---|---|
| Picklist on Opportunity | Lightest; one partner per opp; value drift risk |
| Lookup to Account | Recommended default; standard `AccountId` usable where the Account is the partner (distributor/reseller models, July 2026) [S24] |
| Relation (junction) table | e.g., native OpportunityPartner with Role and IsPrimary; many partners per opp with roles; can filter by Role |
| Custom object | Dedicated Partner object; most flexible, most schema work |
Methods can be layered for multi-tier (e.g., junction for resellers + lookup for implementation partner) [S36]. New deals submitted via Introw populate partner + role on OpportunityPartner automatically [S135].

Salesforce Collaboration Panel (Sept 2026, IntrowPRM 1.15.0) [S22]: on Opportunity and Case pages; lists partners with tier, champion, contacts; actions Ask AI, Collaborate, Share opportunity; opens an Introw overlay with no separate login; requires the "Introw Collaboration User" permission set. Form automations can set Record Type; stage fields offer custom object stages; reports fill "Days to close"; dependent picklists follow controlling field [S22].

Known Salesforce parity gaps: property visibility conditions "Not yet in Salesforce embed" (Sept 2026) [S22]; Partner Connect deal linking is HubSpot-only [S82]; CRM parity is an explicit roadmap direction [S31].

### 3.3 CRM troubleshooting reference
Connection status pills [S40]: Connected; Update available (approve new scopes / install package update); Needs attention (one or more mappings broken); Rate limited (clears automatically); Interrupted (reconnect via three-dots menu, accept all scopes); Not connected.

Mapping failures [S40][S39]: red warning pill in Object Linking for deleted/renamed property, missing association label, Salesforce permission/schema change, inaccessible relation table, MDF sync failure. Fix: repick property or restore permission, then "Re-check after changing permissions" (access checks are cached).

Access verdicts per object [S40]: No access, No read access, Cannot read back (urgent: records created but invisible), Cannot create, Read-only, Cannot update, Partly visible (sharing rules hide records; cannot be quantified), Fields read-only, Record types limited, Visibility unknown.

Submission errors [S40]: Could not create [object], Not allowed to write record/fields, Cannot access linked record, Field not writable, No access to object type, Value not available (picklist/record type), Record no longer exists, Action not permitted, Missing required data (editable, retry), Data validation failure (editable, retry). Failed submissions can be edited and retried; retry re-runs CRM creation and restarts approval (Aug 2026) [S23].

HubSpot card errors [S40]: "Something went wrong" (transient), "Connection lost" (HubSpot admin clicks Reconnect), workflow action failed (check HubSpot workflow history).

Deals not showing in the partner portal [S53][S107]: "No portal yet" = partner has no experience assigned (assign one with a deal pipeline section); "No deal embed yet" = experience lacks a pipeline section for that deal's pipeline (add/modify section). Then publish and reopen the deal. Also check attribution is configured, collaborator scoping, and the "See all shared records" permission [S52][S58].

---

## 4. Feature-by-feature reference

### 4.1 Partner management
- Partners list with saved views, inline CRM field editing (writes straight to CRM, relabel for display), bulk updates, bulk team role/CRM owner editing, safe bulk delete (type "delete") [S24][S23][S27][S116].
- Partner detail view: activity, open deals, shared assets, performance, notes [S116][S126].
- Partner team (June 2026): multiple internal people per partner with roles; roles can map to CRM properties; used in variables, deal owner assignment, approvals ("Partner team role" approver), certificate issuing [S25][S55].
- Tiers [S57]: multiple independent tier programs (e.g., separate Silver for resellers and referrals, since July 2025 [S118]); each tier has name, color, optional 512x512 PNG badge (max 20 MB), description, requirements and benefits; items can be text, checkbox, or goal-linked with live progress (goals in tiers since Dec 2025 [S114]); one tier per partner per program; bidirectional CRM sync requires mapping every tier. No documented automatic tier promotion; the "Tier Promotion Batch Review" is an AI skill with human review [S17]. UNVERIFIED whether workflows can auto-promote (a workflow "Update partner properties" action exists [S84]).
- Goals and KPIs: per-partner goals from CRM data (sourced pipeline, closed revenue, influenced deals), fiscal-year aware buckets [S114][S23].
- Partner directory: public directory built from Introw data [S104].
- Partner application form and dynamic partner conversion links [S111][S104].

### 4.2 Segments, permissions and access
- Dynamic segments: CRM properties plus Introw-native fields (name, phase, tier, last activity, completed courses, certificates, nudge history), operators (is known, contains, is any of, rolling dates), nested AND/OR; re-evaluated on schedule; membership persisted as a stored snapshot since Aug 2026 [S56][S23].
- Static segments: hand-picked; since Aug 2026 static segments with partner + contact filters require explicit contact inclusion [S23].
- Defaults and overrides (Aug 2026): one org-wide default for partner permissions and notifications ("All partners" pinned row); a segment changes settings only when an override is switched on; cascade is org default > override segments > contact opt-outs; when a contact matches several segments the most permissive value wins; override segments must target a subset (a dynamic segment with no conditions is disallowed) [S23][S56].
- Partner-side permissions: "Invite colleagues" and "See all shared records" (off = contact sees only records where they are a collaborator) [S56][S58].
- Visibility rules [S58]: one partner never sees another; unshared records do not exist for partners; only opened fields are visible; free email domains (Gmail etc.) cannot inherit access by domain; CRM sharing rules do not transfer to partners.
- Portal access [S59]: login via 6-digit email OTP (valid 15 min, single use, 3 attempts, 1 request per 60 s per email), Google, Microsoft, or SSO (paid; when enabled it becomes the only method); partner session lasts 30 days; access by invite or by trusted email domain; one login across multiple portals; tabs restrictable to segments. Portal access can be driven from a CRM contact property [S83][S117].
- Aug 2026 behavior change: a form submission no longer grants portal access automatically; requires the "Partner automation" invite setting [S23]. Failed logins no longer create CRM contacts (Sept 2026) [S22].
- Internal roles [S99]: defaults Admin, Partnership Manager, CRM User; access types Admin, Custom, Partner Manager (assigned partners only), CRM Only User; permission categories Portal (configuration, experiences) and Settings (integrations, team, billing); Workflows permission toggleable per role (Sept 2026) [S22]. Internal notifications per role: all partners, own partners only, collaborating partners only, disabled [S27].
- Team admin: bulk invite by pasting emails, delete (not only deactivate) members with records retained, paid-seat validation including SSO/SCIM joins, optional IdP sign-out on SAML/OIDC (Sept 2026) [S22].

### 4.3 Partner portal (Experiences)
- No-code builder: tabs (layouts Centered, Expanded, Full width), tab groups (dropdown nav) and URL tabs (Sept 2026), sections (rich sections, synced sections reused across portals, CTA buttons with custom colors, partner profile, introduction section showing the partner manager, news/social widgets, calendars/appointment schedulers, Notion embeds, website embeds that auto-resize, dashboards, Power BI), columns up to 8, section backgrounds, maximize sections, custom TTF fonts, dynamic variables with "{" [S101][S103][S22].
- Any CRM object, including custom objects, can be a portal section (Sept 2026) [S22].
- Draft/published/preview, version restore, reuse across partner types/regions [S17].
- Branding and white label: logo, colors, login artwork, fonts; AI image generation on every uploader (Aug 2026) [S23].
- Custom domain [S77]: paid; add Introw-generated DNS records (host pointing + ownership verification); SSL auto-issued after verification; until verified the portal serves on the default subdomain; redirects from an old portal supported; custom-domain portals keep their own favicons [S22]. Required to embed forms on a website [S131][S65].
- Custom email domain [S78]: DKIM TXT + return-path CNAME (no separate SPF needed; DMARC aligns via these); verification switches sending on; default sender otherwise `ecosystem@mail.introw.io` [S86]; display name and sender address editable without re-verifying.
- Mobile: installable PWA on home screen; mobile-responsive courses [S110][S22].
- Localization [S17][S28][S27][S30]: multilingual portal (partner preference or self-select, org default fallback), brand glossary, document and filename translation, English (UK) added Sept 2026; multi-currency with read-only CRM conversion rates; 30+ languages add-on [S2].
- Embed portal in your product via API session URLs and iframe (see 4.12).

### 4.4 Forms, deal registration, lead sharing
- Form builder: field types incl. checkbox, uploads, quotes, partner-select; conditional visibility (Aug 2026; "not an access-control or security feature"); field descriptions; video embeds (YouTube, Loom, Vimeo, Vidyard); rich body editor; templates for partner forms [S23][S28][S17].
- Sharing/submitting: portal, partner-specific links (auto-attributed), website embed (custom domain required), email (AI agent reads and submits), AI assistant via MCP, Slack/Teams/WhatsApp chat, API, bulk multi-upload of records via CSV (delimiter auto-detected), bulk submit [S65][S17][S23].
- Spam protection: invisible reCAPTCHA on public/embedded forms, not inside the authenticated portal [S130].
- Automation tab (Sept 2026 redesign): linear flow Submission > Review > Notifications > Records written; each record shows record type, match logic, partner links, mapped fields, defaults; lookups can reference records created by the same submission [S22].
- Approval gate modes (Sept 2026): Manual; AI Assisted; Autonomous AI (agentic, acts above a confidence threshold) [S22]. Approver per step: Anyone, Partner team role, Specific team member, Fund owner (MDF) [S55].
- Submission statuses: Pending, Accepted (final; cannot be reversed), Auto accepted, Declined, Returned (partner edits and resubmits), Error (editable, retry) [S55]. Inbox select-all only selects loaded rows [S55].
- Deal registration specifics [S50]: conflict check across deals, contacts and companies; outcomes create new, link to existing, or decline; configure deal owner and deal name rules [S102]; link a registered deal to an existing lead [S17]; auto-accept only for conflict-free submissions without approval; requires attribution configured.
- Channel conflict: AI assessment runs on registration, shows who is involved, which claim came first, rules; since Aug 2026 the assessment is in reviewer notifications with a "Resolve conflict" button; never shown to the submitting partner [S51][S23][S129]. With Crossbeam connected, submissions are cross-checked against Crossbeam customers, prospects and open opportunities and flagged [S48].
- Two-tier channel: automatic attribution of reseller and distributor; register a two-tier deal; multi-tier attribution [S102 #7][S17].
- Lead sharing / referrals: referral arrives as an attributed lead; when partner-qualified, full deal context is created; referrers get automatic deal progress updates [S65][S17].

### 4.5 Shared pipelines and co-selling
- Views: board by stage or table; multiple named views with filters; aggregation property configurable (e.g., MRR, ACV) [S52].
- Per-field Visible / Editable / Renamed; stages can be reordered, renamed, removed (removed = not a column and not an edit option) [S52].
- Property visibility conditions by stage (Sept 2026), not yet in Salesforce embed [S22].
- Custom actions: buttons that run a form with conditions, approval gates and CRM automations, enabling guarded updates even on read-only fields; conditional visibility (Aug 2026) [S52][S23]. Pipeline rules can show rejection reasons (Sept 2026) [S22].
- Bulk updates: partners tick up to 100 records in table view; Edit sets one property across all; custom actions run once per record (Sept 2026) [S22].
- Collaboration: comments, @mentions, internal-only comments (hidden from partners, silent), tasks with owners and due dates, file attachments, activity timeline; reply-by-email threads onto the record [S26][S24][S83].
- Collaborators: partner contacts in the loop on a record; with the collaboration restriction, contacts see only records where they are collaborators [S117][S52]. Sharing no longer auto-subscribes all to updates (Sept 2026) [S22].
- Sleeping-deal nudges; watched-property notifications on key CRM field changes [S116][S119].
- Custom-object collaboration is a plan module (Enterprise) [S52][S2].

### 4.6 CPQ and products
- Partners build and send quotes on deals; product catalog visibility governed per partner; discount methods: None, Partner based (negotiated discount from CRM), Tier based, Custom price, Custom discount (July 2026) [S24][S17].
- Seller setting: organisation or partner (resellers quote on their own paper); Show pricing toggle per line item [S24].
- Quotes require line items to publish; HubSpot permission errors named (Sept 2026) [S22]. CPQ is an add-on on Scale [S2].

### 4.7 Commissions, SPIFFs, payouts
- Plans [S61]: data sources CRM (object, amount, date properties), billing (Stripe, Chargebee since June 2026), file upload (CSV/Excel up to 50 MB, column mapping remembered, Sept 2026); rate types fixed, percentage, tiered; rates target default, partner, segment or tier; frequencies one-time, monthly, quarterly, yearly with installments (file plans are not recurring); caps per rate; negative amounts reverse as credits; plan versions preserve terms (no retroactive repricing); unmatched file rows held for review.
- Referral reward templates: Revenue share, Fixed fee, Tiered (recurring, adjusts annually) [S64].
- Commission lines: generated on deal close or invoice paid, recalculated on CRM/billing change, reviewable/adjustable, manual lines; expected lines cleared on hard deal delete [S83][S23]. Origin column shows plan/file/manual/API [S22].
- Payouts [S62]: batch per period; stages draft, pending approval, pending partner invoice, pending payment, approved, scheduled, paid, declined, failed, blocked, postponed; only approved lines included; statement PDF (redesigned Sept 2026 to show per-line calculation, logo, VAT block, Markdown notes, custom PDF option); request partner invoices; contact-level visibility of own lines [S22].
- Introw Pay (Sept 2026) [S63]: vendor pays one consolidated invoice (EUR or USD company currency only); Introw distributes to partners by bank transfer (119 countries, KYC under 7 days) or PayPal (93 countries, no KYC, instant); partners verify bank details in the portal Payout setup section; vendor never collects account details; unverified partners held with reminders.
- Finance integration via API (NetSuite/Xero examples) [S16].
- Third-party note (older, now outdated): Growann states payouts must be handled separately [S143]; superseded by Introw Pay [S22]. COMPETITOR/third party.

### 4.8 MDF (Market Development Funds)
- Early access April 2026; lifecycle: funds and allocation (pooled by segment) > projects/requests > proof of expense (claims) > ROI > invoices; optional stages can be disabled; sequential human approval with AI pre-screening; deadlines with overdue warnings [S27][S66].
- Generic (fund-agnostic) intake: partner describes the activity, AI fills the form, reviewer assigns the fund; acceptance disabled until a fund is selected (July 2026) [S24][S66].
- CRM-backed MDF objects on HubSpot or Salesforce custom objects (Aug 2026) via Settings > Marketing Funds > CRM mapping [S23]. MDF is an add-on [S2].

### 4.9 Affiliate (May 2026)
- Campaigns with fixed per-conversion rewards or commission plans; links auto-provisioned on publish or when a partner opens the affiliate block; never duplicated or reissued after revoke; vanity aliases; revoke/restore [S26][S23][S67].
- Conversion tracking: browser snippet with publishable key and allowed origins, server-to-server Conversions API with scoped secret key (most reliable), native HubSpot form tracking; conversions only count inside the campaign attribution window after a tracked click (window length not published) [S69].
- Fraud controls per campaign Quality tab: self-referral block, disposable email block, dedup, new-customer gating, excluded domains; Links tab flags links for review [S68].
- PartnerStack migration: legacy link redirect endpoint maps old PartnerStack links to Introw links [S16].

### 4.10 Content, enablement, LMS
- Asset library with folders, audience filters, trackable share links, per-partner sharing, version history/restore/archive, translation and locale variants, PPTX/DOCX/XLSX preview, embeddable assets (Loom), bulk upload of 15 assets [S17][S25][S22].
- Asset Hub for partner-specific docs (contracts, co-branded materials); co-branded assets generated at scale or on demand [S124][S123].
- TCMA: campaign kits and partner campaign attribution [S17][S102 #76]. COMPETITOR claim that Introw lacks TCMA [S144] predates or ignores this; depth UNVERIFIED.
- Courses [S95]: manual or AI-generated from prompt/deck, SCORM import (up to 2 GB; manifest must be at root), sequential curricula, AI tutor, quizzes (multiple choice, open, upload; AI-graded; conversational quiz), certificates (AI backgrounds, org-issued, validity max 10 years, LinkedIn sharing, revoke), enrollment rules and segment auto-enroll, reminders, progress synced to CRM as enrollment objects [S23][S22][S102].
- Announcements: email + portal, AI-generated, AI-suggested from your LinkedIn posts weekly, categories and filters (Sept 2026), test sends to multiple addresses; consent-aware tracking automatically strips open pixels and link tracking for recipients in France and Italy based on CRM country [S22][S24][S83].

### 4.11 Notifications and channels
- Complete notification catalog [S85]: deals (new, update, closed won, sleeping deal, shared record), portal (announcement, comment, mention), submissions (submitted, accepted, declined, returned, error), tasks (assigned, onboarding, completed, reminder email-only), learning/goals, commissions/funds (payout ready, invoice uploaded, commission line change, MDF invoice forwarded), activity (portal visit, website visit, asset viewed, AI conversation started, monthly engagement summary email-only, Partner Connect nudge), transactional (always sent).
- Contact Notifications tab explains why a contact gets each event (default, overrides, opt-outs) [S23].
- Email troubleshooting [S86]: wrong/bounced address; event set to Disabled or Collaborating only; spam (allowlist `ecosystem@mail.introw.io` or custom domain); corporate gateway (allowlist `introw.io`, `mail.introw.io`); suppressed/unsubscribed (contact support@introw.io). Resend via People tab "Send invite".
- Slack and Teams [S79]: internal channels for team notifications and internal agent; one partner channel per partner (shared channel) where partners @mention Introw for the support agent; per-platform settings since Aug 2026; chat notifications are org-level, not per-contact; Teams bot added as custom app (store listing pending, Sept 2026); private/shared channel linking articles exist [S106][S22][S23].
- WhatsApp [S80]: paid add-on; Introw-provisioned number; inbound-first; partners recognized by exact phone number on the CRM contact.

### 4.12 AI features
- Partner Support Agent [S91]: channels portal AI tab, Slack/Teams partner channels, email, WhatsApp, MCP; answers only from knowledge base (websites crawled, snippets up to 125-char questions, documents incl. full PDFs, MCP tools), portal content, commission data; can run custom action buttons and submit forms; always escalates to partner manager by default (cannot remove hand-off); answers in the partner's language.
- Internal AI Copilot at app.introw.io/agent: reads CRM and knowledge base, takes actions within the user's permissions, conversations traced [S93].
- AI Deal Coaching [S92]: coach per pipeline and motion (Reselling, Co-Selling, Referral); tabs Stage Guidance, Objection Handling, Enablement, Rules of Engagement, Configure; proactive triggers (days after creation, before/after close, in stage); proactive Slack nudges default-on since March 2026 [S28]; requires CRM copilot write access and the Deal Coaching module.
- AI approvals (form approval gates), AI channel conflict, AI announcements, AI course/certificate builder, AI images [S17][S22][S23].
- AI security [S72]: all model calls go through Vercel AI Gateway to providers with zero data retention and no training on prompts/responses; Introw trains/hosts no models; fixed toolset (no browsing or code execution); authorization resolved before model runs; writes checked against editable fields; cross-partner isolation; subprocessors listed on trust.introw.io.
- Headless governance levels for agent actions: Read-only, Allowed, Approval required, Blocked [S96].

### 4.13 MCP and AI assistant connectors
- Vendor MCP: Settings > Integrations; OAuth, acts as the signed-in user; clients Claude (directory listing, "Connect in Claude"), ChatGPT (listing, "Install in ChatGPT"), Cursor, HubSpot agents, and generic MCP (Gemini, Windsurf, Notion AI, Lovable, Langdock, OpenClaw) via "Copy MCP Server URL" [S70][S71][S23][S105].
- Claude connector steps: app.introw.io/settings/integrations/claude > Copy MCP Server URL > Claude Settings > Connectors > add > OAuth; success shows "Connection is active" [S71]. Available on all plans [S71]; generic MCP connector requires "the MCP connection add-on" [S70]. CONFLICT with pricing page listing Claude integration on Starter [S2]: Claude and ChatGPT listed connectors appear free; other MCP clients may need the add-on (UNVERIFIED).
- Partner MCP: partners connect their own Claude/ChatGPT at partners.introw.io, scoped to their data; CRM connections stay with the partner admin [S70][S23].
- MCP tool calls do not consume API credits [S88]. Tool names are not published [S70].
- Skill library (docs): 19 vendor skills (e.g., Crossbeam Co-Sell Partner Finder, Tier Promotion Batch Review, QBR Prep, Email Deal Registration Watcher, Pipeline Partner-Influence Scout, Ecosystem Anomaly Detector, Weekly Channel Slack Digest) and 14 partner skills (e.g., Cross-Vendor Registration Status Tracker, Deal War Room, Incentive Maximizer) [S17]; blog "MCP for Partnerships: 31 Claude skills" [S146].
- Introw's own AI agent can call your MCP servers as knowledge/tools [S105][S116].

### 4.14 Public API (v1, first shipped June 2026)
- Base URL `https://api.introw.io/api/v1` (staging `api.staging.introw.io`); header `x-api-key`; scopes `partners:read/write`, `commissions:read/write`, `forms:read/write`, `affiliate:write`, `portal-sessions:write`, `collaborate:write`; keys created in Settings > Developers > API keys, scoped, time-limited, one-time secret, instant revoke [S87][S89][S16].
- Rate limit 120 requests/min fixed window (429); monthly credit allowance included on every plan since Aug 2026 (402 `API_CREDITS_EXHAUSTED`, do not retry, resets 1st of month UTC; headers `x-introw-credits-limit-month`, `x-introw-credits-remaining-month`); one successful request = one credit; errors, 4xx auth, publishable-key affiliate tracking and MCP calls are free [S87][S88].
- Endpoints: Partners (list, get by ID or external ID, create/upsert, update; accepts partner CRM record ID and experience template); Forms (get schema, submit; runs same pipeline as portal, `partnerId` may be Introw ID or CRM ID); CRM (sync object, rarely needed); Payout batches, Payouts (create, list, get, update stage/PO/statement note, generate statement PDF); Commission lines (list, create with optional `payoutId` and `idempotencyKey`, get, update, decline, detach); Collaboration (create comment on partner, deal, ticket, task, submission or payout; Markdown/HTML; @mentions; `isInternal`); Embed (create portal session, `POST /api/v1/auth/session`, optional `roomId` deep link, domain allow-list in Settings > Developers > Embed); Affiliate (record conversion, legacy PartnerStack redirect) [S16][S89][S90].
- Webhooks: not live. The app's Developers > Webhooks tab reads "Coming soon" (2026-09-29) [L1]. Event-driven integrations use HubSpot app events, Zapier triggers, Slack/Teams, or Workflows.
- Zapier: API-key auth; triggers such as new partner or registered deal; actions create/update records; full trigger list not published in docs [S81].
- Power BI: link Introw to Power BI and embed Power BI reports in the portal (add-on) [S106][S2].
- Billing integrations: Stripe and Chargebee import customers, subscriptions, invoices for commission plans (older Chargebee catalogs supported Sept 2026) [S25][S22].

### 4.15 Reporting and attribution analytics
- Report builder (fully live March 2026): CRM sources (deals, contacts, companies, leads, tickets) and Introw native sources (partners, engagement events, certifications, emails, assets, MDF, commissions); bar, line, pie, single number, table (records with custom columns, Aug 2026); count, distinct, sum/avg, ratio (win rate, conversion, acceptance); CSV export; drilldowns on line charts; partner account field aggregation with two-dimension breakdowns; fiscal year setting [S94][S28][S23][S24].
- Dashboards embeddable in the portal; partner dashboards; Partner Notifications report; email insights (opens, clicks, bounces) [S17][S29][S23].
- Sourced vs influenced: modelled as separate named attributions (properties, association labels, junction roles) rather than a built-in attribution model; reporting groups by attribution; Introw's blog recommends named roles (Sourced by, Influenced by, Distributor, Reseller) over first/last-touch models [S34][S135][S148][S94]. Report builder docs do not describe separate sourced/influenced logic [S94].

### 4.16 Automation
- Built-in automations (no setup): partner detection and auto-sync, contact import, owner suggestion, two-way property and tier sync, segment-driven access/notifications/pricing, CRM-property-driven portal access, domain access, SSO/SCIM provisioning, form-to-CRM with matching and fill-if-empty, approval routing, conflict detection, watched-property updates, journey auto-apply, task due dates and reminders, progressive unlocking, course auto-enroll, auto certificates and expiry, commission line generation and recalculation, scheduled payout runs, affiliate attribution, MDF lifecycle, sleeping-deal nudges, reply-by-email, referrer updates, support agent, deal coaching, weekly LinkedIn announcement suggestions, knowledge crawling [S83].
- Workflows canvas (Aug 2026, per-org rollout): 12 triggers (task assigned/completed, enrolled in/completed journey, course started/completed, certificate issued, partner created/updated, contact added/updated, segment membership; plus CRM record updated) and actions (update partner properties, update partner contact properties incl. portal access (Sept 2026), add to segment, give task, enroll in journey, give commission, issue certificate, send email, send chat message, log CRM note, move to experience); wait nodes relative to due dates; branching (a condition is always last in its chain, no merge node); variables via "{"; draft mode with single-partner test; delays cap at 180 days; max 10 runs of the same workflow per partner per hour [S84][S23][S22].

### 4.17 Security and compliance
- Claims: SOC 2 Type 2, ISO/IEC 27001:2022, GDPR programme; AWS hosting in Europe [S72][S96]. Trust center at trust.introw.io (content is JS-rendered; certification reports not retrievable publicly) [S74]. VENDOR, UNVERIFIED independently.
- SAML 2.0 and OIDC SSO for internal team and partner portal (paid add-on); portal SSO maps only the email claim and replaces OTP/social login; run Test login before enabling; allowed domains for internal SSO; Auth0 guide for partner SSO; Okta SSO/SCIM enabled after TLS requirement (Aug 2026) [S75][S107][S23].
- SCIM 2.0 for internal team only (Base URL + Bearer token); partner contacts come from CRM sync or SSO JIT [S76].
- Audit/governance: experience and asset version history, "every conversation is traced" for AI, AI actions logged to CRM timeline [S73][S93][S96].

---

## 5. Changelog (dated)

Sources: docs release notes (Jan to Sept 2026) and Intercom product updates (May 2024 to July 2026). Intercom "published" dates for older posts were bulk-reset to Feb 2026 in several cases; the month in the title is the feature month.

| Month | Highlights | Source |
|---|---|---|
| May 2024 | New layout, portal preview, breadcrumbs, new help center, single custom domain | [S127] |
| Aug 2024 | Deal registration from pipeline view; collaboration on form submissions | [S126] |
| Sep 2024 | Partnership performance dashboard; partner detail upgrade; Slack integration | [S125] |
| Oct 2024 | Announcements; portal branding; custom domain linking (Pro); notification defaults; attachments sync to HubSpot; deal name config | [S124] |
| Nov 2024 (pub. 17 Dec 2024) | Partner tiers; partner notes; commission automation; Crossbeam integration | [S123] |
| Dec 2024 | HubSpot Certified App | [S147] |
| Jan 2025 (pub. 6 Feb 2025) | Content engagement tracking; role-based partner access per tab; Partner Asset Hub | [S122] |
| Jan 2025 | Crossbeam integration blog (7 Jan 2025) | [S49] |
| Mar 2025 (pub. 2 Apr 2025) | SAML SSO internal and partner; co-branded assets; Power BI embed | [S121] |
| Apr/May 2025 | RBAC; Introw Embed; AI Agent (24/7 support); new navigation and branding | [S120] |
| Jun 2025 | Agentic channel conflict resolution; watched-property partner notifications; email engagement tracking; HubSpot workflow action (create partner); meeting scheduler; HubSpot timeline events; Notion embeds | [S119] |
| Jul 2025 (pub. 30 Jul 2025) | Actionable tasks; CTA section; multi-tier programs; CRM property display; partner role sync | [S118] |
| Aug 2025 (pub. 2 Sep 2025) | New HubSpot Collaboration card replacing Copilot card; collaborator restriction permission; AI announcements; portal access sync from CRM; announcement layouts; AI record matching | [S117] |
| Oct 2025 | Introw AI (internal copilot); HubSpot app events; sleeping deal notifications; partner role attribution; reseller/distributor auto-linking; dynamic asset filters | [S116] |
| Nov 2025 | Partner detail view; saved views; configurable dashboard sections; AI agent MCP integrations; internal collaborator notifications; USD 3M raise | [S115][S4] |
| Dec 2025 (Nov deliveries) | Partner goals; training and certification with conversational AI quiz; dynamic partner links; goals in tiers; test announcements; multi-attribution on CRM deals | [S114] |
| Jan 2026 | Multi-currency; richer CPQ; CRM-driven audience filters; certificate custom backgrounds; OTP login; drag-reorder tabs | [S30] |
| Feb 2026 | AI deal coaching; task templates become Journeys; portal builder branding refresh; SCORM import; email insights; currency bulk update; direct invites | [S29] |
| Mar 2026 | Reports and dashboards fully live; multilingual portal; proactive deal coaching Slack nudges; course chapter duplication; asset locale variants; checkbox field; richer HubSpot cards | [S28] |
| Apr 2026 | Team/users page with granular permissions; scoped notifications; multilingual GA; performance for 100k+ records; asset versioning; MDF early access; safe bulk delete | [S27] |
| May 2026 | Saved filters become segments; affiliate programs; shared-deal collaboration (comments, mentions, tasks, field edits); visitor filters | [S26] |
| Jun 2026 | Segments replace contact roles; multi-person partner teams; public API v1; Stripe/Chargebee commissions; custom email domain (early access); WhatsApp; partner CRM connection visibility; AI document translation; archiving; sync resilience | [S25] |
| Jul 2026 (update pub. 9 Jul 2026) | Partner Connect in partners' own CRMs and AI tools; rebuilt join flow; AI certificates; unified MDF intake; Form Submission API; Comments API; inline CRM editing; internal comments; picklist sync with hiding; partner-named quotes; custom discount method; consent-aware email tracking (FR, IT); chart drilldowns; zero-retention AI enforcement; Salesforce AccountId attribution; Slack AI agent; billing-based commissions; dynamic segments | [S24][S113] |
| Aug 2026 | Workflows canvas; conditional form fields and deal actions; segment defaults/overrides; persisted segments; per-platform chat; CRM-backed MDF; affiliate link auto-provisioning; CRM connection identity; Salesforce permission limitations; free API credits on all plans; form video embeds; AI images everywhere; table reports; partner account field aggregation; conflict detection in notifications; Claude/ChatGPT directory one-click; Teams self-serve; many fixes | [S23] |
| Sep 2026 | Introw Pay (bank + PayPal); file-based commission plans; rebuilt statements; commission columns; Payout setup section; commission API expansion; workflow variables; update contact properties step; announcement categories; Salesforce Collaboration Panel (IntrowPRM 1.15.0); property visibility conditions; bulk deal updates (100); tab groups and URL tabs; any CRM object as section; approval gate modes (Manual, AI Assisted, Autonomous); Teams bot; bulk team invites; English (UK); Crossbeam requires no partner mapping | [S22] |

Roadmap directions (no dates) [S31]: autonomous partner onboarding; end-to-end payment automation; workflow automation across steps; HubSpot/Salesforce parity; scalable governance for tens of thousands of partners; dynamic enablement delivered in partners' tools.

---

## 6. Crossbeam and Introw

- Relationship: complementary. "Crossbeam determines who to work with; Introw handles how you work with them (registration, enablement, payouts)" [S45]. Introw's PRM listicle frames Crossbeam as account mapping, "not a standalone PRM", lacking deal registration [S149] (VENDOR).
- Integration launched Nov/Dec 2024 (product update) and announced 7 Jan 2025 [S123][S49].
- Data flow: one-way read, Crossbeam to Introw; shared account and prospect overlaps for accounts your team works in Introw [S45].
- Where it shows: Crossbeam section in deal details on pipeline views; overlap flags on pending form submissions (checked against customers, prospects, open opportunities); partner overview shows which Crossbeam partners map to Introw partners; integration page shows Crossbeam plan tier and record export usage (bar turns orange then red, days to term reset) [S48][S46].
- Setup: Settings > Integrations > Crossbeam > Connect > authorize with Crossbeam admin > map Crossbeam partners to Introw partners with pickers (auto-saves) [S46]. Sept 2026: "Crossbeam requires no partner mapping" [S22] (mapping may now be automatic; UNVERIFIED).
- Requirements (CONFLICT across sources): Introw side needs the Crossbeam add-on/module [S45][S46]; pricing page places Crossbeam on Scale and Enterprise, excluded on Starter and Pro [S2]. Crossbeam side: "a Crossbeam plan that permits record exports" [S45] vs "Crossbeam Supernode plan (minimum tier)" [S48]. Consumes Crossbeam record export allowance [S45][S46].
- Marketing claims: 1-click setup (~1 minute), auto-attribution of deals sourced from overlap data, conflict avoidance, Slack/email updates [S14][S49]. VENDOR.
- Agentic: "Crossbeam Co-Sell Partner Finder" skill combines Crossbeam MCP overlaps (customer, opportunity, champion, lapsed) with Introw MCP partner performance signals to score and pick top 1 to 3 partners per target account, draft messages and pre-filled registration payloads, and queue tasks for human approval [S47].
- Co-sell setup track places "Discover account overlap: connect Crossbeam" as step 4 (1 to 2 hours, Partner Ops + RevOps) [S97].
- Advisory implication (analysis, not a source fact): Introw does not replace Crossbeam account mapping, and its Crossbeam read is limited to overlap signals for records worked in Introw; Crossbeam remains the data layer, Introw the workflow/portal layer.

---

## 7. Third-party reviews and comparisons

### 7.1 Ratings snapshot
| Site | Rating | Reviews | Notes | Source |
|---|---|---|---|---|
| G2 | 4.8/5 | 98 | Pros: ease of use (22), CRM integration (18), support (17), fast setup (17), HubSpot integration (15). Cons: minor malfunctions/limited custom reporting (4), missing features (4), CRM data quality issues (2), "requires a lot of clicks" (Sept 2026) | [S136] |
| G2 alternatives page | Introw leads PartnerStack on usability 9.5 vs 9.2 and support 9.9 vs 9.1; listed alternatives Impartner, PartnerStack, ZINFI, Channelscaler, impact.com, Salesforce Partner Cloud, Unifyr, Xoxoday, Benepik, Crossbeam | | [S137] |
| HubSpot Marketplace | 4.9/5 | 80 | 500+ installs | [S139] |
| AppExchange | 5.0/5 | 10 | | [S140] |
| AWS Marketplace | 4.8/5 | 93 | Likely syndicated G2 reviews (UNVERIFIED) | [S141] |
| Capterra | 5.0/5 | 2 | Con: wants Attio/Folk CRM support | [S138] |
| ZINFI (citing G2) | 4.8, 95 reviews, NPS 94, 0.6 months to go live, 76% partner adoption, 5-month ROI payback | | COMPETITOR citing G2 | [S144] |

### 7.2 Comparisons (labelled)
- Introw compare hub lists Impartner, Kiflo, PartnerStack, Euler, Salesforce Partner Cloud, ChannelScaler, Mindmatrix, ZINFI, Magentrix, Channeltivity, Partner.io, Suger, Unifyr, all "Comparison Coming Soon" [S145].
- Introw on PartnerStack (VENDOR): CRM disconnect, requires portal logins, limited customization; Introw pitches CRM-native co-selling for B2B vs PartnerStack's affiliate/referral strength [S151][S149].
- Introw on Euler (VENDOR): no custom objects, no white-label portal, generic onboarding, no LMS or MDF, AI advises but does not act, portal-centric; Introw claims 2 to 4 day implementation [S150].
- Introw on Impartner, ZINFI, Magentrix, Mindmatrix, Channeltivity, ChannelScaler, Salesforce PRM (VENDOR): portal-heavy, complex, slower; Introw = CRM-first, off-portal, AI-integrated [S149].
- Introw on Kiflo (VENDOR): lightweight entry-level, scalability ceiling [S149].
- Introw on Crossbeam (VENDOR): account mapping, not PRM [S149].
- ZINFI on Introw (COMPETITOR): strengths fast deploy, high adoption, CRM-native, SCORM + Articulate Rise import; weaknesses: no TCMA, MDF, rebates, community, marketplace, mobile app; cannot run standalone without HubSpot/Salesforce; founded 2023; teams outgrow it for co-branded marketing, MDF, tiered reseller/distributor, enterprise scale [S144]. Several of these (MDF, co-branded assets, mobile PWA, TCMA kits, multi-tier) are now documented by Introw [S66][S123][S110][S17], so this page appears outdated.
- PartnerPortal.io on Introw (COMPETITOR): "AI-native, headless PRM", mid-to-upper market, quote-based pricing, not for tiny budgets or deep TCMA/global governance [S142].
- Forecastable (third party, Alex's company): "Full-suite PRM, AI-first", "cleanest partner experience and fast setup", belongs on every PRM shortlist alongside Euler [S155].
- Growann (third party review site): real CRM sync, go-live under a week for 500 to 600 partners; cons: not a marketplace, payouts separate (now outdated), few integrations beyond HubSpot/Salesforce/Crossbeam [S143].
- Not found in public sources: direct Introw comparisons by Allbound, Channext, Partnerize, Reveal. UNVERIFIED / no data.

---

## 8. Known limitations, gotchas, FAQs (admin checklist)

1. One CRM per organisation; HubSpot and Salesforce are first-class, Pipedrive thinner [S38][S13].
2. Pro plan excludes Salesforce and Crossbeam; Crossbeam needs Scale+ or add-on and a Crossbeam tier with record exports (possibly Supernode) [S2][S45][S48].
3. HubSpot: every scope must be accepted; association-label attribution needs Pro/Enterprise and a Super Admin; custom object attribution needs Enterprise [S33][S34].
4. Salesforce: install/allow the connected app before authorizing (Sept 2025 Salesforce change); use a dedicated integration user; Introw inherits its FLS/sharing; place the Lightning component manually; some features lag HubSpot (visibility conditions in embed, Partner Connect deal linking) [S37][S22][S82].
5. Partner attribution must be configured before shared pipelines, deal registration attribution, commissions and reports work [S50][S52].
6. Portal meter is consumed on first publish of an experience to a partner, not by adding partners [S21].
7. Accepted submissions are final; fix in CRM and return/resubmit instead [S55].
8. Inbox select-all selects only loaded rows [S55].
9. Form conditional visibility is not a security control [S23].
10. Website form embeds need a custom domain [S131].
11. Portal SSO replaces all other partner login methods; test before enabling; SCIM covers internal users only [S75][S76].
12. Free email domains cannot grant domain-based portal access [S58].
13. Form submissions no longer auto-grant portal access (Aug 2026); configure the "Partner automation" invite setting [S23].
14. Segment overrides: most permissive wins; a no-condition dynamic segment cannot be an override [S56].
15. No email alert on broken CRM connection; monitor Integrations status [S40].
16. A CRM edit by your team is visible to a partner within about a minute (no quiet-edit window) [S38].
17. Workflows: 180-day max delay, 10 runs per partner per workflow per hour, no merge node; rollout gated per org [S84].
18. API: 120 req/min, monthly credit cap returns 402 (do not retry); MCP calls free [S87][S88].
19. No outbound webhooks yet; the in-app Webhooks tab says "Coming soon" [L1].
20. Partner Connect: deal linking only for partners on HubSpot; Salesforce partners register instead; partner-to-vendor updates are action-driven, no background polling [S82].
21. WhatsApp: inbound-first, Introw-owned number, exact phone match required [S80].
22. Introw Pay: company currency must be EUR or USD; bank KYC up to 7 days; PayPal covers countries without bank transfer (Brazil, China, India) [S63].
23. Consent-aware email tracking automatically disables tracking for FR and IT recipients using CRM country; accurate country data needed [S24].
24. Email delivery: allowlist `ecosystem@mail.introw.io` and `mail.introw.io`, or set up a custom email domain with DKIM + return-path CNAME [S86][S78].
25. Help center and docs can disagree (e.g., CRM User scope, free-plan goals); prefer docs.introw.io and release notes [S100][S41][S2][S20].
26. Hyperscaler partner type: docs claim Introw "syncs ACE opportunities and marketplace deals into your CRM" [S98], but no AWS/Azure/GCP integration page exists in the integration index [S10][S18]. UNVERIFIED.

---

## 9. Content, media and thought leaders

- Blog: very high publishing cadence since late 2025 (often daily in Aug/Sept 2026), heavily SEO/"best X alternatives" listicles plus guides on channel conflict, referral programs, MDF, SPIFFs, attribution, headless partnerships, MCP skills. Full titles and dates are in [S146][S147]. Selected: "Headless Partnerships" (23 Jul 2026), "MCP for Partnerships: 31 Claude skills" (21 Jul 2026), "Partner Attribution" (19 Jul 2026), "Ecosystem Led Growth" (15 Sep 2026), "Through-Channel Marketing Automation" (16 Sep 2026), "PRM vs CRM" (19 Aug 2026), "The 4 ways to manage your B2B partners in Salesforce and attribute revenue" (30 Apr 2025), "The 3 ways to manage your partners in HubSpot and attribute revenue" (3 Jun 2024), "Partner Deals Have a 32% bigger deal size and 2.8X higher win rate" (14 Jan 2024) [S146][S147].
- Resources hub also includes events, templates (e.g., channel partner profile template), whitepapers, glossary, video library [S1].
- Video library series "Partner Plays" and "Partner with AI" (short 1 to 2 minute clips, Jul to Dec 2025) with guests Eva Fayemi (Bond Agency), Tim Cleary (Coder), Phil Laslett (Move Forward Consulting), Alex Richards (Connected Revenue), Maxime Imbert, Franz-Josef Schrepf (OpusClip), KaraLynn Lewis (Partnership Advisory), Eleanor Thompson (Branchworks), Rob Moyer (Gong), Will Taylor (AudienceLed), Graham Collins (QuotaPath), J. Johnson [S152].
- YouTube channel: youtube.com/channel/UC6efoTpk_pJZLWPx7PV6CeQ (found via search; not crawled) [S153].
- LinkedIn: company page linkedin.com/company/introw; CEO Andreas Geamanu posts on partnerships and product launches (e.g., AI partner support agent launch) [S154][S112]. LinkedIn pages were not fetchable (robots).
- Blog guest content: "A Masterclass in Modern B2B SaaS Partnerships: Martin Scholz" (26 Jan 2026) [S146].
- No podcast or recurring webinar series found in public sources (UNVERIFIED).

---

## 10. Help center and docs article inventory

### 10.1 support.introw.io collections (Intercom) [S15]
Getting Started (9), Connect your CRM (29), Partner Connect (7), Build Your Partner Portal (24), Manage Partners (19), Partner Program Modules (76), Introw AI (20), Integrations and API (10), Account and Settings (16), For Partners (3), Product Updates (21).

Articles enumerated (title: URL). Articles marked * were opened and summarized above; the rest were enumerated only.

Getting Started [S111]
- How to set up a partner application form: https://support.introw.io/en/articles/14112879-how-to-set-up-a-partner-application-form
- Add your team to Introw: https://support.introw.io/en/articles/10373313-add-your-team-to-introw
- How to create a partner portal: https://support.introw.io/en/articles/9357238-how-to-create-a-partner-portal
- How to launch a partner portal: https://support.introw.io/en/articles/9357441-how-to-launch-a-partner-portal
- How to preview a partner portal?: https://support.introw.io/en/articles/9368411-how-to-preview-a-partner-portal
- Partner detail: https://support.introw.io/en/articles/12622728-partner-detail
- Connect your CRM: https://support.introw.io/en/articles/11970521-connect-your-crm
- How Introw keeps your CRM clean*: https://support.introw.io/en/articles/13772924-how-introw-keeps-your-crm-clean
- How partner deal data syncs to your CRM*: https://support.introw.io/en/articles/9399679-how-partner-deal-data-syncs-to-your-crm

Connect your CRM: Salesforce [S112]
- https://support.introw.io/en/articles/10087572-connecting-salesforce-to-introw
- https://support.introw.io/en/articles/10766417-use-a-picklist-in-salesforce-to-attribute-partnership-revenue
- https://support.introw.io/en/articles/10757124-use-a-relation-lookup-field-in-salesforce-to-attribute-partnership-revenue
- https://support.introw.io/en/articles/10757123-use-a-relation-table-in-salesforce-to-attribute-partnership-revenue
- https://support.introw.io/en/articles/10769562-use-a-custom-object-in-salesforce-to-attribute-partnership-revenue
- https://support.introw.io/en/articles/10102826-link-your-salesforce-opportunities-to-introw-via-custom-fields
- https://support.introw.io/en/articles/10104772-link-your-salesforce-opportunities-to-introw-via-a-relation-table
- https://support.introw.io/en/articles/12233044-opportunity-registration-with-introw-and-salesforce
- https://support.introw.io/en/articles/12233861-salesforce-integration-overview
- https://support.introw.io/en/articles/14689114-how-to-use-introw-forms-with-salesforce

Connect your CRM: HubSpot [S112]
- https://support.introw.io/en/articles/15646259-hubspot-integration-overview
- https://support.introw.io/en/articles/9353646-connecting-hubspot-to-introw
- https://support.introw.io/en/articles/9361206-link-your-hubspot-deals-to-introw-via-custom-properties*
- https://support.introw.io/en/articles/9479462-link-your-hubspot-deals-to-introw-via-company-associations*
- https://support.introw.io/en/articles/9529396-link-your-hubspot-deals-to-introw-via-custom-objects
- https://support.introw.io/en/articles/9600440-show-the-introw-card-inside-hubspot
- https://support.introw.io/en/articles/9367758-troubleshoot-hubspot-connection
- https://support.introw.io/en/articles/9882392-create-partner-portal-from-within-hubspot
- https://support.introw.io/en/articles/9939345-allow-partners-to-add-attachments-in-hubspot
- https://support.introw.io/en/articles/10175087-collaborate-from-inside-your-hubspot-deals
- https://support.introw.io/en/articles/10285312-how-to-disconnect-hubspot
- https://support.introw.io/en/articles/9439622-how-to-create-a-workflow-in-hubspot-based-on-the-leads-created-via-introw
- https://support.introw.io/en/articles/10546603-link-partners-to-leads-in-hubspot
- https://support.introw.io/en/articles/11537402-introw-workflow-actions-in-hubspot
- https://support.introw.io/en/articles/11553678-partner-activity-events-in-your-hubspot-timeline
- https://support.introw.io/en/articles/12499910-automating-workflow-actions-in-hubspot-using-introw-app-events
- https://support.introw.io/en/articles/13430413-introw-cpq
- https://support.introw.io/en/articles/14689113-how-to-use-introw-forms-with-hubspot
- https://support.introw.io/en/articles/9357064-how-to-attribute-revenue-to-partners-in-hubspot

Partner Connect [S109]
- What is Partner Connect?: https://support.introw.io/en/articles/15763666-what-is-partner-connect
- Partner MCP: https://support.introw.io/en/articles/15374091-give-your-partners-their-own-ai-assistant-to-collaborate-in-real-time-via-introw-s-partner-mcp
- https://support.introw.io/en/articles/15039830-partner-connect-a-2-way-crm-integration-with-hubspot
- https://support.introw.io/en/articles/15039839-set-up-the-partner-connect-card-in-hubspot
- https://support.introw.io/en/articles/15039840-validate-your-partner-connect-card
- https://support.introw.io/en/articles/15039841-link-an-existing-hubspot-deal-to-your-vendor
- https://support.introw.io/en/articles/15039842-register-a-new-deal-from-your-hubspot

Build Your Partner Portal [S103]
- https://support.introw.io/en/articles/9361984-best-practices-for-a-good-partner-experience
- https://support.introw.io/en/articles/9399620-launch-your-partner-portal
- https://support.introw.io/en/articles/9358660-how-to-create-a-partner-portal-experience
- https://support.introw.io/en/articles/10562182-create-a-partner-portal-experience
- https://support.introw.io/en/articles/10616459-unlink-or-update-an-experience-of-your-partner-portal
- https://support.introw.io/en/articles/13367569-create-and-manage-pipeline-views-in-the-portal-experience-builder
- https://support.introw.io/en/articles/15924171-why-my-embedded-website-shows-up-blank-in-introw
- https://support.introw.io/en/articles/9361509-how-to-manage-sections
- https://support.introw.io/en/articles/9367912-what-are-synced-sections
- https://support.introw.io/en/articles/11711503-call-to-action-buttons
- https://support.introw.io/en/articles/9362193-what-are-rich-sections
- https://support.introw.io/en/articles/13212973-partner-profile-section
- https://support.introw.io/en/articles/11702747-add-a-news-or-social-widget-to-your-partner-portal
- https://support.introw.io/en/articles/11579596-embed-notion-into-introw
- https://support.introw.io/en/articles/10419542-embed-your-google-appointment-scheduler
- https://support.introw.io/en/articles/10115469-brand-your-introw-partner-portal
- https://support.introw.io/en/articles/14618143-multi-language-support
- https://support.introw.io/en/articles/9556236-how-to-personalize-your-partner-portal
- https://support.introw.io/en/articles/10192327-multiple-partner-portal-access
- https://support.introw.io/en/articles/11848308-partner-notifications
- https://support.introw.io/en/articles/10392711-segment-based-access-control
- https://support.introw.io/en/articles/10561979-partner-portal-login
- https://support.introw.io/en/articles/9669389-email-verification
- https://support.introw.io/en/articles/10256349-embed-your-google-calendar-in-introw

Manage Partners [S104]
- https://support.introw.io/en/articles/10221007-partner-tiers
- https://support.introw.io/en/articles/10220987-partner-notes
- https://support.introw.io/en/articles/11662106-introw-home-page
- https://support.introw.io/en/articles/11895888-managing-partner-contacts
- https://support.introw.io/en/articles/11960140-invite-and-manage-partner-portal-users-as-a-partner
- https://support.introw.io/en/articles/11960790-deal-visibility-restrictions-for-partner-contacts
- https://support.introw.io/en/articles/11969738-task-templates
- https://support.introw.io/en/articles/11105067-how-to-invite-partners-to-your-portal-via-introw
- https://support.introw.io/en/articles/12919444-create-dynamic-partner-conversion-links
- https://support.introw.io/en/articles/12982099-create-and-configure-partner-goals
- https://support.introw.io/en/articles/14189246-segment-use-cases
- https://support.introw.io/en/articles/15359478-build-a-partner-directory-powered-by-introw
- https://support.introw.io/en/articles/15596033-the-introw-powered-pam-a-day-in-the-life
- https://support.introw.io/en/articles/10373923-add-your-partners-to-introw
- https://support.introw.io/en/articles/10660509-create-new-partners-via-introw
- https://support.introw.io/en/articles/11892742-assign-partner-managers
- https://support.introw.io/en/articles/15517779-partner-team-roles
- https://support.introw.io/en/articles/13444340-create-and-manage-views-in-the-deal-overview
- https://support.introw.io/en/articles/12634126-create-and-manage-views-in-the-partner-overview

Partner Program Modules (76) [S102]
- Forms: 11092789 how-to-use-introw-forms; 14780170 ai-assisted-form-approvals; 10200408 configure-the-deal-owner-of-your-partner-deals; 9939540 configure-the-deal-name-of-your-partner-deals; 9399649 how-to-manage-form-submissions; 11130706 embed-introw-forms*; 13293870 automatically-attribute-resellers-and-distributors-in-two-tier-channel-deals; 13726825 introw-forms-are-protected-from-spam*; 14006567 multi-upload-bulk-submit-records-via-a-form; 14048936 linking-deals-to-leads-via-introw
- Partner Deals: 9362774 how-to-setup-shared-sales-pipelines; 10353727 configure-which-deal-properties-to-share-with-your-partner; 9826343 collaborate-on-a-deal-or-any-other-crm-object; 12313505 keep-deals-moving-with-automatic-partner-notifications; 12430543 use-collaborators-to-ensure-partners-stay-updated-on-the-right-deals; 12538260 tracking-partner-involvement-on-deals*; 13431965 allow-partners-to-create-quotes-cpq; 13431818 enable-quotes-line-items-in-your-shared-deal-pipeline; 14431991 ai-deal-coach
- Commissions: 15350559 commissions-in-introw-a-complete-walkthrough; 15422218 affiliate-link-management-in-introw; 15551911 introw-s-chargebee-integration; 15588760 introw-s-stripe-integration; 10270932 introw-s-commission-module; 10270915 show-commissions-to-your-partners
- MDF: 14047810 market-development-funds-mdf; 15308334 how-to-set-up-a-mdf-fund; 15308338 how-to-show-the-roi-of-a-mdf; 15308337 how-partners-request-mdf-funds-submit-claims-and-upload-invoices
- Training and Certification: 12976763 partner-training-courses; 15945898 scorm-files-introw-courses; 12976824 how-to-use-introw-s-course-builder; 12988061 course-settings; 12976845 how-to-create-a-partner-certificate; 12991031 partner-certificates; 12981492 enrolling-partners-into-courses; 12994618 using-the-ai-conversational-quiz; 13375419 show-introw-course-enrollments-and-certificates-in-hubspot; 14595957 show-introw-course-enrollments-and-certificates-in-salesforce; 14653179 using-file-uploads-to-verify-partner-expertise; 16412140 build-a-training-curriculum-with-sequential-courses
- Task Management: 10410373 embed-tasks-within-your-partner-experience; 15458290 build-a-mutual-action-plan-with-tasks; 10410224 introw-tasks; 10410246 partner-journeys; 11711321 add-or-delete-tasks; 11716026 task-actions
- Asset Management: 9414557 asset-library; 15068953 governance-and-versioning; 10391889 manage-your-assets-in-the-asset-library; 10401828 embed-your-asset-library-in-your-partner-experience; 12321740 share-assets-at-scale; 10391863 organising-assets; 10410484 partner-asset-hub; 10807750 creating-co-branded-assets; 10807736 how-to-share-co-branded-assets-with-partners; 14621002 managing-assets-in-multiple-languages
- Partner Performance: 12975803 partner-goals; 12982846 edit-the-goals-of-your-partner; 9689534 partner-performance-dashboard; 14011044 how-to-create-a-report; 14019994 how-to-create-a-dashboard; 14022987 how-to-embed-a-report-or-dashboard-in-your-partner-portal
- Partner Engagement: 10115215 announcements; 9436438 engage-your-partners-with-comments-and-activity; 10628194 how-to-share-a-lead-and-other-crm-objects-with-your-partner; 10762826 collaborate-from-inside-hubspot-tickets; 11383276 share-a-deal-to-partners-via-introw-s-app-card-in-hubspot; 11549276 partner-engagement-tracking; 11705562 partner-analytics; 12183151 off-portal-collaboration-in-introw; 12499113 partner-engagement-reporting-in-hubspot-with-introw-app-events; 13427907 monthly-partner-engagement-summary-email; 13600188 send-dedicated-partner-announcements; 14403496 auto-generated-partner-announcements-from-your-linkedin
- Standalone: 15799134 how-introw-solves-tcma-for-vendors
(URL pattern: https://support.introw.io/en/articles/{id}-{slug})

Introw AI [S105]
- 11558434 ai-agent-security-at-introw; 15970623 using-introw-with-chatgpt; 15598653 the-introw-powered-partner-a-day-in-the-life; 11107074 introw-agent; 15590009 using-introw-with-gemini-via-mcp; 13892885 save-time-with-introw-s-ai-agent; 14498766 ai-course-builder-and-live-tutor; 15293107 let-claude-manage-your-partners-agentic-partner-updates-via-introw; 14498771 ai-channel-conflict-resolution; 14498787 ai-deal-coaching-an-expert-sales-coach-in-every-partner-deal; 14498781 connect-introw-ai-to-notion-lovable-openclaw-and-beyond; 14498758 ai-agents-that-actually-take-action-for-your-partners; 14494687 introw-s-ai-agent-in-slack; 11579537 ai-detected-channel-conflict-resolution; 12182958 using-your-mcp-server-with-introw-s-ai-agent; 12381063 using-introw-ai-across-your-partners; 14034406 install-the-claude-connector-of-introw; 14044252 introw-claude-use-cases-what-s-possible; 15392372 introw-s-submission-agent-is-now-fully-autonomous; 15392105 customer-deep-dive-how-quatt-powers-installer-operations-with-the-introw-mcp

Integrations and API [S106]
- 9911638 how-does-the-integration-with-slack-work; 15054557 how-does-the-integration-with-microsoft-teams-work; 15054592 microsoft-teams-link-private-and-shared-channels; 9449132 slack-link-private-channels; 10227780 integrating-introw-with-crossbeam*; 10839375 introw-s-zapier-integration; 10809685 embed-your-power-bi-reports; 12034448 link-introw-to-power-bi; 11122927 embed-introw-in-your-product; 15386268 the-introw-api-connect-your-partner-program-to-the-rest-of-your-stack

Account and Settings [S107]
- 9460002 best-practices-to-activate-your-partners-via-introw; 13385268 what-does-no-portal-yet-and-no-deal-embed-yet-mean; 13701950 multi-tenant-access*; 15443507 how-to-setup-your-affiliate-link-tracking; 11136281 roles-and-permissions*; 15586173 segments-in-introw; 12079274 crm-user*; 10740664 enable-single-sign-on-for-partners; 10820542 setup-single-sign-on-for-partners-sso-via-auth0; 10829581 enable-single-sign-on-for-your-team; 12549379 my-partner-does-not-receive-any-emails; 14616921 notification-settings; 10010261 link-your-custom-domain; 15701442 send-notifications-from-your-own-email-domain; 13702763 multi-currency-localise-the-partner-portal-experience; 13193635 how-to-set-a-fiscal-startdate

For Partners [S110]
- 15324870 introw-mobile-experience; 15324724 install-introw-on-your-mobile-home-screen; 15615361 everything-your-partners-can-do-in-introw

Product Updates [S108] (all opened except as noted)
- July 2026* 15885384; June 2026 15430997 (covered via docs release notes); 13 little tricks* 14635252; May 2026 15183455 (covered via docs); April 2026 14441504 (covered via docs); March 2026 14041018 (covered via docs); January 2026 13597835 (covered via docs); December 2025* 13035409; November 2025* 12752596; October 2025* 12534233; August 2025* 12142898; July 2025* 11868054; June 2025* 11594452; May 2025* 11170409; March 2025* 10854679; September 2024* 10023271; January 2025* 10516533; November 2024* 10295136; October 2024* 10114996; August 2024* 9883598; May 2024* 9440109

### 10.2 docs.introw.io structure
Full page index (516 product pages + release notes + API) is in [S16][S17][S18][S19]. Top-level: Get started (Explore, Start free, Welcome, Partner types, Days in the life x7, Setup tracks x6: affiliate, referral, co-sell, reseller, distributor, implementation), Headless (prompt library, 16 agentic use cases, 33 skills), Partner management (Partners: journeys, onboarding incl. agreements, partner management, segments, tasks, team, tiers; Automation: built-in, workflows; Forms: CRM automations, builder, sharing, approvals), Partner performance (report builder, dashboards, partner analytics, goals, Power BI), Deal registration and co-selling (deal/lead registration, shared pipelines, tasks, registration, channel conflict, reseller pipeline, multi-tier; CPQ: discounts, catalog, quotes), Partner engagement (announcements, channels, notifications), AI agents (Partner Connect: partner AI, communication tools, partner CRM; AI: partner support, copilot, deal coaching, channel conflict, approvals, security, training, announcements, knowledge base), Partner portal (branding, custom domains, email domain, experiences, mobile, directory, access), Enablement (asset hub, library, co-branded, synced sections, TCMA; courses: authoring, certificates, enrollments, progress, quizzes), Referrals/incentives/payouts (lead sharing, deal updates, rewards, commissions: lines, plans, payouts, Introw Pay, settings; MDF: funds, projects, claims, ROI, invoices; affiliate: campaigns, conversion tracking, fraud, links), Platform (integrations: CRM, chat, billing, Crossbeam, Zapier, MCP, API; localization; access and security: provisioning, SSO, team management; developer: embed, MCP), plus Why Introw pages, ROI page, AGENTS.md and openapi.json.

### 10.3 URLs that could not be fetched
- https://www.introw.io/about (404; correct page is /about-us, fetched)
- https://quotapath.introw.io/ (fetch permission not granted in time; existence of this portal UNVERIFIED)
- https://www.linkedin.com/products/introw-io/ (blocked by robots.txt)
- https://trust.introw.io (loaded, but certification details are JS-rendered and not retrievable)
- No support.introw.io or docs.introw.io page returned an error. Most individual support.introw.io articles were enumerated but not opened, because the docs.introw.io equivalents (newer) were read instead.

---

---

## 12. Observed in a live tenant (admin session, 2026-09-29) [L1]

Walked read-only in a customer's production Introw org (Pro plan) as an Admin user. Nothing was changed. Customer-specific data is deliberately left out of this file; only product behavior is recorded. Where this section and the docs disagree, this section is newer ground truth for the UI, the docs remain the reference for behavior.

### 12.1 Navigation map (vendor app, app.introw.io)
Left nav, top to bottom, with routes:

| Menu | Route | What it is |
|---|---|---|
| Home | `/` | "Your program, at a glance": Partners (created, last active), Revenue (total, weighted, top partners), Engagement (emails sent, most engaged partners); In the spotlight; Highlights (comments, due tasks, portal visits, won deals); Recent Activity; Support (live chat, docs) |
| Introw AI | `/agent` | Internal copilot chat with history; starter prompts QBR, Inactive Partners, Gold Partners |
| Partners | `/partners` | Table views (All Partners, My Partners, Archived, Add view); columns Account, Phase, Tier, Experience, Champion, Manager, Engagement (e.g. "Low, Inactive" or "Low, active last year"), Categories, Segments; "Partner onboarding on autopilot" banner; Create partner; link to the partner-facing portal URL |
| Opportunities | `/overview/DEAL` | Opportunity overview; tabs All Deals, Due Deals, Overdue Deals, Other; pipeline picker; partner filter; list or board; Share |
| Journeys | `/tasks` | Journeys and standalone tasks; templates Partner Onboarding, Partner Activation, Certification Journey; or from scratch |
| Assets | `/assets/library` | Active, Partner assets, Archived; columns Type (PDF Document, Calendly Embed, Fast Embed, other embeds), Languages, Views, Access (Portal), Categories |
| MDF | `/marketing-funds` | Upsell page when not on plan ("Upgrade plan") |
| Commission | `/commission` | Tabs Payouts, Commission Plans, Imports, Payout Settings; tiles Expected, Upcoming payouts, Total paid, Declined; Create payout |
| Affiliate | `/campaigns` | "Request access" gate when not enabled |
| CPQ | `/products` | Products and Quotes; per product: Visibility (e.g. "Available to all partners"), SKU, Unit price, Billing term, Segments, Deal filters (restrict to deals matching CRM deal properties), Discount method (No discount, Partner based, Tier based, Custom price, Custom discount) |
| Submissions | `/submissions` | Form submissions inbox; Pending, Accepted, Declined; status values include "Auto accepted" |
| Portal > Tiers | `/settings/tiers` | Tier Programs table (Title, Tiers, Partners, Requirements, Benefits); Create Program; Sync |
| Portal > Goals | `/settings/goals` | Create goal |
| Portal > Courses | `/courses` | Create course (AI quizzes, certification) |
| Portal > Certificates | `/certificates` | Create certificate |
| Portal > Forms | `/forms` | Forms list with submission counts; default forms seeded by Introw: Commission form, Become a partner form, Deal form; "Partner onboarding on autopilot" |
| Portal > Portal settings | `/settings/portal` | Opens the portal login preview |
| Portal > Experience builder | `/templates` | Experiences and Synced sections; status Published; Linked partners |
| Track > Reports | `/reports` | Saved reports (Bar, Line, Number); sources Partner, Email, Opportunity, Engagement; metrics Count, Sum, Average (Days to close, Amount), Compounded Count/Sum |
| Track > Dashboards | `/dashboards` | Named dashboards (can be per experience); Add dashboard; Edit dashboard; tiles default to All time or trailing 12 months |
| Engage > AI Agent | `/ai-agents/partner-support/history` | Partner Support AI Agent; "Install AI Agent" when not set up |
| Engage > Notifications | `/settings/notifications` | Partner Notifications report per event: Sent, Opened, Clicked, Bounced, Last sent, Amount of partners. Recipients are configured in Segments (`/settings/segments/default?tab=notifications`), not here. Event keys seen: OBJECT_UPDATE.DEAL, NEW_OBJECT.DEAL, COMMENT.DEAL, OBJECT_SLEEPING.DEAL, DEAL_CLOSED_WON.DEAL, plus Announcement, Comment, Comment mention, Form submission accepted/declined/returned, Task assigned/updated, Tasks nudge, Enroll in course, Give certificate |
| Engage > Deal Coaching | `/deal-coaching` | Create Deal Coach (flagged New) |
| Engage > Announcements | `/announcements` | Columns Status (AI Generated, Published), Sent, Opened, Bounced, Clicked, Categories, Experiences, Author, Publish date, Reach. Introw auto-generates draft announcements from the customer's recent content; they sit unpublished until someone publishes or deletes them |
| Settings > Team | `/settings/team` | Users, Roles, Partner team roles; Invite user; statuses Active, Invite sent |
| Settings > Segments | `/settings/segments` | All, Dynamic, Static, Archived; columns Type, Audience, Permissions, Notifications, Used in; "All partners" is the Default row |
| Settings > Integrations | `/settings/integrations` | Categories below |
| Settings > Company | `/settings/company` | General, Currencies, Billing info, Billing; logos (square 512x512, horizontal 800x200), name, domain, description (Generate with AI), currency, multi-currency toggle, timezone, language, fiscal year start |
| Settings > Languages | `/settings/languages` | Active portal locales; brand glossary and protected terms |
| Settings > Developers | `/settings/developers/*` | Tabs API Keys, Webhooks, Logs, Embed, Portal SSO, Internal SSO; API Credits meter (%); link to developers.introw.io |

Partner detail (`/partners/{id}`): tabs Overview, Analytics, People, Opportunities, Tasks, Notes, plus more; Overview cards Revenue (weighted), Engagement (most engaged contacts with action counts), Inactive or Overdue Opportunities, Won Opportunities, Tasks, Upcoming Meetings, Notes, Goals, Activity; right rail Partner Details (Tier, Phase, Champion, Partner since, Last activity, Language, Categories, Segments, Partner Connect status with "Not onboarded" and a Nudge partner action), Team, CRM fields panel ("View in Salesforce" or HubSpot), Portal Info (Access, e.g. Email domain; Experience; Commission plan), Chat (Private channel, Connect Microsoft Teams). Header actions View portal, Invite.

### 12.2 Integrations catalog as shown in the app
- CRM & Data: HubSpot, Salesforce, Crossbeam, Power BI, Looker (Looker is not in the public docs research; plan-gated).
- MCP: Claude (one click from Claude's connector directory), ChatGPT (from the ChatGPT app directory), generic MCP (Lovable, Notion, Langdock, Cursor, others).
- Billing: Chargebee, Stripe (plan-gated).
- Communication: Slack, Microsoft Teams, WhatsApp (via the customer's Twilio Business account per the tile; plan-gated), Zapier.
- Status pills seen: Connected, Not connected, Interrupted, Update available, Upgrade plan. A "Communication !" badge flags an integration needing action.
- Trust banner in-app: ISO 27001:2022 and SOC 2 Type 2, EU hosted.

### 12.3 Corrections to the public-doc picture
- Webhooks: the Developers area has a Webhooks tab marked "Coming soon". Outbound webhooks are planned, not live, as of 2026-09-29. This resolves the UNVERIFIED item in 4.14 and 8.19.
- Developers also has a Logs tab (API request logs) and an API Credits meter.
- Crossbeam on Pro: a Pro-plan org can hold a live Crossbeam connection (likely grandfathered from before the current price book, connection dated Dec 2024). Do not assume Pro means no Crossbeam; check the tile.
- The Crossbeam integration page shows: who connected it and when, the customer's Crossbeam plan (e.g. Enterprise), Record Export Usage as used / allowance with a percentage bar, days until reset, and the Crossbeam contract term; plus Disconnect and View in Crossbeam. This is the fastest place to see how much of a customer's Crossbeam record-export allowance is gone.
- Salesforce "Configure" on an Interrupted connection does not open a settings page; the fix is reconnect (three-dots menu) per the troubleshooting doc [S40].
- Opportunity overview loads deals from the connected CRM; with the CRM connection Interrupted, pipeline data in Introw is stale (it shows the last synced state and new CRM changes do not arrive).
- Announcements auto-drafted by AI are marked "AI Generated" with Author "Introw" and Reach pre-filled; they are never sent until published.

### 12.4 Admin health signals visible without any API (use these in audits)
1. Integrations tile status for the CRM (anything but Connected is a P1: pipeline, attribution, commissions and reports all depend on it).
2. Crossbeam tile: record export usage percentage versus days left in the term.
3. Slack or Teams "Update available".
4. Team: invites stuck in "Invite sent".
5. Partners table: share of partners with Engagement "Inactive", Tier blank, Experience "Upgrade plan" (no portal published), Manager blank.
6. Submissions: share "Auto accepted" (no human or AI review gate) and date of last submission.
7. Forms: seeded Introw default forms never customized (owner "Introw", 0 submissions).
8. Announcements: count of unpublished "AI Generated" drafts; date of last published announcement.
9. Goals, Courses, Certificates, Journeys, Deal Coaching, AI Agent pages showing the empty-state "Create" screen (module unused).
10. CPQ: test products or deep-discount products set "Available to all partners".
11. Partner detail: leads submitted but Revenue $0 and Opportunities 0 (attribution not closing the loop).
12. Partner detail: Partner Connect "Not onboarded".

---

## 11. Source list

- [S1] https://www.introw.io/
- [S2] https://www.introw.io/pricing
- [S3] https://www.introw.io/about-us
- [S4] https://www.introw.io/blog/introw-raises-3m-to-build-the-future-of-b2b-partnerships
- [S5] https://techfundingnews.com/introw-ai-partner-management-funding/
- [S6] https://www.introw.io/blog/introw-raises-eu1m-to-launch-digital-partnership-rooms
- [S7] https://www.introw.io/case-studies
- [S8] https://www.introw.io/case-studies/factorial
- [S9] https://www.introw.io/case-studies/how-quatt-built-an-agentic-partner-program-with-introw
- [S10] https://www.introw.io/integrations
- [S11] https://www.introw.io/integrations/hubspot
- [S12] https://www.introw.io/integrations/salesforce
- [S13] https://www.introw.io/integrations/pipedrive
- [S14] https://www.introw.io/integrations/crossbeam
- [S15] https://support.introw.io/en/
- [S16] https://docs.introw.io/llms.txt
- [S17] https://docs.introw.io/_llms/product.md
- [S18] https://docs.introw.io/_llms/product/platform.md
- [S19] https://docs.introw.io/_llms/product/referrals-incentives-and-payouts.md
- [S20] https://docs.introw.io/start-free.md
- [S21] https://docs.introw.io/features/access/team-management/guides/understand-your-plan-limits.md
- [S22] https://docs.introw.io/release-notes/2026-09.md
- [S23] https://docs.introw.io/release-notes/2026-08.md
- [S24] https://docs.introw.io/release-notes/2026-07.md
- [S25] https://docs.introw.io/release-notes/2026-06.md
- [S26] https://docs.introw.io/release-notes/2026-05.md
- [S27] https://docs.introw.io/release-notes/2026-04.md
- [S28] https://docs.introw.io/release-notes/2026-03.md
- [S29] https://docs.introw.io/release-notes/2026-02.md
- [S30] https://docs.introw.io/release-notes/2026-01.md
- [S31] https://docs.introw.io/whats-next.md
- [S32] https://docs.introw.io/features/integrations/crm/guides/connect-hubspot.md
- [S33] https://docs.introw.io/features/integrations/crm/guides/hubspot-permissions-and-scopes.md
- [S34] https://docs.introw.io/features/integrations/crm/guides/attribution-in-hubspot.md
- [S35] https://docs.introw.io/features/integrations/crm/guides/connect-salesforce.md
- [S36] https://docs.introw.io/features/integrations/crm/guides/attribution-in-salesforce.md
- [S37] https://docs.introw.io/features/integrations/crm/guides/salesforce-permissions-and-scopes.md
- [S38] https://docs.introw.io/features/integrations/crm/technical/index.md
- [S39] https://docs.introw.io/features/integrations/crm/guides/troubleshoot-a-crm-connection.md
- [S40] https://docs.introw.io/features/integrations/crm/guides/every-crm-error-introw-logs.md
- [S41] https://docs.introw.io/features/integrations/crm/guides/hubspot-crm-users-vs-admin-users.md
- [S42] https://docs.introw.io/features/integrations/crm/guides/set-up-the-hubspot-partner-connect-card.md
- [S43] https://docs.introw.io/features/integrations/crm/guides/use-introw-workflow-actions-in-hubspot.md
- [S44] https://docs.introw.io/features/integrations/crm/guides/report-on-partner-engagement-in-hubspot.md
- [S45] https://docs.introw.io/features/integrations/crossbeam/index.md
- [S46] https://docs.introw.io/features/integrations/crossbeam/guides/connect-crossbeam.md
- [S47] https://docs.introw.io/headless/skills/vendor/crossbeam-cosell-finder.md
- [S48] https://support.introw.io/en/articles/10227780-integrating-introw-with-crossbeam
- [S49] https://www.introw.io/blog/introw-prm-and-crossbeam-integration
- [S50] https://docs.introw.io/features/deal-registration/registration/technical/index.md
- [S51] https://docs.introw.io/features/deal-registration/channel-conflict/index.md
- [S52] https://docs.introw.io/features/co-selling/shared-pipelines/technical/index.md
- [S53] https://docs.introw.io/features/co-selling/shared-pipelines/guides/troubleshoot-deals-not-in-portal.md
- [S54] https://docs.introw.io/features/forms/crm-automations/technical/index.md
- [S55] https://docs.introw.io/features/forms/submissions-approvals/technical/index.md
- [S56] https://docs.introw.io/features/partners/segments/technical/index.md
- [S57] https://docs.introw.io/features/partners/tiers/technical/index.md
- [S58] https://docs.introw.io/features/portal/portal-access/guides/what-partners-can-see.md
- [S59] https://docs.introw.io/features/portal/portal-access/technical/index.md
- [S60] https://docs.introw.io/features/partners/partner-management/guides/detect-partners-from-your-crm.md
- [S61] https://docs.introw.io/features/commissions/commission-plans/technical/index.md
- [S62] https://docs.introw.io/features/commissions/payouts/technical/index.md
- [S63] https://docs.introw.io/features/commissions/introw-pay/technical/index.md
- [S64] https://docs.introw.io/features/referrals/rewards/technical/index.md
- [S65] https://docs.introw.io/features/referrals/lead-sharing/technical/index.md
- [S66] https://docs.introw.io/features/mdf/index.md
- [S67] https://docs.introw.io/features/affiliate/index.md
- [S68] https://docs.introw.io/features/affiliate/fraud-protection/technical/index.md
- [S69] https://docs.introw.io/features/affiliate/conversion-tracking/technical/index.md
- [S70] https://docs.introw.io/features/developer/mcp/technical/index.md
- [S71] https://docs.introw.io/features/developer/mcp/guides/connect-claude.md
- [S72] https://docs.introw.io/features/ai/security/index.md
- [S73] https://docs.introw.io/why/enterprise-grade.md
- [S74] https://trust.introw.io
- [S75] https://docs.introw.io/features/access/sso/technical/index.md
- [S76] https://docs.introw.io/features/access/provisioning/technical/index.md
- [S77] https://docs.introw.io/features/portal/custom-domains/technical/index.md
- [S78] https://docs.introw.io/features/portal/email-domain/technical/index.md
- [S79] https://docs.introw.io/features/integrations/chat/technical/index.md
- [S80] https://docs.introw.io/features/integrations/chat/guides/set-up-whatsapp.md
- [S81] https://docs.introw.io/features/integrations/zapier/technical/index.md
- [S82] https://docs.introw.io/features/partner-connect/partner-crm/technical/index.md
- [S83] https://docs.introw.io/features/automation/built-in-automation/guides/every-automation-that-runs-out-of-the-box.md
- [S84] https://docs.introw.io/features/automation/workflows/technical/index.md
- [S85] https://docs.introw.io/features/engagement/notifications/guides/every-notification-introw-sends.md
- [S86] https://docs.introw.io/features/engagement/channels/guides/troubleshoot-partner-email-delivery.md
- [S87] https://docs.introw.io/general/authentication.md
- [S88] https://docs.introw.io/general/api-credits.md
- [S89] https://docs.introw.io/openapi.json
- [S90] https://docs.introw.io/general/embed-overview.md
- [S91] https://docs.introw.io/features/ai/partner-support/technical/index.md
- [S92] https://docs.introw.io/features/ai/deal-coaching/technical/index.md
- [S93] https://docs.introw.io/features/ai/copilot/technical/index.md
- [S94] https://docs.introw.io/features/reporting/report-builder/technical/index.md
- [S95] https://docs.introw.io/features/courses/index.md
- [S96] https://docs.introw.io/headless/index.md
- [S97] https://docs.introw.io/tracks/co-sell.md
- [S98] https://docs.introw.io/partner-types.md
- [S99] https://support.introw.io/en/articles/11136281-roles-and-permissions
- [S100] https://support.introw.io/en/articles/12079274-crm-user
- [S101] https://support.introw.io/en/articles/14635252-13-little-introw-tricks-you-probably-didn-t-know-about
- [S102] https://support.introw.io/en/collections/19666606-partner-program-modules
- [S103] https://support.introw.io/en/collections/19666562-build-your-partner-portal
- [S104] https://support.introw.io/en/collections/11054343-manage-partners
- [S105] https://support.introw.io/en/collections/13351436-introw-ai
- [S106] https://support.introw.io/en/collections/9459545-integrations-api
- [S107] https://support.introw.io/en/collections/9546568-account-settings
- [S108] https://support.introw.io/en/collections/9540839-product-updates
- [S109] https://support.introw.io/en/collections/19650482-partner-connect
- [S110] https://support.introw.io/en/collections/19666565-for-partners
- [S111] https://support.introw.io/en/collections/14517212-getting-started
- [S112] https://support.introw.io/en/collections/19666559-connect-your-crm
- [S113] https://support.introw.io/en/articles/15885384-introw-product-update-july-2026
- [S114] https://support.introw.io/en/articles/13035409-introw-product-update-december-2025
- [S115] https://support.introw.io/en/articles/12752596-introw-product-update-november-2025
- [S116] https://support.introw.io/en/articles/12534233-introw-product-update-october-2025
- [S117] https://support.introw.io/en/articles/12142898-introw-product-update-august-2025
- [S118] https://support.introw.io/en/articles/11868054-introw-product-update-july-2025
- [S119] https://support.introw.io/en/articles/11594452-introw-product-update-june-2025
- [S120] https://support.introw.io/en/articles/11170409-introw-product-update-may-2025
- [S121] https://support.introw.io/en/articles/10854679-introw-product-update-march-2025
- [S122] https://support.introw.io/en/articles/10516533-introw-product-update-january-2025
- [S123] https://support.introw.io/en/articles/10295136-introw-product-update-november-2024
- [S124] https://support.introw.io/en/articles/10114996-introw-product-update-october-2024
- [S125] https://support.introw.io/en/articles/10023271-introw-product-update-september-2024
- [S126] https://support.introw.io/en/articles/9883598-introw-product-update-august-2024
- [S127] https://support.introw.io/en/articles/9440109-introw-product-update-may-2024
- [S128] https://support.introw.io/en/articles/9399679-how-partner-deal-data-syncs-to-your-crm
- [S129] https://support.introw.io/en/articles/13772924-how-introw-keeps-your-crm-clean
- [S130] https://support.introw.io/en/articles/13726825-introw-forms-are-protected-from-spam
- [S131] https://support.introw.io/en/articles/11130706-embed-introw-forms
- [S132] https://support.introw.io/en/articles/13701950-multi-tenant-access
- [S133] https://support.introw.io/en/articles/9361206-link-your-hubspot-deals-to-introw-via-custom-properties
- [S134] https://support.introw.io/en/articles/9479462-link-your-hubspot-deals-to-introw-via-company-associations
- [S135] https://support.introw.io/en/articles/12538260-tracking-partner-involvement-on-deals
- [S136] https://www.g2.com/products/introw/reviews
- [S137] https://www.g2.com/products/introw-prm/competitors/alternatives
- [S138] https://www.capterra.com/p/10021118/Introw/
- [S139] https://ecosystem.hubspot.com/marketplace/listing/introw
- [S140] https://appexchange.salesforce.com/appxListingDetail?listingId=54d27313-9aa0-4e9f-9ec6-3f9dae7a6a6e
- [S141] https://aws.amazon.com/marketplace/pp/prodview-6nmuuuotww36o
- [S142] https://www.partnerportal.io/introw-vs-partnerportal
- [S143] https://www.growann.com/review/introw
- [S144] https://www.zinfi.com/compare/introw-alternatives/
- [S145] https://www.introw.io/compare
- [S146] https://www.introw.io/blog
- [S147] https://www.introw.io/blog?b8c509f9_page=2
- [S148] https://www.introw.io/blog/partner-attribution
- [S149] https://www.introw.io/blog/best-partner-relationship-management-software
- [S150] https://www.introw.io/blog/best-euler-prm-alternatives
- [S151] https://www.introw.io/blog/best-partnerstack-alternatives
- [S152] https://www.introw.io/video-library
- [S153] https://www.youtube.com/channel/UC6efoTpk_pJZLWPx7PV6CeQ (search result only)
- [S154] https://www.linkedin.com/in/andreas-geamanu/ (search result only)
- [S155] https://forecastable.com/partnerstack-alternatives/
- [S156] https://www.quotapath.com/partners/
- [L1] Live admin walk-through of a customer Introw org (Pro plan), app.introw.io, 2026-09-29, read-only.
