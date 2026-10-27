# Collection: Developer Documentation

Source: https://help.crossbeam.com/en/collections/16160781-developer-documentation. Captured September 30th, 2026.


## Overview (HC 12548850)
URL: https://help.crossbeam.com/en/articles/12548850-crossbeam-scim-integration-guide

Crossbeam supports SCIM (System for Cross-domain Identity Management) to automate user provisioning and deprovisioning between your identity provider (such as Okta, Azure AD, or OneLogin) and Crossbeam.

Using SCIM, your identity provider automatically keeps your Crossbeam user directory up to date by creating, updating, or deactivating users based on changes in your organization’s directory.

#### What Crossbeam’s SCIM Enables
- Automatic provisioning : Create new users in Crossbeam when they’re added in your identity provider
- Automatic updates : Sync user attributes (name, email, roles) whenever they change in your IdP
- Automatic deprovisioning : Deactivate users in Crossbeam when they’re removed from your IdP
- Role-based access enforcement : Ensure users can only access Crossbeam if they’ve been properly provisioned and assigned roles
‼️ Important
This feature is currently available for Enterprise plan only.

SCIM setup cannot be completed through the Crossbeam application interface. You must contact Crossbeam support .

### Getting Started
Crossbeam’s current SCIM implementation supports user provisioning and allows roles to be assigned directly in the SCIM payload using the core_role and sales_role attributes.
Role management through groups (SCIM Groups API) is not yet supported .


#### Before you Begin
- Confirm SCIM availability with Crossbeam Support . SCIM must be enabled for your organization.
- Obtain your SCIM endpoint and token from Crossbeam Support. These credentials are required for authentication.
- Identify your available roles using the /roles endpoint so that user provisioning requests include valid role IDs.
- Test with a small user group before enforcing SCIM for your entire organization.
- Enable SCIM enforcement : Once setup is verified, Crossbeam can enforce SCIM-only user management. After enforcement, users can only access Crossbeam if provisioned through SCIM. Manual user management in the Crossbeam UI will be disabled.
- After enforcement, users can only access Crossbeam if provisioned through SCIM.
- Manual user management in the Crossbeam UI will be disabled.
✍️ Note
Role management through groups (SCIM Groups API) is not yet supported, but may be added in a future version.

### Configure SCIM in Crossbeam
Before configuring SCIM with your identity provider, you must first enable SCIM provisioning in Crossbeam.
✍️Note
SCIM can only be configured after Single Sign-On (SSO) has already been set up. Review the setup process here .
In Crossbeam:
- Go to Organization Settings In Crossbeam, navigate to Organization Settings Scroll down to the Login Options section
- In Crossbeam, navigate to Organization Settings
- Scroll down to the Login Options section
- Confirm SSO is configured The Login Options section contains two areas: Single Sign-On (SSO) SCIM Provisioning SCIM provisioning is only available if SSO has already been configured If SSO is not yet set up, complete SSO configuration first before proceeding
- The Login Options section contains two areas: Single Sign-On (SSO) SCIM Provisioning
- Single Sign-On (SSO)
- SCIM Provisioning
- SCIM provisioning is only available if SSO has already been configured
- If SSO is not yet set up, complete SSO configuration first before proceeding
- Enable SCIM Provisioning Once SSO is configured, the SCIM Provisioning section will become available Toggle On SCIM Configuration to configure SCIM provisioning Crossbeam will generate a SCIM bearer token
- Once SSO is configured, the SCIM Provisioning section will become available
- Toggle On SCIM Configuration to configure SCIM provisioning
- Crossbeam will generate a SCIM bearer token
- Copy the SCIM token This token is required to complete setup in your identity provider (IdP). Copy and securely store the token; you’ll paste it into your IdP’s SCIM configuration
- This token is required to complete setup in your identity provider (IdP).
- Copy and securely store the token; you’ll paste it into your IdP’s SCIM configuration
- Set SCIM requirement level You’ll see two options: Not Required and Required Start with Not required during initial setup, then return to this workspace and switch to Required once provisioning is working as expected
- You’ll see two options: Not Required and Required Start with Not required during initial setup, then return to this workspace and switch to Required once provisioning is working as expected
- Start with Not required during initial setup, then return to this workspace and switch to Required once provisioning is working as expected
- Click Save Settings to finalize the configuration

Once saved, Crossbeam is ready to receive SCIM requests from your identity provider.

### What is Supported and How it Works
Crossbeam requires the following attributes in SCIM user objects:


#### Required Attributes
- userName (string): The user's email address - used as the primary identifier
- active (boolean): Whether the user account is active (true) or inactive (false)
- externalId (string): External identifier from your identity provider
- displayName (string): User's display name
- name (object): User's name information givenName (string): First name familyName (string): Last name
- givenName (string): First name
- familyName (string): Last name
- emails (array): Array of email objects value (string): Email address type (string): Email type (e.g., "work") primary (boolean): Whether this is the primary email
- value (string): Email address
- type (string): Email type (e.g., "work")
- primary (boolean): Whether this is the primary email

#### Crossbeam-Specific Attributes
- urn:ietf:params:scim:schemas:extension:crossbeam:2.0:User (object): Crossbeam-specific user configuration core_role (UUID, optional): ID of the core role to assign to the user sales_role (string, optional): Sales edge role to assign to the user
- core_role (UUID, optional): ID of the core role to assign to the user
- sales_role (string, optional): Sales edge role to assign to the user
‼️ Important
Each user must have either a core_role OR a sales_role (or both), but at least one is required. You cannot create a user with no role assigned.

#### Available Roles
The /v1/scim/{sso-config-id}/roles endpoint returns all available roles for your organization, including both core roles and sales edge roles:
{ "core_roles": [ { "label": "Role Name", "description": "Role description", "value": "role-uuid-string" } ], "sales_roles": [ { "label": "Manager", "description": "Configures Crossbeam for Sales, manages other users' access to Crossbeam for Sales", "value": "partner-manager" } ] }

#### Core Roles
Core roles are organization-specific and returned in the core_roles array. These roles are managed within the Crossbeam app and cannot be managed via SCIM .

#### Sales Roles
Sales roles are predefined and returned in the sales_roles array.

Sales roles are predefined and returned in the sales_roles array of the roles endpoint.
- Manager ( partner-manager ): Configures Crossbeam for Sales, manages other users' access to Crossbeam for Sales
- Standard ( co-seller ): Full access to Crossbeam for Sales features, make partner requests, use Chrome extension, full access to Crossbeam Copilot, gets alerts, access to lists, access to Deal Navigator, reply to conversations, complete conversations and mark Attribution, does not have Crossbeam Core Access
- Limited ( viewer ): Full access to Crossbeam for Sales features listed for the Standard role (including access to Crossbeam Copilot), but cannot make partner requests or access lists, does not have Crossbeam Core Access

#### Seat Quota Validation
Crossbeam enforces seat quotas during user provisioning:
- Core seat: Users with a core_role (with or without a sales role) consume one core seat
- Sales seat: Users with only a sales_role consume one sales seat
If your organization exceeds its quota, SCIM returns an error:
{ "scimType": "overquota", "schemas": ["urn:ietf:params:scim:api:messages:2.0:Error"], "detail": "No more core seats available: you need to get more seats", "status": "400" }

#### SCIM Endpoints
Crossbeam provides the following SCIM endpoints that comply with the SCIM 2.0 specification:


#### User Management
- GET /v1/scim/{sso-config-id}/users - List users
- POST /v1/scim/{sso-config-id}/users - Create user
- GET /v1/scim/{sso-config-id}/users/{user-id} - Get specific user <!-- VALIDATE-OK[identity]: verbatim public Crossbeam Help Center text -->
- PUT /v1/scim/{sso-config-id}/users/{user-id} - Replace user <!-- VALIDATE-OK[identity]: verbatim public Crossbeam Help Center text -->
- PATCH /v1/scim/{sso-config-id}/users/{user-id} - Update user <!-- VALIDATE-OK[identity]: verbatim public Crossbeam Help Center text -->
- DELETE /v1/scim/{sso-config-id}/users/{user-id} - Delete user <!-- VALIDATE-OK[identity]: verbatim public Crossbeam Help Center text -->

#### Role Management
- GET /v1/scim/{sso-config-id}/roles - List available roles (not a SCIM endpoint, but metadata to help provide valid values for roles in the Crossbeam user extension)
Note: Endpoints are case-insensitive ( /Users, /USERS, etc.).
Test endpoints using the Postman collection:
SCIM 2.0 CROSSBEAM.postman_collection.json

#### Authentication
All SCIM requests require a Bearer token in the Authorization header:
Authorization: Bearer <your-scim-token>


#### Example SCIM User Creation
{ "schemas": [ "urn:ietf:params:scim:schemas:core:2.0:User", "urn:ietf:params:scim:schemas:extension:crossbeam:2.0:User" ], "userName": "john.doe@company.com", "active": true, "displayName": "John Doe", "name": { "givenName": "John", "familyName": "Doe" }, "emails": [ { "value": "john.doe@company.com", "type": "work", "primary": true } ], "urn:ietf:params:scim:schemas:extension:crossbeam:2.0:User": { "core_role": "12345678-1234-1234-1234-123456789abc", "sales_role": "co-seller" } } <!-- VALIDATE-OK[person-address]: verbatim public Crossbeam Help Center text --> <!-- VALIDATE-OK[uuid]: verbatim public Crossbeam Help Center example -->


#### Error Handling
Crossbeam returns standard SCIM-compliant error codes:
| Status | Description |
| 400 Bad Request | Invalid data, missing attributes, or exceeded seat quota |
| 401 Unauthorized | Invalid or missing SCIM token |
| 404 Not Found | User or organization not found |
| 409 Conflict | User already exists |

#### Audit Logging
All SCIM operations are logged in Crossbeam’s audit system for transparency and compliance.
| Field | Description |
| User | Logged as “System (SCIM)” ( system@SCIM ) |
| Actions | Create, update, delete |
| Details | Before/after user states, including active status and roles |
- Setting Up SAML SSO in Crossbeam
- Installation Guide: Crossbeam for Salesforce (v2)
- For Sales Seats: Getting Started with Crossbeam and Crossbeam Features
- Crossbeam Overview for Compliance Teams


## Overview (HC 12601327)
URL: https://help.crossbeam.com/en/articles/12601327-crossbeam-mcp-server

In this article:
- Overview Requirements Crossbeam Credits
- Requirements
- Crossbeam Credits
- What You Can Do with Crossbeam MCP Top Use Cases Example Prompts
- Top Use Cases
- Example Prompts
- Crossbeam MCP Server Specifics
- Supported Tools
- Troubleshooting
- Accessing the Crossbeam MCP Server
- Connecting Crossbeam to Claude.ai
- Connecting Crossbeam to ChatGPT
- Connecting Crossbeam to Glean
- Connecting Crossbeam to Gong Agent Studio
- Connecting Crossbeam MCP to Other AI Tools Additional Third‑Party MCP
- Additional Third‑Party MCP
- FAQs
As of September 1st, Crossbeam MCP is generally available on all plans, including Free and Connector. Crossbeam Credit metering is now live.

Connect your AI tools to Crossbeam using the Model Context Protocol (MCP), an open standard that lets AI assistants interact with your Crossbeam data.

What is an MCP Server
An MCP server provides AI tools with structured access to external tools and data.

It acts like a translator between an AI model (like Claude or ChatGPT) and a software system, providing information in a standardized format the AI can understand and interact with.

Crossbeam MCP
Crossbeam MCP is our remote server that gives AI tools secure, structured access to your ecosystem data.

It works with AI assistants like ChatGPT, Claude, and custom internal agents, enabling them to access your ecosystem data and deliver insights, actions, and automations directly within your workflows.

So instead of logging into a dashboard or copying data manually, AI agents can now access Crossbeam data programmatically, enabling smarter prioritization, recommendations, and next-best actions directly within your GTM workflows.
Want to learn more about privacy at Crossbeam? Click here .
Learn more about the Crossbeam MCP Server in Crossbeam Academy.

#### Requirements
All Crossbeam plans have access to Crossbeam's MCP Server, including access to our native AI connectors, along with a baseline amount of Credits included in your platform fee.

✍️ Note
Full Access or Sales seat are required to connect.
Admins can also control MCP access by role. Manage this from Settings > Roles & Permissions . Click Edit next to a role, locate the MCP permission, and set it to either Access or No Access . All roles default to Access, so nothing changes for your team unless an admin updates it.
| Plan | MCP Access | Annual Credits |
| Free | ✓ | 50/yr |
| Connector | ✓ | 500/yr |
| Supernode | ✓ | 2500/yr |
| Enterprise | ✓ | 5000/yr |

### Crossbeam Credits
🤓 For the full picture on how Credits are counted, how to estimate usage, and how to buy more, see the Crossbeam Credits FAQ .
Crossbeam Credits measure how your ecosystem data moves from Crossbeam into your AI tools. When an AI tool or agent,  like Claude, ChatGPT, or a custom agent, pulls partner and account intelligence from Crossbeam, it draws from your organization's shared credit balance.

Credits are pooled across your whole team, not assigned per user, so anyone with a qualifying seat draws from the same balance. Credits reset annually and do not roll over.

Admins can monitor credit consumption and overall usage from the Plan & Billing page, broken down by MCP tool calls and active users by week, month, or all time. Only admins have access to the org-level usage view.

### What You Can Do with Crossbeam MCP

#### Top Use Cases
- Bring partner context directly into internal copilots or CRM assistants so reps can see partners to leverage, recommendations on next steps, and key account highlights
- Layer in ecosystem data to existing account prioritization for an even more strategic list
- Trigger actions based on ecosystem signals, like surfacing partners to engage when a deal hits a certain stage
- Get ranked partner recommendations for an open opportunity, powered by the same Ecosystem Intelligence as Deal Navigator
- Surface partner owner contacts and decision-maker contacts (when those fields are being shared by the partner) to support introductions and deals
- Find net new accounts and qualified leads sourced from your partner ecosystem, including companies not yet in your CRM
- Pull account insights from your own Standard and Custom Fields, as well as those shared by partners, for richer account context

#### Example Prompts
Prioritize accounts and territory planning:
- Which of my open opportunities have an active partner working the same account?
- Layer partner overlaps and recent signals into my account list and show me the warmest targets.
- Which accounts should I focus on this week based on recent ecosystem activity?
Prep for calls and pipeline reviews:
- What ecosystem context exists on [Account] before my call tomorrow?
- Which partners also have [Account] in their pipeline?
Find the right partner for an open deal:
- Which partner can help me move this deal forward?
- Who at [Partner X] can help me get a warm intro to [Account]?
Surface ecosystem activity:
- What's happening in my ecosystem across my deals?
- Which partners have been most active on my accounts this quarter?
Expand your ecosystem and discover new partners:
- Show me potential partners with lots of existing relationships in our space.
- Suggest new partners we should invite based on our ecosystem data.
Understand partner performance and impact:
- Who are our most active partners in the past quarter?
- Which partners have helped us close deals the fastest?
- How much revenue has [Partner X] influenced this year?

### Crossbeam MCP Server Specifics
| Endpoint | https://mcp.crossbeam.com/mcp |
| Transport | Streamable HTTP |
| Auth | OAuth 2.1 with PKCE - Dynamic Client Registration (DCR) |
| Tools | read only |

### Supported Tools
🤓 For full details on tool outputs, including example requests, see our MCP Server technical documentation . To stay up to date on newly added capabilities and changes to what’s available, see our changelog .
Tools are individual functions that AI agents can call through the MCP server to retrieve data or perform specific actions using your Crossbeam account.

Each tool exposes a different slice of your ecosystem data, from partner performance to account overlaps, making it possible for AI assistants to surface insights, suggest next steps, or automate tasks based on live Crossbeam data.

These tools work seamlessly together through prompts, and their real power comes from combining them, for example, identifying top-performing partners and immediately checking which ones are engaged on a specific account.
| Tool | Description |
| find_overlapping_accounts_and_leads | Pulls a list of accounts you share with one or more partners. Supports filtering by partner, population, segment, and partner score, and can run across your entire ecosystem at once. |
| get_account_context | Get a unified view of one of your accounts. Returns account details, owner information, and population membership, including custom feilds. Look up by domain, CRM record ID, or company name. |
| find_partner_shared_contacts | Find partner-shared contacts at an account. Surfaces decision makers, economic buyers, executive sponsors, and other key contacts your partners are sharing. |
| find_new_accounts | Returns accounts from Pipeline Generation, high-potential prospects based on where your partners already have customers, including net new accounts not yet in your CRM. Use for greenfield prospecting and net new pipeline generation. |
| get_partner_overlaps_shared_context | Returns the CRM fields a specific partner is sharing on a given account, including standard fields and any custom mapped fields like account tier or renewal date. |
| find_partner_recommendations | Returns ranked partner suggestions for an open opportunity, powered by the same recommendation engine as Deal Navigator . |
| find_overlapping_partners | Returns which of your partners have a given account in their data. Surfaces co-sell opportunities at the account level. |
| get_partner_context | Get a full picture of your partner relationships, overlap counts, open deals, potential revenue, partner score, win rate, deal size, and how recently each partner has been active. Filter by partner name, tag, or region. |
| get_ecosystem_activity | Surface recent partner activity across your ecosystem, ordered from latest to oldest. Delivers three signal event types: partner deals opened, partner deals closed won, and recent greenfield signals (deals a partner closed on a company that isn't in your CRM yet). Each event can include contact context from the partner's CRM when sharing is enabled. |
| get_list_link | Instantly generates a shareable Crossbeam list link using plain language, no need to navigate the UI. Works for both single-partner overlap lists and ecosystem-wide views. |
| search_crossbeam _knowledge | Answers "how does Crossbeam work" and shares Ecosystem-Led Growth best practices. Leverages our help docs, the ELG Insider blog, and the Ecosystem-Led Growth book as sources and references for suggestions and case studies. |
| get_partner_suggestions | Surfaces companies you don't yet partner with on Crossbeam, but should consider based on ecosystem fit. Powered by Partnerbase data, with a direct link to invite them. |

### Troubleshooting
If you encounter authorization issues, try disconnecting and reconnecting your Crossbeam account in your AI tool's connector settings. If issues persist, reach out to your Crossbeam point of contact or services@crossbeam.com . <!-- VALIDATE-OK[person-address]: verbatim public Crossbeam Help Center text -->

### Accessing the Crossbeam MCP Server
Crossbeam MCP is available on all plans, with a yearly baseline amount of Credits included with each plan. See our Credits FAQ for more details.

Follow the instructions below to connect to your AI tool of choice. You will need your Crossbeam login credentials to authenticate.

### Connecting Crossbeam to Claude.ai
✍️ Note
Crossbeam has a native connector in the Claude.ai marketplace. Using Crossbeam MCP with Claude.ai requires a Claude plan with access to connect remote MCP servers. You'll need to authenticate using your Crossbeam login credentials to connect the Crossbeam connector to your Claude account.
💡 Want to see it in action?
Watch this short video of the MCP server connected to Claude.ai here .

#### For Claude.ai Team and Enterprise plans
Find the most up-to-date documentation on adding connectors to Claude in Claude's documentation .

Claude.ai Admins
Only Workspace Owners and Primary Owners can set up MCP server connections in Claude.ai:
- Navigate to Organization Settings > Connectors
- Click " + " to add a new connector
- Search for Crossbeam and click “Add to your team.”
- Done! The Crossbeam Connector will now appear in the list of available Connectors at Customize > Connectors for your organization

What happens next:
- Individual team members can now go to their personal Customize > Connectors
- They'll find the Crossbeam Connector in the list and click Connect
- Each user authenticates with their own credentials to start using the connector

#### For Individual Claude.ai Users
Prerequisites: If you're on a Team or Enterprise plan, your organization's Owner must have already enabled the Crossbeam Connector for your team.
- Navigate to Customize > Connectors
- Click " + " and search for the Crossbeam Connector
- Click the Connect button next to the Crossbeam Connector
- Sign in with your Crossbeam credentials You'll go through an OAuth authentication flow Review and accept the requested permissions
- You'll go through an OAuth authentication flow
- Review and accept the requested permissions
- Start using it! Once authenticated, you can start using the Crossbeam Connector with Claude
Using your connector:
- Enable or disable specific tools by going to Customize > Connectors > Crossbeam
- Claude will only access data you have permission to access in that service
Managing your connection:
- You can disconnect the Crossbeam Connector anytime from Customize > Connectors
- You can also revoke access through the third-party service's security settings
- Use the Search and tools menu to enable/disable specific tools for each conversation
✍️ Note
Once you've connected on Claude web, you can also use the same connector on Claude for iOS or Android.

### Connecting Crossbeam to ChatGPT
✍️ Note
Crossbeam has a native connector in the ChatGPT plugin marketplace. You'll need to authenticate using your Crossbeam login credentials to connect the Crossbeam connector to your ChatGPT account.

Any paid ChatGPT user can find and connect the Crossbeam app from the Plugin Directory .


#### For Individual or ChatGPT Business accounts
- Go to Settings → Plugins → Browse Plugins
- Search for Crossbeam in the list of available connectors
3. Click Connect
4. Sign in with your Crossbeam credentials
- You'll go through an OAuth authentication flow
- Review and approve the requested permissions

#### Using Crossbeam in ChatGPT
Connecting Crossbeam links your account to your ChatGPT, but ChatGPT may not automatically run in every conversation. To use it, you can either:
- Type the "@" symbol followed by the app name (e.g., @Crossbeam ) in the message box before asking your question.
- Or click the + button in a chat and select More → Crossbeam before asking your question in chat.
Both of these options enable Crossbeam for that conversation. Find more general information on ChatGPT Plugins here .

### Connecting Crossbeam to Glean
For Glean Admins
Only Glean administrators can configure MCP server connections.
- In Glean, open the Admin Console and go to Platform > Actions
- Click Add actions and select the MCP servers tab
- Search for Crossbeam, it will appear under Connection verified
4. Click Crossbeam MCP to open the configuration flow
5. Under Connect to server, click Initiate connection and authenticate with your Crossbeam credentials

6. Under Enable actions, click Edit settings and select where you want to make Crossbeam available across Chat, Agents, and/or Platform

7. Click Save


#### For Glean Users
Once your admin has enabled Crossbeam in Glean, you can access it through Glean Assistant or Glean Agents.

To use it in Glean Assistant, ask a natural-language question that references Crossbeam data, for example:
- "Use Crossbeam to show me which partners have my open opportunities as customers.”
- "Give me a brief on [account name]. Is there any ecosystem context I should know ahead of their renewal?"
To use it in Glean Agents, agent creators can add Crossbeam MCP tools as steps in any agent workflow via the Plan + Execute step in Agent Builder.

### Connecting Crossbeam to Gong AI agents
Connect Crossbeam to Gong's AI agents to bring live second-party account intelligence into your Gong AI workflows. Once connected, your team can surface relevant partner relationships, co-sell opportunities, and warm paths into an account directly inside the agents they're already using.

Why connect Crossbeam to Agent Studio
Once connected, Crossbeam becomes a data source available across Gong's Agent Studio, so any team building custom AI Briefs or other Agent Studio agents can pull in live Crossbeam partner data as a building block.
🤓 Check out our guide on bringing Crossbeam into Gong's AI Briefer for an example of how you can action Crossbeam data in Gong AI Agents.
For Gong Admins
Only Gong administrators can configure new MCP server connections.
- In Gong, go to Admin Center > Settings > MCP connections (under Ecosystem)

2. Click Explore connections, then search for Crossbeam MCP Server, and click Connect

4. Toggle on Authentication required
5. Under Who can use this connection, choose Shared access or Personal access

- When you choose Personal access, each user authenticates using their own Crossbeam account before seeing content generated using the MCP connection. The data returned reflects their own seat and permissions.
- If you choose Shared access, one person authorizes the connection to Crossbeam. Everyone in Gong who uses Crossbeam sees the data that the authenticating account is permitted to see, regardless of their own seat or permissions.
6. (Optional) Select what data you’d like to make available to your Gong AI Agents via Crossbeam MCP by toggling on/off certain MCP tools.

7. Click Connect and complete authentication when prompted.
🤓 Review Gong’s MCP Client Documentation for more information on which of their AI Agents you can add custom MCP connections to.

### Connecting Crossbeam MCP to Other AI Tools
We're actively working on adding our MCP to other AI marketplaces. Until then, our Crossbeam MCP can be enabled in any AI tool that supports custom MCP connections. If your AI tool has a setting to add a custom integration, plugin, or data connector using a URL, it can connect to Crossbeam.


#### How to Connect to Additional AI Tools
Crossbeam provides a hosted MCP server that allows any Crossbeam user with a Full Access or Sales seat to connect to supported AI tools.

The exact steps vary by tool, but the pattern is the same: find your tool's connector or integration settings, add a new custom MCP server, enter the Crossbeam MCP Server URL below, and authenticate with your Crossbeam credentials.

Connection URL:
https://mcp.crossbeam.com/mcp

These are just a few examples of common AI tools and workflow builders that support custom MCP connections. Find their setup guides here:
| Name | External Resource |
| n8n | Click here |
| Microsoft Copilot | Click here |
| LibreChat | Click here |
| Amazon Quick | Click here |
| Tines | Click here |
| Cursor | Click here |
✍️ Note
This is not an exhaustive list. Any MCP‑capable client can connect to Crossbeam MCP once properly configured.

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
