<!-- Library file for crossbeam-admin-reference.md. Source: Crossbeam Help Center, extracted September 25th, 2026. Cite (HC number); confirm in-app when a screen may have moved. -->

# F. Crossbeam Partner API, Signals and Webhooks, Deal Alerts, Legacy Features, Clari

Sources: HC 4677142 (REST API), HC 12732223 (Signals via API and webhooks), HC 11464781 (Deal Alerts beta), HC 4236661 (Per-Population Overrides legacy), HC 4353321 (Overlaps custom object in Salesforce legacy), HC 8732549 (Salesforce install legacy), HC 7827330 (Clari), HC 9035095 (Send shared list to account owner legacy), and the developers.crossbeam.com Partner API reference (API docs).

---

> Path shorthand: `{USERS}` means `/v1/users` and `{USERS01}` means `/v0.1/users`. Written this way because the plugin build gate reads the literal path as a home folder.

## 1. REST API and Webhooks

### 1.1 Plan requirements

| Capability | Free | Connector | Supernode | Enterprise | Source |
|---|---|---|---|---|---|
| REST API (raw overlap data) | No | No | Yes | Yes (see note) | HC 4677142, HC 12732223 |
| Signals API endpoint | No | No | Yes | Yes | HC 12732223 |
| Webhook (Signals push) | No | No | No | Yes | HC 12732223, API docs |

- The REST API help article states access "is only available on our Supernode plan" (HC 4677142). The Signals article lists Supernode as "Access to the API (Signals and the API endpoint)" and Enterprise as "Access to the API and Webhook" (HC 12732223).
- The developer docs state "Webhooks are an enterprise only feature" (API docs).
- Free and Connector plans have no access to Signals API or webhooks (HC 12732223).
- Upgrades are done from the Plan and Billing page at app.crossbeam.com/billing (HC 4677142, HC 12732223).
- Only Admin users can create or edit webhooks and API integrations (HC 12732223).
- No additional licenses are required to leverage signals and the webhook. Only Admins create webhooks, but anyone in the organization can benefit from the workflows or alerts they trigger in other tools (HC 12732223).

### 1.2 Record export impact

- REST API calls count toward Record Exports limits (HC 4677142).
- API calls and webhooks are both included in Record Exports limits. The webhook counts toward Record Export limits "just like Crossbeam's existing API" (HC 12732223).
- For help, contact the Crossbeam support inbox (support at crossbeam.com) (HC 4677142, HC 12732223).

### 1.3 Creating credentials (a Custom Integration / Application)

Help Center path (HC 4677142):
1. Click Data in the left navigation, then Integrations.
2. Click + Create Integration.
3. Fill in:
   - Integration name: anything that identifies the app to you.
   - Integration description: optional, 140 characters max.
   - Callback URL: set to `https://oauth.pstmn.io/v1/callback`.
   - Allowed Origins: leave blank.
4. Click Create Integration.

Signals article path (HC 12732223): Data, then Integrations, then +Create New, then API Integration. Define Integration name, Integration description, Callback URL and Allowed Origins. Click Create Integration, then follow the Developer Documentation.

Developer docs path (API docs):
1. Log in and visit app.crossbeam.com/integrations. The custom integration section is labeled `Custom`. Click `Create Integration`.
2. Integration name (any), Integration description (optional), Callback URL `https://oauth.pstmn.io/v1/callback` (for Postman), Allowed Origins blank.
3. Click `Create`, then `View`. Copy the `Client ID` and `Client Secret`.

Note: the `https://oauth.pstmn.io/v1/callback` callback URL is the Postman callback. The docs say an existing application should follow the OAuth 2.0 standards for its own architecture (API docs).

### 1.4 Authentication method

- OAuth 2.0 (API docs).
- Authorization URL: `https://auth.crossbeam.com/authorize?audience=https://api.getcrossbeam.com` (API docs).
- Access Token URL: `https://auth.crossbeam.com/oauth/token` (API docs).
- Access tokens are valid for only 24 hours (API docs).
- To get a refresh token, add `offline_access` to the requested scopes, for example `openid read:partnerships offline_access` (API docs).
- Refresh exchange: POST to `https://auth.crossbeam.com/oauth/token` with header `content-type: application/x-www-form-urlencoded` and form fields `grant_type=refresh_token`, `client_id`, `client_secret`, `refresh_token` (API docs).
- A sample client app (as-is, not for production) is at gitlab.com/crossbeam-public/crossbeam-simple-oauth2 (API docs).
- For Salesforce-style OAuth integrations where SSO is enforced, authorize as the SSO exception user (HC 8732549).

### 1.5 Scopes

Every request needs at minimum `openid`, plus the scopes for the endpoints the token should reach (API docs). Accepted scopes listed in the docs:

| Scope | Used by |
|---|---|
| `openid` | Always required |
| `read:partnerships` | `/v1/partners`, `/v1/partners/:id`, `/v1/partner-tags`, `/v1/partner-populations`, `/v1/partner-populations/:id` |
| `read:reports` | `/v1/reports`, `/v1/records/*`, `/v1/overlaps/*`, `/v1/signals/*` |
| `read:populations` | `/v1/populations`, `/v1/populations/:id` |
| `write:activity-timeline` | Listed as accepted; no endpoint in the reference uses it |
| `offline_access` | Request a refresh token |
| `read:audit-log` | `/v1/audit-logs` (named on the endpoint, not in the general scope list) |

(API docs)

### 1.6 Base URL and required headers

- Base URL: `https://api.crossbeam.com` (all endpoints are under `/v1/`) (API docs).
- The Salesforce package also lists api.crossbeam.com (getting Crossbeam data) and auth.crossbeam.com (authenticating users) as its third-party hosts (HC 8732549).
- Header 1: `Authorization: Bearer <token>` (API docs).
- Header 2, organization selection: `Xbeam-Organization: <organization uuid>`. A Crossbeam user can belong to one or more organizations. Get the list from the users/me endpoint and use the `organization.uuid` from each item in `authorizations` (API docs). The docs spell it both `Xbeam-Organization` and `XBeam-Organization`.
- The general auth section references `{USERS01}/me` for the org list; the endpoint reference is `GET {USERS}/me` (API docs).
- users/me is "the first endpoint you should inspect before others" because it gives the header value (API docs).

### 1.7 Pagination scheme

Cursor based. Paged responses return a top-level `items` array and a top-level `pagination` object with (API docs):
- `next_href`: full URL for the next page, including cursor and all original query params. Preferred.
- `next_cursor`: the cursor value alone.
- `has_more`: `false` is "the only definitive way to know there are no more records."

Rules by endpoint family (API docs):
- `/v1/records/accounts`, `/v1/records/leads`: iterate while `next_href` exists; `null` means end of results. `limit` default 25, max 1000.
- `/v1/audit-logs`: `limit` default 1000, max 1000. When `has_more` is false you have reached the end "for now" and should try again later.
- `/v1/overlaps/accounts`, `/v1/overlaps/leads`: bookmarkable. Page while `has_more` is true using `next_href`. Once `has_more` is false, save `next_href`. Next run returns only new, updated or deleted overlaps. Changes captured include a record value change, a data sharing rule change, a record deletion, and a record creation. Order is not reliable.
- Deleted overlaps come back with `"is_deleted": true` (unshared, removed from a CRM, or moved populations). When syncing elsewhere, confirm the record still exists before deleting it.
- Changing query parameters invalidates the cursor. The endpoint still returns results but will not accurately track changes. Restart with no cursor.
- `/v1/signals/*`: bookmark with `next_cursor` after a full sync. The bookmark returns only signals created since the last sync. If "partner deal name" changed since the last call, that signal is NOT returned again.
- Search endpoints `/v1/overlaps/accounts/search` and `/v1/overlaps/leads/search` are not paged.

### 1.8 Rate limits

"Rate limits are defined in our security policy and are subject to change with our own discretion." No numeric limit is published (API docs). Webhook retries include status `429` (see 1.12).

### 1.9 Endpoint reference

All paths are relative to `https://api.crossbeam.com`. All are GET. (API docs)

| Method | Path | Purpose | Scope | Key params | Notable response fields |
|---|---|---|---|---|---|
| GET | `{USERS}/me` | Your user profile and the organizations you belong to. Call first. | n/a | none | `authorizations[].organization.uuid` (value for `Xbeam-Organization`) |
| GET | `{USERS}/organization/:id` | All users in an organization. Caller must be in that org. | n/a | `:id` = organization UUID | user list |
| GET | `/v1/partners` | Your partners, including tags your users set on them | `read:partnerships` | none | partner info, tags |
| GET | `/v1/partners/:id` | One partner by ID, including tags | `read:partnerships` | `:id` | partner info, tags |
| GET | `/v1/partner-tags` | Partner tags (docs description duplicates the partners/:id text) | `read:partnerships` | none | tags |
| GET | `/v1/populations` | All of your populations | `read:populations` | none | population list |
| GET | `/v1/populations/:id` | One of your populations by ID | `read:populations` | `:id` | population |
| GET | `/v1/partner-populations` | Populations partners chose to share with you | `read:partnerships` | none | partner population list |
| GET | `/v1/partner-populations/:id` | One shared partner population by ID | `read:partnerships` | `:id` | partner population |
| GET | `/v1/reports` | All reports you have created | `read:reports` | none | report list |
| GET | `/v1/records/accounts` | All your account records from your own populations | `read:reports` | `limit` (25 default, 1000 max), `cursor` | `items`, `pagination` |
| GET | `/v1/records/accounts/search` | Search your own account records by domain and company name | `read:reports` | `term` (fuzzy prefix: "wayne" matches wayne.enterprises.com and Wayne Enterprises), `record_id`, `domain`, `opportunity_id`, `contact_id` (exact) | matching account records |
| GET | `/v1/records/leads` | All your lead records from your own populations | `read:reports` | `limit`, `cursor` | `items`, `pagination` |
| GET | `/v1/records/leads/search` | Search your own lead records by email | `read:reports` | `term` (fuzzy prefix), `record_id`, `email` (exact) | matching lead records |
| GET | `/v1/audit-logs` | Org audit log: user-initiated changes, oldest first | `read:audit-log` | `limit` (1000 default, 1000 max), `cursor` | who made the change, when, IP address, what changed, affected users and partners |
| GET | `/v1/overlaps/accounts` | Your records that overlap a partner's ACCOUNTS (your side need not be an account). Includes partner org info and partner populations matched. | `read:reports` | `limit`, `population-ids[]` (your own, repeatable), `partner-id`, `cursor` | see overlap fields below; bookmarkable |
| GET | `/v1/overlaps/accounts/search` | Your records matching a term that overlap a partner's account | `read:reports` | `term`, `record_id`, `domain`, `partner-population-ids[]` (repeatable), `partner-id` | not paged |
| GET | `/v1/overlaps/leads` | Your records that overlap a partner's LEADS (your side need not be a lead) | `read:reports` | `limit`, `population-ids[]`, `partner-id`, `cursor` | overlap fields; bookmarkable |
| GET | `/v1/overlaps/leads/search` | Your records matching a term that overlap a partner's lead | `read:reports` | `term`, `record_id`, `email`, `partner-population-ids[]`, `partner-id` | not paged |
| GET | `/v1/signals/accounts` | Signals where your side of the overlap is an account | `read:reports` | `limit`, `record_id` (repeatable), `population_id` (repeatable), `partner_id` (repeatable), `partner_population_id` (repeatable), `triggered_at[gt\|gte\|lt\|lte\|eq]`, `cursor` | signal fields below |
| GET | `/v1/signals/leads` | Signals where your side of the overlap is a lead | `read:reports` | same as signals/accounts | signal fields below |
| GET | `/v1/signals/own-deals` | Own-direction deal signals: one row per partner overlap on your own open or closed-won deals | `read:reports` | same as above plus `event_type` (`own_deal_opened`, `own_deal_closed_won`, repeatable) | unique `signal_id` per row, shared `event_id` (group by `event_id` to rebuild the aggregate) |

Notes (API docs):
- Search endpoints say they accept "one of two query parameters" but then list more options.
- `triggered_at` filter takes a datetime such as `"2025-10-15T14:59:06.347Z"`. Example: `triggered_at[lt]="2025-10-15T00:00:00.000Z"` returns signals before 15 October 2025 UTC.
- Population filters on signals do not narrow the `populations` / `partner_populations` fields in the response. Those always show every population the record is in.
- Query param naming differs by family: overlaps use hyphens (`population-ids[]`, `partner-id`); signals use underscores (`population_id`, `partner_id`).

#### Overlap response fields (API docs)
- Your side: `record_id`, `record_name`, `record_website`, `crossbeam_record_id`.
- Partner side (always prefixed `partner_`): `partner_record_id`, `partner_record_name`, `partner_record_website`, `partner_record_company_type`, `partner_record_country`, `partner_record_industry`, `partner_record_employees`, `partner_crossbeam_record_id`.
- Anything without the `partner_` prefix is your data.
- `crossbeam_record_id` is Crossbeam's unique ID for a record. Only the combination of `crossbeam_record_id` and `partner_crossbeam_record_id` uniquely identifies an overlap across all Crossbeam customers. Two overlaps can share a `record_id` (external system IDs) and can share a `crossbeam_record_id` (one record can overlap several partners).
- `is_deleted: true` on removed overlaps.
- The endpoint is chosen by the partner's record type: if the partner record is an account, it appears in `/v1/overlaps/accounts`.
- Simplest match example: identical website on both sides (your "Wayne Inc." and partner "Wayne Enterprises" both at `wayne.enterprises`).

### 1.10 Signals: what they are

- A signal is "a data point or behavioral indicator that suggests an opportunity, risk, or next step" (API docs); a data point or event representing meaningful partner activity such as an opportunity opening or closing (HC 12732223).
- Current signals are based on changes in partners' CRM opportunity data. When a partner opens or closes a deal, Crossbeam generates a signal (API docs).
- Requirements on the PARTNER side: have a CRM connected to Crossbeam, and be syncing and sharing Deal open date, Deal close date, Deal is closed, Deal is won (HC 12732223, API docs).
- Your company only needs to sync these fields; you do not need to share them back (HC 12732223).
- Your own data source can be CSV or Google Sheet; you still receive signals as long as the partner has a connected CRM and shares the required fields (HC 12732223).
- Greenfield account signals cannot be pushed "at this time" (HC 12732223).
- Contact info on opportunity signals requires the partner to also sync and share CRM contact data. Required contact fields: Contact Name, Contact Title. Signal contact parameters: `contact_name` (full name), `contact_role` (role at the organization), `contact_type` (decision maker, influencer, buyer). Appears only if the partner is actively sharing (HC 12732223).
- Difference from the existing API: the existing API gives raw overlap data; signals API and webhook give event-based enriched data ("Opportunity Opened", "Closed Won"), real-time push via webhook or on-demand pull, AI-ready formats for Crossbeam's MCP or other AI tools, and structured real-time streams (HC 12732223).

### 1.11 Signal event types and payload fields

Event types:
- Webhook UI choices: Deal opened (partner opens a new opportunity), Deal closed-won (partner closes a deal) (HC 12732223).
- Own-deal API values: `own_deal_opened`, `own_deal_closed_won` (API docs).

Payload fields (identical between the signals endpoint and the webhook body; `record_type` exists to match the webhook) (API docs):

| Field | Meaning |
|---|---|
| `event_id` | Unique identifier of the signal (shared across rows on own-deals) |
| `signal_id` | Unique per row on `/v1/signals/own-deals` |
| `event_type` | What caused the signal |
| `triggered_at` | Time the signal event occurred |
| `record_name` | Name of your CRM record the signal relates to |
| `record_type` | `account` or `lead` (your side) |
| `record_id` | ID of your CRM record |
| `populations` | Your Crossbeam populations the record was in just AFTER the signal |
| `partner_populations` | Partner populations just after the signal (a deal closing moves a record from "Open Opportunities" to "Customers", so only "Customers" appears) |
| `partner_name` | Partner involved |
| `partner_id` | Partner UUID |
| `partner_data` | Shared deal data: can include `is_closed`, `is_won`, `open_date`, `close_date`, `stage`, `name` |
| `contact_name`, `contact_role`, `contact_type` | Only when partner shares contact data (HC 12732223) |

### 1.12 Webhook setup (Enterprise, Admin only)

Steps (HC 12732223):
1. Left navigation: Data, then Integrations, then +Create New, then Webhook.
2. Event types: choose Deal opened and/or Deal closed-won.
3. Add Webhook name.
4. Add Destination URL.
5. Click Finish. A secret key appears. Copy and store it safely; you cannot view the same key again. Some external tools may require it to authenticate incoming data.
6. Test: Crossbeam sends a test call to the destination URL. If the test fails, click the edit configuration button and retry until it succeeds.
7. Filters (only after a successful test): narrow by partners and populations. The webhook fires only for overlaps between your selected populations and the selected partners' selected populations.
8. Click Save Settings. The webhook appears in your installed integrations.
9. Manage later: Data, then Integrations, then the Settings button for the Webhook.

Webhook security (API docs):
- Header `X-Crossbeam-Signature-256`: base64 encoded HMAC. Compute HMAC SHA-256 with your secret key over the request body with the `X-Crossbeam-Timestamp` value appended (string "body+timestamp"), base64 encode, compare.
- Validate `X-Crossbeam-Timestamp` is within the past 300 seconds.
- Use a random, hard-to-guess endpoint path.

Retries and response (API docs):
- Crossbeam retries several times on `408`, `429`, `500`, `502`, `503`, `504`. After that, missed messages can be retrieved via the REST API (the signals endpoints).
- Respond with a success status, likely 200 or 201. No body needed.
- Example receiver is a minimal Flask app that verifies headers and returns `{}`, 200.

### 1.13 Choosing webhook vs API (HC 12732223)

| Use case | How | Model |
|---|---|---|
| Instant deal notifications | Partner opens an opp on an overlap, send Slack alert to account owner | Webhook |
| Trigger outreach cadences | Start a HubSpot or Outreach sequence when a partner adds an opp | Webhook |
| Timed follow-ups | Wait 60 days after a partner Closed Won, trigger a "better together" campaign | Webhook |
| Deal prioritization scoring | Fetch Closed Won signals daily to update opp scores in CRM | API endpoint |

Webhook = push, near real-time, for workflows, notifications, automation. API = pull on demand, for supplemental insights, reporting, scheduled analysis (HC 12732223).

### 1.14 Postman quick start (API docs)
- Use the Postman app installed locally, not the web app.
- Create the integration with callback `https://oauth.pstmn.io/v1/callback`.
- Click `Run in Postman` at the top of the docs to clone the collection.
- Select the `Crossbeam` environment.
- Edit the `Crossbeam API` collection, Variables tab, set Current Value of `client_id` and `client_secret`, click `Update`.
- The `scope` variable controls what the tokens can reach.
- A Loom demo is linked from the docs.

---

## 2. Deal Alerts (beta)

What (HC 11464781):
- AI-powered notifications that highlight your most promising opportunities, combining ecosystem signals (partner overlaps, account activity) with your CRM data, with clear reasons why.
- Each alert includes: Opportunity name and account; partner activity insights (new contact overlap, momentum signal); suggested next steps and a reason to act now.
- AI continuously scans CRM and ecosystem for: new contacts at shared accounts; stalled deal stages or inactivity; increased partner activity or engagement; high overlap with strategic partners.

Who (HC 11464781):
- Sales Reps: prioritize accounts with momentum, act on warm partner leads; use the alert digest for daily outreach.
- Account Managers: reignite stalled deals with new contact insights.
- CSMs: uncover expansion; act quickly on expansion or upsell signals.
- Sales Managers: monitor team activity, coach on momentum, spot pipeline trends.
- Partner Teams: springboard for warm intros or co-selling.

Setup and settings (HC 11464781):
- No manual turn-on. As long as your CRM and partners are connected, alerts flow automatically.
- Supported CRMs: Salesforce and HubSpot.
- Frequency: generated weekly; more customization is in development.
- Customization of which deals: "Not yet." Alerts are tied to CRM opportunity and contact data.

---

## 3. Legacy articles

### 3.1 Legacy: Per-Population Overrides (HC 4236661)
- What it was: sharing control for a specific partner's specific population ("per-population" means "per-partner's-population"), layered on Sharing Defaults (all partners) and partner-specific Sharing Settings. Only available for Overlap Counts or Sharing Data options.
- How it was set: Partner Detail Page, Sharing Settings, find the population, edit pencil under Sharing Defaults, Customize, Enable Per Population Overrides, select the partner population, check fields to share, Save.
- What replaced it: the article states it is "no longer available". It does not name a replacement. Related articles point to Sharing Defaults, Sharing Settings for Partners, the Sharing Dashboard, and Sharing Presets (HC 4236661).
- How to recognize a customer still on it: overrides created before 10/2024 are not impacted and still exist. On the Partner Detail Page under Sharing Settings, any population with overrides is displayed with highlighted fields (hover to see the fields). Partner-created overrides are visible via the Shared with You button.
- Migration notes: existing overrides can still be edited or removed via the edit pencil next to the population. New overrides cannot be created. The article gives no migration procedure.

### 3.2 Legacy: Crossbeam Overlaps Custom Object in Salesforce (HC 4353321)
- What it was: the original push of overlap data into a Salesforce custom object `Crossbeam Overlap`, installed alongside the Salesforce widget. Supernode tier.
- What replaced it: "All future updates and supports" are in the v2 article, Installation Guide: Crossbeam for Salesforce (v2) (HC 9280237 link).
- How to recognize: Integrations page shows a Salesforce Custom Object row with a Settings button; the modal has Go to Widget, "Use same customization setting as Widget", and My Data / Partner Data dropdowns. Salesforce has fields prefixed `xbeamprod__` and report types Crossbeam Overlaps, Crossbeam Overlaps with Account, with Leads, with Opportunity.
- Fields (label, API name, type):
  - Account, `xbeamprod__Account__c`, Lookup(Account)
  - Created By, `CreatedById`, Lookup(User)
  - Crossbeam EID, `xbeamprod__Crossbeam_EID__c`, Text(100) External ID, Unique Case Insensitive
  - Crossbeam Overlap Name, `Name`, Text(80)
  - Last Modified By, `LastModifiedById`, Lookup(User)
  - Lead, `xbeamprod__Lead__c`, Lookup(Lead)
  - Opportunity, `xbeamprod__Opportunity__c`, Lookup(Opportunity)
  - Owner, `OwnerId`, Lookup(User,Group)
  - Partner Account, `xbeamprod__Partner_Account__c`, Text(150)
  - Partner AE Email, `xbeamprod__Partner_AE_Email__c`, Text(150)
  - Partner AE Name, `xbeamprod__Partner_AE_Name__c`, Text(150)
  - Partner AE Phone, `xbeamprod__Partner_AE_Phone__c`, Text(150)
  - Partner Name, `xbeamprod__Partner_Name__c`, Text(150)
  - Partner Population, `xbeamprod__Partner_Population__c`, Text(150)
  - Population, `xbeamprod__Population__c`, Text(150)
- Behavior: push defaults to twice a day, every 12 hours (times vary). Bulk API, 5,000 records at a time. Initial sync creates a record per overlap and is heaviest; later syncs push only net new or updated overlaps. No custom fields on standard objects. Partner AE name and contact only come over for partners with Salesforce or HubSpot connected, not CSV or Google Sheets. Salesforce Classic can show data via the `Crossbeam Overlap` related list on Account, Opportunity, Lead layouts, but the app must be set up in Lightning and the widget is Lightning only.
- Suggested report: Group Rows by Account: Account Name; columns Population, Partner Population, Partner Name, Partner AE Name, Partner AE Email.
- Migration notes: initial record exports count toward Record Export Limits; reduce populations before initiating exports. Metering caps Record Exports at 100% of the plan's data limit. Move to the v2 guide for current support.

### 3.3 Legacy: Installation Guide, Crossbeam for Salesforce (HC 8732549)
- What it was: install of the managed package with "Crossbeam Copilot" (Lightning Web Component) and "Crossbeam Overlaps" (custom object).
- What replaced it: article says it was updated; current version is Installation Guide: Crossbeam for Salesforce (v1) (HC 9298987 link); related articles also list v2 and a Connector Plan install guide.
- Install steps: AppExchange listing, Get It Now, choose Install for Admins Only (Install for All Users breaks the permission sets), approve Third-Party Access (api.crossbeam.com, auth.crossbeam.com, sentry.io, login.salesforce.com, test.salesforce.com), Continue.
- Setup user needs: `Crossbeam Setup User` permission set; for the custom object push also Visualforce Page Access and Read on Account and Lead.
- Setup app: App Launcher, search "Crossbeam", Get Started. Three steps:
  1. Outbound Connection: Validate, log in to Crossbeam. User must be Admin for Crossbeam Core and Manager for Crossbeam for Sales. SSO enforced orgs use the SSO exception user.
  2. Crossbeam Organization Selection: pick the account, Next.
  3. Inbound Connection: Authorize; status must change from "Not Connected" to "Connected"; Finish.
- Trusted URL: Setup, Trusted URLs (under Security), New Trusted URL; API Name `Crossbeam`; URL `https://app.crossbeam.com`; CSP Context Lightning Experience Pages; CSP Directives frame-src (iframe content); Save. Needed for Copilot Plays and Contacts tabs.
- Permission sets: Crossbeam Setup User (admin, write to custom object); Crossbeam Account User (Copilot; full access for paid Core or Sales seat, Starter Access high level overview without); Crossbeam Widget Viewer (Copilot with clickable buttons disabled, no partner data, no conversations); Crossbeam Report User (custom object, reports and dashboards). Recommended for the whole team: Crossbeam Account User and Crossbeam Report User.
- Placing Copilot: Setup, Object Manager, Account, Lightning Record Pages, Default Accounts, Edit, drag Crossbeam Copilot from "Custom - Managed", Activation, Set as Org Default, Save. Can be placed on Account, Opportunity, Contact, Lead pages; recommended on Account and Opportunity.
- How to recognize: customer references the "Crossbeam Widget" or "Salesforce push", the Crossbeam Setup App with 3 setup steps, or the `xbeamprod__` object.
- Migration notes: follow the current v1/v2 guides linked from the article; no migration steps in this article.

### 3.4 Legacy: Send Accounts from a Shared List to the Account Owner (HC 9035095)
- What it was: select accounts in a Shared List and send them to the account owner in Crossbeam for Sales. Connector or Supernode plan; Explorer plan limited to Invite Only; required a Co-Seller Seat in Crossbeam for Sales.
- Flow: Collab icon, All Shared Lists, open list, check account boxes, Send, Send to Account Owner, choose owner, Send Records (or row arrow, Send to Account Owner). The Sales column then shows send date and owner; link opens the record in Crossbeam for Sales. Recipients find it under Lists in Crossbeam for Sales. Notifications by email, Slack, and Copilot for Salesforce Feed tab (Get Intel). No notification when sending to yourself.
- What replaced it: "no longer available in Crossbeam." The article names no replacement.
- How to recognize: customer mentions "Send to Account Owner", "Send Records", or a Sales column with dates in a Shared List.
- Migration notes: none given in the article.

---

## 4. Clari (HC 7827330)

Requirements: Supernode tier and the "Crossbeam Overlaps" custom object in Salesforce. Prerequisite: Salesforce App installed and pushing overlap data into Salesforce.

Why: most Clari modules are built on the opportunity object. To show Crossbeam data in the Opportunity Grid or Details Panel in Clari Web, fields must exist on the Salesforce opportunity object. By default each partner match is a separate Crossbeam Overlap record (example: account PlanView matching Bozala, Surfzer, Yaarde creates 3 records). A Salesforce flow copies these onto Account and Opportunity fields.

Exact steps:
1. Salesforce Step 1, Account Object Flow: follow "Add Crossbeam Overlap data to Account Object" (HC 8868816).
2. Salesforce Step 2, Opportunity Object Flow: follow "Add Crossbeam Overlap data to Opportunity Object" (HC 8868815).
3. Clari: add the fields in Clari's Field Configuration Module.
4. Recommended Opportunity Grid columns: "Partners (Customer)" and "Partners (Opportunity)".

Field meanings:
- Partners (Customer): insight into the prospect's tech stack; which partners can offer assistance or influence.
- Partners (Opportunity): tech the prospect may be shopping for; which partners you can co-sell or coordinate with.

Other facts:
- Deployment estimate: an experienced Salesforce Admin, 2 to 3 hours.
- To limit to strategic partners: Crossbeam Integrations page, "Salesforce App Settings", customize which partners and partner populations are pushed.

---

## 5. Troubleshooting

| Symptom / error string | Cause | Fix | Source |
|---|---|---|---|
| API calls return data for the wrong org or fail authorization | Missing or wrong `Xbeam-Organization` header | Call `GET {USERS}/me`, take `authorizations[].organization.uuid`, send as `Xbeam-Organization` | API docs |
| Token stops working after a day | Access tokens valid only 24 hours | Request `offline_access` scope and exchange `refresh_token` at `https://auth.crossbeam.com/oauth/token` | API docs |
| Endpoint rejected for scope | Token lacks endpoint scope | Add the scope (for example `read:reports`, `read:audit-log`) along with `openid` | API docs |
| Overlap sync misses changes after changing filters | Changing query params invalidates the cursor | Restart with no cursor | API docs |
| Overlaps disappeared from sync | Returned with `"is_deleted": true` (unshared, removed from CRM, moved populations) | Verify the record still exists in the target system before deleting | API docs |
| Signal with renamed deal not returned | Signals bookmark returns only newly created signals | Expected; deal name changes do not re-emit | API docs |
| No signals from a partner | Partner lacks connected CRM or is not sharing Deal open date, Deal close date, Deal is closed, Deal is won | Ask partner to sync and share those fields | HC 12732223 |
| No contact data on signals | Partner not sharing CRM contact data (Contact Name, Contact Title) | Ask partner to share contacts | HC 12732223 |
| Greenfield signals wanted | Not supported | None at this time | HC 12732223 |
| Cannot create webhook or API integration | Not Admin, or plan lacks access (webhook is Enterprise; API is Supernode) | Use Admin user; upgrade via Plan and Billing | HC 12732223, HC 4677142 |
| Webhook test fails | Destination URL did not accept the test call | Click edit configuration and retry until it succeeds | HC 12732223 |
| Cannot add webhook filters | Webhook not yet tested successfully | Pass the test first | HC 12732223 |
| Lost webhook secret key | Key shown once after Finish | Cannot be viewed again; article gives no recovery step | HC 12732223 |
| Missed webhook deliveries | Retries exhausted after `408`, `429`, `500`, `502`, `503`, `504` | Retrieve via the signals REST endpoints | API docs |
| Sample receiver logs `Missing required headers`, `Invalid timestamp format`, `Timestamp too old or too new`, `Invalid signature` | These are messages from Crossbeam's example Flask code: missing `X-Crossbeam-Signature-256`/`X-Crossbeam-Timestamp`, non-integer timestamp, timestamp older than 300 seconds, HMAC mismatch | Hash body + timestamp with the webhook secret using SHA-256, base64 encode, compare; check clock drift | API docs |
| Record export limit reached | API calls, webhooks, and custom object exports count toward Record Exports | Reduce populations or partners pushed; contact the Crossbeam support inbox (support at crossbeam.com) | HC 4677142, HC 12732223, HC 4353321 |
| Email: push to Salesforce failed because of an expired token | Salesforce token expired | Re-authorize by going through the app installation steps again | HC 4353321 |
| `Insufficient Privileges` during Inbound Connection | Using Salesforce "login as" with an Integration User | Log in directly as that user | HC 8732549 |
| Status stays "Not Connected" | Authorize not completed or not approved | Click Authorize, approve the Salesforce window, confirm "Connected" | HC 8732549 |
| Permission sets not working | Package installed with "Install for All Users" | Package should be installed with Install for Admins Only | HC 8732549 |
| Copilot Plays and Contacts tabs do not load | Trusted URL missing | Add Trusted URL `Crossbeam`, `https://app.crossbeam.com`, frame-src, Lightning Experience Pages | HC 8732549 |
| No overlap data on Opportunities (custom object) | Opportunity custom object does not support custom populations | Include the Open Opportunities standard population in Salesforce settings | HC 4353321 |
| Partner AE name/email blank | Partner uses CSV or Google Sheets | Only Salesforce or HubSpot partners send owner info | HC 4353321 |
| Crossbeam data not in Clari | Data lives on custom object, not Opportunity | Build the Account and Opportunity flows, then add fields in Clari Field Configuration | HC 7827330 |
| Too many partners in Salesforce and Clari | All partners pushed | Salesforce App Settings on Integrations page: select partners and partner populations | HC 7827330 |
| Cannot create per-population overrides | Legacy feature removed | Only pre 10/2024 overrides remain editable | HC 4236661 |
| "Send to Account Owner" missing in Shared Lists | Legacy feature removed | No replacement named | HC 9035095 |
| No Deal Alerts | CRM or partners not connected, or CRM is not Salesforce or HubSpot | Connect CRM and partners; alerts are weekly and automatic | HC 11464781 |
