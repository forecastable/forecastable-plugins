<!-- Library file for crossbeam-admin-reference.md. Source: Crossbeam Help Center, extracted September 25th, 2026. Cite (HC number); confirm in-app when a screen may have moved. -->

# Crossbeam Admin Reference C: Account Mapping Lists, Analysis Metrics, AI Hub (MCP), Release Notes, Video Tutorials

Source: 48 Crossbeam Help Center articles (group C), cited as (HC nnnnnnn). Conflicts are flagged. Anything not in the articles is labeled "Derived".

---

## 0. Quick orientation for Eva

- "Account Mapping Reports" no longer exist as a name. They were redesigned into **Lists** (first shipped 12/10/2025 as the "Account Mapping Reports Redesign", then fully launched as the "New Lists Experience" in the 02/11/2026 release). Saved Reports, Shared Lists, and Ecosystem Reports were consolidated into Lists. Old "Shared Lists" are now called **Static Lists**. (HC 11801904, HC 13688795, HC 13017615, HC 13613176)
- Two main entry points: **Account Mapping** (left nav, `https://app.crossbeam.com/account-mapping`) shows the full ecosystem-wide overlap List; **Lists** (left nav, `https://app.crossbeam.com/lists`) is the **Lists Hub** holding every List, including historical ones. (HC 13688795, HC 11801904)
- The Account Mapping Matrix lives on each partner's **Partner Detail Page** (Partners page, click partner icon or name). (HC 5303061)
- Credit limits on the Crossbeam MCP server are enforced on all plans starting **September 1, 2026**. (HC 15588582)

---

## 1. Plans, seats, and roles relevant to Lists and analysis

### 1.1 Plan gates (collected)

| Capability | Free / Explorer | Connector | Supernode | Enterprise | Source |
|---|---|---|---|---|---|
| View Account Mapping List | Up to 10 records (see conflict note) | Yes | Yes | Yes | HC 13688795 |
| Create / edit / save Lists | No | Yes | Yes | Yes | HC 13688795 |
| Internal List sharing, Notes collaboration | No | Yes | Yes | Yes | HC 13688795 |
| Export Lists | Only via Account Mapping Pass (1:1 mapping) | Yes, max 1,000 rows per List export | Unlimited record exports | Yes | HC 13688795, HC 8195191, HC 8195206 |
| Single Partner List | Yes (Explorer) | Yes | Yes | n/a stated | HC 8195191 |
| Custom List | No | Yes | Yes | n/a stated | HC 8195206 |
| Greenfield Lists and Greenfield sharing | No (paid plans only; not via AMP) | Yes | Yes | Yes | HC 10592414 |
| List Notifications | No | Yes | Yes | n/a stated | HC 3640085 |
| Dynamic Shared List (external) | View and contribute only when shared by a paid partner | Yes | Yes | Yes | HC 14489383, HC 8195191 |
| Potential Revenue configuration | View only | Yes | Yes | n/a stated | HC 6797349, HC 5303061 |
| Partner Score | No | Yes | Yes | Yes | HC 9204052 |
| Deal Navigator | Limited rows for full-access users | Full access for full-access seat users (Opportunity Owner filter) | Full access for Sales Seat users, also inside Salesforce | n/a stated | HC 10844915 |
| Pipeline Generation | Limited rows | Full access for Sales Manager seat users | Full access for Sales Seat users, also in Salesforce | n/a stated | HC 11420734 |
| Net New Accounts view | No access | Yes | Yes | Yes plus Net New Accounts webhook | HC 14463832 |
| Performance Dashboard | No | No | Yes (Full Access seat only) | n/a stated | HC 10845010, HC 11509867 |
| Issue Account Mapping Passes | No | No (cannot buy either) | Yes, automatic | Yes, automatic | HC 10592414 |
| MCP credits per year | 50 | 500 | 2,500 | 5,000 | HC 15588582 |
| Buy credit packs | No | No | Yes | Yes | HC 15588582 |

**Conflict flags:**
- Free plan record view limit: HC 13688795 says "View up to 10 records" for the Account Mapping List. HC 5303061, HC 3162265, and the AMP table in HC 10592414 say the Matrix and Lists display a maximum of **50 records** (effective March 4, 2025). Treat the Lists-era table (10) as newer but confirm in-app.
- Connector exports: HC 8195191/8195206/8195198 say Connector List exports are limited to **1,000 rows** (per export). HC 10592414 lists Connector record exports as **5,000 records / year**. Both limits may apply (per-export and annual).

### 1.2 Seat facts

- Free (Explorer) and AMP holders: 3 Full Access seats included. Connector: starts at 1 paid seat. (HC 10592414)
- Sales seat users can view, edit, and comment on Lists **shared with them**; cannot create Lists; cannot share Lists; have access to Deal Navigator and Pipeline Generation. (HC 13688795, HC 11801904)
- Legacy Connector sales seat users have access to Deal Navigator and Pipeline Generation. (HC 10844915, HC 11420734)
- Sales Seat with a **Manager role** can view ALL opportunities in the org in Deal Navigator and filter by opportunity owner. (HC 10844915)
- Performance Dashboard requires a Full Access seat; not available to Sales seats. (HC 10845010)
- MCP requires a Full Access or Sales seat. (HC 15588582)
- **Integration Seat** (GA 08/19/2026, Supernode and Enterprise): dedicated seat type scoped to CRM connections, data sources, and outbound integrations. One Integration User included per organization; it does not count toward your seat limit. (HC 16075353)
- Sales Seat users were redirected from `sales.crossbeam.com` to `app.crossbeam.com` (06/10/2025). (HC 11509867)

### 1.3 List access roles and access levels

Crossbeam role to available List access levels (HC 13688795, HC 11801904):

| Crossbeam role | Available List access |
|---|---|
| Admin | Manage, Edit, Comment, View only |
| Standard | Manage, Edit, Comment, View only |
| Limited | View only |

Access level capabilities:

| Level (also written Manager/Editor/Commenter/Viewer in HC 3160236) | Can do |
|---|---|
| Manage | Create, edit, delete, add Notes, share the List |
| Edit | Create, edit, delete, add Notes |
| Comment | View List, add Notes |
| View only | View List, including definitions and results |

Default permissions (HC 13688795):
- Full Access seats: Admin gets Manage on Lists and on Partner Shared Lists (externally shared Lists). Standard User gets Manage on both. Limited User gets View only on Lists and no access to Partner Shared Lists.
- Sales seats: Edit on Lists; no access to Partner Shared Lists.
- Admins have Edit access to all Lists by default, whether or not explicitly shared. (HC 3160236, HC 11801904)
- HC 11801904 also states: users with Standard and Manager Crossbeam access have Editor access in Shared Lists; Editors can edit, delete, and add team members to existing Lists; Limited users have View Only in Shared Lists. (Note: this conflicts slightly with HC 13688795, which gives Standard users Manage by default.)
- To change someone's access: open the List, click **Share**, remove them or update their access level. (HC 11801904)

---

## 2. The Lists experience

### 2.1 What Lists are

- Lists let you create, organize, and collaborate on dynamic or highly segmented sets of accounts and leads in one place. They consolidate Saved Reports, Shared Lists, and Account Mapping Reports. (HC 11801904)
- Capabilities: build targeted Lists for internal collaboration or external sharing; pre-defined **System Lists** for ecosystem visibility, opportunities, or prospects; filter, sort, customize; Notes and notifications; Dynamic vs Static tracking. (HC 13688795, HC 11801904)

### 2.2 Lists Hub

Path: left nav **Lists** (`https://app.crossbeam.com/lists`). (HC 3160236)
- Views: **All Lists**, **Your Lists**, **Lists shared with you**.
- **New** button: create a new List or start from a pre-built System List.
- Filter Lists by **Partner Overlaps** or **Owner**.
- Search bar finds a List by name.
- Organize Lists into folders.
- Hover the **Shared With** column to see who has access. If shared with all, the organization name appears in that column. (HC 11801904)
- Bell icon in a List row sets notifications without opening the List. (HC 3640085, HC 8195198)
- Folder sort order: by creation date and most recent changes by the user, so newly created and recently renamed folders appear first. (HC 11801904)

Folders (HC 3160236):
1. Check the box next to one or more Lists. The **Action** button appears.
2. Click **Action**, choose an existing folder or **New Folder**.
3. To delete a folder: open it, click the edit (pencil) icon, select **Delete Folder**.

### 2.3 Dynamic vs Static Lists

- Lists are **dynamic by default**: they update automatically as accounts enter or leave the filter criteria. (HC 3160236, HC 8195191)
- **Dynamic Shared List** (Connector and Supernode; release notes also list Enterprise): share a Dynamic List externally with a partner so both sides see the same updating accounts. Both sides control column visibility and collaborate using Notes. **Filters lock at the time of sharing.** Free users can view and contribute to Lists shared with them. (HC 8195191, HC 14489383)
- 06/17/2026 update: users can apply **AND** filter logic on top of existing filters on a Dynamically Shared List to narrow their own view without affecting what others see, and can share a List with the entire organization in one action in addition to per-user sharing. (HC 15303766)
- **Static Lists**: your current externally Shared Lists; a fixed set of accounts that do not update when new accounts match criteria. Can be shared externally; account set stays fixed until manually updated. Historical Shared Lists are accessible in the Lists Hub and are static. (HC 11801904, HC 8195191)
- External sharing of dynamic Lists was in beta at one point: sign up at `https://app.crossbeam.com/labs`. (HC 11801904)

### 2.4 Privacy defaults and ownership

- Newly created Lists are **private by default**. The user who saves the List becomes the List owner. (HC 8195191)
- New saved Lists are visible only to the creator and admins until shared. (HC 11801904)
- All historical Reports (now Lists) created **before December 10, 2025** keep access for everyone in the organization. (HC 11801904, HC 8195198)

### 2.5 Common List workflow (applies to all List types)

**Configure Columns** (HC 8195191, HC 3160236, HC 13688795):
1. Click **Configure Columns** (called **Columns** in the Account Mapping List).
2. Expand **Your Data** and **Partner Data** (Custom and Greenfield Lists show **Your Data** only).
3. Check boxes to add or remove data.
4. **Organize Columns** area: rearrange or remove columns. In the Account Mapping List, under **Select Columns**, expand and adjust the current columns.
5. Click **Save**.
- Scroll horizontally to see more columns, including detailed partner overlap indicators. (HC 13688795)
- The old single Overlaps column is split into **Is a Prospect of**, **Is an Opportunity for**, and **Is a Customer of** where applicable. (HC 11801904)

**Filters** (HC 3160236, HC 8195191):
1. Click **Filters** (or **Filter**).
2. Select a data source: **Crossbeam** (My Populations, Partner Populations, or Partner Tags) or a **specific CRM** (its available fields).
3. Click **Apply**.
4. For granular filtering: open an applied filter, click **Convert to Advanced Filter**. Use comparison operators such as `is`, `is not`, `is empty`, `contains`; add object fields on Account, User, or Opportunity; edit and **Apply**.
- You can also filter from a column header arrow.
- Greenfield Lists use **+Add Filter**, pick a field, set operators, **Apply**. (HC 8195198)
- As long as a field exists in your data, you can filter on it. (HC 3160236)
- 04/15/2026 improvements: OR logic between segments, filter on specific Populations under "My Population", "Select all" for partners in filters, only actively used data sources shown in the multi-CRM filter dropdown. (HC 14489383)
- Account Mapping List: filter by **Select partner score** dropdown. (HC 9204052)

**Sorting**: column header arrows or the **Sort** button, Ascending or Descending. Combine with filters. (HC 3160236)

**Save**: after filters, columns, sorting, click **Save as a new list**. Then **Action** gives Notifications, Export, Duplicate, Delete (and Edit per HC 11801904). (HC 8195191)

**Share** (HC 3160236):
- The Share button is **disabled until the List is saved**.
- Click **Share**, add name or email, click **Share**, set access level.
- 04/15/2026: bulk List sharing added. (HC 14489383)

**Notes** (HC 3160236, HC 11801904):
- Available in all Lists; click in the **Note** column to add.
- List-specific: Note history stays in that List and does not follow the account or opportunity to other Lists.
- Users with Manage, Edit, or Comment access can add Notes. Reply to existing Notes supported.
- Unread Notes appear bolded; read Notes are not.
- Notes are included in List exports.
- Clicking a Note opens the Notes section of the Account Details Drawer.
- Notes in (internal) Lists are available only to your internal organization. (Dynamic Shared Lists allow Notes with partners, HC 14489383.)
- 04/15/2026: Notes column sorting by recency. (HC 14489383)

**Note notifications** (HC 3160236, HC 11801904):
- Sent when someone adds a Note or mentions you.
- Admin and non-admin core users: activity in all Lists they have been added to.
- Sales users: only activity in (private) Lists they have access to.
- Delivered as in-app and email alerts.

**Account Detail Drawer**: click any account to open it. View Partner Impact and partner-level context, partner overlaps, contacts, activity, Notes, and take action without leaving the List. Partner Score tag shows for displayed partners. (HC 8195191, HC 9204052)

### 2.6 Export, duplicate, delete

- Export: in the List, **Action** > **Export**. An email notifies you when complete; click **Download Export** in the email. (HC 3160236)
- Use filters before exporting to stay within record export limits. Consider List notifications instead of repeated exports. (HC 3160236)
- Duplicate or Delete: **Action** > **Duplicate** or **Delete**, confirm. **Deleting a List is permanent and cannot be undone.** (HC 3160236)
- Explorer plan: effective **March 4, 2025**, the Free Explorer plan no longer supports record exports. Free Explorer customers from before March 4, 2025 kept export functionality until **July 1, 2025**. (HC 3160236)

---

## 3. List types

### 3.1 Account Mapping List (ecosystem-wide)

- Path: left nav **Account Mapping** (`https://app.crossbeam.com/account-mapping`). A 360-degree list view of account overlaps across your entire partner ecosystem, refined into focused Lists. (HC 13688795)
- Steps: start from the full List, **Filter** > **Crossbeam** (Populations, Partner Tags), refine; click the quick filter > **Convert to Advanced Filter** to layer your data and partner data fields; **Sort**; **Columns**; **Save as a new list**. (HC 13688795)
- Launched as beta 11/6/2025, GA with the New Lists Experience 02/11/2026. (HC 12674444, HC 13613176)
- The Account Mapping Pass applies only to 1:1 Account Mapping, not to Account Mapping Lists. (HC 13688795)
- Free accounts can only access full Lists when shared by a paid partner. (HC 13688795)

### 3.2 Single Partner List (Standard Account Mapping)

- Plans: Explorer, Connector, Supernode. Saving a List or notifications requires Connector or Supernode. (HC 8195191)
- Create: **Lists** > **+New** > **Single Partner**. In the Create List modal: select the Partner, click an overlap box in the matrix, click **Create List**. (HC 8195191)
- Columns: Your Data and Partner Data. (HC 8195191)

### 3.3 Custom List (Advanced Account Mapping)

- Plans: Connector and Supernode. (HC 8195206)
- Create: **Lists** > **+New** > **Custom**. Select your Population(s); select each Partner(s) and Population(s) from dropdowns; **Create List**. (HC 8195206)
- Columns: Your Data. (HC 8195206)

### 3.4 Greenfield List (Advanced Account Mapping)

- Purpose: identify **non-overlapping** accounts with partners for joint campaigns. Includes region, tier, health score, industry, employee count, revenue. (HC 8195198)
- Check the **Sharing Dashboard** before adjusting sharing settings. (HC 8195198)
- Paid plans only; not available through an Account Mapping Pass. (HC 10592414)
- Create: **Lists** > **+New** > **Greenfield**, then pick one of two options (HC 8195198):
  - **New Accounts for You**: accounts in your Partner's Populations that are not in your Populations. Steps: select New Accounts for You, select Partner, check Partner Population(s), select Your Populations, **Create List**.
  - **New Accounts for your partner**: accounts in your Populations that are not in your Partner's Populations. Steps: check your Population(s), select Partner from dropdown, check Partner Population(s), **Create List**.
- Filters: **+Add Filter**, field, comparison operators, **Apply**. (HC 8195198)
- **Greenfield List Notifications**: alert you when a partner record is added to the Population in the **New Accounts for You** List. Turn on/off: Lists Hub, search for the List, click the **bell** icon in the row, enter email(s) and Slack channel(s), **Save Preferences**. (HC 8195198)
- Exports: Connector limited to 1,000 rows; Supernode unlimited. (HC 8195198)

### 3.5 System Lists

- Pre-defined Lists for ecosystem visibility, opportunities, or prospects, started from the **New** button in the Lists Hub. (HC 13688795, HC 11801904)

---

## 4. List Notifications (email and Slack)

- Plan: Connector or Supernode. (HC 3640085)
- Setup: open a saved List > **Action** > **Notifications**, or click the **bell icon** in the List row in the Lists Hub. (HC 3640085)
- **Email**: enter any email address, including non-Crossbeam users; unlimited count. (HC 3640085)
- **Slack**: choose public channels, private channels, Slack Connect public channels, Slack Connect private channels. Private channels (regular and Slack Connect) appear only if the Crossbeam app has been invited: type `/invite`, choose **Add apps to this channel**, select **Crossbeam**. (HC 3640085)
- If Slack is not connected, a **Connect to Slack** button shows instead of the channel dropdown. (HC 3640085)
- Frequency: every **four hours**. (HC 3640085)
- Slack message contents: account name and website, account overlaps, your Account Owner's name, Account Owner Slack username (if mentions enabled), link to the account and List. (HC 3640085)

**Mentioning Account Owners in Slack** (HC 3640085), all must be true:
- CRM data source includes **Account Owner Name** and **Account Owner Email**.
- CSV or Google Sheet data source maps the **Account Owner Email** column.
- The List includes both Account Owner Name and Account Owner Email as columns.
- If only Name (no Email) is in the List, Slack shows the name but does not tag the user.
- If the owner is not in the channel, they are not alerted, but the name is still mentioned so others can add them.

**Slack Connect safety** (HC 3640085):
- Slack notifications are visible to everyone in the channel. Do not send a List for one partner into a shared channel containing a different partner.
- Crossbeam flags channels that include an unknown organization, contain a partner not included in the List, or have multiple organizations.

---

## 5. Account Mapping Matrix

- Location: **Partners** (`https://app.crossbeam.com/partners`) > click a partner icon or name > Partner Detail Page. (HC 5303061)
- Layout: your Populations (Standard and Custom) in the left column; partner's Populations (Standard and Custom) in the top row. (HC 5303061)
- **Blue boxes**: number of shared-data overlaps. Click the overlap count to open a pre-generated List of overlapping accounts; then configure columns, filter, sort, save, share, export, set notifications. (HC 5303061)
- **White boxes**: data not shared; you only see the overlap count. Click the white box > **Request Data** to ask the partner for more sharing. (HC 5303061)
- Clicking a cell loads all accounts across every Population in that category. To drill into one Population, use the expand icon on the row or column header and pick the Population type. (HC 5303061)
- Since 11/6/2025, Population Types (customers, open opportunities, prospects) can be assigned to custom Populations, and the Matrix reflects those types. (HC 12674444)
- Two views via dropdown: **Total Overlaps** and **Potential Revenue**. (HC 6797349, HC 5303061)
- Free Explorer: Matrix and Lists display a maximum of 50 records from March 4, 2025 (pre-March 4 Explorer customers kept functionality until July 1, 2025). (HC 5303061, HC 3162265)

---

## 6. Account Mapping Pass (AMP) and the Free plan

- AMP is included in Supernode and Enterprise plans and gives your Free partners full Account Mapping and overlap visibility with your org, plus exports up to **100 records at a time** (with that partner only). (HC 10592414)
- Automatic since **March 4, 2025**, distributed to all existing Free partners that day and to future Free partners. Nothing to activate. (HC 10592414)
- Supernode/Enterprise customers cannot choose which Free partners get a Pass; all do. Free users cannot request one. Connector customers cannot purchase or add one. (HC 10592414)
- Free users can hold multiple Passes from different Supernode/Enterprise partners, and see **Account Mapping Pass badges** in select areas of the app. (HC 10592414)
- Supernode/Enterprise customers see their unlocked Passes on the **Billing** page. (HC 10592414)
- AMP does not upgrade the Free plan; it expands visibility and exports within that one relationship. (HC 10592414)
- AMP does not grant Greenfield Lists or Greenfield sharing. (HC 10592414)
- AMP applies only to 1:1 Account Mapping, not Account Mapping Lists. (HC 13688795)
- Notice: participation lets Crossbeam share aggregated insights about your partnership and engagement with the accounts that provide the Pass. (HC 10592414)

AMP comparison (HC 10592414):

| Feature | Free (Explorer) | With AMP | Connector |
|---|---|---|---|
| Overlap visibility | Up to 50 records | Full detail with granting partner | Full, all partners |
| Record exports | None | Up to 100 per export, that partner only | 5,000 records / year |
| Create and save Lists | No | No | Yes |
| View Lists shared by paying partner | Yes | Yes | Yes |
| Can issue Passes | No | No | No |
| Full Access seats | 3 | 3 | Starts at 1 paid seat |

---

## 7. Record-level views

### 7.1 Record Detail Page

- Open via **Search** in the navigator bar. (HC 3188944)
- Shows: **Account Information** (all fields synced from your data source: CRM, CSV, Snowflake, per your selected sync fields); **Activity Timeline** (when overlaps were created or updated, partner data changes); **Ecosystem Context** (the record's Populations such as Customers, Open Opportunities, Prospects, Custom; plus partner-shared data on the same record). (HC 3188944)
- **Share with Partner** button at top adds the record to a Static List. (HC 3188944)

### 7.2 Account Detail Drawer tabs (Deal Navigator and Pipeline Generation)

- **Account** tab: key partner insights and company info. (HC 10844915)
- **Partners** tab: **Message** button to request warm intros or align on deal strategy. (HC 10844915)
- **Contact** tab: partner-surfaced contacts with context from number of shared partners and partner activity; Ecosystem Intelligence signals indicate likely decision makers or recent activity with your partner. (HC 10844915, HC 11420734)

---

## 8. How overlap numbers are calculated

### 8.1 Why your count differs from your partner's

- Crossbeam comparisons act as an **inner join**: records only show when there is a match on both sides. (HC 3431068)
- Results are always expressed in terms of **your data** (root data). If you have 1,000 accounts, you see how many of your 1,000 match, even many-to-one. Example: you see 4 matches, partner sees 3, because one of their accounts matched two of yours. (HC 3431068)
- Crossbeam does **no data cleansing**. Duplicates in your CRM or file each count on your side; your partner sees one match per their account. (HC 3431068)
- Crossbeam deliberately does not merge duplicates because they are often different divisions or locations of the same company. (HC 3431068)
- Fix: de-dupe the CRM or file before comparison, or use advanced population filters to weed out duplicates. (HC 3431068)

### 8.2 Matching inputs

- **DUNS matching** (beta, 02/04/2025): adds precision when both sides have DUNS. (HC 10375251)
- **Smarter Matching** (11/6/2025): goes beyond domains and names using multiple attributes including DUNS, phone numbers, and marketplaces. (HC 12674444)

---

## 9. Potential Revenue

- Plans: Connector and Supernode configure; Explorer is view only (calculation only, no Revenue Settings). (HC 6797349)
- Currency: all deal amounts converted to USD at **current** exchange rates, not rates at deal close. (HC 6797349)
- Where: Partner Detail Page (hover **Potential Revenue** > **Go to Revenue Settings**) or the **Settings** icon in the nav, then **Potential Revenue Settings**. (HC 6797349)
- Matrix view definition: the dollar amount of your open opportunities that overlap with your partner's accounts. (HC 6797349)

**Calculation** (HC 6797349):
- Sum of **open opportunity amount** values in each Population.
- An opportunity counts when **deal is closed = false** AND **amount > 0**.
- The partner-level total is **not** the sum of the 1:1 Matrix cells, because opportunities can exist in multiple Populations; summing cells would double count.
- Default field is open opportunity amount. To use a different opportunity field, pick it on the Settings page (`https://app.crossbeam.com/organization/settings`) via the Potential Revenue field dropdown. Only fields you currently sync appear.

**Configure Populations included** (global setting, applies to all partners) (HC 6797349):
- Your Populations: Your Customers, Your Open Opportunities, Your Prospects, All Custom Populations.
- Partner Populations: Partner Customers, Partner Open Opportunities, Partner Prospects, All Custom Populations.
- Click **Save Settings**. It may take a few minutes for numbers to update.

**Requirements to see Potential Revenue in the Matrix** (HC 6797349):
- CRM connected as data source, syncing opportunity **amount** and **deal is closed** (or use the Crossbeam **Pipeline Mapping Preset**).
- You share overlap counts for at least one Population.
- At least one partner Population shares data with you.
- Paid plan (Connector or Supernode).
- CSV or Google Sheet sources do not populate Potential Revenue.

**Interpretation by Matrix cell** (HC 6797349):
- Your Customers x Partner Customers: upgrade or renewal revenue potential.
- Your Open Opps x Partner Customers: get partner intel on buying and procurement, decision makers, a good word.
- Your Customers x Partner Open Opps: reciprocity, help partner's deals.
- Your Open Opps x Partner Open Opps: co-selling potential on accounts both are working.
- Also: vet new partners, pick focus partners, justify investment, instant data-backed ROI analysis.

---

## 10. Partner Score and Partner Impact

### 10.1 Definition

- Partner Score is Crossbeam's unified signal of relationship strength. Labels: **High** (green), **Medium** (yellow), **Low** (red), **None**, **Unknown**. (HC 9204052)
- Plans: Connector, Supernode, Enterprise. Released 04/15/2026. (HC 9204052, HC 14489383)

### 10.2 Calculation (HC 9204052)

- Per partner, per org, rolling **365 days**.
- Input 1, **Pipeline Impact**: how your pipeline performs on accounts that are already customers of that partner, measured by **win rate**, **average opportunity size**, **average time to close**. Each is compared against your **without-partner baseline**, combined into an aggregate score; partners are then ranked within your network by **percentile distribution**.
- Input 2, **Coverage Percentage**: what share of your total partner overlap pool that partner accounts for (higher means more of your overlapping customers and open opportunities are covered).
- Measures performance when selling to a partner's customers, **not** partner involvement in the deal. High means that partner's customer base correlates with better outcomes regardless of co-sell.
- Partner Impact on the Partner Detail Page aggregates Win Rate, Opportunity Size, and Time to Close into a percentile distribution; shows only if enough data. (HC 6797349)
- Deal amounts use USD at current exchange rates. (HC 9204052)

Label meanings:
- High: strong pipeline performance with that partner's customers and strong coverage.
- Medium: moderate performance or coverage.
- Low: limited performance and low coverage.
- None: calculated, but not enough overlapping closed-won history.
- Unknown: could not be calculated due to a data gap.

### 10.3 Requirements (all must be true) (HC 9204052)

- Connector, Supernode, or Enterprise plan.
- Your org has a **Customers Population**.
- Partner has a Customers Population and shares data with you (partner does not need a CRM).
- Your org has a **CRM** connected (CSV-only orgs cannot get a score; CSVs lack deal data).
- Required CRM fields synced: **Deal Stage, Deal Name, Deal Amount, Close Date, Open Date, Is Won, Is Closed** (names vary by CRM).
- At least **10 overlapping closed-won deals** with that partner in the past 365 days.

### 10.4 Where Partner Score appears (HC 9204052)

- **Partners** > **Partner List**: **Quick Filter** > **Partner Score** to sort; hover or click tag to open Partner Detail.
- Partner Detail Page: Partner Score tag.
- Account Mapping (`/reports/account-mapping`): **Select partner score** dropdown.
- Account drawer in a List row.
- **Pipeline Generation**: primary input for partner recommendations. Accounts overlapping multiple High Score partners are flagged as top prospects at the top with a fire icon.
- **Deal Navigator**: shown alongside partner recommendations, but recommendations are based primarily on recent deal signals, not Partner Score. A Medium or Low partner can still be recommended.
- **Performance Dashboard** > **Partners** tab: Partner Leaderboard has a Partner Score column; sort dropdown **Highest Partner Score**; hover a score for the breakdown (win rate, avg opportunity size, avg time to close, coverage %, each vs baseline).
- **Crossbeam Copilot**: **Partner** tab; click the Partner box for Overlap Detail. Copilot integrates with Salesforce, HubSpot, Chrome, Outreach, Gong.
- **Crossbeam MCP (beta)**: Partner Score data is returned to AI assistants, for prompts like "Who are my top partners?" and "Which partners should I prioritize this quarter?"

---

## 11. Deal Navigator

- Path: left nav **Deal Navigator** (`https://app.crossbeam.com/deal-navigator/close-deals`). A table of open opportunities overlapping your partners' customers. Does **not** rely on Populations. (HC 10844915)
- Open Opportunity definition: **Closed = false**, excluding test data (record domain matches its own domain), close dates more than a year out, amounts less than 0. (HC 10844915)

**Top Opportunities smart sort** (HC 10844915):
- Deal Size: larger first.
- Close Date: prioritized if expected close within the next **14 days**.
- Stage and Activity: late-stage deals with no activity in the past **3 days** surfaced.

**Ecosystem Intelligence signals for recommended partners** (HC 10844915):
- **Recent Wins**: partner closed a deal with the account in the last 3 months.
- **New Contacts**: partner added 1+ new contacts at the opportunity level.
- **Long-Term Relationship**: partner has had the account as a customer for 2+ years.
- **Missing Contacts**: partner has key contacts not in your CRM.
- **Crossbeam Activity**: partner has recent engagement on Crossbeam.

**Filters**: Stage, Deal Size, Close Date, Partner, Opportunity Owner (Sales Managers only). (HC 10844915)

**Actions**: Action icon or click Account row opens the Account Detail Drawer; **Add to Shared List** action icon for team follow-up. (HC 10844915)

**Export** (Connector and Supernode, added 06/17/2026) (HC 10844915, HC 15303766):
1. **Action** > **Export**.
2. Review the number of records (counts toward your org's Record Export limit).
3. **Export Data**. Email notifies when ready.

**Fields to sync** (HC 10844915):
- Required: Account Owner Name (`user`/`user_name`), Account ID (`company_key`), Account Name (`company_name`), Deal Name (`deal_name`), Is Closed (`deal_is_closed`), Deal Owner ID (`deal_owner_id`).
- Recommended: Deal Amount (`deal_amount`), Deal Closed Date (`deal_close_date`), Deal Stage (`deal_stage`), Contacts.
- If a custom amount field is set in **Settings > Organization Settings**, Deal Navigator uses it.

**Salesforce tab** (HC 10844915):
- Reports and dashboards features require the Salesforce custom object enabled.
- Crossbeam app access to Deal Navigator still requires a Crossbeam user seat.
- Set up the Crossbeam tab in Salesforce; open it via the icon next to settings in Crossbeam Copilot for Salesforce.

---

## 12. Pipeline Generation and Net New Accounts

### 12.1 Pipeline Generation

- Path: left nav **Pipeline Generation** (`https://app.crossbeam.com/generate-pipeline`). Surfaces **Top Prospects**: net-new accounts that overlap with partners and match your ICP. Originally "Generate Pipeline in Deal Navigator" (beta 06/10/2025, released 08/05/2025); got its own nav entry 02/11/2026. (HC 11420734, HC 11509867, HC 11786254, HC 13613176)
- Default view **Sort by Top Prospects**. Filters: Account Owner, Industry, Number of Employees, Recent Partner Customer, Partners, Country. (HC 11420734)
- Alternate view **Sort by Recent Partner Customer**: prospects that recently became partner customers (strong buying intent); most recent partners first in the **Is a customer of** column. (HC 11420734)
- **Top Prospect** definition: overlaps with at least one high-impact partner; sorted by number of partner overlaps. (HC 11420734) Partner Score is the primary input; multiple High Score overlaps get the fire icon. (HC 9204052)
- Row actions: view record in CRM, message a partner, add to Shared List; click row for Account Detail Drawer. (HC 11420734)
- Actions list: Open in CRM, Assign in CRM, Add to CRM, Request Partner Introduction. (HC 11420734)
- Does **not** use the **Lead** object. (HC 11420734)
- ICP filter requirements (sync from CRM): Industry, Company Size / Number of Employees (if available), Geography (Country), Account Owner. (HC 11420734)

### 12.2 Three account categories (HC 14463832)

- **Prospects in Your Populations**: your prospects that are customers of at least one partner. Filter **My Populations > Prospects**.
- **Not in any Population (Greenfield)**: not in any of your Populations, customer of at least one partner. Filter **Not in My Populations**.
- **Net New Accounts**: do not exist in your CRM at all, customer of at least one partner. Toggle **Net New Accounts** at the top of the list.

### 12.3 Net New Accounts

- Plans: Free none; Connector and Supernode full view; Enterprise view plus webhook. (HC 14463832)
- Seat access: Full Access seats and Sales seats with Manager permissions can view all. (HC 14463832)
- Requirement: at least one connected partner has **Greenfield sharing (All Accounts)** enabled. (HC 14463832)
- Request it: **Partners** > click partner > settings > **Shared with You** tab > **Request Data** next to the Population > message asking for sharing level **All Accounts** > **Send Request**. (HC 14463832)
- Act: **Export** to route to reps or BDRs. **Add to CRM** is not yet available for accounts not in your CRM. (HC 14463832)

**Net New Accounts webhook (Enterprise only)** (HC 14463832):
- Pushes accounts to Salesforce, HubSpot, Outreach, or any connected destination when a partner closes a deal on an account not in your CRM.
- Create: Pipeline Generation > **Create Webhook** (top left) > Integrations page > **Select Events** dropdown > **Deal Closed-Won** > complete setup > in webhook settings (`https://app.crossbeam.com/integrations`), under **Customize Data in Push**, check **Net New Accounts** > **Save Settings**.
- Edit existing Deal Closed-Won webhook: Integrations > **Settings** next to webhook > check **Net New Accounts** under Customize Data in Push > save. No need for a new webhook.

---

## 13. Performance Dashboard

- Plan: Supernode. Full Access seat required; not for Sales seats. Data source must be a CRM. (HC 10845010)
- Path: left nav **Performance**. Four tabs: **Open** (Generated Pipeline and Open Opportunities), **Closed** (Closed-Won), **Team** (Team Engagement), **Partner** (Partner Performance). Each tab has its own filters and sorting (for example quarter and opportunity owner). (HC 10845010)
- Required CRM fields: Deal Amount, Deal Close Date, Deal Is Closed, Deal Is Won, Deal Name, Deal Open Date, Deal Owner ID. Missing fields produce empty metrics and a prompt to update data source settings. (HC 10845010)

**Org settings** (HC 10845010):
- Preferred CRM: **Settings** > **Organizational Settings** > General Settings > **What CRM do you use?**
- Fiscal year: same place > **What is your fiscal year?** The timeframe applies to Closed-Won Opportunities, Team Engagement, Missed Opportunities, Partner Leaderboard; changing it in one updates all four. **Save Changes**.
- New vs Existing Business: **Data Sources** > open CRM data source settings > **Field Mapping** > adjust the New Business / Existing Business mapping.

**Definitions** (HC 10845010):
- **Coverage**: the opportunity overlaps with at least one partner's customer Population.
- **Engagement**: the opportunity has at least one engagement activity. Activities: messages sent or received in Copilot or Crossbeam for Salesforce; partner mentions on Gong recordings; Copilot contacts added to CRM; Notes created/updated on a shared list; research activity in Copilot (account or contacts); leads sent to PartnerStack; attribution created; records added to a list.

**Open tab, Generated Pipeline (EQL metrics)** (HC 10845010):

| Metric | Calculation | Data source |
|---|---|---|
| Ecosystem Qualified Leads (EQLs) | Count of accounts in the Generate Pipeline table that are not currently open opportunities and have 1+ partner overlap | CRM plus Crossbeam partner data |
| EQLs with Engagement | EQLs with 1+ engagement activity (viewed in CRM, opened account drawer, added to list, partner interaction) | User activity logs plus Copilot integrations |
| EQLs Converted to Opportunities (Opened Opportunities) | Count of EQLs appearing in Open Opportunities table | CRM opportunity data |
| Closed-Won Opportunities from EQLs | Closed deals linked to EQL source account | CRM opportunity stages |
| Revenue from EQLs | Sum of Deal Amount for Closed-Won opps tied to EQLs | CRM opportunity data |

**Open tab, Open Opportunities** (HC 10845010):
- **Current Coverage**: % and count of open opps with 1+ partner overlap (for example "78 of 100").
- **Coverage Value**: total USD of opps with overlap (multi-currency converted at current rate).
- **Current Engagement**: % and count of open opps with 1+ ecosystem engagement while open, out of all open opps in CRM.
- Metric card arrows open Deal Navigator; counts may differ from Deal Navigator due to different sync schedules.

**Closed tab** (HC 10845010):
- Toggle **Coverage View** (with vs without overlap: avg deal size, win rate, time to close) and **Engagement View** (with vs without engagement).
- Basis: Is Closed = true, Is Won = true, Close Date in timeframe.
- Total Closed-Won bar split: With engagement; With coverage, no engagement; No coverage. Bar percentages are rounded and represent **% of total deal value**, not count.
- **Missed Opportunities**: Closed-Lost Opportunities with Coverage (overlap but no engagement), Value of Missed Opportunities (USD), Reps Who Didn't Engage. Basis: Is Closed = true, Is Won = false, close date in timeframe. Table: Opportunity Name, Owner, Amount, Close-lost Date, partners that had the account as a customer while the opp was open. Click row for account drawer.

**Team tab** (HC 10845010; expanded 12/10/2025 per HC 13017615):
- Filters: Timeframe, Opportunity owner.
- Number of Engagement Events (all records, all users); Number of Users with Engagement; % of Users with Engagement (uses currently allocated seats, not historical allocation).
- Event types: **Copilot Events** (researching accounts, contacts, partners in Copilot or Deal Navigator drawer) and **Collaboration Events** (notes on shared lists, adding accounts to shared lists, messages via Copilot/CB4S). MoM bar graph.
- Team Engagement Table: User, Total Events, Accounts, Copilot Events, Collaboration Events.
- Engagement Impact: Closed with Engagement (count and %), top event types, and a table by opportunity owner: Total Events, % of Total Opportunities, Copilot Events, Collaboration Events. Opportunity owners may not be Crossbeam users; non-users show an **invite** icon.

**Partner tab** (HC 10845010, HC 9204052):
- Columns: partner name, recent activity, opportunity engagement, account overlaps, attributed value (if enabled), impact score, Partner Score.
- Sort: Most engaged, Biggest coverage, Highest impact, Most attributed, Highest Partner Score.
- Click partner name for Partner Detail Page.

**Salesforce tab**: the Crossbeam tab in Salesforce is only for Supernode users with the Salesforce Custom Object enabled and Salesforce as a data source. (HC 10845010)

Refresh: last sync timestamp in upper right; cadence follows your org's configured CRM sync. (HC 10845010)

---

## 14. Acting on overlaps (playbook facts)

- Example motion: find accounts that are your partner's customers but your prospects; human-led sales for the top 10% of accounts, automated co-marketing (ABM or ESP) for the rest. (HC 3376702)
- Actions: export the List; distribute via Crossbeam Copilot in Salesforce, HubSpot, or Microsoft Dynamics; connect Account Owners on both sides; push data back to Salesforce for rep workflow and attribution; run co-marketing campaigns with integration proof points; use partner emails for direct campaigns. (HC 3376702)
- Reciprocity: identify your customers who are your partner's prospects. (HC 3376702)

---

## 15. AI Hub

### 15.1 Coverage note

The AI Hub articles in this set are mostly signposts. The detailed MCP setup, connection steps, and tool list live in **Crossbeam MCP Server** (HC 12601327), which is not in this article group. Facts below come only from the group C articles.

### 15.2 Crossbeam MCP server facts

- Launched **11/6/2025** as **MCP Server (Limited Availability)**, Supernode and Enterprise only: "Provides AI-friendly access to Crossbeam's Ecosystem Intelligence, giving AI tools real-time, ready-to-use partner data with no setup required." (HC 12674444)
- 06/17/2026: MCP supports **Glean** (Glean Assistant and Glean Agents). Limited Availability. (HC 15303766)
- Partner Score data is available through MCP (labeled "Crossbeam MCP (beta)" in HC 9204052).
- Seat: Full Access or Sales seat required to connect MCP to an LLM such as Claude or ChatGPT. (HC 15588582)
- Role control: **Settings > Roles & Permissions** > **Edit** next to a role > **MCP** permission > **Access** or **No Access**. All roles default to **Access**. (HC 15588582)
- MCP usage does not count toward the Record Export limit (may change with notice). (HC 15588582)
- Pointers: setup and plan access in HC 12601327; overview at `https://www.crossbeam.com/what-is-crossbeam/crossbeam-mcp`; AI Agents in HC 15961519; data use in HC 15297694. (HC 16632186)
- Academy course "Let Your AI Talk Directly with Crossbeam": step-by-step for connecting Claude and ChatGPT. (HC 16720390, HC 13613176)

### 15.3 Crossbeam Credits (MCP metering)

- Credits measure AI access to your ecosystem data. When an AI tool or agent pulls partner and account intelligence from Crossbeam, it draws from the org's **shared, pooled balance**; no per-user allocations or caps. (HC 15588582)
- Today credits meter the **MCP server** only; may expand later with notice. (HC 15588582)
- Enforcement starts **September 1, 2026** on all plans. Before then, you could exceed allocation without interruption. (HC 15588582)

| Plan | Annual credits | Can buy more |
|---|---|---|
| Free | 50/yr | No |
| Connector | 500/yr | No |
| Supernode | 2,500/yr | Yes |
| Enterprise | 5,000/yr | Yes |

- Baseline credits come within the platform fee; plans without an annual platform fee should contact support for MCP access. (HC 15588582)
- Credits reset annually at renewal; plan-included and purchased credits do **not** roll over. (HC 15588582)
- Packs: **10K** = 10,000 credits for $1,000; **25K** = 25,000 for $2,500; **100K** = 100,000 for $9,000 (10% discount). Flat **$0.10 per credit**. Packs combinable. (HC 15588582)
- Buying: self-serve at **Plan & Billing** > **Add more credits** > choose pack > confirm authorization; applies immediately. Only admins with Plan & Billing access can buy in-app. Self-serve packs **renew automatically** with the subscription; invoiced to the billing contact on existing terms. Or add via Order Form with the Account Manager or the Crossbeam support inbox (support at crossbeam.com). (HC 15588582)
- Out of credits: free AI capabilities keep working (best practices, your own account context, product knowledge). Paid AI features pause until annual reset or pack purchase. Free and Connector plans are paused until reset. (HC 15588582)
- Usage tracking: admins only, **Plan & Billing** page, broken down by **MCP tool calls** and **active users**, by week, month, or all time. (HC 15588582)
- Alerts: email at **75%, 90%, 100%** of credits; in-app banner as you approach limits. (HC 15588582)

Usage estimates (HC 15588582):

| Pattern | Credits per user per month | Typical work | Typical persona |
|---|---|---|---|
| Light | ~200 | Account lookups before calls, ad hoc overlap checks, quick partner context | Individual sales reps |
| Moderate | ~600 | Partner recommendations, ecosystem lists, light automation | Partnership managers |
| Heavy | ~1,000 | Scheduled ecosystem scans, automated enrichment, batch reporting | RevOps and always-on automation |

Estimate method: pattern x headcount mix. (HC 15588582)
Derived (arithmetic on the above): one Moderate user at ~600/month consumes a Supernode's 2,500 annual baseline in about 4 months and a Connector's 500 in under one month. An always-on Eva-style automation at ~1,000/month uses about 12,000 per year, above every plan's baseline, so a Supernode or Enterprise org would need packs.

### 15.4 Prompts, skills, playbooks, and learning

- **Crossbeam MCP Prompt Guide** (PDF): 15 use cases and prompts organized by role. URL: `https://4716094.fs1.hubspotusercontent-na1.net/hubfs/4716094/AI%20Email%20Template%20Import/%5BFinal%5D%20Crossbeam%20MCP%20Prompt%20Guide.pdf` (HC 16632206)
- **AI Skills**: "Claude & ChatGPT Skills for Partnerships and GTM Teams" at `https://www.crossbeam.com/skills`, to get the most value from your MCP connection. (HC 16632210)
- **AI workflow playbooks**: GTM Playbooks at `https://www.crossbeam.com/resources/playbooks`, section **Crossbeam in AI**. (HC 16632208)
- Example MCP prompts (verbatim): "Who are my top partners?" and "Which partners should I prioritize this quarter?" (HC 9204052)
- ELG Insider AI collection: `https://insider.crossbeam.com/collection/elg-ai`. (HC 16632219)
- The AI Ecosystem Podcast, hosted by Bob Moore (CEO) and Lindsey DeFalco (VP of Product). (HC 16632216)
- Academy: **Quick Start: AI in Crossbeam** (AI Chat, Copilot AI Recommended Plays, more) and **Let Your AI Talk Directly with Crossbeam**. (HC 16720390)

### 15.5 In-app AI features

- **Crossbeam AI Chat**: in-app assistant; answers based on your ecosystem, CRM, and Crossbeam playbooks; can take actions like creating reports. Beta 08/05/2025, released 11/6/2025; dedicated nav entry 02/11/2026. (HC 12674444, HC 11786254, HC 13613176, HC 16632214)
- **AI Recommended Plays in Copilot**: surfaces partner moves where you work, CRM to Chrome. (HC 16632214)
- **Crossbeam Deal Alerts** (beta, Supernode only, 06/10/2025): AI combines Crossbeam data with CRM to email top opportunities and why they matter now, with suggested next steps. (HC 11509867)
- **AI Agents** (public beta 08/19/2026; Connector, Supernode, Enterprise): watch for a condition in Crossbeam data, such as a new mutual customer or a partner closing a deal on a shared account, and post a Slack notification on match. Configure once to flag new mutual customers, shared opportunities, and closed-won deals. (HC 16075353)

---

## 16. Onboarding and setup facts from video tutorials

- Register at `https://app.crossbeam.com/register`. (HC 4216565)
- Five steps to start (HC 11010806): (1) **Add a Partner**: invite via link or search in Crossbeam; (2) **Add Data**: connect CRM (Salesforce, HubSpot, etc.) or upload data; (3) **Create Populations**: customers, prospects, etc.; (4) **Set Sharing Settings**; (5) **Analyze Overlaps** with reports.
- Three Sharing Settings levels: **Sharing Data**, **Overlap Counts**, **Hidden**. Sharing can be customized per partner, with **Per-Population Overrides**. (HC 4270674)
- CSV upload video covers required fields and Sharing Defaults for Populations. (HC 3162302)
- Use Partnerbase.com to find partners already on Crossbeam. (HC 4361129)
- Reauthorize the Salesforce Custom Object integration when the connection has expired, credentials changed, or when troubleshooting related errors. Screenshot guide in HC 12013434. (HC 11987083)
- Crossbeam organizes connected data into segments called Populations, which you share and compare with partners; live demo sessions are bookable. (HC 8614169)

---

## 17. What changed recently (newest first)

**08/19/2026** (HC 16075353)
- **Open Data Partners (ODPs)** beta to GA (availability varies by plan): curated tech vendors whose customer data is sourced and maintained by Crossbeam. Instant overlaps without invitation, connection, or data-sharing agreement; one is added automatically when you create your account.
- **Partner Invitations** GA (all plans): upload a target list, send individual or bulk invites, track invite status in one workspace.
- **AI Agents** private to public beta (Connector, Supernode, Enterprise): Slack alerts on conditions.
- **Integration Seat** GA (Supernode, Enterprise): one per org, not counted toward seat limit.
- **Google Sheets for Offline Partners** (all plans): sheet as data source in addition to CSV; syncs on standard cadence.

**06/17/2026** (HC 15303766)
- **Opportunity Signals** (Supernode, Enterprise): shared contacts, overlapping accounts, co-sell context inside open opportunities.
- **Databricks as a Data Source** (all plans) and **Databricks Integration** (Connector, Supernode) for automated ongoing syncs.
- **Lists updates** (Connector, Supernode, Enterprise; Free can view and contribute to Lists shared with them): AND logic on Dynamically Shared List filters; share a List with the entire org at once.
- **Audit Log** (all plans): successful logins, failed logins, logouts.
- **Partner Invitations (beta)**.
- **MCP Server**: Glean support (Limited Availability).
- **Deal Navigator Exports** (Connector, Supernode).

**04/15/2026** (HC 14489383)
- **Dynamic Shared Lists** (Connector, Supernode, Enterprise): live external lists; filters lock at sharing.
- **Net New Accounts in Pipeline Generation** (Connector, Supernode view; Enterprise webhook).
- **Partner Account CRM Integration** (Connector, Supernode, Enterprise; Salesforce only): 1:1 link from each Crossbeam partner to its Salesforce Partner Account record; every Ecosystem Overlap record gains a Partner Account lookup.
- **Partner Score** (Connector, Supernode, Enterprise).
- **Sharing Hub** improvements (all plans): Population and Partner sharing settings in one place.
- **Lists and Navigation** (all plans): OR logic between segments, filter on specific Populations under My Population, partner "Select all", bulk List sharing, Notes sort by recency, Help Center / Academy entry in nav, only active data sources in multi-CRM filter.
- **Partner Tracker** (private beta, by request from your ASM): wish list of target partners, bulk import and invite.

**02/11/2026** (HC 13613176)
- **New Lists Experience**: Account Mapping Reports redesigned into Lists.
- **Account Mapping List**: dynamic, filterable ecosystem-wide overlap view.
- **New Navigation**: dedicated entries for **Search**, **AI Chat**, **Pipeline Generation**.
- **Product Line Sync** (Supernode, Enterprise; Salesforce only): product line data at opportunity level.
- **In-app SCIM** (Supernode, Enterprise): generate SCIM token and manage provisioning from organization settings.
- **Expanded Ecosystem Signals** (Supernode, Enterprise): contact-level details on Opportunity Created and Opportunity Closed Won signals, including role in the deal.
- **External Sharing via Lists (beta)**: share a saved List with a partner while controlling which columns they see or edit.
- **Sharing Hub (beta)**.

**12/10/2025** (HC 13017615)
- **Population Builder Modal** redesign: larger modal, expanded record preview.
- **Managed Offline Partners in onboarding**: Salesforce, AWS, Google Cloud, Microsoft available right after onboarding.
- **Account Mapping Reports Redesign**: single reports page, private-by-default, updated roles and sharing, cleaner UI, Notes.
- **Performance Dashboard Team metrics**: total activities, activity types, breakdowns by user and opportunity owner.
- **Suggested Partners** logic now uses Crossbeam and Partnerbase signals.

**11/6/2025** (HC 12674444)
- **Crossbeam AI Chat** (GA).
- **Ecosystem Signals via API and Webhook** (Supernode, Enterprise): real-time event data.
- **Managed Offline Partners (public data)**: overlaps with Salesforce, AWS, Google Cloud, Microsoft using third-party data curated by Crossbeam.
- **Smarter Matching**: DUNS, phone numbers, marketplaces beyond domain and name.
- **Population Types** (paid): assign customers, open opportunities, or prospects type to any custom Population; Matrix reflects types; data flows into Deal Navigator etc.
- **Custom Populations for Offline Partners** (paid).
- **Generate Pipeline Insights in Performance Dashboard** (Supernode, Enterprise).
- **Account Mapping Lists (beta)**.
- **MCP Server (Limited Availability)** (Supernode, Enterprise).

**08/05/2025** (HC 11786254)
- **Generate Pipeline in Deal Navigator** released.
- **Partner Field Mapping** (Supernode, Enterprise): map partner-shared custom fields to Salesforce or HubSpot.
- **Crossbeam AI Chat (beta)**.
- **Managed Offline Partners (beta)**.
- New Academy course: HubSpot-Powered Crossbeam Admin Certification.

**06/10/2025** (HC 11509867)
- **Crossbeam for Sales**: Sales Seat users redirected from `sales.crossbeam.com` to `app.crossbeam.com`.
- **Deal Navigator** released (in Crossbeam or Salesforce).
- **Performance Dashboard** released (Supernode only).
- **New Navigation Bar** released.
- **Partner Field Mapping (beta)** (Enterprise only at the time).
- **Generate Pipeline in Deal Navigator (beta)**.
- **Crossbeam Deal Alerts (beta)** (Supernode only).

**04/15/2025** (HC 10763503)
- **Salesforce fields** "Is a Customer of" and "Is an Open Opportunity For" auto-populate on the Account object (usable in Clari, Gong, Gainsight).
- **HubSpot fields** "is a customer of" and "is an opportunity for" pushed to the standard Company object, usable as report filters.
- **Deal Navigator (beta)**, **Performance Dashboard (beta)**, **New Navigation Bar (beta)**.

**03/04/2025** (from HC 10592414, HC 5303061, HC 3160236)
- Account Mapping Pass auto-included in Supernode and Enterprise and distributed to all Free partners.
- Free Explorer: Matrix and Lists capped at 50 records; record exports removed (legacy Explorer grandfathered until July 1, 2025).

**02/04/2025** (HC 10375251)
- **Ecosystem Activities Tracking** (attribution activities such as adding a missing contact to CRM from Copilot).
- **HubSpot Fields (beta)**.
- **Multi-currency support**: USD at current exchange rates.
- **Partner Visibility (beta, by request via CSM)**: data visibility limited to select users by role or need to know.
- **Pipedrive** as a data source.
- **DUNS matching (beta)**.
- **Optional Salesforce Permissions**: integration user connections with fewer required permissions.
- **Updated role names** for clarity.

**11/13/2024** (HC 10055272)
- Copilot **Ecosystem Intelligence** contact updates: signals for Decision Makers and Economic Buyers; **filled** signals = your partner ecosystem (shown first), **outlined** signals = broader Crossbeam Network; new quick filters; streamlined Account Highlights.
- **Message flow in Copilot**: message partners from Copilot or Slack, with status updates.
- **Universal Integration Settings**: toggle new partner and population pushes, see estimated record exports.
- **Record exports usage summary**: "Learn More" on Populations, Integrations, Plan & Billing pages.
- **Microsoft Dynamics Custom Object**.
- **Ready-to-use Salesforce reports** (Crossbeam 360 Dashboard).
- **Clay Integration**: continuous overlap sync for list building.
- **Pipedrive (beta)**.
- Push additional fields to **Salesforce and Snowflake**.

Renames and deprecations summary:
- Account Mapping Reports renamed to **Lists**; Saved Reports, Shared Lists, Ecosystem Reports consolidated. (HC 13688795)
- Shared Lists now called **Static Lists**. (HC 13688795)
- Free plan formerly called **Explorer**. (HC 10592414)
- "Generate Pipeline in Deal Navigator" became standalone **Pipeline Generation**. (HC 13613176, HC 11420734)
- `sales.crossbeam.com` retired in favor of `app.crossbeam.com` for Sales Seats. (HC 11509867)
- Overlaps column split into Is a Prospect of / Is an Opportunity for / Is a Customer of. (HC 11801904)
- Free Explorer record exports removed March 4, 2025. (HC 3160236)

---

## 18. Troubleshooting

None of the group C articles contain literal system error strings. The following are every symptom and UI message named in the articles, with UI labels in backticks.

| Symptom / message | Cause | Fix | Source |
|---|---|---|---|
| `Share` button is disabled on a new List | List not saved yet | Click `Save as a new list`, then Share | HC 3160236, HC 11801904 |
| Teammates cannot see my new List | New Lists are private by default (creator and admins only) | Share it, or share with the whole org (06/17/2026 option) | HC 11801904, HC 15303766 |
| Cannot create or share Lists as a Sales seat | Sales seats cannot create or share | Have a Full Access user create and share it | HC 13688795 |
| Limited user cannot edit a List or see Partner Shared Lists | Limited role is View only, no Partner Shared Lists | Change role or seat | HC 13688795 |
| Free plan shows only 10 (or 50) records | Free plan cap | Get shared a List by a paid partner, AMP from a Supernode/Enterprise partner, or upgrade | HC 13688795, HC 5303061 |
| Free user cannot export | Exports removed from Free on March 4, 2025 | AMP allows 100 records per export with the granting partner only | HC 3160236, HC 10592414 |
| Free user cannot open Greenfield List even with AMP | Greenfield is paid only | Upgrade | HC 10592414 |
| Connector export stops at 1,000 rows | Connector per-export row limit | Filter first; use List notifications; Supernode is unlimited | HC 8195191 |
| Note I wrote is missing in another List | Notes are List-specific | Add the Note in that List | HC 11801904 |
| Private Slack channel missing from notification dropdown | Crossbeam app not in channel | In Slack: `/invite` > `Add apps to this channel` > `Crossbeam` | HC 3640085 |
| `Connect to Slack` button appears instead of channel dropdown | Slack not connected | Connect Slack | HC 3640085 |
| Slack shows rep name but does not tag them | List lacks Account Owner Email column, or data source lacks it | Sync and add both Account Owner Name and Account Owner Email; map email column for CSV/Sheets | HC 3640085 |
| Rep mentioned but not alerted | Owner not in the Slack channel | Add them to the channel | HC 3640085 |
| Crossbeam flags a Slack Connect channel | Channel has an unknown org, a partner not in the List, or multiple orgs | Pick a channel containing only relevant partners | HC 3640085 |
| Notifications not immediate | Sent every four hours | Expected | HC 3640085 |
| Partner sees a different overlap count | Results are from each side's root data; many-to-one matches; your duplicates count separately | De-dupe CRM/CSV or use advanced population filters | HC 3431068 |
| White box in Matrix, no records visible | Partner shares only overlap counts | Click the box > `Request Data` | HC 5303061 |
| Potential Revenue missing in Matrix | Not a CRM source or not syncing amount and deal is closed; not sharing overlap counts for 1+ Population; partner not sharing any Population; free plan | Fix each; or apply the Pipeline Mapping Preset | HC 6797349 |
| Potential Revenue not updated after settings change | Recalculation delay | Wait a few minutes | HC 6797349 |
| Potential Revenue total does not equal sum of Matrix cells | Opportunities in multiple Populations are not double counted | Expected | HC 6797349 |
| Desired amount field not in Potential Revenue dropdown | Field not synced | Add the field to sync | HC 6797349 |
| Partner Score = `Unknown` | Partner shares no data; required CRM fields not synced; no Customers Population on your side or partner's; free tier | Fix data gap | HC 9204052 |
| Partner Score = `None` | Fewer than 10 overlapping closed-won deals in 365 days, or zero impact | Setup is correct; needs more history | HC 9204052 |
| Partner Score unavailable, CSV-only org | CSVs lack deal data | Connect a CRM | HC 9204052 |
| Low-score partner recommended in Deal Navigator | Recommendations use deal signals, not Partner Score | Expected | HC 9204052 |
| Performance Dashboard empty, lists fields | Required CRM deal fields not synced | Sync the 7 required fields via data source settings | HC 10845010 |
| Performance Dashboard shows benefits screen instead of data | Fewer than 10 opportunities with engagement activities since start of year | Drive engagement activity | HC 10845010 |
| Performance Dashboard counts differ from Deal Navigator | Different sync schedules | Expected | HC 10845010 |
| New vs Existing Business split looks wrong | Field mapping | Data Sources > CRM > Field Mapping > New Business / Existing Business | HC 10845010 |
| `+Add` / `Added` button missing next to a contact in the drawer | Salesforce authorizing user lacks Write access on Contacts | Salesforce admin grants Write on Contacts | HC 10844915 |
| Deal Navigator missing or empty | Required fields not synced (Account Owner Name, Account ID, Account Name, Deal Name, Is Closed, Deal Owner ID) | Sync them | HC 10844915 |
| Opportunities missing from Deal Navigator | Excluded: test data, close date over a year out, amount below 0, or closed | Expected | HC 10844915 |
| Deal Navigator in Salesforce not working for reports/dashboards | Salesforce custom object not enabled; Crossbeam tab not set up | Enable custom object; set up Crossbeam tab | HC 10844915 |
| Pipeline Generation shows no leads from Leads | Lead object not used | Use Account data | HC 11420734 |
| ICP filters missing in Pipeline Generation | Industry, Employees, Country, Account Owner not synced | Sync them | HC 11420734 |
| Net New Accounts empty | No partner has Greenfield sharing (All Accounts) | Request Data asking for All Accounts | HC 14463832 |
| Cannot `Add to CRM` for Net New Accounts | Not yet supported | Export instead | HC 14463832 |
| Paid AI features paused | Credits exhausted (enforced from Sept 1, 2026) | Supernode/Enterprise buy packs; Free/Connector wait for annual reset or upgrade | HC 15588582 |
| User cannot use MCP | No Full Access/Sales seat, or role MCP permission set to No Access | Assign seat; Settings > Roles & Permissions > MCP = Access | HC 15588582 |
| Cannot buy credits in app | Not an admin with Plan & Billing access, or on Free/Connector | Use an admin; Free/Connector not eligible | HC 15588582 |
| Salesforce Custom Object integration errors, expired connection, changed credentials | Authorization lapsed | Reauthorize per HC 12013434 | HC 11987083 |
| Deleted a List by mistake | Deletion is permanent | Cannot be undone | HC 3160236 |

---

## 19. Source coverage notes

- Several AI Hub and Video Tutorial articles are signposts (links or embedded video with little text); their facts are captured above where present.
- The MCP server tool list, connection URL, and client setup steps are not in this group; see HC 12601327.
