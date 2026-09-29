# Introw help center (support.introw.io), part 4 of 4

Verbatim text of every public help article, fetched 2026-09-29. Older than docs.introw.io; where they disagree, prefer docs.introw.io and the release notes.

## 🚀 Customer Deep Dive: How Quatt Powers Installer Operations with the Introw MCP
Source: https://support.introw.io/en/articles/15392105-customer-deep-dive-how-quatt-powers-installer-operations-with-the-introw-mcp

Quatt , a market leader in smart heat pumps, relies heavily on its Installer Channel (IC) to scale operations. To manage this complex ecosystem, Quatt deploys an AI assistant named "Wall-e" to orchestrate workflows across HubSpot, Introw, distributors, Snowflake, and Slack.
"We treat the MCP like a read replica of the database. Every single Installer Channel workflow opens with an MCP read. That’s how load-bearing it has been for us."
At the absolute center of this orchestration layer sits the Introw MCP .
Over a three-month production period, Quatt treated the Introw MCP as a load-bearing "read replica" of their ecosystem, pulling real-time, structured data to open and process every single installer order. 
### The Architecture: High-Volume Workflows
The Introw MCP serves as the starting gate for six core operational workflows at Quatt :
- Standard IC Deal Processing: The highest-volume engine, managing day-to-day installer orders.
- Deal Processing: Managing dedicated SKU mapping for specific enterprise partners.
- Bulk Multi-Unit Orders: Splitting massive multi-unit orders into $N$ separate, clean deals.
- Extra Materials Orders: Capturing secondary form notes (e.g., extra brackets, cables, or conduits) and mirroring them between the distributor and HubSpot.
- Just-in-Time Partner Onboarding: Automatically onboarding installers into the partner portal on the exact day of their training.
- Product & Pricing Refreshes: Running a comprehensive sync every 2.5 weeks to keep product references pristine.
### The MCP Toolkit: What Solves the Problem?
Quatt’s AI assistant heavily leverages a core suite of Introw MCP tools to automate complex cross-organizational reads without the need for manual scraping.
Tool Name
Operational Impact
search_crm_objects
The universal first step; initiates every single deal-processing run.
search_partner_engagement
The "secret weapon" that extracts full engagement feeds in a single call, cleanly identifying secondary equipment needs.
search_form_submissions
Handles clean, structured data intake for incoming orders.
search_partners
Instantly looks up partner tiers to gate pricing and handle company association on the fly.
share_lead_or_register_deal
Utilized for seamless bulk submissions and high-volume partner batches.
### Real-World Results & Production Impact
During the 3-month tracking window, the Introw MCP proved its scalability and reliability through several key milestones:
- Massive Bulk Automation: Successfully processed a 10-deal stock order batch for a major partner, all accepted and converted to HubSpot deals flawlessly.
- Granular Data Accuracy: Flawlessly synced a single, complex "Chill" add-on order containing 4 distinct line items without data loss.
- Instant Cross-Org Intelligence: Cross-referenced 434 Introw partner records against 147 external prospects , flagging 4 critical overlaps in a matter of seconds.
- Install the Claude connector of Introw
- Connect Introw AI to Notion, Lovable, OpenClaw, and beyond
- Give your partners their own AI assistant to collaborate in real time via Introw's Partner MCP
- Using Introw with Gemini via MCP
- What is Partner Connect?

---

## Introw's submission agent is now fully autonomous
Source: https://support.introw.io/en/articles/15392372-introw-s-submission-agent-is-now-fully-autonomous

Introw's AI just took a major step forward. The Form Submission Agent can now autonomously respond to submissions based on instructions you set as a human operator. Instead of routing every request to a person, the agent reads the submission, checks it against your internal policies and requirements, and takes the next step on its own. 
The result: dramatically fewer human escalations and manual interventions, so your partner teams can manage their inboxes on autopilot. 
This agent works alongside the Channel Conflict Agent, but goes far beyond it. Its job is to evaluate any submission, MDF requests, "become a partner" applications, deal registrations, customer projects, and more, against the rules you define. From there it can either suggest the next step to a human in the loop , or, when you're ready, execute that step autonomously .
You stay in control. You write the instructions; the agent follows them. You decide which submission types it handles on its own and which still need a human signoff.
Deal registration without the back-and-forth. Let the agent qualify each registered deal against your criteria, champion, contact, pain point, and budget signal. Complete deals get accepted and pushed straight into your CRM, while thin ones are sent back for the missing details. Your team only sees deals worth working, and partners get an instant answer instead of waiting on a manual review. 
Implementation kickoffs. Need a partner to provide details after closing a deal? Add a call-to-action in your form asking for implementation information. The agent can automatically approve or reject the submission and create an implementation ticket in your CRM, no manual handoff required. 
Partner applications on autopilot. Make sure potential partners explain why they want to work with you. The agent reviews each application, asks for more information when something is missing, and approves strong-fit partners autonomously. 
 MDF requests. When requests already align with your policy, let the agent auto-accept them so no one has to lift a finger. And any lead that comes out of an MDF campaign can be reviewed and accepted by the agent, so your sales team receives partner-qualified leads, ready to work. 
Every submission that the agent handles end-to-end is one less item in a human queue. Reviewing for policy compliance, requesting missing information, approving, rejecting, and creating downstream CRM records all happen automatically, consistently and around the clock. Your team's time shifts from processing forms to building partner relationships.
To enable autonomous handling, define the instructions and policies you want the agent to enforce for each submission type, then choose whether it should suggest the next step or execute it automatically. You can start with suggestions to build confidence, then switch specific flows to fully autonomous when you're ready. 
- Introw Agent
- Market Development Funds (MDF)
- Introw's AI Agent in Slack
- Introw Product update - May 2026
- Introw Product update - June 2026

---

## Affiliate link management in Introw
Source: https://support.introw.io/en/articles/15422218-affiliate-link-management-in-introw

Introw gives you everything you need to run an affiliate campaign end-to-end. You can generate unique tracking links for every partner at scale, hand them out automatically, and let Introw attribute every click and conversion back to the right partner, no spreadsheets, no manual link building, and no guesswork about who drove what.
This article walks you through how affiliate link management works in Introw, from setting up your campaign to the experience your partners get on the other side.
### How affiliate links work in Introw
An affiliate link is a unique, trackable URL tied to a single partner. When someone clicks that link, Introw records the visit, follows them through to a conversion, and credits the partner who sent them. Because every link is generated and tracked inside Introw, you always know which partner is driving traffic and which traffic turns into real outcomes. 
### Set up your affiliate campaign
An affiliate campaign defines where your partner links send people and what counts as a conversion. Introw uses the campaign as the template for every partner link it generates, so all your affiliates point to the same destination and are measured the same way.
To create one, fill in the following: 
Campaign name : A label for your own reference, e.g. "Q3 Affiliate Campaign."
Destination URL : The page the visitor lands on after clicking a partner link. This can be your homepage, a campaign landing page, or a signup flow.
Conversion commission (optional) : A flat amount credited to the attributed partner on every conversion. Leave empty to disable.
Attribution window : How many days after a click a conversion still counts toward the partner.
Attribution model: Which click gets credit when a visitor clicks multiple affiliate links before converting. 
 Introw generates a unique link for each partner pointing to this campaign. Share those links with your partners, and conversions are tracked and attributed automatically. 
### Generate unique links for partners at scale
Rather than building links one by one, Introw generates a unique tracking link for each partner automatically. Whether you have ten partners or several thousand, every partner gets their own link tied to their record, no manual copying, no risk of duplicate or mismatched links. 
- One link per partner, each affiliate link is uniquely associated with a single partner, so attribution is unambiguous.
- Generated in bulk, Introw creates links across your whole partner base at once, and new partners get a link automatically as they're added.
- Always in sync, because links are tied to partner records, they stay connected to the right partner as your campaign grows.
#### Manage aliases without breaking attribution
A random string of characters doesn't inspire clicks. Partners can create readable aliases for their referral link like their company name, a campaign tag, a channel-specific variant and every alias resolves to the same partner record. One partner, multiple links, one attribution trail. 
- Branded, human-readable links : replace the generated key with something recognizable (e.g. acme.introw.io/r/northwind instead of acme.introw.io/r/zPpScHyL ). Familiar links build trust and convert better. 
- Multiple aliases per partner : partners can run separate aliases per channel, northwind-blog for their website, northwind-newsletter for their email list, to see which channel performs, while everything rolls up to the same partner. 
- Attribution stays intact : aliases are pointers, not new links. Whichever alias a buyer clicks, the conversion is attributed to the right partner record in your CRM. Renaming or adding an alias never orphans past or in-flight referrals.
### The partner experience
Each partner finds their personal affiliate link inside their partner portal, ready to copy and share across their website, email, social posts, or campaigns. Because the link lives in the portal, partners always have access to the correct, up-to-date URL without you having to send it to them. 
Alongside their link, partners can see how their link is performing, giving them a clear, motivating view of the traffic and results they're driving.
### Track clicks and conversions automatically
Once links are live, Introw tracks performance for you. Every click is recorded against the partner who owns the link, and when a visitor completes the conversion you defined, Introw attributes it back to that same partner automatically.
- Clicks : see how much traffic each partner is generating.
- Conversions : see which clicks turn into the outcomes that matter to you.
- Per-partner attribution : every result is tied to the partner who drove it, so you can compare performance across all of your affiliates.
Because attribution happens automatically, you always have an accurate, real-time picture of which partners are delivering, without manual tracking or reconciliation.
### Connect affiliate performance to the rest of Introw
Affiliate tracking doesn't live in isolation. Because Introw attributes clicks and conversions back to each partner record, you can automatically build on that data across the rest of Introw for example, rewarding affiliate-driven conversions through your commission plans and surfacing affiliate performance in your reporting.
### How Introw prevents affiliate fraud
Affiliate programs are a magnet for fraud. Bad actors fake clicks to manufacture conversions, exploit programs that pay out before anything is verified (which can be the costliest one in B2B claim commission) on deals that were already in your pipeline. Left unchecked, your program quietly turns into a payout liability. Introw is built to stop this.
- Fake clicks go nowhere: Every click is registered server-side with a cryptographically signed, single-use token. Fabricated or replayed events don't pay out, each token backs one conversion, period.
- Money never moves before it's verified: Commissions flow through a held → payable → reversed lifecycle, so suspicious or high-volume activity stacks up for review instead of landing in a payout run. Volume-based abuse becomes a queue, not a loss.
- Credit only for net-new business: Every referral is matched against your existing customers and open deals (ignoring generic email domains), so partners can't get paid for revenue that was already in flight.
The result: partners are rewarded for real influence, and your program scales without becoming a payout liability.
- Link your HubSpot deals to Introw via custom properties
- Introw Product update - June 2026
- How to setup your affiliate link tracking
- Everything Your Partners Can Do in Introw
- How Introw Solves TCMA for Vendors

---

## Introw Product update - June 2026
Source: https://support.introw.io/en/articles/15430997-introw-product-update-june-2026

The best partner programs grow on two fronts at once, bringing in new pipeline and rewarding the partners who drive it, without piling more manual work on your team.
### 📣 Market Development Funds
MDF programs usually live in spreadsheets and inboxes, which is exactly why so many of them quietly become a cost center no one can measure. Now they live in Introw, end to end.
Partners request funds from their portal, your team approves and tracks spend against fixed or pooled budgets, and partners file claims with proof of spend that you review in context, invoices, approvals, and a full audit trail all in one place. Run programs across regions with multi-currency support, chain multiple approvers for sequential sign-off, and let the built-in AI agent pre-screen each request against your rules, partner tier, and remaining budget so your team only weighs in where it matters. 
Most importantly, every dollar is attributed back to the deals it influenced in your CRM. Partners attach deals and leads to their approved requests, and the return is calculated in real time, so MDF stops being a cost center and starts proving real ROI you can take to your next QBR. Learn more
### 🤖 Your AI agent is now fully autonomous
The Form Submission Agent has gone from assistant to autopilot. Instead of routing every request to a person, it now reviews partner submissions and takes the next step on its own, following the instructions you set as a human operator.
It reads each submission, checks it against your policies, and acts: qualifying deal registrations against your criteria and pushing complete ones straight to your CRM, sending thin ones back for the missing details, screening "become a partner" applications, auto-accepting MDF requests that already fit policy, and creating implementation tickets without a manual handoff. Your team only sees the work worth their time, and partners get an instant answer instead of waiting on a manual review.
You stay in control of every decision. Start with the agent suggesting next steps to build confidence, then flip specific submission types to fully autonomous when you're ready. Every submission it handles end-to-end is one less item in a human queue, so your team's time shifts from processing forms to building partner relationships. Learn more
### 🔗 Affiliate link management
You can run a full affiliate campaign in Introw, without spreadsheets or manual link building. Define your campaign once, the destination and the conversion you want to measure, and Introw generates a unique tracking link for every partner automatically, whether you have ten affiliates or several thousand. 
Partners grab their personal link straight from the portal and share it anywhere, while Introw records every click and attributes each conversion back to the partner who drove it. And because that attribution lives on the partner record, you can reward affiliate-driven conversions through your commission plans and surface the results in your reporting. Learn more
### Additional improvements
##### A refreshed commission module
The commission module got a cleaner look and feel and more automation under the hood, with much bigger commission automation landing soon. Learn more
##### Give your partners their own AI assistant
Your partners can now sign up at partners.introw.io and connect Introw's Partner MCP to their own AI assistant (Claude, ChatGPT, or any MCP-supported tool) to register deals, track commissions, and collaborate in real time. Learn more
- Market Development Funds (MDF)
- Introw Product update - May 2026
- Introw's submission agent is now fully autonomous
- Everything Your Partners Can Do in Introw
- Introw Product Update - July 2026

---

## How to setup your affiliate link tracking
Source: https://support.introw.io/en/articles/15443507-how-to-setup-your-affiliate-link-tracking

Introw affiliate tracking is quick to set up and flexible. You add a single lightweight script to your site, and from there Introw automatically detects visitors arriving through a partner link and registers the referral. When a visitor converts, you report it whichever way fits your setup: client-side with one function call, server-to-server from your backend, or easiest of all and automatically through your existing HubSpot forms , with nothing extra to wire up.
Because Introw stores attribution server-side rather than in a client-written browser cookie, tracking stays resilient to browser tracking restrictions and clean for GDPR purposes.
### Install the tracking script
Add the following snippet to the <head> of every page on your site.
<!-- Introw affiliate tracking --> <script async src="https://app.introw.io/affiliate.js" data-publishable-key="pk_aff_org_y2ckxrlGTguABYgRhEIv8tIvRdPSOLiI" ></script> <!-- End Introw affiliate tracking -->
On page load, the script reads the ref parameter from the URL (for example https://yoursite.com/?ref=zPpScHyL ), calls Introw to register the referral, and stores the attribution server-side. No further action is needed for referral detection.
💡 Introw : Once the snippet is correctly installed, a green Installed status indicator will appear
### Track conversions
When a visitor completes the action you want to credit, Introw records it in one of three ways: client-side, server-to-server, or automatically when you use HubSpot forms. Choose the method that matches where your conversion event fires. 
#### Option A, Client-side tracking
Recommended when conversions happen on your website. Execute this when a visitor converts (for example, after signup):
window.introw.affiliate.track({   email: customer.email,   properties: {     "ikfexbkmwac5nko9lpk70ke8": "email"   }, });
Advanced: scope a call to this campaign (rarely needed) Pass the campaign key as publishable Key to guard the call to this campaign: if the visitor's click belongs to another campaign, the conversion is ignored. The click cookie always decides attribution.
#### Option B, Server-to-server API
Best when the conversion is confirmed on your backend (for example, a closed deal or a verified payment). Send a POST request to Introw's conversion endpoint using your Introw API key scoped to affiliate:write .
Use the email (or another identifier you also pass at referral time) so Introw can match the conversion to the stored referral.
curl -X POST https://api.introw.io/api/v1/affiliate/conversions \ -H "x-api-key: $INTROW_API_KEY" \ -H "Content-Type: application/json" \ -d '{ "clickId": "<value of the _introw_aff cookie>", "email": " [email protected] ", "properties": { "ikfexbkmwac5nko9lpk70ke8": "email" } }'
#### Option C, Automatic tracking with HubSpot forms
Best when you already capture conversions through HubSpot forms. If your site uses HubSpot forms, Introw detects form submissions automatically and attributes them to the originating partner, no tracking call or API request required and the same snippet handles both classic and v4 HubSpot forms. 
Make sure the tracking script above is installed so the referral is registered, and that the form captures the visitor's email (or another identifier used at referral time) so Introw can match the submission to the stored referral.
### Attribution settings
The attribution window and attribution model are defined on the affiliate campaign, not in the install:
- Attribution window : how many days after a click a conversion still counts toward the partner.
- Attribution model : which partner gets credit when a visitor clicks multiple affiliate links before converting (first click or last click).
### How Introw prevents affiliate fraud
Affiliate programs are a magnet for fraud. Bad actors fake clicks to manufacture conversions, exploit programs that pay out before anything is verified (which can be the costliest one in B2B claim commission) on deals that were already in your pipeline. Left unchecked, your program quietly turns into a payout liability. Introw is built to stop this.
- Fake clicks go nowhere: Every click is registered server-side with a cryptographically signed, single-use token. Fabricated or replayed events don't pay out, each token backs one conversion, period.
- Money never moves before it's verified: Commissions flow through a held → payable → reversed lifecycle, so suspicious or high-volume activity stacks up for review instead of landing in a payout run. Volume-based abuse becomes a queue, not a loss.
- Credit only for net-new business: Every referral is matched against your existing customers and open deals (ignoring generic email domains), so partners can't get paid for revenue that was already in flight.
The result: partners are rewarded for real influence, and your program scales without becoming a payout liability.
### Verifying your setup
To confirm tracking works end to end: visit your site using a test partner link with a ref parameter, complete a conversion, and check that the event appears against the correct partner in Introw. If referrals register but conversions don't attribute, confirm the identifier you send at conversion (such as email) matches the one captured at referral.
- Partner Engagement Tracking
- Partner activity events in your HubSpot timeline
- How to use Introw forms with HubSpot
- Link an existing HubSpot deal to your vendor
- Affiliate link management in Introw

---

## Build a mutual action plan with Tasks
Source: https://support.introw.io/en/articles/15458290-build-a-mutual-action-plan-with-tasks

A mutual action plan (MAP) or joint business plan (JBP) keeps you and your partner aligned on what needs to happen, who owns it, and by when. With Introw Tasks and Journeys you can build exactly that inside the partner portal: a shared, structured plan that runs from onboarding through every recurring milestone, visible to the right people and tracked automatically.
This article walks you through the full setup. Watch the video below for a complete walkthrough, then use the sections underneath as a reference.
### Add a Tasks section to your partner portal
Your joint business plan lives in a Tasks section inside the partner portal. To add it, open your partner portal experience, click Add section , and select the rich section named Tasks .
This is a smart section : Introw dynamically fills it with the tasks linked to whichever partner the portal experience is assigned to. Each partner sees their own plan, and both you and your partner can update tasks or create new ones directly from the portal.
When you add the section you can choose which tasks to show :
- A predefined set of tasks from a journey (like a set or template of tasks), for example a complete partner onboarding flow that is identical for every partner.
- Ad-hoc or standalone tasks created on the fly during the partnership, such as the follow-up items that come out of a QBR or joint business plan.
You can display both task types together in a single section so partners see one unified plan, or organize them into distinct sections of the experience, placing marketing tasks under the Marketing page and commercial or sales tasks in their respective areas.
Tip: to keep the experience clean, you can automatically hide completed tasks after a set number of days . Finished items stay visible long enough to confirm they are done, then drop off so the partner only sees what still needs attention.
### Predefined plans with journeys
A journey is a predefined set of tasks you build once and apply to one or many partners. Journeys are ideal for the repeatable parts of a partnership that are the same for every partner or partner type, like for example most commonly partner onboarding .
A typical onboarding journey might include:
- Agreeing on the terms & conditions
- Watching a tutorial video on how to use the portal
- Registering their first deal
- Scheduling a QBR
Once the journey is assigned, Introw rolls out the same structured experience to every partner automatically, so nobody falls through the cracks and onboarding stays consistent at scale.
### Ad-hoc and standalone tasks
Not everything in a partnership is predefined. Standalone tasks are ad-hoc items created outside a journey, perfect for one-off actions that come up while you work together, for example the follow-ups agreed during a QBR , a specific document you need from the partner, or a unique request.
With standalone tasks you can:
- Create and manage tasks independently from journeys
- Handle unexpected or unique partner requests as they arise
- View them alongside journey-based tasks in the same plan
- Filter by assignee so everyone focuses on what is relevant to them
### Let partners create and assign tasks too
A joint business plan is a two-way commitment. Introw lets your partner create their own tasks inside the portal and assign them to your team members . This turns the plan into a genuinely shared workspace, if a partner needs something from you, they can capture it as a task and route it to the right person, rather than chasing it over email.
### The task detail: powerful options
Beyond a name and description , every task carries a few powerful options that make your plan precise and automated.
##### Relative due dates
Instead of a fixed calendar date, you can set a relative due date, a number of days after the task is assigned to the partner.
- Use case: the "Sign T&Cs" task should be due 3 days after assignment. If you assign it on 10 January, the due date is automatically set to 13 January, and the partner is nudged to complete it as the deadline approaches.
Relative dates are what make journeys work at scale: the same plan adapts to each partner's own start date.
##### Assignee, internal or partner-facing
Each task can be owned by your side or the partner's side, and partner-facing tasks can target the right people automatically based on the partner persona (role or segment) :
- Internal team, the task belongs to your team members.
- All partner contacts, visible to every contact at the partner organisation.
- Specific role, choose a role as a dynamic assignee , and only the partner contacts with that role are assigned. For example, a "Complete tax form" task can automatically land with the partner's finance contact, while a "Watch the sales enablement video" task goes to their sales reps.
##### Visibility
Visibility controls who can see a task, which matters in a shared plan where some items are for the partnership team only:
- Public, visible to the relevant external contacts and your internal team.
- Internal, visible only to your team. Use this for tasks that are key to managing the partnership but that the partner should not see.
- Assignee only, on the partner side, only the assigned contact sees the task. As an Introw user you still see these tasks and can follow up on progress.
Choosing the right visibility keeps sensitive information with the right audience while keeping everyone who needs to be informed in the loop.
### Running the partner journey at scale
The real power of journeys is consistency across your whole partner base. Build a journey once, agree on T&Cs, watch a portal tutorial, register a first deal, schedule a QBR, and Introw delivers that same structured experience to every partner , with relative due dates adapting to each partner's start.
You can then track completion across all partners from the Tasks overview, so you instantly see who is on track, who needs a nudge, and where onboarding is stalling, without managing each plan by hand.
To go deeper on any part of this, see Partner journeys .
- Introw tasks
- Embed tasks within your partner experience
- Introw Agent
- Introw workflow actions in HubSpot
- Task actions

---

## Partner team roles
Source: https://support.introw.io/en/articles/15517779-partner-team-roles

Introw now lets your partner team include multiple people with multiple roles on a single partner account. Instead of assigning just one partner manager, you can reflect the full team that actually supports a partnership, sales, marketing, support, and more, and put each role to work across the partner experience.
### Build a partner team with multiple roles
A partner account is rarely owned by one person. Introw lets you add several teammates to the same account and give each one a role, so responsibilities are clear on both sides of the partnership.
A few common setups:
- Two partner managers sharing a large, strategic partner account.
- A partner marketing manager and a partner support manager on the same account, each covering their own area.
- Any other combination of roles that matches how your team works.
These roles can also be synced from user-based dropdown fields in your CRM, such as deal owner, account owner, or ticket owner. Introw maps each field to the matching role, so the right people are assigned to every partner account automatically and stay in sync as ownership changes in your CRM.
### Use roles as dynamic options across the experience
Once roles are assigned, Introw turns them into dynamic options you can reuse throughout the partner portal. You set them up once at the experience level, and Introw automatically fills in the right person for each partner account. 
### Experience variables
Reference a role anywhere in your experience and Introw resolves it to the right person for that partner, for example, "Hi, this is {support manager}, here to help you with support." Each partner sees the teammate who actually holds that role on their account.
### Deal owners on form submissions
Assign form submissions to a role rather than a fixed person. When a partner submits a form, say, raising a support ticket, Introw routes it to the right role, like the partner support manager, so it always lands with the teammate responsible for that account.
### Team section in the partner experience
Show the full team behind a partnership in a dedicated team section. Partners can see everyone responsible for their account and exactly who to reach for what, making your team and points of contact clear from day one 
### Dynamic author on announcements
Publish announcements under a dynamic role so the right person is credited as the author. Commercial news can come from the partner manager, while more technical or support-related updates come from the relevant support or technical role. 
### Dynamic issuer on certificates
Issue certificates from a dynamic role so each certificate is signed by the right owner. A technical support manager can grant technical certifications, while a partner business development manager issues sales training certificates.
Introw tip: Because roles are configured at the experience level, you only set them up once. Every partner portal linked to that experience automatically shows the correct people for each role.
- Best practices for a good partner experience
- How to personalize your partner portal?
- Roles and permissions
- Managing partner contacts
- Partner certificates

---

## Introw's Chargebee integration
Source: https://support.introw.io/en/articles/15551911-introw-s-chargebee-integration

Connect Introw with Chargebee to calculate partner commissions on your actual revenue, the invoices and subscriptions your customers genuinely pay for through your partners. Instead of estimating payouts on closed deals, Introw reads your live billing data and rewards partners on real, recognised revenue. The result: commissions you can trust, and partners who can see exactly where every cent comes from 🚀.
Paying commissions on deal data tells you what should happen. Paying on Chargebee billing data tells you what actually happened. That difference matters for both you and your partners:
- Reward real revenue. Commissions are based on invoices that have genuinely been paid, so you never pay out on revenue that churned, was discounted, or never landed.
- Real-time and recurring. Because Introw pulls directly from Chargebee, every new paid invoice and renewal flows into the commission calculation automatically, perfect for subscription and usage-based models.
- Full transparency for partners. Each commission line item traces back to the exact Chargebee invoice it came from, so partners can see precisely why they're being paid, no spreadsheets, no black box.
💡 Introw tip: You can run Chargebee-based plans alongside your CRM-based plans. A partner can earn a one-off fee on a closed-won deal and a recurring share of the paid invoices that follow, both calculated automatically.
### 1. Connect Chargebee
Go to Integrations > Chargebee and connect your account by entering your Chargebee API key . Once connected, Introw can read your billing data, invoices, subscriptions, and their properties. 
### 2. Link Chargebee objects to your partners
Next, choose which objects you want to link to your partners. In most cases this is your invoices . To attribute an invoice to a partner, Introw uses a field on the invoice in your Chargebee account.
- In the example, a custom field called Introw Partner is added in Chargebee as a drop-down to select the partner.
- This can be any value, a partner name or an ID, as long as the mapping between Chargebee and Introw is set up. Once mapped, Introw tracks the attribution automatically.
💡 Note: Attribution lives on the Chargebee record, so the way you already tag partner-sourced revenue in your billing system carries straight through to Introw.
### 3. Build a commission plan on Chargebee data
When creating a commission plan, set the data source to Chargebee . Introw then pulls the relevant data directly from your account instead of your CRM. From there you define:
- Object & commission date, choose the object the plan is calculated on (e.g. invoices ) and the date that drives eligibility, such as the date an invoice was paid .
- Conditions, decide exactly which invoices qualify. For example, only invoices with a status of paid and a total > $25 . You can layer on as many conditions as you like using any Chargebee property.
- Rewards, define what the partner earns, for instance 5% of the total billed amount on each qualifying invoice.
A live preview shows the potential payouts based on your rules, so you can confirm the right invoices are being captured before anything goes live.
### 4. Review payouts and line items
When you open a payout, Introw shows every commission line item for that partner. With a Chargebee invoice plan, each line item is one of the subscriptions or invoices your customers paid for and that is attributed to that partner, for example, 5% on the total billed amount of each Chargebee invoice. 
### 5. The partner experience
Inside the partner portal, partners get a full overview of their commissions: what's pending, what's upcoming, and what has already been paid. For commissions powered by Chargebee, they can see that the payout comes from the actual invoices their customers paid, giving them complete confidence in the numbers. 
Full transparency towards your partners! They can trace every commission back to real, paid revenue, which builds trust and keeps the focus on driving more of it.
### Recap
With the Chargebee integration, Introw calculates commissions on the revenue your partners actually generate, paid invoices and recurring subscriptions, in real time. You connect Chargebee with an API key, link invoices to partners, build a plan on your billing data with the conditions and rewards you choose, and Introw handles eligibility, payouts, and a transparent partner-facing breakdown end-to-end.
- Introw's commission module
- Commissions in Introw: a complete walkthrough
- The Introw API: connect your partner program to the rest of your stack
- Introw's Stripe integration
- Introw Product Update - July 2026

---

## Segments in Introw
Source: https://support.introw.io/en/articles/15586173-segments-in-introw

Segments let you group partners and partner contacts so you can target, organise, and control access to them across the whole platform. You can build segments based on partners (companies) or on partner contacts (individual people) for example a Gold partners segment of your top-tier partner companies, or a Partner Sales reps segment of every contact whose role is sales rep. 
You can find all segments under Settings > Segments . From here you can see each segment's name, type, the number of members it currently contains, and whether it overrides your organisation defaults, and create a new segment. The first row, All partners · Default , is pinned: it holds the baseline permissions and notifications that apply to everyone.
Each segment opens on four tabs, General , Audience , Permissions , and Notifications, covered in order below.
Every segment starts with a Name and an optional Description . The name is how the segment appears everywhere it's used across the platform, so pick something clear and recognisable (e.g. Gold partners or Partner Sales reps ). Use the description to explain what the segment is for and who belongs in it, which is helpful when your team grows. 
The Audience defines who belongs to the segment. Segments can be dynamic or static :
- Dynamic enrollment, members are determined automatically based on conditions you set. As partners or contacts change, they're added to or removed from the segment automatically, so the segment always stays up to date.
- Static list, you hand-pick the exact partners or contacts that belong to the segment. Membership only changes when you edit the list yourself.
For dynamic segments, Introw offers extensive condition filtering based on both your CRM data and Introw data . You can combine conditions to target precisely the audience you want, for example all Introw certified partners , or all partner contacts where employment role = Sales rep .
The next two tabs work differently from General and Audience. Partner permissions and email notifications start from one organisation-wide default , and a segment changes that default only when you deliberately turn on an override. Every setting resolves in three steps:
- All partners · Default, applies to everyone, always. It's the pinned first row in the Segments table, and its General tab shows how many segments override each setting.
- Segment overrides, apply only to segments where you switched the override on, and to their members.
- Contact opt-outs, let individual contacts silence notifications, nothing else.
Three rules are worth knowing before you configure anything:
- Segments can restrict, not just grant. An override can turn capabilities off for its members as well as on, so you can hold a group back from something the default leaves open.
- Within segments, the most permissive setting wins. If a contact matches two override segments with conflicting rules, the more permissive one applies, a segment can't hold a group back from what another segment grants.
- Contacts can only opt out. When policy leaves an event on, a contact can disable their own copy. When policy turns it off, the toggle is locked and they can't switch it back on.
One restriction to keep in mind: a dynamic segment with zero conditions can't have overrides enabled, it would target everyone, which is what the default is for. Introw blocks it with: "An override segment must target a subset. Add at least one condition." Static lists are exempt.
Permissions control what partners and contacts are allowed to do in their partner portal. Set the baseline on All partners · Default , then open a segment's Permissions tab and switch on Override the default for this segment to change it for that group. Leave the switch off and you see the org defaults read-only. Any setting that diverges from the default gets an Override badge.
Invite colleagues Whether contacts can add coworkers to the portal. The preview shows the partner-side Your team panel. Restrict this if you only want certain partners to grow their portal access.
See all shared records Whether contacts see all records shared with their company, or only the ones they're assigned to. The preview shows how notifications follow access, partners never get notified about records they can't reach.
Notifications work the same way: a baseline on All partners · Default , changed per segment via Override the default for this segment . Each event has a single Recipients value:
- All partners, sends to every applicable partner.
- Collaborating only, sends only to assigned collaborators, for CRM-record events.
- Disabled, switches the event off.
💡 Introw Tip: Slack and Teams notifications are configured on the integration itself, under Settings > Integrations > Communication tool> Partner channels , not per segment.
Open a partner contact and go to their Notifications tab. A card walks through all three layers, and each event row is badged with the layer that decided it, for example "All partners · default settings" or "Disabled · segment Tier 1" . Locked rows mean policy owns the setting and the contact can't change it. The contact's Permissions tab shows a resolved yes/no per permission and names the segment or default that granted it.
Because segments are used across the whole platform, configuring audience, permissions, and notifications once lets you consistently target and govern the same group of partners or contacts everywhere in Introw.
- Introw CPQ
- Segment use cases
- Introw Product update - May 2026
- Build a partner directory powered by Introw
- Using Introw with ChatGPT

---

## Introw's Stripe integration
Source: https://support.introw.io/en/articles/15588760-introw-s-stripe-integration

Connect Introw with Stripe to calculate partner commissions on your actual revenue, the invoices and subscriptions your customers genuinely pay for through your partners. Instead of estimating payouts on closed deals, Introw reads your live Stripe data and rewards partners on real, recognised revenue. The result: commissions you can trust, and partners who can see exactly where every cent comes from 🚀.
A closed-won deal captures the contract, but usage-based and subscription pricing means the real number keeps changing, expansions, upgrades, downgrades, churn. That ongoing billing detail lives in Stripe. Pull it in and partners get paid on actual subscription revenue, not the figure that was true on signing day
- Reward real revenue. Commissions are based on invoices that have genuinely been paid, so you never pay out on revenue that churned, was discounted, or never landed.
- Real-time and recurring. Because Introw pulls directly from Stripe, every new paid invoice and renewal flows into the commission calculation automatically, perfect for subscription and usage-based models.
- Full transparency for partners. Each commission line item traces back to the exact Stripe invoice it came from, so partners can see precisely why they're being paid, no spreadsheets, no black box.
💡 Introw tip: You can run Stripe-based plans alongside your CRM-based plans. A partner can earn a one-off fee on a closed-won deal and a recurring share of the paid invoices that follow, both calculated automatically.
### Connect Stripe
Go to Integrations > Stripe and connect your account by entering your Stripe API key . Once connected, Introw can read your billing data, invoices, subscriptions, and their properties. You can use Stripe's Test Mode to try it out.
### Link Stripe objects to your partners
Next, choose which objects you want to link to your partners. In most cases this is your invoices . To attribute an invoice to a partner, Introw uses a field on the invoice in your Stripe account. 
- In Stripe this is typically a customfield, for example a key called introw_partner that holds the partner.
- This can be any value like a partner name or an ID as long as the mapping between Stripe and Introw is set up. Once mapped, Introw tracks the attribution automatically.
💡 Note: Attribution lives on the Stripe record, so the way you already tag partner-sourced revenue in your billing system carries straight through to Introw.
### Build a commission plan on Stripe data
When creating a commission plan, set the data source to Stripe . Introw then pulls the relevant data directly from your account instead of your CRM. 
From there you define:
- Object & commission date, choose the object the plan is calculated on (e.g. invoices ) and the date that drives eligibility, such as the date an invoice was paid .
- Conditions, decide exactly which invoices qualify. For example, only invoices with a status of paid and a total > $25 . You can layer on as many conditions as you like using any Stripe property.
- Rewards, define what the partner earns, for instance 5% of the total billed amount on each qualifying invoice. 
A live preview shows the potential payouts based on your rules, so you can confirm the right invoices are being captured before anything goes live.
### Review payouts and line items
When you create a payout, Introw shows every commission line item for that partner. With a Stripe invoice connection, each line item is one of the subscriptions or invoices your customers paid for and that is attributed to that partner, for example, 5% on the total billed amount of each Stripe invoice. Because plans can be CRM- or Stripe-driven, a single payout can combine commissions coming from deals and from Stripe subscriptions in one place.
### The partner experience
Inside the partner portal, partners get a full overview of their commissions: what's pending, what's upcoming, and what has already been paid. For commissions powered by Stripe, they can see that the payout comes from the actual invoices their customers paid, giving them complete confidence in the numbers.
That transparency is the whole point: partners don't have to take your word for it. They can trace every commission back to real, paid revenue, which builds trust and keeps the focus on driving more of it.
### Recap
With the Stripe integration, Introw calculates commissions on the revenue your partners actually generate, paid invoices and recurring subscriptions, in real time. You connect Stripe with an API key, link your subscriptions, customer, invoices  or other Stripe objects to partners, build a plan on your billing data with the conditions and rewards you choose, and Introw handles eligibility, payouts, and a transparent partner-facing breakdown end-to-end.
- Introw's commission module
- Commissions in Introw: a complete walkthrough
- The Introw API: connect your partner program to the rest of your stack
- Introw's Chargebee integration
- Introw Product Update - July 2026

---

## Using Introw with Gemini via MCP
Source: https://support.introw.io/en/articles/15590009-using-introw-with-gemini-via-mcp

Connect Introw to Gemini so you can search partner data, pull together account research, manage deals and tasks, and take action in Introw, all without leaving Gemini.
Once the connection is live, your team can use Gemini to work with live Introw data in natural language. For example:
- "Which of my partners have pending deal registrations this week?"
- "Show me the commission status for our Gold tier partners."
- "Pull everything Introw has on Amazon into one summary."
- "Which partners haven't been active in the last 30 days?"
- "Create a follow-up task for my top partners this quarter."
- "Generate a QBR for our largest partner."
Gemini reasons across your live partner data, surfaces insights instantly, and helps you act, all enforcing the exact same permissions you already have in Introw.
💡 Personalised by design. Thanks to Introw's MCP, Gemini only ever sees the data you're authorised to see in Introw, your permissions, enforced automatically. Nothing more, nothing less.
The integration uses MCP (Model Context Protocol) , an open standard that lets AI models like Gemini connect securely to the tools you already use.
When you connect Gemini to Introw:
- Gemini authenticates on your behalf using your Introw credentials.
- Every query is scoped to your user permissions, the exact same access rules that apply when you log into Introw directly.
- No data bleeds across users. A partner manager sees their partners and deals. An admin sees what an admin sees. Your data stays yours, always.
Gemini becomes a smart, always-on layer on top of your existing Introw access, not a workaround, not a shortcut, but a genuinely better way to stay on top of your partner ecosystem.
### Overview
Setup is split between workspace administrators , who register Introw as a data store one time, and end users , who authenticate their own Introw account. Here are the values you'll need:
Configuration parameter
Value
MCP server name
Introw
Endpoint URL
Your Introw MCP URL, generated in Settings → Integrations (see Step 1 below)
Authentication type
OAuth
### For administrators (setting up the connection)
This only needs to be done once. After this, everyone on your team can connect their own Introw account to Gemini in seconds.
Step 1 to Copy your Introw MCP URL Inside your Introw workspace, go to Settings → Integrations , find the Gemini integration and click Configure . Introw will generate an MCP connector URL - copy it, you'll need it in the next step.
Step 2 to Create the data store in Gemini Log in to your Google Cloud Console , navigate to Gemini Enterprise → Integration Management , and click ➕ Create data store . Select Custom MCP Server .
Step 3 to Configure the endpoint Set the display name to Introw and paste the MCP connector URL you copied from Introw.
Step 4 to Configure authentication Select OAuth . This ensures every user authenticates with their own Introw account, keeping data boundaries intact.
Step 5 to Discover and enable tools Open the new Introw data store, go to Actions , and click Reload custom actions . Review the discovered Introw tools and click Enable actions .
🔧 Need technical details?  Read Google's documentatio n for connecting a custom MCP server to Gemini for the configuration options.
The admin setup is done. The Introw connector is now available to your team in Gemini. Each team member follows the steps below to start using it.
### For end users
You don't need access to Google Cloud. You just authorise Gemini to use your own Introw permissions. It takes less than a minute.
Step 1 to Ask a question about Introw In your usual Gemini chat, type a prompt related to Introw, for example "Check Introw for my partners with pending deal registrations."
Step 2 to Authorise via OAuth Because your admin configured OAuth, Gemini will show a sign-in card reading "Introw requires authentication." Click it, login in with your usual Introw account, and grant Gemini permission to access your data.
Step 3 to Start exploring Once authenticated, Gemini answers using live data from Introw, enforcing the exact same permissions you have in the platform. From here, the possibilities are wide open.
### Permissions and data security
Gemini's access mirrors your Introw access exactly, the same data, the same actions, the same boundaries. If you can see it or do it in Introw, Gemini can too. If you can't, neither can Gemini.
On top of that, you're in full control of how Gemini behaves. For each capability, like adding comments, retrieving tier information, updating deals or creating tasks, you can choose one of three modes:
Mode
What it means
✅ Allowed
Gemini performs the action automatically
🔔 Approval required
Gemini asks for your confirmation before acting
🚫 Blocked
Gemini cannot perform this action at all
This means you can move fast where you trust it, and stay in control where it matters. For example, you might allow Gemini to read all partner data freely, require approval before it adds comments, and block it from updating deal stages entirely, all at once.
### Frequently asked questions
Does Gemini store my Introw data? No. Your Introw data is fetched in real time when you ask a question and is scoped to your session, it isn't persisted between conversations.
Can other Gemini users see my partner data? Absolutely not. The MCP connection is tied to your individual Introw account, and your data is never shared with other users.
Do I need a specific Introw plan to use this? This feature is available on all Introw paid plans. You'll also need a Gemini Enterprise plan that supports custom MCP data stores.
### Need help?
We're here for you. Reach out via the chat widget in your Introw portal, or email us at [email protected] . We'd also love to hear how you're using Gemini with Introw, the use cases our customers discover always inspire us. 🚀
- Using your MCP Server with Introw’s AI Agent
- Install the Claude connector of Introw
- Give your partners their own AI assistant to collaborate in real time via Introw's Partner MCP
- 🚀 Customer Deep Dive: How Quatt Powers Installer Operations with the Introw MCP
- Using Introw with ChatGPT

---

## The Introw-Powered PAM: A Day in the Life
Source: https://support.introw.io/en/articles/15596033-the-introw-powered-pam-a-day-in-the-life

What if your entire partner program briefed you every morning, and offered to handle the follow-ups for you? ☕  Partner data is scattered between new registrations, quiet accounts, and shifting deal stages, things slip through the cracks.
Introw + Claude fixes this by turning your live partner data into an actionable morning briefing. It doesn't just tell you what's wrong; it proposes the next move and handles the execution from updating deals, messaging partners, and creating tasks for you and your partners.
Here is a look at a PAM/CAM's new daily routine thanks to Introw, featuring copy-paste prompts you can start using today.
### Make it your daily habit, or let Claude run it for you
Instead of clicking through dashboards, you open Claude and ask one question. Introw pulls your live data and hands back a prioritised view of your morning, and then suggests what to do about each item.
💬 "Give me my partner briefing for today. What's new since yesterday, which deals need me, which partners have gone quiet, and where should I focus? For each item, suggest the action I should take."
Want to take the manual step out entirely? In Claude, you can schedule your briefing as a recurring task so it runs on its own, every weekday morning, for example, and your partner overview is waiting for you before you've even opened the chat. Just describe the cadence and Claude sets it up:
⏰ "Every weekday at 8am, run my partner briefing: what's new since yesterday, deals that need me, stalled deals, quiet partners, and where to focus, with a suggested action for each."
From there it's a true daily view that finds you, instead of one you have to remember to ask for. You stay in full control: the scheduled briefing surfaces everything and proposes the actions, and anything that changes a record still follows the permission modes you've set.
In one response, Introw surfaces the things that would otherwise take an hour of digging, and pairs each one with a recommended next step:
- New partner registrations waiting on you → approve, or create an onboarding task
- Deals that moved or got updated → update the close date, or comment to the partner
- Stalled deals that haven't moved in too long → add a nudge comment and a follow-up task
- Quiet partners and regions losing momentum → re-engage, or enrol them in a refresher course
- A focus list: the handful of partners worth your time today
You don't just see the problem, you see the fix, and you can greenlight it in the same breath.
🤝 You decide, Introw does. Claude proposes the action; you approve. Update a deal, post a comment, spin up a task, or enrol a partner in training, all from the chat, all within your Introw permissions.
### See what's new since yesterday
Every morning starts with the same question: what happened while I was offline? Introw answers it instantly: new partner sign-ups, fresh deal registrations, and submitted forms waiting for your review, and offers to clear the queue.
💬 "Which partners registered or submitted a deal in the last 24 hours? Approve the ones that meet our criteria and create an onboarding task for each new partner."
No more checking whether a deal registration slipped through overnight. Introw shows you what came in, recommends a decision, and, on your go-ahead, actions it.
### Pick up the right deals and update them on the spot
Not every deal needs you every day, but the ones that changed usually do. Introw flags the deals where something happened, then proposes the update each one needs.
💬 "Show me all partner deals with activity in the last 3 days. For any with a close date that's now in the past, suggest a realistic new close date and update it, and add a comment to the partner asking for a status."
Here's what Introw does behind the scenes:
- Claude pulls every recently active deal and spots the ones with stale or past close dates.
- It proposes a new close date for each, based on stage and recent activity.
- On your approval, Introw updates the close date directly on the deal.
- It adds a partner-facing comment requesting a status update, and gives you a clean summary of everything it touched.
A pipeline clean-up that used to eat your Monday becomes a single, reviewable prompt.
### Catch stalled deals before they die and re-engage them
Stalled deals rarely announce themselves, they just quietly stop moving. Introw makes them impossible to miss, then turns the alert into action.
💬 "Which open partner deals haven't changed stage in over 30 days? For each, add a comment nudging the partner to schedule a check-in and create a follow-up task for me due this Friday."
Introw surfaces the at-risk pipeline, posts the nudge to each partner, and lines up your follow-ups, so idle deals get a push the moment you spot them, not next quarter.
### Spot quiet partners and enrol them in what they're missing
A partner going dark is the earliest warning sign of churn, and it's the easiest thing to miss across a large portfolio. Introw tracks engagement across your whole partner base, tells you who's slipping, and proposes a way back in.
💬 "Which partners have had no activity in the last 45 days but still have open deals? Add a re-engagement comment to each, create a task for me to call them, and enrol any that never finished onboarding in the 'Product Essentials' course."
Introw turns silence into action: a nudge to the partner, a reminder for you, and the right training course to get a cooling partner productive again, before the relationship goes cold.
### Decide where to focus, then act on it
The hardest part of the job isn't seeing the data, it's deciding what's worth your limited hours. Introw weighs goal progress, pipeline, and recent activity together, points you at the partners where your attention pays off most, and sets up the work.
💬 "Based on goal progress and open pipeline, which 5 partners should I prioritise this week? Create a task for each with a suggested next step, and add a comment to the two that are closest to hitting their target."
You walk into the week with a clear plan, and the tasks already created to execute it.
### Everything Introw can do for you, in the same chat
A briefing is only useful if you can act on it. That's the point of the Introw connection: Claude doesn't just answer, it proposes the next step and, with your go-ahead, carries it out inside Introw. Here's what it can take off your plate:
Update deals: close dates, stage, amount, and other fields, straight from the conversation
"Push the close date on the Acme deal to end of next month and log why."
Comment to partners: leave partner-facing notes on deals or partner records
"Add a comment on BrightPath's stalled deal to schedule a check-in this week."
Create and update tasks: for yourself or your partners, with due dates
"Create a task for me to review TechVentures' three quiet deals by Friday."
Enrol partners in training: assign the right course to keep partners certified and productive
"Enrol every partner who joined this month in the onboarding course, and add the 'Advanced Selling' course for any Gold partner who hasn't completed it."
Prepare for the call you just lined up
"I have a call with BrightPath in 30 minutes, give me a full briefing: deal activity, goal progress, open tasks, and anything that needs my attention."
⚡ From reading to doing. Introw closes the gap between spotting what matters in the morning and handling it before lunch: proposing each action and executing it on your word, all from one chat.
### What to expect
Introw works best when you give Claude context. The more specific your question, the sharper the answer and the action. Adding the partner name, time period, tier, region, or deal stage all help. Broader questions work too, and you can always follow up to drill in.
A few things worth knowing:
- Every answer is based on your live Introw data at the moment you ask.
- Introw enforces your permissions: Claude only ever sees and acts on the partners and fields your user can access.
- It works in multiple languages, so use whichever suits you.
### Getting started
If Claude is already connected to your Introw workspace, you're ready: just try the briefing prompt above in your next conversation. If you haven't connected it yet, follow the steps in Install the Claude connector of Introw . For more inspiration, see Introw + Claude: use cases & what's possible and Let Claude manage your partners .
### Need help?
We'd love to hear how you've built your daily view: the workflows our customers invent always push us further. Reach out via the chat widget in your Introw portal, or email [email protected] . 🚀
- Install the Claude connector of Introw
- Introw + Claude: use cases & what's possible
- Let Claude manage your partners, agentic partner updates via Introw
- The Introw-Powered Partner: A Day in the Life
- Using Introw with ChatGPT

---

## The Introw-Powered Partner: A Day in the Life
Source: https://support.introw.io/en/articles/15598653-the-introw-powered-partner-a-day-in-the-life

What if your partners could just ask for what they need, register a deal, check their tier, see what's next, and get a clear answer in seconds, any hour of the day?
For most partners, selling alongside a vendor means chasing logins, digging for the right deck, and emailing someone to ask where a deal stands. The friction is quiet, but it's the reason partners drift.
Introw removes it. Your partners open one branded portal that already knows who they are, what they've sold, and what they should do next, with an AI assistant on hand 24/7 that answers from their own pipeline data and your connected knowledge bases, and can take action for them on the spot.
Here's a look at a single day for one of your partners, a sales rep at a reselling partner we'll call Northwind, and how the Introw-powered portal carries them through it.
No username, no password, nothing to reset or share around the office. Your partner clicks the link in their email (or their saved bookmark), confirms it's them, and lands straight in your branded portal. 
🔐 No passwords, no lockouts. Introw signs partners in with a secure verification link, plus SSO out of the box for Google and Microsoft, or your own provider via OIDC and SAML. The biggest reason partners stop logging in just disappears.
Because the portal carries your branding and can live on your domain , your partner experiences it as your partner program, not a third-party tool they had to learn.
The home page isn't generic. Introw personalises it from your CRM and partner data, so your partner immediately sees their current tier, how close they are to the next one, and the handful of things worth doing today. No hunting, no "where do I even start."
If they'd rather just ask, the AI assistant is right there:
💬 "What tier am I on right now, what's my progress this quarter, and what do I need to do to reach the next tier?"
Introw answers from their live data: current tier, the exact metrics behind it, the gap to the next level, and what closing that gap is worth, like a higher commission rate or new benefits. The partner sees not just where they stand, but the next move that moves them up.
This is the heart of the experience. Your partner doesn't file a ticket or wait for their partner manager to be online. They ask, in plain language, any time, and Introw answers instantly from the data they're allowed to see, plus the knowledge bases you've connected.
💬 " What tier am I on right now, what's my progress this quarter, and what do I need to do to reach the next tier ?"
One question, three answers, pulled together instantly. The partner's current tier and quarterly progress come from their own CRM-synced data, strictly gated so they only ever see their own numbers, never another partner's. The "what do I need to do next" part is answered from your connected knowledge bases over MCP, the same approved tier criteria and program docs your team maintains, so the guidance is always on-message and never out of date.
🔒 Gated by design. Introw enforces your permissions on every answer. The assistant only ever reads the partner's own deals, contacts, tasks, and the content you've shared with them, and pulls supporting knowledge only from the sources you've connected. Power for the partner, control for you.
Partners who prefer to work inside their own AI tools can connect to the same data through the Introw MCP, so the assistant comes to them, in the tools they already use, with exactly the same gating applied.
Mid-morning, your partner gets a warm intro to a new prospect. Instead of breaking flow to fill out a registration form, they just tell the assistant:
💬 "Register a new deal with Stryker: €120K ARR, close date is 7/1/2026, my contact is [email protected] "
Introw turns that sentence into a structured deal registration, confirms the details back, and on the partner's go-ahead submits it, pushing it straight into your CRM and routing it for review. Partners who like a classic form still have one; the point is they can choose.
Either way, the deal lands in your pipeline clean and complete.
Behind the scenes, your team's review and approval flow runs exactly as you've configured it, and the partner is kept in the loop automatically as their registration moves from submitted to approved.
Your partner doesn't have to email anyone to ask " where does this deal stand ?" Their portal shows every deal they're involved in, at the real stage it's at, synced live from your CRM. When something changes, your AE updates the stage, a close date shifts, a note is added, the partner sees it, and gets notified, without anyone having to relay it.
💬 "Summarise everything that changed on my deals since last week, and flag anything that needs me."
That shared, always-current view is what makes co-selling actually feel joint. The partner stops guessing, you stop fielding status requests, and both sides are working from the same truth.
Visibility tells your partner where a deal stands. The AI deal coach tells them what to do about it. Introw embeds a personalised coach in every partner deal, one that knows your sales process, your objection handling, and your enablement, and tailors its guidance to that deal's stage, vertical, and recent activity. For a partner rep who doesn't sell your product every day, it's the difference between guessing and knowing. 
Because the coach reads the live deal, its advice is specific to this opportunity: the best next action to move the stage forward, how to handle the exact objection the partner is hearing, and which approved asset to share with the prospect right now, the security overview during evaluation, the ROI one-pager when price comes up, the case study that matches the prospect's industry. The partner always knows the next step and walks away with the right content already in hand.
💬 "I'm at the proposal stage with CarMax and they pushed back on not being able to handle their complexity. What's my next move, how do I handle the objection, and what should I send them"
🎯 Your best sales coach, on every deal. Whether it's a partner's first opportunity or their fiftieth, the coach is grounded in your playbook and the deal's real state, so partners sell the way you'd want them to and reach for the right asset at the right moment, without pulling in your team.
A new product release drops, or you launch a Q3 promo. Your partner doesn't have to go looking. Introw surfaces your latest announcements, enablement updates, and news right in the portal, and can notify the partners it's relevant to.
💬 "What's new from the vendor this month that's relevant to my open deals?"
The assistant connects the news to the partner's own pipeline, so an update isn't just an announcement, it's "here's the new feature that helps you win the Contoso deal."
After lunch, the portal nudges your partner toward training, but not generic, one-size-fits-all training. Introw tailors the learning path to who the partner is and what they've actually done , using your CRM and partner data.
A partner sales rep like our Northwind contact is guided down a selling track: discovery, demo certification, objection handling, the courses that help them close. A marketing contact at the same partner gets a completely different path, focused on co-marketing, campaign assets, and brand guidelines. Same portal, two personalised journeys, assigned automatically.
💬 "What should I complete next to get sales-certified, and how close am I?"
Introw assigns the right next course, tracks completion and certification automatically, and reflects it back in the partner's tier and benefits, no spreadsheets, no manual enrolment on your side. A partner who finishes their selling certification can see their new status and unlocked perks the moment they're done.
🎓 Right person, right path, automatically. Because enrolment is driven by partner role and CRM signals, every contact is trained on what their job actually needs, and you never hand-build a learning plan again.
Serious partnerships run on a mutual action plan, the set of steps both sides agreed to, with owners and due dates. In the portal, your partner sees that plan live: what they own, what you own, what's done, and what's coming up.
And it doesn't rely on anyone remembering. Introw watches the due dates and nudges automatically, reminding the partner of their next step before it slips, and flagging the items they're waiting on you for.
💬 "What's outstanding on my action plan with the vendor, and what's due this week?"
The partner can add a comment, mark a step complete, or create a follow-up task right from the conversation. The plan stays alive between meetings instead of dying in a doc, so the joint motion keeps its momentum, on autopilot.
Late in the day, the partner needs the one-pager for the Contoso pitch. No folder-digging, no "which version is current?" They ask, and Introw serves the right, approved asset from your content library, scoped to what this partner is allowed to access.
💬 "Find me the latest Data processing agreement for a security overview I can share with a prospect."
Because the assistant pulls from your maintained library and connected knowledge bases, partners always reach for the current, on-brand version, and you stop emailing the same decks over and over.
The thread running through the whole day is that the partner is never stuck and never alone. Whatever the moment, checking standing, moving a deal, finding an answer, the same assistant is there, grounded in their real data and your real content.
💬 "Given my pipeline, my tier progress, and my open tasks, what are the three best things I can do this week to grow with you?"
Introw weighs their pipeline, goal progress, and activity together and hands back a focused, personal plan, then helps them act on it. That's the difference between a portal partners have to be reminded to visit and one they actually want to.
A few things worth knowing about the partner experience:
- Every answer is grounded in your live Introw and CRM data at the moment the partner asks.
- Introw enforces your permissions on every read and action: a partner only ever sees and touches their own data and the content you've shared.
- Agentic actions, like registering a deal, adding a comment, or completing a task, follow the permission modes you set, so partners move fast while you stay in control.
- It works in multiple languages, so each partner can work in whichever suits them.
- Partners can work inside the portal or connect to the same gated data from their own AI tools via the Introw MCP or directly from their CRM via Introw's Partner Connect module.
- Build a partner directory powered by Introw
- Give your partners their own AI assistant to collaborate in real time via Introw's Partner MCP
- The Introw-Powered PAM: A Day in the Life
- Everything Your Partners Can Do in Introw
- Using Introw with ChatGPT

---

## Everything Your Partners Can Do in Introw
Source: https://support.introw.io/en/articles/15615361-everything-your-partners-can-do-in-introw

What can a partner actually do inside Introw? Just about everything they'd otherwise email you for, on their own, any hour of the day.
Every capability below shares the same foundation. The partner opens one branded portal that already knows who they are and what they've sold, with an AI assistant on hand 24/7 that answers from their own pipeline data and your connected knowledge bases, and can take action for them on the spot. Throughout, we'll follow a sales rep at a reselling partner we'll call Northwind.
Deal registration is the moment co-selling either starts clean or starts as a mess. Introw gives partners three ways in, so registering is never the reason a deal goes unreported. 
In the portal. A classic registration form for partners who want one: structured fields, your required data, validation built in. It lands in your CRM clean and complete. Or via the portal agent in their own wording. 
Via an embedded form. Drop a registration form straight onto your partner page, microsite, or campaign landing page. A partner (or their prospect) can submit a deal without even being in the portal, and it still routes into your pipeline and review flow. 
Agentically, in the tools they already use. No form at all. The partner just says it, in their own CRM , Slack, Teams, Claude or other LLM' s.
💬 "Register a new deal with Stryker: €120K ARR, close date 7/1/2026, my contact is [email protected] "
Introw turns the sentence into a structured registration, confirms the details back, and on the partner's go-ahead submits it into your CRM and routing. 
🔐 Your review flow, unchanged. However a deal comes in, your approval process runs exactly as you've configured it, and the partner is kept in the loop automatically as it moves from submitted to approved.
Once a deal is in, the partner never has to email anyone to ask where it stands. The portal shows every deal they're involved in, at its real stage, synced live from your CRM. 
 Updates come to them. When an AE moves a stage, shifts a close date, or adds a note, the partner sees it, and gets notified by email, Slack, or Teams, whichever they use. No one has to relay anything. 
Sleepy deals get nudged. Introw watches for deals that have gone quiet and prompts the partner before momentum is lost, so a stalled opportunity gets a push instead of being forgotten. Learn more
💬 "Summarise everything that changed on my deals since last week, and flag anything that needs me."
That shared, always-current view is what makes co-selling feel joint. The partner stops guessing, and you stop fielding status requests.
Beyond individual deals, the partner gets a live read on how they're doing overall, updated in real time from your CRM, not a quarterly recap that arrives too late to act on.
Depending on what your program tracks, a partner can see their revenue and ARR generated, deals registered, closed-won deals, tickets closed, certifications acquired, and progress against the goals you've set for them. It's the same scoreboard you see on your side, gated to their own numbers.
💬 "How am I tracking against my targets this quarter, and what's my closed-won revenue so far?"
🎯 Goals that pull, not nag. Because progress is tied to tier and benefits, a partner can see exactly what hitting the next goal unlocks, so the numbers point them at the next move instead of just reporting the past.
Introw tailors the learning path to who the partner is and what they've actually done, using your CRM and partner data. Our Northwind rep is guided down a selling track; a marketing contact at the same partner gets a co-marketing path instead. Same portal, different journeys, assigned automatically. 
Partners complete courses, earn certification, and can share that credential straight to LinkedIn, turning your enablement into their visible proof of expertise (and a bit of free reach for your program).
💬 "What should I complete next to get sales-certified, and how close am I?"
🎓 No manual enrolment. Completion and certification are tracked automatically and reflected in the partner's tier and benefits, so you never hand-build a learning plan.
Marketing development funds usually live in email threads and spreadsheets. In Introw, the partner runs the whole thing themselves. 
 Request a budget. A partner can ask for funding to launch a marketing event or campaign that generates leads, with the request routed into your approval flow.
See everything, end to end. The partner gets full transparency on their available budget, the claims they've submitted, and what's been paid out, with no need to ask you for a status.
💬 "How much MDF do I have left this quarter, and where do my open claims stand?"
Partners sell harder when they can see what selling is worth. Introw gives them full transparency on commission, grounded in your CRM data. 
A partner can see the commission they're eligible to earn for closing a deal or referring a lead, what's upcoming based on their performance, and what's already been paid. No black box, no waiting for a statement.
💬 "What commission am I in line for if I close Contoso, and what's already been paid out to me this quarter?"
For partners who drive demand rather than close deals directly, Introw turns referrals into tracked, paid outcomes. 
A partner can capture an affiliate link for a campaign and share it with their prospects. When a prospect converts, the lead is automatically attributed and created for you, and the partner sees the resulting commission come through, all the way from click to payout.
💬 "Grab me an affiliate link for the spring campaign, and show me which leads it's brought in so far."
A partner shouldn't have to dig through a shared drive or guess which deck is current. Introw gives them a content library, but it isn't the same library for everyone.
Assets are curated to the individual partner: they only see what's relevant to them, based on their tier, their performance, or the type of partner they are. A new bronze reseller sees onboarding and core selling material; a top-tier partner sees advanced enablement and co-marketing assets. Nothing irrelevant, nothing they haven't earned access to, nothing out of date.
💬 "Find me the latest sales one-pager and the security overview I can share with a prospect."
Because the assistant pulls from your maintained library and connected knowledge bases, partners always reach for the current, on-brand version, and you stop emailing the same decks over and over.
📁 Right assets, right partner. You curate once by tier, segment, or performance, and Introw shows each partner only their slice, so the library scales without becoming a dumping ground.
- Commissions in Introw: a complete walkthrough
- Give your partners their own AI assistant to collaborate in real time via Introw's Partner MCP
- The Introw-Powered PAM: A Day in the Life
- The Introw-Powered Partner: A Day in the Life
- Using Introw with ChatGPT

---

## HubSpot integration overview
Source: https://support.introw.io/en/articles/15646259-hubspot-integration-overview

Keep your partner relationships and CRM data aligned with the Introw + HubSpot integration. Automatically sync partner information, contacts, deals, and tickets in real time, so your team can collaborate efficiently, make informed decisions, and grow faster.
Give resellers, referral partners, and distributors a branded portal where they can collaborate on deals, support tickets, and any custom HubSpot data, without giving them access to your HubSpot and without spending HubSpot seats on them.
### Build the partner experience with no-code blocks
- Drag in any section you need: introduction banners with CTAs, dashboards, goal trackers, tiering models, FAQs, documents, videos, and forms.
- Embed any HubSpot data directly into the portal and edit it as easily as you would a document: deals, customer lists, lead lists, line items, quotes, any object within your HubSpot environment.
- Apply your own branding (fonts, colors, logos) and host the portal on a custom domain such as partners.yourcompany.com to make it fully aligned with your brand.
### Run your partner program with agents that act, not just answer
Introw isn't AI bolted onto a portal, it's agents doing the work, on both sides of the partnership. All enabled in one click. Partners don't just ask questions and self-serve; the agent acts for them: registering deals, submitting forms, and pulling commission or status updates in the flow of conversation. Less manual support on your side.
- AI deal coach on every deal : the agent reads each open deal and tells partners what to do next, where it's stuck, what's missing, and the move most likely to advance it. Coaching that used to depend on a partner manager's attention, now on every deal by default.
- Agentic deal registration : partners register deals by simply describing them in natural language, or straight from their own Claude or AI agent via the Introw MCP. The agent handles the submission and routes it, no forms to fill, no portal login required.
- Autonomous approvals : agents react to inbound partner requests on your behalf, deal registrations, MDF requests, partner applications. Set the rules and the agent reviews, responds, and auto-approves what qualifies, so partners get instant answers and your team only touches the edge cases. Learn more
- Internal AI agent : the prep work that eats a partner manager's week, done for you. It walks into QBRs ready with the numbers, surfaces the opportunities worth chasing, and lays out your day around what actually moves partners. Run it inside Introw, or from your own Claude instance or any MCP-connectable agent. The partner data comes to where you already work, so your team spends time managing relationships, not assembling them.
- AI-powered LMS : generate full training courses from your website, portal content, or MCP server in minutes, modules, multiple-choice or open-ended quizzes, and certifications you can enroll partners into in a single click. Learn more
### Collaborate on deals, contacts and any custom object
- Choose exactly which HubSpot objects (including custom objects), pipelines, stages, and properties are visible and editable for partners.
- Allow partners to update selected properties and create custom object records, line items or orders, for example, that all sync back to HubSpot in real time.
- Add a deal registration form so partners can submit deals that automatically create HubSpot deals.
- Trigger automated email updates when a deal's stage changes, partners can reply directly from email without logging in to the portal.
- Co-sell in real time: partner comments appear on the HubSpot deal timeline, and HubSpot stage or property changes flow back to the portal instantly.
### Share sales enablement and support content
- Announcements to publish product updates and news partners need to see.
- Documents and videos to share enablement assets and see how partners engage with each one.
- Support tickets to collaborate on issues and resolutions without leaving the portal.
- Projects to assign mutual action items so partners can move tasks through onboarding or joint plans.
### Give partners a personalized view
- HubSpot data fills in dynamically per partner: total revenue, deal count, qualified leads, tier, and any custom KPI.
- Goals update in real time so partners always know where they stand.
- Partners log in through a branded sign-in page you fully control.
- Share a deal to partners via Introw's app card in HubSpot
- Salesforce integration overview
- Partner Connect: a 2-way CRM integration with HubSpot
- Give your partners their own AI assistant to collaborate in real time via Introw's Partner MCP
- What is Partner Connect?

---

## Send notifications from your own email domain
Source: https://support.introw.io/en/articles/15701442-send-notifications-from-your-own-email-domain

By default, Introw sends all partner notifications, portal invites, announcements, comments, deal updates, and more from [email protected] . With a custom email domain, Introw sends these notifications from your own domain instead, so they arrive in your partners' inboxes as [email protected] . 
For example, instead of partners receiving a notification from:
- [email protected]
- they receive it from [email protected]
### Why send from your own domain
Sending notifications from your own verified domain gives you three big advantages:
- More trust with your partners : emails come from a brand they already recognize, not a third-party address.
- Higher open rates : recognizable senders get opened far more often than unfamiliar ones.
- Fewer emails in spam : because the domain is authenticated (SPF, DKIM), inbox providers are far less likely to filter Introw notifications into Spam, Junk, or Promotions. 
Good to know : This is the email-sending equivalent of linking your custom portal domain . The portal domain controls the URL partners visit; the email domain controls the address your partners' notifications are sent from. You can set up either or both.
### Before you start
- You'll need access to your domain's DNS settings (usually through your hosting or domain provider). If you're not sure who manages your DNS, ask your IT team.
- Decide which sending address you'd like to use, e.g. [email protected] or [email protected] .
### Set up your custom email domain
Navigate to Portal > Portal settings , and click Configure your own email domain . 
- Enter the domain you'd like to send from, e.g. yourdomain.com , and the sender address and display name you'd like partners to see, e.g. Partner team < [email protected] > . Click Next . 
- Introw shows you the DNS records to add. Copy the TXT names, values and CNAME records exactly as provided, these authenticate your domain (SPF, DKIM) so inbox providers know Introw is allowed to send on your behalf. 
- Go to the DNS page of your domain management platform and add each record with the values provided.
- Return to Introw and click Finish . Once the records are detected, your custom email domain becomes active and all future partner notifications are sent from your address.
Note : It may take up to 24 hours for your DNS settings to propagate worldwide, depending on your hosting provider. Until verification succeeds, Introw continues sending from [email protected] .
### How to access the DNS settings of your domain
The following steps must be completed on your domain's DNS settings (not in your Introw account). We recommend contacting your hosting provider if you need help.
- Log in to your domain provider (usually your hosting platform).
- Find the DNS settings for your domain. You can find instructions by searching "DNS settings" + your hosting provider's name on any search engine.
- Create the records with the type , Name , and Value exactly as shown in Introw.
Hosting providers may label these fields differently. They can be referred to as:
- Name and Host
- Domain and Value
- Domain and Host
#### Make sure your DNS is configured correctly!
- Add every record Introw provides, SPF, DKIM  must all be present for authentication to pass.
- Check the Name and Value of each record match exactly, with no trailing spaces.
- Allow up to 24 hours for propagation before assuming verification has failed.
### What happens after setup
Once verified, Introw automatically sends all partner-facing notifications from your custom domain, including portal invites, announcements, comments, and CRM updates. No other configuration is needed, your existing notification settings stay exactly as they are.
If your partners were previously asked to whitelist [email protected] , that's no longer necessary, emails now come from your own trusted domain.
- Launch your partner portal
- Link your Custom Domain
- Add your partners to Introw
- My partner does not receive any emails
- Introw forms are protected from spam

---

## What is Partner Connect?
Source: https://support.introw.io/en/articles/15763666-what-is-partner-connect

Partners don't live in your portal. They live in their own tools.
Most PRMs assume partners will log into the vendor's portal, work in the vendor's pipeline, and update the vendor's records. They won't. Partners have their own CRM, their own pipeline stages, and their own process, and they sell many other vendors' products through that same pipeline. Forcing them into yours is friction, and friction means deals don't get registered, stages don't get updated, and your partner pipeline data goes stale within a week of launching the program.
Partner Connect closes that gap by making Introw a headless PRM : the portal becomes optional, not the point. Partners collaborate with you from wherever they already work, their own CRM, their email inbox, or their own AI assistant, and every deal, comment, and update flows into your CRM automatically. Partners stop logging into a portal to update you, and you stop chasing them for updates that never come.
💡 What "headless" means: There's no interface a partner has to adopt. Introw's MCP acts as the connective layer between your partners' tools and your CRM, so collaboration happens inside the apps they already live in. The portal is there when they want it, but they never need it.
Partner Connect isn't a single feature, it's a principle: partners collaborate from the tools they already use, not from a portal you ask them to adopt. Today that takes three forms, all powered by Introw's MCP.
### 1. From their CRM
Your partners connect their own HubSpot and work entirely from it. Partner Connect embeds as a card on their existing deal, contact, and company records, so from inside their CRM they can register a new deal, link an existing one to your shared pipeline, comment, and share updates, all without ever logging into Introw.
On your side, Introw keeps everything in sync. Whatever CRM you run, every action a partner takes flows into your CRM and the Introw shared pipeline you already use. What you get:
- ⚡ Set up and connect a CRM in minutes. Simple connection for HubSpot, no implementation project needed.
- 🔄 Two-way sync with field and stage mapping. Deal stage, value, close date, and custom fields sync bidirectionally. Each side keeps their own pipeline stages, and Introw maps between them automatically, so the partner never has to adopt your process.
- 🧩 A native experience inside the partner's CRM. The card sits on deal, contact, and company records, with two-way comment sync and manual object linking from either side.
- 📝 Smart forms and deal registration. Forms auto-fill from the partner's CRM data, attribution is handled automatically, and partners register or link a deal in one click, no double entry.
- 🌐 One unified partner app. A single app supports multiple vendor connections from the same CRM, with role-based access and notifications that route partners back to the record when it's linked.
### 2. From their own LLM or tooling
Partners can also collaborate with you entirely through their own AI assistant or tooling , by connecting it to Introw's Partner MCP . Using MCP (Model Context Protocol), an open standard, your partners connect Introw to Claude, ChatGPT, Gemini or any other MCP-ready tool they already use. From their first chat, they can collaborate by simply asking. For example:
- "Register a new deal for Acme Corp, €40k, expected to close end of Q3."
- "Update my shared deals with Acme and add a comment that the buyer asked to postpone."
- "What's the status of my commissions this quarter?"
- "What tier am I on, and what do I need to reach the next one?"
- "How much MDF budget do I have left, and how do I request more?"
Introw answers in full context against live data and acts on the partner's behalf, registering deals, posting deal updates, and surfacing tier, commission, and MDF information, so collaboration happens at the speed of a conversation. No portal, no email, no waiting.
### 3. From their inbox
Collaboration doesn't get more headless than email. With Introw, a partner can simply reply to an Introw mail , the way they already work every day and Introw turns that reply into a live update on the deal in your CRM. A note on where things stand, a new close date, a next step: it lands on the right record automatically, with no form to fill in and no portal to open.
For the partner, it feels like nothing changed, they're just answering email. For you, the pipeline stays current on its own, and the context that usually gets buried in scattered threads is captured against the deal instead.
What ties these together is Introw's MCP, the layer that lets your partners' tools talk to Introw and your CRM. It's what links the partner's own CRM to yours, translates an email reply into a deal update, and lets an AI assistant act on a partner's behalf. Every action is scoped to exactly what a partner is allowed to see and do, so their data stays theirs and yours stays yours. Introw becomes an always-on layer on top of the access a partner already has, never a workaround.
### The problems Partner Connect solves
The problem
How Introw solves it
Partners forget to log into the vendor portal
Partners work from their own CRM, inbox, or AI, no portal switch required
Vendor pipeline stages don't match how the partner sells
Each side keeps their own stages; Introw maps between them
Deal registration takes too long, so partners skip it
Register a deal from the partner's CRM, an email reply, or a quick chat
Comments and updates live in scattered email threads
Email replies and comments sync onto the right deal automatically
Vendor data goes stale because no one updates the portal
CRM-to-CRM sync runs automatically in the background
Partner managers chase status updates manually
Pipeline activity flows both ways without intervention
Partner-sourced revenue is hard to attribute
Every partner deal links to a verified CRM record on both sides
Forms require partners to re-type data they already have
Forms auto-fill from the partner's CRM data on submit
Everything starts at partners.introw.io . Your partners sign up or log in there to reach their portal, connect their HubSpot, grab their Partner MCP connector URL to link their AI assistant, and access the tools that power Partner Connect. 
Introw tip: Partner Connect is the lowest-friction way to activate a partner. Whether they prefer their CRM, their inbox, or their own AI, most partners are collaborating with you within minutes of signing up on partners.introw.io.
- Salesforce integration overview
- Partner Connect: a 2-way CRM integration with HubSpot
- Give your partners their own AI assistant to collaborate in real time via Introw's Partner MCP
- The Introw-Powered Partner: A Day in the Life
- HubSpot integration overview

---

## How Introw Solves TCMA for Vendors
Source: https://support.introw.io/en/articles/15799134-how-introw-solves-tcma-for-vendors

Through-Channel Marketing Automation (TCMA) is meant to turn a vendor's partners into an extension of their own marketing engine. Most TCMA platforms try to deliver this by building a full marketing suite inside the partner portal, then asking partners to leave the tools they already use and run campaigns from a system they don't want to be in. That model is breaking down. Partners already run marketing in HubSpot, Marketo, Klaviyo, and increasingly through their own AI agents. Introw takes the opposite approach: instead of being the place partners do their marketing, it is the asset and data layer that plugs into wherever they already work. The vendor keeps control of the content and the attribution, the partner keeps their own tools, and the marketing actually gets used.
### Partners connect their own AI agent
Introw's Partner MCP lets a partner connect their own LLM agent, like Claude or Gemini, directly to their Introw data. Instead of clicking through a portal to find what they need, a partner can ask their agent for the right assets, the latest program details, or their current deal and pipeline data, and get it back in context.
This is the shift that matters. Partners no longer come to the portal to hunt for content. Their agent brings the vendor's content and data to them, inside the workflow they already run. For a vendor, that means the assets you publish are far more likely to be picked up and used, because reaching them takes seconds instead of a login and a search.
### Every asset is tracked
The content a vendor publishes in Introw is not a static folder of files. Every asset is tracked. When a partner downloads or pulls an asset, Introw records it, so the vendor can see which assets are actually being used and which are being ignored.
That visibility changes how a channel marketing team operates. Instead of guessing which collateral is landing, you can see it. The one-pager that gets pulled by every partner in a segment is worth doubling down on. The deck nobody touches is a signal to retire or rework it. TCMA is supposed to give vendors this kind of feedback loop, and here it comes directly from real partner behavior rather than a survey or a hunch.
### Links are personalized and automatically partner-attributed
Content is only half of through-channel marketing. The other half is knowing what it produced. Introw generates affiliate campaign links that are personalized per partner, attributed to that partner out of the box.
When a partner takes one of those links and runs it through their own marketing, whether that is an email in HubSpot, a landing page, or a paid campaign, the resulting traffic and leads carry the partner's attribution with them. The vendor gets a clean line of sight from an asset to a partner to the demand it created, without asking the partner to manually tag anything or report back.
### Partners use it all in their own tools
Because the assets and the links are built to travel, partners drop them straight into the marketing tools they already run. There is no rebuilding a campaign inside the portal. A partner grabs the co-branded asset and the attributed link, runs the campaign in their own stack, and the results flow back with attribution intact.
For the vendor, this is the TCMA outcome without the TCMA overhead: partners running vendor-supplied marketing at scale, in tools they actually use, with the vendor keeping full visibility over which content works and which partners are driving demand.
### Why this model wins
The traditional TCMA platform asks partners to change how they work and hopes they comply. Introw meets partners where they are.
- Vendors supply the partner personalized content and the attributed links via Introw at scale
- Partners access them through their own AI agent and run them in their own marketing tools.
- Introw tracks every download and every attributed link, so vendors see what gets used and what it produces.
The result is through-channel marketing that partners adopt because it fits their workflow, and that vendors trust because the usage and attribution data is real. That is the need TCMA was always meant to solve, delivered without forcing anyone into a portal they don't want to live in.
- Introw Agent
- Affiliate link management in Introw
- The Introw-Powered Partner: A Day in the Life
- Everything Your Partners Can Do in Introw
- What is Partner Connect?

---

## Introw Product Update - July 2026
Source: https://support.introw.io/en/articles/15885384-introw-product-update-july-2026

A great partner program comes down to three things: meeting partners where they already work, paying them accurately for what they drive, and treating the right partners the right way. This month's release moves all three forward, Introw's AI agent now works inside Slack , commissions can run on real billing data from Stripe and Chargebee , and segments let you target the right partners everywhere in Introw.
### 💬 Introw's AI agent, now in Slack
The full power of Introw's AI agent now lives right in your Slack channels, no tab switching, no CRM login. In shared partner channels, partners simply mention @Introw to register deals, add comments, and create follow-up tasks, with every action structured correctly and synced straight to your CRM. In your internal channels, the same agent pulls partner insights and helps you prepare QBRs on the spot, so your team gets answers without digging through dashboards. Everyone stays where they already work, and your data quality improves along the way. Learn more 
### 💸 Commission based on Stripe & Chargebee data
You can now also calculate commissions on real billing and usage data from Stripe and Chargebee, so partners are rewarded on actual recurring revenue rather than a one-off deal value, and everything stays transparent on the partner record. Learn more
### 🎯 Segments: group partners once, target them everywhere
Group partners or partner contacts once (dynamically, based on any CRM or Introw data) and Introw keeps membership in sync automatically. As a partner's data changes, their experience adapts on its own across the whole platform, so every partner sees exactly what's relevant to them. Learn more
### Additional improvements
#### Custom email domain
Send partner emails from your own domain for a fully branded, trusted experience that lands better in the inbox. Learn more 
#### AI image generation
Create branded visuals for courses and announcements in seconds, no marketing or design team needed. 
- Introw's AI Agent in Slack
- Introw Product update - May 2026
- Commissions in Introw: a complete walkthrough
- Introw's Chargebee integration
- Introw's Stripe integration

---

## Why my embedded website shows up blank in Introw
Source: https://support.introw.io/en/articles/15924171-why-my-embedded-website-shows-up-blank-in-introw

💡 Introw tip: A blank embed is almost never an Introw problem, it's the embedded site telling the browser "don't display me inside another site." The fix lives on that site's server, and you (or its owner) can make it in a few minutes.
#### What's happening
When you add an Embed link section and paste a URL, Introw loads that page inside the partner portal in an <iframe> . Most content works out of the box, Google docs, Loom, Calendly, Notion, and similar providers all allow this.
Some websites, though, tell the browser they refuse to be displayed inside any other site. When that happens the browser blocks the page and Introw shows an empty section. Introw is doing its job; the browser is enforcing the rule the embedded site set. 
You can confirm this is the cause. Open the portal in Chrome, right-click the blank section, choose Inspect , and look at the Console tab. You'll see a message like:
- Refused to display 'https://yoursite.com/' in a frame because it set 'X-Frame-Options' to 'deny'.
- Refused to display '…' in a frame because an ancestor violates the following Content Security Policy directive: "frame-ancestors …".
Either message means the website is blocking the frame.
#### Why the website blocks it
Websites control framing with two HTTP response headers:
- X-Frame-Options, an older header. DENY blocks all framing; SAMEORIGIN allows framing only by pages on the same domain. It can't allow-list another site like Introw.
- Content-Security-Policy: frame-ancestors, the modern replacement. It lists exactly which domains are allowed to frame the page, and browsers give it priority over X-Frame-Options .
Sites often turn these on for security (to prevent clickjacking) without realizing it also blocks intentional embeds like the partner portal.
#### How to fix it
The change is made on the embedded website's server , not in Introw, so this is for the person who manages that site (often your web or IT team, or the tool's support if it's a third-party product).
They need to allow the domain your portal is served on. Check that domain in your browser's address bar while viewing the portal, it's your custom domain if you've set one up, otherwise your Introw portal address.
The recommended fix is to set a frame-ancestors directive that includes Introw:
Content-Security-Policy: frame-ancestors 'self' https://app.introw.io https://your-portal-domain.com;
Replace https://your-portal-domain.com with your actual portal domain, and keep 'self' so the site still works normally on its own.
If the site also sends X-Frame-Options: DENY or SAMEORIGIN , that header must be removed or updated too, modern browsers honor frame-ancestors , but a leftover X-Frame-Options: DENY can still block the frame in some cases. X-Frame-Options has no reliable way to allow a specific external domain, which is why frame-ancestors is the right tool.
Once the header change is live, refresh the portal and the embed will render.
### When you can't change the headers
If the website is a third-party tool you don't control and its owner won't allow framing, that page can't be embedded, the browser will always block it. In that case:
- Link out to it from a portal section instead of embedding it, or
- Embed an equivalent that does support framing (for example, a published Notion page, a Google Doc, or a hosted PDF).
- How to invite Partners to your portal via Introw
- Embed Introw in your product
- Embed Introw forms
- What does “No portal yet" and "No deal embed yet” mean?
- Introw forms are protected from spam

---

## SCORM Files & Introw Courses
Source: https://support.introw.io/en/articles/15945898-scorm-files-introw-courses

### Overview
Introw supports importing SCORM files as courses. This lets you bring in e-learning content built in tools like Articulate Storyline, Articulate Rise, Adobe Captivate, or iSpring and deliver it inside Introw.
You can simply import a SCORM file as a full Introw course. Introw processes the SCORM zip file and displays the content within the course, so a course you've already built in an authoring tool becomes a ready-to-assign Introw course without rebuilding it.
#### What is a SCORM file?
SCORM (Sharable Content Object Reference Model) is a technical standard for e-learning content packaging and delivery. It's essentially a ZIP file with a specific internal structure that allows learning management systems (LMSs) to import, launch, and track e-learning courses in a standardized way.
#### How does it work?
When creating a new course, choose the option to start from a SCORM file and upload the SCORM zip file on the next screen. 
Introw will process the zip file and then display the SCORM content within the course.
#### Which SCORM files are supported?
Introw supports SCORM 1.2 and SCORM 2004 file types.
When downloading SCORM files from tools like Articulate, make sure to select the LMS option and then choose one of the supported file types.
#### Analytics & SCORM files
What Introw Tracks
Notes
Course completion
Used for course progress and completion tracking
Time spent on course
Captured at the course level
Events within the SCORM file
Not tracked by Introw. This data stays within your SCORM authoring tool
Here's how to think about analytics when using SCORM files:
- Introw captures when a SCORM course has been completed. This allows admins to track the progression or completion of a course.
- Introw captures time spent on a SCORM course.
- Introw doesn't capture any events or analytics within the SCORM file itself. That data lives with your SCORM provider and authoring tool.
### FAQ
Can I export Introw courses as a SCORM file?
No. Introw only supports importing external SCORM files. Introw courses cannot be exported as SCORM files.
Can I add additional content to a SCORM course?
No. All content is controlled by the external provider and SCORM file. It's not possible to add additional Introw content within a SCORM course.
My SCORM file isn't displaying correctly. What should I check?
- Confirm the file was published as SCORM 1.2 or SCORM 2004 (not xAPI/cmi5)
- Confirm you're uploading the .zip file directly, do not unzip it first
- Check that the zip file includes an imsmanifest.xml at the root level; if it doesn't, the package wasn't exported correctly
- If published from Articulate, re-export using the LMS output type and re-upload
- How to use Introw's course builder
- Show Introw course enrollments and certificates in HubSpot
- Introw product update - March 2026
- Show Introw course enrollments and certificates in Salesforce
- 13 little Introw tricks you probably didn't know about

---

## Using Introw with ChatGPT
Source: https://support.introw.io/en/articles/15970623-using-introw-with-chatgpt

Introw is officially listed in ChatGPT's plugin directory. Find it, click Install Plugin, sign in with your Introw account. That's the whole setup.
From that moment on, your partner program lives inside the assistant you already have open. Ask a question, get an answer from live Introw data. Ask for an action, and it happens in Introw and flows straight into your CRM. No tabs, no portal hopping, no exports.
Under a minute, and you only do it once.
- Open the plugin directory in ChatGPT and search for Introw . You can also manage it any time under Settings → Apps .
- Click Install plug-in. ChatGPT opens an Introw sign-in.
- Sign in with your usual Introw account and grant access. No API key, no URL, no secret to paste.
- Start asking. Open a new chat and try "Introw, which of my is performing the best this year?" 
💡 Nothing to configure in Introw. There's no integration to switch on, no URL to copy, no admin project. Your existing Introw login is the integration.
Everyone who touches the partner program gets the same thing: their Introw data, in plain language, with the ability to act on it. What that looks like depends on the job.
### Partner managers
Stop preparing for partner calls and start having them.
- "Generate a QBR for Amazon, pipeline, deal activity, open tasks and where we're behind."
- "Which of my partners went quiet in the last 30 days, and what should I say to each one?"
- "Register a deal for Acme, roughly $40k, closing next month, sourced by our reseller."
- "Log a summary of today's call on the Contoso deal and create a follow-up task for next Tuesday."
- "Coach me on the three biggest partner deals in my pipeline, what's the risk on each?"
### RevOps and partner ops
The reporting you used to build by hand, answered in a sentence.
- "What's total partner-attributed pipeline this quarter, split by partner type?"
- "Show commission status for our Gold tier partners and flag anything unpaid for more than 30 days."
- "Which partners are above their tier threshold and should be upgraded?"
- "Where is our deal registration data incomplete or stale?"
- "Compare partner-sourced against partner-influenced revenue for H1 and tell me what moved."
### Partner marketing
Campaigns built on what partners actually do, not on what you hope they do.
- "Which collateral did partners actually use last quarter, and which never got opened?"
- "Which partners have unused marketing funds, how much, and by when do they have to spend it?"
- "Draft a launch email for our top 20 resellers, tailored to each one's tier and goals."
- "Who submitted our co-marketing request form in the last month and what did they ask for?"
- "Find every partner who sells into fintech and build me a segment brief."
🚀 This list is not a menu. Anything you can see or do in Introw, you can ask for in plain language, then chain it, compare it, turn it into a document, schedule it, and ask again next week. The limit is what you think to ask.
ChatGPT's access mirrors your Introw access exactly, the same data, the same actions, the same boundaries. If you can see it or do it in Introw, ChatGPT can too. If you can't, neither can ChatGPT.
Every request is authenticated as you and scoped to your user permissions, the same rules that apply when you log into Introw directly. A partner manager sees their partners and their deals. An admin sees what an admin sees. Nothing bleeds across users.
On top of that, you control what ChatGPT is allowed to do. For each capability, adding comments, retrieving tier information, updating deals, creating tasks, pick one of three modes:
Mode
What it means
✅ Allowed
ChatGPT performs the action automatically
🔔 Approval required
ChatGPT asks for your confirmation before acting
🚫 Blocked
ChatGPT cannot perform this action at all
Move fast where you trust it, stay in control where it matters. Let ChatGPT read all partner data freely, require approval before it comments on a deal, and block deal stage updates entirely, all at the same time.
Do I need to set anything up in Introw first? No. Introw is listed in ChatGPT, so there's no URL to copy and no integration to configure. You need a paid Introw plan and your normal Introw login.
Why don't I see Introw in ChatGPT? On Enterprise and Edu, apps are disabled until a workspace admin enables them, ask your ChatGPT admin to enable Introw under Workspace settings → Apps . On Business, Plus, Pro and Go, availability depends on your plan and workspace settings.
How do I make sure ChatGPT uses Introw? Mention it by name, "Introw, which partners are up for renewal?", or pick it from the apps menu in the composer. Once it's connected, ChatGPT will also reach for it on its own when your question is clearly about partner data.
Does ChatGPT store my Introw data? No. Your data is fetched in real time when you ask and is scoped to that conversation, it isn't persisted between sessions. Results do pass through OpenAI's infrastructure as part of your chat; see OpenAI's privacy documentation for details.
Can other ChatGPT users see my partner data? No. The connection is tied to your individual Introw account and your permissions. Your data is never shared with other users.
Can ChatGPT change data in my CRM? Yes, within your permissions and whatever modes you've allowed. Introw stays two-way synced with HubSpot or Salesforce, so a deal registered or a comment logged from ChatGPT lands in your CRM like any other update.
Can I use Introw with other assistants too? Yes. Introw also connects to Claude, Gemini and any other MCP-compatible assistant, and your partners get their own version through Partner Connect . Same data, same permissions, whichever tool your team already lives in.
- Install the Claude connector of Introw
- Introw + Claude: use cases & what's possible
- Give your partners their own AI assistant to collaborate in real time via Introw's Partner MCP
- Using Introw with Gemini via MCP
- The Introw-Powered Partner: A Day in the Life

---

## Build a training curriculum with sequential courses
Source: https://support.introw.io/en/articles/16412140-build-a-training-curriculum-with-sequential-courses

You rarely want a brand new partner to land on Advanced Sales Training on day one. You want a path: Introduction to Acme → Basic Sales Training → Advanced Sales Training , where each course opens up only once the one before it is done.
In Introw you build that path with two things you already use: segments and course enrollment . There's no separate sequencing engine to configure, and no enrollment list to maintain by hand.
Courses enroll partner contacts through segments, and segments are dynamic, membership is re-evaluated automatically as data changes. One of the conditions you can build a segment on is whether a contact completed a specific course .
Put those two together and your curriculum chains itself:
- Level 1 · New partners, condition e.g. role = Sales rep → enrolled in Introduction to Acme
- Level 2 · Basic sales, condition completed course = Introduction to Acme → enrolled in Basic Sales Training
- Level 3 · Advanced sales, condition completed course = Basic Sales Training → enrolled in Advanced Sales Training
The moment a contact finishes Introduction to Acme, they join the Level 2 segment and Basic Sales Training appears in their portal. Finish that one, and Level 3 unlocks the same way. You don't touch anything.
Step 1: Create your courses
Go to Portal → Courses and build each course in the curriculum. Keep them as separate courses rather than modules of one course, that's what makes the sequencing possible.
Step 2: Create one segment per level
Go to Settings → Segments and create a partner contact segment with Dynamic enrollment for each level:
- Level 1, the entry point. Use whatever defines a new learner, e.g. phase = Onboarding or role = Sales rep .
- Level 2, condition: completed course is Introduction to Acme .
- Level 3, condition: completed course is Basic Sales Training .
Step 3: Assign each segment to its course
Open a course, click Configure (gear icon) and scroll to Enrollment settings . Select the segment that should be enrolled. Repeat for each course.
That's the whole setup. Three courses, three segments, three assignments.
💡 Introw Tip: Combine conditions to make a level more precise, for example completed course = Introduction to Acme AND role = Sales rep , so only sales contacts continue down the sales track while technical contacts follow their own path.
Partners only ever see the course they're ready for. The next one appears in their portal automatically when they complete the current one, so the curriculum feels like a path rather than a catalog.
Because segments are evaluated continuously, this works for partners who join later too, a contact added six months from now enters at Level 1 and moves through the exact same sequence, without anyone enrolling them.
- Add as many levels as you want. The pattern doesn't change: one segment per level, each conditioned on the previous course being completed.
- Attach a certificate to each course so partners get recognition at every step, not just at the end.
- Track where everyone is from the Enrolled tab on each course, or in partner analytics, a partner sitting in Level 2 for weeks is a nudge waiting to happen.
- Reuse the segments elsewhere. The same "completed Advanced Sales Training" segment can unlock a portal tab, an asset folder, or the ability to register deals.
- Partner training courses
- How to use Introw's course builder
- Enrolling partners into courses
- Show Introw course enrollments and certificates in HubSpot
- Show Introw course enrollments and certificates in Salesforce

---

## Connecting HubSpot to Introw
Source: https://support.introw.io/en/articles/9353646-connecting-hubspot-to-introw

### C onnect your HubSpot account
- Go to https://app.introw.io
- To get started, navigate to the Settings section of your navigation bar. From there, click on Integrations and click Connect on the HubSpot card
- Enter your HubSpot login and choose the correct HubSpot account you would like to link to Introw. After you choose the desired account, click on ' Allow access ' to proceed.
#### Authorize Introw to connect with your HubSpot
### Choose how you store your partners in HubSpot.
To be able to import partners from your CRM, we need to know how you store them. This can be done as either a company or as custom object. 
In this example: we store our partners as regular HubSpot companies.
### Find your partners in your HubSpot.
Once we know how you store your partners in your CRM, we will try to find them by identifying them based on filters. This way you can decide to only import for example your Reseller partners or Integration partners by using the filters. 
By default Introw will look for any companies with the type property set for Partner or Reseller.
### Configure your partner attribution
Choose which objects you link to your partners and how you attribute partners to those objects. 
In this example: we select the Deal and confirm that we attribute the deal object to partners via Custom properties using a property called Partner which is a dropdown list.
Introw will show which partner companies in your CRM are already linked to Introw and for which of them there are already properties linked. 
If nothing is linked yet, you can connect the partner company from your CRM that you want to use for deal* attribution by linking it to the appropriate property value.
Pro Tip: In case you don't have the property value created yet for your partners within your CRM, Introw will help you with this by clicking on manage property values. Introw will create the property value in HubSpot and link it to the right partner company.
### Attributing other HubSpot objects to partners
In Introw, you can configure how you link your partners in HubSpot to multiple objects like Deals , Leads , Tickets, etc.
You can follow the same flow as described above and identify which object you attribute to partners and how that attribution is done within your HubSpot account.
Example: linking HubSpot tickets to partners.
### Finish the configuration
Make sure to Finish the configuration so Introw can start gathering all the data from your CRM and setup all your partners in no time.
Once this is done, Introw will automatically create your lead, deal  or ticket pipelines for your specific partners and keep them up-to-date in real-time without leaving your partner portal.

- Link your HubSpot deals to Introw via custom properties
- Link your HubSpot deals to Introw via company associations
- Link your HubSpot deals to Introw via custom objects
- Introw workflow actions in HubSpot
- How to use Introw forms with HubSpot

---

## How to attribute revenue to partners in HubSpot?
Source: https://support.introw.io/en/articles/9357064-how-to-attribute-revenue-to-partners-in-hubspot

Already using Introw to share deals with partners? Attribution happens automatically through Introw. This article covers how to additionally track partner attribution inside HubSpot using native HubSpot properties, useful if you want to report on revenue directly within HubSpot.

There are three ways to attribute deals to partners within HubSpot. Each has different trade-offs depending on your HubSpot plan and reporting needs.
Create a custom deal property (e.g. "Partner") and populate it with your partner names. Works on all HubSpot plans but doesn't scale well with large partner programs.
Step 1, Go to Settings → Data management → Properties
Step 2, Create a new property with the following settings:
- Object type: Deal
- Group: Deal information
- Label: e.g. Partner
- Field type: Dropdown select (one partner per deal) or Multiple checkboxes (multiple partners)
Step 3, Add your partner names as property values, then add the property to your deal view to attribute partners directly from the deal record.
✅ Easy and fast set-up ✅ Possible with all HubSpot plans ❌ Not very scalable
Associate a partner company to a deal using a custom association label (e.g. partner sourced or partner influenced ). More scalable but requires a HubSpot plan that supports association labels.
Step 1, Go to Settings → Data management → Objects → Deals → Associations
Step 2, Create an association label:
- Objects: Deals-to-companies
- Label: partner sourced (and optionally partner influenced )
Step 3, On any deal, click + Add company and associate the partner company with the appropriate label.
✅ Easy and fast set-up ✅ Scalable ❌ Requires association labels (not available on all plans) ❌ Reporting on this in HubSpot is limited
Create a custom Partner object in HubSpot and associate it to deals. Best for larger partner programs that need robust reporting.
Step 1, Go to Settings → Data management → Objects → Custom objects
Step 2, Create a custom object:
- Object name (singular/plural): Partner
- Primary display property: Partner Name (Single-line text)
Step 3, Associate the partner company to the Partner object, then associate the Partner object to your deals. Optionally add association labels to differentiate partner sourced vs. partner influenced.
✅ Scalable ✅ Good for large partner programs ❌ Requires a HubSpot plan with custom objects ❌ More complex to set up
- Link your HubSpot deals to Introw via custom properties
- Link your HubSpot deals to Introw via company associations
- Link your HubSpot deals to Introw via custom objects
- Link partners to leads in HubSpot
- How to use Introw forms with HubSpot

---

## How to create a partner portal
Source: https://support.introw.io/en/articles/9357238-how-to-create-a-partner-portal

Creating a partner portal in Introw starts from the partner detail page. Each portal is built from an experience, a pre-configured template that defines the sections, forms, and pipelines your partner will see.

Step 1, Go to the partner detail page
Navigate to the partner you want to create a portal for.
Step 2, Click Apply experience
Introw offers default experiences with pre-built sections, forms, and pipelines so you don't have to start from scratch. Choose the experience that matches the partner type, for example, a lightweight one for new partners or a more advanced one for top-tier partners.
Step 3, Preview and confirm
Use View portal to see exactly what your partner will see before you invite them. Once you're happy with it, the portal is ready.
Introw tip: You can apply different experiences to different partners and switch them at any time, without losing any existing deal or activity history.
Next steps: Launch your partner portal →
- How to preview a partner portal?
- Partner performance dashboard
- Create a Partner portal experience
- What does “No portal yet" and "No deal embed yet” mean?
- What is Partner Connect?

---

## How to launch a partner portal
Source: https://support.introw.io/en/articles/9357441-how-to-launch-a-partner-portal

Once you have created a portal it would be great to invite your partner. In the top right corner you will see the option to invite them to their dedicated partner portal. 
You can limit the access for sharing your portal with your partner via the following options:
- Via Email Only selected people can access the portal based on their email address.
- Via Email domain This is Introw's default and the most recommended option for giving portal access. It gives you control over which email domains are allowed to access the portal while making it scalable as it only allows people with certain domains in the list to access the shared space. 
Once your partner clicks the link you've shared, they can easily access the partner portal using Single Sign-On (SSO) with our built-in login options via Google or Microsoft or your own partner SSO ( learn more ) . Alternatively, they can simply enter their email address to receive a verification email and log in securely.
Via verification email 
Introw's verification link will ensure that the person who inputs their email to visit the digital partnership space actually owns that email and can access the portal in a secure and frictionless manner. When a person adds their email, they will be sent an email to verify email ownership.
Introw remark The email of the partner has to match the email of the selected people that can join or have the same domain as the domain you whitelisted
### Invite your partners via Introw announcements
This video shows how you can leverage Introw's announcement feature to easily invite your partners to your new partner portal at scale and keep them engaged with an in-app message. 
- Launch your partner portal
- Partner Portal login
- Unlink or update an experience of your partner portal
- Enable Single-Sign-On for Partners
- Invite and manage partner portal users as a partner

---

## How to create a partner portal experience
Source: https://support.introw.io/en/articles/9358660-how-to-create-a-partner-portal-experience

What is the experience builder and how to use it? 
The experience builder creates the structure of your shared portal with your partner. This can be used across multiple shared partner portals so you can speed up the onboarding of your partners without spending too much time on configuration  Introw provides you with two default experiences ( Referral partnership and Reseller partnership ) that can be used as a starting block or inspiration.
It is not mandatory to use the Introw experiences and you can start your own custom experience from scratch!
- The default experience has tabs which you can see on top : Introduction, Deal pipeline, Documents,… you can drag and drop these tabs you can add new tabs you can change the width of the page via the tab settings or give every tab their unique name so it is easy for you partner to understand In case you want to hide certain tabs from partner users, we offer the option to limit the access on those tabs.  Learn more about tab based security
- you can drag and drop these tabs
- you can add new tabs
- you can change the width of the page via the tab settings
- or give every tab their unique name so it is easy for you partner to understand
- In case you want to hide certain tabs from partner users, we offer the option to limit the access on those tabs.  Learn more about tab based security
- Every tab can be filled with Sections which represent the content within a portal. Below a list of the most common sections that are present within a partner portal Shared pipeline Mutual action plan or task list Lead or deal form Product video's (embed your favourite video content via loom, vidyard, youtube, vimeo and so much more) Asset library section for marketing content, sales material, documents, co-branded content ( learn more ) and so much more..
- Shared pipeline
- Mutual action plan or task list
- Lead or deal form
- Product video's (embed your favourite video content via loom, vidyard, youtube, vimeo and so much more)
- Asset library section for marketing content, sales material, documents, co-branded content ( learn more )
- and so much more..
Check out this article if you want to learn more about sections
You can easily duplicate an experience
- This can be very convenient if you want to copy the structure of an experience but want to style it towards a certain segment or market where your partners are operating in. E.g. An experience for resellers in the EU vs an experience for resellers in EMEA and while the structure for both them would be the same, you might want to change the copy to match the culture or language of your partner etc.  Simply click on the 3 dots and select Duplicate
- Simply click on the 3 dots and select Duplicate
- How to create a partner portal
- Show commissions to your partners
- Embed tasks within your partner experience
- Create a Partner portal experience
- Multi-Currency: localise the partner portal experience

---

## Link your HubSpot deals to Introw via custom properties
Source: https://support.introw.io/en/articles/9361206-link-your-hubspot-deals-to-introw-via-custom-properties

Link your HubSpot deals to Introw via Custom properties
You prefer looking at a video instead of reading a text? ⬇️ This is for you.
You want to take your time and go through the steps in detail? Below you can find a detailed description of all the steps you need to take. 
Make sure you have connected your Introw account to the right HubSpot account. If not, please check out this article: connecting-hubspot-to-introw
Navigate to the Settings section of your navigation bar. Click on Integrations
#### Step 1
Choose how you store your partners in HubSpot.   In this example: we store our partners as regular HubSpot companies.
#### Step 2
Find your partners in your HubSpot. 
By default Introw will look for any companies with the type property set for Partner or Reseller.
#### Step 3
Choose which objects you link to your partners and how you attribute partners to those objects? 
We select Deals and attribute it to partners via Custom properties
In this example: we select the property " Partner " that is linked to the deal object in HubSpot.
Introw will show which partner companies in your CRM are already linked to Introw and for which of them there are already properties linked. 
If nothing is linked yet, you can connect the partner company from your CRM that you want to use for deal* attribution by linking it to the appropriate property value. 
*In this example: I want to link/attribute my partner company  "Facebook" from my CRM to the correct Partner property value "Meta" on a deal detail.
When you click Finish, we will automatically create all the relevant Introw partners. 
### Save time with Introw!
Every time you have a new partner, Introw will do the heavy lifting. 
=> All your CRM embedded sections related to Deals, Leads, Contacts, Companies, Tickets etc. will be kept in sync and be prefilled with the related partner data every time you add a new partner to Introw.
Check out the Introw magic  ✨ !

 
- Connecting HubSpot to Introw
- Link your HubSpot deals to Introw via company associations
- Link your HubSpot deals to Introw via custom objects
- Share a deal to partners via Introw's app card in HubSpot
- Linking deals to leads via Introw

---

## How to manage sections?
Source: https://support.introw.io/en/articles/9361509-how-to-manage-sections

In your experience you can add all kind of sections like introductions, tiers, goals, mutual action plans, deal pipelines, ticket pipelines etc.
These items are all called sections.
### How to add a section in your experience
- To add a section click on “+ Add Section”
- Select the preferred section you would like to add
- You can use the slash command / to add titles, text, tables,… Type /heading or /h1 , /h2 , or /h3 to choose the heading size you want. Use Markdown shortcuts, like # , ## , and ### to create the perfect section
- Type /heading or /h1 , /h2 , or /h3 to choose the heading size you want.
- Use Markdown shortcuts, like # , ## , and ### to create the perfect section
#### How to manage a section in your experience
Sections can have multiple actions within your experience
 Click on the 3 dots that appear in the top left corner when you hover over the title of your section to access them 
Section action
Result
Sync section
Add this section to your synced sections so you can use it across all your portals
Rename section
Simply rename the section
Move section
If you made a mistake on where to put certain sections, you can move a section from one tab to another so you don't need to recreate it.
Hide in shared view
This hides the section in the portal for your partner but allows you to still see it.
Enable editing by partner
In case you want your partner to edit your section you can allow them to.
Duplicate
Simply duplicate the section to easily re-use again
- What are rich sections?
- What are synced sections?
- How to personalize your partner portal?
- Partner profile section
- Create and manage pipeline views in the portal experience builder

---

## Best practices for a good partner experience
Source: https://support.introw.io/en/articles/9361984-best-practices-for-a-good-partner-experience

#### Partner experience example
Check out the video below how a partner will experience the partner portal.
### Learn how to build this by yourself
##### Smart introduction
Automatically personalize the introduction by displaying the assigned partnership manager to each partner when they log in.
##### Smart partner profile section
The Partner Profile section allows you to display and manage partner information directly inside your partner portal. Learn more
#### Make it easy for partners to reach you
Embedding your meeting links within your portal offers your partner an easy way to get in contact with you or the necessary person. Make sure to add the meeting link to your team members detail page so it can be used within the portal of their partners within the dynamic introduction section. 
You can also embed the full meeting link if you want by adding a Meeting section. 
#### Dynamic Variables
Using variables in your experience builder is a great way to personalize your portal at scale. Variables can be added by using the { key on your keyboard or entering a / and simply select dynamic variables and the option you want and it will be placed into your partner experience: e.g. Partner First name 
#### Your Brand, Your Portal
Shape every section by applying your branding. Embedding your marketing materials like banners, background, header colours, and ensuring partners stay immersed in your brand identity.
- Header color : Sets the background of the top navigation bar in the partner portal.
- Background color : Defines the main portal’s overall background.
- Button color : Applies to all primary call-to-action buttons.
- Button text color : The text inside primary call-to-action buttons. Be sure to choose a color that contrasts with the button for readability.
- Active tab color : Highlights the tab currently in use within the partner portal.
#### Add a custom font
Custom fonts help reinforce your brand and create a consistent look across your partner portal and other brand touchpoints. This feature is available on the Pro plan.
You can upload a variable font file (TTF), and Introw will apply it across partner-facing experiences, including the portal, announcements, certificates, and email notifications. We recommend choosing a font that aligns with your brand guidelines and includes appropriate fallbacks for accessibility and readability. 
##### What Is a Variable Font?
A variable font is a single font file that supports multiple styles - such as different weights or widths - without needing separate files for each. Variable fonts are part of the OpenType standard and are supported by most modern browsers and operating systems.
Personalize your portal’s look and feel by selecting custom text colors and fonts, ensuring every word aligns with your brand’s style. 
#### Keep your Partners aligned
Keeping your partners focused with Introw's task section. This is a smart section that will be prefilled within the partner portal including the tasks for that specific partner. 
#### Elevate your content’s appearance
Learn how to enhance your content by resizing images, adding colors, and formatting elements to make it visually appealing and engaging. 
For some content in your Introw portal it would be nicer for you and your partners to see it in a more expanded view or even in full page mode. We offer this functionality on the tab level by clicking the 3 dots on the tab.
- select layout and choose Centered Expanded Full width (best used for deal pipelines)*
- Centered
- Expanded
- Full width (best used for deal pipelines)*
Full Width Layout This layout gives you maximum horizontal space but does not include navigation . If you add multiple sections, users will need to scroll through the page. Best suited for single, wide views like deal pipelines
Use the section area to its full potential by maximising your content within a specific section. This will eliminate the white borders around your content. 
Section Backgrounds Tailor each section of your partner portal with custom background colors or images, creating a cohesive look that reflects your brand across every widget.   The ideal aspect ratio:
- 3:1 (landscape)
- Example dimensions 1536×512, 1920×640, 3000×1000 Display width: Up to ~960px (centered layout)or full tab width on FULL layout Height: Width ÷ 3 at 3:1 (e.g. ~320px tall at 960px wide)
- 1536×512, 1920×640, 3000×1000
- Display width: Up to ~960px (centered layout)or full tab width on FULL layout
- Height: Width ÷ 3 at 3:1 (e.g. ~320px tall at 960px wide)
#### Organize your content with ease
Create structure within your portal by simply dividing the section in up to 8 equal parts or you can manually resize the content to your liking 
Simplify and make your content more digestible by applying tab restrictions based on partner roles. Not all partner users need access to the full range of content - this ensures that only relevant content is visible to specific partner contacts, preventing information overload and keeping the experience focused and manageable.  Learn more about role based access control 
As example below: a regular partner contact will only see the tabs that have no role restrictions applied to them to keep it easy and not overwhelming. 
#### Brand your partner portal
Customise the partner portal to reflect your company’s branding, including logos, colours, and messaging to improve the partner’s experience! 

- How to personalize your partner portal?
- Brand your Introw partner portal
- Create a Partner portal experience
- Unlink or update an experience of your partner portal
- 13 little Introw tricks you probably didn't know about

---

## What are rich sections?
Source: https://support.introw.io/en/articles/9362193-what-are-rich-sections

### What are rich sections?
Every partner portal is based on a certain experience and the experience builder contains the sections or building blocks on how you would like your partner portal to look like and what your partners can do in their dedicated partner portal. 
 Rich Sections are curated, predefined content blocks that let you quickly add visually engaging and structured elements, such as banners, CTAs, images, or text, to the partner portal, making it easy to highlight key information and enhance the user experience.
##### Introduction section
A section that will contain a small introduction text to your partners accompanied by your profile info. 
##### Banner
Banners are full-width hero images most commonly placed at the top of the partner portal page, primarily used for branding and visual impact. 
The ideal aspect ratio:
- 3:1 (landscape)
- Example dimensions 1536×512, 1920×640, 3000×1000 Display width: Up to ~960px (centered layout)or full tab width on FULL layout Height: Width ÷ 3 at 3:1 (e.g. ~320px tall at 960px wide) 
- 1536×512, 1920×640, 3000×1000
- Display width: Up to ~960px (centered layout)or full tab width on FULL layout
- Height: Width ÷ 3 at 3:1 (e.g. ~320px tall at 960px wide) 
##### Product overview
A section that can be used to showcase your different products or features towards all of your partners.
##### Mutual action plan
A section that is used to engage collaboration and to create accountability between you and your partner. Simply create your tasks and assign them with a date and owner so you have a good overview on what the action points are and where you or your partner needs to focus on. 

##### Call to Action
The Call to Action (CTA) Button section allows you to add customizable buttons to your partner portal that help guide users to key actions or destinations. These buttons can be configured to redirect partners to other tabs within the partner portal, open forms like deal registration, or open links to external resources, making it easy to streamline navigation and drive engagement where it matters most.
##### Collapsible content
The collapsible content section is often used as for a Frequently Asked Questions (FAQ) section. Example: It can give a clear overview on common questions and answers without cluttering the partner experience.
##### People
A section used to inform your partners on who the key stakeholders are in the your organisation regarding partners. 
##### Table
A table can be added within a section to show case information in a structured manner.
- How to create a partner portal experience
- How to manage sections?
- Best practices for a good partner experience
- What are synced sections?
- Embed tasks within your partner experience

---

## How to setup shared sales pipelines
Source: https://support.introw.io/en/articles/9362774-how-to-setup-shared-sales-pipelines

The best way of engaging with your partners is by going over a shared sales pipeline.
Introw offers the functionality to create shared pipelines for Deals, Leads, Contacts, Companies and even support tickets all synced from your connected CRM.
Example of shared deal pipeline.
### Manage multiple deal pipelines with ease
With Introw , you can create and share multiple pipelines directly in your partner portal, giving your partners a clear view of every deal type and stage. Whether you’re managing new opportunities , upsells , renewals , or onboarding processes , each pipeline can be customized and displayed to suit your collaboration needs. This flexibility makes it easy to keep partners aligned, build trust through transparency, and streamline how deals progress across different workflows. 
Go to Experience builder and start setting it up right now! 
#### Step 1: Click Add section
Select your CRm (in this case Hubspot is linked) and choose the desired object for creating a shared pipeline. In this article we discuss the shared deal* pipeline.
#### Step 2: Select your pipeline
Select the pipeline from your CRM that you want to use. 
#### Step 3: Configure your pipeline stages
Configure the stages you want to show or hide from the pipeline view . You can also rename them in case you don't want to share the internal channel name to your partners. In case you hide certain stages, deals within those stages are no longer visible or selectable when partners when to update a certain deal.
#### Step 4: Set your filters
💡 Introw tip : make sure the linked partner association or property is selected in your filters to see the real magic
Once your CRM is connected and you have defined which objects you link to your partner, Introw will automatically set the right association or property filter so your Partner will only see their deals*. 
#### Step 5: Configure views
In the Configure views step, you can define how deals are displayed for your partners. Choose which default views are available, adjust filtering and remove any views that aren’t relevant. This helps ensure your partners see a clean, focused deal overview that aligns with how they work and makes it easier for them to track progress at a glance.
#### Step 6: Configure the properties
In the Configure properties settings, you can control which deal properties are visible to your partners and how they are shared . Rename, hide, or reorder properties to tailor the deal view to your partner’s needs.
For each property, decide whether it should appear as a header, be sortable (ascending or descending), remain editable by partners , or be hidden entirely by selecting don’t share property .
For any CRM object fields such as deal stage, close date, or amount, enable notifications so partners are alerted immediately when changes occur . Notifications are sent for updates made both in Introw and directly in your CRM, ensuring partners can act quickly on important changes without needing to constantly check for updates.
This keeps deals moving forward, reduces manual follow-ups, and ensures everyone stays aligned on the most critical information.

Choose the header of the deal card
By default Introw shows the Primary account linked to the deal as the card header which is most commonly the end customer you and your partner are working with. But you can change this to another property in case you want to have the deal name for example to be the card header.  Card configuration example
Choose the aggregation property
You can now select which property from your CRM is used as the aggregation metric on the shared pipeline. This is the total shown at the top of each pipeline view, summed across the deals your partner can see.
By default Introw uses the deal amount , but you can point it at any currency property instead. Pick the same field you report on internally and the totals your partners see will line up with the rest of your reporting, so everyone is working from the same numbers.
#### Step 7: Set your collaboration options
Use the configuration cards to control what your partners can see and edit on each deal. These cards make it quick to grant the right visibility and editing permissions, so partners have the info they need without exposing sensitive data. 
Contact visibility: Let partners view the related contacts from your CRM.
- Show related contacts
- Include phone numbers (GDPR)
- Allow to create new contacts on the deal.
Quotes & Line Items : Configure quote and line item permissions for partners.
- Show and allow line item editing
- Show and allow quote creation
When you allow partners to create a quote, define these key steps to ensure it’s accurate and enforceable. 
- Choose a template: Select the quote layout from your CRM that you want partners to use.
- Require a signature: Decide if the partner or customer must sign before the quote is finalized.
- Set payment method: Specify how payments will be collected to streamline processing.
- Set expiration lock date: Define when the quote expires as after this date, partners won’t be able to make any changes.
#### Step 8: New deal registration
Link your Introw form if you want your partners to create a new deal* directly from the shared pipeline.
Introw will show a create button on the shared pipeline once a form is linked. 
#### Last step: Make sure you save the pipeline section.
Finally, save your changes to the shared pipeline and publish the experience to ensure all linked partner portals are updated.
- Collaborate on a deal or any other CRM object
- Configure which deal properties to share with your partner
- Enable Quotes & Line Items in your shared deal pipeline
- Allow partners to create quotes (CPQ)
- What is Partner Connect?

---

## Troubleshoot HubSpot connection
Source: https://support.introw.io/en/articles/9367758-troubleshoot-hubspot-connection

Couldn't complete the connection
Authorization failed because you don't have permissions to authorize the scopes required by the app. Please contact your super admin to get the necessary permissions.
Follow the next steps to this resolved
- Click the ⚙️ icon on the top right
- Go to Users and Teams
- Click on your name (you should be Admin or Super admin ) + go to Access
- Click on Change Seat and make sure the user has a seat selected . Sales enterprise or Service enterprise or Sales professional Seat
5. Click Save
- Connecting HubSpot to Introw
- Connect your CRM
- Show Introw course enrollments and certificates in HubSpot
- Validate your Partner Connect Card
- Using Introw with Gemini via MCP

---

## What are synced sections?
Source: https://support.introw.io/en/articles/9367912-what-are-synced-sections

What is a synced section? 
A synced section is a reusable content block that can be shared across multiple partner portals and updated from one central place. While experiences are ideal for segmenting partners , by region (e.g. English or French) or partner type (e.g. reseller, distributor, agency), synced sections are perfect for universal content that stays the same across all segments. Think of brand guidelines , pricing sheets , onboarding instructions , or co-marketing materials . When you update a synced section, the changes automatically appear in every partner portal where it's used, saving you time and ensuring consistency across your entire ecosystem.
How to create a synced section? 
Option 1 : Hover over a section in your experience and choose " Sync " to save it as a synced section and give it a clear name.
Option 2 : go to synced settings in the navigation bar  and click " Create section "
Choose what type of section you want to include and save your synced section. 
How to use a synced section? 
When configuring your portal experience, you have the option to insert a previously created synced section. This not only streamlines the setup process but also ensures consistency in structure and content across all your partner experiences. 

How to update a synced section?
When you click on a synced section you can replace the content and publish this so it updates the content across all your experiences
and partner portals (based on the experiences) that are using that synced section. 
 
- How to manage sections?
- Asset library
- Managing partner contacts
- Partner profile section
- Segment use cases

---

## How to preview a partner portal?
Source: https://support.introw.io/en/articles/9368411-how-to-preview-a-partner-portal

When you're using the Experience Builder to add content or edit sections, you might want to see how it looks from your partner's perspective. Introw makes this easy with a preview feature. Simply publish your latest changes, then click Preview to view the portal as your partners would see it. 
- Go to the top right corner and select Preview , then choose the partner whose experience you want to view.
- On your partner overview you can instantly checkout the portal that your partner is experiencing by clicking on the 👁️ icon .  This action will open a new tab in your browser with a view of how your partner will experience Introw.
- You can go back to the editor of your partner experience by clicking ✏️ Edit
- How to create a partner portal
- Launch your partner portal
- Create partner portal from within HubSpot
- Create a Partner portal experience
- Unlink or update an experience of your partner portal

---

## Launch your partner portal
Source: https://support.introw.io/en/articles/9399620-launch-your-partner-portal

Introw offers a clear overview of who of your partners can access the portal and an easy way to give new contacts access or remove access from partner contacts you would rather not give access.
Take control of the roll-out of your partner portal and start nudging those partners!
#### Invite your partner
On a partner detail, in the top right corner you can select to "invite" your partner to their portal. 
#### Define the access and select your partner contacts
Choose the access settings for your partner contacts to access their partner portal and portal.
- Via Email Only selected people can access the portal based on their email address.
- Via Email domain This is Introw's default and the most recommended option for giving portal access. It gives you control over which email domains are allowed to access the portal while making it scalable as it only allows people with certain domains in the list to access the shared space.
Make sure to select the partner contacts you want to give access to their new partner portal and click Next. 
#### Set the default notification settings
Choose the default notification settings for your partner contacts to receive. These default settings can be customized later at the individual contact level but provide a consistent starting point for managing partner updates on auto-pilot. 
You have the flexibility to grant partners access to their partner portal either by sending an invitation email or by enabling access without sending one. 
When you choose to send an invitation email, you can personalize the message included - adding context or a warm welcome to guide your partner into their portal experience. This is a great way to provide instructions, share onboarding resources, or simply add a personal touch. 
Your partner will receive an email invitation to access their portal and get started. 
If you prefer not to send an invitation email you can choose to " give access without email ". This way partners can still access the portal by entering their email on the portal login page and completing the verification flow. This is useful when migrating partners to Introw from another system, or when you want to enable access in bulk without overwhelming their inboxes.
Learn more on how partners will login into your shared space
- How to create a partner portal
- How to launch a partner portal
- How to invite Partners to your portal via Introw
- Partner Engagement Tracking
- Invite and manage partner portal users as a partner

---

## How to manage form submissions?
Source: https://support.introw.io/en/articles/9399649-how-to-manage-form-submissions

When you have enabled the setting " Require manual acceptance to proceed " on the form automation you will get notified by e-mail that a form has been submitted and you can find them in your navigation under Form submissions
- Go to Form submissions in your side navigation 
- Select the pending form submission and click Decline or Accept
Declined a submission by mistake? A decline isn't final, open the declined submission and click Reopen to move it back to pending, so it can be reviewed and accepted again.
### Multi-step approval
Submissions can be routed through multiple approvers in sequence. Each step must be approved before the next approver is notified, giving you full control over review order while keeping every decision visible in the form activity timeline.
- Configure approval steps on the form's automation step.
- Each approver only sees the submission once all previous steps have been accepted.
- A decline at any step stops the workflow and notifies the partner, later approvers don't need to weigh in.
- Every accept and decline is logged in the form activity timeline so you can trace how a submission moved through the chain.
### AI pre-check before human approval
You can add an AI pre-check step before any human approver. The AI reviews the submission against your acceptance criteria and gives the reviewer:
- A clear recommendation (accept or decline) with the reasoning behind it.
- Suggested partner-ready communication the approver can send as-is or tweak before replying.
The human approver always makes the final call, the AI step simply gives them context up front so reviews are faster and more consistent. AI pre-check works on every step that comes before a human approval, including in multi-step approval chains.
### Duplicate detection and enrichment
Introw will check for records within your CRM to avoid duplication of companies and contacts. We will not create a new contact based on the exact match with an e-mail address in your CRM and not create a new company based on the domainname. 
In case there is more information provided by the partner, that seems to be missing within your CRM, we will enrich the data properties with this info.  Ex. If you request your partner to provide an email-address and phone number for a lead that the share and Introw detects there is an exact match for the email but the phone number is not filled in your CRM, we will use the data from the partner and enrich this value in your CRM.
### Form activity
You can collaborate with your partner on their submitted forms and see all historical events on this form submission like comments and acceptance. 

Example of the mail you will get on a form submission.
- How partner deal data syncs to your CRM
- How to use Introw forms
- How to set up a partner application form
- AI-assisted form approvals
- Introw's submission agent is now fully autonomous

---

## How partner deal data syncs to your CRM
Source: https://support.introw.io/en/articles/9399679-how-partner-deal-data-syncs-to-your-crm

Introw offers to map and automate the data entries from the form submissions into your CRM so you can have clean and updated information on all your companies, deals, contacts, etc.
- Go to Portal > Forms
- Select the form you would like to automate
- Link the form fields to your preferred CRM objects in the CRM mapping column 
- Introw will show the icon of your linked CRM (Hubspot, Salesforce, etc.) in to the input field to indicate that it is mapped .
When a partner shares a deal with you via the Introw form either directly from the portal or through off-portal collaboration ( learn more here ), the deal is automatically attributed to them using the method configured in your CRM integration.
This could be through a custom property, association label, relational tables or custom objects all synced from your CRM.
- Go to the “Automation” tab This is where you can create rules to automatically push data from your forms into your CRM.
- This is where you can create rules to automatically push data from your forms into your CRM.
- Click “Add automation” Select the CRM property you want to automate. Example: “Create deal” automation.
- Select the CRM property you want to automate.
- Example: “Create deal” automation.
- Attribution (partner assignment) When a partner shares a deal via the Introw form (either directly from the portal or through off-portal collaboration), the deal is automatically linked or attributed to them. Attribution can be set based on the the attribution methods configured and synced from your CRM integration: Could be a custom property Association label Relational tables Custom objects
- When a partner shares a deal via the Introw form (either directly from the portal or through off-portal collaboration), the deal is automatically linked or attributed to them.
- Attribution can be set based on the the attribution methods configured and synced from your CRM integration: Could be a custom property Association label Relational tables Custom objects
- Could be a custom property
- Association label
- Relational tables
- Custom objects
- Choose the form field Pick the CRM property that should be filled with the value from the input field in your form.
- Pick the CRM property that should be filled with the value from the input field in your form.
- Choose default values (optional) Set a fixed value that should always be pushed to your CRM property if no value is provided in the form. Example: “Sales Pipeline” for the pipeline of a new deal. 
- Set a fixed value that should always be pushed to your CRM property if no value is provided in the form.
- Example: “Sales Pipeline” for the pipeline of a new deal. 
- Set the write mode for each field Fill in if not known: Only fills the CRM property if it’s currently empty (enrichment). Example: Add a country value only if the CRM record doesn’t already have one. Overwrite: Always updates the CRM property with the new value from the form, replacing whatever is already there.
- Fill in if not known: Only fills the CRM property if it’s currently empty (enrichment). Example: Add a country value only if the CRM record doesn’t already have one.
- Example: Add a country value only if the CRM record doesn’t already have one.
- Overwrite: Always updates the CRM property with the new value from the form, replacing whatever is already there.
### Relative-date default values
For date properties, default values can be set relative to the form submission date, the approval date, or another date field on the form, instead of as fixed calendar dates. The value automatically aligns with each submission's lifecycle, so your CRM data stays consistent without you having to update the form every time.
- Example, approval-relative: Set Close date to default to 30 days after the form is approved . Every approved submission lands in your CRM with a close date aligned to its own approval moment. 
- Example, field-relative: Take the partner's selected Kick-off date on the form and add 14 days on top to populate a follow-up date. 
- Combine with Fill in if not known to only apply the relative default when the partner didn't provide a value, or with Overwrite to enforce it on every submission.
💡 Introw Tip : When used alongside multi-step approval , the approval-relative date is calculated from the moment the submission is fully approved.
If you'd like to review submissions before any data is pushed to your CRM, enable Require manual acceptance to proceed on the form's automation step. The submission lands in Form submissions as pending, and only once it's approved, by a single approver, a multi-step chain, or with an optional AI pre-check, does Introw run the configured automations and create or update records in your CRM.
For the full setup and reviewer flow, see Form approval workflows and How to manage form submissions .
You can also enhance the Introw form with additional automation steps to create any object you need, such as contacts, companies, notes, tickets or custom objects, and link them to the appropriate partner when required. 

- How to use Introw forms
- Tracking Partner involvement on deals
- Automatically attribute resellers and distributors in two-tier channel deals
- Linking deals to leads via Introw
- How to set up a partner application form

---

## Asset library
Source: https://support.introw.io/en/articles/9414557-asset-library

Every partnership team struggles with asset management. It's hard for marketing to share content with the right partners, nobody knows where to find the latest case study, pitch deck, or product update, and partnership managers end up sharing old or outdated files. It becomes a mess quickly.
Introw's Asset Library gives partnership teams one place to upload, organize, and share partner-facing content. Teams can upload videos, links, PDFs, and images and, in one click, find what they're looking for and share it with partners at scale by adding it to the right experience.
Assets can be organized into folders to keep your library structured and easy to navigate.
### Asset detail
Clicking on an asset opens the asset detail view. Here you can manage everything related to that specific asset. The asset detail shows who created the asset and when. This makes it easy to track ownership and spot outdated content that may need refreshing. 
#### Add a description
When you describe what an asset is and when to use it, the agent can match it to the right partner conversations and surface it at the right moment. The more context you give, the better it finds and recommends the asset.
#### Add a thumbnail
Upload a custom thumbnail to make assets easier to recognize at a glance, especially useful when partners browse the Asset Hub in their partner portal and there is no preview available like for specifc
#### Categories
Assign one or more categories to keep your library organized, for example Online marketing or Branding . Categories help your team filter and find assets quickly, and can be used to structure the Asset Hub view in the partner portal.
#### Access to assets
- Public Access : Anyone with the link can view the asset
- Portal Access : Only partner users with portal access can view this asset
- Restricted Access : Only a segment of partner users with portal access can view the asset
##### Public access
Assets can also be made publicly available, allowing partners to share them directly with prospects, no login required to view. When public sharing is not enabled, the asset is only accessible to the specific partner it's shared with, and login is enforced when the asset is opened outside the portal.
##### Restricted access
Control which partners can access an asset using smart audience filters based on CRM data synced with Introw. 
- Choose restriction access
- Add a segment for example ( learn more on segments ) Gold Partners → only Gold-tier partners can see this asset Partner Sales reps → only partner contact sales reps have access
- Gold Partners → only Gold-tier partners can see this asset
- Partner Sales reps → only partner contact sales reps have access
Partners and partner contacts who match the segment filter conditions will be able to see the asset in their portal. Partners who don't match will not.
You can combine multiple segments to target a specific segment like for example, Gold-tier resellers in a specific region. This makes it easy to manage content visibility at scale without manually assigning assets to individual partners.
💡 Tip: Smart asset filters are powered by CRM data synced to Introw. Make sure the relevant properties are set correctly on your partner record in your CRM for filters to work correctly.
### Engagement tracking
For each asset, you get a view of partner engagement, both inside the partner room and outside of it when an asset link is shared via email. Partners don't need to visit your partner portal for engagement to be tracked.
### History
Introw's asset library is built for data governance. Every change, renames, file replacements, access restriction updates, variant edits, is logged with the user and timestamp, and you can restore any previous version in one click. 
### Archiving assets
You have the option to archive assets instead of permanently deleting them. Archiving is a great way to clean up your asset library while keeping a safety net in case you need to bring something back.
How it works:
- When you archive an asset, you can provide a reason for archiving. This helps your team keep track of who changed what and why.
- Archived assets are moved to a dedicated Archived tab in the asset library, making it easy to find and review all archived content in one place.
- Archived assets will be automatically deleted after 90 days . Until then, they remain available for review or restoration.
- If you need an archived asset back, you can restore it at any time before the 90-day window expires, and it will reappear in your active library.
💡 Tip: Use archiving instead of deleting to maintain a clear audit trail. The archiving reason helps your team understand why an asset was removed and makes it easier to decide whether to restore it later.
### Sharing assets with partners
Once uploaded, assets can be added to partner portal experience in seconds. You can choose to embed your asset library in a partner experience using the Asset Hub smart section and use the smart asset filters to manage it at scale. Learn more here
Example how this can look towards your partners.  
- Manage your assets in the asset library
- Partner Asset Hub
- Creating Co-branded assets
- Share assets at scale
- Governance and versioning

---

## Engage your partners with comments and activity
Source: https://support.introw.io/en/articles/9436438-engage-your-partners-with-comments-and-activity

The Activity panel in Introw gives you and your partners a shared, real-time view of everything happening across the partnership, from portal visits to deal updates to comments. Click Activity in the top right corner of any partner portal to open it.

Every time a partner or one of their contacts visits the portal, it's tracked automatically. Visit data is only visible to you, not to the partner.
The assigned partner manager receives an email notification each time a partner visits.
Note: Introw batches comment emails and sends them every 2 hours to avoid inbox overload for your partners.
Mentions
Use the @-symbol to mention any related contact of the partner. Mentioned users receive an email notification immediately.
Comments
You and your partner can comment on any shared CRM object (deals, leads, companies, tickets), tasks, form submissions, and within the portal itself. All comments sync to your CRM automatically.
The deal activity feed shows you what progress your partner is making, and gives your partner full transparency into how you're moving their deals forward.
Partner managers, the primary partner contact, and all enabled partner contacts with notifications on will receive an email when a deal update occurs.
Introw tracks the following deal events:
- Deal or CRM object updates, when a tracked property like deal amount or close date is updated
- New CRM object added, when a deal, company, contact, or ticket is added to the portal
- Deal closed won, when a deal moves to Closed Won
- Deal comments, comments left by either side on a shared deal
- Partner Engagement Tracking
- Partner activity events in your HubSpot timeline
- Partner notifications
- Off-portal collaboration in Introw
- What is Partner Connect?

---

## How to create a workflow in HubSpot based on the leads created via Introw?
Source: https://support.introw.io/en/articles/9439622-how-to-create-a-workflow-in-hubspot-based-on-the-leads-created-via-introw

Whenever an object like a contact, lead or deal  is created in your HubSpot  account via Introw it will be marked by Hubspot with a property “Record source detail” = “Introw”.  
Within the HubSpot workflow builder you can use this property to build out your desired workflow.
 For example : you want to set the contact owner automatically based on the country of the created contact via Introw. 

- Link your HubSpot deals to Introw via custom properties
- Link your HubSpot deals to Introw via company associations
- Introw workflow actions in HubSpot
- Automating workflow actions in HubSpot using Introw App events
- How to use Introw forms with HubSpot

---

## Introw product update - May 2024
Source: https://support.introw.io/en/articles/9440109-introw-product-update-may-2024

💡 Find out about our latest product changes from May 2024 as we continue improving Introw to help you collaborate with your partners. 
### New layout 🖥️
When working with your partner on a shared deal pipeline or showing a marketing video or presentation, you can now choose which tab of your portal to expand for a wider view.
### Preview portal 👁️
We are happy to announce that we now offer the function to preview your partner portal so you can get the same experience as your partner.
### Improved top navigation 🍞
You might have noticed that on the top of your screen we have added so called "breadcrumbs". A technical term used to show where you are within the application.
Example: Partner > Microsoft >
You can easily go back to the partner detail of Microsoft by clicking on "Microsoft"
### New helpcenter 🆘
With the launch of Introw 2.0, we also like to introduce our help center to help you and your partners find the answers to all your questions.
### Extra new: Custom domain
We carefully listened to your feedback and noticed that the link sharing could be better. So we decided to create 1 custom domain for all your partners
Click on your avatar to see your domain!
Enjoy!
Effortless collaboration, every step of the way!
Team Introw
- Introw product update - October 2024
- Introw product update - May 2025
- Introw product update - June 2025
- Introw product update - August 2025
- Introw product update - November 2025

---

## Slack - Link private channels🔒
Source: https://support.introw.io/en/articles/9449132-slack-link-private-channels

To use private channels with the integration for Slack , you must go into each private channel in Slack and add the Introw.io app.  A private channel in Slack is shown with a 🔒 icon, for further instructions on how to add the app to a private channel, read on!
 Step 1 
Go to your Slack account and open the private channel that you would like to use with the integration. Click on the channel name to open the channel detail or click on the 3 dots in the top right corner - " open channel details " . From there, click on the " Integrations " tab and select " Add an App " 
##### Step 2
Search for "Introw" to locate the Introw app. Click "Add" to add the Introw app to your private channel. 
The Introw App will be added to the private Slack channel which allows you to link the channel to a partnership portal within Introw.
Note: You must repeat this process for each private channel that you would like to use with the integration for Slack.
##### Step 3
Go to your Introw account Navigate to Settings > Integrations and click on the integration with Slack. Here you can link the private channel to your partner portal. 
##### Step 4
Choose which internal notifications you want to receive in your connected Slack channels. 
##### Troubleshooting
If you still aren't able to add the private channel to your integration recipe, you'll need to remove Introw from Slack and then re-authenticate. Please check out this article for instructions on how to remove an app or customer integration from Slack. Once you've removed the app, follow the steps to set up the integration and/or add the app again. 
- How does the integration with Slack work?
- AI detected channel conflict resolution
- Introw's AI Agent in Slack
- How does the integration with Microsoft Teams work?
- Microsoft Teams - Link private and shared channels🔒

---

## Best practices to activate your partners via Introw
Source: https://support.introw.io/en/articles/9460002-best-practices-to-activate-your-partners-via-introw

Getting partners to adopt a new tool takes more than just sending an invite. These practices will help you reduce friction, drive engagement, and keep things moving from day one.

Every Introw workspace has a dedicated URL: yourcompany.introw.io . Share this in your onboarding email, partner welcome message, and any ongoing communications.
- Partners access their portal through one simple link, no separate logins or multiple URLs to track
- Your team can distribute it consistently across all partner touchpoints
Best practice: Include your dedicated URL in every partner communication, from the first onboarding email to ongoing check-ins.
Introw's shared space centralizes all partner activities, deals, tasks, documents, and forms, in one place both sides can see.
- Both you and your partner see deal updates in real time, keeping everyone accountable
- The shared space replaces scattered emails and spreadsheets with one clear view of the partnership
Best practice: Keep your marketing and sales content up to date in the shared space so partners always have the latest materials at hand.
Configure Introw to automatically notify you and your partners whenever there's a change on a shared deal, stage updates, close date changes, new deals added, and more.
- Partners stay informed without needing to check in manually
- If a deal goes quiet for a defined period, a re-engagement notification can be triggered automatically
Best practice: Add a shared pipeline to the partner experience and enable deal notifications so partners are activated automatically when activity happens.
- Create new partners via Introw
- Share a deal to partners via Introw's app card in HubSpot
- Give your partners their own AI assistant to collaborate in real time via Introw's Partner MCP
- Using Introw with Gemini via MCP
- The Introw-Powered Partner: A Day in the Life

---

## Link your HubSpot deals to Introw via company associations
Source: https://support.introw.io/en/articles/9479462-link-your-hubspot-deals-to-introw-via-company-associations

Introw tip! In case you are not sure how your partners are linked to HubSpot, please check the following article !
You prefer looking at a video instead of reading a text? ⬇️ This is for you
You want to take your time and go through the steps in detail?
Below you can find a detailed description of all the steps you need to take to link your HubSpot deals to Introw via Company associations. 
Make sure you have connected your Introw account to the right HubSpot account. If not, please check out this article: connecting-hubspot-to-introw 
Navigate to Settings > Integrations 
#### Step 1: How do you store your partners in HubSpot
Choose how you store your partners in HubSpot.
 In this example: we store our partners as regular HubSpot companies 
#### Step 2: Find your partners in your CRM
Introw will identify your partners from HubSpot based on the property type = partner or reseller.  In case you use a different configuration to identify a partner, simply adjust the filter.
#### Step 3: Select which objects you link with partners
Choose which object you link to your partners to attribute their influence. You can link deals, contacts, companies or tickets to your partners.  In this example we say that in our CRM we link our deals to our partner via a company association label called "Partner". 
#### Step 4: Click finish
Once you click finish, we will create all partners identified in step 2 and fetch all linked objects (deals in this case) related to them.  
### Save time with Introw!
Every time you have a new partner registered deal, lead or any other object, Introw will do the heavy lifting by creating the deal and correctly associating the partner company with the right label. 
=> All your CRM embedded sections related to Deals, Leads, Contacts, Companies, Tickets etc. will be kept in sync and be prefilled with the related partner data every time you add a new partner to Introw.
- Link your HubSpot deals to Introw via custom properties
- Link your HubSpot deals to Introw via custom objects
- Share a deal to partners via Introw's app card in HubSpot
- Introw workflow actions in HubSpot
- Linking deals to leads via Introw

---

## Link your HubSpot deals to Introw via custom objects
Source: https://support.introw.io/en/articles/9529396-link-your-hubspot-deals-to-introw-via-custom-objects

Introw tip! In case you are not sure how your partners are linked to HubSpot, please check the following article !
Below you can find a detailed description of all the steps you need to take to link your HubSpot deals to Introw via Custom objects. 
Make sure you have connected your Introw account to the right HubSpot account. If not, please check out this article: connecting-hubspot-to-introw
### Step 1
Navigate to the Settings section of your navigation bar. Click on Integrations
### Step 2
Choose how you store your partners in HubSpot.
 In this example: we store our partners as a custom object in  HubSpot called "Partner".
### Step 3
Choose how you attribute partners to your CRM objects.
In this example: we select Associations
### Step 4
Choose which objects you link with your custom object 
In this example: we select the deal object that we link to our custom object "Partner" via associations labels.
### Step 5
Which association label do you use to link a deal with your custom object?
In this example: we select the association label "Partner deal" that can be associated to our custom object
### Step 6
Introw will show which partners in your CRM are already linked to Introw and which objects are associated to it via a custom object. 
If nothing is linked yet -> Click on the 3 dots icon to create a partner in Introw or link to an existing one.

Save time with Introw!
Every time you have a new partner, Introw will do the heavy lifting. 
=> All your CRM embedded sections related to Deals, Leads, Contacts, Companies, Tickets etc. will be kept in sync and be prefilled with the related partner data every time you add a new partner to Introw.
Check out the Introw magic ✨ !
- Connecting HubSpot to Introw
- Link your HubSpot deals to Introw via custom properties
- Link your HubSpot deals to Introw via company associations
- Linking deals to leads via Introw
- How to use Introw forms with HubSpot

---

## How to personalize your partner portal?
Source: https://support.introw.io/en/articles/9556236-how-to-personalize-your-partner-portal

Personalization in Introw lets you tailor each partner's portal experience without creating a separate portal for every partner. Use dynamic sections and variables to automatically adapt content based on who's logged in.
#### Dynamic introduction
Add the Introduction rich section to your experience to automatically display the assigned partner manager's details, name, email, job title, and meeting link, to each partner when they log in.
Introw tip: Partner managers can add their meeting link from their profile (bottom left of the app). Admins can set it on the Teams page.
#### Dynamic variables
Add variables anywhere in your experience using the { command or use / and select Dynamic variables. Select the variable name from the list and it will be inserted into the template, for example, First name or Company name (your partner's company). 
When a partner visits their portal, Introw automatically fills in their information. You only need to set up the variable once in the experience, it applies to all portals linked to it.

#### Personalization at scale
Because variables and dynamic sections are set at the experience level, you don't need to update every portal individually. Update the experience once and every partner portal linked to it reflects the change automatically.
Introw tip: Combine personalization with segment-based access control to show or hide entire sections based on partner type, tier, or region.
- Best practices for a good partner experience
- Embed tasks within your partner experience
- Create a Partner portal experience
- How to embed a report or dashboard in your partner portal
- Partner team roles

---

## Show the Introw card inside HubSpot
Source: https://support.introw.io/en/articles/9600440-show-the-introw-card-inside-hubspot

The Introw Collaboration card gives you a command center for partner collaboration directly inside HubSpot, available on Deals, Companies, Tickets, and custom objects.

You need to add the Introw Collaboration card to each HubSpot object view separately. Follow these steps for Deals, Companies, and Tickets.
Step 1, Show the card on your HubSpot Deals
Step 2, Show the card on your HubSpot Companies
Step 3, Show the card on your HubSpot Tickets
Note: If you previously had an older version of the Introw card, remove it from the layout first and replace it with the new Introw Collaboration card through sidebar customization.
Once the card is added, you can share objects with partners, track their activity, leave comments, and manage tasks, all without leaving HubSpot.
- Link your HubSpot deals to Introw via company associations
- Collaborate from inside your HubSpot deals
- Share a deal to partners via Introw's app card in HubSpot
- Show Introw course enrollments and certificates in HubSpot
- How to use Introw forms with HubSpot

---

## Email verification
Source: https://support.introw.io/en/articles/9669389-email-verification

### How to login in Introw via our magic logic link
When your partner wants to access Introw will send them an email them with a magic login link to verify their email address. 
- Go to the shared URL of your partner portal Via your custom domain or your Introw portal URL: domain.introw.io
- Via your custom domain or your Introw portal URL: domain.introw.io
- Choose to login via Google or Microsoft or Enter your email address
- Select Login via email and Introw will send an email with a magic link to verify their email
- Click Go to shared space in the email and you get automatically redirected and logged into Introw.

Please note:
- Be sure to check your spam folder if you do not see the email in your regular inbox.
- The link will be invalidated once it is clicked or used in a browser preview.
- If the clicking link still does not work, you can copy and paste it directly into the web browser on your phone to be redirected.
- If you request a new email, all previous links are invalid. You must click the most recently sent link.
- How to launch a partner portal
- Partner Portal login
- Unlink or update an experience of your partner portal
- Enable Single-Sign-On for Partners
- Partner Connect: a 2-way CRM integration with HubSpot

---

## Partner performance dashboard
Source: https://support.introw.io/en/articles/9689534-partner-performance-dashboard

A Partner Performance dashboard gives your partners a live view of the metrics that matter, deals closed, pipeline contribution, revenue over time, engagement, and anything else you want to track. You build it in Introw using Reports & Dashboards and embed the result in your partner portal. Each partner automatically sees only their own data, no manual scoping, no exports, no stale numbers.
There are three steps:
- Create your reports
- Combine them into a dashboard
- Embed the dashboard in your partner portal
💡 Introw Tip: Any report or dashboard you embed is automatically scoped to the partner viewing the portal, the same dashboard works for every partner, and each one only ever sees their own numbers.
Each widget on your dashboard is a saved report. Build the individual metrics you want your partners to see, for example Total Revenue , Weighted Pipeline , Number of deals , Average deal size , Average sales cycle , or Revenue over time .
Reports can be built on CRM data (deals, opportunities, leads, tickets, …) or on Introw data (portal visits, engagement events, certifications, …), and support number, bar, line, and pie visualisations.
📘 Full step-by-step: How to create a report .
Create a new dashboard (e.g. Partner Performance Overview ), add the reports you just built as widgets, and arrange them in a layout that tells a clear story for your partners.
📘 Full step-by-step: How to create a dashboard .
In the Experience Builder , add a Dashboard section to your partner experience and pick your Partner Performance dashboard. Save and publish, each partner will now see a live version scoped entirely to their own data.
📘 Full step-by-step: How to embed a report or dashboard in your partner portal .
- How to create a partner portal
- What does “No portal yet" and "No deal embed yet” mean?
- How to create a dashboard?
- How to embed a report or dashboard in your partner portal
- What is Partner Connect?

---

## Collaborate on a deal or any other CRM object
Source: https://support.introw.io/en/articles/9826343-collaborate-on-a-deal-or-any-other-crm-object

When a deal or any other CRM object is shared with a partner in Introw, both sides can view it, update properties, leave comments, and stay notified, all in one shared workspace. Every change syncs back to your CRM automatically.
In the experience builder, open the deal pipeline embed and go to its configuration panel. For each CRM property, you can control exactly what your partner can do:
- View only, the partner can see the property value but cannot edit it
- Editable, the partner can update the value directly from their shared portal
- Notifications, the partner is automatically notified when that property changes
Note: Only properties that are editable in your CRM can be set to editable in Introw.
For example, you can allow a partner to edit the deal stage and close date. Any change they make in Introw syncs to your CRM immediately, no manual update needed on either side.
Introw tip: Start with a focused set of editable properties and expand from there. Giving partners edit access to too many fields at once can create friction and confusion.
### Line items
For reseller partners, you can also allow them to manage line items directly from the deal view. Partners can search your CRM product library by name or SKU, add products, and adjust quantities. All changes are logged in the deal's activity feed.
Notifications let partners stay on top of deal activity without needing to log in and check manually. You can configure exactly which property changes trigger a notification, per CRM embed, per partner experience.
To enable: in the experience builder, open the configuration panel of the pipeline embed. Select a property and toggle notifications on.
A 🔔 icon appears next to each tracked property. Any update to that property, whether made in Introw or directly in your CRM, automatically notifies the relevant partner contacts.
You can also manage all notification settings in one place from the Notifications tab within the pipeline section.
Introw tip: Enable notifications for high-signal properties like deal stage and close date. This keeps partners engaged without overwhelming them with every minor update.
### Slack notifications
If your workspace has Slack connected, partner notifications are also delivered directly to Slack. Partners receive a message when tracked deal events occur, such as a stage change, a new comment, or a deal being added to their portal.
- Configure which deal properties to share with your partner
- CRM User
- Keep deals moving with automatic partner notifications
- AI Deal Coach
- What is Partner Connect?

---

## Create partner portal from within HubSpot
Source: https://support.introw.io/en/articles/9882392-create-partner-portal-from-within-hubspot

If you have a new partner or an existing partner without an Introw partner portal, you can easily create one using the workflow builder or via the Introw Copilot in HubSpot.
### Via the HubSpot workflow builder
Use the Introw PRM workflow action to automate partner and partner portal creation without leaving HubSpot. This article will walk you through adding and configuring the Introw action inside a HubSpot workflow.
Here you can learn more on the Introw workflow action in the HubSpot workflow builder
### Via the Introw Copilot card
Remark -  In case you have not set the Copilot card on a company card, see here how to do this.
When the Introw Copilot card is set up in your record detail view in HubSpot, you’ll see a "Create partner portal" option. This allows you to create a partner portal in Introw directly for the company you're working on in your CRM.

- Create new partners via Introw
- Collaborate from inside HubSpot tickets
- Introw workflow actions in HubSpot
- Partner activity events in your HubSpot timeline
- Partner Connect: a 2-way CRM integration with HubSpot

---

## Introw product update - August  2024
Source: https://support.introw.io/en/articles/9883598-introw-product-update-august-2024

🆕 Allow partners to register deals from the pipeline view  Say goodbye to a separate view to register and track deals! Link your deal registration form to your pipeline allowing partners to register deals in one view. This can also be done for leads, contacts and support tickets - Learn how
PS: In this video we'll show you how you can leverage this new feature to collaborate on support tickets with your partners.
👬 Collaborate on form submissions  Start collaborating on form submissions and make sure the lead, deal or support ticket your partner is sending you contains all relevant information before you accept them.
- Introw product update - September 2024
- Introw product update - August 2025
- Introw product update - November 2025
- Introw Product update - January 2026
- Introw product update - March 2026

---

## How does the integration with Slack work?
Source: https://support.introw.io/en/articles/9911638-how-does-the-integration-with-slack-work

Get instant notifications on Slack when there are updates in your Introw partner portal and keep your partner collaboration at an all time high. All notifications on deal updates, form submissions, comments, mentions and task activity are pushed into your preferred Slack channel.
Check out this video below on how our integration with Slack keeps both you and your partners updated on deals, leads, tasks, etc.  instantly.
Follow the steps below to learn how ⬇️:
- Go to Integrations and click Connect
2. Click Allow when Introw requests for permissions 
3. Link your shared Slack channels to a partner portal. 
Remark: Link Introw to a private Slack channel
In case you don't see the private channels appear in the dropdown list, make sure to add the Introw app from the Slack directory to your private channel.
4. Choose which internal notifications you want to receive into your linked internal Slack channels. 
5. Choose which partner notifications you want to receive into your shared Slack channels
You can do this in the navigation panel: Engage > Notifications and enable/disable the notifications you want to receive in the shared Slack channels with your partners. 

Once you've done that, you're all set!
If anything went wrong along the way, please contact us at [email protected]
- Slack - Link private channels🔒
- Announcements
- Partner notifications
- Introw's AI Agent in Slack
- How does the integration with Microsoft Teams work?

---

## Allow partners to add attachments in HubSpot
Source: https://support.introw.io/en/articles/9939345-allow-partners-to-add-attachments-in-hubspot

When you are collaborating on a deal with a partner, all files that are uploaded on the deal in Introw are being pushed automatically to the attachment section on your deal in HubSpot. This to make sure all relevant data from your partner on the deal is captured within your CRM.
In this example Kelly Maine is a reseller partner of John and he asked her to upload the purchase order that was send to the end customer Wasabi.
Introw will push a note and add the uploaded file to the attachments card on the deal in your HubSpot account.  
- Connecting HubSpot to Introw
- Collaborate from inside your HubSpot deals
- Partner activity events in your HubSpot timeline
- How to use Introw forms with HubSpot
- Partner Connect: a 2-way CRM integration with HubSpot

---

## Configure the deal name of your partner deals.
Source: https://support.introw.io/en/articles/9939540-configure-the-deal-name-of-your-partner-deals

To make sure the deals registered by your partners follow a similar convention as the ones created by your sales team, we allow to choose how the deal name is created during the automatic creation of a deal in your CRM. 
How to set this up:
- Go to your form and choose Configuration
- Select the automation " Deal automation "
- Go to "Default fields" and select Deal Name as CRM property
- Configure how you want the deal name to be by combining free text with variables from your partner or form fields. E.g. "New deal - Company name (= name of the end customer company)" OR "Opportunity via {Partner} for {amount} licences"
- E.g. "New deal - Company name (= name of the end customer company)" OR "Opportunity via {Partner} for {amount} licences"
- Whenever your partners register deals, Introw will make sure the naming convention of the deal name is applied when creating the deal in your CRM.
- Configure the deal owner of your partner deals
- Configure which deal properties to share with your partner
- Tracking Partner involvement on deals
- AI agents that actually take action for your partners
- What is Partner Connect?