# Clay Intelligence

Version: 2026-10-04. Next refresh due: 2026-11-04 (monthly).
Owner: Forecastable. Audience: Eva (partner-operations assistant) and Forecastable implementation leads.

How to read this file:

- Every fact carries a source tag like `[C7]`. Section 11 maps tags to URLs and the date read.
- Source labels: **VENDOR** (Clay wrote it), **PARTNER** (Crossbeam, a Clay Solutions Partner, or an
  integration vendor), **INDEPENDENT** (press, practitioner blogs, review sites). Clay docs are VENDOR
  but are treated as the operating truth for settings and limits; Clay marketing claims (customer
  outcomes, coverage percentages) are flagged VENDOR inline.
- **UNVERIFIED** marks anything not confirmed by a primary source. Section 12 lists what to confirm in
  a live workspace before telling a customer it is true.
- Clay ships weekly (section 10). Prices, plan gates, model names and limits are true as of the version
  date only. Clay's own pages disagree with each other in several places (row limits, plan names);
  conflicts are called out where they occur, never silently resolved.

---

## 0. The twelve things that matter most

1. **Clay is a spreadsheet-shaped orchestration layer over 150+ data providers plus AI agents**, not a
   database you buy contacts from. Value comes from waterfalls (try provider A, then B, then C, pay
   only on a hit), Claygent research and pushing results into CRM, sequencers and ads (VENDOR) [C11]
   [C53] [C63].
2. **Pricing changed on 2026-03-11.** The single "credits" meter split into **Actions** (platform
   work, fractions of a cent each) and **Data Credits** (third-party data, a few cents each). Self-serve
   plans are Free, Launch ($185/mo monthly, $167/mo annual), Growth ($495/mo monthly, $446/mo
   annual), Enterprise (custom) [C1] [C2] [C3] [C6]. Legacy Starter/Explorer/Pro customers keep their
   plans until they change anything; modern-feature access for them ends 2026-12-31 [C4].
3. **Bring-your-own API keys are no longer free.** BYO keys remove the Data Credit cost but still
   consume 1 Action per enrichment [C2] [C6].
4. **Crossbeam to Clay is one-way, inbound, and needs Crossbeam Supernode.** Clay has a Crossbeam
   source ("Import from Crossbeam", overlaps by partner and population, default limit 1,000 overlaps)
   and an action ("Enrich Company with Partner Data", partner relationship status for a domain). OAuth
   once per workspace. Nothing writes back to Crossbeam [C38] [C39] [C40] [C42].
5. **Clay has an official remote MCP server**: `https://api.clay.com/v3/mcp`, OAuth 2.1 with Dynamic
   Client Registration and PKCE, hosted only [C9] [C15]. It is built for reps doing 1 to 20 records
   at a time inside Claude, ChatGPT, Codex, Copilot and Glean, not for bulk work [C11] [C10].
6. **MCP tools as of 2026-10-02:** `search-contacts`, `search-companies`, `search-contacts-by-name`,
   `add-contact-data-points`, plus admin-enabled custom Functions and (Enterprise) Audiences queries.
   The old `find-and-enrich-*` tools are deprecated aliases [C17] [C8] [C7]. Searches are free;
   enrichment and Function runs cost the same credits as in a table [C8] [C7].
7. **Builders use the Agent Plugin and CLI, not MCP.** `clay` CLI plus Public API
   (`https://api.clay.com/public/v0`, header `clay-api-key`) for Claude Code, Codex and Cursor on Mac
   and Linux. The CLI/API **cannot create or write to Clay tables**; it runs searches, Functions,
   Workflows, reads Audiences and (Enterprise) reads tables [C18] [C21] [C24].
8. **Functions are the unit of reuse.** Build an enrichment chain once, call it from any table, from
   MCP, from the API and from Workflows. Launched 2026-04-15, all paid plans, no extra cost beyond the
   enrichments inside [C28] [C29]. Anything Eva should run repeatedly belongs in a Function.
9. **Row limits are the most common surprise and Clay's own pages conflict**: pricing page says Launch
   50,000 rows per table and Growth/Enterprise unlimited; docs say 50,000 rows per table on all plans
   and webhook sources cap at 50,000 submissions for the life of the source unless Enterprise
   auto-delete is on [C1] [C50] [C26] [C51]. Design for 50,000.
10. **Clay has no native event-platform integrations except Sequel.io.** Luma reaches Clay through
    Zapier or the HTTP API column (Luma API needs Luma Plus); Zuddl, Goldcast, Eventbrite and Splash
    have no Clay integration found [C60] [C61] [C62] [C81]. CSV, webhook and Chrome-extension scraping
    are the practical event inputs [C59] [C26].
11. **Credit burn is controlled by run settings, not by hope.** Auto-run is on by default at table
    level; turn it off while building, test on about 10 rows, use "Only run if" conditions, and use
    lookups instead of re-enriching [C51] [C52]. Enterprise gets credit budgets; all modern paid plans
    get per-user MCP limits [C54] [C7].
12. **Sculpt 2026 is Thursday 2026-10-08 at Pier 48, San Francisco** ($600 tickets, Clay Cup with a
    $50K prize pool). Expect launches; refresh this file the week after [C70].

---

## 1. What Clay is and the object model

### 1.1 Company context

- Founded and led by Kareem Amin (CEO) and Varun Anand. Series D of $115M at a $7.1B valuation
  announced 2026-09-09, led by Wellington Management; 17,000+ customers; revenue grew 4x in 2025 and
  passed $100M ARR in December 2025 (company statements via press, VENDOR claims) [C79].
- Stated direction: a "self-learning revenue engine" combining internal data (CRM, calls, email) with
  external signals, while keeping user control over deterministic steps (VENDOR) [C79].

### 1.2 Object model

| Object | What it is | Notes for an operator |
|---|---|---|
| Workspace | Billing and permission boundary; credits, connections, members, MCP settings live here | Roles: Admin, Editor, Viewer (Enterprise only), Sales Rep (MCP and Sequencer only) [C56] |
| Workbook | Container for related tables; the primary unit Enterprise credit budgets attach to [C54] | Add sources and custom signals with `+ Add` inside a workbook [C38] [C33] |
| Table | Spreadsheet of rows; each column is data, a formula, or an enrichment | 50,000-row practical cap (see 0.9); history 30 days on Launch/Growth, 180 days Enterprise, off on Free/Trial [C51] |
| Row | One company, person, job or event record | Webhook rows count against a lifetime 50,000-submission cap per source [C26] |
| Source | What creates rows: Find People, Find Companies, Find Jobs, Google Maps, CSV, Webhook, HubSpot/Salesforce import, Crossbeam, HTTP API, Sequel, signals | Sources can be scheduled to re-run [C50] [C34] [C27] |
| Column types | Text/data, formula, enrichment (provider action), AI (Use AI / Claygent), lookup, write-to-table | Formulas and filters cost nothing [C2] |
| Enrichment | One provider action on a row (email, phone, firmographics, tech stack, CRM write) | Each run costs 1 Action plus provider Data Credits unless BYO key [C2] |
| Waterfall | Ordered set of providers for one data point; stops at the first valid result; optional free "Infer Email" step and validation | "You only pay credits for the provider that finds a match" [C53] |
| Formula | Deterministic transform; can be written in plain language with AI assist | Free [C2] [C52] |
| Claygent | Clay's AI research agent: reads websites, extracts, decides, row by row | Models include Clay Helium, Neon, Argon, Navigator plus OpenAI, Anthropic, Google [C36] |
| Claygent Navigator | Browser-driving Claygent: clicks, fills forms, paginates, reads PDFs | Launched 2025-08-20 at 6 credits per run (legacy credit era); private keys not supported [C37] |
| Sculptor | Natural-language GTM copilot that builds tables, columns and analyses | Free to use (Sculptor itself consumes no Data Credits); changes land in Sandbox mode [C2] [C34] |
| Function | Saved, reusable chain of columns with defined inputs and outputs | All paid plans; "Enable for MCP" exposes it to reps; unlimited rows via passthrough [C28] [C7] |
| Workflow | Node graph started by a trigger; moves one record at a time down a path (open beta) | Nodes: Run enrichment, Run Claygent, Conditional, Run code (Python), Run function, Update audience members, Delay (max 60 min) [C30] |
| Audiences | Persistent people/company data layer unifying CRM, warehouse and Clay data, with segments and sync-back | Growth: up to 250,000 CRM/warehouse records, daily refresh; Enterprise: up to 25M records, 15-minute refresh [C31] |
| Signals | Monitored changes: new hires, promotions, job changes, news and fundraising, plus custom signals and web intent | Frequency-based scheduling only, 24-hour minimum for custom signals [C32] [C33] |
| Sequencer | Clay's own email sequencer (up to 4 emails per campaign) | 1 Action per lead sequenced [C57] |
| Clay Ads | Audience sync to LinkedIn, Meta, Google, Bing, Vibe, Reddit | Growth and Enterprise [C58] |

### 1.3 Plan matrix (modern plans, read 2026-10-04)

| Capability | Free | Launch | Growth | Enterprise | Source |
|---|---|---|---|---|---|
| Price, monthly billing | $0 | $185/mo | $495/mo | Custom, annual | [C3] [C6] |
| Price, annual billing (10% off) | $0 | $167/mo | $446/mo | Custom | [C1] |
| Actions per month (base) | 500 | 15,000 | 40,000 | 100,000+ (custom) | [C1] [C2] |
| Data Credits per month | 100 | 2,500 to 10,000 (slider) | 6,000 to 100,000 (slider) | 100,000+ | [C1] [C2] |
| Rows per table | 200 (pricing page) | 50,000 | Unlimited per pricing page; 50,000 per docs | Unlimited per pricing page; passthrough via auto-delete | [C1] [C50] [C51] |
| Seats and tables | Unlimited | Unlimited | Unlimited | Unlimited | [C1] |
| Phone enrichment | No | Yes | Yes | Yes | [C1] |
| Job signals | No | Yes | Yes | Yes | [C1] |
| Web intent signals | No | No | Yes | Yes | [C1] |
| CRM auto-sync | No | No | Yes | Yes | [C1] |
| HTTP API integration | No | No | Yes | Yes | [C1] |
| Ad audiences | No | No | Unlimited | Unlimited | [C1] [C58] |
| Audiences CRM/warehouse import | No | Clay DB and CSV only | 250,000 records, daily | 25M records, 15 min | [C31] |
| Sequencer | No | Yes | Yes | Yes | [C57] |
| Functions | No | Yes | Yes | Yes | [C28] |
| Workflows | Limited | Yes | Yes | Yes | [C30] |
| MCP "Enable for MCP" and credit controls | No | Yes | Yes | Yes | [C7] |
| Audiences via MCP | No | No | No | Yes | [C7] |
| Tables API (read) | No | No | No | Yes | [C24] |
| Credit budgets | No | No | No | Yes | [C54] |
| SSO, RBAC, Viewer role, dedicated CSM | No | No | No | Yes | [C1] [C56] |
| Webhook auto-delete (passthrough) | No | No | No | Yes | [C26] [C51] |
| Trial | 14 days, 1,000 Data Credits, webhooks, CRM integrations, sequencers, HTTP API; no phone enrichment | | | | [C3] |

Plan-name trap: many Clay docs and partner pages still say "Explorer" or "Pro" (legacy names). The
HubSpot and Salesforce integrations are documented as "Pro plan or higher" [C45] [C46]; Crossbeam's
help article says "Clay Pro" [C39]. On modern plans CRM auto-sync is Growth [C1] [C6]. Treat "Pro" as
Growth and "Explorer" as Launch when translating, and confirm (section 12).

---

## 2. Pricing and credits

All prices USD, read 2026-10-04 from clay.com/pricing and Clay docs unless stated.

### 2.1 Timeline

- **2026-03-11:** Clay announced the new model (Actions plus Data Credits; Launch $185, Growth $495)
  (INDEPENDENT reporting) [C6].
- **2026-04-10:** after this date any plan change forces migration to modern plans; legacy customers
  cannot switch between legacy plans or return [C4].
- **2026-12-31:** legacy Starter, Explorer and Pro lose temporary Growth-level access to Audiences,
  Sequencer v2, Workflows and MCP/CLI/API, reverting to free-plan versions of those features; data is
  kept. Legacy Enterprise is grandfathered with no sunset [C4] [C30].

### 2.2 The two meters

| | Actions | Data Credits |
|---|---|---|
| Measures | Platform orchestration work | Third-party data purchases and AI token use |
| Unit cost | "A few tenths of a penny"; "less than $0.01 each and get cheaper with scale" | "A few pennies"; from $0.05 each with volume discounts |
| Consumed by | Every enrichment from any provider, AI runs, signals, Slack/email/Notion sends, Clay Sequencer (1 per lead added), external sequencer exports (1 per record), CRM and warehouse exports and syncs, HTTP API calls, ad audience exports | Marketplace enrichments (unless BYO key), AI usage |
| Not consumed by | | Sourcing lists, imports, formulas, filters, manual entry, Sculptor, audience creation |
| Rollover | None; reset each billing cycle | Monthly plans: up to 2x the monthly allocation; Enterprise/annual: up to 15% of prior year's purchase when renewing at equal or higher tier |
| Typical per-record | | 6 to 20 Data Credits for a typical enrichment; 0.5 to 10+ per single enrichment |

Sources: [C1] [C2] [C3]. Clay says plans are sized so "90% of customers will never hit a usage limit"
(VENDOR) [C1].

### 2.3 Slider defaults and overages

- Pricing page slider defaults: Launch "15K/mo ($60/mo)" actions and "3K data credits/mo"; Growth
  "40K actions/mo ($205/mo)" and "6K data credits/mo" [C1]. The pricing summary lists Launch base at
  2,500 Data Credits [C1] [C2]; the slider default of 3K is how the page renders today. Quote the
  2,500 base and confirm in the live slider.
- Overage: one-time top-ups at a **30% premium** (legacy plans: 50%) on Launch and Growth; automatic
  top-ups available on paid self-serve plans (Auto Top-Ups shipped week of 2026-09-14); maximum top-up
  across both meters 4x monthly allocation (10x on a "Flex" plan); caps of $1,000 per top-up and $5,000
  per 7-day window. Enterprise top-ups are custom [C1] [C2] [C4] [C48]. The "Flex" plan is mentioned
  only in the credits doc (UNVERIFIED as a purchasable plan).
- Mid-cycle upgrades: unused credits become invoice credit, not rollover; prorated refunds for upgrades
  shipped week of 2026-08-24 [C3] [C48].
- Legacy reference: legacy plans used a single credit at roughly $0.07 to $0.08 (Starter tier) and
  $0.012 to $0.016 (Pro tier) per credit; legacy annual discount 10% [C4].

### 2.4 AI pricing

| Model | Content generation (Data Credits) | Web research (Data Credits) |
|---|---|---|
| Clay Helium | n/a | 1 |
| Clay Argon | n/a | 3 |
| GPT-4o | 1 | variable |
| GPT-5.1 | 2 | variable |
| Claude 4.5 Haiku | 1 | variable |
| Claude 4.6 Opus | 7.5 | variable |

- About 80% of models are fixed price; about 20% (token-heavy) are variable at 0% markup. Variable runs
  withhold an estimate (75th percentile of past runs times row count) and refund the difference [C5]
  [C1].
- If the Data Credit balance hits zero mid-run, processing stops; no charge beyond balance [C5].
- BYO model keys are supported; Clay claims its pooled keys run "up to 2x faster" due to negotiated
  rate limits (VENDOR) [C5]. Open-weight Claygent models (Kimi K2.6, GLM 5.2) added 2026-07-16 for
  cheaper research [C48].
- Workflows: Claygent steps cost about one Action; `Run code`, deterministic conditionals and writing
  back to Audiences are free [C30].

### 2.5 Other metered items

- Web intent: 1 Action per successful IP enrichment plus provider Data Credits; IPs cached 30 days;
  "Waterfall" de-anonymization is 5 to 10x cheaper than "Best Match" [C35].
- Clay Ads: regular syncs 1 Action per exported record; enhanced matching 1 to 2 credits per row (good)
  or 2 to 3 (best) [C58].
- MCP: no surcharge; a Function costing 12 credits in a table costs 12 via Claude or ChatGPT [C7].
  First MCP connection grants 500 free Clay credits; upgrading to a paid plan from that path adds 2,000
  [C11] [C12]. One practitioner reports MCP Function calls at "20 to 100 credits per call"
  (INDEPENDENT, UNVERIFIED) [C16].
- Third-party estimates of total cost of ownership exist but are not used here; quote list prices only.

---

## 3. Access paths for an agent

### 3.1 Which path for which job

| Job | Path | Why |
|---|---|---|
| Rep asks about 1 to 20 accounts or contacts in chat | Clay MCP for reps | Governed by admin-enabled Functions and per-user budgets [C10] [C11] |
| Run a standard enrichment chain on a list from code or an agent | Public API or CLI, Routines (Functions) | Async, batch over JSONL, webhook on completion [C20] |
| Build or change tables | Clay web app (or Sculptor) | CLI/API cannot create or write tables [C18] |
| Push records into a table from another system | Table webhook source, Zapier "Create Record in Table" | Real-time JSON POST [C26] [C61] |
| Call any external API from inside a table | HTTP API column (Growth+) | GET/POST/PUT/DELETE with rate-limit settings [C27] [C1] |
| Read table results into a dashboard or app | Tables API (Enterprise, read-only) | Structured query, 100 rows per page [C24] |

### 3.2 Clay MCP server (for reps)

- **Endpoint:** `https://api.clay.com/v3/mcp`. Hosted only; self-hosting not supported [C9] [C8] [C15].
- **Auth:** OAuth. Discovery by unauthenticated POST to the endpoint; Dynamic Client Registration at
  `https://api.clay.com/oauth/register`; authorization code plus PKCE at
  `https://app.clay.com/oauth/authorize`; token at `https://api.clay.com/oauth/token`. Confidential
  clients use `client_secret_basic` or `client_secret_post`; public clients use PKCE with
  `token_endpoint_auth_method: none`. The authorizing person must be a member of the selected
  workspace. Sessions expire after 14 days of inactivity [C9].
- **Clients:** Claude (official connector, web, desktop, mobile, Claude Code, API), ChatGPT, Codex <!-- VALIDATE-OK[identity]: public list of supported MCP client apps, not an operator path -->
  (since 2026-06-02), Microsoft Copilot / Microsoft 365 Copilot, Glean, Cursor, VS Code, Claude
  Desktop, and other OAuth-registering clients [C7] [C8] [C14] [C48]. Clay is also on Glean's <!-- VALIDATE-OK[identity]: public list of supported MCP client apps, not an operator path -->
  supported remote-MCP list (Forecastable Glean file, 2026-10-02) [C80].
- **Claude setup:** Free, Pro and Team users add Clay from the Claude Connectors page; Enterprise
  needs an admin to add the connector first [C12] [C11].
- **Tools (2026-10-02):** `search-contacts`, `search-companies`, `search-contacts-by-name`,
  `add-contact-data-points`. Legacy `find-and-enrich-*` ("Find and Enrich list of contacts") still
  answer as compatibility aliases with deprecation notices [C17]. A "List Subroutines" tool lists
  available Functions; each admin-enabled Function appears as a callable tool; Enterprise adds
  read-only Audiences queries [C8] [C7]. Advanced Search (cross-entity companies, people and jobs, OR
  filters) became default in MCP the week of 2026-08-31; reconnect if new tools do not appear because
  hosts cache tool lists [C47].
- **Costs:** people/company search and Audiences queries are free; live enrichment and Function runs
  consume credits at table rates [C8].
- **Result limits:** groups of 20, up to 100 per search (5 pages of "Load more") [C8] [C12].
- **Governance (Settings, MCP users):** default workspace credit limit, per-user overrides, limit 0
  hard-blocks a user, monthly reset on the 1st at midnight UTC, "Allowed MCP clients" allow-list,
  Function allow-listing ("Enable for MCP" / "MCP for reps" toggle), Sales Rep role (MCP only, no web
  app), Enterprise toggles to sync user IDs from Audiences and allow querying all accounts [C7] [C8]
  [C13]. Every MCP user needs an explicit workspace invite even with SSO [C8].
- **Function exposure checklist:** a Function shows in Clay but not in Claude or ChatGPT unless it has
  a name, a description and an output column and the MCP toggle is on. Use the `MCP Caller Email`
  input to know which rep called it [C8].
- **Known errors:** 403 on `/backend-api/ecosystem/call_mcp` in ChatGPT means the OpenAI admin
  disabled the Clay app or its actions; "Unverified application" consent screen is expected for
  self-registering clients; Viewer role cannot complete OAuth (use Sales Rep or Editor); a rep who
  connected before accepting the invite lands in a personal workspace (disconnect, accept, reconnect)
  [C8]. Claude Code registering as "Claude" can be rejected with "Client name must not impersonate a
  known platform"; workaround is `npx -y mcp-remote https://api.clay.com/v3/mcp` in `.mcp.json`
  (INDEPENDENT, 2026-07-22) [C16].
- **What reps cannot do:** browse tables, see raw table data, or use integrations the admin did not
  enable. MCP-triggered actions do not show in the Audiences Activity UI [C8].
- **Scale boundary:** Clay positions MCP for 1 to 20 contacts and exploratory work; 20+ records,
  automation and deep CRM sync belong in the platform [C11]. Claude can parse an uploaded CSV and call a
  Function per row, but there is no dedicated upload path [C8].

### 3.3 Agent Plugin, CLI and Public API (for builders)

- **Install (Claude Code):** `/plugin marketplace add clay-run/agent-plugins` then
  `/plugin install clay@clay-plugins`; Codex: `codex plugin marketplace add clay-run/agent-plugins`.
  Supported in Claude Code, Codex and Cursor; Mac and Linux only (Windows via WSL) [C18] [C19].
  Latest release seen: clay-cli-v0.1.14 (2026-07-09) [C19].
- **CLI auth:** `clay login` (browser) or `clay login --device` (headless, shipped week of
  2026-07-27); check with `clay whoami`; create API keys with `clay api-keys create` (shown once)
  [C18] [C48].
- **Public API:** base `https://api.clay.com/public/v0`, header `clay-api-key`; keys at Settings,
  Account, API keys (beta). Keep keys server-side [C21].
- **What it can do:** searches (advanced query language), run Clay-managed and custom Functions
  ("Routines") on 1 to 100 items async, batch runs over uploaded JSONL via presigned URL, build and run
  Workflows (alpha/beta), read and segment Audiences, create and manage signals, build and edit
  Sequencer campaigns, read workspace credit balances, query tables (Enterprise) [C18] [C20].
  **Cannot** create tables or write rows [C18].
- **Search quotas:** Free 50 results per request, 100 per month; Trial 50 per request, 10,000 per 14
  days; Paid 500 per request, 1M per year; Enterprise 500 per request, 10M per year [C18].
- **Rate limits:** enforced per workspace; HTTP 429 with `Retry-After` (required) and optional
  `X-RateLimit-Limit`, `X-RateLimit-Remaining`, `X-RateLimit-Reset`; CLI exit code 4. Back off with
  jitter; no numeric limits published [C23]. Max 20 concurrent batch runs per workspace (raised from 2
  in June 2026); inline runs do not count [C25].
- **Outbound webhooks (API):** fire when a routine run finishes; payload `webhookId`, `createdAt`,
  `data.routine_run_id`; HMAC-SHA256 signature in `X-Clay-Signature` as `sha256=<hex>`; "Webhook
  delivery is not guaranteed", so keep polling as a fallback [C22].
- Costs: same credits and actions as in-product; no API surcharge [C18].

### 3.4 Table webhooks (inbound)

- Add with `+ Add`, search "Webhooks", "Monitor webhook"; Clay gives a URL and cURL sample; JSON POST;
  optional auth token shown once [C26].
- **50,000 submissions per webhook source, lifetime; deleting rows does not reset it.** Non-Enterprise
  must create a new webhook after that. Enterprise auto-delete ("passthrough tables") processes, sends
  on and deletes rows once the table passes a 5,000-row threshold [C26] [C51]. Auto-delete warnings
  shipped 2026-05 and 2026-08 [C48].

### 3.5 HTTP API column (Growth and up)

- Enrichment mode (per row) or source mode (creates rows). Methods GET, POST, PUT, DELETE. Store
  headers in a workspace "HTTP API (Headers)" account instead of plain-text fields. Rate limit setting
  as "Request limit" per "Duration (ms)" (10 per second = 10 per 1,000 ms). Retry on failure is
  configurable. Source mode paginates by query param, body param or next URL, up to 50,000 rows [C27].
  1 Action per call [C2]. JWT-authenticated variant exists [C48].

### 3.6 Zapier and other automation

- Clay Zapier actions: Create Record in Table, Update Record in Table, Find Row in Table, Find User,
  Find Select Option ID [C61]. This is how Luma "Guest Registered" can feed a Clay table without code.

---

## 4. Integrations catalog relevant to partner teams

### 4.1 Crossbeam (in detail)

| Item | Detail | Source |
|---|---|---|
| Direction | Crossbeam to Clay only. No write-back to Crossbeam | [C38] [C39] |
| Source | "Import from Crossbeam" (Crossbeam's help calls it "Crossbeam Source"): imports accounts that overlap with a partner | [C38] [C39] |
| Source inputs | Organization, Partner (optional), Populations, Limit (default and maximum 1,000 overlaps per the Clay doc) | [C38] |
| Action | "Enrich Company with Partner Data": all Crossbeam partners related to a company and the relationship status (Customer, Prospect, Opportunity) | [C40] |
| Action inputs | Organization, Company domain, Partner (optional), Partner populations | [C38] |
| Fields returned | "All fields available through Crossbeam's account overlaps endpoint", including partner owner, record email, record website, Crossbeam ID | [C38] [C39] |
| Auth | OAuth to Crossbeam once; no re-auth per table; "Bring Your Own Account Required" | [C38] [C40] |
| Setup | In Clay only; nothing to configure in Crossbeam. Workbook `+ Add`, search Crossbeam, connect, set inputs. Existing table: Actions, Import, Crossbeam Source | [C38] [C39] |
| Multiple partners | One Crossbeam source per partner in the same table | [C38] [C39] |
| Freshness | Auto-update option; new matching accounts flow into the table and can trigger downstream columns | [C38] [C39] |
| Crossbeam plan | Supernode minimum (Crossbeam help, updated 2026-07-23; the Claybook also names Supernode). Crossbeam's pricing page puts its REST API on Supernode and Enterprise; Connector ($4,800/yr) gets "unlimited integrations" for outbound tools but Clay is not named | [C39] [C42] [C44] |
| Clay plan | Crossbeam's help says "Clay Pro" (legacy name). Clay's action page says "Available on All Plans". The Claybook lists Clay "Free tier" | [C39] [C40] [C42] |
| Credit cost | Not documented. Expect at least 1 Action per enrichment run under the modern model (UNVERIFIED) | [C2] |
| Shipped | Product roundup 25.Q2.4, 2025-06-06 | [C41] |
| Crossbeam marketing claims | "75+ enrichment tools", AI outreach at scale (PARTNER) | [C43] |

**Claybook: "Find overlapping accounts with Crossbeam and automate personalized outreach"** [C42]:
(1) copy template; (2) Import from Crossbeam for one partner; (3) connect Salesforce twice (account
details, then contacts) or HubSpot/Pipedrive; (4) write contacts to a second table; (5) formula labels
each account joint customer, high-intent prospect or partner customer, then subject and body prompts
with conditional messaging; (6) Outreach (or Salesloft) columns for prospect lookup, update, mailbox
lookup and add-to-sequence.

Practical implications for Forecastable:

- A customer on Crossbeam Free or Connector cannot use the native Clay source per Crossbeam's own
  article. Workarounds: Crossbeam CSV export into Clay, or Crossbeam's outbound integrations that land
  overlap data in the CRM, then a Clay CRM source (both UNVERIFIED as Crossbeam-sanctioned paths).
- The 1,000-overlap limit means big partners need population-level splits or several sources.
- Clay never updates Crossbeam. Results go to CRM, sequencer, Slack, or Forecastable via HTTP API.
- Crossbeam also runs its own MCP server (Supernode-effective); an agent can read overlaps there
  directly and use Clay MCP for people and enrichment, without a Clay table [C80].

### 4.2 CRMs

| CRM | Actions | Sources | Auth and plan | Gotchas |
|---|---|---|---|---|
| HubSpot | Create object, Look up object, Update object, Create association, Get associated objects, Find owner, Add record to list, Enroll contact in sequence, Get enrollment status | Import objects | OAuth with required read scopes (`crm.lists.read`, `crm.objects.contacts.read`, `crm.objects.companies.read`, `crm.objects.leads.read`, `crm.objects.owners.read`, `crm.schemas.companies.read`, `crm.schemas.contacts.read`); optional write scopes on by default; custom object and sequence scopes off by default. "Pro plan or higher" (legacy name) | Enabling custom-object scopes on a non-Enterprise HubSpot portal breaks authorization. Subdomain handling options for company domains [C45] |
| Salesforce | Lookup records via SOQL, Create record, Lookup record, Upsert object, Update record, Convert lead; Pardot (Account Engagement) create, update by ID, upsert by email, list ops (GA week of 2026-08-31) | Import from list view or report; SOQL as source (Jan 2026) | User OAuth or Client Credentials (My Domain, consumer key/secret). "Pro plan" (legacy) | Reports cap at 2,000 records; integration/API-only users and SSO-enforced users must use Client Credentials; "Approve uninstalled connected apps" permission needed. Restricted-user guide exists [C46] [C47] [C48] |
| Audiences sync | Salesforce import and export; HubSpot import only; Snowflake, BigQuery, Databricks, Gong, CSV | | Growth 250,000 records daily; Enterprise 25M, 15 min; weekly full re-imports | HubSpot is one-way into Audiences; write back to HubSpot from tables instead [C31] |
| Others | Attio (push and pull, 2026-03-27), Pipedrive (Claybook), Microsoft Teams, Notion, Google Docs/Slides/Sheets | | | [C48] [C42] |

### 4.3 Event platforms

| Platform | Clay path | Notes |
|---|---|---|
| Sequel.io | Native. Sources: "Find Sequel events by company ID", "Pull attendees from Sequel event"; action "Find Sequel events by ID" | Attendee fields include attendance, registration date, engagement and lead scores, live and on-demand view duration, poll responses, questions, chat. Read-only. Auth by sign-in or Client ID/Secret [C60] |
| Luma | No native integration found. Zapier: Luma triggers (Guest Registered, Guest Updated incl. check-in, Ticket Registered, Event Created/Updated) into Clay "Create Record in Table" | Or HTTP API column against Luma's API, which requires Luma Plus on the calendar; 200 req/min per calendar key, 500 per organization key [C61] [C62] |
| Zuddl, Goldcast, Eventbrite, Splash, Bizzabo, ON24 | No Clay integration found on Clay's integrations page or docs (2026-10-04) | Use CSV export, the platform's webhooks into a Clay webhook source, Zapier, or HTTP API (UNVERIFIED per platform) [C81] |
| Any event website | Clay for Chrome autodetects lists (speakers, sponsors, exhibitors) and sends to a table; Clip to Clay saves pages | Plan limits not documented [C59] |
| Typeform, RSS, Mixpanel, RB2B, Trigify, Apify | Native sources and actions useful for registration forms, social listening and scraping | [C48] and docs index |

### 4.4 Sequencers and engagement

Native Clay Sequencer [C57]; HubSpot sequences enrollment [C45]; Outreach and Salesloft (Claybook)
[C42]; Smartlead, Instantly, Salesforge, Woodpecker, Email Bison, Nooks (2026-08), Gong Engage and
Sendoso appear in the changelog [C48] [C63].

---

## 5. Core recipes an operator needs

### 5.1 Build a safe table (every time)

1. Create the workbook and table; add the source (CSV, Find People/Companies, CRM, Crossbeam).
2. **Turn table-level auto-run off** before adding enrichments (it is on by default) [C51] [C52].
3. Add a dedupe rule (Table settings, Auto-dedupe on the key column; blanks and cells over 200
   characters are skipped) [C51].
4. Add enrichments; set each column's "Only run if" condition and "Keep existing results" [C51] [C52].
5. Run on about 10 rows; check outputs and the credit usage dashboard [C52].
6. Turn auto-run back on only when the table is final. Use Sandbox mode for changes to live tables
   (100% rollout, 2026-06) [C48].

### 5.2 Work email waterfall

Enrichment "Work Email"; Quick setup or Full configuration; map first name, last name and **domain
(mandatory)**; optional free Infer Email step first; choose validation strategy Conservative, Balanced
or Aggressive (or Advanced). Pay only for the provider that matches; validation costs extra but less
than running unpaired providers [C53].

### 5.3 Qualify before you pay

Put a cheap AI or formula ICP check (Helium at 1 credit for web research, or a formula at 0) before
email and phone waterfalls, and gate the waterfalls with "Only run if ICP = yes" [C5] [C52]. Use
lookups against CRM or other Clay tables to skip already-enriched records [C52].

### 5.4 Save a chain as a Function and expose it to reps

Select the columns, right-click, "Save as function"; set name, description, inputs (domain, name,
LinkedIn URL) and outputs; test in Edit Mode (testing shipped week of 2026-08-17); in Settings, MCP
users, toggle "Enable for MCP"; set rep budgets [C28] [C29] [C7] [C48].

### 5.5 Push to HubSpot without duplicates

Look up object (by email or domain) first; branch: Update object if found, Create object if not; then
Create association (contact to company); optionally Add record to list or Enroll contact in sequence.
Keep custom-object scopes off unless the portal is HubSpot Enterprise [C45].

### 5.6 Salesforce upsert

Prefer Upsert object on an external ID; use Lookup records via SOQL for exact matching; batch mode is
available for Create, Update and Upsert. For integration users, use Client Credentials [C46].

### 5.7 Crossbeam overlap to outreach (partner co-sell)

1. Source: Import from Crossbeam, one partner, chosen populations (Supernode needed) [C38] [C39].
2. Formula: classify overlap type (their customer and our prospect, joint customer, etc.) [C42].
3. Find People at each account (title filters) then work email waterfall [C53].
4. Use AI column: draft a partner-referencing opener, conditional on overlap type [C42].
5. Look up and upsert to CRM; enroll in sequence or post to Slack for the AE.
6. Optional: HTTP API column to create the record in Forecastable (Forecastable's API, not Clay's;
   design, UNVERIFIED end to end).

### 5.8 Enrich a known account list with partner context

Action "Enrich Company with Partner Data" with Organization, domain and partner populations returns
which partners hold the account and in what status [C40] [C38]. Use it to tag event attendees,
inbound leads or target account lists with partner coverage.

### 5.9 Signals

Tools, Signals on a table of people (professional social URLs) or companies (website or social URL);
pick new hires, promotions, job changes, or news and fundraising; set frequency (frequency only, not a
specific time); preview; add downstream enrichments [C32]. Custom signals monitor websites, social,
tech adoption, hiring, RSS on a schedule (24-hour minimum) [C33].

### 5.10 Web intent (Growth and up)

Install the snippet before `</body>` on all pages (direct, GTM or Segment); results are company-level
only, grouped by domain, up to 30-minute delay; choose Waterfall de-anonymization [C35].

---

## 6. Event workflows in Clay

Clay has no "event" object. Events are run as tables fed by CSV, webhooks, Sequel, Zapier or
scraping, plus Claygent research and signals. Sources below; Forecastable-specific combinations are
labeled **Forecastable design** (not a Clay claim).

### 6.1 Pre-event

| Step | How in Clay | Source |
|---|---|---|
| Build the target list for a named event | Sculptor "Generate event leads": give event and title ("VP of Sales at SaaStr companies"); searches Clay's company DB, reads sponsor and exhibitor pages with Claygent, waterfalls 150+ providers for verified email; one-click sync to sequencers and CRMs | VENDOR [C63] |
| Get the sponsor, speaker, exhibitor list | Clay for Chrome autodetects lists on the event site and sends them to a table; or Instant Data Scraper CSV into Clay | [C59] [C66] [C67] |
| Attendee list | **No native attendee scraping.** Workarounds: LinkedIn posts by keyword about the event, then Enrich Profile; or the organizer's export | INDEPENDENT [C66] [C67] |
| Booth and meeting targeting | Score companies for ICP fit with an AI column, match titles to personas, then find contacts and generate a reason to meet tied to the event | INDEPENDENT [C69] |
| Partner overlay | Forecastable design: run "Enrich Company with Partner Data" on every sponsor and registrant domain to tag which partners own the account, then route invites through the partner's AE | [C40] |
| Registration intake | Webhook source or Typeform source, or Luma via Zapier; Claybook "Enrich and score event signups" (ICP scoring prompt, title verification, pitch generated only for ICP matches; runs on Free) | [C26] [C61] [C64] |

### 6.2 During the event

- Badge scans, booth forms or Luma check-ins (Luma "Guest Updated" fires on check-in) post into a
  webhook or Zapier-fed table; Clay enriches and alerts the rep in Slack in near real time [C61] [C26].
- Mind the 50,000-submission webhook cap and auto-run settings before doors open [C26] [C51].

### 6.3 Post-event

| Step | How in Clay | Source |
|---|---|---|
| Pull who actually attended (virtual) | Sequel "Pull attendees from Sequel event" with engagement, view duration, polls, questions, chat | [C60] |
| Enrich attendees | Template "Enrich webinar attendees with verified emails, LinkedIn profiles, and company details" (Google Sheets export) | VENDOR [C65] |
| Score and tier | Engagement score (session duration, Q&A, polls) plus ICP and signals; Tier 1 within 2 hours, Tier 2 within 24 hours, Tier 3 nurture | INDEPENDENT [C68] |
| Follow up | Clay Sequencer (1 Action per lead), HubSpot "Enroll contact in sequence", or Outreach/Salesloft columns | [C57] [C45] [C42] |
| Find more people at engaged accounts | Find People at the attendee's company plus event-mention LinkedIn posts | INDEPENDENT [C67] |
| Retarget | Clay Ads segment of attendees and lookalike accounts to LinkedIn (account audiences) and Meta | [C58] |

Forecastable design for partner-hosted events: one table per event; columns: registrant, domain,
Crossbeam partner data (status per partner), ICP score, attendance (Sequel/Luma), follow-up owner
(our AE or partner AE by overlap type), CRM upsert, Forecastable record via HTTP API. Expose the
enrichment chain as a Function so Eva can run it on a single attendee through Clay MCP.

---

## 7. Limits, gotchas and admin pitfalls

### 7.1 Credit burn

- Auto-run is on by default at table, column and conditional levels; adding rows to a live table
  fires every enrichment [C51]. Disable while building; filtered views run only visible rows [C52].
- BYO keys still cost Actions since 2026-03 [C2].
- Web intent "Best Match" costs 5 to 10x "Waterfall" [C35].
- Variable-priced AI models hold credits upfront at the 75th percentile times rows; a big run can look
  blocked before refunds land [C5].
- Signals, sequencer leads, CRM syncs, HTTP calls and ad exports all consume Actions, which do not roll
  over [C2].
- Tools: Credit Usage Dashboard with spend attribution and time series, credit spike alerts (2026-08),
  table credit dashboard, connection usage traces (2026-09), credit spend limits [C48]. Credit budgets
  (Enterprise only) track Data Credits only, not Actions; they block, they do not reserve; reset Never,
  Monthly, Quarterly or Annual [C54].

### 7.2 Row and volume limits

| Limit | Value | Source |
|---|---|---|
| Rows per table | 200 Free (pricing page; FAQ says 50 for trial/free), 50,000 Launch; Growth and Enterprise "unlimited" per pricing page but 50,000 "across all plans" per Sources doc | [C1] [C78] [C50] |
| Webhook source | 50,000 submissions lifetime; Enterprise auto-delete bypasses | [C26] |
| HTTP API as source | 50,000 rows | [C27] |
| Salesforce report import | 2,000 records; list views 50,000 | [C46] [C50] |
| Crossbeam source | 1,000 overlaps limit setting | [C38] |
| Functions | Unlimited rows via passthrough (previously 50,000) | [C28] |
| Workflows | No row caps; 5 MB per record per step; delay max 60 minutes | [C30] |
| MCP results | 20 per page, 100 per search | [C8] |
| API page size (tables) | 100 | [C24] |
| Concurrent API batch runs | 20 per workspace | [C25] |
| Sequencer | 4 emails per campaign; reply events 15 to 30 minutes late | [C57] |
| Audiences fields | about 70 per type non-Enterprise, 135 Enterprise; 600 string fields after a July 2026 increase (conflict, UNVERIFIED) | [C31] [C48] |

### 7.3 Dedupe and data freshness

- Auto-dedupe keeps oldest or newest; ignores blanks and cells over 200 characters [C51].
- Enrichment results are point-in-time. Use scheduled sources and scheduled columns to refresh;
  Audiences re-imports weekly and refreshes daily (Growth) or every 15 minutes (Enterprise) [C50]
  [C31]. Clay's public FAQ still says scheduled re-enrichment is "actively being worked on" and CRM
  two-way sync is every 24 hours; that FAQ appears older than the docs (stale, do not quote) [C78].
- Web intent IP results cached 30 days [C35].

### 7.4 Integration gotchas

- HubSpot custom-object scope on a non-Enterprise portal breaks OAuth [C45].
- Salesforce SSO-enforced and API-only users cannot do browser OAuth [C46].
- MCP rep connected before accepting invite ends up in a personal workspace [C8].
- MCP tool lists are cached by hosts; reconnect after Clay ships tool changes [C47].
- Crossbeam source needs Crossbeam Supernode [C39].
- Table history: off on Free/Trial, 30 days Launch/Growth, 180 days Enterprise; Table versioning and
  changelog shipped 2026-03-23 [C51] [C48].

### 7.5 LinkedIn, email and phone compliance

- Clay supplies features, customers carry compliance: DNC scrub at least every 28 days before calling
  (optional 14-day), maintain internal opt-out lists, remove opt-outs before any further outreach,
  document and audit. Meer integration flags DNC status [C55].
- Clay's docs include B2B email direct-marketing best practices and Clay Ads compliance guides [C48]
  (not read in full; UNVERIFIED detail).
- LinkedIn: Clay offers LinkedIn-derived enrichment and monitoring (LinkedIn Monitoring, Feb 2026)
  [C48]. Scraping LinkedIn posts or attendee lists through third-party tools is a practitioner pattern,
  not a Clay feature, and may conflict with LinkedIn's terms; route customers to legal review [C66].
- GDPR: Clay acts as processor; users are controllers [C36] [C13].

---

## 8. Security and terms

- SOC 2 Type II completed, announced 2024-09-09 [C76]. Clay's MCP security doc states SOC 2 Type II,
  ISO 27001 and GDPR/CCPA compliance, TLS 1.2/1.3 in transit and encryption at rest [C13].
- Trust Center: `trust.clay.com` (redirect loop to http on 2026-10-04; could not be read) [C76] [C77].
  Privacy: `privacy.clay.com` [C76].
- AI: "Your data is never used for AI model training"; contracts with AI providers prohibit training
  on customer data [C36] [C13]. Prompts typed in Claude or ChatGPT are governed by that provider's
  agreement, not Clay's [C13].
- Workspace data logically isolated; deletion completes after 30 days [C13].
- Enterprise: SSO, RBAC, Viewer role, IP access restrictions (2026-09), trusted domain access,
  self-serve sign-in controls (2026-09), static IPs for Enterprise integrations (2026-06), sensitive
  connection controls (2026-05), user groups, "Headless CRM mode where no data is stored in Clay"
  [C1] [C48] [C76].
- MCP: tokens scoped per user and workspace; client allow-list; Function allow-list; zero data
  retention available from Anthropic and OpenAI for qualifying orgs [C13] [C8].

---

## 9. Partner/expert program and Sculpt

### 9.1 Clay Partner Program

- Launched 2025-08-19 (announced by Lele Xu and Billie Solomon): **Solutions Partner Program** (GTM
  engineers, consultancies, agencies; replaced the Experts and Enterprise Partners programs) and
  **Integrations Partner Program** (data providers, platforms, APIs) [C72].
- Solutions Partner tiers: Artisan, Advanced Artisan, Studio, Elite Studio [C72] [C73]. Benefits:
  directory listing, certification, beta previews and custom enablement, priority support,
  co-marketing, Partner Growth Fund (amount not disclosed) [C72].
- Directory at clay.com/experts: 186 partners (2026-10-04), filter by expertise, ICP, industry,
  language, pricing, minimum engagement; Elite Studio examples The Kiln, RevPartners, Growth Engine X,
  Frontal AI, FullFunnel, Go Nimbly; apply via Typeform; a "Matchmaking agent" matches buyers [C73].
- Example: demandDrive became a Clay Studio Partner on 2026-05-05 (PARTNER) [C74].
- Tyler Swanson's LinkedIn headline reads "Head of Solution Partners @ Clay" (search snippet only;
  profile not read) [C75].
- Forecastable angle (design): a partner-data specialization (Crossbeam overlaps into Clay) is not a
  listed directory filter; Studio-tier criteria are not public (UNVERIFIED).

### 9.2 Sculpt

- Sculpt 2025: Clay's first annual user conference, 2025-09-17, San Francisco [C71].
- **Sculpt 2026: Thursday 2026-10-08, Pier 48, San Francisco, 8:00 AM to 7:30 PM; $600; three tracks
  (Main Stage, Builder Stage, Roundtables); opening keynote by Kareem Amin; Clay Cup with $50K prize
  pool; speakers from HubSpot, Canva, Figma, Airbnb, NVIDIA.** Sponsors: Platinum Kernel AI; Gold
  Octave, Smartlead, Lusha, People Data Labs, Vibe, Exa, 2x, Intentsify; Silver Surfe, G2, Trestle IQ.
  Refunds: full 30+ days out, 50% at 15 to 30 days, none inside 15; transfers until 7 days before
  [C70].

---

## 10. Changelog of notable 2025 to 2026 changes

| Date | Change | Source |
|---|---|---|
| 2025-02-28 | Scheduled columns and sources | [C48] |
| 2025-04-18 | Signals hub, LinkedIn API, Gong transcripts | [C48] |
| 2025-06-06 | Sandbox Mode, waterfall step pausing, **Crossbeam integration** | [C41] |
| 2025-08-19 | Clay Partner Program (Solutions and Integrations) | [C72] |
| 2025-08-20 | Claygent Navigator (browser agent) | [C37] |
| 2025-09-17 | Sculpt 2025 | [C71] |
| 2025-11-26 | Bulk enrichment, Web Intent | [C48] |
| 2026-01-16 | Clay in ChatGPT, HubSpot Sequences, Gemini 3 Pro | [C48] |
| 2026-01-26 | Clay in Claude | [C49] |
| 2026-01-30 | Credit spend limits, HTTP API as Source, SOQL as Source, saved searches | [C48] |
| 2026-03-11 | **Actions plus Data Credits pricing; Launch $185, Growth $495** | [C6] |
| 2026-03-23 | Table versioning and changelog | [C48] |
| 2026-03-30 | Clay in Claude and ChatGPT V2, Sculptor for Search, email waterfall controls | [C48] |
| 2026-04-10 | Legacy plan changes force migration | [C4] |
| 2026-04-15 | **Functions** GA | [C29] |
| 2026-05 | Table alerts, sensitive connection controls, Sculptor Sandbox mode | [C48] |
| 2026-06-02 | Clay MCP in Codex | [C48] |
| 2026-06 | Static IPs (Enterprise), HubSpot Deals and Salesforce activities in Audiences, HTTP API source pagination, batch run limit raised 2 to 20 | [C48] [C25] |
| 2026-07 | AgentMail inbox as source, Function observability, open-weight Claygent models, CLI device login, Connections page | [C48] |
| 2026-08 | Credit budgets, credit spike alerts, Skills in Claygent Builder, Nooks, signal results in Audiences, prorated upgrade refunds | [C48] |
| 2026-08-31 week | **Advanced Search in Clay MCP**, Pardot GA | [C47] |
| 2026-09-09 | Series D $115M at $7.1B | [C79] |
| 2026-09 | Auto top-ups, self-serve sign-in controls, IP access restrictions, Clay Ads company list sync to LinkedIn | [C48] |
| 2026-10-02 | MCP `find-and-enrich-*` tools replaced by `search-contacts`, `add-contact-data-points`, `search-contacts-by-name` | [C17] |
| 2026-10-08 | Sculpt 2026 (expect launches) | [C70] |
| 2026-12-31 | Legacy self-serve plans lose temporary modern features | [C4] |

---

## 11. Sources

All read 2026-10-04 unless noted.

| Tag | URL | Label |
|---|---|---|
| C1 | https://www.clay.com/pricing | VENDOR |
| C2 | https://university.clay.com/docs/actions-data-credits | VENDOR |
| C3 | https://university.clay.com/docs/plans-and-billing | VENDOR |
| C4 | https://university.clay.com/docs/legacy-plans | VENDOR |
| C5 | https://university.clay.com/docs/ai-pricing | VENDOR |
| C6 | https://www.salesforge.ai/blog/clay-pricing | INDEPENDENT (competitor-adjacent sequencer vendor) |
| C7 | https://university.clay.com/docs/mcp-settings | VENDOR |
| C8 | https://university.clay.com/docs/mcp-troubleshooting-and-faqs | VENDOR |
| C9 | https://university.clay.com/docs/connect-to-clay-mcp | VENDOR |
| C10 | https://university.clay.com/docs/mcp-for-reps-vs-agent-plugin | VENDOR |
| C11 | https://www.clay.com/guides/clay-mcp | VENDOR |
| C12 | https://university.clay.com/docs/using-clay-in-claude | VENDOR |
| C13 | https://university.clay.com/docs/mcp-security-privacy | VENDOR |
| C14 | https://claude.com/connectors/clay | PARTNER (Anthropic directory) |
| C15 | https://mcpservers.org/remote-mcp-servers/clay | INDEPENDENT |
| C16 | https://informgrowth.com/blog/connect-clay-mcp-claude-code-project-scoped (published 2026-07-22) | INDEPENDENT |
| C17 | https://github.com/clay-run/public-docs/pull/3123 (2026-10-02) | VENDOR |
| C18 | https://university.clay.com/docs/clay-api-cli | VENDOR |
| C19 | https://github.com/clay-run/agent-plugins | VENDOR |
| C20 | https://developers.clay.com/llms.txt | VENDOR |
| C21 | https://developers.clay.com/public-api/authentication.md | VENDOR |
| C22 | https://developers.clay.com/public-api/webhooks.md | VENDOR |
| C23 | https://developers.clay.com/public-api/rate-limits | VENDOR |
| C24 | https://developers.clay.com/tables.md | VENDOR |
| C25 | https://github.com/clay-run/public-docs/pull/3126 (2026-10-02) | VENDOR |
| C26 | https://university.clay.com/docs/webhook-integration-guide | VENDOR |
| C27 | https://university.clay.com/docs/http-api-integration-overview | VENDOR |
| C28 | https://university.clay.com/docs/functions | VENDOR |
| C29 | https://www.clay.com/changelog/functions | VENDOR |
| C30 | https://university.clay.com/docs/workflows | VENDOR |
| C31 | https://university.clay.com/docs/audiences | VENDOR |
| C32 | https://university.clay.com/docs/signals | VENDOR |
| C33 | https://university.clay.com/docs/custom-signals | VENDOR |
| C34 | https://university.clay.com/docs/sculptor | VENDOR |
| C35 | https://university.clay.com/docs/website-tracking | VENDOR |
| C36 | https://university.clay.com/docs/ai-in-clay | VENDOR |
| C37 | https://www.clay.com/blog/introducing-claygent-navigator | VENDOR |
| C38 | https://university.clay.com/docs/crossbeam-integration | VENDOR |
| C39 | https://help.crossbeam.com/en/articles/10080441-clay-crossbeam-integration (updated 2026-07-23) | PARTNER (Crossbeam) |
| C40 | https://www.clay.com/integrations/action/enrich-company-with-partner-data-crossbeam | VENDOR |
| C41 | https://www.clay.com/changelog/2025-06-06 | VENDOR |
| C42 | https://university.clay.com/claybooks/find-overlapping-accounts-with-crossbeam-and-automate-personalized-outreach | VENDOR |
| C43 | https://marketplace.crossbeam.com/partners/clay | PARTNER (Crossbeam) |
| C44 | https://www.crossbeam.com/pricing | PARTNER (Crossbeam) |
| C45 | https://university.clay.com/docs/hubspot-integration-overview | VENDOR |
| C46 | https://university.clay.com/docs/salesforce-integration-overview | VENDOR |
| C47 | https://www.clay.com/changelog/product-roundup-week-of-august-31-2026 | VENDOR |
| C48 | https://www.clay.com/changelog (index of entries 2024-12 to 2026-09-28) | VENDOR |
| C49 | https://www.clay.com/changelog/clay-in-claude | VENDOR |
| C50 | https://university.clay.com/docs/sources | VENDOR |
| C51 | https://university.clay.com/docs/table-management-settings | VENDOR |
| C52 | https://university.clay.com/docs/clay-credit-conservation | VENDOR |
| C53 | https://university.clay.com/docs/work-email-waterfall | VENDOR |
| C54 | https://university.clay.com/docs/credit-budgets | VENDOR |
| C55 | https://university.clay.com/docs/dnc-compliance | VENDOR |
| C56 | https://university.clay.com/docs/roles-and-permissions | VENDOR |
| C57 | https://university.clay.com/docs/email-sequencer | VENDOR |
| C58 | https://university.clay.com/docs/clay-ads | VENDOR |
| C59 | https://university.clay.com/docs/clay-chrome-extensions | VENDOR |
| C60 | https://university.clay.com/docs/sequel-integration | VENDOR |
| C61 | https://zapier.com/apps/luma/integrations/clay | INDEPENDENT (Zapier) |
| C62 | https://help.luma.com/p/luma-api | PARTNER (Luma) |
| C63 | https://www.clay.com/tools/generate-event-leads | VENDOR |
| C64 | https://university.clay.com/claybooks/enrich-and-score-event-signups | VENDOR |
| C65 | https://www.clay.com/templates/enrich-webinar-attendees-with-verified-emails-linkedin-profiles-and-company-details | VENDOR |
| C66 | https://pipelinefactory.co/blog/clay-scrape-event-attendee-lists.html | INDEPENDENT |
| C67 | https://www.clayhacker.com/p/maximize-your-upcoming-events-and-conferences | INDEPENDENT |
| C68 | https://www.linkedotter.com/articles/enrich-webinar-attendees-clay-post-event-outbound-2026 | INDEPENDENT |
| C69 | https://fractionaldemand.com/resources/blog/clay-workflow-trade-show-intelligence-dashboard | INDEPENDENT |
| C70 | https://sculpt.clay.com/ | VENDOR |
| C71 | https://www.clay.com/blog/sculpt-announcement-2025 | VENDOR |
| C72 | https://www.clay.com/blog/announcing-the-clay-partner-program | VENDOR |
| C73 | https://www.clay.com/en/experts | VENDOR |
| C74 | https://www.demanddrive.com/insight/demanddrive-joins-clays-partner-ecosystem-as-an-official-clay-studio-partner/ | PARTNER (Clay Studio Partner) |
| C75 | https://www.linkedin.com/in/tyler-swanson1/ (search result title only, not fetched) | INDEPENDENT |
| C76 | https://www.clay.com/blog/clay-is-soc-2-type-2-compliant | VENDOR |
| C77 | https://trust.clay.com/ (redirect loop, not readable on 2026-10-04) | VENDOR |
| C78 | https://www.clay.com/faq (content appears older than current docs) | VENDOR |
| C79 | https://runtimewire.com/article/kareem-amin-clay-115m-series-d-7-1b-valuation | INDEPENDENT reporting VENDOR claims |
| C80 | Forecastable project doc `claude/glean/glean-intelligence.md` (built 2026-10-02), sections 12.2 | Internal |
| C81 | https://www.clay.com/integrations | VENDOR |

Domains not reachable: trust.clay.com (redirect loop), app.notion.com Clay MCP doc (login wall),
LinkedIn profile pages (not fetched).

---

## 12. Open items to confirm live

1. **Row limits by plan:** pricing page (Growth/Enterprise unlimited) versus Sources doc (50,000 on
   all plans) and plans-and-billing (Growth 50,000). Test by importing 50,001 rows in a Growth
   workspace [C1] [C50] [C3].
2. **Crossbeam source plan gates on both sides:** does the native source work for Crossbeam Connector
   or only Supernode, and which modern Clay plan (Crossbeam says legacy "Pro"; Clay says all plans)?
   Is the 1,000-overlap limit a default or a hard maximum [C38] [C39] [C40]?
3. **Crossbeam action cost:** Actions only, or Data Credits too [C2]?
4. **Full MCP tool list** in a live Claude connection after the 2026-10-02 rename, including the exact
   name of the Function-listing tool ("List Subroutines" in docs) [C17] [C8].
5. **MCP credit cost per call** (independent claim of 20 to 100 credits per Function call) [C16].
6. **Launch Data Credit base:** 2,500 (docs) versus 3K slider default (pricing page) [C1] [C2].
7. **"Flex" plan** with 10x top-up cap: does it exist as a purchasable plan [C2]?
8. **Audiences field limits:** about 70/135 per type versus 600 string fields after July 2026 [C31]
   [C48].
9. **HubSpot and Salesforce plan gate** in modern terms (assumed Growth via "CRM auto-sync"; Launch may
   still allow manual CRM actions) [C1] [C45] [C46].
10. **Trust Center contents** (ISO 27001 report, subprocessors, data residency) once trust.clay.com
    loads [C77].
11. **Event platforms:** confirm no native Luma, Zuddl, Goldcast, Eventbrite or Splash actions exist in
    the in-app Enrich tab (the website catalog may lag the app) [C81].
12. **Sculpt 2026 announcements** (2026-10-08): pricing, MCP, Workflows GA, partner program changes.
    Refresh this file by 2026-10-12.
13. **Tyler Swanson's scope** (Solutions Partners only, or also integrations) and Studio-tier criteria
    [C75] [C72].
14. **Public API numeric rate limits** (not published) [C23].
