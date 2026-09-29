# Glean Intelligence: administration and use

Version: 2026.09 (built 2026-09-26). Next refresh: first week of 2026-10.
Owner: Forecastable. Maintained by the monthly `glean-intelligence-refresh` scheduled task.

How to read this file:

- Every fact carries a source tag like `[D23]`. The Sources table at the bottom maps tags to URLs.
- Source bias labels: **VENDOR** (Glean wrote or commissioned it), **PARTNER** (a Glean services or
  technology partner), **INDEPENDENT** (analyst, press, review site), **COMPETITOR** (sells against Glean).
  Weight claims accordingly. Benchmarks marked VENDOR are Glean's own and have not been reproduced.
- Glean ships monthly. Anything tied to a setting name, menu path, model name, price or limit is true
  as of the version date above. Before telling someone a setting exists in *their* tenant, say which
  deployment-date rules apply (see 1.3) and tell them to confirm in their Admin Console.
- Items we could not verify are listed in section 22. Never state them as fact.

---

## 0. The twelve things that matter most

1. **Glean is an identity, permissions, data-quality and change program that happens to install fast.**
   Technology is rarely the hard part; permissions, outcomes, governance, adoption, connectivity and
   cost are [P1] [V13]. Standard deployment is about 1 to 3 weeks to first use; large orgs budget 3 to
   4+ weeks because content sync dominates [D1]. "Indexed" and "adopted" are different finish lines:
   partners quote 4 to 8 weeks to value and a 12-week onboarding package [P3] [P1].
2. **Glean exposes bad permissions, it does not fix them.** Permission-aware retrieval faithfully
   surfaces over-shared source content. Glean's own first "leak" (Rubrik, around 2020) was an
   over-provisioned source document, not a Glean bug [V12]. Alchemy has found hidden SharePoint
   subfolders with salary and termination data, and managers who still held a departed employee's
   mailbox [P1] [V13]. Run a permission hygiene campaign before broad rollout (section 7).
3. **Do not let users in until ML training finishes.** Crawl and index take 2 to 3 days (small) to
   10 to 14 days (large); ML adds 2 to 14 more and cannot start until every Phase 1 connector is
   indexed. Launch early and spellcheck, autocomplete, acronyms and Assistant quality all degrade
   [D4]. Connect 4 to 6 mission-critical apps first, not everything [D2].
4. **"Crawl finished" is not "ready."** Validate people data, connector health, item counts,
   freshness, visibility and source permissions with a test group before go-live [D19] [D32].
5. **Indexed content and live tools are separate control surfaces.** Connectors crawl content plus
   ACLs into the index; tools call apps live and may write. Treat retrieval permissions and action
   permissions separately; write scopes must be narrower than read scopes [D18] [D47].
6. **Glean does knowledge; warehouses and CRMs do numbers.** Route "forecast revenue" or "churn by
   cohort" to a governed system (Databricks Genie, Snowflake, SOQL tools), not to an LLM reading
   documents [P3] [A6] [D39].
7. **Salesforce field-level security is NOT enforced by the connector.** Any indexed field on a
   visible record can appear in snippets and AI answers. Red-list sensitive fields (margins, partner <!-- VALIDATE-OK[economics]: names customer CRM fields to red-list in Glean, not Forecastable economics -->
   economics, compensation) [D23].
8. **Restrict building, open using.** Ashisuto: about 15% builders, 85% users; build rights through
   per-division Knowledge Managers; "strong governance for creators, wide openness for users" [P9].
   Alchemy: designated builders, an approval step, publish centrally [V13].
9. **Cost is now an operating expense, not a feature.** Enterprise Flex meters Thinking and premium
   queries, agent runs, Deep Research, slides and API/MCP use in FlexCredits. Set org, department,
   user and agent limits plus alerts at launch, disable or hide premium models by default, and name a
   spend owner [D66] [D67] [P2].
10. **The browser extension is the single biggest adoption lever.** Access only via app.glean.com or
    an SSO tile leads to poor adoption [D8]. Launch around concrete jobs ("before your customer
    meeting, ask Glean for open tickets, the latest Slack escalation and contract terms"), not "AI".
11. **Measure in four layers:** platform health, adoption, quality, business outcomes (section 15).
    Segment by department; a company average hides a great engineering rollout and a failed sales one
    [D75].
12. **Glean is becoming a context layer beneath other AI front doors.** 78% of customers access Glean
    through APIs and MCP (Glean:GO 2026) [V1]. Claude, ChatGPT, Copilot and Cursor can use Glean as
    governed context via Glean's remote MCP server [D53]. Plan for Glean both as a destination and as
    plumbing.

---

## 1. Mental model and architecture

### 1.1 The logical architecture

```
Systems of record (M365, Google Drive, Slack, Jira, Salesforce, HubSpot, Gong, GitHub, ServiceNow, custom)
        |  native / partner / custom connectors: content + metadata + ACLs + activity
        v
Glean context layer: index + ranking + Enterprise Graph (people, teams, customers, projects) + permission filtering
        |                 |                  |                      |
      Search          Assistant           Agents          Glean MCP server / APIs  --> Claude, ChatGPT, Copilot, Cursor
                                            |
                              live tools / MCP (read and write): CRM, tickets, code, BI, Crossbeam, HubSpot
Control planes: IdP/SSO, RBAC, Audit/SIEM, Protect(+), Model Hub, usage limits, Insights
```

- Enterprise Graph: relationships between people, content, projects, built from indexed content,
  metadata, permissions and identity resolution [D18]. Ranking uses a per-company semantic model,
  hybrid lexical plus semantic retrieval, activity signals (views, edits, shares, links in Slack,
  email, Jira), authorship, org-chart proximity and freshness [D31] [B5].
- Structured data and data lakes hold only 5 to 10% of enterprise knowledge; the rest is in email,
  messages, meeting notes and exceptions (Jain, VENDOR) [V1].

### 1.2 Access modes

| Mode | What happens | Implications |
|---|---|---|
| Indexed | Crawled ahead, permission snapshot mirrored | Low latency, covered by Protect scans and content hiding |
| Live | Fetched at query time, often per-user auth | Different rate limits; tenant restrictions and DLP may not apply the same way |
| Hybrid | Index for recall plus live top-ups | Common for CRM |

[D18] Slack is now live-only (Real Time Search), so sensitive-findings scans and content hiding do not
apply to Slack results [D26] [D32].

### 1.3 Deployment-date rules that change setup (check first)

- Deployments created **on or after 2026-08-14** get the new one-step setup for Google Drive, Google
  Calendar, Gmail, Microsoft 365, Outlook, SharePoint, OneDrive, Salesforce, Notion, Slack and
  BigQuery; their tools enable automatically [D24] [D47].
- Deployments created **on or after 2026-09-22** configure MCP integrations in the Connectors catalog;
  earlier deployments look in Connectors first, else Platform, Tools. Existing MCP configs are not
  moved; do not create duplicates [D18].
- Always ask a customer their deployment date before walking them through a connector or tool setup.

### 1.4 Hosting models

| | Glean Hosted | Customer Hosted (formerly Cloud-Prem) |
|---|---|---|
| Where | Glean's single-tenant GCP/AWS | Customer's GCP or AWS project, managed by Glean |
| Pros | True SaaS, auto-scaling, simpler pricing | Data residency, raw logs, VPC SC/SCPs, burn cloud commits, lower licensing |
| Cons | Less network control | Region fixed after build; blocking Glean's maintenance account voids SLAs |

Both: single-tenant, SSO-only, AES-256 at rest, TLS, key rotation 30 days (GCP) or 90 days (AWS),
audit of agent access and tool history, backups up to 7 days, "no logging of individual user queries
or responses" [D3]. No on-prem option [A12]. Mid-market default: Glean Hosted unless a hard constraint
exists.

---

## 2. Deployment runbook

### 2.1 Stages (official)

Pre-deployment, Deployment model, Stage 1 Create workspace, Stage 2 Prepare workspace, Stage 3 Go
live, Stage 4 Get the most out of Glean, Post launch [D1].

### 2.2 Pre-deployment checklist

- [ ] Phase 1 apps: 4 to 6 mission-critical; minimum one document repository and one communications
      app. Connecting everything upfront delays ML training and launch [D2].
- [ ] App-owner and security approvals started early (the biggest delay; some docs need an NDA) [D2].
- [ ] Admin emails (they receive the magic link), every sign-in email domain (unknown domains are
      blocked), deployment region (some regions cost more) [D2].
- [ ] People data source chosen and clean: First, Last, Email, Title, Team, Department, Location,
      Manager Email [D2].
- [ ] Hosting model decided [D3].
- [ ] Named owners: each data source owner, IT admins, the long-term Glean owner [P1].
- [ ] Business outcomes and KPI baselines written before deployment [P2] [P1].
- [ ] Permission hygiene scan (Varonis or Purview) on the top sources, or plan Protect+ [V13].
- [ ] Two admin training sessions scheduled: "lay of the land," then org decisions (who builds
      agents, sharing, approval, templates) configured before any pilot [V13].

### 2.3 Stage 1: create workspace

1. Admin Console at app.glean.com/admin. Before SSO is active, it runs in Central Workspace Setup
   (CWS) mode with magic-link sign-in (single-use, about 15 minutes) [D9].
2. Add admins. Setup-time roles: Admin, and Setup Admin (connectors and crawls only; give to app
   owners) [D9].
3. Configure SSO (section 3). Configuring SSO in CWS does NOT activate it [D9].
4. Connect people data (section 3.2).
5. Add Phase 1 connectors. **Crawls do not start automatically:** select connectors, **Enable crawl**
   (post-launch the button is **Start crawl**) [D19].

### 2.4 Crawling, indexing, learning

- Three background processes: crawling, indexing (builds the Knowledge Graph), learning (ML) [D4].
- Crawl plus index: 2 to 3 days small, 10 to 14 days large. ML: 2 to 14 more days; slower on T4 GPU
  regions (4 to 6x). ML status is not visible in the UI; a Glean engineer notifies you [D4].
- Monitor at Admin Console, Platform, Connectors: Initial sync (Crawling step 1/2, Indexing 2/2), then
  Items synced, Crawl rate, Change rate. Metrics refresh hourly [D4].
- Steady state: webhooks processed in 1 to 5 minutes; incremental crawl every 24 hours; each connector
  crawls in parallel on its own crawler [D4].

### 2.5 Stage 2: validate the workspace

Do not treat "crawl finished" as production ready. Check [D19] [D33] [D32]:

- People data "Attention required" tab clean (bad emails, unknown departments) [D16].
- Per connector: health, item counts versus source, freshness, visibility.
- Source permissions: use **Document lookup** (Admin console, Content management) to check a doc's
  last crawled, last indexed, visibility, and whether a named user can access it [D33].
- Limit new connectors to a **test group** (up to 10 groups, 1,000 members each, about 30 minutes to
  propagate; Okta groups not supported for test groups) [D32].
- Run the permission hygiene tests in section 7 and a 50 to 200 question role-based benchmark
  (section 18).

### 2.6 Stage 3: go live

Five-step rollout checklist [D5]:

1. Users and permissions, People data, clear "Attention required."
2. User roles: set **Default Member permissions** (Answers, Collections, public Pins, Go Links,
   create/save agents) [D16].
3. Assign the Glean app to users in the IdP (SSO becomes the only sign-in).
4. User roles, **Invite teammates**.
5. Managed rollout of the browser extension (Chrome, Edge, Firefox, Safari, Brave) [D8].

Launch recipe [D6] [D7]:

- Pilot 100 to 300 users across departments (or one department); pre-launch survey; #glean-feedback
  channel including the Glean account team; 60-minute kickoff with a pre-recorded exec message;
  weekly office hours with a feature deep dive.
- Seed content before launch: about 10 Answers, 5 Go Links, 2+ pinned results, verified canonical
  docs (handbook, T&E, IT setup). Menu: Knowledge, Announcements / Answers / Go Links.
- Branding: Admin console, Customization, Appearance [D5].

**Pilot sizing, reconciled.** Alchemy pilots with 5 to 7 people even at 20 employees [P1]; Glean says
100 to 300 [D6]. Use both: a 5 to 7 person tuning cohort (mixed departments and tenure; long-tenured
staff know where data lives, new hires test onboarding), then a 100 to 300 scale pilot, then business
unit waves of 1 to 2 weeks each with their own training and comms [V13]. Expect the pilot to reorder
priorities: "You spend weeks on the ERP and CRM, and the first question is 'what is my PTO policy?'"
[P1].

### 2.7 Post-launch

Add sources gradually, build agents and tools, monitor adoption and connector health, follow-up survey
about four weeks after kickoff, expand in waves, meet the Delivery Excellence Manager regularly, use
Glean Academy [D1]. status.glean.com only shows multi-customer incidents; tenant issues arrive by
email or banner; tickets at support.glean.com [D1].

### 2.8 Timelines by source

| Source | Claim | Label |
|---|---|---|
| Glean docs | 1 to 3 weeks standard; 3 to 4+ weeks large [D1] | VENDOR |
| Glean partner manager | "about two weeks" to set up [V14] | VENDOR |
| Glean Community | few weeks small; 4 to 5 weeks mid-size; delays from identity, people data, permission decisions, stakeholders [P14] | VENDOR community |
| Alchemy | 4 to 8 weeks to value; 12-week onboarding plus 6 months of follow-on [P3] [P1] | PARTNER |
| Ashisuto | search, then Assistant, then agents over 2.5 years, each layer trusted first [P9] [P11] | PARTNER |

---

## 3. Identity

### 3.1 SSO

- Mandatory for every deployment and configured first. OIDC or SAML with Okta, Entra ID, OneLogin,
  Google or generic SAML. Glean recommends **OIDC** (asynchronous directory sync, finer permissioning;
  SAML attributes refresh only on re-auth). Add an IdP conditional access policy with MFA [D10].
- Three states: Configured, Verified, Active. On activation, replace the central `apps-be.glean.com`
  callback, ACS and entity values in the IdP with tenant-specific values, then test **both**
  Glean-to-IdP and IdP-to-Glean redirects. If "Switch to logging into Glean via SSO" is missing, the
  tenant is still provisioning [D9].
- Backend domain (tenant ID) format `tenant_id-be.glean.com`, also shown at
  app.glean.com/admin/about-glean as "Server instance (QE)". It is used for login, search, crawling,
  webhooks, APIs and MCP URLs [D10] [D54].
- Force re-auth: User roles, row menu, **Sign out of all sessions** (up to 5 minutes; includes MCP
  hosts) [D16] [D53].

### 3.2 People data

- Separate from SSO. SSO controls who signs in; people data powers profiles, org chart, permissions
  enforcement, RBAC and ranking. A user can sign in without a profile or appear in the directory
  without SSO assignment [D11].
- Sources: Okta, Entra ID, Google Workspace, Workday, BambooHR, Pingboard, Lattice, CSV, Indexing API.
  Initial sync 2 to 4 hours, then about hourly. Enable it under People data even when OIDC SSO uses
  the same IdP [D12] [D11].
- **Manager email is used heavily in ranking** and required for the org chart. Okta, Google and Workday
  require Manager and Department or the sync fails. CSV is not recommended ongoing [D12].
- Entra needs application permissions (`Directory.Read.All`, `User.Read.All`) [D11]. Okta connector
  scopes `okta.users.read`, `okta.apps.read`, `okta.logs.read`, `okta.groups.read`; revoke the token
  after setup [D12].
- **Identity stitching:** one person per primary email; connector accounts link only by primary or
  alias. Maintain aliases in admin-controlled `proxyAddresses`; otherwise content shared to an
  alternate address never shows for that user [D13].
- MAU above headcount usually means recently terminated users in the 28-day window or a stale org
  chart [D75].

### 3.3 Groups

Map IdP groups (Entra via the Microsoft 365 connector, Google Groups, Okta) to one primary role plus
secondary roles. Highest primary wins; secondaries union. Max 1,000 groups. Sync near real time for
SAML/SCIM, up to 3 hours for OIDC. Does not change connector ACLs. Path: Users & permissions, User
roles, Default Member permissions, "User group permissions" [D17].

---

## 4. Admin roles and RBAC

| Role | Can | Notes |
|---|---|---|
| Setup Admin | SSO, connectors, crawls, test groups, Indexing API tokens only | Give to app owners [D14] |
| Admin | Everything above plus settings, UI, roles (not Super Admin), visibility, Assistant, invites, all API tokens except global | [D14] |
| Super Admin | Global tokens, Sensitive Content Moderator, Admin Search, Sensitive findings, AI Security | Off by default; first grant by Glean support after written CISO/VP+ approval (1 to 2 days); cannot be downgraded by Admins [D14] |
| Member | View Announcements/Answers, edit Collections, own Go Links, private pins, verify own docs | Sees the Actions tab in Admin Console; cannot be hidden [D15] |

Moderator and special roles [D15]: Announcements, Answers, Collections, Go Links, Pinned Results,
Teams, Verification moderators; **Insights Moderator** (recommended for senior leadership only);
**Billing Moderator** (Credits dashboard, for finance and cost-center owners); **MCP Server
Moderator** (create Glean MCP servers; recommended for engineering, GTM or AI platform teams);
Sensitive Content Moderator (security only); Action Creator; Agent Creator, Agent Moderator,
Departmental Agent Moderator (section 10.4); Skills Moderator [D79].

Design rules:

- Separate routine administration from the most privileged roles. Map roles to managed IdP groups,
  least privilege, no permanent broad Super Admin [D14] [D17].
- Default Member permission changes take up to 15 minutes [D16].
- Admin audit logs (connector, crawl, feature, MCP and OAuth changes; not end-user activity) at Users &
  permissions, Audit logs; 30-day default retention; CSV export; ongoing delivery to GCS, S3,
  BigQuery or Athena by arrangement [D72].

---

## 5. Connectors

### 5.1 Types and setup journey

- Native (API-direct, attachments, threads, activity), Web history (from the browser extension,
  private to the user), Push API / custom (Indexing API), Partner connectors (built by partners on
  the Indexing API) [D18].
- Six steps: find in Connectors hub, prerequisites, configure (Admin console, Connectors, Add
  connector), index (Crawl now or schedule), validate with a test group, monitor each capability
  separately [D19]. Some connectors add a **Manage data** tab for inclusion and exclusion rules.
- 250+ connectors (Glean press, August 2026) [B14]; older partner pages say 100+ or 120+ [P1]. Cite
  the current number with its date.

### 5.2 Limits (not changeable)

Items over 64 MB: metadata and permissions only. Under 64 MB: first 16.875 MB of text indexed.
Spreadsheets about 250,000 characters. Non-indexed content loses Summarize. For big corpora use date
windows, greenlists/redlists or owner rules [D21]. Exclusion beats inclusion when both match [D85].

### 5.3 Default refresh rates (selected) [D20]

| Connector | Incremental | Full | Other |
|---|---|---|---|
| Salesforce | 10 min | 28 days | share records hourly, people 1 h |
| Slack | live (RTS) | n/a | identity crawls only |
| Google Drive | 3 h | 28 days | activity via Reports API 10 min |
| Jira | 6 h | 28 days | webhook under 5 min |
| Gong | 5 min | 12 h | Gong itself takes 10 to 60 min per call |
| Zendesk | 1 h | 28 days | webhooks for tickets |
| HubSpot | webhooks plus incremental | not in table | see 5.5 |

Deletions: minutes to hours for Drive, SharePoint, OneDrive, Box, Slack, Confluence; otherwise next full
crawl. Support can purge urgent sensitive items; admins can hide docs meanwhile [D19].

### 5.4 Salesforce (Glean's deepest CRM integration)

- One authorization covers permission-aware search over Accounts, Contacts, Leads, Opportunities,
  Cases, Tasks, Campaigns, Knowledge, Files, CPQ and any SOQL-queryable custom object, plus live data
  and tools [D23] [D24].
- **New setup** (deployments from 2026-08-14): authorize the Glean connected app once; live data and
  tools work immediately; indexing builds in the background. **Previous setup**: integration user and
  connected app first [D24]. Each end user authorizes their own Salesforce account on first live use.
- Permissions mirror OWD, role hierarchy, sharing rules, manual shares, profiles, permission sets,
  territories. **FLS is not enforced.** Share records re-scan hourly, so a revoked share can persist
  up to about an hour [D23].
- Large orgs: start with Accounts, Contacts, Opportunities, Cases, Knowledge; add objects later [D23].
- Tools (25+): Search Salesforce with SOQL, Update Opportunity (stage, close date, amount, forecast
  category), Create/Update lead, contact, account, note, call log, campaign membership, send and log
  email, and more. Writes use a review flow by default [D47]. Assistant updates one opportunity per
  request with a side-by-side review [D34].
- Content triggers: new record, record updated, record meets condition (filter by object, owner,
  stage) [D38]. Search filters: `app:salescloud`, `app:servicecloud` [D23].

### 5.5 HubSpot

- Indexes **only** Contacts, Companies, Deals, Tickets. No custom objects, no Leads, no Marketing Hub,
  no embedding Glean in HubSpot. Permissions enforced at query time via HubSpot's permissions API [D25].
- Setup (HubSpot super admin): private app with scopes `crm.objects.users.read`,
  `crm.objects.owners.read`, `crm.objects.contacts.read`, `crm.objects.deals.read`,
  `crm.objects.companies.read`, `crm.objects.tickets.read`, `crm.schemas.tickets.read`; webhook
  subscriptions per object for created, deleted, restored, association changed; enter portal ID,
  access token and client secret in Glean. No webhooks means changes wait for the next crawl [D25].
- Live HubSpot actions go through HubSpot's own remote MCP server, which is in Glean's supported MCP
  list [D51] [B13]. Partner or custom objects in HubSpot need the MCP route or the Indexing API.

### 5.6 Slack (Real Time Search)

- Since Slack's 2025 API terms blocked bulk export for LLMs [A24], Glean uses Slack RTS: federated,
  zero-copy, fetched live; only identity crawls run, so low "Items synced" counts are normal. Pair
  with the Slack connector for engagement signals and triggers [D26].
- **Every user must authorize** Slack; until then results are typically public channels only. Toggles
  for private channels and DMs. Slack admins may need to approve the Glean Marketplace app. Slack rate
  limits (HTTP 429) cannot be raised by Glean. Email-to-channel messages are not supported [D26].
- Semantic Slack search needs Slack AI Search enabled in the workspace [D26].
- Slack Connect / external shared channels cannot fire content triggers; Gleanbot messages never
  trigger (loop protection) [D38].
- Gleanbot: auto-answers when a question is detected or `@Glean` is mentioned (private by default),
  `/glean`, daily digest DMs. With your own model key, channel auto-answers incur LLM cost [D81].

### 5.7 Google Drive, Gong, Jira, Zendesk

- Google Drive: service account with domain-wide delegation impersonating a directory admin; Google
  quota 12,000 QPM; exclusions by folder ID (not recursive), shared drive, or Google Group [D27].
- Gong: admin OAuth; calls, transcripts, metadata, library. Calls shared via Gong's UI sharing are not
  enforced (API gap); calls over 2 hours wait for the full crawl [D28].
- Jira: Forge crawler app; custom fields reach Assistant and agents only if greenlisted (Manage data,
  Inclusion rules) or the "Index Jira issue custom fields for assistant" toggle is on [D29].
- Zendesk: API token from a service account; 12 QPS default [D30].

### 5.8 Custom connectors and the Indexing API

- Push documents, metadata **and** users, groups and ACLs. Run Glean-hosted (Docker in your Glean
  deployment) or self-hosted [D22]. A connector that ingests content without the source's permission
  model is unsafe by construction [D22] [P8].
- First-run checklist: metadata, rendering, permissions model, token scope, then index one public and
  one permissioned sample before scaling [D22]. Useful endpoints: `/indexdocument`,
  `/bulkindexdocuments`, `/processalldocuments`, check document access, `/deletedocument`. Examples:
  github.com/gleanwork/indexing-api-connectors [D22].
- Token types: Indexing (rotation, IP ranges, required expiry), Client (Chat, Search, Answers scopes),
  Authentication Token API key [D22].
- Migrating native to custom: separate namespace; update agents, saved searches, filters and pins;
  run both in parallel [D22].
- Partner practice: Alchemy builds custom connectors in "a couple of weeks"; "Eighty percent coverage
  is a good start. One hundred percent is what makes search trustworthy" [P1]. Bridge IT: map the full
  entity schema first, enforce ACLs at index time, incremental delta sync [P15].

---

## 6. Search relevance and curation

- No manual ranking knobs are documented; ranking learns from interactions, access, sharing and
  cross-app references [D31]. Levers you control [D7] [D32] [D80]:
  - Pinned results (Only me vs Teammates), Verification (Verified / Deprecated, reverify reminders),
    Answers (shown on top when high confidence; create from any Slack message), Collections (being
    replaced by Projects, auto-migrated), Go Links (need extension or DNS; variable links like
    `go/dashboard/<customer>`), connector facets and custom properties, test groups, content hiding
    CSV, greenlists/redlists, LLM exclusion rules (searchable but out of Assistant and agents).
- Diagnostics: Document lookup and connector Change rate [D33].
- Known complaints: stale docs ranking above current ones, noisy Slack threads above authoritative
  pages, Microsoft sources "finicky" [A11] [A12]. Fix with verification and deprecation, pins for
  canonical pages, and retiring obsolete repositories [A14].

---

## 7. Permission hygiene campaign (run before broad rollout)

| Test | What to verify |
|---|---|
| Former employees | Deprovisioning removes group, mailbox and delegated access completely |
| Delegated mailboxes | Managers no longer hold departed employees' mailboxes [V13] |
| Nested groups | Effective membership resolves as expected |
| Shared links | "Anyone in company" and public links are intended |
| Exec / HR / legal / finance | No hidden subfolders inherited by broad groups [P1] |
| CRM data | Record-level entitlements behave; FLS-sensitive fields red-listed [D23] |
| Custom connectors | Indexed ACLs reproduce source semantics [D22] |
| Agents and tools | Write scopes narrower than search scopes |
| Service identities | Tokens and non-human identities owned, rotated, revocable |
| Aliases | Alternate emails stitched via `proxyAddresses` [D13] |

Tools: Varonis or Microsoft Purview scans before connecting; Purview sensitivity labels can exclude
SharePoint/OneDrive items; Glean Protect+ sensitive findings and auto-hide inside Glean, with the
caveat "It's not going to solve your actual downstream data source issue" [V13] [D32] [D69].

"Can access" is not "need to know." RAG can blend content across permission boundaries; schedule
red-team prompt simulations (Knostic, COMPETITOR-adjacent vendor) [P16]. Treat any "leak" report as a
source-permission audit first [V12].

---

## 8. Assistant configuration

- Activate at Admin Console, Platform, Assistant, Setup (greyed out until people data, initial
  crawls and ML complete). Enable for all or a test group [D34].
- Up to five custom instructions (affect response, not retrieval; apply instantly to everyone; can hurt
  quality) [D34]. LLM exclusion and inclusion rules by connector, container or document (up to an hour)
  [D80].
- Chat history retention: Off, 30 days, 90 days, 6 months, 1 year; decreasing permanently deletes;
  event logs (GCE) continue regardless [D73].
- Surfaces: Chat, AI Answers, Summarize, Glean in Slack and Teams, agents, Deep Research, canvas,
  artifacts (docs, sheets, slides, interactive HTML and dashboards), image generation, Meeting Notes,
  memory (Universal Key on GCP only), warehouse data via BigQuery, Snowflake, Databricks Genie [D34]
  [B12] [D64].

---

## 9. Skills

- SKILL.md packages (Agent Skills standard) routed by description, by name, `/skill-name`, or `+`.
  Types: Glean built-in, Personal, Shared. Upload `.zip`/`.md`/`.skill` (100 files, 10 MB zip) or
  import from GitHub with daily one-way sync. Skills grant no new data access [D78].
- Admin: Admin console, Skills, Setup: "Skills in Assistant" (disabled, test group up to 100, all),
  third-party GitHub skills, sharing. Member share toggles are all off by default; admins can
  "Auto-enable" [D79].
- Evidence: a Salesforce skill that sequences multiple Salesforce tools raised accuracy from 73% to 85%
  and cut time to first token 18%; adding negative examples to a description fixed a 20% trigger drop
  (VENDOR) [B8] [V11].
- Skills are on-demand expertise; agents automate processes and can call skills [D78]. Skill
  adoption has no dashboard; use GCE logs [D75].

---

## 10. Agents

### 10.1 Build modes

- **Auto mode** (default): describe the outcome; the agent plans. Best for research, analysis,
  summarizing, drafting. Can use sub-agents (Task tool), embedded Skills, artifacts, sandboxed code.
  Always runs with the current user's permissions [D35] [D36].
- **Workflow mode**: explicit steps, branches, loops; deterministic. Use for strict conditional logic
  and fixed procedures (Ashisuto's rule) [P10]. Step memory defaults to "Previous step only"; reference
  outputs with `[[ ]]` [D35].
- Builder: Create agent, Builder Assistant, Instructions (markdown SOP style), Tools, Resources,
  Triggers, Model (Fast vs Thinking, per-step model), **Preview** and **Debug** (path, tool calls,
  traces, context use), **Save** publishes. Version history keeps 30 versions; export Workflow agents
  as JSON [D36].
- Scope knowledge on purpose. Glean's own security-RFP agent is limited to one Drive folder, the policy
  docs and one Slack thread so it ignores informal chatter [V14].

### 10.2 Triggers

- Chat message, input form, content trigger, schedule, custom webhook [D37].
- Scheduled triggers are off by default (Admin console, Platform, Agents, Scheduled triggers). Per
  user, max 10 active background agents per user; scheduled runs time out at about 30 minutes; if a
  tool needs confirmation, Glean emails the user [D37] [D39].
- Content triggers ("when X happens, do Y"): low-latency sources Gong (new call), Jira, Salesforce
  (new, updated, meets condition), Gmail, Google Calendar (new event, before the event), Outlook,
  Slack (not external channels). Experimental (up to hours): Drive, GitHub, OneDrive, SharePoint,
  ServiceNow, Zendesk, Zoom, Outlook Calendar. Admin enable at Agents, Setup, Content triggers. Always
  add a filter; unscoped triggers burn the hourly quota; prefer "Meets condition" when fields fill
  later [D38].

### 10.3 Limits and patterns

Hard per-run tool-call and response-size caps (numbers not published). Use company search for ranked
relevance; use native tools (SOQL, JQL, SQL) for exhaustive counts and precise filters; batch by date;
start with low result counts [D39].

### 10.4 Sharing, publishing and governance

- Access: Viewer, Editor, Owner (one owner; groups get Viewer/Editor only). Admins own all agents.
  Deactivated owner passes to their manager, else an Agent Moderator [D40].
- Roles: **Agent Creator** (publishes without approval), **Agent Moderator** (see, edit, disable all),
  **Departmental Agent Moderator** [D40].
- Default Member toggles: "Can create and publish agents" (On), "Can publish agents via embedding,
  API, and Slack" (Off), "Can share agents" (On, department or company scope). **"Publishing an agent
  requires approval"**: Never / company-wide only / specific people or company [D40].
- Governed states: Draft, Ready to publish (builder requests; moderator emailed), Published [D41].
- Agent Library curation: about 5 core categories per department, verified badge, company attribution
  [D40].
- **Auto-routing**: up to 15 conversational agents, routing condition up to 500 characters, first
  match wins, applies to all users [D42].
- **Knowledge profiles**: a bounded "public data" corpus (specific Slack workspaces, Drive groups, Gong
  workspaces) so a shared agent answers consistently for everyone. Powers public Gleanbot answers [D43].
- Slack publishing (chat-message agents only): one agent per channel; recommended visibility "only
  visible to user with option to share"; write tools needing approval do not complete from Slack [D44].
- **Independent agents** (beta) and **service credentials**: agent-owned identity, runs unattended
  with admin-scoped permissions; credentials injected server-side; templates for Salesforce, Gong,
  Slack, Teams, Google, Atlassian, Zendesk, ServiceNow, Snowflake and more. Start read-only or shadow
  mode [D45].
- Agent Development Lifecycle: plan, define quality, build safely, test and launch, manage versions,
  govern and monitor; risk tiers Low to Critical; monitor WAU, runs per week, feedback ratio, error and
  permission-denied rates, golden-set spot checks; "CRM write agent" gets quarterly write-logic review,
  audit logs, rollback readiness [D46].

### 10.5 Builder program design (field practice)

| Pattern | Source |
|---|---|
| 15% builders, 85% users; build rights via per-division Knowledge Managers | Ashisuto [P9] |
| Designated builders, approval, publish to wide groups, maintain centrally | Alchemy [V13] |
| Decide builders, sharing and approval in admin training before the pilot | Alchemy [V13] |
| Let teams experiment once the gate exists; label agents "still testing!" | Ashisuto [P9] |
| Hybrid: everyone may build, departmental builders top-down, moderated library, search over agents | Jain [V2] [V6] |
| Write the steps you do in your head, then map each to an agent step | Harvey CSM [V8] |
| Measure the function baseline (contracts per lawyer, meetings per rep) before building | Jain [V3] |

Agent sprawl is real: some customers have 30,000 to 40,000 user-built agents, most duplicative [V2].
Ashisuto's numbers (about 1,300 staff, February 2026): 2,100+ active agents, 74% ever used an agent,
43% monthly, 45,948 executions, peak 703 per day, about 200 creators; daily runs rose from about 200
to 700+ over six months [P9].

---

## 11. Tools, actions and write governance

- Tools are live read/write operations; sources: first-party, MCP (by connector), custom (OpenAPI spec,
  single endpoint, you host it) [D47].
- Admin paths: Admin console, Connectors (catalog MCP) and Admin console, Platform, Tools (Enabled
  tools, Add tool, Import from MCP server). Per tool pack: OAuth connection, surface toggles (Chat,
  Agents, Glean MCP Server), per-tool enable, visibility scope [D47].
- Two access layers: **visibility scope** (who can use the tool anywhere, including via MCP and the
  Claude Code plug-in) and **role-based access** (which builders can add it). A company-wide agent using
  a tool scoped to one department fails that step silently for everyone else [D48].
- **Run without user confirmation** is two-tier: admin eligibility per tool plus builder activation per
  step. New MCP write tools default to Allowed, but destructive tools are not auto-excluded; disable
  delete, close and archive explicitly [D49].
- Human in the loop: write tools pause with Allow/Cancel and an editable preview (Salesforce fields,
  Jira comments); Approve All for batches; users can set per-app Always allow / Needs approval [D50].
- Protect+ **agent access policies** (CEL rules at tool call or tool output: Block, Filter, Flag). Up to
  20 rules per policy; most restrictive wins; fails open on config errors. Flag for 7 to 14 days, then
  enforce. Examples: block posting to `#all`/`#general`; flag email to external domains; filter
  `/Finance/` documents from search output for automated agents [D70].
- Governance tier two for agents: explicit tool registration, constrained OAuth scopes, named owner,
  logging, approval for high-impact writes, rollback procedure, central publication [P1] [D46].
- Action gap critique: competitors say Glean is "retrieval-focused, limited action" and lacks action
  packs for HR/ERP (Workday, SAP, UKG, ServiceNow) [A16] [A21]. Verify per system.

---

## 12. MCP, A2A and APIs

### 12.1 Glean as an MCP server (Glean context inside Claude, ChatGPT, Cursor, Copilot)

- Built in; enabled by default with OAuth for new customers. Dynamic Client Registration restricted to
  a Glean-vetted list. Manage at Users & permissions, Third-party access (OAuth) [D53].
- URL: `https://{backend-domain}/mcp/{server-path}` (backend at app.glean.com/admin/about-glean).
  Create servers at Admin console, Platform, Glean MCP servers, Create server. MCP Server Moderator can
  manage servers; enabling MCP needs Admin [D54].
- Default tools: `search`, `chat`, `read_document`, `employee_search`, `user_activity`, `memory`,
  `memory_schema`. Others: `code_search`, `gmail_search`, `outlook_search`, `meeting_lookup`,
  Artifacts (`upload_artifact`, `update_artifact`, `share_artifact`), images, and the "Dynamic skills
  and tools" set (`find_skills`, `read_skill_files`, `run_tool`) [D54]. Hosts may prefix names.
- Routing rules: people to `employee_search`, meetings to `meeting_lookup`, cross-source analysis to
  `chat`, documents always `search` then `read_document` [A23].
- Best practice: design servers by job ("Glean - Sales" at `/mcp/sales`); avoid one server with every
  tool; prefer Glean `search`/`read_document` over granular external read tools; add external read
  tools only for exact structured queries [D55]. Recommended sales server: `search`, `chat`,
  `read_document`, `employee_search`, plus Salesforce write tools [D54].
- Auth: OAuth 2.1 with PKCE (preferred) via Glean's authorization server or your IdP; fallback
  user-scoped Client API tokens with scopes `MCP`, `AGENT`, `SEARCH`, `CHAT`, `DOCUMENTS`, `TOOLS`,
  `ENTITIES` [D53].
- **Claude (Team/Enterprise):** enable Glean OAuth and the MCP server, allow Anthropic IP ranges
  through any firewall, add the remote URL as an org integration in Claude's admin settings, users sign
  in via Glean OAuth, validate with a test search [D56]. The host guide lists only `search`, `chat`,
  `read_document`; newer docs list more (verify in tenant) [D56] [D54].
- **Claude Code:** `/plugin marketplace add gleanwork/claude-plugins` then
  `/plugin install glean@glean-plugins`; needs DCR configured. Claude Cowork and GitHub Copilot are not
  supported by the plug-in [A23] [D59].
- **Agents as MCP tools:** not allowed with write tools or human-in-the-loop steps; host timeouts
  Claude Desktop about 60 s, Cursor 30 to 60 s, VS Code about 30 s; aim under 30 s; descriptions start <!-- VALIDATE-OK[identity]: product name, not an operator path -->
  with a verb and name sources and outputs [D57].
- **MCP Gateway:** one governed endpoint exposing 2,000+ tools to Claude, ChatGPT, Cursor, Gemini,
  Copilot, with Protect+ guardrails on tool calls and per-user tool visibility [D58].
- Pricing: MCP is "subject to usage-based pricing" under FlexCredit terms; per-call cost is not
  published; rate limits are not published [D53].
- Monitoring: MCP activity logs and a separate MCP Insights dashboard (MCP-only users do not raise
  Search or Assistant numbers) [D86].
- Glean Docs MCP (public docs, not a tenant): `https://docs.glean.com/mcp` with `docs_search` and
  `docs_fetch`. Use it to verify any fact in this file live [D60].

### 12.2 Glean as an MCP host (external tools inside Glean)

- Add remote MCP servers under Platform, Tools (Vendor provided tools via MCP) or the Connectors
  catalog on newer deployments. Prefer **OAuth User** so each person's own permissions apply; OAuth
  Admin shares one credential and gives up per-user permissions. MCP tools work in "Plan and execute"
  steps and autonomous agents [D52].
- Supported list: 178 remote MCP servers including **Crossbeam**, **HubSpot**, Gong, Outreach, Apollo,
  Clay, Common Room, ZoomInfo, Gainsight, Klue, Superhuman Mail, Slack, Notion, Asana, Monday.com [D51].
- Crossbeam's side confirms Glean as a supported MCP client (2026-09-01). Crossbeam MCP: URL
  `https://mcp.crossbeam.com/mcp`, OAuth 2.1 with PKCE and DCR, read-only, 11 tools, annual credits
  Free 50, Connector 500, Supernode 2,500, Enterprise 5,000, needs a Full Access or Sales seat [A18]
  [A19]. Forecastable's own note: the MCP server is effectively Supernode and up (doc 20).

### 12.3 A2A and REST

- A2A host (Glean agent calls an external agent; OAuth auth code only; text only), Glean A2A server
  (Gemini Enterprise, Copilot Studio call Glean), per-agent A2A endpoints [D62].
- Client API (search, chat, agents) and Indexing API; tokens at Admin Console, Platform, API tokens;
  agent-scoped tokens expire after one year [D22].

---

## 13. Models, pricing and cost control

### 13.1 Model Hub

- Universal Model Key (Glean-managed contracts, failover, "Auto" selection) or Customer Key/BYOK (you
  own capacity and failover) [D63]. BYOK loses Memory, Meeting Notes and podcast artifacts; LLM
  Insights only exists for BYOK [D64].
- Models listed September 2026 span OpenAI GPT-4.1 to GPT-6, Gemini 3.x, Anthropic Claude Haiku 4.5
  to Opus 5.5, Amazon Nova, Glean's Waldo, and open models (GLM, DeepSeek, Nemotron 3 Ultra, Kimi)
  [D63]. Names change monthly.
- Restrict: toggle off in Models; "Blocked models in assistant" or "in agents"; hide premium models
  from pickers (Models, Advanced settings); limit non-default models to departments or IdP teams
  [D65]. Best practice: balanced default, upgrade only chosen workflows, consistent model families [D84].

### 13.2 Enterprise Flex and FlexCredits [D66]

- Per-user seats plus a pooled org allowance of FlexCredits; packs for more.
- Included: Fast Mode Assistant, search in app, Collections, Go Links, People, agent creation and
  testing, Platform/Admin/Indexing APIs, Thinking and Adaptive queries on Standard models up to 100
  per user per week.
- Consume credits: premium models, Code Writer, slides, Deep Research, Meeting Notes, **agent runs**,
  and Client API calls (Search, Chat, Agents, including via MCP).
- Typical credits (p50 / p90): basic search via API 1; Fast Mode 3 / 15 (0 in app); Thinking standard
  7 / 26; Thinking premium 35 / 120; slides 45 / 142; Deep Research 33 / 144; **agent run 7 / 114**.
- Model tiers: Basic (Waldo, Haiku 4.5, Flash), Standard (GPT-5.x, Gemini Pro, GLM), **Premium (all
  Claude Sonnet 4.6+/Opus, GPT Sol/Terra)**. Claude-based agent steps burn premium credits.
- Protect+ and Premium Support (24x7, 1-hour critical SLA) are site-wide annual fees.
- Alternate plan, Glean Core Suite: seats plus "Model Hub Usage" at provider API rates plus a
  management fee [D83].

### 13.3 Usage controls [D67] [D68]

- Admin console, Usage (Super Admin, Admin, Billing Moderator): by product, user (per month from July
  2026), model, department; CSV for chargeback.
- Alerts at 50/75/90/100%; monthly limits for total, per user, per agent; optional block until next
  month; overrides by user, department or IdP team (precedence user, then department/team, then
  default). Flex users keep basic chat after hitting a limit.

### 13.4 Cost playbook

1. Name a spend owner and a Billing Moderator in finance [D15] [P2].
2. Default to Standard models; premium only for heavy-research teams ("Most people don't need the best
   of the best") [V13].
3. Set department and per-agent limits before scheduled or triggered agents go live; scope every
   content trigger with a filter [D38].
4. Review usage monthly by department and agent; kill runaway agents.
5. Keep the right to swap models: if one provider's price jumps, turn it off and route elsewhere
   [V13].
6. Treat Glean's cost benchmarks as directional (81% lower token cost than Claude Cowork on 180+ tasks,
   preferred 78%: VENDOR) and test on your own tasks [B2] [P2].
7. Buyer benchmarks: Vendr median contract $98,890 per year, minimums often 100 to 250 users, average
   negotiated savings about 20% [A8]. Estimates of $45 to $75 per user per month plus about $15 for a
   Work AI add-on are secondary sources [A9] [A10]. Glean publishes no list prices.

---

## 14. Security, Protect and audit

- Baseline: single tenant, zero LLM data retention, ISO 42001, SOC 2 Type II, ISO 27001, regional
  residency [D69]. Get current reports from the Trust Center under NDA; map controls to your own
  obligations rather than trusting a certification list.
- Protect (included): indexing inclusion/exclusion, one-time sensitive content CSV reports, manual
  remediation. **Protect+** (paid): continuous findings across 100+ sources, auto-hide, prompt
  injection and jailbreak detection, agent alignment, restricted topics, SIEM/SOAR partners. Only Super
  Admin or Sensitive Content Moderator can access Protect [D69].
- Sensitive findings cover indexed data only, not live fetches such as Slack RTS [D69].
- Content hiding CSV: `HIDE_ALL`, `HIDE_ALL_EXCEPT_OWNER`, `HIDE_FROM_GROUPS`; one active CSV that
  must carry the full list; any error blocks all; folders cannot be hidden [D32].
- Restricted topics: out of the box Compensation, Personal financial advice, Performance and personnel
  decisions; up to 10 custom [D71].
- Agent trace export via OTLP to Datadog, Arize, Langfuse and others; native tool args redacted [D74].
- DLP: pair Glean retrieval with autonomous hosts (for example Claude Cowork) only with output DLP
  (Nightfall, DLP vendor) [A20].
- Public sector: FedRAMP status was not confirmed anywhere; verify before saying anything [P13].

---

## 15. Insights, KPIs and scorecards

- Insights needs Insights Moderator. MAU (trailing 28 days), WAU (7), DAU (previous UTC day); 270 days
  of history; Insights chat for natural-language questions [D75].
- Core ratios: **Coverage** = signups / employees; **Activity** = MAU / signups; **Stickiness** = WAU /
  MAU [D75].
- Diagnostic playbook: low coverage and low activity = rollout problem; high coverage, low activity =
  training and use cases; high activity, low stickiness = embed into weekly workflows [D76].
- Agents insights: active agent users, runs (conversational: each message; background: each trigger),
  time saved, top agents and users, feedback, runs by outcome [D77].
- Glean company stat: 45% weekly DAU/MAU (VENDOR) [B10]. GM tracks "5D30" (active 5 of last 30 days)
  above 80% after 0 to 60,000 users in 90 days [V1].
- Export: Databricks Lakeflow Connect for Glean ingests `insights` and `shortcuts` (go links) tables;
  Beta, full refresh only [A7].

Four-layer scorecard:

| Layer | Metrics |
|---|---|
| Platform health | Connector health, crawl freshness, indexing errors, API failures, permission-test pass rate |
| Adoption | Activated users, MAU, WAU, WAU/MAU, queries per user, Assistant use, agent use, by department |
| Quality | Successful-query rate, answer acceptance, citation correctness, stale-answer rate, agent eval pass rate, up/downvote rate |
| Business outcomes | Search time saved, onboarding time, support deflection, resolution time, sales prep time, cycle time, revenue or cost impact |

Agent program template (Ashisuto): ever-used %, monthly active %, total executions, peak daily
executions, creator count, daily execution trend to test for novelty decay [P9].

---

## 16. Adoption and change management

- Operating model: **central team** (platform, connectors, security, standards, analytics, model and
  cost controls, agent publishing); **business champions** (use-case discovery, office hours,
  feedback); **expert builders** (approved agents and skills); **ordinary users** (search, Assistant,
  approved agents). Mid-market: a platform owner, identity/security partner, KM representative and 5 to
  15 champions is enough [PDF brief] [P5].
- AHEAD (about 3,000 staff): licenses gated behind the Glean Foundations course; 2,990+ completed by
  mid-April 2026 (treat the exact figure with caution); curriculum on prompt design, output
  verification, problem framing, workflow design; BU champions with toolkits, role charters, weekly
  forums, Learning Labs [P5].
- Ashisuto: departmental evangelists ("1GAN"), later Knowledge Managers who gate building; minimal
  hand-holding worked in its culture; an internal "Push the AI Agent" session drew 100 attendees [P9]
  [P11]. Mandatory training versus organic pull is a real disagreement; culture and size decide.
- Alchemy: the pilot group becomes the champions; training was the underestimated part ("What can I
  even do with this platform?"); "You get roughly one chance to earn user trust" [V13] [P1].
- Harvey: Glean agent in the new-hires channel; monthly usage about 85% to 98%; a 3.5-hour G&A
  hackathon with 65+ submissions [V8].
- Jain: about 90% of users are occasional and 10% power users; proactive AI closes the gap; executives
  should build their own automations [V2].
- Launch comms name concrete jobs, not "AI." Deploy the extension as the new tab page. Position Glean
  as one front door across vendor copilots [D8] [V14].

---

## 17. ROI and the business case

- Forrester TEI (commissioned by Glean, September 2024): 141% three-year ROI, $15.6M NPV, payback under
  six months, composite of 10,000 employees at 93% adoption and $40 per user, built from four
  interviews [A1]. 87% of benefit is one line: 60 to 70 hours saved per user per year. Glean's page
  says "up to 110 hours," which is not the modeled value [A1]. Pre-agents and pre-FlexCredits.
- Rebuild with your own wages, adoption curve, recapture assumption, contract cost and support baseline.
- **Time returned is not captured value.** Rank value as: (1) operating cost removed, (2) avoided
  hiring or contractor spend, (3) reduced cycle time tied to output, (4) added capacity or coverage,
  (5) time returned but not monetized.
- Full program cost: seats, add-ons, premium support (reported about 12% of license), implementation,
  FlexCredit forecast, admin FTE (Forrester assumed 1 FTE even at 10,000 users), content cleanup,
  custom connectors, change management [A1] [A9] [A13].

---

## 18. Vendor selection and proof of concept

Weights:

| Criterion | Weight | Test, don't ask |
|---|---|---|
| Permission fidelity and identity | 20% | Positive and negative access cases; leaver, nested group, shared link |
| Connector fit and freshness | 15% | Your top 10 systems, object types, API limits, sync lag |
| Retrieval and answer quality | 15% | Blind benchmark on real employee queries with citations |
| Security and compliance | 15% | Current audit reports, subprocessors, residency, retention, logging |
| Agent and action governance | 10% | OAuth scopes, approval, identity, logging, publication, revocation, evals |
| Administration and observability | 10% | Connector monitoring, RBAC, Insights, audit logs |
| Economics and model flexibility | 10% | Seats plus AI usage plus services over three years |
| Adoption and ecosystem | 5% | UX, extension, training, partner depth |

POC design: 50 to 200 role-based questions across departments with expected sources and entitlements;
include obsolete docs, duplicate policies, conflicting Slack threads, recently changed permissions and
data the tester must **not** see. Grade blind; rerun monthly (mirrors Glean's own eval method) [V12]
[B5]. Ask whether the POC is free or paid (reports of paid POCs up to $70,000, COMPETITOR source) [A10].
Negotiate 2 to 3 year terms, escalator caps of 3 to 5%, itemized services [A8].

Existing enterprise search? Run a migration benchmark before decommissioning; public benchmarks do not
reproduce enterprise relevance [B5].

Coexistence: SharePoint, Drive, Confluence stay systems of record; Slack/Teams stay the conversational
record; Jira/ServiceNow stay workflow authority; Salesforce/HubSpot stay customer authority;
Snowflake/Databricks stay the computation layer; ChatGPT, Claude, Copilot can stay front doors with
Glean feeding them context.

Who not to sell Glean to: small teams with one clean knowledge base, orgs with unreliable source
permissions, leadership expecting AI to replace documentation ownership [A13] [A14].

---

## 19. Structured versus unstructured routing

- "Databricks excels at what happened. Glean brings the why" [A6]. Patterns: Genie inside Glean
  Assistant via MCP, direct Databricks SQL, indexing Databricks objects, Glean context into notebooks
  [A6] [B6].
- Alchemy: Glean for knowledge discovery ("Where is the sales playbook?"); warehouse for analytics
  ("pipeline conversion by region") via Snowflake Cortex or Databricks Genie [P3].
- CRM: index search for fuzzy discovery; SOQL tools for exact counts, amounts, stages, dates [D39].
- Rule: numbers come from a system of record through a tool; explanations, precedent and "who knows"
  come from the Glean index; an answer that mixes both cites each.

---

## 20. Sales and revenue team use

- Eight quickstart sales agent templates: Account snapshot, Prospect outreach emails, Deal strategy,
  Competitive brief, Intelligent reminders, Sales call coaching, Deal loss insights, Account handoff (AE
  to CSM) [B7].
- Content-trigger recipes: Gong call transcribed, update the Salesforce opportunity and draft the
  follow-up; opportunity created or moved stage, summarize and assess health; before a customer
  meeting, build a brief from CRM, call, email and support context [D38].
- MCP for Sales (any MCP host): Customer 360, prospect research, call prep, competitive intel, weekly
  account reports, lost-deal analysis, CS handoff, territory planning, RFP support, lead qualification.
  Recommended connectors: Salesforce or HubSpot, Slack, Gong or Zoom, Gmail or Outlook, Confluence or
  Notion, Zendesk, Google Drive [D61].
- July 2026 sales connectors: Clari plus Salesloft, Crayon, Fathom, Granola, Otter, Showpad, Zoom,
  joining Salesforce, Dynamics 365, Gong, Seismic, Highspot [B9].
- Skills for account planning: encode sections, questions, systems to pull and risk summary; pair
  with a weekly agent to leadership [B8].
- Cloud Ace test: Glean reconstructed why a 5M yen proposal closed at 6.8M yen by combining a client
  exec request, the manager's Slack advice and the final contract in Drive, with source links [V15].
- Partner and co-sell use: see `forecastable-crossbeam-glean.md`.

---

## 21. Troubleshooting: symptom, cause, fix

| Symptom | Likely cause | Fix |
|---|---|---|
| Users see sensitive content | Over-shared source ACLs | Source remediation; hide via CSV; Protect+ findings; Purview/Varonis [V13] [D32] |
| A doc is missing for one user | Not crawled yet, alias not stitched, or no source access | Document lookup with that user; add `proxyAddresses` alias [D33] [D13] |
| Slack results only from public channels | User has not authorized Slack RTS | User connects at Your settings, Connectors; Slack admin approves app [D26] |
| Slack errors or empty results at peak | Slack HTTP 429 | Only Slack can raise quotas; reduce agent Slack calls [D26] |
| Stale doc outranks current one | No verification or deprecation | Verify canonical, deprecate old, pin, retire repositories [D7] |
| Poor search right after launch | Users let in before ML finished | Wait for Glean's ML confirmation before inviting users [D4] |
| MAU above headcount | Leavers in 28-day window, stale org chart | Refresh people data [D75] |
| Agent step fails for some users | Tool visibility scoped to one department | Widen scope or split agent [D48] |
| Background agent stalls | Tool needs confirmation | User approves via email or Agent Inbox; or enable run without confirmation deliberately [D37] [D49] |
| Credit spend spike | Unscoped content trigger, premium model default, Deep Research | Filters, department and agent limits, hide premium [D38] [D67] |
| Revoked Salesforce share still visible | Hourly share-record scan | Wait up to an hour; hide urgently [D23] |
| Salesforce field appears that users can't see in SFDC | FLS not enforced | Red-list the field or object [D23] |
| HubSpot custom object or Lead missing | Not supported by the connector | HubSpot remote MCP or Indexing API [D25] |
| Jira custom field not in answers | Not greenlisted | Manage data, Inclusion rules [D29] |
| Glean agent unavailable in Claude | Has write tools or HITL, or too slow | Read-only agent under 30 s [D57] |
| Claude cannot reach Glean MCP | Firewall blocks Anthropic IPs or MCP/OAuth off | Enable OAuth and MCP server; allow IPs [D56] |

---

## 22. Strategy and roadmap context (2026)

- Positioning moved from enterprise search to an enterprise context layer beneath every AI front door;
  model-agnostic middleware between models and systems [A22] [V5]. Gartner's First Take (2026-08-28)
  advises evaluating Glean "as a unifying context layer," model and tool agnostic, now competing with
  much larger platforms [A2].
- Glean:GO 2026 (2026-08-26/27) announcements: AI Gateway, portable memory and skills, Glean Tau desktop <!-- VALIDATE-OK[identity]: product name, not an operator path -->
  app, proactive task management, email triage, meeting coach, interactive dashboards, Team chat,
  independent agents, Glean Transform (workflow mining; demo 38 sales opportunities), auto-routing,
  spend-aware usage controls, agent governance policies, context-aware threat detection [V1]. Status of
  Glean Intelligence auto-routing (beta vs GA) conflicts across sources [P2].
- Open models: Jain expects most enterprise inference to shift to open models within 12 to 18 months;
  Glean Waldo (on NVIDIA Nemotron 3 Nano) plans search cheaply and hands off to frontier models [V3]
  [B11] [A25].
- Company facts (VENDOR): $300M ARR (May 2026), 85%+ of customers use Glean in 5+ departments [B10];
  Glean Partner Network launched 2026-08-25 with Referral, Commercial, Services and Solutions,
  Technology pathways [B3]. 2026 partner award winners: Bain, Deloitte, AHEAD, Alchemy, EggNest,
  Caylent, Carahsoft, KK Ashisuto, Inco, Softcat [B4].

---

## 23. Unverified or conflicting (never state as fact)

- Exact per-run agent tool-call cap and response-size cap; MCP rate limits; FlexCredits per MCP call;
  FlexCredit dollar price; Protect+ price.
- Whether Claude Desktop's Glean integration still supports only `search`, `chat`, `read_document`. <!-- VALIDATE-OK[identity]: product name, not an operator path -->
- `meeting_lookup` confirmed only via a mirror of Glean's Claude plugin skill file.
- Glean Intelligence auto-routing: beta (Alchemy) versus GA (The Ravit Show).
- Whether Slack RTS reduces ranking quality versus the old indexed connector.
- Glean FedRAMP status.
- Forecastable's MCP server as a custom remote MCP inside Glean: not tested. Glean supports custom
  remote MCP servers; OAuth compatibility with app.forecastable.com/mcp is unconfirmed.
- HubSpot refresh cadence (absent from Glean's table).
- DaVita headcount in the keynote (17,000 vs 70,000 in the transcript).

---

## Sources

Glean docs (VENDOR). Prefix `https://docs.glean.com/`. Raw Markdown at the same path plus `.md`; full
index at `llms.txt`.

| Tag | Path |
|---|---|
| D1 | get-started/welcome |
| D2 | get-started/prepare/items-to-prepare |
| D3 | get-started/prepare/about-deployment |
| D4 | get-started/review/crawling-and-learning |
| D5 | get-started/golive/roll-out-glean-to-teammates |
| D6 | get-started/golive/launch-preparation |
| D7 | get-started/golive/populate-content |
| D8 | get-started/golive/deploy-apps |
| D9 | get-started/setup/configure-sso |
| D10 | administration/identity/sso/about |
| D11 | administration/identity/people-data/troubleshooting/sso-vs-people-data |
| D12 | get-started/setup/sync-people-data |
| D13 | administration/identity/people-data/user-aliases |
| D14 | administration/identity/roles/admin-roles |
| D15 | administration/identity/roles/user-roles |
| D16 | administration/identity/roles/manage-users |
| D17 | administration/identity/roles/group-based-permissions |
| D18 | connectors/about |
| D19 | connectors/getting-started |
| D20 | connectors/crawling-refresh-rates |
| D21 | connectors/crawler-and-indexing-limits |
| D22 | connectors/custom/about |
| D23 | connectors/native/salesforce/about |
| D24 | connectors/native/salesforce/choose-your-setup |
| D25 | connectors/native/hubspot/about |
| D26 | connectors/native/slack/setup/slack-rts-connector |
| D27 | connectors/native/gdrive/about |
| D28 | connectors/native/gong/overview |
| D29 | connectors/native/jira |
| D30 | connectors/native/zendesk |
| D31 | administration/search/about |
| D32 | administration/search/hiding-content |
| D33 | administration/search/access-verification |
| D34 | get-started/golive/setup-glean-assistant |
| D35 | agents/how-agents-work |
| D36 | agents/auto-mode-agent |
| D37 | agents/concepts/schedule-triggers |
| D38 | agents/concepts/content-trigger |
| D39 | agents/concepts/limits-and-best-practices |
| D40 | administration/managing-agents/agent-access |
| D41 | administration/managing-agents/review-and-publish-agents |
| D42 | administration/managing-agents/agent-routing |
| D43 | administration/managing-agents/knowledge-profiles |
| D44 | agents/concepts/publish-slack |
| D45 | administration/agent-identity/overview |
| D46 | agents/agent-development-lifecycle/adlc |
| D47 | administration/tools |
| D48 | administration/tools/managing-tools/tool-visibility-scoping |
| D49 | administration/tools/managing-tools/run-without-user-confirmation |
| D50 | tools/human-in-the-loop-experience-for-tools |
| D51 | administration/tools/supported-mcp-servers |
| D52 | administration/tools/connect-remote-mcp-servers-to-glean |
| D53 | administration/platform/mcp/about |
| D54 | administration/platform/mcp/create-mcp-servers |
| D55 | administration/platform/mcp/best-practices |
| D56 | administration/platform/mcp/host-guides/claude-desktop | <!-- VALIDATE-OK[identity]: product name, not an operator path -->
| D57 | administration/platform/mcp/agents-as-tools |
| D58 | administration/platform/mcp/mcp-gateway |
| D59 | administration/platform/mcp/glean-plugin |
| D60 | docs-mcp |
| D61 | user-guide/mcp/sales |
| D62 | administration/platform/a2a-host |
| D63 | administration/llms |
| D64 | administration/llm-key-feature-availability |
| D65 | administration/model-exclusion |
| D66 | glean-enterprise-flex-pricing |
| D67 | administration/management/usage/set-usage-limits-and-alerts |
| D68 | administration/management/usage/flexcredits-dashboard |
| D69 | administration/protect/overview |
| D70 | administration/protect/ai-security/agent-access-policies |
| D71 | administration/protect/ai-security/restricted-topics |
| D72 | administration/management/audit-logs/admin-audit-logs |
| D73 | administration/assistant/configuration/chat-history |
| D74 | administration/agent-trace-export |
| D75 | administration/insights/overview |
| D76 | administration/insights/departments-and-managers |
| D77 | administration/insights/agents |
| D78 | user-guide/assistant/skills |
| D79 | administration/managing-skills/skills-roles |
| D80 | administration/assistant/configuration/content-restrictions |
| D81 | administration/platform/embedded-integrations/slackbot |
| D83 | glean-core-suite-pricing |
| D84 | administration/configure-llms |
| D85 | connectors/excluding-content |
| D86 | administration/platform/mcp/analytics |

Glean blog and press (VENDOR). Prefix `https://www.glean.com/`.

| Tag | Path |
|---|---|
| B1 | blog/from-enterprise-search-to-enterprise-context-what-ai-agents-actually-need |
| B2 | blog/go-glean-cowork (token-efficiency benchmark vs Claude Cowork) |
| B3 | blog/glean-partner-network |
| B4 | blog/2026-glean-partner-award-winners |
| B5 | blog/enterprise-search-evaluation-2026 |
| B6 | blog/glean-databricks-isv-ai-visionary-partner-of-the-year-2026 |
| B7 | blog/glean-agents-dec-drop-2025 |
| B8 | blog/glean-skills-launch-2026 |
| B9 | press/glean-unifies-sales-context-for-ai-powered-revenue-teams |
| B10 | press/glean-surpasses-300m-arr-unrivaled-enterprise-context-fuels-ai-adoption |
| B11 | blog/waldo-launch |
| B12 | blog/live-spring-26-main |
| B13 | blog/mcp-mar-drop-2026 |
| B14 | press/glean-launches-global-partner-network-to-scale-its-growing-enterprise-ai-ecosystem |

Video (YouTube IDs; `https://www.youtube.com/watch?v=`).

| Tag | ID | What | Label |
|---|---|---|---|
| V1 | vGmmt7p2Hyk | Glean:GO 2026 keynote | VENDOR |
| V2 | 5w1Is9TaC1c | Canva Prompted, Arvind Jain | INDEPENDENT host |
| V3 | 6q33c2M-mlg | Composio, Arvind Jain | INDEPENDENT host |
| V4 | 1csags-vTCI | FirstMark MAD podcast (April 2025) | INDEPENDENT host |
| V5 | J8hFAOoUEM0 | TechCrunch Equity | INDEPENDENT host |
| V6 | 1ZMDA6atOhc | Greylock, Glean and Cresta | INDEPENDENT host |
| V7 | GuwoULakxdY | Glean:GO Day 1 afternoon keynote | VENDOR |
| V8 | wyoNrTx08dA | Harvey on Unprompted | VENDOR |
| V9 | nWkwo4QLarA | Token Economy webinar | VENDOR |
| V10 | CVJVfCi_e0s | Managing AI webinar | VENDOR |
| V11 | Vd5-rsmLtLA | July Drop: Enterprise-ready skills | VENDOR |
| V12 | NY8gftpN8q4 | Arize Observe 2026, Eddie Zhou | INDEPENDENT host |
| V13 | QSwURbfiTqI | Alchemy, 10 rollout tips | PARTNER |
| V14 | nU1L3iN-Srk | Alchemy In the Lab with Glean | PARTNER |
| V15 | p_xtCne1Tdo | Cloud Ace hands-on test (Japanese) | PARTNER |
| V16 | u2_N1xsBfrU | Proactive and predictive AI (no transcript) | VENDOR |

Partners and practitioners (PARTNER unless noted).

| Tag | URL |
|---|---|
| P1 | https://alchemytechgroup.com/blog/10-tips-for-a-successful-glean-deployment |
| P2 | https://alchemytechgroup.com/blog/glean-go-conference-2026 |
| P3 | https://alchemytechgroup.com/blog/when-glean-needs-snowflake |
| P4 | https://alchemytechgroup.com/blog/glean-2026-delivery-excellence-partner-of-the-year |
| P5 | https://www.ahead.com/resources/how-ahead-is-building-an-ai-ready-workforce-from-the-inside-out/ |
| P6 | https://www.ahead.com/news/ahead-named-collaboration-partner-of-the-year-in-inaugural-glean-partner-awards/ |
| P7 | https://www.eggnest.ai/project-services |
| P8 | https://www.eggnest.ai/advanced-services |
| P9 | https://www.ashisuto.co.jp/cm/glean-blog/ai-agent/ai-agent-ashisuto01.html |
| P10 | https://www.ashisuto.co.jp/cm/glean-blog/ai-agent/glean-agent-automode.html |
| P11 | https://www.ashisuto.co.jp/pr/west/article/column-202403.html |
| P12 | https://www.ashisuto.co.jp/english/partner/202507-glean.html |
| P13 | https://www.carahsoft.com/glean |
| P14 | https://community.glean.com/public/resources/what-does-a-realistic-from-contract-to-first-value-timeline-look-like-for-glean-2026-04-23 (VENDOR community) |
| P15 | https://www.bridgeitconsulting.com/insights/glean-custom-connector-backstop-integration |
| P16 | https://www.knostic.ai/blog/glean-data-security (security vendor) |
| P17 | https://www.gend.co/blog/glean-insights-admin-chat |

Analysts, ecosystem, reviews.

| Tag | URL | Label |
|---|---|---|
| A1 | https://tei.forrester.com/go/Glean/workAIplatform/ | VENDOR-commissioned |
| A2 | https://www.gartner.com/en/documents/8322953 | INDEPENDENT (paywalled) |
| A3 | https://www.gartner.com/reviews/market/enterprise-ai-search/vendor/glean | INDEPENDENT |
| A4 | https://www.bain.com/insights/ai-enterprise-code-red/ | INDEPENDENT |
| A5 | https://www.bain.com/insights/what-is-an-ai-native-enterprise/ | INDEPENDENT |
| A6 | https://www.databricks.com/dataaisummit/session/search-sql-how-glean-tap-databricks-genie-everyday-analytics | PARTNER |
| A7 | https://docs.databricks.com/aws/en/ingestion/lakeflow-connect/glean | PARTNER |
| A8 | https://www.vendr.com/marketplace/glean | INDEPENDENT |
| A9 | https://www.sentra.app/articles/glean-pricing | INDEPENDENT |
| A10 | https://www.gosearch.ai/blog/glean-pricing-explained/ | COMPETITOR |
| A11 | https://www.g2.com/products/glean-technologies-glean/reviews | INDEPENDENT |
| A12 | https://aws.amazon.com/marketplace/reviews/reviews-list/prodview-3hxyfnuih42u2 | INDEPENDENT |
| A13 | https://discoverai.tools/articles/glean-ai-review-2026 | INDEPENDENT |
| A14 | https://saas-expert.com/articles/glean-review/ | INDEPENDENT |
| A15 | https://cybernews.com/ai-tools/glean-ai-review/ | INDEPENDENT |
| A16 | https://www.moveworks.com/us/en/resources/blog/the-best-enterprise-search-software | COMPETITOR |
| A17 | https://www.getguru.com/alternatives/glean | COMPETITOR |
| A18 | https://help.crossbeam.com/en/articles/12601327-crossbeam-mcp-server | PARTNER (Crossbeam) |
| A19 | https://www.crossbeam.com/product-updates/crossbeam-mcp-server-bring-your-ecosystem-into-your-ai-tools | PARTNER (Crossbeam) |
| A20 | https://www.nightfall.ai/blog/100-saas-apps-one-query-zero-alerts-how-glean-and-claude-cowork-expose-the-agentic-ai-data-risk | security vendor |
| A21 | https://www.stackone.com/blog/best-mcp-gateway-for-glean/ | COMPETITOR-adjacent |
| A22 | https://techcrunch.com/2026/02/15/the-enterprise-ai-land-grab-is-on-glean-is-building-the-layer-beneath-the-interface/ | INDEPENDENT |
| A23 | https://github.com/gleanwork/claude-plugins | VENDOR |
| A24 | https://www.computerworld.com/article/4005509/salesforce-changes-slack-api-terms-to-block-bulk-data-access-for-llms.html | INDEPENDENT |
| A25 | https://blogs.nvidia.com/blog/nemotron-open-models-ai-trust-control-customize/ | PARTNER |

[PDF brief] = the "Glean AI Content Creators and Enterprise Implementation Best Practices" research
brief Alex supplied on 2026-09-26 (ChatGPT-generated synthesis; used for frameworks, not facts).
