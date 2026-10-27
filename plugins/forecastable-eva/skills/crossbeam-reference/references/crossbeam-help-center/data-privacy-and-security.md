# Collection: Data Privacy And Security

Source: https://help.crossbeam.com/en/collections/1845471-data-privacy-and-security. Captured September 30th, 2026.


## Overview (HC 15297694)
URL: https://help.crossbeam.com/en/articles/15297694-understanding-crossbeam-ai-and-data-use

In this article:
- Overview
- AI-Powered Features
- What AI Does Not Do
- Data Use and Model Training
- Matching Engine
- Ecosystem Intelligence and Aggregated Insights
- Delivering the Product and Improving the Product
- Personal Data
- Responsibility and Ethics
- Third-Party AI Governance
- More Information
This article is provided for informational purposes only. It is not legal advice, not a contract, and does not create any legal rights or obligations. Capitalized terms refer to those defined in Crossbeam's Terms of Service.

Crossbeam is a business-to-business SaaS platform that enables companies to identify overlapping customers, opportunities, and prospects with their partners, while keeping the rest of their data private and protected. The data in Crossbeam is business-to-business CRM data, such as information related to your prospects, opportunities, and customers.

Crossbeam uses Customer Data to provide, support, and improve the Service. This Explainer describes specifically how Crossbeam uses AI and machine learning and data aggregations, and how Customer Data is protected in that context.


### AI-Powered Features
Crossbeam offers AI-powered features. They use OpenAI's API, and OpenAI is a listed subprocessor under Crossbeam's Data Processing Addendum (DPA). Below are examples of our two live features that use AI as of May 2026; we'll update as new features launch.


#### AI Chat
AI Chat is an in-product conversational interface that allows users to explore and navigate their ecosystem data using natural language. AI Chat is strictly read-only and assistive: it interprets data that the user already has access to within their existing permissions settings. It does not take actions on behalf of the user, such as editing sharing permissions, connecting with partners, managing team members, or modifying any account or integration settings. It is scoped to the authenticated user's access and permissions in Crossbeam.


#### AI Recommended Plays
AI Recommended Plays is an AI-powered feature that surfaces recommended partnership plays based on a user's ecosystem data and overlap signals. Like AI Chat, AI Recommended Plays operates within the user's existing permissions and does not modify data or take action on behalf of the user.

### What AI Does Not Do
To be explicit about the boundaries of AI functionality in Crossbeam:
- AI features do not make changes in the product on behalf of the user;
- Crossbeam does not review or pre-verify AI-generated outputs before they are shown to a user. AI Chat responses are generated in real time in response to user queries.

### Data Use and Model Training
Crossbeam's use of Customer Data in connection with AI features is limited as follows:
- Crossbeam does not train any large language models using Customer Data
- OpenAI processes prompts to generate real-time responses. OpenAI does not use Customer Data from Crossbeam to train its own models.
- Inputs and outputs from AI Chat interactions are retained in Crossbeam's AWS infrastructure as part of the user's session history, subject to Crossbeam's standard data retention and deletion practices.
- All Customer Data remains stored within Crossbeam's infrastructure on AWS US.

### Matching Engine
Crossbeam's Matching Engine is not an AI feature and does not currently use machine learning. It is built around a deterministic, facts-based framework that does not currently employ AI or LLMs in any way. Future iterations of the Matching Engine may incorporate ML or AI; we will update this document to reflect those changes.

The Matching Engine is the core system that determines when records from different organizations represent the same underlying entity, governing when partner data may be shared. The Matching Engine only accesses data that customers elect to sync to Crossbeam from their CRM, it does not access data that has not been explicitly synced. Matching occurs before any sharing takes place, which allows Crossbeam to calculate overlap counts (for example, "you have 300 overlaps with this partner") without any underlying data being shared with that partner. The fields used for matching are limited identifiers: primarily company domain and email address for accounts, and email address for leads and contacts, though this may expand over time as the Matching Engine evolves.

The Matching Engine normalizes and compares key identifiers such as company domain, email address, DUNS number, and phone number (more fields will be added in future releases - this document will update to reflect changes). If data points align according to defined comparison rules, a match is declared. If they do not, no match is declared. There is no probabilistic or model-driven inference: the outcome is a deterministic "yes" or "no" based on facts.

In some cases, the Matching Engine improves match quality by drawing on aggregated, network-derived signals. For example, helping resolve a record where a customer's CRM is missing a standard identifier. These signals are built only from fields that customers have synced to Crossbeam, incorporate no Personal Data, and are never surfaced to customers or partners as a product output; they are used solely to enable matching. The signals used and the methods used to derive them may evolve over time.


### Ecosystem Intelligence and Aggregated Insights
Ecosystem Intelligence (EI) is Crossbeam's proprietary analytics layer that generates insights and signals using aggregated, anonymized data across the Crossbeam network. EI is not an AI feature, but it is a meaningful part of how Crossbeam delivers the product, built on the network.


#### How aggregation and anonymization work
- EI is built only from data that customers have synced to Crossbeam. Fields that are not synced are never pulled into Crossbeam and therefore cannot contribute to EI. The relevant control for EI is sync, not share. Whether or not a customer shares a given field with a particular partner does not affect EI computation.
- If a customer is syncing CRM fields that contain Personal Data (see more on this in Section 8), then EI computation may use Personal Data (such as email addresses) as inputs to identify and aggregate records across the network. The outputs surfaced to customers (the insights and signals themselves) do not contain Personal Data. EI insights take two forms: insights on Accounts (for example, signals related to recent deal activity on a given company) and insights on Contacts. Contact insights are categorical tags such as 'Economic Buyer' or 'Decision Maker' derived from aggregated deal and activity patterns; no contact-level Personal Data fields (such as name or email address) are exposed through EI insights.
- Each insight is only surfaced when a minimum number of underlying data points exist across distinct organizations. Below that threshold, no insight is shown. This is what makes an insight anonymous: it cannot be traced back to any single organization's contribution.
- Access to EI follows the same permission model as all other data in Crossbeam. A user will only see an insight on an Account or Contact they already have access to either through their own synced data or through an explicit partner share. If a contact or account is not accessible to a user, neither the record nor any associated insights will be visible.

### Delivering the Product and Improving the Product
A common customer question is whether Crossbeam uses data only to deliver the product to that customer, or also to improve the product more broadly.

For AI features (e.g. AI Chat and Recommended Plays), Customer Data is used only to fulfill real-time requests. It is not retained or used to improve the product.

For network-level features like Ecosystem Intelligence, the product value is inseparable from the aggregate network. These features deliver insights to a customer that are derived from the broader Crossbeam network, which is itself built from data contributed by all customers. Crossbeam's ability to deliver EI to any individual customer depends on the aggregated contributions of the network. Note that these features use only aggregated Customer Data and that no individual customer's data is ever surfaced in identifiable form to another customer through these features.

### Personal Data
Crossbeam can be used without sharing any Personal Data with partners. If a customer chooses to include Personal Data fields (such as contact names, email addresses, titles, or phone numbers) in their CRM sync, Crossbeam's granular controls make it easy to exclude those fields from partner sharing at any time.

Crossbeam does not use Personal Data to create independent lead lists or to provide net-new Personal Data to other organizations.

### Responsibility and Ethics
Crossbeam's current AI features are assistive: they help users navigate and interpret data they already have access to within their existing permissions. They do not introduce net-new data, expand sharing permissions, or surface Personal Data outside the scope of a user's own query.

Crossbeam does not use AI to score, profile, or make automated decisions that produce legal or similarly significant effects on individuals.

From a regulatory standpoint, as currently configured, Crossbeam's AI features are not subject to the automated decision-making restrictions under GDPR Article 22 because they do not produce decisions that have legal or similarly significant effects on individuals; a human user interprets and acts on all outputs. Under the EU AI Act, Crossbeam's AI features fall within the minimal risk tier: they are not used in any high-risk context enumerated under Annex III (such as employment, credit, education, or law enforcement), and they are not general-purpose AI systems subject to transparency obligations under Title IV. Under CCPA/CPRA, Crossbeam's AI does not engage in profiling to produce legal or similarly significant effects, and no automated decision-making opt-out right is triggered. Similarly, under the Colorado AI Act (SB 24-205) and analogous state-level frameworks, Crossbeam's AI does not constitute a high-risk AI system because it does not make or substantially influence consequential decisions about consumers.

Crossbeam expects AI capabilities to expand over time. This may include features that take actions in-product on behalf of users. For example, agentic workflows that coordinate multi-step partner interactions or initiate routine tasks. For any such capability, Crossbeam will: keep users in the loop for actions that materially affect data sharing or security; reassess each of the regulatory frameworks above before deployment; and update this Explainer to reflect the new capability and any new subprocessors involved.

Across current and future AI features, Crossbeam holds to a consistent set of principles: Customer Data is not used to train Crossbeam's own models or those of its AI providers; access to AI features follows the same permission model as the rest of the product.

### Third-Party AI Governance
Crossbeam currently uses one external AI provider: OpenAI, accessed via API. OpenAI is a listed subprocessor under Crossbeam's Data Processing Addendum and is subject to contractual obligations governing how Customer Data may be processed. Under Crossbeam's agreement with OpenAI, Customer Data is processed to fulfill real-time requests and is not used to train OpenAI's models.

Crossbeam evaluates AI tools and providers as part of its vendor risk management program prior to deployment. This includes review of the provider's data processing terms, subprocessor status, security posture, and model training commitments before any integration with Customer Data is permitted. Ongoing vendor relationships, including OpenAI, are subject to periodic review. Any new AI provider that would process Customer Data would be added to Crossbeam's subprocessor list with advance notice to customers in accordance with the DPA.

### More Information
For more detail on Crossbeam's data privacy and security practices, please refer to:
- Crossbeam's Data Sharing White Paper : detailed guidance on data sharing controls
- Crossbeam's Trust Center : comprehensive information on security and privacy practices
- Crossbeam's DPA : the Data Processing Addendum governing Customer Data processing
- Understanding Partner Score in Crossbeam
- Crossbeam Overview for Compliance Teams
- Crossbeam MCP Server


## You Can Put Your Trust in Crossbeam (HC 3160400)
URL: https://help.crossbeam.com/en/articles/3160400-data-privacy

The trust in your partners is core to our business. Companies need a secure and compliant way to ensure when you partner with your ecosystem; your data and your partner’s data is secure. From day one, we have prioritized the security of your data to ensure trust is the primary focus.
❗️ Important
Click here to learn about our Internationally-recognized ISO/IEC 27001 and 27701 information security and data privacy certifications.
✍️ Note
Crossbeam does not sell customer data.

For more information, please review our Terms of Service here .

#### Purpose-built for partner data sharing.
A security and privacy-first platform: We know your data is important, so we designed our platform with privacy and security top of mind. For more details, see https://security.crossbeam.com /.

Smart data sharing: Our powerful data sharing features are built around the concept of “overlaps”: companies or contacts that are known to both Partners in a partnership. You can share as much information as you want about the companies you have in common, while keeping everything else private.


#### Granular control over your data, at multiple levels. You control:
The data you import into Crossbeam: Whether connecting to a CRM or uploading a raw CSV file, you control what data goes into Crossbeam, at the individual field level.

The data that will be shared: Crossbeam never automatically shares the raw data you import. Instead, we only share your “Populations”: curated subsets of your raw data, filtered to include or exclude data based on any attribute you choose.

The specific data you share with each Partner: For each Population you select to share with a Partner, Crossbeam lets you set rules about which fields of data you want to share when specific matching conditions are met, on a Partner-by-Partner basis.


#### Transparency into your data at all times.
You control your Partners : Partnerships on Crossbeam are dual opt-in relationships: one company sends an invite that the other must accept before any data can be shared.

You set the rules before any data is shared: Even once you establish a partnership, Crossbeam won’t share any of your data with your new Partner until you have proactively confirmed or configured your data sharing rules for that Partner.

You have full transparency: Crossbeam provides powerful reporting tools that let you see how much of your data is being shared, along with the partners that are receiving it, and how your data sharing rules are being applied.
✍️ Note
Crossbeam offers a Data Processing Addendum (DPA) which incorporates Standard Contractual Clauses (SCCs) as a means of meeting the regulatory contractual requirements of GDPR in our role as processor and also to address international data transfers.
Our DPA sets out the basis on which Crossbeam processes Customer Personal Data. An up-to-date listing of Crossbeam’s sub-processors can be accessed here .

📄 Related Articles
- Crossbeam Overview for Compliance Teams
- Security

#### 
- What is Partnerbase?
- Data Security Policies for Crossbeam Employees
- Data Sharing Guide
- Data Privacy FAQ


## You Can Put Your Trust in Crossbeam (HC 3160445)
URL: https://help.crossbeam.com/en/articles/3160445-security

The trust in your partners is core to our business. Companies need a secure and compliant way to ensure when you partner with your ecosystem; your data and your partner’s data is secure. From day one, we have prioritized the security of your data to ensure Trust is the primary focus.
✍️ Note
Crossbeam does not sell customer data. For more information, please review our Terms of Service here .
Our Chief Information Security Officer Chris Castaldo offers a 101 overview of Crossbeam Security in this 19-minute on-demand webinar .

For a high-level overview of our program, please visit:
The Crossbeam Trust Center .

You can also watch this 1-minute video to learn more: ​
For a deeper dive, and to gain access to more comprehensive security and compliance details including requesting our SOC 2 Type II report, please visit: https://security.crossbeam.com/ . You can also check out this 3-minute video to learn more. ​
In addition, our Security Policy is incorporated into our agreements with all customers. We use a single platform to provide Crossbeam to all our customers, so operationally we can't accept bespoke security requirements for individual customers. Our Security Policy documents our security practices and is part of our terms, and we are happy to provide additional information on request. Contact privacy@crossbeam.com . <!-- VALIDATE-OK[person-address]: verbatim public Crossbeam Help Center text -->

📄 Related Articles
- Crossbeam Overview for Compliance Teams
- Data Privacy
- Data Security Policies for Crossbeam Employees
- Company Verification
- Installation Guide: Crossbeam for Salesforce (v2)
- Crossbeam Overview for Compliance Teams
- Crossbeam MCP Server


## 3160458-data-security-policies-for-crossbeam-employees.html (HC 3160458)
URL: https://help.crossbeam.com/en/articles/3160458-data-security-policies-for-crossbeam-employees

The trust in your partners is core to our business. Companies need a secure and compliant way to ensure when you partner with your ecosystem; your data and your partner’s data is secure. From day one, we have prioritized the security of your data to ensure Trust is the primary focus.
✍️ Note
Visit the Security Portal here to gain access to the most recent and sensitive security details at Crossbeam.

#### Systems Access
Crossbeam employee access to our internal vendor systems is granted based on least privileges. Employees are granted privileges to any system only as needed to perform their role. Access is tracked and audited quarterly. Crossbeam’s production environment is accessed via SSH. The production SSH server is firewalled to restrict access outside our VPN. Production database access is then accessed via username/password authentication. SSH access is protected by Duo MFA and uses key-based authentication.


#### Internal policies
Crossbeam Employee Policies and Procedures: All Crossbeam employees are required to follow strict procedures to ensure your data remains secure. Additionally, Crossbeam educates employees on an ongoing basis on their role in protecting your data.

Security policies, privacy policies, disaster recovery plan, incident response plan, and any other pertinent documents related to privacy and security are reviewed, at minimum, on a quarterly basis by Crossbeam’s Security and Disaster Management Committee.
📄 Related Articles
- Crossbeam Overview for Compliance Teams
- Data Privacy
- Security
- Crossbeam Overview for Compliance Teams
- Crossbeam MCP Server
- Understanding Crossbeam AI and Data Use


## What is Company Verification? (HC 3935700)
URL: https://help.crossbeam.com/en/articles/3935700-company-verification

The trust in your partners is core to our business. Companies need a secure and compliant way to ensure when you partner with your ecosystem; your data and your partner’s data is secure. From day one, we have prioritized the security of your data to ensure Trust is the primary focus.
✍️ Note
Visit the Security Portal here to gain access to the most recent and sensitive security details at Crossbeam.
We take a few additional steps when anyone creates an account so that we can keep our customers confident in the validity of companies they're partnering with on Crossbeam.

Crossbeam performs an automated verification process to ensure that people who register belong to the company they claim. This is so we're confident we're providing a secure environment for you to trust who you're partnering with on Crossbeam.


### How do we perform Company Verification?
We perform automated verification using a multistep process that incorporates the information you provided when registering and some third party data.


### What does this mean for me as a Crossbeam user?
Ideally, you never know this even happened. If you pass automatic verification, the process is instant and invisible during registration. If you do not pass auto-verification, your account will be put into a queue to be manually verified by a Crossbeam team member. You will be blocked from using the Crossbeam app until we verify you belong to the company you are registering for.
❗️ Important
While this system helps us keep our network in check, you are still responsible for only accepting partnerships with known partners and verifying their legitimacy before sharing data or other information.

- Security
- Data Security Policies for Crossbeam Employees
- Installation Guide: Crossbeam for Salesforce (v2)
- Crossbeam Overview for Compliance Teams


## Overview (HC 6172688)
URL: https://help.crossbeam.com/en/articles/6172688-audit-logs

In this article:
- Overview
- How to Export Your Audit Logs
- Audit Logs Data
- FAQ

Audit Logs empower your cybersecurity and compliance teams to:
- Quickly Gain Usage Insights : Download a timeline of all actions within Crossbeam to understand their impact on partners and users.
- Effortlessly Scale Compliance : Access essential data as your partner network grows to maintain compliance.
- Ensure Data Governance : Monitor historical changes in data management, sharing, partnerships, populations, team invitations, and user roles.
✍️ Note
This is available on our Supernode Plan.

To upgrade your account, visit the Plan & Billing page .

### How to Export Your Audit Logs
From the Crossbeam Settings :
- Select Organizational Settings
- Scroll down to the Audit Logs section
- Select a date range for your Audit Log export
Click the Export CSV button.

You will receive an email to download a CSV file of your audit history for the date range you have selected.

Once you've downloaded your CSV export, you can export it to Google Sheets or Excel to review your audit history.
✍️ Note
You can export historical actions that have occurred since May 28th, 2021 to a CSV file. The following fields may be missing in audit log exports because Crossbeam didn’t start tracking this data until May 11, 2022: metadata, previous state, users impacted, organizations impacted, IP address.

### Audit Logs Data
| Data source connection(s) changes Removed a data source Synced additional fields Connected a data source Removed fields being synced Connection status changes Update frequency changes Established connection was reauthorized ​ | Data sharing defaults/settings changes Which population was affected Which partners were impacted by the change Date/time the change was made What the sharing default/setting was before and what it is now Who made the change (User or system account associated with an event) |
- Removed a data source
- Synced additional fields
- Connected a data source
- Removed fields being synced
- Connection status changes
- Update frequency changes
- Established connection was reauthorized ​
- Which population was affected
- Which partners were impacted by the change
- Date/time the change was made
- What the sharing default/setting was before and what it is now
- Who made the change (User or system account associated with an event)
| Partnership invites Date/time invite was accepted/sent Who made the change (User or system account associated with an event) | Population changes What field(s) was previously included/excluded Date/time the change was made Which partners were impacted by this change Who made the change (User or system account associated with an event) |
- Date/time invite was accepted/sent
- Who made the change (User or system account associated with an event)
- What field(s) was previously included/excluded
- Date/time the change was made
- Which partners were impacted by this change
- Who made the change (User or system account associated with an event)
| Integrations Activity Who installed, updated, or removed an integration Date/time the integration was installed, updated, or removed What action was taken: installed, updated, or removed Which integration was impacted | User role changes If the role was updated What were the changes made Date/time the change was made/role was created Who made the change (User or system account associated with an event) ​ |
- Who installed, updated, or removed an integration
- Date/time the integration was installed, updated, or removed
- What action was taken: installed, updated, or removed
- Which integration was impacted
- If the role was updated
- What were the changes made
- Date/time the change was made/role was created
- Who made the change (User or system account associated with an event) ​
| Team invites and users Date/time invite was sent or user was deleted Who sent the invite or deleted the user (User or system account associated with an event) Successful user logins Failed login attempts User logout events | Additional data Export Report Data Activity Date - the date and time the action took place (times will be in UTC) IP Address User - the name of the user who completed the action User Email Address - the email address of the user who completed the action Metadata - specific details about the completed action (i.e. If a user created a population, the metadata will tell you the population name, the data source it's pulling from, and what filters are applied) Previous State - what the data was before a user changed it Partner(s) Impacted - the names of the partner(s) impacted User(s) Impacted - The ID, name, and email of user(s) impacted by changes to user roles or permissions and new users/removed users on the Team page. |
- Date/time invite was sent or user was deleted
- Who sent the invite or deleted the user (User or system account associated with an event)
- Successful user logins
- Failed login attempts
- User logout events
- Export Report Data
- Activity Date - the date and time the action took place (times will be in UTC)
- IP Address
- User - the name of the user who completed the action
- User Email Address - the email address of the user who completed the action
- Metadata - specific details about the completed action (i.e. If a user created a population, the metadata will tell you the population name, the data source it's pulling from, and what filters are applied)
- (i.e. If a user created a population, the metadata will tell you the population name, the data source it's pulling from, and what filters are applied)
- Previous State - what the data was before a user changed it
- Partner(s) Impacted - the names of the partner(s) impacted
- User(s) Impacted - The ID, name, and email of user(s) impacted by changes to user roles or permissions and new users/removed users on the Team page.

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


## 6596903-crossbeam-open-source-disclosure.html (HC 6596903)
URL: https://help.crossbeam.com/en/articles/6596903-crossbeam-open-source-disclosure

✍️ Note
Visit the Security Portal here to gain access to the most recent and sensitive security details at Crossbeam.
Some software components of the Crossbeam platform incorporate software licensed under the open source licenses listed below. Crossbeam does not necessarily use all the open source software referred to below and may also only use portions of a given package. With respect to the open source software listed in this document, if you (i) have any questions, (ii) wish to receive source code for packages under licenses that require their source code to be made available, or (iii) discover any errors or omissions in the licensing information provided, please contact us at legal@crossbeam.com . Please identify in source code requests: (i) the packages for which you are requesting corresponding source; and (ii) an email address (if available) or postal address at which Crossbeam may contact you. <!-- VALIDATE-OK[person-address]: verbatim public Crossbeam Help Center text -->

| Component | Version | License | Source |
| @ag-grid-community/client-side-row-model | 32.3.5 | MIT | https://github.com/ag-grid/ag-grid |
| @ag-grid-community/core | 32.3.5 | MIT | https://github.com/ag-grid/ag-grid |
| @ag-grid-community/styles | 32.3.5 | MIT | https://github.com/ag-grid/ag-grid |
| @ag-grid-community/vue3 | 32.3.5 | MIT | https://github.com/ag-grid/ag-grid |
| @ag-grid-enterprise/server-side-row-model | 32.3.5 | Commercial | https://github.com/ag-grid/ag-grid |
| @crossbeam/bitts | workspace:* | | |
| @crossbeam/pointbreak | workspace:* | | |
| @crossbeam/types | workspace:* | | |
| @datadog/browser-rum | 4.50.1 | Apache-2.0 | https://github.com/DataDog/browser-sdk |
| @fortawesome/vue-fontawesome | 3.0.6 | MIT | https://github.com/FortAwesome/vue-fontawesome |
| @getoutreach/extensibility-sdk | 1.1.5 | UNKNOWN | |
| @highlightjs/vue-plugin | 2.1.0 | BSD-3-Clause | |
| @itly/plugin-iteratively | 2.4.0 | MIT | https://github.com/amplitude/itly-sdk |
| @itly/plugin-schema-validator | 2.4.0 | MIT | https://github.com/amplitude/itly-sdk |
| @itly/plugin-segment | 2.4.0 | MIT | https://github.com/amplitude/itly-sdk |
| @itly/sdk | 2.4.0 | MIT | https://github.com/amplitude/itly-sdk |
| @storybook/vue3-vite | 10.0.7 | MIT | https://github.com/storybookjs/storybook |
| @tailwindcss/postcss | 4.1.16 | MIT | https://github.com/tailwindlabs/tailwindcss |
| @tanstack/vue-virtual | 3.13.18 | MIT | https://github.com/TanStack/virtual |
| @unhead/vue | ^3.1.4 | MIT | https://github.com/unjs/unhead |
| @vee-validate/rules | 4.13.1 | MIT | https://github.com/logaretm/vee-validate |
| @vitejs/plugin-vue | 6.0.3 | MIT | https://github.com/vitejs/vite-plugin-vue |
| @vuelidate/core | 2.0.0 | MIT | https://github.com/vuelidate/vuelidate |
| @vuelidate/validators | 2.0.0 | MIT | https://github.com/vuelidate/vuelidate |
| @vueuse/core | 12.5.0 | MIT | https://github.com/vueuse/vueuse |
| @zxcvbn-ts/core | 3.0.4 | MIT | https://github.com/zxcvbn-ts/zxcvbn |
| @zxcvbn-ts/language-common | 3.0.4 | MIT | https://github.com/zxcvbn-ts/zxcvbn |
| @zxcvbn-ts/language-en | 3.0.2 | MIT | https://github.com/zxcvbn-ts/zxcvbn |
| ant-design-vue | 4.2.6 | MIT | https://github.com/vueComponent/ant-design-vue |
| auth0-js | 10.0.0 | MIT | https://github.com/auth0/auth0.js |
| autoprefixer | 10.4.17 | MIT | https://github.com/postcss/autoprefixer |
| axios | 1.12.2 | MIT | https://github.com/axios/axios |
| boto | 2.49.0 | Other | https://github.com/boto/boto/ |
| camel-snake-kebab | 0.4.2 | Eclipse Public License | https://github.com/clj-commons/camel-snake-kebab |
| canvas-confetti | 1.9.2 | ISC | https://github.com/catdad/canvas-confetti |
| chart.js | 4.4.7 | MIT | https://github.com/chartjs/Chart.js |
| chartjs-plugin-datalabels | 2.2.0 | MIT | https://github.com/chartjs/chartjs-plugin-datalabels |
| cheshire | 6.1.0 | The MIT License | https://github.com/dakrone/cheshire |
| cheshire/cheshire | 6.0.0 | The MIT License | https://github.com/dakrone/cheshire |
| cider/cider-nrepl | 0.23.0 | Eclipse Public License | https://github.com/clojure-emacs/cider-nrepl |
| cli-matic | 0.3.11 | Eclipse Public License, v2 | https://github.com/l3nz/cli-matic |
| clj-bom | 0.1.2 | Eclipse Public License | https://github.com/jimpil/clj-bom |
| clj-http | 3.9.1 | The MIT License | https://github.com/dakrone/clj-http |
| clj-http-fake | 1.0.3 | MIT License | https://codeberg.org/valpackett/clj-http-fake |
| clj-time | 0.15.2 | MIT License | https://github.com/clj-time/clj-time |
| clojure-csv/clojure-csv | 2.0.2 | UNKNOWN | https://github.com/davidsantiago/clojure-csv |
| com.amazonaws/aws-java-sdk-kms | 1.11.714 | UNKNOWN | https://aws.amazon.com/sdkforjava |
| com.amazonaws/aws-java-sdk-s3 | 1.11.714 | UNKNOWN | https://aws.amazon.com/sdkforjava |
| com.amazonaws/aws-java-sdk-sts | 1.11.714 | UNKNOWN | https://aws.amazon.com/sdkforjava |
| com.cemerick/url | 0.1.1 | Eclipse Public License | https://github.com/cemerick/url |
| com.cognitect.aws/api | 0.8.741 | Apache License 2.0 | http://github.com/cognitect-labs/aws-api |
| com.cognitect.aws/ec2 | 847.2.1387.0 | Apache License 2.0 | http://github.com/cognitect-labs/aws-api |
| com.cognitect.aws/endpoints | 1.1.12.504 | Apache License 2.0 | http://github.com/cognitect-labs/aws-api |
| com.cognitect.aws/es | 847.2.1387.0 | Apache License 2.0 | http://github.com/cognitect-labs/aws-api |
| com.cognitect.aws/kms | 848.2.1413.0 | Apache License 2.0 | http://github.com/cognitect-labs/aws-api |
| com.cognitect.aws/monitoring | 847.2.1387.0 | Apache License 2.0 | http://github.com/cognitect-labs/aws-api |
| com.cognitect.aws/rds | 847.2.1387.0 | Apache License 2.0 | http://github.com/cognitect-labs/aws-api |
| com.cognitect.aws/sts | 847.2.1387.0 | Apache License 2.0 | http://github.com/cognitect-labs/aws-api |
| com.datadoghq/dd-trace-api | 0.95.0 | Apache License 2.0 | https://github.com/datadog/dd-trace-java |
| com.draines/postal | 2.0.3 | MIT | https://github.com/drewr/postal |
| com.fzakaria/slf4j-timbre | 0.3.19 | Eclipse Public License | https://github.com/fzakaria/slf4j-timbre |
| com.github.em-schmidt/aws-sso | 9e5118640b4fee597d5485c92dddfb660424ef2d | UNKNOWN | https://github.com/em-schmidt/aws-sso |
| com.github.seancorfield/honeysql | 2.2.861 | Eclipse Public License | https://github.com/seancorfield/honeysql |
| com.github.seancorfield/next.jdbc | 1.3.925 | Eclipse Public License | https://github.com/seancorfield/next-jdbc |
| com.grammarly/perseverance | 0.1.3 | Apache License, Version 2.0 | https://github.com/grammarly/perseverance |
| com.grzm/awyeah-api | d98a9f6210c61d64f22e9b577d2254d6f6d2f35f | Apache License 2.0 | https://github.com/grzm/awyeah-api |
| com.mchange/c3p0 | 0.10.0 | UNKNOWN | https://www.mchange.com/projects/c3p0 |
| com.stuartsierra/component | 0.4.0 | The MIT License | https://github.com/stuartsierra/component |
| com.taoensso/timbre | 6.3.1 | Eclipse Public License - v 1.0 | https://github.com/taoensso/timbre |
| compojure | 1.7.0 | Eclipse Public License | https://github.com/weavejester/compojure |
| dayjs | 1.11.10 | MIT | https://github.com/iamkun/dayjs |
| dom-to-image | 2.6.0 | MIT | https://github.com/tsayen/dom-to-image |
| dompurify | 3.2.6 | (MPL-2.0 OR Apache-2.0) | https://github.com/cure53/DOMPurify |
| eftest | 0.5.9 | Eclipse Public License | https://github.com/weavejester/eftest |
| eventemitter3 | 4.0.7 | MIT | https://github.com/primus/eventemitter3 |
| fastapi | 0.115.6 | MIT License | https://github.com/fastapi/fastapi |
| highlight.js | 11.9.0 | BSD-3-Clause | https://github.com/highlightjs/highlight.js |
| honeysql/honeysql | 1.0.461 | Eclipse Public License | https://github.com/seancorfield/honeysql |
| html2canvas | 1.4.1 | MIT | https://github.com/niklasvh/html2canvas |
| humanize-plus | 1.8.2 | MIT | https://github.com/HubSpot/humanize |
| interactjs | 1.10.27 | MIT | https://github.com/taye/interact.js |
| io.github.em-schmidt/bblf | e08d9f7b40f8d4e65baa074c14743b6e62fc73b8 | Other | https://github.com/em-schmidt/bblf |
| io.github.nextjournal/clerk | 0.17.1102 | ISC License | http://github.com/nextjournal/clerk |
| jonase/eastwood | 0.3.5 | Eclipse Public License | https://github.com/jonase/eastwood |
| jsvat | 2.5.3 | MIT | https://github.com/se-panfilov/jsvat |
| lein-ancient | 0.6.15 | MIT License | https://codeberg.org/xsc/lein-ancient |
| lein-eftest | 0.5.7 | Eclipse Public License | https://github.com/weavejester/eftest |
| lein-zprint | 1.2.9 | MIT License | https://github.com/kkinnear/lein-zprint |
| lodash | 4.17.21 | MIT | https://github.com/lodash/lodash |
| luposlip/json-schema | 0.4.5 | Apache License, Version 2.0 | https://github.com/luposlip/json-schema |
| luxon | 3.4.4 | MIT | https://github.com/moment/luxon |
| lz-string | 1.5.0 | MIT | https://github.com/pieroxy/lz-string |
| migratus | 1.2.7 | Apache License, Version 2.0 | https://github.com/yogthos/migratus |
| nilenso/honeysql-postgres | 0.4.112 | Eclipse Public License | https://github.com/nilenso/honeysql-postgres |
| nrepl | 0.6.0 | Eclipse Public License | https://github.com/nrepl/nrepl |
| nrepl/nrepl | 1.1.0 | Eclipse Public License | https://github.com/nrepl/nrepl |
| org.apache.commons/commons-text | 1.9 | UNKNOWN | https://commons.apache.org/proper/commons-text |
| org.babashka/http-client | 0.4.22 | MIT License | https://github.com/babashka/http-client |
| org.clojure/algo.generic | 0.1.3 | Eclipse Public License 1.0 | https://github.com/clojure/algo.generic |
| org.clojure/clojure | 1.11.1 | UNKNOWN | http://clojure.org/ |
| org.clojure/core.memoize | 0.8.2 | Eclipse Public License 1.0 | http://github.com/clojure/core.memoize |
| org.clojure/data.codec | 0.1.1 | Eclipse Public License 1.0 | https://github.com/clojure/data.codec |
| org.clojure/data.csv | 1.0.1 | Eclipse Public License 1.0 | https://github.com/clojure/data.csv |
| org.clojure/java.jdbc | 0.7.11 | Eclipse Public License 1.0 | https://github.com/clojure/java.jdbc |
| org.clojure/math.combinatorics | 0.1.6 | Eclipse Public License 1.0 | https://github.com/clojure/math.combinatorics |
| org.clojure/math.numeric-tower | 0.0.4 | Eclipse Public License 1.0 | https://github.com/clojure/math.numeric-tower |
| org.clojure/test.check | 0.10.0 | UNKNOWN | https://github.com/clojure/build.poms |
| org.jsoup/jsoup | 1.15.1 | UNKNOWN | https://jsoup.org/ |
| org.postgresql/postgresql | 42.7.3 | UNKNOWN | https://jdbc.postgresql.org |
| path | 0.12.7 | MIT | https://github.com/jinder/path |
| path-to-regexp | 8.2.0 | MIT | https://github.com/pillarjs/path-to-regexp |
| peridot | 0.5.4 | Eclipse Public License | https://github.com/xeqi/peridot |
| pinia | 2.2.1 | MIT | https://github.com/vuejs/pinia |
| posthog-js | 1.367.0 | SEE LICENSE IN LICENSE | https://github.com/PostHog/posthog-js |
| potemkin | 0.4.5 | UNKNOWN | https://github.com/clj-commons/potemkin |
| pymysql | 1.1.1 | UNKNOWN | |
| qs | 6.9.4 | BSD-3-Clause | https://github.com/ljharb/qs |
| ring/ring-core | 1.8.0 | The MIT License | https://github.com/ring-clojure/ring |
| ring/ring-jetty-adapter | 1.8.0 | The MIT License | https://github.com/ring-clojure/ring |
| ring/ring-json | 0.5.1 | The MIT License | https://github.com/ring-clojure/ring-json |
| ring/ring-mock | 0.4.0 | The MIT License | https://github.com/ring-clojure/ring-mock |
| selmer | 1.12.18 | Eclipse Public License | https://github.com/yogthos/Selmer |
| software.amazon.awssdk/sso | 2.27.7 | UNKNOWN | https://aws.amazon.com/sdkforjava |
| software.amazon.awssdk/ssooidc | 2.27.7 | UNKNOWN | https://aws.amazon.com/sdkforjava |
| storybook | 10.2.10 | MIT | https://github.com/storybookjs/storybook |
| tailwindcss | 4.1.16 | MIT | https://github.com/tailwindlabs/tailwindcss |
| test2junit | 1.4.2 | Eclipse Public License | https://github.com/ruedigergad/test2junit |
| ts-md5 | 1.2.7 | MIT | https://github.com/cotag/ts-md5 |
| turndown | 7.2.2 | MIT | https://github.com/mixmark-io/turndown |
| uuid | ^11.1.1 | MIT | https://github.com/uuidjs/uuid |
| v-clipboard | 3.0.0-next.1 | MIT | https://github.com/euvl/v-clipboard |
| valid-url | 1.0.9 | UNKNOWN | https://github.com/ogt/valid-url |
| vee-validate | 4.13.1 | MIT | https://github.com/logaretm/vee-validate |
| viesti/timbre-json-appender | 0.2.5 | MIT License | https://github.com/viesti/timbre-json-appender |
| vue | 3.5.12 | MIT | https://github.com/vuejs/core |
| vue-chartjs | 5.3.2 | MIT | https://github.com/apertureless/vue-chartjs |
| vue-router | 4.4.3 | MIT | https://github.com/vuejs/router |
| vue-tsc | 2.1.6 | MIT | https://github.com/vuejs/language-tools |
| vue3-click-away | 1.2.4 | MIT | https://github.com/VinceG/vue-click-away |
| vuedraggable | 4.1.0 | MIT | https://github.com/SortableJS/Vue.Draggable |
| vuetify | 3.6.9 | MIT | https://github.com/vuetifyjs/vuetify |
| vuex | 4.1.0 | MIT | https://github.com/vuejs/vuex |
| vuex-map-fields | 1.4.0 | MIT | https://github.com/maoberlehner/vuex-map-fields |


## About Crossbeam (HC 9956727)
URL: https://help.crossbeam.com/en/articles/9956727-crossbeam-overview-for-compliance-teams

In this article:
- About Crossbeam
- How it works Example
- Example
- Required Data
- Recommended Data

Crossbeam allows partners to identify mutual prospects, opportunities, and customers by syncing data sources (e.g. CRMs like Hubspot and Salesforce) and then selecting certain data from those synced sources to share with partners, if applicable. Each partnership on Crossbeam is a dual opt-in relationship. Nothing is shared automatically.

More than 30,000 companies use Crossbeam (including Fortune 500 and publicly traded companies) to build more effective partnerships and help their sales team collaborate on deals and discover new prospects.

Crossbeam allows users to apply granular controls to define precisely what data is shared, and which partners can access it.


### How It Works
- Users register an account and connect with partners via a dual opt-in invitation: both parties must agree to work together on the platform.
- Users upload a spreadsheet or connect a CRM and choose a selection of data to work with. At this point, nothing has been shared.
- Users organize the data into segments of data (e.g. “Customers” and/or “Prospects”) and select the partners they’d like to compare segments with. Here too, nothing is shared during this phase.
- Users define what happens when there is a mutual account (“match”) across segments: Sharing Data: At this point, users can define which specific fields from the synced and organized data that they wish to share.
- Sharing Data: At this point, users can define which specific fields from the synced and organized data that they wish to share.
OR
- Counts Only: Users can also elect to share only the number of matches with a partner (without sharing any underlying data).
- Segments can be hidden/revoked from a partner at any time.
- Data can be removed from Crossbeam at any time.
These controls give users flexibility to deploy partnering strategies that vary from partner-to-partner and segment-to-segment. See below for some illustrative examples.

#### Example
Sharing Data
- Company A is in my “Prospects” segment.
- Partner X has configured the sharing rule to share a single basic data point when there is a match among segments: they will share “Company Name.”
- In the Crossbeam UI, I can see that my Prospect Company A is a Customer of Partner X.

Counts Only
- Company A is in my “Prospects” segment.
- Partner X has configured the sharing rule to Counts Only, so no underlying data is shared.
- In the Crossbeam UI, I can see that 1 of my Prospects is a Customer of Partner X. I do not see which prospect.

1-Way Sharing
- Company A is in my “Prospects” segment.
- I have configured the sharing rule to Counts Only, so no underlying data is shared from me. But Partner X has configured the sharing rule to share data point: “Company Name” with me.
- In the Crossbeam UI, I can see that my Prospect Company A is a Customer of Partner X. Partner X can only see that 1 of my Prospects is a Customer of Partner X. Partner X does not see which of my prospects is their customer.

### Required Data
Matching Engine
The Crossbeam matching engine can find matches on companies and on business contacts.

For company matching to work, the dataset must include:
Account/Company Name
Account/Company Website

For business contact matching to work, the dataset must include:
Email Address

CRM Connector
For a CRM connection to work, object read-access and some additional fields are required to ensure data remains up-to-date and organized. This data is not automatically shared. These fields are required for syncing the data into Crossbeam:

Salesforce
Object access:
(Read) Account, Opportunity, Lead, Contact, User

Field access:
(Read) Record ID, Owner ID, Name, Website, IsDeleted, SystemModstamp, CreatedAt

Reach out to Crossbeam to learn more about required fields for HubSpot, Microsoft Dynamics and Snowflake.

### Recommended Data
We recommend users upload/sync additional data beyond what is required for the matching engine to operate. Some data is required for advanced but optional features of Crossbeam. Other data can make using Crossbeam quicker and more effective.

For instance, users with large datasets may find that they have hundreds or thousands of matches to organize and devise a GTM strategy. They will appreciate the ability to filter matches to narrow down into an actionable list (e.g. Billing Country = Germany, Employees = 10,000+).
| Object | Fields | Purpose |
| Account | Account ID Owner ID IsDeleted SystemModstamp Account Created At | Required to establish CRM connection |
| Account Name Account Website | Required for matching engine to function | |
| Account Type Billing Country Employees Industry | Recommended data: for creating accurate segments and filtering on match results | |
| Contact | Account ID Contact ID Contact Email | Required if syncing Contact object |
| Contact Created At Contact Last Activity At Contact Name Contact Phone Contact Title | Recommended data: for creating accurate segments, filtering on match results | |
| Opportunity | Account ID Opportunity ID | Required if syncing Opportunity object |
| Opportunity Contact Role | Contact ID Contact Role ID Opportunity ID Primary Role | |
| Amount Close Date Closed Name Open Date Opportunity ID Sales Stage Won | Recommended data: for creating accurate segments, filtering on match results, and access to advanced features | |
| Lead | Lead ID Lead Email Owner ID | Required if syncing Lead object |
| Lead Created At Lead Name Lead Phone | Recommended data: for creating accurate segments, filtering on match results | |
| User | Account Owner Email User ID | Required if syncing User object |
| Account Owner Name | Recommended data: for creating accurate segments, filtering on match results, and access to advanced features | |
📄 Related Articles
- Security
- Data Security Policies for Crossbeam Employees
- Data Privacy
- Audit Logs
- What is Crossbeam?
- Glossary of Key Terminology in Crossbeam
- For Sales Seats: Getting Started with Crossbeam and Crossbeam Features
- Crossbeam MCP Server
- Understanding Crossbeam AI and Data Use
