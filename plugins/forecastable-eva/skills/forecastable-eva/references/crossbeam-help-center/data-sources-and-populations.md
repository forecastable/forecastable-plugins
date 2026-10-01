# Collection: Data Sources And Populations

Source: https://help.crossbeam.com/en/collections/1845457-data-sources-and-populations. Captured September 30th, 2026.


## Overview (HC 10055030)
URL: https://help.crossbeam.com/en/articles/10055030-connecting-pipedrive-as-a-data-source

In this article:
- Overview
- Connecting Your Data Source
- Sync Data Options
- How to Customize Data Sync Fields
- Adjust Settings
- How Crossbeam Matches Pipedrive Records

Integrating Pipedrive as a data source streamlines data management, eliminating the need for manual CSV or Google Sheet updates. This integration allows you to pull fields directly from Pipedrive, ensuring only the most relevant data is shared in your Crossbeam account.
❗️ Important
Pipedrive as a data source is available on all Crossbeam plans.
Pipedrive as a data source does not include Copilot or pushing custom objects to Pipedrive. To upgrade your account, visit the Plan & Billing page .

To establish this connection, you must be a Crossbeam Admin. Learn more about user seats and roles in Crossbeam here .

### Connecting your Data Source
Click on Data from the navigation menu and select Data Sources for the dropdown options.
Scroll down and select Connect Pipedrive .

In the modal, select Connect Pipedrive to open the authorization window.

Review the permissions, then click Allow and Install . Wait for the connection to establish, and you’ll be redirected to Crossbeam.
REMINDER : At this stage, no data is shared; this step only syncs your selected data with Crossbeam. Later, you will be able to decide what to share (or not share) with your partners.

### Sync Data Options
Once Pipedrive is connected to Crossbeam, choose from the following sync options:
- Recommended : the best option for unlocking value from our full range of features
- Custom: Define a custom select of your data
Hover over each option to see the field names.

After selecting your syncing option, you will be prompted to review the fields. You can click Sync Now or Customize .

### How to Customize Data Sync Fields
How to Customize Sync Fields:
- From the Review Fields modal, click Customize
- In the next window, expand any table under All Data by clicking the drop-down arrow, or use the search bar to locate specific fields
- Select or deselect any of the fields to customize your data You can also click the Toggle button to turn entire tables on or off
- You can also click the Toggle button to turn entire tables on or off
- Click Review Fields, then select Sync Now to complete the connection
- Or click Go Back to edit your changes before completing the sync


#### Data Presets
Data Presets allow you to quickly add data that corresponds to direct use cases and Crossbeam functionality. After clicking the Customize button, Data Presets are located on the left side, highlighted in blue:
| Account Mapping: Compare your data with partners to identify overlapping prospects, opportunities, and customers | Pipeline Map: Accelerate opportunities and forecast revenue more accurately with more visibility into your partner's pipeline |
| Co-Market: Target overlapping prospects, opportunities, and customers for your better together stories and integration outreach | Co-Sell: Use your partner ecosystem to surface pre-vetted overlapping accounts that can shorten sales cycles and increase opportunity sizes |
Hover over the options to see the list of fields required.

After customizing your syncing option, click on Review fields . Confirm the sync by clicking on, Sync Now .
On the Data Sources workspace, the Pipedrive row will show Setting up while the sync processes. Once the sync is complete, you will see Pipedrive listed as Active .

You’ll receive an email confirmation once the sync is complete. You can then move on to creating your Populations .

### Adjust Settings
On the Data Sources workspace, hover over the three dots at the end of the Pipedrive row to reveal the Settings button. Click on Settings to:
- View Connection Status and Details: Check the connection status, error messages, and reauthorization requirements Reauthorization may be needed if user access or permissions have changed, and any errors will display here when available
- Reauthorization may be needed if user access or permissions have changed, and any errors will display here when available
- Adjust Data Sync Frequency : Use the Update Frequency dropdown to select how often Crossbeam syncs with Pipedrive
- Edit Data Sync: Click Edit Data Sync to open the Customize pop-up, allowing you to add or remove specific fields
- Remove Data Source: Select Remove Data Source to disconnect Pipedrive from Crossbeam

When finished, select Save Changes to apply your updates.

### How Crossbeam Matches Pipedrive Records
Pipedrive does not require a website field on organization records. To ensure account matching works correctly, Crossbeam generates a website value for each record using the primary contact email address domain.

This field appears as Crossbeam Generated Website in your field mapping and population builder. It is not syncing from your Pipedrive CRM, it is created by Crossbeam so the matching engine can function properly.

🎓 Sign into Crossbeam Academy to further explore Salesforce as a Data Source!
- Connecting Salesforce as a Data Source
- Connect HubSpot Data
- What are Data Sources?
- Salesforce as a Data Source FAQs
- Connect Databricks as a Data Source


## Overview (HC 12399814)
URL: https://help.crossbeam.com/en/articles/12399814-population-types-for-custom-populations

In this article:
- Overview Why this matters Available Population Types Who can edit Population Types
- Why this matters
- Available Population Types
- Who can edit Population Types
- FAQ
Custom Populations let you segment your data however you want in Crossbeam.
For example:
- Customers - EMEA
- Open Opportunities - Enterprise
You're now able to give every Custom Population a standard type : Customers, Open Opportunities, Prospects, or Other . ​ By assigning standard types, Crossbeam can automatically recognize what each Population represents, so your data flows into all the right places across the platform. That means a clearer view in the Account Mapping Matrix, Reports, Deal Navigator, Performance Dashboard, and more. ​
Starting November 6, you’ll see all your populations grouped by standard type, making it easier to understand your ecosystem and overlaps.
✍️ Note
New to Custom Populations? Learn how to create them in this article .
Auto-assigned types for existing Populations ​
We have auto-assigned standard types to your existing Custom Populations using keyword matching (for example: Customers - NA → Customers ).

You can review and adjust these assignments anytime.
👉 Review your Population types to make sure everything is categorized correctly.
​ This will not affect your Record Exports.

#### Why this matters
Your data works harder for you. All of your Populations, not just the standard ones, now count toward key features like reports, dashboards, and CRM sync. ​
No more blind spots. If you’ve been using Custom Populations for customers, opportunities, or prospects, they’ll now be included everywhere that data matters. ​
Accurate, complete insights. Overlap numbers and partner views reflect the full picture of your ecosystem. ​
Flexible, but consistent. Split customers by region, segment, or business line, they’ll all roll up under the right type, ensuring consistency without losing detail.


#### Available Population Types
When creating a Custom Population, you’ll assign one of these standard types:
- Customers
- Open Opportunities
- Prospects
- Other, for Populations that don’t fit into the above categories (e.g., “Partners,” “Closed Lost”)
If your Population name contains words like “Customer,” “Prospect,” or “Opp,” Crossbeam will automatically suggest a type for you.

#### Who can edit Population Types
- Admins (or users who can create/edit Populations) can assign or update a type.
- All users can view the assigned type.

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


## Overview (HC 14827573)
URL: https://help.crossbeam.com/en/articles/14827573-how-to-build-a-product-based-population-using-product2

In this article:
- Overview
- Plan Availability
- How It Works
- Steps to Build a Product-Based Population
- Related Articles
Product-based Populations let you segment accounts in Crossbeam by the products those accounts have purchased. Once you've synced Product2 data from Salesforce and configured your field mapping, you can build a custom Population that identifies all accounts associated with a specific product. This gives you a clear, shareable view of your customer base by product line.
✍️ Note This feature requires Salesforce as your data source and is not currently available for other CRMs.

You must have Product2 and Opportunity Line Item synced and your Product Line Type field mapped before building a product-based population.

See How to Sync Product Line Support (Product2) into Crossbeam to complete setup first.

### Plan Availability
| | Free | Connector | Supernode | Enterprise |
| Use Product2 in Standard Populations | ✓ | ✓ | ✓ | ✓ |
| Use Product2 in Custom Populations |, | ✓ | ✓ | ✓ |

### How It Works
Populations in Crossbeam are built around accounts . When you sync Product2 from Salesforce, Crossbeam makes product data available as a filter when building custom Populations. This allows you to build a Population of accounts associated with a specific product based on their closed-won opportunities, making it ideal for building a Customer Population.

### Steps to Build a Product-Based Population
Step 1: Navigate to Populations
- Click Data from the left-hand navigation and select Populations from the dropdown
- Click the Create Population button to open the Population Builder

Step 2: Name your Population and select a type
- Enter a descriptive name (e.g., Advanced Security Module, Customers )
- Under Population Type, select Customers
- Under Data Source, select Salesforce
- Under Object, select Accounts
- Add an optional description
- Click Continue

✍️ Note Selecting Customers for Population type ensures this Population is recognized across Crossbeam features like the Account Mapping Matrix, Deal Navigator, and Performance Dashboard.

See Population Types for Custom Populations to learn more.
Step 3: Add a Product2 filter
- Click Add Filter
- Under the Product2 filter group, select Product Name or Product ID
- Set the operator to is and enter the product value you want to filter by
Step 4: Filter to Closed opportunities
- Click Add Filter
- Search for Closed ; this field is listed under Opportunity
- Set the value to true
Step 5: Filter to Won opportunities
- Click Add Filter
- Search for Won; this field is listed under Opportunity
- Set the value to true
- Confirm the logic for both filters reads where Closed is true and where Won is true
- Click Apply Filters to preview the accounts in this Population
Step 6: Create your Population
- Review the previewed accounts to confirm the results look correct
- Click Create Population

Related Articles
- How to Sync Product Line Support (Product2) into Crossbeam
- Custom Populations
- Population Types for Custom Populations
- Managing Population Settings
- Build a Standard Population
- What are Populations?
- Custom Populations
- Installation Guide: Crossbeam for Salesforce (v2)
- How to Sync Product Line Support (Product2) into Crossbeam


## Overview (HC 15231542)
URL: https://help.crossbeam.com/en/articles/15231542-connect-databricks-as-a-data-source

In this article:
- Overview
- Plan Availability
- Prerequisites Creating the Service Principal
- Creating the Service Principal
- Step 1: Create the Catalog and Schema
- Step 2: Create the Source Tables
- Step 3: Grant the Service Principal Read Access
- Step 4: Connect from Crossbeam
- Supported Features
- Supported Column Types
- Limitations
- Manage Databricks Connection

Databricks as a Data Source pulls account, contact, deal, lead, and user data from your Databricks workspace into Crossbeam. Once connected, Crossbeam uses this data to generate partner overlaps.

Crossbeam integrates with Databricks in two directions: this article covers the Data Source (Pull), which syncs your data into Crossbeam. You can also use Databricks Integration (Push) to send partner overlaps back into your Databricks workspace. Both are independent and can point to different catalogs and schemas.
👀 Looking to push Crossbeam overlap data back into Databricks?
See Databricks Integration .

### Plan Availability
| | Free | Connector | Supernode | Enterprise |
| Connect Databricks as a Data Source | ✅ | ✅ | ✅ | ✅ |

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
✍️ Note
If you plan to enable both the Databricks as a Data Source and Databricks Integration, you can use the same Service Principal for both.

### Step 1: Create the Catalog and Schema
Create a dedicated catalog and schema for the data you're sharing with Crossbeam. You can reuse existing objects, but most customers create a dedicated crossbeam schema.

CREATE CATALOG IF NOT EXISTS crossbeam_share;CREATE SCHEMA IF NOT EXISTS crossbeam_share.crm;
💡 Check out these Databricks resources if you need help with creating a catalog and creating a schema .

### Step 2: Create the Source Tables
The only required table is accounts . Add other tables only if they're relevant to your use case. Crossbeam will automatically discover any extra columns you add and surface them as fields in the UI.

About the users table: This table holds your CRM users, the record owners behind accounts, deals, and leads. It powers AE-attribution features in Crossbeam. To set it up, add an owner_id STRING column to your accounts, deals, and/or leads tables that references users.id .

Add an optional is_deleted BOOLEAN column to any table to enable soft-delete detection. When rows are flagged as deleted, Crossbeam removes them from your overlaps.

-- REQUIRED: accountsCREATE TABLE IF NOT EXISTS crossbeam_share.crm.accounts ( id STRING NOT NULL, name STRING, website STRING, duns_number STRING, owner_id STRING, is_deleted BOOLEAN, updated_at TIMESTAMP NOT NULL) USING DELTA;-- OPTIONAL: contactsCREATE TABLE IF NOT EXISTS crossbeam_share.crm.contacts ( id STRING NOT NULL, name STRING, email STRING, account_id STRING, is_deleted BOOLEAN, updated_at TIMESTAMP NOT NULL) USING DELTA;-- OPTIONAL: dealsCREATE TABLE IF NOT EXISTS crossbeam_share.crm.deals ( id STRING NOT NULL, account_id STRING, amount DECIMAL(18,2), owner_id STRING, is_deleted BOOLEAN, updated_at TIMESTAMP NOT NULL) USING DELTA;-- OPTIONAL: leadsCREATE TABLE IF NOT EXISTS crossbeam_share.crm.leads ( id STRING NOT NULL, email STRING, owner_id STRING, is_deleted BOOLEAN, updated_at TIMESTAMP NOT NULL) USING DELTA;-- OPTIONAL: usersCREATE TABLE IF NOT EXISTS crossbeam_share.crm.users ( id STRING NOT NULL, email STRING NOT NULL, name STRING, phone STRING, title STRING, is_deleted BOOLEAN, updated_at TIMESTAMP NOT NULL) USING DELTA;

✍️ Note
Every table must include id (STRING) and updated_at (TIMESTAMP) for incremental syncs to work.

### Step 3: Grant the Service Principal Read Access
Replace crossbeam-sp with the display name or UUID of your Service Principal.

GRANT USE CATALOG ON CATALOG crossbeam_share TO `crossbeam-sp`;GRANT USE SCHEMA ON SCHEMA crossbeam_share.crm TO `crossbeam-sp`;GRANT SELECT ON SCHEMA crossbeam_share.crm TO `crossbeam-sp`;
To grant access table-by-table instead of schema-wide:

GRANT SELECT ON TABLE crossbeam_share.crm.accounts TO `crossbeam-sp`;GRANT SELECT ON TABLE crossbeam_share.crm.contacts TO `crossbeam-sp`;-- … etc.


### Step 4: Connect from Crossbeam
- In Crossbeam, navigate to Data Sources → click the Databricks tile

Enter the following when prompted:
| Field | Value |
| Server hostname | From SQL Warehouse → Connection Details |
| HTTP path | From SQL Warehouse → Connection Details |
| Catalog | crossbeam_share |
| Schema | crm |
| Client ID | Service Principal Application ID |
| Client Secret | OAuth client secret from the Service Principal |
Click Connect .

Crossbeam will:
- Connect using your Service Principal credentials
- Verify the required accounts table is present
- Discover all other tables and columns
- Validate required field types
Once connected, the initial sync starts automatically. Subsequent syncs are incremental and run against the updated_at column.

### Supported Features
| Feature | Details |
| Authentication | OAuth M2M (Service Principal client_id and client_secret ) |
| Supported objects | accounts (required), contacts, deals, leads, users |
| Incremental sync | Yes, bookmarked on updated_at |
| Full re-sync | Yes, resets the bookmark |
| Soft-delete detection | Yes, opt-in via an is_deleted boolean column |
| Preview sync | Yes, last 10,000 records ordered by updated_at DESC |
| Discovery | Automatic via INFORMATION_SCHEMA.TABLES and INFORMATION_SCHEMA.COLUMNS |
| Per-org record limit | Yes, contact support if exceeded |

### Supported Column Types
| Databricks Type | Mapped To |
| STRING, VARCHAR, CHAR | Text |
| INT, BIGINT, SMALLINT, TINYINT, FLOAT, DOUBLE, DECIMAL, NUMERIC, REAL | Number |
| DATE, TIMESTAMP, TIMESTAMP_NTZ, TIMESTAMP_LTZ | Timestamp (with time zone) |
| BOOLEAN | Boolean |
| ARRAY, MAP, STRUCT, INTERVAL, BINARY | Not supported, column will be skipped |
✍️ Note
The deals.amount column is treated as a money type. Complex types ( ARRAY, MAP, STRUCT, INTERVAL, BINARY ) are not supported, flatten them into separate columns or views if you need to share them.

### Limitations
- Authentication: Service Principal OAuth M2M only. Personal access tokens and interactive OAuth are not supported.
- Required table: The accounts table is mandatory. The connection cannot be enabled without it.
- Required columns: Every table must include id (STRING) and updated_at (TIMESTAMP) for incremental syncs to work.
- Unsupported types: Complex Databricks types ( ARRAY, MAP, STRUCT, INTERVAL, BINARY ) are skipped.

### Managed Databricks Connection
In Crossbeam, navigate to Data Sources → click the Settings icon next to your Databricks connection.

From here you select:
- General : Adjust how and when Crossbeam syncs data from your Databricks workspace, check the status of the integration, and see connection details
- Field Sync : Control which individual fields are pulled into Crossbeam from Databricks
- Field Presets : Create a custom set of fields to control which data is shared with partners. Learn more about Using Data Sharing Presets in Crossbeam
- Learn more about Using Data Sharing Presets in Crossbeam
- Field Mapping: Map your Databricks workspace as the data source, establish your opportunity fields, and set your product line type field. Learn more about How to Sync Product Line Support (Product2) into Crossbeam
- Learn more about How to Sync Product Line Support (Product2) into Crossbeam
- Click Remove data source to delete it from your Crossbeam account

Click Save when done managing your settings.
Related Articles
- Databricks Integration
- Connect HubSpot Data
- Connect Snowflake Data
- Data Sources Overview: CSVs, CRMs and Data Warehouses
- Databricks Integration


## Video Tutorial (HC 3160182)
URL: https://help.crossbeam.com/en/articles/3160182-connecting-salesforce-as-a-data-source

Learn how to connect your Salesforce data to Crossbeam.

In this article:
- Video Tutorial
- Connecting your Data Source
- Syncing Data Options
- How to Customize Sync Fields Data Presets
- Data Presets
- Adjust Data Settings
Watch this video or keep reading to learn how to connect Salesforce:

❗️ Important
The user setting up Salesforce as a data source for Crossbeam will need to meet the requirements below, or the connection will fail.


### Crossbeam user requirements
You'll need a Crossbeam user seat with the following roles :
- Full Access Role: Admin
Review your seat assignment by visiting the Team page in the Crossbeam web app:


### Salesforce user requirements

#### Administrative Permissions
| Permission | Required? |
| API Enabled | Required |
| View All Users | Optional |
| View Setup and Configuration | Optional |


#### Object Permissions
| Object | Access | Required? |
| Account | Read | Required |
| Contact | Read | Optional |
| Lead | Read | Optional |
| Opportunity | Read | Optional |
| User | Read | Optional |
✍️ Note
Read access to Account OR Lead objects is required: if only syncing Lead object, Account is not required .

#### Field Permissions:
-Id, Owner Id (for identifying records).
-Name, Website (for matching algorithm to find overlaps).
-IsDeleted, SystemModstamp, CreatedAt (for record-level bookkeeping).

By Object

Account : Account ID, Account Name, Account Website, Owner ID
Contact : Account ID, Contact Email, Contact ID
Lead : Lead Email, Lead ID, Owner ID
Opportunity : Account ID, Opportunity ID
Opportunity Contact Role : Contact ID, Contact Role ID, Opportunity ID, Primary, Role
User : Account Owner Email, User ID

Note: These are the “bare minimum” fields required for Crossbeam to function. Your Partnerships team and GTM end-users may need additional fields in order to achieve their specific goals and use cases.

### Connecting your Data Source
- Click on Data from the navigation bar, then select Data Sources from the dropdown
- Scroll to the Salesforce tile and click on Salesforce
- You'll have an option to Connect to Sandbox or Connect to Salesforce to go straight to production

✍️ Note
Connecting Salesforce as a Data Source requires OAuth authentication.

### Syncing Data Options
Once Salesforce is connected to Crossbeam, choose from the following sync options:
- Recommended : the best option for unlocking value from our full range of features
- Custom: Define a custom select of your data
Hover over each option to see the field names.

After selecting your syncing option, you will be prompted to review the fields. You can click Sync Now or Customize .


### How to Customize Sync Fields
- How to Customize Sync Fields: From the data source Salesforce Settings, click Field Sync >Edit In the next window, expand any table under All Data by clicking the drop-down arrow, or use the search bar to locate specific fields Select or deselect any of the fields to customize your data You can also click the Toggle button to turn entire tables on or off Click Review Fields, then select Sync Now to complete the connection Or click Go Back to edit your changes before completing the sync
- From the data source Salesforce Settings, click Field Sync >Edit
- In the next window, expand any table under All Data by clicking the drop-down arrow, or use the search bar to locate specific fields
- Select or deselect any of the fields to customize your data You can also click the Toggle button to turn entire tables on or off
- You can also click the Toggle button to turn entire tables on or off
- Click Review Fields, then select Sync Now to complete the connection
- Or click Go Back to edit your changes before completing the sync


#### Data Presets
Data Presets allow you to quickly add data that corresponds to direct use cases and Crossbeam functionality. After clicking the Customize button, Data Presets are located on the left side, highlighted in blue. Select from the following preset data field options:
| Account Mapping: Compare your data with partners to identify overlapping prospects, opportunities, and customers | Pipeline Map: Accelerate opportunities and forecast revenue more accurately with more visibility into your partner's pipeline |
| Co-Market: Target overlapping prospects, opportunities, and customers for your better together stories and integration outreach | Co-Sell: Use your partner ecosystem to surface pre-vetted overlapping accounts that can shorten sales cycles and increase opportunity sizes |
| Refer : Give and get warm introductions into your target accounts with insights into partner overlaps | |
Hover over the options to see the list of fields required. When ready, simply click the option you want and Crossbeam will do the rest.

### Adjust Data Settings
On the Data Sources workspace, hover over the three dots at the end of the Salesforce row to reveal the Settings button.

Click on Settings to:
- View Connection Status and Details: Check the connection status, error messages, and reauthorization requirements Reauthorization may be needed if user access or permissions have changed, and any errors will display here when available
- Reauthorization may be needed if user access or permissions have changed, and any errors will display here when available
- Adjust Data Sync Frequency : Use the Update Frequency dropdown to select how often Crossbeam syncs with Salesforce
- Edit Data Sync: Click Edit Data Sync to open the Customize pop-up, allowing you to add or remove specific fields
- Remove Data Source: Select Remove Data Source to disconnect Salesforce from Crossbeam

✍️ Note
You'll also get email confirmation when the sync is complete. You can then move on to creating your dynamic Standard Populations .
🎓 Sign into Crossbeam Academy to further explore Salesforce as a Data Source!
📄 Related Articles
- Manage your Connection
- Troubleshoot your Connection
- Salesforce as a Data Source FAQs

- Connect HubSpot Data
- Salesforce as a Data Source FAQs
- Attribution for Salesforce Users
- Connecting Pipedrive as a Data Source
- Connect Databricks as a Data Source


## Connect your Data Source (HC 3160183)
URL: https://help.crossbeam.com/en/articles/3160183-connect-hubspot-data

In this article:
- Connect your Data Source
- Sync Data Options
- How to Customize Sync Fields Data Presets
- Data Presets
- Adjust Data Settings
Ready to unlock your HubSpot data? Kick off your HubSpot training in Crossbeam Academy.

Learn how to connect your HubSpot data to Crossbeam.

Visual learner? Click on the video tutorial below:

- Click Data from the navigation menu, select Data Sources from the drop-down options
- Click on HubSpot tile
- In the pop-up, click Connect HubSpot to confirm that you would like to create a HubSpot connection. Next, confirm the account you are authorizing in HubSpot as a data source and click Connect App

❗️ Important
To complete the HubSpot connection, you must have Super Admin permissions and Marketplace Access in HubSpot.

### Sync Data Options
Once HubSpot is connected to Crossbeam, choose from the following sync options:
- Recommended : the best option for unlocking value from our full range of features
- Custom: Define a custom select of your data
Hover over each option to see the field names.

After selecting your syncing option, you will be prompted to review the fields. You can click Sync Now or Customize within the options.


#### Mandatory Fields to Sync
- Companies : Company ID, Company name, Owner ID, Website URL

#### Recommended Fields to Sync
- Companies : Lifecycle Stage
- Contacts : Contact ID, Email, Primary Associated Company ID
- Deal Contact Associations : Contact ID, Deal ID, ID, Label
- Deals : Deal ID, Deal Stage, Deal Stage ID, Pipeline, Pipeline ID
- Owners : Account Owner Email, Owner ID

### How to Customize Sync Fields
- How to Customize Sync Fields: From the data source HubSpot Settings, click Field Sync >Edit Expand any table under All Data by clicking the drop-down arrow, or use the search bar to locate specific fields Select or deselect any of the fields to customize your data You can also click the Toggle button to turn entire tables on or off Click Review Fields, then select Sync Now to complete the connection Or click Go Back to edit your changes before completing the sync
- From the data source HubSpot Settings, click Field Sync >Edit
- Expand any table under All Data by clicking the drop-down arrow, or use the search bar to locate specific fields
- Select or deselect any of the fields to customize your data You can also click the Toggle button to turn entire tables on or off
- You can also click the Toggle button to turn entire tables on or off
- Click Review Fields, then select Sync Now to complete the connection
- Or click Go Back to edit your changes before completing the sync


#### Data Presets
Data Presets allow you to quickly add data that corresponds to direct use cases and Crossbeam functionality. After clicking the Customize button, Data Presets are located on the left side, highlighted in blue. Select from the following preset data field options:
| Account Mapping: Compare your data with partners to identify overlapping prospects, opportunities, and customers | Pipeline Map: Accelerate opportunities and forecast revenue more accurately with more visibility into your partner's pipeline |
| Co-Market: Target overlapping prospects, opportunities, and customers for your better together stories and integration outreach | Co-Sell: Use your partner ecosystem to surface pre-vetted overlapping accounts that can shorten sales cycles and increase opportunity sizes |
Hover over the options to see the list of fields required. When ready, simply click the option you want and Crossbeam will do the rest.

### Adjust Data Settings
On the Data Sources workspace, hover over the three dots at the end of the HubSpot row to reveal the Settings button.

Click on Settings to:
- View Connection Status and Details: Check the connection status, error messages, and reauthorization requirements Reauthorization may be needed if user access or permissions have changed, and any errors will display here when available
- Reauthorization may be needed if user access or permissions have changed, and any errors will display here when available
- Adjust Data Sync Frequency : Use the Update Frequency dropdown to select how often Crossbeam syncs with HubSpot
- Edit Data Sync: Click Edit Data Sync to open the Customize pop-up, allowing you to add or remove specific fields
- Remove Data Source: Select Remove Data Source to disconnect HubSpot from Crossbeam

🎓 Sign into Crossbeam Academy to further explore HubSpot as a Data Source!
📄 Related Articles
Manage your Connection
Attribution for HubSpot Users

- Connect Snowflake Data
- What are Data Sources?
- Connect Microsoft Dynamics
- Step-by-Step Guide: Reauthorizing Your HubSpot Custom Object Integration
- Connect Databricks as a Data Source


## What are Populations? (HC 3160192)
URL: https://help.crossbeam.com/en/articles/3160192-create-a-population-from-a-csv-file

In this article:
- What are Populations?
- How to Create a Population from a CSV File Set Sharing Default
- Set Sharing Default
- Manage Populations
Populations are segments of data from your data source . These Populations align with key stages in your funnel, such as prospects, open opportunities, and customers.


### How to Create a Population from a CSV File
✍️ Note
Before you begin, make sure have created and successfully uploaded a CSV file, learn more here .
Click on Data from the navigation menu. Select Populations from the dropdown options.
- Click the Create Population button

This will take you to the Population Builder area:
- Add Population name
- Add Optional Population description
- Select CSV Upload from the Data Source menu
- Under File the Name will be pre-filled base on the CSV file you uploaded or you can click the drop-down menu to select a different file
Click Continue .

To add filters, click the drop-down menu to Add Table Filters .
You will be able to preview the Population or save the Population by selecting the appropriate button.

Click Save Population when done .


#### Set Sharing Default
After creating a Population, you will also be prompted to set default sharing settings for each new Population you create.

To fully understand sharing settings in Crossbeam, please click here .


### Manage Populations
Select Data from the navigation bar and Populations f rom the dropdown options.
For each Population, you can:
- Click Edit to open the Population Builder and adjust filters
- Click the three dots to adjust: sharing, duplicate or delete the population or export
- Click the pencil icon next to Sharing Settings to adjust

🎓 Sign in to Crossbeam Academy to further explore Data Sources!
Related Articles
- Sharing Defaults for Populations
- Remove a CSV File
- Add Data to a CSV File

​

- Add Data to a CSV File
- Build a Standard Population
- Upload a CSV File and Map Your Fields
- Video: Upload CSV Files & Create Populations
- Custom Populations


## How to Add Data to an Existing CSV File (HC 3160196)
URL: https://help.crossbeam.com/en/articles/3160196-add-data-to-a-csv-file

In this article:
- How to Add Data to an Existing CSV File
- Best Practices
✍️ Before you Begin
- Make sure your new CSV follows the same column structure and format as the original.
- Only include new records, re-uploading the full original file could result in duplicates.
Need help uploading a CSV File? Read this article here .
The steps of adding Data to an existing CSV file are similar to the steps to uploading a new CSV file.

Click on Data from the navigation menu. From the dropdown, select Data Sources .

Add a new CSV File:
- Click the Add button at the end of the CSV upload row to add a new CSV file or
- Click on the small arrow to the right of the data source name to display all of your uploaded sheets to add data to an existing CSV file click the Settings gear icon
- click the Settings gear icon
Next, follow the rest of the instructions for uploading CSVs, and the data will be added to the file that you select.
✍️ Note
The newly added records will automatically be included in any Populations that use this CSV file.

### Best Practices
Add New Data, Don't Replace It
Avoid re-uploading the entire CSV file to prevent duplicate records. Instead:
- Create a new CSV file with only the additional rows
- Maintain the same headers, formatting, and column order
Handling Account Churn
If an account churns or is no longer relevant:
- You cannot delete or modify individual rows from a CSV upload.
- Instead, apply filters to your Populations to exclude churned accounts from overlaps and Lists.
For more flexibility and easier updates, use Google Sheets or a CRM .
Click here to learn more about Google Sheets as a data source in Crossbeam.
🎓 Sign in to Crossbeam Academy to further explore Data Sources!
📄 Related Articles
- Upload a CSV File
- Create a Population from a CSV File
- Remove a CSV File
- Population Filters
- List Filters
- Google Sheets as a Data Source
- Create a Population from a CSV File
- Upload a CSV File and Map Your Fields
- Video: Upload CSV Files & Create Populations
- How to Remove a CSV File
- Offline Partners


## What are Populations? (HC 3160197)
URL: https://help.crossbeam.com/en/articles/3160197-build-a-standard-population

In this article:
- What are Populations?
- Create a Population Pre-Applied Filters Set Sharing Default
- Pre-Applied Filters
- Set Sharing Default
- Manage Populations
Populations are segments of data from your data source . These Populations align with key stages in your funnel, such as prospects, open opportunities, and customers.

### Create a Population
Click on Data from the navigation menu, select Populations from the dropdown options.
On this page, you'll see the three Standard Populations :
- Customer
- Open Opportunities
- Prospects
Each standard Population has a create button next to it. Click Create to begin setting up that Population.

This will take you to the Population Builder:
- Select a data source from the Data Source menu
- Select the specific object you're using in your data source
- Add Optional Population description
- Click Continue
- Next, you will define your Population and apply filters you will be able to review the data in a preview window before creating the Population
- you will be able to review the data in a preview window before creating the Population

#### Pre-Applied Filters
When creating a new Standard Population (Customer, Open Opportunities, Prospects), Crossbeam will recommend filters to define your Population quickly to align with best practices for overlaps.

These filters are based on your connected CRM and the fields you've synced, serving as a baseline for that Population type.
- Example: For a Customer Population in Salesforce, Crossbeam might auto-apply Stage = Closed Won or Account Type = Customer as default filters
- A tooltip will display next to each filter shows why it was suggested
- You can edit, remove, or add filters at anytime
- click Apply Filters when done

Populations can be adjusted by return to the Population workspace.

#### Set Sharing Default
After creating a Population, you will also be prompted to set default sharing settings for each new Population you create.

To fully understand sharing settings in Crossbeam, please click here .

### Manage Populations
Select Data from the navigation bar and Populations from the dropdown options.
For each Population, you can:
- Click the pencil to open the Population Builder and adjust filters
- Click the three dots to adjust: sharing, duplicate or delete the population or export

🎓 Sign into Crossbeam Academy to further explore Populations!
Related Articles
- Sharing Defaults for Populations
- Advanced Population Filtering
- Create a Population from a CSV File
- What are Populations?
- Custom Populations
- Population Types for Custom Populations
- How to Build a Product-Based Population Using Product2


## Add Filters to the Population (HC 3160198)
URL: https://help.crossbeam.com/en/articles/3160198-how-to-use-population-filters

In this article:
- Add Filters to the Population Building a Filter Using Comparison Operators Add Multiple Filters Filter Groups for Advanced Logic Edit or Remove Filters
- Building a Filter
- Using Comparison Operators
- Add Multiple Filters
- Filter Groups for Advanced Logic
- Edit or Remove Filters

Filters allow you to define exactly which records belong in your Population, whether you’re targeting key accounts, large deals, or specific AEs. You can use filters to build both simple and complex logic based on your connected data source.

Click on Data from the navigation menu, select Populations from the dropdown options.

Open an existing Population from the list, or click Create Population to start a new one.

Once in the Population Builder, click to the Filters area. Here, you’ll build logic to segment your data.


#### Building a Filter
- Type or scroll to find a field
- Can't find a field? Click Add Filters from another object to open the Customize Fields modal
- From there, you can: Apply data presets Expand data objects (like Account or Contact) to browse all available fields Use the search bar to find specific fields Check the box for the fields you want to sync
- Apply data presets
- Expand data objects (like Account or Contact) to browse all available fields
- Use the search bar to find specific fields
- Check the box for the fields you want to sync
- When finished, click Review Fields > Sync Now to apply your changes.


#### Using Comparison Operators
Once you've selected a field to filter on, you'll be prompted to choose a comparison operator, this defines how Crossbeam should evaluate the field's value.
The operators available will depend on the type of field you're working with:
- For text fields (like Account Name or Industry), you'll see options such as: is / is not, to match an exact value contains / does not contain, to match partial values or keywords
- is / is not, to match an exact value
- contains / does not contain, to match partial values or keywords
- For numeric fields (like Opportunity Size or Number of Employees), you’ll see: equals, greater than, less than, or between
- equals, greater than, less than, or between
- For date fields (like Created Date or Last Modified), you can filter by: is on, is before, is after
- is on, is before, is after
If you want to build a list of values, say, multiple industries or account owners, you can:
- Use the is or is not operator
- Then click and / or to add additional values to include or exclude
This approach is especially helpful when segmenting by territory, product line, or custom tags.


#### Add Multiple Filters
- Click + Add Filter from another object to define additional filter criteria
- Use AND / OR logic within each filter group: AND chains together filters that must all be true. OR adds flexibility, useful for matching any one of several criteria.
- AND chains together filters that must all be true.
- OR adds flexibility, useful for matching any one of several criteria.
Example:
Filter accounts where Industry is Tech AND Opportunity Size is greater than $500K ​ OR ​ Region is APAC


#### Filter Groups for Advanced Logic
To structure more complex logic:
- Use AND inside a group for tight filtering
- Use OR between groups to broaden your scope


#### Remove or Edit Filters
- Click the Pencil icon next to a filter to edit it
- Click the Trash icon to delete a single filter, this won't affect the rest of your setup
Filtering Tips
- Nest filters using AND / OR strategically to create accurate, targeted Populations.
- Use multiple values with “is” or “is not” filters by adding OR conditions to build lists.
- Revisit the Customize Fields modal any time your data changes or new fields become available.
🎓 Sign in to Crossbeam Academy to further explore Populations!
- Build a Standard Population
- What are Populations?
- Understanding Sharing Settings for Partners
- Custom Populations
- How to Build a Product-Based Population Using Product2


## How to Delete a Population (HC 3160199)
URL: https://help.crossbeam.com/en/articles/3160199-delete-a-population

❗️ Important
Deleting a Population will:
- Permanently remove it from Crossbeam
- Stop sharing this Population’s data with partners
- Remove the data from any reports using it
- This action is permanent and cannot be reversed
To delete a Population in Crossbeam:
- Click on Data from the navigation menu, select Populations from the dropdown
- Locate the row with the Population you want to remove
- Click the three dots at the end of the row Select Delete Population from the options Confirm the deletion in the pop-up window to permanently remove it
- Select Delete Population from the options
- Confirm the deletion in the pop-up window to permanently remove it

- What are Populations?
- Managing Population Settings
- Delete a Partner
- Offline Partners
- Onboarding: Lookalike Prospects Population


## Overview (HC 3160473)
URL: https://help.crossbeam.com/en/articles/3160473-upload-a-csv-file-and-map-your-fields

In this article:
- Overview
- How to Add a CSV File Upload CSV Field Mapping
- Upload CSV
- Field Mapping
- Map Additional Columns on Existing CSVs
- Manage CSV Files

A CSV (comma-separated values) file is a text file that stores data in a table-structured format. Once you upload your CSV file into Crossbeam, you can use that data to create Populations, reports, and grow your ecosystem.

✍️ Note
Because CSV files are static, you'll need to upload a new file each time your data changes. You can remap columns at any time as your data evolves.

### How to Add a CSV File
❗️ Important
The file must be in CSV format with a size limit of 15 MB. For larger files, use Google Sheets as a Data Source .
Download a CSV File template here as a starting point.
You can edit the template to add columns.
Navigate to Data from the navigation menu and select Data Sources from the dropdown.

Add a new CSV file using one of two options:
- Click the Add button at the end of the CSV Upload row, or
- Click the CSV Upload tile under Add a Data Source
This opens a modal that walks you through the upload process.


#### Upload CSV
- Click Browse to select a file from your computer, or drag and drop it into the modal.
- Enter a CSV Name
- Select a data type,  Companies or People

Click Next to continue.
✍️ Note
This file name is shared with partners when you share data.

#### Field Mapping
This step aligns your CSV column headers with Crossbeam's data mapping.

If your data type is Companies, select the corresponding column from your CSV for each field:
| Crossbeam Fields for Companies | |
| Company Name | Required |
| Website | Required |
| Account Owner Name | Recommended |
| Account Owner Email | Recommended |
| DUNS Number | Optional |
| Industry | Optional |
| Number of Employees | Optional |
| Account Owner Phone | Optional |
| Country | Optional |
| Postal Code | Optional |
| Region | Optional |
| City | Optional |
| Address | Optional |
| Company Phone Number | Optional |

If your data type is People, select the corresponding column from your CSV for each field:
| Crossbeam Fields for People | |
| Email | Required |
| Account Owner Name | Recommended |
| Account Owner Email | Recommended |
| Lead Name | Optional |
| Lead Phone | Optional |
| Lead Title | Optional |
| Company Name | Optional |
| Company Website | Optional |
| Country | Optional |
| Postal Code | Optional |
| Region | Optional |
| City | Optional |
| Address | Optional |
| Account Owner Phone | Optional |
Click Upload to complete the upload.

### Map Additional Columns on Existing CSVs
You can map additional fields to any existing CSV dataset at any time. This is useful when uploading updated data with new columns or when correcting a previous mapping.
- Navigate to Data Sources from the left-hand navigation
- Click the dropdown arrow next to the CSV dataset you want to update
- Click the Settings gear icon for the file
- Click Add Data
- Select the appropriate column from your CSV for each field
- Click Upload
Be sure to click Save when done.

Crossbeam reprocesses the dataset to apply the updated mappings. The dataset will show a processing status until complete.

### Manage CSV Files
Once your CSV files are connected, manage them from Data Sources .
Click the dropdown arrow to the right of the data source name to display all uploaded files and their status.

Click the Settings gear icon to:
- Check Connection
- Add Data
- Map New Columns
- Adjust Sharing Presets
- Remove Data Source
🎓 Sign into Crossbeam Academy to further explore Data Sources!
- Create a Population from a CSV File
- Add Data to a CSV File
- Video: Upload CSV Files & Create Populations
- How to Use Google Sheets as a Data Source
- Offline Partners


## 3160813-what-are-populations.html (HC 3160813)
URL: https://help.crossbeam.com/en/articles/3160813-what-are-populations

Populations play a crucial role in Crossbeam, as they serve as a common language, enabling you and your partners to merge and compare data effectively.

Populations are segments of data from your data source . These Populations align with key stages in your funnel, such as Prospects, Open Opportunities, and Customers.
Populations serve two important purposes in Crossbeam:
- Standardization: Data sources vary. Comparing raw data from Salesforce, HubSpot, and CSV upload for overlaps is impractical. Organizing data into Populations by all partners streamlines this process. Crossbeam's matching algorithm can compare and merge data sets on an apples-to-apples basis, significantly enhancing speed and precision by using Populations.
- Crossbeam's matching algorithm can compare and merge data sets on an apples-to-apples basis, significantly enhancing speed and precision by using Populations.
- Data cleansing: Everyone's data is dirty, and Populations are a way of cleaning up this complexity. Rather than share your entire list of accounts or every lead generated, Populations enable you to distill your data into meaningful segments that truly reflect your business.
❗️ Important
Populations aren't intended for detailed data analysis. Best practice is for companies to establish a few large, broadly defined Populations as their foundation. Next, they refine the results of these comparisons using Lists to analyze overlaps in detail.
Ready to build Populations?
- Build a Standard Population
- How to Edit a Population
- How to Use Population Filters
- Delete a Population
- How to Use the Partner List and Partner Detail Page
- Population Types for Custom Populations
- Databricks Integration
- Onboarding: Lookalike Prospects Population


## 3161135-how-to-edit-a-population.html (HC 3161135)
URL: https://help.crossbeam.com/en/articles/3161135-how-to-edit-a-population

Select Data from the navigation bar and Populations from the dropdown options.

For each Population, you can:
- Click Edit to open the Population Builder and adjust filters
- Click the three dots to adjust: Sharing default, duplicate or delete the Population or export
- Sharing default, duplicate or delete the Population or export
- Click the pencil icon next to Sharing Settings to adjust
​To fully understand sharing settings in Crossbeam, please click here .
🎓 Sign in to Crossbeam Academy to further explore Populations!
🔗 Related Articles
- Build a Standard Population
- How to Use Population Filter s
- Delete a Population

- Create a Population from a CSV File
- Build a Standard Population
- Data Sharing Requests from Partners
- Managing Population Settings
- Custom Populations


## Reauthorize your Connection (HC 3380461)
URL: https://help.crossbeam.com/en/articles/3380461-manage-your-salesforce-connection

In this article:
- Reauthorizing your Connection
- Pause your Sync
- View Connection Status
- Update Sync Frequency
- Edit Field Sync
Salesforce connection reauthorization is required if user permissions change, users lose access to Salesforce, or user who completed the initial authorization leave the organization.
❗️ Important
A Crossbeam Admin is required to complete the Salesforce reauthorization.
Additionally, the Crossbeam Admin needs the required Salesforce permissions:
- API enabled
- View Setup and Configuration
- View all users
- Read access to Lead and Account and Contact and Opportunity objects
Click on Data from the navigation menu, then select Data Sources .
- Locate the Salesforce row and click the setting gear icon
- Click the Reauthorize button to authenticate the connection in Salesforce
- Enter the new username and password, and follow the prompts in Salesforce
- Click Save

### Pause your Sync
On the Data Sources page, within the Salesforce row, click the settings gear icon .
In the settings modal, use the Sync Data from Salesforce toggle to pause or restart syncing.


### View Connection Status
The connection status appears within the Salesforce Settings menu and also on your Data Sources workspace.
- Active: the connection is active and will sync according to your sync frequency.
- Not Syncing: the connection is paused and will not sync data until it is made active.
- Error: the connection hit an error and is unable to sync. If available, details on the error will appear.

### Update Sync Frequency
❗️ Important
To avoid exceeding your Salesforce API quota, consider reducing sync frequency to reduce the number of API calls.
Crossbeam pauses syncing at 80% of your quota and notifies you by email and in-app.

To adjust this value to something higher (or lower), please reach out to us at support@crossbeam.com . <!-- VALIDATE-OK[person-address]: verbatim public Crossbeam Help Center text -->
On the Data Sources page, within the Salesforce row, click the settings gear icon .
- In the Salesforce settings, click the dropdown next to Update Frequency
- Select how often your Salesforce data should sync
- Click Save


### Edit Field Sync
Click on the Edit Data Sync in the Salesforce Settings pop-up. This will open the Customize Fields pop-up modal.

How to Customize Sync Fields:
- From the data source Salesforce Settings, click Field Sync >Edit
- In the next window, expand any table under All Data by clicking the drop-down arrow, or use the search bar to locate specific fields
- Select or deselect any of the fields to customize your data You can also click the Toggle button to turn entire tables on or off
- You can also click the Toggle button to turn entire tables on or off
- Click Review Fields, then select Sync Now to complete the connection
- Or click Go Back to edit your changes before completing the sync

🎓 Sign into Crossbeam Academy to further explore Salesforce as a Data Source!
📄 Related Articles
- Connecting Salesforce Data
- Troubleshooting your Salesforce Connection
- Salesforce as a Data Source FAQs
- Connecting Salesforce as a Data Source
- Manage your HubSpot Connection
- Troubleshooting your Salesforce Connection
- Salesforce as a Data Source FAQs
- Step-by-Step Guide: Reauthorizing Your Salesforce Custom Object Integration


## Reauthorize Your Connection (HC 3380769)
URL: https://help.crossbeam.com/en/articles/3380769-manage-your-hubspot-connection

In this article:
- Reauthorize your Connection
- Pause your Sync
- View Connection Status
- Update Sync Frequency
- Edit Field Sync
Kick off your HubSpot training in Crossbeam Academy.

Reauthorization is required if user permissions change or users lose access to HubSpot.
❗️ Important
To complete the HubSpot connection, you must have Super Admin permissions and Marketplace Access in HubSpot.
Click on Data from the navigation menu. Select data sources from the dropdown options.
- Locate the HubSpot row and click the setting gear icon
- Click the Reauthorize button to authenticate the connection
- Enter the new username and password, follow the prompts in HubSpot
- Click Save

### Pause Data Sync
On the Data Sources page, within the HubSpot row, click the settings gear icon .
In the settings modal, use the Sync Data from HubSpot toggle to pause or restart syncing.

❗️ Important You will not be able to select or remove fields while the sync is paused.

### View Connection Status
The connection status appears within the HubSpot Settings menu and also on your Data Sources page.
- Active: the integration is active and will sync according to your sync frequency.
- Not Syncing: the integration is paused and will not sync data until it is made active.
- Error: the integration hit an error and is unable to sync. If available, details on the error will appear.
✍️ Note
Contact us at support@crossbeam.com if you have problems with your sync. <!-- VALIDATE-OK[person-address]: verbatim public Crossbeam Help Center text -->

### Update Sync Frequency
On the Data Sources page, within the HubSpot row, click the settings gear icon .
- In the HubSpot settings, click the dropdown next to Update Frequency
- Select how often your HubSpot data should sync
- Click Save


### Edit Field Sync
Click on the Edit Data Sync in the HubSpot Settings pop up. This will open the Customize Fields pop up modal.

How to Customize Sync Fields:
- From the data source HubSpot Settings, click Field Sync >Edit
- In the next window, expand any table under All Data by clicking the drop-down arrow, or use the search bar to locate specific fields
- Select or deselect any of the fields to customize your data You can also click the Toggle button to turn entire tables on or off
- You can also click the Toggle button to turn entire tables on or off
- Click Review Fields, then select Sync Now to complete the connection
- Or click Go Back to edit your changes before completing the sync

🎓 Sign into Crossbeam Academy to further explore HubSpot as a Data Source!
📄 Related Articles
- Connecting HubSpot Data
- Connecting Salesforce as a Data Source
- Connect HubSpot Data
- Manage your Salesforce Connection
- Connecting Pipedrive as a Data Source
- Step-by-Step Guide: Reauthorizing Your HubSpot Custom Object Integration


## 4136739-troubleshooting-your-salesforce-connection.html (HC 4136739)
URL: https://help.crossbeam.com/en/articles/4136739-troubleshooting-your-salesforce-connection

In this article:
- Over API Quota Limit
- API_CURRENTLY_DISABLED: API is disabled for this User
- API_DISABLED_FOR_ORG The REST API is not enabled for this Organization Limits resource is not enabled
- The REST API is not enabled for this Organization
- Limits resource is not enabled
- Invalid Grant invalid_grant: expired access/refresh token invalid_grant: inactive user
- invalid_grant: expired access/refresh token
- invalid_grant: inactive user
- REQUEST_LIMIT_EXCEEDED: TotalRequests Limit exceeded
- UnknownHostException: invalid instance url
- NOT_FOUND: The requested resource does not exist
- OAUTH_APP_BLOCKED: salesforce admin needs to unblock crossbeam oauth app
✍️ Note
The Salesforce data push sync defaults to twice a day, every 12 hours . Actual update times may vary.

If you encounter a Salesforce connection error, reauthorizing the connection is often the solution to fix it .

Watch the video below for detailed steps.
✍️Want to see these steps with detailed screenshots? Click here to view the article.
Below are additional common errors with their corresponding solutions. Some issues may require your Salesforce admin.
✍️ Note
REST API access is only available on the Connector plan and Supernode plan.
To upgrade your account, visit the Plan & Billing page .

#### Over API Quota Limit
- What happened? We paused our sync with Salesforce because your Salesforce organization has used up 80% or more of its daily Bulk API quota. (For most companies, many other services besides Crossbeam drive the majority of this quota usage.) We pause our sync at this percentage as a safety precaution so we don't push your organization over its limit and interfere with critical Salesforce functionality. We'll try to sync again the next day when the limit is reset.
- ​ What does the error look like? Below is an example of the error. Salesforce has reported 189737/218000 (87%) total REST API quota used across all Salesforce Applications. Terminating data sync to not go past configured percentage of 80% total quota.
Salesforce has reported 189737/218000 (87%) total REST API quota used across all Salesforce Applications. Terminating data sync to not go past configured percentage of 80% total quota.
- What do I do? If this is your first time getting this error, you may not need to do anything. If you've received this error more than once, it may be time to reach out to your sales ops team to see what's impacting your Bulk API quota limit. Your Salesforce admin can also check the Bulk Data Load Jobs log to see which integrations are consuming the most API calls. To find it, navigate to Setup → Jobs → Bulk Data Load Jobs in Salesforce. This shows a breakdown of bulk batch usage across all connected integrations so you can identify what's driving your quota usage.
- To find it, navigate to Setup → Jobs → Bulk Data Load Jobs in Salesforce. This shows a breakdown of bulk batch usage across all connected integrations so you can identify what's driving your quota usage.

#### API Current Disabled
- What happened? We were unable to sync with Salesforce because the user that authenticated Salesforce does not have API access in Salesforce.
- ​ What does the error look like? Below is an example of the error. API_CURRENTLY_DISABLED: API is disabled for this User
API_CURRENTLY_DISABLED: API is disabled for this User
- What do I do? You can reauthorize the Salesforce connection with a user that has API access, or you can ask your Salesforce admin to give API access to your existing user in Salesforce.

#### API Disabled for Org
Below are two variations of this error:


##### API_DISABLED_FOR_ORG: The REST API is not enabled for this Organization
- What happened? We were unable to sync with Salesforce because your Salesforce organization does not have API access.
- What was the error? Below is an example of the error. API_DISABLED_FOR_ORG: The REST API is not enabled for this Organization.
API_DISABLED_FOR_ORG: The REST API is not enabled for this Organization.
- What do I do? You will need to reach out to your Salesforce admin to ensure your Salesforce org has API access.

##### API_DISABLED_FOR_ORG: limits resource is not enabled
- What happened? We were unable to sync with Salesforce because your Salesforce organization does not have API access properly configured.
- What was the error? Below is an example of the error. API_DISABLED_FOR_ORG: limits resource is not enabled
API_DISABLED_FOR_ORG: limits resource is not enabled
- What do I do? You will need to reach out to your Salesforce admin to ensure your Salesforce org has both the API enabled and "View Setup and Configuration" system permissions enabled. This error is likely because do not have "View Setup and Configuration" system permissions enabled.
- Please Note: The user who is authenticating the Salesforce connection in Crossbeam must have "View Setup and Configuration" system permissions enabled on their Salesforce user profile.

#### Invalid Grant
Below are two variations of this error:


##### Invalid_grant: expired access/refresh token
- What happened? We were unable to sync with Salesforce because we no longer have access to your Salesforce instance. ​​
- What was the error?
invalid_grant: expired access/refresh token
- What do I do? You will need to reauthorize your Salesforce connection in Crossbeam.

##### Invalid_grant: inactive user
- What happened? We were unable to sync with Salesforce because the user who originally connected Salesforce to Crossbeam does not have access to Salesforce anymore. The user may have been deactivated or removed from the org.
- ​ What was the error?
invalid_grant: inactive user
- What do I do? You can reauthorize the Salesforce connection with a new user, or you can ask your Salesforce admin to verify that the user that is currently authenticated has access to your Salesforce org.

#### REQUEST_LIMIT_EXCEEDED: TotalRequests Limit exceeded.
- What happened? We were unable to sync with Salesforce because your Salesforce organization has used up all of its daily Bulk API quota. (For most companies, many other services besides Crossbeam drive the majority of this quota usage.) We are not able to sync your data at this time. We'll try to sync again the next day when the limit is reset.
- ​ What was the error? REQUEST_LIMIT_EXCEEDED: TotalRequests Limit exceeded.
REQUEST_LIMIT_EXCEEDED: TotalRequests Limit exceeded.
- ​ What do I do? Check your API quota in Salesforce by heading to: Setup -> Environments -> System Overview. Your team can increase the quota, or see what other tools are taking up the majority of your daily quota.

#### UnknownHostException: invalid instance url
- What happened? This error is caused by a system outage or interruption on Salesforce's end. You are being notified because we tried to sync your data for an update, but weren't able to because of the Salesforce server issue.
- ​ What was the error?
UnknownHostException: invalid instance url
- What do I do? Head to Salesforce's Trust Status page for more information regarding the error. Rest assured that your data is still in Crossbeam and useable during this Salesforce sync issue. Once Salesforce corrects the problem, the error message will be removed without any need to re-authorize your connection in Crossbeam.

#### NOT_FOUND: The requested resource does not exist
- What happened? The Salesforce instance that was previously authorized with Crossbeam either does not exist anymore, OR current the person that authorized it does not have permission to do so anymore. This could have happened if the person that set up the connection left your company, or had Salesforce API permission revoked.
- What was the error? NOT_FOUND: The requested resource does not exist
NOT_FOUND: The requested resource does not exist
- What do I do? Another user with API permission can reauthorize the connection under the Salesforce Settings within Crossbeam.

#### OAUTH_APP_BLOCKED: salesforce admin needs to unblock crossbeam oauth app
- What happened? The Crossbeam Oauth app has been blocked from accessing the Salesforce environment.
- What was the error? OAUTH_APP_BLOCKED: salesforce admin needs to unblock crossbeam oauth app
OAUTH_APP_BLOCKED: salesforce admin needs to unblock crossbeam oauth app
- What do I do? Contact the Salesforce Admin. In Salesforce, the Admin should: Navigate to Setup > Apps > Connected Apps > Connect Apps Oauth Usage Locate the Crossbeam row in the list Under the action column, click Unblock
- In Salesforce, the Admin should: Navigate to Setup > Apps > Connected Apps > Connect Apps Oauth Usage Locate the Crossbeam row in the list Under the action column, click Unblock
- Navigate to Setup > Apps > Connected Apps > Connect Apps Oauth Usage
- Locate the Crossbeam row in the list
- Under the action column, click Unblock
This ensures the Crossbeam app is re-enabled and can connect.

- Connecting Salesforce as a Data Source
- Manage your Salesforce Connection
- Salesforce as a Data Source FAQs
- Step-by-Step Guide: Reauthorizing Your Salesforce Custom Object Integration
- Troubleshooting Salesforce Authorization with Crossbeam


## Connect Crossbeam to Snowflake (HC 4470887)
URL: https://help.crossbeam.com/en/articles/4470887-connect-snowflake-data

In this article:
- Connect Crossbeam to Snowflake Requirements
- Requirements
- Manage your Snowflake Integration in Crossbeam
- Configuring your Snowflake Data Share
- Tracking deleted records (Optional)
Have your CRM data in Snowflake? Skip integrating your CRM and use Snowflake Data Sharing to share data with Crossbeam's Snowflake account, allowing you to get your CRM data into Crossbeam, all via Snowflake.
✍️ Note
Before you click the Snowflake tile in Crossbeam, confirm that your Snowflake Shares have been created and configured in your Snowflake instance. Your connection in Crossbeam will not complete successfully until these Shares are established.
Once your Shares are set up, return to your Crossbeam account and continue by selecting the Snowflake tile to connect.

From the left-side Navigation Menu, click on the Data icon. This will open the data sources workspace. Scroll down under Add a Data source, click the Snowflake tile.

✍️ Note
Snowflake is retiring the Classic UI on an account-by-account basis. If your account still has Classic, the screenshots below will match your experience. If your account has migrated to Snowsight only, switching back to Classic from your profile is no longer available. The steps below are the same, but your screens will look different.

#### Requirements
This data source is available to all Crossbeam plans.

To get started, you'll need three pieces of information:

1. Your Snowflake account region
Currently, we support five regions:
- US West (Oregon): this region is the only one not included in snowflake URLs
- US East (Ohio)
- US East (N. Virginia)
- EU West (Ireland)
- EU-Central (Frankfurt)
✍️ Note
Please contact support@crossbeam.com if your account is in a different region, and we can work to add support for you. <!-- VALIDATE-OK[person-address]: verbatim public Crossbeam Help Center text -->
2. Your Snowflake account locator
Account locator information can be found in the Account Information section of your Snowflake instance:

3. Your Snowflake data share name
Crossbeam will provide you with a data share name to use in Snowflake.
It will be in the format of crossbeam_share_{123} where 123 will be a unique number to your organization.
You will enter this in the Shares tab in Snowflake.


### Manage your Snowflake Integration in Crossbeam
Once your Snowflake connection is set up, you can manage it from the Data Source workspace. Locate the Snowflake row, click the Settings icon, and select Field Sync >Edit .

In the settings, you can:
- Pause the sync into Crossbeam
- Select which fields to sync into Crossbeam from Snowflake
- Remove the Snowflake connection
✍️ Note
Update frequency is not configurable for Snowflake. Contact Crossbeam if you'd like to change the frequency of updates.

### Configuring your Snowflake Data Share
In Snowflake, your shared database must contain a set of required tables and fields under a _CROSSBEAM schema.

We expect the following tables and fields to be shared with a share called CROSSBEAM_SHARE_{ID} (this ID is provided in the Crossbeam UI on the data source page when connecting Snowflake as a data source - see above).

To create a share in the Snowsight UI, navigate to Data > Private Sharing, click the Share button in the top right, and create a Direct Share .

a) Secure Share Identifier should be the name Crossbeam provides on the data sources page when you click the Snowflake tile.
b) Add accounts in your region by name should be the Account Locator we provide in the help doc

✍️ Note
If your account still has Snowflake Classic UI, you can access the Shares tab at:
https:// <organization>-<name> .snowflakecomputing.com/console#/shares .
If Classic has been retired for your account, this link will return a 404, use the Snowsight steps above instead.
❗️ Important
Capitalization counts here, be sure that _CROSSBEAM is in ALL CAPS.
Next, you'll need to add Crossbeam as a Consumer using the Account Locator associated with your region.

Account Locators:
| Region | Account Locator |
| US East 1 | ZAA86167 |
| US East 2 | KP43495 |
| US West 2 | CROSSBEAM |
| EU West 1 | LV64179 |
| EU Central | AV17996 |

✍️ Note
You don't need all the following tables for the integration to work.
❗️ Important
To support Account Owners in Crossbeam, you must include the user table specified below.

The fields marked as required need to exist in order for Crossbeam to properly integrate. The fields not marked as required can be skipped, but are recommended. ​You can also include additional fields if there is any other data that you would like to be able to filter on or share with partners in Crossbeam.

### Tracking Deleted Records (Optional)
If your Snowflake source soft-deletes records (marks them as deleted rather than removing the row), you can include a IS_DELETED column on any of the shared tables.

When this column is present:
- Records where IS_DELETED is TRUE will be removed from your Crossbeam overlaps on the next sync.
- Records where IS_DELETED is FALSE (or empty) will sync normally.
The column can be a BOOLEAN or a VARCHAR . If it's a VARCHAR, the values "true" and "TRUE" are both treated as deleted.

If you delete records directly from Snowflake without using the IS_DELETED column, those deletions will be picked up automatically during a full sync, which runs every 30 days.

Without this column, records that have been removed from your Snowflake share will stay in Crossbeam until they're cleaned up manually.
✍️ Note
We recommend adding IS_DELETED to all five tables (Accounts, Leads, Contacts, Deals, and Users) so your Crossbeam data stays in sync with your source.

#### ACCOUNTS
Important Note on ID Fields
The ID field in your connected Snowflake instance is Crossbeam's primary key. It must remain static and uniquely identify a record in your Snowflake instance, changing it will create duplicate records in our system. If you need to modify an existing record, ensure that the ID field remains unchanged to avoid data inconsistencies.
| Field | Type | Notes | Is Required? |
| ID | VARCHAR | Account ID | ✅ |
| WEBSITE | VARCHAR | Account Website | ✅ |
| NAME | VARCHAR | Account Name | ✅ |
| TYPE | VARCHAR | Account Type | |
| OWNER_ID | VARCHAR | FK to a User | |
| DUNS_NUMBER | VARCHAR | Dun & Bradstreet (DUNS) Number | |
| CREATED_AT | TIMESTAMP_TZ | Account Created At | ✅ |
| UPDATED_AT | TIMESTAMP_TZ | Equivalent of Salesforce's SystemModstamp. Last time record was upserted into snowflake | ✅ |
| IS_DELETED | BOOLEAN or VARCHAR | When TRUE (or "true" for VARCHAR), the record is removed on the next sync. More details here . | |

#### LEADS
| Field | Type | Notes | Is Required? |
| ID | VARCHAR | Lead Id | ✅ |
| EMAIL | VARCHAR | Lead Email | ✅ |
| NAME | VARCHAR | Lead Name | |
| PHONE | VARCHAR | Lead Phone | |
| TITLE | VARCHAR | Lead Title | |
| OWNER_ID | VARCHAR | FK to a User | |
| CREATED_AT | TIMESTAMP_TZ | Lead Created At | ✅ |
| UPDATED_AT | TIMESTAMP_TZ | Equivalent of Salesforce's SystemModstamp. Last time record was upserted into snowflake | ✅ |
| IS_DELETED | BOOLEAN or VARCHAR | When TRUE (or "true" for VARCHAR), the record is removed on the next sync. More details here . | |

#### CONTACTS
| Field | Type | Notes | Is Required? |
| ID | VARCHAR | Contact Id | ✅ |
| EMAIL | VARCHAR | Contact Email | ✅ |
| NAME | VARCHAR | Contact Name | ✅ |
| PHONE | VARCHAR | Contact Phone | |
| TITLE | VARCHAR | Contact Title | |
| ACCOUNT_ID | VARCHAR | FK to an Account | ✅ |
| CREATED_AT | TIMESTAMP_TZ | Contact Created At | |
| UPDATED_AT | TIMESTAMP_TZ | Equivalent of Salesforce's SystemModstamp. Last time record was upserted into snowflake | ✅ |
| IS_DELETED | BOOLEAN or VARCHAR | When TRUE (or "true" for VARCHAR), the record is removed on the next sync. More details here . | |

#### DEALS
| Field | Type | Notes | Is Required? |
| ID | VARCHAR | Deal Id | ✅ |
| AMOUNT | DOUBLE | | |
| NAME | VARCHAR | Deal name | |
| STAGE_NAME | VARCHAR | Sales Stage | |
| ACCOUNT_ID | VARCHAR | FK to an Account | ✅ |
| CLOSED_AT | VARCHAR | Close Date | |
| CREATED_AT | TIMESTAMP_TZ | Open Date | |
| UPDATED_AT | TIMESTAMP_TZ | Equivalent of Salesforce's SystemModstamp. Last time record was upserted into snowflake | ✅ |
| IS_CLOSED | BOOLEAN | Closed | |
| IS_WON | BOOLEAN | Won | |
| OWNER_ID | VARCHAR | FK to a Users | |
| TYPE | VARCHAR | Deal Type | |
| IS_DELETED | BOOLEAN or VARCHAR | When TRUE (or "true" for VARCHAR), the record is removed on the next sync. More details here . | |

#### USERS
| Field | Type | Notes | Is Required? |
| ID | VARCHAR | User Id | ✅ |
| NAME | VARCHAR | User Name | |
| EMAIL | VARCHAR | User Email | ✅ |
| PHONE | VARCHAR | User Phone | |
| CREATED_AT | TIMESTAMP_TZ | User Created At | |
| UPDATED_AT | TIMESTAMP_TZ | Equivalent of Salesforce's SystemModstamp. Last time record was upserted into snowflake | ✅ |
| IS_DELETED | BOOLEAN or VARCHAR | When TRUE (or "true" for VARCHAR), the record is removed on the next sync. More details here . | |
- Snowflake Integration
- What are Data Sources?
- Crossbeam Overview for Compliance Teams
- How to Set Up the Partner Account CRM Integration
- Connect Databricks as a Data Source


## How to Remove a CSV file (HC 5018090)
URL: https://help.crossbeam.com/en/articles/5018090-how-to-remove-a-csv-file

Keep data clean and organized to uncover insights within your partnership ecosystem. Crossbeam makes it easy to remove and manage unwanted CSV files.

‼️ Important‼️
Deleting a CSV file will also remove any Populations powered by that file, which may impact related Lists and Overlaps .
Click on the Data from the navigation menu, select Data Sources .
- Find the row labeled CSV Upload and click the down arrow to expand
- Click the gear icon next to the file name
- Select Delete
- When prompted, type DELETE to confirm

🎓 Sign in to Crossbeam Academy to further explore Data Sources!
📄 Related Articles
- Create a Population from a CSV File
- Upload a CSV File
- Add Data to a CSV File
- Create a Population from a CSV File
- Add Data to a CSV File
- Upload a CSV File and Map Your Fields
- Video: Upload CSV Files & Create Populations
- What are Data Sources?


## Going Further: Advanced CRM Customizations (HC 5391508)
URL: https://help.crossbeam.com/en/articles/5391508-data-sources-overview-csvs-crms-and-data-warehouses

With a library of data sources available, you can upload a CSV, connect a CRM, or route data from a Data Warehouse to build your partner data foundation in Crossbeam.

This article walks through the different data source options and how to use them based on common use cases.

#### Getting Started: Google Sheets or CSVs
If you're just beginning to identify overlaps with your partners, uploading a Google Sheet or a CSV file is the fastest way to get started with account mapping.

Pros and Considerations
Pros: Google Sheets and CSV uploads are free and quick to set up, and accelerate your initial account mapping efforts.
- Google Sheets: You can map, manage, and dynamically update your account data from Google Sheets directly within Crossbeam.
- CSVs: You can store unlimited CSVs in Crossbeam, keep versions organized, and streamline data with built-in storage. Once you've imported a CSV, you can use it to create Populations and Lists to grow your ecosystem intelligence. See how to set up a Population from a CSV in this video .
Considerations: CSV uploads are useful for one-off partner comparisons, but don't scale as well as other data sources. CSVs are a static snapshot of your data and are not automatically refreshed with the latest account information. To stay useful beyond the initial upload, CSVs must be updated manually and maintained consistently.

Learn more about managing CSVs

#### Scaling Up: CRMs and Data Warehouses
CRM systems (Salesforce, HubSpot, and Microsoft Dynamics) and Data Warehouses (Snowflake and Databricks) serve as a dynamic system of record in Crossbeam for your sales pipeline and customer base.

Unlike CSVs, data sources connected through a CRM or Data Warehouse update automatically several times a day, keeping your data current and accurate. With these data sources in place, your account mapping can move at the speed of your business.

Pros and Considerations
Pros: Fast and scalable. Using a CRM or Data Warehouse as a data source helps your Crossbeam ecosystem grow alongside your business. Capture account changes in near real-time and act on opportunities as they surface, with scheduled data syncs throughout the day. Extend your reach by using data from your CRM or Data Warehouse to build Populations for a complete view of your partner landscape, then narrow your focus to the most relevant accounts. See how to connect your CRM and create Populations .

Considerations: This type of data source may require some initial configuration and setup. Contact our support team if you need help getting started.

For customers moving from CSVs to CRM or Data Warehouse integrations, you can customize the default fields you want synced into Crossbeam.

With advanced filtering capabilities, you can create suppression streams, targeted account segmentation, or simply be more selective about the data you bring into Crossbeam. If you already have a CRM connected, you can customize these fields at any time, though filtering will not be applied retroactively.

Interested in advanced CRM customizations? Contact our support team to get started.

Pros and Considerations
Pros: Better segmentation. Keep data clean and organized by proactively removing unnecessary fields when setting up your CRM integration. During implementation, customize the default fields you'd like to sync with Crossbeam for cleaner, more actionable account mapping. If your CRM is already connected, you can re-sync it and go through the same customization steps to adjust your preferred data going forward.

Considerations: This type of data source may require some initial configuration and setup. Contact our support team if you need help getting started.

You can also browse the full library of data sources by visiting the Data Sources page in Crossbeam.
💡 Tip
When connecting your CRM for the first time, it pays to be selective with your data. Use advanced CRM customization to cut through the clutter and focus on your most valuable partner ecosystem data.
- Upload a CSV File and Map Your Fields
- Integrations Overview
- What are Data Sources?
- Crossbeam Overview for Compliance Teams
- Connect Databricks as a Data Source


## How to Prepare and Sync your Google Sheet (HC 5613345)
URL: https://help.crossbeam.com/en/articles/5613345-how-to-use-google-sheets-as-a-data-source

In this article:
- How to Prepare and Sync your Google Sheet Google Sheet Requirements
- Google Sheet Requirements
- Google Authentication Having authentication trouble?
- Having authentication trouble?
- Add & Map Google Sheets Optional: Map Account Owner Data
- Optional: Map Account Owner Data
- Manage Connected Sheets
- Frequently Asked Questions


#### Google Sheet Requirements
Before you connect a Google Sheet to Crossbeam, make sure it meets these requirements:
- Crossbeam does not support XLSX files (Excel format) uploaded to Google Drive. If you see a green .XLSX label next to the file name, it will not work. Convert it to Google Sheets format first.
- If you see a green .XLSX label next to the file name, it will not work. Convert it to Google Sheets format first.
- Your Google Sheet must have: A unique name Unique headers for each column For example, do not use Website as a header for multiple columns Required columns: Company Name Company URL Optional for Account Owner Mapping: Account Owner Email (required for account owner mapping) Account Owner Name (optional) Account Owner Phone (optional)
- A unique name
- Unique headers for each column For example, do not use Website as a header for multiple columns
- For example, do not use Website as a header for multiple columns
- Required columns: Company Name Company URL
- Company Name
- Company URL
- Optional for Account Owner Mapping: Account Owner Email (required for account owner mapping) Account Owner Name (optional) Account Owner Phone (optional)
- Account Owner Email (required for account owner mapping)
- Account Owner Name (optional)
- Account Owner Phone (optional)

✍️ Note
Rows with identical values in the Company Name and the Company Website columns will be flagged as duplicates and skipped.

Once you've mapped these required columns in Crossbeam, do not change them or your sync will return an error.

### Google Authentication
Only one user per org can authenticate, and they must use a Google Workspace email.

To connect Google Sheets:
- Click on Data from the navigation menu, select Data Sources from the dropdown
- Locate the Google Sheets tile and click on it
- Click Authenticate with Google
- Choose an organizational Google account (not a personal Gmail)

Make sure:
- That same user has access to every Google Sheet your team wants to connect
- Your team admin should ideally complete the authentication to ensure consistency and ownership

#### 💡 Having authentication trouble?
Reach out to your IT team with the following instructions:
- Log into admin.google.com using an account with sufficient privileges, such as Super Admin
- Navigate to: Security > API Controls > Manage Third-Party App Access Click Configure New App > OAuth App Name or Client ID
- Security > API Controls > Manage Third-Party App Access
- Click Configure New App > OAuth App Name or Client ID
- In the search field, type Crossbeam and click Search
- From the search results: Hover over Crossbeam and click Select
- Hover over Crossbeam and click Select
- On the next screen: Under Select OAuth Client IDs, check the box for all listed IDs Under Select Access Level, choose: Trusted: Can access all Google services
- Under Select OAuth Client IDs, check the box for all listed IDs
- Under Select Access Level, choose: Trusted: Can access all Google services
- Trusted: Can access all Google services
- Click Configure to apply the policy
✍️ Note
Crossbeam only requests access to Google Drive to sync and read Sheets. Crossbeam does not gain access to any other Google Workspace services.

### Add & Map Google Sheets
After authenticating:
- Navigate to Data Sources
- Click Add next to your Google Sheets connection
- Paste the Google Sheet URL and select the sheet tab from the dropdown
- Choose your Data Type : Companies or People
- Companies or
- People

- Map the columns for Company Name (Required) For Companies : map Company Name and Company Website For People : map Email
- For Companies : map Company Name and Company Website
- For People : map Email

Click Add Google Sheet to complete the setup.

#### Optional: Map Account Owner Data
If your sheet includes account owner details, you can map those fields in Crossbeam.
To do this:
- In the Data Sources list, locate your connected Google Sheet
- Click the settings gear icon next to the sheet
- Select Map Account Owner
- Map the following fields: Account Owner Email (required) Account Owner Name (optional) Account Owner Phone (optional)
- Account Owner Email (required)
- Account Owner Name (optional)
- Account Owner Phone (optional)
- Click Apply to save the mapping


### Manage Connected Sheets
Once your sheets are connected, you can manage them from Data Sources .
On the Google Sheets row:
- Click Add to a Google Sheet
- Click Sync Now to manually refresh
- Click the Settings gear icon to: Adjust sync frequency Reauthorize the connection Remove the data source View Connection Details
- Adjust sync frequency
- Reauthorize the connection
- Remove the data source
- View Connection Details
Click on the small arrow to the right of the data source name to display all of your uploaded sheets and their status. ​

Click the Settings gear icon to:
- Check Connection
- Add Field Mapping: Map Account Owner
- Adjust Sharing Presets
- Remove data source

Click Save when done.

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


## Add a Data Source (HC 6805089)
URL: https://help.crossbeam.com/en/articles/6805089-what-are-data-sources

Crossbeam works with your data source to create lists of prospects, opportunities, and customers. Crossbeam supports most popular data sources including CRMs, data warehouses, Google Sheets, and CSVs. No matter the source of your data, you have total control over the data in Crossbeam.

Need a visual walkthrough? Check out the video below:

Click on Data from the navigation menu. Select Data Sources from the dropdown options. Locate your Data Source and click on the tile name .
❗️ Important
No data is being shared at this point. This step is simply syncing your Data Source with Crossbeam. Later, you will be able to decide what to share (or not share) with your ecosystem.
🔗 Related Articles
- Data Sources Overview: CSVs, CRMS, and Data Warehouses
- Connect Salesforce Data
- Connect HubSpot Data
- Connect Microsoft Dynamics
- Connect Snowflake Data
- Google Sheets as a Data Source
- Upload a CSV File
🎓 Sign in to the Crossbeam Academy to learn more about Data Sources!

- Upload a CSV File and Map Your Fields
- Connect Snowflake Data
- Integrations Overview
- Data Sources Overview: CSVs, CRMs and Data Warehouses
- Connect Databricks as a Data Source


## Before You Begin (HC 6952388)
URL: https://help.crossbeam.com/en/articles/6952388-connect-microsoft-dynamics

Learn how to connect your Microsoft Dynamics data to Crossbeam.

In this article:
- Before You Begin
- Connect your Data Source
- Sync Data Options
- How to Customize Sync Fields Data Presets
- Data Presets
- Adjust Settings
Before connecting Microsoft Dynamics to Crossbeam, make sure the following requirements are met:


#### Admin Setup Required
A Microsoft Dynamics admin must complete the initial connection. Company admins should go to admin.microsoft.com to assign the correct permissions to the user setting up the integration.

The assigned user must have:
- A Microsoft Dynamics 365 license
- Read access to the following objects: Leads Accounts Contacts Opportunities
- Leads
- Accounts
- Contacts
- Opportunities
- Access level : Basic or higher
- API permissions, including the ability to: Generate access tokens Generate refresh tokens
- Generate access tokens
- Generate refresh tokens
- API view and configuration permissions enabled
If these permissions are not set correctly, the sync will fail or behave unexpectedly.
Once setup is complete and the connection is authorized, you'll be prompted to begin syncing your data into Crossbeam.

### Connect your Data Source
- From the navigation menu, click on Data and select Data Sources
- Scroll down and click Microsoft Dynamics

- Click Connect Microsoft Dynamics to confirm that you would like to create a Microsoft Dynamics connection
- Sign in to your Microsoft Dynamics instance After authentication, Crossbeam will begin preparing the connection ​
- After authentication, Crossbeam will begin preparing the connection ​


### Sync Data Options
Once Microsoft Dynamics is connected to Crossbeam, choose from the following sync options:
- Recommended : the best option for unlocking value from our full range of features
- Custom: Define a custom select of your data
Hover over each option to see the field names.

After selecting your syncing option, you will be prompted to review the fields. You can click Sync Now or Customize .


### How to Customize Sync Fields
- How to Customize Sync Fields: From the data source Microsoft Dynamics Settings, click Field Sync >Edit In the next window, expand any table under All Data by clicking the drop-down arrow, or use the search bar to locate specific fields Select or deselect any of the fields to customize your data You can also click the Toggle button to turn entire tables on or off Click Review Fields, then select Sync Now to complete the connection Or click Go Back to edit your changes before completing the sync
- From the data source Microsoft Dynamics Settings, click Field Sync >Edit
- In the next window, expand any table under All Data by clicking the drop-down arrow, or use the search bar to locate specific fields
- Select or deselect any of the fields to customize your data You can also click the Toggle button to turn entire tables on or off
- You can also click the Toggle button to turn entire tables on or off
- Click Review Fields, then select Sync Now to complete the connection
- Or click Go Back to edit your changes before completing the sync


#### Data Presets
Data Presets allow you to quickly add data that corresponds to direct use cases and Crossbeam functionality. After clicking the Customize button, Data Presets are located on the left side, highlighted in blue:
| Account Mapping: Compare your data with partners to identify overlapping prospects, opportunities, and customers | Pipeline Map: Accelerate opportunities and forecast revenue more accurately with more visibility into your partner's pipeline |
| Co-Market: Target overlapping prospects, opportunities, and customers for your better together stories and integration outreach | Co-Sell: Use your partner ecosystem to surface pre-vetted overlapping accounts that can shorten sales cycles and increase opportunity sizes |
Hover over the options to see the list of fields required.

After customizing your syncing option, click on Review fields . Confirm the sync by clicking on, Sync Now .

### Adjust Settings
On the Data Sources workspace, click on the Settings gear icon to:
- View Connection Status and Details: Check the connection status, error messages, and reauthorization requirements Reauthorization may be needed if user access or permissions have changed, and any errors will display here when available
- Reauthorization may be needed if user access or permissions have changed, and any errors will display here when available
- Adjust Data Sync Frequency : Use the Update Frequency dropdown to select how often Crossbeam syncs with Microsoft
- Edit Data Sync: Click Edit Data Sync to open the Customize pop-up, allowing you to add or remove specific fields
- Remove Data Source: Select Remove Data Source to disconnect Microsoft Dynamics from Crossbeam

🔗 Helpful Resources
For more information on assigning roles in Microsoft Dynamics, check out this helpful resource here .
- Connecting Salesforce as a Data Source
- Connect HubSpot Data
- Data Sources Overview: CSVs, CRMs and Data Warehouses
- What are Data Sources?
- Connect Databricks as a Data Source


## There's a Salesforce authorization error when connecting to Crossbeam. What Should I do? (HC 7197979)
URL: https://help.crossbeam.com/en/articles/7197979-salesforce-as-a-data-source-faqs

In this article:
- What are the required permissions to connect Salesforce to Crossbeam?
- What type of API does Crossbeam use to pull in Salesforce Data?
- For each bulk API, how many records does Crossbeam sync?
- We have concerns around the number of API calls. How does Crossbeam refresh updates from Salesforce? Does Crossbeam refresh every record or only recently updated records?
- Can we control what data from Salesforce is synced to Crossbeam?
- Why can't I select User types to sync in from Salesforce?
- When this feature is turned on, will I see the lookup fields for users immediately?
- How do I sync multiple User lookup fields?
- What fields do you recommend we import from Salesforce into Crossbeam?
- How does Crossbeam connect to Salesforce?
- What happens if I remove a Salesforce data field from being synced into Crossbeam?
- Can I import fields without sharing them with my partners?
- The field I'm looking for is missing!
- Why does the selected field say "Not Supported" next to it?
- There's a Salesforce authorization error when connecting to Crossbeam. What Should I do?
❗️Important
To sync Salesforce into Crossbeam, you'll need to have a plan that has API access. Salesforce has different Editions which are outlined here .

#### What are the required permissions to connect Salesforce to Crossbeam?
A Salesforce admin is required to have the following permissions to set up the initial Oauth:
- API enabled ( Required )
- View Setup and Configuration (Recommended)
- View all users (Recommended)
- Read access to Account OR Lead objects (Required)
The following fields are required:
-Id, Owner Id (for identifying records)
-Name, Website (for matching algorithm to find overlaps)
-IsDeleted, SystemModstamp, CreatedAt (for record-level bookkeeping)

#### What type of API does Crossbeam use to pull in Salesforce Data?
Bulk API 2.0. Instead of the REST API, we use a mechanism called the Bulk API 2.0 to sync data from Salesforce to Crossbeam. These are subject to different quotas than the standard Salesforce REST API.


#### For each bulk API, how many records does Crossbeam sync?
By default, we sync 10,000 records at a time. Reach out to support@crossbeam.com to customize your needs. <!-- VALIDATE-OK[person-address]: verbatim public Crossbeam Help Center text -->


#### We have concerns around the number of API calls. How does Crossbeam refresh updates from Salesforce? Does Crossbeam refresh every record or only recently updated records?
We will only pull records whose SystemModStamp changes after the initial sync. At the time of the initial sync, we pull everything from Salesforce. Upon completion of that initial sync, we “bookmark” the last time we synced. Subsequent syncs then pull records from Salesforce after that bookmark. ​ For example: 1) You connect Salesforce to Crossbeam 2) Our Salesforce sync feed for then pulls all records and sets a bookmark of say “July 11, 2022 6:00 am”, the date the time the initial sync was completed 3) On the next run (i.e. the frequency you selected when you connected Salesforce), our sync asks for records that have a SystemModStamp greater than July 11, 2022 4) This process repeats continuously

#### Can we control what data from Salesforce is synced to Crossbeam?
We can only access the data that the authorized user who is connecting Salesforce to Crossbeam has access to. If the authorized user has more limited permissions (i.e., only access to a certain subset of accounts/data), then that would be the only data that would be pulled into Crossbeam.

#### Why can't I select User types to sync in from Salesforce?
You must first select the Account Owner User type. Once that role is selected, you will now be able to select multiple User types and their contact details.

#### When this feature is turned on, will I see the lookup fields for users immediately?
The feed needs to sync again to see the Lookup Fields. The sync timing depends on your sync schedule, as you can select anywhere from 30 minutes to 24 hours in your Salesforce
settings.

#### How do I sync multiple User lookup fields?
- On the Data Sources, open the Salesforce settings
- Click Edit Data Sync and expand the arrow next to the User object
- Select Account Owner Name, Account Owner Phone, and Account Owner Email from the User object. The Account Owner fields must be selected in order to sync additional lookup fields
- The Account Owner fields must be selected in order to sync additional lookup fields
- Next, scroll to the Account or Lead object to select any additional User type or contact details

#### What fields do you recommend we import from Salesforce into Crossbeam?
Once Salesforce is connected to Crossbeam, choose from the following sync options:
- Recommended: the best option for unlocking value from our full range of features
- Custom: Define a custom select of your data
Hover over each option to see the field names.

After selecting your syncing option, you will be prompted to review the fields. You can click Sync Now or Customize .

For full details on syncing options, Data Presets, and how to customize sync fields, see Connecting Salesforce as a Data Source .

At any time, you may review or edit the fields on the Data Sources page. Locate the Salesforce row, click the Settings gear, and click Field Sync --> Edit .

#### How does Crossbeam connect to Salesforce?
Crossbeam uses OAuth authentication to connect to Salesforce. We don’t store credentials, just the OAuth token. That token is stored in an encrypted format in a database. The token is encrypted using AWS’s Key Management System (KMS) feature. You can disconnect the connection both in Crossbeam and in your own Salesforce at any time.

#### What happens if I remove a Salesforce data field from being synced into Crossbeam?
During the next sync, the master data is rewritten to include only fields selected for sync (plus any internally required fields, mainly some ID fields). This deletes the deselected field data from the master records Crossbeam uses to fuel populations.

#### Can I import fields without sharing them with my partners?
Yes! You should import all the fields necessary to filter reports. You may not share select fields with partners, but you can add them to overlap reports and filter partner data using your organization’s own values.

#### The field I am looking for is missing!
Check with your CRM administrator to ensure:
- The field still exists in your CRM
- Field-level security in your CRM is set to “read” for the user profile used to sync your data into Crossbeam
Once the field is available to Crossbeam again, go to your CRM settings in Crossbeam, and select the field you were missing.

#### Why does the selected field say “Not Supported” next to it?
Typically, the reason you are unable to pull in a field is because the user who initially authorized the Salesforce connection no longer has access to that field. To resolve this issue, you can either:
- Give that user the correct permissions
- Have someone with the correct permissions reauthorize the Salesforce connection
| Example Fields Not Supported: | Example Fields that are Supported: |
| Base64 | id |
| byte | string |
| anyType | picklist |
| calculated | phone |
| Address | URL |
| json | lookups (account to user, lead to user) |
| complexvalue | multi-selected picklists |
| formula | combo boxes |
| roll-up | encrypted strings |
| | emails |
| | master records |
| | text areas |
| | numbers |
| | dates and date/times |
| | booleans |
This can happen due to Salesforce’s September 2025 security update blocking “uninstalled” connected apps. For full troubleshooting steps, see our dedicated article: Troubleshooting Salesforce Authorization with Crossbeam .
- Connecting Salesforce as a Data Source
- Connect Snowflake Data
- Attribution for Salesforce Users
- Crossbeam for Sales Attribution FAQs
- Crossbeam Copilot for Salesforce FAQs


## Create a Population (HC 7239725)
URL: https://help.crossbeam.com/en/articles/7239725-custom-populations

Organize and segment any target accounts with Custom Populations.

In this article:
- Create a Population
- Build a Customized Population Apply Filters to Define Your Population
- Apply Filters to Define Your Population
- Set Sharing Defaults
- Manage Custom Populations Edit Population Type or Filter for a Custom Population
- Edit Population Type or Filter for a Custom Population
❗️ Important
Custom Populations are only available on Connector and Supernode plans . Visit the Billing page to upgrade your plan.
Click on Data from the navigation menu, select Populations from the dropdown options.
Click the Create Population button to open the Population Builder.


### Build a Customized Population
In the Population Builder:
- Name your Population
- Choose a Population Type (Customer, Open Opportunities, Prospects, Others.)
- Choose a Data Source from the dropdown
- Depending on your data source, select the specific Object
- Add a description (optional)

Click Continue.

#### Apply Filters to Define Your Population
- Under the Filters section, select fields to filter by
- Choose a comparison operator (e.g., is, contains, greater than, etc.)
- Enter a value to complete the filter
- You can add multiple filters to narrow your Population
- Use AND/OR logic between filter groups for more complex segmentation

Click Apply filter to preview the data.
Click Create Population when done.
✍️ Note
Available filter options will vary based on the data source and field type. Click here to explore the filter options.

### Set Sharing Defaults
After creating a Population, you will also be prompted to set default sharing settings for each new Population you create.

To fully understand sharing settings in Crossbeam, please click here .


### Manage Custom Populations
Select Data from the navigation bar and Populations from the dropdown options.
For each Population, you can:
- Click the pencil to open the Population Builder and adjust filters
- Click the three dot menu to adjust: sharing default, duplicate, delete, or export the Population


#### Edit a Population Type or Filter for a Custom Population
Assign a type to any Custom Population, helping Crossbeam better understand what that Population represents. This improves how your data is used across features.

How to assign a type:
- Click on Data from the navigation menu, select Populations from the dropdown options
- Locate the Custom Population and click the edit icon
- Under Details, adjust the Population type from the dropdown options

Under filters:
- click Add filter to apply more filters to the Population
- click the trashcan icon to remove a filter or click Delete Group to remove more complex filter groups

Select the Apply filters button to preview changes, click Save Changes when done.
✍️ Note
Population Types are an optional setting. You can leave a Population uncategorized by selecting Other .
🎓 Sign into Crossbeam Academy to further explore building Populations!
📄 Related Articles
- Building a Standard Population
- Editing a Population
- Advanced Population Filtering ​

- Create a Population from a CSV File
- Build a Standard Population
- How to Edit a Population
- Managing Population Settings
- How to Build a Product-Based Population Using Product2
