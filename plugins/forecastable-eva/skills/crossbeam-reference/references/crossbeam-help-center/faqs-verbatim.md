# Crossbeam Help Center FAQs, verbatim

Every FAQ section in the Help Center, plus the FAQs collection, captured September 30th, 2026. Cite `HC <id>`.


## Steps to Request a Connector Free Trial (HC 10644667)
URL: https://help.crossbeam.com/en/articles/10644667-how-to-request-a-connector-free-trial

### FAQs
What does the Connector-tier Free Trial include?
The 30-day free trial grants access to the full Connector experience, including the Copilot Chrome extension.
- Export limits: Users can export up to 100 records per report
- Integrations : Connecting integrations is not allowed during the trial
- Data sharing : This functionality remains unchanged
- Seats: Max of 3 users
Who is eligible for a free trial?
New users on the free Explorer plan and have completed the onboarding process in Crossbeam.
How can I access a free trial?
Once onboarding is complete, a Request Free Trial button will appear in the top-right corner of the app. Click the button to schedule a time to talk to sales or to request sales contact you.
Can I upgrade my account during the trial?
Yes, you can upgrade your plan anytime during the trial in-app or by reaching out to sales.
- Managing User Seats and Roles in Crossbeam
- Manage Your Connector Plan FAQs
- For Sales Seats: Getting Started with Crossbeam and Crossbeam Features
- Installation Guide: Crossbeam for Salesforce (Connector Plan)
- Crossbeam Connector Enablement Catalog


## What is Crossbeam AI? (HC 11731834)
URL: https://help.crossbeam.com/en/articles/11731834-crossbeam-ai-chat

### FAQs
Is customer data used to train the LLM?
No. Customer data is not used to train the LLM (large language model) we use.

Is my data secure? Yes. Crossbeam AI only accesses data from your account and uses OpenAI as a subprocessor under strict security and compliance measures.

Does Crossbeam AI take action automatically? Only when prompted. It may suggest actions, but you stay in control of what gets executed.

Is it available to all users? AI Chat is available on all Crossbeam plans. Access may vary based on your plan and seat type.
- Installation Guide: Crossbeam for Salesforce (v2)
- For Sales Seats: Getting Started with Crossbeam and Crossbeam Features
- Crossbeam MCP Server
- Understanding Crossbeam AI and Data Use
- Setting up AI Agents in Crossbeam (public beta)


## Overview (HC 15507121)
URL: https://help.crossbeam.com/en/articles/15507121-onboarding-lookalike-prospects-population

### Frequently Asked Questions
What are Open Data Partners? Open Data Partners (ODPs) are curated technology vendors whose customer data is sourced and maintained by Crossbeam. ODPs let you identify account overlaps instantly, no partner invitation, connection, or data-sharing agreement required.

Does the Population update automatically?
No. Lookalike Prospects is generated once during signup and does not sync or refresh.

Can I see overlaps immediately?
Yes. Crossbeam automatically maps the Population against an Open Data Partner and displays the results as your first list.

Why do I see Sample Prospects instead?
Sample Prospects is generated when Crossbeam cannot confidently create a tailored lookalike list. It functions the same way as Lookalike Prospects.

Can I delete the Population?
Yes. Navigate to Populations and delete it like any custom Population.
- What are Populations?
- Getting Started with Crossbeam: Onboarding Guide
- Population Types for Custom Populations


## Overview (HC 6172688)
URL: https://help.crossbeam.com/en/articles/6172688-audit-logs

### FAQ
Can you revert changes or restore a “previous version” of an action? No

Can I export my audit log data into other tools via API access? We do not offer that capability at this time. ​
Who can view Audit Logs? Admins or users with the “View Audit Logs” permission in Crossbeam. ​
How much historical data can I export? You can export historical actions that have occurred since May 28th, 2021 to a CSV file. The following fields may be missing in audit log exports because Crossbeam didn’t start tracking this data until May 11, 2022.
- Metadata (specific details about actions taken in Crossbeam)
- previous_state
- users_impacted
- organizations_impacted
- ip_address
Further explore Audit Logs in the Crossbeam Academy!

📄 Related Articles
- Crossbeam Overview for Compliance Teams

#### 
- Understanding Record Exports
- Installation Guide: Crossbeam for Salesforce (v2)
- Crossbeam Overview for Compliance Teams


## Overview (HC 12399814)
URL: https://help.crossbeam.com/en/articles/12399814-population-types-for-custom-populations

### FAQ
Does this change how data is shared with partners?
No. Data Sharing rules stay the same, Population types only affect how Crossbeam organizes and interprets your data.

Will this change my Record Exports?
No. Record Exports aren’t affected.

Can I skip assigning a type?
No, but you can always select Other if none of the categories apply.
- Build a Standard Population
- What are Populations?
- Custom Populations
- Installation Guide: Crossbeam for Salesforce (v2)
- Onboarding: Lookalike Prospects Population


## How to Prepare and Sync your Google Sheet (HC 5613345)
URL: https://help.crossbeam.com/en/articles/5613345-how-to-use-google-sheets-as-a-data-source

### Frequently Asked Questions
If the same account (for example, Partnerbase.com ) appears on multiple tabs in a Google Sheet, does Crossbeam count it as multiple accounts?
No. Crossbeam recognizes this as the same account. Each tab can be selected individually as its own sheet data source, but data is not automatically merged across tabs.

If Partnerbase.com appears on Tab A and Tab B in a Google Sheet, does it count as a second Record Export?
No. Crossbeam recognizes Partnerbase.com as the same account, even if it appears on multiple tabs. Exporting that same account again from another tab does not count as an additional Record Export.

What are common sources for the data in these sheets? Most often, data comes from a CRM. If your CRM isn’t supported, or you lack permission to connect it, export the data to Google Sheets and connect that instead. For ongoing sync, use tools like Zapier or Workato to automate it.

Can I collaborate with partners using Google Sheets? Sure! Any columns that are outside of the columns you're collaborating with your partner on, will be pulled into Crossbeam and viewable in reports (and shareable) as “Account information”.

How do you authenticate with Google Sheets from Crossbeam? We authenticate with your Google account so we can view your sheets. Any sheet you want to include in Crossbeam must have a unique name and be shared with the person that authenticated Google in Crossbeam.
- Upload a CSV File and Map Your Fields
- How to Use the Slack App for Crossbeam
- Data Sources Overview: CSVs, CRMs and Data Warehouses
- What are Data Sources?
- Offline Partners


## Overview (HC 11730520)
URL: https://help.crossbeam.com/en/articles/11730520-managed-offline-partners

### FAQs
How often is the data updated? We update the Customer population for each Managed Offline Partner twice per year using a curated Google Sheet.

Where is the data sourced from? We pull from publicly available and verifiable sources (like customer pages or directories), using AI-powered tools to ensure data quality and coverage. Every data point has a traceable source to ensure a high level of confidence
This is the same type of information you'd find from sources like ZoomInfo, Crunchbase, HG Insights, or Partnerbase. We only include companies when we can confidently identify public evidence, such as customer logos on websites, case studies, job listings, or press releases, that validates a company as a customer of the partner in question. What makes Crossbeam unique is not the data itself. It's how we apply it. By infusing this public data into our platform, we enable account mapping across your pipeline and your broader partner ecosystem.

Can I hide these partners? Yes. If you prefer not to see them in your Partners List, you can hide Managed Offline Partners from view.

Can I invite these partners to join Crossbeam? Absolutely! These managed records are meant to give you immediate value, but you can still invite the partner to join the network if you'd like a fully connected experience.

What makes these different from standard partners?
- They're not real Crossbeam accounts
- Their data is sourced and maintained entirely by Crossbeam
- They only have one Population: Customers
- They're clearly labeled and separated from user-generated partners
👀Have access to Open Data Partners? Learn more here.
- Offline Partners
- How to Set Up the Partner Account CRM Integration
- How to Create a Combined Overlap and Partner Account Report Type in Salesforce
- Crossbeam Product Release Notes 08/19/2026


## Overview (HC 15453957)
URL: https://help.crossbeam.com/en/articles/15453957-understanding-open-data-partners

### FAQs
Is my Crossbeam data used to build Open Data Partners? No. Your CRM data, Populations, overlaps, and Lists are never used to build an ODP record and are never visible to anyone else.

Can I get product-level data on my Managed Offline Partners? No. Products are available on Open Data Partners only. If you have a Managed Offline Partner for a vendor with an equivalent ODP, you can replace it to get product-level data.

Will Open Data Partners replace my partner relationships? No. ODPs complement your partner program by providing immediate overlap data while you build direct partner connections.

How is ODP data sourced? ODP data is publicly sourced ' is-a-customer-of ' signals, partner directories, tech stack listings, marketplaces, public case studies, and integration pages. Crossbeam independently maintains these datasets and refreshes them daily.

Can I swap Open Data Partners? Free plans that had an ODP automatically allocated during onboarding can swap once. On other plans, you select your own Open Data Partners when you add them. If you’ve hit your limit, reach out to our team for steps on how to add additional ODPs.

Why can I only see Customer overlaps? ODPs are based on customer datasets sourced and maintained by Crossbeam. Prospect data is not currently included.
- How to Use the Partner List and Partner Detail Page
- Offline Partners
- Managed Offline Partners
- How to Set Up the Partner Account CRM Integration
- Crossbeam Product Release Notes 08/19/2026


## Overview (HC 8042999)
URL: https://help.crossbeam.com/en/articles/8042999-attribution-for-salesforce-users

### FAQs
Q. I see an error message like this, and I am nervous about syncing in more data to Crossbeam: ​
A: Any new fields you sync to Crossbeam are yours only - this data is not shared with your partners. This data allows Crossbeam to accurately reflect the actual revenue impacts of your Partners.

Q. What happens if my Opportunity gets deleted (or changed) in Salesforce? But it already has an Attributed Partner in Crossbeam?
A: Attributed revenue from this opportunity will no longer count towards your statistics or those partner(s).

Q. What happens if an Opportunity has an empty amount or close date?
A: Attributed revenue from opportunities without amount or close date are excluded from the denominator when calculating Roll-Up Metrics. ​
Q. Is it possible to pull in the attribution type (i.e. influenced, sourced, etc.) into the report?
A. Yes. We send the attribution type, sourced or influenced, along with each opportunity.

Q. Does this new attribution object get installed with the existing manage package? Or is this a second manage package I’ll have to install?
A. It is a second manage package, so you can install it via the Integration Marketplace or from the tile in Crossbeam Core.

Q. Does this feature come with pre-built reports? Or do I have to create a custom report?
A. This attribution feature comes with four standard report types:
- Crossbeam Attributions
- Crossbeam Attributions with Account
- Crossbeam Attributions with Opportunity
- Crossbeam Attributions with Partner
Q. Similarly to opportunities that get pushed into Salesforce today, does each attribution record connect to an account and an opportunity?
A. Yes. Each attribution is related to the account (i.e. the account you closed) and the partner account (if you include it during the setup of the integration).

Q. When configuring the Attribution Push in Crossbeam Core Settings, what does “Add a Partner ID from Salesforce” do?
A. If you input your Partner Account IDs here, your attributions will be linkable to the Partner in your Salesforce instead of by their text name only.

Q. How often does my Attribution data get synced to my Salesforce? A. 30 minutes after the initial setup and every 12 hours after that.

🔗 Related Articles
- Gong Inbound Integration
- Attribution for HubSpot Users
- Attribution from Crossbeam for Sales to Salesforce
- Crossbeam for Sales Attribution FAQs
- Installation Guide: Crossbeam for Salesforce (v2)
- How to Set Up the Partner Account CRM Integration


## Overview (HC 8301786)
URL: https://help.crossbeam.com/en/articles/8301786-attribution-for-hubspot-users

### FAQs
Q. I see an error message like this, and I am nervous about syncing in more data to Crossbeam:
A: Any new fields you sync to Crossbeam are yours only - this data is not shared with your partners. This data allows Crossbeam to accurately reflect the actual revenue impacts of your Partners.
Q. What happens if my Deal gets deleted (or changed) in HubSpot? But it already has an Attributed Partner in Crossbeam?

A: Attributed revenue from this Deal will no longer count towards your statistics or those partner(s).

Q. What happens if a Deal has an empty amount or close date?

A: Attributed revenue from Deals without amount or close date are excluded from the denominator when calculating Roll-Up Metrics.
- Connect HubSpot Data
- Potential Revenue
- Attribution for Salesforce Users
- Crossbeam for Sales Attribution FAQs
- Enhanced Ecosystem Reporting: “is a customer of” & “is an opportunity for” Fields in HubSpot


## What is the Account Mapping Pass? (HC 10592414)
URL: https://help.crossbeam.com/en/articles/10592414-account-mapping-pass-in-crossbeam-how-it-works

### FAQs
What do I need to do to activate the Account Mapping Pass?
Nothing; this is an automatic functionality included within the Supernode and Enterprise plans. This unlocks full Account Mapping functionality with Free partners.

What happens if I'm a Supernode or Enterprise customer and my Free plan partner has an Account Mapping Pass?
If an organization on the Free plan has an Account Mapping Pass via a Supernode or Enterprise partner, the Free account will have full visibility of the Account Mapping results and can export up to 100 records.

If I'm a Supernode or Enterprise customer, can I choose which of my Free partners has an Account Mapping Pass?
No. By default, all Free partners of any Supernode or Enterprise customer will receive an Account Mapping Pass from that partner and have access to the functionality included.

If I'm on the Free plan, can I request an Account Mapping Pass?
No. By default, all Free partners of any Supernode or Enterprise customer will receive an Account Mapping Pass from that partner and have access to the functionality included. Account Mapping Passes are only an available feature on our Supernode or Enterprise plans.

If I'm on the Connector plan, can I purchase or add on an Account Mapping Pass for my Free partners?
No. Account Mapping Passes are only an available feature on our Supernode or Enterprise plans.

Can I access Greenfield Lists with the AMP pass? No. Greenfield sharing and Lists are only available on paid plans. Visit crossbeam.com/pricing to learn more.

- Video: Account Mapping Matrix
- Managing User Seats and Roles in Crossbeam
- Account Mapping Matrix
- How to Set Up the Partner Account CRM Integration
- Crossbeam Product Release Notes 06/17/26


## Overview (HC 10845010)
URL: https://help.crossbeam.com/en/articles/10845010-crossbeam-performance-dashboard-guide

### FAQ
How often is the dashboard updated?
Crossbeam updates the data regularly and displays the last sync timestamp in the upper right corner of the dashboard. The refresh timing is based on your organization’s configured CRM sync field, which determines how frequently data is pulled into Crossbeam.
Why am I seeing an empty state in the Performance Dashboard?
There are two reasons you might see an empty state:
- Missing required fields: If your CRM isn’t syncing all the required fields for the dashboard, you’ll see an empty screen listing the fields that need to be synced. You will see a prompt directing you to your data source settings to update them.
- Insufficient engagement activity : If your organization hasn’t completed engagement activities on at least 10 opportunities since the start of the year, you’ll see a screen explaining the benefits of the Performance Dashboard.
📄 Related Articles
- Crossbeam Deal Navigator
- Plays and Contacts for Crossbeam Copilot for Salesforce
- Crossbeam Copilot Overview
- Crossbeam Copilot for Gong
- Understanding Partner Score in Crossbeam
- Ecosystem Intelligence Signals and Insights in Crossbeam Copilot


## Overview (HC 11801904)
URL: https://help.crossbeam.com/en/articles/11801904-account-mapping-reports-new-lists-experience

### FAQs
Why is the “Share” button disabled when I create a new List?
You’ll need to save the List first. Once it’s saved, the Share button becomes active, allowing you to invite internal collaborators.

Are newly saved Lists visible to my team by default?
No, new saved lists are only visible to the creator and admins until shared.

How are folders and Lists sorted now?
Folders are shown based on creation date and by most recent changes made by the user. For example, newly created folders and recently renamed folders would appear first. This makes it easier to return to Lists and folders you’re actively using.

What about old Shared Lists? Historical Shared Lists are accessible via the Lists Hub and are static. They remain available alongside dynamic Lists.
📄 Related Article
- How to Use the Account Mapping List
- Standard Account Mapping Single Partner List
- Advanced Account Mapping Greenfield List
- Advanced Account Mapping Custom List
- Static Shared Lists
- How to Use the Account Mapping List


## How to Get Started (HC 6797349)
URL: https://help.crossbeam.com/en/articles/6797349-potential-revenue

### FAQs
If I’m using a CSV file or a Google Sheet as a data source, will Potential Revenue data still populate in my Account Mapping Matrix with a partner?
No, you must be syncing deal is closed and amount from a CRM data source. To get connected to a CRM data source, check out our articles on Managing your Salesforce Connection and Managing your HubSpot Connection .
How is the Potential Revenue number calculated?
The Potential Revenue numbers in the Account Mapping Matrix are the sum of the open opportunity amount values in each population. The total Potential Revenue number is not a perfect sum of all the 1-1 population comparisons that you see in the Account Mapping Matrix because some opportunities could exist across multiple Populations.
Why am I not seeing the Potential Revenue summary or metrics in the Account Mapping Matrix?
- Your data source isn’t a CRM, or you’re not syncing opportunity data. In order to display potential revenue amounts, you must be syncing opportunity data from your CRM, including opportunity amount and opportunity deal/deal is closed .
- You’re not sharing overlap counts for at least one population.
- Your Partner isn’t sharing data with you. At least one of your partner’s populations needs to be sharing data with you.
- You’re not on a paid plan. You must be on a Connector or Supernode pricing plan to see a breakdown of your potential revenue metrics in the Account Mapping Matrix and to build opportunity Lists. If you are on a free plan (Explorer) and would like to use all of this feature, simply visit your billing page and upgrade .
What if my company uses a different field instead of Open Opportunity Amount?
By default, we will use the open opportunity amount field to calculate potential revenue. If you wish to use a different opportunity field, you can select the field on the Settings page . If you do not see the field you wish to use for Potential Revenue, it's because you are not currently syncing that specific field into Crossbeam. You can add additional fields through the Potential Revenue field dropdown.
Does the Account Mapping Matrix display Potential Revenue for custom Populations?
Yes. With a paid account, you can choose which Populations of yours, and your partners' (globally), that you want to see included in the Account Mapping Matrix view of Potential Revenue. If you are on a free plan (Explorer) and would like to use all of this feature, simply visit your billing page and upgrade .
Which opportunities are included in the Potential Revenue calculation?
Any deal where the sales deal is closed field is false, and the deal amount is positive (greater than 0) is an open deal that we count for potential revenue.
🎓 Sign into Crossbeam Academy to further explore Potential Revenue!
- How to Use the Partner List and Partner Detail Page
- Account Mapping Matrix
- Understanding Partner Score in Crossbeam
- Crossbeam Deal Navigator
- Crossbeam Product Release Notes 11/6/2025


##  (HC 14546228)
URL: https://help.crossbeam.com/en/articles/14546228-dynamic-shared-lists

### FAQs
Can I share a Dynamic Shared List with more than one partner?
No. Dynamic Shared Lists support one partner at a time. You can invite multiple users from that partner org, and each side can add internal collaborators, but the list is scoped to a single partner relationship.

Why is the Share with Partner option disabled?
This can happen if:
- Your Population is set to Overlap Counts Only or Hidden, it must be fully shared to enable external sharing
- The list is not scoped to a single partner
- You don't have the Partner Shared Lists: Manage permission
Can my partner see data I haven't shared with them?
No. You control column visibility explicitly. Anything added after sharing is private by default. Sharing a Dynamic Shared List does not change your underlying sharing settings with that partner.

Is there a record limit on Dynamic Shared Lists?
No. Dynamic Shared Lists do not have a record limit.

What happens if I add a new Population after sharing?
The list dataset is locked at the time of sharing. New Populations added later are not automatically pulled in, even if they match the filter criteria being used.

Can my partner edit the list filters?
No. The original filter logic is locked once the list is shared and will appear grayed out for all users, including the list owner. However, any user with access can temporarily adjust the existing filters using AND logic to narrow the list during their session. These adjustments are not saved and will not persist after you leave the list.

OR logic and net-new filters are intentionally blocked to prevent the list from being expanded beyond its original scope.

What's the difference between a Dynamic Shared List and a Static Shared List?
Dynamic Shared Lists are filter-based and update automatically as accounts enter or leave the criteria. Static Shared Lists contain a manually selected, fixed set of accounts and do not auto-update. See Static Shared Lists for more.
📄 Related Articles
- Static Shared Lists
- How to Use the Account Mapping List
- Understanding Sharing Settings for Partners
- Manage Team Members
- Understanding Sharing Settings for Partners
- Standard Account Mapping Single Partner List
- Advanced Account Mapping Greenfield List
- Static Shared Lists
- How to Use the Account Mapping List


## Create a Static Shared List (HC 8345701)
URL: https://help.crossbeam.com/en/articles/8345701-static-shared-lists

### FAQs
Will this work for non-overlapping lists?
Yes, you can share non-overlapping lists with a partner.

Why can't I create a Static Shared List?
You must have Standard user level permissions in order to create a Static Shared List or to be invited to join a Static Shared List. Learn more about roles and permissions here .

What happens to records on my list if my partner deletes their data source or stops sharing data with me?
The Records will still exist on your Static Shared List, but will remain static.

Can I send a Static Shared List to multiple partners?
No, Static Shared Lists only work on a 1-to-1 level, so you can only share with 1 partner. However, you can invite multiple internal collaborators to a list from your org, and your partner can do the same.

If the owner of the list removes those records, are they deleted on the partner side too?
Correct.

I f I'm creating the list and my data is set to overlap counts and the partners sharing data with me, do I have to enable permissions?
As long as your partner is sharing data with you, and you are at least sharing overlap counts, you will be able to add that Record to a list.

Do you have to share account owner?
No, account owner is automatically on the list.

For Free plan users with "Invite-Only" access, are they getting access to the full Static Shared Lists feature once invited?
Yes, they have full access to the feature if they're invited to collaborate on a Static Shared List.

Will you automatically see your partner's updates in the Static Shared List? Or do you need to manually refresh?
It will automatically push to your Crossbeam instance, and you will receive a notification for any updates.

Will Static Shared Lists work for all data sources, including sheets and CSVs?
Yes, but CSVs will be static and not active like CRM connections.
- How to Use the Slack App for Crossbeam
- Installation Guide: Crossbeam for Salesforce (v2)
- For Sales Seats: Getting Started with Crossbeam and Crossbeam Features
- Setting Up a Crossbeam Ecosystem Overlaps Related List in Salesforce


## Overview of Crossbeam's Matching Process (HC 10492031)
URL: https://help.crossbeam.com/en/articles/10492031-updated-matching-process-with-duns

### FAQ
Is DUNS supported for all data sources? You can map DUNS data for any data source.
There are some limitations on mapping DUNS data retroactively for CSVs and G-Sheets. If you run into issues, please reach out to support.

Does Crossbeam strip out any dashes in DUNS numbers? Yes, this means 123456789 matches 12-345-6789.

Does Crossbeam only support DUNS fields that are type “text” from CRMs? Yes, DUNS numbers from CRMs that are type “number” may not work properly within our matching. DUNS numbers may have a leading 0, which will get removed if the field type is 0, causing us to be unable to match with high confidence in our system.

Does Crossbeam currently support DUNS+4 numbers?
No, we do not currently support DUNS+4 numbers. ​ Context: Businesses may choose to append four extra alphanumeric characters to their DUNS number. This is called a DUNS+4 number. The suffix is for the use of the business (for example, to identify different electronic funds transfer accounts). It has no significance otherwise and is not tracked by Dun & Bradstreet.

Can I retroactively select more than one DUNS column name for file uploads?
No, Crossbeam can only retroactively select one DUNS column name for file uploads. For file uploads, if there are currently multiple files that have DUNS data where the files have different column names for DUNS.
- Crossbeam cannot retroactively map multiple different DUNS column names, we can only choose 1
- For any additional data that is added, we CAN add a different column name for DUNS at the time of upload
- Understanding Crossbeam Matching
- Upload a CSV File and Map Your Fields
- Crossbeam Product Release Notes--02/04/2025
- Crossbeam Product Release Notes 11/6/2025
- The Crossbeam Matching Engine: Our Secret Sauce


## Matching Overview (HC 3160297)
URL: https://help.crossbeam.com/en/articles/3160297-understanding-crossbeam-matching

### FAQ
How does DUNS matching work?
Read more about it here .

Can you match using other dimensions?
Not currently, no, but our matching engine is always getting more intelligent as we add more matching dimensions.

- Crossbeam Overview for Compliance Teams
- Crossbeam Product Release Notes--02/04/2025
- Updated Matching Process with DUNS
- The Crossbeam Matching Engine: Our Secret Sauce
- Understanding Crossbeam AI and Data Use


## Report Incorrect Matches (HC 5246994)
URL: https://help.crossbeam.com/en/articles/5246994-report-incorrect-matches

### FAQs
What happens next?
Your report is used as an input to our matching engine, which will learn from any mistakes and improve matching based on your reports.

When does Crossbeam let me know that a match was removed?
Crossbeam does not respond to Incorrect Match Reports. They are used to train our matching engine, and are not treated as individual support requests. If you have an issue with a match that requires immediate resolution, please reach out to your customer support manager or email us at support@crossbeam.com . <!-- VALIDATE-OK[person-address]: verbatim public Crossbeam Help Center text -->
- Understanding Crossbeam Matching
- Snowflake Integration
- Installation Guide: Crossbeam for Salesforce (v2)
- Crossbeam Overview for Compliance Teams
- The Crossbeam Matching Engine: Our Secret Sauce


## Overview (HC 10080441)
URL: https://help.crossbeam.com/en/articles/10080441-clay-crossbeam-integration

### FAQs
What fields are pulled in from Crossbeam?
Clay pulls in all fields available through the Crossbeam account overlaps endpoint . This includes data like partner owner, record email, record website, Crossbeam ID, and more.

Do you have to authenticate Crossbeam as a source every time you create a new table?
No, you only need to authenticate Crossbeam once. After that, Crossbeam can be selected as a source in any new table without re-authentication.

Can you select multiple partners at once in a single table?
You can add multiple partners by creating a second source within the same table for each additional partner. This enables you to build tables that include data from multiple partners.

- Installation Guide: Crossbeam for Salesforce (v2)
- Crossbeam Copilot for Outreach
- Crossbeam Product Release Notes--11/13/2024
- Crossbeam Product Release Notes 08/19/2026


## Overview (HC 10578034)
URL: https://help.crossbeam.com/en/articles/10578034-how-to-upgrade-from-the-crossbeam-legacy-salesforce-integration-v1-to-v2

### FAQs
Will we lose any data?
No, this is an upgrade to the current custom object (v1). The upgrade enhances data customization and improves report-building features.

How long does the upgrade to take v2?
After completing the above setup, allow for at least an hour before data will be synced.

How can the Salesforce Admin help with the transition?
The Salesforce admin can manually go into the Reports tab, locate the Crossbeam Overlap Reports (v1), and select Hide Report Type from the drop-down option. Additionally, any workflows built on v1 will need to be recreated in v2.

Who should I reach out to for help?
Feel free to contact our support team either in-app or via email at support@crossbeam.com . <!-- VALIDATE-OK[person-address]: verbatim public Crossbeam Help Center text -->
- Crossbeam Copilot for Salesforce
- Upgrade & Reauthorize Crossbeam for Salesforce
- Installation Guide: Crossbeam for Salesforce (v2)
- Troubleshooting Salesforce Authorization with Crossbeam


## Overview (HC 12732223)
URL: https://help.crossbeam.com/en/articles/12732223-getting-started-with-signals-how-to-access-real-time-partner-data-via-api-and-webhooks

### FAQs
- Does the webhook count towards Record Exports? Yes, just like Crossbeam's existing API, the new webhook will also count towards Record Export limits.
- Do you need to have a license to leverage signals and the webhook? No additional licenses are required. Only Admins can create webhooks, but anyone in your organization can benefit from the workflows or alerts they trigger in other tools.
- Can I access signals if my data source is a CSV or Google Sheet? Yes, as long as your partner has a connected CRM and is sharing the required fields, you’ll receive signals for that partner’s data.
- How is this different from Crossbeam's existing API? Our existing API provides access to raw overlap data. The new API and webhook deliver: Event-based, enriched data, like “Opportunity Opened” or “Closed Won” as they happen Real-time push updates via webhook (or on-demand pulls via API) AI-ready formats for use with intelligent systems like Crossbeam’s MCP or other AI tools Richer integrations that reflect structured, real-time data streams
- Event-based, enriched data, like “Opportunity Opened” or “Closed Won” as they happen
- Real-time push updates via webhook (or on-demand pulls via API)
- AI-ready formats for use with intelligent systems like Crossbeam’s MCP or other AI tools
- Richer integrations that reflect structured, real-time data streams
- Are we able to push Greenfield account signals? No, this capability isn’t supported at this time.
📄 Related Articles
- Crossbeam REST API
- Understanding Partner Score in Crossbeam
- Ecosystem Intelligence Signals and Insights in Crossbeam Copilot
- Crossbeam Performance Dashboard Guide
- Crossbeam Product Release Notes 11/6/2025
- Crossbeam Product Release Notes 02/11/2026


## Overview (HC 15961519)
URL: https://help.crossbeam.com/en/articles/15961519-setting-up-ai-agents-in-crossbeam-public-beta

### FAQ
What's the difference between an Agent and a Slack notification I already get from Crossbeam?
Standard Crossbeam Slack notifications report on population changes in bulk. AI Agents are user-defined: you configure the specific condition to watch for, and each alert includes a short recommendation rather than a raw data summary.

Do Agents fire for matches that already existed when I created the Agent?
No. AI Agents diff results against the previous run and only surface new matches.

Can I edit the message an Agent sends?
Not in beta, message copy is fixed. Configurable instructions for the message are planned for a future release.

Can an Agent send a Slack DM?
Yes. AI Agents can send notifications via Slack DM, a Slack channel, or a Slack Connect channel.

Why didn't my Agent fire even though the condition seems to be met?
Check the following:
- The match existed before the Agent was created (not a new result)
- The partner required by the trigger isn't actively sharing data
- Required CRM fields aren't synced (for the two opportunity-based triggers)
- The Agent is disabled
Can multiple Agents use the same trigger type?
Yes. You can create multiple active Agents with the same trigger but different conditions, actions, or channels.

How often do Agents run?
Hourly. Each Agent produces at most one notification per run, even if multiple records match.

What happens if my Slack integration needs reauthorization?
If your org's Slack connection requires reauthorization, the Agent's run is skipped for that cycle, no notification is delivered until the connection is reconnected.

- How to Use the Slack App for Crossbeam
- Crossbeam Copilot for Outreach
- For Sales Seats: Getting Started with Crossbeam and Crossbeam Features
- Crossbeam MCP Server


## Overview (HC 3639783)
URL: https://help.crossbeam.com/en/articles/3639783-how-to-use-the-slack-app-for-crossbeam

### FAQ
Can I connect more than one Crossbeam account to Slack?
No. Only one Crossbeam account can be connected to Slack at a time. Authorizing Slack from a second organization removes the connection from your first.

Can I send notifications to private channels?
Yes, as long as you have invited the Crossbeam app into the private channel first. In the channel, type /invite, select Add apps to this channel, and choose Crossbeam . This applies to Slack Connect channels as well.

How often will I receive notifications?
Notifications are delivered every four hours via Slack.
Crossbeam's privacy policy can be found here .

- Crossbeam Copilot for Salesforce
- Crossbeam Sales Settings and Features
- Understanding Crossbeam for Sales Notifications
- For Sales Seats: Getting Started with Crossbeam and Crossbeam Features
- Setting up AI Agents in Crossbeam (public beta)


## Uninstall the Current HubSpot Legacy Integration (HC 7971155)
URL: https://help.crossbeam.com/en/articles/7971155-hubspot-custom-object-integration

### FAQ
Does Crossbeam impact my HubSpot Private App API limits?
This integration will use some of your Private App API limits, but employs batch calls and resumes where it last left off to reduce usage. For questions about the integration's API usage, please reach out to the support team.

What happens to my legacy HubSpot integration once I delete it?
You will not be able to reinstall this deprecated integration, as it is no longer available.

What are the custom object fields and what do they mean?
| Field Label | Brief Description |
| Account ID | Identifies the HubSpot account record associated with the overlap. |
| Crossbeam EID | For Crossbeam housekeeping purposes: this identifier is used as part of our process to push records into your HubSpot environment. |
| Lead ID | Identifies the HubSpot contact record associated with the overlap. |
| Name | For HubSpot housekeeping purposes: name of the overlapping record. Can be clicked by a user (e.g. in a view of the custom object or in a card) to be taken to the full details of the Crossbeam Overlap record. |
| Overlap Unique Id | For Crossbeam housekeeping purposes: this identifier is used as part of our process to push records into your HubSpot environment. |
| Partner Name | The name of the Partner (as it appears in Crossbeam) that the account or contact matched with. |
| Partner Population | The name of the Partner's Population that the account or contact matched with. |
| Partner AE Email | Data being shared with you by your partner: the email address of the Account Owner for the account or contact. |
| Partner AE Name | ​Data being shared with you by your partner: the name of the Account Owner for the account or contact. |
| Partner AE Phone | ​Data being shared with you by your partner: the phone number of the Account Owner for the account or contact. |
| Population | The name of Your Population (as it appears in Crossbeam) that the account or contact matched with. |
Ready to build smarter reports and dashboards? Kick off your HubSpot training in Crossbeam Academy.

- Installation Guide: Crossbeam for Salesforce (v2)
- Microsoft Dynamics Custom Object Integration
- Enhanced Ecosystem Reporting: “is a customer of” & “is an opportunity for” Fields in HubSpot
- Databricks Integration


## Before you begin (HC 9280237)
URL: https://help.crossbeam.com/en/articles/9280237-installation-guide-crossbeam-for-salesforce-v2

### Frequently Asked Questions

#### How can my team run reports on Crossbeam data?
The managed package comes with several standard report types. Ensure that your team has the Crossbeam Report User permission set assigned for the reports to be accessible.

To run reports,
- Navigate to Reports -> New Report
- In the subsequent "Create Report" screen, make sure you are in the "All" Category on the left and type "Crossbeam Ecosystem" into the search bar:
- Select the desired report type and click the Start Report button
- Navigate to the "Filters" tab of the report and select All crossbeam ecosystem overlaps and All Time :
- Continue building out your report with the relevant columns and filters

#### What are best practices for running reports on Crossbeam data?
Navigate to the Outline tab and add the columns that are most relevant for your team. We recommend adding Partner Name next to Partner Standard Populations . Consider adding your Account Owner field as a row group.

Expand the "Fields" ribbon on the left hand side to see all the fields you can add from your Account object and your Crossbeam Ecosystem Overlap object:

🔎 A best practice is to narrow in on a specific use case and get as granular as possible with your filters.
For a report focused on driving net new pipeline, filter out everything except for where your cold prospects are existing customers of your partners.

Navigate to the Filters tab and apply the following filters:
- Standard Populations equals Prospects
- Partner Standard Population s equals Customers
In this example, rows are grouped by Account Owner. We can quickly see Sales reps Brandon and Sara have cold prospects that can be warmed up with help from partners Bozala, Surfzer, and Yaarde.

Add columns Partner Record Owner Name and Partner Record Owner Email to make rep-to-rep collaboration easy.

Save your report and consider adding it to a Public folder. Encourage your team to access the report and play around with it, cloning it and applying their own filters.

Ready-to-Use Salesforce Reports are automatically created when the Crossbeam for Salesforce Package is installed in your Salesforce.
Learn more here .

Click here to build the Crossbeam 360 Dashboard.

#### What should Crossbeam Ecosystem Overlap record pages look like?
Organize the way data is presented in a Crossbeam Ecosystem Overlap record so it's easy for your team to understand.

In Salesforce Setup, navigate to Object Manager > Crossbeam Ecosystem Overlap. Select "Page Layout" from the left hand navigation bar and click "Crossbeam Ecosystem Overlap Layout" to enter the configuration page.

Consider organizing "your" information on one side and "your partner's" information on the other:

In this example, the left side of the overlap detail will show your Account and/or Opportunity the Crossbeam Overlap is associated with. It will also confirm which of your Standard or Custom Crossbeam populations this record resides in. The right side will tell you which partner it matched with, the partner population, the partner account owner detail (if this information was shared with you), and the name of the account as it appears in the partner's dataset. The bottom shows the timestamp of when the overlap was created, and when it was modified.


#### What are the custom object fields and what do they mean?
| Field Label | Brief Description |
| Account | Identifies the Salesforce account record associated with the overlap. |
| Created By | Identifies the Salesforce user creating the overlap record - this will usually be your Salesforce Admin or user that installed the integration. |
| Create Date | The date and time the overlap was first matched and the record was created in Salesforce. This timestamp does not change if the overlap is later updated. |
| Crossbeam EID | For Crossbeam housekeeping purposes: this unique identifier is used as part of our process to push records into your Salesforce environment. |
| Last Modified By | Identifies the Salesforce user modifying the overlap record, this will usually be your Salesforce Admin or user that installed the integration. |
| Last Modified Date | The date and time the overlap record was last updated in Salesforce, for example, if shared partner data changed. |
| Lead | Identifies the Salesforce lead record associated with the overlap. |
| Opportunity | Identifies the Salesforce opportunity record associated with the overlap. |
| Overlap Name | For Salesforce housekeeping purposes: this unique identifier can be clicked by a user (e.g. in a report or related list) to be taken to the full Crossbeam Overlap record. |
| Owner | Identifies the Salesforce owner of the overlap record - this will usually be your Salesforce Admin or user that installed the integration. |
| Partner Name | The name of the Partner (as it appears in Crossbeam) that the account or lead matched with. |
| Partner Populations | The name of the Partner's Custom Population that the account or lead matched with. |
| Partner Record Name | Data being shared with you by your partner: the name of the overlapping account or lead as it appears in your partner's Data Source. |
| Partner Record Owner Email | Data being shared with you by your partner: the email address of the Account Owner for the account or lead. |
| Partner Record Owner Name | ​Data being shared with you by your partner: the name of the Account Owner for the account or lead. |
| Partner Record Owner Phone | ​Data being shared with you by your partner: the phone number of the Account Owner for the account or lead. |
| Partner Standard Populations | The name of the Partner's Standard Population that the account or lead matched with. |
| Partner Record Country | ​Data being shared with you by your partner: the country of the partner's account or lead. |
| Partner Record Employees | ​Data being shared with you by your partner: the number of employees in the partner's account or lead. |
| Partner Record Industry | ​Data being shared with you by your partner: the industry of the partner's account or lead. |
| Partner Record Type | ​Data being shared with you by your partner: the type of the partner's account or lead. |
| Partner Record Website | ​Data being shared with you by your partner: the website of the partner's account or lead. |
| Partner Record Owner Title | ​Data being shared with you by your partner: the job title of the partner's account or lead owner. |
| Populations | The name of Your Custom Population (as it appears in Crossbeam) that the account or lead matched with. |
| Standard Populations | The name of Your Standard Population (as it appears in Crossbeam) that the account or lead matched with. |


#### How do I reauthorize the Salesforce Custom Objects integration in Crossbeam?
If your Salesforce Custom Objects integration connection has expired, your integration user’s credentials have changed, or you’re troubleshooting related errors, you may need to reauthorize the connection.
- Watch this video, Reauthorizing the Salesforce Custom Objects Integration to fix it.
- Or read this article, Step-by-Step Guide: Reauthorizing Your Salesforce Custom Object Integration .

#### There's a Salesforce authorization error when connecting to Crossbeam. What Should I do?
This can happen due to Salesforce’s September 2025 security update blocking “uninstalled” connected apps. For full troubleshooting steps, see our dedicated article: Troubleshooting Salesforce Authorization with Crossbeam .

- Crossbeam Copilot for Salesforce
- Salesforce Guide for Reports, Dashboards, & Automations Powered by Crossbeam
- Setting Up a Crossbeam Ecosystem Overlaps Related List in Salesforce
- How to Create a Combined Overlap and Partner Account Report Type in Salesforce


## Before you begin (HC 9298987)
URL: https://help.crossbeam.com/en/articles/9298987-installation-guide-crossbeam-for-salesforce-v1

### Frequently Asked Questions


#### How can my team run reports on Crossbeam data?
The managed package comes with several standard report types. Ensure that your team has the Crossbeam Report User permission set assigned for the reports to be accessible.

To run reports,
- Navigate to Reports -> New Report
- In the subsequent "Create Report" screen, make sure you are in the "All" Category on the left and type "Crossbeam" into the search bar:

- Select the desired report type and click the Start Report button
- Navigate to the "Filters" tab of the report and select All crossbeam ecosystem overlaps and All Time :
- Continue building out your report with the relevant columns and filters


#### What are best practices for running reports on Crossbeam data?
Navigate to the Outline tab and add the columns that are most relevant for your team. We recommend adding Partner Name next to Partner Population . Consider adding your Account Owner field as a row group.

Expand the "Fields" ribbon on the left hand side to see all the fields you can add from your Account object and your Crossbeam Overlap object:

🔍 Narrow in on a specific use case and get as granular as possible with your filters.
For a report focused on driving net new pipeline, filter out everything except for where your cold prospects are existing customers of your partners.

Navigate to the Filters tab and apply the following filters:
- Population equals Prospects
- Partner Population equals Customers
In this example, rows are grouped by Account Owner. We can quickly see Sales reps Brandon, Sara, and Sawyer have 5 cold prospects that can be warmed up with help from partner Yaarde. Add columns "Partner AE Name" and "Partner AE Email" to make rep-to-rep collaboration easy:

Save your report and consider adding it to a Public folder. Encourage your team to access the report and play around with it, cloning it and applying their own filters.


#### What should Crossbeam Overlap record pages look like?
Organize the way data is presented in a Crossbeam Overlap record so it's easy for your team to understand.

In Salesforce Setup, navigate to Object Manager > Crossbeam Overlap. Select "Page Layout" from the left hand navigation bar and click "Crossbeam Overlap Layout" to enter the configuration page.

Consider organizing "your" information on one side and "your partner's" information on the other:

In this example, the left side of the overlap detail will show your Account and/or Opportunity the Crossbeam Overlap is associated with. It will also confirm which of your Crossbeam populations this record resides in. The right side will tell you which partner it matched with, the partner population, the partner account owner detail (if this information was shared with you), and the name of the account as it appears in the partner's dataset. The bottom shows the timestamp of when the overlap was created, and when it was modified:


#### What are the custom object fields and what do they mean?
| Field label | Brief description |
| Account | Identifies the Salesforce account record associated with the overlap. |
| Created By | Identifies the Salesforce user creating the overlap record - this will usually be your Salesforce Admin or user that installed the integration. |
| Crossbeam EID | For Crossbeam housekeeping purposes: this unique identifier is used as part of our process to push records into your Salesforce environment. |
| Crossbeam Overlap Name | For Salesforce housekeeping purposes: this unique identifier can be clicked by a user (e.g. in a report or related list) to be taken to the full Crossbeam Overlap record. |
| Last Modified By | Identifies the Salesforce user modifying the overlap record - this will usually be your Salesforce Admin or user that installed the integration. |
| Lead | Identifies the Salesforce lead record associated with the overlap. |
| Opportunity | Identifies the Salesforce opportunity record associated with the overlap. |
| Owner | Identifies the Salesforce owner of the overlap record - this will usually be your Salesforce Admin or user that installed the integration. |
| Partner Account | Data being shared with you by your partner: the name of the overlapping account or lead as it appears in your partner's Data Source. |
| Partner AE Email | Data being shared with you by your partner: the email address of the Account Owner for the account or lead. |
| Partner AE Name | ​Data being shared with you by your partner: the name of the Account Owner for the account or lead. |
| Partner AE Phone | ​Data being shared with you by your partner: the phone number of the Account Owner for the account or lead. |
| Partner Name | The name of the Partner (as it appears in Crossbeam) that the account or lead matched with. |
| Partner Population | The name of the Partner's Population that the account or lead matched with. |
| Population | The name of Your Population (as it appears in Crossbeam) that the account or lead matched with. |

​
- Crossbeam Copilot for Salesforce
- Salesforce Guide for Reports, Dashboards, & Automations Powered by Crossbeam
- Crossbeam Copilot for Salesforce FAQs
- Installation Guide: Crossbeam for Salesforce (v2)
- Installation Guide: Crossbeam for Salesforce (Connector Plan)


## AI Recommended Plays in Copilot Overview (HC 9596637)
URL: https://help.crossbeam.com/en/articles/9596637-ai-recommended-plays-in-copilot

### FAQs
Is my data safe? We obfuscate PII data sent to the LLM so that there are no PII / GDPR concerns. No data sent can be used by the LLM provider, so it’s not unlike many other services we use that touch customer data in some way.

How do we choose which play and partner is shown first? We prioritize the plays based on their level of impact. For example, if a partner has recently won the account, we will prioritize them in the recommended plays so that you can leverage the timing.

What happens when I click on thumbs up or down? The product team gathers all feedbacks on this feature, and it will help use improve it in the future.

What happens when I click regenerate? A new play is generated by leveraging a different partner or another contact within the same partner organization if they are the only eligible option. Additionally, the play suggests various approaches for engaging with them.
📄 Related Articles
- Crossbeam Copilot for Salesforce
- Crossbeam Copilot for HubSpot
- Crossbeam Copilot for Gong
- Crossbeam Copilot for Chrome
- Crossbeam Copilot for Outreach
- Crossbeam Copilot for Chrome
- Crossbeam Copilot for HubSpot
- Crossbeam Copilot Overview
- Crossbeam Copilot for Gong
- Crossbeam Copilot for Outreach


## What are Record Exports? (HC 8399864)
URL: https://help.crossbeam.com/en/articles/8399864-understanding-record-exports

### FAQ
What happens to integrations when an account hits its limit?
When an organization reaches its limit, data exports are blocked, and updates to existing exported data are halted. Integrations are paused completely, with no further CSV exports allowed. Your record export limit will reset annually based on your contract date.

What does “record” mean for different data?
| Salesforce Accounts and Leads | HubSpot Companies | Microsoft Dynamics Accounts and Leads |
- Salesforce Accounts and Leads
- Accounts and Leads
- HubSpot Companies
- Companies
- Microsoft Dynamics Accounts and Leads
- Accounts and Leads
| Snowflake Accounts and Leads | CSV All rows (these are “companies” or “people”) | Google Sheets All rows (these are “companies” or “people”) |
- Snowflake Accounts and Leads
- Accounts and Leads
- CSV All rows (these are “companies” or “people”)
- All rows (these are “companies” or “people”)
- Google Sheets All rows (these are “companies” or “people”)
- All rows (these are “companies” or “people”)
Will any integrations be excluded?
Yes, Slack Integration, all Crossbeam Copilots, and Crossbeam for Sales are excluded from the Record Export limits.

Can I control users' access to List exports?
Yes. Access to List exports is determined by user permissions. You can adjust permissions to control who can export records. Learn more about permissions here .

To dive deeper into Record Exports, jump into Crossbeam Academy and start learning!
📄 Related articles
- Integrations Overview
- Delete, Duplicate, or Export a List
- Account Mapping Pass in Crossbeam

- Glossary of Key Terminology in Crossbeam
- REST API
- Gong Integration
- Offline Partners
- How to Set Up the Partner Account CRM Integration


## Overview (HC 13066154)
URL: https://help.crossbeam.com/en/articles/13066154-data-privacy-faq

In this article:
- Is any data shared automatically when I sync my CRM?
- Where does my data go once it’s uploaded to Crossbeam?
- What data does Crossbeam collect, and do you sell customer data?
- When does data get shared with a partner?
- Can I control what data is shared, and with whom?
- What type of data sharing is possible?
- Can I revoke sharing or remove data at any time?
- What happens to the records that do not match with a partner?
- Will my partners ever see my full customer or pipeline lists?
- How does Crossbeam maintain privacy and security?
Crossbeam gives you complete control over your data and how it’s shared. This FAQ answers common privacy questions and explains how Crossbeam protects your information at every step.

#### Is any data shared automatically when I sync my CRM?
No! Syncing or uploading data does not share anything by default.

#### Where does my data go once it’s uploaded to Crossbeam?
Your data is stored securely in your private Crossbeam account and is not shared unless you explicitly configure sharing with a partner.

#### What data does Crossbeam collect, and do you sell customer data?
Crossbeam only processes the data you choose to import, either via CRM sync or CSV upload. Crossbeam does not sell customer data.

#### When does data get shared with a partner?
Nothing is shared automatically. Data sharing only happens when: (a) you and a partner both opt-in by accepting a partnership invite; (b) you explicitly define which segment (called Populations) to share; and (c) you configure which fields will be shared under what matching conditions.

#### Can I control what data is shared, and with whom?
Yes! Crossbeam gives you granular control. You decide what data to import, which data subsets to share, and which specific fields get shared with each partner when matches occur.

#### What type of data sharing is possible?
When a match is found between shared data segments, you can choose to share full data fields (e.g., company name, website) or opt for Counts Only, where only the number of matches is shared, or you can choose not to share any data.

#### Can I revoke sharing or remove data at any time?
Yes! Data segments (called Populations) can be hidden or revoked for any partner at any time, and you can also remove data from Crossbeam altogether.

#### What happens to the records that do not match with a partner?
Non-matching records remain completely private within your Crossbeam account and are not visible to partners or used by Crossbeam. In some use cases, partners do opt to share non-overlapping accounts.

#### Will my partners ever see my full customer or pipeline lists?
No! Partners only see the specific shared fields for records that match, based on your sharing data configurations.

#### How does Crossbeam maintain privacy and security?
Learn more about Crossbeam’s privacy and security controls here . You’ll find information about Crossbeam’s ISO certifications, SOC 2 Type II report and more.
- Data Privacy
- Connect Snowflake Data
- Audit Logs
- Crossbeam Overview for Compliance Teams
- Understanding Crossbeam AI and Data Use


## How does it work? (HC 3160299)
URL: https://help.crossbeam.com/en/articles/3160299-what-is-partnerbase

In this article:
- How Does it Work?
- Explore Partnerbase
- View, Edit, and Delete Partnerships
- Create Lists
- Manage your Company Profile

Partnerbase is a website database built by Crossbeam and maintained by the public. It publishes a free listing of partnerships that exist between B2B companies.

The data that powers Partnerbase has been collected, both manually and programmatically, by Crossbeam and the public. The partners added to Partnerbase are gathered through two sources:
- our research team finds public evidence of a partnership, usually through a partner page or announcement
- a Partnerbase user added the partnership Anyone with a free, verified Partnerbase account can add partnerships
- Anyone with a free, verified Partnerbase account can add partnerships
Partnerships are categorized between tech and channel, generally using the following criteria:
- Tech = an integration
- Channel = everything else
In both cases, we know the information is not going to be 100% perfect, although it is generally accurate.


### Explore Partnerbase
You can start finding partners in your industry, uncover opportunities, and more, by searching for a company in Partnerbase .

Click Browse at the top of the page and scroll through the 90,000 plus companies in the database.

To apply filter(s) to the search results, simply explore the dropdown boxes to customize your search.

### View, Edit, and Delete Partnerships
Select a company from the Partner List in the search results or from a Company page. Click the dropdown arrow at the end of a company row. This will display a summary of the partner ecosystem including the amount of overlaps, the number of companies in each ecosystem, and the largest companies in both ecosystems.

Click the Edit Partnership button to change the type of Partnership, the date the partnership was established, and the source link used to identify the partnership. You can remove the partnership by clicking the Delete Partnership button.
✍️ Note
You must be logged in with a verified, non-personal email in order to edit, add, or delete partnerships.
Click the View Partnership button to explore more details of the shared partnerships in a 1:1 comparison.


### Create Lists
To share or save lists of partners, log in to Partnerbase to access My Lists.

With My Lists, you can:
- create and save lists
- export up to 500 records for additional analysis
- create custom tags visible only to you for additional filtering and tracking
- receive in-app notifications and email notifications as new companies enter your saved lists

When you log in to Partnerbase you can receive real-time notifications in-app and occasional emails updating you on companies from your saved lists.


### Manage your Company Profile
Log in with your work email to manage your company's Partnerbase profile.

On the Partnerbase homepage, search for your company (or create it if it does not exist). On the company profile, you can click on the edit pencil icons next to General Info and Partnership Info to make changes. You can also click the Add Partnership button to update your ecosystem. Click on the Show Overlapping Accounts button will take you to a Company's partner invite link if they are discoverable on Crossbeam. Learn more about discoverability on Crossbeam here .

Have questions or feedback?
We're all ears-- send emails to partnerbase@crossbeam.com . <!-- VALIDATE-OK[person-address]: verbatim public Crossbeam Help Center text -->
🔗 Helpful Resources
- Crossbeam Insider
- What is Crossbeam?
- Add a Partner to Crossbeam
- Data Privacy
- How Discoverability Works in Crossbeam
- Use Partnerbase.com to find Partners Already On Crossbeam


## Contact Our Support Team (HC 3160301)
URL: https://help.crossbeam.com/en/articles/3160301-crossbeam-support

Crossbeam gives you several ways to get help, whether you need a quick answer or hands-on guidance from your account team. Start with our Support Team for day-to-day questions, work with your Account Success Manager (ASM) for account-specific strategy, or explore our self-serve resources anytime.
Reach our support team directly from within your Crossbeam account.
- Navigate to Help in the navigation bar
- Hover over Help and select Chat with Support to start a live chat
- Alternatively, email us at support@crossbeam.com <!-- VALIDATE-OK[person-address]: verbatim public Crossbeam Help Center text -->

Our support team is available Monday to Friday, 3:00 AM to 7:00 PM (EST).

Messages sent outside these hours receive a response on the next business day.

### Work with Your Account Success Manager (ASM)
Your Account Success Manager (ASM) is your primary point of contact for account strategy, guidance, and getting the most value out of Crossbeam over time. Reach out to your ASM directly for:
- Guidance on your ecosystem strategy and account setup
- Questions about your plan, seats, or renewal
- Help prioritizing which features to adopt next
If you are not sure who your ASM is, contact our support team and they will connect you.

### Self-Serve Resources
Prefer to find answers on your own? Crossbeam offers self-serve options, all accessible from the navigation bar in-app.


#### Help Center
The Help Center provides you with access to hundreds of articles covering every part of Crossbeam.
- Navigate to Help in the navigation bar
- Hover over Help and select Help Center

#### Crossbeam Academy
Crossbeam Academy offers free courses to help you get more out of your ecosystem.
- Navigate to Help in the navigation bar
- Hover over Help and select Crossbeam Academy . You will be redirected to the Academy in a new window
- You will be redirected to the Academy in a new window
- Select Course Catalog from the top menu to browse available courses
- Select Get Crossbeam Certified to work toward Crossbeam certification

#### Crossbeam AI Chat
Crossbeam AI Chat answers your questions instantly using Crossbeam's own knowledge base, playbooks, and your ecosystem data.
- Navigate to Ask AI in the navigation bar
- Enter your question to get an instant, AI-generated answer

- Installation Guide: Crossbeam for Salesforce (v2)
- For Sales Seats: Getting Started with Crossbeam and Crossbeam Features
- Crossbeam Enablement Catalog
- Crossbeam MCP Server


## 1. Exclude certain companies from your populations (HC 3889182)
URL: https://help.crossbeam.com/en/articles/3889182-customer-confidentiality-and-crossbeam

So, you uploaded your data into Crossbeam and you're ready to build populations and start sharing data with partners so you can find valuable overlaps. But wait! You have a clause in your contracts where you promise not to reveal the identity of some customers to third parties. What now? The following are some options so you can move forward and get the same great value out of Crossbeam.

If the companies with this confidentiality option are flagged in your CRM or CSV upload, you can exclude them from Crossbeam populations entirely so that they are strictly never revealed to partners. Check out population filtering to learn more. This works best if the number of companies with this option is relatively small.


### 2. You may be covered by your NDAs with your partners
Depending on the wording of your contract clause about keeping the customer relationship private, you may be comfortable sharing that knowledge with partners under NDAs and treating that knowledge as protected and proprietary. In these cases, the understanding with the partner is that the overlap is only to be used in the context of the partnership and not used for any external communications, including with the customer.


### 3. Create broad populations
Some companies opt to create a broader population called "All Relationships" that includes both customers and prospects, without disclosing which is which by not sharing the account status. That way, the identity of customers is protected by obscurity and you can still do account mapping across known entities, sorting out the details on a collaboration-by-collaboration basis.


### 4. Create strict sharing defaults and settings
Some companies opt to not share data about customer populations outward with partners, but instead make their partners share data inward to them. That way, you can see the overlaps and decide on the best course of action for each, but not have knowledge about the overlap leave in any automated fashion. ​

- Glossary of Key Terminology in Crossbeam
- Crossbeam Partner Collaboration Session
- Installation Guide: Crossbeam for Salesforce (v2)


## Overview (HC 12601327)
URL: https://help.crossbeam.com/en/articles/12601327-crossbeam-mcp-server

### FAQs
Who has access to Crossbeam MCP? Crossbeam MCP is available on all plans, including Free and Connector, at no extra cost. A Full Access or Sales seat is required to connect.

Admins can also control MCP access by role. Manage this from Settings > Roles & Permissions . Click Edit next to a role, locate the MCP permission, and set it to either Access or No Access . All roles default to Access .

What AI tools can use Crossbeam MCP? Crossbeam currently has native connectors for Claude, ChatGPT, Glean, Gong, Superhuman, and Outreach. You can also connect to any AI tool or workflow builder that supports custom MCP connections.

How can I stay up to date with Crossbeam’s MCP changes and updates?
Our changelog is the best place to stay up to date with new releases and updates to Crossbeam’s MCP.

What consumes Crossbeam Credits today?
As of September 1, 2026, Crossbeam Credits meter access to Crossbeam's MCP server, the connection that lets AI tools and agents easily work with your Crossbeam data. MCP is where Credits apply today. Over time, Credits may expand to meter other ways AI works with your Crossbeam data. ​ For the full picture on how Credits are counted, how to estimate usage, and how to buy more, see the Crossbeam Credits FAQ .
- Integrations Overview
- Understanding Partner Score in Crossbeam
- For Sales Seats: Getting Started with Crossbeam and Crossbeam Features
- Crossbeam Product Release Notes 06/17/26
- Connect your AI tools to Crossbeam via MCP
