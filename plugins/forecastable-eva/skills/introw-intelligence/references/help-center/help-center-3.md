# Introw help center (support.introw.io), part 3 of 4

Verbatim text of every public help article, fetched 2026-09-29. Older than docs.introw.io; where they disagree, prefer docs.introw.io and the release notes.

## Introw CPQ
Source: https://support.introw.io/en/articles/13430413-introw-cpq

Introw CPQ ensures your partners always quote from the same product data as your CRM, without any manual imports or maintenance.
Managing product lists for partners often means exporting data from the CRM, maintaining spreadsheets, and manually updating prices or SKUs when something changes. 
With Introw CPQ, all products are automatically imported from your CRM and kept in sync daily. You can then apply partner-specific pricing rules on top of this data, without duplicating or managing products in multiple systems.
This keeps your product catalog consistent, up to date, and easy for partners to use when generating quotes.
Introw CPQ is built directly on top of your CRM product catalog. Once your CRM is connected, products are automatically linked to Introw and kept up to date through a daily sync. There is no need for manual uploads, imports, or ongoing product maintenance in Introw.
Please note:
- If your CRM connection was created before January 1, 2026 , you’ll need to reconnect your CRM to enable CPQ.
- Only active (non-archived) products are synced.
❗ Introw remark: If you don’t see the CPQ option after reconnecting, please contact your Introw account manager.
Your CRM remains the single source of truth and Introw will extend it to partners.
On top of this synced catalog, you can configure two things :
- Partner segmentation (product visibility)
- Discount settings (pricing rules)
Partner segmentation defines which partners are allowed to see and use a product line item.
This is especially useful when:
- Some products are meant only for internal sales teams
- Different partner types sell different offerings
- Products vary by market, region, or partner role
### How segmentation works
You can segment product visibility using:
- Introw partner properties , such as: Partner experience (Reseller, Referral, etc.)
- Partner experience (Reseller, Referral, etc.)
- CRM properties , such as: Partner type Country Any custom CRM field
- Partner type
- Country
- Any custom CRM field
💡 Introw Tip : Only partners matching the defined conditions will see the product when creating quotes. This allows you to reuse one CRM product catalog while exposing the right subset to each partner.
Once product visibility is defined, you configure how discounts are applied.
Introw supports three pricing models: partner-based discounts , tier-based discounts , and custom pricing . 
### Partner-based discounts
Discounts can be applied dynamically based on a partner-related CRM property, for example:
- Partner (Company) property in your CRM : Partner Discount %
This allows you to manage discounts at scale directly from your CRM, without updating individual products.
### Tier-based discounts
You can also define discounts based on partner tiers, such as:
- 10% discount for Bronze partners
- 15% discount for Gold partners
Tier-based discounts are ideal when pricing is standardized across partner levels.
### Custom pricing
Partners can now set their own price for products, giving you flexibility to accommodate unique agreements or negotiated rates. Custom pricing overrides any partner-based or tier-based discounts, allowing partners to sell products at a rate that works best for them.
From the partner’s perspective:
- They see only relevant, approved products
- Prices are pre-filled with the correct discount
- They can edit line items and quantities
- Quotes can be generated directly in Introw while product data remains aligned with your CRM.
- Add your partners to Introw
- Off-portal collaboration in Introw
- Enable Quotes & Line Items in your shared deal pipeline
- Allow partners to create quotes (CPQ)
- Build a partner directory powered by Introw

---

## Enable Quotes & Line Items in your shared deal pipeline
Source: https://support.introw.io/en/articles/13431818-enable-quotes-line-items-in-your-shared-deal-pipeline

The Quotes & Line Items feature lets you control how partners interact with deal details in shared pipelines. You can let them view, create, or edit quotes and line items while keeping your CRM data accurate and enforceable.
This ensures partners have the right tools to collaborate on deals without needing full CRM access.
Important: If your CRM integration was connected before January 1, 2026 , make sure to install the update or reconnect via the Introw integrations page. This ensures quotes and line items/products sync correctly with your CRM and partners have full access to the latest data.
To understand how partners create and publish quotes step by step, see Allow Partners to Create Quotes .
In your Experience Builder , open the pipeline section for your shared deals and click Configure (⚙️) . Under Quotes & Line items , you can enable:
- Show Line Items to Partners can view the products or services attached to a deal.
- Edit Line Items to Partners can update quantities or add new products; changes sync back to your CRM automatically.
- Show Quotes to Partners can view existing quotes associated with a deal.
- Allow Partners to Create Quotes to Partners can generate new quotes directly in the shared deal experience.
Once the experience is saved and published, partners can immediately interact with deals according to the settings you've enabled.
When Edit Line Items is enabled, partners can update the products or services associated with a deal directly in the shared pipeline. This includes adjusting quantities or adding approved products from your CRM's product library. All changes are synced back to your CRM automatically. 
Within a deal detail, a partner will be able to edit line items.
When this setting is enabled, partners gain the ability to generate new quotes . You can further configure these quotes to maintain accuracy and enforceability.
- Quote Template Layout to Choose the CRM quote template partners should use.
- Signature Requirement to Decide whether a partner or customer signature is required before the quote is finalized.
- Payment Collection to Specify the payment method to streamline processing.
- Expiration Date to Lock the quote after a specific date to prevent changes.
Why it matters: Allowing partners to create quotes directly in Introw saves time and reduces manual work. Partners can generate accurate, compliant proposals without waiting for internal approvals, helping deals move forward faster while keeping your CRM data consistent.
### How it works behind the scenes
- Introw pulls quote and line item data directly from your CRM (e.g., HubSpot or Salesforce) and keeps it in sync automatically.
- Product data like name, SKU, and price are always taken from your CRM's product library so partners are always seeing accurate, up‑to‑date information.
- Line item edits made by partners (if enabled) are synced back to your CRM and reflected in the deal record to keeping your internal team aligned.
- If a deal in your CRM has no quotes or line items , nothing will appear to meaning partners only see relevant data.
Enabling quotes and line items in your partner deal view gives you:
- Deeper context for partners to they understand exactly what's in a deal and what's been proposed.
- Fewer manual updates to partners don't need to ask for attachments or CRM quote links.
- Faster collaboration to partners can act (and even adjust products) in the flow of working deals.
- CRM data alignment to changes partners make (when permitted) sync back to your CRM record.
In short: you get visibility + actionability without sacrificing control.
- How to setup shared sales pipelines
- Collaborate on a deal or any other CRM object
- Configure which deal properties to share with your partner
- Introw CPQ
- Allow partners to create quotes (CPQ)

---

## Allow partners to create quotes (CPQ)
Source: https://support.introw.io/en/articles/13431965-allow-partners-to-create-quotes-cpq

When Allow partners to create quotes is enabled, partners can generate quotes directly from a shared deal using your CRM quote templates. This gives partners a structured, guided way to produce accurate and compliant quotes without relying on your internal team for manual creation.
You stay in control of how much autonomy partners have.
Using the Allow quote publishing setting in your pipeline configuration, you decide whether partners can publish quotes directly or are limited to creating drafts for your team to review and publish, giving you a built-in approval step where you want oversight.
This feature is part of the broader Quotes & Line Items configuration, where you can control line item visibility, editing, and quote access across shared deals.
### How the Partner Quote creation flow works
Partners start by opening the deal detail in their shared pipeline and clicking " Add " in the quotes section. Introw will pre-populate buyer and seller details from the CRM data, and guides the partner through reviewing and adjusting line items (if editing is allowed), completing any required signature steps, and reviewing purchase terms and comments. Depending on your configuration, the partner then either publishes the quote directly or saves it as a draft for your team to publish. Once published, the quote is synced back to your CRM, keeping the deal record up to date.
### 1. End user or buyer information
Buyer  details are automatically fetched from the associated deal using information from your CRM . This ensures the quote is issued with the correct customer data without requiring manual input from the partner.

### 2. Review and Adjust Line Items (if allowed)
Partners review the products or services included in the deal and can adjust line items if editing is enabled .
All products come from your CRM's product catalog, ensuring consistency and accuracy and the discount % are auto applied based on the product library configuration.
### 3. Signature Step (optional)
If required, the quote can include a signature step for the partner or customer before it can be finalized. This helps ensure the quote is enforceable and aligned with your approval rules. 
### 4. Review Quote
Before publishing, partners can review the quote, including:
- Quote title
- Expiration date
### 5. Create a draft or Publish the Quote
Introw lets you control how much autonomy partners have over quotes through the Allow quote publishing setting in your pipeline configuration panel. When disabled, partners can only create quotes as drafts, leaving them for your team to review and publish. When enabled, partners can publish quotes directly themselves. This gives you a built-in approval step where you want oversight, and a faster, hands-off flow where you don't. 
Once the partner saves the quote, it's created in your CRM and synced back to Introw, where it becomes part of the deal record.
All data is directly synced from Introw to your CRM including an activity note that the quote got created by the partner user via Introw PRM.
- How to setup shared sales pipelines
- Collaborate on a deal or any other CRM object
- Introw CPQ
- Enable Quotes & Line Items in your shared deal pipeline
- Partner Connect: a 2-way CRM integration with HubSpot

---

## Create and manage views in the Deal Overview
Source: https://support.introw.io/en/articles/13444340-create-and-manage-views-in-the-deal-overview

The Deal Overview gives you a complete picture of all your deals and pipeline activity across your partner deals. To make it easier to focus on the segments that matter most to you, you can use Views, saved combinations of filters that you can reuse anytime.
### How to Create a Deal View
- Go to your Deal Overview .
- Use the filter options at the top (e.g., Deal Stage, Pipeline, Close Date, Owner, Amount, etc. ) to narrow down the deals you want to see.
- Once your filters are set, click Create view .
- Give your view a clear name (e.g., “High-value Deals”, “Closing This Month”, “My Open Pipeline”).
- Choose whether you want to save it as: Private View to visible only to you. Shared View to available to everyone on your team.
- Private View to visible only to you.
- Shared View to available to everyone on your team.
- Click Save .
Your new view will now appear as a tab in the Views section for quick access.
💡 Introw Note: Views work the same way in both the Deal Overview and the Partner Overview . If you want to learn how to create and manage views in the Partner Portal experience, check out this article .
### Update an Existing View
You can modify any saved view at any time:
- Open the view you want to update.
- Adjust the filters to refine which deals are shown (e.g., change the stage, update date ranges, add or remove criteria).
- Click Save View to update it.
This updates the existing view with your new filter settings.
### Manage Your Views
To organize your saved deal views:
- Click the three dots (⋯) next to any view name to: Rename the view Duplicate it (create a copy with the same filters) Delete it if it’s no longer needed
- Rename the view
- Duplicate it (create a copy with the same filters)
- Delete it if it’s no longer needed
This makes it easy to keep your list of views clean and relevant.
- Collaborate on a deal or any other CRM object
- Create and manage views in the partner overview
- What does “No portal yet" and "No deal embed yet” mean?
- Enable Quotes & Line Items in your shared deal pipeline
- AI Deal Coach

---

## Introw Product update - January 2026
Source: https://support.introw.io/en/articles/13597835-introw-product-update-january-2026

The new year 2026 started with major improvements to Introw, designed to give admins and partners more flexibility, automation, and visibility. From smarter learning workflows to targeted communications and portal enhancements, here’s a deep dive into everything new this month.
### Make partner training smarter and more flexible
Partners can now get the right training at the right time, without extra follow-ups. Courses can be automatically assigned based on your CRM filters, and deadlines can be set as fixed dates or relative to when a course starts, like 30 days after starting or before year-end . 
 Learn more about Introw's Partner training courses and get your partners revenue-ready in no-time.
- Auto-enrollment based on CRM filters Automatically enroll partners in the right courses based on CRM attributes like partner type, region, or certification status. This reduces manual work and ensures partners get the training they need, when they need it. 
- Flexible Deadlines Courses can now have: Fixed deadlines: e.g., Must be completed before December 31, 2026 . Relative deadlines: e.g., Complete within 30 days after starting . 
- Fixed deadlines: e.g., Must be completed before December 31, 2026 .
- Relative deadlines: e.g., Complete within 30 days after starting . 
- Adaptive Assessments You can now allow questions to be skipped or failed, with a maximum number of attempts configurable per course. 
- Passing Scores & Certificates Set the minimum score required to pass a course. Certificates are automatically issued if partners meet the threshold.
### Saved views for your partners (across CRM objects)
You can now create and save custom views for any shared partner object from your CRM, directly visible in the partner portal. While deals are the most common use case, this also works for leads, tickets, contacts, cases, projects, and more . Use saved views to guide partners toward what’s most important, improve follow-ups, and keep your pipelines clean. Learn more 
Stop wasting time setting the same filters daily. You can now pre-configure and save Dynamic Views as permanent tabs within a pipeline section in the Partner Portal.
- Scalable Clarity: You define the views your partners see, such as "New Leads to Claim" or "Closing This Month."
- Frictionless Experience: Partners get a "ready-to-work" overview the moment they enter the portal, with no manual filtering required.
### Targeted Partner Announcements
To make communications even more relevant, you can now send segmented partner announcements to specific partner audiences defined by CRM filters or Introw properties. This lets you tailor updates based on criteria like:
- Partner tier
- Industry
- Region
- Partner activity level
- Contact persona
- And more...
With segmented announcements, you can share product updates , incentives , or key reminders only with the partners who need them, reducing noise and improving engagement. For example:
- Announce a new co‑marketing offer exclusively to Gold‑tier partners .
- Share compliance deadlines with partners in a specific region .
- Notify partners who have been most active about advanced training opportunities.
This capability helps you deliver more personalized and impactful communication , so partners receive updates that matter to their business and priorities. Learn more 
### Additional improvements
- Stylish Certificates Upload custom background images to your certificates to match your brand. Plus, partners can now share their achievements on LinkedIn with a single click . Learn more 
- Trigger-Based Commissions We’ve added CRM filters to commission plans so you can now set triggers like "Customer Paid" or "Subscription Active" to automatically detect partner commissions. Learn more
- AI partner support with secure MCP access You can now configure MCP access directly in Introw. Connect any MCP server, enabling Introw’s AI agent to answer partner questions while keeping full control over what’s exposed. Learn more
- Frictionless Partner Registration You can now link your "Become a Partner" form directly to the portal login page, making it easier than ever for new partners to sign up and get started. Learn more  
- Introw product update - October 2025
- Introw product update - November 2025
- Introw Product update - December 2025
- Introw product update - March 2026
- Introw product update - April 2026

---

## Send dedicated partner announcements
Source: https://support.introw.io/en/articles/13600188-send-dedicated-partner-announcements

Deliver the right message to the right partners, every time. With audience-based Partner Announcements , you can now target updates based on partner properties and CRM filters, helping you communicate more effectively, reduce noise, and increase engagement.
### What are audience-based announcements?
Audience-based announcements let you define a specific group of partners or partner contacts to receive your message. Instead of sending updates to all partners or linked partner portal experiences, you can also focus on those for whom the message is relevant.
This feature is ideal for:
- Product updates for select partner tiers
- Regional compliance reminders
- Incentives for high-performing or active partners
- Targeted event invitations
By tailoring announcements to specific audiences, your partners receive information that matters most to them.
### Defining your audience
When creating a segmented announcement, you can define your audience using CRM filters or Introw partner properties . Filters can include:
- Partner Tier (e.g., Gold, Silver, Bronze)
- Industry (e.g., SaaS, Retail, Healthcare)
- Region or Location
- Partner Activity Level (e.g., active, inactive)
- Contact Persona (e.g., decision-maker, technical contact)
Once your audience is defined, the announcement will only be sent to partners matching those criteria.
### How to create a segmented announcement?
- Go to Announcements in the Partner Portal Admin.
- Click Create New Announcement .
- Choose whether to use Introw AI or manual creation .
- In the Audience section configure your segmented audience. Apply CRM filters or Introw partner properties to define your target group.
- Apply CRM filters or Introw partner properties to define your target group.
- Complete the announcement details (title, content, thumbnail, pop-up settings).
- Review and publish .
Your announcement will now be send and only appear to the defined partners in the audience across the portal, email, and Slack.
### Benefits of audience segmentation
- Relevance: Partners only receive updates that matter to them.
- Engagement: Personalized messaging drives higher open and click rates.
- Efficiency: Reduce clutter and prevent information overload.
- Insights: Track engagement per audience segmented message to optimize future communications.
### Best Practices
- Use clear and specific CRM filters to avoid missing partners who should receive the message.
- Combine partner properties (e.g., tier + region) for precise targeting.
- Schedule announcements to appear when the audience is most likely to engage.
- Track engagement metrics to refine future segmentation strategies.
- Partner Tiers
- Partner Engagement Tracking
- Introw CPQ
- How to set up a partner application form
- Build a partner directory powered by Introw

---

## Multi-Tenant Access
Source: https://support.introw.io/en/articles/13701950-multi-tenant-access

#### What is Multi-Tenant?
Multi-tenant access allows a single user profile to be associated with multiple, independent Introw organizations. It’s designed to provide unified access and effortless switching between different environments while keeping your data strictly siloed and secure
This is a game-changer for:
- Corporate Groups: Switch between legal entities (e.g., Introw US vs. Introw EU) without logging in and out.
- Implementation & Solution Partners: Manage all your client Introw accounts from one login.
- Power Users: Easily transition between a "Sandbox" testing environment and your live production account.
#### How to add a new organisation
Starting a new Introw organisation is just as easy as when you first signed up for Introw. You don’t need a new email address to get the ball rolling.
- Click on your Organisation Avatar (or Organisation name) in the top-left corner of your navigation panel.
- Select the "Add Organisation" option. 
- A "Create new organisation" screen will appear. This will look familiar, as it mirrors the initial Introw setup process. You will be asked to provide: Company Name: The name of the new entity or Introw client. Domain: The web domain for the new organisation. CRM Integration: Select which CRM (HubSpot, Salesforce, etc.) this specific organisation will connect to.
- Company Name: The name of the new entity or Introw client.
- Domain: The web domain for the new organisation.
- CRM Integration: Select which CRM (HubSpot, Salesforce, etc.) this specific organisation will connect to.
- Click " Create Organisation ," and Introw will instantly provision your new Introw account.
Note: As the creator, you are automatically assigned as the Admin of the new Introw organisation. You can immediately start inviting team members, prospects, or customers to this specific instance.
#### Switching between organisations
Once you belong to more than one organisation, moving between them takes two clicks:
- Click on your Organisation Avatar or name in the top-left sidebar.
- Select the Organisation you want to access from the sub-menu.
### Important to know
Permission Isolation: Being a user in Organisation A does not automatically give you access rights in Organisation B unless you are the creator or have been invited/added to that organisation with the same email.
Data Siloing: Each organisation is a "walled garden." There is no data leakage between accounts.
- Link Introw to Power BI
- CRM User
- Multi-language support
- Partner Connect: a 2-way CRM integration with HubSpot
- What is Partner Connect?

---

## Multi-Currency: localise the partner portal experience
Source: https://support.introw.io/en/articles/13702763-multi-currency-localise-the-partner-portal-experience

In a global economy, your partners shouldn't have to do mental math to understand their performance. Whether you’re working with a reseller in London or a referral partner in Tokyo, seeing data in a familiar currency builds trust and clarity. 
Introw’s Multi-Currency feature allows you to display aggregated deal and pipeline data in the specific currency of your partners, while maintaining the original data integrity of your CRM.
#### Enabling Multi-Currency
Multi-currency is an "opt-in" feature to ensure it is only activated when you are ready for it.
- Navigate to your Company Settings page.
- Locate the Multi-Currency section.
- Toggle the feature to Enabled .
#### How the currency synchronisation works
Once enabled, Introw does the heavy lifting for you. We automatically import the currency configurations already established in your connected CRM.
No manual setup of exchange rates or currency codes is required within Introw; we mirror the settings you've already perfected in your source of truth.
#### Assigning a Currency to a Partner
After the feature is enabled, a new currency field will appear on every Partner Detail page.
- Go to the Partners tab and select a specific partner.
- In the Partner Detail view, look for the Currency field.
- Select the appropriate currency from the dropdown menu (populated by your CRM).
From this moment on, that partner's experience is localized.
#### The Partner Experience: Localized totals vs. native deal data
Once a currency is linked to a partner, their partner portal provides a localized experience without losing the accuracy of the original CRM data. We use a "Best of Both Worlds" approach to ensure clarity and precision.
Here is how the data is displayed to your partners:
Portal Section
Currency Displayed
Purpose
Pipeline Aggregation
Partner’s Local Currency
Allows partners to see the total of their pipeline at a glance without doing mental math.
Individual Deal Cards
Original CRM Currency
Ensures the deal matches the actual contract and CRM record, preventing any confusion during the closing process.
Dashboards & Analytics
Provides high-level insights and performance metrics in the partner's home currency for easy understanding.
### Frequently Asked Questions
What happens if I don't link a currency to a partner? If no specific currency is linked to a partner, Introw will default to your organization's primary functional currency.
How often are exchange rates updated? Introw pulls currency data and conversion logic directly from your CRM. As long as your CRM rates are up to date, your Introw dashboards will be too.
- How partner deal data syncs to your CRM
- Configure which deal properties to share with your partner
- Create a Partner portal experience
- AI agents that actually take action for your partners
- What is Partner Connect?

---

## Introw forms are protected from spam
Source: https://support.introw.io/en/articles/13726825-introw-forms-are-protected-from-spam

When you’re collecting leads or data through public Introw forms, the last thing you want is a CRM cluttered with "bot" submissions. At Introw, we prioritize lead quality as much as lead quantity. 
To keep your account clean, we’ve integrated reCAPTCHA directly into all Introw forms hosted outside of the Partner Portal. This ensures that while your partners and prospects have a seamless experience, automated scripts stay at the gate. 
### Securing your shared and embedded Introw forms
##### When using direct form Links
When you share a public Introw form link via email or social media, reCAPTCHA works in the background to verify the user before they can submit their information.
##### When using embedded Introw forms
For Introw forms embedded directly into your website or landing pages, the same protection applies. The reCAPTCHA shield integrates seamlessly with your site’s UI, blocking automated scripts without disrupting your brand experience.
### How it works: the reCAPTCHA shield
For any public-facing Introw form, such as a lead registration page or a contact form embedded on your site, we utilize invisible reCAPTCHA technology.
- Seamless partner experience: Real users typically won't see a "challenge" (like picking out traffic lights). The system analyzes risk patterns in the background. 
- Automatic blocking: If the system detects behavior consistent with a bot (e.g., inhumanly fast typing or suspicious IP origins), the submission is blocked before it ever reaches your Introw dashboard. 
- No setup required: This protection is active by default for all Introw forms used outside the authenticated Partner Portal environment.
### Why is this necessary?
While the Partner Portal is a "walled garden" requiring a seamless login , public forms are, by definition, open to the internet. Without prevention, your workflow could be disrupted by:
- Skewed Analytics: Bot entries can make your conversion rates look artificially high.
- Notification Fatigue: Your team may stop responding to alerts if half of them are junk.
- Data Integrity: Keeping your CRM "source of truth" clean is vital for accurate forecasting.
### Frequently Asked Questions
Do my partners need to solve puzzles in the Partner Portal? No. Since the Partner Portal requires a secure login, we trust those authenticated sessions and do not trigger reCAPTCHA, ensuring your partners can work at high velocity. 
What happens if a legitimate user is blocked? This is rare, but usually caused by a highly restrictive VPN or browser extension. If a user reports an issue, suggesting they try an incognito window or disable aggressive ad-blockers usually clears the path.
- Introw's Zapier Integration
- Embed Introw in your product
- Embed Introw forms
- How Introw keeps your CRM clean
- How to use Introw forms with HubSpot

---

## How Introw keeps your CRM clean
Source: https://support.introw.io/en/articles/13772924-how-introw-keeps-your-crm-clean

Introw is fully integrated with your CRM to ensure every introduction, lead, and deal maintains the highest level of data integrity. Instead of operating as a standalone form tool, Introw works directly with your CRM's properties, validation rules, and existing records to prevent duplicates, errors, and channel conflicts. 
All Introw form fields are directly linked to your CRM property fields.
This means:
- Dropdown fields reflect the exact values defined in your CRM
- Required fields follow your CRM configuration
- Validation rules (e.g., phone formats, ZIP codes, numeric ranges) are enforced automatically
- Custom properties behave exactly as configured in your CRM
There is no need to recreate validation logic in Introw, your CRM remains the single source of truth.
When a partner submits a form, Introw validates the data against your CRM's rules before the record is created or updated. 
Examples:
- Phone numbers must match the required format
- Dropdown selections must match allowed CRM values
- Required properties cannot be left empty
- Custom validation rules are automatically enforced
This ensures only clean, properly formatted data enters your CRM, out of the box.
Before creating any new record, Introw performs a comprehensive check across your CRM to determine whether the contact, company, lead, or deal already exists.
This prevents:
- Duplicate contacts
- Duplicate companies
- Multiple records for the same opportunity
- Fragmented deal histories
If a matching record exists, Introw updates or routes accordingly based on your configuration.
Introw goes beyond duplicate detection. It also performs AI-powered channel conflict detection to ensure there are no partner overlaps.
This means Introw checks:
- Whether another partner is already working on the same deal
- Whether the same partner has already submitted the opportunity
- Whether there are existing related records that indicate a conflict
Important: Channel conflict results are only visible to your internal team, such as the designated partner manager or admin within Introw. The partner submitting a deal registration or lead registration form will not see any conflict information. This way, Introw keeps your internal routing and conflict resolution process confidential while still allowing partners to submit deals seamlessly.
By identifying conflicts early, Introw protects partner relationships and ensures fair deal attribution. 
Because Introw is tightly embedded within your CRM ecosystem:
- Your CRM rules are always enforced
- Duplicate records are minimized
- Channel conflicts are detected early
- Data stays consistent and trustworthy
Introw doesn't just collect introductions, it safeguards your CRM integrity at every step.
- Integrating Introw with Crossbeam
- How to use Introw forms
- AI detected channel conflict resolution
- Connect your CRM
- Introw CPQ

---

## Save time with Introw’s AI Agent
Source: https://support.introw.io/en/articles/13892885-save-time-with-introw-s-ai-agent

Introw’s Agentic AI enables partners and internal teams to create, update, and collaborate on shared CRM objects directly from the partner portal. The AI converts natural input into structured CRM actions, reducing manual data entry and keeping records accurate.
💡 Prefer to work in Slack? The same agent is available there, see Introw's AI Agent in Slack .
Agentic AI allows users to take action on shared CRM objects without navigating complex CRM interfaces. It works across standard and custom objects, including:
- Deals
- Opportunities
- Leads
- Tickets
- Cases
- Custom CRM objects
All actions are automatically structured and synced with your connected CRM.
Users can create new records (e.g., deals, leads, tickets, or custom objects) directly from the partner portal.
The Agentic AI:
- Captures required information
- Structures the data correctly
- Creates the record in the connected CRM
This ensures accurate data entry without manual CRM input.  📺 Watch how it works 
Users can update existing records in real time from within the portal.
Supported updates include:
- Changing stages or statuses
- Editing field values
- Adding relevant details
The AI translates user input into structured CRM updates, keeping pipelines and records up to date.
📺 Watch how it works 
Users can collaborate on shared objects without leaving the portal.
This includes:
- Adding contextual comments
- Creating follow-up tasks
- Logging structured activity
All collaboration is recorded and synced with the CRM, ensuring visibility and accountability across teams.  📺 Watch the collaboration magic
- Eliminates manual CRM data entry
- Reduces friction for partners
- Improves data accuracy
- Keeps pipelines and shared objects up to date
- Supports all shared CRM objects, including custom ones
- Off-portal collaboration in Introw
- Introw's AI Agent in Slack
- AI agents that actually take action for your partners
- Partner Connect: a 2-way CRM integration with HubSpot
- What is Partner Connect?

---

## Multi-upload: bulk submit records via a form
Source: https://support.introw.io/en/articles/14006567-multi-upload-bulk-submit-records-via-a-form

Multi-upload is an optional feature you can enable on any existing Introw form. When enabled, partners get an extra option to upload multiple records in one go, directly within the standard form they already use for single submissions. 
The form itself stays exactly as you configured it. Multi-upload simply adds a bulk submission option on top, so partners can choose what works best for them at that moment.
### How it works
Every form in Introw is built for single record submissions. You define the fields, link them to your CRM properties, and your partners fill them in one by one.
When you enable multi-upload on that form, partners see an additional upload option. The upload template they can download contains exactly the same columns as your single-submission form, nothing more, nothing less.
Partners fill in the spreadsheet with one record per row and upload it when ready.
Introw then processes each row individually, applying the same validations, duplicate checks, and automations as a regular single-form submission. 
### How to enable multi-upload on a form
- Go to Forms in your Introw portal.
- Open the form you want to update, or create a new one.
- In the form builder, add a form field called Batch Upload .
- Save the form. 
#### Configuring the button copy
You have full control over the labels shown to your partners for the multi-upload buttons. In the form settings, you can customize the copy for:
- The upload button (e.g. "Upload file", "Submit multiple records")
- The template download button (e.g. "Get template", "Download CSV example", "Get CSV example")
- Any other multi-upload related call-to-action shown in the form
This lets you match the language to your brand or make the instructions clearer for your specific partner audience.
### What happens after upload
Once a partner submits the file, Introw processes every row individually via the full form automation workflow:
#### CRM-based data validation
- Required fields are checked on every row, rows with missing or invalid values are flagged and reported back to the partner
- Field formats are validated against your CRM rules (e.g. phone number formats, dropdown values, numeric ranges)
- Custom CRM validation rules apply automatically, no separate configuration needed in Introw
For example, if a partner enters a phone number in the wrong format, Introw will flag that specific row with a clear error message explaining what's wrong, so the partner can correct it and re-upload without having to guess. 
#### Duplicate detection
- Before creating a new record, Introw performs a 360° CRM check to identify whether the object (contact, company, deal, opportunity, or other) already exists
- If a match is found, Introw updates or routes the record based on your configuration, no duplicates are created
#### Channel conflict detection
- Introw checks whether the submitted record is already being worked on by another partner
- Conflicts are flagged for your review, keeping deal attribution fair and transparent
#### Automations
- Every successfully processed row triggers the same automations as a single-form submission
- This includes CRM workflows, owner assignments, email notifications, and any other automation you have configured
### Reviewing upload results
After processing, partners can see a submission overview listing every row from their upload with a clear status per record. At a glance, they can see which records were accepted and which ones went into error, along with the specific reason so they know exactly what to fix. 
Partners can correct the flagged rows and re-upload without affecting already-processed entries.
- How partner deal data syncs to your CRM
- Create new partners via Introw
- How to use Introw forms
- How to set up a partner application form
- AI-assisted form approvals

---

## How to create a report
Source: https://support.introw.io/en/articles/14011044-how-to-create-a-report

Most partner teams track performance the hard way by exporting CRM data and PRM data into spreadsheets, stitching together numbers from different tools, and rebuilding the same reporting every quarter. It's slow, error-prone, and by the time it's done, the data is already outdated. 
Introw lets you build reports directly on top of your live CRM and partner portal data. Pick your data source, choose a visualisation, and configure what you want to measure.
### Step 1: Go to reports & dashboards
In your Introw sidebar, click on Reports and click + New Report in the top right corner.
### Step 2: Configure your report
The Configure tab is where you set up the core of your report.
Pick a data source to choose what you want to report on:
- CRM data, any object attributed to partners in your CRM (deals, opportunities, leads, tickets, ...)
- Introw data, partner portal data like partners, engagement events, certifications, or emails sent
💡 Introw Tip: All data sources are already scoped to your partners in Introw. If you select deals, you'll only see deals linked to your partners, not your entire CRM. The same applies to Introw data like portal visits or engagement events. Introw user data like partner managers is also part of this underlying data, so you can track and compare partner team performance across any report.
#### Choose your visualisation
Select how you want your data to be displayed
Visualisation
Best used for
Bar chart
Comparing values across partners, tiers, or time periods
Line chart
Tracking trends over time
Pie chart
Showing proportional breakdowns (e.g. revenue share by tier)
Number
Highlighting a single key metric at a glance
#### Set your axes and measurement:
- X axis, what to group by (e.g. per month (time), partner name, tier)
- Y axis, what to measure: Count , Sum , or Average
For Number widgets, just select the metric and measurement as no axes are needed.
#### Break down by (optional)
Add a second dimension to your chart by splitting results across any Introw property (e.g. partner tier, partner manager, attribution) or any CRM property linked to your partner.
- Partner tier, see how results differ across your tier structure
- Partner manager, understand which team members are driving the most activity
- Partner Name, compare individual partner contributions side by side
- Partner Contact - Compare engagement across your partner contacts
- Any Introw partner or CRM property, use any CRM or Introw property to slice the data further
Your chart will display the results as stacked or grouped segments which gives you a richer insight, without needing multiple reports.
💡 Introw Tip: Breaking down a revenue chart by partner tier instantly shows whether your top-tier partners are truly outperforming the rest.
Example: asset engagement per partner contact 
Say you want to know which individual contacts are actually consuming your sales enablement assets, not just which partner companies.
- Select the Asset engagement metric.
- Set Breakdown by to Partner contact .
- (Optional) Filter to a specific partner, segment, or asset to narrow the view.
You'll get a ranked view of contacts by asset views, downloads, and time spent, so you can spot your most engaged champions inside each partner account, and the contacts who've gone quiet. 
Other useful combinations
- Portal logins broken down by Partner contact, identify active vs. dormant users inside a partner org.
- Asset engagement broken down by Asset, find your highest- and lowest-performing content.
### Step 3: Filter your data
In the Filters tab , narrow down which records are included in the report. Filters support dynamic date ranges so your report always stays current without needing to be updated manually.
By default, Introw shows data across all time . If you want to focus on a specific period, this is where you set it. 
💡 Introw Tip: A great starting report for any partner team is portal visits in the last 90 days . Select engagement events as your data source, set the date filter to last 90 days, and break down by partner, instantly showing you who's actively engaging with your portal and who's gone quiet.
### Step 4: Fine-tune your layout
In the Layout tab , control how your chart looks. Not all options are available for every visualisation.
Option
What it does
Available for
Show data values
Display exact numbers on the chart
Bar, Line
Compact format
Abbreviate large numbers (e.g. 10k)
All
Show as % of total
Show values as a % of the total
Bar
Show legend
Shown when a breakdown is applied
Show 0 values
Include zero-value records
Bar, Line, Number
Bar orientation
Switch between vertical and horizontal
Sort by value
Order results from highest to lowest
Limit results
Cap to a top N (e.g. top 10)
* For pie charts , data values, % of total, and legend are always shown and cannot be toggled.
💡 Introw Tip: Sort by value + top 10 limit on a bar chart = instant partner leaderboard.
### Step 5: Inspect the underlying data
Switch to the Data tab at any point to see a table of the raw records behind your chart. This is useful for validating your report or diving deeper into specific results. You can also export the underlying data as a CSV from this tab. 
### Step 6: Name and save
Give your report a clear name like Deals Closed This Year by Tier and click Save . The name you choose will also appear as the title of the chart which makes it easy to identify it when added to a dashboard. 
- Partner performance dashboard
- Partner Analytics
- Partner engagement reporting in HubSpot with Introw app events
- How to create a dashboard?
- Build a partner directory powered by Introw

---

## How to create a dashboard?
Source: https://support.introw.io/en/articles/14019994-how-to-create-a-dashboard

Tracking your partner program shouldn't mean opening spreadsheets or re-running reports every Monday. Dashboards in Introw give you a live view of your partner data that is always up to date, no manual work needed. You can even embed them directly in your partner portal, where Introw automatically shows each partner only their own data.
### Step 1: Open Reports & Dashboards
In your Introw sidebar, click Dashboards → + Create Dashboard .
You can give your dashboard a name (e.g. Partner Performance Overview or Channel Revenue Q3 ) in the header of the page. 
### Step 2: Add reports to your dashboard
Your empty canvas will appear. Under Add Reports you can find the available report wdigets and start building your dashboard view. Any report you've previously created will be available to add here. 
💡 Introw Tip: Haven't created any reports yet? Check out How to Create a Report first as each widget on your dashboard is a saved report.
### Step 3: Arrange your layout
Drag and drop reports to arrange them in a layout that works for you. You can also:
- Resize : drag the bottom-right corner of any widget to make it larger or smaller
- Edit : click the 3 dots → Edit to adjust the underlying report without leaving the dashboard
- Remove : click the 3 dots → Remove to take a report widget off the dashboard 
### Step 4: Save your dashboard
Click Save changes to lock in your dashboard layout.
### Managing your dashboards
You can create as many dashboards as you need like one for revenue, one for engagement, one per partner tier, or whatever fits your workflow. In the Dashboards overview you can:
- Rename a dashboard at any time by hovering over its name via the 3 dots.
- Reorder dashboards by dragging them into the sequence that makes most sense for your team
- Filter across all widgets using the global date filter to instantly shift the time range of an entire dashboard which great for switching between a monthly, quarterly, or yearly view without editing individual reports
- Save your filter state so the next time you open a dashboard it picks up right where you left off.
💡 Introw Tip: Setting up a dedicated dashboard per use case, like one for your QBR prep and one for day-to-day monitoring, keeps things focused and saves time when you need answers fast.
- Partner performance dashboard
- Show commissions to your partners
- How to use Introw's course builder
- How to create a report
- How to embed a report or dashboard in your partner portal

---

## How to embed a report or dashboard in your partner portal
Source: https://support.introw.io/en/articles/14022987-how-to-embed-a-report-or-dashboard-in-your-partner-portal

Sharing performance data with partners usually means exporting a report, building a slide, and sending an email only for it to be outdated by the time they open it. By embedding a report or dashboard in your partner portal, your partners always have access to their latest numbers without you having to lift a finger.
Introw automatically scopes any embedded report or dashboard to the partner visiting the portal, so every partner sees only their own data.
### Reports vs. dashboards in the portal
Both reports and dashboards can be embedded anywhere in your portal, it's entirely up to you how you use them. That said, here's how teams often approach it: 
A single report works nicely as a widget on the home page, for example, a number showing deals registered in the last 30 days gives partners a live snapshot every time they log in without overwhelming them. 
A dashboard tends to fit well as a dedicated section under its own tab, like a Partner Performance page where partners can explore their deal pipeline, revenue contribution, and engagement all in one place. 
There's no right or wrong way. The best setup is the one that makes the portal most useful for your partners.
💡 Introw Tip: Focus on metrics that are meaningful to a partner, deals closed, revenue generated, average deal size, tickets resolved, certifications completed. An internal partner leaderboard, for example, isn't something a partner needs to see.
### How to embed a report or dashboard
The flow is the same whether you're embedding a report or a dashboard, it works just like the rest of the Experience Builder. 
Step 1: Open the Experience Builder
In your Introw sidebar, navigate to the Experience Builder and open the partner experience where you want to add the report or dashboard. 
Step 2: Add a section
Click + Add Section and select Report or Dashboard from the list of available section types. 
Step 3: Select your report or dashboard
From the overview, choose which report or dashboard you want to embed. Only reports or dashboards you've already created in Introw will appear here. 
Step 4: Save and publish
Click Save and publish the changes in the experience builder. The section will now appear in your partner portal. 
When a partner visits their portal, Introw automatically filters the content to display only their data: their deals, their activity, their performance. No additional configuration needed.
### What your partners will see
Each partner sees a live version of the report or dashboard scoped entirely to their own data. If you embed a deal revenue report, they'll see their deals. If you embed an engagement dashboard, they'll see their own portal activity.
Partners cannot see data from other partners and have no visibility into your internal reports or dashboards.
### Exporting the drill-down data as CSV
Beyond viewing the visual, partners can dive into the underlying records and export the drill-down data of a report as a CSV, useful when they want to share numbers internally, build their own pivots, or work with the data offline. 
As an admin in Introw, you have full control over which properties are shared in the export . When configuring the report, you decide exactly which fields partners can see and download, so sensitive internal properties stay inside Introw, while the data partners actually need is just one click away. 
 
- Partner performance dashboard
- Show commissions to your partners
- Unlink or update an experience of your partner portal
- Embed your Power BI reports
- What does “No portal yet" and "No deal embed yet” mean?

---

## Install the Claude connector of Introw
Source: https://support.introw.io/en/articles/14034406-install-the-claude-connector-of-introw

### A new way of working
The way partnership teams work is changing and this is one of those moments you'll look back on. Imagine starting your morning by simply asking:
- "Which of my partners have pending deal registrations this week?"
- "Show me the commission status for our Gold tier partners."
- "Which partners haven't completed onboarding yet?"
- "What's the total partner-attributed pipeline for Q2?"
- "Who are my most engaged partners by deal activity this month?"
Claude reasons across your live partner data, surfaces insights instantly, and helps you stay one step ahead, without ever leaving the conversation. This is what AI-powered partnership management actually looks like in practice.
💡 Personalised by design. Thanks to Introw's MCP, Claude only ever sees the data you're authorised to see in Introw, your permissions, enforced automatically. Nothing more, nothing less.
### How it works
The integration uses MCP (Model Context Protocol) , an open standard that lets AI models like Claude connect securely to the tools you already use.
When you connect Claude to Introw:
- Claude authenticates on your behalf using your Introw credentials.
- Every query is scoped to your user permissions, the exact same access rules that apply when you log into Introw directly.
- No data bleeds across users. A partner manager sees their partners and deals. An admin sees what an admin sees. Your data stays yours, always.
Claude becomes a smart, always-on layer on top of your existing Introw access, not a workaround, not a shortcut, but a genuinely better way to stay on top of your partner ecosystem.
### How to connect
🎬 Watch the setup walkthrough, from installing the MCP connector to your first Claude conversation with Introw, all in one short video.
### For Claude admins, setting up the MCP connection
This only needs to be done once. Once you've completed these steps, everyone on your team can connect their own Introw account to Claude in seconds. 
Step 1 to Go to Integrations in Introw Inside your Introw workspace, navigate to Settings → Integrations and find the Claude integration. Click Configure . 
Step 2 to Copy the MCP URL Introw will generate an MCP connector URL. Copy it, you'll need it in the next step.
Step 3 to Add the connector in Claude Go to claude.ai/customize/connectors and click Add customer connector , paste the MCP URL of Introw, authorize and confirm. 
The admin setup is done. The Introw connector will be available in your team's Claude. Each member of your team will need to follow the instructions below to start using Introw MCP.
🔧 Need technical details? Full MCP setup documentation including advanced configuration and supported clients  can be found at https://claude.com/docs/connectors/custom/remote-mcp
### For Claud users: connecting your Claude account to Introw
Once your Claude owner has completed the setup above, connecting your personal Introw account takes less than a minute. 
Step 1 to Open Claude and go to Customize Go to claude.ai/customize/connectors or claude.ai and click Customize → Connectors . 
 Step 2 to Find Introw and connect Introw will appear in the list. Click Connect and sign in with your Introw credentials to authorise access. 
Step 3 to Start exploring Open a new Claude chat and try asking something like:
"Generate a QBR for Amazon" 
Claude will pull your live Introw data and respond in full context. From here, the possibilities are wide open.   Example of a QBR review generated by Claude based on real-time partner data from Introw.
### Permissions and data security
Claude's access mirrors your Introw access exactly, the same data, the same actions, the same boundaries. If you can see it or do it in Introw, Claude can too. If you can't, neither can Claude.
On top of that, you're in full control of how Claude behaves. For each capability like adding comments, retrieving tier information, updating deals, creating tasks you can choose one of three modes:
Mode
What it means
✅ Allowed
Claude performs the action automatically
🔔 Approval required
Claude asks for your confirmation before acting
🚫 Blocked
Claude cannot perform this action at all
This means you can move fast where you trust it, and stay in control where it matters. For example, you might allow Claude to read all partner data freely, require approval before it adds comments, and block it from updating deal stages entirely, all at once.
### Frequently asked questions
Does Claude store my Introw data? No. Claude does not persist your Introw data between sessions. Data is fetched in real time when you ask a question and is never stored by Claude or Anthropic. 
Can other Claude users see my partner data? Absolutely not. The MCP connection is tied to your individual Introw account. Your data is never shared with other Claude users.
Do I need a specific Introw plan to use this? This feature is available on all Introw paid plans. You'll also need a Claude.ai Pro subscription or above to use MCP integrations.
### Need help?
We're here for you. Reach out via the chat widget in your Introw portal, or email us at [email protected] . We'd also love to hear how you're using Claude with Introw as the use cases our customers discover always inspire us. 🚀
- Introw Agent
- Introw + Claude: use cases & what's possible
- Connect Introw AI to Notion, Lovable, OpenClaw, and beyond
- Give your partners their own AI assistant to collaborate in real time via Introw's Partner MCP
- Using Introw with Gemini via MCP

---

## Introw product update - March 2026
Source: https://support.introw.io/en/articles/14041018-introw-product-update-march-2026

### Manage your partner program by just talking to Claude
We launched our Claude MCP connector , allowing you to connect Claude directly to Introw and manage your partner program through natural conversation. This is a huge change in how partner program managers and their teams interact with their PRM, no more navigating menus or making manual updates. Just tell Claude what needs to happen, and it handles the rest. 
Learn more about setting up the Claude MCP connector in Introw. 
#### What you can do
- Register and update deals, Ask Claude to register a new deal, update a deal stage, or add notes to an opportunity, and it will reflect instantly in Introw.
- Assign follow-ups and tasks, Delegate next steps to partners or team members directly through conversation, without logging into the portal.
- Log partner activity, Track meetings, calls, and touchpoints by simply describing what happened. Claude captures and syncs it back to Introw automatically.
- Query your partner data, Ask questions like "Which partners haven't registered a deal in the last 30 days?" and get instant answers drawn from your live Introw data.
### See exactly how your partner program is performing
Introw sits directly on top of your CRM and adds a partner engagement layer through the portal. Advanced Reporting & Dashboards brings both sides together for the first time, your live CRM pipeline data combined with how partners actually engage in the portal, in one unified view, with no syncing, exporting, or manual reconciliation required. 
#### What's included
- Unified dashboards, A single view that combines CRM data (deals, pipeline, contacts) with Introw engagement data (portal activity, training completion, deal collaboration). Everything is live and always up to date.
- Customisable reports, Build reports filtered by any CRM attribute, partner tier, region, partner type, industry, enriched with the engagement layer only Introw can provide. Save your most-used views for quick access.
- Performance trends, Track partner activity and deal progression over time to identify patterns, spot disengaged partners early, and recognise your top performers before your next business review.
### Additional improvements
##### SCORM support in Courses
Upload SCORM files directly into Introw's course module and put your existing e-learning content to work immediately, no rebuilding required. Once uploaded, SCORM courses behave like any other Introw course: assignable via CRM filters, with deadlines, completion tracking, and reporting included. Learn more
##### Goals on certificates
Certificates can now include a goal, giving partners a clear target tied to their achievement, whether that's a revenue milestone, a number of deals, or a training objective. Particularly useful for tiered programs where partners need to know exactly what's required to progress. Learn more
##### More layout & branding options in the Experience Builder
New layout and branding controls give you greater flexibility to make the partner portal feel like a natural extension of your brand, from page structure and typography to colour schemes and component styling. Learn more
- Introw product update - October 2025
- Introw product update - November 2025
- Introw Product update - December 2025
- Introw Product update - January 2026
- Introw product update - April 2026

---

## Introw + Claude: use cases & what's possible
Source: https://support.introw.io/en/articles/14044252-introw-claude-use-cases-what-s-possible

Partnership management just levelled up and this is the new way of working! 🚀  With Claude natively connected to Introw, you no longer just manage your partner program, you have a conversation with it. Ask questions, generate reviews, track performance, and take action, all without leaving your chat. 
This article covers what's possible today, with real examples to get you started.
One of the most powerful things Claude can do is generate a full business review for any partner, pulling live pipeline data, goal progress, and deal activity into a structured, ready-to-use output.
"Generate a QBR for Acme Corp, include pipeline contribution, goal progress, and deal activity over the last 90 days." "Create an MBR summary for TechVentures." 
Claude structures the review with the key sections your partner conversation needs: pipeline breakdown, goal tracking, recent activity, and a suggested agenda. What used to take hours to prepare manually now takes seconds. 
Create a performance review
Get a clear picture of how your partners are performing over any timeframe, without building a single report.
"Breakdown the performance of my partner Amazon from the last 6 months." 
Track partner targets and goal progress
How is my partner tracking against their goals? A question every partner manager asks themselves when they are preparing for a QBR. Simply prompt it to Claude and see the magic happen. 

Stay on top of where every partner stands against their targets without digging through individual records.
"How are my partners tracking against their goals this quarter?" "Which partners are at risk of missing their Q2 targets?" "Show me goal progress for all Gold tier partners." 
Claude gives you a clear overview across your full partner base, so you can have the right conversations before issues compound. 
Claude doesn't just answer questions, it can act inside Introw on your behalf. This is where the real time savings come in. 
Add comments to partners or deals
"Set a new close date to end of March 2026 and add comment to schedule follow-up meeting" 
Create and update tasks
"Add a task for BrightPath to submit their Q3 deal registrations by Friday." "Mark the task to create a trial account for Microsoft as complete." 
Update deals
"Can you update all open deals that still have a close date in 2025" 
The use cases above are just the starting point. Here are a few more examples of what partnership teams are exploring: 
Send a QBR directly to your partner
"Generate a QBR for Acme Corp and draft an email to their partner contact sharing the highlights. 
Summarise call recordings and log them as deal comments Paste in a transcript from Gong, Chorus, or any recording tool and Claude extracts the key points and adds them directly to the deal in Introw, no manual note-taking needed.
"Here's the transcript from my call with TechVentures. Summarise the key points and add them as a comment on their open deal." 
Prepare for partner calls in seconds
"I have a call with BrightPath in 30 minutes. Give me a full briefing, deal activity, goal progress, open tasks, and anything that needs my attention." 
Spot at-risk partners before they go quiet
"Which of my partners have had no activity in the last 45 days and still have open deals?"
Introw now sits alongside HubSpot, Salesforce, Gong, Apollo, Slack, Intercom and many more. With one prompt, your AI can pull the partner intelligence that lives only in Introw (commissions, goals, tiers, MDF, portal activity) and join it with the rest of your stack.
No more exporting from one tool, exporting from another, and merging in a spreadsheet to see the full picture. Your AI does the joining for you, rich with partner context from Introw.
A few cross-stack plays partnership teams are already running:
- Introw + Gong/Modjo: Compare what a partner committed to on the co-sell call with how the deal actually moved in Introw, then log the gaps as deal comments.
- Introw + Apollo: Find fresh stakeholders at partners that have gone quiet, then queue them into a re-engagement sequence.
- Introw + Intercom: Surface partners whose support tickets spiked while portal engagement dropped, before it hits renewal.
- Introw + Slack: Turn your daily partner briefing into a channel post, with the deals that need a human this week.
- Introw + Gmail & Calendar: Book QBRs with partners at risk of missing goals and draft the invite from their live pipeline.
Claude works best when you give it context. The more specific your question, partner name, time period, tier, deal stage, the more precise the response. That said, broader questions work too, and you can always follow up to drill into the details.
A few things worth knowing:
- All responses are based on your live Introw data at the time of asking.
- Claude respects your Introw permissions, it can only see and act on data you have access to.
- Claude supports multiple languages, so feel free to work in whichever language suits you.
- Install the Claude connector of Introw
- Introw's AI Agent in Slack
- Let Claude manage your partners, agentic partner updates via Introw
- The Introw-Powered PAM: A Day in the Life
- Using Introw with ChatGPT

---

## Market Development Funds (MDF)
Source: https://support.introw.io/en/articles/14047810-market-development-funds-mdf

Introw's MDF (Market Development Funds) module gives you everything you need to run partner-funded marketing programs end to end. Partners request marketing funds from their portal, your team approves and tracks spend, and every dollar is attributed back to the deals it influenced in your CRM, closing the loop between marketing investment and pipeline.
### Fund management
See every fund in your program at a glance, total budget, allocated amount, spent amount, and remaining balance. Filter by partner, region, program, or any custom dimension to understand exactly where your marketing dollars are going.
### Budget management
Assign fixed MDF budgets to specific partners, programs, or campaigns when you want predictability and tight control over who gets what. Or work with a pooled budget that partners can tap into ad hoc by submitting requests for approval, ideal for rewarding the partners who show up with the best opportunities.
 Multi-currency support. Run MDF programs across regions with funds denominated in multiple currencies. Introw handles the conversion and consolidated reporting so you can manage a global program without losing the local context.
### Request overview
Every MDF request lives in a centralized view where your team can filter by partner, status, fund, or date range. Comment back-and-forth with partners directly on the request, bulk-action through pending items, and follow each submission through its full lifecycle.
### Approval workflow
Every MDF request can go through an approval workflow before funds are reserved. Use a single approver for simple programs, or chain multiple approvers for sequential review, for example, the Partner Manager approves first, then the CRO, then the CFO.
#### AI-assisted pre-approval
When a partner submits an MDF request, our AI agent reviews it against your program rules, partner tier, remaining budget, and historical ROI, then suggests an approval, rejection, or adjusted amount with reasoning you can act on in one click. You stay in control of every decision; the AI just removes the busywork of digging through context.
#### Full audit trail, clear timelines for partners
Every accept, decline, and comment is logged in the request timeline, so you always know who approved what and when. 
Partners get the same clarity on their side: they can see exactly where their request stands, when to expect a decision, when proof-of-execution is due, and when claims need to be submitted, no back-and-forth on status updates, no chasing for next steps.
### Claim management
#### Configurable claim flow
Once approved, the partner runs the campaign and submits a claim with proof of spend. Route claims through single or multi-step approval, and once signed off, Introw deducts the payout from the partner's available budget in real time.
Set the submission window to match your program: relative to activity (e.g. 30 days after campaign execution) or a fixed date (e.g. by December 31). Partners see the deadline upfront, no more chasing late claims at year-end.

#### Centralized invoice management
Upload, review, and track every invoice tied to a partner claim directly within Introw, no more switching between systems or chasing PDFs across email threads to reconcile partner spend. 
Partners attach proof-of-execution and invoices to their claims in the portal, your team reviews them in context next to the original request, approved budget, and attached pipeline, and every action is logged against the claim timeline. Approve, request changes, or reject with a comment, and the partner sees the update instantly, with no extra notification work on your side. 
 The result: one source of truth for every dollar spent, ready for finance, audit, or your next QBR. 
#### Prove ROI on every dollar spent
This is where MDF stops being a cost center and starts driving measurable pipeline.
Define ROI on your terms. Choose which CRM object counts toward MDF return, deals, leads, or any custom object you already track, and how it's measured: a count of records, a sum of any property (like deal amount or pipeline value), or a flat monetary value per record (e.g. every new deal sourced from an MDF campaign is worth $1,000).
Partners attach deals and leads to their approved MDF requests through an embedded MDF deal form, and the return is calculated in real time. Every approved MDF shows the deals it influenced, the pipeline it generated, and the closed revenue it returned, visible directly within the linked deal in the partner portal, so both you and your partner see the same number at the same time.
Give your partners a frictionless way to fund their marketing initiatives directly from their portal. Through a fully customizable, embedded dashboard, partners can submit funding requests in minutes and easily file reimbursement claims by attaching invoices and proof of performance directly to the record.
From their dedicated dashboard, partners get total visibility to:
- View budgets at a glance: Instantly see available, pending, and consumed funds.
- Track approvals and payouts: Follow the real-time status of requests and reimbursement claims.
- Access campaign history: View all active and past marketing initiatives in one place.
By removing the administrative headache, you make it effortless for partners to co-market your brand and drive revenue.
- How to enable approval on forms
- How to use Introw forms
- How to manage form submissions
- How to set up a MDF fund
- How partners request MDF funds, submit claims, and upload invoices
- How to show the ROI of a MDF
- Introw Product update - June 2026
- Everything Your Partners Can Do in Introw

---

## Linking deals to leads via Introw
Source: https://support.introw.io/en/articles/14048936-linking-deals-to-leads-via-introw

When partners register deals through Introw, you can automatically associate those deals with the corresponding leads in your CRM. This article walks you through the full setup from configuring your Introw form to automating the link in HubSpot.
### Overview
The flow works in three stages:
- Introw Form, A CRM embed list lets partners select the lead they want to link to their deal at registration time.
- Form Automation, The selected lead's ID is written to a dedicated deal property in your CRM.
- HubSpot Workflow, A workflow picks up the newly created deal and formally associates it with the linked lead.
#### Step 1: Add a lead embed list to your Introw form
The first step is giving partners a way to select the relevant lead directly within the deal registration form.
- Open the Introw form used for deal registration.
- Add a CRM embed list field to the form.
Introw automatically displays the correct leads for each partner based on your attribution setup, no additional filtering or configuration needed. Partners will only see the leads relevant to them when filling out the form.
#### Step 2: Create a "Linked Lead" property on the deal object
For the association to be stored in your CRM, you need a dedicated property on the deal object.
- In HubSpot , navigate to Settings → Data Management → Properties .
- Select the Deal object and create a new property (or use an existing one).
- Give it a recognizable name, Linked Lead is a common choice, but any name works as long as you can identify it later.
- Use any text-based field type (e.g. single-line text) to store the lead ID.
### Step 3: Configure form automation to write the Lead ID
Once the form field and CRM property are in place, connect them through Introw's form automation.
- In Introw, open the automation settings for your deal registration form.
- Add an action that maps the value of the CRM embed list field (the selected lead) to the Linked Lead property on the deal object. (in this example the property is called "Lead id") 
- Save the automation.
When a partner submits the form and selects a lead, Introw will automatically write that lead's ID into the Linked Lead property on the newly created deal, in the background, without any manual steps.
### Step 4: Set up a HubSpot workflow to associate the deal and lead
The final step is creating a HubSpot workflow that detects Introw-created deals and uses the Linked Lead property to formally associate the deal with the lead record.
- In HubSpot, go to Automations → Workflows and create a new Deal-based workflow .
- Set the enrollment trigger to: Object created or updated Filter by Source detail = Introw PRM This ensures the workflow only fires for deals submitted through Introw. 
- Object created or updated
- Filter by Source detail = Introw PRM
- Add a workflow action to look up the associated lead using the value stored in the Linked Lead property on the deal.
- Add a subsequent action to associate the looked-up lead record with the deal.
- Test and publish the workflow.
Once active, HubSpot will automatically link the lead to every deal that comes in through Introw.
### Summary
Stage
Where
What Happens
Partner registers a deal
Introw Form
Partner selects a lead from the embedded CRM list
Lead ID is stored
Form Automation
Lead ID is written to the Linked Lead property on the deal
Deal and lead are associated
HubSpot Workflow
Workflow looks up the lead and creates the association in HubSpot
### Tips & Troubleshooting
- Leads not appearing in the embed list? Introw automatically shows the leads associated with the submitting partner based on your attribution setup. If leads are missing, verify that the attribution is correctly configured in Introw for that partner.
- Workflow not triggering? Verify that the Source detail filter is set to exactly Introw PRM, casing and spacing must match.
- Lead ID not writing to the deal? Double-check the form automation mapping and confirm the Linked Lead property exists on the deal object in HubSpot before testing.
- Link your HubSpot deals to Introw via custom properties
- Link your HubSpot deals to Introw via company associations
- Link your HubSpot deals to Introw via custom objects
- How to use Introw forms
- How to use Introw forms with HubSpot

---

## How to set up a partner application form
Source: https://support.introw.io/en/articles/14112879-how-to-set-up-a-partner-application-form

Introw lets you automate your entire partner application process, from form submission to partner creation, CRM record linking, and portal access, all without setting up workflows in your CRM. This is powered by the Partner Automation action in the form automation builder. 
### Step 1: Open your form
Navigate to Forms in your Introw account and open an existing partner application form, or create a new one.
### Step 2: Set up the terms & conditions checkbox (optional)
Your partner application form comes with a T&C checkbox and label included by default, so there's nothing to build from scratch. Whether you use it is entirely up to you, but it's a good way to make sure applicants have explicitly agreed to your terms before they're created in Introw and your CRM.
There are two things you'll want to configure to make it work for your situation:
- Link to your T&Cs, In the field label, replace the placeholder URL with the link to your actual terms and conditions page. This gives applicants easy access to the full document before they agree.
- Map to your CRM (optional), If you want to track T&C acceptance in your CRM, map this checkbox field to the corresponding CRM property under Form fields in the Partner Automation block. You can map it to two properties at once: A boolean property to record whether the applicant accepted your T&Cs A date/time property to capture exactly when they accepted
- You can map it to two properties at once: A boolean property to record whether the applicant accepted your T&Cs A date/time property to capture exactly when they accepted
- A boolean property to record whether the applicant accepted your T&Cs
- A date/time property to capture exactly when they accepted
This gives you a clean compliance record without any manual work, you'll always know who agreed and when.
If T&C acceptance isn't relevant for your program, you can simply remove the field from your form.
### Step 3: Add the Partner Automation action
In the form automation builder (the second tab), add the Partner Automation action.
### Step 4: Enrich partner
At the top of the Partner Automation block you'll find the Enrich Partner section. When an application is submitted, Introw matches the provided form fields against existing partners and enriches them with the new data rather than creating a duplicate. This keeps your partner data accurate and your attribution clean.
### Step 5: Auto-link to CRM
Under Auto-link to CRM , click + Add for each record type you want automatically created in your CRM:
- Company automation, creates the partner company and enables deal attribution, so you always know which partner sourced each record.
- Contact automation, saves the applicant as a contact in your CRM, linked to the partner company.
Both are optional but recommended for a fully linked setup.
### Step 6: Map form fields to partner properties
Under Form fields , map your form fields to the corresponding Introw partner properties. For each mapping you can set a Write Mode (e.g. Fill in if not known ) to control whether existing values should be overwritten. Common mappings include:
- Partner name → your company name field on the form
- Partner domain → optional, can be mapped or left blank
### Step 7: Set default values
Under Default values , define fixed values assigned to every new partner created through this application form. These are ideal for fields that should be the same for all submissions, such as:
- Tier, assign the right tier from the start
- Phase, e.g. Potential Partner
- Partner manager, immediately assign the right person responsible
- Experience, ensure the partner lands in the right portal experience from day one
### Step 8: Configure partner invitation
Under Partner invitation , toggle on Auto-invite submitter to automatically send the applicant a portal invitation email once their application is processed.
You can also add a custom Welcome message (optional) that will appear in the invitation email, e.g. "We're excited to invite you to our partner portal. Your space to collaborate on pipeline, content, and strategy."
Use the Preview email button to see exactly what the partner will receive before going live.
### Step 9: Save and publish
Save your changes and publish the form. Every accepted application will now instantly create a fully populated partner in Introw and linked records in your CRM.
### Step 10: Link your form to the partner portal login page (optional)
### If you want potential partners to be able to apply directly from your portal login page, you can connect this form there in just a few clicks.
Go to your portal settings page and navigate to the Become a partner tab. Select the form you've just set up, and customize the message and button text shown to visitors, e.g. "Not a partner yet? Apply to join our partner program." Save your changes and the form will appear on your portal login page automatically.
💡 Introw tip: Introw forms can be embedded anywhere, your website, a landing page, or your partner portal login page. Drop a partner application form wherever it fits and every submission will automatically flow into Introw and your CRM.
### Enable application review and approval (optional)
By default, every application is processed automatically. If you'd prefer to review submissions before anything is created, you can enable form approval in your form settings. 
When approval is turned on, submitted applications will land in your approval queue in Introw first. No partner record and no CRM data is created until you manually approve the submission. Once approved, everything flows through as normal, the partner is created in Introw and all linked records are pushed to your CRM.
This is useful if your partner program has a vetting step, or if you want a human review before an applicant gets portal access.
As a best practice, we recommend configuring Partner Automation to create the following records on each application:
- Partner in Introw, populated with fields like name, domain, tier, phase, partner manager, and partner experience. The more you configure here, the less work is needed after the partner signs up.
- Partner company in your CRM, mapped to the right CRM properties (country, industry, partner type, and more) so the record is accurate and complete from day one.
- Partner contact in your CRM, created from the applicant's details and automatically linked to the partner company.
None of these are strictly required, you can configure only what makes sense for your workflow. That said, setting up all three gives you a complete, fully linked partner record without any manual follow-up.
- How partner deal data syncs to your CRM
- Create new partners via Introw
- Partner activity events in your HubSpot timeline
- Managing partner contacts
- What is Partner Connect?

---

## Segment use cases
Source: https://support.introw.io/en/articles/14189246-segment-use-cases

Segments let you personalize your partner portal experience based on who your partners are and where they are in their journey. Below are some of the most impactful ways to put segments to work.
### Spot your most engaged and inactive partners
Partner managers usually notice a partner has gone quiet only once a renewal wobbles or a number slips, by then the momentum is already lost. Segmenting on last activity turns engagement into something you can act on ahead of time: automatically group the partners who are leaning in right now, and the ones drifting away, so your follow-up lands where it matters. 
Last activity is available as a condition on both partners (the company as a whole) and partner contacts (the individual person), so you can track engagement at whichever level fits your motion. 
How to set it up:
- Create a dynamic segment for your most engaged partners using a recent window, e.g. last activity within 7 days . Members move in and out automatically as partners stay active or go quiet.
- Create a second dynamic segment for partners going cold, e.g. last activity more than 30 days ago . This becomes your standing "inactive" list, always current, with no manual clean-up.
- Put each segment to work: target the engaged segment with advanced enablement, co-marketing, or expansion offers, and route the inactive segment into a re-engagement announcement or nudge.
Because the segments are evaluated continuously, a partner who re-engages drops out of the inactive segment on their own so recognition and follow-up stays aligned with real behaviour, not a snapshot from last quarter. 
### Partner Onboarding
Show partners only what's relevant to their current onboarding phase, and unlock more as they progress.
*the lock icons are not visible to the portal visitors, this is seen from the Introw admin perspective when building the partner experience. 
- Create a segment for each onboarding phase (e.g. phase = Prospecting , phase = Signed Agreement ). 
- Assign tabs to the matching segment, e.g. a Getting Started tab visible only to phase = Prospecting . 
- Use the form builder to let partners trigger phase changes themselves. For example, create a T&C acceptance form that overwrites their partner phase from Prospecting to Signed Contract on submission.
- Once the property updates, the partner automatically moves into the new segment and new tabs unlock instantly.
For example:
- A partner in an onboarding segment sees a Getting Started tab with setup instructions and training resources.
- Once they completed their onboarding tasks and move to an active segment, additional tabs, such as deal registration or co-marketing materials, become available automatically.
This keeps the portal focused and avoids overwhelming new partners with content they're not ready for yet.
### Ability to Create Quotes
Restrict quote creation to partners who have reached a certain tier or completed certification. 
- Create a segment for qualifying partners (e.g. tier = Gold or certified = true ).
- In the Quotes settings, navigate to the Allow quote creation option and assign the segment that is allowed to create quotes.
- As a partner's properties are updated, access is granted or removed automatically, no manual steps needed. 
### Ability to Edit the Partner Profile
Limit profile editing to specific contacts within a partner organization, such as admins. 
- Create a partner contact segment (e.g. contact role = Admin ).
- Configure the partner profile section to Edit profile properties and select that segment which is allowed to edit those selected properties.
- Other contacts can still view the profile but won't see the option to make changes.
### Restrict assets to specific segments
Show certain assets only to the partners who should see them, such as making advanced enablement material or pricing sheets visible only to certified or tier-1 partners while keeping general onboarding content open to everyone.
- Create a partner contact or company segment (e.g. partner tier = Gold or certification status = Completed ).
- Configure the asset (or asset folder) visibility and select that segment as the one allowed to view it.
- Partners outside the segment simply won't see the asset in their portal, no empty states or locked placeholders, it's hidden entirely.
### Target Announcements to Specific Segments
Send announcements only to the partners they're relevant to, instead of broadcasting to everyone, for example, a regional promotion to partners in a specific country, or a new-feature update to a single tier. 
- Create a partner company or contact segment for the intended audience (e.g. country = United States or tier = Gold ).
- When creating the announcement, assign the segment that should receive it.
- Only partners matching the segment will see the announcement in their portal.
### Enroll Partners into Courses by Segment
Tailor learning paths by enrolling partners into courses based on their segment, for example, a foundational course for new partners and advanced enablement for certified ones. 
- Create a segment for the target learners (e.g. phase = Onboarding or role = Sales Rep ).
- In the course settings, assign the segment that should be enrolled.
- Matching partners are enrolled automatically, and the course appears in their portal.
### Award Certifications by Segment
Grant certifications to partners based on the segment they belong to, so recognition stays aligned with the partners who have met the right criteria. 
- Create a segment that represents the qualifying partners or contacts (e.g. completed training = Yes ).
- Assign the certification to that segment.
- Partners in the segment receive the certification, and it updates automatically as membership changes.
### Scope Deal Coach per Segment
Tailor Deal Coach guidance to specific segments, so the coaching and recommendations partners receive match their tier, region, or maturity. 
- Create a segment for the partner contacts the coaching applies to (e.g. Partner Sales Reps ).
- Scope the Deal Coach configuration to that segment.
- Only partner contacts in the segment receive the scoped Deal Coach experience.
### Apply Pricing & Discount Rules per Segment (CPQ)
Set different pricing and discount rules per segment, so each group of partners sees the commercial terms that apply to them, for example, deeper discounts for top-tier partners. 
- Create a segment for the partners a pricing rule applies to (e.g. tier = Platinum ).
- In CPQ / Discount settings, configure the product and assign the segment it applies to.
- Quotes created by matching partners use the segment-specific products automatically so they can only choose those product items.
### Track Goals per Segment
Set and track goals or KPIs per segment, so targets reflect each group's stage or potential rather than applying a single benchmark to everyone. 
- Create a segment for the partners a goal applies to (e.g. region = EMEA ).
- Define the goal or KPI and assign it to that segment.
- Progress is tracked per segment, making it easy to compare performance across partner groups.
### Manage Permissions & Notifications by Segment
Use segments to control collaboration and invitation options, and to scope notifications so partners only get updates relevant to them, for example, sending deal updates only to partners collaborating on those deals. 
- Select a segment for the partners or contacts the rule applies to (e.g. contact persona = partner champion).
- Configure collaboration and invite settings for that segment. 
- Set up segment-based notifications, for example, deal update notifications sent only to partners collaborating on the relevant deals. 
- Segment based access control
- Partner journeys
- Introw workflow actions in HubSpot
- Automating workflow actions in HubSpot using Introw App events
- Segments in Introw

---

## Auto-generated partner announcements from your LinkedIn
Source: https://support.introw.io/en/articles/14403496-auto-generated-partner-announcements-from-your-linkedin

Partners are often the last to hear about the news they should be sharing, product launches, case studies, new integrations. By the time it reaches them, the moment has passed. Introw closes that gap automatically: every Wednesday, you get an email with up to 3 ready-to-publish announcement drafts, generated from your company's LinkedIn posts of the past 7 days. No copywriting, no coordinating with marketing. Just review and hit publish.
Introw scans your company's LinkedIn page and filters for posts that are relevant for partners, product launches, case studies, new integrations, company news. Posts like new hire announcements or team events are automatically skipped.
The qualifying posts are turned into announcement drafts and saved in your Introw account. The Wednesday email is your weekly nudge that they're ready.
Note: If no partner-relevant posts were found that week, you won't receive an email.
Each AI-generated announcement has a suggested title and body, written in a partner-facing tone. They're saved with an AI Generated status, nothing is sent to partners until you publish.
Before publishing you can edit the copy, target a specific partner segment, or schedule for a later date. If a draft isn't relevant, simply delete it .
Partner engagement doesn't have to be a separate workload. Introw turns what you're already doing, posting on LinkedIn, into a consistent partner communication habit. Informed partners start more conversations, spot more opportunities, and close more deals. The content was always there. Now it reaches them.
- Announcements
- Create a Partner portal experience
- Partner certificates
- Send dedicated partner announcements
- What is Partner Connect?

---

## AI Deal Coach
Source: https://support.introw.io/en/articles/14431991-ai-deal-coach

Introw helps partner managers and partners close deals faster with Deal Coaching, a structured, AI-powered way to guide partners through every stage of the sales process. Each deal coach is tied to a specific CRM pipeline, so whether it's new business or renewals, partners always get the right coaching for the right motion. 
### Creating a deal coach
You can create multiple deal coaches, for example, one for your new business pipeline and another for renewals, ensuring each pipeline has dedicated coaching tailored to the sales motion.
- Navigate to Engage → Deal Coaching .
- Click Create Deal Coach .
- Select your CRM pipeline you want to base the coach on.
- Choose one of Introw's built-in templates to start from: Reselling Coach, for reseller-led deal motions Co-selling Coach, for joint selling with partners Referral Coach, for referral-driven pipelines
- Reselling Coach, for reseller-led deal motions
- Co-selling Coach, for joint selling with partners
- Referral Coach, for referral-driven pipelines
Introw uses AI to generate the deal coach based on your selected template and pipeline stages. Once created, you can fully customize every section to match your process.
#### Stage Guidance
The first tab in every deal coach is Stage Guidance . This is where Introw provides partners with clear direction for each stage of the deal pipeline.
For every deal stage , you'll find three sections:
- Must have been achieved, the key milestones or criteria that should be met before moving to the next stage.
- How to achieve it, practical guidance on the actions partners should take during that stage.
- Example email template, a ready-to-use email template partners can send when engaging with prospects at that stage.
Each of these sections is fully customizable per deal stage , so you can tailor the coaching to your exact sales process and messaging
#### Objection Handling
The Objection Handling tab surfaces the most common objections partners will face during the sales process and provides recommended responses. This gives partners the confidence to navigate pushback from prospects without needing to escalate every conversation.
#### Enablement
The Enablement tab lets you attach assets from your Asset Library that partners will need to close deals, such as pitch decks, one-pagers, battle cards, or case studies. By linking the right materials directly to the deal coach, Introw ensures partners always have the resources they need at their fingertips.
#### Rules of Engagement
The Rules of Engagement tab is where you define the guardrails for partner-led deals. This includes stakeholder engagement guidelines, escalation rules, and any other operational boundaries you want partners to follow when working a deal. Setting these expectations upfront keeps collaboration structured and avoids conflicts.
### Assigning a deal coach to partners
Not every partner needs the same coaching. Introw lets you configure each deal coach to be available to all partners or to specific partners based on the partner properties of Introw or your CRM
This means you can create differentiated coaching experiences, for example, a deal coach designed for Bronze resellers might focus on foundational sales skills, while Gold resellers get a coach optimized for advanced deal strategies. Similarly, newly signed partners bringing in their first deal will benefit from more guided coaching than experienced partners who already know the process.
💡 Introw Tip: Deal coaching segmentation ensures every partner gets coaching that matches their level and needs!
Once a deal coach is active, Introw surfaces it directly where partners need it most, inside the Deal Detail within their partner portal. 
When a partner opens a deal, the activity panel will show the assigned deal coach, giving them immediate visibility into the coaching available for that deal. For the full coaching experience, including stage guidance, objection handling, enablement assets, and rules of engagement, partners can navigate to the Deal Coach tab within the deal detail. 
This means partners don't need to go looking for coaching separately, Introw brings it to them in the context of every deal they're working on.
- Collaborate on a deal or any other CRM object
- Configure which deal properties to share with your partner
- AI deal coaching: an expert sales coach in every partner deal
- Introw mobile experience
- The Introw-Powered Partner: A Day in the Life

---

## Introw product update - April 2026
Source: https://support.introw.io/en/articles/14441504-introw-product-update-april-2026

### Segment-based access control
Introw takes role-based access control further with segment-based access control, a smarter, more scalable way to manage visibility across your entire partner experience. Instead of manually assigning tabs, assets, announcements, courses, each can be targeted to specific partner segments. As data changes in HubSpot or Salesforce, access updates in real time . No manual syncing, no stale permissions.
- Two segment types, full flexibility: Partner-based segments target entire organisations (e.g. by tier or region), while contact-based segments target individuals (e.g. by job role or language).
- Always up to date: Access updates dynamically as attributes change, the right content reaches the right audience without manual upkeep.
- Tab-level precision: Control visibility per tab in the Experience Builder, so each partner group sees exactly what's relevant to them.
Learn more about segment-based access control 
### Deal coaching
Introw now offers AI-powered deal coaching, a structured way to guide partners through every stage of the sales process, directly inside the portal. Each deal coach connects to a specific CRM pipeline, so you can tailor coaching for different sales motions like new business versus renewals. 
- Stage-by-stage guidance: Partners get key milestones, practical actions, and ready-to-use email templates for each pipeline stage.
- Handle objections with confidence: Common objections surface automatically with recommended responses, so partners can move deals forward without escalating.
- Attach what matters: Link pitch decks, battle cards, and case studies directly to the coach, the right assets, at the right moment.
You can even assign coaches to specific partner groups based on partner properties enabling differentiated coaching for different tiers or experience levels. 
Learn more about deal coaching.
### Turn your LinkedIn posts into partner announcements
Partners often miss time-sensitive updates, and keeping them in the loop manually takes effort. Introw now automatically turns your company's LinkedIn posts into partner announcement drafts , so your latest news reaches your partners without extra work. 
- Hands-off drafting: Every week, Introw scans your LinkedIn page and generates up to 3 announcement drafts from partner-relevant posts like product launches, case studies, and integrations.
- Full editorial control: Edit the copy, target specific segments, schedule for later, or delete what's not relevant. Nothing goes out until you publish.
- Skip the noise: Internal posts like team updates are automatically filtered out, only partner-relevant content makes it through.
Learn more about auto-generated partner announcements.
- Introw product update - August 2025
- Introw product update - October 2025
- Introw Product update - December 2025
- Introw Product update - January 2026
- Introw product update - March 2026

---

## Introw's AI Agent in Slack
Source: https://support.introw.io/en/articles/14494687-introw-s-ai-agent-in-slack

Introw brings the full power of its AI Agent directly into Slack. Whether you're working in a shared channel with a partner or an internal team channel , Introw's Slack bot gives you the same capabilities as the partner portal AI, right where your conversations already happen.
No switching tabs. No logging into the CRM. Just message Introw in Slack, and it takes care of the rest.
📺 See it in action ⬇️
In shared Slack channels with your partners, Introw acts as a support agent that both you and your partners can interact with. Partners simply mention @Introw and describe what they need, Introw handles the structured data entry behind the scenes.
### Register deals
Partners can register deals directly from the shared Slack channel by mentioning @Introw with the deal details. Introw captures the required information, structures it correctly, and creates the record in your CRM, no portal login required.
For example, a partner can simply type:
"@Introw I want to register a deal for my partner UHG. The company they're selling to is Bizzy (bizzy.ai) from Ghent, Belgium. Amount is 30k, close date end of quarter, type is new business."
Introw processes the request, confirms the details, and registers the deal, all within seconds.
### Add comments and create tasks
Partners and internal users can collaborate on shared CRM objects without leaving Slack:
- Add comments to deals, leads, or any shared object to provide context or updates
- Create follow-up tasks to keep deals moving forward
All activity is synced back to your CRM, so nothing gets lost.
### Get help with enablement
Partners can ask Introw questions about your products, processes, or partner program directly in the shared channel. Introw surfaces relevant enablement content and answers, reducing the back-and-forth with your partner team.
Introw is just as powerful in your internal team channels. Your partnership, sales, and RevOps teams can use Introw to quickly pull insights and prepare for strategic conversations, without digging through dashboards.
### Get partner insights
Ask Introw for a quick snapshot of any partner's performance, pipeline, or activity. Introw pulls the data from your CRM and delivers a structured summary right in the channel.
### Prepare QBRs
Need to get ready for a quarterly business review? Introw helps you pull together the key metrics, deal progress, and partner engagement data, so you walk into every QBR fully prepared.
- Connect Slack to Introw, Head to Integrations in Introw and connect your Slack workspace. ( See setup guide )
- Link your channels, Link shared partner channels and/or internal team channels to Introw.
- Mention @Introw, In any linked channel, mention @Introw and describe what you need. Introw takes it from there.
- Zero context switching, Partners and teams stay in Slack, where they're already working
- Faster deal registration, Partners register deals in seconds with a simple message
- Better data quality, Introw structures every input correctly before syncing to your CRM
- Full visibility, Comments, tasks, and updates are all logged and synced automatically
- Internal efficiency, Pull partner insights and prepare QBRs without leaving Slack
- Introw Agent
- Save time with Introw’s AI Agent
- AI agents that actually take action for your partners
- How does the integration with Microsoft Teams work?
- Introw Product Update - July 2026

---

## AI agents that actually take action for your partners
Source: https://support.introw.io/en/articles/14498758-ai-agents-that-actually-take-action-for-your-partners

Most AI assistants in partner tools do one thing: answer questions. When a partner needs to register a deal, add a comment, or create a task, they're still forced to navigate forms, log into portals, or wait for their partner manager to do it for them.
Introw's AI agents are different. They take action .
### What makes Introw's agents actionable?
Introw's partner-facing and internal AI agents can execute real operations on your CRM and within Introw, not just surface information. From a single natural-language message, a partner or team member can:
- Register a deal by describing the opportunity in plain English. Introw structures and creates it in your CRM with all required fields.
- Add comments to any shared CRM object (deals, leads, companies) without opening the CRM.
- Create tasks with due dates and assignees to keep deals moving forward.
- Prepare QBRs by pulling deal activity, pipeline metrics, and engagement data into a partner-ready business review.
- Analyze partner performance across pipeline contribution, deal velocity, and goal attainment from a single natural-language prompt.
Everything is synced back to your CRM in real time, structured, clean, and attributed to the right partner.
#### Partners actually use it
The biggest challenge with partner portals is adoption. When you reduce deal registration from a 10-field form to a single message like "Register a deal for Acme Corp, 50k, closing Q3, new business" , partners stop avoiding the process and start using it.
#### Better data quality
Introw's agent validates and structures every input before writing to your CRM. It asks clarifying questions when information is missing and maps values to your existing picklists and fields. The result is cleaner pipeline data with fewer manual corrections.
#### Less operational overhead
Your partner managers spend less time chasing partners for deal details or manually entering data on their behalf. The agent handles the back-and-forth, so your team can focus on strategy and relationship building.
Introw's actionable agents are available everywhere your partners and team operate:
- Partner portal , built into the Introw partner experience
- Slack , via the Introw agent in shared and internal channels
- MS Teams , via the Introw Agent in shared and internal channels
- Email so partners can act on prospects, deals directly from their mailbox
No matter where the conversation happens, the agent can take action in any preferred communication channels.
### The bottom line
An AI that only answers questions is a knowledge base with a chat interface. An AI that takes action is a force multiplier for your partner program. Introw's agents turn every partner interaction into structured, CRM-ready data, without the friction.
- Tracking Partner involvement on deals
- Save time with Introw’s AI Agent
- Introw's AI Agent in Slack
- Partner Connect: a 2-way CRM integration with HubSpot
- What is Partner Connect?

---

## AI course builder and live tutor
Source: https://support.introw.io/en/articles/14498766-ai-course-builder-and-live-tutor

Creating partner enablement content is only half the battle. The real challenge is making sure partners actually learn and retain what you teach them. Static slide decks and one-way video courses have notoriously low knowledge retention. Partners complete them to check a box, not to build lasting understanding.
Introw's AI course builder takes a fundamentally different approach to partner enablement.
### Build courses from what you already have
You don't need to start from scratch. Introw's AI course builder generates structured courses from two sources:
- Your knowledge base : existing help articles, FAQs, and documentation you've already written
- Uploaded documents : sales playbooks, product guides, competitive battlecards, onboarding materials, or any document you upload
The AI structures the content into a logical learning path, breaking it into digestible modules with clear learning objectives. What used to take days of instructional design now takes minutes.
### Conversational assessments that actually test understanding
Traditional quizzes (multiple choice, true/false) test recall, not understanding. Introw's conversational assessments work differently:
- AI-generated questions that adapt to the content of each module
- Open-ended, conversational format where partners explain concepts in their own words rather than picking from a list
- Adaptive follow-ups that probe deeper when a partner's answer shows a gap in understanding
- Instant, contextual feedback so partners learn from their mistakes immediately, with explanations grounded in your actual content
This approach mirrors how real learning works: through dialogue, not checkboxes.
### Live AI tutor: always-on support inside every course
This is a game-changer for knowledge retention. Every Introw course includes a live AI tutor that partners can interact with in real time while going through the material.
Partners can:
- Ask questions about anything in the course and get instant, contextual answers
- Request deeper explanations of complex concepts
- Explore tangential topics ("How does this apply to healthcare verticals?") and get relevant responses grounded in your enablement content
- Revisit material in a conversational way, rather than re-reading static pages
The tutor is grounded in your actual knowledge base and documents, so it always gives answers that align with your messaging and processes.
#### Higher knowledge retention
Active learning (conversational assessments + live tutoring) produces dramatically better retention than passive consumption. Partners who truly understand your product sell it better.
#### Faster partner ramp
New partners get up to speed faster because they can ask questions and get immediate help, rather than waiting for your team to respond or scheduling a training call.
#### Scalable enablement
The AI tutor is available 24/7 to every partner, in every time zone. Your enablement scales without scaling your team.
Partner enablement should be a competitive advantage, not a checkbox exercise. Introw's AI course builder, conversational assessments, and live AI tutor turn your existing content into an interactive, adaptive learning experience that partners actually retain, and that drives better selling outcomes.
- Partner training courses
- How to use Introw's course builder
- Course Settings
- Using the AI Conversational Quiz
- Introw Product update - May 2026

---

## AI channel conflict resolution
Source: https://support.introw.io/en/articles/14498771-ai-channel-conflict-resolution

Channel conflict is inevitable in any growing partner program. Two partners claim the same account. A direct sales rep is already working a deal a partner just registered. An inbound lead lands that overlaps with an existing partner opportunity.
How you handle these conflicts defines partner trust. Handle them poorly, or slowly, and partners disengage. Handle them fairly and transparently, and partners invest more. 
Introw AI transforms channel conflict from a gut-feel judgment call into a structured, data-backed decision .
#### Full 360° CRM context at the point of decision
When a new deal registration or inbound lead comes in, Introw's AI automatically assesses it against your complete CRM picture:
- Existing pipeline : is there already an open opportunity with the same account? At what stage? How active is it?
- Historical engagement : has a partner been working this account? For how long? What's their activity level?
- Partner relationships : which partners have existing relationships with the account? What's their track record?
- Direct sales activity : is your direct team already engaged? What stage are they at?
- Deal details : how do the competing registrations compare on deal size, expected close date, and strategic fit?
All of this context is pulled automatically from your CRM and presented to the channel partner manager in a single, structured view.
### Guided recommendations, not just data
Introw doesn't just surface information. It provides a clear recommendation. The AI weighs the evidence and suggests a course of action, along with the reasoning behind it. Your channel partner manager still makes the final call, but they do so with:
- Complete visibility into all relevant data points
- A structured recommendation they can accept, adjust, or override
- Documented rationale that can be shared with partners for transparency
### Why this matters
##### Faster resolution
No more digging through CRM records, cross-referencing spreadsheets, or asking three colleagues for context. The AI gathers everything in seconds, so conflicts are resolved in minutes rather than days.
##### Fairer outcomes
Decisions backed by data are inherently more defensible than decisions based on who complained loudest. Partners see a transparent, consistent process, and that builds long-term trust.
##### Proactive conflict detection
Introw doesn't wait for partners to raise a conflict. It flags potential overlaps as new registrations come in, so your team can address issues before they escalate.
- AI detected channel conflict resolution
- How Introw keeps your CRM clean
- AI Deal Coach
- Introw's AI Agent in Slack
- AI agents that actually take action for your partners

---

## Connect Introw AI to Notion, Lovable, OpenClaw, and beyond
Source: https://support.introw.io/en/articles/14498781-connect-introw-ai-to-notion-lovable-openclaw-and-beyond

Introw ships with its own MCP (Model Context Protocol) server , giving you a standardized way to connect your partner intelligence to a rapidly growing ecosystem of AI-powered tools, far beyond just Claude.
Model Context Protocol (MCP) is an open standard that allows AI tools and applications to share context, data, and capabilities. Think of it as a universal connector for AI: any tool that supports MCP can talk to any other MCP-compatible tool.
Introw's MCP server exposes your partner data, intelligence, and actions as MCP resources, making them available to any tool in the MCP ecosystem.
Because MCP is an open standard, the list of compatible tools is growing rapidly. Today, Introw's MCP server connects with tools like:
- Claude for natural language access to partner intelligence
- Notion to pull partner data directly into your workspace, docs, and databases
- Lovable to build partner-powered applications and workflows with AI
- OpenClaw to integrate partner data into your broader AI and automation pipelines
- And more : any tool that implements the MCP standard can connect to Introw
#### Partner data everywhere you need it
Instead of Introw being one more tab to check, your partner intelligence travels with you. Building a deck in Notion? Your partner metrics are there. Automating a workflow in Lovable? Introw's deal and engagement data is available as a data source.
#### Actions, not just data
Introw's MCP server doesn't just expose read-only data. It also exposes actions, meaning connected tools can register deals, create tasks, and update records in Introw, all through the MCP interface.
#### Composable AI workflows
MCP lets you chain tools together. Pull partner data from Introw, process it in Claude, and push the output to Notion, all as a single, automated workflow. The possibilities expand with every tool that joins the MCP ecosystem.
#### No custom integrations needed
MCP is a standard protocol, not a custom API integration. You connect once, and every MCP-compatible tool can access Introw's data and actions. No engineering time required for each new connection.
#### Future-proof connectivity
As the MCP ecosystem grows, Introw automatically becomes connectable to more tools. Every new MCP-compatible application is a potential new destination for your partner intelligence.
#### Control and security
You control which data and actions are exposed through the MCP server. Partner data only flows where you allow it, with the same security and access controls you expect from Introw.
Introw's MCP server turns your partner ecosystem intelligence into a portable, composable asset. Connect it to Claude, Notion, Lovable, OpenClaw, or any MCP-compatible tool and let your partner data work wherever your team does.
Check out this great use case of Quatt
- Using your MCP Server with Introw’s AI Agent
- Install the Claude connector of Introw
- Give your partners their own AI assistant to collaborate in real time via Introw's Partner MCP
- 🚀 Customer Deep Dive: How Quatt Powers Installer Operations with the Introw MCP
- Using Introw with Gemini via MCP

---

## AI deal coaching: an expert sales coach in every partner deal
Source: https://support.introw.io/en/articles/14498787-ai-deal-coaching-an-expert-sales-coach-in-every-partner-deal

Your best partners close deals because they understand your product, your sales process, and how to handle objections. But not every partner has that level of expertise, and even the best ones encounter deals where they need guidance.
Introw's AI deal coaching puts an expert sales coach in every single deal . One that knows your process, your materials, and the specific context of the opportunity at hand.
### What the AI deal coach knows
Every deal in Introw gets its own AI coach that is deeply grounded in:
- Your sales process : the specific stages, milestones, and criteria your organization uses to move deals forward
- Objection handling frameworks : how your team addresses common pushbacks, competitive comparisons, and pricing concerns
- FAQ and enablement material : product positioning, feature documentation, use cases, and competitive battlecards
But knowledge alone isn't enough. What makes Introw's deal coaching powerful is that it's always contextual to the specific deal .
### Context-aware coaching for every deal
The AI coach doesn't give generic advice. It understands the real-time context of each deal:
- Deal stage : recommendations adapt based on whether the deal is in discovery, evaluation, negotiation, or closing
- Vertical : guidance is tailored to the industry the prospect operates in, surfacing relevant case studies and positioning
- Engagement signals : the coach factors in deal activity like competitor mentions, objections raised, comments from stakeholders, and partner engagement patterns
- Deal history : everything that's happened on the deal so far (every comment, update, and interaction) informs the coaching
This means the coach's advice is never generic. It's specific, timely, and actionable for that exact deal.
### Available everywhere partners need it
Deal coaching isn't locked behind a portal login. It's embedded across every touchpoint where partners interact with deals:
- Partner support agent : partners can ask the AI agent in the portal for deal-specific coaching at any time
- Slack Introw Agent (coming soon) : via the Introw Slack agent in shared channels, partners get coaching advice right where the conversation is happening
- Email deal updates : when deal updates are sent via email, coaching insights are included alongside the update, giving partners guidance without them having to ask
- Slack deal notifications : deal update notifications in Slack also include contextual coaching, so partners get proactive guidance with every status change
Partners receive coaching where they already are, not where you wish they'd go.
### Why this transforms partner-led selling
Partner-sourced pipeline is only as strong as the partners selling it. Introw's AI deal coaching ensures every partner, on every deal, has instant access to expert guidance that's specific to the opportunity they're working, delivered wherever they are, whenever they need it.
- Tracking Partner involvement on deals
- AI Deal Coach
- Introw's AI Agent in Slack
- Set up the Partner Connect Card in HubSpot
- The Introw-Powered Partner: A Day in the Life

---

## Show Introw course enrollments and certificates in Salesforce
Source: https://support.introw.io/en/articles/14595957-show-introw-course-enrollments-and-certificates-in-salesforce

Introw syncs partner course enrollments and certificates directly into Salesforce. By adding Introw's related lists to your Salesforce page layouts, your team can track a partner's learning progress and earned certificates without ever leaving Salesforce.
### Before you start
- You must have the Introw app connected to Salesforce Introw installations created before January 1, 2026 must be reconnected to enable the course enrollment and certificate objects in Salesforce. Reconnecting the app grants the additional permissions required for Introw to sync course and certificate data into your Salesforce org. New installations made on or after January 1, 2026 already include the required permissions. Learn more about connecting Salesforce to Introw 
- Introw installations created before January 1, 2026 must be reconnected to enable the course enrollment and certificate objects in Salesforce.
- Reconnecting the app grants the additional permissions required for Introw to sync course and certificate data into your Salesforce org.
- New installations made on or after January 1, 2026 already include the required permissions.
- Learn more about connecting Salesforce to Introw 
- You need Salesforce admin permissions to edit page layouts This is required to add Introw related lists to your Account and Contact page layouts.
- This is required to add Introw related lists to your Account and Contact page layouts.
Reconnecting ensures Salesforce can securely access the data needed to display Introw course enrollments and certificates on your records.
### Add Introw course cards to Account page layouts
Introw syncs course enrollment and certificate data at both the Account and Contact level. To see this data on your records, you need to add the Introw related lists to the relevant Salesforce page layouts.
To add the Introw course enrollment and certificate related lists to Account records:
- In Salesforce, go to Setup
- Navigate to Object Manager and select Account
- Click on Page Layouts
- Select the page layout you want to edit
- Scroll to the Related Lists section in the layout editor
- Drag the Introw Course Enrollments and/or Introw Certificates related lists into the Related Lists section of the layout
- Save your changes
💡 Introw Tip : If you use Lightning Record Pages, you can also add these components via the Lightning App Builder . Edit the Account record page, drag a Related List component onto the layout, and select the Introw Course Enrollments or Introw Certificates list.
### Add Introw course cards to Contact page layouts
To track individual partner contacts' learning progress and certifications, add the same related lists to your Contact page layout:
- Navigate to Object Manager and select Contact
- Drag the Introw Course Enrollments and/or Introw Certificates related lists into the Related Lists section
- Save your changes 
💡 Introw Tip : Repeat these steps for any other objects or page layouts where you want Introw course data to appear.
### What you'll see in Salesforce
Once the related lists are added, Introw displays course enrollment and certificate data across your Salesforce records. This setup gives your sales, support, and partner teams full visibility into training and certification status, directly inside Salesforce.
- Account record: See all course enrollments and certificates for the partner company. Each enrollment is shown for every partner contact, and each certificate reflects every certified contact within the account. Introw gives you a complete overview of your partners' learning activity and certification status at the account level. 
- Contact record: Track individual partner contacts' certifications and which certificates they have earned. Course enrollments are also visible on the Contact record, giving your team a complete view of each contact's learning progress and achievements.  
- Link your Salesforce opportunities to Introw via a relation table
- Opportunity registration with Introw and Salesforce
- How to use Introw's course builder
- Show Introw course enrollments and certificates in HubSpot
- How to use Introw forms with Salesforce

---

## Notification settings
Source: https://support.introw.io/en/articles/14616921-notification-settings

Introw lets you configure notification settings per role, so every new team member automatically inherits the right defaults the moment they're assigned a role. Whether you're onboarding a new partnership manager or a RevOps team member, they'll receive exactly the notifications that make sense for their responsibilities, no manual setup needed. 
#### Available options per notification type
Depending on the notification type, you can choose from:
- All partners, Get notified for activity across your entire partner base.
- Own partners, Only get notified for partners assigned to you.
- Collaborating only, Only get notified for partners you're actively collaborating with.
- Disabled, Turn off that notification entirely.
Not every option is available for every notification type. Some only support a subset of these options. You can also use the toggle at the top of each category to enable or disable all notifications within that group at once.
#### Where to manage notification settings
Notification preferences can be managed in three places:
- On a role (recommended): The most efficient way to manage notifications is at the role level. Any notification settings configured on a role are automatically applied to all users with that role, making it easy to roll out consistent defaults across your team without any manual per-user setup. 
- Your own profile : Each user can update their notification settings directly from their profile settings, without needing admin access. User-level settings override the role defaults. 
- As an admin : Admins can view and manage notification settings for any team member from Settings > Team > Users. Click on a user and navigate to the Notifications tab to configure their preferences. Useful for one-off adjustments without changing the role defaults. 
- Add your team to Introw
- Introw tasks
- Roles and permissions
- Segments in Introw
- Send notifications from your own email domain

---

## Multi-language support
Source: https://support.introw.io/en/articles/14618143-multi-language-support

Running a global partner program means working with partners across languages. Manually translating every touchpoint creates friction and takes tons of time and resources. While asking partners to navigate in an unfamiliar language only makes it worse!
Introw removes that friction. Multi-language support auto-translates the full partner experience from the portal to forms and courses, in up to 97 languages , so every partner engages in the language they're most comfortable with.
#### Adding languages
To get started, navigate to your languages under settings and add the languages you want to support. 
Once a language is added, Introw automatically translates all partner-facing content into that language. This includes:
- Portal pages, all portal content your partners see
- Forms, registration forms, deal registration forms, and any other forms partners interact with
- Courses, all course content, modules, and assessments
- Email content - All CRM property related fields of deal updates are auto-translated. (eg. Deal amount => Importe de la operación etc).
There's no need to manually translate each piece of content. Introw handles the translation automatically across every touchpoint.
Add languages while working in the experience builder. When working within your experience builder you can preview the partner experience in the available languages to see how it will look and also add additional languages if needed. 
### Glossary
Some terms should never be translated, brand names, product names, technical terminology, or any other words specific to your business.
Introw includes a built-in glossary where you can add terms that should remain untranslated, regardless of the partner's language. This ensures your brand identity and product naming stay consistent across every language and every partner interaction.
### Setting a partner's language
Introw gives you multiple ways to control which language a partner sees when interacting with the portal:
##### Partner level
You can set a default language on the partner company. This applies to all contacts within that partner unless overridden at the contact level. 
##### Partner contact level
If you know the preferred language of a specific partner contact, you can set it directly on that contact. This takes priority over the partner-level default. 
#### Partner language switching
Partners are always in control of their own experience. If a partner prefers a different language than what was detected or assigned, they can switch their language at any time from their profile settings. Once changed, Introw automatically updates the entire portal experience to reflect the selected language.
#### How Introw determines the language
Introw follows a clear priority order when determining which language to show a partner contact
- Partner contact language, if set manually or changed by the partner themselves, this always takes priority. 
- Browser-detected language, if no language has been set on the partner contact, Introw automatically detects the partner's preferred language on their first portal visit, based on browser settings. This applies only if a translation exists for that language, otherwise Introw falls back to the next option. 
- Partner-level default, the default language set on the partner company, used as the final fallback.
#### Managing assets in multiple languages
Multi-language support goes beyond the portal interface, it also applies to assets. With multi-language enabled, you can add translated variants of specific assets (sales decks, product specs, case studies, marketing materials, training resources) without creating separate asset library sections for each language. Introw intelligently serves the variant that matches each partner's language preference.
##### How asset variants work
Asset variants let you keep a single asset entry with multiple language versions, no duplicate libraries, no messy folder structures. 
- Automatic language matching, Introw serves the variant matching the partner's profile language.
- Smart fallback, if no variant exists for their language, the default version is shown instead.
- Partner choice, partners can switch their language and access any available variant from the asset details.
For a full walkthrough of asset variants see Managing assets in multiple languages . 
#### Available languages
Up to 97 languages are supported in your Introw's partner portal experience.
- Afrikaans
- Albanian
- Aragonese
- Armenian
- Assamese
- Aymara
- Azerbaijani
- Bashkir
- Basque
- Belarusian
- Bengali
- Bosnian
- Breton
- Bulgarian
- Burmese
- Catalan
- Chinese
- Croatian
- Czech
- Danish
- Dutch
- English
- Esperanto
- Estonian
- Finnish
- French
- Galician
- Georgian
- German
- Greek
- Guarani
- Gujarati
- Haitian Creole
- Hausa
- Hindi
- Hungarian
- Icelandic
- Igbo
- Indonesian
- Irish
- Italian
- Japanese
- Javanese
- Kazakh
- Korean
- Kyrgyz
- Latin
- Latvian
- Lingala
- Lithuanian
- Luxembourgish
- Macedonian
- Malagasy
- Malay
- Malayalam
- Maltese
- Maori
- Marathi
- Mongolian
- Nepali
- Norwegian (bokmål)
- Occitan
- Oromo
- Polish
- Portuguese (Brazil)
- Portuguese (Portugal)
- Punjabi
- Quechua
- Romanian
- Russian
- Sanskrit
- Serbian
- Sesotho
- Slovak
- Slovenian
- Spanish (Latin America)
- Spanish (Spain)
- Sundanese
- Swahili
- Swedish
- Tagalog
- Tajik
- Tamil
- Tatar
- Telugu
- Thai
- Tsonga
- Tswana
- Turkish
- Turkmen
- Ukrainian
- Uzbek
- Vietnamese
- Welsh
- Wolof
- Xhosa
- Zulu
- How to create a partner portal
- Create new partners via Introw
- Partner activity events in your HubSpot timeline
- Task actions
- Managing assets in multiple languages

---

## Managing assets in multiple languages
Source: https://support.introw.io/en/articles/14621002-managing-assets-in-multiple-languages

### Overview
When multi-language support is enabled in Introw, you can now add translated variants of specific assets without creating separate asset library sections for each language. Introw intelligently visualizes assets based on your partner's language preference, streamlining asset management and improving the partner experience. 
### How to add translated assets?
Asset language variants let you create language-specific versions of the same asset  like sales decks, product specs, case studies, marketing materials, training resources all organized within a single entry. No duplicate libraries, no messy folder structures. Just one asset, with every language variant in one place.
- Open an asset, go to your Asset Library and create a new asset or open an existing one.
- Add a translation, Select the Languages and check the button to add a variant of a language for the specific assets.
- Upload the file, upload the translated asset (PDF, video, image, or other file type). That's it, the variant is immediately available alongside the original
#### Managing Variants
- Replace file : open the asset, select the language variant, and upload a new file.
- Remove tranlation : remove a variant without affecting the original or other variants.
### How it will work for the partner
When a partner accesses the asset library, Introw automatically serves the variant that matches their language, based on their profile language or default partner language.
- Automatic language matching, Introw serves the variant matching the partner's profile language.
- Smart fallback, if no variant exists for their language, the default version is shown instead.
- Partner choice, partners can switch their language and access any available variants (translations) from the asset details.
### FAQ
##### What happens if a partner's language doesn't have a variant?
Introw will display the default version of the asset (typically the original language) if no variant exists for the partner's preferred language. You can gradually add variants as translations become available.
##### Do I need to create separate assets for each language?
No. With asset variations, you maintain a single asset entry with multiple language variants. This keeps your asset library organized and easier to manage.
##### Can partners download variants in languages other than their preference?
Yes. Partners can change their language and get access to any available language variant from the asset details. 
- Asset library
- Manage your assets in the asset library
- Partner Asset Hub
- Creating Co-branded assets
- Multi-language support

---

## 13 little Introw tricks you probably didn't know about
Source: https://support.introw.io/en/articles/14635252-13-little-introw-tricks-you-probably-didn-t-know-about

Big features tend to get all the attention. But some of the best parts of Introw are the little details, the things that save you five minutes here, eliminate a workaround there, or just make the portal feel more yours . Here are 13 tricks worth knowing about.
#### 1. Let your CRM validate form submissions automatically
When a partner submits a form, Introw automatically checks every mapped field against the validation rules defined in your CRM, phone number formats, postal code patterns, required fields, numeric ranges, all of it. If something doesn't match, the partner gets prompted to fix it before submission goes through.
No setup needed. Introw reads your CRM's existing rules, so your data stays clean without any extra configuration.
Learn more →
#### 2. Let Introw match form submissions to existing CRM records
When a partner submits a form, Introw's AI automatically suggests matching records already in your CRM, based on name, domain, and email. If the match isn't right, you can adjust or correct it before confirming. This prevents duplicate records and keeps your CRM clean without manual lookups.
#### 3. Use custom association labels on form automations
When setting up form automations, Introw lets you override the default CRM association labels for linked objects. For example, when a lead comes in through a partner form, you can automatically label the contact-to-company relationship as "End Customer" or "Billing Contact", giving your CRM records the right context from day one.
Find this in the Advanced section of any form automation step.
#### 4. Personalise your portal at scale with dynamic variables
Type { anywhere in the Experience Builder to insert a dynamic variable, partner first name, company name, or any other contact property. Introw fills in the right value for each partner automatically when they log in.
You set it up once in the experience. Every portal linked to it gets the personalisation automatically. A small touch that makes every partner feel like the portal was built just for them.
#### 5. Choose a tab layout that fits your content
Not every tab needs the same amount of space. Introw lets you choose between three layout options per tab: Centered , Expanded , or Full Width . Full width is perfect for deal pipelines where you need maximum horizontal space. Centered keeps things clean and readable for text-heavy content.
Click the three dots on any tab, select Layout , and pick the one that works best.
#### 6. Add custom section backgrounds
Every section in your portal can have its own background colour or image. Use this to visually separate content areas, highlight important sections, or add branded banners that make the portal feel like a natural extension of your marketing site.
#### 7. Upload your own brand font
Introw supports custom font uploads, just add a variable font file (TTF) and it applies across the entire partner experience: portal, announcements, certificates, and email notifications. It's a small detail that makes a big difference in how polished and on-brand the portal feels.
#### 8. Split any section into columns
Need a two-column layout? A three-column grid? Introw lets you divide any section into up to 8 equal parts , or manually resize columns to custom widths. Great for side-by-side content like an image next to a text block, or a set of CTA cards in a row.
#### 9. Maximise sections to remove white borders
If you want content to take up the full section area, like a banner image or an embedded video, just maximise the section. This eliminates the default white padding around your content, giving you a cleaner, edge-to-edge look.
#### 10. Choose how announcements look in the portal
Introw gives you three display layouts for the announcement section: list , card , or posts . You can also control how many announcements show upfront, partners can always click "view more" to see the full archive. Pick the layout that fits the vibe of your portal.
#### 12. Show the right partner manager automatically
Add the Introduction section to your experience and Introw automatically displays the assigned partner manager's name, email, job title, and meeting link, personalised for each partner when they log in. No manual setup per portal.
Pro tip: Make sure each partner manager adds their meeting link in their profile (bottom left of the app). That way partners can book time in one click.
#### 13. Upload SCORM content straight into Introw
Already have e-learning content? Introw now supports SCORM file uploads directly into the course module. Upload your existing training content and put it to work immediately, no rebuilding required. Once uploaded, SCORM courses behave like any other Introw course: assignable via CRM filters, with deadlines, completion tracking, and reporting included.
Learn more about courses →
- Add your team to Introw
- Create new partners via Introw
- Introw's Zapier Integration
- How to use Introw's course builder
- Introw product update - March 2026

---

## Using file uploads to verify partner expertise
Source: https://support.introw.io/en/articles/14653179-using-file-uploads-to-verify-partner-expertise

Course Quizzes just got more practical. While AI coaching and agentic grading handle the theory, the new File Upload question type verifies hands-on skill. Now, you can require partners to submit "proof of work", like a screenshot of their demo instance or a video walkthrough, to ensure they’re truly ready for the field.
### Why file uploads in Quizzes?
Knowing something and being able to do it are not the same thing. A partner can pick the right multiple-choice answer on integration setup and still freeze the first time they're sitting in front of the actual product.
A file upload question is the cheapest way to tell the two apart. The partner does the task, captures the result, and attaches it, without leaving the Course, and without you having to set up a separate hands-on exercise.
Step 1: Add a file upload question to your Quiz  Open the Quiz builder in any Introw Course and pick File Upload as the question type. Be precise about what you want, vague prompts get vague submissions. Something like "Configure use case X in your demo environment and upload a screenshot of the finished result" works far better than "Upload proof of your setup."
#### Step 2: Partners upload their files
The upload question shows up alongside whatever else is in the Quiz. Partners can drag and drop or browse from their device, images, PDFs, and common document formats are all accepted.
Step 3: Review partner submissions  Each uploaded file is stored against the partner's Quiz attempt, right next to their other answers. Open the submission, look at the file, decide whether the partner is ready to move forward.
Implementation partner certification, Before partners are cleared to deliver for customers, have them upload a screenshot of their demo environment with the required configuration in place. One look at the image tells you whether they're ready.
Technical knowledge validation, Ask for an architecture diagram, an integration write-up, or an exported config. You get a window into how partners actually reason about your product, not just whether they can pick the right option from a list.
Onboarding proof of completion, Build the file upload into the onboarding Quiz itself, so partners can't simply click through the exercises, they have to do them, and then show you.
### Best practices
The clearer your prompt, the cleaner the submission. Spelling out exactly what should be visible in the file, "a screenshot of your configured demo instance with the user list visible", gets the right artifact on the first try and saves you a round of follow-up. And don't treat file uploads as a replacement for the other question types: mix them in the same Quiz, so a single Quiz attempt gives you both the partner's reasoning and the proof that they can put it into practice.
- How to use Introw's course builder
- Using the AI Conversational Quiz
- Introw Product update - May 2026
- How partners request MDF funds, submit claims, and upload invoices

---

## How to use Introw forms with HubSpot
Source: https://support.introw.io/en/articles/14689113-how-to-use-introw-forms-with-hubspot

Introw forms give you the flexibility to create forms for your partners to fill in for any use case you might have and to use them inside or even outside your partner portal while automating the creation towards HubSpot and giving you the ability to collaborate on your partners' form submissions. 
### How to create a deal form
Go to the "Form Builder" in the navigation menu to access an overview of suggested forms provided by Introw. You can also create a form from scratch.  We recommend starting with Introw's preconfigured deal form and adjusting it to your needs. 
The Form Builder is a fully flexible form editor that lets you seamlessly link form fields to your HubSpot properties, such as Pipeline, Deal amount, Close date, Deal stage, and more. Any object (deals, companies, contacts, tickets or custom objects) or property in HubSpot can be connected to fields in your Introw form, all without any coding required. 
### Automatic HubSpot property validation
Introw automatically validates form submissions against your HubSpot property rules, no additional setup required.
When a partner submits a form, all mapped fields are checked against the validation rules defined on your HubSpot properties (such as phone number formats, ZIP/postal code patterns, required formats, numeric ranges, or custom property rules). If a value doesn't meet HubSpot's requirements, the submission is blocked and the partner is prompted to correct the field.
Because validation is driven directly by your HubSpot configuration, your existing data rules are always enforced, ensuring clean, consistent data and protecting the integrity of your HubSpot portal out of the box.
### How to automate the partner attribution towards HubSpot
When a partner shares a deal with you via the Introw form, either directly from the portal or through off-portal collaboration ( learn more here ) the deal, ticket or other object you are creating with the Introw form is automatically attributed to them using the method configured in your HubSpot integration. This simple flow requires no special setup and ensures every deal is tracked correctly against the right company and contact in HubSpot.

With the multi-selector , you can credit partners for multiple roles on the same deal. For example, a partner can be marked as the partner-sourced partner while also being recognized for their role as a reseller. You can configure forms so that deals submitted through one form are automatically attributed to resellers, while another form can automatically credit distributors.
### Advanced automation options
Each automation step includes an Advanced section with extra control over how Introw handles created objects in HubSpot.
- Disable net new company creation When enabled, Introw will only attach the deal, ticket or contact to a company if the company already exists in HubSpot and never create new company records. 
- Custom association labels for company relations Override the default HubSpot association labels used when linking other created objects to this company. Use the Contact to Company association label option to select a label like "End Customer" or "Billing Contact". This way when a lead or deal comes in the prospect's contact information will be linked to the prospect company with that particular HubSpot association label. 
### The result in HubSpot
Below are two examples of a deal submitted by my partner, Microsoft, automatically created in my HubSpot account with the correct partner attribution. Introw adapts to your existing HubSpot setup, here are two common configurations:
Example 1, Custom property (Company dropdown) Partner attribution is stored in a custom "Partner Company" property on the deal, rendered as a dropdown that links directly to the partner's Company record on the deal record view. 
 Example 2, Association label Partner attribution is stored as a labeled association between the deal and the partner company (e.g. "Partner"), displayed in the associated companies card on the deal, supporting multiple partners per deal and native HubSpot reporting on association labels. 
All actions are logged in HubSpot's activity timeline events and notes on the deal, company, contact and ticket records, including the full details of the form submission. 
- How to attribute revenue to partners in HubSpot?
- Link your HubSpot deals to Introw via custom objects
- Link partners to leads in HubSpot
- How to use Introw forms
- How to use Introw forms with Salesforce

---

## How to use Introw forms with Salesforce
Source: https://support.introw.io/en/articles/14689114-how-to-use-introw-forms-with-salesforce

Introw forms give you the flexibility to create forms for your partners to fill in for any use case you might have and to use them inside or even outside your partner portal while automating the creation towards Salesforce and giving you the ability to collaborate on your partners' form submissions. 
Go to the "Form Builder" in the navigation menu to access an overview of suggested forms provided by Introw. You can also create a form from scratch.  We recommend starting with Introw's preconfigured deal form and adjusting it to your needs. 
The Form Builder is a fully flexible form editor that lets you seamlessly link form fields to your Salesforce fields, such as Pipeline, Amount, Close Date, Stage, and more. Any object (opportunities, accounts, contacts, cases or custom objects) or field in Salesforce can be connected to fields in your Introw form, all without any coding required. 
### Automatic Salesforce field validation
Introw automatically validates form submissions against your Salesforce validation rules, no additional setup required.
When a partner submits a form, all mapped fields are checked against the validation rules defined on your Salesforce fields (such as phone number formats, ZIP/postal code patterns, required formats, numeric ranges, picklist values, or custom validation rules). If a value doesn't meet Salesforce's requirements, the submission is blocked and the partner is prompted to correct the field.
Because validation is driven directly by your Salesforce configuration, your existing data rules are always enforced, ensuring clean, consistent data and protecting the integrity of your Salesforce org out of the box.
### How to automate the partner attribution towards Salesforce
When a partner shares an opportunity with you via the Introw form, either directly from the portal or through off-portal collaboration ( learn more here ) the opportunity, case or other object you are creating with the Introw form is automatically attributed to them using the method configured in your Salesforce integration.  This simple flow requires no special setup and ensures every opportunity is tracked correctly against the right account and contact in Salesforce.

Form field mapping
Each field on the Introw form is mapped directly to a Salesforce property on the opportunity (or any other object you're creating), so partner submissions flow straight into the right fields without manual cleanup. You can also set default values that are filled in dynamically at submission, for example, auto-generating the Opportunity Name from the partner and account 
You can also enhance the Introw form with additional automation steps to create any Salesforce object you need such as contacts, accounts, notes, cases or custom objects and link them to the appropriate partner when required. 
### The result in Salesforce
Below are two examples of an opportunity submitted by my partner, Microsoft, automatically created in my Salesforce org with the correct partner attribution. Introw adapts to your existing Salesforce setup, here are two common configurations: 
Example 1, Custom property (Account lookup dropdown) Partner attribution is stored in a custom "Partner Account" lookup field on the opportunity, rendered as a dropdown that selects the partner's Account record directly on the opportunity layout.
 Example 2, Relation table (junction object / related list) Partner attribution is stored on a related junction object (e.g. Partners), displayed as a table on the opportunity layout, supporting multiple partners, attribution roles, and split credit per deal.
All actions are logged in Salesforce's activity timeline and notes on the opportunity, account, contact and case records, including the full details of the form submission. 
- Connecting Salesforce to Introw
- Link your Salesforce opportunities to Introw via custom fields
- How to use Introw forms
- Opportunity registration with Introw and Salesforce
- How to use Introw forms with HubSpot

---

## AI-assisted form approvals
Source: https://support.introw.io/en/articles/14780170-ai-assisted-form-approvals

Form approval lets you require a human, and optionally an AI, to review a form submission before it becomes a record in your CRM. It's most often used to gate deal registrations and lead registrations from partners, but the same workflow applies to any Introw form: partner applications, support tickets, MDF requests, or any custom-object submission. 
### When to use form approval
Introw form approval is best when the review should happen alongside the partner, before any record hits your CRM. For deal or lead approvals, you can alternatively let your CRM handle sign-off (e.g. a "Pending registration" pipeline stage or a custom approval property ), pick whichever fits your team. 
Common uses:
- Deal registration, vet the opportunity and confirm partner attribution.
- Lead registration, qualify and route before pushing to the CRM.
- Partner applications, check program fit before partners are created.
- Any other form, quote requests, tickets, custom objects, etc.
### Enable approval on a form
- Open the form in Form Builder and go to the Automation step.
- Toggle on Require manual acceptance to proceed .
- Add the approver(s). Use a single approver for simple cases, or chain multiple approvers for sequential review (see below).
Once enabled, every new submission lands in Form submissions in pending status until it's approved or declined.
### Multi-step (sequential) approval
When more than one person needs to sign off, chain approvers on the same form. Submissions move through the chain step by step:
- Each approver only sees the submission once the previous step has been accepted, reviews always happen in the order you define.
- A decline at any step stops the workflow and notifies the partner. Later approvers don't need to weigh in.
- Every accept and decline is logged in the form activity timeline so the chain is fully auditable.
Example, deal registration: a Channel Manager approves the partner attribution first, then a Sales Director signs off on deals before the record is created in the CRM.
### AI pre-check before human approval
You can add an optional AI pre-check step before any human approver. The AI evaluates the submission against your acceptance criteria and gives the next reviewer:
- A clear recommendation (accept or decline) with the reasoning behind it.
- Suggested partner-ready communication the approver can send as-is or tweak before replying.
The human approver always makes the final call, the AI step simply gives them context up front so reviews are faster and more consistent. AI pre-check runs ahead of every human step, including across multi-step chains. 
### Review form submissions
Pending submissions live in the Form submissions view in your side navigation. Approvers receive an email notification, can comment back-and-forth with the partner, and click Accept or Decline from there. 
 For a full walkthrough, see How to manage form submissions .
### What happens after approval
As soon as a submission is fully approved, Introw pushes the data into your CRM using the automations configured on the form. Any relative-date default values (e.g. Close date = approval + 30 days) are calculated from the moment of full approval, so date fields stay aligned with the deal's actual lifecycle even when a submission spends time in review.
### Related articles
- How to use Introw forms
- How to manage form submissions
- How partner deal data syncs to your CRM
- How to manage form submissions?
- AI detected channel conflict resolution
- Market Development Funds (MDF)

---

## Partner Connect: a 2-way CRM integration with HubSpot
Source: https://support.introw.io/en/articles/15039830-partner-connect-a-2-way-crm-integration-with-hubspot

Partner portals are powerful, but they ask partners to step out of the tool they actually live in, their own CRM. Every login adds friction, every context switch slows the deal down, and a lot of the time partners simply forget. Introw Partner Connect closes that gap by bringing deal registration, deal collaboration and the partner portal directly into your partners' HubSpot.
### How Partner Connect works
Your partners install the Introw app from the HubSpot marketplace and pin the Partner Connect Card to their deal records. From that single card, they can register a new deal, link an existing HubSpot deal to your shared pipeline, get coaching on the next step, or open the partner portal, all without ever logging into Introw.
On your side, Introw keeps your CRM in sync. Whether you run on Salesforce, HubSpot or Pipedrive, every action your partner takes from their HubSpot flows into your CRM and the Introw shared deal pipeline you already use.
### What's included
- ✅ 1-click deal collaboration from the partner CRM Partners share deal updates with you straight from their HubSpot record, no portal login.
- 📝 Deal registration directly from the partner CRM Partners submit new deals to you without ever leaving HubSpot.
- 🔗 Deal linking via Introw's shared deal pipeline Partners link an existing HubSpot deal to your buyer-side CRM in one click.
- 🤖 Deal coach inside the partner CRM Introw surfaces next-best-action coaching directly on the deal record so partners always know what to do next.
- 🌐 Partner portal launch Partners open the full partner portal from the same card whenever they need it.
### Who can use Partner Connect
Partner Connect works whenever your partner is on HubSpot. On the vendor side, that's you, your CRM can be Salesforce, HubSpot or Pipedrive. Introw handles the translation between the two systems, so neither side has to change tools or rebuild their workflow.
Introw tip: Partner Connect is the lowest-friction way to onboard a new HubSpot partner. Most partners can install the app and submit their first deal in under five minutes.
### Key benefits
- Zero portal logins Partners never leave HubSpot to share a deal with you.
- Higher deal-registration volume Introw eliminates the biggest friction point of partner portals, so more deals get registered earlier in the cycle.
- Cleaner attribution Every deal that flows in from a partner's HubSpot is linked back to the right partner record in your CRM automatically.
- One source of truth Partner-side and vendor-side updates sync through the Introw shared pipeline, so nobody is working off a stale view.
### Get your partners set up
Share these videos with the partners you want to onboard:
- Set up the Partner Connect Card in HubSpot
- Validate your Partner Connect Card
- Link an existing HubSpot deal to your vendor
- Register a new deal from your HubSpot
Once the card is live, your partners are one click away from working with you, without ever opening a portal again.
- Create partner portal from within HubSpot
- Share a deal to partners via Introw's app card in HubSpot
- CRM User
- What is Partner Connect?

---

## Set up the Partner Connect Card in HubSpot
Source: https://support.introw.io/en/articles/15039839-set-up-the-partner-connect-card-in-hubspot

The Partner Connect Card is the home base for everything you do with your vendor from inside HubSpot, registering deals, linking existing deals, opening the partner portal and getting deal coaching. Introw drops the card straight onto your HubSpot deal record, so you never have to leave the tool you already work in. This guide walks you through the one-time setup.
### Add the Partner Connect Card to your deal record layout
In HubSpot, go to Settings → Objects → Deals → Record customisation , open the deal layout you want to update, and add the Introw Partner Connect middle-column card to the layout. Save the layout.
For an interactive, click-by-click walkthrough, follow the demo here: Setup Introw Partner Connect Card →
### What happens next
Once the card is on the layout, every HubSpot deal in your portal will show the Partner Connect Card. From there you can register new deals, link existing ones to your vendor, or jump straight into the partner portal for deals that are already linked.
Introw tip: Setup is a one-time action. After this, every teammate in your HubSpot account sees the same Partner Connect Card on every deal record automatically.
### Next step
Before you start using the card on real deals, take a moment to validate the connection, see Validate your Partner Connect Card .
- Show the Introw card inside HubSpot
- Share a deal to partners via Introw's app card in HubSpot
- Partner Connect: a 2-way CRM integration with HubSpot
- Validate your Partner Connect Card
- Link an existing HubSpot deal to your vendor

---

## Validate your Partner Connect Card
Source: https://support.introw.io/en/articles/15039840-validate-your-partner-connect-card

Once the Partner Connect Card is on your HubSpot deal layout, there's a quick validation step that confirms Introw recognises you, links you to the right vendor partner portal, and is ready to push deal data both ways. This article walks you through it.
### How to validate
For an interactive, click-by-click walkthrough, follow the Arcade demo here: Validate your Partner Connect Card →
### Why validation matters
The Partner Connect Card is the bridge between your HubSpot and your vendor's CRM. Validation is how Introw verifies that the HubSpot user opening the card matches an active partner contact in the vendor's portal. Without this step, deal registrations and links won't be attributed to the right partner record.
### How to tell it's working
Once validated, the Partner Connect Card will show your vendor's logo and the actions you can take, Collaborate. and Go to portal . If you see those actions, you're connected and good to go.
### Troubleshooting
- "We couldn't find your partner record" Ask the vendor admin to confirm your email address is on the partner contact in their Introw portal. Introw matches by email.
- The card is empty Make sure the Introw app is installed and the Partner Connect Card has been added to the deal layout, see Set up the Partner Connect Card in HubSpot .
### Next step
Now that the card is validated, you can start using it: Link an existing HubSpot deal to your vendor or Register a new deal from your HubSpot .
- Partner Connect: a 2-way CRM integration with HubSpot
- Set up the Partner Connect Card in HubSpot
- Link an existing HubSpot deal to your vendor
- Register a new deal from your HubSpot
- What is Partner Connect?

---

## Link an existing HubSpot deal to your vendor
Source: https://support.introw.io/en/articles/15039841-link-an-existing-hubspot-deal-to-your-vendor

A lot of partner deals are already in motion in your HubSpot before they ever get logged with the vendor. Instead of double-entering them in a portal, Introw lets you link an existing HubSpot deal to your vendor's shared pipeline directly from the Partner Connect Card. From that moment on, both sides see the same deal, and updates flow automatically.
### When to use deal linking
Use deal linking when:
- You already have a HubSpot deal that involves the vendor's product
- You already registered the deal via the Introw partner platform of your vendor.
- You want the vendor to be visible on the deal within your HubSpot
- You want vendor-side updates and coaching directly into your HubSpot
### How to link a deal
##### Step 1: Open your HubSpot deal
Open the deal in your HubSpot. The Partner Connect Card sits in the right column of the record. 
##### Step 2: Click "Collaborate"
On the Partner Connect Card, click Collaborate, select one of the already attributed deals you have registered in the past to your vendor via Introw and Link deal. 
### What happens after a deal is linked
Once a HubSpot deal is linked, Introw keeps both sides in sync through the shared deal pipeline:
- Deal collaboration is unlocked between your HubSpot and the vendor's CRM
- Notes and comments from the vendor appear on the Partner Connect Card
- Deal coach recommendations show up directly on the deal record
Introw tip: If a deal is genuinely new, meaning your vendor doesn't know about it yet, use Register deal instead. Linking is for deals the vendor is already aware of by submitting them via the Introw partner portal beforehand.
#### Troubleshooting
- How can I unlink a deal if I made a mistake? Under Actions you can select Unlink deal so the deal is no longer connected to that deal of your vendor and you can link the right one.  
- Share a deal to partners via Introw's app card in HubSpot
- Partner Connect: a 2-way CRM integration with HubSpot
- Set up the Partner Connect Card in HubSpot
- Validate your Partner Connect Card
- Register a new deal from your HubSpot

---

## Register a new deal from your HubSpot
Source: https://support.introw.io/en/articles/15039842-register-a-new-deal-from-your-hubspot

Deal registration is one of the most common reasons partners log into a vendor portal, and one of the easiest steps to skip when life gets busy. Introw removes that login altogether. With the Partner Connect Card on your HubSpot deal, you can register a new deal with your vendor directly from the deal record. This article shows you how.
### When to register a deal
Register a deal whenever you want to formally let your vendor know about an opportunity, to lock in attribution, qualify for incentives, or get vendor support on the deal. Registration creates a fresh record on the vendor side and links it back to your HubSpot deal automatically.
For an interactive, click-by-click walkthrough, check a demo here: Register a deal →
### How to register a deal
##### Step 1: Open your HubSpot deal
Open the deal in your HubSpot. The Partner Connect Card sits in the right column of the record. 
##### Step 2: Click "Collaborate"
On the Partner Connect Card, click Collaborate and Register deal . Introw opens the vendor's deal registration form right inside your HubSpot, pre-filled with the deal data already on the record (deal name, amount, close date, primary contact and company).
##### Step 3: Review and submit
Check the pre-filled fields, complete anything the vendor still needs (e.g. product, use case, expected go-live date, comments etc), and hit Submit . Introw routes the registration into the vendor's CRM and notifies their team.

### What happens next?
Once submitted:
- Introw creates the registration on the vendor's CRM (Salesforce, HubSpot or Pipedrive) and links it to your HubSpot deal through the shared deal pipeline.
- The Partner Connect Card on your HubSpot deal updates with the registration status (e.g. Pending , Approved , Rejected ).
- Vendor-side comments, stage changes and deal coach guidance flow back into your HubSpot record automatically.
Introw tip: Register the deal as early as you reasonably can. Earlier registrations protect your attribution and give the vendor's team time to bring the right resources to the deal.
- Linking deals to leads via Introw
- Partner Connect: a 2-way CRM integration with HubSpot
- Set up the Partner Connect Card in HubSpot
- Validate your Partner Connect Card
- Link an existing HubSpot deal to your vendor

---

## How does the integration with Microsoft Teams work?
Source: https://support.introw.io/en/articles/15054557-how-does-the-integration-with-microsoft-teams-work

Get instant notifications in Microsoft Teams when there are updates in your Introw partner portal and keep your partner collaboration at an all time high. All notifications on deal updates, form submissions, comments, mentions and task activity are pushed into your preferred Teams channel, both internal channels and shared channels with your partners.
In addition to notifications, the Introw AI Agent is available natively inside Microsoft Teams. Partners and internal users can register deals, add comments, create tasks, and pull partner insights directly from a Teams message, no portal hop required. Learn more about Introw AI agents .
Follow the steps below to learn how ⬇️:
- Go to Integrations and click Connect on the Microsoft Teams card
In Introw, navigate to Settings > Integrations and find the Microsoft Teams tile. Click Connect to start the authorization flow.
2. Sign in and grant permissions with your Microsoft 365 account 
You'll be redirected to Microsoft to sign in. Approve the requested permissions so Introw can post messages in your Teams channels and surface the Introw app to your users.
Remark: depending on your organization's policies, a Microsoft 365 Global Admin may need to grant tenant-wide consent before the integration becomes available to other users. If you hit a consent screen you can't approve, share the link with your IT administrator.
3. Link your shared Teams channels to a partner portal 
Once connected, you can map a shared Teams channel (a channel that includes external partner users) to the corresponding partner portal in Introw. All partner-facing notifications and AI Agent interactions for that partner will flow into the linked channel. 
Remark: if a channel doesn't appear in the dropdown, make sure the Introw app has been added to that Teams channel from the Microsoft Teams app store, and that the channel type (standard, private, or shared) is supported by your tenant's external collaboration settings.
4. Choose which internal notifications you want to receive into your linked internal Teams channels 
From the Microsoft Teams integration page, link an internal Teams channel and toggle which internal notification types you want to receive (e.g. notifications on all partners, only your own partners, or only partners you collaborate on).
5. Choose which partner notifications you want to receive into your shared Teams channels
You can do this in the navigation panel: Engage > Notifications and enable/disable the notifications you want pushed into the shared Teams channels with your partners (deal updates, form submissions, comments, mentions, task activity, sleeping deal nudges, etc.).
Once the integration is live, the Introw AI Agent works in any linked Teams channel, both internal and shared with partners. From a single natural-language message, users can:
- Register a deal by describing the opportunity in plain English. Introw structures and creates it in your CRM with all required fields.
- Add comments to any shared CRM object (deals, leads, companies) without opening the CRM.
- Create tasks with due dates and assignees to keep deals moving forward.
- Prepare QBRs and pull partner performance insights directly into the channel.
Everything is synced back to your CRM in real time, structured, clean, and attributed to the right partner.

- How does the integration with Slack work?
- How Introw keeps your CRM clean
- Introw's AI Agent in Slack
- AI agents that actually take action for your partners
- Microsoft Teams - Link private and shared channels🔒

---

## Microsoft Teams - Link private and shared channels🔒
Source: https://support.introw.io/en/articles/15054592-microsoft-teams-link-private-and-shared-channels

To use private or shared channels with the integration for Microsoft Teams , you must go into each private/shared channel in Teams and add the Introw app. A private channel in Teams is shown with a 🔒 icon, and a shared channel (which can include external partner users) is shown with a linked-people icon. For instructions on how to add the Introw app to one of these channels, read on!
 Step 1 
Open Microsoft Teams and navigate to the private or shared channel that you would like to use with the integration. Click the ••• (more options) icon next to the channel name and select Manage channel . From the channel settings, open the Apps tab and click Add an app .
Note: In Microsoft Teams, apps installed at the team level are not automatically available in private or shared channels. Each private and shared channel needs the Introw app added individually.
Search for " Introw " to locate the Introw app. Click Add to install it into the private/shared channel. 
Once added, the Introw bot will be a member of the channel and can post notifications and respond to AI Agent prompts inside that channel.
Note: You must repeat this process for each private or shared channel that you would like to use with the Microsoft Teams integration.
Go to your Introw account. Navigate to Settings > Integrations and click on the Microsoft Teams integration. The private or shared channel will now appear in the dropdown, link it to the appropriate partner portal.
Choose which internal notifications you want to receive in your connected Microsoft Teams channels, and configure partner notifications under Engage > Notifications for the channels shared with your partners.
If the private or shared channel still doesn't appear in the Introw dropdown after adding the app, try the following:
- Confirm the Introw app is listed in the channel's Apps tab (not just at the team level).
- For shared channels with external partner users, confirm your tenant allows external collaboration and that the channel owner has accepted any pending invitations.
- If the integration was authorized before the Introw app was published to your tenant's app catalog, disconnect and reconnect Microsoft Teams from Settings > Integrations in Introw, then refresh the channel list.
- If a Microsoft 365 Global Admin needs to approve the Introw app for your tenant, share the consent link with your IT administrator. Without admin approval, the app may not be installable in restricted channels.
Still stuck? Reach out to us at [email protected] and we'll help you get connected.
- Slack - Link private channels🔒
- How does the integration with Slack work?
- Add your team to Introw
- AI detected channel conflict resolution
- How does the integration with Microsoft Teams work?

---

## Governance and versioning
Source: https://support.introw.io/en/articles/15068953-governance-and-versioning

As your partner program scales, keeping track of who changed what and when can become critical. A renamed asset, an experience updated mid-quarter, or an access setting flipped from public to restricted can quietly break partner-facing content if no one notices.
Every change to an asset or a partner portal experience is logged automatically, and you can roll back to any previous version in one click, no support ticket, no manual restore, no lost work.
There are two types of versioning in Introw, each tracking a different surface of your partner program:
- Asset versioning, covers every change to files and content in your asset library.
- Experience versioning, covers every change to your partner portal experiences.
### Asset versioning
Asset versioning protects everything stored in your asset library, PDFs, videos, images, links, and their metadata. Whenever someone uploads a replacement file, renames an asset, or changes who can see it, that change becomes a restore point.
What gets tracked on an asset:
- Name changes, every rename of the asset
- Asset replacements, when a new version of a PDF, video, image, or link is uploaded
- Access changes, switches between Public, Portal, and Restricted access, including added or removed audience filters
- Category changes, when an asset is recategorized or moved
- Thumbnail updates, when a custom thumbnail is added, replaced, or removed
- Archiving and restoring, including the reason provided when archiving
#### Viewing the asset history
Open any asset and select the History tab from the detail view. You'll see a chronological log of every change made since it was first created. 
#### One-click version restore
Every asset replaced entry in the history log is a restore point. If a teammate replaces an asset with the wrong file, you can bring back the previous version instantly.
How to restore a previous version:
- Open the asset or experience and go to the History tab.
- Find the version you want to restore.
- Click Restore next to that entry.
The object reverts to the selected version immediately. The restore itself is logged as a new entry in the history, so the audit trail stays intact and you can always roll forward again if needed.
💡 Tip: Restoring a previous version doesn't delete newer history entries, every change before and after the restore stays in the log. This means you can safely experiment with restores without losing the record of what happened.
### Experience versioning
Experience versioning protects the partner portal experiences your partners actually see. Because experiences are made of sections, text, embedded assets, and styling, history captures changes at the section and content level, not just at the top of the page.
=> You can find the version history of an experience in the top right on the 3 dots.
What gets tracked on an experience:
- Sections added or removed, when a new section is dropped into the experience, or an existing section is deleted
- Text added or removed, every edit to a text block, including new paragraphs, deleted copy, and inline formatting changes
- Name and title changes, every rename of the experience itself or any of its sections
- Layout and visibility changes, when sections are hidden, shown, or layout updates happened
Each entry shows the user who made the change and the exact timestamp, giving you a complete audit trail for compliance reviews or internal investigations.
### Governance best practices
- Provide a reason when archiving. A short note explaining why something was archived helps your team decide later whether to restore or let it expire.
- Review the history before making changes. A quick glance at the log tells you when the current version was last updated and by whom, useful context before overwriting.
- Audit access changes regularly. Filter the history view for access-related changes to confirm that restricted assets and experiences are still scoped to the right partner segments.
- Coordinate large edits. For portal experiences shared with many partners, check the history to see recent changes by other teammates before publishing, this avoids overwriting in-flight updates.
- How to create a partner portal
- Asset library
- Manage your assets in the asset library
- Partner journeys
- Multi-language support

---

## Introw Product update - May 2026
Source: https://support.introw.io/en/articles/15183455-introw-product-update-may-2026

Last month's release is squarely focused on that: Introw now gives you a partner portal that adapts to every partner's preferred language, fine-grained team member roles for permissions and notifications, and proof of submission in courses to verify partners are putting what they learn into practice. Alongside those, we shipped a set of governance and AI improvements, and there's a sizeable Microsoft Teams integration on the runway.
Here's the full rundown. 🚀
### 🌍 Speak your partners' language
The partner portal is now multi-lingual. Each partner sees Introw in their preferred language, navigation, labels, forms, and announcements all adapt automatically. Not yours, not the language of your headquarters, and not whatever default the browser happened to pick. Every partner-facing surface is rendered in the language each partner has selected on their profile. Learn more 
For programs running across the globe, this is a major friction-remover. Partners in Japan, Germany, Brazil, or France no longer have to mentally translate every screen before they can do their job. They land in a portal that feels native, which means faster onboarding, higher engagement, and fewer "where do I find…" support tickets for your team.
A few things worth knowing:
- The portal auto-adapts the moment a partner visits the portal based on their browser language,  no admin action required per partner.
- Announcements and rich content you publish can be authored in multiple languages, so the right version is shown to the right audience.
- Your internal admin experience stays in your team's language; only the partner-facing side adapts.
### 👥 Team member roles: permissions and notifications
Different teammates need different views. Your channel manager doesn't need the same access as your legal reviewer. Your CFO probably doesn't want every deal-registration notification, but definitely wants the MDF spend ones. Team member roles let you define who sees what inside Introw and who gets notified about what, so every person on your team gets the right access and only the updates that matter to them. Learn more 
With roles you can:
- Scope what each teammate sees inside Introw, partners, deals, MDF requests, content libraries, courses, analytics, by role.
- Tailor notifications per role , so people only get pinged about the things that are theirs to act on. No more inbox noise from updates that don't concern them.
- Apply roles in bulk when you add new teammates, so onboarding a new channel rep doesn't mean a 20-minute permissions audit.
### Additional improvements
##### 📷 Proof of submission in courses
Quizzes prove partners read the material, not that they used it. That gap matters: a certified partner who never actually runs a demo or hosts an event isn't really enabled, they just passed a test. Learn more 
Proof of submission closes that loop. Add a required photo or video upload to any Introw course, a demo recording, a screenshot, an event photo, a signed customer artifact, to see the work itself. The submission becomes part of the partner's training record, so program managers can review the actual evidence before granting tier benefits, listing the partner publicly, or unlocking deal registration. It's a small change that turns enablement from a checkbox exercise into a verifiable practice.
##### 👀 Full audit trail, one-click rollback
Every change to your portal experiences and shared assets is captured, giving you an extra layer of governance. You can see who changed what and when, across content libraries and partner-facing portal experiences. If something goes wrong, a single click rolls it back to the previous version. A meaningful step up for teams who need to demonstrate change control or simply want a safety net. Learn more. 
##### 🤖 AI-assisted approvals
Every form submission flowing through Introw, MDF requests, deal registrations, partner applications, now gets an eligibility recommendation against your criteria before anything hits your CRM. The AI surfaces the relevant policy or rule, flags any missing information, and suggests an approve / decline / request-more-info action. The result: faster turnarounds, fewer back-and-forth emails, and cleaner data in your CRM. Learn more
### 🚀 Coming soon: Microsoft Teams integration
Introw turns Teams into an AI-powered partner workspace, right inside the shared channels where you collaborate with partners.
On one side: partner announcements, deal updates, and portal notifications stream directly into your Teams channels, no more tab-hopping to keep partners in the loop.
On the other side, the Introw AI Agent works alongside your team in the same channel. From a single message you can ask it to:
- Register a deal, captured in Teams, written straight to your CRM with the right partner attribution.
- Add comments or create tasks on partners, deals, or MDF requests without leaving the channel.
- Pull partner insights, tier, pipeline, recent activity, training status, on demand.
- Coach on open deals by surfacing next steps, missing information, and risk signals.
- Prep QBRs with a summary of partner performance, top deals, and program highlights ready to share.
- How to use Introw forms
- How to use Introw forms with HubSpot
- Introw's submission agent is now fully autonomous
- Introw Product update - June 2026
- Introw Product Update - July 2026

---

## Let Claude manage your partners, agentic partner updates via Introw
Source: https://support.introw.io/en/articles/15293107-let-claude-manage-your-partners-agentic-partner-updates-via-introw

### From answering to acting
Until now, Claude could read your partner program inside out, pipeline, goals, engagement, deal history. But the moment you wanted to act on what you saw, you had to switch tabs and open Introw.
That changes today. Introw now lets Claude update partner records directly from the conversation, turning insights into action without ever leaving the chat.
⚡ One workflow, one chat. Introw closes the gap between analysing your partner program and managing it, ask the question, get the answer, take the action, all in one place.
### What Claude can now manage for you
Through Introw, Claude can read and update the partner fields that drive your program day-to-day:
- Tier, promote, demote, or reassign partners across your tier structure
- Experience, adjust the partner's experience level
- Champion, set or change the partner's internal champion
- Phase, move partners through onboarding and lifecycle phases
- Commission plan, assign the right commission plan to each partner
- Manager, reassign the internal partner manager
- Currency & locale, keep partner localisation accurate
Anything Claude reads in Introw, it can now act on, within the same permissions you'd have if you were logged into Introw directly.
### A use case to try today: align partner tiers with actual performance
One of the most common questions in any partner program is also one of the hardest to answer at scale: which partners are sitting in a tier they're no longer earning?
With Introw + Claude, you can ask, decide, and act in a single conversation:
💬 "Check all my partners against their goals. For any partner that's significantly behind their tier targets, demote them one tier and add a comment nudging them to re-engage."
Here's what Introw does behind the scenes:
- Claude pulls each partner's current tier and live goal progress.
- It flags the partners that are materially behind their tier requirements.
- For those partners, Introw updates the tier to the level below and logs a comment on the partner record nudging them on next steps.
- You get a clean summary of what changed and which partners were touched.
What used to be a quarterly spreadsheet exercise becomes a single prompt.
#### More prompts to get you started
Promote your top performers
"Show me all Silver partners who have exceeded their annual revenue goal and promote them to Gold." 
Reassign managers after an org change
"Move every partner currently managed by Sarah to John, and add a comment introducing John as their new point of contact." 
Onboard new partners through the right phase
"For all partners that joined in the last 14 days and have completed their training, move their phase from Onboarding to Active." 
Tidy up partner categorisation
"Tag every partner with at least one closed-won deal in the SaaS vertical with the 'SaaS' category." 
Set the right champion
"For every partner in EMEA without a champion assigned, set their champion to their most active contact in Introw." 
### You stay in control
Agentic updates are powerful, so Introw makes sure you decide how far Claude can go on your behalf. For every action like updating a tier, changing a champion, or reassigning a manager, you choose one of three modes:
Mode
What it means
✅ Allowed
Claude performs the update automatically
🔔 Approval required
Claude proposes the change and waits for your confirmation
🚫 Blocked
Claude cannot perform this action at all
A common starting point: allow Claude to update soft fields like categories or champions freely, require approval before changes to tier or commission plan, and block anything you'd rather keep manual. You can adjust this at any time inside Introw.
🔒 Permissions, always enforced. Claude only ever sees and updates the partners and fields your Introw user has access to. If you can't change it in Introw, neither can Claude.
If Claude is already connected to your Introw workspace, partner management is enabled by default, just try one of the prompts above in your next Claude conversation.
If you haven't connected Claude yet, follow the setup steps in Install the Claude connector of Introw . For more inspiration on what's possible once you're connected, see Introw + Claude: use cases & what's possible . 
We'd love to hear how you're putting agentic partner management to work, the use cases our customers come up with always push us further. Reach out via the chat widget in your Introw portal, or email [email protected] . 🚀
- Install the Claude connector of Introw
- Introw + Claude: use cases & what's possible
- Give your partners their own AI assistant to collaborate in real time via Introw's Partner MCP
- The Introw-Powered PAM: A Day in the Life
- Using Introw with ChatGPT

---

## How to set up a MDF fund
Source: https://support.introw.io/en/articles/15308334-how-to-set-up-a-mdf-fund

Introw lets you spin up a Market Development Fund in minutes, define the budget, decide who can tap into it, and set the approval chain that protects every dollar. This article walks you through creating a fund from scratch.
#### 1. Create the fund
Head to MDF > Funds in your admin workspace and click New fund . Give the fund a name partners will recognize (e.g. "EMEA Co-marketing 2026" or "Reseller Event Pool"), and a short description that explains what the money is meant for.
#### 2. Choose a budget model
Introw supports two budget models, pick the one that matches how you want partners to access funds: 
- Fixed allocation: Assign a set amount to a specific partner, program, or campaign. Best when you want predictability and tight control over who gets what.
- Pooled budget: Allocate a total amount that any eligible partner can request against. Introw deducts from the pool as requests are approved. Best for rewarding the partners who bring the strongest opportunities forward.
You can run both models in parallel across different funds.
#### 3. Set the currency
Introw supports multi-currency funds out of the box. Pick the currency the fund will be denominated in, Introw handles conversion automatically when partners in other regions request against it, and keeps consolidated reporting in your reporting currency.
#### 4. Define eligibility
Decide which partners can see and request against this fund. Introw lets you scope eligibility by tier, region, program, lifecycle stage, or any custom partner property you already track within your CRM. Only eligible partners will see the fund in their portal.
#### 5. Configure the approval workflow
Every request submitted against the fund runs through the approval chain you define here. Use a single approver for simple programs, or chain multiple approvers for sequential review (e.g. Partner Manager → CRO → CFO). Introw's AI agent can pre-review each request against your rules, partner tier, and remaining budget, so approvers act on a recommendation instead of digging through context.
#### 6. Set claim rules
Define when partners must submit proof of execution and invoices after their request is approved. Choose a relative window (e.g. 30 days after campaign execution) or a fixed deadline (e.g. by December 31). Introw shows the deadline to partners upfront and tracks it on every claim.
#### 7. Save and publish
Once you save, the fund goes live in the portal for every eligible partner. They can submit requests immediately, and Introw tracks every allocation, approval, claim, and ROI attribution back to this fund from day one.
- Market Development Funds (MDF), overview
- AI-assisted form approvals
- Market Development Funds (MDF)
- How partners request MDF funds, submit claims, and upload invoices
- How to show the ROI of a MDF
- Introw Product update - June 2026

---

## How partners request MDF funds, submit claims, and upload invoices
Source: https://support.introw.io/en/articles/15308337-how-partners-request-mdf-funds-submit-claims-and-upload-invoices

From the partner side, Introw turns MDF into a self-service flow. Partners request funds, track approval status, and file claims with invoices directly from their portal, no email chains, no chasing for status updates. This article walks through that flow end to end.
#### Step 1: Submit a funding request
From the MDF dashboard in the partner portal, partners see every fund they're eligible for, along with available balance and submission deadlines. To request funds, they click New request on the relevant fund and fill in the embedded request form, typically campaign name, requested amount, planned activities, expected outcomes, and any supporting attachments. 
Once submitted, Introw routes the request through the approval workflow you've configured on the fund. Your partner managers can then review and approve requests faster with AI-assisted form approvals , which automatically surface key details, highlight compliance checks, and help streamline decision-making across your partner portfolio.
#### Step 2: Track approval status
Partners can follow every request through its full lifecycle from their dashboard. Introw shows the current status (pending, approved, declined, or adjusted), who is reviewing it, and the expected decision timeline. 
If your team adds a comment or requests changes on the request, the partner sees it instantly in the request timeline, and can reply back in the same thread. Every accept, decline, and comment is logged, so both sides have one source of truth on what was decided and when.
#### Step 3: Run the campaign
Once approved, the request is reserved against the fund's available budget. Partners can see exactly when proof of execution is due and when claims need to be submitted, so they're never surprised by a deadline. 
#### Step 4: Submit a claim with proof of execution
After running the campaign, partners file a claim against the approved request. From the request page in their portal, they click Submit claim and provide:
- Proof of execution: Screenshots, performance reports, attendee lists, post links, or any artifact that shows the campaign ran as planned.
- Actual spend amount: What the campaign actually cost, which may be lower than the approved amount.
#### Step 5: Attach invoices
Partners upload invoices directly to the claim, no email back-and-forth, no separate finance portal. Introw stores every invoice next to the original request, the approved budget, and any attached pipeline, so your team reviews everything in context.
Once your team approves the claim, Introw deducts the payout from the partner's available budget in real time and updates the dashboard. If your team requests changes or rejects the claim with a comment, the partner sees the update instantly and can respond in the same thread.
#### What partners see in their dashboard
At any moment, partners get full visibility from a single MDF dashboard:
- Budgets at a glance: Available, pending, and consumed funds.
- Approval and payout status: Real-time progress on every request and claim.
- Campaign history: Every active and past initiative in one place.
- Market Development Funds (MDF), overview
- Market Development Funds (MDF)
- How to set up a MDF fund
- How to show the ROI of a MDF
- Introw Product update - June 2026
- Everything Your Partners Can Do in Introw

---

## How to show the ROI of a MDF
Source: https://support.introw.io/en/articles/15308338-how-to-show-the-roi-of-a-mdf

MDF only earns its place in the budget when you can prove what it returned. Introw closes the loop between every dollar approved and the pipeline it influenced, so MDF stops being a cost center and starts driving measurable revenue. This article shows you how to configure ROI on your program and surface it everywhere it matters.
#### 1. Define what counts as ROI
In your MDF settings, choose which CRM object counts toward return. Introw can attribute ROI to deals, leads, or any custom object you already track in your CRM. Pick the one that best reflects the outcome your program is funded against.
#### 2. Choose how ROI is measured
Introw gives you three measurement models. Pick the one that matches how your finance and partner teams already talk about pipeline:
- Count of records: Every attached deal or lead counts as one unit of return. Best for early-stage programs where activity matters more than amount.
- Sum of a property: Roll up any numeric CRM property, deal amount, ARR, pipeline value, contract value, across every attached record. Best for closed-loop revenue reporting.
- Flat value per record: Assign a fixed monetary value to each attached record (e.g. every MDF-sourced deal or lead is worth $1,000). Best for standardizing reporting across partners and regions where deal sizes vary.
#### 3. Let partners attach deals and leads to MDF requests
Partners link the deals and leads their MDF campaign influenced through an embedded form in the partner portal. They can add individual records (deals, leads, contacts, companies) or bulk upload, whatever counts as ROI in your organization. 
Introw writes directly to your CRM and automatically links the records to the approved MDF request. No duplicate entry. No spreadsheets. No reconciliation. 
#### 4. Surface ROI everywhere it matters
Introw shows ROI in the places your team and partners already work:
- On every approved request: See the deals it influenced, the pipeline it generated, and the closed revenue it returned.
- On the linked deal: The MDF activity that touched a deal shows up directly inside that deal in the partner portal, so partners and your team are looking at the same number at the same time.
- In fund-level reporting: Aggregate ROI across every request tied to a fund, filtered by partner, region, or program.
#### 5. Bring ROI into your QBRs
Introw rolls MDF return into the business review reports you run with your partners, so the conversation moves from "did we spend it?" to "what did it return, and where do we double down?" Generate a QBR for any partner and the MDF section auto-fills with funds approved, dollars spent, deals attributed, and pipeline generated.
The result: one source of truth on MDF ROI, ready for your CFO, your QBR, and your next budget conversation.
- Market Development Funds (MDF), overview
- Tracking partner involvement on deals
- Market Development Funds (MDF)
- AI agents that actually take action for your partners
- How to set up a MDF fund
- How partners request MDF funds, submit claims, and upload invoices
- Introw Product update - June 2026

---

## Install Introw on your mobile home screen
Source: https://support.introw.io/en/articles/15324724-install-introw-on-your-mobile-home-screen

Introw is built mobile-friendly, so the partner portal works exactly the same on a phone as it does on a laptop, deals, tasks, assets, courses, all render in a touch-friendly layout.
To make access even faster, Introw can be installed directly onto a partner's mobile home screen as a Mobile friendly Web App. No app store, no download, just a one-tap shortcut that opens the portal in full-screen mode.

▶️ Watch the 30-second walkthrough 
#### On iPhone
- Open the partner portal in Safari.
- Tap the Share icon at the bottom of the screen.
- Select Add to Home Screen .
- Confirm the name and tap Add .
#### On Android
- Open the partner portal in Chrome.
- Tap the three-dot menu in the top-right corner.
- Select Add to Home screen (or Install app ).
- Tap Install to confirm.
💡 Tip: Once installed, Introw opens like a native app, partners stay logged in between sessions and get a faster, distraction-free experience.
- Embed your google calendar in Introw
- How to invite Partners to your portal via Introw
- Partner Connect: a 2-way CRM integration with HubSpot
- Introw mobile experience
- Using Introw with ChatGPT

---

## Introw mobile experience
Source: https://support.introw.io/en/articles/15324870-introw-mobile-experience

The partner portal works beautifully on mobile, because the best deals happen outside the office. Register opportunities, track progress, and get AI-powered coaching from your phone.
### Why Mobile Matters for Partners
Selling on the go means being where your customers are. With Introw on mobile, you don't miss pipeline updates, deal deadlines, or coaching feedback just because you're not at a desk. Your entire go-to-market activity syncs in real time.
### Registering Deals on Mobile
Get deals into the system in seconds, not minutes.
On the spot registration : See a selling opportunity? Register it immediately from anywhere. The mobile deal form captures what matters, deal name, value, company, and stage, without unnecessary friction. Submit, and your deal appears in the pipeline.
Pre-filled smart forms : Introw remembers your company, your account details, and your recent activity. Forms auto-populate so you're typing less and closing more.
Photo and attachment support : Attach contracts, screenshots, or customer emails directly from your phone. Evidence travels with your deal.
Instant confirmation : Get immediate feedback that your deal registered. No confusion about whether it went through.
### View Your Pipeline in Real Time
Your deals move fast. Your visibility should too.
Live pipeline snapshot : Open Introw and see your active opportunities at a glance. Filter by stage, opportunity size, or timing. Know exactly where things stand without scrolling through email.
Stage-by-stage breakdown : See how many deals are in proposal, negotiation, or closing. Spot bottlenecks. Know what needs attention.
Deal details on demand : Tap any deal to see the full picture, timeline, associated contacts, history, and next steps. Everything you need to move it forward.
Notifications that matter : Get alerts when deals move between stages, when feedback is ready, or when your manager adds comments. Stay in the loop without noise.
### Track Goals and Commission
Know where you stand. Always.
Live goal progress : See your quota, your pipeline coverage, and your progress toward targets. Updated continuously, not monthly.
Commission tracking : Understand how deals map to your commissions. See what's approved, pending, or in dispute. No surprises at payout time.
Historical view : Review past quarters. Understand patterns. Plan better.
Milestone notifications : Get reminded when you're close to hitting targets or when commission payouts are processed.
### AI-Powered Deal Support
Your mobile copilot is always available.
Pre-check intelligence : Before you submit a deal, Introw's AI reviews it. Missing required information? Need better qualification? Get guidance in seconds. Reduce back-and-forth with your manager.
Deal coaching in your pocket : Get specific suggestions on how to position deals, what questions to ask, or how to overcome common objections. Coaching that fits in your context, not a training module.
Messaging assistance : Unsure how to describe a deal to your buyer? Need help on a follow-up? Get suggested language and templates right in the app.
Real-time recommendations : As you move a deal through stages, get AI-generated next steps. What should you do tomorrow? Ask Introw.
### Agentic Deal Coaching
Go beyond suggestions. Get active support.
Automated deal analysis : Introw's AI agent continuously watches your pipeline. It spots risks, opportunities, and patterns you might miss, deals stalling too long, deals sized too small, deals lacking qualification signals.
Proactive alerts : You don't ask. The agent tells you. "Your Acme deal has been in proposal for 20 days, consider reaching out." Or: "Your Q4 pipeline is 30% short of target."
One-tap guidance : When an alert matters, get the full context. Why is Introw flagging this? What should you do? How can you fix it? All one tap away.
Learning loop : The agent learns how you sell. Over time, its coaching gets sharper and more relevant to your style and market.
- Opportunity registration with Introw and Salesforce
- AI Deal Coach
- AI deal coaching: an expert sales coach in every partner deal
- The Introw-Powered Partner: A Day in the Life
- Everything Your Partners Can Do in Introw

---

## Commissions in Introw: a complete walkthrough
Source: https://support.introw.io/en/articles/15350559-commissions-in-introw-a-complete-walkthrough

This article walks you through everything you need to know about the commission module in Introw, from setting up your first plan to processing payouts and the experience your partners get on the other side.
The commission plans section is where you define your commission structure. You can create as many plans as you need, for example, a revenue-sharing plan and a fixed-fee plan running side by side.
To help you get started quickly, Introw offers default templates for common structures, including:
- Fixed fee per qualified lead plan
- Revenue sharing plan
- Tiered annual commission plan
However, you are entirely free to build plans from scratch and make them as complex as your business requires.
💡 Need a hand? If you have a unique or highly complex commission structure that you aren't sure how to configure, please feel free to reach out to us at [email protected] . Both our team and our network of partners are standing by to help you set it up.
### Plan basics
- Name, give the plan a clear name so your partners understand what it entitles them to (e.g. RevShare ).
- Effective date, only deals after this date are eligible. For example, set May 20th and only deals closing on or after that date qualify.
- Data source, today plans are calculated on your CRM data. Stripe and Chargebee subscription/invoice data are coming soon, so commissions can be calculated directly on recurring revenue.
- Object & commission date, pick the object the commission is calculated on (typically the deal ) and the date field that defines eligibility (e.g. Close date ). When that deal is within that date range, the deal becomes eligible.
### Conditions
Conditions decide which deals are eligible. You can combine any property from your CRM and any Introw data (including partner attribution).
- Example: isClosedWon = true + deal type = New deal .
- You can layer on additional filters, e.g. contract duration > 365 days, to only reward longer commitments or deal amount > 10000 $ to reward higher deal values.
- You can also use partner attribution to pay more or less depending on who sourced the deal.
A live preview shows exactly which deals from your CRM match the rules. If a deal is missing or shouldn't be there, adjust the filters until the preview matches your intent.
### Rewards
Define how partners get paid:
- Fixed fee or percentage-based reward.
- Percentages can be applied to any amount property on the deal, amount , contract value, recurring revenue, etc.
- Frequency : one-time, monthly, quarterly, yearly, or for a lifetime even. 
- Tiered rewards : configure a different reward per partner tier or segment.
- Maximum reward : cap the eligible amount, e.g. include the first $10K, exclude anything above.
### Enrollment
Choose which partners (via segments ) are enrolled in the plan. A partner can be enrolled in multiple plans at the same time, for example, a revenue-share plan and a $100 fixed fee per closed-won deal, and both will be calculated on the same deals.
After you have created a commission plan and you open the commission module, you land on the commission overview. From here you get a clear view of:
- How much commission is still pending
- What is coming up in upcoming payouts
- What has already been paid out to your partners
💡 Introw tip: An explanation of each status can be found by clicking the ℹ️ icon in the upper right corner.
Payouts bundle eligible deals together so you can pay your partners in one go.
- Frequency : monthly, quarterly, yearly, or manual. Introw automatically creates the payout detail for you.
- Minimum payout amount : commission payouts below this threshold are rolled into the next payout, useful for avoiding tiny transactions (e.g. anything under $50).
In the payouts view you see an overview of all pending commissions , upcoming payments , and the total already paid .
### Reviewing a payout
Open a payout (e.g. April) and you'll see every eligible partner with their line items. For each partner you can:
- See each commission line item with a direct link back to the deal.
- Mark commissions as paid or unpaid as an admin, every change is tracked in the comments and activity.
- View the partner's uploaded invoice file when applicable.
### Draft commissions
Commissions that still need processing sit in draft and are not visible yet for the partner within their portal. From here you can:
- Add a PO number .
- Request the invoice, your partner is notified to upload their invoice so you can process the payment.
- Add a manual line item, for example an "extra effort fee" of $250 for a deal not captured in your CRM.
Once the partner has received their statement by email or when visiting the portal, they can upload the invoice (or include it as attachment by replying on the e-mail, so they don't need to go into the portal). From your side you can then mark the commission as paid , or push it to the next payment cycle .
Inside the partner portal, your partners get a dedicated Commission tab where they can see:
- Expected commission they're entitled to.
- Upcoming payments .
- Total amount paid to date.
Drilling into a paid payout shows every line item and links back to the originating deal, with the exact amount paid. Drilling into a specific deal shows partners the breakdown of what's already been paid, what's upcoming, and what's still pending approval but scheduled.
Clicking through to the details, a partner can see exactly why they're entitled to a commission, which plan it came from, the percentage or fixed fee, and the status of each line item (paid, upcoming, pending).
The commission module is fully flexible and CRM-driven. You have the freedom to design any reward structure, tiered, capped, fixed, percentage, or combined, and Introw handles eligibility, bundling, statements, partner notifications, and payout tracking end-to-end.
If you have any questions, reach out to us!
- Show commissions to your partners
- Introw's commission module
- The Introw API: connect your partner program to the rest of your stack
- Introw's Chargebee integration
- Introw's Stripe integration

---

## Build a partner directory powered by Introw
Source: https://support.introw.io/en/articles/15359478-build-a-partner-directory-powered-by-introw

Create a searchable partner directory that stays current without manual work. By building on top of Introw's partner data, your directory showcases the right partners to the right audience, with every update synced in real-time from your CRM.
### Why a partner directory matters
A partner directory gives your ecosystem visibility. It helps customers find the right partners, enables partners to discover collaboration opportunities, and creates a single trusted source for partner capabilities.
But only if the data stays accurate. Manual directories go stale. A directory powered by Introw doesn't.  By combining full partner profile management with automatic attribution , and tier changes and certifications updating on the fly, your directory maintains itself, ensuring your ecosystem data is always accurate, verified, and live.
### Keep your directory up to date automatically
Every partner manages their own profile within Introw. When they update their company information, select which products they support, or change their vertical or industry they are active in, that data syncs directly to your CRM. Your directory reflects those changes instantly with no admin work required. 
Partners stay in control of their listing. You stay in control of accuracy. With Introw’s approval flows, you can easily gate profile updates, giving you the power to review and approve changes before they ever go live on your directory.
### What partners can self-serve update
You decide exactly what CRM properties you want to show and what you want to allow partners to edit. Based on your custom configuration, partners can manage approved parts of their profile directly from the portal, like for example:
- Company Basics: Instantly update their website , billing or shipping address , logo, and team contact information.
- Verticals & Expertise: Tag the specific industries and verticals they target, ensuring they surface in relevant prospect searches.
- Product Offerings: Select which products they actively support from a dropdown that matches your CRM catalog, keeping your ecosystem aligned without messy free-text fields.
- Certifications, Tiers, & Status: Track completed training and active partner badges with certification data and status automated directly within Introw , while toggling whether they are actively accepting new business.
Every change syncs to Introw and CRM instantly and surfaces in your directory in real-time.
### Filter and segment your directory by what matters
Build a directory that targets the right audience. Show different partners based on:
- Partner tier: Display only Gold-tier partners to enterprise prospects, or show all tiers but sorted by level.
- Partner status: Include only active, certified partners; exclude pending or inactive accounts.
- Product interests: Let customers filter by the products partners actually support, pulled directly from partner profiles.
- Partner type: Segment by reseller, implementation partner, technology partner, or custom categories synced from your CRM.
- Geography and region: Filter partners by location or assigned territories.
- Verticals and industries: Allow customers to find specialized experts by filtering for partners with a proven track record in specific sectors like Healthcare, FinTech, or Retail.
All filtering logic is driven by real-time data synced seamlessly from Introw straight to your CRM, ensuring your directory always reflects the most up-to-date partner information. 
### Direct attribution from first interaction
Introduction requests submitted through your directory are powered by partner-specific Introw forms that are auto-generated for each partner. This means:
 Every lead is automatically attributed: Because each introduction request uses that partner's auto-generated Introw form, the lead is automatically associated with the correct partner in your CRM. No manual lookup or reassignment needed.
Your pipeline stays clean: Lead source is clear. Partner attribution is automatic. Reporting works without workarounds.
### Partners own their reputation
Because partners manage their own profile data within Introw, they stay invested in keeping it accurate. They see their listing in real-time. They control what's visible. And they know that being findable in your directory is part of staying competitive in your ecosystem.
This self-service model eliminates the bottleneck of admin-managed directories and shifts the incentive to keep data current.
- Partner Tiers
- Add your partners to Introw
- Introw CPQ
- The Introw-Powered Partner: A Day in the Life
- What is Partner Connect?

---

## Give your partners their own AI assistant to collaborate in real time via Introw's Partner MCP
Source: https://support.introw.io/en/articles/15374091-give-your-partners-their-own-ai-assistant-to-collaborate-in-real-time-via-introw-s-partner-mcp

You already use Claude to have a conversation with your partner program in Introw. Now Introw brings that same agentic experience to the other side of the relationship: your partners. 
Your partners can sign up on partners.introw.io and connect Introw's Partner MCP to their own AI assistant. From their first chat, they can register deals, check commission status, track their goals and collaborate with you in real time, without ever logging into a portal or waiting on an email.
Imagine your partners starting their day by simply asking:
- "Register a new deal for Acme Corp, €40k, expected to close end of Q3."
- "What's the status of my commissions this quarter?"
- "How am I tracking against my partner targets?"
- "Which of my registered deals need an update from me?"
- "What do I need to do to reach the next tier?"
Introw answers in full context against live data, and acts on their behalf, so collaboration happens at the speed of a conversation. This is what a modern, two-sided partnership actually looks like in practice.
💡 Built on the open standard. The Partner MCP uses MCP (Model Context Protocol), so it works with Claude and any other MCP-supported AI assistant (such as ChatGPT). Your partners connect the AI they already use, Introw does the rest.
Every deal a partner registers, every update they make and every commission question they answer themselves is one less email in your inbox and one more data point in your CRM, in real time. Introw turns your partners into active collaborators instead of passive participants, which means:
- Faster deal registration. Partners register and update deals from their own AI, so your pipeline stays current without manual chasing.
- Fewer status questions. Partners self-serve commission, goal and tier information instead of asking you.
- Cleaner data. Everything a partner does flows straight into Introw and your connected CRM, scoped to exactly what they're allowed to see.
The Partner MCP connects your partner's AI assistant securely to Introw using MCP (Model Context Protocol) , an open standard that lets AI models connect to the tools you already use.
When a partner connects their AI to Introw:
- They authenticate with their own Introw partner account.
- Every query and action is scoped to their partner permissions, the exact same access they have when they log into their Introw partner portal.
- No data bleeds across partners. Each partner only ever sees and acts on their own deals, commissions and goals. Their data stays theirs, and yours stays yours.
Introw becomes an always-on layer on top of the access your partner already has, never a workaround, never a shortcut.
Connecting takes less than a minute, and there's nothing for you to set up, the Partner MCP is ready the moment a partner has an Introw account.
Step 1 to Sign up on partners.introw.io Your partner creates or logs into their account at partners.introw.io .
Step 2 to Go to Integrations Claude and copy the Partner MCP URL Inside their partner login, they open the Claude / AI connector section and copy their  MCP connector URL.
Step 3 to Add the connector in their AI assistant The steps below use Claude as the example, but the same flow works for any MCP-supported assistant.
- In Claude: go to claude.ai/customize/connectors , click Add custom connector , paste the Partner MCP URL, then authorise with their Introw partner credentials.
- In another MCP-supported AI (such as ChatGPT): add a custom connector / MCP server in the assistant's settings and paste the same Partner MCP URL.
Step 4 to Start collaborating Open a new chat and try something like:
"Register a deal for TechVentures and add a note for my partner manager."
Introw pulls live data and responds in full context. From here, the possibilities are wide open.
🔧 Need technical details? Full MCP setup documentation, including supported clients and advanced configuration, can be found at https://claude.com/docs/connectors/custom/remote-mcp
These are just the starting points, the more context a partner gives, the more precise Introw's MCP response.
Register deals and share leads
"Register a new deal for Acme Corp worth €40k, closing end of Q3, and flag it for my partner manager to review."
Update and follow up on deals
"Update my shared deals with Acme with a close date in June and move the close date for 30 days and add  a comment that the prospects are busy with tons of events and roadshows that they have asked to postphone." 
Track commissions
"What's the status of my commissions this quarter, and which deals are still pending payout?"
Stay on top of goals and tiers
"How am I tracking against my targets this quarter, and what do I need to reach the next tier?"
Manage tasks and prep
"What open tasks do I have with this vendor, and what's due this week?" 
A partner's AI access mirrors their Introw access exactly, the same data, the same actions, the same boundaries. If they can see it or do it in their partner portal, their AI can too. If they can't, neither can their AI.
Each partner connects with their own credentials, and the MCP connection is tied to their individual account. One partner can never see another partner's data, and they only ever see the part of your program you've shared with them.
Does this work with AI assistants other than Claude? Yes. The Partner MCP is built on the open MCP standard, so it works with Claude and any other MCP-supported assistant, such as ChatGPT. Partners connect whichever AI they already use.
Do I need to set anything up for my partners? No. The Partner MCP is available to your partners as soon as they have an Introw account on partners.introw.io. There's nothing for you to configure.
Can one partner see another partner's data? Never. Each connection is scoped to the individual partner's account and permissions, exactly as in the partner portal.
Is partner data stored by the AI assistant? No. Data is fetched in real time when a partner asks a question and is never persisted between sessions by the AI provider.
- Install the Claude connector of Introw
- Connect Introw AI to Notion, Lovable, OpenClaw, and beyond
- Let Claude manage your partners, agentic partner updates via Introw
- Using Introw with Gemini via MCP
- What is Partner Connect?

---

## The Introw API: connect your partner program to the rest of your stack
Source: https://support.introw.io/en/articles/15386268-the-introw-api-connect-your-partner-program-to-the-rest-of-your-stack

Introw is where your partner program lives, partners, deals, and the commissions they earn. The Introw API lets that data flow automatically between Introw and the other tools you already run your business on, so nothing has to be re-keyed by hand and nobody has to check two systems to get one answer.
Below is what the API can do, the problems it solves, and a light look at how it fits together. When you're ready to build, your developers (or ours) can take it from there.
### Headless vision
Think of Introw as the source of truth for everything partner-related : who your partners are and what commission they've earned. The API opens two doors:
- Partners, read and manage your partner records programmatically, so the rest of your stack always reflects the latest partner data.
- Payouts, let your existing finance software handle approvals and payments, while status flows back into Introw so partner managers still see one clean view.
The result: Introw stays the commission system of record, your finance tools stay the payment system of record, and the API keeps them in line.
### Keep partner data in sync
The Partners endpoints let you create, read, update, and list partners without anyone touching the Introw UI. A few of the things this unlocks:
- Onboard partners automatically. When a new partner is approved in your CRM or signup flow, create them in Introw in the same moment, no double entry.
- Power an always-current partner directory. Pull your active partner list into a website, internal dashboard, or data warehouse, and let it refresh itself.
- Keep records clean. When a partner changes their company details or goes inactive, push the update once and have it reflected everywhere.
### Run commission payouts through your own finance system
Most teams already pay vendors and partners through an ERP or accounts-payable system like NetSuite or Xero. The Payouts endpoints let you keep that workflow instead of managing payouts in two places. Introw calculates the commissions and generates partner statements; your finance stack handles approval rules, invoice collection, and the actual payment, and the API syncs status back.
- Pull payouts ready for review. Your finance system can fetch the commissions Introw has calculated and feed them straight into your approval process.
- Reflect your real workflow. Mark payouts as approved, scheduled, paid, declined, or failed so Introw mirrors exactly what's happening in finance.
- Keep the paperwork together. Download the Introw-generated commission statement for your records, and upload or retrieve the partner's invoice, all attached to the right payout.
- Give partners a single source of truth. Because status flows back, partners and partner managers see accurate, up-to-date payout information in Introw without anyone sending a manual update.
### Use cases at a glance
- "New partner approved" → instantly in Introw. Connect your intake process so approved partners appear in Introw automatically.
- "Commission earned" → paid through our ERP. Let finance approve and pay in the system they already trust, with no copy-paste from Introw.
- "One view for partner managers." Payment status syncs back, so the partner team never has to ask finance "did this go out yet?"
- "Live partner directory." Surface your current partners on a webpage or internal tool that updates itself.
- "Clean books at close." Statements and invoices stay attached to each payout, ready for reconciliation and audit.
### Getting started
When you're ready to connect Introw to your stack, the full developer documentation including authentication, every endpoint, and copy-paste examples lives at developers.introw.io . Your team creates an API key in Introw under Settings > Developers > API keys , chooses the right permissions, and they're off. 
- Introw's commission module
- Commissions in Introw: a complete walkthrough
- Affiliate link management in Introw
- Introw's Chargebee integration
- Introw's Stripe integration