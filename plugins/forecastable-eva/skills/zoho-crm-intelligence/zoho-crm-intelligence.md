# Zoho CRM Intelligence

Version: 2026-09-29. Owner: Forecastable (Eva build). Refresh: monthly (see `refresh-protocol.md`).

Source tags: [A#] Zoho CRM API v8 developer docs and Kaizen posts; [B#] Zoho product, help, MCP and
pricing pages, Claude connector listing, direct HTTP checks; [Y:video_id mm:ss] YouTube transcript,
channel and date in section 14. OURS marks Forecastable's own recommendation. UNVERIFIED and CONFLICT
items are collected in section 13 and must not be stated as fact.

---

## 1. Mental model

- **Core chain.** Leads are standalone records for unqualified people. Converting a Lead creates an
  Account (company), a Contact (person) and optionally a Deal, per Setup lead conversion mapping; the
  converted Lead drops out of the Leads list [Y:Ngm045YcMgc 02:53][Y:CJtqyyYNOyU 1:21:30]. Account is
  the parent of Contacts and Deals; a Deal is a child of both Account and Contact [Y:-zZ-1nJ-IEc 00:41].
  Deals have built-in Contact Roles for several contacts per deal [Y:CJtqyyYNOyU 1:44:30].
- **Activities.** Tasks, Meetings (API name `Events`) and Calls are separate modules linked to a person by
  `Who_Id` (Contact or Lead) and to anything else by `What_Id` plus `$se_module` [A42]. Open Activities
  and Closed Activities related lists show them on the record [Y:Ngm045YcMgc 07:04].
- **Customized orgs move the "deal".** Real estate and other verticals often put the real transaction in
  a custom or renamed module, sometimes a linking module that behaves like a deal (Property Interests in
  Zoho's own demo). Inspect modules and related lists before assuming Deals [Y:m588QX4WmYA 11:23].
- **Custom modules** (Enterprise and above) are "org modules" or "team modules"; team modules add
  Manager, Member, Participant and Requester roles [Y:0m05tx5_fVU 12:58][B41].
- **Multi-select lookups** create a hidden **linking module** (junction) with two lookups; **subforms**
  are their own modules with `Parent_Id` [A43][Y:x-QiW-pVF2M 11:49, 28:04].
- **Layouts** can differ per record type; required fields and picklists can differ per layout, and
  Blueprint is configured per layout [Y:m588QX4WmYA 25:49, 32:21].
- **Permissions shape everything.** Profiles say what a user can do (including API access); roles say
  whose records roll up to whom; sharing rules add exceptions [Y:Ngm045YcMgc 12:21][B10][B31]. Every UI,
  API and MCP read is filtered by the acting user [A13][B3].
- **Team Spaces** decide which modules a user sees in the sidebar; module names and sets differ by team
  space and role [Y:Ngm045YcMgc 02:21][Y:CJtqyyYNOyU 41:00].

## 2. Reaching Zoho CRM from Claude

### 2.1 Zoho CRM connector in the Claude directory
- Published by Zoho, 41 tools, sign-in required; listing claude.com/connectors/zoho-crm [B1].
- Regional endpoints (path `/mcp/message`): US `claude-zohocrm.zohomcp.com`, EU `.eu`, IN `.in`,
  **AU `https://claude-zohocrm.zohomcp.com.au/mcp/message`**, CA `.ca`, SA `.sa`, JP `.jp`, AE `.ae` [B1].
  AU endpoint answered with an OAuth challenge on 2026-09-29; its OAuth server is on mcp.zoho.com.au [B2].
- Named tools [B1]: read `Get_Organization`, `Get_Modules`, `Get_Module`, `Get_Fields`, `Get_Layouts`,
  `Get_Layout`, `Get_Users`, `Get_User`, `Search_Records`, `Get_Records`, `Get_Record`,
  `executeCOQLQuery`; write `Create_Records`, `Update_Record`, `Update_Records`, `Upsert_Records`,
  `Delete_Record`, `Delete_Records`, `Create_Field`, `Create_Notes`, `Update_Notes`, `Delete_Notes`,
  `Update_Users`, `Update_User`. 17 tools are not named on the listing (UNVERIFIED).
- Requested scopes include `ZohoCRM.modules.ALL`, `ZohoCRM.settings.ALL`, `ZohoCRM.coql.READ`,
  `ZohoCRM.bulk.READ`, per-module scopes incl. Calls, Events, Tasks, Notes, custom [B2].
- **Known bug:** the directory connector does not ask for a data center and has defaulted users to
  zoho.eu, error "Invalid server url. Kindly re-verify oauth url from metadata and try again." (GitHub
  anthropics/claude-ai-mcp#311, May to Jul 2026) [B6]. Workaround for AU (OURS, UNVERIFIED): custom
  connector with the AU URL above.
- Partners prefer a custom server over the directory tile because the tile exposes delete tools and a
  long tool list that can mislead the model [Y:325hWpN_lEs 16:33][Y:F45GH-yPisM 03:25].

### 2.2 Custom servers in the Zoho MCP console
- Console mcp.zoho.com (AU mcp.zoho.com.au) [B2][B7]. Create Server (name without spaces) or a
  pre-configured server, Add Tools, pick product and tools, Add Now [B7][Y:325hWpN_lEs 00:24].
  Zoho CRM exposes 999 to 1,202 actions depending on the video [Y:F45GH-yPisM 01:20][Y:325hWpN_lEs 01:40].
- Each server has a unique URL with an embedded key (treat as a secret, can be regenerated) [B7][B8]
  [Y:325hWpN_lEs 07:46].
- **Auth modes.** "Authorization on demand" (default): each user OAuths and sees only what their
  profile, role and sharing allow; requires CRM API access on their profile [Y:325hWpN_lEs 08:10][B6b].
  "Authorization via connection": everyone inherits one account's permissions; audit log and recycle bin
  show that account, so use only for read-only work [Y:325hWpN_lEs 11:51][Y:F45GH-yPisM 02:40].
- Zoho CRM also ships four prebuilt servers: Data Insights (read-only COQL and schema), Data Operations
  (CRUD), Module Customization, Workflow and Process Automation [B3][B4][B13]. For Eva, OURS: Data
  Insights or a custom read-only server.
- Tool hygiene from practitioners: start with the fewest tools; minimum read set is Search Records, Get
  Record, Get Fields and a COQL tool [Y:325hWpN_lEs 03:36, 27:03]; avoid Delete; Update Records opens all
  fields [Y:325hWpN_lEs 04:50]; separate servers for customization vs data work [Y:325hWpN_lEs 29:20];
  removing an unwanted tool works better than instructing the model not to use it
  [Y:F45GH-yPisM 18:30]; adding a tool requires reconnecting in Claude [Y:325hWpN_lEs 29:44].
- Per-record writes: MCP has no bulk create; 20 tasks = 20 calls; use Bulk Write for volume
  [Y:F45GH-yPisM 15:50]. "Volume trap": MCP is for micro tasks, not thousands of records
  [Y:UGi0tFOyWYg 05:50].
- Give the model a data map: which tools are on, which module holds what, business definitions
  ("needs attention" = overdue close date, overdue tasks, stale leads) [Y:F45GH-yPisM 05:25, 21:35].
  Without it, the model writes to the standard location (Account Industry instead of a Deal field)
  [Y:325hWpN_lEs 24:20].
- Claude side: org owner adds the connector (Organization settings > Connectors > Add), each user then
  Customize > Connectors > Connect, Allow, choose Production, Sandbox or Developer, Accept
  [Y:325hWpN_lEs 15:45][B5][B8]. Set reads to Always allow and writes to Needs approval
  [Y:UGi0tFOyWYg 03:21].
- **Cost:** Zoho MCP is free; every tool call consumes normal CRM API credits [B9][B4].

### 2.3 The "you need API permission" error
- Signature: HTTP 403 `{"code":"NO_PERMISSION","details":{"permissions":["Crm_Implied_Api_Access"]}}`
  on a valid token, affecting some users and not others (profile-level) [B15].
- Fix: Setup > Security Control > Profiles > [profile] > Developer Permissions > **Zoho CRM API Access**
  ON [B10][B11][B12]. NextGen saves instantly [B11]; have the user sign out and in, then reconnect the
  connector [B12]. Linking the error code to this toggle is strongly indicated but not stated by Zoho
  (UNVERIFIED) [B15].
- Only administrators edit profiles; the built-in Standard profile cannot be edited, so orgs clone it
  [Y:Ngm045YcMgc 12:21][Y:-D67j_-YhM0 24:49]. Enabling API access also lets that user script against
  the API outside MCP [Y:325hWpN_lEs 08:10].

### 2.4 Data centers
| DC | Accounts (OAuth) | API domain |
|---|---|---|
| US | accounts.zoho.com | www.zohoapis.com |
| **AU** | **accounts.zoho.com.au** | **www.zohoapis.com.au** |
| EU | accounts.zoho.eu | www.zohoapis.eu |
| IN | accounts.zoho.in | www.zohoapis.in |
| JP | accounts.zoho.jp | www.zohoapis.jp |
| CA | accounts.zohocloud.ca | www.zohoapis.ca |
| CN | accounts.zoho.com.cn | www.zohoapis.com.cn |
- Always call the `api_domain` returned with the token; a token minted on the wrong DC fails [A1][A9]
  [Y:ZdicRo5Z6IU 28:09]. The DC is set at sign-up from IP [Y:-D67j_-YhM0 04:31]. Sandbox and developer
  orgs use `sandbox.zohoapis.*` and `developer.zohoapis.*`; tokens are environment specific [A46].
- Web UI: crm.zoho.com or crm.zoho.com.au; Zoho One and CRM Plus wrap it with a different top nav
  [B20][Y:CJtqyyYNOyU 16:30].

## 3. Navigating the UI (CRM for Everyone / NextGen)

### 3.1 Layout
- Left rail: Home, Work Queue, Reports, Analytics (dashboards), Requests, Agents; then Team Spaces
  holding modules; bottom left: create (+), Calendar, Emails, Signals, Setup (gear) [Y:Ngm045YcMgc 00:24]
  [Y:0m05tx5_fVU 01:04]. No switch back to the classic UI [B17].
- Hotkeys: `/` global search (across modules and non-name fields such as phone and email, can scope to a
  module); `G D` jumps to Deals [Y:CJtqyyYNOyU 16:35].
- Top right: Ask Zia (good for insights, unreliable for actions), Signals, Calendar, Emails,
  Marketplace, Setup [Y:Ngm045YcMgc 10:47].
- Setup is a searchable list with categories and a Frequently Used block [B18][Y:0m05tx5_fVU 03:09].

### 3.2 Setup paths
| Item | Path | Src |
|---|---|---|
| Modules, fields, layouts, custom modules | Setup > Customization > Modules and Fields > [module] > Layouts | [B19][Y:8QsKQ1PsGtQ 01:45] |
| Field permissions | Setup > Customization > Modules and Fields > [module] > Fields > Field Permissions | [B31] |
| **API names** | Setup > Developer Hub > APIs and SDKs > API Names tab > [module] | [B39][Y:ZdicRo5Z6IU 34:21] |
| API credits dashboard | Setup > Developer Hub > APIs and SDKs > Credits | [B28] |
| Connections | Setup > Developer Hub > Connections | [B32] |
| Queries (live data widgets) | Setup > Developer Hub > Queries | [Y:ulbaHD97rOE 13:30] |
| Functions (Deluge, Python, Java, Node.js) with logs and revisions | Setup > Developer Hub > Functions | [Y:MA_Baod_Tzk 01:50] |
| Profiles | Setup > Security Control > Profiles | [B10] |
| Roles and sharing | Setup > Security Control > Roles and Sharing | [B31] |
| Audit Log (3 years, export up to 1M entries) | Setup > Security Control > Audit Log (moved in 2026 UI) | [B27][Y:CJtqyyYNOyU 2:27:00] |
| Workflow Rules | Setup > Automation > Workflow Rules | [B21][Y:Df8NuKBZW0I 02:47] |
| Assignment Rules | Setup > Automation > Assignment | [B22] |
| Cadences | Setup > Automation > Cadences | [Y:CJtqyyYNOyU 2:32:00] |
| Blueprint, Approval Processes | Setup > Process Management | [B23][Y:0IrMNcpzg58 00:16] |
| Pipelines (Deals only) | Setup > Customization > Pipelines | [Y:CJtqyyYNOyU 2:11:00][Y:-D67j_-YhM0 50:09] |
| Email configuration, sharing | Setup > Channels > Email | [B34][Y:_Dn2IF2DVQM 21:40] |
| Telephony (PhoneBridge, Zoho Voice) | Setup > Channels > Telephony | [B35][B36] |
| WhatsApp | Setup > Channels > Business Messaging | [Y:_Dn2IF2DVQM 43:05] |
| Import, Export, Data Backup, Recycle Bin (60 days), Sandbox | Setup > Data Administration | [B25][B26][Y:0m05tx5_fVU 03:09] |
| Zia models | Setup > Zia > Models | [B37] |
| Zia Agents | Setup > Zia > Agents (build); Setup > General > Agents > Configured (deployed) | [Y:8ENy7rjO4AI 00:15][B38] |
| Team Spaces | Setup > Customization > Team Spaces, or module rail > Manage Team Space | [Y:0m05tx5_fVU 08:17] |

### 3.3 Module views and records
- Views: List, Grid (inline edit), Kanban, Chart, Timeline, Split, Canvas (custom list, tile, table),
  Map (IN DC only), Sheet [B40][Y:CJtqyyYNOyU 47:30]. List views show at most 100 rows per page
  [Y:CJtqyyYNOyU 53:30].
- Custom views are shared saved filters; saved filters are private and stack on a view
  [Y:CJtqyyYNOyU 53:30]. A view's cvid is in its URL and works in COQL (`FROM Leads#<cvid>`) and Bulk
  Read [A35][Y:hTL0FMjG4x4 11:15]. UI counts can differ from API counts when a view filter applies
  [Y:325hWpN_lEs 21:04].
- The filter panel covers system filters, fields, subform fields, related modules and activity filters
  such as "without open activity" [Y:CJtqyyYNOyU 59:00]. "Last Activity Time age in days >= 7" makes a
  work list [Y:0m05tx5_fVU 30:33].
- Record page: Details (own fields), Related lists (children), Timeline tab (History and Interactions:
  emails with status and sentiment) [Y:CJtqyyYNOyU 1:12:00][B42]. The Timeline shows "created by
  workflow rule" when automation fired [Y:Ngm045YcMgc 17:21].
- The record id is the long number in the record URL [Y:Vy5OMHFJd_g 03:53].

### 3.4 Reports and dashboards (inside CRM)
- Reports tab needs the "create reports" permission [Y:MmWulZdg2kk 03:32]. Prebuilt folders by module;
  useful Deal reports: Pipeline by Stage, Sales by Lead Source, Salesperson's Performance
  [Y:MmWulZdg2kk 04:10]. Clone before building [Y:-zZ-1nJ-IEc 15:09].
- Create Report > primary module > add related modules. Child modules are **Inclusive** (all primary
  records, outer join) or **Exclusive** (only primaries with children, inner join); parents have no such
  option [Y:-zZ-1nJ-IEc 03:58][Y:7jzz-jrTn1o 40:00]. Start at the top of the hierarchy
  [Y:-zZ-1nJ-IEc 01:59].
- Row groups, column groups (matrix, detail columns disappear), aggregate columns (Sum, Average, Min,
  Max, Count), Quick View filters vs Advanced filters [Y:-zZ-1nJ-IEc 07:31, 09:52, 11:08]. Group on
  picklists, not single-line text [Y:7jzz-jrTn1o 48:30].
- **Preview totals are wrong:** the builder aggregates only preview rows [Y:MmWulZdg2kk 09:25].
- A module missing from the report builder means a missing lookup; a module listed twice means two
  lookups [Y:7jzz-jrTn1o 55:00].
- Dashboards live in the Analytics tab; build components from reports for drill-down; date charts omit
  empty periods [Y:-zZ-1nJ-IEc 16:07, 25:20]. Zoho Analytics is a separate app with SQL and cross-app
  data; lookups arrive as numeric ids and counts should use distinct id [Y:CJtqyyYNOyU 05:00]
  [Y:cuBin4KtrpM 09:22, 26:35].
- Pre-build test for any report: X vs Y, which module holds each, extra fields and their modules,
  filters and period [Y:7jzz-jrTn1o 22:30].

## 4. API v8 read reference

### 4.1 Auth and scopes
- Header `Authorization: Zoho-oauthtoken {access_token}` [A24]. Access token 1 hour; refresh token until
  revoked (max 20 per user); max 10 access tokens per refresh token per 10 minutes; cache tokens [A7].
- Self Client at the DC's API console for single-org backends; grant code then token exchange at the
  DC's accounts server [A8][A9][Y:ZdicRo5Z6IU 17:12].
- Read-only scope string (OURS, from per-endpoint requirements):
  `ZohoCRM.modules.READ,ZohoCRM.settings.READ,ZohoCRM.users.READ,ZohoCRM.org.READ,ZohoCRM.coql.READ,ZohoCRM.bulk.READ,ZohoSearch.securesearch.READ,ZohoCRM.modules.notes.READ,ZohoCRM.modules.attachments.READ,ZohoCRM.modules.emails.READ`
  [A5][A33][A35]. Calling outside granted scopes returns OAUTH_SCOPE_MISMATCH [Y:-D67j_-YhM0 06:42].

### 4.2 Metadata
| Purpose | Endpoint | Src |
|---|---|---|
| Modules | `GET /crm/v8/settings/modules` | [A12] |
| Fields | `GET /crm/v8/settings/fields?module={api}` | [A14] |
| Layouts (per-layout required fields, picklists) | `GET /crm/v8/settings/layouts?module={api}` | [A15] |
| Related lists (`href` to call verbatim) | `GET /crm/v8/settings/related_lists?module={api}` | [A16] |
| Custom views | `GET /crm/v8/settings/custom_views?module={api}` | [A17] |
| Users (`type=ActiveUsers` etc.) | `GET /crm/v8/users` | [A18] |
| Roles, profiles | `GET /crm/v8/settings/roles`, `/settings/profiles` | [A19][A20] |
| Org (edition type, currency, time zone) | `GET /crm/v8/org` | [A21] |
- Module keys: `api_name` (use everywhere; Meetings = `Events`), `generated_type`
  (default/custom/linking/subform/web), `api_supported`, `visible` [A12]. Only modules the user can
  access are returned [A13].
- Field keys: `api_name`, `data_type` (text, textarea, email, phone, picklist, multiselectpicklist,
  integer, currency, boolean, date, datetime, lookup, ownerlookup, multiselectlookup, subform, formula,
  rollup_summary, and more), `custom_field`, `lookup`, `multiselectlookup.linking_module`,
  `pick_list_values` [A14]. Renamed fields keep their original API name [Y:Vy5OMHFJd_g 11:00].
- Always read field metadata before any write or import [Y:-D67j_-YhM0 54:54].

### 4.3 Records, related records, notes, emails, timeline
- `GET /crm/v8/{module}?fields=a,b,c` : `fields` mandatory (max 50), `per_page` max 200, `page_token`
  beyond 2,000 rows (from `info.next_page_token`, valid 24 h, max 100,000), `sort_by` id, Created_Time or
  Modified_Time, `converted=both` to include converted leads, `cvid` for a view (3 credits),
  `If-Modified-Since` header for incremental pulls [A24]. List calls truncate rich text to 500 chars and
  omit subforms [A24].
- Related: `GET /crm/v8/{module}/{id}/{related_list_api_name}?fields=...` [A25]; counts via
  `POST /{module}/{id}/actions/get_related_records_count` (up to 20 lists) [A31].
- Notes: `/{module}/{id}/Notes` (`Note_Title`, `Note_Content`, `Parent_Id`) [A26]. Attachments:
  `/{module}/{id}/Attachments` [A27].
- Emails: `/{module}/{id}/Emails`, 10 per call, page with `index`; body only on single-email fetch [A28].
- Timeline: `GET /{module}/{id}/__timeline` with `filters` on module, `done_by.id`, `audited_time`,
  `source` (crm_api, workflow, blueprint...) and `include_inner_details=field_history.data_type,...`;
  the best source for stage-change history [A29].
- Deleted: `GET /{module}/deleted?type=all|recycle|permanent` (recycle 60 days, permanent ids 120 days)
  [A30]. Record count: `GET /{module}/actions/count` costs 50 credits; use COQL COUNT instead [A32][A41].

### 4.4 Search
- `GET /crm/v8/{module}/search?criteria=((Field:operator:value)and(...))` or `email=`, `phone=`,
  `word=`; max 10 criteria; `in` up to 100 values; URL-encode and escape `( ) , \` [A33][Y:x-QiW-pVF2M 01:15].
- `equals` on text acts as contains; reads a separate index so new or edited records can return 204;
  hard cap 2,000 records; 200 per page; needs `ZohoSearch.securesearch.READ` [A33][Y:x-QiW-pVF2M 02:53].
- Subform rows: search the subform module with `Parent_Id:equals:<id>` [Y:x-QiW-pVF2M 11:49].

## 5. COQL cookbook

Endpoint `POST {api_domain}/crm/v8/coql`, body `{"select_query": "..."}`; MCP tool `executeCOQLQuery`
[A35][Y:_Jr2ur1wlqo 07:25].

### 5.1 Rules
- Syntax: `SELECT f1, Lookup.Field FROM Module WHERE (...) [GROUP BY] [ORDER BY] LIMIT offset, count`
  [A34]. WHERE is required; select all with `where id is not null` [A35].
- Bracket combined conditions: `((A and B) and C)`; max 25 conditions [A34][A35].
- LIMIT default 200, max 2,000 per call; credits 1 (to 200), 2 (to 1,000), 3 (to 2,000) [A34]
  [Y:x-QiW-pVF2M 23:30]. COQL is under the 10-call sub-concurrency limit [A41].
- Beyond the per-criteria window, switch to keyset paging: `order by id asc` and add `id > '<last id>'`,
  restart offset at 0 [A34][Y:x-QiW-pVF2M 30:47]. Pairing `Created_Time >` with `id >` can skip rows
  that share a timestamp; id-only keyset is safest (OURS).
- Comparators: text and picklist `= != like 'x%' '%x%' in, not in, is null`; lookups `= != in is null`;
  dates and numbers `> >= < <= between`; boolean `=` only; textarea fields cannot be filtered [A35]
  [Y:x-QiW-pVF2M 22:08].
- Dates `'2026-09-01'`; datetimes ISO 8601 with offset, AU `'2026-09-01T00:00:00+10:00'` (AEST) or
  `+11:00` (AEDT, first Sunday in October to first Sunday in April in NSW, VIC, ACT, TAS; QLD stays
  +10:00) [A35]. Confirm the org time zone with `Get_Organization`.
- Lookups return `{id, name}`; add dot notation for other parent fields; aliases with AS [A35]
  [Y:x-QiW-pVF2M 25:40]. Polymorphic: `'What_Id->Accounts.Account_Name'`, `'Who_Id->Contacts.Email'`
  (quoted) [A35]. Custom views as source: `FROM Deals#<cvid>` [A35].
- Aggregates SUM, AVG, MIN, MAX, COUNT (uppercase), GROUP BY up to 4 fields, required when mixing
  aggregates and plain fields [A34][A35].
- Subqueries: WHERE only, one column each, up to 5 per query, 100 rows each; run inside out
  [Y:_Jr2ur1wlqo 09:40, 18:40].
- Multi-select lookup fields cannot be selected; query the linking module. Subforms: query the subform
  module with `Parent_Id.` [A35][Y:x-QiW-pVF2M 25:11, 28:04].
- Quote reserved words used as names; prefix `!` to disambiguate a module name [A34][A35].
- Errors: SYNTAX_ERROR (often missing WHERE or brackets), LIMIT_EXCEEDED (drop to 200), INVALID_QUERY
  (wrong API name, textarea in WHERE, multi-select lookup selected), OAUTH_SCOPE_MISMATCH [A35].

### 5.2 Queries (replace api names after discovery)
```sql
-- Discover volume cheaply
select COUNT(id) from Deals where id is not null

-- Deals won this quarter with account and owner (AU, Q2 FY27 = Oct to Dec 2026)
select Deal_Name, Amount, Stage, Closing_Date, Account_Name.Account_Name, Owner, Lead_Source
from Deals where (Stage = 'Closed Won' and Closing_Date between '2026-10-01' and '2026-12-31')
order by Closing_Date asc limit 0, 2000

-- Won deals by owner (counts and value)
select Owner, COUNT(id), SUM(Amount) from Deals
where (Stage = 'Closed Won' and Closing_Date between '2026-10-01' and '2026-12-31') group by Owner

-- Deals created in a window (opened), with a custom lookup to a custom module
select Deal_Name, Created_Time, Stage, <Partner_Lookup>.<Partner_Name_Field>, Owner from Deals
where Created_Time between '2026-10-01T00:00:00+10:00' and '2026-10-31T23:59:59+11:00' limit 0, 2000

-- Leads by source pair (two picklists), including converted: COQL returns converted leads unless filtered
select Lead_Source, <Lead_Source_2>, COUNT(id) from Leads
where Created_Time >= '2026-10-01T00:00:00+10:00' group by Lead_Source, <Lead_Source_2>

-- Custom module records with owner and status
select Name, <Status_Field>, Owner, Created_Time, Modified_Time from <Custom_Module_Api> where id is not null limit 0, 2000

-- Calls in a month with the related account
select Subject, Call_Type, Call_Start_Time, Call_Duration, Owner, 'What_Id->Accounts.Account_Name', Who_Id
from Calls where Call_Start_Time between '2026-10-01T00:00:00+10:00' and '2026-10-31T23:59:59+11:00' limit 0, 2000

-- Contacts at accounts with no closed-won deal (subquery)
select Last_Name, Email, Account_Name.Account_Name from Contacts
where Account_Name not in (select Account_Name from Deals where Stage = 'Closed Won') limit 0, 200

-- Linking module from a multi-select lookup
select <Lookup_A>.Name, <Lookup_B>.Name from <Linking_Module_Api> where <Lookup_A> is not null

-- Lookup by email before creating anything (dedupe)
select id, Account_Name, Owner from Contacts where Email = 'name@example.com.au'

-- Keyset page after 2,000 rows
select id, Deal_Name from Deals where id > '<last id>' order by id asc limit 0, 2000
```
`COUNT(id)` is used widely but the docs' example counts a field; if rejected, count a lookup or picklist
field (UNVERIFIED) [A35]. `Name` is the default name field of a custom module (UNVERIFIED per org; read
the fields).

## 6. Bulk Read, notifications and sync
- Bulk Read: `POST /crm/bulk/v8/read` with module, fields (dot notation for parent fields), criteria
  groups, optional cvid; poll `GET /crm/bulk/v8/read/{job_id}` or use a callback; download ZIP of CSV
  (ICS for Events) [A36][A37][Y:hTL0FMjG4x4 07:45].
- 200,000 rows per job, `page` up to 500, 50 credits per job, file kept 24 hours; no Notes,
  Attachments or Emails; no sort; non-admins cannot pull parent sub-fields [A37][A40]
  [Y:hTL0FMjG4x4 12:40].
- Notification API: subscribe to `Module.create/edit/delete` with a notify_url; PUT replaces the event
  list, PATCH appends; channels expire and must be renewed [Y:hTL0FMjG4x4 15:10, 21:00].
- One-way sync pattern: subscribe first, then Bulk Read, keep the newer `Modified_Time`, store
  last_sync_time and re-pull `Modified_Time > last_sync_time` daily [Y:hTL0FMjG4x4 22:15].
- Composite API: up to 5 sub-requests in one call with optional rollback [Y:ZdicRo5Z6IU 06:43].

## 7. Activities: calls, meetings, tasks, email
- **Calls** fields: `Call_Type` (Inbound, Outbound, Missed), `Call_Start_Time`, `Call_Duration`
  (HH:mm), `Call_Purpose`, `Who_Id`, `What_Id` + `$se_module`, `Description`; Call_Type and Owner of
  completed calls cannot be edited [A42][B43].
- **How calls get into Zoho:** manual Log a Call (unreliable) [Y:_Dn2IF2DVQM 33:06]; telephony
  (PhoneBridge providers, Zoho Voice, built-in) auto-logs calls to matching records with duration and
  outcome and fires call signals [Y:_Dn2IF2DVQM 37:31, 38:36][B35][B36]; mobile app: Android can log
  incoming calls only when the number is already in CRM; **iPhone cannot log incoming calls at all**
  (Apple restriction), only outgoing [B29][B30]. Zoho Voice is available in Australia
  [Y:M3iX6q1SjOk 00:15].
- **Meetings** are `Events`: `Event_Title`, `Start_DateTime`, `End_DateTime`, `Participants`,
  `What_Id` [A42]; usually from calendar sync (Google and Microsoft two-way calendar)
  [Y:Ngm045YcMgc 25:13].
- **Tasks:** `Subject`, `Due_Date`, `Status`, `Priority`, `Who_Id`, `What_Id` (Status and Priority
  UNVERIFIED names) [A42]. Creating tasks needs `$se_module` when `What_Id` is set
  [Y:F45GH-yPisM 15:50].
- **Email:** each user integrates their own mailbox (admins cannot do it for them); IMAP recommended;
  Private vs Public sharing decides whether colleagues see the mail on the record. Emails from users who
  did not integrate, or who are private, are missing from records [Y:_Dn2IF2DVQM 24:05, 30:56][B34].
  Signals report opens, clicks, bounces and replies [Y:_Dn2IF2DVQM 09:21].
- **WhatsApp** creates a Messages module; free-form replies only inside 24 hours; initiate with
  Meta-approved templates [Y:_Dn2IF2DVQM 45:41, 47:00].

## 8. Custom modules, fields and layouts
- Create custom modules and fields at Setup > Customization > Modules and Fields; custom modules need
  Enterprise or above (Enterprise 100, Ultimate 500) [B41][Y:Ngm045YcMgc 14:29].
- A lookup with a "related list title" shows the custom module as a related list on the parent
  [Y:Ngm045YcMgc 14:29]. Name the related list after the module that holds the lookup
  [Y:0m05tx5_fVU 14:33].
- Field type choices that decide reportability: picklists (not text) for anything grouped; currency for
  money; user lookup for people; multi-select only when multiple values are certain; global picklist sets
  for shared lists [Y:m588QX4WmYA 49:24, 56:01, 61:22].
- Adding a Lead field: use the option to create the same field on Contacts, Accounts and Deals so the
  conversion mapping is created; otherwise data is lost on conversion [Y:m588QX4WmYA 60:02].
- Lead Source should describe the campaign or nature (Referral, Web, Open House), not the channel
  [Y:m588QX4WmYA 38:52].
- Formula fields compute only when a source field changes and trigger nothing; roll-up summary fields
  aggregate child values onto the parent (for example Sum of Amount where Stage = Closed Won)
  [Y:m588QX4WmYA 62:41, 67:57].
- Picklist History Tracking gives time-in-value for status fields [Y:m588QX4WmYA 56:01].
- Removing a field moves it to Unused (data kept); deleting is separate [Y:8QsKQ1PsGtQ 03:50].
- Custom modules have no pipelines; stage is a Status picklist plus workflows [Y:-D67j_-YhM0 50:09].

## 9. Automation that changes what you read
- Workflow rules: module, trigger (record action or date/time; also score and notes), condition,
  actions (field update, task, email, webhook, function, create record) [Y:Df8NuKBZW0I 03:00]
  [Y:0m05tx5_fVU 26:25]. "Repeat on every edit" re-fires while criteria match [Y:Ngm045YcMgc 19:17].
  Blank task owner goes to the record owner [Y:Df8NuKBZW0I 08:32].
- **Blueprint locks the stage field**: records move only through defined transitions, which explains
  failed stage updates from UI or API [Y:0IrMNcpzg58 15:05].
- Assignment rules trigger only on import, web form and API, not manual records [B22].
- Deluge: `zoho.crm.getRecordById`, `searchRecords`, `updateRecord`; a wrong API name in an update map
  fails silently [Y:Vy5OMHFJd_g 03:53, 14:00]. Function logs, revisions and credit analytics are on each
  function's page [Y:MA_Baod_Tzk 01:50, 05:45].
- Queries feature: live CRM, COQL or REST data rendered in Canvas, Kiosk and custom related lists
  [Y:ulbaHD97rOE 04:50][Y:C3ubARNjAU8 05:40].

## 10. Zia, Zia Chat and Zia Agents
- Zia Agents: Setup > Zia > Agents; build from scratch with instructions, knowledge base and tools
  (COQL, Search, Update scoped to modules), guardrails, deploy by connection or as a digital employee
  [Y:8ENy7rjO4AI 00:15, 03:10][B38]. Practitioners call them early; good at reading and writeups, weak
  at creating records [Y:Ngm045YcMgc 00:24][Y:JtVFSZVuY_k 05:08].
- Zia Chat (early access, 2026) reads across Zoho apps with the user's permissions; actions go through
  Zia agents [Y:JtVFSZVuY_k 00:16, 10:37].
- Model choice at Setup > Zia > Models (Zoho LLM default, OpenAI by key) [B37].
- Practice for customized orgs: wrap Zoho MCP in a skill that routes questions to the right module or app
  [Y:JtVFSZVuY_k 03:38]. This skill is that layer for Forecastable.

## 11. Editions, credits and limits
| Edition | USD per user per month (annual) | API credits per 24 h | Concurrency |
|---|---|---|---|
| Free | 0 | 5,000 | 5 |
| Standard | 14 | 50,000 + 250 per user (max 100,000) | 10 |
| Professional | 23 | 50,000 + 500 per user (max 3,000,000) | 15 |
| Enterprise / Zoho One | 40 | 50,000 + 1,000 per user (max 5,000,000) | 20 |
| Ultimate / CRM Plus | 52 | 50,000 + 2,000 per user (no max) | 25 |
Sources [B41][B48][B51][A41]. AUD ex GST annual: Standard 20, Professional 32, Enterprise 55,
Ultimate 73; AU page prices include 10% GST [B48][B50].
- Sub-concurrency 10 for COQL, Get Records with cvid or sort_by, and heavy writes; exceeding returns
  TOO_MANY_REQUESTS [A41]. Header `X-API-CREDITS-REMAINING` appears after 50% use [A41].
- Credit costs: most GETs 1; COQL 1 to 3; Get Records with cvid 3; Record Count 50; Bulk Read 50 [A41].
- Custom fields per module: Standard 10, Professional 155, Enterprise 300, Ultimate 500. Sandbox:
  Enterprise and Ultimate. Exports per day: Free 10 to Ultimate 1,000 [B41][B25].

## 12. Gotchas (ranked by how often they cost time)
1. Label is not API name; Meetings is `Events`; renamed fields keep old API names [A12][Y:Vy5OMHFJd_g 11:00].
2. API permission missing on the profile blocks every MCP and API call [B10][B15].
3. Directory connector data center bug; use the regional URL [B6].
4. `getRecords`/Get Records returns one page; the model stops early. Use COQL or a criteria search
   [Y:F45GH-yPisM 10:25].
5. Converted leads hidden by default in Get Records and Search [A24][A33].
6. Search index lag and fuzzy equals; not for counts [A33].
7. Datetime offsets: AU switches +10:00 and +11:00; QLD does not [A35].
8. Numbers differ by user because of roles and sharing [A13][B3].
9. Calls on personal mobiles, especially iPhone inbound, are not in Zoho [B30].
10. Emails exist only for users who integrated their mailbox with sharing on [Y:_Dn2IF2DVQM 30:56].
11. Blueprint-locked stages reject direct updates [Y:0IrMNcpzg58 15:05].
12. Report builder preview totals are partial [Y:MmWulZdg2kk 09:25].
13. Multi-select lookups need the linking module; subforms need the subform module [A35].

## 13. UNVERIFIED and CONFLICT (never state as fact)

| Item | Status | Detail | How to settle |
|---|---|---|---|
| COQL join limit | CONFLICT | v8 docs: 2 lookup hops [A34]; Zoho's COQL video: 5 base joins and 15 select-column joins [Y:_Jr2ur1wlqo 06:00] | Test a 3-hop query in the org; keep to 2 hops in production |
| COQL rows per criteria | CONFLICT | v8 docs: 100,000 via OFFSET [A34]; developer video (v6 era): 10,000 per unique query [Y:x-QiW-pVF2M 30:47] | Use keyset paging past 10,000 either way |
| COQL SELECT field cap | CONFLICT | Overview says 500, error table says 50 [A34][Y:x-QiW-pVF2M 19:10] | Keep to 50 |
| COQL rows per call | CONFLICT (minor) | Overview 2,000; v8 error table 200 [A34] | Handle LIMIT_EXCEEDED by dropping to 200 |
| `COUNT(id)` in COQL | UNVERIFIED | Docs example counts a field [A35] | Fall back to counting a lookup or picklist |
| Grant token lifetime | CONFLICT | 1, 2, 3 or 10 minutes across pages and videos [A7][A11][A46][Y:ZdicRo5Z6IU 12:26] | Use immediately |
| Bulk Read download rate | CONFLICT | Docs 10 per minute [A40]; video 50 per minute [Y:hTL0FMjG4x4 12:40] | Assume 10 |
| Notification channel expiry | UNVERIFIED | Presenter: 1 hour default, 24 hours max [Y:hTL0FMjG4x4 17:15] | Check current docs |
| `Crm_Implied_Api_Access` = Zoho CRM API Access toggle | UNVERIFIED | Strong inference [B10][B15] | Confirm after the admin flips it |
| Directory connector workaround for AU | UNVERIFIED | Custom connector with AU URL [B1][B6] | Test in the customer's Claude |
| 17 unnamed connector tools | UNVERIFIED | Listing names 24 of 41 [B1] | List tools after connecting |
| Standard profile has API access on by default | UNVERIFIED | [B10] | Check the profile |
| Deleting an Account deletes its Contacts and Deals | UNVERIFIED | Presenter claim [Y:CJtqyyYNOyU 30:00] | Never delete; moot for reads |
| Contacts are the parent of Leads | Treat as wrong | Presenter claim [Y:7jzz-jrTn1o 31:30]; standard model says Leads are standalone | Ignore |
| Mass email limit 1,000 per day, 100 at a time | UNVERIFIED | [Y:CJtqyyYNOyU 1:09:00] | Check by edition |
| Limit of lookup fields per module | UNVERIFIED | Customer admins sometimes cite a small cap; not found in docs this pass | Check Setup when designing |
| Zoho One plan labels and prices | UNVERIFIED | Inferred from pricing data file [B49] | Pricing page |
| Emails related list via MCP tools | UNVERIFIED | No obvious emails scope in the connector [B2] | Test |
| Multi-word module API names (`Sales_Orders`, `Price_Books`) | UNVERIFIED | [A23] | Read `/settings/modules` |
| Claude per-request token limits quoted in ZDH 25 | Treat as outdated | [Y:zZQChcQhV-8 18:25] | Ignore |

## 14. Sources

### API docs [A]
- [A1] Zoho CRM v8 Multi DC Support: https://www.zoho.com/crm/developer/docs/api/v8/multi-dc.html
- [A2] Zoho OAuth Multi DC support (accounts URLs incl. SA, UK): https://www.zoho.com/accounts/protocol/oauth/multi-dc.html
- [A3] Zoho accounts server info JSON: https://accounts.zoho.com/oauth/serverinfo
- [A4] Bigin (Zoho) Multi DC with zohoapis domains per DC: https://www.bigin.com/developer/docs/apis/multi-dc.html
- [A5] Zoho CRM v8 Scopes: https://www.zoho.com/crm/developer/docs/api/v8/scopes.html
- [A6] Zoho CRM v8 OAuth overview: https://www.zoho.com/crm/developer/docs/api/v8/oauth-overview.html
- [A7] Zoho CRM v8 Token Validity: https://www.zoho.com/crm/developer/docs/api/v8/token-validity.html
- [A8] Zoho Self Client overview: https://www.zoho.com/accounts/protocol/oauth/self-client/overview.html
- [A9] Zoho Self Client authorization code flow: https://www.zoho.com/accounts/protocol/oauth/self-client/authorization-code-flow.html
- [A10] Zoho CRM v8 Refresh Access Token: https://www.zoho.com/crm/developer/docs/api/v8/refresh.html
- [A11] Zoho CRM v8 Authorization Request: https://www.zoho.com/crm/developer/docs/api/v8/auth-request.html
- [A12] Zoho CRM v8 Get Modules: https://www.zoho.com/crm/developer/docs/api/v8/modules-api.html
- [A13] Zoho CRM v8 Module Metadata: https://www.zoho.com/crm/developer/docs/api/v8/module-meta.html
- [A14] Zoho CRM v8 Fields Metadata: https://www.zoho.com/crm/developer/docs/api/v8/field-meta.html
- [A15] Zoho CRM v8 Layouts Metadata: https://www.zoho.com/crm/developer/docs/api/v8/layouts-meta.html
- [A16] Zoho CRM v8 Related Lists Metadata: https://www.zoho.com/crm/developer/docs/api/v8/related-list-meta.html
- [A17] Zoho CRM v8 Custom Views Metadata: https://www.zoho.com/crm/developer/docs/api/v8/custom-view-meta.html
- [A18] Zoho CRM v8 Get Users: https://www.zoho.com/crm/developer/docs/api/v8/get-users.html
- [A19] Zoho CRM v8 Roles: https://www.zoho.com/crm/developer/docs/api/v8/get-roles.html
- [A20] Zoho CRM v8 Profiles: https://www.zoho.com/crm/developer/docs/api/v8/get-profiles.html
- [A21] Zoho CRM v8 Organization: https://www.zoho.com/crm/developer/docs/api/v8/get-org-data.html
- [A22] Zoho CRM Help: API Names: https://www.zoho.com/crm/help/api-names.html
- [A23] Zoho CRM v8 Create Custom Field (field types, supported modules incl. Visits, DealHistory): https://www.zoho.com/crm/developer/docs/api/v8/create-custom-field.html
- [A24] Zoho CRM v8 Get Records: https://www.zoho.com/crm/developer/docs/api/v8/get-records.html
- [A25] Zoho CRM v8 Get Related Records: https://www.zoho.com/crm/developer/docs/api/v8/get-related-records.html
- [A26] Zoho CRM v8 Get Notes: https://www.zoho.com/crm/developer/docs/api/v8/get-notes.html
- [A27] Zoho CRM v8 Get Attachments: https://www.zoho.com/crm/developer/docs/api/v8/get-attachments.html
- [A28] Zoho CRM v8 Get Emails of a Record: https://www.zoho.com/crm/developer/docs/api/v8/get-email-rel-list.html
- [A29] Zoho CRM v8 Timeline of a Record: https://www.zoho.com/crm/developer/docs/api/v8/timeline-of-a-record.html
- [A30] Zoho CRM v8 Deleted Records: https://www.zoho.com/crm/developer/docs/api/v8/get-deleted-records.html
- [A31] Zoho CRM v8 Related Records Count: https://www.zoho.com/crm/developer/docs/api/v8/get-related-records-count.html
- [A32] Zoho CRM v8 Record Count in a Module: https://www.zoho.com/crm/developer/docs/api/v8/module_record_count.html
- [A33] Zoho CRM v8 Search Records: https://www.zoho.com/crm/developer/docs/api/v8/search-records.html
- [A34] Zoho CRM v8 COQL Overview: https://www.zoho.com/crm/developer/docs/api/v8/COQL-Overview.html
- [A35] Zoho CRM v8 Get Records through COQL Query: https://www.zoho.com/crm/developer/docs/api/v8/Get-Records-through-COQL-Query.html
- [A36] Zoho CRM v8 Bulk Read overview: https://www.zoho.com/crm/developer/docs/api/v8/bulk-read/overview.html
- [A37] Zoho CRM v8 Create Bulk Read Job: https://www.zoho.com/crm/developer/docs/api/v8/bulk-read/create-job.html
- [A38] Zoho CRM v8 Bulk Read Job Details: https://www.zoho.com/crm/developer/docs/api/v8/bulk-read/job-details.html
- [A39] Zoho CRM v8 Download Bulk Read Result: https://www.zoho.com/crm/developer/docs/api/v8/bulk-read/download-result.html
- [A40] Zoho CRM v8 Bulk Read Limitations: https://www.zoho.com/crm/developer/docs/api/v8/bulk-read/limitations.html
- [A41] Zoho CRM v8 API Limits: https://www.zoho.com/crm/developer/docs/api/v8/api-limits.html
- [A42] Zoho CRM v8 Insert Records (mandatory fields, Calls/Events field semantics): https://www.zoho.com/crm/developer/docs/api/v8/insert-records.html
- [A43] Kaizen #125 Multi-Select Lookup (MxN) via APIs: https://help.zoho.com/portal/en/community/topic/kaizen-125-manipulating-multi-select-lookup-fields-mxn-using-zoho-crm-apis
- [A44] Kaizen #32 Handling Custom Modules: https://help.zoho.com/portal/en/community/topic/kaizen-32-handling-custom-modules-with-zoho-crm-api
- [A45] Zoho CRM What's New in V8: https://www.zoho.com/crm/developer/docs/api/v8/whats-new.html
- [A46] Zoho CRM v8 Access and Refresh Tokens: https://www.zoho.com/crm/developer/docs/api/v8/access-refresh.html

### Product, MCP, help and pricing [B]
- [B1] https://claude.com/connectors/zoho-crm
- [B2] Direct HTTP checks 2026-09-29: https://claude-zohocrm.zohomcp.com.au/.well-known/oauth-protected-resource , https://claude-zohocrm.zohomcp.com.au/.well-known/oauth-authorization-server , https://mcp.zoho.com.au , https://mcp.zoho.eu , https://crm.zoho.com.au
- [B3] https://www.zoho.com/crm/developer/mcp.html
- [B4] https://www.zoho.com/crm/developer/docs/mcp/overview.html
- [B5] https://www.zoho.com/crm/developer/docs/mcp/setup/claude.html
- [B6] https://github.com/anthropics/claude-ai-mcp/issues/311
- [B6b] https://help.zoho.com/portal/en/kb/mcp/getting-started/articles/zoho-mcp-help-documentation-29-9-2025
- [B7] https://www.zoho.com/mail/help/mcp/mcp-server-configuration.html
- [B8] https://www.zoho.com/au/billing/help/ai/mcp.html
- [B9] https://www.zoho.com/mcp/pricing.html
- [B9b] https://www.zoho.com/mcp/
- [B10] https://help.zoho.com/portal/en/kb/crm/users-and-control/profile-management/articles/manage-profile-permissions
- [B11] https://help.zoho.com/portal/en/kb/crm-nextgen/security-control/profile-management/articles/nextgen-manage-profile-permissions
- [B12] https://help.eazybe.com/en/integrations/zoho/api-access
- [B13] https://help.zoho.com/portal/en/community/topic/zoho-crm-with-built-in-mcp-support
- [B14] https://www.zoho.com/us/books/help/mcp/zoho-books-mcp.html
- [B15] https://help.zoho.com/portal/en/community/topic/organization-api-code-403-crm-implied-api-access-error-for-https-www-zohoapis-com-crm-v2-org
- [B16] https://www.zoho.com/crm/developer/docs/api/v8/update-profile-permission.html
- [B17] https://help.zoho.com/portal/en/kb/crm/using-crm-for-everyone/zoho-crm-next-gen-ui/articles/faq-transition-to-the-nextgen-ui
- [B18] https://help.zoho.com/portal/en/community/topic/navigate-with-ease-announcing-improvements-to-your-zoho-crm-for-everyones-setup-experience-13-10-2025
- [B19] https://help.zoho.com/portal/en/kb/crm/customize-crm-account/customizing-fields/articles/use-custom-fields
- [B20] https://www.zoho.com/crm/developer/docs/api/v8/multi-dc.html
- [B21] https://www.zoho.com/crm/help/automation/workflow-rules-email.html
- [B22] https://help.zoho.com/portal/en/kb/crm/faqs/automation/assignment-rules/articles/faqs-assignment
- [B23] https://help.zoho.com/portal/en/kb/crm/process-management/blueprint/articles/design-a-blueprint
- [B24] https://help.zoho.com/portal/en/kb/crm-nextgen/experience-center/commandcenter/commandcenter-in-zoho-crm-2-0/articles/orchestrate-customer-journey-using-commandcenter-from-zoho-crm
- [B25] https://help.zoho.com/portal/en/kb/crm/faqs/data-administration/export/articles/faqs-exporting-data-from-zoho-crm
- [B26] https://help.zoho.com/portal/en/kb/articles/recycle-bin
- [B27] https://help.zoho.com/portal/en/kb/crm-nextgen/security-control/audit-log/articles/nextgen-monitor-audit-log
- [B28] https://www.zoho.com/crm/developer/docs/api/v8/purchase-from-dashboard.html
- [B29] https://help.zoho.com/portal/en/kb/crm-nextgen/crm-mobile-app/android/articles/communicating-with-customers-28-8-2024
- [B30] https://help.zoho.com/portal/en/kb/crm-nextgen/crm-mobile/apple/collaboration-and-communication/articles/nextgen-communicating-with-customers-through-iphone
- [B31] https://help.zoho.com/portal/en/kb/crm/faqs/roles-and-profiles/articles/faqs-roles-and-profiles
- [B32] https://www.zoho.com/crm/developer/docs/connectors/set-up.html
- [B33] https://www.zoho.com/crm/developer/docs/api/v8/register-client.html
- [B34] https://help.zoho.com/portal/en/kb/crm/connect-with-customers/email/user-functions/articles/email-configuration-for-imap-and-pop3
- [B35] https://help.zoho.com/portal/en/kb/crm/faqs/integration/articles/faqs-zoho-phonebridge-16-2-2023
- [B36] https://help.zoho.com/portal/en/kb/crm/connect-with-customers/telephony/articles/using-built-in-telephony
- [B37] https://help.zoho.com/portal/en/community/topic/switch-between-multiple-llms-instantly-for-tailored-zia-experiences
- [B38] https://help.zoho.com/portal/en/kb/crm-nextgen/zia-artificial-intelligence/nextgen-agentic-ai/articles/nextgen-zia-agents-in-zoho-crm
- [B39] https://www.zoho.com/crm/help/api-names.html
- [B40] https://help.zoho.com/portal/en/kb/crm/customize-crm-account/managing-module-views/articles/module-views
- [B41] https://www.zoho.com/crm/comparison.html
- [B42] https://help.zoho.com/portal/en/community/topic/zoho-crm-community-digest-march-2026-part-1
- [B43] https://help.zoho.com/portal/en/community/topic/kaizen-38-calls-api
- [B44] https://www.zoho.com/crm/help/automation/calls-transition.html
- [B45] https://www.zoho.com/sites/default/files/crm/help/working-with-calls.pdf
- [B46] https://help.zoho.com/portal/en/community/topic/mobile-apps-not-automatically-logging-calls
- [B47] https://help.zoho.com/portal/en/kb/crm/salesinbox/getting-started/articles/zoho-salesinbox-your-sales-focused-email-client
- [B48] https://www.zoho.com/sites/zweb/json/pricing/crm-pricing-val.json (data file used by https://www.zoho.com/en-us/crm/zohocrm-pricing.html)
- [B49] https://www.zoho.com/sites/zweb/json/pricing/one-pricing-val.json
- [B50] https://www.zohowebstatic.com/sites/zweb/js/template/zp_pricing.js
- [B51] https://www.zoho.com/crm/developer/docs/api/v8/api-limits.html
- [B52] https://www.zoho.com/en-us/crm/zohocrm-pricing.html
- [B53] https://www.businesswire.com/news/home/20250204066995/en/Zoho-Corporation-Announces-Zia-Agents-AI-Platform-Supporting-Autonomous-Agents-Across-Organizations-Broad-Portfolio
- [B54] https://www.hpcwire.com/bigdatawire/this-just-in/zoho-launches-zia-llm-introducing-prebuilt-agents-agent-builder-mcp-and-marketplace/
- [B55] https://www.zoho.com/crm/zia/agents.html

### Videos [Y] (timestamped notes in `research/transcript_notes0-2.md`; raw transcripts kept in the zoho-crm-transcripts.zip bundle, not in the project)
| Tag | Title | Channel | Date | Length | Topic |
|---|---|---|---|---|---|
| [Y:_Jr2ur1wlqo] | [Zoho CRM Developer Series: Zoho CRM APIs - Part 6: Mastering COQL](https://www.youtube.com/watch?v=_Jr2ur1wlqo) | Zoho (@Zoho) | 2025-05-29 | 21:28 | COQL |
| [Y:x-QiW-pVF2M] | [Zoho CRM Developer Series: Zoho CRM APIs - Part 3: Search API and COQL](https://www.youtube.com/watch?v=x-QiW-pVF2M) | Zoho (@Zoho) | ~2024-06 | 35:53 | COQL / Search API |
| [Y:hTL0FMjG4x4] | [Zoho CRM Developer Series: Zoho CRM APIs - Part 4: Bulk Read and Notification APIs, and Data Sync](https://www.youtube.com/watch?v=hTL0FMjG4x4) | Zoho (@Zoho) | 2024-07-09 | 29:31 | Data export / Bulk Read API |
| [Y:ZdicRo5Z6IU] | [Zoho CRM Developer Series: Zoho CRM APIs - Part 1](https://www.youtube.com/watch?v=ZdicRo5Z6IU) | Zoho (@Zoho) | ~2024-04 | 44:28 | API fundamentals / OAuth |
| [Y:-D67j_-YhM0] | [Zoho CRM Developer Series: Zoho CRM APIs - Part 8 - CRUD Operations with Metadata APIs](https://www.youtube.com/watch?v=-D67j_-YhM0) | Zoho (@Zoho) | ~2025 | 1:03:20 | Custom modules / Metadata API |
| [Y:ulbaHD97rOE] | [Zoho CRM Developer Series: Queries - Part 1: Introduction and Basics](https://www.youtube.com/watch?v=ulbaHD97rOE) | Zoho (@Zoho) | ~2025 | 24:13 | Queries (COQL in UI) |
| [Y:C3ubARNjAU8] | [NEW! How to Use Queries in Zoho CRM / No Code](https://www.youtube.com/watch?v=C3ubARNjAU8) | Zenatta Consulting (@Zenatta) | ~2025 | 11:45 | Queries (COQL in UI) |
| [Y:OAYGHWSCitY] | [Inbox to CRM: Automate Lead Management / #claude AI + #Google Apps Script + #zohocrm](https://www.youtube.com/watch?v=OAYGHWSCitY) | OfficeHubTech (@OfficeHubTech) | 2026-09-21 | 12:32 | API v8 / COQL / Claude |
| [Y:F45GH-yPisM] | [How to Set Up and Use Zoho MCP // Hands on Demo and Tutorial](https://www.youtube.com/watch?v=F45GH-yPisM) | Zenatta Consulting (@Zenatta) | 2026-05-27 | 23:14 | Zoho MCP / Claude |
| [Y:325hWpN_lEs] | [Zoho MCP FULL Tutorial 2026 // How to USE MCP](https://www.youtube.com/watch?v=325hWpN_lEs) | Zenatta Consulting (@Zenatta) | 2026-08-13 | 34:35 | Zoho MCP / Claude |
| [Y:UGi0tFOyWYg] | [Zoho MCP - Connect in 2 minutes - Save hours!](https://www.youtube.com/watch?v=UGi0tFOyWYg) | CRMOZ (@CRMOZ) | 2026-04-02 | 6:32 | Zoho MCP / Claude |
| [Y:39lBp8seCAU] | [Turn Zoho into Conversational AI Workspace with Claude & MCP / Zoho Developer Hangout (ZDH) - 30](https://www.youtube.com/watch?v=39lBp8seCAU) | Zoho (@Zoho) | 2026-07-08 | 26:06 | Zoho MCP / Claude Skills |
| [Y:zZQChcQhV-8] | [Zoho Developer Hangout 25 / AI-Powered Sales Automation: Zoho CRM + Claude + MCP Server](https://www.youtube.com/watch?v=zZQChcQhV-8) | Zoho (@Zoho) | 2025-08-07 | 35:35 | Custom MCP server / API limits |
| [Y:JtVFSZVuY_k] | [Zia Chat // Built-in LLM Across Zoho](https://www.youtube.com/watch?v=JtVFSZVuY_k) | Zenatta Consulting (@Zenatta) | 2026-09-28 | 12:37 | Zia / AI |
| [Y:8ENy7rjO4AI] | [How to Use ZIA AI Agents in Zoho CRM for Beginners](https://www.youtube.com/watch?v=8ENy7rjO4AI) | Drew Brockbank | Brockbank Consulting (@drewbrockbank) | 2026-06-15 | 10:31 | Zia Agents |
| [Y:MmWulZdg2kk] | [How to Use Reports and Dashboards in Zoho CRM to Improve Your Sales Performance](https://www.youtube.com/watch?v=MmWulZdg2kk) | Zoho (@Zoho) | 2026-09-29 | 12:28 | Reports / dashboards |
| [Y:-zZ-1nJ-IEc] | [Mastering Reports & Dashboards in Zoho CRM](https://www.youtube.com/watch?v=-zZ-1nJ-IEc) | Zenatta Consulting (@Zenatta) | ~2025 | 27:37 | Reports / dashboards |
| [Y:7jzz-jrTn1o] | [Role Based Reporting in Zoho CRM - Zoho Admin Beginner (Part 4)](https://www.youtube.com/watch?v=7jzz-jrTn1o) | Zoho (@Zoho) | ~2026-06 | 56:30 | Reports / roles and data visibility |
| [Y:cuBin4KtrpM] | [Zoho Analytics Tutorial and Training // Working with Zoho CRM Data](https://www.youtube.com/watch?v=cuBin4KtrpM) | Zenatta Consulting (@Zenatta) | ~2025-11 | 38:23 | Data export / analytics |
| [Y:m588QX4WmYA] | [Customizing CRM Layouts for Data Capture and Flow - Zoho Admin Beginner (Part 1)](https://www.youtube.com/watch?v=m588QX4WmYA) | Zoho (@Zoho) | ~2026-06 | 1:10:18 | Modules, fields, layouts |
| [Y:8QsKQ1PsGtQ] | [How to Create and Customize Modules in Zoho CRM](https://www.youtube.com/watch?v=8QsKQ1PsGtQ) | Zoho (@Zoho) | ~2026-05 | 14:15 | Standard and custom modules |
| [Y:0m05tx5_fVU] | [Zoho CRM for Everyone 2025 Full Tutorial // What's New?](https://www.youtube.com/watch?v=0m05tx5_fVU) | Zenatta Consulting (@Zenatta) | ~2025 | 48:29 | CRM for Everyone new UI |
| [Y:Ngm045YcMgc] | [Zoho CRM Product Overview for Beginners 2026](https://www.youtube.com/watch?v=Ngm045YcMgc) | Zenatta Consulting (@Zenatta) | ~2026-08 | 28:31 | CRM navigation / overview |
| [Y:CJtqyyYNOyU] | [Zoho CRM FULL Beginners Tutorial 2026 / Complete Training Course](https://www.youtube.com/watch?v=CJtqyyYNOyU) | Drew Brockbank | Brockbank Consulting (@drewbrockbank) | 2026-02-26 | 3:15:01 | CRM navigation / admin |
| [Y:0IrMNcpzg58] | [Blueprints Tutorial for Zoho CRM / 2026](https://www.youtube.com/watch?v=0IrMNcpzg58) | Zenatta Consulting (@Zenatta) | ~2026-02 | 22:58 | Blueprint |
| [Y:Df8NuKBZW0I] | [How to Create Workflow Rules in Zoho CRM](https://www.youtube.com/watch?v=Df8NuKBZW0I) | Zoho (@Zoho) | ~2026-06 | 13:33 | Workflow rules |
| [Y:MA_Baod_Tzk] | [BIG Updates to Zoho Deluge Management in Zoho CRM](https://www.youtube.com/watch?v=MA_Baod_Tzk) | Zenatta Consulting (@Zenatta) | 2026-08-26 | 10:03 | Deluge / functions |
| [Y:Vy5OMHFJd_g] | [Zoho Deluge Functions Beginner Tutorial // Write your first Script EASY](https://www.youtube.com/watch?v=Vy5OMHFJd_g) | Zenatta Consulting (@Zenatta) | ~2025 | 20:18 | Deluge |
| [Y:_Dn2IF2DVQM] | [Enable Customer Communication through Zoho CRM - Zoho Admin Beginner (Part 5)](https://www.youtube.com/watch?v=_Dn2IF2DVQM) | Zoho (@Zoho) | 2026-08-07 | 51:57 | Call logging / telephony / email |
| [Y:M3iX6q1SjOk] | [Zoho Voice walk through demo!](https://www.youtube.com/watch?v=M3iX6q1SjOk) | Avon Collis on Zoho (@avon.collis) | 2026-02-19 | about 8 min (from chapters, not verified) | Telephony (Australia) |
