---
name: crossbeam-admin-reference
description: Eva's Crossbeam administrator reference. Plan gating, setup from scratch, data sources, sharing, lists, integrations, attribution, Copilot, exports, roles, symptom-first troubleshooting and analysis plays. Built from the full Crossbeam Academy catalog (75 courses) and the full Crossbeam Help Center (about 220 articles) plus the Partner API reference, as of September 25th, 2026. Companion to the "Crossbeam MCP mechanics" section of the Eva skill, which covers the MCP side.
source: Crossbeam Academy (75 courses), Crossbeam Help Center (all 15 collections plus linked articles), developers.crossbeam.com, extracted September 25th, 2026
---

# Crossbeam Admin Reference for Eva

How to use this file. Eva reads the MCP mechanics section of her skill for anything she pulls through the MCP. She reads this file for everything a Crossbeam admin does: standing an instance up, fixing it when it breaks, and turning its data into a recommendation. This file is the index and the fast answer. The deep detail lives in the six library files listed below; open the one that matches the question before giving step-by-step instructions or diagnosing an error string.

Rules for using it:
- Answer from this file and the library first, cite the Help Center article as (HC number), and fall back to `search_crossbeam_knowledge` for anything newer than the extraction date or not covered here.
- The UI moves often. Account Mapping Reports became Lists in February 2026 and Shared Lists became Static Lists. Name the screen and the article, and say when a step may have moved.
- Where two Help Center articles disagree, the library records both. Say so, give both values, and tell the customer to confirm in-app rather than picking one silently.
- Plan gating decides most answers. Check section 1 before recommending anything.

Help Center links are `https://help.crossbeam.com/en/articles/<number>`.

## 0. The library (open the file that matches the question)

| File | Covers |
|---|---|
| `crossbeam-hc-data-sources-populations.md` | Plans and trials, navigation, AI Chat, every data source (Salesforce, HubSpot, Dynamics, Pipedrive, Snowflake, Databricks, Google Sheets, CSV), Populations and Population Types, the matching engine (domain, name, DUNS), missing and incorrect overlap diagnosis, error strings for every connector, dependency map, numbers cheat sheet |
| `crossbeam-hc-sharing-partners-account.md` | Sharing model and Sharing Hub, field presets, data share requests, partner connection lifecycle, offline, managed offline and Open Data Partners, Shared Lists, Attribution, Gong, Ecosystem Intelligence, seats, roles and every permission, plans, billing and Crossbeam Credits, Record Exports, SAML SSO and SCIM, notifications, Audit Logs, privacy and security |
| `crossbeam-hc-lists-analysis-ai.md` | Lists (all types, access levels, notes, exports), List notifications, Account Mapping Matrix, Account Mapping Pass, how overlap numbers are calculated, Potential Revenue, Partner Score and Partner Impact, Deal Navigator, Pipeline Generation and Net New Accounts, Performance Dashboard, AI Hub and MCP credits, release notes newest first |
| `crossbeam-hc-integrations.md` | Salesforce managed package v2 and v1, custom object and reauthorization, Enhanced Ecosystem Reporting fields, Partner Field Mapping, Partner Account CRM Integration, Product2, SF reporting, HubSpot and Dynamics custom objects, Snowflake and Databricks push, Matillion, REST API, Ecosystem Signals, Clay, PartnerStack, Marketo, Slack, AI Agents, Universal Integration Settings, SSO exception user |
| `crossbeam-hc-sales-copilot.md` | Crossbeam for Sales and Sales Settings, co-selling templates and Get Intel, Messages, sales notifications, Pipeline Generation, Deal Navigator, Performance Dashboard, Dynamic Shared Lists, Copilot on Salesforce, HubSpot, Chrome, Gong and Outreach, AI Recommended Plays, SCIM roles |
| `crossbeam-hc-api-webhooks-legacy.md` | Partner REST API (auth, headers, pagination, every endpoint), Signals webhooks and payloads, Deal Alerts (beta), legacy features and how to recognize a customer still on them, Clari |

## 1. Plan and seat matrix (check this before recommending anything)

Most "it doesn't work" questions are really "their plan or seat doesn't include it." Plans: Free (formerly Explorer), Connector, Supernode, Enterprise. Details and sources are in the library.

| Capability | Free | Connector | Supernode | Enterprise |
|---|---|---|---|---|
| Full Access seats | 3 included, no Sales seats | From 1 paid seat, no cap | Minimum 3 | By contract |
| Integration seat (data sources and integrations only, not counted) | No | No | 1 included | 1 included |
| Account Mapping Matrix and List rows | Capped (50 per older articles, 10 per the Lists-era article; confirm in-app) | Full | Full | Full |
| Create, save, share Lists; List notifications | No (can view and contribute to Lists a paid partner shares) | Yes | Yes | Yes |
| Single Partner List | Yes | Yes | Yes | Yes |
| Custom, Greenfield, Ecosystem, Partner Tag, Pipeline Lists | No | Yes | Yes | Yes |
| List exports | Only via an Account Mapping Pass (100 records with a Supernode or Enterprise partner) | Yes, 1,000 rows per export | Yes | Yes |
| Record Export limit per year (integrations, CSV, API, webhooks) | None | 5,000 | Customizable | Customizable |
| Custom Populations | No | Up to 3 | Unlimited | Yes |
| Offline Partners | 1 | Unlimited | Unlimited | Unlimited |
| Open Data Partners | 1 | 1 | 3 | 10 |
| Share All (greenfield sharing) | No | Yes | Yes | Yes |
| Custom roles and groups | No | No | Yes | Yes |
| Partner Score | No | Yes | Yes | Yes |
| Potential Revenue configuration | View only | Yes | Yes | Yes |
| Copilot (Salesforce, HubSpot, Chrome) | Preview / Starter access only | Yes | Yes | Yes |
| Copilot for Gong | No | No | Yes (plus Gong Engage) | Yes |
| Copilot for Outreach | No | No | Yes | Yes |
| Salesforce custom object data push, SF report templates, Enhanced Ecosystem Reporting fields | No | Object installs, no data pushed | Yes | Yes |
| HubSpot and Dynamics custom objects, HubSpot reporting | No | No | Yes | Yes |
| Partner Field Mapping | No | No | Yes | Yes |
| Deal Navigator | Limited rows | Full Access seats | Sales seats, also inside Salesforce | Yes |
| Pipeline Generation, Net New Accounts | Limited | Yes | Yes | Yes, plus Net New Accounts webhook |
| Performance Dashboard | No | No | Yes, Full Access seat only | Yes |
| Attribution and Salesforce Attribution Push | No | No | Yes | Yes |
| Audit Logs (full) | Login events only | Login events only | Yes | Yes |
| SAML SSO | No | No | Yes (one article says Supernode and Enterprise) | Yes |
| SCIM provisioning | No | No | In-app per Feb 2026 release notes | Yes (requires SSO first) |
| REST API and Signals via API | No | No | Yes | Yes |
| Signals via webhook | No | No | No | Yes |
| AI Agents (beta), Universal Integration Settings | No | Yes | Yes | Yes |
| Crossbeam MCP server | Yes, 50 credits a year | Yes, 500 | Yes, 2,500 | Yes, 5,000 |
| Buy credit packs | No | No | Yes | Yes |
| Partner Workshops (Crossbeam Services) | No | Free for first 5 partners | Free for first 5 partners | |

Seats. **Full Access** seats use Crossbeam Core (roles Admin, Standard, Limited). **Sales** seats get Copilot, Deal Navigator, Pipeline Generation, Messages and co-selling templates without Core (roles Manager, Standard, Limited). **Integration** seats see only Data. AI features that spend Crossbeam Credits need a Full Access or Sales seat. MCP credit limits are enforced on all plans from September 1st, 2026, as one org-wide pool; admins see usage on Plan & Billing. Packs for Supernode and Enterprise: 10K for $1,000, 25K for $2,500, 100K for $9,000.

Connector free trial: 30 days, requested from the "Request Free Trial" button once onboarding is complete; 3 users max, 100 records per report export, no integrations (HC 10644667).

Note on conflicts: the Academy said the MCP server was Supernode-only; the Help Center (September 2026) says every plan, credit-metered. Trust the Help Center. Conflicting row values above are marked; the library cites both articles.

---

## 2. Stand up an instance from scratch (the admin runbook)

Order matters. Each step depends on the one before.

1. **Team and roles.** Settings > Team > Invite User (Admin only). The account creator is Admin. There must always be at least one Admin; a sole Admin promotes someone else before changing their own role. Default roles: Admin (system, not editable), Standard User (partner manager template), View Only / Limited User, Sales User (no Core access). On Connector and Supernode create custom roles (Add Role: name, description, permissions) instead of editing defaults. Permissions per feature are No access / View only / Manage. Invites expire after one year. Help 4292722, 3160294.
2. **Data source** (Data > Data Sources). At least one is required, and connecting one shares nothing. See section 3.
3. **Populations** (Data > Populations). Build the three standard populations first: Customers, Open Opportunities, Prospects. Keep them broad and do the narrowing in lists. Add Custom Populations on paid plans. See section 4.
4. **Sharing defaults** (set when saving each population, editable on the Sharing Settings page). Start standard populations at Overlap Counts, then open up per partner. See section 5.
5. **Company profile and discoverability.** Set the org to Discoverable so partners can find you (Partnerbase then lists Crossbeam in your Partner Tech Stack). Claim and correct your Partnerbase.com listing. Help 5392236, 3160299.
6. **Invite partners.** Partners > Add Partner > copy the company invite link, or send a partner-specific invite. Use offline partners for anyone not on Crossbeam. See section 6.
7. **Tags.** Tag every partner (type, tier, owner, region, lifecycle stage, status, specialization). Tags drive Partner Tag lists and surface in Copilot. See section 7.
8. **Org settings.** Settings > Organizational Settings > General: "What CRM do you use?" and "What is your fiscal year?". Required for the Performance Dashboard.
9. **Put data where reps work.** Copilot in Salesforce, HubSpot, Chrome and Gong; Slack app; Crossbeam for Sales (Settings > Sales Settings). See section 9.
10. **Lists and alerts.** Build and save the standard list set with Slack or email notifications. See section 8.
11. **Attribution** (Supernode). Co-Sell data preset, then the Salesforce Attribution Push. See section 10.

---

## 3. Data sources

Supported: Salesforce, HubSpot, Microsoft Dynamics, Pipedrive, Snowflake, Google Sheets, CSV. Request others via Help 3160188. Only CSV does not auto-update. Setup collection: https://help.crossbeam.com/en/collections/1845495-setting-up-data-sources

### Salesforce (Help 3160182, troubleshooting 4136739)
- Data > Data Sources > Salesforce tile. Tick "I am connecting to a Sandbox environment" only for sandbox. Connect Salesforce > OAuth.
- Authorizing user needs API permissions, and the org needs API enabled and "View Setup and Configuration". Reauthorization should be done by a Salesforce admin.
- Choose Recommended or Custom fields > Review Fields > Customize > Sync Now. Status goes "Setting up..." to Active, and an email arrives on completion.
- Minimum fields for mapping and reporting. Account: ID, Name, Website, Type, Created At, Billing Country, Employees, Industry, Owner ID. Opportunity: Account ID, Amount, Close Date, Open Date, Sales Stage, Closed, Won, Name, ID. Contact: Account ID, Email, Name, ID. User: Owner Email, Owner Name, User ID.
- Settings (three dots > Settings): Reauthorize, pause (toggle "Sync Data from Salesforce"), status, Update Frequency (the Academy lists 6h, 12h, 24h, 1 week; the Help Center says 30 minutes to 24 hours, default push every 12 hours; confirm in-app), Edit Data Sync (Customize Fields modal and Data Presets), remove.
- Statuses: Active, Not Syncing (paused), Error (detail shows in the modal and on the Integrations page).

### HubSpot (Help 3160183)
- A HubSpot admin authenticates with their own credentials, so add them as a Crossbeam user first. Data Sources > HubSpot > Connect HubSpot > confirm the portal.
- Settings (gear): reauthorize, pause, status, frequency, Field Sync. Data Presets control shareable field sets.
- Most common failure: the HubSpot admin who connected left or lost rights. A new HubSpot admin must reauthorize.

### Microsoft Dynamics (Help 6952388) and Snowflake (Help 4470887)
Connected from the same Data Sources page. The Dynamics custom object is a separate Supernode integration (section 9).

### Google Sheets (Help 5613345)
- Only ONE user per org can authenticate Google. Every sheet must be shared with that user. Make the Crossbeam admin the authenticator.
- Sheet needs a unique name and at minimum Company Name plus Website (People sheets: email). Unique column headers. Duplicate company names are skipped.
- Do NOT rename mapped headers after mapping or the sync errors.
- Add: Data Sources > Google Sheets > Authenticate with Google > Allow. Then Add > paste URL > pick tab > Companies or People > map Company Name and Website > optional "Map Account Owner Columns" > Add Google Sheet.
- Google Workspace blocking the app: admin.google.com > Security > API Controls > Manage Third-Party App Access > Configure New App > search "Crossbeam" > select all OAuth client IDs > Trusted (the scope is Drive only) > Configure.

### CSV
- Max 15MB. Remove blank rows, columns and cells first. Companies need company name and website columns; People need email.
- The CSV name is visible to partners when you share, so name it plainly ("Customers").
- Does not create a population automatically, and report notifications are disabled for CSV-backed data.
- Add Data appends to an existing file (old plus new). Filter the population on "Upload Time" to show only the newest rows.
- Removing a CSV deletes every population built on it and breaks the lists and threads that used those populations.
- Record export trap: deleting a CSV and re-uploading the same file counts every row as a NEW record.

---

## 4. Populations

- Segments of your accounts or people. The basis for all sharing and mapping, and the thing that makes a Salesforce customer comparable to a HubSpot or CSV partner.
- Builder: Data > Populations > Create (standard) or Create Population (custom). Name, description, data source, object or file or table, Add Table Filters with group logic, Preview, Save Population. Help 3160197, 3160198 (advanced filtering), 3161135 (edit), 3160199 (delete), 3160813.
- Strategy: cast a wide net in populations, then narrow in lists. Narrow populations hide overlaps and waste record exports.
- Custom Population ideas: Closed Lost (partner revives), Churned (win-back through the integration), All Accounts (match without revealing your status), a region like EMEA, an ICP cut (2,000+ employees, revenue, industry). Help 7239725.
- When a partner shares counts only, ICP-shaped custom populations still tell you how many of their overlaps fit your ICP.
- Offline partners get standard populations only, built from their uploaded CSV. Sheet tabs are not imported as populations; rebuild them with filters.

---

## 5. Data sharing

Levels per population:
- **Hidden** (share toggled off): partner cannot see the population.
- **Overlap Counts**: the number only, no account detail.
- **Share Overlaps**: the fields you pick, for overlapping accounts only.
- **Share All**: overlapping and non-overlapping (greenfield) accounts. Needed for Greenfield plays.

Where it is set:
- **Default** per population: applies to every partner. Set at save time or on the Sharing Settings page. Help 4236547, 4236619.
- **Per-partner override**: Partners > Partner List > partner > Settings (or Sharing Settings > pencil per population). Change the level, choose fields, X to stop sharing a population, "+Share another Population" to add a custom one > Save. The "Shared with You" tab shows what they send you.
- **Presets**: Crossbeam's Recommended Fields Preset exists for Salesforce and HubSpot, and you can build your own. The Co-Sell preset is what Attribution needs. Help 11583486.
- **Data Share Requests**: request fields from a partner in-app (Request Data), for example their AE name and email. Incoming requests arrive by email and on the Pending Requests page. Help 3976078, 3976123.
- **Shared Lists** ignore sharing settings. Everything in a Shared List is shared except records carrying opportunity data.

Operating guidance. Tier the sharing (Intercom: counts for Plus partners, detail for Premier). Test new workflows with a trusted partner first. Start minimal and expand. Put a mutual NDA (Bonterms, Common Paper, OneNDA) in the partner agreement.

Admin tell: a partner with a large total overlap count and zero shared overlaps is taking your data and giving nothing back (see MCP note 10).

---

## 6. Partners

- **Invite**: company-specific link (email, Slack, signature, partner page button program, QR) or partner-specific invite, both from Partners > Add Partner. If they are already on Crossbeam, clicking sends you a request to accept. Otherwise they register first. Defaults apply on connect. Help 3160222, 3499611, 7128217 (find partners already on Crossbeam).
- **Offline partners** (partner not on Crossbeam): Partners > dropdown next to Add Partner > name > Create Partner. Then partner > Partner Data > Upload a CSV (company name plus website required, 15MB max) > build standard populations on the Offline Partner Detail Page. Initial record exports count toward the Record Export limit.
- **Vetting a new partner**: ICP overlap, fit to your Ideal Partner Profile per category (tech, channel, strategic), comparable program maturity (buy-in, budget, ops, tooling), mutual understanding of goals, appetite for enablement, ecosystem multiplier. Red flags: no leadership buy-in on their side, you can't state their goals.

---

## 7. Tags

- Tags apply to partners only (not populations or lists). Partner List > grey pencil on a partner > type or pick a tag. Bulk-add to many partners is supported. Edit or delete via the three dots next to the tag. Filter the partner list with AND or OR logic. Help 5467749.
- Tags show in Copilot on paid plans, so tag with the rep in mind (Intercom tags segment, use case and job).
- Recommended taxonomy: type, tier, partner account manager, region, lifecycle stage ("GTM Ready"), active or inactive, specialization. Align with the organization's existing tag vocabulary before inventing new values.

---

## 8. Lists (formerly Reports) and the Account Mapping Matrix

### Account Mapping Matrix (Help 5303061)
Your populations against one partner's, with counts and Potential Revenue. The play for each cell:

| Your side | Partner side | Play |
|---|---|---|
| Customers | Customers | Integration case, case studies, upsell or renewal value |
| Customers | Opportunities | Give the partner intel or an intro (reciprocity) |
| Customers | Prospects | Referral revenue |
| Opportunities | Customers | Ask the partner for intel, procurement insight, a good word |
| Opportunities | Opportunities | Co-sell, solution selling |
| Prospects | Customers | Warm intro, EQL (ecosystem-qualified lead) |
| Prospects | Prospects | Co-marketing, joint ABM |

Matching Engine: proprietary, needs very high confidence before calling a match (Help 3160297). Missing matches are usually bad website data on one side.

### Potential Revenue (Help 6797349)
- Sum of YOUR open opportunity amounts that overlap the partner, per population. The total is not the sum of the matrix cells, because one opportunity can sit in several populations.
- Default open opportunity: stage does not contain "closed" (case-insensitive) and amount > 0. Paid plans can redefine it (Pipeline list > Potential Revenue settings).
- Needs a CRM source syncing opportunity amount and stage. Never shows for CSV or Sheets. Blank for a partner usually means your source is not a CRM or the partner is not sharing.

### List types (Lists tab)
- **Single Partner**: your populations against one partner. All plans. Help 8195191.
- **Pipeline**: Potential Revenue drill-down. Help 8195192.
- **Greenfield**: partner accounts outside your overlaps. "New Accounts for You" (theirs, counts toward export limits) and "New Accounts for Your Partner" (yours, does not). Needs Share All, a trusted partner with a similar ICP, and both sides on Connector or higher. Help 8195198.
- **Ecosystem**: your populations against ALL partners. Ecosystem health and where to focus. Help 8195204.
- **Partner Tag**: overlaps only with partners carrying a tag. Help 8195202.
- **Custom**: anything else. Help 8195206.
- **Deal Navigator**: pipeline-first view for sellers (section 9).

Working a list: add Partner Data columns (partner owner name and email, their segment) if shared. "Your Data" fields come from your sources; "Partner Data" fields come from theirs, filtered by their sharing. Save (rename at top) > Actions > notifications by email or Slack > Save Preferences. Organize into folders; unsaved or unfiled lists sit in the Unfiled tab. Export respects plan limits and partner agreements. Help 3160236.

### The standard list set to build for every customer
1. EQLs: your Prospects x partners' Customers (Ecosystem list), Slack alert on new rows.
2. Deal assist: your Open Opps x partners' Customers and Open Opps, filtered to open stages.
3. Reciprocity: your Customers x partners' Open Opps (what we can give).
4. Mutual customers: Customers x Customers, for integration adoption and case studies.
5. Renewal risk and expansion: your Customers with upcoming renewals x partners' Customers.
6. Per-rep versions of 1 and 2 filtered on account owner, pushed to where the rep works.

---

## 9. Getting data to reps (integrations)

All installs start at Data > Integrations.

### Crossbeam Copilot for Salesforce (Help 3685976; install guides v1 9298987, v2 9280237)
Prereqs: Crossbeam roles Full Access Admin and Sales Manager. Salesforce: installer holds the Crossbeam Setup User permission set, plus Visualforce Page Access and read on Account and Lead for the custom object.
1. Salesforce **custom domain is mandatory** (Setup > Company Settings > My Domain > register > log in to new domain > Deploy to Users).
2. AppExchange > Get it Now > **Install for Admins Only**. "Install for All Users" breaks the permission sets. Approve third-party access (api.crossbeam.com, auth.crossbeam.com, sales-backend-api.crossbeam.com, api.segment.io, sentry.io, login and test.salesforce.com).
3. Assign yourself Crossbeam Setup User (Setup > Users > Permission Sets > Manage Assignments). App Launcher > "Crossbeam Setup" > Get Started > Validate > pick org > Authorize > Finish. Finishing the assistant does NOT make Copilot visible yet.
4. Add the Crossbeam component to the Account, Lead and Opportunity page layouts.
5. Assign permission sets to every user or they see an error:
   - **Crossbeam Setup User**: admins. Required for whoever installs or reauthorizes. Write access to the Crossbeam Ecosystem Overlap object.
   - **Crossbeam Account User**: Copilot access. Needs Crossbeam credentials. Full data only with a paid Core or Sales seat.
   - **Crossbeam Report User**: read the custom object and build reports and dashboards.
   - **Crossbeam Widget Viewer**: sees Copilot, buttons disabled, no partner-shared data.
   - Default for the whole sales team: Account User plus Report User.
6. **Trusted URL** for the Account, Contacts and Plays tabs: Setup > Trusted URLs > New. API Name Crossbeam, URL https://app.crossbeam.com, CSP Context Lightning Experience Pages, CSP directive frame-src. Done by a SF admin with Setup User (no Crossbeam seat needed).
- Supernode can customize what Copilot shows per partner (hide a partner that asked you to hold off).

### Salesforce custom object reports and dashboards (Supernode; Help 4353321, 8765980, v2 settings 8705869)
- Report types: Crossbeam Ecosystem Overlaps, and Overlaps with Account, Lead, or Opportunity. Check for a prebuilt "Crossbeam Reports" folder first.
- Standard builds. **EQLs**: Overlaps with Account; Partner Standard Populations contains Customers; Standard Populations contains Prospects; group by Account Owner, Account. **Top Revenue EQLs**: add Annual Revenue >= threshold. **Open Opps with Partner Overlaps**: Overlaps with Opportunity; partner pops contains Customers, Open Opportunities; stage not Closed Won or Lost; own pops excludes Customers. **Opportunity Influence** by Stage or Owner. **Partner Mutual Customers**. **Expansion Opportunities**. **Aging deals**: open more than 90 days where the account is a partner customer.
- Dashboard components: EQLs, Integration Partners mutual customers, Ecosystem Market Overlap, Partner Influenced Open Pipeline.

### HubSpot (Supernode for reporting; Copilot Help 8940278; custom object Help 7971155)
- **Copilot for HubSpot**: requires Crossbeam for Sales configured, a Full Access or Sales seat, Admin or Sales Manager role with Integrations permission, and HubSpot "App Marketplace Access". Data > Integrations > Crossbeam Copilot for HubSpot > Install > pick portal. In HubSpot it is a right-sidebar card; drag it to the top and use View All.
- **Custom object**: Crossbeam Overlaps associates to Companies, Contacts and Deals only.
- **Reports**: Reporting > Reports > Create report. Single object "Crossbeam Overlaps" (change the default date range "This quarter so far" to All data) or Custom Report Builder with Crossbeam Overlaps as primary (overlaps only) or Companies as primary (to see whitespace).
- **Push to standard objects**: HubSpot Custom Object > Settings > Enable Data Push > Save > Account Object tab > Push to Account Object. Creates "Is a Customer Of" and "Is an Open Opportunity For" company properties, usable in any report, workflow, or downstream tool (Gong, Clari, Gainsight).
- **Push a Crossbeam list to a HubSpot list**: save the list > HubSpot Custom Object > Settings > Re-authorize > pick the list > Next. Updates dynamically. Every pushed record counts toward Record Export limits.
- **Crossbeam 360 Dashboard** in HubSpot: News Feed (partner recently closed or opened a deal on your prospect), Source Opportunities, Influence Deals, Retain and Expand (mutual customers, expansion, integration adoption potential). Use "contains" filters on population names.
- Pair with the `forecastable-hubspot-setup` skill for Forecastable's own property rules.

### Microsoft Dynamics custom object (Supernode; Help 10064960)
Dynamics 365 Sales Professional, Enterprise or Premium. Data > Integrations > Microsoft Dynamics Custom Object > Install > Crossbeam auth > Dynamics auth > instance URL > Create > wait for "Crossbeam Overlap entity is in place" > Finish (if the entity step errors, Previous then Next). Surface on Account pages via Default Solution > Crossbeam Overlaps > Relationships > Account > Display Settings > Publish All Customizations. Add to the Sales Hub nav via Site Maps > Sub Area > Entity: Crossbeam Overlap > Publish.

### Chrome, Slack, Crossbeam for Sales
- **Copilot for Chrome**: Data > Integrations > Install > Chrome Web Store > pin. Alerts when a visited site or LinkedIn page matches an overlap. Help 4779242.
- **Slack app**: install, then notifications are PER SAVED LIST (bell icon > channel). Nothing alerts by default. `/crossbeam` slash command looks up overlaps on demand. Help 3639783, 3640085.
- **Crossbeam for Sales / Sales seats**: Settings > Sales Settings > Finish Setup > company description (partners see it) > Enable Crossbeam for Sales > select partners > confirm standard-population mapping > Confirm and Import Data > Add to Slack > edit Co-Selling Template questions and context (toggle "Allow custom questions").
- **Deal Navigator** (Help 10844915): app.crossbeam.com/deal-navigator/close-deals or the Copilot icon in Salesforce (Supernode, SF as data source). Account Drawer shows partner-shared contacts and partner owners (Details > Owners tab). Add to Shared List from the row.

---

## 10. Attribution, Performance Dashboard, Audit Logs (Supernode)

### Attribution (Help 8042999)
- Setup: sync the Co-Sell data preset. Salesforce Attribution Push: SF must already be the data source, and only a SF admin can install. Data > Integrations > Salesforce Attribution Push > Install. Install the Attribution Object package (Install for Admins Only, review View Components, acknowledge the Non-Salesforce Application banner). Grant profiles access to the object. Back in Crossbeam, Attribution Push > Settings > enter partners' Salesforce Account IDs (optional) > Save.
- Use: Attribute tab shows Total Sourced, Influenced and Unattributed plus time to close (gear customizes). Filter by account, stage, partner or tag, date and amount. Filters live in the URL, so share the link. Open an account > recommended overlapping partners or search > Sourced or Influenced > check Activity > Save.
- Rules: one Sourced partner per opportunity, any number Influenced. The customer defines what each means.

### Performance Dashboard (Help 10845010)
Needs a Full Access seat, a CRM source syncing Amount, Is Closed, Is Won, Name, Owner ID, Close Date and Open Date, and CRM plus fiscal year set in Organizational Settings. Shows partner-influenced against non-partner win rate, deal size and cycle, plus rep engagement (Copilot usage) for coaching.

### Audit Logs (Help 6172688)
Admins or the "View Audit Logs" permission. CSV export delivered by email, covering history since May 28 2021 (metadata, previous state, impacted users and orgs, and IP only since May 11 2022). Covers data sources, sharing, partnerships, populations, invites and roles. First stop for "who changed our sharing?"

---

## 11. Record Exports (Help 8399864)

- Counted: records leaving Crossbeam to integrations, warehouses, CRMs, CSV downloads, and API or webhook reads (see MCP note 12).
- Each unique record counts ONCE per subscription term regardless of destinations, partners or re-exports. Updates do not recount.
- Not counted: Slack, Copilot for Salesforce, Crossbeam for Sales, Deal Navigator, Pipeline Generation, Copilot for Chrome, Greenfield "New Accounts for Your Partner".
- Traps: Greenfield "New Accounts for You" counts. Every record pushed to a HubSpot list counts. A deleted and re-uploaded CSV counts again. Offline-partner initial exports count.
- At 90% a banner appears in Plan & Billing, Integrations and Populations. The Record Export Summary shows unique records per integration, 14-day activity, and unique records per population. At 100% ALL exports stop.
- Conservation: only push populations each integration needs, filter lists before export, keep standard populations broad, and train the team.

---

## 12. Troubleshooting by symptom

| Symptom | Check, in this order |
|---|---|
| Data source shows Error | Connecting user still exists and has rights (SF: API enabled plus View Setup and Configuration; HubSpot: the same admin). Reauthorize from Settings. SF: Help 4136739. No error text but broken: the Crossbeam support inbox (support at crossbeam.com) |
| Data source "Not Syncing" | Sync toggle is paused. Fields cannot be edited while paused |
| Google Sheet stopped syncing | A mapped header was renamed; the sheet is not shared with the one authenticator; the authenticator left the company |
| CSV upload fails | Blank rows or columns, over 15MB, missing company name or website (or email for People) |
| Population count lower than expected | Filters too narrow; CSV "Add Data" appended rows and old ones still match (filter on Upload Time); wrong object or file picked |
| Overlaps with a partner are zero | Is the partner sharing that population, or hiding it? Are your populations built? Website quality on either side (matching engine needs confidence). Explorer 50-row cap? |
| Partner shows counts but no accounts | They share Overlap Counts only. Send a Data Share Request, or build ICP custom populations to read the counts |
| Partner fields missing from a list | They are not sharing those fields. Request Data; agree a field set in the partner plan |
| Potential Revenue blank | Your source is not a CRM; opportunity amount or stage not synced; partner not sharing; opportunities all match "closed" or have $0 amounts |
| No Slack or email alert | Notifications are per saved list and must be switched on. The list must be saved (paid plan). The user needs Manage access on that feature, because view-only users get no notifications |
| A user never gets data source error emails | Their role is View only on Data Sources. Grant Manage |
| Copilot not showing in Salesforce | No custom domain; installed "for All Users"; component not on the page layout; user missing a permission set; setup assistant never completed |
| Copilot Account, Contacts or Plays tabs blank with a config message | Trusted URL for https://app.crossbeam.com (frame-src, Lightning Experience Pages) missing |
| Copilot shows only an overview | User has no paid Core or Sales seat (starter access) or has Widget Viewer |
| Salesforce report type missing | Select "All" in the report type picker; user lacks Crossbeam Report User |
| SF or HubSpot report returns nothing for a partner | Using "equals" on population names. Use "contains" ("Customer" vs "Customers" differ by partner) |
| HubSpot Crossbeam report empty | Date filter still "This quarter so far"; custom object not installed; not on Supernode |
| Duplicated opportunities in SF report | Show Unique Counts |
| Attribution not in Salesforce | Attribution Push not installed, object package not installed, or profiles lack object access |
| Exports suddenly disabled | Record Export limit hit. Open the Record Export Summary and find the integration or population burning records |
| Performance Dashboard empty | Sales seat instead of Full Access; CRM or fiscal year not set in Organizational Settings; opportunity fields not synced |
| "Can't create custom population / greenfield list / folder" | Plan tier (see section 1) |
| Offline partner custom population unavailable | By design; standard populations only |
| "Who changed this?" | Audit Logs (Supernode) |
| Salesforce error string (`invalid_grant`, `API_DISABLED_FOR_ORG`, `REQUEST_LIMIT_EXCEEDED`, `OAUTH_APP_BLOCKED`, over 80% API quota and so on) | Exact cause and fix per string: library `crossbeam-hc-data-sources-populations.md`, Troubleshooting 17.1. Reauthorizing fixes most; quota errors pause sync until the next day |
| Salesforce field shows "Not Supported" or is missing from the picker | Authorizing user lost field access, unsupported field type, or field-level security not Read for that profile (library, 17.2) |
| Only some accounts synced | The authorizing user only sees a subset. Reauthorize with a user with broader visibility |
| Salesforce authorization blocked since September 2025 | Salesforce's uninstalled-connected-app block (HC 12510571) |
| SSO is enforced and an OAuth integration will not authorize | Needs an SSO Exception User (library `crossbeam-hc-integrations.md`, 0.5) |
| A specific account does not overlap | Run the missing-overlap procedure (library, 17.9): account in a Population on both sides, shared on both sides, domains identical (subdomains and different TLDs never match), DUNS stored as text not number |
| A wrong match | Report an Incorrect Match; equal DUNS forces a match (library, 17.10) |
| Snowflake, Databricks, Pipedrive, Dynamics symptoms | Library, 17.4 to 17.6 |
| Custom Population missing from Matrix, Deal Navigator or Performance Dashboard | Population Type not set (or set to Other) |
| MCP calls start failing or AI features stop | Crossbeam Credits exhausted for the year (enforced from September 1st, 2026). Admin checks Plan & Billing; Supernode and Enterprise can buy packs |
| Integration data stopped updating | Record Export limit reached (existing exported data also stops updating), or a reauthorization is needed in Universal Integration Settings |
| Error on a custom object, Slack, API or webhook | Library `crossbeam-hc-integrations.md` and `crossbeam-hc-api-webhooks-legacy.md`, Troubleshooting sections |

When a signal is patchy across a roster, check partner hygiene before blaming the program (MCP note 16).

---

## 13. Analysis playbook: turning the data into a recommendation

1. **Is this partner worth it?** Matrix counts for the cells that match the goal (integration: Customers x Customers; referral: your Customers x their Prospects; co-sell: Opps x Opps). Multiply overlaps by average deal size for the immediately addressable market. Check reciprocity (shared vs total overlaps). Output: invest, maintain, test, or deprioritize, and escalate the judgment call to the partnerships lead.
2. **Integration business case (Friendbuy method).** Mutual customer count, their MRR from the CRM, retention lift, plus open opportunities and mutual prospects for new business. Formula: available shared data + what we need + what they need = partnership plan.
3. **Technographic ICP.** Ecosystem list of your Customers x all partners' Customers. Find partners (or partner combinations) your best customers share, then target prospects who are customers of those same partners.
4. **Deal influence.** Open Opps x partner Customers and Open Opps, filtered to the deal's owner. Ask the partner owner about buying process, procurement, decision makers, timing. Use Deal Navigator for the partner owner.
5. **Reciprocity first.** Before any ask, pull your Customers x their Open Opps for that partner's AE and lead with what you can give.
6. **Rep-level adoption.** Performance Dashboard Copilot usage by rep. Coach low users on one of their own accounts in a 15-minute session. Recognize high users as peer coaches.
7. **Program proof for execs.** Partner-influenced against non-partner win rate, deal size and cycle (Performance Dashboard), plus Attribution sourced and influenced totals. Present it as an executive update, not a data dump.

Benchmarks the Academy cites (use as illustrations, never as the customer's numbers): RollWorks partners influence ~80% of deals, partner-influenced deals +10% ACV and 66% higher close rate, integration users renew ~30% higher. Vidyard ~20% higher reply rate referencing tech stack. Friendbuy +45% outbound opportunities from partner-led messaging. Deel AE: 30% of pipeline partner-sourced, closing 25% higher.

---

## 14. Crossbeam AI and MCP

- Copilot AI plays: generated per account; thumbs feedback or regenerate. View Play Details lists when the play fits and what limits it. Help 9596637.
- Crossbeam AI Chat (all plans): in-app first-line help for how-to and troubleshooting. Help 11731834.
- Crossbeam MCP server: available on all plans since the September 2026 Help Center update, metered by Crossbeam Credits (Free 50, Connector 500, Supernode 2,500, Enterprise 5,000 a year; enforced from September 1st, 2026; packs for Supernode and Enterprise). Needs a Full Access or Sales seat, and the role's MCP permission (on by default). Works in Claude, ChatGPT and Glean. Crossbeam also publishes an MCP Prompt Guide, a skills repo (github.com/getcrossbeam/crossbeam-claude-skills) and AI Playbooks. Per Eva's MCP mechanics section, never build against Crossbeam's published skill files; resolve tools live. Help 12601327, 15588582.
- Credit discipline: every Eva MCP call spends the customer's credits as well as Record Exports. Pull narrow, reuse results, and say so when a sweep would be expensive.
- AI Agents (public beta, Connector and up): Slack alerts on conditions. Ecosystem Signals (Supernode and Enterprise): real-time events by API, and by webhook on Enterprise. Library `crossbeam-hc-api-webhooks-legacy.md`.

---

---

## Coverage and gaps

Captured: the text of all 75 Academy courses (including quizzes, flashcards and linked resources), every article in all 15 Help Center collections plus the articles they link to (about 220), and the full Partner API reference from developers.crossbeam.com. Thirteen linked article numbers now redirect to the Help Center home page (retired articles); they are not in the library.

Not captured: narrated videos and click-through demos, the downloadable PDF checklists and MCP Prompt Guide, and the live event replays. Where a procedure only existed on video, the library summarizes the surrounding text; confirm the click path against the cited article before walking a customer through it.

Refresh: re-pull the Help Center and release notes quarterly, or sooner when a customer reports a screen that does not match.
