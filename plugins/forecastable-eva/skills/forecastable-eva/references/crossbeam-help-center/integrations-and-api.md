# Collection: Integrations And Api

Source: https://help.crossbeam.com/en/collections/2111215-integrations-and-api. Captured September 30th, 2026.


## Overview (HC 10064960)
URL: https://help.crossbeam.com/en/articles/10064960-microsoft-dynamics-custom-object-integration

In this article:
- Overview
- Install Integration Crossbeam Authentication Steps Microsoft Dynamics 365 Authentication Steps
- Crossbeam Authentication Steps
- Microsoft Dynamics 365 Authentication Steps
- Crossbeam Overlaps in Microsoft Dynamics Display Crossbeam Overlaps on the Accounts Page Display Crossbeam Overlaps in the Navigation Bar
- Display Crossbeam Overlaps on the Accounts Page
- Display Crossbeam Overlaps in the Navigation Bar
- Troubleshooting
The Crossbeam custom object integration with Microsoft Dynamics lets you bring partner ecosystem data directly into your Dynamics environment. With this integration, you can:
- Build Custom Dashboards and Reports : Create dashboards in Microsoft Dynamics that provide insights into your ecosystem to inform strategic decisions.
- Empower Sales Teams : Give your sales team access to ecosystem data, helping them prioritize accounts and close deals faster.
- Showcase Ecosystem Impact : Highlight the value of your partner ecosystem to stakeholders, supporting data-driven decisions and growth.
This integration is designed to help your team maximize the value of your partner ecosystem and drive revenue growth.
❗️ Important
Microsoft Dynamics Custom Object Integration is only available on the Supernode Plan. To upgrade your account, visit the Plan & Billing page .

To establish this integration, you must be a Crossbeam admin. Learn more about user seats and roles in Crossbeam here .

This integration works with: Dynamics 365 Sales Premium, Dynamics 365 Sales Enterprise, or Dynamics 365 Sales Professional.

### Install Integration
From the Integrations workspace, locate the Microsoft Dynamics Custom Object tile from the Available Integrations section and click the Install button.


#### Crossbeam Authentication Steps
Next, you will complete Crossbeam Authentication in the pop-up modal.

You will be prompted to add a new account; click Next when done.

Once you have completed The Crossbeam Authentication, you will be prompted to complete the Microsoft Dynamics 365 Authentication.

#### Microsoft Dynamics 365 Authentication Steps
On the Microsoft Dynamics 365 authentication screen, click add a new account .

In the next window, add the URL for the Microsoft Dynamics instance.

When complete, select Create .

If prompted, log in to your Microsoft Dynamics account.
✍️ Note
The initial setup and authentication process may take some time to complete. Please be patient.
The next screen will display Dynamic Crossbeam Overlap Entity Creation once the custom object has been created. Click Next .

The next screen confirms the installation is complete. Click Finish to close the authentication process.

✍️ Note
Opportunity fields are not currently pushed into Microsoft Dynamics.

### Crossbeam Overlaps in Microsoft Dynamics
Build custom dashboards and reports in Microsoft Dynamics to gain insights into your ecosystem and guide strategic decisions.


#### Display Crossbeam Overlaps on the Accounts Page
To display Crossbeam Overlaps in Microsoft Dynamics:
- Navigating to an Account Page in Microsoft Dynamics Go to the top menu and click on Advanced Settings In the settings menu, select the Default Solution Within the solution, find the Crossbeam Overlaps object or table Go to the Relationships section, select Account, and click Edit In the advanced options, locate the Display Settings Choose to display plural names or select the customized table option After making your changes, click Save Return to the main menu and select Publish All Customizations to make the changes live
- Go to the top menu and click on Advanced Settings
- In the settings menu, select the Default Solution
- Within the solution, find the Crossbeam Overlaps object or table
- Go to the Relationships section, select Account, and click Edit
- In the advanced options, locate the Display Settings
- Choose to display plural names or select the customized table option
- After making your changes, click Save
- Return to the main menu and select Publish All Customizations to make the changes live

Once these steps are complete, you will be able to view related Crossbeam overlaps on the account page.

#### Display Crossbeam Overlaps in the Navigation Bar
Add a link to Crossbeam Overlaps in the Microsoft Dynamics Navigation Bar:
- Open Settings in Microsoft Dynamics: Navigate to Advanced Settings Click Solutions from the menu and select the Default Solution from the displayed options In the Default Solution, find Site Maps from the search bar and select Sales Hub from the displayed options Locate the Sales Insight Settings and click on it. Locate the ➕ icon and click Sub Area Under the Sub Area: Select Entity under the Type dropdown options Select Crossbeam Overlap under the Entity dropdown options Save and close your changes Click Done in the pop-up Back on the main menu and click Publish to apply the changes
- Navigate to Advanced Settings
- Click Solutions from the menu and select the Default Solution from the displayed options
- In the Default Solution, find Site Maps from the search bar and select Sales Hub from the displayed options
- Locate the Sales Insight Settings and click on it.
- Locate the ➕ icon and click Sub Area
- Under the Sub Area: Select Entity under the Type dropdown options Select Crossbeam Overlap under the Entity dropdown options Save and close your changes Click Done in the pop-up
- Select Entity under the Type dropdown options
- Select Crossbeam Overlap under the Entity dropdown options
- Save and close your changes
- Click Done in the pop-up
- Back on the main menu and click Publish to apply the changes
- (Optional) to customize the Columns in the Crossbeam Overlaps View: Navigate back to Settings Locate Crossbeam Overlap under Tables and click the arrow to expand Select the Views from the options Click on All Crossbeam Overlaps from the displayed view options From here, you can modify columns, adjust column order, set filters, and make any additional customizations as needed
- Navigate back to Settings
- Locate Crossbeam Overlap under Tables and click the arrow to expand
- Select the Views from the options
- Click on All Crossbeam Overlaps from the displayed view options
- From here, you can modify columns, adjust column order, set filters, and make any additional customizations as needed

These steps will add a quick link to the Crossbeam Overlaps list in your Microsoft Dynamics Sales Hub navigation bar and allow you to customize the view as desired.

### Troubleshooting
During the Microsoft Dynamics integration installation, users may encounter an error when the custom entity is created.
- Message: ERROR: Please back up a screen and try again.

To correct this error:
- Click on the Previous button to go back a screen.
- Click on Next to proceed again.
This action should reset the integration process and allow you to continue with the installation. If the error persists, please contact support for further assistance.
🎓 Head over to Crossbeam Academy to dive deeper into the MSD integration.
- Integrations Overview
- Connect Microsoft Dynamics
- HubSpot Custom Object Integration
- Crossbeam Product Release Notes--11/13/2024
- Clay + Crossbeam Integration


## Overview (HC 10064990)
URL: https://help.crossbeam.com/en/articles/10064990-ready-to-use-salesforce-crossbeam-reports

In this article:
- Overview
- Reports: How-To Video
- How to Make the Crossbeam Reports Folder Visible
- What type of Crossbeam Reports are available?
The Crossbeam Ready-to-Use Reports for Salesforce provide fast, actionable insights into ecosystem data, reducing the need for RevOps support. Ready-to-use templates empower Sales, Partnerships, and Customer Success teams to make data-driven decisions, boost growth, and close deals.

These tools give a clear view of ecosystem data for specific use cases, like sourcing new leads, influencing deals, and retaining customers, enabling teams to communicate Crossbeam’s value to revenue leaders effectively.

### Reports: How-To Video

### How to Make the Crossbeam Reports Folder Visible
The Reports folder in Salesforce initially defaults to private, meaning only a Salesforce Admin will initially have access to this folder.

To make the Crossbeam Reports folder visible, a Salesforce Admin must complete the following steps to share it with the appropriate users, roles, or groups.
- In Salesforce, navigate to the Reports Tab and select All Folders
- Locate the Crossbeam Reports folder and click the Dropdown arrow at the end of the row to display the menu options
- Select Share from the options
- In the Share Folder modal: Under the Share With section, click the dropdown arrow and select Users, Roles, and/or Public Groups Under the Who Can Access section, confirm the selected Users, Roles and/or Public Groups are displayed with View Access
- Under the Share With section, click the dropdown arrow and select Users, Roles, and/or Public Groups
- Under the Who Can Access section, confirm the selected Users, Roles and/or Public Groups are displayed with View Access

😎 Pro Tip
Ready to level up? Build a Salesforce dashboard for a clear, high-level view of sourcing, influencing, and expanding customer relationships.
- Quickly evaluate opportunities for sourcing, influencing, and expanding customer relationships
- Identify trends, prioritize accounts, and focus on high-impact actions within your revenue pipeline
Learn how to create the Crossbeam 360 Dashboard in this article.
✍️ Note
Ready-to-Use Crossbeam Reports for Salesforce are only available on the Supernode plan.

Ready-to-Use Crossbeam Reports for Salesforce require the Salesforce Custom Object Integration; learn more here .

To upgrade your account, visit the Plan & Billing page .

### What type of Crossbeam Reports are available?
Crossbeam Reports are organized by specific use cases. These reports make Crossbeam data actionable by highlighting key account overlaps with your partners.
- Source Opportunities : Identify ecosystem-qualified leads by comparing your prospects to your partners' customers.
- Influence Deals : Understand which of your open opportunities overlap with your partners' customer bases, helping to enhance deal influence.
- Retain & Expand Customers : Track expansion opportunities by analyzing overlap between your customer base and your partners' customers.
Each report template is crafted to help you extract value from ecosystem data, turning insights into targeted actions that can drive your success.

To access Crossbeam Reports:
- Go to Reports in Salesforce
- Select All Folders
- Find and open Crossbeam Reports to view available reports

Click the Done button.

Available Reports:
| Ecosystem Qualified Leads | Expansion Opportunities with Stages | Expansion Opportunities with Partner Overlaps |
| Opportunity Influence (by Stage) | Partner Mutual Customers | Top Revenue EQLs |
| Expansion Opportunities | Opportunity Influence (by Owner) | |
📄 Related Articles
- Installation Guide: Crossbeam for Salesforce (v2)
- Salesforce Guide for Reports, Dashboards, & Automations Powered by Crossbeam
- Installation Guide: Crossbeam for Salesforce (v2)
- For Sales Seats: Getting Started with Crossbeam and Crossbeam Features
- Create the Crossbeam 360 Dashboard in Salesforce
- Access Crossbeam Deal Navigator inside Salesforce


## Overview (HC 10080441)
URL: https://help.crossbeam.com/en/articles/10080441-clay-crossbeam-integration

In this article:
- Overview About the Clay + Crossbeam Integration
- About the Clay + Crossbeam Integration
- Key Use Cases
- Building Lists with Ecosystem Data How to Get Started Using Your Table
- How to Get Started
- Using Your Table
- FAQs

Clay is a powerful tool designed to support go-to-market (GTM) teams in scaling growth across outbound, inbound, expansion, and retention efforts. It consolidates and enriches your team’s data, making it easy to create personalized outreach at scale.


#### About the Clay + Crossbeam Integration
The Clay + Crossbeam integration allows you to seamlessly import accounts based on overlaps with key partners, automatically crafting tailored outreach and syncing it to your sales engagement tools. This ensures your sales team always delivers a relevant, partner-aligned message, driving faster deal cycles and more effective ecosystem-led growth.
- Data Sharing: Clay pulls all available data shared by your partners, such as their CRM data
- Setup: Integration is configured within Clay, with no additional setup required in Crossbeam
❗️ Important
There are no additional setup requirements in Crossbeam. This integration is configured within Clay.

The Crossbeam Clay Integration is only available on the Supernode Plan. To upgrade your account, visit the Plan & Billing page .

The Crossbeam integration within Clay is only available via a Clay Pro plan. To upgrade your account, visit the Clay Plan & Billing page .

### Key Use Cases
- Achieve 100% ICP (Ideal Customer Profile) Accuracy Further qualify high - intent leads with relevant ecosystem data: Import existing Ecosystem Qualified Leads (EQLs) through Crossbeam and enhance them with additional firmographic and intent data, creating a highly targeted list.
- Import existing Ecosystem Qualified Leads (EQLs) through Crossbeam and enhance them with additional firmographic and intent data, creating a highly targeted list.
- Automate Personalized Outreach With ecosystem data layered into Clay tables, outreach gets even more relevant: Prospecting : Trigger workflows in CRMs like HubSpot or sales tools like Outreach to send hyper-personalized messaging based on the data in your Clay table, highlighting shared connections or partner benefits Co-marketing : Segment accounts for campaigns based on partner overlap and trigger outreach sequences tailored to each segment's relationship with partners
- Prospecting : Trigger workflows in CRMs like HubSpot or sales tools like Outreach to send hyper-personalized messaging based on the data in your Clay table, highlighting shared connections or partner benefits
- Co-marketing : Segment accounts for campaigns based on partner overlap and trigger outreach sequences tailored to each segment's relationship with partners
- Notify Reps of Co-Selling Opportunities Provide real-time insights on accounts ready for collaboration: Alerts : Enable real-time notifications for your reps and partner reps when a new co-sell opportunity arises based on ecosystem data
- Alerts : Enable real-time notifications for your reps and partner reps when a new co-sell opportunity arises based on ecosystem data

### Building Targeted Lists with Ecosystem Data
With the Clay + Crossbeam integration, you can create highly targeted account lists using ecosystem data.
✍️Note
Make sure your partners and Populations are correctly configured in Crossbeam before completing the steps below.

#### How to Get Started
- In your Clay workspace, navigate to Create New
- Select the Crossbeam Source action
- Within the Crossbeam Source action, Click Add Account

- You will be redirected to the Crossbeam authentication page to authorize access from Clay
- Authenticate your Crossbeam account within Clay to allow it as a source within Clay tables
- Import your Crossbeam data into your Clay tables
- Select your organization, partner, and relevant Populations
- Set overlap limits for imported data to return into your table

Click Continue when done.

If you are adding Crossbeam to an existing table:
- In the top right corner of your Clay table, select Actions > Import
- Select the Crossbeam Source action

#### Using Your Table
- Click into the Source Cell for overlapping accounts to see additional data including partner owner, record email, and other key data points

- New accounts matching your criteria will automatically be sent into the Clay table, allowing you to set up workflows that trigger whenever a new account matches your source criteria.
By leveraging the Crossbeam + Clay integration, GTM teams can streamline partner-aligned outreach and boost collaboration, ultimately driving ecosystem-led growth.

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


## Overview (HC 10080455)
URL: https://help.crossbeam.com/en/articles/10080455-universal-integration-settings

In this article:
- Overview
- Where to Find Universal Integration Settings Integrations with Universal Integration Settings
- Integrations with Universal Integration Settings
- Manage Universal Integration Settings
The Universal Integration Settings page centralizes integration controls, simplifying data management and giving users greater control over what data is pushed to the chosen integration. With this cohesive setup, users can easily customize integration behavior to fit their specific needs.

✍️ Note
Universal Integration Settings are only available on Connector and Supernode plans.

To upgrade your account, visit the Plan & Billing page .

### Where to Find Universal Integration Settings
From the left-side menu, click on the Data icon. From the side panel, select Integrations and open the Settings of your integration.

#### Integrations with Universal Integration Settings
Universal Integration Settings apply to the following integrations:
- All Copilots
- Snowflake Custom Object
- HubSpot Custom Object
- Salesforce Custom Object
- Gong Integration
- MS Dynamics Custom Object

### Managing Universal Integration Settings
The Universal Integration Settings provide a streamlined view of key options for managing data pushes.
- Adjust Data Pushes Toggle on or off to enable or disable data pushes for new partners or data populations as needed
- Toggle on or off to enable or disable data pushes for new partners or data populations as needed
- View Estimated Record Exports See an estimate of the records that will be exported through each integration for better transparency
- See an estimate of the records that will be exported through each integration for better transparency
- Customize Data in Push Click the arrow next to My Population to expand your available Populations Select or deselect the Populations to be pushed into the integration Click the arrow next to Partner Populations to expand and see the available Populations
- Click the arrow next to My Population to expand your available Populations Select or deselect the Populations to be pushed into the integration
- Select or deselect the Populations to be pushed into the integration
- Click the arrow next to Partner Populations to expand and see the available Populations
- Partner-Specific Settings You can choose to apply these settings to all specific partners collectively or customize them individually for each partner, depending on your needs
- You can choose to apply these settings to all specific partners collectively or customize them individually for each partner, depending on your needs
- Re-authorization If there are any authorization changes or errors with the integration, click the Re-authorize button and follow the prompts to complete the process
- If there are any authorization changes or errors with the integration, click the Re-authorize button and follow the prompts to complete the process
After making your selections, click Save to confirm and apply your changes.
- Snowflake Integration
- HubSpot Custom Object Integration
- Enhanced Ecosystem Reporting: “is a customer of” & “is an opportunity for” Fields in HubSpot
- Enhanced Ecosystem Reporting: “is a customer of” & “is an opportunity for” Fields in Salesforce
- How to Set Up the Partner Account CRM Integration


## Overview (HC 10149634)
URL: https://help.crossbeam.com/en/articles/10149634-create-the-crossbeam-360-dashboard-in-salesforce

In this article:
- Overview
- Dashboard: How-To Video
- Step 1: Create a New Dashboard
- Step 2: Set Up the Dashboard Layout
- Step 3: Add Report Widgets to the Dashboard
- Step 4: Add Source Opportunities to the Dashboard
- Step 5: Add Influence Deals to the Dashboard
- Step 6: Add Retain & Expand Customers to the Dashboard
- Step 7: Review and Save

Building this dashboard in Salesforce provides a visual summary of your key use cases, enabling you to quickly evaluate opportunities for sourcing, influencing, and expanding customer relationships. By offering a high-level view of your data, it helps you identify trends, prioritize accounts, and focus on high-impact actions that drive success within your revenue pipeline.

Follow these steps to set up your dashboard and gain actionable insights at a glance.

### Dashboard: How-To Video
❗️ Important
Dashboards in Salesforce are built on reports. Ensure the Crossbeam reports you want to include are already created and contain relevant data.
Watch this video for the Crossbeam 360 dashboard overview:


### Step 1: Create a New Dashboard
- Go to the Dashboards tab in Salesforce
- Click on Create New Dashboard
- Give the dashboard a name (Crossbeam 360 Dashboard)
- Select a public folder to save the dashboard

### Step 2: Set Up the Dashboard Layout
For the next step, save the header graphic image below to your computer by right-clicking on it, selecting Save Image As, and choosing a location on your computer.

This will be your header graphic:

- You’ll see a grid layout where all components (widgets) will be placed.
Add a Header Graphic:
- Click Widget and select image
- Upload the graphic from your files
- Set Scale to Fit Width and click Add
- Adjust the image to fit the width and position it near the top of the grid


### Step 3: Add Report Widgets to the Dashboard


#### Add Ecosystem Qualified Leads Report Widget
- Click Widget and select Chart or Table from the options
- Select the Ecosystem Qualified Leads report from the Crossbeam Reports folder and click Select In the Add Widget modal: Click the Metric Chart under Display As Set the measure to Record Count Delete the default Title box Customize the footer with My prospects VS partners' customers Click Add
- In the Add Widget modal:
- Click the Metric Chart under Display As
- Set the measure to Record Count
- Delete the default Title box
- Customize the footer with My prospects VS partners' customers
- Click Add
- Drag and drop the widget directly under the header graphic

#### Add Top Revenue EQLs Report Widget
- Click Widget and select Chart or Table from the options
- Select the Top Revenue EQLs report from the Crossbeam Reports folder and click Select In the Add Widget modal: Click the metric chart under Display As Set the measure to Record Count Set Display Units to Shortened Number Set Ranges to: -100 & 1 Set Decimal Places to Automatic Delete the default Title box Customize the footer with My strategic prospects VS partners’ customers Click Add
- In the Add Widget modal:
- Click the metric chart under Display As
- Set the measure to Record Count
- Set Display Units to Shortened Number
- Set Ranges to: -100 & 1
- Set Decimal Places to Automatic
- Delete the default Title box
- Customize the footer with My strategic prospects VS partners’ customers
- Click Add
- Drag and drop the widget directly under the header graphic

#### Add Open Opps with Partner Overlaps Report Widget
- Click Widget and select Chart or Table from the options
- Select the Open Opps with Partner Overlaps report from the Crossbeam Reports folder and click Select On the Add Widget modal: Click the metric chart under Display As Set the measure to Record Count Set Display Units to Shortened Number Set Ranges to: -100 & 1 Set Decimal Places to Automatic Delete the default Title box Customize the footer with My open opps VS partners’ customers/open opps Click Add
- On the Add Widget modal:
- Click the metric chart under Display As
- Set the measure to Record Count
- Set Display Units to Shortened Number
- Set Ranges to: -100 & 1
- Set Decimal Places to Automatic
- Delete the default Title box
- Customize the footer with My open opps VS partners’ customers/open opps
- Click Add
- Drag and drop the widget directly under the header graphic

#### Add Partner Mutual Customers Report Widget
- Click Widget and select Chart or Table from the options
- Select Partner Mutual Customers report from the Crossbeam Reports folder and click Select In the Add Widget modal: Click the metric chart under Display As Set the measure to Record Count Set Display Units to Shortened Number Set Ranges to -100 & 1 Set Decimal Places to Automatic Delete the default Title box Customize the footer with My customers VS partners’ customers Click Add
- In the Add Widget modal:
- Click the metric chart under Display As
- Set the measure to Record Count
- Set Display Units to Shortened Number
- Set Ranges to -100 & 1
- Set Decimal Places to Automatic
- Delete the default Title box
- Customize the footer with My customers VS partners’ customers
- Click Add
- Drag and drop the widget directly under the header graphic

#### Add Expansion Opps Report Widget
- Click Widget and select Chart or Table from the options
- Select the Expansion Opps report from the Crossbeam Reports folder and click Select In the Add Widget modal: Click the metric chart under Display As Set the measure to Record Count Set Display Units to Shortened Number Set Ranges to -100 & 1 Set Decimal Places to Automatic Delete the default Title box Customize the footer with My customers with an open opp VS partners’ customers Click Add
- In the Add Widget modal:
- Click the metric chart under Display As
- Set the measure to Record Count
- Set Display Units to Shortened Number
- Set Ranges to -100 & 1
- Set Decimal Places to Automatic
- Delete the default Title box
- Customize the footer with My customers with an open opp VS partners’ customers
- Click Add
- Drag and drop the widget directly under the header graphic

### Step 4: Add Source Opportunities to the Dashboard

Click Widget and select Text from the options and add the following text:
| Source Opportunities Identify your prospects that are customers of your partners Use your partners to source new opportunities by getting unique insights, decision-making contacts, or an intro into the account. |
Adjust its size to fit the layout.

#### Add Top Revenue EQLs Widget
- Click Widget and select Chart or Table from the options
- Select the Top Revenue EQLs report from the Crossbeam Reports folder and click Select In the Add Widget modal: Click the metric chart under Display As Set the measure to Record Count Set Display Units to Shortened Number Set Ranges to -100 & 1 Set Decimal Places to Automatic Set Title to Top prospects to focus on (with a high projected revenue) Customize the footer with My customers with an open opp VS partners’ customers Click Add
- In the Add Widget modal:
- Click the metric chart under Display As
- Set the measure to Record Count
- Set Display Units to Shortened Number
- Set Ranges to -100 & 1
- Set Decimal Places to Automatic
- Set Title to Top prospects to focus on (with a high projected revenue)
- Customize the footer with My customers with an open opp VS partners’ customers
- Click Add
- Drag and drop the widget directly under the Source Opportunities widget box

#### Add Ecosystem Qualified Leads Widget
- Click Widget and select Chart or Table from the options
- Select the Ecosystem Qualified Leads report from the Crossbeam Reports folder and click Select In the Add Widget modal: Click the Donut Chart under Display As Set the value to Record Count Set Sliced by to Account: Account Owner check boxes for: Show Values, Combine Small Groups into “others”, Show Total Set Decimal Places to Automatic Set Sort By to Account: Account Owner Set Max Values Displayed to 100 Set Title to Prospects to Source Deals Set Legend Position to Right Click Add
- In the Add Widget modal:
- Click the Donut Chart under Display As
- Set the value to Record Count
- Set Sliced by to Account: Account Owner check boxes for: Show Values, Combine Small Groups into “others”, Show Total
- check boxes for: Show Values, Combine Small Groups into “others”, Show Total
- Set Decimal Places to Automatic
- Set Sort By to Account: Account Owner
- Set Max Values Displayed to 100
- Set Title to Prospects to Source Deals
- Set Legend Position to Right
- Click Add
- Drag and drop the widget directly under the Ecosystem Qualified Leads Widget

#### Add Ecosystem Qualified Leads Table Widget
- Click Widget and select Chart or Table from the options
- Select the Ecosystem Qualified Leads report from the Crossbeam Reports folder and click Select In the Add Widget modal: Click the Lightning Table under Display As Add Columns: Account: Account Owner, Account: Account Name, Partner Name, Account: Revenue Bands Set Sort By to Account: Revenue Bands (descending arrow) Set Display Units by Shortened Number Set Decimal Places to Automatic Set Max Groups Displayed to 100 Set Title to Accounts where partners can help source opportunities Click Add
- In the Add Widget modal:
- Click the Lightning Table under Display As
- Add Columns: Account: Account Owner, Account: Account Name, Partner Name, Account: Revenue Bands
- Account: Account Owner, Account: Account Name, Partner Name, Account: Revenue Bands
- Set Sort By to Account: Revenue Bands (descending arrow)
- Set Display Units by Shortened Number
- Set Decimal Places to Automatic
- Set Max Groups Displayed to 100
- Set Title to Accounts where partners can help source opportunities
- Click Add
- Drag and drop the widget directly under the Source Opportunities text box

### Step 5: Add Influence Deals to the Dashboard

Click Widget and select Text from the options and add the following text:
| Influence Deals Identify your open opportunities that are customers or open opps of your partners Use your partners to influence deals by getting unique insights, decision-making contacts, or an intro to new stakeholders. |
Adjust its size to fit the layout.

#### Add Open Opps with Partner Overlaps Report Widget
- Click Widget and select Chart or Table from the options
- Select the Open Opps with Partner Overlaps report from the Crossbeam Reports folder and click Select In the Add Widget modal: Click the Metric Chart under Display As Set the measure to Record Count Set Display Units to Shortened Number Set Ranges to -100 & 1 Set Decimal Places to Automatic Set the Title to Open Opportunities that can be influenced by Partners Click Add
- In the Add Widget modal:
- Click the Metric Chart under Display As
- Set the measure to Record Count
- Set Display Units to Shortened Number
- Set Ranges to -100 & 1
- Set Decimal Places to Automatic
- Set the Title to Open Opportunities that can be influenced by Partners
- Click Add
- Drag and drop the widget directly under the Influence Deals text box

#### Add Opportunity Influence (By Stage) Widget
- Click Widget and select Chart or Table from the options
- Select the Opportunity Influence (By Stage) report from the Crossbeam Reports folder and click Select In the Add Widget modal Click the Vertical Bar Chart under Display As Set X-Axis to Opportunity: Stage Set Y-Axis to: Record Count, Sum of Amount Check the boxes for: Plot as Line Chart, Plot on Second Axis Set Display Units by Shortened Number Set Y-Axis Range to Automatic Set Decimal Places to Automatic Set Sort by to Opportunity: Stage Set Max Groups Displayed to 100 Set Title to Open Deals that can be influenced by Partners Set Legend Position to Bottom Click Add
- In the Add Widget modal
- Click the Vertical Bar Chart under Display As
- Set X-Axis to Opportunity: Stage
- Set Y-Axis to: Record Count, Sum of Amount Check the boxes for: Plot as Line Chart, Plot on Second Axis
- Check the boxes for: Plot as Line Chart, Plot on Second Axis
- Set Display Units by Shortened Number
- Set Y-Axis Range to Automatic
- Set Decimal Places to Automatic
- Set Sort by to Opportunity: Stage
- Set Max Groups Displayed to 100
- Set Title to Open Deals that can be influenced by Partners
- Set Legend Position to Bottom
- Click Add
- Drag and drop the widget directly under the Open Opportunities that can be influenced by Partners Widget

#### Add Opportunity Influence (By Owner) Widget
- Click Widget and select Chart or Table from the options
- Select the Opportunity Influence (By Owner) report from the Crossbeam Reports folder and click Select In the Add Widget modal: Click the Donut Chart under Display As Set the value to Sum of Amount Set Sliced by to Opportunity: Opportunity Owner Set Display Units to Shortened Number Check the boxes for: Show Values, Combine Small Groups into “others, Show Total Set Decimal Places to Automatic Set Sort By to Opportunity: Opportunity Owner Set Max Values Displayed to 6 Set Title to Amount of Open Deals that can be influenced by Partners Set Legend Position to Right Click Add
- In the Add Widget modal:
- Click the Donut Chart under Display As
- Set the value to Sum of Amount
- Set Sliced by to Opportunity: Opportunity Owner
- Set Display Units to Shortened Number Check the boxes for: Show Values, Combine Small Groups into “others, Show Total
- Check the boxes for: Show Values, Combine Small Groups into “others, Show Total
- Set Decimal Places to Automatic
- Set Sort By to Opportunity: Opportunity Owner
- Set Max Values Displayed to 6
- Set Title to Amount of Open Deals that can be influenced by Partners
- Set Legend Position to Right
- Click Add
- Drag and drop the widget directly under the Open Deals that can be influenced by Partners Widget

#### Add Opportunity Influence (By Owner) Table Widget
- Click Widget and select Chart or Table from the options
- Select Opportunity Influence (By Owner) report from the Crossbeam Reports folder and click Select In the Add Widget modal: Click the Lightning Table under Display As Add Columns: Opportunity: Opportunity Owner, Opportunity: Opportunity Name, Opportunity: Stage, Opportunity: Amount, Partner Name, Partner Standard Populations Set Sort By to Opportunity: Amount (descending arrow) Set Display Units by Shortened Number Set Decimal Places to Automatic Set Max Groups Displayed to 100 Set Title to Oppty Influence (By Owner) Click Add
- In the Add Widget modal:
- Click the Lightning Table under Display As
- Add Columns: Opportunity: Opportunity Owner, Opportunity: Opportunity Name, Opportunity: Stage, Opportunity: Amount, Partner Name, Partner Standard Populations
- Opportunity: Opportunity Owner, Opportunity: Opportunity Name, Opportunity: Stage, Opportunity: Amount, Partner Name, Partner Standard Populations
- Set Sort By to Opportunity: Amount (descending arrow)
- Set Display Units by Shortened Number
- Set Decimal Places to Automatic
- Set Max Groups Displayed to 100
- Set Title to Oppty Influence (By Owner)
- Click Add
- Drag and drop the widget directly under the Influence Deals text box

### Step 6: Add Retain & Expand Customers to the Dashboard

Click Widget and select Text from the options and add the following text:
| Retain & Expand Customers Identify your customers that are also customers of your partners Use your partners to understand ways to expand your clients’ usage of your product and integrations, request an intro to new stakeholders, or to gather intel and recommendations. |
Adjust its size to fit the layout.

#### Add Expanision Opps Report Widget
- Click Widget and select Chart or Table from the options
- Select the Expansion Opps report from the Crossbeam Reports folder and click Select In the Add Widget modal: Click the Metric Chart under Display As Set the Measure to Record Count Set Display Units to Shortened Number Set Ranges to -100 & 1 Set Decimal Places to Automatic Set the Title to Open Deals on Existing Customers Click Add
- In the Add Widget modal:
- Click the Metric Chart under Display As
- Set the Measure to Record Count
- Set Display Units to Shortened Number
- Set Ranges to -100 & 1
- Set Decimal Places to Automatic
- Set the Title to Open Deals on Existing Customers
- Click Add
- Drag and drop the widget directly under the Retain & Expand Customers text box

#### Add Expansion Opps Widget
- Click Widget and select Chart or Table from the options
- Select the Expansion Opps report from the Crossbeam Reports folder and click Select In the Add Widget modal: Click the Horizontal Bar Chart under Display As Set Y-Axis to: Opportunity: Opportunity Owner Set X-Axis to Sum of Opportunity: Amount Set Display Units by Shortened Number Check box: Show Values Set X-Axis Range to Automatic Set Decimal Places to Automatic Set Sort by to Opportunity: Opportunity Owner (ascending arrow) Set Max Groups Displayed to 100 Set Title to Expansion Opportunities Click Add
- In the Add Widget modal:
- Click the Horizontal Bar Chart under Display As
- Set Y-Axis to: Opportunity: Opportunity Owner
- Set X-Axis to Sum of Opportunity: Amount
- Set Display Units by Shortened Number Check box: Show Values
- Check box: Show Values
- Set X-Axis Range to Automatic
- Set Decimal Places to Automatic
- Set Sort by to Opportunity: Opportunity Owner (ascending arrow)
- Set Max Groups Displayed to 100
- Set Title to Expansion Opportunities
- Click Add
- Drag and drop the widget directly under the Open Deals on Existing Customers widget box

#### Add Expansion Opps with Stages Table Widget
- Click Widget and select Chart or Table from the options
- Select the Expansion Opps with Stages report from the Crossbeam Reports folder and click Select In the Add Widget modal: Click the Lightning Table under Display As Add Columns: Opportunity: Opportunity Owner, Opportunity: Account Name, Opportunity: Opportunity Name, Opportunity: Stage, Opportunity: Amount, Partner Name, Partner Standard Populations, Opportunity: Close Date Set Sort By to Opportunity: Close Date (descending arrow) Set Display Units by Shortened Number Set Decimal Places to Automatic Set Max Groups Displayed to 100 Set Title to Expansion Opps with Stages Click Add
- In the Add Widget modal:
- Click the Lightning Table under Display As
- Add Columns: Opportunity: Opportunity Owner, Opportunity: Account Name, Opportunity: Opportunity Name, Opportunity: Stage, Opportunity: Amount, Partner Name, Partner Standard Populations, Opportunity: Close Date
- Opportunity: Opportunity Owner, Opportunity: Account Name, Opportunity: Opportunity Name, Opportunity: Stage, Opportunity: Amount, Partner Name, Partner Standard Populations, Opportunity: Close Date
- Set Sort By to Opportunity: Close Date (descending arrow)
- Set Display Units by Shortened Number
- Set Decimal Places to Automatic
- Set Max Groups Displayed to 100
- Set Title to Expansion Opps with Stages
- Click Add
- Drag and drop the widget directly under the Retain & Expand Customers text box

### Step 7: Review and Save
- Review it for consistency and ensure all widgets use the appropriate reports
- Save the dashboard once all widgets are added and customized
- Return to the Dashboard at any time; click the edit pencil to make changes
- Crossbeam Copilot for Salesforce
- Salesforce Guide for Reports, Dashboards, & Automations Powered by Crossbeam
- Ready-to-Use Salesforce Crossbeam Reports
- Create the Crossbeam 360 Dashboard in HubSpot


## Overview (HC 10445323)
URL: https://help.crossbeam.com/en/articles/10445323-enhanced-ecosystem-reporting-is-a-customer-of-is-an-opportunity-for-fields-in-hubspot

In this article:
- Overview
- How to Get Started Manage Settings
- Manage Settings
- Use Cases
Turn your HubSpot data into action. Kick off your HubSpot training in Crossbeam Academy.

This new feature enhances the Crossbeam-HubSpot integration by pushing is a customer of and is an open opportunity of fields directly to the standard HubSpot Company object, unlocking advanced reporting capabilities and streamlined workflows.

These fields can:
- Be applied as filters for precise targeting
- Generate new or supplement existing reports for actionable insights
Key Benefits:
- Improve Pipeline Efficiency: Provide actionable insights within HubSpot, enabling sales teams to focus on high-value accounts
- Eliminate Tool-Switching: Access Crossbeam data directly within HubSpot for more informed and efficient decision-making
- Automate Workflows: Set up workflows to streamline processes such as task assignments, follow-ups, and deal updates on Ecosystem Qualified Leads (EQLs)

### How to Get Started
✍️ Note
This feature is only available on the Supernode plan. To upgrade your account, visit the Plan & Billing page .
- You must have a Full Access Seat in Crossbeam Core with Integration permissions to install.
- Enterprise license is required to utilize and push data to the custom object. Check your plan in HubSpot by visiting the Account & Billing page to confirm compatibility.
Required Permissions
To create these fields in HubSpot, the HubSpot user must have:
- Edit access on the Company (Account) properties
Without these permissions, the properties cannot be created or populated.
In Crossbeam, navigate to the Data → Integrations → Settings for the HubSpot integration row.

Under General Settings: Toggle Enable Data Push ON

Click Save General Settings when done.
- Next, click on the Crossbeam Custom Object tab Toggled ON Push to Custom Object to send overlaps to HubSpot
- Toggled ON Push to Custom Object to send overlaps to HubSpot

Click Save Custom Object when done.

Company Object tab:
- Toggle Push to HubSpot Object ON to push partner overlap data into HubSpot

Click Save Company Object to apply your settings.

In HubSpot, go to the Company section and apply filters to see these new fields:

Click on a specific Company to see the specific fields that are being pushed from Crossbeam.

If NONE is displayed under the field name, this means there is no data currently connected to that field.
✍️ Note
For detailed information about the HubSpot Custom Object, refer to the complete installation guide here .

#### Manage Settings
Return to the Crossbeam integration workspace and click on the Settings at anytime to adjust the data push.
✍️ Note
This integration only pushes data; it never deletes anything existing in HubSpot. Data cleanup is the user's responsibility.

### Use Cases

#### Sales Operations
- Pipeline Analysis: Filter accounts with partner overlap to measure the influence of ecosystem insights on revenue and optimize resources accordingly.

#### Sales Leaders
- Report Creation: Generate detailed co-selling or cross-selling reports by leveraging Crossbeam data to identify ideal partners for collaboration.
- Revive Stalled/Lost Opportunities: Use partner data to re-engage stalled or lost deals by tapping into trusted relationships.
- Market Entry Planning: Build reports to identify high-value prospects who are already customers of partners, aiding in referrals, warm introductions, and market entry strategies.
- Workflow Automation: Automate follow-ups, task assignments, and deal updates for accounts with high partner alignment potential to ensure no opportunity is overlooked.
- HubSpot Custom Object Integration
- Crossbeam Copilot for HubSpot
- Enhanced Ecosystem Reporting: “is a customer of” & “is an opportunity for” Fields in Salesforce
- How to Create a Crossbeam Report in HubSpot


## Overview (HC 10578034)
URL: https://help.crossbeam.com/en/articles/10578034-how-to-upgrade-from-the-crossbeam-legacy-salesforce-integration-v1-to-v2

In this article:
- Overview
- Step-by-Step Upgrade Process Step 1: Review your current Integration Setup Step 2: Install the v2 Integration Step 3: Configure Data Push Settings in Crossbeam Step 4: Validate Update in Salesforce Step 5: Deactivate v1 in Crossbeam
- Step 1: Review your current Integration Setup
- Step 2: Install the v2 Integration
- Step 3: Configure Data Push Settings in Crossbeam
- Step 4: Validate Update in Salesforce
- Step 5: Deactivate v1 in Crossbeam
- FAQs
Crossbeam’s Salesforce v2 integration offers improved performance and new report building features. This guide walks you through everything you need to know to upgrade from v1 to v2 smoothly.
✍️ Note
Please set aside at least 30 minutes to complete the upgrade process following the steps below.

### Step-by-Step Upgrade Process

#### Step 1: Review your Current Integration Setup
Click on Data from the navigation bar, then select Integrations from the dropdown

Scroll down the page to locate the Salesforce Custom Object Legacy row .

Click the Install button.


#### Step 2: Install the v2 Integration
In the pop-up window, complete both the Crossbeam and Salesforce authentication steps when prompted.

On the Salesforce Custom Object Package screen, you do not need to download the package again. Click Next, then click Finish in the following window to complete the process.


#### Step 3: Configure Data Push Setting in Crossbeam
In Crossbeam, click on Data from the navigation bar, and select Integrations .

Scroll down the page to locate the Salesforce Custom Object row . Click the Setting button .

In the Settings panel:
- Adjust Data Pushes Toggle on or off to enable or disable data push Select or deselect the box next to Push Opportunity Data
- Toggle on or off to enable or disable data push
- Select or deselect the box next to Push Opportunity Data
- Customize Data in Push Click the arrow next to My Population to expand your available Populations Select or deselect the Populations to be pushed into the integration Click the arrow next to Partner Populations to expand and see the available Populations
- Click the arrow next to My Population to expand your available Populations Select or deselect the Populations to be pushed into the integration
- Select or deselect the Populations to be pushed into the integration
- Click the arrow next to Partner Populations to expand and see the available Populations
- Add new Partnerships Automatically Toggle on or off to automatically add new partners
- Toggle on or off to automatically add new partners
- Partner-Specific Settings You can choose to apply these settings to all specific partners collectively or customize them individually for each partner, depending on your needs
- You can choose to apply these settings to all specific partners collectively or customize them individually for each partner, depending on your needs

After making your selections, click Save Changes to confirm.

#### Step 4: Validate Update in Salesforce
In Salesforce, go to Setup in the Setup menu. Use the quick find search to locate the Object Manager. Open Object Manager and search for Crossbeam Ecosystem Overlap, which should appear as a deployed Custom Object.

Please note, v2 is called Crossbeam Ecosystem Overlap.

However, v1 (called Crossbeam Overlap ) will also be displayed in the table. Your Salesforce admin will be able to make modifications to workflows connected to the v1 custom object and to hide reports connected to v1.
😎 Pro Tip
Be sure to check out the new Crossbeam Reports available with Salesforce v2.

#### Step 5: Deactivate v1 in Crossbeam
In Crossbeam, click on Data from the navigation bar, and select Integrations .

Scroll down the page to locate the Salesforce Custom Object Legacy row . Click the Setting button .

In the Setting panel, deselect all the boxes, and this data will be removed during the next sync.

Click here for the full guide on installing and configuring the Crossbeam Managed Package for Salesforce (v2), including Crossbeam Copilot.

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


## Overview (HC 10742955)
URL: https://help.crossbeam.com/en/articles/10742955-enhanced-ecosystem-reporting-is-a-customer-of-is-an-opportunity-for-fields-in-salesforce

In this Article:
- Overview
- How to Get Started Add Custom Fields in Salesforce Enable Data Push in Crossbeam Manage Settings
- Add Custom Fields in Salesforce
- Enable Data Push in Crossbeam
- Manage Settings
- Use Cases Clari Use Case
- Clari Use Case
With these new Salesforce fields, you can integrate Ecosystem insights into Salesforce, enabling more informed decision-making, streamlined workflows, and enhanced revenue opportunities.

Key Benefits:
- Actionable Partner Data: Automatically populate is a customer of & is an open opportunity for fields on the Account object
- Enhanced Reporting: Use these fields as filters in new or existing reports for deeper ecosystem insights
- Seamless Integration: Leverage this data in tools like Clari, Gong, Gainsight, and more
- Workflow Automation: Sync partner insights across your Salesforce workflows for more efficient operations

### How to Get Started
✍️ Note
The Salesforce Custom Object is only available on the Supernode Plan. To upgrade your account, visit the Plan & Billing page .

Crossbeam for Salesforce must be installed before you can add these new fields.

This feature applies only to Standard Populations and does not work with Custom Populations.
😎 Pro Tip
Keep the complete Crossbeam for Salesforce Installation Guide close by for any questions. Click here to open it in another window.

#### Add Custom Fields in Salesforce
In your Salesforce instance, you will need to add two separate fields: is a customer of & is an open opportunity for to the Account object.
Required Permissions
To create these fields in Salesforce, the Salesforce user must have:
- Edit/Write access on the Account object
Without these permissions, the fields cannot be created or populated.
In Salesforce:
- Open the Setup gear icon
- Use the quick find search box and type Object Manager Select Account from the list of objects
- Select Account from the list of objects

- Click on Fields & Relationships for the side panel Click the New button
- Click the New button
- In the next screen, scroll down under Data Type and click next to Picklist (Multi-Select) Click the Next button
- Click the Next button
- Enter the following details: Field Label: is a customer of Values: select Enter Values and type NONE as the default value Uncheck the box next to Restrict picklist to predefined values (to allow dynamic partner names) The Field Name autopopulates from the label Check or uncheck the box next to Auto add the custom report type (you will be able to manually add the field later)
- Field Label: is a customer of
- Values: select Enter Values and type NONE as the default value
- Uncheck the box next to Restrict picklist to predefined values (to allow dynamic partner names)
- The Field Name autopopulates from the label
- Check or uncheck the box next to Auto add the custom report type (you will be able to manually add the field later)
- Click the Next button

- In the next screen, assign permissions to the Crossbeam Setup User and the assigned permission sets for your team.
- In the final step, decide whether to add the field to page layouts (optional) by checking or unchecking the boxes

Click Save & New to repeat these steps to create is an open opportunity for for the Account object.

#### Enable Data Push in Crossbeam
✍️ Note
Before setting up the data push in Crossbeam, you must complete all the custom field setup steps in your Salesforce standard account object.
In Crossbeam, navigate to the Data icon found on the left-side menu. From the side panel, select Integrations and open the Settings on the row for the Salesforce integration.

In the Settings, toggle ON Enable Data Push :
- In the Crossbeam Custom Object tab, ensure the push is toggled ON to send Crossbeam data overlaps to the Crossbeam custom object in Salesforce. Don't forget to hit Save!

- In the Account Object tab, toggle the Push to Account Object ON to send “is a customer of” and “is an opportunity for” fields in your standard Account object in Salesforce. You will see two drop-downs (one for each field). Select the Salesforce fields on which you would like to write the data. Hit Save!

Click Save Changes to apply your settings.
❗️ Important
Crossbeam cannot complete this data push unless the two custom fields are created in Salesforce first.
✍️ Note
Any partner-specific settings you’ve configured in the integration settings will also apply to this data push. For details on how these settings work, check out this article .

#### Manage Settings
Return to the Crossbeam Integration workspace and click on the Settings at anytime to adjust the data push.


### Use Cases
- Automated Workflows: Trigger alerts or automate actions when an account becomes a customer or opens an opportunity with a partner in your current Salesforce reports, dashboards, and workflows.
- Seamless GTM Integration: Push Crossbeam data into Clari, Gong, Gainsight, and any tool connected to Salesforce for deeper ecosystem insights

#### Clari Use Case
By integrating Crossbeam's is a customer of and is an opportunity for fields into Clari, you can enhance your sales strategies and pipeline analysis:
- Enhanced Pipeline Analysis: Push these custom fields to Clari to identify which accounts are customers or have open opportunities with your partners, allowing for more precise pipeline analysis
- Partner-Specific Insights: Filter by partner to refine your sales strategies, focusing on accounts with specific partner engagements

##### How this transforms your deal reviews on Clari
When a deal stalls, stop guessing your next move. Instead, you can create:
- Tailored Pitches: Customize your approach based on the tools your prospect already uses, increasing the relevance of your pitch
- Co-Selling Opportunities: Identify co-selling possibilities with partners working on the same account, fostering collaborative sales efforts
- Access to Decision-Makers: Discover decision-makers your partner is connected to but aren't yet in your CRM, facilitating strategic introductions
Additionally, learn how to show standard account fields on your opportunity grid in Clari by visiting: Salesforce Account Field on Opportunity Grid .
📄 Related Articles
- Getting Crossbeam data to Display in Clari
- Attribution for Salesforce Users
- Installation Guide: Crossbeam for Salesforce (v2)
- Enhanced Ecosystem Reporting: “is a customer of” & “is an opportunity for” Fields in HubSpot
- Crossbeam Product Release Notes--04/15/2025


## Overview (HC 11378668)
URL: https://help.crossbeam.com/en/articles/11378668-how-to-create-a-crossbeam-report-in-hubspot

In this article:
- Overview
- Create a Report Add Filters to the Report Add Visualization to the Report
- Add Filters to the Report
- Add Visualization to the Report

Ready to build smarter reports and dashboards? Kick off your HubSpot training in Crossbeam Academy.

Learn how to create a Crossbeam Overlaps report in HubSpot, apply filters, and push report results into dynamic HubSpot Lists for ongoing updates.
✍️ Note
Crossbeam Reporting in HubSpot is only available on the Supernode plan and require the HubSpot Custom Object .

To upgrade your account, visit the Plan & Billing page .

### Create a Report
In HubSpot, navigate to the reporting section on the main navigation bar:
- Select Reports from the dropdown options
- Click on the Create Report button.
- In the next screen, select Single Object as the report type
- in the search bar, type Crossbeam and select Crossbeam Overlaps
- Click the Next button

Set your Date Range
The report defaults to This quarter so far . Click on This quarter so far to open additional options, and select All data to view your full dataset.

Name Your Report
Click the pencil icon to give your report a name.

Add properties to the Report
By default, the report includes your partners and the Populations properties.
To add more Crossbeam properties:
- Click Add Crossbeam Overlap Property
- Use the search box to add additional Crossbeam properties to the report.


#### Add Filters to the Report
- Click Advanced filters in the report view
- In the side drawer, click the Add filter button
- Select filters such as Populations and Partner Populations to define your overlaps
- Edit the filter value in the Add Values field Continue to add filters as needed
- Continue to add filters as needed
- Close the side draw by clicking on the X in the top corner
✍️ Note
Filter values must be exact matches. Copy and paste Population names directly from the report for best results.

#### Add Visualization to the Report
After you close the filters, click the Next button to add Visualization to the report. Choose a chart type to display your data.
Under the Displaying section, drag and drop the available properties to display.

Click Save .

Your new report will now be available in your HubSpot reports list and will automatically update as account data changes in Crossbeam.
🎓 Want to go deeper? ​ Sign in to Crossbeam Academy to learn more about building and customizing HubSpot reports with Crossbeam data.
- HubSpot Custom Object Integration
- Crossbeam Copilot for HubSpot
- Enhanced Ecosystem Reporting: “is a customer of” & “is an opportunity for” Fields in HubSpot
- Create the Crossbeam 360 Dashboard in HubSpot


## Overview (HC 11394640)
URL: https://help.crossbeam.com/en/articles/11394640-create-the-crossbeam-360-dashboard-in-hubspot

In this article:
- Overview
- Step 1: Create a New Dashboard
- Step 2: Add the Header Image
- Step 3: Add News Feed Section
- Step 4: Add Reports to the Dashboard Sourced Opportunities Influenced Deals Retain and Expand Customers
- Sourced Opportunities
- Influenced Deals
- Retain and Expand Customers
Ready to build smarter dashboards? Kick off your HubSpot training in Crossbeam Academy.

The Crossbeam 360 Dashboard gives your team a visual summary of ecosystem activity by consolidating Crossbeam data inside HubSpot. Whether you're tracking partner-sourced opportunities or monitoring key segments, this dashboard enables smarter, data-informed decisions without leaving your CRM.

Before you begin, decide what you want to track.
- What partner-influenced metrics are most important to us?
- Who is this dashboard for sales leaders, CSMs, partner managers?
- Do we want to track by Population, overlap, source, or sync status?
❗️ Important
Dashboards in HubSpot are built on reports. Ensure the Crossbeam reports you want to include are already created and contain relevant data you need.
✍️ Note
Crossbeam 360 Dashboard in HubSpot is only available on the Supernode plan and require the HubSpot Custom Object .

To upgrade your account, visit the Plan & Billing page .

### Step 1: Create a new Dashboard
In HubSpot, navigate to the reporting section on the main navigation bar:
- Select Dashboards from the dropdown options
- Click on the Create Dashboard button
- Name your dashboard Crossbeam 360 Dashboard
- Choose who can view it
- Click Create Dashboard to save

### Step 2: Add the Header Image
For the next step, save the header graphic image below to your computer by right-clicking on it, selecting Save Image As, and choosing a location on your computer.

This will be your header graphic:

In your dashboard, click Actions and select Add images, text, or video from the dropdown.
- Click the Insert Image icon and upload the header image
- Resize the image to approximately 1300×150 pixels
- Click the Add button
- In the dashboard grid, drag the corner of the image block to span the top of the dashboard

### Step 3: Add News Feed Section
The News Feed section helps you stay on top of recent partner activity. Add both reports below under the dashboard image.
✍️ Note
You will need to build each report in the 360 Dashboard. Review this article on building reports to learn more.

#### News Feed: Prospects where a Partner recently closed a customer
Spot where a partner has recently converted a customer that overlaps with one of your prospects.

Visualization : Table
Filters : Set Include data if it matches to: ALL of the filters below
- Partner Population contains any of customers
- Population contains any of prospect
Columns :
- OBJECT LAST MODIFIED DATE/TIME, MONTHLY
- COMPANY NAME
- PARTNER NAME
- PARTNER AE NAME
- PARTNER POPULATION
- POPULATION
If your populations or fields are named differently, adjust the settings accordingly.


#### News Feed: Prospects where a Partner recently opened an opportunity
This report surfaces recent opportunity creation by your partners that may align with your prospect list.

Visualization : Table
Filters : Set Include data if it matches to: ALL of the filters below
- Partner Population contains any of open opportunities
Columns :
- OBJECT LAST MODIFIED DATE/TIME, MONTHLY
- COMPANY NAME
- PARTNER NAME
- PARTNER AE NAME
If your populations or fields are named differently, adjust the settings accordingly.

### Step 4: Add Reports to the Dashboard
Each section below aligns with a different stage of the partner lifecycle: Sourcing, Influencing, and Retaining/Expanding. Add the recommended reports to your dashboard to get a complete view of how partners are impacting your pipeline.
✍️ Note
You will need to build each report in the 360 Dashboard. Review this article on building reports to learn more.

#### Sourced Opportunities

In the Dashboard, click Actions, select Add images, text, or video . Copy and paste to the following text:
Source Opportunities
Identify partners already working with one of your cold prospects!
Use these partners to help you source a new opp by getting an idea of the prospect's tech stack, request an intro to a contact, get some intel on the account, or ask them to put in a good word on your behalf.

Drag the section to resize it in the dashboard.
How to Create
Report: Partners with a Customer Relationship
- Visualization : Horizontal Bar
- Filters : Set Include data if it matches to: ALL of the filters below Partner Population contains any of customers
- Set Include data if it matches to: ALL of the filters below Partner Population contains any of customers
- Partner Population contains any of customers
- X-Axis : COUNT OF COMPANIES
- Y-Axis : PARTNER NAME
Copy and paste the report description:
This report provides a detailed view of companies that are categorized as "customers" and have a population containing "Prospects." It highlights the names of these companies, their associated partners, and the owner responsible for them. This information can help you identify potential opportunities for collaboration or growth by focusing on customer relationships that also have prospective elements.

Save when done.
How to Create
Report: Accounts Where Partners Can Help Source Opportunities
- Visualization : Table
- Filters : Set Include data if it matches to: ALL of the filters below Partner Population is equal to any of customers Population contains any of prospect
- Set Include data if it matches to: ALL of the filters below Partner Population is equal to any of customers Population contains any of prospect
- Partner Population is equal to any of customers
- Population contains any of prospect
- Columns : COMPANY OWNER COMPANY NAME PARTNER NAME PARTNER POPULATION
- COMPANY OWNER
- COMPANY NAME
- PARTNER NAME
- PARTNER POPULATION
- Copy and paste the report Description : Use this table to view detailed accounts where partners have existing relationships and could help source new deals.

#### Influenced Deals

In the Dashboard, click Actions, select Add images, text, or video . Copy and paste to the following text:
Influence Deals
Identify partners already working with an account you're actively engaging!
Use these partners to help you influence a deal by getting an overview of the prospect's tech stack, requesting an intro to a specific contact, gathering some intel on the buying process, or asking them to recommend your product.

Drag the section to resize it in the dashboard.
How to Create
Report: Partner Deal Influence
- Visualization : Set the chart to Pie
- Filters : Set Include data if it matches to: ALL of the filters below Add these filters: Partner Population contains any of customers or open opportunities Companies Total open deal value is known
- Set Include data if it matches to: ALL of the filters below
- Add these filters: Partner Population contains any of customers or open opportunities Companies Total open deal value is known
- Partner Population contains any of customers or open opportunities
- Companies Total open deal value is known
- VALUES: TOTAL OPEN DEAL VALUE
- BREAK DOWN BY: PARTNER NAME
If your populations or fields are named differently, adjust the settings accordingly.

How to Create
Report: Accounts where partners can help influence existing opportunities
- Visualization : Table
- Filters : Set Include data if it matches to: ALL of the filters below Add these filters: Partner Population is equal to any of customers or open opportunities Population contains any of prospect Total open deal value is known Add these columns: COMPANY NAME COMPANY OWNER TOTAL OPEN DEAL VALUE PARTNER NAME PARTNER POPULATION
- Set Include data if it matches to: ALL of the filters below
- Add these filters: Partner Population is equal to any of customers or open opportunities Population contains any of prospect Total open deal value is known
- Partner Population is equal to any of customers or open opportunities
- Population contains any of prospect
- Total open deal value is known
- Add these columns: COMPANY NAME COMPANY OWNER TOTAL OPEN DEAL VALUE PARTNER NAME PARTNER POPULATION
- COMPANY NAME
- COMPANY OWNER
- TOTAL OPEN DEAL VALUE
- PARTNER NAME
- PARTNER POPULATION
If your populations or fields are named differently, adjust the settings accordingly.

#### Retain and Expand Customers

In the Dashboard, click Actions, select Add images, text, or video . Copy and paste to the following text: ​
Retain & Expand Customers
Identify partners also working with your existing customer base!
Use these insights to understand ways to expand your clients' usage of your product and integrations, request an intro to new stakeholders, and to gather intel and recommendations.

Drag the section to resize it in the dashboard.
How to Create
Visualization: Mutual customers
- Visualization : Vertical Bar
- Filters : Set Include data if it matches to: ALL of the filters below Add these filters: Partner Population contains any of customers Population contains any of customer X-axis: PARTNER NAME Y-axis: COUNT OF COMPANIES
- Set Include data if it matches to: ALL of the filters below
- Add these filters: Partner Population contains any of customers Population contains any of customer
- Partner Population contains any of customers
- Population contains any of customer
- X-axis: PARTNER NAME
- Y-axis: COUNT OF COMPANIES
If your populations or fields are named differently, adjust the settings accordingly.

How to Create
Report: Accounts that are also customers of your Partners
- Visualization : Pivot Table
- Filters : Set Include data if it matches to: ALL of the filters below Add these filters: Partner Population contains any of customers Population contains any of customers
- Set Include data if it matches to: ALL of the filters below
- Add these filters: Partner Population contains any of customers Population contains any of customers
- Partner Population contains any of customers
- Population contains any of customers
- Add these rows: COMPANY NAME PARTNER NAME PARTNER POPULATION PARTNER AE NAME
- COMPANY NAME
- PARTNER NAME
- PARTNER POPULATION
- PARTNER AE NAME
If your populations or fields are named differently, adjust the settings accordingly.

How to Create
Visualization : Expand Opportunities
- Visualization : Horizontal Bar
- Filters : Set Include data if it matches to: ALL of the filters below Add these filters: Population contains any of customers Total open deal value is greater than or equal to 1 X-axis: TOTAL OPEN DEAL VALUE Y-axis: PARTNER NAME
- Set Include data if it matches to: ALL of the filters below
- Add these filters: Population contains any of customers Total open deal value is greater than or equal to 1
- Population contains any of customers
- Total open deal value is greater than or equal to 1
- X-axis: TOTAL OPEN DEAL VALUE
- Y-axis: PARTNER NAME
If your populations or fields are named differently, adjust the settings accordingly.

How to Create
Visualization: Integration adoption potential
- Visualization : Vertical Bar
- Filters : Set Include data if it matches to: ALL of the filters below Add these filters: Integration is not equal to any of N or is empty Partner Population contains any of customer Population contains any of customer X-axis: PARTNER NAME Y-axis: COUNT OF CROSSBEAM OVERLAPS
- Set Include data if it matches to: ALL of the filters below
- Add these filters: Integration is not equal to any of N or is empty Partner Population contains any of customer Population contains any of customer
- Integration is not equal to any of N or is empty
- Partner Population contains any of customer
- Population contains any of customer
- X-axis: PARTNER NAME
- Y-axis: COUNT OF CROSSBEAM OVERLAPS
If your populations or fields are named differently, adjust the settings accordingly.
🎓 Want to go deeper? ​ Sign in to Crossbeam Academy to learn more about building and customizing HubSpot reports and dashboards with Crossbeam data.
- Salesforce Guide for Reports, Dashboards, & Automations Powered by Crossbeam
- Create the Crossbeam 360 Dashboard in Salesforce
- Crossbeam Performance Dashboard Guide
- How to Create a Crossbeam Report in HubSpot
- Crossbeam Product Release Notes 11/6/2025


## Before You Begin (HC 11407240)
URL: https://help.crossbeam.com/en/articles/11407240-installation-guide-crossbeam-for-salesforce-connector-plan

In this article:
- Before You Begin
- Step 1: Install the Managed Package
- Step 2: Connect Salesforce to Crossbeam
- Step 3: Configure Trusted URLs
- Step 4: Assign Permission Sets
- Step 5: Place the Crossbeam Copilot
- Step 6: Configure Universal Integration Settings

Crossbeam Requirements:
- On the Crossbeam Connector Plan
- Ensure you have a Crossbeam user seat with one of the following roles: Full Access Role: Admin Sales Role: Manager
- Full Access Role: Admin
- Sales Role: Manager
Salesforce Requirements:
- Salesforce Lightning Experience is required
- You must have a My Domain (custom domain) enabled to use Crossbeam Copilot Follow this Salesforce guide to set it up
- Follow this Salesforce guide to set it up
Permissions Sets
Assign the appropriate Crossbeam permission sets to your users in Salesforce:
- Crossbeam Setup User For Salesforce admins configuring the integration
- For Salesforce admins configuring the integration
- Crossbeam Account User For sellers who will actively use Copilot to view and interact with data
- For sellers who will actively use Copilot to view and interact with data
- Crossbeam Widget Viewer Grants view-only access to Copilot Users will see shared partner overlaps and insights All interactive features are disabled, including the ability to view partner-shared data or start conversations Use Widget Viewer for users who need visibility but shouldn’t take action inside Copilot
- Grants view-only access to Copilot Users will see shared partner overlaps and insights All interactive features are disabled, including the ability to view partner-shared data or start conversations
- Users will see shared partner overlaps and insights
- All interactive features are disabled, including the ability to view partner-shared data or start conversations
- Use Widget Viewer for users who need visibility but shouldn’t take action inside Copilot
✍️ Note
Copilot does not support "API Only" Integration User Profiles.
For more details on managed packages, including required user permissions and installation types, review Salesforce's documentation Install a Package .

### Step 1: Install the Managed Package
- Navigate to Crossbeam's Salesforce AppExchange listing
- Click Get It Now Choose Install in Production (or Sandbox, if you’re testing first). Log in with your Salesforce Admin credentials when prompted
- Choose Install in Production (or Sandbox, if you’re testing first).
- Log in with your Salesforce Admin credentials when prompted

- Approve Installation Details When asked, select Install for Admin Only: t his option allows for controlling access and permissions after the package has been installed Check the boxes to approve third-party access for these domains (used by Crossbeam to deliver insights within Salesforce) Click Install
- When asked, select Install for Admin Only: t his option allows for controlling access and permissions after the package has been installed
- Check the boxes to approve third-party access for these domains (used by Crossbeam to deliver insights within Salesforce)
- Click Install

#### Installation Timing
- The package may take several minutes to install
- You’ll receive a confirmation email from Salesforce once the installation is complete
Once the installation is complete, proceed to assign the appropriate Crossbeam permission sets to users as needed.
✍️ Note
Connector plan users do not have access to data in the Crossbeam Custom Object. However, the object is still installed as part of the managed package. No data is pushed to it for Connector plan users.

To upgrade your account, visit the Plan & Billing page .

### Step 2: Connect Salesforce to Crossbeam
- In Salesforce, open the App Launcher and search for Crossbeam Setup
- Click Get Started to initiate the setup process
- Complete the three authentication steps to connect Crossbeam and Salesforce inside the Crossbeam Setup page

### Step 3: Configure Trusted URLs
- In Salesforce Setup, go to Security > Trusted URLs
- Click New Trusted URL and enter the following: API Name: Crossbeam URL: https://app.crossbeam.com CSP Context: Lightning Experience Pages CSP Directives: frame-src
- API Name: Crossbeam
- URL: https://app.crossbeam.com
- CSP Context: Lightning Experience Pages
- CSP Directives: frame-src
- Click Save to add the trusted site

### Step 4: Assign Permission Sets
- In Salesforce Setup, navigate to Users > Permission Sets
- Locate and click on the relevant Crossbeam permission set: Crossbeam Setup User, for admins configuring the integration Crossbeam Account User, for sellers using Copilot Crossbeam Widget Viewer, for users who need read-only access
- Crossbeam Setup User, for admins configuring the integration
- Crossbeam Account User, for sellers using Copilot
- Crossbeam Widget Viewer, for users who need read-only access
- Click Manage Assignments
- Click Add Assignment
- Select the users who need access, then click Next
- Click Assign, then Done

### Step 5: Place the Crossbeam Copilot

#### Add Copilot to Standard Salesforce Objects
We recommend adding Copilot to the following standard objects:
- Account
- Opportunity
- Lead
- Contact
Follow these steps for each object:
- Go to Setup > Object Manager
- Search for and click into the object (Account, Opportunity, Lead, and Contac t )
- In the sidebar, click Lightning Record Pages
- Select the record page you'd like to modify or click New to create one
- Click Edit to launch the Lightning App Builder
- From the left panel, under Custom, Managed, find and drag the Crossbeam Copilot component onto the layout
- Most teams place it in the right-hand column or within a dedicated Partner Insights tab
- Click Save, then click Activation to assign the page: Assign as Org Default or configure for specific apps, record types, or profiles.
- Assign as Org Default or configure for specific apps, record types, or profiles.
- Repeat for each object (Account, Opportunity, Lead, and Contact) where you want Copilot to appear

### Step 6: Configure Universal Integration Settings
Set which partners and types of overlaps your users can see in Copilot by adjusting your Universal Integration Settings in Crossbeam.

To find the settings in Crossbeam:
- From the left-side navigation bar, select Data > Integrations
- In the Salesforce row, open Settings
- Locate the Control what data shows in Copilot section
- Choose which partners and types of overlaps to surface in Copilot by checking or unchecking the boxes

Learn more about managing Universal Integration Settings here .
✍️ Note
Users will only see data in Copilot if they have the required Crossbeam role and Salesforce permissions.
Learn how to run winning plays in Copilot with Crossbeam Academy.

- Crossbeam Copilot for Salesforce
- Upgrade & Reauthorize Crossbeam for Salesforce
- Crossbeam Copilot for Salesforce FAQs
- Installation Guide: Crossbeam for Salesforce (v2)


## What is Partner Field Mapping? (HC 11419695)
URL: https://help.crossbeam.com/en/articles/11419695-partner-field-mapping-to-your-crm

In this article:
- What is Partner Field Mapping?
- Setting up Partner Field Mapping
- Understanding the Data

Partner Field Mapping lets you sync unique, partner-sourced data into your CRM (Salesforce and HubSpot). These fields go beyond standard integration points and give you visibility into the context your partners have on shared accounts.

You can use this enriched data in:
- Enrich your CRM with high-value, partner-sourced insights
- Power reports, dashboards, and workflows with deeper account context
- Improve targeting and prioritization during outreach
- Increase win rates by delivering more personalized pitches
- Strengthen partnerships by activating the data your partners share
Example Use Cases
The examples vary based on the fields you choose to sync back to your CRM.
- Product Sold: Identify which specific partner product a prospect uses to tailor your pitch and prioritize relevant integrations
- Tech Stack: Surface tools your prospect is already using (e.g., CRM, ATS, analytics platforms) to position your solution more effectively and uncover integration opportunities
- ACV: Prioritize accounts based on potential deal size, allowing sales to focus on high-value opportunities.
Partner Field Mapping often contain data you won’t find anywhere else, driving more informed and strategic sales motions.
✍️ Note
This feature is available on the Supernode plan and Enterprise plan.

To upgrade your account, visit the Plan & Billing page .

### Setting up Partner Field Mapping
In Crossbeam, select the Data icon> Integrations>HubSpot Custom Object OR Salesforce Custom Object> Account Object tab> Map Partner Data to CRM

### Understanding the Data
Once your partner fields are mapped to your CRM fields, here’s how the data behaves and what to keep in mind:

Where You'll See Partner Data
Mapped Partner Fields appear as custom fields in your Salesforce Account object or HubSpot Company object, specifically in the text fields you’ve created and mapped.
✍️ Note
Users can only sync partner account fields to their Salesfroce account object.
Users can only sync partner company fields to their HubSpot company object.

How to map your data in your CRM:
- Create a TEXT field on the Account object (Salesforce) or Company object (HubSpot) in your CRM
- In Crossbeam, locate the Integration settings>Account object (Salesforce) or Company object (HubSpot) Toggle On Map Partner data to CRM t o add partner account fields to the text fields you created in your CRM
- Toggle On Map Partner data to CRM t o add partner account fields to the text fields you created in your CRM
- Click Save Account Object
Crossbeam will then push the mapped partner data to those CRM text fields on the next sync.
For Salesforce users, these fields will also appear in the Crossbeam Copilot widget if they’ve been synced.
✍️ Note
The sync that pushes mapped partner data to your CRM is separate from the update frequency set for your data sources. However, you can expect mapped partner data to appear within 24 hours of saving your configuration.
Field Compatibility and Limitations
Partner account fields are pushed to text fields in your CRM. To ensure proper syncing:
- Create a text field on the Company object in HubSpot or the Account object in Salesforce
- Map each partner account field to one of these CRM text fields NOTE: Field format matching is not supported. All data is converted to text before syncing.
- NOTE: Field format matching is not supported. All data is converted to text before syncing.
- Date fields cannot be mapped
- Picklist fields require manual mapping to each value to ensure accurate syncing
- Integrations Overview
- Attribution for Salesforce Users
- Enhanced Ecosystem Reporting: “is a customer of” & “is an opportunity for” Fields in Salesforce
- How to Sync Product Line Support (Product2) into Crossbeam
- How to Set Up the Partner Account CRM Integration


## How to Reauthorize the Salesforce Custom Object Integration (HC 12013434)
URL: https://help.crossbeam.com/en/articles/12013434-step-by-step-guide-reauthorizing-your-salesforce-custom-object-integration

Follow these steps to reauthorize your Salesforce connection for the Custom Object integration.
👀 Prefer video? Click here for a detailed walkthrough of these steps.

#### Before You Begin
Make sure you are logged in as the integration user in both Salesforce and Crossbeam.
- The integration user requires the following permissions: Crossbeam Setup User assigned in Salesforce, Visualforce Page Access enabled, and read access to Account and Lead objects
- For more detailed information on permissions, review this article here
We recommend using a dedicated Integration Seat in Crossbeam for this connection. Integration Seat is available on Supernode and Enterprise plans. Learn more in Managing User Seats and Roles in Crossbeam .

### In Salesforce
- In Salesforce, go to the App Launcher and search for Crossbeam
- Select Crossbeam Setup from the options
- Navigate to System Connections and click Edit
- Revalidate each of the steps: Outbound Connection → Click Next Select your Crossbeam organization → click Finish
- Outbound Connection → Click Next
- Select your Crossbeam organization → click Finish

#### In Crossbeam
- Go to Data → Integrations
- Locate the Salesforce Custom Object integration and click Settings

- Open Advanced Settings
✍️ Note
In the next steps, you’ll need to locate the three-dot menu (⋯). This menu can be easy to miss, it has been clearly marked with red arrows in the accompanying screenshots for your convenience.
- In the modal, click the three dots next to the connection and select Update
- Reauthorize the connection when prompted, click Save

Next, you will repeat these steps to complete the Salesforce authentication process within Crossbeam.
- Click the three dots next to the connection and select Update

- Next, reauthorize the connection in Salesforce when prompted
- In the modal, click Next → Finish

- Back in the Settings, click on Save General Settings

Once complete, your reauthorization should be active. Related errors should clear automatically after your next sync, which may take up to 12 hours.
🧐 Experiencing Salesforce Authorization Errors? If you see errors when connecting Salesforce to Crossbeam, it may be due to Salesforce’s September 2025 security update blocking “uninstalled” connected apps. For full troubleshooting steps, see: Troubleshooting Salesforce Authorization with Crossbeam .

- Crossbeam Copilot for Salesforce
- Installation Guide: Crossbeam for Salesforce (v2)
- Video Tutorial: Reauthorizing the Salesforce Custom Object Integration
- Step-by-Step Guide: Reauthorizing Your HubSpot Custom Object Integration


## Overview (HC 12158775)
URL: https://help.crossbeam.com/en/articles/12158775-step-by-step-guide-reauthorizing-your-hubspot-custom-object-integration

This article guides users through reauthorizing the HubSpot Custom Object integration in both HubSpot and Crossbeam.

#### Before You Begin
- Ensure you’re logged into Crossbeam with a Full Access seat (Standard or Admin) that includes Integration permissions
- In HubSpot, you must have a Sales Hub, Enterprise license to create and manage custom objects, and (if using contact lists) a Marketing Hub, Professional license
- For more detailed information on the HubSpot Custom Object, click here .
We recommend using a dedicated Integration Seat in Crossbeam for this connection. Integration Seat is available on Supernode and Enterprise plans. Learn more in Managing User Seats and Roles in Crossbeam .

#### Confirm HubSpot Private App Permissions
Before reauthorizing, double-check that your HubSpot Private App still has the correct scopes.
- In HubSpot, go to Settings → Private Apps and select the Crossbeam App →Auth tab
- Under Scopes, confirm the app still has the following scopes enabled: crm.lists.read / crm.lists.write crm.objects.companies.read / crm.objects.companies.write crm.objects.contacts.read / crm.objects.contacts.write crm.objects.custom.read / crm.objects.custom.write crm.schemas.companies.read / crm.schemas.companies.write crm.schemas.custom.read / crm.schemas.custom.write crm.import
- crm.lists.read / crm.lists.write
- crm.objects.companies.read / crm.objects.companies.write
- crm.objects.contacts.read / crm.objects.contacts.write
- crm.objects.custom.read / crm.objects.custom.write
- crm.schemas.companies.read / crm.schemas.companies.write
- crm.schemas.custom.read / crm.schemas.custom.write
- crm.import
- If any are missing, click Edit App, and update the Scopes before continuing

### In Crossbeam
- Go to Data → Integrations
- Locate the HubSpot Custom Object integration and click Settings

- Open Advanced Settings

✍️ Note
In the next steps, you’ll need to locate the three-dot menu (⋯). This menu can be easy to miss, it has been clearly marked with red arrows in the accompanying screenshots for your convenience.
- In the modal, click the three dots next to the connection and select Update

- In the Edit Authentication screen, click Save

Next, you will repeat similar steps to complete the HubSpot Authentication process within Crossbeam.
- Click the three dots next to the connection, select Update

- In the next window, click Save

- Back in the HubSpot Authentication window, click Next

- Configure lists by adding or removing them, if needed
- Click Next

- In the next screen, click Finish

- Back in the integration settings, click on Save General Settings

Once complete, your reauthorization should be active. Related errors should clear automatically after your next sync, which may take up to 12 hours.

- Connect HubSpot Data
- HubSpot Custom Object Integration
- Installation Guide: Crossbeam for Salesforce (v2)
- Video Tutorial: Reauthorizing the Salesforce Custom Object Integration
- Step-by-Step Guide: Reauthorizing Your Salesforce Custom Object Integration


## Salesforce Authorization Issues with Crossbeam (HC 12510571)
URL: https://help.crossbeam.com/en/articles/12510571-troubleshooting-salesforce-authorization-with-crossbeam

Salesforce recently introduced stricter security measures for Connected Apps . As part of this update, Salesforce may block “uninstalled” connected apps, apps that were authorized by a user but never formally installed in the Salesforce org.

This error could appear when users connect Salesforce Custom Object Integration or Salesforce as a Data Source in Crossbeam. The following troubleshooting steps are the same; the only differences are the name of the connected app ( “Crossbeam” instead of “Crossbeam Salesforce Overlaps Push” ) and the installation link.

This change can cause authorization issues when setting up the Salesforce Custom Object Integration or Salesforce as a Data Source in Crossbeam. Users may see errors when trying to connect if the connected app is blocked.


#### How to Resolve Authorization Issues
If you’re unable to authorize or reauthorize your Salesforce connection in Crossbeam, follow one of the options below.


#### Option A: Install via Connected Apps OAuth Usage
- In Salesforce, go to Setup → Connected Apps OAuth Usage
- Find the connected app named Crossbeam Salesforce Overlaps Push (or Crossbeam for Salesforce Data Source)
- Click Install

- Optional: Adjust security and access policies so that only users with the Crossbeam Setup User permission set have access
- Return to Crossbeam and retry the Salesforce connection.

#### Option B: Install via Direct URL
✍️ Note
The link below is intended for production environments only. If you are installing in a Sandbox or UAT environment, contact your Salesforce admin for the correct install URL.
If the app isn’t listed in Connected Apps OAuth Usage, you can install it directly using the following URL (replace {sfdc-domain} with your Salesforce domain):

Crossbeam Salesforce Overlaps Push
https://{your-sfdc-domain}/identity/app/AppInstallApprovalPage.apexp?app_id=0Ci1U000000L2SJ&app_org_id=00D1U000001BPt6
Crossbeam (for Salesforce Data Source)
https://{your-sfdc-domain}/identity/app/AppInstallApprovalPage.apexp?app_id=0Ci1U000000bmwH&app_org_id=00D1U000001BPt6
After installation, return to Crossbeam and retry the Salesforce connection.

#### Option C: Temporarily Approve Uninstalled Connected Apps
If the app is still not visible after trying Option A or B, you can temporarily allow the connection by:
- Adding the Approve Uninstalled Connected Apps scope to your Salesforce Integration/Service user
- Retry the connection in Crossbeam
- Once the connection is successful, you’ll now see Crossbeam listed in Connected Apps OAuth Usage ( see Option A )
- Next: Install the app Remove the Approve Uninstalled Connected Apps scope from the Integration user to maintain strict security
- Install the app
- Remove the Approve Uninstalled Connected Apps scope from the Integration user to maintain strict security
- Upgrade & Reauthorize Crossbeam for Salesforce
- Installation Guide: Crossbeam for Salesforce (v2)
- Access Crossbeam Deal Navigator inside Salesforce
- Setting Up a Crossbeam Ecosystem Overlaps Related List in Salesforce


## Overview (HC 12732223)
URL: https://help.crossbeam.com/en/articles/12732223-getting-started-with-signals-how-to-access-real-time-partner-data-via-api-and-webhooks

In this article:
- Overview
- What are signals? Requirements Receiving Contact Information on Opportunity Signals Plan Access
- Requirements Receiving Contact Information on Opportunity Signals Plan Access
- Receiving Contact Information on Opportunity Signals
- Plan Access
- How It Works Webhooks How to Set up a Webhook in Crossbeam APIs How to Set up APIs in Crossbeam
- Webhooks How to Set up a Webhook in Crossbeam
- How to Set up a Webhook in Crossbeam
- APIs How to Set up APIs in Crossbeam
- How to Set up APIs in Crossbeam
- Example Use Cases
- FAQs
Crossbeam’s newest API endpoint gives you programmatic access to ecosystem signals, partner-driven events that surface key moments across your ecosystem, such as when a strategic partner opens or closes an opportunity. These signals are designed to help your teams and tools act on partner activity as it happens. You can:
- Access these signals via the API for on-demand data retrieval
- Receive these signals via a webhook for real-time delivery into your existing tools and workflows
Together, these options make it easier to connect Crossbeam data to the systems your team already uses for automation, analytics, and reporting.

### What are signals?
A signal is a data point or event that represents a meaningful partner activity, such as an opportunity opening or closing, that could influence your pipeline, customer success, or co-selling strategy.

Signals help your teams:
- Detect opportunities or risks early (a partner closing a deal in an overlapping account)
- Automate next steps (notify account owners, trigger workflows)
- Power AI-driven insights and recommendations
These are delivered in real time through our webhook, or retrieved when needed via our API endpoint.
‼️ Important
API calls and Webhooks are included in Record Exports limits.

Contact the support team at support@crossbeam.com for further assistance. <!-- VALIDATE-OK[person-address]: verbatim public Crossbeam Help Center text -->

#### Requirements
To receive signals, your partner must:
- Have a CRM connected to Crossbeam
- Be syncing and sharing the following fields with you: Deal open date Deal close date Deal is closed Deal is won
- Deal open date
- Deal close date
- Deal is closed
- Deal is won
✍️ Note
Your company only needs to sync these fields with Crossbeam, you do not need to share them back with your partner.


##### Receiving Contact Information on Opportunity Signals
To receive contact information on opportunity signals, your partner must also be syncing and sharing CRM contact data.

If contact data is included, signals may contain the following fields:

Required Contact Fields
- Contact Name
- Contact Title
Signal Contact Parameters
- contact_name, Full name of the contact
- contact_role, The contact’s role at the organization
- contact_type, Classification of the contact (decision maker, influencer, buyer)
Contact information will only appear in signal if your partner is actively sharing this data.


##### Plan Access
- Free and Connector plans: No access
- Supernode plan: Access to the API (Signals and the API endpoint)
- Enterprise plan: Access to the API and Webhook
To upgrade your account, visit the Plan & Billing page .
✍️ Note : Only Admin users can create or edit webhooks and API integrations.

### How It Works
Choosing Between Webhooks and the API Endpoint
- Webhook: Delivers immediate, near real-time updates to your system as events occur. This is ideal when you need to trigger workflows, send notifications, or automate actions in response to partner events. Because updates are pushed automatically, you don’t need to pull data repeatedly, ensuring your system responds instantly.
- API Endpoint: Provides on-demand access to data, which you retrieve by pulling updates from the API. This is useful for supplemental insights, reporting, or tasks that don’t require immediate action . Unlike webhooks, you control when and how often you pull the data.
Crossbeam’s APIs make signals available in two main ways:


##### Webhook (Push Model)
The webhook automatically sends signal updates to your system the moment an event occurs.

Example: ​
When a partner opens a new opportunity in a shared account, Crossbeam “pings” your connected app, such as Slack, HubSpot, or a custom internal tool, to trigger a workflow or alert.

Best for:
- Real-time notifications or automations
- Systems that should respond instantly to partner events

###### How to Set up a Webhook in Crossbeam
From the left-side Navigation Menu in Crossbeam:
- Click on Data → Integrations → +Create New → Webhook

- Next, define your webhook settings: Event types → Choose which event(s) you’d like to receive signals for: Deal opened (when a partner opens a new opportunity) Deal closed-won (when a partner closes a deal) Add Webhook name Add Destination URL
- Event types → Choose which event(s) you’d like to receive signals for: Deal opened (when a partner opens a new opportunity) Deal closed-won (when a partner closes a deal)
- Deal opened (when a partner opens a new opportunity)
- Deal closed-won (when a partner closes a deal)
- Add Webhook name
- Add Destination URL
- After clicking Finish, a secret key will appear Copy and store it safely, you won’t be able to view this same key again Some external tools may require this key to authenticate incoming data See Developer Documentation here for me details
- Copy and store it safely, you won’t be able to view this same key again
- Some external tools may require this key to authenticate incoming data See Developer Documentation here for me details
- See Developer Documentation here for me details

Test your webhook
- Crossbeam will send a test call to the destination URL you provided
- If the test fails, you can click the edit configuration button and try again until it succeeds
- Once you pass the test, you will be able to move on to apply filters
Define and select filters for your webhook
✍️ Note
Filters cannot be added until the webhook has been successfully tested.
- Filters let you narrow which partners or Populations you want to receive signals for
- The webhook will only be triggered for the overlaps between your selected Populations and partner/s’ selected Populations

Click Save Settings to finalize setup. Your webhook is now active and will appear in your list of installed integrations.

To manage your webhook later, navigate to Data > Integrations, then click Settings button for the Webhook.
👉 For more technical details on configuring your webhook, visit our Developer Documentation

##### 2. API Endpoint (Pull Model)
The API endpoint allows your systems or AI agents to request the latest signal data from Crossbeam when needed.

Example: ​
Your CRM or internal analytics platform can call the Crossbeam API to fetch all new Opportunity Closed Won signals from the past 24 hours.

Best for:
- On-demand insights or scheduled analyses
- Use cases that don’t require immediate real-time actions

###### How to Set up APIs in Crossbeam
From the left-side Navigation Menu in Crossbeam:
- Click on Data → Integrations → +Create New → API Integration

- Next, define your API settings: Integration name Integration description Callback URL and Allowed Origins
- Integration name
- Integration description
- Callback URL and Allowed Origins
Click Create Integration, then follow the step-by-step instructions in our Developer Documentation to complete your endpoint setup.
👉 See setup details in the Developer Documentation

### Example Use Cases
| Use Case | How It Works | Model |
| Instant deal notifications | When a partner opens a new opportunity on an overlap, send a Slack alert to the account owner | Webhook |
| Trigger outreach cadences | Automatically start a HubSpot or Outreach sequence when a partner adds a new opportunity | Webhook |
| Timed follow-ups | Wait 60 days after a partner’s Closed Won deal, then trigger a “better together” campaign | Webhook |
| Deal prioritization scoring | Fetch Closed Won signals daily to update opportunity scores in your CRM | API Endpoint |

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


## Overview (HC 12872312)
URL: https://help.crossbeam.com/en/articles/12872312-setting-up-a-crossbeam-ecosystem-overlaps-related-list-in-salesforce

In this article:
- Overview
- How to Add Crossbeam Ecosystem Overlaps

This article assumes you have already created the custom object and related configurations. Click here for the full guide to Crossbeam for Salesforce.

Once the custom object is installed, this guide walks you step by step through configuring the page layout, so users with the proper permissions can view the related list.

You can display Crossbeam data directly on Account or Opportunity records by adding the Crossbeam Ecosystem Overlaps related list. This allows users to see partner overlap details from Crossbeam within Salesforce. An SFDC admin can complete this setup, and anyone with Crossbeam Report User permissions will be able to access the related list once added.


### How to Add Crossbeam Ecosystem Overlaps
- In Salesforce, click the gear icon in the top-right corner and select Setup
- In the Setup menu, select the Object Manager tab
- Choose either Account or Opportunity, depending on where you want Crossbeam Ecosystem Overlaps to appear
- In the left-hand menu, click Page Layouts
- Select the layout you want to edit (e.g., Account Layout )
- At the top of the editor, click Related Lists
- Find Crossbeam Ecosystem Overlaps, then drag and drop it into the Related Lists section of the layout
- To customize the fields shown, click the wrench/tool icon on the Crossbeam Ecosystem Overlaps related list
- Select the fields you’d like to display
- Recommended Fields to Include: Partner Name Partner Standard Populations Partner Populations Partner Record Owner Name Partner Record Owner Email
- Partner Name
- Partner Standard Populations
- Partner Populations
- Partner Record Owner Name
- Partner Record Owner Email

✍️ Note
Learn more about customized fields in the Related Lists here .

Click Save when done.

📄 Related Articles
- Salesforce Guide to Reports, Dashboards, & Automations Powered by Crossbeam

- Crossbeam Copilot for Salesforce
- Salesforce Guide for Reports, Dashboards, & Automations Powered by Crossbeam
- Installation Guide: Crossbeam for Salesforce (v2)
- How to Create a Combined Overlap and Partner Account Report Type in Salesforce


## Overview (HC 13613493)
URL: https://help.crossbeam.com/en/articles/13613493-how-to-sync-product-line-support-product2-into-crossbeam

In this article:
- Overview
- Requirements
- Plan Availability
- How to Sync in Crossbeam
- How it Works
- Where You Can Use It
Product Line Support (Product2) is only available for Salesforce and is not currently available for other CRMs.
Salesforce Product Line Support (Product2) allows companies to sync product data into Crossbeam. This allows teams to see not just which accounts they share with partners but also which products are actually in play on opportunities.

With product data available across Lists, Deal Navigator, and the Performance Dashboard, teams can filter and segment ecosystem data by product, making it easier to prioritize the right partners, identify whitespace, and run more targeted GTM motions.

Key benefits include:
- Product-aware prioritization Focus partner engagement and internal effort around the products you’re actively selling, not just shared accounts
- Focus partner engagement and internal effort around the products you’re actively selling, not just shared accounts
- More relevant partner engagement Bring the right partners into the right deals based on product context, reducing noise, misalignment, and potential conflict
- Bring the right partners into the right deals based on product context, reducing noise, misalignment, and potential conflict
- Clearer expansion paths Identify whitespace and natural cross-sell opportunities within existing accounts
- Identify whitespace and natural cross-sell opportunities within existing accounts

### Requirements
Before setting up Salesforce Product Line Support (Product2) in Crossbeam, ensure the following requirements are met:

Salesforce as a Data Source
- You must have Salesforce (SFDC) connected in Crossbeam
- Product Line Support (Product2) is not currently available for other CRMs
Opportunity Data Sync
- Your Salesforce integration must be syncing Opportunity data This allows Crossbeam to link products to specific deals so you can see which products are actually involved in which Opportunities, not just a list of products
- This allows Crossbeam to link products to specific deals so you can see which products are actually involved in which Opportunities, not just a list of products
Required Salesforce Objects
Your Salesforce instance must have the following objects:
- Product2 (Product) Contains your product catalog (product names, SKUs, and identifiers)
- Contains your product catalog (product names, SKUs, and identifiers)
- Opportunity Line Item Connects products (Product2) to opportunity records
- Connects products (Product2) to opportunity records
✍️ Note
Both objects must exist in Salesforce to sync product data into Crossbeam.

### Plan Availability
All plans can sync product line data, share it with partners, and use it when building Populations. Filtering by product in Lists and the Dashboard is available on Supernode and Enterprise only.
| | Free | Connector | Supernode | Enterprise |
| Sync | ✓ | ✓ | ✓ | ✓ |
| Share | ✓ | ✓ | ✓ | ✓ |
| Use in Standard Populations | ✓ | ✓ | ✓ | ✓ |
| Use in Custom Populations |, | ✓ | ✓ | ✓ |
| Filter Lists |, |, | ✓ | ✓ |
| Filter Dashboard |, |, | ✓ | ✓ |

#### Salesforce Data Access
Your Crossbeam Salesforce connection must have read permissions for:
- Product2
- Opportunity Line Item
- Opportunity objects
If you’re unsure whether these permissions are enabled, work with your Salesforce administrator to confirm that Crossbeam has read access to these objects. Without the correct permissions, product data cannot be synced.

If only a Product ID is synced without a readable product name, product values will appear as alphanumeric IDs in Crossbeam.

### How to Sync in Crossbeam
Follow these steps to set up Product Line Support in Crossbeam.

Step 1: Sync the Required Salesforce Objects in Crossbeam
- Navigate to Data → Data Sources on the side navigation
- Locate the Salesforce row and open the Settings icon
- In the modal, click Field sync → Edit button
- Toggle on Product 2, expand to check any additional fields to the required presets
- Next, toggle on Oppourtunity LIne Item, and expand to check any additional fields to the required presets
- Click the Review Fields button → Sync Now button

✍️ Note
Both Product2 and Opportunity Line Item must be synced so Crossbeam can link products to opportunities in Crossbeam.
Step 2: Configure Field Mapping
Next, define which field in your CRM represents the product line.

Return to the Crossbeam Data Source settings:
- Navigate to Data → Data Sources on the side navigation
- Locate the Salesforce row and open the Settings icon
- In the modal, click Field Mapping
- Locate the Product Line Type Field
- From the drop-down options, define what field in your CRM represents the product line (commonly Product Name)
- Click Save

💡 Sharing Product Data with Partners To allow partners to see Product2 data in overlaps, you must adjust your data sharing settings to share Product2 data. Visit the Sharing Dashboard to review and update which populations and fields (including product data) are shared with each partner.

Click here to learn more about the Sharing Dashboard.

### How it Works
In Salesforce, products are not linked directly to accounts, they are associated through opportunities. Crossbeam uses a bridge model to sync this data:
- Product2 : Holds the product catalog (names, SKUs, identifiers)
- Opportunity Line Item : Links products to specific Opportunity records
By syncing both objects, Crossbeam can identify:
- Which products are tied to open opportunities in your pipeline
- Which products customers are using based on their most recent Closed-Won opportunity
This approach ensures product-level insights are available where Opportunity-level data is used in Crossbeam.

### Where You Can Use It
Product2 data will now be available across key Crossbeam workflows:
- Deal Navigator : now includes a Product Type filtering button
- Account Mapping List : Use the Product Name filter to drill into product-specific overlaps
- Performance Dashboard : Can filter Opportunity data by Product Type
- Anywhere we surface Opportunity-level data: Record Detail Page, the Account Detail Drawer, and Copilot: View the specific products associated with opportunities on a partner account
- Record Detail Page, the Account Detail Drawer, and Copilot: View the specific products associated with opportunities on a partner account
- Building Populations: Create custom populations based on product ownership
✍️ Note
Crossbeam uses the most recent Closed-Won Opportunity to determine which product an account is using; to see this product data for partners, the partner must be sharing Opportunity data with you.
💡 Pro Tip Create a Custom Population using the Product Type field and compare it against your partners’ opportunities to quickly spot expansion and co-sell opportunities.
- Installation Guide: Crossbeam for Salesforce (v2)
- Crossbeam Deal Navigator
- Crossbeam Product Release Notes 02/11/2026
- How to Build a Product-Based Population Using Product2


## Overview (HC 14463181)
URL: https://help.crossbeam.com/en/articles/14463181-how-to-set-up-the-partner-account-crm-integration

In this article:
- Overview
- Plan Availability
- Requirements
- Step 1: Navigate to Partner Mapping Settings
- Step 2: Configure a Mapping Rule
- Step 3: Resolve Unmapped Partners Manually
- Step 4: Enable Partner Tags sync
- What Changes in Salesforce

The Partner Account CRM Integration creates a 1:1 link between each of your Crossbeam partners and their corresponding Partner Account record in Salesforce. Once mapped, every Crossbeam Ecosystem Overlap record gains a Partner Account lookup field in Salesforce, a real relationship, not just a partner name as text, so you can build reports that combine overlap data and Partner Account attributes like partner owner, tier, and type in a single view.
❗️ Important
Mapped Partner Account records count toward your Record Exports, the same as any other data pushed to Salesforce via Crossbeam. Your initial auto-matched mappings are set up by Crossbeam and do not count against your limit.

Crossbeam Record Exports can be monitored here . Once you hit the Export Limit, Crossbeam insights will stop flowing into external tools.

Learn more about maximizing your record exports here .

### Plan Availability
| Feature | Free | Connector | Supernode / Enterprise |
| Map Partner Accounts to Crossbeam partners in Crossbeam | ✓ | ✓ | ✓ |
| Partner Account lookup field on Ecosystem Overlap records |, |, | ✓ |
| Partner metadata sync to Salesforce (Partner Tags) |, |, | ✓ |
✍️ Note: This integration is currently available for Salesforce only.

### Requirements
- Salesforce connected as a data source in Crossbeam
- Salesforce Custom Object Integration (v2) installed and active (Supernode / Enterprise)
- Crossbeam Admin role to configure partner mapping settings

### Step 1: Navigate to Partner Mapping Settings
- Click Data in the left-hand navigation
- Select Data Sources from the dropdown
- Locate the Salesforce row and click the gear icon to open Salesforce settings
- Click the Partner Mapping tab

You will see a list of your Crossbeam partners on the left. Crossbeam automatically attempts to match each partner to a corresponding Salesforce account using domain data.
- Partners that matched display their mapped Salesforce account
- Partners with no match show an Unmapped status


### Step 2: Configure a mapping rule
A mapping rule tells Crossbeam which Salesforce accounts to consider as Partner Accounts, improving auto-match accuracy for existing partners and ensuring future partners are matched correctly.
- At the top of the Partner Mapping tab, locate the mapping rule field.
- Set a filter that identifies your Partner Account records in Salesforce. Common examples: Account Record Type equals Partner Account Type equals Partner Partner Type equals Strategic Partner
- Account Record Type equals Partner
- Account Type equals Partner
- Partner Type equals Strategic Partner
- Click Apply .

Once the rule is applied, Crossbeam re-runs matching across your full partner list. Any partner that couldn't be matched surfaces with an Unmapped status.
✍️ Note: After applying a rule, mapping may take a few minutes to update.

### Step 3: Resolve unmapped partners manually
After the mapping rule runs, some partners may still show as Unmapped because no Salesforce account matched the rule or domain.

Resolve these individually by:
- Locate an unmapped partner in the list
- Click the dropdown in the Salesforce Account column next to that partner
- Type the name of the corresponding Salesforce account in the search field
- Select the correct account from the results. The ID shown is the Salesforce record ID, use it to confirm you're selecting the right account if multiple records share a name
Repeat for each unmapped partner. This is a one-time setup that does not require ongoing maintenance.

Return to the Salesforce setting at any time to update as needed.


### Step 4: Enable Partner Tags sync
(Supernode and Enterprise plans only)
Once partner mapping is complete, you can push Crossbeam Partner Tags directly onto the mapped Partner Account records in Salesforce.


#### Add tags to your partners in Crossbeam
Before enabling the sync, make sure your partners have tags assigned in Crossbeam.
- Navigate to the Partners page in Crossbeam
- Open a partner and add or confirm the tags you want to push to Salesforce
Repeat for each partner whose tags you would like to sync.

For more detailed steps on creating and adding Partner Tags, click here .

#### Create the Crossbeam Tags field in Salesforce
Before enabling the Partner Tags sync in Crossbeam, you must create a custom text field on the Account object in Salesforce to receive the data.

Required Permissions
To create this field in Salesforce, the Salesforce user must have:
- Edit/Write access on the Account object
Without these permissions, the field cannot be created or populated.

In Salesforce:
- Open the Setup gear icon
- Use the quick find search box and type Object Manager Select Account from the list of objects
- Select Account from the list of objects
- Click Fields & Relationships from the side panel Click the New button
- Click the New button
- Under Data Type, select Text Click the Next button
- Click the Next button
- Enter the following details: Field Label: (Crossbeam) Tags The Field Name autopopulates from the label Check or uncheck the box next to Add to Custom Report Types (you can manually add the field later)
- Field Label: (Crossbeam) Tags
- The Field Name autopopulates from the label
- Check or uncheck the box next to Add to Custom Report Types (you can manually add the field later)
- Click the Next button
- In the next screen, assign permissions to the Crossbeam Setup User and the assigned permission sets for your team
- In the final step, decide whether to add the field to page layouts (optional) by checking or unchecking the boxes
- Click Save
❗️ Important
Crossbeam cannot complete this data push unless the (Crossbeam) Tags field is created in Salesforce first. Complete the steps above before enabling the sync below.

#### Enable the sync in Crossbeam
- Navigate to Data > Integrations > Salesforce Custom Object
- Click the gear icon to open the Salesforce Custom Object settings
- Under the Account Object tab, locate Push Crossbeam partner tags to Salesforce
- Toggle it on
- From the dropdown, select the (Crossbeam) Tags field you just created in Salesforce

Click Save Account Object when done.

Crossbeam will populate the selected Salesforce field during the next Salesforce sync.

Once the sync runs, open a Partner Account record in Salesforce and navigate to the Details tab to confirm the (Crossbeam) Tags field is populated with the partner's tags from Crossbeam.

### What changes in Salesforce
After mapping is complete, two things are available in Salesforce:
- Partner Account lookup field, Every Crossbeam Ecosystem Overlap record gains a lookup field pointing to the mapped Partner Account. This is a true Salesforce relationship, not a text field, which means Salesforce understands the connection and can use it in reports and filters.
- Richer Salesforce reports, You can now build reports that filter and group Ecosystem Overlap records by Partner Account attributes: partner owner, partner tier, partner type, and Crossbeam Partner Tags.
💡Ready to build the report? See How to Create a Combined Overlap and Partner Account Report in Salesforce for step-by-step instructions.
Example use cases enabled by the integration:
- Filter partner-influenced pipeline by partner owner so each Partner Manager works from a view scoped to their own portfolio
- Break down overlaps by partner tier to prioritize co-sell efforts
- Report on partner-sourced pipeline by partner type (ISV, reseller, strategic) for leadership dashboards
- For channel and CAM teams: overlap data now sits in the same Salesforce record as deal registrations and MDF tracking, both anchored to the Partner Account
Related Articles
- Installation Guide: Crossbeam for Salesforce (v2)
- Connecting Salesforce as a Data Source
- Partner Field Mapping to Your CRM
- Salesforce Guide for Reports, Dashboards, & Automations Powered by Crossbeam
- How to Use the Slack App for Crossbeam
- Installation Guide: Crossbeam for Salesforce (v2)
- Setting Up a Crossbeam Ecosystem Overlaps Related List in Salesforce
- How to Create a Combined Overlap and Partner Account Report Type in Salesforce


## Overview (HC 14625782)
URL: https://help.crossbeam.com/en/articles/14625782-how-to-create-a-combined-overlap-and-partner-account-report-type-in-salesforce

In this article:
- Overview
- Requirements
- Step 1: Create the Custom Report Type
- Step 2: Build a Report Using the New Report Type
This article explains how to create a custom Salesforce Report Type that combines Crossbeam Ecosystem Overlaps with your Account and Partner Account objects. Once configured, this report type lets you and your team view overlap data alongside account fields and Partner Account ownership in a single report.

### Requirements
- Crossbeam for Salesforce (v2) managed package installed
- At least one mapped Partner Account within Crossbeam
- Salesforce user with the Manage Report Types permission
- Users running reports must have the Crossbeam Report User permission set assigned

### Step 1: Create the Custom Report Type

#### Set Up the Report Type
- Navigate to Setup in Salesforce
- In the Quick Find box, type Report Types and select Report Types from the results
- Click New Custom Report Type

- In the Primary Object field, select Crossbeam Ecosystem Overlaps
- Enter a Report Type Label . Recommended: Crossbeam Ecosystem Overlaps with Account and Partner Account
- Enter a Description . For example: Report on Crossbeam overlaps with your Account fields and Partner Account fields in a single view
- Set Store in Category to Other Reports, or whichever category your team uses for Crossbeam reports
- Set Deployment Status to Deployed
- Click Next

Select the Fields to Include
- On the Edit Layout page, select the fields to make available when building reports with this type.
- Recommended fields by object: Crossbeam Ecosystem Overlaps: Partner Name, Standard Populations, Partner Standard Populations, Account, Opportunity Accounts: Account Owner, Account Name, Industry, Annual Revenue Partner Account: Account Owner (Partner Manager/CAM), Account Name, Type, and any custom tier or priority fields your team uses
- Crossbeam Ecosystem Overlaps: Partner Name, Standard Populations, Partner Standard Populations, Account, Opportunity
- Accounts: Account Owner, Account Name, Industry, Annual Revenue
- Partner Account: Account Owner (Partner Manager/CAM), Account Name, Type, and any custom tier or priority fields your team uses
- Click Save .

Your custom Report Type is now available.

### Step 2: Build a Report Using the New Report Type
- Navigate to Reports in Salesforce and click New Report
- Search for your new Report Type label and select it
- Click Start Report

- In the Filters tab, set the date filter to All Time and the overlap filter to All Crossbeam Ecosystem Overlaps
- In the Outline tab, add the columns most relevant to your use case
Recommended starting columns:
- Account Name (your account)
- Partner Name (from the overlap record)
- Partner Account: Account Owner (the Partner Manager or CAM who owns the relationship)
- Partner Account: Type (for example, Reseller, ISV, Strategic Partner)
- Standard Populations
- Partner Standard Populations
- Account Owner (your AE or account owner)
- Apply filters as needed. For example, filter by Partner Account: Type to scope to a specific partner segment, or group rows by Partner Account: Account Owner so each Partner Manager sees only their own accounts
- For example, filter by Partner Account: Type to scope to a specific partner segment, or group rows by Partner Account: Account Owner so each Partner Manager sees only their own accounts
- Click Save & Run
- Salesforce Guide for Reports, Dashboards, & Automations Powered by Crossbeam
- Installation Guide: Crossbeam for Salesforce (v2)
- Setting Up a Crossbeam Ecosystem Overlaps Related List in Salesforce
- How to Set Up the Partner Account CRM Integration


## Overview (HC 15231550)
URL: https://help.crossbeam.com/en/articles/15231550-databricks-integration

In this article:
- Overview
- Plan Availability
- Prerequisites Creating the Service Principal
- Creating the Service Principal
- Step 1: Create the Destination Catalog and Schema
- Step 2: Grant the Service Principal Write Access
- Step 3: Enable Push in Crossbeam
- Destination Table Schema
- Supported Features
- Limitations
- Manage Databricks Integration

The Databricks Integration writes the partner overlaps Crossbeam generates back to your Databricks workspace. Crossbeam creates and maintains a single overlaps Delta table in a catalog and schema you specify.

Crossbeam integrates with Databricks in two directions: this article covers the Databricks Integration (Push), which sends partner overlaps back into your Databricks workspace. You can also connect Databricks as a Data Source to sync your account data into Crossbeam. Both are independent and can point to different catalogs and schemas.
🔄 Need to pull data from Databricks into Crossbeam first? See Connect Databricks as a Data Source .

### Plan Availability
| | Free | Connector | Supernode | Enterprise |
| Databricks Integration | -- | -- | ✅ | ✅ |

### Prerequisites
Before connecting, confirm you have the following in your Databricks environment:
- A Databricks workspace with Unity Catalog enabled
- A SQL Warehouse that Crossbeam can connect to, both values are visible under your SQL Warehouse → Connection Details : Server hostname (e.g. dbc-12345abc-6789.cloud.databricks.com ) HTTP path (e.g. /sql/1.0/warehouses/abc123def456 )
- Server hostname (e.g. dbc-12345abc-6789.cloud.databricks.com )
- HTTP path (e.g. /sql/1.0/warehouses/abc123def456 )
- A Service Principal with an OAuth client secret, Crossbeam authenticates as this Service Principal and does not support personal access tokens or interactive OAuth

#### Creating the Service Principal
In your Databricks account console, navigate to:
- Settings → Identity and access → Service principals
- Click Add service principal
- Open the newly created Service Principal and navigate to Secrets → Generate secret
- Copy the Client ID (Application ID) and Client Secret, Crossbeam needs both The Client Secret is only shown once . Store it securely before closing the window.
- The Client Secret is only shown once . Store it securely before closing the window.
- Grant the Service Principal CAN USE on your SQL Warehouse: Navigate to SQL Warehouses → your warehouse → Permissions, then add the Service Principal with Can use
- Navigate to SQL Warehouses → your warehouse → Permissions, then add the Service Principal with Can use

### Step 1: Create the Destination Catalog and Schema
Create the catalog and schema where Crossbeam will write overlap data. You can use the same catalog and schema as your Sync integration or a different one. The schema must exist before enabling push, Crossbeam will create the overlaps table automatically.

CREATE CATALOG IF NOT EXISTS crossbeam_push;CREATE SCHEMA IF NOT EXISTS crossbeam_push.overlaps;
💡 Check out these Databricks resources if you need help with creating a catalog and creating a schema .

### Step 2: Grant the Service Principal Write Access
Replace crossbeam-sp with the display name or UUID of your Service Principal.
| -- Grant catalog access GRANT USE CATALOG ON CATALOG crossbeam_push TO `crossbeam-sp`; -- Grant schema usage and table creation permissions GRANT USE SCHEMA, CREATE TABLE ON SCHEMA crossbeam_push.overlaps TO `crossbeam-sp`; -- Grant read/write access to schema objects GRANT MODIFY, SELECT ON SCHEMA crossbeam_push.overlaps TO `crossbeam-sp`; |

These privileges allow Crossbeam to:
| Privilege | What it allows |
| CREATE TABLE | Create the overlaps Delta table on the first push |
| MODIFY | Merge (upsert) and delete overlap records on subsequent pushes |
| SELECT | Validate the table structure and confirm write permissions |

### Step 3: Enable Push in Crossbeam
In Crossbeam, navigate to Integrations → Databricks Push → Enable .

Enter the following:
| Field | Value |
| Server hostname | From SQL Warehouse → Connection Details |
| HTTP path | From SQL Warehouse → Connection Details |
| Catalog | crossbeam_push |
| Schema | overlaps |
| Client ID | Service Principal Application ID |
| Client Secret | OAuth client secret |
Click Enable.

When you enable push, Crossbeam will:
- Connect using your Service Principal credentials.
- Run CREATE TABLE IF NOT EXISTS <catalog>.<schema>.overlaps … USING DELTA .
- Validate that every required column is present.
- Run a no-op merge to confirm write permissions.
If any of these steps fail, you'll see a specific error in the UI indicating the cause (missing permissions, table not found, etc.).

### Destination Table Schema
Crossbeam writes overlap rows to <catalog>.<schema>.overlaps with the following columns:
| Column | Type | Description |
| organization_id | INT | Your Crossbeam organization ID |
| population_id | INT | Your population ID |
| population_name | STRING | Your population name |
| master_id | STRING | Your record ID for the overlapping account |
| mdm_type | STRING | Record type ( account, lead, etc.) |
| partner_organization_id | INT | Partner's Crossbeam org ID |
| partner_population_id | INT | Partner's population ID |
| partner_population_name | STRING | Partner's population name |
| partner_master_id | STRING | Partner's record ID for the same company |
| partner_name | STRING | Partner organization name |
| partner_domain | STRING | Partner organization domain |
| partner_ae_email | STRING | Partner AE email (if shared) |
| partner_ae_name | STRING | Partner AE name (if shared) |
| partner_ae_phone | STRING | Partner AE phone (if shared) |
| partner_ae_title | STRING | Partner AE title (if shared) |
| partner_record_name | STRING | Partner's record name |
| partner_record_website | STRING | Partner's record website |
| partner_record_type | STRING | Partner's record type |
| partner_record_country | STRING | Partner's record country |
| partner_record_industry | STRING | Partner's record industry |
| partner_record_employees | INT | Partner's record employee count |
| matched_at | TIMESTAMP | When the overlap was first matched |
| created_at | TIMESTAMP | When the row was created |
| updated_at | TIMESTAMP | When the row was last updated |
Rows are upserted via MERGE on (population_id, partner_population_id, master_id, partner_master_id) . Overlaps that are removed in Crossbeam (e.g., when a population changes) are deleted from this table on the next push.

✍️ Note
To populate partner_ae_name, partner_ae_email, partner_ae_phone, and partner_ae_title, you must include a users table in your Sync integration and add owner_id references on your accounts, deals, and/or leads tables.

matched_at reflects the original match date only, it does not update if the overlap itself changes later (e.g., an opportunity stage update or new shared fields). To track when an overlap record was last changed, use updated_at instead.

### Supported Features
| Feature | Details |
| Authentication | OAuth M2M (Service Principal client_id and client_secret ) |
| Destination | A single overlaps Delta table created by Crossbeam in your chosen catalog/schema |
| Write mode | Incremental MERGE (upsert) on every push |
| Stale-record cleanup | Yes, overlaps removed in Crossbeam are deleted from your overlaps table |
| Bookmarking | Per population pair, on updated_at |
| Table creation | Automatic, CREATE TABLE IF NOT EXISTS … USING DELTA |
| Trigger | On-demand via Crossbeam, no manual scheduling needed |

### Limitations
- Authentication: Service Principal OAuth M2M only. Personal access tokens and interactive OAuth are not supported.
- Fixed schema: The destination table schema is fixed. Additional columns cannot be added to the overlaps table.
- Single destination: Push cannot be split across multiple destination tables.

### Manage Databricks Integration
In Crossbeam, navigate to Integration → click on the Settings icon next to your Databricks integration.

From here you can:
- Enable Data Push : Turn on the push integration to send partner overlap data to your Databricks workspace
- Customize Data in Push : Control which overlap data and fields are included in each push
- Manage Partner Populations : Configure which partner Populations are included in your overlap data
- Partner-Specific Settings : Adjust settings on a per-partner basis to control what data is pushed for each partner relationship

Click Save changes when done.
Related Articles
- Connect Databricks as a Data Source
- How to Use the Slack App for Crossbeam
- Snowflake Integration
- Integrations Overview
- How to Set Up the Partner Account CRM Integration
- Connect Databricks as a Data Source


## Overview (HC 15961519)
URL: https://help.crossbeam.com/en/articles/15961519-setting-up-ai-agents-in-crossbeam-public-beta

In this article:
- Overview
- Plan Availability
- Prerequisites
- Permissions
- Create an Agent
- Test an Agent
- Example Slack Notifications
- Manage AI Agents
- FAQ

🧪 Join the Public Beta
AI Agents is available through Labs in the Crossbeam app.
Go to Settings > Labs, find AI Agents, and click Join Waitlist to get access.
AI Agents automate ecosystem alerts by watching for a specific condition in your Crossbeam data and posting a notification to Slack when a new match occurs. Instead of manually monitoring overlaps, you configure an Agent once and let it flag new mutual customers, shared opportunities, and closed-won deals as they happen.

Have a look at this video for a Demo on AI Agents:

✍️ Note
AI Agents run on an hourly cadence and only notify you of new matches identified since the last run. They don't fire for matches that already existed before the Agent was created.

### Plan Availability
🚧 Public Beta: AI Agents is available on Connector, Supernode, and Enterprise plans during public beta. Features, triggers, and conditions are subject to change before general availability.

If you encounter bugs, have suggestions, or want to share feedback, reach out to us at product@crossbeam.com, we'd love to hear from you. <!-- VALIDATE-OK[person-address]: verbatim public Crossbeam Help Center text -->

### Prerequisites
| Requirement | Details |
| Seat type | Full-access seat required to create or edit Agents |
| Slack | A Slack workspace must be connected, all beta actions are Slack-based |

### Permissions
Under Roles and Permissions, a new Agents permission controls what each role can do:
| Permission level | What it allows |
| Manage | Create, edit, enable/disable, and delete Agents |
| View | See the Agents page and existing Agents, but can't create or edit them |
✍️ Note
Only full-access seats can create AI Agents. Any user with access to the destination Slack channel will see the alerts.

### Create an Agent
- Click on Agents in the navigation bar
- Click the Create Agent button If Slack isn't connected yet, you'll see a prompt to connect it before you can continue ( steps here )
- If Slack isn't connected yet, you'll see a prompt to connect it before you can continue ( steps here )
- In the modal, enter a name for your Agent
- Select a trigger, the signal that will notify you when it occurs: New mutual customer New mutual account detected Partner opens a new opportunity on a mutual account Partner closes a deal won on a mutual account
- New mutual customer
- New mutual account detected
- Partner opens a new opportunity on a mutual account
- Partner closes a deal won on a mutual account
(Optional) Add one or more conditions to filter the trigger:
| Partner | Partner Score |
| Partner tag | Industry |
| Number of Employees | Amount |
| Close Date | Is Closed/Is Open |
✍️ Note: Conditions combine with AND only in this release, there's no OR or grouping.
- Select an action : Send a Slack message to channel (public or private) Send a Slack message to partner (Slack Connect) Send a Slack direct message Tag Account Owner by toggling on or off this option
- Send a Slack message to channel (public or private)
- Send a Slack message to partner (Slack Connect)
- Send a Slack direct message
- Tag Account Owner by toggling on or off this option
- Choose the Slack channel from the dropdown that appears after you select your action.


### Test an Agent
- Once all fields are filled in, click Test Agent
- Check the selected Slack channel for an example notification confirming your setup works as expected
- Click Save Agent to activate the Agent
✍️ Note
You must test an Agent before you can save it. Check your Slack channel to confirm you received the sample message.

### Example Slack Notifications
Single match
When only one record matches, the notification shows full detail, account owner, partner account owner, and employee count, along with a short recommendation and a button to view the overlap in Crossbeam.

Multiple matches
When more than one record matches in a single run, the notification shortens to a list of the top matches, each with its own short recommendation, plus a button to view the overlaps in Crossbeam.


### Manage AI Agents
The AI Agents page lists every Agent you have access to, showing its name, trigger, action, owner, and last run time.

From this page, you can:
- Enable or disable an Agent using the toggle, disabling pauses notifications without deleting the configuration
- Edit an Agent to change its name, trigger, conditions, or action
- Delete an Agent to remove it permanently

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

In this article:
- Overview
- Plan Availability
- How to Install the Crossbeam Slack App
- Search for a Company or a Person Search for a Company Search for a Person
- Search for a Company
- Search for a Person
- Understanding Slack Connect
- Set Up List Notifications Configure @Mentions for Account Owners
- Configure @Mentions for Account Owners
- Accessing Partner Owner Information
- FAQ
The Slack App for Crossbeam lets you search for account overlaps on demand, @mention Account Owners when new overlaps appear, and collaborate with partners in Slack Connect channels.

### Plan Availability
| Feature | Free | Connector | Supernode |
| /crossbeam command | ✓ | ✓ | ✓ |
| List Notifications |, | ✓ | ✓ |
| Partner owner fields (via Salesforce) |, |, | ✓ |
RevOps Note on Setup Time
The estimated setup time for this integration is 30 minutes . Please note that actual setup duration can vary based on your team’s configuration, customization needs, and overall account setup.

For a more accurate estimate or additional guidance, contact our Support team at support@crossbeam.com . <!-- VALIDATE-OK[person-address]: verbatim public Crossbeam Help Center text -->

### How to Install the Crossbeam Slack App
From the navigation menu, click on Data and select Integrations from the dropdown options

✍️ Note
​ You must have a Crossbeam account to use Crossbeam for Slack . You can only connect one Crossbeam account to Slack at a time. Authorizing Slack from a second organization removes the connection from your first.

### Search for a Company or Person

#### Search for a Company
Type /crossbeam followed by a company name in any Slack channel. Results display:
- The company name
- Which of your partners overlap with that account
- A link to view the full record in Crossbeam

The results are only visible to you, even in a public channel. To share results with your team, click the Share in Channel button.


#### Search for a Person
Enter /crossbeam people [First Last] to search for a specific contact. You must include people in the command for contact search to work.
😎 Pro Tip
Type /crossbeam help for a full list of available commands in Slack.

### Understanding Slack Connect
If you use the /crossbeam Slack command in a Slack Connect channel, click the View in Crossbeam button to open the full overlap record in your Crossbeam
account.

#### Set Up List Notifications
List notifications alert your team in Slack when new overlaps appear on a list. Notifications can route to public channels, private channels, or Slack Connect channels.

To configure a Slack notification from a list:
- Navigate to the List hub, click the bell icon directly in the list row, or open a saved list and click the Action button, then select notifications
- Under Slack channel, pick a channel from the dropdown If you have not connected to Slack, you will see a Connect to Slack button
- If you have not connected to Slack, you will see a Connect to Slack button

✍️ Note
You can only select private channels that the Crossbeam app has been invited to. In the channel, type /invite, select Add apps to this channel, and choose Crossbeam . This applies to Slack Connect channels as well.

#### Configure @Mentions for Account Owners
To @mention your Account Owner in a list notification, confirm the following:
- Your CRM Data Source includes Account Owner Name and Account Owner Email
- Your CSV or Google Sheet Data Source maps the Account Owner Email column
- Your List includes both Account Owner Name and Account Owner Email as columns
✍️ Note
If the Account Owner is not a member of the Slack channel, they won't receive an alert, but their name still appears in the notification so other members can add them.

If you include Account Owner Name but not Account Owner Email, the notification displays the name without an @mention.

Slack Connect Best Practices
Before routing notifications to a Slack Connect channel, confirm that all List overlaps are relevant to the partner(s) in that channel. Crossbeam will flag potential issues if you attempt to send notifications to a Slack Connect channel that includes an unknown organization, contains a partner not included in the List, or has multiple organizations in the channel.

### Accessing Partner Owner Information
The Slack App surfaces your account data only ; it does not display partner owner information.
| Slack Feature | What It Shows | What It Does Not Show |
| List Notifications | Your Account Owner (with optional @mention) | Partner's Account Owner |
| /crossbeam command | Company name, overlapping partners, link to Crossbeam | Partner owner fields |
Partner owner fields, such as the partner AE name, CSM name, email, or phone number, are available through your CRM instead. (Supernode plan only) If your partner shares owner fields from their CRM into Crossbeam (e.g., Partner Record Owner Name, Partner Record Owner Email, Partner Record Owner Phone ), you can surface them in:
- Crossbeam Ecosystem Overlap reports in Salesforce
- Related lists on Account or Opportunity layouts in Salesforce
To get partner owner visibility into your reps' workflow:
- Ask your partners to share owner fields. Request that partners push fields like AE name, CSM name, email, and phone into Crossbeam from their CRM.
- Push overlaps into Salesforce. Use the Crossbeam custom object to expose Partner Record Owner fields in Salesforce reports and related lists.
- Build alerts on top of Salesforce data. Optionally, configure Salesforce- or Slack-based alerts that include partner owner context to notify reps when new overlaps appear.
✍️ Note
See Salesforce Reporting with Crossbeam's Custom Object and Set Up Crossbeam Ecosystem Overlap Alerts in Salesforce for more details.

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


## Create a Custom Integration in Crossbeam (HC 4677142)
URL: https://help.crossbeam.com/en/articles/4677142-rest-api

Bring Crossbeam data to other parts of your company’s tech stack to drive automations, increase partner program visibility, and drive revenue growth.
❗️ Important
- Access to the REST API is only available on our Supernode plan. To upgrade your account, visit the Plan & Billing page .
- REST API calls do count towards Record exports limits .
Contact the support team at support@crossbeam.com for further assistance. <!-- VALIDATE-OK[person-address]: verbatim public Crossbeam Help Center text -->
Once your account has API access:
- Click Data in the left navigation, then Integrations
- Click + Create Integration
- Fill in the fields: Integration name, anything that identifies this app to you Integration description, optional, 140 characters max Callback URL, set to https://oauth.pstmn.io/v1/callback Allowed Origins, leave blank
- Integration name, anything that identifies this app to you
- Integration description, optional, 140 characters max
- Callback URL, set to https://oauth.pstmn.io/v1/callback
- Allowed Origins, leave blank
- Click Create Integration

#### Full Setup Instructions
For authentication, endpoints, and everything else you need to build against the API, head to the Crossbeam Developer Documentation .

- Salesforce Guide for Reports, Dashboards, & Automations Powered by Crossbeam
- Offline Partners
- Installation Guide: Crossbeam for Salesforce (v2)
- How to Set Up the Partner Account CRM Integration


## Enabling Snowflake Push (HC 4694521)
URL: https://help.crossbeam.com/en/articles/4694521-snowflake-integration

In this article:
- Enabling Snowflake Push Manage Integration Settings
- Manage Integration Settings
- Prerequisites
- Data Spec
- Overlaps
RevOps Note on Setup Time
The estimated setup time for this integration is 1 hour . Please note that actual setup duration can vary based on your team’s configuration, customization needs, and overall account setup.

For a more accurate estimate or additional guidance, contact our Support team at support@crossbeam.com . <!-- VALIDATE-OK[person-address]: verbatim public Crossbeam Help Center text -->
Our Snowflake integration allows Crossbeam to push partner overlap data back into Snowflake. Create custom dashboards, run analytics, and augment your CRM data with partner overlap data from Crossbeam.

Looking for our article about using Snowflake as a data source for Crossbeam? You can find it here .
❗️ Important
The initial Record Export when setting up an integration will also count towards the Record Export limit for your account.

Crossbeam Record Exports can be monitored here . Once you hit the Export Limit, Crossbeam insights will stop flowing into external tools.
On the Integrations page, locate the Snowflake tile and turn on the Enable toggle to enable pushing data back into Snowflake.
✍️ Note
If you don't see an option to enable the Snowflake push, you may not have it included in your plan. Contact your CSM, sales rep, or support@crossbeam.com for help. <!-- VALIDATE-OK[person-address]: verbatim public Crossbeam Help Center text -->


#### Manage Universal Integration Settings
From the left-side menu, click on Data . Select Integrations and open the Settings on the row for the Snowflake integration.

In the integration settings panel, you can:
- Adjust Data Pushes Toggle on or off to enable or disable data pushes for new partners or data populations as needed
- Toggle on or off to enable or disable data pushes for new partners or data populations as needed
- Customize Data in Push Click the arrow next to My Population to expand your available Populations Select or deselect the Populations to be pushed into the integration Click the arrow next to Partner Populations to expand and see the available Populations
- Click the arrow next to My Population to expand your available Populations Select or deselect the Populations to be pushed into the integration
- Select or deselect the Populations to be pushed into the integration
- Click the arrow next to Partner Populations to expand and see the available Populations
- Partner-Specific Settings You can choose to apply these settings to all specific partners collectively or customize them individually for each partner, depending on your needs
- You can choose to apply these settings to all specific partners collectively or customize them individually for each partner, depending on your needs
- Re-authorization If there are any authorization changes or errors with the integration, click the Re-authorize button and follow the prompts to complete the process
- If there are any authorization changes or errors with the integration, click the Re-authorize button and follow the prompts to complete the process

After making your selections, click Save to confirm and apply your changes.

### Prerequisites
Before enabling the push, you must set up your Snowflake integration. Go to your integrations page and click Set Up next to Snowflake.

We'll need two things:

1. Your Snowflake account region. Currently, we support four regions:
- US West (Oregon): this region is the only one not included in Snowflake URLs
- US East (Ohio)
- US East (N. Virginia)
- EU West (Ireland)
- EU-Central (Frankfurt)
Please let us know if your account is in a different region, and we can work to add support for you.

2. Your Snowflake account name. Account name can be found in the url of your Snowflake instance: https://<account_name>.<region>.snowflakecomputing.com.

Next, flip on the toggle to enable pushing data into Snowflake .

You're all set! Now, you will receive an incoming data share in Snowflake.


### Data Spec
You will receive an incoming data share in Snowflake called CROSSBEAM_OVERLAPS_<ORG-ID>_<RAND-IDENTIFIER>

When the data share is mounted, you will see a CROSSBEAM schema with an OVERLAPS view, defined below:


#### OVERLAPS
| Column | Data Type | Description |
| ENTITY_ID | VARCHAR | The CRM ID of the account/lead |
| ENTITY_TYPE | VARCHAR | One of account or lead |
| POPULATION_NAME | VARCHAR | The name of your population |
| PARTNER_NAME | VARCHAR | The partner organization name |
| PARTNER_POPULATION_NAME | VARCHAR | The name of the partner's population |
| PARTNER_AE_NAME | VARCHAR | The partner's AE name |
| PARTNER_AE_EMAIL | VARCHAR | The partner's AE email |
| PARTNER_AE_PHONE | VARCHAR | The partner's AE phone |
| MATCHED_AT | TIMESTAMP_TZ | The time the overlap was first visible in Crossbeam |
| PARTNER_DOMAIN | VARCHAR | Domain of partner org based on the website from registration |
| UPDATED_AT | TIMESTAMP_TZ | Last time the overlap record was updated in Snowflake |
| CREATED_AT | TIMESTAMP_TZ | When the overlap records were created in Snowflake |
| PARTNER_AE_TITLE | VARCHAR | The partner's AE title |
| PARTNER_RECORD_NAME | VARCHAR | The name of the partner record |
| PARTNER_RECORD_WEBSITE | VARCHAR | The website associated with the partner record |
| PARTNER_RECORD_TYPE | VARCHAR | The type of the partner record (e.g., organization, individual) |
| PARTNER_RECORD_COUNTRY | VARCHAR | The country associated with the partner record |
| PARTNER_RECORD_INDUSTRY | VARCHAR | The industry associated with the partner record |
| PARTNER_RECORD_EMPLOYEES | INTEGER | The number of employees at the partner's organization |
✍️ Note ​ MATCHED_AT reflects the original match date only, it does not update if the overlap itself changes later (e.g., an opportunity stage update or new shared fields). To track when an overlap record was last changed, use UPDATED_AT instead.
Related Articles
- Universal Integration Settings

- Connect Snowflake Data
- HubSpot Custom Object Integration
- How to Set Up the Partner Account CRM Integration
- Databricks Integration


## About this integration (HC 5206786)
URL: https://help.crossbeam.com/en/articles/5206786-matillion

The Matillion (Extract, Transform, Load) ETL connector helps data teams get things done faster in the cloud. With Matillion, you can unlock the value of your data cloud with low-code data ingestion, transformation, and data platform control. Matillion is a good option for companies that want to work with Crossbeam data inside cloud data platforms, across any major cloud provider or region.

This integration is built, hosted, and supported by Matillion, setup happens entirely on their side using an API-based OAuth connection with a Crossbeam Client ID and Client Secret. Visit the Crossbeam connector page on Matillion Exchange to download the connector and follow their setup instructions.

### What can you do with this integration?
- Enrich your enterprise analytics by including partner insights
- Extract, load, and transform your data without sacrificing sophistication or speed
- Meet data security and sovereignty requirements in any region of the world
- Remove connector anxiety with Matillion's create-your-own-connector feature
- Replicate data into your cloud data warehouse at no additional cost

### How can you get support?
This integration was built and is supported by Matillion. Send all bug reports and enhancement requests to Matillion via their support center .

Our customer success team can help you get oriented on the Crossbeam side (like generating API credentials), but setup and troubleshooting of the connector itself is handled by Matillion.
- Crossbeam Sales Settings and Features
- Offline Partners
- Crossbeam for Sales Attribution FAQs
- Crossbeam MCP Server
- How to Build a Product-Based Population Using Product2


## What Integrations are available? (HC 5251445)
URL: https://help.crossbeam.com/en/articles/5251445-integrations-overview

In this article:
- What integrations are available?
- Data sources
- External Data Connections
Crossbeam connects to the tools your team already uses, so partner data flows in from your systems of record, and account mapping insights flow back out to where your team works.
Explore all available integrations on the Integrations page in Crossbeam.

Additionally, visit the Crossbeam Marketplace for full details on every integration and solution, including Gong, Snowflake, HubSpot, Salesforce, Slack, and Adobe Marketo Engage.

### Data Sources
Crossbeam syncs data from the systems you already use to track customers and prospects:
- Salesforce
- HubSpot
- Microsoft Dynamics 365
- Snowflake
- Databricks
- Pipedrive
- Google Sheets
- CSV upload

### External Data Connections
Once your data's in Crossbeam, you can push insights back into your everyday tools:
- Crossbeam MCP Server, Connect AI tools like Claude, ChatGPT, and Glean to your Crossbeam data using the Model Context Protocol, so agents can surface partner context, recommendations, and account insights directly in your workflows.
- Crossbeam Copilot, Access Ecosystem Intelligence directly inside Salesforce, HubSpot, Gong, Outreach, and Chrome.
- Custom object integrations, Store account mapping results and partner data in custom objects in your CRM, kept up to date automatically.
- Ecosystem Signals, Get real-time partner activity (like an opportunity opening or closing) delivered via webhook, or pull it on demand via the REST API.
- Crossbeam for Slack, Get overlap alerts via DM or in a Slack Connect channel, and look up companies, people, and matches with the /Crossbeam command.
- Data Sources Overview: CSVs, CRMs and Data Warehouses
- Crossbeam Copilot Overview
- Crossbeam Copilot for Gong
- For Sales Seats: Getting Started with Crossbeam and Crossbeam Features
- Crossbeam Product Release Notes--11/13/2024


## 6574122-salesforce-reporting-with-crossbeam-s-custom-object.html (HC 6574122)
URL: https://help.crossbeam.com/en/articles/6574122-salesforce-reporting-with-crossbeam-s-custom-object

The Crossbeam Ecosystem Overlap Custom Object allows you to push partner data from Crossbeam directly into your Salesforce instance for reporting, dashboards, and viewing overlaps in Salesforce Classic.
✍️ Note
This feature is only available on the Supernode Plan. To upgrade your account, visit the Plan & Billing page .
Once your team has installed the Salesforce app, follow the steps in our Guide to Salesforce Reports, Dashboards & Automations.
Here is an example Report:

- Crossbeam Copilot for Salesforce
- Installation Guide: Crossbeam for Salesforce (v2)
- For Sales Seats: Getting Started with Crossbeam and Crossbeam Features
- Ready-to-Use Salesforce Crossbeam Reports
- How to Set Up the Partner Account CRM Integration


## Uninstall the Current HubSpot Legacy Integration (HC 7971155)
URL: https://help.crossbeam.com/en/articles/7971155-hubspot-custom-object-integration

In this article:
- Uninstall HubSpot Legacy Integration
- How to Install the HubSpot Custom Object Crossbeam Authentication Steps HubSpot Authentication Steps Configure Population Data in Crossbeam
- Crossbeam Authentication Steps
- HubSpot Authentication Steps
- Configure Population Data in Crossbeam
- HubSpot Contact Lists
- FAQ
RevOps Note on Setup Time
The estimated setup time for this integration is 3 hours but can vary significantly based on actual on your team’s configuration, customization needs, and overall account setup.

For a more accurate estimate or additional guidance, contact our Support team at support@crossbeam.com . <!-- VALIDATE-OK[person-address]: verbatim public Crossbeam Help Center text -->

❗️ Important
Already have a HubSpot Legacy integration installed? Follow the uninstallation steps below.

If you are installing the HubSpot Outbound Integration for the first time, click here to start the installation process.

From the Integration workspace, locate HubSpot Custom Object (legacy) from the Installed Integrations list.

On the right end of the row, click on the three dots . Next, you will see Remove Integration. Click on it.

In HubSpot, you will need to clear out all the existing records pushed from Crossbeam. The new integration will push new copies of these records once it is running.
✍️ Note
Any workflows or reports you have built with these objects will continue to work once we start pushing the new records. Click here for instructions for deleting records in HubSpot. Delete all records for the Custom Object called Crossbeam Overlaps . Users must have Bulk Delete permission to complete this process.

### How to Install the HubSpot Custom Object
✍️ Note
HubSpot Custom Object is only available on the Supernode plan.

To upgrade your account, visit the Plan & Billing page .
- You must have a Full Access Seat (Standard user or Admin role)in Crossbeam Core with Integration permissions to install.
- A HubSpot Sales Hub - Enterprise license is required to create the HubSpot custom object.
- You must have a HubSpot Marketing Hub - Professional license to send Crossbeam data to contact lists.
❗️ Important
The initial Record Export when setting up an integration will also count towards the Record Export limit for your account.

Crossbeam Record Exports can be monitored here . Once you hit the Export Limit, Crossbeam insights will stop flowing into external tools.

Learn more about maximizing your record exports here .

#### Crossbeam Authentication Steps
From the Integration workspace, locate HubSpot Custom Object from the Available Integrations section, and click the Install button.

Next, you will complete Crossbeam Authentication in the pop-up modal.

Once you have completed The Crossbeam Authentication, you will be prompted to complete the HubSpot Authentication.

​
Click the Next button when this step is complete.

#### HubSpot Authentication Steps
❗️Important
To complete the following authentication steps, you must add the required list of scopes for the Private App Access Token in HubSpot before successfully completing the setup process.

Failure to include the following required scopes will result in an error message, and the integration will not be completed.

Click here to learn how to create a HubSpot Private App Access Token.
The required scopes for this token are:
​
crm.lists.read crm.lists.write crm.objects.companies.read crm.objects.companies.write crm.objects.contacts.read crm.objects.contacts.write crm.objects.custom.read crm.objects.custom.write crm.schemas.companies.read crm.schemas.companies.write crm.schemas.custom.write crm.schemas.custom.read crm.import
On the HubSpot Authentication screen, click next to the New Authentication, and input the Access Token.

​Click the Next button when this step is complete.
In the next screen, configure the Crossbeam reports to be exported as Lists into HubSpot by clicking on the dropdown options under Report, and then click Add to Configuration . ​
Click the Next button when this step is complete.

The next screen will state the Installation is complete and prompt you to click Finish .
❗️ Important
The HubSpot Custom Object is not complete until you configure the Population data in Crossbeam.

#### Configure Population Data in Crossbeam
After clicking Finish in the HubSpot Authentication process, you will return to the Crossbeam Integration workspace to customize the data from Crossbeam that is pushed into HubSpot.

From the side panel, locate the Customize Data in Push section. To complete the HubSpot Custom Object Integration:
- Click the arrow next to My Data to expand your available Populations Select or deselect the Populations to be pushed into HubSpot
- Select or deselect the Populations to be pushed into HubSpot
- Click the arrow next to Partner Data to expand and see the available Populations and a list of your Specific Partners Select or deselect the Populations under Partner Data to be applied to all the Specific Partners collectively or individually per Specific Partner, depending on your needs
- Select or deselect the Populations under Partner Data to be applied to all the Specific Partners collectively or individually per Specific Partner, depending on your needs
Click Save Changes when done.

To adjust these settings or to reauthorize the connection, return to the Integrations workspace, locate HubSpot from the Installed Integrations list, and click Settings .
‼️New Fields Available in HubSpot‼️
The “Is a customer of” and “Is an open opportunity of” fields are now pushed directly to the HubSpot Company object, enabling smarter segmentation and reporting. ​
Learn about Enhanced Ecosystem Reporting here .

### HubSpot Contact Lists
Selected reports from the Install process will automatically sync relevant overlaps to corresponding lists in HubSpot. These lists will maintain the same naming convention as your Crossbeam reports, with 'Crossbeam' added for easy recognition.

All overlaps in associated contact lists update in real-time, ensuring accuracy by removing stale overlaps and revealing new records. Your marketing team can now utilize these lists for precise co-marketing campaigns.

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


## Setting Up (HC 8337148)
URL: https://help.crossbeam.com/en/articles/8337148-sso-exception-user-for-oauth-integrations-with-crossbeam

When OAuth (Open Authentication) is required from external applications, you will need to establish an SSO Exception User with Crossbeam to complete the integration.
❗️ Important
SSO Exception User is required for any OAuth integrations, including the Salesforce Copilot and Crossbeam for Sales.
In the Crossbeam settings, click on Organizational Settings . Scroll down the page to Login Options.

- Temporarily enable the Don't Require SSO option and click Save Settings
- Invite the user that will be authenticating the integration into Crossbeam with an Admin role.
- Once the user receives their registration email from Crossbeam, they will register with a Username + Password or Google Sign In. After registering, the user will appear in the list of users on the Team Page . In the Login Method column, you should see "Standard" or "Google" instead of "SSO"

- Return to the Organizational Settings page and select Require SSO. Be sure to click into the SSO Login Exception box and select the name of the Standard or Google login method user :
- Click Save Settings
- To authenticate the Salesforce Integration, follow the SFDC Installation steps, here .
- In the first step of Crossbeam Setup in Salesforce, click Validate to log in in to your Crossbeam account. Be sure to use the credentials of the SSO Exception User.
✍️ Note
When authenticating/validating an integration, be sure to use the same login credentials listed on your team page (Username+ Password or Google Sign In).
📄 Related Articles
- Crossbeam Copilot for Salesforce
- Setting Up SAML SSO in Crossbeam
- Crossbeam Copilot for Salesforce FAQs
- Installation Guide: Crossbeam for Salesforce (v2)
- For Sales Seats: Getting Started with Crossbeam and Crossbeam Features


## Connect PartnerStack (HC 8533576)
URL: https://help.crossbeam.com/en/articles/8533576-partnerstack-integration

In this article:
- Connect PartnerStack
- Access PartnerStack in Crossbeam Lists Shared Lists Activity Timeline
- Lists
- Shared Lists
- Activity Timeline
- Manage Integration
PartnerStack's comprehensive partner ecosystem platform is designed to empower companies to boost their partnership-generated revenue. The integration of Crossbeam and PartnerStack helps users seamlessly connect account mapping with partner relationship management. With this integration, users can:
- Identify valuable partnership opportunities
- Easily refer leads from Crossbeam to PartnerStack
- Monitor the progress of these leads directly within PartnerStack
- Automatically compensate partners for closed-won deals
✍️ Note
PartnerStack Integration is only available on the Connector Plan and Supernode Plan. To upgrade your account, visit the Plan & Billing page .
❗️ Important
User must be a PartnerStack Admin to complete the installation in Crossbeam.
To install PartnerStack:
- Click the Data icon and select Integrations from the side panel
- Next, locate the PartnerStack tile from the Available Integrations section
- Click Install to start the process

Click Connect to Crossbeam when prompted by the PartnerStack authorization page to complete the installation. Your Lists will now display a new private Column for PartnerStack.

### Access PartnerStack in Crossbeam

#### Lists
Select List from the navigation bar and open a saved List.
Once in an open List, it will now display a private column labeled PartnerStack .

If you don't see the column straight away, add the Partnerstack column by clicking the Columns button -> expand Crossbeam Columns, checking the box for Partnerstack-> click Save.

Locate a lead you want to send to PartnerStack from the table. Click the Refer Lead button. After clicking the button, select a Partner from the drop-down options and complete the required fields in the pop-up.

Once the Refer Leads information is complete, click Submit Lead and the information will be sent to PartnerStack.

After submitting the lead, the PartnerStack column will now display the date the Lead was sent to PartnerStack to complete the deal cycle.


#### Activity Timeline
Once a lead has been submitted to PartnerStack, Crossbeam will add this information to the Individual Record Activity Timeline. To access this information, click the record Name in the List or Shared List with the PartnerStack Referred Lead. This will open the Individual Record. Select the Timeline tab to see the date and time the lead was sent to PartnerStack.


#### Static Shared Lists
You can also refer leads to PartnerStack from Static Shared Lists . Navigate to Lists from the navigation bar. Click on a Static shared List to open it. You will see an icon in the Name column; click it to send partner info to PartnerStack. After clicking the button, select a Partner from the drop-down options and complete the required fields in the pop-up.

Once the Refer Leads information is complete, click Submit Lead, and the information will be sent to PartnerStack.

### Manage Integration
Click on Data from the navigation bar, and select Integrations . Next, locate the PartnerStack row under the Installed Integrations section.

This row displays if the integration is Active. Click the View App button to be redirected to PartnerStack, or click the three dots to reauthorize or to delete the integration.

📄 Related Articles
- Standard Account Mapping Single Partner List
- Shared Lists

- HubSpot Custom Object Integration
- Gong Integration
- Installation Guide: Crossbeam for Salesforce (v2)
- How to Set Up the Partner Account CRM Integration


## Set Up Integration (HC 8575980)
URL: https://help.crossbeam.com/en/articles/8575980-adobe-marketo-engage-integration

In this article:
- Set Up Integration
- Connect Adobe Marketo Engage Authentication Process Configuration of Crossbeam Reports to Marketo Programs
- Authentication Process
- Configuration of Crossbeam Reports to Marketo Programs
- Manage Integration Add or Remove Reports to Marketo Configuration
- Add or Remove Reports to Marketo Configuration
With the Crossbeam and Adobe Marketo Engage integration, Marketing Teams can improve leads and get them to sales faster. The integration uses Crossbeam reports to automatically bring in partner overlaps, making co-marketing tasks like nurturing joint integrations and promoting partner events and webinars much simpler.
✍️ Note
Adobe Marketo Integration is only available on the Supernode Plan. To upgrade your account, visit the Plan & Billing page .
Click here for the detailed Adobe Marketo Engage Installation Guide.
❗️ Important
Salesforce must be connected as a Data Source within your Crossbeam account. Click here to learn more.
To install Adobe Marketo Engage Integration:
- Click on Data from the navigation bar, select Integrations
- Next, locate the Adobe Marketo Engage tile from the Available Integrations section
- Click Install to start the process

After clicking Install, a new window will open.

### Connect Adobe Marketo Engage
❗️ Important
To complete the installation, a Marketo Admin is required.

#### Authentication Process
Click here for the detailed instructions the Marketo Administrator will need to complete this process.
In the pop-up modal, you will be prompted to complete the following:
- Crossbeam Authentication process Click on New Authentication Create a New Authentication Select your personal credentials Authorize App Access
- Click on New Authentication
- Create a New Authentication
- Select your personal credentials
- Authorize App Access
- Marketo Authentication process Click on New Authentication Create a New Authentication
- Click on New Authentication
- Create a New Authentication

❗️ Important
The required fields for the New Marketo Authentication Process will need to be provided by a Marketo Administrator.

#### Configuration of Crossbeam Reports to Marketo Programs
After the authentication process is set up, you will be prompted to configure Crossbeam reports to Marketo Program.

Follow the instructions below or watch this video:

To configure Crossbeam Reports to Marketo:
- Associate your Crossbeam Reports to your Marketo Programs on the Please Configure Overlaps window Under Organization, click the drop-down arrow to select your Crossbeam Organization Under Crossbeam Report, click the drop-down arrow to select your desired Crossbeam Report Under Program, click the drop-down arrow to associate the selected Crossbeam Report to the desired Marketo Program Repeat the above steps to add more associations Click Next when done
- Under Organization, click the drop-down arrow to select your Crossbeam Organization
- Under Crossbeam Report, click the drop-down arrow to select your desired Crossbeam Report
- Under Program, click the drop-down arrow to associate the selected Crossbeam Report to the desired Marketo Program Repeat the above steps to add more associations
- Repeat the above steps to add more associations
- Click Next when done
- Enter a date for processing to ensure all persons are captured in the Members tab of your desired Marketo Programs
- Click Next
Click finish when done. Please note, the initial installation sync may take up to 10 mins before data will be available to view in Marketo.

### Manage Integration
Click Data from the navigation bar, and select Integrations . Next, locate the Adobe Marketo Engage row under the Installed Integrations section.

This row displays the integration status as Active. Click the Configure button to adjust the configuration setup, or click the three dots to remove the integration from Crossbeam.


#### Add or Remove Reports to Marketo Configuration
Reports made in Crossbeam can be associated with a program built in your Marketo account.

Add a Report:
- Create a Report in Crossbeam with overlaps
- Navigate to the Integrations workspace and locate Adobe Marketo Engage under the Installed Integrations list Click the Configure button next to Adobe Marketo Engage
- Click the Configure button next to Adobe Marketo Engage
- In the pop-up modal, you will be prompted through the authorization windows; click Next until you reach the Please Configure Overlaps window On the Please Configure Overlaps window, click the Add to Configuration button Select an Organization, Crossbeam Report, and Marketo Program from each of the drop-down options Click the Next button until you reach the Finish button to close the modal
- On the Please Configure Overlaps window, click the Add to Configuration button
- Select an Organization, Crossbeam Report, and Marketo Program from each of the drop-down options
- Click the Next button until you reach the Finish button to close the modal
Remove a Report:
- to remove a report from the Please Configure Overlaps window Hover your mouse over the row you want to remove, and a red X will appear to the right of the row Click the red X to remove the row Click the Next button until you reach the Finish button to close the modal
- Hover your mouse over the row you want to remove, and a red X will appear to the right of the row
- Click the red X to remove the row
- Click the Next button until you reach the Finish button to close the modal

- Integrations Overview
- HubSpot Custom Object Integration
- Adobe Marketo Engage Installation and Configuration Guide
- Microsoft Dynamics Custom Object Integration
- How to Set Up the Partner Account CRM Integration


## Create a Basic Crossbeam Ecosystem Overlap Report (HC 8765980)
URL: https://help.crossbeam.com/en/articles/8765980-salesforce-guide-for-reports-dashboards-automations-powered-by-crossbeam

Follow this guide to efficiently utilize partner intelligence in Salesforce. Learn to generate reports for sales and marketing teams and create visual dashboards for your GTM team.

In this article:
- Create a Basic Crossbeam Ecosystem Overlap Report
- Create a Crossbeam Overlap Report for Account Executives Common Use Cases
- Common Use Cases
- Guide to Dashboards
- Salesforce Workflows and Automations Create Alert in Salesforce Partnership Introduction Requests
- Create Alert in Salesforce
- Partnership Introduction Requests
❗️ Important
To create Reports & Dashboards: a user will need to have the Crossbeam Reports User or Crossbeam Setup User Permission Set in Salesforce.

To create Workflows and Automations: a user will need to be a system admin in Salesforce.
Use Reports to identify overlapping accounts with partners to facilitate warm introductions, accelerate deals, prioritize integrations, and gain other strategic advantages for your organization.

First, click the Reports tab in Salesforce
- Select New Report
- On the Create Report screen, make sure you select All on the left-hand side before next steps

- Next, type in the word Crossbeam to select a report type
- Then select Crossbeam Ecosystem Overlaps with Account and click Start Report
- Now that you’re in the report view, click the Filters tab on the left-hand side
- Now change the filter selection within the Show Me drop-down from My Crossbeam ecosystem overlaps to All Crossbeam Ecosystem Overlaps in order to see all of your organization’s accounts where an overlap occurs with your partners.

- Next, click on the Outline tab on the left-hand side to start bringing data into the report
- In the columns section on the bottom left, bring in the fields (adjust as needed): Partner Name, Partner Standard Population, Partner AE Name, and Partner AE Email You can bring these fields in by simply typing in Partner, and you’ll see the options appear.
- You can bring these fields in by simply typing in Partner, and you’ll see the options appear.
- Hit Run to generate the report

Example Report:

Add more filers as needed.

For example, if we want to look at one specific partner based on mutual accounts that are a customer of that partner, we can apply a filter:
- Within the report, click Edit on the top right If you prefer to preserve the original report, select Save As then follow the steps below Go into the Filters tab again And add the filter Partner Name and select contains followed by the name of the partner Next, add the filter Partner Standard Populations and select equals followed by customers
- If you prefer to preserve the original report, select Save As then follow the steps below
- Go into the Filters tab again
- And add the filter Partner Name and select contains followed by the name of the partner
- Next, add the filter Partner Standard Populations and select equals followed by customers

- Click Run, now you’ve automatically surfaced all the mutual customer overlaps across the partner you were curious about.
In this example, we’re now looking at all accounts that are customers of our partner Bozala :

✍️ Note
You can remove the column Crossbeam Ecosystem Overlap: Overlap Name . This is a unique ID for that specific overlap and is not compelling for revenue reporting purposes.

### Create a Crossbeam Ecosystem Overlap Report for Account Executives
Create a Crossbeam Ecosystem Overlap Report for Account Executives to prioritize target accounts and potential co-selling partners based on partner intelligence for specific time frames.
- Continue with the Report you created in the above section If you prefer to preserve the original report - Select Save As
- If you prefer to preserve the original report - Select Save As
- In the report builder, open the Outline panel
- In the Group Rows section, type in Account Owner
- Next, click Run

In the example below, we’re now looking at a report that’s segmented by Account Executive/Owner. We can see all of Sawyer Porter's accounts that are currently customers of our partner, Bozala.


#### Common Use Cases
- SDR Prospecting Reports How do our prospects overlap with our partners' customers? Can we use that partner intelligence for more personalized messaging? How can we leverage those partners to bridge warm introductions?
- How do our prospects overlap with our partners' customers?
- Can we use that partner intelligence for more personalized messaging?
- How can we leverage those partners to bridge warm introductions?
- AE Target Account Reports How do our prospects overlap with our partners' customers? Can we use that intel for more personalized messaging? Can we leverage those partners to bridge warm introductions?
- How do our prospects overlap with our partners' customers?
- Can we use that intel for more personalized messaging?
- Can we leverage those partners to bridge warm introductions?
- Marketing Campaign Reports Who are the shared customers across our partners? Can we leverage a list of overlapping accounts with a specific partner to highlight our recently launched integration to boost retention? Can we target a list of shared customers that haven’t adopted our integration yet to boost activation? Can we combine partner data with intent data to create a targeted list of accounts where we can generate extremely personalized messaging to drive high-quality pipe gen?
- Who are the shared customers across our partners?
- Can we leverage a list of overlapping accounts with a specific partner to highlight our recently launched integration to boost retention?
- Can we target a list of shared customers that haven’t adopted our integration yet to boost activation?
- Can we combine partner data with intent data to create a targeted list of accounts where we can generate extremely personalized messaging to drive high-quality pipe gen?

### Guide to Dashboards
Dashboards effectively guide GTM teams in analyzing Crossbeam ecosystem overlaps, helping them identify where, who, and how to allocate their time strategically.

Get started by saving a report, similar to the one we built earlier.

Let’s take the below Target Account Report as an example:

We’re looking at a report grouped by both Account Owner and Partner. We’ve applied the filter to only look at accounts that are mutual customers of these partners using the Custom Overlap Object, as well as specific account tiers.

In the columns, we’ve added: Account Name, Partner Population, Account Tier, Account Region, Partner AE Name, Partner AE Email, and Revenue Bands (note - this is all illustrative data).

Now, as a quick refresher, below is the Outline of the report and associated Filters:

To save this Report:
- Click the Dashboards tab in Salesforce and click New Dashboard

- Give your Dashboard a name and then proceed from there.
- Click + Widget, which is a big blue button at the top right
- Select the Report you want to bring into the dashboard. This may be front and center, or you can use the search bar to find the exact report you want.

- Add a display Widget. You can choose how you want the visualization to be displayed, whether that’s a bar graph, linear graph, pie chart, etc.:

Click Add and you have the first step towards building out a Dashboard.
Below are a few examples of Dashboards the sales team uses here at Crossbeam to help identify the right partners to engage with and where to prioritize our time.

We think about the following information to help with co-selling:
- Open Opportunities that are Customers of our Partners
- Named Accounts that are Customers of our Partners

One really powerful set of data to dive into--which Partner AEs should our AEs be working with based on the highest number of overlaps between the two?

Similar to the report above, you can create a new report that’s grouped by:
- Account Owner
- Partner AE Name
- Partner Name

Example Dashboard:

With this Dashboard, you can now see:
- AEs vs. Partner AEs with regard to number of overlapping accounts
- Example: Brandon has the majority of his overlaps with Tom
- Example: Tracy has the majority of her overlaps with both Tom and Murphy
This will enable you to identify the right partners to engage with and where to prioritize your time.

### Salesforce Workflows and Automations
Explore the flexibility of Crossbeam’s overlap data and harness the vast capabilities of Salesforce through automation and workflows for enhanced efficiency.

#### Create Alert in Salesforce
When activity is happening on an account, this is a great time to connect with that partner to get insight on what’s happening/happened with that account.

For example:

If a partner opened up a new opportunity, it’s helpful to understand:
- Who are they working with?
- How far along are they in the sales cycle?
- What’s the use case?
- Have integrations (i.e. your product) been brought up in conversations?
- What’s the overall solution they’re looking to implement?
- Is there a joint solution opportunity for co-selling?
Or, if a partner just closed the account as a customer, it’s helpful to know:
- What did procurement look like?
- Is there anything from a legal, security, or finance perspective that we should know?
- Who was involved from an influencer/champion perspective?
- Who tends to be the final signer?
- What does implementation look like and the rollout plan? (many times you need both products to complete the full-end solution)
- Did they bring up a need for where our solution could help out/complement this?
👀Learn more about setting up alerts in this article here .

#### Partnership Introduction Requests
Getting warm partner data into the hands of your GTM teams is great, but maybe you want to create a more formalized process?

It’s important (especially for tracking influenced revenue) to:
- Centralize control of introduction requests vs. granting Account Executives full autonomy
- Have visibility into which partners have more influence & prioritize introduction requests accordingly (i.e.: account overlaps with multiple partners)
- Manage the volume of introduction requests to a given partner(s)

These are all important things to consider, depending on your approach to partner introductions and the processes you have in place to support.

Create a Task (sometimes Tasks are placed beneath Crossbeam’s Salesforce App)
When a rep sees an overlap in the App/Widget, they can kick off a request by filling in a Subject, some additional comments/context, and the Partner they want to be introduced to.

Those requests can then be sent into a Report where the partnership/alliance teams can track and manage everything in one single location.

The tasks will be assigned to the relevant Partner Manager to execute on, as well as relevant dates associated to those requests.

As partner teams track partner sourced and influenced revenue, conversions, and deals, there will be an entire report that allows them to see each and every account where requests were made. This is not to say it covers everything 100%, but does provide a more succinct workflow and process.
That’s it! You’re now a pro in building reports for your sales and marketing teams and creating visual dashboards for your entire GTM team.
✍️ Note
Want to build an ecosystem dashboard to evaluate opportunities for sourcing, influencing, and expanding customer relationships at a glance? To learn more, see our article: Create the Crossbeam 360 Dashboard in Slaesforce .
🎓 Sign into Crossbeam Academy to further explore the Crossbeam Salesforce Custom Object!
- Crossbeam Copilot for Salesforce
- Installation Guide: Crossbeam for Salesforce (v2)
- Setting Up a Crossbeam Ecosystem Overlaps Related List in Salesforce
- How to Create a Combined Overlap and Partner Account Report Type in Salesforce


## Option 1: Create Email Template (HC 8770077)
URL: https://help.crossbeam.com/en/articles/8770077-set-up-crossbeam-ecosystem-overlap-alerts-in-salesforce

Follow the steps below to create overlap alerts in Salesforce.

In this article:
- Option 1: Create Email Template Create Email Alerts Create a Flow
- Create Email Alerts
- Create a Flow
- Option 2: Create a Flow
Click the Setup icon in the top-right corner.
In the Quick Find search bar, type Email Templates, select Classic Email Templates .

Next, create a new Email Template. Click on the New Templates button.

Additional email template options can be viewed here .
Under Choose the type of email template, select Text, click Next .

In the next screen, fill in: Email Template Name, Subject, and Email Body.

Check the Available For Use checkbox.

To provide a link to the Overlap record:
- open an existing Overlap record and replace the Id in the link with {!xbeamprod__Crossbeam_Overlap__c.Id}
- {!xbeamprod__Crossbeam_Overlap__c.Id}
Click Save .

#### Create Email Alerts
Create two Email Alerts: one for Account Owner and the other for Lead Owner.
- In the search bar, type Email Alert and select Email Alerts from the dropdown options

- Click New Email Alert to create a new Email Alert.
- Name your first Email Alert as New Overlap Notification - Account Owner Description: New Overlap Notification - Account Owner Object: Crossbeam Overlap Email Template: New Overlap Notification Recipient Type: Account Owner (Move “Account Owner” from Available Recipients to Selected Recipients) From Email Address: Current User’s email address (Select Org-Wide email address if applicable) Click Save & New
- Description: New Overlap Notification - Account Owner
- Object: Crossbeam Overlap
- Email Template: New Overlap Notification
- Recipient Type: Account Owner (Move “Account Owner” from Available Recipients to Selected Recipients)
- From Email Address: Current User’s email address (Select Org-Wide email address if applicable)
- Click Save & New
- Name your second Email Alert as New Overlap Notification - Lead Owner Description: New Overlap Notification - Lead Owner Object: Crossbeam Overlap Email Template: New Overlap Notification Recipient Type: Related Lead or Contact Owner (Move “Lead or Contact Owner” from Available Recipients to Selected Recipients) From Email Address: Current User’s email address (Select Org-Wide email address if applicable) Click Save.
- Description: New Overlap Notification - Lead Owner
- Object: Crossbeam Overlap
- Email Template: New Overlap Notification
- Recipient Type: Related Lead or Contact Owner (Move “Lead or Contact Owner” from Available Recipients to Selected Recipients)
- From Email Address: Current User’s email address (Select Org-Wide email address if applicable)
- Click Save.

#### Create a Flow
In the search box, type in Flow and select Flows from the dropdown options.

- Click New Flow on the top right to create a new Flow.
- Select Record-Triggered Flow and click Next . Select Auto-Layout and click Next .
- In Configure Start: Object: Crossbeam Ecosystem Overlap Configure Trigger: A record is created Optimize the Flow for: Actions and Related Records
- Object: Crossbeam Ecosystem Overlap
- Configure Trigger: A record is created
- Optimize the Flow for: Actions and Related Records

- Click the “+” symbol and search Decision Label: Account or Lead There should be 3 Outcomes Account Label = Account Condition Requirements to Execute Outcome = All Conditions Are Met (AND) {!$Record.xbeamprod__Account__c} Is Null = {!$GlobalConstant.False} Lead Label = Lead Condition Requirements to Execute Outcome = All Conditions Are Met (AND) {!$Record.xbeamprod__Account__c} Is Null = {!$GlobalConstant.True} {!$Record.xbeamprod__Lead__c} Is Null = {!$GlobalConstant.False} Default Outcome
- Label: Account or Lead
- There should be 3 Outcomes Account Label = Account Condition Requirements to Execute Outcome = All Conditions Are Met (AND) {!$Record.xbeamprod__Account__c} Is Null = {!$GlobalConstant.False} Lead Label = Lead Condition Requirements to Execute Outcome = All Conditions Are Met (AND) {!$Record.xbeamprod__Account__c} Is Null = {!$GlobalConstant.True} {!$Record.xbeamprod__Lead__c} Is Null = {!$GlobalConstant.False} Default Outcome
- Account Label = Account Condition Requirements to Execute Outcome = All Conditions Are Met (AND) {!$Record.xbeamprod__Account__c} Is Null = {!$GlobalConstant.False}
- Label = Account
- Condition Requirements to Execute Outcome = All Conditions Are Met (AND)
- {!$Record.xbeamprod__Account__c} Is Null = {!$GlobalConstant.False}
- Lead Label = Lead Condition Requirements to Execute Outcome = All Conditions Are Met (AND) {!$Record.xbeamprod__Account__c} Is Null = {!$GlobalConstant.True} {!$Record.xbeamprod__Lead__c} Is Null = {!$GlobalConstant.False}
- Label = Lead
- Condition Requirements to Execute Outcome = All Conditions Are Met (AND)
- {!$Record.xbeamprod__Account__c} Is Null = {!$GlobalConstant.True}
- {!$Record.xbeamprod__Lead__c} Is Null = {!$GlobalConstant.False}
- Default Outcome

- Click the “+” under the Account Path and select Action Search for New Overlap Notification - Account Owner and select New Overlap Notification - Account Owner Label = New Overlap Notification - Account Owner Record Id = {!$Record.Id}
- Search for New Overlap Notification - Account Owner and select New Overlap Notification - Account Owner
- Label = New Overlap Notification - Account Owner
- Record Id = {!$Record.Id}
- Click the “+” under the Lead Path and select “Action” Search for “New Overlap Notification - Lead Owner” and select “New Overlap Notification - Lead Owner” Label = New Overlap Notification - Lead Owner Record Id = {!$Record.Id}
- Search for “New Overlap Notification - Lead Owner” and select “New Overlap Notification - Lead Owner”
- Label = New Overlap Notification - Lead Owner
- Record Id = {!$Record.Id}
- Save and activate the Flow. Your Flow should look something like this.


### Option 2: Create a Flow
In the search bar, type in Flow and select Flows.

- Click New Flow on the top right to create a new Flow.
- Select Record-Triggered Flow and click Next . Select Auto-Layout and click Next .
- In Configure Start: Object: Crossbeam Ecosystem Overlap Configure Trigger: A record is created Optimize the Flow for: Actions and Related Records
- Object: Crossbeam Ecosystem Overlap
- Configure Trigger: A record is created
- Optimize the Flow for: Actions and Related Records

- Open the Toolbox, located on the left side of the screen, click New Resource, choose Text Template API Name = NewOverlapNotificationTemplate Body = The email body. Example: Hello, A new Overlap record was created. Link to record: https://candyboxcrm--crossbeam.lightning.force.com/lightning/r/xbeamprod__Crossbeam_Overlap__c/{!record.Id}/view
- API Name = NewOverlapNotificationTemplate
- Body = The email body. Example: Hello, A new Overlap record was created. Link to record: https://candyboxcrm--crossbeam.lightning.force.com/lightning/r/xbeamprod__Crossbeam_Overlap__c/{!record.Id}/view
- Example: Hello, A new Overlap record was created. Link to record: https://candyboxcrm--crossbeam.lightning.force.com/lightning/r/xbeamprod__Crossbeam_Overlap__c/{!record.Id}/view
- Hello, A new Overlap record was created. Link to record: https://candyboxcrm--crossbeam.lightning.force.com/lightning/r/xbeamprod__Crossbeam_Overlap__c/{!record.Id}/view
- Click New Resource under the Toolbox and select Formula API Name = EmailAddressFormula Data Type = Text Formula = IF( {!$Record.xbeamprod__Account__c} != '', {!$Record.xbeamprod__Account__r.Owner.Email}, {!$Record.xbeamprod__Lead__r.Owner:User.Email} )
- API Name = EmailAddressFormula
- Data Type = Text
- Formula = IF( {!$Record.xbeamprod__Account__c} != '', {!$Record.xbeamprod__Account__r.Owner.Email}, {!$Record.xbeamprod__Lead__r.Owner:User.Email} )
- Click the “+” and select Action . Select Send Email . Set the variable values like below:
- Set the variable values like below:

Click the Done button.

Your flow should look like this:

- How to Use the Slack App for Crossbeam
- Crossbeam Sales Settings and Features
- Installation Guide: Crossbeam for Salesforce (v2)
- Setting Up a Crossbeam Ecosystem Overlaps Related List in Salesforce


## Install the App (HC 8801394)
URL: https://help.crossbeam.com/en/articles/8801394-adobe-marketo-engage-installation-and-configuration-guide

In this article:
- Install the App
- Configure Crossbeam Reports to Marketo
The Crossbeam-Marketo integration identifies overlapping accounts, retrieves associated individuals in Marketo, and applies them to your designated Marketo Programs. This document serves as an installation and configuration guide for the Marketo app.
Installation Requirements
- You must have Salesforce connected as a Data Source within your Crossbeam account to leverage this integration. See our help article here for more information on Salesforce as a Data Source.
- You must be on the Supernode plan to access this integration. Visit our pricing page here for more details.
- Navigate to the Integrations Workspace in your Crossbeam account On the Marketo tile, click Install
- On the Marketo tile, click Install
- Complete the Crossbeam Authentication process: Click on New Authentication Create a New Authentication Select your personal credentials Authorize App Access
- Click on New Authentication
- Create a New Authentication
- Select your personal credentials
- Authorize App Access
- Complete the Marketo Authentication process: Click on New Authentication
- Click on New Authentication
- Create a New Authentication Details to fill in the required fields will need to be accessed and provided by a Marketo administrator. See below for instructions on how to find them in your Marketo instance.
- Details to fill in the required fields will need to be accessed and provided by a Marketo administrator. See below for instructions on how to find them in your Marketo instance.
In Marketo, navigate to:
- API endpoint domain: Admin >> Integration >> Web Services >> Rest API >> Endpoint Copy the endpoint URL, excluding the “/rest” at the end of the URL
- Copy the endpoint URL, excluding the “/rest” at the end of the URL
- Client ID and Client Secret: Admin >> Integration >> LaunchPoint >> Create a New Service Enter details
- Enter details
example:
- Select Create
- Select View Details Client ID and Client Secret will be displayed
- Client ID and Client Secret will be displayed
- Copy & paste the above values from Client ID and Client Secret into the Crossbeam modal Select Create within the Crossbeam modal to complete installation
- Select Create within the Crossbeam modal to complete installation

### Configure Crossbeam Reports to Marketo
Once you’ve installed the Marketo app using the steps above, follow the instructions below or watch this 1-minute video to learn how to configure and associate Crossbeam Reports to Marketo Programs.
- Associate your Crossbeam Reports to your Marketo Programs Organization >> Select your Crossbeam Organization Report >> Select your desired Crossbeam Report Program >> Associate the selected Crossbeam Report to the desired Marketo Program
- Organization >> Select your Crossbeam Organization
- Report >> Select your desired Crossbeam Report
- Program >> Associate the selected Crossbeam Report to the desired Marketo Program
- Repeat the above steps for additional associations. Associations can be removed at any time.

- Enter a date for processing to ensure all persons are captured in the Members tab of your desired Programs

- HubSpot Custom Object Integration
- Adobe Marketo Engage Integration
- Installation Guide: Crossbeam for Salesforce (v2)
- Installation Guide: Crossbeam for Salesforce (Connector Plan)


## Before you begin (HC 9280237)
URL: https://help.crossbeam.com/en/articles/9280237-installation-guide-crossbeam-for-salesforce-v2

In this article:
- Before you begin What's in this guide? Crossbeam user requirements Salesforce user requirements
- What's in this guide?
- Crossbeam user requirements
- Salesforce user requirements
- Installing the managed package
- Connecting to your Crossbeam account Assigning the "Crossbeam Setup User" permission set Accessing the Crossbeam Setup App Completing the Setup Steps
- Assigning the "Crossbeam Setup User" permission set
- Accessing the Crossbeam Setup App
- Completing the Setup Steps
- Configure Trusted URLs
- Enable & Configure Push to Crossbeam Ecosystem Overlap Custom Object Customize What Data is Pushed
- Customize What Data is Pushed
- Assigning permission sets Administrative Permissions Lightning Web Component (Crossbeam Copilot) Permissions: Custom Object Permissions: Placing the Lightning Web Component (Crossbeam Copilot)
- Administrative Permissions
- Lightning Web Component (Crossbeam Copilot) Permissions:
- Custom Object Permissions:
- Placing the Lightning Web Component (Crossbeam Copilot)
- Frequently Asked Questions How can my team run reports on Crossbeam data? What are best practices for run reports on Crossbeam data? What should Crossbeam Ecosystem Overlap record pages look like? What are the custom object fields and what do they mean? How do I reauthorize the Salesforce Custom Object integration in Crossbeam? There's a Salesforce authorization error when connecting to Crossbeam. What Should I do?
- How can my team run reports on Crossbeam data?
- What are best practices for run reports on Crossbeam data?
- What should Crossbeam Ecosystem Overlap record pages look like?
- What are the custom object fields and what do they mean?
- How do I reauthorize the Salesforce Custom Object integration in Crossbeam?
- There's a Salesforce authorization error when connecting to Crossbeam. What Should I do?
Use this guide to understand how to install and configure the Crossbeam managed package for Salesforce, which includes "Crossbeam Copilot" (a Lightning Web Component) and "Crossbeam Ecosystem Overlap" (a custom object).

👋 Hello there! This guide is written for Salesforce Administrators / RevOps teams. You'll use this guide to install and configure Crossbeam's Salesforce integration.
RevOps Note on Setup Time
The estimated setup time for this integration is 1 hour for basic setup to 3 hours for more advanced setup . Please note that actual setup duration can vary based on your team’s configuration, customization needs, and overall account setup.

For a more accurate estimate or additional guidance, contact our Support team at support@crossbeam.com . <!-- VALIDATE-OK[person-address]: verbatim public Crossbeam Help Center text -->
The integration includes:
- A Lightning Web Component ( Crossbeam Copilot), placed on a variety of Salesforce Lightning pages to bring the partner ecosystem directly to your GTM teams.
- A custom object ( Crossbeam Ecosystem Overlap), which receives data from Crossbeam so your GTM teams can enrich Salesforce reports and dashboards with partner insights.
Get started by reviewing the overview and user requirements below.

Ready to upgrade from the Crossbeam Legacy Salesforce Integration v1 to v2? Click here to learn more.


#### What's in this guide?
- Install the managed package in Salesforce: to get the Lightning Web Component and custom object into your Salesforce environment. Then, hook it up to your Crossbeam account.
- Then, hook it up to your Crossbeam account.
- Configure the integration in Crossbeam: to choose the data that is pushed from Crossbeam to the Salesforce custom object and enable the push.
- Assign permission sets in Salesforce: to control who can access the component and/or the custom object.
- Place the component on Salesforce page layouts: to define where your team will go to see and interact with Crossbeam Copilot.

#### Crossbeam user requirements
You'll need a Crossbeam user seat with the following roles :
- Full Access Role: Admin
- Sales Role: Manager
Integration Seat users can now complete this setup without needing a Crossbeam user seat. Integration Seat is available on Supernode and Enterprise plans. Learn how to assign the Integration Seat in Managing User Seats and Roles in Crossbeam .
Review your seat assignment by visiting the Team page in the Crossbeam web app:

Keep your Crossbeam login credentials handy, you'll need them to authenticate the connection between Salesforce and Crossbeam!


#### Salesforce user requirements
You'll need some Salesforce permissions to be able to complete the installation. One is a permission set that comes with our managed package (called Crossbeam Setup User ), the others are standard Salesforce permissions for users configuring managed packages/integrations:
- Users setting up the Lightning Web Component (" Crossbeam Copilot" ) need: the Crossbeam Setup User permission assigned to their user profile
- the Crossbeam Setup User permission assigned to their user profile
- Users setting up the Custom Object ( "Crossbeam Ecosystem Overlap" ) need: Read access to the Account or Lead objects Note: An optional feature for pushing partner-shared data into custom fields on the Account object would require Write access Full access (Read, Create, Edit, Delete, View All Records, Modify All Records) to the Crossbeam Ecosystem Overlaps custom object
- Read access to the Account or Lead objects Note: An optional feature for pushing partner-shared data into custom fields on the Account object would require Write access
- Note: An optional feature for pushing partner-shared data into custom fields on the Account object would require Write access
- Full access (Read, Create, Edit, Delete, View All Records, Modify All Records) to the Crossbeam Ecosystem Overlaps custom object
For more details on managed packages, including required user permissions and installation types, review Salesforce's documentation " Install a Package ."


### Installing the managed package
Navigate to Crossbeam's Salesforce AppExchange listing and click the Get It Now button. If you are not already logged into the Salesforce instance you wish to install the package into, Salesforce will prompt you to log in. Once logged in:
- Select Install for Admins Only : this option allows for controlling access and permissions after the package has been installed.
- Then, click the Install button:
⚠️ if you select " Install for All Users," the permission sets that come with the managed package will not function properly: you won't be able to control exactly which users can see Crossbeam data and the actions they are able to take.
- Approve Third-Party Access by ticking the checkbox and clicking the Continue button:

Third-Party access must be approved to continue with the installation and use the Crossbeam Integration in Salesforce. The third-party access is used for:
- api.crossbeam.com - getting Crossbeam data
- api.segment.io - reporting on usage
- auth.crossbeam.com - authenticating your Crossbeam users
- login.salesforce.com - authenticating your Salesforce access for data
- sales-backend-api.crossbeam.com - getting Crossbeam for Sales data
- sentry.io - reporting on errors
- test.salesforce.com - sandbox testing

### Connecting to your Crossbeam account
Now that the package is successfully installed, you'll need to connect it to your Crossbeam account.


#### Assigning the "Crossbeam Setup User" permission set
The permission set named Crossbeam Setup User gets installed as part of the managed package. Be sure to assign it to yourself in order to complete the setup steps:


#### Accessing the Crossbeam Setup App
- Navigate to Salesforce App Launcher and search for "Crossbeam" to access the Crossbeam Setup App:

- Click the Get Started button:

#### Completing the Setup Steps
When completing the 3 setup steps outlined below, be sure to click the "Next" button until you see and click the final "Finish" button.


##### Step 1: Outbound Connection
This part of the Crossbeam Setup will validate access to your Crossbeam account and allow Crossbeam data to be viewed in Crossbeam Copilot. Have your Crossbeam login credentials handy.
- Click the Validate button:
- A new window will pop up asking for Crossbeam login credentials: Log in with your Crossbeam username and password (or click "Log in with Google" if you used Google as your auth method when registering your Crossbeam account). If your Crossbeam account has SSO enforced, be sure to log in as your SSO exception user .
- Log in with your Crossbeam username and password (or click "Log in with Google" if you used Google as your auth method when registering your Crossbeam account).
- If your Crossbeam account has SSO enforced, be sure to log in as your SSO exception user .
- Click the Next button:

##### Step 2: Crossbeam Organization Selection
If you successfully authenticated your Crossbeam account in the previous step, this screen will display the name of your Crossbeam account. Users with access to more than one Crossbeam account will see all of their accounts displayed.
- Select the Crossbeam account you are connecting to this Salesforce instance:
- Click the Next button.
You should see a successful System Connections screen:


### Configure Trusted URLs
For advanced functionality of Crossbeam Copilot such as access to the "Plays" and "Contacts" tabs, Crossbeam must be added as a New Trusted URL in Salesforce. This will allow Copilot to load resources contained in <iframe> elements from this specific trusted URL only.
- Navigate to Setup, click the Trusted URLs tab (under Security header) Click the New Trusted URL button: Complete the Trusted URL Information section with the following: API Name: Crossbeam URL: https://app.crossbeam.com Complete the CSP Settings section with the following: CSP Context: Lightning Experience Pages CSP Directives: frame-src (iframe content) Note: in some cases (e.g., if your Salesforce instance has "Adopt updated CSP directives" enabled) you will also need to add https://api.crossbeam.com as a trusted URL (iframe-src). Click the Save button.
- Click the New Trusted URL button:
- Complete the Trusted URL Information section with the following: API Name: Crossbeam URL: https://app.crossbeam.com
- API Name: Crossbeam
- URL: https://app.crossbeam.com
- Complete the CSP Settings section with the following: CSP Context: Lightning Experience Pages CSP Directives: frame-src (iframe content)
- CSP Context: Lightning Experience Pages
- CSP Directives: frame-src (iframe content)
- Note: in some cases (e.g., if your Salesforce instance has "Adopt updated CSP directives" enabled) you will also need to add https://api.crossbeam.com as a trusted URL (iframe-src).
- Click the Save button.
- Navigate to Crossbeam Setup to verify both System Connections and Configure Trusted URLs are marked as complete:


### Enable & Configure Push to Crossbeam Ecosystem Overlap Custom Object
❗️ Important
Enabling the data push will count toward your account's Record Export limit. The initial push when setting up this integration counts as your first export, and records will continue to count against your limit on each subsequent sync.
To understand your current limit and monitor usage, visit the Plan & Billing page . Learn more in Understanding Record Exports .

Navigate to the Crossbeam Web App and access the Integrations page .
- Find the "Salesforce Custom Object" tile and click the Install button:

- In the window that pops up, click New authentication :
- Click the Create button:
- A Crossbeam login window will appear, log in with your Crossbeam credentials.
- Click the Next button:
- Click New authentication:
- Click the Create button:
- A Salesforce login window will appear, log in with your Salesforce credentials. Click the Allow button.
- Click the Allow button.
- Click the Next button:
- In the previous steps in this installation guide, you installed the Salesforce package. No further action is required here. Click the Next button:
- Click the Finish button:
- On the following screen: (Optional) Customize what data is pushed: Review the "Customize Data in Push" section. By default, all your populations and all your partners' populations are selected. Remove any populations you do not want to push to Salesforce. Don't worry: you can change your mind - if you come back to this screen and de-select a population after it has already pushed in, it will be deleted from the custom object in Salesforce on the next sync cycle. Review the "Push opportunity data" setting. Turn this on to allow for more flexible reporting in Salesforce: when this setting is on, Crossbeam Ecosystem Overlap records will be created for every Opportunity with a partner overlap. This will allow your Salesforce users to run reports utilizing the Opportunity object and useful Opportunity fields. Keeping this off can help reduce volume of data being pushed in. ​ Slide the "Enable Data Push" toggle to ON then Click the Save Changes button:
- (Optional) Customize what data is pushed: Review the "Customize Data in Push" section. By default, all your populations and all your partners' populations are selected. Remove any populations you do not want to push to Salesforce. Don't worry: you can change your mind - if you come back to this screen and de-select a population after it has already pushed in, it will be deleted from the custom object in Salesforce on the next sync cycle. Review the "Push opportunity data" setting. Turn this on to allow for more flexible reporting in Salesforce: when this setting is on, Crossbeam Ecosystem Overlap records will be created for every Opportunity with a partner overlap. This will allow your Salesforce users to run reports utilizing the Opportunity object and useful Opportunity fields. Keeping this off can help reduce volume of data being pushed in. ​

##### (Optional) Customize what data is pushed:
- Review the "Customize Data in Push" section. By default, all your populations and all your partners' populations are selected. Remove any populations you do not want to push to Salesforce. Don't worry: you can change your mind - if you come back to this screen and de-select a population after it has already pushed in, it will be deleted from the custom object in Salesforce on the next sync cycle.
- Don't worry: you can change your mind - if you come back to this screen and de-select a population after it has already pushed in, it will be deleted from the custom object in Salesforce on the next sync cycle.
- Review the "Push opportunity data" setting. Turn this on to allow for more flexible reporting in Salesforce: when this setting is on, Crossbeam Ecosystem Overlap records will be created for every Opportunity with a partner overlap. This will allow your Salesforce users to run reports utilizing the Opportunity object and useful Opportunity fields. Keeping this off can help reduce volume of data being pushed in. ​
- Keeping this off can help reduce volume of data being pushed in. ​
- Slide the "Enable Data Push" toggle to ON then Click the Save Changes button:
Return to the Integrations page at any time to modify these settings:

Keep in mind that when you add new partners, or when partners share new Populations with you, additional records may push into the custom object.
Looking to push even more data to the Account object? See Enhanced Ecosystem Reporting: "is a customer of" & "is an opportunity for" Fields in Salesforce" to set up additional ecosystem fields.
✍️ Note
The Salesforce data push sync defaults to twice a day, every 12 hours . Actual update times may vary.


### Assigning permission sets
The Crossbeam managed package comes with a number of different permission sets so you can control exactly which users can see Crossbeam data and the actions they are able to take.
We recommend assigning "Crossbeam Account User" and "Crossbeam Report User" to your entire team. This allows them to interact with Crossbeam Copilot, and enrich Salesforce reports and dashboards using Crossbeam data.

#### Administrative Permissions:
- Crossbeam Setup User : full access for an administrator must be assigned to the user installing or reauthorizing the integration grants admin access to the Lightning Web Component (Crossbeam Copilot) grants write access to the "Crossbeam Ecosystem Overlap" custom object
- must be assigned to the user installing or reauthorizing the integration
- grants admin access to the Lightning Web Component (Crossbeam Copilot)
- grants write access to the "Crossbeam Ecosystem Overlap" custom object

#### Lightning Web Component (Crossbeam Copilot) Permissions:
- Crossbeam Account User : enables access to the Crossbeam Copilot Full Access: Users with a paid Crossbeam Core or Sales seat will have full access to the Crossbeam Copilot, including the ability to see data partners have shared. Starter Access: Users without a paid Crossbeam Core or Sales seat will see a high level overview.
- Full Access: Users with a paid Crossbeam Core or Sales seat will have full access to the Crossbeam Copilot, including the ability to see data partners have shared.
- Starter Access: Users without a paid Crossbeam Core or Sales seat will see a high level overview.
- Crossbeam Widget Viewer : grants access to Crossbeam Copilot but disables any clickable buttons users will not be able to access data shared by partners or initiate conversations
- grants access to Crossbeam Copilot but disables any clickable buttons
- users will not be able to access data shared by partners or initiate conversations

#### Custom Object Permissions:
- Crossbeam Report User : enables access to the custom object grants access to the "Crossbeam Ecosystem Overlap" custom object allows users to build Salesforce reports and dashboards with Crossbeam data
- grants access to the "Crossbeam Ecosystem Overlap" custom object
- allows users to build Salesforce reports and dashboards with Crossbeam data

### Placing the Lightning Web Component (Crossbeam Copilot)
The Crossbeam Copilot component may be placed on lightning page layouts for Account, Opportunity, Contact, and Lead records.
We recommend placing the Crossbeam Copilot on Account and Opportunity record pages, in a conspicuous location.
This example will show you how to place the Crossbeam Overlaps component on an account record page:
- Navigate to Setup, click the Object Manager tab (under Objects and Fields header) Click on Account Click on Lightning Record Pages Click Default Accounts (or the account record layout relevant to you) Click the Edit button
- Click on Account
- Click on Lightning Record Pages
- Click Default Accounts (or the account record layout relevant to you)
- Click the Edit button
- In the subsequent "Lightning App Builder" page, on the left hand navigation bar, scroll down to the "Custom - Managed" section
- Click and drag the Crossbeam Copilot component, placing it in the desired location on your page layout:

- Click Activation -> Set as Org Default -> Save
Consider adding visibility filters to the component if you don't want it to appear on the page for certain user roles, for example. More on component visibility here .

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

❗️ Important
This integration has been updated, and the guide below will no longer be maintained.
For detailed steps to install Crossbeam for Salesforce (v2), please click here .

Use this guide to understand how to install and configure the Crossbeam managed package for Salesforce, which includes "Crossbeam Copilot" (a Lightning Web Component) and "Crossbeam Overlap" (a custom object).

👋 Hello there! This guide is written for Salesforce Administrators / RevOps teams. You'll use this guide to install and configure Crossbeam's Salesforce integration.

The integration includes:
- A Lightning Web Component ( Crossbeam Copilot), placed on a variety of Salesforce Lightning pages to bring the partner ecosystem directly to your GTM teams.
- A custom object ( Crossbeam Overlap), which receives data from Crossbeam so your GTM teams can enrich Salesforce reports and dashboards with partner insights.
Get started by reviewing the overview and user requirements below.


#### What's in this guide?
- Install the managed package in Salesforce: to get the Lightning Web Component and custom object into your Salesforce environment. Then, hook it up to your Crossbeam account.
- Then, hook it up to your Crossbeam account.
- Configure the integration in Crossbeam: to choose the data that is pushed from Crossbeam to the Salesforce custom object and enable the push.
- Assign permission sets in Salesforce: to control who can access the component and/or the custom object.
- Place the component on Salesforce page layouts: to define where your team will go to see and interact with Crossbeam Copilot.

#### Crossbeam user requirements
You'll need a Crossbeam user seat with the following roles :
- Full Access Role: Admin
- Sales Role: Manager
Review your seat assignment by visiting the Team page in the Crossbeam web app:

Keep your Crossbeam login credentials handy, you'll need them to authenticate the connection between Salesforce and Crossbeam!


#### Salesforce user requirements
You'll need some Salesforce permissions to be able to complete the installation. One is a permission set that comes with our managed package (called Crossbeam Setup User ), the others are standard Salesforce permissions for users configuring managed packages/integrations:
- Users setting up the Lightning Web Component (" Crossbeam Copilot" ) need: the Crossbeam Setup User permission assigned to their user profile
- the Crossbeam Setup User permission assigned to their user profile
- Users setting up the Custom Object ( "Crossbeam Overlap" ) need: the Crossbeam Setup User permission assigned to their user profile Visualforce Page Access enabled Read access to the Account and Lead objects
- the Crossbeam Setup User permission assigned to their user profile
- Visualforce Page Access enabled
- Read access to the Account and Lead objects
For more details on managed packages, including required user permissions and installation types, review Salesforce's documentation " Install a Package ."


### Installing the managed package
Navigate to Crossbeam's Salesforce AppExchange listing and click the Get It Now button. If you are not already logged into the Salesforce instance you wish to install the package into, Salesforce will prompt you to log in. Once logged in:
- Select Install for Admins Only : this option allows for controlling access and permissions after the package has been installed.
- Then, click the Install button:
⚠️ if you select " Install for All Users," the permission sets that come with the managed package will not function properly: you won't be able to control exactly which users can see Crossbeam data and the actions they are able to take.
- Approve Third-Party Access by ticking the checkbox and clicking the Continue button:
Third-Party access must be approved to continue with the installation and use the Crossbeam Integration in Salesforce. The third-party access is used for:
- api.crossbeam.com - getting Crossbeam data
- api.segment.io - reporting on usage
- auth.crossbeam.com - authenticating your Crossbeam users
- login.salesforce.com - authenticating your Salesforce access for data
- sales-backend-api.crossbeam.com - getting Crossbeam for Sales data
- sentry.io - reporting on errors
- test.salesforce.com - sandbox testing


### Connecting to your Crossbeam account
Now that the package is successfully installed, you'll need to connect it to your Crossbeam account.


#### Assigning the "Crossbeam Setup User" permission set
The permission set named Crossbeam Setup User gets installed as part of the managed package. Be sure to assign it to yourself in order to complete the setup steps:


#### Accessing the Crossbeam Setup App
- Navigate to Salesforce App Launcher and search for "Crossbeam" to access the Crossbeam Setup App:

- Click the Get Started button:


#### Completing the Setup Steps
When completing the 3 setup steps outlined below, be sure to click the "Next" button until you see and click the final "Finish" button.


##### Step 1: Outbound Connection
This part of the Crossbeam Setup will validate access to your Crossbeam account and allow Crossbeam data to be viewed in Crossbeam Copilot. Have your Crossbeam login credentials handy.
- Click the Validate button:

- A new window will pop up asking for Crossbeam login credentials: Log in with your Crossbeam username and password (or click "Log in with Google" if you used Google as your auth method when registering your Crossbeam account). If your Crossbeam account has SSO enforced, be sure to log in as your SSO exception user .
- Log in with your Crossbeam username and password (or click "Log in with Google" if you used Google as your auth method when registering your Crossbeam account).
- If your Crossbeam account has SSO enforced, be sure to log in as your SSO exception user .
- Click the Next button:


##### Step 2: Crossbeam Organization Selection
If you successfully authenticated your Crossbeam account in the previous step, this screen will display the name of your Crossbeam account. Users with access to more than one Crossbeam account will see all of their accounts displayed.
- Select the Crossbeam account you are connecting to this Salesforce instance:
- Click the Next button.

##### Step 3: Inbound Connection
This part of the Crossbeam Setup will generate a refresh token that allows Crossbeam to share information with your Salesforce organization.
- Click the Authorize button:

- A new Salesforce approval window may pop up. If so, click to approve/confirm. Make sure the connection status changes from "Not Connected" to "Connected."
- Make sure the connection status changes from "Not Connected" to "Connected."
⚠️ If you are using an Integration User, make sure you are logged in directly. If you use Salesforce's "login as" functionality, an Insufficient Privileges error will display.
- Click the Finish button:

You should see a successful System Connections screen:


### Configure Trusted URLs
For advanced functionality of Crossbeam Copilot such as access to the "Plays" and "Contacts" tabs, Crossbeam must be added as a New Trusted URL in Salesforce. This will allow Copilot to load resources contained in <iframe> elements from this specific trusted URL only.
- Navigate to Setup, click the Trusted URLs tab (under Security header) Click the New Trusted URL button:
- Click the New Trusted URL button:
- Complete the Trusted URL Information section with the following: API Name: Crossbeam URL: https://app.crossbeam.com
- API Name: Crossbeam
- URL: https://app.crossbeam.com
- Complete the CSP Settings section with the following: CSP Context: Lightning Experience Pages CSP Directives: frame-src (iframe content)
- CSP Context: Lightning Experience Pages
- CSP Directives: frame-src (iframe content)
- Click the Save button.
- Navigate to Crossbeam Setup to verify both System Connections and Configure Trusted URLs are marked as complete:


### Enable & Configure Push to Crossbeam Overlap Custom Object
Navigate to the Crossbeam Web App and access the Integrations page .
- Scroll down to the "Installed Integrations" section and click the Settings button on the Salesforce Custom Object tile :
- On the following screen, toggle Enable Push ON :
- Expand the "My Data" and "Partner Data" sections to filter out any data you don't want to push over to the Salesforce custom object:
- Finally, click the Save button. Data will push at your next data sync cycle.
Return to the Integrations page at any time to modify these settings:

Keep in mind that when you add new partners, or when partners share new populations with you, additional records may push into the custom object.


### Assigning permission sets
The Crossbeam managed package comes with a number of different permission sets so you can control exactly which users can see Crossbeam data and the actions they are able to take.
We recommend assigning "Crossbeam Account User" and "Crossbeam Report User" to your entire team. This allows them to interact with Crossbeam Copilot, and enrich Salesforce reports and dashboards using Crossbeam data.

#### Administrative Permissions:
- Crossbeam Setup User : full access for an administrator must be assigned to the user installing or reauthorizing the integration grants admin access to the Lightning Web Component (Crossbeam Copilot) grants write access to the "Crossbeam Ecosystem Overlap" custom object
- must be assigned to the user installing or reauthorizing the integration
- grants admin access to the Lightning Web Component (Crossbeam Copilot)
- grants write access to the "Crossbeam Ecosystem Overlap" custom object

#### Lightning Web Component (Crossbeam Copilot) Permissions:
- Crossbeam Account User : enables access to the Crossbeam Copilot Full Access: Users with a paid Crossbeam Core or Sales seat will have full access to the Crossbeam Copilot, including the ability to see data partners have shared. Starter Access: Users without a paid Crossbeam Core or Sales seat will see a high level overview.
- Full Access: Users with a paid Crossbeam Core or Sales seat will have full access to the Crossbeam Copilot, including the ability to see data partners have shared.
- Starter Access: Users without a paid Crossbeam Core or Sales seat will see a high level overview.
- Crossbeam Widget Viewer : grants access to Crossbeam Copilot but disables any clickable buttons users will not be able to access data shared by partners or initiate conversations
- grants access to Crossbeam Copilot but disables any clickable buttons
- users will not be able to access data shared by partners or initiate conversations

#### Custom Object Permissions:
- Crossbeam Report User : enables access to the custom object grants access to the "Crossbeam Ecosystem Overlap" custom object allows users to build Salesforce reports and dashboards with Crossbeam data
- grants access to the "Crossbeam Ecosystem Overlap" custom object
- allows users to build Salesforce reports and dashboards with Crossbeam data

### Placing the Lightning Web Component (Crossbeam Copilot)
The Crossbeam Copilot component may be placed on lightning page layouts for Account, Opportunity, Contact, and Lead records.
We recommend placing the Crossbeam Copilot on Account and Opportunity record pages, in a conspicuous location.
This example will show you how to place the Crossbeam Overlaps component on an account record page:
- Navigate to Setup, click the Object Manager tab (under Objects and Fields header) Click on Account Click on Lightning Record Pages Click Default Accounts (or the account record layout relevant to you) Click the Edit button
- Click on Account
- Click on Lightning Record Pages
- Click Default Accounts (or the account record layout relevant to you)
- Click the Edit button
- In the subsequent "Lightning App Builder" page, on the left hand navigation bar, scroll down to the "Custom - Managed" section
- Click and drag the Crossbeam Copilot component, placing it in the desired location on your page layout:
- Click Activation -> Set as Org Default -> Save
Consider adding visibility filters to the component if you don't want it to appear on the page for certain user roles, for example. More on component visibility here .


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
