<!-- Library file for crossbeam-admin-reference.md. Source: Crossbeam Help Center, extracted September 25th, 2026. Cite (HC number); confirm in-app when a screen may have moved. -->

# Crossbeam Admin Reference B: Partners, Data Sharing, Collaboration, Privacy, Security, Account Management

Source: 54 Crossbeam Help Center articles. Citations give the article number, for example (HC 4236547). Where articles disagree, both statements are given and flagged.

---

## 1. Core Data Sharing Model

### 1.1 Trust model
- Every partnership is dual opt-in: one company invites, the other must accept before any data can be shared. Nothing is shared automatically (HC 9956727, HC 3160400, HC 13066154).
- Syncing a CRM or uploading a CSV shares nothing. Data stays private until you configure sharing (HC 13066154).
- Data is shared only when: (a) both sides accepted the partnership; (b) you chose which Populations to share; (c) you configured which fields are shared under which matching conditions (HC 13066154).
- Crossbeam never shares raw imported data, only Populations (filtered subsets). Even after connecting, nothing is shared until you confirm or configure rules for that partner (HC 3160400).
- Non-matching records stay private unless you choose to share non-overlapping accounts (HC 13066154). Partners never see your full customer or pipeline lists unless you choose All Accounts (HC 13066154, HC 4236660).
- Populations can be hidden or revoked per partner at any time; data can be removed from Crossbeam at any time (HC 9956727, HC 13066154).

### 1.2 Vocabulary
- Populations: segments of your data used to find overlaps. Sharing Defaults: the per-Population starting setting applied to every partner without a custom setting. Sharing Settings: per-partner settings. Overrides: partner-specific settings that differ from the default (HC 4236547, HC 9389961, HC 4236660).
- Data Sources: Salesforce, HubSpot, Microsoft Dynamics, Snowflake, CSV, Google Sheets. Crossbeam encrypts all data (HC 4236547).
- Overlaps: companies or contacts known to both partners. Greenfield: your accounts that do not overlap with a partner, exposed only by All Accounts (HC 3160400, HC 4236619).

### 1.3 Sharing levels
| Level | Partner sees | Best for |
|---|---|---|
| All Accounts | All accounts, overlapping and non-overlapping (Greenfield) | Pipeline generation, discovery |
| Overlapping Accounts | Only accounts in both datasets | Account mapping (required for it), collaboration |
| Counts Only | Only the number of overlaps | High-level visibility |
| Hidden | Nothing | Sensitive or internal-only data |
(HC 4236660, HC 4236619)

- Legacy names in older articles: Overlap counts = Counts Only; Share overlaps / Sharing overlaps = Overlapping Accounts; Share all = All Accounts. Older hide method: turn off `Share your Population` for all partners, or click the unshare icon next to the Population for one partner (HC 4236547, HC 9389961).
- All Accounts is not available on the Free plan (HC 4236660).
- On Enterprise plans only admins can configure sharing levels; others are view-only (HC 4236660).
- Field Presets and Dynamic Shared Lists require Overlapping Accounts or All Accounts (HC 11583486, HC 4236660, HC 14546228).
- You can start a partnership with only counts visible even if your default shares fields (HC 4236547).
- Creating any Population prompts you to set a sharing default (HC 4236619).

### 1.4 How it evaluates
- Your setting on a Population governs how it appears when it overlaps with any of the partner's Populations (HC 4236547).
- Example: Customers default = Counts Only; override for partner Holver = Share Overlaps with Account Name and Website. Holver sees name and website of overlaps; all other partners see counts (HC 4236547).
- One-way: you set Counts Only, partner shares Company Name. You see which of your Prospects are their Customers; they only see that 1 of your Prospects is their Customer (HC 9956727).

---

## 2. Where Sharing Is Managed

### 2.1 Sharing Hub (primary)
- Path: Data > Sharing Settings. Replaces the old Default Sharing Settings page; prior configurations preserved (HC 4236660).
- Table: each Population, sharing level, field preset, and `Using Default` count (partners on the default). Filters: Population Type (Customer, Prospect, Open Pipeline, and so on), Sharing Level, Field Presets (HC 4236660).
- Click a Population: partners with custom settings (overrides) at top, default users below, with level, preset, and partner tags. Row actions: `↺ Reset to default` (removes override), `↗ Open partner settings` (HC 4236660).

### 2.2 Bulk edits
- By Population: Data > Sharing Settings > filter (optional) > check Populations > `Bulk Edit` > level and preset > `Save` (HC 4236660, HC 11583486).
- By Partner: Data > Sharing Settings > click Population > filter by partner tag, level, or preset > check partners > `Bulk Edit` > level and preset > `Save` (HC 4236660).
- Alternate: Data > Populations > three dots > `Partner Specific Sharing` > check partners > `Bulk Edit` > `Save` (HC 11583486).
- Bulk edits change defaults only. Partners with overrides keep their settings (HC 4236660, HC 11583486).
- Tag-filtered bulk changes are not applied to partners tagged later; reconfigure manually in the Hub (HC 4236660).
- Crossbeam recommends All Accounts for pipeline generation, Overlapping Accounts for account mapping (HC 4236660).

### 2.3 Populations workspace
- Data > Populations > click the `Sharing Setting` in a row > choose level > `save`. The modal's `Field Presets for Selected Population` section picks a preset or keeps the recommended Crossbeam default fields. Fields are configured per data source (HC 4236619).

### 2.4 Sharing Dashboard
- Partners > Sharing Dashboard (HC 9389961).
- `Your Population Default Setting`: rotating cards for Standard and Custom Populations showing type, number of partners on the default, setting, and shared fields on hover. Pencil opens the Sharing Default modal (HC 9389961).
- `Sharing Settings with Partners`: filters `All`, `Using Default`, `Using Custom`, search, Populations, Sharing Settings (Sharing data, Counts, Hidden), Overrides. Expand a partner to see each Population's setting and customization, then what the partner shares with you (hover for fields, `Request Data` if not sharing). `Edit` opens the partner's settings (HC 9389961).

### 2.5 Partner Detail Page
- Partners > partner > `Settings` (or `Sharing Settings` button). Contains `Shared with You`, per-Population level and preset, `Team Access`, and `Delete Partnership` (HC 4236660, HC 11583486, HC 10438608, HC 8545332).
- See what you share with a partner: Data > Sharing Settings > Population > `↗` on the partner row (HC 4236660).

### 2.6 At invite acceptance
- The invite screen has an `Org Sharing Defaults` toggle. Off: the `Save` button becomes `Sharing Settings` so you can set this partner's sharing before accepting (HC 3160223, HC 11583486).

---

## 3. Field Presets

- A saved, reusable set of fields to share, applicable across partners and Populations (for example tech vs. channel). Built-in preset: `Crossbeam Default`. Only available at Overlapping Accounts or All Accounts (HC 11583486, HC 4236660).
- Presets are chosen from a dropdown; each option has a pencil to edit it (HC 11583486).
- Create (`Manage > Create Field Preset` > name > fields > `Create`) from: Data Sources settings gear > `Field Presets`; Sharing Dashboard pencil > `Field Presets for Selected Population`; Data > Populations three dots > `Partner-specific Sharing`; Sharing Hub > Population > preset in row (HC 11583486).
- Who uses a preset: Sharing Hub > Population > `Field Preset` filter; or per partner on Partner Detail Page > Settings. All presets for a source: data source gear > `Field Presets` (HC 11583486).
- Apply: Sharing Dashboard `Edit`; Partner Detail Page > Settings; Sharing Hub partner row dropdown > `Manage`; or during invite acceptance (HC 11583486).
- Edit: pencil > adjust > `Create`. Changes apply to every partner using it; check usage first (HC 11583486).
- Delete: `Manage` or pencil > `Delete Preset` > `Delete`. Permanent. Populations using it switch to `Crossbeam Default` (HC 11583486).

---

## 4. Populations (sharing-relevant)

- Data > Populations. Pencil opens the Population Builder; `Save Changes` (HC 4236619).
- Three-dot actions: `Duplicate` (same description and filters), `Convert to Custom Population`, `Export Population`, `Delete Population` (permanent; removes it from active account mapping reports and partner sharing configurations) (HC 4236619).
- Population Management permission (Enabled) needed to create, edit, delete (HC 4292722).
- Account Mapping Matrix on the Partner Detail Page: your Populations on the left, partner's across top, Standard then Custom; click a count for a report; toggle Total Overlaps vs. Potential Revenue (HC 3160224).

---

## 5. Data Sharing Requests

- Request: Partners > Partner List > partner > `Settings` > `Shared with You` > `Request Data` next to a Population > optional message > `Send Request`. Partner gets in-app plus email (if enabled) (HC 3976078). Also from the Sharing Dashboard (HC 9389961).
- Track outgoing: Partners > `Pending Requests` > filter `Share Requests` (HC 3976078).
- Incoming: same Pending Requests filter. From the email, `Go to Sharing Settings` opens the Partner Detail Page; find the Population; edit pencil under Sharing Defaults. After you save, the partner is notified in-app and by email (HC 3976123).
- For Copilot contacts, note that the request is for contact data (HC 9486432).
- Notification control: Settings > `Profile & Preferences` > `Data Notifications` > `Save changes` (HC 3976123).

---

## 6. Partner Connection Lifecycle

### 6.1 Discoverability
- Settings > `Organizational Settings` > `Discoverable` section > `Save Changes` (HC 5392236):
  - `Discoverable`: others can send you partnership requests.
  - `Make Users Discoverable`: users with Manage Partnership permissions receive requests directly; other companies see a list of your users.
- Partnerbase's Partner Tech Stack filter for Crossbeam shows only discoverable companies (HC 7128217).
- You can invite non-discoverable companies and companies not on Crossbeam. No limit on partner connections (HC 7128217).
- Universal Search (top of dashboard) finds existing and suggested partners, Populations, records, and offers `Invite Partner` (HC 5392236).

### 6.2 Sending invites
- Permission: Partner Invites Enabled (send, receive, accept); Disabled can only view (HC 4292722).
- Search: Partners > `+Invite Partner` > search > `Invite`. Email plus in-app notification; non-members land on registration (HC 3160222).
- Not in dropdown: type the name, supply company name, contact name, contact email (HC 3160222).
- Invite link: Partners > `+Invite Partner` / `Add Partners` > copy link. If the partner is on Crossbeam, clicking sends you an invitation to accept. If not, they register, then send you an invite, which you accept in Pending Requests (HC 3499611).
- Mobile: log in from a mobile browser; partner scans your QR code (sends invite by email and in-app) or you `Copy Link`. Invites can be accepted on mobile (HC 3160222, HC 3499611).
- Partner Activation CC (Connector, Supernode, Enterprise): when inviting an org that is not a paying customer, `Help your partner get started faster` appears; toggle on to visibly CC the Crossbeam partnersactivation inbox (partnersactivation at crossbeam.com), who will contact the partner to onboard. Not shown for paying orgs (HC 16547255).

### 6.3 Partner Invitations (bulk wishlist)
- All plans. Sending requires partnership management permission; others can view (HC 15421724).
- Partners > Invitations > `Upload Wishlist` > CSV > `Add to Wishlist`. Template in the modal. Columns: Company Name, Domain, Contact Email Addresses (optional, required for companies not on Crossbeam), Owner Name, Tags (HC 15421724).
- Row source: `From CSV`, `Direct Invite`, `From CRM`. Crossbeam flags which companies are already on Crossbeam (HC 15421724).
- `Bulk Invite` > `Send Invites`, maximum 100 per action (HC 15421724).
- Statuses: Not Invited, Pending, Accepted, Declined. When a wishlist company joins: `NEW` badge in `On Crossbeam`, counted in `Just Joined`, in-app plus email; badge clears when you invite or dismiss (HC 15421724).
- Filter by Crossbeam account, owner, status, tags; assign owners; bulk remove via `Actions` > `Remove` (HC 15421724).

### 6.4 Receiving, accepting, declining, revoking
- Invites arrive by email and in My Partners / Pending Requests. `Ignore` dismisses without notifying the inviter (HC 3160223).
- Accept: `View Invite` > optionally toggle `Org Sharing Defaults` off to set sharing > `Accept` (HC 3160223).
- Requests drawer (top of Invitations page): `Accept`, `Decline` with optional reason, or `Revoke` your own pending request (HC 15421724).
- Decline reasons: Legal or data privacy restrictions; Bad timing, reconnect later; No formal partnership in place yet; Not the right person; Other; Prefer not to say (shares nothing). Optional note up to 1,000 characters (HC 15421724).
- Declined invites show `View Reason` (who, reason, note). You can re-invite at any time from the wishlist row (HC 15421724).

### 6.5 Company verification
- Automated multistep check at registration using provided info and third-party data. Pass is instant; fail queues the account for manual verification and blocks app use until verified. You are still responsible for vetting partners before sharing (HC 3935700).

### 6.6 Deleting a partner
- Partner Detail Page > `Settings` > `Delete Partnership` > type `DELETE` > `Delete Partner`. Also a `Delete Partner` button in the left column (HC 8545332, HC 3160224).
- Permanent; removes the partnership and all data shared between you. Alternatives: set Populations to Counts Only or Hidden for that partner, or restrict fields with presets (HC 8545332).
- Static Shared List records remain, frozen, if the partner deletes their data source or stops sharing (HC 8345701).

### 6.7 Partner List and Detail Page
- Partner List: `+Add Partner`, list/grid toggle, search, sort by Name, Populations, Overlaps, Potential Revenue, Partnered Date, tag filters. Rows show Overlaps, Potential Revenue (open opps on shared accounts), Tags, Partnered Date (HC 3160224).
- Detail left column: Partner Impact, Overlaps, Potential Revenue, Total Attribution, Tags, Sharing Settings, Delete Partner. Partner Impact summarizes closed opps (Win Rate, Opportunity Size, Time to Close) with High, Medium, Low tier (HC 3160224).
- Potential Revenue: Connector and Supernode only; "Explorer Plan is View Only" (HC 3160224).

### 6.8 Partner Tags
- Maximum 80 tags. Permission: HC 5467749 says Partnerships set to `Manage`; HC 4292722 says Partner Invites `Enabled`.
- Add: `+Add Tags` on a Partner List row, or `Add Tags`/pencil on the Detail Page > `Save` (HC 5467749).
- Add many partners to a tag: Partners > `Filter` > ellipses on tag > `Add to Partners` > `Save`. Edit or red `Delete` from the same ellipses; changes apply to every partner with that tag (HC 5467749).
- Filter by clicking a tag or `Filter` with `AND` (all tags) or `OR` (any tag) (HC 5467749).
- Suggested schemes: Partner Type, Tier, Partner Account Manager, Region, Lifecycle Stage, Status, Specialization (HC 5467749).

### 6.9 Partner visibility (user access to partnerships)
- By request via CSM; Admin required (HC 10438608).
- Levels: `Manage Access` (view and manage access to all partnerships); `View Access` (see partnerships, customizable per partner); `Per-Partner Access` (no visibility unless granted or they created the partnership) (HC 10438608).
- By role: Settings > `Role & Permissions` > `Edit` > `Save Changes` (applies to existing and new users). Per partner: Partners > partner > `Sharing Settings` > `Team Access` > `Close` (HC 10438608).
- Partner Sharing permission only works on partnerships the user can access (HC 4292722).

---

## 7. Offline, Managed Offline, and Open Data Partners

### 7.1 Offline Partners (your upload)
- For partners without a Crossbeam account; data via CSV or Google Sheet (HC 8799966).
- Free: one Offline Partner with Standard Populations. Connector and Supernode: unlimited. Custom Populations for Offline Partners: Connector and Supernode (HC 8799966).
- Requires Offline Partners permission `Manage` (HC 8799966, HC 4292722).
- Add: Partners > `Add Partner` > `Add Offline Partner` tab > search > select > `Create Partner`; filter with `Offline` (HC 8799966).
- Data: Offline Partner > `Partner Data` tab > `Google Sheet` (paste URL, Google consent, choose sheet and tab, map columns, `Save`; syncs immediately then on the standard cadence) or `Upload CSV` (`Browse`, name, map Company Name and Website, `Upload`) (HC 8799966).
- Deleting a Google Sheet row does not delete the record in Crossbeam; delete from the Population (HC 8799966).
- Population: Partner Data tab > `Create` > name, type (Customer, Open Opportunity, Prospect, Other), `File`, description > `Continue` > filters > `Create Population` (HC 8799966).
- Mapping: Account Mapping > `+New` > list type > choose the Offline Partner > click a matrix overlap box (HC 8799966).
- Manage: `Edit` or `Delete` Populations; `Add Data` to append CSV rows; `Map Fields` to remap. Delete partner: Settings > `Delete Partnership` > `DELETE` (HC 8799966).
- Initial Record Export when setting up an integration counts toward your limit (HC 8799966).

### 7.2 Managed Offline Partners (deprecated)
- From August 19, 2026: still available but no data updates, and no new ones can be added. No required migration; Crossbeam recommends Open Data Partners (HC 11730520, HC 15453957).
- Were on all plans; Crossbeam-curated public data for players like Salesforce, AWS, Microsoft, SAP, Google Cloud; single `Customers` Population; not real accounts; badged; hideable; can still be invited. Updated twice a year from a curated Google Sheet. Added via arrow next to `Add Partner` > `Add Managed Offline Partners`, listed under `Offline` (HC 11730520).
- Do not count toward the ODP limit; existing Lists and reports keep working (HC 15453957).

### 7.3 Open Data Partners (ODPs)
- Crossbeam-maintained vendor customer data; no invite or agreement. One ODP auto-added at account creation based on your ecosystem profile (HC 15453957).
- Requirements: Full Access seat, connected CRM, configured Populations (HC 15453957).
- Limits: Free 1, Connector 1, Supernode 3, Enterprise 10. Product-level segmentation on Supernode and Enterprise only (HC 15453957).
- Connector's ODP applies to updated Connector plans with a platform fee; earlier packages must add platform capabilities. Free can swap its onboarding ODP once via support; other plans pick their own (HC 15453957).
- Customer Population only, no Prospect data. You can map your Customers, Prospects, Open Opportunities against it; see overlaps, Potential Revenue and Partner Score (plan-dependent); build Lists; hide it (HC 15453957).
- Products filter: `is` matches only accounts where that product is the sole one; use `contains` to include accounts with other products too (HC 15453957).
- Source: public "is-a-customer-of" signals (directories, tech stack listings, marketplaces, case studies, integration pages); refreshed daily per FAQ. Never built from your or any customer's Crossbeam data; kept separate from network data (HC 15453957).
- Add: arrow next to `Add Partner` > `Add Open Data Partners` > choose > `Add` (HC 15453957).
- Delete: ODP > `Settings` > `Delete partnership` (bottom left). Deleting does not free a slot; at the limit you must upgrade to add another (HC 15453957).
- `Replace with Open Data Partner` (single or bulk) on a Managed Offline Partner permanently deletes the original and its Lists, Tags, Populations; uses one ODP allocation that then cannot be swapped (HC 15453957).
- Vendors: 1Password, accessiBe, Airtable, Atlassian, AWS, Bitwarden, Brevo, BrowserStack, Calendly, Checkout.com, DigitalOcean, Duo Security, Dynatrace, ElevenLabs, Fastly, Freshworks, GCP, GitLab, HERE Technologies, HPE, IBM, Lovable, Mailgun, Microsoft, monday.com, MongoDB, New Relic, Odoo, PagerDuty, Pendo, Personio, Postman, Progress, Salesforce, SAP, SendGrid, Sentry, Slack, Sophos, Supabase, Vimeo, Wix, WP Engine, Zapier (list may change) (HC 15453957). (list abridged; full list in the cited article)

---

## 8. Shared Lists

### 8.1 Static Shared Lists
- Create on Connector or Supernode. Free is Invite Only but gets full access to a list it is invited to (HC 8345701).
- Requires Data Sharing enabled with the partner and Standard user level permissions (HC 8345701). Shared Lists permission `Manage` covers create, edit, delete, and list access (HC 4292722).
- Fixed, handpicked set of overlapping and non-overlapping accounts. Up to 50 records per add (HC 8345701).
- Independent of default Sharing Settings: everything on the list is shared except Opportunity Name, Stage, Amount, which only you see. Account owner is included automatically (HC 8345701).
- You can add a record if the partner shares data with you and you share at least overlap counts (HC 8345701).
- One partner per list; multiple internal collaborators per side. CSV-sourced records are static; CRM sources update. Partner edits push automatically with a notification. Records the owner removes disappear for the partner too (HC 8345701).
- Steps: open a list or `+ New` > select records > `Share with partner` > pick an existing list or `+ Create New List` (partner as Owner, name, description, `Share List`) > `Add Selected Records to List` (HC 8345701).
- In the list: drag columns by the dot handle; `Delete Rows`; add Custom Columns with `+` at the far right (edit via the horizontal lines icon); `Share` > names or emails > `Send Invites` or `Remove` teammates (HC 8345701).
- Find in Lists (triangle sharing icon; filter by partner or owner). Pencil to rename or `Delete List` (permanent) (HC 8345701).
- Emails for new list, new records, new note. Manage at Settings > Profile & Preferences > `Lists Notification` (HC 8345701).

### 8.2 Dynamic Shared Lists
- Filter-based, auto-updating (HC 14546228).
- Free: view and contribute only. Connector, Supernode, Enterprise: create, save, share externally (HC 14546228).
- Access by seat: Full Access Admin and Standard get Manage, Edit, Comment, View Only; Limited View Only. Sales Manager and Standard get Edit, Comment, View Only; Limited View Only; Sales seats cannot create or share (HC 14546228).
- Levels: Manage (create, edit, delete, share); Edit (create, edit, delete, Notes); Comment (view, Notes); View Only (HC 14546228).
- External sharing needs `Partner Shared Lists: Manage`; partner users with Manage can share within their own org. Making a column public needs Data Sharing permission (HC 14546228).
- Requirements: list scoped to one partner (Single Partner List or Custom List filtered to one partner); Population not Counts Only or Hidden; Data Sharing enabled; the Manage permission. Not available from the Account Mapping List view (HC 14546228).
- Steps: Lists > open or create Single Partner List > set filters (they lock at sharing, even for the owner) > `Save as a new list` (private until shared) > `Share` > `Share with a Partner` > users > Manage, Edit, Comment, or View Only > `Share`. Or `Your organization` with General Access `Everyone at your org` or `Only people invited` (HC 14546228).
- After sharing, owner filters are grayed out; anyone may temporarily narrow with AND for their session; OR and new filters blocked; nothing persists (HC 14546228).
- Columns: those saved before sharing are included; columns added after default to Private. Header dropdown > `Make Public` > confirm (immediate). Removing a public column removes it for the partner. You can share columns not in your sharing settings; sharing a list does not change underlying settings. Each org sees its own CRM view; no cross-org dedup (HC 14546228).
- Notes: both orgs, Manage/Edit/Comment can add, Enter saves, per-account per-list, unread bolded, included in exports (HC 14546228).
- No record limit. Dataset locked at share time: later Populations are not pulled in. One partner per list. `Duplicate` makes an unshared copy. `Delete` notifies the partner. If the owner leaves, access persists; an admin can delete and recreate (HC 14546228).
- Notifications on share, new Note, new account entering. Manage at Settings > Profile & Preferences > `Collaboration Notifications` (HC 14546228).

### 8.3 Partner Collaboration Session
- CSM-led call with you and a partner; complete the Partner Ecosystem Enablement Program first. Agenda: goals and use cases, sharing rules in place (and limits), reports, KPIs, action items. In-app review: Populations, partner connection, Sharing Settings and data requests, Partner Dashboard, Threads, Reports, Integrations. Recap actions and share the recording (HC 8770611).

---

## 9. Attribution

- Supernode feature. Path: `Attribution` in left menu (older: `Measure` > `Attribute`). Amounts converted to USD at current exchange rates, not rates at close (HC 8042999, HC 8301786, HC 11553885, HC 10440025).
- Permission: Attribution Manage, View Only, No Access (HC 4292722).
- Dashboard: Total Sourced, Total Influenced, Total Unattributed, Time to Close with and without Partners. Filters: account, Sales stage, Partner, Tags, dates, amounts; gear customizes metrics (HC 11553885).
- Accounts table: account, partners, type (Sourced, Influenced, Review Attribution), amount, stage, close date. Click an account for a side panel to change type or add partners; `Activity` shows interactions; Salesforce link appears if Attribution Push is configured (HC 11553885).
- Ecosystem Activities logged in the Activity tab and Record Timeline: adding contacts, notes on shared lists (yours or partner's), Copilot research, Slack messages and searches about a record (HC 10440025).
- Required Salesforce Opportunity fields: Name, Sales Stage, Amount, Closed, Won, Open Date, Close Date (HC 8042999).
- Required HubSpot fields: dealname__value, dealstage_label, amount__value, pipeline_label, days_to_close__value, hs_is_closed_won__value, hs_date_entered_closedwon__value, hs_date_exited_closedwon__value, hs_is_closed__value, createdate__value (HC 8301786).
- Change fields: Data > Data Sources > gear on the source. Added fields are yours only, not shared (HC 8042999, HC 8301786).
- Revenue Settings: Settings > `Organizational Settings` > `Revenue Settings` (HC 8042999, HC 8301786).
- Deleted or changed opportunity/deal: its attributed revenue drops out of stats. Missing amount or close date: excluded from the roll-up denominator (HC 8042999, HC 8301786).

**Salesforce Attribution Push** (HC 8042999):
- Only the Salesforce Admin can install. It is a second managed package.
- Data > `Integrations` > Salesforce Attribution Push > `Install`, or the package link login.salesforce.com/packaging/installPackage.apexp?p0=04tDn000000GDBi. Choose `Install for Admins Only`; banner says not part of AppExchange; `View Components` shows a small custom object; tick the Non-Salesforce Application acknowledgement; `Install`. Then check profiles for object access.
- Partner IDs: Integrations > Salesforce Attribution Push > `Settings` > enter 18-character Salesforce Account ID per partner > `Save Changes`; links attributions to the Partner Account instead of text name.
- Sync 30 minutes after setup, then every 12 hours.
- Crossbeam for Sales: completing a conversation lets you pick an Opportunity and Sourced, Influenced, or Neither; a "Crossbeam Attribution" record is created after the next sync.
- Report types: Crossbeam Attributions; with Account; with Opportunity; with Partner. Attribution type is included.

---

## 10. Gong Integration

- Since July 1, 2025, new Connector plan Outbound integrations cannot be created; earlier ones continue (HC 8365716).
- Activity Timeline (Partner Mentions): Connector and Supernode, no Gong Engage needed. Copilot for Gong: Supernode plus Gong Engage (HC 8365716).
- Requires Gong Admin, Crossbeam Admin, Connector or Supernode. Authorizer needs Activity Timeline `Manage` (HC 8365716, HC 4292722).
- Install: Integrations > Gong tile > `Install` > confirm account > authenticate Gong > choose and prioritize partners > Similarity Cutoff > `Finish` (HC 8365716).
- Similarity Cutoff default 90; lower it if mentions are missed. Use Gong Keyword Trackers for unique names (HC 8365716).
- Backfills 30 days, then monitors all new transcripts (HC 8365716).
- Manage: Installed Integrations > Gong > `Settings` > `Advanced Settings` > edit partners > `Finish` (HC 8365716).
- Mentions appear in the Record Timeline tab and Copilot Chrome Extension, and on Supernode the Attribution page; not in Copilot for Salesforce. With Attribution Push each attributed opp carries a Gong link (HC 8365716).

---

## 11. Ecosystem Intelligence in Copilot

- Aggregated, anonymized signals from standard role fields across network CRMs (HC 9486432).
- Contacts tab shows only contacts partners share with you; EI tags come from aggregate data but no shared contact means no tag shown. `Add to CRM` for missing contacts (HC 9486432).
- Tags: Opportunity Contact, Decision Maker, Primary Contact, Economic Buyer, Economic Decision Maker, Executive Sponsor, Technical Buyer, Popular Contact. Unlimited per contact; tagged contacts listed first (HC 9486432).
- Account tab > Account Highlights: range of companies that marked the account recently won, rolling 3 months (HC 9486432).

---

## 12. Seats, Roles, Permissions

### 12.1 Seats
- Settings > `Team` > Seat Summary shows Full Access assigned of total, and Sales assigned (HC 4292722).
- Full Access: all products. Sales: Crossbeam for Sales only. Integration: data sources, CRM connections, integrations only; user sees only `Data` in navigation (HC 3160294, HC 4292722).
- Free: 3 Full Access seats, no Sales seats. Connector: no minimum, no cap. Supernode: minimum 3. Supernode and Enterprise include one Integration seat outside seat limits (HC 4292722, HC 7897487).
- AI features using Crossbeam Credits require a Full Access or Sales seat (HC 4292722).
- Integration seat: `Invite User` > Seat Type `Integration`; or Edit pencil on a user > Seat Type `Integration` > `Save Changes`. You can temporarily convert a user to make integration changes, then revert (HC 4292722, HC 3160294).

### 12.2 Roles
- Full Access: Admin (highest; manages roles in Core and Sales); Standard (data sharing, reports, shared lists, attribution; Data Sources, Integrations, users view-only); Limited (all view only) (HC 4292722, HC 3160294).
- Sales: Manager (configures Sales, manages others' access); Standard (all Sales features, partner requests, Chrome extension, Copilot, alerts, lists, Deal Navigator, conversations, attribution; no Core); Limited (same but no partner requests or lists; no Core); No Access (HC 4292722, HC 3160294).
- Custom roles and groups: Supernode and admin (HC 4292722).

### 12.3 Permissions
Settings > Roles & Permissions > `Edit` on a role > set each dropdown > `Save Changes`. `Delete Role` in the modal. Only Admins assign (HC 4292722).

| Permission | Options |
|---|---|
| Activity Timeline | Manage (read and post), View Only, No Access |
| Applications | Manage, View Only, No Access (OAuth Applications) |
| Attribution | Manage, View Only, No Access |
| Audit Log | View Only, No Access |
| Billing | Manage (billing, credit usage, credit packs), No Access |
| Data Sources | Manage, View Only |
| Deal Navigator | View, No Access |
| Integrations | Manage, View Only |
| Offline Partners | Manage, View Only |
| Organization | Manage, View Only |
| Partner Invites | Enabled, Disabled (view only); needed for Partner Tags |
| Partner Sharing | Enabled (needs access to the partnership), Disabled |
| Population Management | Enabled, Disabled |
| Report Exports | Enabled (default), No Access |
| Reports | Manage (create, edit, export, delete), View Only (no export) |
| SSO | Manage, No Access |
| Shared Lists | Manage, No access |
| MCP | Access (default for all roles), No Access |
(HC 4292722)

- Record Exports permission is on by default; set No Access to restrict. List exports follow permissions (HC 8399864).

### 12.4 Team management
- Only Admins invite or edit roles (HC 3160294, HC 4292722).
- Invite: Settings gear > `Team` > `+Invite User` > seat type > emails > role > `Send Invites`. With SSO enabled, invites go directly to the user (HC 3160294).
- Reminders: 3 days after invite, 4 days after that, weekly for a month, then monthly up to 6 months total (HC 3160294).
- Edit via `Edit`; remove via trash can > `Delete` (HC 3160294).
- Seat requests (including those from HubSpot and Salesforce): Settings > Team > `Seat Requests` > filter > multi-select > `Approve` or `Reject` (HC 4292722, HC 3160294).
- Mobile: Home page > scroll past partner QR code > `Invite` > emails and role > `Invite` (HC 3160294).
- All admins gone: contact support (chat or the Crossbeam support inbox (support at crossbeam.com)) for a manual check (HC 10309518).

---

## 13. Plans, Billing, Credits

- Settings > `Plan & Billing`: plan, other plans, renewal date, seats, billing details. Self-serve on Free and Connector; Supernode and Enterprise via Sales or Account Success Manager (HC 4000710).
- Upgrade to Connector: `Upgrade` / `Upgrade to Connector` > payment option and seats > `Continue to Payment` > Stripe. Supernode or Enterprise: `Talk to Sales`, response within 24 business hours (HC 7897487, HC 4000710).
- Downgrade: `Downgrade` under Explore or Connector opens support chat (HC 7897487).
- Payment method: Next Invoice Amount box > `View Invoices`; `edit Payment Method` in Billing Details. Invoices: Plan Renewal Date box > `View Plan Details` > payment portal (HC 7897487).
- Auto-renews annually; cancel needs 30 days notice; no prorated refunds. Cancel via `Manage Plan` (support chat) or ASM (HC 7897487, HC 4000710).
- Connector seats: `Invite User`; if at max, prompted to buy; `Pay Now` charges saved method; prorated from purchase date. Remove seats via `Manage Plan`. Supernode/Enterprise seat changes via ASM or support (HC 7897487, HC 4000710).
- Crossbeam Credits: every plan; meter AI access to ecosystem data; org-wide pool, no per-user allocation; separate from Record Exports. Usage on Plan & Billing by tool calls and active users (week, month, all time); admins only. Extra packs for Supernode and Enterprise (self-serve or ASM or support): 10K for $1,000; 25K for $2,500; 100K for $9,000 (10% discount) (HC 4000710, HC 8399864).

**Plan gates from these articles**
- Free: 3 seats; 1 Offline Partner; 1 ODP; no Record Exports (except Account Mapping Pass); no All Accounts; Static Shared Lists invite-only; Dynamic Shared Lists view and contribute only (HC 4292722, HC 8799966, HC 15453957, HC 8399864, HC 4236660, HC 8345701, HC 14546228).
- Connector: 5,000 exports/yr; unlimited Offline Partners; 1 ODP; Shared Lists; Gong Timeline; Potential Revenue; Partner Activation CC (HC 8399864, HC 8799966, HC 15453957, HC 8365716, HC 3160224, HC 16547255).
- Supernode: minimum 3 seats; Integration seat; 3 ODPs with products; custom exports; Attribution and Push; Audit Logs; SAML SSO; custom roles; Copilot for Gong (HC 4292722, HC 15453957, HC 8399864, HC 8042999, HC 6172688, HC 4477745, HC 8365716).
- Enterprise: 10 ODPs with products; Integration seat; admin-only sharing level changes; SAML SSO per HC 4477745 (HC 15453957, HC 4236660).
- Partner visibility access levels: by request (HC 10438608).

---

## 14. Record Exports

- Moving enriched account-mapping data to warehouses, integrations, CRMs. Each record counts once per subscription term regardless of destinations, partners, overlaps, or updates (HC 8399864).
- Limits: Free none (Account Mapping Pass from a Supernode or Enterprise partner allows 100 records with that partner); Connector 5,000/yr; Supernode customizable; Enterprise customizable via Account Manager. CSV exports disabled at the limit. Resets annually on contract date; increase via `Talk to Sales` (HC 8399864).
- Record means: Salesforce, Dynamics, Snowflake Accounts and Leads; HubSpot Companies; CSV and Sheets all rows (HC 8399864).
- Excluded: Slack integration, all Copilots, Crossbeam for Sales (HC 8399864).
- Counts: initial export when setting up an integration; "New Accounts for You" List. Does not count: "New Accounts for Your Partner" List; updating or deleting existing CSV/Sheet rows. New CSV/Sheet data counts; re-uploading a deleted file counts again (HC 8399864).
- Integration settings show estimates based on matches, often higher than actual unique deductions (HC 8399864).
- Banners on Plan & Billing, Integrations, Populations at 90%; at 100% integration data flow is disabled. Admin email at over 75% with `Review my Account` (HC 8399864).
- Record Export Summary (Plan & Billing): allotted, remaining, renewal; unique records per integration and per Population (arrows to edit); 14-day volume; Recent Exports sortable by Date or Exported to (HC 8399864).
- At limit: exports blocked, existing exported data stops updating, integrations paused, no CSV or List exports (HC 8399864).
- Conserve: filter lists; tune integration settings; use Copilot and the Account Mapping Matrix; prefer CRM Populations over CSV (HC 8399864).

---

## 15. SAML SSO and Login

- Plan: HC 4477745 says Supernode and Enterprise; HC 7257593 and HC 7257567 say Supernode. SSO permission Manage controls it (HC 4292722).
- Required attributes: email, first name, last name (HC 4477745).
- Setup: Settings > `Organization Settings` > `Login Options` > `Identity provider Single Sign On URL` and `X.509 certificate` > `Save Settings`. Certificate must be wrapped in `-----BEGIN CERTIFICATE-----` and `-----END CERTIFICATE-----`. Toggle SSO on; to enforce select `Enable SAML SSO & Require SSO` (HC 4477745).
- SSO Exception Users (`SSO Login Exceptions` box): needed for OAuth from external applications to complete integrations; also for users who cannot use SSO and as fallback during IdP failure (HC 4477745).
- When requiring SSO, existing users not listed as exceptions are removed and must log in via the IdP to be re-added (HC 4477745).
- JIT: anyone with IdP credentials can join and gets the default role from the `Full Access Role` dropdown. Users created on first SSO login get Limited role (HC 4477745).
- Pre-provision: Settings > Team > invite modal > `Pre-Register using SSO` (locked on when SSO is required). Invitees keep assigned seats and roles (HC 4477745).
- Org login URL: https://app.crossbeam.com/login?sso=<id>, shown on Settings; landing page button `Log in with SAML SSO` (HC 4477745, HC 7257567).

**Okta** (Okta admin required) (HC 7257567): Applications > `Add Application` > `Create New App` > Web, SAML 2.0 > `Create`. App Name Crossbeam; visibility boxes unchecked. Single sign on URL = Crossbeam `Assertion Consumer Service (ACS) URL`; Audience URI = Crossbeam `Entity ID`; RelayState blank; Name ID `EmailAddress`; username `Email`; update on `Create and update`. Attributes exactly `first` (user.firstName), `last` (user.lastName), `email` (user.email). Feedback: `I'm an Okta customer adding an internal app` > `Finish`. Sign On > `View Setup Instructions` gives the SSO URL and certificate for Crossbeam. Assign users or groups for the Okta chiclet.

**Salesforce IdP** (HC 7257593): follow Salesforce "Salesforce as a SAML Identity Provider" first. On the Crossbeam Connected App > Custom Attributes > `New`: key `first` = $User > First Name; key `Last` = $User > Last Name; key `emailAddress` = $User > Email; `Insert Field` then `Save` each. Note key spelling differs from Okta's.

**Login basics**: app.crossbeam.com/login with email/password or SSO; logout via account menu > `Logout` (HC 3160245). Reset: `Forgot?` > work email > `Reset Password`, email subject `Reset Your Password`; or Profile & Preferences > `Reset Password` (HC 3160247, HC 3160248). Profile: Avatar or Settings > `Profile & Preferences` > `Edit Profile Information`; avatar not editable for SSO users (HC 3160248).

---

## 16. Notifications

- `Activity` bell (upper right): Partner Invites and Requests, Data Sharing, Data Processing; dot for new; purple dot or `Mark All as Read` (HC 3426387).
- Preferences: Profile & Preferences, enable all or per category > `Save Changes`. Sections include `Data Notifications`, `Lists Notification`, `Collaboration Notifications` (HC 3426387, HC 3160248, HC 3976123, HC 8345701, HC 14546228).
- Saved report alerts: Mapping > `Saved Reports` > Bell in Notifications column > emails or Slack > `Save Preferences` (HC 3426387).

---

## 17. Audit Logs

- Supernode. Admins or users with View Audit Logs permission (HC 6172688).
- Settings > `Organizational Settings` > `Audit Logs` > date range > `Export CSV`; download link arrives by email (HC 6172688).
- History since May 28, 2021; metadata, previous state, users impacted, organizations impacted, IP address may be missing before May 11, 2022 (HC 6172688).
- Covers: data source changes (connect, remove, field adds/removes, status, frequency, reauth); sharing default/setting changes (Population, partners, before/after, actor); partnership invites; Population changes; integration installs/updates/removals; role changes; team invites and deletions; successful and failed logins; logouts (HC 6172688).
- Columns: Activity Date (UTC), IP Address, User, User Email, Metadata, Previous State, Partner(s) Impacted, User(s) Impacted (HC 6172688).
- No revert or restore; no API export (HC 6172688).

---

## 18. Privacy, Security, Compliance

### 18.1 Assurances and contacts
- ISO/IEC 27001 and 27701; SOC 2 Type II via Trust Center security.crossbeam.com (HC 3160400, HC 3160445, HC 13066154).
- Crossbeam does not sell customer data (HC 3160445, HC 3160400, HC 13066154).
- Security Policy is part of all agreements; single platform, so no bespoke per-customer security requirements; the Crossbeam privacy inbox (privacy at crossbeam.com) (HC 3160445).
- DPA with Standard Contractual Clauses for GDPR (Crossbeam as processor) and transfers; subprocessor list at crossbeam.com/subprocessors (HC 3160400).
- Open source license or source requests: the Crossbeam legal inbox (legal at crossbeam.com), naming packages and a contact address (HC 6596903).
- Employee access: least privilege, audited quarterly; production via SSH behind VPN with key auth and Duo MFA; policies reviewed at least quarterly by the Security and Disaster Management Committee (HC 3160458).

### 18.2 Sync data requirements
- Company matching: Name and Website. Contact matching: Email (HC 9956727).
- Salesforce connector: read on Account, Opportunity, Lead, Contact, User; fields Record ID, Owner ID, Name, Website, IsDeleted, SystemModstamp, CreatedAt. Other CRMs: ask Crossbeam (HC 9956727).
- Required when syncing each object: Contact (Account ID, Contact ID, Email); Opportunity (Account ID, Opportunity ID); Opportunity Contact Role (Contact ID, Contact Role ID, Opportunity ID, Primary, Role); Lead (Lead ID, Email, Owner ID); User (Account Owner Email, User ID) (HC 9956727).
- Recommended for segmentation and filtering: Account Type, Billing Country, Employees, Industry; contact name, title, phone, dates; opportunity amount, dates, stage, won/closed; lead name, phone, created; Account Owner Name (HC 9956727).

### 18.3 Customer confidentiality options
- Exclude flagged companies via Population filters; rely on NDAs; build a broad "All Relationships" Population without sharing status; share customer Populations inward only (HC 3889182).

### 18.4 AI and data use
- AI Chat and AI Recommended Plays (live as of May 2026) use OpenAI via API, a DPA subprocessor. Both are read-only, permission-scoped, and take no actions (no sharing edits, partner connections, team or settings changes). Outputs are not pre-verified (HC 15297694).
- No LLM training on Customer Data by Crossbeam or OpenAI. AI Chat history retained in Crossbeam AWS under standard retention and deletion practices. All Customer Data on AWS US. AI features use data only for real-time requests (HC 15297694).
- Matching Engine: deterministic, not AI; compares normalized domain, email, DUNS, phone; uses only synced data; matching precedes sharing, enabling counts without sharing. May use network-derived non-personal signals internally, never surfaced (HC 15297694).
- Ecosystem Intelligence: not AI; built from synced data (sync, not share, is the control); shown only above a minimum threshold across distinct orgs; outputs contain no Personal Data; visible only on records you can already access (HC 15297694).
- Personal Data can be excluded from sharing; Crossbeam does not build lead lists from it or give net-new Personal Data to others; no automated decisions with legal effect (HC 15297694).

### 18.5 Retention and deletion facts
- Data removable at any time; Populations hideable per partner (HC 9956727, HC 13066154).
- Partner deletion removes all shared data permanently (HC 8545332). Population deletion is permanent (HC 4236619). Sheet row deletion does not delete the record (HC 8799966). Audit logs cannot restore state (HC 6172688).

---

## 19. Partnerbase and Support

- Partnerbase: free public database of B2B partnerships, 90,000+ companies; Tech = integration, Channel = everything else; not 100% accurate. Editing requires a verified non-personal email. My Lists export up to 500 records, private tags, notifications. `Show Overlapping Accounts` goes to a discoverable company's Crossbeam invite link. the Crossbeam partnerbase inbox (partnerbase at crossbeam.com) (HC 3160299, HC 7128217).
- Support: Help > `Chat with Support` or the Crossbeam support inbox (support at crossbeam.com), Monday to Friday 3:00 AM to 7:00 PM EST; off-hours answered next business day. ASM handles strategy, plan, seats, renewal. Help > `Help Center`, Help > `Crossbeam Academy`, `Ask AI` (HC 3160301).

---

## 20. Troubleshooting

**Sharing**
- Partner sees only counts. Cause: Counts Only default or override. Fix: set Overlapping Accounts or All Accounts in the Sharing Hub (HC 4236660).
- Nothing shown under a partner's Population on the Sharing Dashboard. Partner lacks the Population or is not sharing; `Request Data` (HC 9389961).
- Bulk edit skipped partners. Overrides are preserved; use `↺ Reset to default` or edit the row (HC 4236660).
- Newly tagged partner missing settings. Tag-based bulk edits are not retroactive (HC 4236660).
- Field preset options missing. Level is Counts Only or Hidden (HC 11583486).
- Shared fields changed for many partners. A shared preset was edited, or deleted (reverted to `Crossbeam Default`); check the Hub filter and Audit Logs (HC 11583486, HC 6172688).
- All Accounts unavailable. Free plan, or Enterprise non-admin (HC 4236660).
- Copilot Contacts empty. Partners not sharing contact data (HC 9486432).

**Partners and invites**
- Inviter never notified. `Ignore` sends no notification (HC 3160223).
- Invite declined. `View Reason`; re-invite from the wishlist (HC 15421724).
- Bulk invite over 100. Split batches (HC 15421724).
- Cannot send invites. Partner Invites permission disabled (HC 15421724, HC 4292722).
- `Help your partner get started faster` missing. Partner already paying, or you are on Free (HC 16547255).
- New user blocked after signup. Failed auto verification; manual review pending (HC 3935700).
- Cannot manage tags. Permission missing or 80-tag cap (HC 5467749).
- Partner deleted by mistake. Irreversible; reinvite and reconfigure (HC 8545332).
- Cannot add Offline Partner. Offline Partners permission not Manage, or Free already has one (HC 8799966).
- Sheet row deleted but record remains. Delete in the Population (HC 8799966).
- Cannot add ODP after deleting one. Slot not freed; upgrade (HC 15453957).
- No Prospect overlaps on ODP. Customer data only (HC 15453957).
- Products filter misses accounts. Use `contains` (HC 15453957).
- Lists, Tags, Populations gone after `Replace with Open Data Partner`. Permanent by design (HC 15453957).
- Managed Offline Partner stale or cannot add. Deprecated August 19, 2026 (HC 11730520).

**Shared Lists**
- Cannot create Static Shared List. Free plan, below Standard level, or Data Sharing not enabled (HC 8345701).
- Cannot add over 50 records at once. Add in batches (HC 8345701).
- Partner cannot see opportunity columns. Private by design (HC 8345701).
- `Share with Partner` disabled on Dynamic list. Population Counts Only or Hidden; not scoped to one partner; missing `Partner Shared Lists: Manage`; or started from Account Mapping List (HC 14546228).
- `Make Public` unavailable. No Data Sharing permission (HC 14546228).
- Cannot change filters after sharing. Locked; duplicate (unshared) and reshare (HC 14546228).
- New Population not in list. Dataset locked at share (HC 14546228).

**Attribution and Gong**
- Attribution prompts to sync more fields. Fields stay private; sync them (HC 8042999, HC 8301786).
- Attributed revenue vanished. Opp or deal deleted or changed in CRM (HC 8042999, HC 8301786).
- Opp missing from roll-ups. Empty amount or close date (HC 8042999).
- Attribution Push install fails. Must be Salesforce Admin; tick the Non-Salesforce Application box; check profile access afterwards (HC 8042999).
- Attributions not yet in Salesforce. First sync 30 minutes, then every 12 hours (HC 8042999).
- Gong mentions missing. Lower Similarity Cutoff from 90; add Keyword Trackers; authorizer needs Activity Timeline Manage (HC 8365716, HC 4292722).
- Gong mentions absent in Copilot for Salesforce. Not supported there (HC 8365716).
- Cannot create Connector Outbound integration. Blocked since July 1, 2025 (HC 8365716).

**Record Exports**
- Yellow banner (90%) or red banner (limit); integrations paused, CSV and List exports disabled at 100%. Contact sales, trim Populations and integration scope, or wait for annual reset (HC 8399864).
- Estimate higher than actual. Estimates count matches (HC 8399864).
- Re-uploaded CSV used exports. Re-upload after delete counts as new (HC 8399864).
- Free cannot export. Only Account Mapping Pass, 100 records (HC 8399864).

**Login, SSO, users**
- Users locked out after `Enable SAML SSO & Require SSO`. Not in SSO Login Exceptions; log in via IdP or add exceptions (HC 4477745).
- OAuth integration fails with required SSO. Configure an SSO Exception User (HC 4477745).
- SAML validation fails. Certificate not in BEGIN/END CERTIFICATE format (HC 4477745).
- Okta names or emails missing. Attributes must be exactly `first`, `last`, `email` (HC 7257567).
- New SSO user too limited. JIT default role or Limited role; adjust in Team (HC 4477745).
- `Pre-Register using SSO` locked on. SSO is required (HC 4477745).
- No `Reset Your Password` email. Try `Log in with Google` (org may use SSO), else support (HC 3160247).
- Cannot change avatar. SSO uses IdP image (HC 3160248).
- All admins left. Support manual check (HC 10309518).
- Cannot create custom roles. Needs Supernode and admin (HC 4292722).
- Audit Logs unavailable or blank older fields. Needs Supernode plus permission; fields untracked before May 11, 2022 (HC 6172688).
- Cannot remove seats yourself. Use `Manage Plan` chat (HC 7897487).
