<!-- Library file for crossbeam-admin-reference.md. Source: Crossbeam Help Center, extracted September 25th, 2026. Cite (HC number); confirm in-app when a screen may have moved. -->

# Crossbeam Admin Reference A: Getting Started, Data Sources, Populations, Matching Engine

Source: 42 Help Center articles (Getting Started, Data Sources and Populations, Matching Engine). Citations are (HC nnnn). Conflicts between articles are listed in section 20.

---

## 1. Platform model in one paragraph

Crossbeam is a SaaS Partnership Ecosystem Platform that syncs with your CRM data, standardizes it into segments called Populations, and lets you share and compare those Populations with partners (HC 3159940). Core objects and their relationships (HC 3160166):

- **Data Sources**: systems Crossbeam syncs from (Salesforce, HubSpot, custom data sources, CSV uploads). Connecting a data source shares nothing; it only syncs data into Crossbeam. Sharing decisions come later (HC 6805089, HC 10055030).
- **Populations**: segments of people or companies from a data source, usually mapped to funnel stages (leads, qualified opportunities, customers). They are the basis for data sharing and are kept up to date automatically by the data integrations (HC 3160166).
- **Overlaps**: a match between a record in your Population and a Population of your partner. Data Sharing uses Overlaps as a condition for exposing data; Reports use Overlaps to show intersections. Overlaps impact billing tier (HC 3160166).
- **Partners**: companies you collaborate with. Partnerships are established only through a double opt-in invite system. Data sharing and overlap analysis are only available once a partnership exists (HC 3160166).
- **Data Sharing Rules**: control what conditions must be met for data to be exposed, and what data is shared when they are (HC 3160166).
- **Data Sharing Requests**: the Request Data feature lets you choose data you want from established partners and send them a request inside Crossbeam (HC 3160166).
- **Integrations**: export overlap data by pushing into Salesforce, exporting to CSV, or via the REST API (HC 3160166).
- **Record Exports**: transfer enriched account-mapping data to external platforms (data warehouses such as Snowflake, integrations, CRMs). Each record counts once per subscription term regardless of number of integrations, destinations, partners, or overlaps, and regardless of how many times it is updated in that term (HC 3160166).
- **User Roles**: determine access levels in Crossbeam and Crossbeam for Sales; roles are customizable (HC 3160166).

---

## 2. Navigation (current and legacy)

### 2.1 Current navigation bar (HC 11021727)

What changed versus the old nav:

| Feature | Change |
|---|---|
| Search bar | Moved into the navigation |
| Ask AI | Moved in the navigation |
| Pipeline Generation | Moved from Deal Navigator into the main navigation |
| Lists | Central hub to find, manage, create, and share all Lists |
| Messages | Replaces Collaboration |

Also new: a dedicated Copilot section that groups Get Intel, Playbooks, and more; streamlined Ecosystem and Insights categories; action-first pathways into lead discovery and prospecting (HC 11021727).

**Full Access Seat view.** Top of nav: Search, Notifications, Ask AI. Nav grouped into three focus areas; Full Access users land in Ecosystem by default (HC 11021727).

- **Ecosystem**: Partners (Partner List, Pending Requests, Sharing Dashboard), Lists, Messages, Performance, Attribution.
- **Revenue**: Account Mapping, Deal Navigator, Performance.
- **Workspace**: Data (Data Sources, Populations, Default Sharing), Integrations, Settings (Organization Settings, Sales Settings, Team, Roles & Permissions, Plan & Billing, Profile & Preferences), Labs.

**Sales Seat view.** Default landing is the Revenue section, containing Pipeline Generation, Deal Navigator, Lists, Messages, and Settings (HC 11021727).

Admin click path shorthand used throughout this reference: **Data > Data Sources** (app.crossbeam.com/data-sources) and **Data > Populations** (app.crossbeam.com/populations).

### 2.2 Legacy icon navigation (HC 3160087, superseded by HC 11021727)

Useful URLs: Home app.crossbeam.com/home, Activity /notifications, Partners /partners, Mapping /reports, Measure /attribution, Data /data-sources, Settings /organization/settings, Billing /billing. Partner detail shows Account Mapping Matrix, Potential Revenue, Top Overlaps, Population Breakdowns, Total Attributed, Sharing Settings. Missing Homepage sections mean no data yet.

---

## 3. Sign-up and first-run onboarding

### 3.1 Creating an account (HC 9713136)

1. Go to crossbeam.com, click **Sign-Up for Free**.
2. Enter work email, first and last name, create and confirm password. Check the box agreeing to Terms of Service and Privacy Policy. Click **Create Account**.
3. Verify via the email Crossbeam sends, then log in.
4. If your company already has a Crossbeam account, you get a prompt to request to join it: add a message, click **Request to Join**. Once approved you receive an email invite.

Next steps after sign-up: connect a data source and invite partners. Support: the Crossbeam support inbox (support at crossbeam.com), plus office hours (HC 9713136).

### 3.2 Product tour (HC 3161958)

First login runs a four-step tour on sample open data: Prospects Preview (Lookalike Prospects), Overlapping Accounts, Take Action (export multi-partner overlaps), Connect with Partners. **Go to Onboarding** skips it; **Done** finishes it.

### 3.3 Four onboarding steps (HC 3161958)

1. **Connect a Data Source.** Click **Complete Setup**. CRM recommended; Google Sheet or CSV also allowed. If someone else must complete the CRM connection, click **Invite Your CRM Admin** to send them access. Issues: support chat or the Crossbeam support inbox (support at crossbeam.com).
2. **Define Your Populations.** Create three: **Customers** (current customers), **Prospects** (accounts actively pursued), **Open Opportunities** (deals in pipeline). Click **Continue** when all three are defined.
3. **Set Your Sharing Settings.** Default: only overlapping accounts are visible to partners. Adjust via the dropdown under **Sharing Accounts**; optionally create field presets to control which fields are shared. Click **Continue**. Sharing can be changed later from partner settings.
4. **Invite a Partner.** Search partner by company name, enter a contact email, optional personal message, click **Invite**, or **Skip** to finish without inviting.

After onboarding: invite more partners (app.crossbeam.com/partners), review partner list, start account mapping. For inviting many partners at once and tracking invitation status, use **Partner Invitations** (upload a target partner list, manage outreach from one workspace). AI Chat in the nav can help prioritize partners (HC 3161958).

### 3.4 Lookalike Prospects Population (HC 15507121)

- Auto-generated at sign-up. Crossbeam verifies your company domain, identifies similar accounts using customer data sourced and maintained by Crossbeam, creates a **Lookalike Prospects** Population, and maps it against an **Open Data Partner (ODP)**. First view in Crossbeam is an overlap report of which lookalike prospects are customers of the selected ODP. No setup required.
- If Crossbeam cannot confidently generate a tailored list, the Population appears as **Sample Prospects**. It behaves identically.
- Behaves like any custom Population: view in Populations, filter in Lists, run overlap reports, edit, delete. Remains available after onboarding.
- **One-time snapshot. Does not sync or refresh.**
- **Open Data Partners**: curated technology vendors whose customer data is sourced and maintained by Crossbeam. Overlaps are instant with no invitation, connection, or data-sharing agreement.
- Delete it from Populations like any custom Population.

---

## 4. Plans, trials, and feature gating

### 4.1 Plan gates stated in this article set

| Capability | Free / Explorer | Connector | Supernode | Enterprise | Source |
|---|---|---|---|---|---|
| Custom Populations | No | Yes | Yes | (not stated in HC 7239725; Yes per HC 14827573 Product2 table) | HC 7239725, HC 14827573 |
| Product2 in Standard Populations | Yes | Yes | Yes | Yes | HC 14827573 |
| Product2 in Custom Populations | No | Yes | Yes | Yes | HC 14827573 |
| Databricks as a Data Source | Yes | Yes | Yes | Yes | HC 15231542 |
| Snowflake as a Data Source | All plans | | | | HC 4470887 |
| Pipedrive as a Data Source | All plans (no Copilot, no pushing custom objects to Pipedrive) | | | | HC 10055030 |
| REST API access | No | Yes | Yes | | HC 4136739 |
| Partner Workshops (enablement) | No | Yes | Yes | | HC 12004979 |
| AI Chat | All plans; access varies by plan and seat type | | | | HC 11731834 |

Salesforce requires a Salesforce edition with API access (HC 7197979).

### 4.2 Connector free trial (HC 10644667)

- **Eligibility**: new users on the free **Explorer** plan who have completed onboarding.
- **Gate**: all onboarding steps must be complete. If incomplete, the **Request Free Trial** button still shows, but clicking it shows a message prompting you to finish onboarding.
- **Where**: **Request Free Trial** button, top-right corner of the app.
- **Flow**: click it to see included features; pick a date on the calendar to book time with sales; if no times shown or you prefer direct outreach, click **Talk to Sales** (sends a request). A confirmation message appears. Sales activates the trial.
- **Trial terms**: 30 days, full Connector experience including the Copilot Chrome extension. Export limit **100 records per report**. **Connecting integrations is not allowed** during the trial. Data sharing unchanged. **Max 3 users**.
- If certain Connector features were used, access is retained until the account is downgraded. You can upgrade any time during the trial in-app or via sales.

### 4.3 Enablement and training offers

**Standard catalog (HC 12004979)**

| Offer | Key terms | Price |
|---|---|---|
| Team Enablement (Basic) | Up to 3 standard topics, one team per session, up to 30, 45 min | From $500/session |
| Team Enablement (Customized) | 30-min scoping plus 45-min session, up to 30 | From $1,500/session |
| Recurring Dedicated Office Hours | Up to 2 customized sessions/month for Sales, CSMs, or Marketing, up to 15 | From $2,500/month |
| ELG Certification Bootcamp | Sellers with Sales seats, up to 25, 90 or 60 min | Not stated |
| Partner Workshops (Connector and Supernode only) | 30-min alignment plus 45-min workshop, 1 person per side | Not stated |
| Enablement Pathways | Two scoping calls, 45-min live session, 8 weeks weekly content, bi-weekly challenges, up to 30 | Not stated |
| Public Office Hours | No account needed | Free |
| Crossbeam Academy | 100+ lessons; certifications: Salesforce-Powered Admin, HubSpot-Powered Admin, Crossbeam Partner Manager | Free with a login |

**Enablement Pathways (HC 12771021)**: four stages (Pre-Enablement scoping, 45-min Live Enablement, Growth and Reflection Weeks, Final Goal review). Start via your Account Success Manager (ASM) or the Crossbeam support inbox (support at crossbeam.com).

**Connector plan catalog (HC 14854896)**: Team Enablement from $500/session; Custom Team Enablement (two 30-min scoping sessions plus 45-min live session) from $1,500/session; both up to 30 participants.

---

## 5. Crossbeam AI Chat (HC 11731834)

- Role-aware assistant; icon top-right of the app ("Ask AI" in nav, HC 11021727). Answers adapt to seat type (Sales Seat vs Full Access) and permissions. All plans; access varies by plan and seat.
- Retrieves overlap insights and influence signals, answers questions (e.g. "Which deals have partner overlap but no activity?"), drafts intros, and executes actions only when prompted: create a smart list, send a Slack message, trigger a Salesforce update.
- Data: your partner data (overlaps, attribution fields, CRM context), ELG playbooks, Help Center, public data (job postings, company websites). Integrated with Slack, Salesforce, Lists (beta).
- LLM with OpenAI as subprocessor. Customer data is not used to train the LLM; only your account's data is accessed.

---

## 6. Data sources: choosing and general rules

### 6.1 Supported source types (HC 6805089, HC 5391508)

CRMs: Salesforce, HubSpot, Microsoft Dynamics, Pipedrive. Data warehouses: Snowflake, Databricks. Files: Google Sheets, CSV. To add: **Data > Data Sources**, locate the source tile, click the tile name (HC 6805089).

### 6.2 Tradeoffs (HC 5391508)

- Google Sheets and CSV: free, fast, good for first account mapping and one-off comparisons. Sheets can be updated dynamically; unlimited CSVs can be stored, but CSVs are static and must be refreshed manually.
- CRMs and warehouses: update automatically several times a day; may need initial configuration.
- Advanced CRM customization (via support): choose default synced fields, filter to build suppression streams or segments. Changeable any time, but filtering is **not applied retroactively**; you can re-sync and re-customize.

### 6.3 Common sync configuration pattern (CRMs)

Applies to Salesforce, HubSpot, Microsoft Dynamics, Pipedrive (HC 3160182, HC 3160183, HC 6952388, HC 10055030):

1. After connecting, choose a sync option: **Recommended** (best for full feature range) or **Custom** (define your own selection). Hover to see field names.
2. Review fields, then click **Sync Now** or **Customize**.
3. Customize: from the source's **Settings**, click **Field Sync > Edit** (Pipedrive: from the Review Fields modal click **Customize**). Expand tables under **All Data** or search; select/deselect fields; use **Toggle** to switch entire tables on/off. Click **Review Fields** then **Sync Now**, or **Go Back** to edit.
4. **Data Presets** (left side of Customize modal, highlighted blue). Hover to see required fields; click to apply:
   - **Account Mapping**: compare data to identify overlapping prospects, opportunities, customers.
   - **Pipeline Map**: visibility into partner pipeline for acceleration and forecasting.
   - **Co-Market**: target overlapping accounts for better-together stories and integration outreach.
   - **Co-Sell**: surface pre-vetted overlapping accounts.
   - **Refer**: give and get warm intros (listed only in the Salesforce article, HC 3160182).
5. **Settings** (on Data Sources, hover the three dots at the end of the row, or the gear icon): View Connection Status and Details (status, error messages, reauthorization needs), **Update Frequency** dropdown, **Edit Data Sync** (opens Customize pop-up), **Remove Data Source**.
6. An email confirmation arrives when the sync completes; then build Populations (HC 3160182, HC 10055030).

For best matching accuracy, sync using the **Co-Selling Preset** (HC 3160297).

Adding filters from fields not yet synced: in the Population Builder filter area, **Add Filters from another object** opens the same Customize Fields modal (HC 3160198). See section 13.

### 6.4 Connection statuses (Salesforce and HubSpot) (HC 3380461, HC 3380769)

- **Active**: syncing on schedule.
- **Not Syncing**: paused; no sync until made active.
- **Error**: hit an error, unable to sync; details shown if available.

Pipedrive shows **Setting up** while the initial sync processes, then **Active** (HC 10055030). CSV re-mapping shows a processing status until complete (HC 3160473).

---

## 7. Salesforce as a data source

### 7.1 Requirements

**Crossbeam side**: Full Access Role: **Admin**. Check seat on the Team page (app.crossbeam.com/team) (HC 3160182).

**Salesforce edition**: must include API access (HC 7197979).

**Salesforce admin permissions** (HC 3160182):

| Permission | Required? |
|---|---|
| API Enabled | Required |
| View All Users | Optional (HC 7197979 says Recommended) |
| View Setup and Configuration | Optional (HC 7197979 says Recommended; HC 4136739 says the authenticating user must have it or you get `API_DISABLED_FOR_ORG: limits resource is not enabled`) |

**Object permissions** (HC 3160182): Account Read (Required), Contact Read (Optional), Lead Read (Optional), Opportunity Read (Optional), User Read (Optional). Read access to Account **or** Lead is required; if only syncing Lead, Account is not required (HC 3160182, HC 7197979).

**Required fields** (HC 3160182, HC 7197979):
- Id, Owner Id: identifying records.
- Name, Website: matching algorithm.
- IsDeleted, SystemModstamp, CreatedAt: record-level bookkeeping.

**Minimum fields by object** (HC 3160182): Account: Account ID, Account Name, Account Website, Owner ID. Contact: Account ID, Contact Email, Contact ID. Lead: Lead Email, Lead ID, Owner ID. Opportunity: Account ID, Opportunity ID. Opportunity Contact Role: Contact ID, Contact Role ID, Opportunity ID, Primary, Role. User: Account Owner Email, User ID. These are the bare minimum; GTM use cases may need more.

### 7.2 Connect (HC 3160182)

1. **Data > Data Sources**, scroll to the Salesforce tile, click **Salesforce**.
2. Choose **Connect to Sandbox** or **Connect to Salesforce** (production). OAuth authentication.
3. Choose Recommended or Custom sync; review; **Sync Now** or **Customize** (see 6.3). Presets include Refer.
4. Email confirmation on completion; then build Standard Populations.

### 7.3 How the Salesforce sync works (HC 7197979)

- **API**: Bulk API 2.0, not the REST API. Subject to different quotas than the standard REST API.
- **Batch size**: 10,000 records at a time by default; contact the Crossbeam support inbox (support at crossbeam.com) to customize.
- **Incremental**: initial sync pulls everything and sets a bookmark at completion time. Later syncs pull only records whose **SystemModStamp** is greater than the bookmark. Repeats continuously.
- **Sync frequency**: selectable from **30 minutes to 24 hours** in Salesforce settings.
- **Scope**: Crossbeam can only access data the authorizing user can access. Restricted user means restricted data.
- **Auth**: OAuth. No credentials stored, only the OAuth token, encrypted with AWS KMS. Disconnect any time from Crossbeam or Salesforce.
- **Quota safety**: Crossbeam pauses syncing at **80%** of your Salesforce API quota and notifies by email and in-app. Contact support to change the threshold. Reduce sync frequency to lower API calls (HC 3380461, HC 4136739).
- The Salesforce data **push** sync (Crossbeam writing to Salesforce) defaults to twice a day, every 12 hours; actual times vary (HC 4136739).

### 7.4 User lookup fields (HC 7197979)

- You cannot select other User types until you first select the **Account Owner** User type.
- Steps: **Data Sources > Salesforce settings > Edit Data Sync**, expand **User** object, select **Account Owner Name**, **Account Owner Phone**, **Account Owner Email**. Then scroll to the **Account** or **Lead** object to select additional User types or contact details.
- New lookup fields do not appear until the feed syncs again (per your 30 min to 24 hr schedule).

### 7.5 Field behavior (HC 7197979)

- Review or edit fields any time: Data Sources, Salesforce row, **Settings** gear, **Field Sync > Edit**.
- **Removing a field**: on the next sync, master data is rewritten to only the selected fields plus internally required fields (mainly IDs). The deselected field's data is deleted from the master records that fuel Populations. Anything that depended on it (Population filters, reports) loses that data.
- **Import without sharing**: yes. Import every field you need for filtering reports. Unshared fields can still be added to overlap reports and used to filter partner data by your own values.
- **Supported field types**: id, string, picklist, phone, URL, lookups (account to user, lead to user), multi-select picklists, combo boxes, encrypted strings, emails, text areas, numbers, dates and date/times, booleans.
- **Not supported**: Base64, byte, anyType, calculated, Address, json, complexvalue, formula, roll-up, master records.

### 7.6 Manage the connection (HC 3380461)

**Reauthorize** when: user permissions change, users lose Salesforce access, or the original authorizer leaves the org. Requires a **Crossbeam Admin** who also has in Salesforce: API enabled, View Setup and Configuration, View all users, and Read access to Lead, Account, Contact, and Opportunity.
Steps: **Data > Data Sources**, Salesforce row gear icon, **Reauthorize**, enter new username and password, follow Salesforce prompts, **Save**.

**Pause**: Salesforce row gear icon, toggle **Sync Data from Salesforce** off (or on to restart).

**Sync frequency**: gear icon, **Update Frequency** dropdown, select, **Save**.

**Edit Field Sync**: **Edit Data Sync** in Settings opens Customize Fields (see 6.3).

A step-by-step screenshot guide for reauthorizing the Salesforce custom object integration is HC 12013434 (referenced, not in this set).

---

## 8. HubSpot as a data source

### 8.1 Requirements and connect (HC 3160183)

- HubSpot **Super Admin** permissions and **Marketplace Access** are required to complete (and reauthorize) the connection (HC 3160183, HC 3380769).
- Steps: **Data > Data Sources**, click the **HubSpot** tile, click **Connect HubSpot** in the pop-up, confirm the HubSpot account being authorized, click **Connect App**.
- Choose Recommended or Custom; **Sync Now** or **Customize**.

**Mandatory fields**: Companies: Company ID, Company name, Owner ID, Website URL.

**Recommended fields**: Companies: Lifecycle Stage. Contacts: Contact ID, Email, Primary Associated Company ID. Deal Contact Associations: Contact ID, Deal ID, ID, Label. Deals: Deal ID, Deal Stage, Deal Stage ID, Pipeline, Pipeline ID. Owners: Account Owner Email, Owner ID.

Presets: Account Mapping, Pipeline Map, Co-Market, Co-Sell.

### 8.2 Manage (HC 3380769)

- **Reauthorize** when user permissions change or users lose HubSpot access: gear icon, **Reauthorize**, enter credentials, follow HubSpot prompts, **Save**.
- **Pause**: toggle **Sync Data from HubSpot**. Gotcha: **you cannot select or remove fields while the sync is paused.**
- **Update Frequency** dropdown, **Save**.
- **Edit Data Sync** opens Customize Fields.
- Sync problems: the Crossbeam support inbox (support at crossbeam.com).
- Custom object reauthorization guide: HC 12158775 (referenced, not in this set).

---

## 9. Microsoft Dynamics as a data source (HC 6952388)

**Requirements**: a Microsoft Dynamics admin must complete the initial connection. Company admins assign permissions at admin.microsoft.com. The connecting user needs:
- A Microsoft Dynamics 365 license.
- Read access to Leads, Accounts, Contacts, Opportunities.
- Access level Basic or higher.
- API permissions: generate access tokens, generate refresh tokens, API view and configuration permissions enabled.

If these are wrong, the sync fails or behaves unexpectedly.

**Connect**: **Data > Data Sources**, scroll, click **Microsoft Dynamics**, click **Connect Microsoft Dynamics**, sign in to your Dynamics instance. Crossbeam prepares the connection, then prompts to sync. Recommended or Custom, then Sync Now or Customize. Presets: Account Mapping, Pipeline Map, Co-Market, Co-Sell.

**Settings** (gear icon): connection status and errors (reauthorize if user access or permissions changed), **Update Frequency**, **Edit Data Sync**, **Remove Data Source**.

---

## 10. Pipedrive as a data source (HC 10055030)

- Available on all plans. Does **not** include Copilot or pushing custom objects to Pipedrive.
- Must be a **Crossbeam Admin** to connect.
- Steps: **Data > Data Sources**, scroll, **Connect Pipedrive**, in the modal **Connect Pipedrive** opens the auth window, review permissions, **Allow and Install**, wait for redirect to Crossbeam.
- Recommended or Custom; from Review Fields click **Customize** for field selection; presets Account Mapping, Pipeline Map, Co-Market, Co-Sell. Review fields, **Sync Now**.
- Row status shows **Setting up** during processing, then **Active**. Email on completion.
- Settings (three dots at row end): status, Update Frequency, Edit Data Sync, Remove Data Source; then **Save Changes**.
- **Matching gotcha**: Pipedrive does not require a website on organization records. Crossbeam generates a website from the **primary contact email address domain**. It appears as **Crossbeam Generated Website** in field mapping and the Population builder. It is not synced from Pipedrive. If the primary contact uses a personal or wrong domain, matching is affected accordingly.

---

## 11. Snowflake as a data source (HC 4470887)

### 11.1 Model and order of operations

- Uses Snowflake Data Sharing to share CRM data from your Snowflake with Crossbeam's Snowflake account, skipping direct CRM integration.
- **Create and configure your Snowflake Shares first.** The Crossbeam connection will not complete until the Shares exist. Then click the **Snowflake** tile (**Data > Data Sources**, under Add a Data Source).
- Available on all Crossbeam plans.
- Snowflake Classic UI is being retired per account. Steps are the same in Snowsight; screens differ.

### 11.2 Three required inputs

1. **Account region**. Supported: US West (Oregon), the only region not included in Snowflake URLs; US East (Ohio); US East (N. Virginia); EU West (Ireland); EU-Central (Frankfurt). Other regions: contact the Crossbeam support inbox (support at crossbeam.com).
2. **Your Snowflake account locator** (Account Information section of your Snowflake instance).
3. **Data share name** provided by Crossbeam, format `crossbeam_share_{123}` (unique number per org), shown on the Crossbeam data source page when you click the Snowflake tile.

### 11.3 Create the share

- Snowsight: **Data > Private Sharing**, click **Share** (top right), create a **Direct Share**. Secure Share Identifier = the name Crossbeam provides. "Add accounts in your region by name" = Crossbeam's account locator for your region.
- Classic UI: https://<organization>-<name>.snowflakecomputing.com/console#/shares. Returns 404 if Classic is retired; use Snowsight.
- Shared database must contain tables under a schema named `_CROSSBEAM`, **all caps; capitalization counts**. Share name `CROSSBEAM_SHARE_{ID}`.
- Add Crossbeam as a **Consumer** using the locator for your region:

| Region | Crossbeam Account Locator |
|---|---|
| US East 1 | ZAA86167 |
| US East 2 | KP43495 |
| US West 2 | CROSSBEAM |
| EU West 1 | LV64179 |
| EU Central | AV17996 |

### 11.4 Table schemas (required fields marked R)

Not all tables are needed. To support Account Owners you must include the **USERS** table. Extra fields can be added for filtering or sharing.

- **ACCOUNTS**: ID VARCHAR (R), WEBSITE VARCHAR (R), NAME VARCHAR (R), TYPE VARCHAR, OWNER_ID VARCHAR (FK to User), DUNS_NUMBER VARCHAR, CREATED_AT TIMESTAMP_TZ (R), UPDATED_AT TIMESTAMP_TZ (R, equivalent of Salesforce SystemModstamp; last upsert time), IS_DELETED BOOLEAN or VARCHAR.
- **LEADS**: ID (R), EMAIL (R), NAME, PHONE, TITLE, OWNER_ID, CREATED_AT TIMESTAMP_TZ (R), UPDATED_AT (R), IS_DELETED.
- **CONTACTS**: ID (R), EMAIL (R), NAME (R), PHONE, TITLE, ACCOUNT_ID (R, FK to Account), CREATED_AT, UPDATED_AT (R), IS_DELETED.
- **DEALS**: ID (R), AMOUNT DOUBLE, NAME, STAGE_NAME, ACCOUNT_ID (R), CLOSED_AT VARCHAR, CREATED_AT TIMESTAMP_TZ (open date), UPDATED_AT (R), IS_CLOSED BOOLEAN, IS_WON BOOLEAN, OWNER_ID, TYPE, IS_DELETED.
- **USERS**: ID (R), NAME, EMAIL (R), PHONE, CREATED_AT, UPDATED_AT (R), IS_DELETED.

**ID gotcha**: ID is Crossbeam's primary key. It must stay static and unique. Changing it creates duplicate records in Crossbeam.

### 11.5 Deletes

- Optional `IS_DELETED` column on any table. TRUE removes the record from overlaps on the next sync; FALSE or empty syncs normally. BOOLEAN or VARCHAR; for VARCHAR both "true" and "TRUE" count as deleted.
- Rows hard-deleted from Snowflake without IS_DELETED are picked up by the **full sync every 30 days**. Without the column, removed records stay in Crossbeam until cleaned up manually.
- Recommendation: add IS_DELETED to all five tables.

### 11.6 Manage

Data Sources, Snowflake row, Settings icon, **Field Sync > Edit**: pause sync, select fields, remove connection. **Update frequency is not configurable** for Snowflake; contact Crossbeam to change it.

---

## 12. Databricks as a data source (HC 15231542)

### 12.1 Scope

Pulls accounts, contacts, deals, leads, users into Crossbeam to generate overlaps. Separate from **Databricks Integration (Push)**, which sends overlaps back to Databricks (HC 15231550, not in this set). The two are independent and can point to different catalogs and schemas. Available on Free, Connector, Supernode, Enterprise.

### 12.2 Prerequisites

- Databricks workspace with **Unity Catalog** enabled.
- A **SQL Warehouse**; from SQL Warehouse > Connection Details get **Server hostname** (e.g. dbc-12345abc-6789.cloud.databricks.com) and **HTTP path** (e.g. /sql/1.0/warehouses/abc123def456).
- A **Service Principal** with an **OAuth client secret**. Personal access tokens and interactive OAuth are **not supported**.

### 12.3 Create the Service Principal

1. Account console: **Settings > Identity and access > Service principals > Add service principal**.
2. Open it, **Secrets > Generate secret**. Copy **Client ID** (Application ID) and **Client Secret**. The secret is shown **only once**.
3. Grant **Can use** on the SQL Warehouse: **SQL Warehouses > your warehouse > Permissions**, add the Service Principal.
4. The same Service Principal can serve both the Data Source and the Integration.

### 12.4 Catalog, schema, tables

```sql
CREATE CATALOG IF NOT EXISTS crossbeam_share;
CREATE SCHEMA IF NOT EXISTS crossbeam_share.crm;
```

- Only **accounts** is required: `id STRING NOT NULL, name STRING, website STRING, duns_number STRING, owner_id STRING, is_deleted BOOLEAN, updated_at TIMESTAMP NOT NULL`, USING DELTA.
- Optional **contacts**: id, name, email, account_id, is_deleted, updated_at.
- Optional **deals**: id, account_id, amount DECIMAL(18,2), owner_id, is_deleted, updated_at.
- Optional **leads**: id, email, owner_id, is_deleted, updated_at.
- Optional **users**: id STRING NOT NULL, email STRING NOT NULL, name, phone, title, is_deleted, updated_at. Powers AE attribution; add `owner_id STRING` on accounts, deals, and/or leads referencing users.id.
- **Every table must include `id` (STRING) and `updated_at` (TIMESTAMP)** for incremental sync.
- Optional `is_deleted BOOLEAN` on any table enables soft-delete detection; flagged rows are removed from overlaps.
- Extra columns are auto-discovered and surfaced as fields.

### 12.5 Grants

```sql
GRANT USE CATALOG ON CATALOG crossbeam_share TO `crossbeam-sp`;
GRANT USE SCHEMA ON SCHEMA crossbeam_share.crm TO `crossbeam-sp`;
GRANT SELECT ON SCHEMA crossbeam_share.crm TO `crossbeam-sp`;
```
Or per table: `GRANT SELECT ON TABLE crossbeam_share.crm.accounts TO ...`. Replace `crossbeam-sp` with the SP display name or UUID.

### 12.6 Connect

**Data Sources > Databricks tile**. Enter Server hostname, HTTP path, Catalog (crossbeam_share), Schema (crm), Client ID, Client Secret. Click **Connect**. Crossbeam authenticates, verifies the **accounts** table exists, discovers tables and columns (via INFORMATION_SCHEMA.TABLES and INFORMATION_SCHEMA.COLUMNS), validates required field types. Initial sync starts automatically; later syncs are incremental on `updated_at`.

### 12.7 Capabilities and limits

- Auth: OAuth M2M only.
- Incremental sync bookmarked on updated_at. **Full re-sync** available; resets the bookmark.
- Preview sync: last **10,000** records ordered by updated_at DESC.
- **Per-org record limit** exists; contact support if exceeded (number not stated).
- Type mapping: STRING/VARCHAR/CHAR to Text; INT, BIGINT, SMALLINT, TINYINT, FLOAT, DOUBLE, DECIMAL, NUMERIC, REAL to Number; DATE, TIMESTAMP, TIMESTAMP_NTZ, TIMESTAMP_LTZ to Timestamp (with time zone); BOOLEAN to Boolean. ARRAY, MAP, STRUCT, INTERVAL, BINARY are **skipped**; flatten into columns or views.
- `deals.amount` is treated as money.
- Connection cannot be enabled without the accounts table.

### 12.8 Manage

Data Sources, Settings icon next to Databricks: **General** (sync timing, status, connection details), **Field Sync**, **Field Presets** (fields shared with partners, see HC 11583486), **Field Mapping** (map Databricks as data source, opportunity fields, product line type field, see HC 13613493), **Remove data source**. Click **Save**.

---

## 13. Google Sheets as a data source (HC 5613345)

### 13.1 Sheet requirements

- **XLSX files stored in Google Drive are not supported.** A green **.XLSX** label next to the file name means it will not work; convert to Google Sheets format.
- Unique sheet name. Unique column headers (e.g. do not use "Website" for two columns).
- Required columns: **Company Name**, **Company URL**.
- Account owner mapping: **Account Owner Email** (required for owner mapping), Account Owner Name (optional), Account Owner Phone (optional).
- Rows with identical Company Name and Company Website are flagged as duplicates and **skipped**.
- **Once required columns are mapped, do not change them or the sync returns an error.**

### 13.2 Authentication

- **Only one user per org** can authenticate, and must use a **Google Workspace** email (not personal Gmail). Ideally the team admin.
- That user must have access to **every** sheet the team wants to connect. Each sheet must be shared with the authenticating person.
- Steps: **Data > Data Sources**, Google Sheets tile, **Authenticate with Google**, choose an organizational account.
- Crossbeam only requests Google Drive access to sync and read Sheets; no other Workspace services.

**If authentication fails**, IT (Super Admin) at admin.google.com: **Security > API Controls > Manage Third-Party App Access > Configure New App > OAuth App Name or Client ID**, search "Crossbeam", hover and **Select**, check **all** listed OAuth Client IDs, Access Level **Trusted: Can access all Google services**, **Configure**.

### 13.3 Add and map

1. **Data Sources**, click **Add** next to the Google Sheets connection.
2. Paste the Google Sheet URL, select the tab.
3. Data Type: **Companies** (map Company Name and Company Website) or **People** (map Email).
4. **Add Google Sheet**.

Optional owner mapping: in the Data Sources list, the sheet's gear icon, **Map Account Owner**, map Account Owner Email (required), Name, Phone, **Apply**.

### 13.4 Manage

Google Sheets row: **Add** (another sheet), **Sync Now** (manual refresh), gear icon (adjust sync frequency, reauthorize, remove data source, view connection details). Expand the arrow next to the source name to see each sheet and status; per-sheet gear: Check Connection, Add Field Mapping (Map Account Owner), Adjust Sharing Presets, Remove data source. **Save**.

### 13.5 Behavior

- Each tab is its own data source; data is **not merged across tabs**. The same account (e.g. Partnerbase.com) on multiple tabs is recognized as one account and does **not** count as an additional Record Export.
- Non-mapped columns come in as "Account information", viewable and shareable in reports.
- Common pattern: export from an unsupported CRM (or one you lack permission to connect) into Sheets; automate ongoing sync with Zapier or Workato.

---

## 14. CSV uploads

### 14.1 Limits and format (HC 3160473)

- CSV format only, **15 MB** size limit. Larger files: use Google Sheets.
- Template: s3.amazonaws.com/assets.getcrossbeam.com/template.csv; add columns as needed.
- Static: upload a new file each time data changes. Columns can be remapped any time.
- **The CSV name is shared with partners** when you share data.

### 14.2 Upload steps (HC 3160473)

1. **Data > Data Sources**. Click **Add** at the end of the CSV Upload row, or the **CSV Upload** tile under Add a Data Source.
2. **Browse** or drag and drop. Enter **CSV Name**. Choose data type **Companies** or **People**. **Next**.
3. Map fields, then **Upload**.

**Companies fields**: Company Name (Required), Website (Required), Account Owner Name (Recommended), Account Owner Email (Recommended), DUNS Number, Industry, Number of Employees, Account Owner Phone, Country, Postal Code, Region, City, Address, Company Phone Number (all Optional).

**People fields**: Email (Required), Account Owner Name (Recommended), Account Owner Email (Recommended), Lead Name, Lead Phone, Lead Title, Company Name, Company Website, Country, Postal Code, Region, City, Address, Account Owner Phone (Optional).

### 14.3 Map additional columns on an existing CSV (HC 3160473)

Data Sources, dropdown arrow next to the CSV dataset, file's gear icon, **Add Data**, select columns per field, **Upload**, then **Save**. Crossbeam reprocesses the dataset; it shows a processing status until complete.

CSV row gear icon options: Check Connection, Add Data, Map New Columns, Adjust Sharing Presets, Remove Data Source (HC 3160473).

### 14.4 Add data to an existing CSV (HC 3160196)

- New file must use the **same column structure, headers, format, and column order**.
- Include **only new records**. Re-uploading the full original file can create duplicates.
- Steps: Data Sources; either **Add** on the CSV row (new file) or expand the small arrow next to the source name, file's **Settings gear**, then follow upload steps; data is added to the selected file.
- New records are **automatically included** in any Populations that use that CSV.
- **You cannot delete or modify individual rows** in a CSV upload. For churned accounts, apply Population filters to exclude them. For easier updates use Google Sheets or a CRM.

### 14.5 Remove a CSV (HC 5018090)

**Deleting a CSV removes every Population powered by that file**, which can affect related Lists and Overlaps.
Steps: **Data > Data Sources**, expand the **CSV Upload** row, gear icon next to the file, **Delete**, type `DELETE` to confirm.

### 14.6 Population from a CSV (HC 3160192)

Prerequisite: a successfully uploaded CSV.
1. **Data > Populations**, **Create Population**.
2. Population name, optional description, choose **CSV Upload** in the Data Source menu. Under File, the name is pre-filled or pick a different file. **Continue**.
3. **Add Table Filters** from the dropdown. Preview or **Save Population**.
4. Set sharing defaults when prompted.

### 14.7 DUNS on files (HC 10492031)

- Mapping DUNS retroactively for CSVs and Google Sheets has limitations; contact support if issues.
- Only **one** DUNS column name can be retroactively selected across existing file uploads. If existing files use different DUNS column names, only one can be mapped retroactively. Newly added data can use a different DUNS column name at upload time.

---

## 15. Populations

### 15.1 Concepts and best practice (HC 3160813)

- Two purposes: **Standardization** (compare Salesforce, HubSpot, CSV data apples-to-apples; speeds matching) and **Data cleansing** (share meaningful segments, not every account or lead).
- **Not intended for detailed analysis.** Best practice: a few large, broadly defined Populations; refine with **Lists** (app.crossbeam.com/lists).

### 15.2 Standard Populations (HC 3160197)

- Three standard Populations: **Customer**, **Open Opportunities**, **Prospects**. Each has a **Create** button on **Data > Populations**.
- Population Builder: select data source, select object, optional description, **Continue**, define with filters, preview, create.
- **Pre-applied filters**: Crossbeam recommends filters based on your connected CRM and synced fields (e.g. Salesforce Customer: `Stage = Closed Won` or `Account Type = Customer`). Tooltip explains each suggestion. Edit, remove, or add any time; click **Apply Filters**.
- Set sharing defaults when prompted after creation (HC 4236619 for details, not in set).

### 15.3 Custom Populations (HC 7239725)

- **Connector and Supernode plans only.** Upgrade on the Billing page.
- **Data > Populations > Create Population**. Name; **Population Type** (Customer, Open Opportunities, Prospects, Other); Data Source; Object; optional description. **Continue**.
- Filters: field, comparison operator, value; multiple filters; AND/OR between filter groups. **Apply filter** to preview. **Create Population**.
- Filter options vary by data source and field type.

### 15.4 Population Types (HC 12399814, HC 7239725)

- Types: **Customers**, **Open Opportunities**, **Prospects**, **Other** (e.g. "Partners", "Closed Lost").
- Why it matters: typed custom Populations feed the Account Mapping Matrix, Reports, Deal Navigator, Performance Dashboard, dashboards, and CRM sync. From November 6, Populations are grouped by standard type.
- Existing custom Populations were auto-typed by keyword (e.g. "Customers - NA" became Customers). Names containing "Customer", "Prospect", or "Opp" trigger an auto-suggested type. Review assignments.
- Who: **Admins** or users who can create/edit Populations can set the type; all users can view it.
- Type does **not** change data sharing rules or Record Exports.
- HC 12399814 says you **cannot skip** assigning a type (choose Other). HC 7239725 calls types "optional" and says leave uncategorized by selecting Other. Net: a value is always set; Other is the neutral choice.
- Change type: **Data > Populations**, the custom Population's edit icon, under **Details** change the type dropdown, **Apply filters**, **Save Changes**.

### 15.5 Filters (HC 3160198)

- **Data > Populations**, open existing or **Create Population**, go to **Filters**.
- Find a field by typing or scrolling. Missing field: **Add Filters from another object** opens **Customize Fields**: apply data presets, expand objects, search, check fields, **Review Fields > Sync Now**. This changes what your data source syncs.
- Operators by type: text (is, is not, contains, does not contain); numeric (equals, greater than, less than, between); date (is on, is before, is after).
- Lists of values: use is / is not, then and/or to add values (territory, product line, tags).
- **+ Add Filter from another object** adds criteria. AND means all must be true; OR means any. Use AND inside a group, OR between groups.
- Example: Industry is Tech AND Opportunity Size greater than $500K, OR Region is APAC.
- Pencil icon edits a filter; trash icon deletes one filter without affecting others. For custom Populations, **Delete Group** removes a filter group (HC 7239725).

### 15.6 Edit and manage (HC 3161135, HC 3160197, HC 3160192)

**Data > Populations**. Per Population: **Edit** or pencil to open the Builder and adjust filters; **three dots** for sharing default, duplicate, delete, export; pencil next to **Sharing Settings** to adjust.

### 15.7 Delete (HC 3160199)

Deleting a Population permanently removes it, **stops sharing its data with partners**, and **removes its data from any reports** using it. Irreversible.
Steps: **Data > Populations**, row's three dots, **Delete Population**, confirm in the pop-up.

### 15.8 Product-based Populations with Product2 (HC 14827573)

- **Salesforce only.** Prerequisites: **Product2** and **Opportunity Line Item** synced, and **Product Line Type** field mapped (setup in HC 13613493, not in set).
- Plan: Product2 in Standard Populations on all plans; in Custom Populations on Connector, Supernode, Enterprise.
- Populations are account-based; the Product2 filter finds accounts tied to a product via closed-won opportunities. Ideal for Customer Populations.

Steps:
1. **Data > Populations > Create Population**.
2. Name (e.g. "Advanced Security Module - Customers"); Population Type **Customers** (so it appears in Account Mapping Matrix, Deal Navigator, Performance Dashboard); Data Source **Salesforce**; Object **Accounts**; **Continue**.
3. **Add Filter**, Product2 group, **Product Name** or **Product ID**, operator **is**, value.
4. **Add Filter**, search **Closed** (under Opportunity), value **true**.
5. **Add Filter**, search **Won** (under Opportunity), value **true**. Logic should read "where Closed is true and where Won is true". **Apply Filters**.
6. Review preview, **Create Population**.

---

## 16. Matching engine

### 16.1 Principles (HC 3160297, HC 10492031, HC 12871671)

- Confidence-driven. Matches can trigger data sharing, so very high confidence is required. **False positives are treated as far worse than false negatives.**
- Multiple properties produce a confidence score, extra weight on unique attributes.
- **Customers cannot modify the matching algorithm.**
- Only domain, email, DUNS, phone, brand/marketplace (plus names as a weak signal) are used; no other dimensions currently (HC 3160297 FAQ).
- Minor shifts in match rates are normal as methodology improves (HC 3160297).
- Sync with the **Co-Selling Preset** for most accurate matching (HC 3160297).

### 16.2 Domain rules (HC 3160297, HC 14693133)

- Anything after the TLD is stripped: google.com matches google.com/en.
- Capitalization and slashes ignored: GoOgle.com matches google.com.
- https://, www., trailing slashes normalized: acme.com, www.acme.com, https://acme.com all match.
- **Subdomains are not stripped**: flights.google.com does not match google.com; shop.acme.com does not match acme.com.
- **Different TLDs are separate accounts**: google.com vs google.net; acme.com vs acme.net do not match.
- Crossbeam tracks some multi-domain ownership for indirect matches (example: delta.com and deltaairlines.com should match, HC 12871671).

### 16.3 Email

High-confidence person matches, cleansed like domains. Matching people helps resolve company matches, and under quality conditions contact email domains can be used as a company matching property (HC 3160297).

### 16.4 DUNS (HC 10492031, HC 3160297)

- DUNS present and equal: match. DUNS present and different: **not** a match. No DUNS: standard algorithm including URL.
- DUNS takes precedence over other criteria when available.
- DUNS field must be **manually mapped per data source**. Mappable on any source.
- Dashes are stripped (123456789 matches 12-345-6789).
- CRM DUNS fields must be **text**. Number-type fields can drop a leading 0 and break matching.
- **DUNS+4 not supported.**
- Gotcha: a wrong DUNS value actively blocks an otherwise good domain match, because mismatched DUNS means no match.

### 16.5 Phone and brand (HC 3160297)

- Phone: matches accounts sharing the same valid phone even when domains differ. Normalized, validated, deduplicated to international standards; invalid or test data removed. A phone number appearing across too many records is discounted (HC 12871671).
- Brand/Marketplace: matches accounts sharing a brand name across different domains (franchises, marketplace listings, multi-brand orgs); brand parsed from social profiles or marketplace URLs.

### 16.6 Names (HC 3160297, HC 14693133)

- Names alone are low-confidence; combined with other dimensions (HC 3160297).
- When no website domain is available, Crossbeam falls back to company name. Names are normalized by removing punctuation, common suffixes (Inc., LLC), and accents. Abbreviations, trade names, alternate spellings can still block a match (HC 14693133).

### 16.7 Pipeline stages (HC 12871671)

Data cleaning (normalize name, domain, phone, email to root format), quality filtering (drop junk, test domains, placeholders), network-informed enrichment (anonymized, aggregated associations across 30,000+ companies fill gaps when a strong identifier exists), then strict matching. Crossbeam does not train a custom LLM for matching or use customer data as training data.

### 16.8 Report incorrect matches (HC 5246994)

- On an Account page, click **Report an Incorrect Match** (button on the right), provide details, **Send Report**.
- Reports (yours or your partner's) show as an indication in the partner section of the Account page; this is the **only** place to view them.
- Crossbeam **does not respond** to reports; they train the engine, not support tickets. For immediate resolution contact your customer support manager or the Crossbeam support inbox (support at crossbeam.com).
- Dirty data in either CRM is the usual cause of wrong matches.

---

## 17. Troubleshooting

### 17.1 Salesforce connection errors (HC 4136739 unless noted)

General: reauthorizing the connection is often the fix. Some fixes require the Salesforce admin.

| Error (verbatim) | Cause | Fix |
|---|---|---|
| `Salesforce has reported 189737/218000 (87%) total REST API quota used across all Salesforce Applications. Terminating data sync to not go past configured percentage of 80% total quota.` (Over API Quota Limit) | Org used 80%+ of daily Bulk API quota (usually driven by other services). Crossbeam pauses as a safety measure. | First occurrence: often nothing; retries next day after reset. Repeated: ask sales ops; admin checks **Setup > Jobs > Bulk Data Load Jobs** to see which integrations consume quota. Reduce Crossbeam sync frequency; support can change the 80% threshold (HC 3380461). |
| `API_CURRENTLY_DISABLED: API is disabled for this User` | Authenticating user lacks API access. | Reauthorize with a user that has API access, or have admin grant API access to the existing user. |
| `API_DISABLED_FOR_ORG: The REST API is not enabled for this Organization.` | Salesforce org has no API access. | Salesforce admin enables API access for the org (edition must include API, HC 7197979). |
| `API_DISABLED_FOR_ORG: limits resource is not enabled` | API not properly configured; most likely the authenticating user lacks **View Setup and Configuration**. | Admin ensures API enabled and View Setup and Configuration system permission on the authenticating user's profile. |
| `invalid_grant: expired access/refresh token` | Crossbeam no longer has access to the instance. | Reauthorize. |
| `invalid_grant: inactive user` | Original connecting user deactivated or removed. | Reauthorize with a new user, or admin verifies the current user's access. |
| `REQUEST_LIMIT_EXCEEDED: TotalRequests Limit exceeded.` | Org used all daily Bulk API quota. | Check **Setup > Environments > System Overview**; raise quota or find the heavy consumers. Crossbeam retries next day. |
| `UnknownHostException: invalid instance url` | Salesforce outage or interruption. | Check Salesforce Trust Status page. Data remains usable in Crossbeam. Clears automatically once Salesforce recovers; no reauth needed. |
| `NOT_FOUND: The requested resource does not exist` | Authorized instance no longer exists, or authorizer lost permission (left company, API revoked). | Another user with API permission reauthorizes in Salesforce Settings in Crossbeam. |
| `OAUTH_APP_BLOCKED: salesforce admin needs to unblock crossbeam oauth app` | Crossbeam OAuth app blocked in the Salesforce environment. | Admin: **Setup > Apps > Connected Apps > Connect Apps Oauth Usage**, Crossbeam row, **Unblock**. |
| Salesforce authorization error when connecting (HC 7197979) | Salesforce's September 2025 security update blocking "uninstalled" connected apps. | See HC 12510571 (Troubleshooting Salesforce Authorization with Crossbeam, not in set). |

### 17.2 Salesforce field and sync symptoms (HC 7197979, HC 3380461)

| Symptom | Cause | Fix |
|---|---|---|
| Field shows **"Not Supported"** | Usually the original authorizing user lost access to that field; or the field type is unsupported (Base64, byte, anyType, calculated, Address, json, complexvalue, formula, roll-up, master records). | Give that user the permission, or have a properly permissioned user reauthorize. |
| Field missing from the picker | Field deleted in CRM, or field-level security not "read" for the syncing user's profile. | CRM admin restores field or sets FLS to read; then select it in Crossbeam CRM settings. |
| Cannot select other User types | Account Owner User type not selected first. | Select Account Owner Name, Phone, Email on User object first. |
| New lookup fields not visible | Feed has not re-synced. | Wait for next sync (30 min to 24 hr schedule). |
| Only some accounts synced | Authorizing user can only see a subset of records. | Reauthorize with a user who has broader access. |
| Data disappeared from Populations or filters after field change | Field was deselected; next sync rewrote master data without it. | Reselect field and resync. |
| Status **Not Syncing** | Sync paused via toggle. | Turn on **Sync Data from Salesforce**. |
| Status **Error** | Connection error. | Read error details in Settings; see 17.1. |

### 17.3 HubSpot symptoms (HC 3160183, HC 3380769)

| Symptom | Cause | Fix |
|---|---|---|
| Cannot complete connect or reauthorize | Missing HubSpot Super Admin or Marketplace Access. | Use a user with both. |
| Cannot select or remove fields | Sync is paused. | Re-enable **Sync Data from HubSpot**, then edit fields. |
| Status Error or sync problems | Permission change or loss of access. | Reauthorize; contact the Crossbeam support inbox (support at crossbeam.com). |

### 17.4 Microsoft Dynamics, Pipedrive (HC 6952388, HC 10055030)

- Dynamics sync fails or behaves unexpectedly: connecting user lacks Dynamics 365 license, read on Leads/Accounts/Contacts/Opportunities, Basic+ access, or token/API permissions. Fix at admin.microsoft.com, then reauthorize if status shows it is needed.
- Pipedrive accounts not matching: no website on organization record, so Crossbeam derives **Crossbeam Generated Website** from the primary contact's email domain. Fix the primary contact email or record data.
- Pipedrive stuck at **Setting up**: initial sync still processing; wait for **Active** and email.

### 17.5 Snowflake (HC 4470887)

| Symptom | Cause | Fix |
|---|---|---|
| Crossbeam connection does not complete | Shares not created/configured before clicking the tile. | Create the Direct Share, add Crossbeam consumer locator, then connect. |
| Tables not found | Schema not named `_CROSSBEAM` in all caps; wrong share name; wrong locator/region. | Use exact casing and the `CROSSBEAM_SHARE_{ID}` name; use correct regional locator. |
| Classic shares URL returns 404 | Classic UI retired on your account. | Use Snowsight Data > Private Sharing. |
| Region not supported | Outside the five supported regions. | Contact the Crossbeam support inbox (support at crossbeam.com). |
| Duplicate records | ID field changed for existing records. | Keep ID static and unique. |
| Deleted rows still in overlaps | No IS_DELETED column; hard deletes only picked up at 30-day full sync. | Add IS_DELETED (all five tables) or clean up manually. |
| No account owners | USERS table not included. | Add USERS table and OWNER_ID FKs. |
| Want faster/slower sync | Frequency not configurable in UI. | Contact Crossbeam. |

### 17.6 Databricks (HC 15231542)

| Symptom | Cause | Fix |
|---|---|---|
| Connection cannot be enabled | `accounts` table missing. | Create accounts table. |
| Auth fails | Using PAT or interactive OAuth; missing Can use on warehouse; missing grants. | Service Principal OAuth M2M; grant Can use; USE CATALOG, USE SCHEMA, SELECT. |
| Lost client secret | Shown only once. | Generate a new secret. |
| Incremental sync not working | Table lacks `id` STRING or `updated_at` TIMESTAMP. | Add both columns. |
| Column missing in Crossbeam | ARRAY, MAP, STRUCT, INTERVAL, BINARY are skipped. | Flatten into columns or views. |
| Record limit exceeded | Per-org limit. | Contact support. |

### 17.7 Google Sheets (HC 5613345)

| Symptom | Cause | Fix |
|---|---|---|
| Sheet will not connect; green .XLSX label | Excel file in Drive. | Convert to Google Sheets. |
| Sync returns an error | Mapped required columns were changed after mapping. | Restore headers or remap. |
| Rows missing | Duplicate Company Name plus Website rows skipped. | Deduplicate. |
| Sheet not visible/accessible | Not shared with the single authenticating user, or non-unique sheet name. | Share with that user; rename uniquely. |
| Cannot authenticate | Personal Gmail used, or Workspace blocks third-party app. | Use Workspace account; IT sets Crossbeam OAuth clients to Trusted in admin.google.com. |
| Second user cannot authenticate | Only one user per org can authenticate. | Use the existing authenticator or reauthorize. |

### 17.8 CSV (HC 3160473, HC 3160196, HC 5018090, HC 10492031)

| Symptom | Cause | Fix |
|---|---|---|
| Upload rejected | Over 15 MB or not CSV. | Split or use Google Sheets. |
| Duplicate records | Full file re-uploaded instead of new rows only. | Upload only new rows with identical structure. |
| Churned account still overlapping | Rows cannot be deleted or edited. | Exclude via Population filters. |
| Populations, Lists, overlaps vanished | A CSV was deleted; Populations built on it are removed. | Re-upload and rebuild Populations. |
| DUNS not mapping on older files | Retroactive DUNS mapping limits; only one DUNS column name retroactively. | Contact support; use new column name on new uploads. |

### 17.9 Missing overlaps (HC 14693133)

Common causes: domains differ; one or both records lack a domain; record not in a shared Population on **both** sides. Crossbeam cannot view or disclose a partner's Population configuration; coordinate with the partner.

Steps:
1. **Search** the account (side nav search bar) and open the record page. Confirm it belongs to a Population (**No Populations** means no overlap), and note imported Website and Company Name. Ask partner to do the same.
2. **Confirm shared Population**: **Data > Populations**, open the Population, review filters, confirm the account qualifies, **Close**. Three-dot menu, **Partner-specific Sharing**, search partner, confirm shared. Update filters if needed and wait for sync.
3. **Compare domains** with the partner. If different, fix in CRM and wait for the next sync. Subdomains and different TLDs never match.
4. **Compare company names** when neither side has a domain; fix significant differences in CRM.
5. **Contact support** only if the record is in shared Populations on both sides and domains match (or names align), with: account name, website domain, partner org name, screenshots of the record in your shared Population.

Additional causes from other articles: mismatched DUNS values block matches (HC 10492031); DUNS stored as number type loses leading zeros (HC 10492031); Pipedrive generated website from a personal email domain (HC 10055030); field containing Website deselected from sync (HC 7197979).

### 17.10 Incorrect overlaps (false positives) (HC 5246994)

Use **Report an Incorrect Match**; no reply will come. For urgent cases, email the Crossbeam support inbox (support at crossbeam.com). Check your own and partner CRM data quality, and check DUNS values since equal DUNS forces a match (HC 10492031).

### 17.11 Other onboarding symptoms

| Symptom | Cause | Fix | Source |
|---|---|---|---|
| Clicking **Request Free Trial** shows a finish-onboarding message | Onboarding incomplete. | Finish all onboarding steps. | HC 10644667 |
| Cannot connect integrations during trial | Trial restriction. | Upgrade. | HC 10644667 |
| Exports capped at 100 records per report | Trial limit. | Upgrade. | HC 10644667 |
| Prompted to request to join at sign-up | Company already has a Crossbeam account. | **Request to Join**, wait for approval email. | HC 9713136 |
| Cannot create Custom Population | Plan is not Connector or Supernode. | Upgrade on Billing page. | HC 7239725 |
| Product2 filter unavailable | Not Salesforce, or Product2 / Opportunity Line Item not synced, or Product Line Type not mapped; or Free plan in custom Population. | Complete setup (HC 13613493); check plan. | HC 14827573 |
| Custom Population missing from Matrix, Deal Navigator, Performance Dashboard | Wrong or Other Population Type. | Assign the correct type. | HC 12399814 |

---

## 18. What breaks what (dependency map)

- Delete CSV: its Populations, Lists, Overlaps go (HC 5018090).
- Delete Population: partner sharing and report data go; irreversible (HC 3160199).
- Deselect synced field: purged from master records next sync (HC 7197979).
- Authorizer leaves or loses access: `invalid_grant: inactive user`, `NOT_FOUND`, or "Not Supported" fields (HC 4136739, HC 7197979).
- Authorizer sees a subset: only that subset syncs (HC 7197979).
- Salesforce quota at 80%: sync paused until next day (HC 3380461).
- HubSpot sync paused: field selection locked (HC 3380769).
- Mapped Google Sheet columns changed: sync error (HC 5613345).
- Snowflake ID changed: duplicates; no IS_DELETED: deletes lag up to 30 days (HC 4470887).
- Mismatched or number-typed DUNS: blocks matches (HC 10492031).
- Population unshared or filters exclude the account: no overlap (HC 14693133).
- Population Type: changes feature placement, not sharing or Record Exports (HC 12399814).
- CRM sync filtering: not retroactive (HC 5391508). CSV names: visible to partners (HC 3160473).

---

## 19. Numbers cheat sheet

| Item | Value | Source |
|---|---|---|
| CSV file size limit | 15 MB | HC 3160473 |
| Salesforce Bulk API batch | 10,000 records (default) | HC 7197979 |
| Salesforce sync frequency range | 30 minutes to 24 hours | HC 7197979 |
| Salesforce quota pause threshold | 80% | HC 3380461, HC 4136739 |
| Salesforce push sync default | Twice a day, every 12 hours | HC 4136739 |
| CRM/warehouse refresh | Several times a day | HC 5391508 |
| Snowflake full sync (catches hard deletes) | Every 30 days | HC 4470887 |
| Databricks preview sync | Last 10,000 records by updated_at DESC | HC 15231542 |
| Google Sheets authenticators per org | 1 | HC 5613345 |
| Connector trial | 30 days, 3 users max, 100 records per report export, no integrations | HC 10644667 |

---

## 20. Conflicts and ambiguities across articles

- **Salesforce permissions for connect vs reauth**: HC 3160182 lists only API Enabled and Account (or Lead) Read as required. HC 3380461 says the reauthorizing Crossbeam Admin needs API enabled, View Setup and Configuration, View all users, and Read on Lead, Account, Contact, and Opportunity. HC 4136739 says lacking View Setup and Configuration causes `API_DISABLED_FOR_ORG: limits resource is not enabled`. Safe practice per these articles: grant the full HC 3380461 set.
- **Salesforce quota wording**: HC 4136739 describes the 80% pause as Bulk API quota, while the sample error text says "total REST API quota". HC 7197979 says Crossbeam uses Bulk API 2.0, not REST.
- **Population Type optional vs required**: HC 7239725 says optional (choose Other); HC 12399814 says it cannot be skipped (choose Other).
- **Name-based matching**: HC 14693133 says Crossbeam falls back to company name when no domain; HC 3160297 says names alone are low-confidence and combined with other dimensions.
- **Custom Populations and Enterprise**: HC 7239725 names only Connector and Supernode; HC 14827573 shows Enterprise supports Product2 in Custom Populations.
- **Legacy navigation** (HC 3160087) is superseded by HC 11021727 but still describes Partner detail contents and URLs.
- **Google Sheets required column naming**: requirements list "Company URL", mapping step says "Company Website" (HC 5613345).
