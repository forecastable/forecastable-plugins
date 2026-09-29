<!-- Library file for crossbeam-admin-reference.md. Source: Crossbeam Help Center, extracted September 25th, 2026. Cite (HC number); confirm in-app when a screen may have moved. -->

# Crossbeam Admin Reference: Integrations and API (Group D)

Distilled from 36 Crossbeam Help Center articles (Integrations and API collection); citations as (HC nnnnnnn). This source set has no dedicated Gong, Chrome, Zapier, or Outreach articles.

---

## 0. Cross-cutting concepts

### 0.1 Integration categories

- Data sources (sync data into Crossbeam): Salesforce, HubSpot, Microsoft Dynamics 365, Snowflake, Databricks, Pipedrive, Google Sheets, CSV upload. (HC 5251445)
- External data connections (push insights out): Crossbeam MCP Server (connects AI tools like Claude, ChatGPT, and Glean via Model Context Protocol), Crossbeam Copilot (inside Salesforce, HubSpot, Gong, Outreach, and Chrome), custom object integrations (store account mapping results in CRM custom objects, kept up to date automatically), Ecosystem Signals (webhook or REST API), Crossbeam for Slack (overlap alerts via DM or Slack Connect, `/crossbeam` lookups). (HC 5251445)
- All integrations are listed on the Integrations page at app.crossbeam.com/integrations; full details for each live on the Crossbeam Marketplace (marketplace.crossbeam.com). (HC 5251445)
- Navigation used across articles: left nav **Data** icon, then **Integrations**. Installed integrations appear under **Installed Integrations**; new ones under **Available Integrations**. (HC 10080455, HC 8533576)

### 0.2 Plan tier matrix (as stated per article)

| Integration or feature | Free | Connector | Supernode | Enterprise |
|---|---|---|---|---|
| Salesforce Custom Object (Crossbeam Ecosystem Overlap data) | no | object installed, no data pushed | yes | yes (per HC 14463181) |
| Salesforce Copilot managed package install | not stated | yes (HC 11407240) | yes | not stated |
| Ready-to-Use Salesforce Reports | no | no | yes | not stated |
| Enhanced Ecosystem Reporting fields (SF and HubSpot) | no | no | yes | not stated |
| Partner Field Mapping | no | no | yes | yes |
| Partner Account mapping in Crossbeam | yes | yes | yes | yes |
| Partner Account lookup field and Partner Tags sync | no | no | yes | yes |
| HubSpot Custom Object | no | no | yes | not stated |
| HubSpot reporting and 360 Dashboard | no | no | yes | not stated |
| Microsoft Dynamics Custom Object | no | no | yes | not stated |
| Snowflake push | "may not be included in your plan" (contact CSM) | | | |
| Databricks push | no | no | yes | yes |
| REST API | no | no | yes | yes |
| Signals via API | no | no | yes | yes |
| Signals via Webhook | no | no | no | yes |
| Clay | no | no | yes (plus Clay Pro) | not stated |
| PartnerStack | no | yes | yes | not stated |
| Adobe Marketo Engage | no | no | yes | not stated |
| Universal Integration Settings | no | yes | yes | not stated |
| Slack `/crossbeam` command | yes | yes | yes | not stated |
| Slack List Notifications | no | yes | yes | not stated |
| Partner owner fields via Salesforce (for Slack context) | no | no | yes | not stated |
| AI Agents (public beta) | no | yes | yes | yes |
| Product2: Sync, Share, Standard Populations | yes | yes | yes | yes |
| Product2: Custom Populations | no | yes | yes | yes |
| Product2: Filter Lists and Dashboard | no | no | yes | yes |
| Integration Seat | no | no | yes | yes |

Sources: each row's own article, cited in its section below.

### 0.3 Record Exports (applies to every push integration)

- The initial Record Export when setting up an integration counts toward the account's Record Export limit. Monitor usage at app.crossbeam.com/billing (Plan & Billing). Once you hit the Export Limit, Crossbeam insights stop flowing into external tools. (HC 4694521, HC 7971155, HC 14463181)
- Salesforce custom object push: the initial push counts as your first export, and records continue to count against the limit on each subsequent sync. (HC 9280237)
- REST API calls count toward Record Exports. (HC 4677142)
- Signals API calls and webhooks count toward Record Exports. (HC 12732223)
- Mapped Partner Account records count toward Record Exports, but the initial auto-matched mappings set up by Crossbeam do not. (HC 14463181)
- Universal Integration Settings show **View Estimated Record Exports**, an estimate of records exported through each integration. (HC 10080455)
- Volume reducers: turning off **Push opportunity data** in Salesforce reduces the volume pushed; deselecting populations reduces scope. (HC 9280237)

### 0.4 Universal Integration Settings

- Available only on Connector and Supernode plans. Location: left menu **Data** icon, **Integrations**, open **Settings** on the integration row. (HC 10080455)
- Applies to: all Copilots, Snowflake Custom Object, HubSpot Custom Object, Salesforce Custom Object, Gong Integration, MS Dynamics Custom Object. (HC 10080455)
- Controls:
  - **Adjust Data Pushes**: toggle on or off to enable or disable data pushes for new partners or data populations.
  - **View Estimated Record Exports**: estimate of records exported per integration.
  - **Customize Data in Push**: expand **My Population** to select or deselect your populations; expand **Partner Populations** to see partner populations.
  - **Partner-Specific Settings**: apply settings to all partners collectively or customize per partner.
  - **Re-authorization**: click **Re-authorize** and follow prompts after authorization changes or errors.
  - Click **Save**. (HC 10080455)
- Partner-specific settings in the integration also apply to the Salesforce "is a customer of" and "is an open opportunity for" Account push. (HC 10742955)

### 0.5 SSO Exception User (OAuth integrations)

- Required for any OAuth integration, including the Salesforce Copilot and Crossbeam for Sales, when SSO is enforced. (HC 8337148)
- Steps:
  1. **Organizational Settings** (app.crossbeam.com/organization/settings), scroll to **Login Options**. Temporarily enable **Don't Require SSO**, click **Save Settings**.
  2. Invite the user who will authenticate the integration with an Admin role.
  3. The user registers from the invite email with Username plus Password or Google Sign In. On the Team page, their Login Method column should show "Standard" or "Google" instead of "SSO".
  4. Return to Organizational Settings, select **Require SSO**, click into the **SSO Login Exception** box and select the Standard or Google user. Click **Save Settings**.
  5. In Salesforce Crossbeam Setup step 1, click **Validate** and log in with the SSO Exception User credentials. (HC 8337148)
- Always authenticate with the same login method shown on the Team page. (HC 8337148)

### 0.6 Integration Seat

- Integration Seat users can complete Salesforce setup without needing a Crossbeam user seat. Available on Supernode and Enterprise plans. (HC 9280237)
- Crossbeam recommends a dedicated Integration Seat for the Salesforce and HubSpot custom object connections. (HC 12013434, HC 12158775)

### 0.7 Setup time estimates (RevOps notes)

- Snowflake: 1 hour. (HC 4694521)
- Slack: 30 minutes. (HC 3639783)
- HubSpot Custom Object: 3 hours, can vary significantly. (HC 7971155)
- Salesforce v2: 1 hour basic to 3 hours advanced. (HC 9280237)
- Salesforce v1 to v2 upgrade: set aside at least 30 minutes; allow at least an hour after setup before data syncs. (HC 10578034)

---

## 1. Salesforce managed package (v2): Crossbeam Copilot and Crossbeam Ecosystem Overlap

### 1.1 What it does

- One managed package installs two things: a Lightning Web Component called **Crossbeam Copilot** (placed on Lightning pages) and a custom object called **Crossbeam Ecosystem Overlap** that receives Crossbeam data for Salesforce reports and dashboards. (HC 9280237)
- The custom object supports reporting, dashboards, and viewing overlaps in Salesforce Classic. Supernode only. (HC 6574122)

### 1.2 Crossbeam-side requirements

- Crossbeam seat with Full Access Role: **Admin** and Sales Role: **Manager**. Check on the Team page. (HC 9280237)
- Integration Seat users can complete setup without a Crossbeam user seat (Supernode and Enterprise). (HC 9280237)
- If SSO is enforced, log in as the SSO exception user. (HC 9280237, HC 8337148)

### 1.3 Salesforce-side requirements

- Setting up Copilot: the **Crossbeam Setup User** permission set assigned. (HC 9280237)
- Setting up the Custom Object: Read access to Account or Lead objects; Write access if using the optional push of partner-shared data into Account custom fields; full access (Read, Create, Edit, Delete, View All Records, Modify All Records) to the Crossbeam Ecosystem Overlaps custom object. (HC 9280237)
- The reauthorization article lists integration user needs as: Crossbeam Setup User, Visualforce Page Access enabled, read access to Account and Lead. (HC 12013434)

### 1.4 Install the managed package

1. Go to Crossbeam's Salesforce AppExchange listing (listingId a0N3A00000FvKuqUAF), click **Get It Now**, log in to the target org.
2. Select **Install for Admins Only**, then **Install**. Selecting **Install for All Users** breaks the permission sets: you cannot control which users see Crossbeam data or what actions they take.
3. Approve Third-Party Access (tick checkbox, **Continue**). Domains: api.crossbeam.com (Crossbeam data), api.segment.io (usage reporting), auth.crossbeam.com (authenticating Crossbeam users), login.salesforce.com (Salesforce auth), sales-backend-api.crossbeam.com (Crossbeam for Sales data), sentry.io (error reporting), test.salesforce.com (sandbox testing). (HC 9280237)

### 1.5 Connect to Crossbeam (Crossbeam Setup App)

1. Assign yourself the **Crossbeam Setup User** permission set.
2. App Launcher, search "Crossbeam", open the Crossbeam Setup App, click **Get Started**. Click **Next** through every step until the final **Finish**.
3. Step 1, Outbound Connection: click **Validate**, log in with Crossbeam username and password or "Log in with Google" (or as SSO exception user). Click **Next**.
4. Step 2, Crossbeam Organization Selection: pick the Crossbeam account (users with several accounts see all). Click **Next**. A successful System Connections screen appears. (HC 9280237)

### 1.6 Configure Trusted URLs

- Needed for advanced Copilot features such as the "Plays" and "Contacts" tabs (iframe content).
- Setup, **Trusted URLs** (under Security), **New Trusted URL**: API Name `Crossbeam`; URL `https://app.crossbeam.com`; CSP Context `Lightning Experience Pages`; CSP Directives `frame-src (iframe content)`. Save.
- If "Adopt updated CSP directives" is enabled, also add `https://api.crossbeam.com` as a trusted URL (iframe-src).
- Verify in Crossbeam Setup that both System Connections and Configure Trusted URLs show complete. (HC 9280237)

### 1.7 Enable push to the Crossbeam Ecosystem Overlap custom object

1. Crossbeam web app, Integrations page, **Salesforce Custom Object** tile, **Install**.
2. **New authentication**, **Create**, log in with Crossbeam credentials, **Next**.
3. **New authentication**, **Create**, log in with Salesforce credentials, **Allow**, **Next**.
4. Package screen: no action (already installed), **Next**, **Finish**.
5. Optional: **Customize Data in Push**. By default all your populations and all partner populations are selected. Deselecting a population that already pushed deletes those records from the custom object on the next sync.
6. **Push opportunity data** setting: when on, a Crossbeam Ecosystem Overlap record is created for every Opportunity with a partner overlap, enabling reports on the Opportunity object and fields. Keeping it off reduces pushed volume.
7. Slide **Enable Data Push** ON, click **Save Changes**. (HC 9280237)
- Adding new partners, or partners sharing new populations, may push additional records. (HC 9280237)
- Sync frequency: defaults to twice a day, every 12 hours. Actual times may vary. (HC 9280237)

### 1.8 Permission sets

- **Crossbeam Setup User**: full admin access; must be assigned to whoever installs or reauthorizes; admin access to Copilot; write access to Crossbeam Ecosystem Overlap.
- **Crossbeam Account User**: access to Copilot. Full Access for users with a paid Crossbeam Core or Sales seat (includes partner-shared data); Starter Access (high-level overview) for users without a paid seat.
- **Crossbeam Widget Viewer**: Copilot access with clickable buttons disabled; cannot access partner-shared data or initiate conversations.
- **Crossbeam Report User**: access to the custom object; build reports and dashboards.
- Recommendation: assign Crossbeam Account User and Crossbeam Report User to the entire team. (HC 9280237)

### 1.9 Place Copilot

- Supported on Lightning pages for Account, Opportunity, Contact, and Lead. Recommended: Account and Opportunity pages, conspicuous location.
- Setup, Object Manager, Account, Lightning Record Pages, Default Accounts (or relevant), **Edit**; in Lightning App Builder scroll to "Custom - Managed", drag **Crossbeam Copilot** onto the layout; **Activation**, **Set as Org Default**, **Save**. Consider component visibility filters by role. (HC 9280237)

### 1.10 Crossbeam Ecosystem Overlap fields (v2)

| Field label | Meaning |
|---|---|
| Account | Salesforce account linked to the overlap |
| Created By | Usually the admin or installing user |
| Create Date | When the overlap was first matched and the record created; does not change on later updates |
| Crossbeam EID | Crossbeam housekeeping ID used in the push |
| Last Modified By | Usually admin or installing user |
| Last Modified Date | When the record was last updated, for example when shared partner data changed |
| Lead | Salesforce lead linked to the overlap |
| Opportunity | Salesforce opportunity linked to the overlap |
| Overlap Name | Clickable unique ID to open the full record |
| Owner | Usually admin or installing user |
| Partner Name | Partner as named in Crossbeam |
| Partner Populations | Partner's Custom Population matched |
| Partner Record Name | Partner-shared: account or lead name in the partner's data source |
| Partner Record Owner Email / Name / Phone | Partner-shared: account owner contact data |
| Partner Standard Populations | Partner's Standard Population matched |
| Partner Record Country / Employees / Industry / Type / Website | Partner-shared firmographics |
| Partner Record Owner Title | Partner-shared: job title of the owner |
| Populations | Your Custom Population matched |
| Standard Populations | Your Standard Population matched |

(HC 9280237)

- API names used in Flow examples: object `xbeamprod__Crossbeam_Overlap__c`; lookups `xbeamprod__Account__c`, `xbeamprod__Lead__c`; relationship paths `xbeamprod__Account__r.Owner.Email`, `xbeamprod__Lead__r.Owner:User.Email`. (HC 8770077)
- Record page layout: Object Manager, Crossbeam Ecosystem Overlap, Page Layout, "Crossbeam Ecosystem Overlap Layout". Suggested: your info (Account, Opportunity, your Standard or Custom populations) on the left; partner info (partner, partner population, partner owner if shared, partner's account name) on the right; created and modified timestamps at the bottom. (HC 9280237)

### 1.11 Running reports (managed package report types)

- Requires Crossbeam Report User. Reports, New Report, select the **All** category, search "Crossbeam Ecosystem", pick a report type, **Start Report**. In Filters select **All crossbeam ecosystem overlaps** and **All Time**. (HC 9280237)
- Best practice: add Partner Name next to Partner Standard Populations; group rows by Account Owner; for net-new pipeline filter Standard Populations equals Prospects and Partner Standard Populations equals Customers; add Partner Record Owner Name and Email for rep-to-rep collaboration; save to a Public folder. (HC 9280237)

---

## 2. Salesforce install on the Connector plan

- Requirements: Connector plan; Crossbeam seat with Full Access Role Admin or Sales Role Manager; Salesforce Lightning Experience; **My Domain** (custom domain) enabled to use Copilot. (HC 11407240)
- Copilot does not support "API Only" Integration User Profiles. (HC 11407240)
- Connector plan users do not have access to data in the Crossbeam Custom Object. The object is still installed with the package but no data is pushed. (HC 11407240)
- Steps:
  1. AppExchange listing, **Get It Now**, **Install in Production** (or **Sandbox** for testing), log in as Salesforce Admin, select **Install for Admin Only**, approve third-party domains, **Install**. Install can take several minutes; Salesforce sends a confirmation email.
  2. App Launcher, search **Crossbeam Setup**, **Get Started**, complete the three authentication steps.
  3. Setup, Security, Trusted URLs, **New Trusted URL**: API Name `Crossbeam`, URL `https://app.crossbeam.com`, CSP Context Lightning Experience Pages, CSP Directives `frame-src`. Save.
  4. Setup, Users, Permission Sets: open Crossbeam Setup User (admins), Crossbeam Account User (sellers), or Crossbeam Widget Viewer (read-only; sees partner overlaps and insights but interactive features disabled, including viewing partner-shared data and starting conversations). **Manage Assignments**, **Add Assignment**, select users, **Next**, **Assign**, **Done**.
  5. Place Copilot on Account, Opportunity, Lead, and Contact: Object Manager, object, Lightning Record Pages, select or **New**, **Edit**, drag **Crossbeam Copilot** from Custom - Managed (commonly right-hand column or a dedicated Partner Insights tab), **Save**, **Activation** as Org Default or for specific apps, record types, profiles.
  6. Crossbeam, Data, Integrations, Salesforce row **Settings**, section **Control what data shows in Copilot**: check or uncheck partners and overlap types. (HC 11407240)
- Users see Copilot data only with the required Crossbeam role and Salesforce permissions. (HC 11407240)

---

## 3. Salesforce v1 (legacy) and upgrade to v2

### 3.1 v1 facts (guide no longer maintained)

- v1 custom object is named **Crossbeam Overlap**; v2 is **Crossbeam Ecosystem Overlap**. (HC 9298987, HC 10578034)
- v1 custom object setup required Crossbeam Setup User, Visualforce Page Access enabled, and Read on Account and Lead. (HC 9298987)
- v1 Setup had a Step 3, **Inbound Connection**: click **Authorize** to generate a refresh token letting Crossbeam share data with Salesforce; approve the popup; status must change from "Not Connected" to "Connected". If using an Integration User, log in directly; Salesforce "login as" causes an Insufficient Privileges error. (HC 9298987)
- v1 push: Installed Integrations, **Settings** on Salesforce Custom Object tile, toggle **Enable Push** ON, filter "My Data" and "Partner Data", **Save**; data pushes at the next sync cycle. (HC 9298987)
- v1 fields: Account, Created By, Crossbeam EID, Crossbeam Overlap Name, Last Modified By, Lead, Opportunity, Owner, Partner Account (partner's record name), Partner AE Email, Partner AE Name, Partner AE Phone, Partner Name, Partner Population, Population. (HC 9298987)
- v1 report best practice filters: Population equals Prospects, Partner Population equals Customers; add Partner AE Name and Partner AE Email. Layout name "Crossbeam Overlap Layout". (HC 9298987)

### 3.2 Upgrade v1 to v2

1. Data, Integrations, find the **Salesforce Custom Object Legacy** row, click **Install**.
2. Complete Crossbeam and Salesforce authentication. On the **Salesforce Custom Object Package** screen you do not need to download the package again; **Next**, **Finish**.
3. Data, Integrations, **Salesforce Custom Object** row, **Setting**: toggle data push; select or deselect **Push Opportunity Data**; Customize Data in Push (My Population, Partner Populations); **Add new Partnerships Automatically** toggle (automatically add new partners); Partner-Specific Settings. **Save Changes**.
4. Validate in Salesforce: Setup, Object Manager, search **Crossbeam Ecosystem Overlap** (should be a deployed custom object). v1 Crossbeam Overlap also still appears.
5. Deactivate v1: Salesforce Custom Object Legacy row, **Setting**, deselect all boxes; the data is removed during the next sync. (HC 10578034)
- FAQs: no data loss (upgrade of the current object); allow at least an hour before data syncs; the Salesforce admin can hide v1 report types (Reports tab, Crossbeam Overlap Reports, **Hide Report Type**); workflows built on v1 must be recreated in v2. (HC 10578034)

---

## 4. Salesforce Custom Object reauthorization

- When needed: connection expired, integration user credentials changed, or troubleshooting related errors. (HC 9280237)
- Log in as the integration user in both Salesforce and Crossbeam (needs Crossbeam Setup User, Visualforce Page Access, Read on Account and Lead). Dedicated Integration Seat recommended. (HC 12013434)
- In Salesforce: App Launcher, **Crossbeam Setup**, **System Connections**, **Edit**, revalidate Outbound Connection (**Next**), select Crossbeam organization, **Finish**. (HC 12013434)
- In Crossbeam: Data, Integrations, **Salesforce Custom Object**, **Settings**, **Advanced Settings**. In the modal click the three-dot menu next to the connection (easy to miss), **Update**, reauthorize, **Save**. Repeat for the Salesforce authentication: three dots, **Update**, reauthorize in Salesforce, **Next**, **Finish**. Back in Settings click **Save General Settings**. (HC 12013434)
- Related errors clear automatically after the next sync, which may take up to 12 hours. (HC 12013434)

---

## 5. Salesforce Enhanced Ecosystem Reporting ("is a customer of", "is an open opportunity for")

- Pushes partner names onto two fields on the standard Account object for filters, reports, workflows, and downstream tools (Clari, Gong, Gainsight). Supernode only. Crossbeam for Salesforce must be installed first. Applies only to Standard Populations, not Custom Populations. (HC 10742955)
- Salesforce user needs Edit/Write on Account. (HC 10742955)
- Create fields: Setup, Object Manager, Account, Fields & Relationships, **New**, Data Type **Picklist (Multi-Select)**, **Next**. Field Label `is a customer of`; Values: **Enter Values**, type `NONE` as the default value; uncheck **Restrict picklist to predefined values** (allows dynamic partner names); Field Name autopopulates; optionally check auto add to custom report type; **Next**; grant field access to Crossbeam Setup User and the team permission sets; optionally add to page layouts; **Save & New** and repeat for `is an open opportunity for`. (HC 10742955)
- Enable in Crossbeam (only after both fields exist): Data, Integrations, Salesforce row **Settings**, toggle **Enable Data Push** ON. **Crossbeam Custom Object** tab: push ON, Save. **Account Object** tab: toggle **Push to Account Object** ON, pick the target Salesforce field in each of two dropdowns, Save. **Save Changes**. (HC 10742955)
- Crossbeam cannot complete the push unless the two custom fields exist first. (HC 10742955)

---

## 6. Partner Field Mapping to your CRM (Salesforce and HubSpot)

- Syncs partner-sourced fields (examples: Product Sold, Tech Stack, ACV) into text fields on the Salesforce Account object or HubSpot Company object. Supernode and Enterprise. (HC 11419695)
- Path: Data, Integrations, **HubSpot Custom Object** or **Salesforce Custom Object**, **Account Object** tab, **Map Partner Data to CRM**. (HC 11419695)
- Steps: create a TEXT field on Account (Salesforce) or Company (HubSpot); in integration settings Account object or Company object tab toggle on **Map Partner data to CRM**, map each partner field to a CRM text field; click **Save Account Object**. Data pushes on the next sync. (HC 11419695)
- Partner account fields sync only to Salesforce Account; partner company fields only to HubSpot Company. (HC 11419695)
- Timing: this sync is separate from data source update frequency; expect mapped data within 24 hours of saving. (HC 11419695)
- In Salesforce, synced mapped fields also appear in the Crossbeam Copilot widget. (HC 11419695)
- Limitations: all data converted to text; field format matching not supported; date fields cannot be mapped; picklist fields require manual mapping of each value. (HC 11419695)

---

## 7. Partner Account CRM Integration (Salesforce only)

- Creates a 1:1 link between each Crossbeam partner and its Partner Account record in Salesforce. Each Crossbeam Ecosystem Overlap record gains a **Partner Account lookup field** (a true relationship, not text), so reports can combine overlap data with partner owner, tier, type. (HC 14463181)
- Plan: mapping in Crossbeam on all plans; lookup field and Partner Tags sync on Supernode / Enterprise. (HC 14463181)
- Requirements: Salesforce connected as data source; Salesforce Custom Object Integration (v2) installed and active (Supernode / Enterprise); Crossbeam Admin role. (HC 14463181)
- Step 1: Data, **Data Sources**, Salesforce row gear icon, **Partner Mapping** tab. Crossbeam auto-matches partners to Salesforce accounts by domain; unmatched show **Unmapped**. (HC 14463181)
- Step 2 mapping rule: set a filter identifying Partner Accounts, for example Account Record Type equals Partner, Account Type equals Partner, Partner Type equals Strategic Partner. Click **Apply**. Matching reruns across all partners; may take a few minutes. (HC 14463181)
- Step 3 manual resolve: for each Unmapped partner use the Salesforce Account column dropdown, search by name, select; the ID shown is the Salesforce record ID for disambiguation. One-time setup. (HC 14463181)
- Step 4 Partner Tags sync (Supernode, Enterprise): add tags on the Partners page first. Create a Text field on Account labeled `(Crossbeam) Tags` (needs Edit/Write on Account; grant access to Crossbeam Setup User and team permission sets). Then Data, Integrations, Salesforce Custom Object gear, **Account Object** tab, toggle **Push Crossbeam partner tags to Salesforce** on, select the `(Crossbeam) Tags` field, click **Save Account Object**. Populates on the next Salesforce sync; verify on the Partner Account record Details tab. The push cannot complete unless the field exists first. (HC 14463181)

---

## 8. Salesforce Product Line Support (Product2)

- Salesforce only. Syncs product data so teams see which products are in play on opportunities. (HC 13613493)
- Requirements: Salesforce connected as a data source; syncing Opportunity data; **Product2** and **Opportunity Line Item** objects exist; Crossbeam's Salesforce connection has read on Product2, Opportunity Line Item, and Opportunity. If only Product ID syncs without a readable name, values appear as alphanumeric IDs. (HC 13613493)
- Step 1: Data, Data Sources, Salesforce **Settings**, **Field sync**, **Edit**; toggle on **Product 2** and **Opportunity Line Item** (expand to add fields beyond required presets); **Review Fields**, **Sync Now**. Both must be synced. (HC 13613493)
- Step 2: Salesforce Settings, **Field Mapping**, **Product Line Type Field**: choose the CRM field representing the product line (commonly Product Name), **Save**. (HC 13613493)
- Sharing: to let partners see Product2 data, update sharing in the Sharing Dashboard. (HC 13613493)
- Bridge model: Product2 holds the catalog; Opportunity Line Item links products to opportunities. Crossbeam identifies products on open opportunities and, for customers, the product on the most recent Closed-Won opportunity. Partner product data requires the partner to share Opportunity data. (HC 13613493)
- Where used: Deal Navigator (Product Type filter), Account Mapping List (Product Name filter), Performance Dashboard (filter by Product Type), Record Detail Page, Account Detail Drawer, Copilot, and Population building (custom populations by Product Type). (HC 13613493)

---

## 9. Salesforce reporting, dashboards, related lists, alerts

### 9.1 Permissions

- Reports and dashboards: Crossbeam Reports User or Crossbeam Setup User permission set. Workflows and automations: Salesforce system admin. (HC 8765980)

### 9.2 Basic Crossbeam Ecosystem Overlap report

- Reports, **New Report**, select **All**, type "Crossbeam", choose **Crossbeam Ecosystem Overlaps with Account**, **Start Report**. Filters: change **Show Me** from "My Crossbeam ecosystem overlaps" to **All Crossbeam Ecosystem Overlaps**. Outline: add Partner Name, Partner Standard Population, Partner AE Name, Partner AE Email (type "Partner" to find). **Run**. (HC 8765980)
- Single-partner mutual customers: filter Partner Name contains [partner] and Partner Standard Populations equals customers. (HC 8765980)
- The column "Crossbeam Ecosystem Overlap: Overlap Name" is a unique ID and can be removed for revenue reporting. (HC 8765980)
- AE version: Outline, Group Rows by **Account Owner**, Run. (HC 8765980)
- Dashboard: **New Dashboard**, **+ Widget**, select report and visualization, **Add**. Grouping by Account Owner, Partner AE Name, Partner Name shows which partner AEs each AE overlaps with most. (HC 8765980)
- Intro requests: reps create a Task (Subject, context, Partner) from Copilot; tasks roll into a report and are assigned to the Partner Manager. (HC 8765980)

### 9.3 Ready-to-Use Salesforce Crossbeam Reports

- Automatically created when the package is installed. Supernode only; requires the Salesforce Custom Object Integration. (HC 9280237, HC 10064990)
- The **Crossbeam Reports** folder defaults to private (admin-only). To share: Reports, **All Folders**, Crossbeam Reports row dropdown, **Share**; Share With: Users, Roles, and/or Public Groups; confirm **View** access. (HC 10064990)
- Categories: Source Opportunities (prospects vs partners' customers), Influence Deals (open opps overlapping partners' customers), Retain & Expand Customers (customers vs partners' customers). (HC 10064990)
- Reports: Ecosystem Qualified Leads, Expansion Opportunities with Stages, Expansion Opportunities with Partner Overlaps, Opportunity Influence (by Stage), Partner Mutual Customers, Top Revenue EQLs, Expansion Opportunities, Opportunity Influence (by Owner). (HC 10064990)

### 9.4 Crossbeam 360 Dashboard (Salesforce)

- Built on the ready-to-use reports, which must exist and contain data. (HC 10149634)
- Step 1: Dashboards, **Create New Dashboard**, name "Crossbeam 360 Dashboard", public folder.
- Step 2: image widget header, Scale **Fit Width**.
- Step 3 top-row metric widgets (Metric Chart, Record Count, delete default Title, Display Units Shortened Number, Ranges -100 and 1, Decimal Places Automatic where stated) with footers: Ecosystem Qualified Leads "My prospects VS partners' customers"; Top Revenue EQLs "My strategic prospects VS partners' customers"; Open Opps with Partner Overlaps "My open opps VS partners' customers/open opps"; Partner Mutual Customers "My customers VS partners' customers"; Expansion Opps "My customers with an open opp VS partners' customers".
- Step 4 Source Opportunities: text widget; Top Revenue EQLs metric; Ecosystem Qualified Leads donut (Record Count sliced by Account: Account Owner, Max Values 100, Title "Prospects to Source Deals"); EQL Lightning Table (Account Owner, Account Name, Partner Name, Revenue Bands, sorted by Revenue Bands descending).
- Step 5 Influence Deals: Open Opps with Partner Overlaps metric; Opportunity Influence (By Stage) vertical bar (X Stage; Y Record Count and Sum of Amount, amount plotted as line on second axis); Opportunity Influence (By Owner) donut (Sum of Amount by Opportunity Owner, Max Values 6); By Owner Lightning Table (Owner, Opportunity Name, Stage, Amount, Partner Name, Partner Standard Populations, sorted by Amount descending).
- Step 6 Retain & Expand: Expansion Opps metric ("Open Deals on Existing Customers"); Expansion Opps horizontal bar (Sum of Amount by Opportunity Owner); Expansion Opps with Stages Lightning Table (adds Account Name and Close Date, sorted by Close Date descending).
- Step 7: review, **Save**; edit later with the pencil. (HC 10149634)

### 9.5 Crossbeam Ecosystem Overlaps related list

- Setup, Object Manager, Account or Opportunity, **Page Layouts**, select layout, **Related Lists**, drag **Crossbeam Ecosystem Overlaps** into the section; wrench icon to choose fields. Recommended: Partner Name, Partner Standard Populations, Partner Populations, Partner Record Owner Name, Partner Record Owner Email. **Save**. Any user with Crossbeam Report User can see it. (HC 12872312)

### 9.6 Combined Overlap and Partner Account report type

- Requirements: v2 package; at least one mapped Partner Account; Salesforce user with **Manage Report Types**; report runners need Crossbeam Report User. (HC 14625782)
- Setup, Quick Find **Report Types**, **New Custom Report Type**; Primary Object **Crossbeam Ecosystem Overlaps**; label recommended "Crossbeam Ecosystem Overlaps with Account and Partner Account"; category Other Reports; Deployment Status **Deployed**; **Next**. Edit Layout: overlap fields (Partner Name, Standard Populations, Partner Standard Populations, Account, Opportunity), Account fields (Account Owner, Account Name, Industry, Annual Revenue), Partner Account fields (Account Owner as Partner Manager/CAM, Account Name, Type, custom tier fields). **Save**. (HC 14625782)
- Report: New Report, pick the type, **Start Report**, Filters All Time and All Crossbeam Ecosystem Overlaps; columns such as Account Name, Partner Name, Partner Account: Account Owner, Partner Account: Type, Standard Populations, Partner Standard Populations, Account Owner; group by Partner Account: Account Owner so each Partner Manager sees their accounts. **Save & Run**. (HC 14625782)

### 9.7 Overlap alerts in Salesforce

- Option 1 (Email template plus Email Alerts plus Flow):
  - Setup, Email Templates, **Classic Email Templates**, **New Templates**, type **Text**, fill name, subject, body, check **Available For Use**. For a record link, take an existing overlap URL and replace the Id with `{!xbeamprod__Crossbeam_Overlap__c.Id}`. Save.
  - Email Alerts: "New Overlap Notification - Account Owner" (Object Crossbeam Overlap, template New Overlap Notification, Recipient Account Owner, From current user or Org-Wide address); "New Overlap Notification - Lead Owner" (Recipient Related Lead or Contact Owner).
  - Flow: **Record-Triggered Flow**, Auto-Layout; Object Crossbeam Ecosystem Overlap; Trigger "A record is created"; Optimize for Actions and Related Records. Decision "Account or Lead" with outcomes: Account when `{!$Record.xbeamprod__Account__c} Is Null = {!$GlobalConstant.False}`; Lead when `{!$Record.xbeamprod__Account__c} Is Null = {!$GlobalConstant.True}` AND `{!$Record.xbeamprod__Lead__c} Is Null = {!$GlobalConstant.False}`; Default. Add the matching Email Alert action on each path with Record Id `{!$Record.Id}`. Save and activate. (HC 8770077)
- Option 2 (Flow only): same start; New Resource **Text Template** API Name `NewOverlapNotificationTemplate` with body including a link to `/lightning/r/xbeamprod__Crossbeam_Overlap__c/{!record.Id}/view`; New Resource **Formula** API Name `EmailAddressFormula`, Text, `IF( {!$Record.xbeamprod__Account__c} != '', {!$Record.xbeamprod__Account__r.Owner.Email}, {!$Record.xbeamprod__Lead__r.Owner:User.Email} )`; Action **Send Email**. (HC 8770077)

---

## 10. HubSpot Custom Object integration

### 10.1 What it does

- Pushes overlaps into a HubSpot custom object named **Crossbeam Overlaps**, syncs selected Crossbeam reports to HubSpot contact lists, and (optionally) pushes "Is a customer of" and "Is an open opportunity of" to the Company object. (HC 7971155)

### 10.2 Requirements

- Supernode plan. Crossbeam Full Access Seat (Standard user or Admin role) with Integration permissions. HubSpot **Sales Hub - Enterprise** to create the custom object; **Marketing Hub - Professional** to send data to contact lists. (HC 7971155)
- HubSpot Private App Access Token with scopes: `crm.lists.read`, `crm.lists.write`, `crm.objects.companies.read`, `crm.objects.companies.write`, `crm.objects.contacts.read`, `crm.objects.contacts.write`, `crm.objects.custom.read`, `crm.objects.custom.write`, `crm.schemas.companies.read`, `crm.schemas.companies.write`, `crm.schemas.custom.write`, `crm.schemas.custom.read`, `crm.import`. Missing scopes cause an error and the integration will not complete. (HC 7971155)

### 10.3 Remove the legacy HubSpot integration first (if present)

- Integrations workspace, **HubSpot Custom Object (legacy)** in Installed Integrations, three dots, **Remove Integration**. In HubSpot delete all records for the custom object **Crossbeam Overlaps** (needs Bulk Delete permission). The new integration pushes new copies; existing workflows and reports keep working. The legacy integration cannot be reinstalled after deletion. (HC 7971155)

### 10.4 Install

1. Integrations, Available Integrations, **HubSpot Custom Object**, **Install**.
2. Complete Crossbeam Authentication in the modal, **Next**.
3. HubSpot Authentication: **New Authentication**, paste the Private App Access Token, **Next**.
4. Configure Crossbeam reports to export as HubSpot Lists: choose under Report, **Add to Configuration**, **Next**.
5. **Finish**.
6. Required: configure population data. In the side panel **Customize Data in Push**: expand **My Data**, select populations; expand **Partner Data**, select populations for all partners or per specific partner. **Save Changes**. The integration is not complete until this is done. (HC 7971155)
- Adjust or reauthorize later: Integrations, HubSpot in Installed Integrations, **Settings**. (HC 7971155)

### 10.5 Contact lists

- Lists use the Crossbeam report name with "Crossbeam" added. Overlaps update in real time, removing stale overlaps and adding new records. (HC 7971155)

### 10.6 Custom object fields

| Field | Meaning |
|---|---|
| Account ID | HubSpot account record for the overlap |
| Crossbeam EID | Crossbeam housekeeping ID |
| Lead ID | HubSpot contact record for the overlap |
| Name | Clickable record name opening the full overlap record |
| Overlap Unique Id | Crossbeam housekeeping ID |
| Partner Name | Partner as named in Crossbeam |
| Partner Population | Partner population matched |
| Partner AE Email / Name / Phone | Partner-shared account owner data |
| Population | Your population matched |

(HC 7971155)

### 10.7 API usage

- Uses some of your HubSpot Private App API limits; uses batch calls and resumes where it left off. (HC 7971155)

### 10.8 Enhanced Ecosystem Reporting (Company object)

- Pushes **is a customer of** and **is an open opportunity of** to the standard Company object. Supernode; Full Access seat with Integration permissions; HubSpot Enterprise license; HubSpot user needs Edit access on Company properties. (HC 10445323)
- Enable: Data, Integrations, HubSpot **Settings**. General Settings: **Enable Data Push** ON, **Save General Settings**. **Crossbeam Custom Object** tab: **Push to Custom Object** ON, **Save Custom Object**. **Company Object** tab: **Push to HubSpot Object** ON, **Save Company Object**. (HC 10445323)
- In HubSpot, filter Companies on the new fields; `NONE` under a field means no connected data. (HC 10445323)
- The integration only pushes; it never deletes existing HubSpot data. Cleanup is the user's responsibility. (HC 10445323)

### 10.9 Reauthorize HubSpot Custom Object

- Prereqs: Full Access seat (Standard or Admin) with Integration permissions; Sales Hub Enterprise; Marketing Hub Professional if using lists; Integration Seat recommended. (HC 12158775)
- Confirm scopes: HubSpot Settings, **Private Apps**, Crossbeam App, **Auth** tab; if any scope is missing, **Edit App** and update. (HC 12158775)
- Crossbeam: Data, Integrations, HubSpot Custom Object **Settings**, **Advanced Settings**; three dots next to the connection, **Update**, **Save** in Edit Authentication; three dots, **Update**, **Save** for HubSpot; **Next**; add or remove lists; **Next**; **Finish**; **Save General Settings**. Errors clear after the next sync, up to 12 hours. (HC 12158775)

### 10.10 HubSpot reports

- Supernode; requires HubSpot Custom Object. Reports, **Create Report**, **Single Object**, search "Crossbeam", pick **Crossbeam Overlaps**, **Next**. Date range defaults to "This quarter so far"; change to **All data**. Name with the pencil. Default properties: partners and Populations; **Add Crossbeam Overlap Property** for more. **Advanced filters**, **Add filter** (Populations, Partner Populations), values in **Add Values**. Filter values must be exact matches; copy population names from the report. **Next** to choose a visualization, drag properties under **Displaying**, **Save**. Reports auto-update as Crossbeam data changes. (HC 11378668)

### 10.11 HubSpot Crossbeam 360 Dashboard

- Supernode; requires HubSpot Custom Object; every report must be built first. (HC 11394640)
- Dashboards, **Create Dashboard**, name "Crossbeam 360 Dashboard", set viewers, create. Header via **Actions**, **Add images, text, or video**, **Insert Image**, about 1300x150 pixels. (HC 11394640)
- News Feed tables (Include data if it matches ALL): "Prospects where a Partner recently closed a customer" (Partner Population contains any of customers; Population contains any of prospect; columns Object Last Modified Date/Time Monthly, Company Name, Partner Name, Partner AE Name, Partner Population, Population). "Prospects where a Partner recently opened an opportunity" (Partner Population contains any of open opportunities). (HC 11394640)
- Sourced: "Partners with a Customer Relationship" horizontal bar (Partner Population contains customers; X Count of Companies; Y Partner Name). "Accounts Where Partners Can Help Source Opportunities" table (Partner Population equals customers; Population contains prospect; Company Owner, Company Name, Partner Name, Partner Population). (HC 11394640)
- Influenced: "Partner Deal Influence" pie (Partner Population contains customers or open opportunities; Companies Total open deal value is known; value Total Open Deal Value by Partner Name). "Accounts where partners can help influence existing opportunities" table. (HC 11394640)
- Retain and Expand: Mutual customers vertical bar; customers-of-partners pivot table; Expand Opportunities horizontal bar (Population contains customers; Total open deal value at least 1); Integration adoption potential (Integration is not equal to N or is empty; both populations contain customer). Adjust names to match your populations. (HC 11394640)

---

## 11. Microsoft Dynamics Custom Object integration

- Supernode only; must be a Crossbeam admin. Works with Dynamics 365 Sales Premium, Sales Enterprise, or Sales Professional. (HC 10064960)
- Install: Integrations, **Microsoft Dynamics Custom Object**, **Install**. Crossbeam Authentication: add a new account, **Next**. Dynamics 365 authentication: **add a new account**, enter the Dynamics instance URL, **Create**, log in if prompted. Setup can take time. The screen shows **Dynamic Crossbeam Overlap Entity Creation** once the custom object is created; **Next**; **Finish**. (HC 10064960)
- Opportunity fields are not currently pushed into Dynamics. (HC 10064960)
- Show on Account page: Account page, **Advanced Settings**, **Default Solution**, find the Crossbeam Overlaps table, **Relationships**, Account, **Edit**, Display Settings (plural names or custom table option), **Save**, **Publish All Customizations**. (HC 10064960)
- Navigation bar: Settings, Advanced Settings, **Solutions**, Default Solution, Site Maps, **Sales Hub**, **Sales Insight Settings**, plus icon, **Sub Area**, Type **Entity**, Entity **Crossbeam Overlap**, save and close, **Done**, **Publish**. Optional: Tables, Crossbeam Overlap, Views, **All Crossbeam Overlaps** to change columns, order, filters. (HC 10064960)
- Covered by Universal Integration Settings. (HC 10080455)

---

## 12. Snowflake integration (push)

- Pushes overlap data into Snowflake via a data share. (Separate from Snowflake as a data source.) (HC 4694521)
- If no enable option appears, it may not be in your plan; contact CSM, sales rep, or the Crossbeam support inbox (support at crossbeam.com). (HC 4694521)
- Prerequisites: on the Integrations page click **Set Up** next to Snowflake and supply (1) account region and (2) account name from `https://<account_name>.<region>.snowflakecomputing.com`. Supported regions listed: US West (Oregon), which is the only one not included in Snowflake URLs; US East (Ohio); US East (N. Virginia); EU West (Ireland); EU-Central (Frankfurt). Other regions: ask Crossbeam. (HC 4694521)
- Enable: Snowflake tile, turn on **Enable**. You then receive an incoming data share. (HC 4694521)
- Settings: Data, Integrations, Snowflake row **Settings**: Adjust Data Pushes, Customize Data in Push (My Population, Partner Populations), Partner-Specific Settings, **Re-authorize**, **Save**. (HC 4694521)
- Data share name `CROSSBEAM_OVERLAPS_<ORG-ID>_<RAND-IDENTIFIER>`; schema `CROSSBEAM`; view `OVERLAPS`. (HC 4694521)
- Columns: `ENTITY_ID` VARCHAR (CRM ID of account or lead); `ENTITY_TYPE` VARCHAR (`account` or `lead`); `POPULATION_NAME`; `PARTNER_NAME`; `PARTNER_POPULATION_NAME`; `PARTNER_AE_NAME`; `PARTNER_AE_EMAIL`; `PARTNER_AE_PHONE`; `MATCHED_AT` TIMESTAMP_TZ (first visible in Crossbeam); `PARTNER_DOMAIN` (from registration website); `UPDATED_AT` TIMESTAMP_TZ (last updated in Snowflake); `CREATED_AT` TIMESTAMP_TZ; `PARTNER_AE_TITLE`; `PARTNER_RECORD_NAME`; `PARTNER_RECORD_WEBSITE`; `PARTNER_RECORD_TYPE`; `PARTNER_RECORD_COUNTRY`; `PARTNER_RECORD_INDUSTRY`; `PARTNER_RECORD_EMPLOYEES` INTEGER. All others VARCHAR. (HC 4694521)
- `MATCHED_AT` never updates after the original match; use `UPDATED_AT` to track changes. (HC 4694521)

---

## 13. Databricks integration (push)

- Writes overlaps to a single `overlaps` Delta table in a catalog and schema you choose. Independent from Databricks as a data source; they can point to different catalogs and schemas. Supernode and Enterprise. (HC 15231550)
- Prerequisites: Unity Catalog enabled; a SQL Warehouse (Server hostname like `dbc-12345abc-6789.cloud.databricks.com`, HTTP path like `/sql/1.0/warehouses/abc123def456`, from Connection Details); a Service Principal with OAuth client secret. Personal access tokens and interactive OAuth are not supported. (HC 15231550)
- Service Principal: account console Settings, Identity and access, Service principals, **Add service principal**; Secrets, **Generate secret**; copy Client ID (Application ID) and Client Secret (shown only once); SQL Warehouses, your warehouse, Permissions, add the SP with **Can use**. (HC 15231550)
- Step 1: `CREATE CATALOG IF NOT EXISTS crossbeam_push; CREATE SCHEMA IF NOT EXISTS crossbeam_push.overlaps;` The schema must exist before enabling. (HC 15231550)
- Step 2 grants: `GRANT USE CATALOG ON CATALOG crossbeam_push TO `crossbeam-sp`;`, `GRANT USE SCHEMA, CREATE TABLE ON SCHEMA crossbeam_push.overlaps`, `GRANT MODIFY, SELECT ON SCHEMA crossbeam_push.overlaps`. CREATE TABLE creates the table on first push; MODIFY merges and deletes; SELECT validates structure and permissions. (HC 15231550)
- Step 3: Integrations, **Databricks Push**, **Enable**; enter Server hostname, HTTP path, Catalog, Schema, Client ID, Client Secret; **Enable**. Crossbeam connects, runs `CREATE TABLE IF NOT EXISTS <catalog>.<schema>.overlaps ... USING DELTA`, validates columns, runs a no-op merge. Failures show a specific UI error (missing permissions, table not found, etc.). (HC 15231550)
- Table columns: `organization_id` INT, `population_id` INT, `population_name`, `master_id` (your record ID), `mdm_type` (account, lead, etc.), `partner_organization_id` INT, `partner_population_id` INT, `partner_population_name`, `partner_master_id`, `partner_name`, `partner_domain`, `partner_ae_email`, `partner_ae_name`, `partner_ae_phone`, `partner_ae_title`, `partner_record_name`, `partner_record_website`, `partner_record_type`, `partner_record_country`, `partner_record_industry`, `partner_record_employees` INT, `matched_at`, `created_at`, `updated_at` TIMESTAMP. Strings are STRING. (HC 15231550)
- MERGE key `(population_id, partner_population_id, master_id, partner_master_id)`. Overlaps removed in Crossbeam are deleted on the next push. Bookmarking per population pair on `updated_at`. Trigger: on-demand via Crossbeam, no manual scheduling. (HC 15231550)
- `partner_ae_*` columns require a `users` table in your Sync integration plus `owner_id` references on `accounts`, `deals`, and/or `leads`. `matched_at` does not update; use `updated_at`. (HC 15231550)
- Limits: fixed schema (no extra columns), single destination table. (HC 15231550)
- Manage: Integrations, Settings icon on Databricks: Enable Data Push, Customize Data in Push, Manage Partner Populations, Partner-Specific Settings, **Save changes**. (HC 15231550)

---

## 14. Matillion

- ETL connector built, hosted, and supported by Matillion. Setup is entirely on Matillion's side via API-based OAuth using a Crossbeam Client ID and Client Secret. Download from the Crossbeam connector page on Matillion Exchange. (HC 5206786)
- Bugs and enhancement requests go to Matillion support. Crossbeam CS helps only with Crossbeam-side tasks like generating API credentials. (HC 5206786)

---

## 15. REST API

- Supernode only. Calls count toward Record Exports. (HC 4677142)
- Create a custom integration: Data, Integrations, **+ Create Integration**; Integration name; Integration description (optional, 140 characters max); Callback URL `https://oauth.pstmn.io/v1/callback`; Allowed Origins blank; **Create Integration**. Auth and endpoints at developers.crossbeam.com. (HC 4677142)
- Existing API provides raw overlap data; the Signals API and webhook deliver event-based data. (HC 12732223)

---

## 16. Ecosystem Signals: API and Webhooks

- A signal is a partner event such as an opportunity opening or closing. (HC 12732223)
- Plans: Free and Connector none; Supernode API; Enterprise API and Webhook. Only Admin users can create or edit webhooks and API integrations. No extra licenses needed. (HC 12732223)
- Partner requirements: CRM connected to Crossbeam and sharing Deal open date, Deal close date, Deal is closed, Deal is won. You only need to sync these yourself, not share back. Your own source can be CSV or Google Sheet. (HC 12732223)
- Contact info on opportunity signals requires the partner to share CRM contact data (Contact Name, Contact Title). Parameters: `contact_name`, `contact_role`, `contact_type` (decision maker, influencer, buyer). (HC 12732223)
- Webhook setup: Data, Integrations, **+Create New**, **Webhook**. Event types: **Deal opened**, **Deal closed-won**. Webhook name, Destination URL, **Finish**. A secret key appears once; copy it. Crossbeam sends a test call; on failure use **edit configuration** and retry. Filters (partners, Populations) only after a successful test; triggers only for overlaps between selected populations. **Save Settings**. Manage via Data, Integrations, Settings. (HC 12732223)
- API setup: Data, Integrations, **+Create New**, **API Integration**; name, description, Callback URL, Allowed Origins; **Create Integration**; follow developer docs. (HC 12732223)
- Greenfield account signals are not supported. Webhooks count toward Record Exports. (HC 12732223)

---

## 17. Clay

- Imports overlap accounts into Clay tables for enrichment and outreach. Clay pulls all partner-shared data. Configured entirely in Clay; no Crossbeam setup. Requires Crossbeam Supernode and Clay Pro. Partners and Populations must be configured in Crossbeam first. (HC 10080441)
- Steps: Clay **Create New**, **Crossbeam Source** action, **Add Account**, authorize on the Crossbeam auth page, select organization, partner, Populations, set overlap limits, **Continue**. Existing table: **Actions**, **Import**, Crossbeam Source. (HC 10080441)
- Fields: everything from the account overlaps endpoint (partner owner, record email, website, Crossbeam ID). New matching accounts flow automatically. Authenticate once for all tables. Multiple partners: add a second source per partner. (HC 10080441)

---

## 18. PartnerStack

- Refer leads from Crossbeam into PartnerStack. Connector and Supernode. User must be a PartnerStack Admin. (HC 8533576)
- Install: Data, Integrations, PartnerStack tile, **Install**, **Connect to Crossbeam**. Lists gain a private **PartnerStack** column (if missing: **Columns**, expand Crossbeam Columns, check Partnerstack, **Save**). (HC 8533576)
- Use: **Refer Lead**, select partner, fill required fields, **Submit Lead**; column shows date sent. Timeline tab on the record shows date and time. Also works from Static Shared Lists via the icon in the Name column. (HC 8533576)
- Manage: Installed Integrations row shows Active; **View App**; three dots to reauthorize or delete. (HC 8533576)

---

## 19. Adobe Marketo Engage

- Adds persons from overlapping accounts in Crossbeam reports to Marketo Programs. Supernode; Salesforce must be a connected data source; Marketo Admin required. (HC 8575980, HC 8801394)
- Install: Integrations, Adobe Marketo Engage tile, **Install**. Crossbeam auth: **New Authentication**, personal credentials, authorize. Marketo auth: **New Authentication** with API endpoint domain (Admin, Integration, Web Services, Rest API, Endpoint; exclude trailing `/rest`), Client ID and Secret (Admin, Integration, LaunchPoint, Create a New Service, **View Details**); **Create**. (HC 8801394)
- Configure on **Please Configure Overlaps**: Organization, Crossbeam Report, Marketo Program; repeat; **Next**; enter a processing date so all persons land in Members tab; **Next**, **Finish**. Initial sync may take up to 10 minutes. (HC 8575980)
- Manage: **Configure** to edit, three dots to remove. Add report: **Add to Configuration**. Remove: hover row, red X. (HC 8575980)

---

## 20. Slack app

- Plans: `/crossbeam` on Free, Connector, Supernode; List Notifications on Connector and Supernode; partner owner fields via Salesforce Supernode only. (HC 3639783)
- Install from Data, Integrations. Requires a Crossbeam account. Only one Crossbeam account connects to Slack at a time; authorizing from a second org removes the first. (HC 3639783)
- `/crossbeam [company]`: shows company, overlapping partners, link; private to you unless **Share in Channel**. `/crossbeam people [First Last]` for contacts (must include `people`). `/crossbeam help`. In Slack Connect use **View in Crossbeam**. (HC 3639783)
- List Notifications: List hub bell icon, or saved list **Action**, notifications; pick channel (or **Connect to Slack**). Private and Slack Connect channels require `/invite`, **Add apps to this channel**, Crossbeam. Delivered every four hours. (HC 3639783)
- @mentions: data source includes Account Owner Name and Email (CSV/Sheet must map Account Owner Email); list includes both columns. Name without email shows the name without mention; owners not in channel get no alert. (HC 3639783)
- Crossbeam flags Slack Connect channels with an unknown org, a partner not in the list, or multiple orgs. (HC 3639783)
- Slack shows only your data, not partner owners; surface partner owners via the Salesforce custom object (Supernode). (HC 3639783)

---

## 21. AI Agents (public beta)

- Join via Settings, Labs, AI Agents, **Join Waitlist**. Connector, Supernode, Enterprise. Full-access seat to create; Slack must be connected. Agents permission: Manage or View. Feedback the Crossbeam product inbox (product at crossbeam.com). (HC 15961519)
- Create: **Agents**, **Create Agent**, name; trigger (New mutual customer, New mutual account detected, Partner opens a new opportunity on a mutual account, Partner closes a deal won on a mutual account); optional AND-only conditions (Partner, Partner Score, Partner tag, Industry, Number of Employees, Amount, Close Date, Is Closed/Is Open); action (channel, Slack Connect partner, DM; Tag Account Owner toggle); channel. **Test Agent** required, then **Save Agent**. (HC 15961519)
- Runs hourly, new matches only, at most one notification per run. Message copy fixed. Enable, disable, edit, delete from the Agents page. Skipped if Slack needs reauthorization. (HC 15961519)

---

## Troubleshooting

Error strings appear in backticks exactly as written in the articles. Symptoms without a quoted string are described plainly.

### Salesforce (managed package, custom object, data source)

- Symptom: authorization error when connecting or reauthorizing the Salesforce Custom Object Integration or Salesforce as a Data Source. Cause: Salesforce's September 2025 Connected Apps security update blocks "uninstalled" connected apps (authorized by a user but never formally installed in the org). Connected app names: `Crossbeam Salesforce Overlaps Push` (custom object) and `Crossbeam` (data source). (HC 12510571, HC 9280237, HC 12013434)
  - Fix A: Salesforce Setup, **Connected Apps OAuth Usage**, find the app, click **Install**; optionally adjust security and access policies so only users with the Crossbeam Setup User permission set have access; retry in Crossbeam. (HC 12510571)
  - Fix B (production only; for Sandbox or UAT ask your Salesforce admin for the correct URL): install directly at `https://{your-sfdc-domain}/identity/app/AppInstallApprovalPage.apexp?app_id=0Ci1U000000L2SJ&app_org_id=00D1U000001BPt6` for Crossbeam Salesforce Overlaps Push, or `https://{your-sfdc-domain}/identity/app/AppInstallApprovalPage.apexp?app_id=0Ci1U000000bmwH&app_org_id=00D1U000001BPt6` for Crossbeam (data source). Retry. (HC 12510571)
  - Fix C: if still not visible, add the **Approve Uninstalled Connected Apps** permission to the Salesforce Integration/Service user, retry the connection, confirm Crossbeam now appears in Connected Apps OAuth Usage, install it, then remove Approve Uninstalled Connected Apps from the integration user. (HC 12510571)
- Error: `Insufficient Privileges` during v1 Step 3 Inbound Connection. Cause: using Salesforce's "login as" with an Integration User. Fix: log in directly as that user. (HC 9298987)
- Symptom: v1 Inbound Connection does not complete. Check: status must change from "Not Connected" to "Connected" after **Authorize** and approving the Salesforce popup. (HC 9298987)
- Symptom: cannot control which users see Crossbeam data; permission sets behave incorrectly. Cause: package installed with **Install for All Users**. Fix: package must be installed with **Install for Admins Only**. (HC 9280237, HC 9298987)
- Symptom: Crossbeam Setup steps cannot be completed. Cause: Crossbeam Setup User permission set not assigned to the installer, or Crossbeam seat lacks Full Access Admin plus Sales Manager roles. Fix: assign the permission set; check the Team page, or use an Integration Seat (Supernode, Enterprise). (HC 9280237)
- Symptom: Validate login fails on an SSO-enforced org. Fix: create and use an SSO Exception User with Standard or Google login; authenticate using the same method listed on the Team page. (HC 8337148, HC 9280237)
- Symptom: Copilot "Plays" and "Contacts" tabs do not load. Cause: Trusted URL missing. Fix: add `https://app.crossbeam.com` with CSP Context Lightning Experience Pages and directive frame-src; if "Adopt updated CSP directives" is enabled, also add `https://api.crossbeam.com`. Confirm Configure Trusted URLs shows complete in Crossbeam Setup. (HC 9280237, HC 11407240)
- Symptom: Copilot not working for a user. Causes: "API Only" Integration User Profiles are unsupported; My Domain not enabled; Lightning Experience not in use; user lacks the Crossbeam role or Salesforce permission set. (HC 11407240)
- Symptom: Copilot shows only a high-level overview. Cause: user has Crossbeam Account User but no paid Crossbeam Core or Sales seat (Starter Access). Symptom: buttons disabled and no partner data. Cause: Crossbeam Widget Viewer permission set. (HC 9280237, HC 11407240)
- Symptom: Crossbeam Ecosystem Overlap object empty on Connector plan. Cause: expected; no data is pushed to the custom object for Connector plan. Fix: upgrade to Supernode. (HC 11407240)
- Symptom: custom object not receiving data after install. Checks: **Enable Data Push** toggled ON and **Save Changes** clicked; sync runs every 12 hours (twice a day), times vary; Record Export limit not reached. (HC 9280237, HC 4694521)
- Symptom: overlap records disappeared. Cause: a population was deselected in Customize Data in Push; records are deleted on the next sync. (HC 9280237)
- Symptom: no overlap records per Opportunity; cannot report on Opportunity fields. Cause: **Push opportunity data** off. Fix: turn it on (increases volume). (HC 9280237)
- Symptom: unexpected record growth. Cause: new partners or newly shared partner populations push additional records. (HC 9280237)
- Symptom: users cannot find Crossbeam report types or reports. Fixes: assign Crossbeam Report User; select the **All** category when searching; share the private Crossbeam Reports folder with View access. (HC 9280237, HC 10064990)
- Symptom: report shows only a subset of overlaps. Cause: default Show Me filter "My Crossbeam ecosystem overlaps". Fix: set **All Crossbeam Ecosystem Overlaps** and **All Time**. (HC 8765980, HC 9280237)
- Symptom: Ready-to-Use reports missing. Causes: not on Supernode, or Salesforce Custom Object Integration not installed. (HC 10064990)
- Symptom: after v1 to v2 upgrade, both Crossbeam Overlap and Crossbeam Ecosystem Overlap objects appear. Expected. Fix: hide v1 report types, recreate v1 workflows on v2, deselect all boxes on the Salesforce Custom Object Legacy row so v1 data is removed next sync. Data may take at least an hour to sync after upgrade. (HC 10578034)
- Symptom: reauthorization done but errors remain. Fix: wait for the next sync, up to 12 hours. The three-dot menu in Advanced Settings is easy to miss. (HC 12013434)
- Symptom: "is a customer of" / "is an open opportunity for" not populated. Causes: fields not created before enabling (Crossbeam cannot complete the push otherwise); fields not multi-select picklists with restriction unchecked; target fields not selected in the Account Object tab dropdowns; only Standard Populations are supported; user lacks Edit/Write on Account. Partner-specific integration settings also filter this push. (HC 10742955)
- Symptom: `(Crossbeam) Tags` field empty. Causes: field not created first, partner not mapped, partner has no tags in Crossbeam, sync toggle off, next Salesforce sync not yet run. (HC 14463181)
- Symptom: partners show **Unmapped**. Fix: apply a mapping rule, then map remaining partners manually via the Salesforce Account dropdown (use the displayed Salesforce record ID to disambiguate). Mapping may take a few minutes after a rule is applied. (HC 14463181)
- Symptom: mapped partner fields not showing. Checks: target is a TEXT field on Account; allow up to 24 hours; date fields cannot be mapped; picklists need per-value mapping. (HC 11419695)
- Symptom: product values appear as alphanumeric IDs. Cause: Product ID synced without a readable product name. Fix: sync the name field and set the Product Line Type Field. Other causes of missing product data: Product2 or Opportunity Line Item not synced, no read access to Product2, Opportunity Line Item, Opportunity; partner not sharing Opportunity data. (HC 13613493)
- Symptom: combined report type cannot be created. Causes: user lacks Manage Report Types; no mapped Partner Account. (HC 14625782)

### HubSpot

- Symptom: error during HubSpot authentication; integration not completed. Cause: Private App token missing required scopes. Fix: add all 13 scopes listed in section 10.2 via Settings, Private Apps, Crossbeam App, Auth tab, **Edit App**. (HC 7971155, HC 12158775)
- Symptom: custom object install "done" but no data. Cause: population data not configured. Fix: Customize Data in Push, select My Data and Partner Data populations, **Save Changes**. (HC 7971155)
- Symptom: cannot create custom object or lists. Causes: missing Sales Hub Enterprise (custom object) or Marketing Hub Professional (lists). (HC 7971155)
- Symptom: duplicate or stale Crossbeam Overlaps after migrating from legacy. Fix: bulk delete all Crossbeam Overlaps records (needs Bulk Delete permission) after removing the legacy integration. The legacy integration cannot be reinstalled. (HC 7971155)
- Symptom: HubSpot API limit concerns. The integration consumes some Private App API limits but batches and resumes; contact support for usage questions. (HC 7971155)
- Symptom: Company shows `NONE` under "is a customer of" or "is an open opportunity of". Meaning: no data currently connected to that field. (HC 10445323)
- Symptom: old values remain on Company records. Cause: the push never deletes existing HubSpot data; cleanup is the user's responsibility. (HC 10445323)
- Symptom: Company object fields not created. Cause: HubSpot user lacks Edit access on Company properties, or Push to HubSpot Object not toggled and saved. (HC 10445323)
- Symptom: HubSpot report shows no rows. Causes: date range left on "This quarter so far" (use **All data**); filter values not exact matches (copy population names from the report). (HC 11378668)
- Symptom: errors persist after reauthorization. Fix: wait for next sync, up to 12 hours. (HC 12158775)

### Microsoft Dynamics

- Error: `ERROR: Please back up a screen and try again.` When: custom entity creation during install. Fix: click **Previous**, then **Next**, which resets the process; contact support if it persists. (HC 10064960)
- Symptom: no opportunity data in Dynamics. Cause: opportunity fields are not currently pushed. (HC 10064960)
- Symptom: overlaps not visible on Account page or nav. Fix: configure the relationship display settings or add a Sales Hub Sub Area, then publish customizations. (HC 10064960)

### Snowflake

- Symptom: no Snowflake enable option. Cause: not included in plan. Fix: contact CSM, sales rep, or the Crossbeam support inbox (support at crossbeam.com). (HC 4694521)
- Symptom: account region not listed. Fix: contact Crossbeam to add support. (HC 4694521)
- Symptom: authorization changes or errors. Fix: **Re-authorize** in integration settings. (HC 4694521)

### Databricks

- Symptom: enable fails with a specific UI error such as missing permissions or table not found. Checks: catalog and schema exist before enabling; SP has CAN USE on the warehouse; USE CATALOG, USE SCHEMA, CREATE TABLE, MODIFY, SELECT granted. (HC 15231550)
- Symptom: auth fails with a personal access token. Cause: only Service Principal OAuth M2M is supported. (HC 15231550)
- Symptom: lost client secret. Cause: shown only once. (HC 15231550)
- Symptom: partner_ae columns empty. Fix: include a users table in the Sync integration and owner_id references on accounts, deals, and/or leads. (HC 15231550)

### Signals, webhooks, REST API

- Symptom: webhook test fails. Fix: **edit configuration** and retry until it passes; filters unavailable until a test succeeds. (HC 12732223)
- Symptom: cannot view webhook secret. Cause: shown only once after Finish. (HC 12732223)
- Symptom: cannot create webhook or API integration. Causes: not an Admin; plan (webhook requires Enterprise; API requires Supernode or higher). (HC 12732223, HC 4677142)
- Symptom: no signals for a partner. Cause: partner has no connected CRM or is not sharing Deal open date, Deal close date, Deal is closed, Deal is won. No contact fields: partner not sharing contact data. Greenfield signals unsupported. (HC 12732223)

### Slack

- Symptom: first Crossbeam org lost its Slack connection. Cause: Slack authorized from a second org. Only one at a time. (HC 3639783)
- Symptom: private or Slack Connect channel missing from dropdown. Fix: `/invite`, **Add apps to this channel**, Crossbeam. (HC 3639783)
- Symptom: contact search returns nothing. Fix: include `people` in `/crossbeam people [First Last]`. (HC 3639783)
- Symptom: owner not @mentioned. Causes: Account Owner Email not in data source, not mapped in CSV or Google Sheet, or not a list column; owner not in channel. (HC 3639783)
- Symptom: warning when routing to Slack Connect. Cause: unknown organization, partner not in the list, or multiple orgs in the channel. (HC 3639783)
- Symptom: partner owner not shown in Slack. Expected; use Salesforce custom object reports or related lists (Supernode). (HC 3639783)

### Clay, PartnerStack, Marketo, Matillion

- Clay: requires Crossbeam Supernode and Clay Pro; one partner per source; configure partners and Populations in Crossbeam first. (HC 10080441)
- PartnerStack: installer must be a PartnerStack Admin; if the PartnerStack column is missing, add it via Columns. Reauthorize via the three dots on the Installed Integrations row. (HC 8533576)
- Marketo: requires Salesforce as a data source and a Marketo Admin; endpoint must exclude trailing `/rest`; data may take up to 10 minutes after initial sync; set a processing date so all persons appear in Program Members. (HC 8575980, HC 8801394)
- Matillion: connector issues go to Matillion support, not Crossbeam. (HC 5206786)

### AI Agents

- Symptom: Agent did not fire. Causes: match existed before the Agent was created; partner not sharing data; required CRM fields not synced (opportunity triggers); Agent disabled; Slack connection needs reauthorization (run skipped). (HC 15961519)
- Symptom: cannot save Agent. Cause: must **Test Agent** first. Cannot create: need full-access seat and Manage permission; Slack must be connected. (HC 15961519)

### Record Exports (all push integrations)

- Symptom: insights stopped flowing into external tools. Cause: Export Limit reached. Fix: monitor at app.crossbeam.com/billing; reduce pushed populations or opportunity data. (HC 4694521, HC 7971155, HC 9280237, HC 14463181)
