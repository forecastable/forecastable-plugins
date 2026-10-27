<!-- Library file for crossbeam-admin-reference.md. Source: Crossbeam Help Center, extracted September 25th, 2026. Cite (HC number); confirm in-app when a screen may have moved. -->

# Crossbeam Admin Reference E: Crossbeam for Sales, Copilot, Deal Navigator, Messaging, Attribution, MCP, SCIM

Source set: 20 Crossbeam Help Center articles (group E). Article numbers cited as (HC nnnn). Only facts stated in these articles are included. Where this group is silent on a topic the requester asked about (for example REST API pagination, rate limits, webhooks), that is stated explicitly in the relevant section rather than filled in.

---

## 1. Plan, seat, and role matrix (quick lookup)

### 1.1 Feature by plan and seat

| Feature | Seat required | Plan required | Notes |
|---|---|---|---|
| Sales Settings (admin config) | Sales seat with Manager role, or Full Access seat with Admin role | Connector or Supernode | Settings > Sales Settings (HC 6699011) |
| Pipeline Generation | Sales seat or Full Access seat | Connector or Supernode; Explorer (free) has limited access | Also available in Salesforce (HC 6699011, HC 9708718) |
| Deal Navigator | Sales seat or Full Access seat | Connector or Supernode | Also available in Salesforce via Crossbeam tab (HC 6699011) |
| Performance Dashboard | Full Access seat only | Supernode | Four tabs: Open, Closed, Team, Partner (HC 6699011, HC 9708718) |
| Dynamic Shared Lists | Sales seat (Edit, Comment, or View Only) or Full Access seat (Manage, Edit, Comment, or View Only) | Connector or Supernode to create and share; Free plan can only view when shared by a partner | Sales seat cannot create or share lists (HC 6699011) |
| Co-Selling and Get Intel (Messages) | Sales seat or Full Access seat | Connector or Supernode | Paid feature (HC 6699011, HC 8095694) |
| Sales Notifications | Sales seat or Full Access seat | Connector or Supernode | (HC 6699011) |
| Crossbeam Copilot (general) | Sales seat or Full Access seat | Connector or Supernode; Explorer gets a preview version only for Salesforce and HubSpot | HC 9708718 says Explorer preview is Salesforce only; HC 6699011 says Salesforce and HubSpot (HC 6699011, HC 9708718) |
| Copilot for Salesforce | Sales seat for full access; users without a Sales seat get Starter Access | Free: Starter Access. Connector: full Copilot plus customization. Supernode: full Copilot plus customization via the Crossbeam Custom Object | (HC 3685976) |
| Copilot for HubSpot | Full Access seat and/or Sales seat; installer needs Crossbeam Admin role or Crossbeam for Sales Manager role with Integrations permission, plus HubSpot App Marketplace Access | Connector or Supernode | (HC 8940278) |
| Copilot for Chrome | Installable by Admin role and/or Partner Manager role | Copilot plans (Connector or Supernode) | (HC 4779242, HC 9167877) |
| Copilot for Gong | Crossbeam Admin role, Gong Admin role | Supernode plus Gong Engage subscription | (HC 9167881) |
| Gong Activity Timeline (Partner Mentions) | Not specified | Connector or Supernode, no Gong Engage required | (HC 9167881) |
| Copilot for Outreach | Outreach admin role or custom role that can install apps | Supernode only | (HC 9579063) |
| AI Recommended Plays | Copilot user | Connector or Supernode | (HC 9596637) |
| Plays and Contacts tabs in Copilot for Salesforce | Sales seat | Connector or Supernode | (HC 8986760) |
| Attribution push to Salesforce | Salesforce Admin required to set up | Supernode | (HC 9180986) |
| Ready-to-use Salesforce report templates | Sales seat or Full Access seat | Supernode only; requires Salesforce Custom Object Integration | (HC 9708718) |
| Crossbeam tab (iframe) in Salesforce | Any Salesforce user once the managed package is installed | Not stated | Deal Navigator in app.crossbeam.com still requires a Crossbeam seat (HC 11501777) |
| Crossbeam MCP Server | Full Access or Sales seat | All plans (Free, Connector, Supernode, Enterprise) | Credit metered (HC 12601327) |
| SCIM provisioning | Not applicable | Enterprise only; requires SSO first; enabled via Crossbeam Support | (HC 12548850) |

### 1.2 Access facts

- The free plan (Explorer) does not have Sales seats. There is a limited preview of Copilot for Salesforce that does not require a Sales seat. Upgrades via the Plan & Billing page (app.crossbeam.com/billing). (HC 9708718)
- Crossbeam Copilot is only available for Connector or Supernode customers. Each Crossbeam Core seat comes with access to Crossbeam for Sales and Crossbeam Copilot. Additional Crossbeam for Sales seats are purchased from Plan & Billing. (HC 9167877, HC 9579063)
- Feature access may vary based on permissions configured by the org's Crossbeam admin. (HC 9708718)

### 1.3 Crossbeam for Sales roles (from SCIM role definitions)

| Role label | SCIM value | Capabilities |
|---|---|---|
| Manager | `partner-manager` | Configures Crossbeam for Sales, manages other users' access to Crossbeam for Sales |
| Standard | `co-seller` | Full access to Crossbeam for Sales features, make partner requests, use Chrome extension, full access to Crossbeam Copilot, gets alerts, access to lists, access to Deal Navigator, reply to conversations, complete conversations and mark Attribution. Does not have Crossbeam Core access |
| Limited | `viewer` | Full access to Crossbeam for Sales features listed for Standard (including Copilot), but cannot make partner requests or access lists. Does not have Crossbeam Core access |

(HC 12548850)

- Standard role users can initiate new partner requests, reply, complete conversations, and mark Attribution. Limited role users can reply to and complete conversations but cannot initiate new requests. (HC 9708718)
- You must be a Crossbeam for Sales Manager to set up Co-Selling Templates. (HC 8095694)

---

## 2. Crossbeam for Sales: platform location and the June 2025 change

- Starting June 10, 2025, sellers logging in to Crossbeam for Sales are redirected to Crossbeam core and land on Deal Navigator. Crossbeam for Sales remains accessible "for now", but all Crossbeam for Sales settings must be managed in Crossbeam Core > Settings > Sales Settings. (HC 8095694, HC 8345696)
- Once a Sales seat user accepts their invite, Crossbeam launches on the Deal Navigator page (app.crossbeam.com/deal-navigator/close-deals). (HC 9708718)
- Sales seat left navigation: Pipeline Generation, Deal Navigator, Performance Dashboard (Full Access seat only, Supernode), Shared Lists (Sales seat view and comment on Dynamic Shared Lists shared with them), Messages. (HC 9708718)

---

## 3. Sales Settings: admin setup from scratch

Seats: Sales seat (Manager role) or Full Access seat (Admin). Plan: Connector or Supernode. Sales Settings configures enabled partners and account data, co-selling templates, Slack shared channels, and notifications. (HC 6699011)

### Step 1: Access
- Crossbeam navigation: Settings > Sales Settings. (HC 6699011)

### Step 2: Enable partners (Partner and Account Data)
1. Follow the setup prompts under Partner and Account Data.
2. Check the boxes for partners your team should access, click continue.
3. Select an account status for each partner's custom Population, click continue.
4. Click Confirm and Import Data.
5. Manage enabled partners by clicking Enabled Partners.

From the partner view you can:
- Configure Inbox Settings, including enabling or disabling Direct Shared Conversations.
- Use the three-dot menu to edit co-selling templates, manage partner settings, or hide partner data.
- Assign or update the Partner Manager.
- Add collateral links.
- View partner requests.
- Review overlapping accounts and send messages.

Gotcha: if a partner is not appearing under Enabled Partners, it has not been activated. Click Manage under Crossbeam to search for and add them. (HC 6699011)

### Step 3: Co-selling templates
See section 4. Setting up templates also enables Get Intel. (HC 6699011)

### Step 4: Shared Slack channels
1. Settings > Sales Settings, click Add to Slack, follow prompts to install the app.
2. Click Manage Slack Shared Channels, pick the correct Slack channel for each partner from the dropdown.
3. Save Changes.

Private channels: the Crossbeam Slack app must be added in Slack via channel name > Integrations > Apps before it appears in the dropdown. The partner must have fully joined the channel first. (HC 6699011)

### Step 5: Alerts
- Settings > Sales Settings > Alerts, toggle notification types, Save Changes. If Slack is not configured, all notifications default to email. (HC 6699011)

---

## 4. Co-Selling Automation and Get Intel

### 4.1 What it is
- Get Intel is part of Co-Selling Automation. Enabling Co-Selling also enables Get Intel. (HC 8095694)
- Get Intel is how sellers request partner help on a specific account: an introduction, background intel, or co-sell assist. It is powered by co-selling templates configured by the admin in Sales Settings. (HC 9708718, HC 6699011)
- Co-Selling Automation tools are a paid feature on Connector and Supernode. (HC 8095694)
- Templates set guardrails on which partners reps can reach out to, the questions they should ask, and the context they should provide. (HC 8095694)

### 4.2 Admin setup: questions
Path: Settings > Sales Settings > Co-Selling Templates > Edit Templates. (HC 6699011)
- Click Edit next to a template question. In the pop-up, change the question and optionally limit it to specific partners (type partner names in the box).
- If no partners are assigned, the question is visible to the sales team for all partners.
- Click Save.
- Add custom questions with +Add a question.
- Remove questions with the red trash can.
- Toggle Allow Custom Questions to let reps write their own additional questions.
- Click Continue. (HC 8095694, HC 6699011)

### 4.3 Admin setup: context prompts
- Type talking points directly into the context table (the blank space next to each item).
- +Add adds a new talking point or prompt; red trash can removes one.
- Click Save Changes. (HC 8095694, HC 6699011)

### 4.4 Inbox settings and Direct Shared Conversations
Path: Settings > Sales Settings > under Network, select a partner from Enabled Partners > Inbox Setting.
- Toggle Enable Direct Shared Conversations.
- Enabled: anyone can share conversations and receive messages with the partner.
- Disabled: conversations must be reviewed (approved) before anyone can send or receive messages with the partner.
- Save all changes. (HC 8095694)
- Related: the daily Action Required Reminder email targets Managers to act on outstanding items such as approving conversations. (HC 8345696)

### 4.5 Shared Slack channels for co-selling
- Install the Crossbeam for Sales Slack App (link from sales.crossbeam.com/settings). If you belong to multiple Slack instances, pick the correct one in the dropdown at top right. Without permission to install apps, you can send a request to your Slack Administrators to approve the app. (HC 8095694)
- Set up Slack Connect shared channels with partners if none exist. (HC 8095694)
- For private channels, add Crossbeam for Sales to the channel via the dropdown next to the channel name > Integrations tab. (HC 8095694)
- Link channels: Settings > Sales Settings > under Integrations, Manage Shared Channels; for each partner choose the shared channel; click the refresh icon if a channel is missing; Save Changes. (HC 8095694)
- Prerequisites before a channel can be selected: it is a Shared Slack Channel, the partner has fully joined, and for private channels the app is added via Slack > Integrations > Apps. (HC 8095694)
- When a rep sends a Partner Request using a Co-Selling Template, Crossbeam automatically starts a thread in the shared Slack channel. (HC 8095694)

### 4.6 Where reps access Get Intel
- Crossbeam Copilot: Get Intel button on a partner (Copilot panel). (HC 6699011, HC 9708718)
- Deal Navigator: Message button in the table (the partner column on any open opportunity). (HC 6699011, HC 9708718)
- Pipeline Generation: Message button in the table. (HC 6699011, HC 9708718)
- Messages (left nav): all open and completed partner conversations across all partners. (HC 9708718)

### 4.7 Rep workflow
1. Click Get Intel or Message at the entry point.
2. Select questions from the admin's co-selling template.
3. Add context for the partner and send. (HC 9708718)

Copilot for Salesforce flow specifically: Get Intel > select the warm introduction or +Add your own question > Choose Partners (check the partner) > Add Context (write context against the prompt) > Preview Your Message > Edit or Send. (HC 3685976)

In a conversation the rep can: reply and complete; view overlapping accounts for that partner; mark Attribution on closed deals to credit the partner assist (syncs automatically to Salesforce); view admin-added collateral links for the partner. Clicking into a message shows history and lets the rep continue internally or publicly with the partner. (HC 9708718)

### 4.8 Gotchas
- If the Get Intel button displays an X, that partner has not been enabled for co-selling (is not available for this feature). (HC 6699011, HC 3685976)
- HC 9708718 phrases it as: if the Get Intel button does not display, the partner has not been enabled for co-selling by the admin. (HC 9708718)

---

## 5. Messages in Copilot (shared behavior across Salesforce, HubSpot, Chrome, Gong, Outreach)

- On the Partners tab, users click Message (or Message Partner) when available. After sending, a notification confirms delivery. Clicking the notification opens the messages section in Crossbeam for Sales. (HC 3685976, HC 8940278, HC 4779242, HC 9167881, HC 9579063)
- Message preview states: Blue with reply icon means new message; Gray means awaiting a response. Clicking the Blue Reply icon or the Message icon opens Crossbeam for Sales. (same articles)
- If the message was sent through Slack, a clickable Slack channel appears in the preview linking directly to Slack. (same articles)
- Recipient behavior (Salesforce article): by default only the partner manager is notified. In some cases the account owner can be pinged directly, but only if the partner has mapped their account owners in Crossbeam. (HC 3685976)

---

## 6. Sales Notifications

### 6.1 Two mechanisms
- Sales Alerts: configured in Settings > Sales Settings > Alerts. Covers Deal Insights emails, new overlap notifications, Slack, weekly reports, and action required reminders. (HC 6699011)
- List Notifications: configured on any List via the bell icon. Sends overlap updates via email or Slack and can notify non-Crossbeam users. (HC 6699011, HC 9708718)
- Personal preferences (rep side): Settings > Profile & Preferences > Notifications. Toggle Deal Insights emails, new overlap notifications, Slack nudge messages, weekly reports, action required reminders. (HC 9708718)
- Slack channel notifications and overall alerts configuration are admin-owned in Settings > Sales Settings > Alerts. (HC 9708718)

### 6.2 Notification catalog
Deal Insights (daily and weekly targeted email):
- Weekly Focus List: end-of-week email summarizing new accounts, opportunities, recently won accounts, and closed accounts.
- New Overlaps, Recently Assigned Overlaps, and New Deals: list the account and partner(s) with context prompts to start the conversation.
- New Requests emails.
Other:
- Action Required Reminder: daily email targeting Managers to act on outstanding items such as approving conversations.
Slack notifications:
- Slack Nudge Message
- Weekly Report
- Mid-Week Update for Sales
- New Account Overlaps
(HC 8345696)

### 6.3 Channel routing rules
- Unless Slack is configured, all notifications go over email. After Slack is configured, notifications go to Slack by default rather than email. (HC 8345696)
- To prefer email, toggle Slack alerts off in Notifications settings (Crossbeam says not recommended). (HC 8345696)
- Path: Settings > Sales Settings > Alerts, toggle options. (HC 8345696)

---

## 7. Pipeline Generation

- Surfaces Top Prospects: net-new accounts that overlap with your partners and match your ICP. (HC 6699011, HC 9708718)
- Filters: Account Owner, Industry, Number of Employees, Partners, Country. (HC 6699011, HC 9708718)
- Sort by Recent Partner Customer to see accounts that just became a partner's customer, described as a strong buying intent signal. (HC 6699011, HC 9708718)
- Message button on any account to reach out to a partner (Get Intel). (HC 9708718)
- Available in Crossbeam and in Salesforce (Crossbeam tab). Explorer has limited access. (HC 6699011, HC 9708718)
- The MCP tool `find_new_accounts` returns accounts from Pipeline Generation, including net new accounts not yet in your CRM. (HC 12601327)

---

## 8. Deal Navigator

### 8.1 In Crossbeam
- Prioritized view of existing open pipeline, surfacing deals most likely to benefit from a partner assist. (HC 6699011)
- Sales Managers can view all opportunities across the team and filter by opportunity owner. (HC 6699011)
- Reps click into a deal to see which partners overlap with the account, and click Message to request intel on the deal. (HC 9708718)
- Accessible in Salesforce via the Crossbeam Copilot component on Opportunity records. (HC 9708718)
- The MCP tool `find_partner_recommendations` returns ranked partner suggestions for an open opportunity using the same recommendation engine as Deal Navigator. (HC 12601327)

### 8.2 Crossbeam tab (iframe) inside Salesforce
- The Crossbeam SFDC Iframe is an embedded tab that brings Deal Navigator and the Performance Dashboard into Salesforce. (HC 11501777)
- Deal Navigator in the iframe: a table view of open opportunities that overlap with partners' customers. (HC 11501777)
- Performance Dashboard tab in the iframe: measure ecosystem coverage on open opportunities, analyze ecosystem influence on closed deals, track team engagement with Crossbeam data. (HC 11501777)
- Available to any Salesforce user once the Crossbeam managed package is installed. Reports and dashboards need the Salesforce custom object enabled. Deal Navigator in app.crossbeam.com still requires a Crossbeam user seat. (HC 11501777)
- HC 9708718 describes the Crossbeam tab as giving access to Deal Navigator and Pipeline Generation in Salesforce. (HC 9708718)

Setup, Lightning: Setup > App Manager > find the Sales app > Edit > Navigation Items > add the Crossbeam tab > Save. (HC 11501777)
Setup, Classic: + icon in tab bar > Customize My Tabs > choose current app > add Crossbeam to visible tabs > Save. (HC 11501777)

Note: the full Deal Navigator guide (HC 10844915) is referenced but not in this group.

---

## 9. Performance Dashboard

- Seat: Full Access seat only. Plan: Supernode. (HC 6699011, HC 9708718)
- Purpose: show how partners influence pipeline and revenue, identify reps effectively using ecosystem data, spot missed opportunities for partner engagement, demonstrate ecosystem value. (HC 6699011)
- Tabs:
  - Open: generated pipeline metrics and open opportunities with partner overlap.
  - Closed: closed-won opportunities influenced by partners.
  - Team: team engagement activity across the ecosystem.
  - Partner: partner performance and leaderboard. (HC 6699011)
- Also available in the Salesforce Crossbeam tab. (HC 11501777)
- Detailed metric definitions live in the Performance Dashboard guide (HC 10845010), which is not in this group; no metric formulas are given in these articles.
- Related currency rule stated in attribution articles: deal amounts are represented in USD by converting all currencies at current exchange rates, not the rates at time of deal closure. (HC 9180986, HC 9180987)

---

## 10. Dynamic Shared Lists

- Shared live workspace with a partner for accounts being co-sold. Unlike Static Shared Lists, they update automatically as accounts enter or leave filter criteria. (HC 6699011)
- Sales seat users can edit, comment on, and view lists shared with them but cannot create or share. Full Access users with Standard or Admin roles can create, share, and manage. (HC 6699011)
- Free plan: view only, when shared by a partner. (HC 6699011)
- Copilot for Salesforce Feed tab shows overlaps sent to you from Shared Lists. (HC 3685976)

---

## 11. Crossbeam Copilot (all surfaces)

### 11.1 Overview
- Current Copilot apps: Salesforce, HubSpot, Chrome, Outreach, Gong. (HC 9167877)
- Sellers can identify best partners for insights, introductions, or assistance; access enriched contacts with signals like "Decision-maker" and "Economic Buyer" and add missing contacts to the CRM; run Ecosystem-Led Growth plays based on partner status. (HC 9167877, HC 8986760)

### 11.2 Tabs
- Account (default landing page): key partner insights for the account plus AI Recommended Plays. Buttons: Generate AI Playbook, View Play Details. Ecosystem Intelligence: Partner Scope insights in Account Highlights distinguish "Your Network" (your partner ecosystem) from "The Crossbeam Network" (broader ecosystem insights). (HC 9167877, HC 3685976, HC 8940278, HC 4779242, HC 9167881, HC 9579063)
- Partners: high-level overview of associated partners with Ecosystem Intelligence signals to prioritize who to contact. Filter: All or Pick a Standard Population. Sort: Default or A-Z / Z-A (Chrome: Default or Partner Name). Search bar (HubSpot, Chrome). Partner Impact tagged as High Impact or Med Impact when connected to a partner (HubSpot, Chrome, Gong, Outreach). Get Intel or Message Partner starts a conversation. In Salesforce, the three dots show detailed partner account information. Outreach article also calls this the Overlaps tab. (same articles)
- Partner Impact is a visual recommendation or value within Crossbeam based on partner metrics. (HC 8940278, HC 4779242, HC 9167881)
- Contacts: contacts partners share that you may not have, with context from the shared number of partners and partner activity. Search by name, email, or phone; sort A-Z or Z-A; LinkedIn quick link; Quick Filters by signal. (same articles)
- Plays: actions based on the partner's status with the account and available data. Generate AI Playbook, View Play Details, Play (list of actionable next steps), Risk & Conditions (details, who it is best suited for, key conditions, potential risks). (same articles)
- Feed (Salesforce only): overlaps for new accounts assigned to you, overlaps for new opportunities assigned to you, overlaps sent to you from Shared Lists. (HC 3685976)

### 11.3 Ecosystem Intelligence signals in Contacts (how they are ranked and displayed)
- Crossbeam applies Partner Scope insights to prioritize contacts and highlights signals that identify Decision Makers and Economic Buyers from your partner ecosystem and the broader Crossbeam Network. (HC 3685976, HC 8940278, HC 4779242, HC 9167881, HC 9579063)
- Contacts from your partner ecosystem are marked with filled-in signals and appear first, as they better align with your ICP. Outlined signals represent Ecosystem Intelligence from the wider Crossbeam Network. (same articles)
- Contact ordering also uses the number of partners sharing the contact and partner activity (for example who recently had activity with a key partner). (same articles)
- Plays tab: partners who have the account in their Customers Population are labeled Customers, highlighted in orange with a star. Custom Partner Tags from Crossbeam are shown for each partner. (HC 3685976, HC 8986760)

### 11.4 Universal Copilot Settings (admin)
- Configuring Universal Copilot settings applies to all Copilots on the Crossbeam account: Chrome, Salesforce, Outreach, HubSpot, Gong (also known as Gong Engage). (HC 9167877 and all Copilot articles)
- Path: Integrations workspace (app.crossbeam.com/integrations) > the Copilot row or tile > Settings (or Settings Gear next to Install for Chrome and Outreach tiles, found under Recommended) > side drawer. (HC 3685976, HC 8940278, HC 4779242, HC 9167881, HC 9579063)
- In the drawer, uncheck any of your data or partner data you do not want pushed into Copilot, and uncheck specific partners from the data push. Save. (same)
- Configuring Universal settings does not count toward record export limits. (same)

### 11.5 Reauthorize the Copilot connection (Salesforce, HubSpot, Gong)
- Integrations workspace > Copilot row > three dots to the right of Settings > Connection Details, or click Reauthorize > side drawer > Reauthorize (Salesforce redirects to Salesforce) or follow the modal prompts. (HC 3685976, HC 8940278, HC 9167881)

### 11.6 Login
- SSO orgs: open Copilot in the tool and click Continue with SSO; no separate invite needed. (HC 9708718)
- Non-SSO orgs: users receive a separate email invite for Copilot; click Join Now. (HC 9708718)
- No Sales seat: if Copilot for Salesforce is enabled, users see a preview with limited data and a Request Access button that emails the admin. Admin reviews under Settings > Team > Seat Request tab. (HC 9708718)

---

## 12. Copilot for Salesforce

### 12.1 Basics
- Setup time estimate under 30 minutes. Support: the Crossbeam support inbox (support at crossbeam.com). (HC 3685976)
- Reps see partner data on Accounts, Leads, and Opportunities without logging in to Crossbeam. The FAQ adds that Copilot appears on Accounts, Leads, Opportunities, and Contacts. (HC 3685976, HC 9209268)
- Install using the Installation Guide (v2, HC 9280237, not in this group). New versions are installed by returning to the AppExchange. (HC 3685976)
- Plans: Free, Starter Access Copilot with limited overlap and opportunity details, Request Access emails admin, and once a Sales seat is assigned an invite appears in Copilot (click Accept Invite). Connector: full Copilot, customization allowed. Supernode: full Copilot, customization of data via the Crossbeam Custom Object. (HC 3685976)
- Only overlaps from Populations using Salesforce as a data source are viewable in Copilot for Salesforce. (HC 3685976)

### 12.2 Salesforce Classic
- Setup wizard and Copilot component work only in Lightning. Crossbeam pushes data to a custom object that can be added to Account, Opportunity, and Lead page layouts so it is visible in Classic. (HC 9209268)

### 12.3 Third-party access domains (must be approved during install)
- api.crossbeam.com: get Crossbeam data
- auth.crossbeam.com: authenticate Crossbeam users
- login.salesforce.com: authenticate Salesforce access for data
- sentry.io: error reporting
- test.salesforce.com: required for Salesforce testing
(HC 9209268)

### 12.4 Copilot settings (gear icon inside Copilot)
- Only users with the Crossbeam Setup User permission set can open Settings. Settings apply globally to all Copilot for Salesforce users. (HC 3685976)
- Display or hide fields: Gear > Partner Field Settings tab > select partner > select Salesforce Object > toggle each field Hidden or Displayed > Close. Verify via View Detail next to a partner. (HC 3685976)
- Change partner sort order: Gear > Sort Partners tab > pencil to edit display number > Save icon (or X to cancel) per change > Reset Sort to confirm order change > Close. (HC 3685976)

### 12.5 Trusted URLs (enables Plays and Contacts tabs)
- Plays and Contacts tabs are initially unavailable; the user sees one of two screens depending on permission sets, prompting them to contact their Salesforce Admin. (HC 3685976, HC 8986760)
- A Salesforce Admin with Crossbeam Setup User can do this configuration. A Crossbeam seat is not required. (HC 3685976, HC 8986760)
- Steps: click Configure Trusted URLs (redirects to Salesforce Setup) > Quick Find "Trusted URLs" > New Trusted URL > enter:
  - API Name: Crossbeam
  - URL: https://app.crossbeam.com
  - CSP Context: Lightning Experience Pages
  - CSP Directives: frame-src (iframe content)
  - Save, then click Validate Trusted URLs. (HC 8986760)

### 12.6 Plays availability conditions
- If the partner shares Customer Population, Open Opportunity Population, and opportunity-level data, most plays are available. (HC 8986760)
- For every play except Pitch the Stack, the partner must share the account owner's name and email, because the play instructs you to contact the account owner. Without them Crossbeam has no next steps. (HC 8986760)
- Example play, Recently Won. Conditions: partner closed this deal in the last 90 days; the account is your Prospect or Open Opportunity; partner shares account owner name and email. Outcomes: find the Champion and Economic Buyer; validate your contacts and get the scoop on the sales process. (HC 8986760)
- Contacts tab shows all contacts partners share. If a contact is not in your CRM, Copilot shows Add to CRM to add it directly to Salesforce. (HC 8986760)

### 12.7 Salesforce permission sets (v2 app)
Five permission sets that must be configured:
- Crossbeam Setup User (RevOps, PartnerOps, Admin; MUST have Crossbeam credentials): setup and configuration access; sees overlaps in Copilot; sees and clicks "Open in Crossbeam"; read and write access to reports and the custom object.
- Crossbeam Account User (all roles): sees overlaps with a Crossbeam Core or Crossbeam for Sales role; sees "Open in Crossbeam" with a Core role; denied reports and custom object.
- Crossbeam Report User (sales, CS, marketing without Crossbeam credentials): reports and custom object access; cannot see overlaps in Copilot; "Open in Crossbeam" hidden.
- Crossbeam Copilot Viewer (users who should only see that accounts overlap): sees overlaps in Copilot but cannot see overlap details with a Core or Sales role; "Open in Crossbeam" hidden; denied reports and custom object.
- [Deprecated] Crossbeam Salesforce User: not valid after v1.53, to be removed.
- Crossbeam Report User can be assigned alone or in addition to Crossbeam Account User or Crossbeam Salesforce User.
(HC 8780741)

Assigning in Salesforce: gear > Setup > Administration > Users > Users > click user's full name > Permission Set Assignments > Edit Assignments > move from Available Permission Sets to Enabled Permission Sets with Add arrow (Remove arrow to remove) > Save. (HC 3685976)

### 12.8 Upgrade and reauthorize the Salesforce app
Upgrade:
1. AppExchange listing > Get it Now (log in to the target org if prompted).
2. Select Install for Admins Only (controls access and permissions after install).
3. Click Upgrade. (HC 8780741)
Authorization (Setup Assistant):
1. The user must have the Crossbeam Setup User permission set assigned.
2. App Launcher > search Crossbeam Setup.
3. Click edit, then Revalidate, and log in or authorize with Crossbeam.
4. Next > select the correct organization to sync with Salesforce > Next.
5. Click authorize to enter Salesforce credentials.
6. Click Finish.
7. You must Update Permission Sets after Authorize and Finish to complete reauthorization. (HC 8780741)
Upgrade gotchas:
- Previous Crossbeam Admin User permission set defaults to Crossbeam Setup User after upgrade. Any Crossbeam Setup User must also have Crossbeam credentials to upgrade and reauthorize.
- Users previously assigned no permission sets get an error after the upgrade until a permission set is assigned.
- Salesforce data push sync defaults to twice a day, every 12 hours; actual update times may vary. (HC 8780741)
- Authorization errors may be caused by Salesforce's September 2025 security update blocking "uninstalled" connected apps; see HC 12510571 (not in this group). (HC 8780741)
- Reauthorize from Crossbeam side: Integrations > Copilot for Salesforce row > three dots > Connection Details, or Reauthorize > Reauthorize button > redirected to Salesforce. (HC 3685976)

### 12.9 Salesforce reports and dashboards
- Crossbeam tab: Deal Navigator and Pipeline Generation inside Salesforce. (HC 9708718)
- Custom reports and dashboards: once the Salesforce Custom Object Integration is installed, overlap data is a custom object usable in any Salesforce report or dashboard. See Crossbeam 360 Dashboard guide (HC 10149634, not in this group). (HC 9708718)
- Ready-to-use report templates (Supernode only), organized by three use cases:
  - Source Opportunities: compare prospects to partners' customers to find ecosystem-qualified leads.
  - Influence Deals: open opportunities overlapping partners' customer bases.
  - Retain and Expand Customers: overlap between your customers and partners' customers.
- Templates and custom reporting require the Salesforce Custom Object Integration. The Salesforce Admin must share the Crossbeam Reports folder before templates are visible. (HC 9708718)

---

## 13. Attribution push to Salesforce

### 13.1 What it does
- When a rep completes a request in Crossbeam for Sales, they are prompted to let Crossbeam track the partner's attribution on the associated Salesforce opportunity, removing manual attribution entry. (HC 9180986)
- Reps mark Attribution on closed deals inside a conversation; it syncs automatically to Salesforce. (HC 9708718)

### 13.2 Requirements
- Supernode plan. Salesforce Admin required to set up. (HC 9180986)

### 13.3 Setup
1. Crossbeam must be connected to your Salesforce data source.
2. Crossbeam Integrations page > "Salesforce Attribution Push". A pop-up prompts you to connect Salesforce and download and install the Crossbeam Attribution package.
3. Install the Attribution Object package (link in article: login.salesforce.com/packaging/installPackage.apexp?p0=04tDn000000GDBi).
4. A banner says the managed package is not part of Salesforce's AppExchange partner program. Review contents: it contains only a small custom object.
5. Install for admins only is recommended to control access and permissions after install. You may need to give users access to the custom object.
6. Connect your partners' Account IDs from Salesforce, then Save Changes. Partner IDs can be edited or removed anytime in Crossbeam Settings.
7. When completing a conversation, choose from the drop-down next to Attribution in the Basic Info section. Saving populates attribution data in Salesforce.
(HC 9180986)

### 13.4 FAQ facts
- Attribution type (sourced or influenced) is sent with each opportunity. (HC 9180987)
- The attribution object is a second managed package, separate from the existing one. Install via the Integration Marketplace or the tile in Crossbeam Core. (HC 9180987)
- Four standard report types: Crossbeam Attributions; Crossbeam Attributions with Account; Crossbeam Attributions with Opportunity; Crossbeam Attributions with Partner. (HC 9180987)
- Each attribution record relates to the account you closed and the partner account (if included during setup). Crossbeam for Sales can pull opportunities from the CRM; a search field on the Request lets you change the associated opportunity, and this is pushed to Salesforce. (HC 9180987)
- "Add a Partner ID from Salesforce": entering Partner Account IDs makes attributions linkable to the partner record in Salesforce instead of by text name only. (HC 9180987)
- Sync timing: 30 minutes after initial setup, then every 12 hours. (HC 9180987)
- Deal amounts shown in USD converted at current exchange rates, not rates at deal close. (HC 9180986, HC 9180987)

---

## 14. Copilot for HubSpot

### 14.1 Requirements
- Connector or Supernode plan. (HC 8940278)
- Crossbeam for Sales must be configured before install. Check status via the Co-Sell icon (app.crossbeam.com/co-sell). If not configured, you will be asked to approve the data connection during Copilot setup. (HC 8940278)
- Users must have a Full Access seat and/or Sales seat. Installer must have Crossbeam Admin role or Crossbeam for Sales Manager role, with permission to Crossbeam Integrations. (HC 8940278)
- The installer must have the App Marketplace Access permission set in HubSpot. Contact the HubSpot Super Admin. (HC 8940278)
- If a user is not on the Default View in HubSpot, Copilot is not added automatically. The HubSpot Super Admin must assign the Crossbeam tile under Record Customization in HubSpot settings. (HC 8940278)
- Setup time estimate under 30 minutes. (HC 8940278)

### 14.2 Install
1. Crossbeam: Data icon > Integrations > Crossbeam Copilot for HubSpot tile > Install.
2. New window: choose an account > Choose Account > confirm > success confirmation.
3. Copilot appears on the right side when viewing a company in HubSpot. (HC 8940278)

### 14.3 Rep usage
- Card on the right side lists overlapping partners for the account. View All opens a modal with Account, Partners, Contacts, and Plays tabs. Actions under Plays or Contacts jumps to those tabs. (HC 8940278)
- Users without a Sales seat see a Request Access view that emails the admin. Without a Crossbeam user seat, tabs are not accessible. (HC 8940278)

### 14.4 Migration to new HubSpot App Cards (required by a HubSpot platform change)
- Legacy CRM Card is labeled "Crossbeam"; new App Card is labeled "Crossbeam Copilot". Both can run side by side during migration. (HC 16764911)
- Starting September 30, the old CRM Card links out to the migration article. After October 31, legacy cards are no longer supported. (HC 16764911)
- Permissions: customizing a record view and managing Connected Apps require HubSpot Super Admin or a permission set including App Marketplace Access and Account Customization. (HC 16764911)
Steps:
1. Add the new card: HubSpot CRM > open a record > Customize (right sidebar) > select the default view or the team's specific view > + icon > search Crossbeam > select Crossbeam Copilot HubSpot App Card > Save and exit.
2. Confirm: refresh the record; both legacy and new cards load; the new one is labeled Crossbeam Copilot.
3. Uninstall legacy: settings gear > Integrations > Connected Apps. Two apps appear: the new connection named "Crossbeam" (powering the migrated card) and the legacy app named "Crossbeam Copilot". Select the legacy app > Uninstall > type `uninstall` to confirm.
4. Verify: reopen the record; only the new Crossbeam Copilot HubSpot App Card remains.
(HC 16764911)

Gotcha: naming is inverted between the card and the Connected App. The card you keep is labeled "Crossbeam Copilot", but in Connected Apps the app to keep is "Crossbeam" and the legacy app to uninstall is "Crossbeam Copilot". (HC 16764911)

---

## 15. Copilot for Chrome

- Shows partner overlap data (matching partners and shared Populations) while browsing websites in Chrome. (HC 4779242)
- Installable by the Admin role and/or Partner Manager role. (HC 4779242)
- Setup: Integrations > Crossbeam Copilot Chrome tile under Recommended > Settings Gear next to Install for Universal Copilot settings > Save. Then click the tile > Install to open the Chrome Web Store listing and complete install. Sign in to Crossbeam after installing. (HC 4779242)
- Runs in the background; when a visited site matches Crossbeam data, a circle notification appears on the Copilot icon. (HC 4779242)
- Supported contexts: Microsoft Dynamics (Account or Opportunity tab), LinkedIn and LinkedIn Navigator (company or user profile), Salesforce (Account, Opportunity, Contact records), HubSpot (Company, Deal, Contact records). Contact support to request other sites. (HC 4779242)
- The Gong Activity Timeline (Partner Mentions) surfaces in Crossbeam and the Copilot Chrome Extension. (HC 9167881)

---

## 16. Copilot for Gong

- Requirements: Gong Admin role; Crossbeam Core Admin role; Supernode plan; Gong Engage subscription. (HC 9167881)
- Two distinct Gong features: Activity Timeline (Partner Mentions) on Connector or Supernode with no Gong Engage required, surfacing in Crossbeam and the Chrome extension; and Copilot for Gong, which requires Gong Engage and Supernode. (HC 9167881)
- Setup follows the same process as the Gong Inbound Integration (HC 8365716, not in this group), then return to Integrations to configure Universal Copilot settings. (HC 9167881)
- Rep access: Gong > Engage icon > Accounts > on the Account page click Crossbeam to open Copilot. (HC 9167881)
- Delete: Integrations > Copilot for Gong row > three dots > Delete Integration > Cancel or Delete. (HC 9167881)
- Setup time estimate under 30 minutes. (HC 9167881)

---

## 17. Copilot for Outreach

- Supernode only. Only Outreach users with the admin role or a custom role allowing app installation can set it up. (HC 9579063)
- Use cases: account intel via Message Partner and co-sell templates; deal acceleration and multi-threading for stuck deals. (HC 9579063)
- Setup: Integrations > Crossbeam Copilot for Outreach tile under Recommended > Settings Gear (Universal settings) > Save > Install (opens Outreach Marketplace). (HC 9579063)
- Add tile: Outreach Account Overview > three dots > Customize Layout or New Layout > Add Tiles > Sales Intelligence & Data > Crossbeam Copilot > resize > Save. (HC 9579063)
- A Crossbeam Copilot for Outreach tab also appears on Opportunity, Contact, and Account objects. (HC 9579063)

---

## 18. AI Recommended Plays

- Located under the Account tab (Run a Recommended Play) and the Plays tab. Click Generate AI Playbook; the model returns concise bullet-point next steps. (HC 9596637)
- Thumbs up or down sends feedback to the product team. Regenerate produces a new play using a different partner, or another contact within the same partner org if it is the only eligible option, and suggests different engagement approaches. (HC 9596637)
- Once generated for a play, the steps persist in the Plays tab. (HC 9596637)
- Prioritization: plays are ranked by level of impact. Example: if a partner recently won the account, that partner is prioritized to leverage timing. (HC 9596637)
- Data safety: PII sent to the LLM is obfuscated; data sent cannot be used by the LLM provider. (HC 9596637)
- Plan: Connector or Supernode. (HC 9596637)

---

## 19. Developer documentation

### 19.1 Scope note
The developer articles in this group are the Crossbeam MCP Server (HC 12601327) and the SCIM Integration Guide (HC 12548850). No article in this group documents the Crossbeam REST API, API key authentication, REST base URLs, pagination, API rate limits, or webhooks. The only REST-adjacent facts present are the third-party domains the Salesforce app calls (api.crossbeam.com, auth.crossbeam.com) (HC 9209268). Record export impact: configuring Universal Copilot settings does not count toward record export limits (all Copilot articles); the MCP article does not mention record export limits, and MCP consumption is metered in Crossbeam Credits instead.

### 19.2 Crossbeam MCP Server
Availability and plans:
- As of September 1 (the FAQ specifies September 1, 2026), MCP is generally available on all plans including Free and Connector, and Crossbeam Credit metering is live. (HC 12601327)
- Full Access or Sales seat required to connect. (HC 12601327)
- Admin control by role: Settings > Roles & Permissions > Edit next to a role > MCP permission > Access or No Access. All roles default to Access. (HC 12601327)

Credits:

| Plan | MCP access | Annual Credits |
|---|---|---|
| Free | Yes | 50/yr |
| Connector | Yes | 500/yr |
| Supernode | Yes | 2500/yr |
| Enterprise | Yes | 5000/yr |

- Credits measure ecosystem data moving from Crossbeam into AI tools. Pooled across the org, not per user; anyone with a qualifying seat draws from the same balance. Reset annually, no rollover. (HC 12601327)
- Admins monitor consumption on Plan & Billing, broken down by MCP tool calls and active users by week, month, or all time. Only admins see the org-level usage view. (HC 12601327)
- Today Credits meter MCP only; they may expand to other AI access over time. Full details in the Credits FAQ (HC 15588582, not in this group). (HC 12601327)

Server specifics:
- Endpoint: `https://mcp.crossbeam.com/mcp`
- Transport: Streamable HTTP
- Auth: OAuth 2.1 with PKCE, Dynamic Client Registration (DCR)
- Tools: read only
- Technical docs and changelog: developers.mcp.crossbeam.com
(HC 12601327)

Tools:

| Tool | What it returns |
|---|---|
| `find_overlapping_accounts_and_leads` | Accounts shared with one or more partners; filter by partner, population, segment, partner score; can run ecosystem-wide |
| `get_account_context` | Unified view of one of your accounts: details, owner, population membership, custom fields. Lookup by domain, CRM record ID, or company name |
| `find_partner_shared_contacts` | Partner-shared contacts at an account: decision makers, economic buyers, executive sponsors, other key contacts |
| `find_new_accounts` | Pipeline Generation accounts, including net new accounts not in your CRM |
| `get_partner_overlaps_shared_context` | CRM fields a specific partner shares on an account, standard and custom mapped fields (for example account tier, renewal date) |
| `find_partner_recommendations` | Ranked partner suggestions for an open opportunity, same engine as Deal Navigator |
| `find_overlapping_partners` | Which partners have a given account in their data |
| `get_partner_context` | Overlap counts, open deals, potential revenue, partner score, win rate, deal size, recency of activity. Filter by partner name, tag, region |
| `get_ecosystem_activity` | Recent partner activity latest to oldest. Three event types: partner deals opened, partner deals closed won, recent greenfield signals (partner closed a deal on a company not in your CRM). Can include partner CRM contact context when sharing is enabled |
| `get_list_link` | Shareable Crossbeam list link from plain language, single-partner or ecosystem-wide |
| `search_crossbeam_knowledge` | How Crossbeam works and ELG best practices from help docs, ELG Insider blog, and the Ecosystem-Led Growth book |
| `get_partner_suggestions` | Companies you do not yet partner with, based on ecosystem fit, powered by Partnerbase data, with an invite link |

(HC 12601327)

- Owner and decision-maker contacts are only surfaced when those fields are being shared by the partner. (HC 12601327)

Connecting clients:
- Claude.ai: native connector. Requires a Claude plan that can connect remote MCP servers. Team and Enterprise: only Workspace Owners and Primary Owners add it (Organization Settings > Connectors > + > search Crossbeam > Add to your team); members then go to Customize > Connectors > Connect and authenticate individually. Individuals: Customize > Connectors > + > Crossbeam > Connect > OAuth > accept permissions. Tools can be toggled at Customize > Connectors > Crossbeam and per conversation from the Search and tools menu. Disconnect from Customize > Connectors. The same connection works on Claude for iOS and Android. Claude only accesses data the user has permission to access. (HC 12601327)
- ChatGPT: native connector in the plugin directory, any paid user. Settings > Plugins > Browse Plugins > Crossbeam > Connect > OAuth. It may not run automatically; invoke with @Crossbeam or + > More > Crossbeam. (HC 12601327)
- Glean: only Glean admins. Admin Console > Platform > Actions > Add actions > MCP servers tab > Crossbeam (under Connection verified) > Crossbeam MCP > Initiate connection and authenticate > Enable actions > Edit settings (Chat, Agents, Platform) > Save. Users then use Glean Assistant or add tools via Plan + Execute in Agent Builder. (HC 12601327)
- Gong AI agents / Agent Studio: only Gong admins. Admin Center > Settings > MCP connections (under Ecosystem) > Explore connections > Crossbeam MCP Server > Connect > toggle Authentication required > choose Shared access or Personal access > optionally toggle tools > Connect and authenticate. (HC 12601327)
  - Personal access: each user authenticates with their own Crossbeam account; data reflects their seat and permissions.
  - Shared access: one person authorizes; everyone in Gong sees what the authenticating account can see, regardless of their own seat or permissions. Governance gotcha. (HC 12601327)
- Other tools: any MCP-capable client that can add a custom server by URL, using `https://mcp.crossbeam.com/mcp` and Crossbeam credentials. Examples listed: n8n, Microsoft Copilot, LibreChat, Amazon Quick, Tines, Cursor. (HC 12601327)
- Native connectors exist for Claude, ChatGPT, Glean, Gong, Superhuman, and Outreach. (HC 12601327)

### 19.3 SCIM provisioning
Scope and prerequisites:
- Automates provisioning, attribute updates (name, email, roles), deprovisioning (deactivation), and role-based access enforcement from IdPs such as Okta, Azure AD, OneLogin. (HC 12548850)
- Enterprise plan only. Cannot be completed through the app interface alone; contact Crossbeam Support to confirm availability, have SCIM enabled, and obtain endpoint and token. (HC 12548850)
- SSO must already be configured (HC 4477745, not in this group). (HC 12548850)
- Roles are assigned in the SCIM payload via `core_role` and `sales_role`. SCIM Groups API role management is not yet supported. (HC 12548850)

Configure in Crossbeam:
1. Organization Settings (app.crossbeam.com/organization/settings) > Login Options. It has two areas: Single Sign-On (SSO) and SCIM Provisioning. SCIM appears only after SSO is configured.
2. Toggle On SCIM Configuration. Crossbeam generates a SCIM bearer token. Copy and store it securely for the IdP.
3. Set requirement level: Not Required or Required. Start with Not Required, switch to Required once provisioning works.
4. Save Settings.
(HC 12548850)

Recommended rollout: identify roles via the roles endpoint, test with a small user group, then enable enforcement. After enforcement, users can only access Crossbeam if provisioned through SCIM and manual user management in the UI is disabled. (HC 12548850)

Authentication: `Authorization: Bearer <your-scim-token>` on every request. (HC 12548850)

Endpoints (SCIM 2.0, case-insensitive paths such as /Users or /USERS):
- `GET /v1/scim/{sso-config-id}/users` list users
- `POST /v1/scim/{sso-config-id}/users` create user
> Path shorthand: `{SCIM_USERS}` means `/v1/scim/{sso-config-id}` followed by `/users`. Written this way because the plugin build gate reads the literal path as a home folder.

- `GET {SCIM_USERS}/{user-id}` get user
- `PUT {SCIM_USERS}/{user-id}` replace user
- `PATCH {SCIM_USERS}/{user-id}` update user
- `DELETE {SCIM_USERS}/{user-id}` delete user
- `GET /v1/scim/{sso-config-id}/roles` list available roles (metadata, not a SCIM endpoint)
- A Postman collection "SCIM 2.0 CROSSBEAM.postman_collection.json" is provided.
(HC 12548850)

User object, required attributes: `userName` (email, primary identifier), `active` (boolean), `externalId`, `displayName`, `name` with `givenName` and `familyName`, `emails` array with `value`, `type` (for example "work"), `primary`. (HC 12548850)

Crossbeam extension `urn:ietf:params:scim:schemas:extension:crossbeam:2.0:User`: `core_role` (UUID, optional), `sales_role` (string, optional). Each user must have a core_role or a sales_role or both; a user with no role cannot be created. (HC 12548850)

Roles endpoint response shape: `core_roles` array (label, description, value as role UUID) and `sales_roles` array (for example label Manager, value `partner-manager`). Core roles are org-specific, managed in the Crossbeam app (app.crossbeam.com/roles), and cannot be managed via SCIM. Sales roles are predefined: `partner-manager`, `co-seller`, `viewer` (see section 1.3). (HC 12548850)

Example create payload uses both schemas, userName the user's email address, active true, a core_role UUID, and sales_role `co-seller`. (HC 12548850)

Seat quota validation:
- Any user with a `core_role` (with or without sales role) consumes one core seat.
- A user with only a `sales_role` consumes one sales seat.
- Over quota returns a 400 with scimType `overquota`. (HC 12548850)

Audit logging: all SCIM operations logged; User shown as "System (SCIM)" (`system@SCIM`); actions create, update, delete; details include before and after user states including active status and roles. (HC 12548850)

---

## 20. Troubleshooting

| Symptom or error | Cause | Fix | Source |
|---|---|---|---|
| Partner not listed under Enabled Partners | Partner not yet activated for Sales | Click Manage under Crossbeam to search for and add them | HC 6699011 |
| Get Intel button displays an X | Partner not enabled for co-selling | Admin enables the partner and configures co-selling templates in Sales Settings | HC 6699011, HC 3685976 |
| Get Intel button does not display | Partner not enabled for co-selling by admin | Contact Crossbeam admin | HC 9708718 |
| Slack channel missing from Manage Shared Channels dropdown | Channel not a Shared Slack Channel, partner not fully joined, or private channel without the app added | Confirm Slack Connect channel and partner joined; add the app via channel name > Integrations > Apps; click refresh icon | HC 6699011, HC 8095694 |
| Cannot install the Slack app | Insufficient Slack permissions | Use the option to send a request to your Slack Administrators; verify correct Slack instance in top-right dropdown | HC 8095694 |
| All notifications arriving by email | Slack not configured | Configure Slack in Sales Settings; notifications then default to Slack | HC 6699011, HC 8345696 |
| Slack notifications not available to a rep | Admin-level alerts config | Admin configures Settings > Sales Settings > Alerts | HC 9708718 |
| Error when logging in via SSO | Seat not assigned, or SSO misconfigured | Admin confirms Sales seat or Full Access seat is assigned and SSO settings are correct | HC 9708718 |
| Copilot shows preview with limited data / Request Access | User has no Sales seat | User clicks Request Access; admin assigns seat from Settings > Team > Seat Request tab; user clicks Accept Invite in Copilot | HC 9708718, HC 3685976 |
| HubSpot Copilot tabs not accessible | No Crossbeam user seat | Click Request Access; admin assigns seat | HC 8940278 |
| Copilot login fails in Safari | Safari Prevent Cross-Site Tracking | Safari > Settings > Privacy > uncheck Prevent Cross-Site Tracking, then retry | HC 3685976, HC 8940278, HC 9167881 |
| Copilot for Salesforce Contacts and Plays tabs unavailable, prompt to contact Salesforce Admin | Trusted URL not configured or user lacks permission sets | Salesforce Admin with Crossbeam Setup User adds Trusted URL https://app.crossbeam.com, CSP Context Lightning Experience Pages, frame-src; Validate | HC 3685976, HC 8986760 |
| Plays tab has no or few plays | Partner not sharing account owner name and email, or not sharing Customer and Open Opportunity Populations and opportunity data | Ask partner to share those populations and owner fields | HC 8986760 |
| Overlaps missing in Copilot for Salesforce | Population not sourced from Salesforce | Only Salesforce-sourced Populations display there | HC 3685976 |
| Some partner or own data missing in every Copilot | Unchecked in Universal Copilot settings | Integrations > Copilot row > Settings drawer, re-check data or partners, Save | HC 9167877, HC 3685976 |
| Cannot open Copilot for Salesforce Settings (gear) | Missing Crossbeam Setup User permission set | Assign Crossbeam Setup User | HC 3685976 |
| "Open in Crossbeam" button hidden | User has Crossbeam Report User or Crossbeam Copilot Viewer, or Account User without Core role | Assign the appropriate permission set | HC 8780741 |
| User sees that accounts overlap but no details | Crossbeam Copilot Viewer permission set | Assign Crossbeam Account User if details are needed | HC 8780741 |
| Error for users after Salesforce app upgrade | Users previously had no permission set | Assign one of the Crossbeam permission sets | HC 8780741 |
| Cannot upgrade or reauthorize Salesforce app | Crossbeam Setup User lacks Crossbeam credentials, or setup user lacks Crossbeam Setup User permission set | Ensure the user has the permission set and a Crossbeam login | HC 8780741 |
| Reauthorization appears incomplete | Permission sets not updated after Authorize and Finish | Update Permission Sets | HC 8780741 |
| Errors connecting Salesforce to Crossbeam | Salesforce September 2025 security update blocking "uninstalled" connected apps | Follow HC 12510571 | HC 8780741 |
| Salesforce data or attribution not updated yet | Sync cadence every 12 hours (attribution first sync 30 minutes after setup) | Wait for next sync | HC 8780741, HC 9180987 |
| Attribution shows partner as text only | Partner Account IDs not added | Add Partner IDs from Salesforce in Attribution Push settings | HC 9180987 |
| Users cannot see Attribution object | Package installed for admins only | Grant users access to the custom object | HC 9180986 |
| Banner: managed package not part of Salesforce AppExchange partner program | Expected for Attribution package | Review contents (small custom object) and proceed | HC 9180986 |
| Report templates not visible in Salesforce | Crossbeam Reports folder not shared, or Custom Object Integration missing | Salesforce Admin shares folder; install Custom Object Integration | HC 9708718 |
| Copilot or setup wizard not visible in Salesforce Classic | Lightning only | Add the Crossbeam custom object to Account, Opportunity, Lead layouts | HC 9209268 |
| Salesforce install blocked at third-party access | Domains not approved | Approve api.crossbeam.com, auth.crossbeam.com, login.salesforce.com, sentry.io, test.salesforce.com | HC 9209268 |
| HubSpot Copilot not on record | User not on Default View | HubSpot Super Admin assigns tile under Record Customization | HC 8940278 |
| Asked to approve data connection during HubSpot install | Crossbeam for Sales not configured | Approve, or configure Crossbeam for Sales first (check Co-Sell icon) | HC 8940278 |
| Cannot add HubSpot card or manage Connected Apps | Missing HubSpot Super Admin or App Marketplace Access plus Account Customization | Get HubSpot Super Admin | HC 16764911, HC 8940278 |
| Legacy HubSpot card links to help article | After September 30 migration notice | Add the new Crossbeam Copilot App Card, uninstall legacy app (type `uninstall`) | HC 16764911 |
| Two Crossbeam cards on HubSpot record | Migration in progress | Uninstall legacy app "Crossbeam Copilot" in Connected Apps | HC 16764911 |
| Crossbeam Copilot for Gong unavailable | No Gong Engage or not Supernode | Obtain Gong Engage and Supernode; Activity Timeline works on Connector without Engage | HC 9167881 |
| Cannot install Outreach Copilot | Not Supernode, or Outreach user lacks admin or app-install role | Upgrade; use Outreach admin | HC 9579063 |
| MCP authorization issues | Stale or failed OAuth connection | Disconnect and reconnect Crossbeam in the AI tool's connector settings; then contact Crossbeam point of contact or the Crossbeam services inbox (services at crossbeam.com) | HC 12601327 |
| User cannot connect MCP | Role set to No Access, or no Full Access or Sales seat | Admin sets MCP permission to Access in Settings > Roles & Permissions; assign seat | HC 12601327 |
| ChatGPT does not use Crossbeam | Connector not invoked in that conversation | Type @Crossbeam or use + > More > Crossbeam | HC 12601327 |
| Claude Team member cannot find the connector | Owner has not enabled it | Workspace Owner or Primary Owner adds it in Organization Settings > Connectors | HC 12601327 |
| Gong users see data beyond their own permissions | Connection set to Shared access | Switch to Personal access | HC 12601327 |
| SCIM section not visible in Login Options | SSO not configured or SCIM not enabled for org | Configure SSO; contact Crossbeam Support (Enterprise only) | HC 12548850 |
| SCIM `"detail": "No more core seats available: you need to get more seats"` with `"scimType": "overquota"`, `"status": "400"` | Seat quota exceeded | Get more seats, as the error states; note a user with only a sales_role consumes a sales seat, not a core seat | HC 12548850 |
| SCIM `400 Bad Request` | Invalid data, missing attributes, or exceeded seat quota | Check required attributes and that core_role or sales_role is present | HC 12548850 |
| SCIM `401 Unauthorized` | Invalid or missing SCIM token | Send `Authorization: Bearer <your-scim-token>` with the token generated in Login Options | HC 12548850 |
| SCIM `404 Not Found` | User or organization not found | Check sso-config-id and user-id | HC 12548850 |
| SCIM `409 Conflict` | User already exists | The user is already provisioned; manage the existing user record rather than creating it again | HC 12548850 |
| Users locked out after SCIM enforcement | Not provisioned through SCIM | Provision via IdP; manual UI management is disabled once Required | HC 12548850 |
