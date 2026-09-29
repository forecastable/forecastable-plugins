# Introw help center (support.introw.io), part 2 of 4

Verbatim text of every public help article, fetched 2026-09-29. Older than docs.introw.io; where they disagree, prefer docs.introw.io and the release notes.

## Introw workflow actions in HubSpot
Source: https://support.introw.io/en/articles/11537402-introw-workflow-actions-in-hubspot

Use the Introw PRM workflow action to automate partner and partner portal creation without leaving HubSpot. This article will walk you through adding and configuring the Introw action inside a HubSpot workflow.
💡 Introw Tip : Make sure your Introw account is connected to HubSpot.  Learn how to connect here
#### Step 1: Create a HubSpot workflow
- Navigate to Automation → Workflows in your HubSpot portal.
- Open an existing workflow or click Create workflow to start from scratch.
- Choose a relevant workflow type depending on your use case that would involve the company record in HubSpot. (e.g. an update on the company-object like setting the company type = partner)
#### Step 2: Add an Introw PRM Action
Inside your workflow, click + to add an action, then:
- Go to Integrated Apps
- Select Introw PRM
- Choose one of the available actions below 👇
#### Available Introw actions
Introw now supports 4 powerful workflow actions, giving you full automation coverage across the partner lifecycle.
##### 1. Create Partner
Trigger: A new company should be onboarded as a partner in Introw.
Automatically create a partner record in Introw when a HubSpot company meets your criteria (e.g., deal closed, company type updated).
Configuration
- Partner Name*: select the field of the CRM record that you want to map to your Introw partner company name.
- Partner Domain*: select the field of the CRM record that you want to map to your Introw partner domain.
- Optional settings Set the right partner experience Set the right partner manager Define the partner portal access level
- Set the right partner experience
- Set the right partner manager
- Define the partner portal access level
##### 2. Update Partner
Trigger: A partner's details have changed in HubSpot and need to stay in sync with Introw.
Keep partner data consistent across both platforms. Whenever a relevant company property changes in HubSpot, like tier, region, or assigned manager, this action automatically updates the corresponding partner record in Introw. 
Common use cases:
- Upgrading a partner to a new tier
- Re-assigning a partner manager
- Syncing updated company details after a rebrand
Configuration: Select the Introw partner fields you want to update like:
- Partner experience : upgrade your partner to a new portal experience with perhaps different content, other pipelines and so on.
- Partner tier: Upgrade your partner tier.
- Phase: Upgrade your partners phase within Introw
- Partner Manager : Assign a new partner manager to your partner in Introw
##### 3. Issue Certificate
Trigger: A partner has completed a program, training, or milestone.
Reward and recognize your partners by automatically issuing a certificate through Introw. This action can be tied to deal milestones, training completions, or any other trigger in your workflow.
- Issuing a completion certificate after a partner finishes onboarding
- Recognizing top-performing partners at the end of a quarter
- Certifying partners who complete a product training program
- Certificate : Select the certificate template to issue (required)
- Contact object ID : set a specific value ( contact record ID ) to grant a person the certificate or leave it blank in case you want all active partner portal contacts of the linked partner company get certified.
- Notify the recipient : Let Introw send out an email to the certified contact they are now certified ( learn more )
##### Enroll Partner in Journey
Trigger: A partner is ready to enter a structured onboarding or enablement journey.
Automatically enroll a partner in a predefined Introw journey, a curated sequence of steps, content, and milestones designed to guide partners through onboarding, enablement, or a new program launch. 
- Kicking off the onboarding journey as soon as a partner is created
- Enrolling partners in a new product launch journey after a deal milestone
- Starting a re-engagement journey for dormant partners
- Partner journey: Select the journey to enroll the partner in. 
#### Step 3: Review and Publish
Once your actions are configured:
- Click Review and publish to save your workflow.
- Use HubSpot's Test feature to simulate the workflow and confirm each Introw action fires correctly.
#### Extra automation ideas
You can extend your Introw-powered workflows with other HubSpot-native actions:
- 📣 Slack notification, Alert the company owner or your partnerships Slack channel when a partner is created or updated
- 📧 Email enrollment, Send a welcome email sequence when a partner is created
- 🏷️ Update CRM properties, Stamp a "Partner Created in Introw" date on the HubSpot company record for reporting
- How to create a workflow in HubSpot based on the leads created via Introw?
- Create partner portal from within HubSpot
- Partner activity events in your HubSpot timeline
- Automating workflow actions in HubSpot using Introw App events
- Show Introw course enrollments and certificates in HubSpot

---

## Partner Engagement Tracking
Source: https://support.introw.io/en/articles/11549276-partner-engagement-tracking

Introw helps you track your partner’s engagement both within and outside the partner portal, from deal registrations and asset views to announcement emails, automated notifications, and even AI agent conversations. 
Whether partners are submitting forms, reading your content, or asking questions through the AI assistant, their activity is tracked. This makes it easy to identify active partners, optimize your content or process, and follow up when needed. 
✅ Deal, lead registration via form submissions
Track when partners register a deal, lead, ticket or custom object through custom or default forms. This gives you visibility into who’s actively contributing to your pipeline. 
📄 Asset engagement
See which documents, decks, and resources partners engage with. You’ll know what content resonates and can optimize your portal accordingly. 
📣 Announcement email engagement
Monitor open and click rates for announcement emails sent via Introw. Understand which messages are landing and which may need improvement. 
✉️ Automated notification emails
Track engagement with automated emails such as deal updates or onboarding reminders. Ensure key communications are being received and read. 
💬 AI assistant conversations
Capture and review questions asked by partners to the built-in AI assistant. This gives insight into common support needs and where content or messaging might need clarification.  
### Form submissions
Track every time a partner submits a form, like for example:
- Deal registration forms
- Lead referral forms
- Partner application forms
- Request MDF forms
- etc.
Each submission is logged and tied to the relevant partner and submitter which can be done in-portal or outside the partner portal by using our embed form functionality or sharing a partner specific form link - more info here .  Engagement metrics will include the number of pending, accepted, and declined submissions. 
### Asset engagement
Understand which documents and materials partners are actually using by checking the asset engagement metrics.
Introw is able to track engagement on assets within and outside the partner portal and shows the following
- Engagement (views) across all assets and partners
- Views and clicks of specific assets
- Frequency of engagement per partner
### Automated email engagement
Any notification email sent through Introw like announcements, comments and including automated nudges and alerts on any CRM object like deal updates, ticket updates etc. are tracked for:
- Opens
- Clicks
- Follow-through on calls to action
This helps you monitor how partners respond to key touchpoints.
Example of a the engagement on automated email notifications to partners when a deal is closed won. 
### Announcement emails
If you use Introw’s announcement email feature to send updates, event invites, or new content alerts, you can track:
- Who opened the email
- Which links were clicked
- Overall engagement rates
This is a powerful way to measure interest and drive partner re-engagement directly from the platform.
### Introw AI Agent conversations
When a partner interacts with the Introw AI agent, we log the conversation and assess the outcome, whether it was positive (e.g. they found what they needed) or negative (e.g. they left without a clear answer). This gives you deeper insight into partner needs and helps you identify gaps in content or support.
All of this makes it easier to identify engaged partners, optimize your resources, and follow up when needed. 
### Partners missing out on engagement
Introw proactively alerts you when partners are missing out on key engagement by identifying those who haven’t accessed their partner portal yet. This ensures no valuable relationship goes unattended.
You’ll see clear indicators when a partner hasn’t been invited or hasn’t activated their access giving you the chance to follow up, invite them in, and start collaborating.
### Turn last activity into a segment
Tracking engagement is most useful when you can act on it in bulk rather than partner by partner. Because Introw records when each partner and partner contact was last active, you can turn that signal into a live segment, automatically grouping the partners leaning in right now (e.g. active in the last 7 days) and the ones going quiet (e.g. no activity for 30+ days).
The segments update in real time, so there's no digging through last quarter's data to work out whether a partner was active, a partner who re-engages drops out of the inactive group on their own, and you can target enablement, announcements, or a re-engagement nudge at exactly the right audience. See Segment use cases for the setup.
- Create a Partner portal experience
- Partner activity events in your HubSpot timeline
- Partner Analytics
- Partner engagement reporting in HubSpot with Introw app events
- Automating workflow actions in HubSpot using Introw App events

---

## Partner activity events in your HubSpot timeline
Source: https://support.introw.io/en/articles/11553678-partner-activity-events-in-your-hubspot-timeline

When a partner takes action in Introw, visiting their portal, submitting a form, viewing an asset, or updating a deal, Introw automatically pushes those events to the associated contact and company timeline in HubSpot.

The following partner actions appear in HubSpot, each with contextual details including who took the action, which partner it came from, and when it happened:
- Asset viewed
- Comment made
- Object updated (deal, lead, contact, company, ticket, ...)
- Deal closed won
- Form submitted
- Portal visited
Events appear in the timeline of the partner's company and contact records in HubSpot.
Introw tip: Make sure Introw PRM events are included in your HubSpot activity filters. Click the filter icon in the timeline and enable Introw PRM activity events .
As long as your HubSpot integration is connected in Introw, timeline events appear automatically for any partner company and contacts matched in your CRM. No additional setup needed.
Not connected yet? Set up your HubSpot integration →
Introw tip: Use these timeline events to build custom reports, workflows, or smart lists inside HubSpot, perfect for tracking partner engagement or triggering automated follow-ups.
- Link your HubSpot deals to Introw via company associations
- Create partner portal from within HubSpot
- Introw workflow actions in HubSpot
- Automating workflow actions in HubSpot using Introw App events
- Partner Connect: a 2-way CRM integration with HubSpot

---

## AI Agent security at Introw
Source: https://support.introw.io/en/articles/11558434-ai-agent-security-at-introw

At Introw.io, we take the security and privacy of your data seriously. Our AI agent is designed from the ground up with enterprise-grade security measures, ensuring your data is handled responsibly and stays protected. 
### Built on secure infrastructure
Our Introw AI agent is hosted in AWS Europe , and our AI models are accessed through the Vercel AI Gateway . This ensures that:
- Conversations remain private, we use Vercel AI Zero Retention models .
- Your data stays in Europe, the agent runs on AWS infrastructure located in the European region.
- Prompt protection is enforced through both Introw’s system design and built-in security mechanisms, safeguarding against profanity , prompt injection , and other malicious inputs.
👉 Learn more about Vercel AI Gateway and Zero Retention models here . 
### Strong privacy & compliance standards
Your data is handled with care and in full alignment with leading privacy and security standards:
- We are SOC 2 compliant and follow ISO 27001 best practices.
- Our platform is designed with GDPR principles in mind, ensuring your personal data remains protected and processed lawfully.
- AI agents can only access the data you’re already authorized to see, nothing more.
- Access controls and data handling practices are regularly audited and verified.
👉 Learn more about our Security and Compliance certifications in our TrustCenter
### AI Agent access is strictly limited to authorized data
When you connect Introw to your CRM, your meeting calendar or other tools.
- The AI only sees the information you already have permission to access .
- It never pulls in data from outside your account or organization.
- All integrations follow your platform’s existing access controls, no special permissions are added or extended.
- Partner-Specific access only When a partner asks a question, the AI agent only looks at the data that is specifically relevant to that partner . It does not cross-reference or surface information from other partners, accounts, or unrelated records. 
- When a partner asks a question, the AI agent only looks at the data that is specifically relevant to that partner . It does not cross-reference or surface information from other partners, accounts, or unrelated records. 
### Why you can trust our Introw AI Agent
- ✅ Hosted on secure AWS Europe infrastructure
- ✅ AI models served via the Vercel AI Gateway using Zero Retention models
- ✅ Protected against prompt injection , profanity , and abuse
- ✅ AI only accesses data you’re authorized to see
- ✅ Integrations are permission-aware and scoped
- ✅ Fully aligned with GDPR , SOC 2 , and ISO 27001 standards
- ✅ View our compliance and security posture at trust.introw.io
For any questions or specific concerns about AI security and privacy, don’t hesitate to contact our support team
- Introw Agent
- Using your MCP Server with Introw’s AI Agent
- Using Introw AI across your partners
- Install the Claude connector of Introw
- Using Introw with Gemini via MCP

---

## AI detected channel conflict resolution
Source: https://support.introw.io/en/articles/11579537-ai-detected-channel-conflict-resolution

Channel conflict is a common challenge when working with multiple partners or sales channels like direct and indirect sales especially when partners are targeting for the same customers, resources, or opportunities. At Introw, we’ve built a powerful solution using Agentic AI to pro-actively eliminate channel conflict, boost trust, and ensure every partner has a fair and optimised experience.
Introw’s Agent takes the guesswork out of deal and lead registration by being integrated deeply in your CRM and partner network to route deals and leads fairly, avoid overlap, and keep channel conflict from ever starting. 
Unlike basic validation rules that rely on email or domain matching, our AI agent performs deep contextual mapping across activity signals, relationships, and historical data to ensure the right partner is credited every time.
Introw’s Agent guides you through every step of resolving channel conflict, proactively suggesting solutions, handling messaging to partners, and keeping the entire process smooth and hands-off.
In the form submission overview you will see within the status that there is a channel conflict detected. 
When you open the form submission detail, the Introw Agent will guide you to resolve the channel conflict. 
Our AI identifies which partner should own or co-own a lead, based on contribution history, engagement signals, and predefined rules. This ensures the right partner is credited and compensated for their effort.
This eliminates ambiguity and reduces disputes around lead ownership or partner priority. 
### Real-Time Alerts & Conflict Resolution
If potential overlap or conflict is detected, Introw alerts the appropriate users and provides suggested resolutions before it becomes a problem. Introw’s Agent will also help you with handling the messaging to partners 
Your partner will receive the message that their form submission (like deal registration) has been declined with the message the agent provided or that you rewrote in case you wanted to change the copy. 
Channel conflict detection is enabled by default on any Introw form for deal, lead, contact registration. If enabled, Introw will start watching for channel conflicts based on existing Deals (or opportunities), Leads, Contacts, Companies (or accounts) within your CRM and your other form submissions within Introw.
 Example of a channel conflict with a deal from another Partner that already exists in your CRM.
Not every matching record is a real conflict. A deal your team marked Closed Lost months ago, or an account that's been sitting untouched for half a year, usually isn't worth flagging, it only adds noise for your partner managers and slows down a partner who deserves a fast yes.
To keep detection sharp, add conditions on the form's channel conflict settings that tell Introw which records to leave out. Build them on any field of the matched record, so only relevant, active records are ever treated as a conflict. For example:
- Skip closed deals, ignore deals where the stage is Closed Lost , so an abandoned opportunity never blocks a fresh registration.
- Skip stale deals, ignore deals created more than 180 days ago, so long-dead pipeline isn't counted as an active conflict.
Introw only checks the records that pass your conditions, fewer false flags, faster decisions for partners, and a conflict queue that surfaces only what's worth acting on.
- Integrating Introw with Crossbeam
- Automatically attribute resellers and distributors in two-tier channel deals
- How Introw keeps your CRM clean
- Introw's AI Agent in Slack
- AI channel conflict resolution

---

## Embed Notion into Introw
Source: https://support.introw.io/en/articles/11579596-embed-notion-into-introw

💡 Introw tip: Make sure your Notion document is published so available on the internet to be able to see the embed option in Notion.
##### Step 1: Make your Notion page publicly available
Make sure your Notion page is published so available on the internet to be able to see the embed option in Notion.
##### Step 2: Click share in Notion
In your Notion page, click Share and select </> Embed this page
##### Step 3: Copy the link
Copy the link in between the iframe tags, after scr and between the " " (see screenshot)
##### Step 4: Add a section "Embed Link"
Add a section "Embed link" in your Introw experience builder and copy-paste the link & click Embed link.
##### Step 5: Embed the Notion content
Click on the 3 dots next to the section and select " Embed link content"
##### Step 6: Check out the final result
After you publish the experience, you can click preview to see the result of the Notion embed where Introw will visualize the embeddable content of your Notion page within the partner portal. 
- Embed your google calendar in Introw
- Embed your google appointment scheduler
- Embed Introw in your product
- Embed Introw forms
- Why my embedded website shows up blank in Introw

---

## Introw product update - June 2025
Source: https://support.introw.io/en/articles/11594452-introw-product-update-june-2025

### Agentic channel conflict resolution
Introw’s Agent will resolve channel conflicts in real-time by identifying issues directly from your CRM data and guides you through every step of resolving a channel conflict, proactively suggesting solutions, handling messaging to partners and keeping the entire process smooth and hands-off. Learn more
### Extensive partner engagement
Keep partners in the loop with instant updates when key properties change on any CRM object, including deals, companies, contacts, tickets, custom objects, and more. Just pick the fields to track, and Introw will automatically notify partners the moment something updates. No back-and-forth, just real-time alignment. Learn more 
### Track email engagement
Track all CRM-triggered emails and partner notifications in Introw. Know who’s engaging, what’s working, and where to follow up at scale. Learn more
### HubSpot workflow action
Use the Introw PRM workflow action to fully automate your partner creation without leaving HubSpot. Learn more
### Additional improvements
A dynamic book meeting section for your partners to schedule a meeting with their appropriate partner manager.
 Introw partner activity events are now automatically pushed to your HubSpot timeline events! This means you’ll see key partner engagement signals right where you work.
 Embed Notion pages directly in your Introw partner portals making it easy to share real-time, collaborative content without duplicating work or breaking your workflow.
- Introw product update - July 2025
- Introw product update - August 2025
- Introw product update - October 2025
- Introw Product update - December 2025
- Introw product update - March 2026

---

## Introw Home page
Source: https://support.introw.io/en/articles/11662106-introw-home-page

The Introw Home Page is every user's central hub. It provides a personalized snapshot of partner performance, engagement levels, pending tasks, and all key updates - whether related to deals, leads, or any other activity.
### Introduction to the Introw Home Page
Click the video below to watch a walkthrough of the Home Page and how to use it effectively. 
### What can you do on the Home Page
When you land on the Introw Home Page, you’ll see a personalized overview tailored to your partners and their activity. Here’s what you can access and take action on.
#### Quick Metrics
Stay on top of partner performance with live stats showing:
- Total Partners - Active partner relationships you're working with
- Revenue - Attributed revenue coming from your partner pipeline
- Engagement - How active your partners are (intros, messages, deal flow)
These metrics update in real time, so you always know where you stand.
#### Highlights
This section surfaces important updates and actionable items across your partner portal and includes:
- Deal Updates : see new activity or changes to active deals
- Due Tasks : know what needs your attention today
- Missing Engagements : Identify partners you haven’t interacted with in a while due to no partner portal access or disabled notifications.
- Comments & Mentions : Stay looped into conversations you're part of
Think of this as your smart assistant, flagging what matters most.
#### Partner Portal Activity Feed
Track all real-time events happening across your partner ecosystem:
- New deal, lead or partner registrations
- Recent partner portal visits
- Deal (lead, company, contact, etc) updates
- Task updates and achievements
- Collaborator activity from comments, mentions and much more.
It’s like a live feed of everything happening with your team and partners, all in one place.
#### Get support or learn more
Need help or want to learn more about how to use Introw?
- Chat with Support - Reach out directly from the Home Page
- Help Center Access - Click through to browse feature guides and tutorials
- Introw's commission module
- Embed Introw forms
- Introw + Claude: use cases & what's possible
- Introw's AI Agent in Slack
- Install Introw on your mobile home screen

---

## Add a news or social widget to your partner portal
Source: https://support.introw.io/en/articles/11702747-add-a-news-or-social-widget-to-your-partner-portal

Today’s partners crave relevance, real-time updates, and trust in the vendors they work with. Yet, partner portals are often static, siloed, and disconnected from the broader conversations happening online especially on platforms like LinkedIn and Facebook.
This disconnect creates a few key pain points:
- Stale content : Partners miss timely updates, thought leadership posts, or campaign news that live on social.
- Extra steps : They’re forced to leave your portal to check social channels, which disrupts their experience.
- Missed engagement : Valuable conversations and brand visibility go unnoticed by your partner network.
### How to do it with Introw
Embedding your news or social feed is fast, easy, and code-free thanks to tools like Elfsight , EmbedSocial , POWR , Taggbox , SociableKIT , Common Ninja , Widgetic , SocialPilot , and Walls.io all of which let you create customizable widgets for LinkedIn, Facebook, Instagram, and more. 
#### Step-by-Step Guide (for Elfsight as example)
- Go to Elfsight Visit https://elfsight.com/widgets/ and choose a widget: For LinkedIn, select LinkedIn Feed . For Facebook, choose Facebook Feed . 
- For LinkedIn, select LinkedIn Feed .
- For Facebook, choose Facebook Feed . 
- Customize your widget Add your company page link. Choose layout, style, and what to show (posts, images, videos, etc.). Finish setup and copy the shareable link Elfsight provides. 
- Choose layout, style, and what to show (posts, images, videos, etc.).
- Finish setup and copy the shareable link Elfsight provides. 
- Open your Introw Partner Experience builder Navigate to the tab where you want to display the feed. 
- Click “Add Section” > “Embed Anything” Copy paste the shareable link of your widget customization menu.
- Embed link and Done! Your live social feed will now appear inside your partner portal and update automatically.
- How to personalize your partner portal?
- Embed your google calendar in Introw
- Embed tasks within your partner experience
- Create a Partner portal experience
- How to embed a report or dashboard in your partner portal

---

## Partner Analytics
Source: https://support.introw.io/en/articles/11705562-partner-analytics

Introw’s Analytics gives you a clear, instant view into how your partnerships are performing without the need to dig through your CRM or chase down fragmented reports.
### The problem today
Without centralised analytics, it's hard to answer questions like:
- Which partners are actually engaged?
- Are our assets being seen and used?
- How much revenue is being driven through this channel?
- Who’s responding to our emails, and who’s not?
When data is buried in your CRM or spread across tools, these insights are either delayed, incomplete, or missing entirely.
### How does Introw solve this?
The new Analytics page brings together all your previous metrics and takes things a step further. It now includes:
- Revenue Tracking : See how much revenue is being generated through your partners.
- Asset Views : Understand how often your shared assets are being viewed and by whom.
- Email Notification Activity : Track the performance of Introw's automated email notifications: who’s opening, clicking, and engaging.
- Power Partner Insights : Get a clearer picture of your most engaged partners and the related partner contacts. We highlight your top collaborators and how they’re interacting with you on Introw.
### The CRM integrated advantage of Introw
Introw Analytics pulls directly from your CRM and surfaces the metrics that matter, automatically. You get a full picture of partner engagement and deal activity in one place, with no extra work required.
Here’s what you can track:
- Revenue generated through partner activity
- Tier distribution to understand how partners are grouped by engagement or value levels
- Asset views to see what content is resonating
- Email notification engagement, opens, clicks, responses
- Power partner insights, who your most engaged and impactful partners are
With these insights, you can:
- Double down on relationships that drive revenue
- Spot silent or underperforming partners early
- Improve outreach with real-time feedback on what’s landing
- Build better strategies, backed by actual usage and engagement data
All of this is ready the moment you connect your CRM, no setup, no manual reporting.
- Partner performance dashboard
- Partner Engagement Tracking
- Partner engagement reporting in HubSpot with Introw app events
- Tracking Partner involvement on deals
- What is Partner Connect?

---

## Add or delete tasks
Source: https://support.introw.io/en/articles/11711321-add-or-delete-tasks

Standalone tasks let you assign a specific action to a partner without linking it to a task template. Use these for one-off asks or anything outside your standard onboarding flow.

Step 1, Go to Tasks and click Add task → Standalone task .
Step 2, Fill in the task details:
- Task name
- Internal or partner-facing, internal tasks are only visible to your team, not to the partner
- Due date
- Assignee, assign to your partner, a specific partner contact, or someone from your team
- Description (optional)
- Attached file (optional)
Step 3, Click Add task . The assignee will be notified automatically.
To delete a single task, open the task detail panel and remove it from there. To clean up multiple tasks at once, use the bulk delete feature, select the tasks you want to remove and delete them all in one go.
- Introw tasks
- Partner journeys
- Embed tasks within your partner experience
- Task actions
- Build a mutual action plan with Tasks

---

## Call to Action Buttons
Source: https://support.introw.io/en/articles/11711503-call-to-action-buttons

The Call to Action (CTA) Button section allows you to add customizable buttons to your partner portal that help guide users to key actions or destinations.
You can make it full section by clicking Add section > Rich section > Call-To-Action
You can also add these CTA buttons by using the / symbol when you want to insert it into an existing section like a text.
These buttons can be configured to redirect partners to other pages within the platform, open deal registration forms, or link to external resources, making it easy to streamline navigation and drive engagement where it matters most.
Each CTA button can be personalized with:
- Custom label text
- Button style and color to match your branding
- Destination URL or partner portal tab or Introw form
You can place CTA buttons throughout your portal, whether in rich sections or standalone areas, to draw attention to important processes like submitting deals, accessing marketing materials, or starting onboarding.  This ensures partners stay focused and always know where to go next. 
- What are rich sections?
- How to use Introw forms
- Embed Introw forms
- Task actions
- How to use Introw forms with HubSpot

---

## Task actions
Source: https://support.introw.io/en/articles/11716026-task-actions

Task Actions in Introw are designed to help you streamline your partner onboarding workflows by linking actions to specific tasks . With this feature, you can now automate task completion when partners view content, upload files, or take important steps like registering their first deal, all from within their partner portal.
You can now link automated actions to tasks such as:
- Viewing an asset (e.g., product video, case study, sales deck)
- Uploading a file , such as an NDA, contract, or a specific onboarding form
- Submitting an Introw form (e.g. registering their first partner lead or deal)
- Going to an external link outside Introw (e.g., Calendly, Typeform, or your website for booking a demo)
Once the partners completes the action, the associated task will be automatically marked as done , keeping your taks overview cleaner and your partners on track.
### Use cases
Here are a few ways to use Task actions effectively:
##### Auto-complete a Task when an asset is viewed
Link a task to an Introw asset like a video walkthrough or pitch deck. Once the partners watches it, the task is marked as complete, no need for manual follow-ups.
👍 Great for : Learning from demo recordings, reading case studies or watching a tutorial.
##### Redirect to external links
Do you need your partners to take an action outside their partner portal? Link the task to an external link like a booking page, pricing calculator, survey form, or any external tool like an LMS.
👍 Great for: filling out onboarding forms, visiting a pricing page or starting a training course. 
##### Require file uploads
Collect signed NDAs, agreements, or onboarding documents by linking a task to a file upload action. The task will auto-complete when the partner uploads the required file. Within the task detail you can add an attachment in case you partner needs to download a file before uploading the updated one.
👍 Great for : Legal sign-offs, compliance steps, or onboarding documentation.
##### Open a form in Introw
Trigger a task to auto-complete when a partners opens and submits a form directly within Introw.
👍 Great for : Lead capture, opportunity registration, onboarding intake forms, or collecting structured responses. 
##### Partner experience
Your partners can view and complete your assigned tasks within their partner portal. Each task card can include a task action button to quickly complete the task and stay on track.
- Introw tasks
- Partner journeys
- Task templates
- How does the integration with Microsoft Teams work?
- Build a mutual action plan with Tasks

---

## Partner notifications
Source: https://support.introw.io/en/articles/11848308-partner-notifications

We keep partners informed and aligned on auto-pilot through email and/or Slack notifications. These notifications cover updates to CRM objects like deals, oppportunies, leads, comments, announcements, tasks, and so on. Making sure nothing slips through the cracks.
This article outlines the types of notifications partners receive, what they include, and where they show up. 
#### CRM Object update notifications
Keep partners up to date when shared deals or CRM records are updated or key information on a shared CRM object changes.
- Email : Summary of the changes, who made them, and a link to the deal (CRM record in Introw).
- Slack : Instant message showing the update details with a link to view it in Introw.
#### Comment notifications
Ensure real-time collaboration by notifying the partner when you make comments on a deal (or shared CRM record), a comment within the partner portal or a comment on an Introw form submission.
Delivered via:
- Email : Includes the comment, who posted it, an option to reply via e-mail (off portal collaboration) and a link to the form submission. 
- Slack : Message with the comment, the form preview and a link to jump into the partner porrtal or view the submission.
#### Introw task notifications
Partners receive task update notifications whenever there are changes or progress on a task they’re involved in. These notifications help them stay informed about status updates, new comments, approaching deadlines, or any modifications made to the task details. By keeping you and your partners up to date in real time, you ensure a smooth collaboration and faster follow-ups without the need to manually check the platform.
- How does the integration with Slack work?
- Save time with Introw’s AI Agent
- Introw's AI Agent in Slack
- How does the integration with Microsoft Teams work?
- What is Partner Connect?

---

## Introw product update - July 2025
Source: https://support.introw.io/en/articles/11868054-introw-product-update-july-2025

#### Actionable tasks
Tasks just got smarter and more automated! You can now connect actions like viewing an asset, filling out a form, uploading a file, or visiting a link directly to a task. Once the action is completed, the task updates automatically , making everything smoother for your partners and perfect for streamlining partner onboarding and training. Learn more
### Call to Action section
Introducing the new Call to Action section , a straightforward way to guide partners to take the right next step. Whether it’s registering a deal, referring a lead, booking a meeting, or starting a training, you can now add clear action buttons anywhere in the portal. It’s all about helping partners act faster, right when it matters. Learn more
### Multi-tier programs
You can now create and manage multiple tier structures within your partner ecosystem like separate Silver tiers for resellers and referrals, each with their own rules and benefits. Best of all, tiers sync directly to your CRM for a consistent partner view across all your systems. Learn more
### Additional improvements
Based on your valuable feedback, Introw continuously makes small but meaningful updates to improve performance, usability, and your overall experience.
You are now able to visualize any related CRM properties linked to your partners within your partner overview.
  Thumbnails on asset folders ! This means you’ll see key partner engagement signals right where you work.
   Sync partner roles directly into Introw from your CRM to ensure that key partner data like specific stakeholder roles are always up to date and accurately reflected across both systems.
- Introw product update - June 2025
- Introw product update - October 2025
- Introw product update - November 2025
- Introw Product update - December 2025
- Introw product update - March 2026

---

## Assign partner managers
Source: https://support.introw.io/en/articles/11892742-assign-partner-managers

The Partner Manager is the team member responsible for managing the relationship with a specific partner. Assigning a Partner Manager ensures clear accountability and helps maintain a strong partner experience
You can assign or update the Partner Manager through the following methods:
##### Via the Partners overview
- Navigate to the Partners overview.
- Select the partner(s) you want to assign
- Click the edit icon or property partner manager to be updated
- Select a Partner Manager from the dropdown list and save your changes
#### Via the Partner detail
- Go to the Partner detail .
- Click on the right hand side to open the detail view .
- Look for the Partner Manager field.
- Click Edit , select the manager from the list, and save.
#### Import from your CRM
The Partner Manager field can be automatically synced based on your CRM property field that represent the partner manager
- Navigate to the Partners overview
- Click "Configure" on the right-hand side, select the partner manager property and click the Sync button
- Map it to the appropriate field from your CRM (e.g., "Account Owner " or "Partner Manager").
The Partner Manager property in your CRM must contain a valid email address by using the Field Type HubSpot User and in SFDC it needs to be a Contact Lookup Field. If the user does not yet exist, we will automatically create an Introw account for them and assign the partner accordingly.
The CRM mapping is used only at the time of partner creation . Changes to the CRM field after a partner is created will not automatically update the Partner Manager in Introw.
#### Don’t have a Partner Manager field in your CRM?
No problem! If your CRM doesn’t yet have a dedicated field for the Partner Manager:
- Introw can automatically create this field for you during setup.
- Once created, we’ll populate it with the email addresses of the assigned Introw users for each partner.
- This helps keep your CRM aligned with Introw, even if you’re just getting started with structured partner data.
📌 Tip: This is a great way to ensure consistency between your systems without needing manual setup in your CRM.
- How partner deal data syncs to your CRM
- Add your partners to Introw
- Managing partner contacts
- How to set up a partner application form
- What is Partner Connect?

---

## Managing partner contacts
Source: https://support.introw.io/en/articles/11895888-managing-partner-contacts

Partner Contacts in Introw are the key individuals at your partner organizations who are either:
- Primary associated contacts from your CRM Introw pulls in all associated contact(s) from your CRM, those marked as primary associated contacts on the partner (account) record.
- Introw pulls in all associated contact(s) from your CRM, those marked as primary associated contacts on the partner (account) record.
- Partner portal visitors who are granted access to your partner portal via Introw. Any partner contact who is invited to the partner portal becomes visible in Introw as a partner contact and their email address is saved in Introw and can be pushed in to your CRM if desired
- Any partner contact who is invited to the partner portal becomes visible in Introw as a partner contact and their email address is saved in Introw and can be pushed in to your CRM if desired
#### Show CRM contact properties in Introw
You can enrich each Partner Contact in Introw by displaying any contact-level property from your CRM like phone number, job title, certification status, etc.. 
These values will appear in the Partner people overview, providing more context for your team.
#### How to set this up
- Open Configure from the Partner people overview.
- Select the CRM contact property fields you'd like to display in Introw.
- Save
#### Mapping partner contact roles from your CRM
Partner roles from Introw (e.g., "Decision Maker," "Technical Contact," "Marketing Lead") are used to define the access level to content within the partner portal and used for task assignment within Introw.
- You can link the Partner contact role in Introw to a specific field in your CRM (e.g., a custom "Contact Role" or "Title" field).
- This ensures that each contact's role is automatically populated based on CRM data.
📌 Tip: Roles help with segmenting partner portal content and managing task assignment at scale within the partner portal. Learn more about segments
#### Update partner contact information
You can edit Partner Contact details such as first name , last name , and other CRM-synced properties directly within Introw. 
However, the email address cannot be edited in Introw, as it is used as the login credential for accessing the partner portal.  If a contact's email address needs to be updated, please make the change in your CRM . Once updated there, the new email will be reflected in Introw during the next sync or when the partner is re-created.
- Go to Partner people page
- Open relevant Partner contact
- Update the field you like and this will also be updated in your CRM
Portal Access : This toggle allows you to define if the partner contact will have access or not to their Partner Portal.
#### Sync partner portal access with your CRM
Instead of managing partner users portal access manually in Introw, you can link the Portal access field to a contact property in your CRM . This way, granting or revoking portal access is driven directly from your CRM, no need to touch Introw.

When a contact's CRM property value matches the configured access value, Introw will automatically grant them portal access. When the value is removed or changed, access is revoked accordingly.
- Go to the Partner people overview and open Configure properties .
- Find the Portal access property and select Sync to open the sync settings.
- In the Access property dropdown, select the CRM contact property you want to use to control portal access (e.g., an "Introw access" dropdown field in HubSpot).
- Click Save .
Once configured, the Portal access property in the people overview will show an In Sync badge, confirming the link is active.
📌 Tip: This is especially useful if your team already manages partner contact data in your CRM, you can control who gets portal access without ever leaving your CRM workflow.
💡 Introw Tip : Changes made in your CRM on the partner record and partner contacts are reflected within 15 minutes!
- Add your partners to Introw
- Assign partner managers
- Deal visibility restrictions for partner contacts
- Partner profile section
- Partner team roles

---

## Invite and manage partner portal users as a partner
Source: https://support.introw.io/en/articles/11960140-invite-and-manage-partner-portal-users-as-a-partner

As a partner, you can manage who has access to your Partner Portal. This includes inviting new visitors (such as team members, consultants, or stakeholders) and reviewing who currently has access. 
Introw keeps performing automatic domain and security checks during the invite process to ensure a secure and streamlined experience. This gives your partner more autonomy while keeping access controlled and compliant. 
##### Add partner portal visitors as a partner
Use the avatar in the top-right to invite colleagues or stakeholders to your Partner Portal and send an invite to new partner contacts to join the partner portal 
🔔 The invited user will receive an email with a link to access the Partner Portal.
##### Manage the partner portal visitors as a partner
Use the avatar in the top-right to see which colleagues or stakeholders of your organisation have access to your Partner Portal and invite new ones. 
- How to launch a partner portal
- Launch your partner portal
- Create a Partner portal experience
- How to invite Partners to your portal via Introw
- Managing partner contacts

---

## Deal visibility restrictions for partner contacts
Source: https://support.introw.io/en/articles/11960790-deal-visibility-restrictions-for-partner-contacts

To improve control and simplify deal collaboration, we’ve introduced a new visibility restriction feature based on a role permission called Collaboration Restriction. With this permission enabled, partner contacts will only see deals where they are marked as a collaborator . 
### How can this help your partners?
- Improved data privacy: Protect sensitive deal information from being accessed by unintended partner contacts.
- Focused collaboration: Ensure partner contacts are only involved in deals where they are actively contributing.
- Streamlined experience: Reduce noise by showing each partner only the deals they need to work on.
This feature is ideal for partners with multiple team members handling different deals concurrently, ensuring that each partner user only accesses relevant deal information.
### How to configure this?
- Go to portal settings > partner roles
- Add or update a role by clicking the ⚙️ icon. 
- Enable the "Collaboration Restricted" permission 
💡 Introw tip: Set a default partner role for when adding new partner contacts and optionally link it to a CRM property of your partner contact to keep it in sync.
### How does it work?
- When a partner contact submits a form to register a deal via Introw , they are automatically set as the collaborato r on that deal. This ensures they immediately gain access to the deal they’ve submitted, without requiring any manual setup. If the (defaulted) partner contact role has the “Collaboration Restricted” permission, this also means the deal will only become visible to them maintaining secure, relevant access with minimal effort.
- This ensures they immediately gain access to the deal they’ve submitted, without requiring any manual setup.
- If the (defaulted) partner contact role has the “Collaboration Restricted” permission, this also means the deal will only become visible to them maintaining secure, relevant access with minimal effort.
💡 Introw tip: Partner contacts without the “Collaboration Restricted” permission will continue to see all deals based attributed to them as a partner in general.
2. You can assign collaborators manually to a deal (or any other shared CRM object) in case there is no collaborator assigned yet. 
When a collaborator is assigned to your deal they will get automatic updates about changes on the deal they are assigned to as collaborator. 
- How partner deal data syncs to your CRM
- Collaborate on a deal or any other CRM object
- CRM User
- Use collaborators to ensure partners stay updated on the right deals
- What is Partner Connect?

---

## Task templates
Source: https://support.introw.io/en/articles/11969738-task-templates

Task Templates are pre-built sets of tasks that help guide partners through specific processes such as onboarding, training, campaign execution, or certification. Instead of recreating the same tasks for each partner, you can quickly apply a template in just a few clicks or link it to a partner experience for automatic enrollment.
#### Manage task templates
Easily create a task template by clicking Tasks Add task > Task Template or use one of Introw's suggested task templates and adjust them to your needs.
#### Task execution order: Sequential
Set the task execution order to Sequential which will allow you to create a structured set of tasks that must be completed in a specific order . This ensures partners follow the exact process you’ve designed, such as registering a deal before starting a sales training, completing required certifications before providing customer support, or signing an NDA before accessing sensitive materials.  Each task unlocks only when the previous one is marked complete, keeping partners on track, reducing skipped steps, and maintaining process consistency across all users
#### Task execution order: Flexible
Flexible task templates let partners complete tasks in any order that suits their workflow. For example, they can upload a company logo, review marketing guidelines, register a deal, or update contact information whenever it’s convenient without waiting for other tasks to be finished. This flexibility helps partners progress faster while still ensuring every requirement is eventually completed.
### Create actionable tasks
Task Actions in Introw are designed to help you streamline your partner onboarding workflows by linking actions to specific tasks . With this feature, you can now automate task completion when partners view content, upload files, or take important steps like registering their first deal, all from within their partner portal.
You can now link automated actions to tasks such as:
- Viewing an asset (e.g., product video, case study, sales deck)
- Uploading a file , such as an NDA, contract, or a specific onboarding form
- Submitting an Introw form (e.g. registering their first partner lead or deal)
- Going to an external link outside Introw (e.g., Calendly, Typeform, or your website for booking a demo)
Once the partners completes the action, the associated task will be automatically marked as done .
#### Task template progress
You can track how far along a set of tasks is by opening the task template and checking the overall Progress . This shows you the current stage of the task, such as To Do , In Progress , or Done and how many partners are linked to this set of tasks.
Task progress can also be monitored across multiple partners, making it easy to see who’s on track, who needs support, and where deadlines may be at risk. This helps you quickly spot trends, address bottlenecks, and keep projects moving smoothly.
- Introw tasks
- Partner journeys
- Task actions
- Build a mutual action plan with Tasks
- The Introw-Powered PAM: A Day in the Life

---

## Connect your CRM
Source: https://support.introw.io/en/articles/11970521-connect-your-crm

Connecting your CRM to Introw means managing your partners and their revenue runs directly on top of your single source of truth . No duplicate records, no manual updates, and no “which system is right?” confusion. As Introw PRM is built on top of your CRM ensures that every partner deal, lead, and activity is instantly visible to your sales team, fully aligned with your existing pipeline, and enriched with the same data you already trust.  Our deep CRM integration keeps partners and your sales team perfectly aligned, accelerates sales cycles, increases partner engagement, and ensures everyone works from the same unified source of truth. 
### Why start with a CRM connection?
Auto-detect partners and track partnership revenue instantly. Keeping your CRM as the single source of truth.
- Your CRM remains the single source of truth : keep all partner and revenue data centralized.
- Lightning-fast implementation : get everything up and running in minutes, not months.
- Seamless two-way sync : deal registrations, form submissions, comments, and updates flow effortlessly between both systems.
#### How does it work?
- Go to Settings , then Integrations in the navigation menu. Locate and "Connect" your CRM
- Locate and "Connect" your CRM
- Authenticate and Authorize Access Make sure you have the correct (admin) rights within your CRM to make connections with 3th party apps. 
- Make sure you have the correct (admin) rights within your CRM to make connections with 3th party apps. 
- Identify your partners and their attribution Learn more in the next article  
- Learn more in the next article  
- Partner activity events in your HubSpot timeline
- Introw CPQ
- How Introw keeps your CRM clean
- Partner Connect: a 2-way CRM integration with HubSpot
- What is Partner Connect?

---

## Link Introw to Power BI
Source: https://support.introw.io/en/articles/12034448-link-introw-to-power-bi

#### Introduction
In this article, we’ll walk you through the process of linking Power BI to Introw using a Service Principal. By the end of the steps, you’ll have your Tenant ID , Client ID , and Secret Key which are required to establish a secure connection between Power BI and Introw.
#### Step 1: Register an application in Azure
Azure applications are the credentials that allow us to cross certain bridges, or rather, communicate with different services within the Microsoft cloud. To register a new app, go to the Azure Portal ( https://www.portal.azure.com ). 
Within the Entra ID service (previously called Active Directory) you can find a Registered Applications menu where you can put “New Registration”. Just use the default settings. When completed you will be able to retrieve the Tenant ID and the Client ID. For example: Introw Power BI
#### Step 2: Add the new created app to a Security group
Add the newly created application to a security group or create a new security group and add the newly created application.
#### Step 3: Configure the API permissions of the application
Configure the API permissions for your newly created application. This grants the Introw power BI application to read the required data from Power BI.
The required permissions are:
- Dashboard.Read.All
- Dataset.Read.All
- Report.Read.All
- Workspace.Read.All
#### Step 4: Generate a Secret Key
Generate a secret key for the newly created Service Principal Application.
#### Step 5: Configure the tenant settings
To ensure that our application, registered with a secret (service principal), can use the API services, we need to allow it from the administration portal. As an administrator from Fabric/PowerBI, we open the administration portal from the menu that reveals the configuration gear. Enable the Service principals can call Fabric public APIs setting and apply for the security group where the registered Introw Power Bi application is member of.
#### Step 6: Manage workspace access
The application also needs access to the Power BI workspace that will be used to embed reports and dashboards in Introw. To grant this access, navigate to the relevant workspace, open Manage Access , and add the security group.
Step 7: Link Introw to Power BI
Enter the required credentials in Introw and finalize the connection with Power BI. 
Introw will not store any Client Secret, this is only needed one-time to establish the connection to Power BI.
Learn more how to link the reports to Introw here
#### You are all set!
- Link your HubSpot deals to Introw via company associations
- Create new partners via Introw
- Embed your Power BI reports
- Enable Single-Sign-On for your team
- 🚀 Customer Deep Dive: How Quatt Powers Installer Operations with the Introw MCP

---

## CRM User
Source: https://support.introw.io/en/articles/12079274-crm-user

This article explains the CRM User role , its permissions, and how it differs from other roles within Introw. Please review the information below to understand what this HubSpot only role can and cannot do in the Introw partner portal.
### How to use the Introw card via HubSpot
CRM Users access the Partner Portal exclusively via the HubSpot UI card and separate Introw login credentials are not needed . Learn more 
Users with the CRM User role that try to login to https://app.introw.io will be redirected to use the HubSpot flow.
### Overview
- Login method: CRM Users access the Partner Portal exclusively via HubSpot by clicking the Introw collaboration card . Separate Introw login credentials are not required . Only users who have been assigned an Introw user role with HubSpot Only permissions will be redirected into the Partner Portal. If a user without this role clicks the card, they will see the Introw login page . This ensures: Access is granted only to approved users. Unauthorized HubSpot users are clearly notified that additional permissions are required. 
- CRM Users access the Partner Portal exclusively via HubSpot by clicking the Introw collaboration card .
- Separate Introw login credentials are not required .
- Only users who have been assigned an Introw user role with HubSpot Only permissions will be redirected into the Partner Portal. If a user without this role clicks the card, they will see the Introw login page . This ensures: Access is granted only to approved users. Unauthorized HubSpot users are clearly notified that additional permissions are required. 
- If a user without this role clicks the card, they will see the Introw login page .
- This ensures: Access is granted only to approved users. Unauthorized HubSpot users are clearly notified that additional permissions are required. 
- Access is granted only to approved users.
- Unauthorized HubSpot users are clearly notified that additional permissions are required. 
- Partner info via the Introw card: Before entering the portal, the Introw Collaboration card already provides valuable context, including: Who the partner organization is The main contact person for that partner internally ( partner manager ) The main contact person of the partner externally ( partner champion ) The tier the partner is currently assigned to This ensures CRM Users always have a clear snapshot of partner details at a glance.
- Before entering the portal, the Introw Collaboration card already provides valuable context, including: Who the partner organization is The main contact person for that partner internally ( partner manager ) The main contact person of the partner externally ( partner champion ) The tier the partner is currently assigned to
- Who the partner organization is
- The main contact person for that partner internally ( partner manager )
- The main contact person of the partner externally ( partner champion )
- The tier the partner is currently assigned to
- This ensures CRM Users always have a clear snapshot of partner details at a glance.
### What CRM users can do
When assigned this role, CRM Users receive a portal experience similar to a partner, with three main benefits:
✅ Pipeline visibility
- View partner submitted and attributed deal pipeline in the portal.
- Track deal status and updates at any stage.
✅ Collaboration on deals (leads, tickets, contact, companies or any CRM attributed object)
- Register new deals via the Partner Portal.
- Work directly with partners on deal details and updates.
- Maintain alignment between HubSpot CRM and the Partner Portal without switching platforms.
✅ Access to Partner Resources
- Access to shared documents and other enablement content
- Overview on task progress
#### What CRM users cannot do
The following actions are restricted for CRM Users:
❌ Edit or Manage Records in Introw
- Cannot edit partner information inside Introw.
❌ Admin or Finance Functions
- No access to tasks, workflows, system settings, user permissions, billing info or analytics.
❌ Portal and partner experience configuration
- Cannot change or edit the portal functions or re-configure the partner experience.
- Create partner portal from within HubSpot
- Share a deal to partners via Introw's app card in HubSpot
- What does “No portal yet" and "No deal embed yet” mean?
- Partner Connect: a 2-way CRM integration with HubSpot
- Validate your Partner Connect Card

---

## Introw product update - August 2025
Source: https://support.introw.io/en/articles/12142898-introw-product-update-august-2025

### New HubSpot UI card
Big news for HubSpot users! We’ve upgraded from the legacy Introw Copilot card to a brand-new Introw Collaboration card . To keep collaborating seamlessly with your partners, make sure you add the new card to all your HubSpot views.
🎥 Watch the quick video to see how to add the card to your CRM records .
Here’s why the new card makes things better:
- More flexibility to HubSpot’s new UI card component gives us more building blocks to work with.
- Conditional logic to Decide exactly when the Introw card appears.
- Click-throughs to Faster, easier paths to take action directly.
### Collaborators
Partner collaboration just got smarter. With the new Collaboration Restriction permission, partner contacts will only see deals where they are explicitly marked as collaborators. This subtle but powerful change gives you better control across all partner-shared objects, deals, leads, tickets, and more, so sensitive information stays with the right partner contacts while collaboration stays smooth. Learn more
### AI-Generated Announcements
Keeping your partners in the loop has never been easier. Our AI announcement generator helps you craft updates effortlessly using predefined prompts, whether it’s a blog post, webinar invite, or product update. Prefer to start from scratch? That’s no problem either. The AI ensures your messages are polished and professional while saving you time. Learn more  Watch the video below ⬇️ that demonstrates how you can create an announcement based on a blogpost and send it to your partners in a few clicks
### Additional improvements
Thanks to your continued feedback, Introw is making small but impactful updates that improve performance, usability, and the overall experience
Sync portal access Partner contact portal access from your CRM now flows directly into Introw, making it easier to manage permissions and keep everything aligned across systems.
Partner announcement display Announcements can now be displayed in the partner portal with flexible layouts,  list, card, or posts and you can choose how many to show upfront while still letting partners click view more to see all past announcements.
  Link existing CRM records When partners submit a form, Introw AI will suggest matching existing CRM records based on name, domain, email and users can adjust or correct the match if needed.
- Introw product update - October 2024
- Introw product update - June 2025
- Introw product update - October 2025
- Introw product update - November 2025
- Introw product update - April 2026

---

## Using your MCP Server with Introw’s AI Agent
Source: https://support.introw.io/en/articles/12182958-using-your-mcp-server-with-introw-s-ai-agent

### Introduction
One of the most powerful features of Introw’s AI Agent is its ability to connect with external knowledge bases and tools via an MCP (Model Context Protocol) server .
MCP is an open standard that allows AI agents to securely access and query data from external sources. By linking your MCP server to Introw, you can extend the AI Agent beyond Introw’s built-in resources making it smarter, more relevant, and more aligned with your organization’s unique needs.
### What is MCP?
The Model Context Protocol (MCP) is a universal framework that connects AI systems with external data, tools, and services. It standardizes how AI queries information and retrieves results, ensuring security, consistency, and compatibility across platforms.
In the context of Introw, MCP enables the AI Agent to:
- Pull in external knowledge base content
- Connect to custom enterprise tools or APIs
- Provide more personalized, accurate answers to your partners and team
### How MCP Works in Introw
Introw supports direct integration with external MCP servers through a dedicated MCP configuration. 
Once configured:
- The Introw AI Agent functions as an MCP client , issuing structured, authenticated requests to the configured MCP server.
- Requests are sent over TLS-encrypted channels and include the bearer token for access control.
- The MCP server executes the request , retrieves or computes the required data, and returns a structured MCP response.
- The AI Agent consumes the MCP response and incorporates the returned data into its reasoning and final response delivered to the partner or end user.
All MCP traffic is handled in real time , with end-to-end encryption in transit and credentials securely stored and managed via the Introw UI.
### Connecting Your MCP Server to Introw
Follow these steps to connect your MCP server to Introw:
- Prepare your MCP Server Ensure your knowledge base or data source is exposed via an MCP-compatible endpoint. Configure authentication using a bearer token or API key. 
- Ensure your knowledge base or data source is exposed via an MCP-compatible endpoint.
- Configure authentication using a bearer token or API key. 
- Add the MCP Connection Specify the MCP server URL and authentication credentials ( bearer toke n). The connection configuration is securely stored and used by the AI Agent at runtime. 
- Specify the MCP server URL and authentication credentials ( bearer toke n).
- The connection configuration is securely stored and used by the AI Agent at runtime. 
- Validate the Integration Use the Test Agent to issue sample queries against the MCP server. Confirm that responses are returned successfully and contain the expected data. 
- Use the Test Agent to issue sample queries against the MCP server.
- Confirm that responses are returned successfully and contain the expected data. 
- Go Live After validation, the AI Agent begins using the MCP server for partner-facing and internal queries.
- After validation, the AI Agent begins using the MCP server for partner-facing and internal queries.
### Security & Privacy
Security is central to Introw’s MCP integration. Key protections include:
- Authentication: The AI Agent uses secure API tokens or keys to communicate with your MCP server. Unauthorized clients cannot connect.
- Encryption: All queries and responses travel over encrypted HTTPS/TLS channels , preventing interception or tampering.
- Data segregation: Your organization’s MCP data is isolated from all other tenants. No other company or partner can access your server.
Additionally, Introw enforces prompt protection and malicious input filtering to ensure attackers cannot manipulate the AI Agent into exposing or misusing MCP-connected data.
### Benefits of connecting your MCP
By integrating your MCP server, you can:
- Extend knowledge: Incorporate external data sources into the AI Agent’s responses
- Personalize support: Surface company-specific information for partners
- Unify access: Bring multiple knowledge systems into one conversational interface
- Stay secure: Leverage enterprise-grade encryption, isolation, and compliance safeguards
- Introw Agent
- Install the Claude connector of Introw
- Connect Introw AI to Notion, Lovable, OpenClaw, and beyond
- Give your partners their own AI assistant to collaborate in real time via Introw's Partner MCP
- Using Introw with Gemini via MCP

---

## Off-portal collaboration in Introw
Source: https://support.introw.io/en/articles/12183151-off-portal-collaboration-in-introw

Not every partner wants to log in to a portal to stay engaged. With Introw's off-portal collaboration , partners can collaborate on deals directly from their email. When a partner replies to a deal notification email, Introw automatically captures the response and pushes it into:
- The activity timeline on the deal in Introw
- Chatter/Notes in your connected CRM (e.g., Salesforce, HubSpot).
This keeps all stakeholders in sync without forcing partners to leave their inbox.
### How it works
- A partner receives a notification email from Introw about a shared object (e.g., deal, company, ticket, lead).
- Instead of logging into the portal, the partner simply hits “Respond via email” .
- The partner’s response is:
- Captured in Introw under the deal’s activity time line.
- Synced automatically to your CRM (in Notes and Chatter), so internal teams see the same context.
Introw tip: This feature works for any object shared with the partner, including deals, companies, tickets, leads, and more, ensuring all collaboration stays centralized, regardless of object type.
### Benefits of off-portal collaboration
- Lower friction: Partners can collaborate directly from their inbox.
- Better engagement: Makes it easier for partners to provide updates quickly.
- Single source of truth: All deal-related discussions are stored in Introw and synced to your CRM.
- Time savings: Eliminates manual copy-pasting of partner emails into CRM or Introw.
##### Example Use Case
- You share a deal update with a partner.
- The partner replies to the email: “We’ve secured approval from our sales director; let’s move forward.”
- Their reply is instantly logged as a Comment in Introw and synced to your CRM, visible to your team.
No portal login required, no extra steps.
#### Example flow
Below we describe an off-portal collaboration flow. 
##### Notification sent to Partner
You have made an update on a deal within Introw or within your CRM and Introw will automatically inform you partner on this update.
##### 2. Partner Replies from Inbox (email)
The partner simply responds to the email directly, no portal login required.
##### 3. Reply captured and synced
Introw records the partner’s reply and automatically pushes it into your CRM for full visibility.
- How to use Introw forms
- Embed Introw forms
- Save time with Introw’s AI Agent
- Partner Connect: a 2-way CRM integration with HubSpot
- What is Partner Connect?

---

## Opportunity registration with Introw and Salesforce
Source: https://support.introw.io/en/articles/12233044-opportunity-registration-with-introw-and-salesforce

When you connect Introw with Salesforce, your opportunity registration process via partners becomes seamless and automated. Here’s how it works:
- Opportunity Creation in Introw When a partner submits an opportunity through Introw, the details are captured instantly.
- When a partner submits an opportunity through Introw, the details are captured instantly.
- Automatic Sync to Salesforce The submitted opportunity is automatically pushed to Salesforce. Key fields such as account, contact, deal value, stage, and notes are mapped to your Salesforce Opportunity record.
- The submitted opportunity is automatically pushed to Salesforce.
- Key fields such as account, contact, deal value, stage, and notes are mapped to your Salesforce Opportunity record.
- Real-Time Updates Any updates made in Introw (e.g., changes in deal status or value) are synced with Salesforce. This ensures both systems stay aligned without manual entry.
- Any updates made in Introw (e.g., changes in deal status or value) are synced with Salesforce.
- This ensures both systems stay aligned without manual entry.
- Visibility & Tracking Sales teams can track all registered opportunities directly in Salesforce. Partners see any updates  in Introw, keeping both sides informed.
- Sales teams can track all registered opportunities directly in Salesforce.
- Partners see any updates  in Introw, keeping both sides informed.
- Connecting Salesforce to Introw
- Link your Salesforce opportunities to Introw via custom fields
- Link your Salesforce opportunities to Introw via a relation table
- Salesforce integration overview
- How to use Introw forms with Salesforce

---

## Salesforce integration overview
Source: https://support.introw.io/en/articles/12233861-salesforce-integration-overview

Keep your partner relationships and CRM data aligned with the Introw + Salesforce integration. Automatically sync partner information, leads, opportunities, and cases in real time, so your team can collaborate efficiently, make informed decisions, and grow faster.
Give resellers, referral partners, and distributors a branded portal where they can collaborate on opportunities, support cases, and any custom Salesforce data, without giving them access to your Salesforce and without creating Salesforce users for them.
### Build the partner experience with no-code blocks
- Drag in any section you need: introduction banners with CTAs, dashboards, goal trackers, tiering models, FAQs, documents, videos, and forms.
- Embed any Salesforce data directly into the portal and edit it as easily as you would a document: opportunities, customer lists, lead lists, orders, quotes, any object within your Salesforce environment.
- Apply your own branding (fonts, colors, logo's) and host the portal on a custom domain such as partners.yourcompany.com to make it fully aligned with your brand..
### Run your partner program with agents that act, not just answer.
Introw isn't AI bolted onto a portal, it's agents doing the work, on both sides of the partnership. All enabled in one click. Partners don't just ask questions and self-serve; the agent acts for them: registering deals, submitting forms, and pulling commission or status updates in the flow of conversation. Less manual support on your side.
- AI deal coach on every opportunity : the agent reads each open deal and tells partners what to do next: where it's stuck, what's missing, and the move most likely to advance it. Coaching that used to depend on a partner manager's attention, now on every opportunity by default.
- Agentic deal registration : partners register deals by simply describing them in natural language, or straight from their own Claude or AI agent via the Introw MCP. The agent handles the submission and routes it, no forms to fill, no portal login required. 
- Autonomous approvals : agents react to inbound partner requests on your behalf: deal registrations, MDF requests, partner applications. Set the rules and the agent reviews, responds, and auto-approves what qualifies, so partners get instant answers and your team only touches the edge cases. Learn more 
- Internal AI agent : the prep work that eats a partner manager's week, done for you. It walks into QBRs ready with the numbers, surfaces the opportunities worth chasing, and lays out your day around what actually moves partners. Run it inside Introw, or from your own Claude instance or any MCP-connectable agent. The partner data comes to where you already work, so your team spends time managing relationships, not assembling them. 
- AI-powered LMS : generate full training courses from your website, portal content, or MCP server in minutes: modules, multiple-choice or open-ended quizzes, and certifications you can enroll partners into in a single click. Learn more
### Collaborate on opportunities, leads and any custom object.
- Choose exactly which Salesforce objects (including custom objects), pipelines, stages, and object properties are visible and editable for partners.
- Allow partners to update selected properties, create custom object records like orders for example. That all sync back to Salesforce in real time.
- Add a deal registration form so partners can submit deals that automatically create Salesforce opportunities.
- Trigger automated email updates when an opportunity's stage changes, partners can reply directly from email without logging in to the portal.
- Co-sell in real time: partner comments appear in Salesforce Chatter, and Salesforce stage or property changes flow back to the portal instantly.
### Share sales enablement and support content
- Announcements to publish product updates and news partners need to see.
- Documents and videos to share enablement assets and see how partners engage with each one.
- Support cases to collaborate on issues and resolutions without leaving the portal.
- Projects to assign mutual action items so partners can move tasks through onboarding or joint plans.
### Give partners a personalized view
- Salesforce data fills in dynamically per partner: total revenue, deal count, qualified leads, tier, and any custom KPI.
- Goals update in real time so partners always know where they stand.
- Partners log in through a branded sign-in page you fully control.
### How to setup the integration
- Connecting Salesforce to Introw
- Opportunity registration with Introw and Salesforce
- Tracking Partner involvement on deals
- HubSpot integration overview
- What is Partner Connect?

---

## Keep deals moving with automatic partner notifications
Source: https://support.introw.io/en/articles/12313505-keep-deals-moving-with-automatic-partner-notifications

It’s easy for deals to stall when they stay too long in the same stage. The Sleeping Deal notification helps you keep partners on their toes by automatically sending them a notification when a deal has been inactive in a stage for longer than you define. This ensures partners are reminded to take action, keeping momentum in your pipeline and pushing deals forward. 
See video below ⬇️

### What is a sleepy deal?
A Sleepy Deal is any deal that has remained in the same stage for longer than a defined number of days. With this feature, you can automatically send a notification to your partner to prompt action, keeping your pipeline moving smoothly.
💡 Introw tip: Use shorter time limits in qualification stages to keep momentum, and longer ones in later stages like negotiation.
### How to set it up?
- Within a CRM embed section like a deal pipeline click on Configure .
- Select Notifications .
- Click on the ⚙️ icon next to Sleeping deal
- Setup the conditions and enter the number of days a deal can stay within a certain deal stage(s) .
- Click Save .
An example email of a sleeping deal notification.
### Benefits
- Faster deals to deals move along more smoothly because partners are reminded to take action before they stall.
- Active partners to automatic notifications keep partners engaged and accountable at every stage.
- Clear pipeline to with deals moving consistently, your sales forecast reflects the real state of your pipeline.
- Collaborate on a deal or any other CRM object
- Configure which deal properties to share with your partner
- Partner notifications
- Introw product update - October 2025
- AI Deal Coach

---

## Share assets at scale
Source: https://support.introw.io/en/articles/12321740-share-assets-at-scale

When you want to distribute content to a broad partner audience while still keeping control over who sees what, the available to filters make it easy. You can configure these filters to automatically make assets available to the right group of partners based on attributes like partner tier, partner phase, experience, and partner role . 
### What are asset audience filters?
Asset audience filters are rules you apply to an asset to control which partners can access it. Filters ensure that each partner sees only the content that is relevant to them, based on their profile, role, and data synced from your CRM.
Asset filters can be based on both partner attributes and CRM properties , including:
#### Introw audience filter options
These filters are based on information maintained directly in the Introw platform or in sync with CRM properties (like partner tier and partner role)*.
- Partner Phase Share assets based on where a partner is in their journey  (e.g., Onboarding, Activation, Growth).
- Partner Tier Control access to content by partner tier  (e.g., Silver, Gold, Platinum).
- Partner Categories Use flexible, platform-agnostic categories to group partners in any way that fits your program. Categories are fully customizable and can be defined freely.  Examples: Reseller, Distributor, Technology Partner, Strategic Partner, EMEA Focus, SMB Specialist.
- Experience Ensure assets are visible only to partners within the appropriate partner experience.
- Partner Role Make assets available only to partner contacts with specific roles  (e.g., Sales, Marketing, Solution Architect, Customer Success), ensuring each role gets access to the most relevant materials.
#### CRM Audience fillter Options
These filters use partner data synced from your CRM to refine access further like for example:
- Region or country
- Partner type
- Partner account status
- Custom CRM fields specific to your partner program

#### Embed all assets before applying filters
Before you can use filters, you’ll first need to add your assets into the Experience where they’ll be made available. Once assets are placed within an Experience, asset filters are applied dynamically, meaning that as partners meet the asset filter criteria (based on their phase, tier, role, or experience), they’ll automatically gain access. This ensures that distribution is seamless and continuously updated without requiring you to manually re-share assets.
#### Apply filters to an asset
- Open the asset you want to apply a filter on
- Click the Add filter button next to "Available to"
- Choose one or more filters and set the right values. Partner Phase Partner Tier Experience Partner Role CRM properties
- Partner Phase
- Partner Tier
- Experience
- Partner Role
- CRM properties
- Click Save .
The asset is now only visible to all partners that meet the filter criteria.
❗ Introw remark: When you click Preview on an Experience, the attributes of the partner you select (such as Partner Role, Partner Tier, Partner Phase, and Experience level) will be applied on the assets you will see. This allows you to see exactly which assets that partner would see based on the Available to filters.
### Example Use Cases
- Training Guides → Make onboarding materials available to partners in the Onboarding phase .
- Sales Playbooks → Provide extensive playbooks to your Gold and Platinum partners .
- Technical Documentation → Share advanced integration guides to the Solution Architect partner contact.
- Marketing Kits → Make promotional assets available to the Marketing role in the Growth phase .
- Asset library
- Partner Asset Hub
- Creating Co-branded assets
- Introw product update - October 2025
- Send dedicated partner announcements

---

## Using Introw AI across your partners
Source: https://support.introw.io/en/articles/12381063-using-introw-ai-across-your-partners

With Introw AI, you can now ask any question about your partners and instantly get accurate, actionable answers. Whether you’re a partner manager, revenue ops professional, or part of a channel team, Introw AI becomes your daily assistant for managing relationships and uncovering insights across your entire partner ecosystem.
### How it works
Introw AI is built directly into your Introw workspace. Simply type your question in plain language, and the AI agent will search across your partner data to return clear, usable results.
- Go to your Introw workspace
- Open Introw AI in the navigation bar
- Enter your question or select a suggested question
- Review the answer and take action
### What you can ask
Here are just a few examples of what Introw AI can do:
- Prepare for a QBR meeting with your partner “ Generate a QBR agenda for Partner X.
- Track partner activity “ Show me all inactive partners and suggest next steps. ”
- Understand program tiers “ List all gold-tier partners with their benefits and requirements. ”
These are just starting points, you can ask Introw AI any partner-related question that helps you work smarter.
### Why use Introw AI?
- Faster decisions, no more digging through spreadsheets or reports
- Actionable insights, answers come with context and next steps
- Everyday support, designed for partner managers, RevOps, and channel teams who work with partners daily
### FAQ
Q: What data does Introw AI have access to? A: Introw AI only has access to the data you are already authorized to see. It never pulls in data from outside your account or organization. All integrations respect your existing permissions. More info 
Q: Are my agent conversations shared? A: No. Conversations are private and the Vercel Zero retention AI models (which power Introw AI) do not share your conversation content. More info 
Q: How is the AI protected against malicious inputs (like prompt injection)? A: Introw’s system design, together with Azure’s built-in security mechanisms, protects against abuse, profanity, prompt injection, and other malicious inputs. More info 
Q: What compliance and privacy standards does Introw follow? A: Introw complies with enterprise-grade standards, including SOC 2 and ISO 27001 , and is designed in alignment with GDPR principles. More info
- Add your partners to Introw
- Introw Agent
- AI Agent security at Introw
- Introw + Claude: use cases & what's possible
- Introw's AI Agent in Slack

---

## Use collaborators to ensure partners stay updated on the right deals
Source: https://support.introw.io/en/articles/12430543-use-collaborators-to-ensure-partners-stay-updated-on-the-right-deals

The Collaborators feature in introw.io is designed to keep both your team and your partner contacts aligned on deals. By adding collaborators, you ensure everyone who matters gets automatically notified whenever something changes, making collaboration effortless and transparent.
### What are Collaborators?
Collaborators are the people you bring into a deal (or any other shared CRM object like leads, tickets, etc) to stay up-to-date. They can be:
- Internal team members : colleagues like account executives, sales managers, or cross-functional teammates.
- Partner contacts : external partner contacts who are directly involved in driving the deal forward.
Once added, collaborators automatically receive notifications about updates such as deal stage changes, new comments, or attached documents.
### Why use Collaborators?
Adding collaborators helps you:
- Keep partners informed without endless email threads.
- Ensure stakeholders (both internal and external) are notified when something important happens.
- Improve transparency across your pipeline by making deal progress visible to the right people.
- Save time by reducing back-and-forth updates outside the platform.
### How to add Collaborators
##### Automatic Assignment
Collaborators are added to deals (or other CRM objects created via the form) automatically to reduce manual work:
- The partner contact who registers or submits the deal via a deal form is automatically added as a collaborator.
- The partner manager (internal owner of that partner relationship) is also automatically assigned as a collaborator.
This ensures both the external partner and the responsible internal manager are immediately connected to the deal from the start.
##### Manual Assignment
You can also add collaborators manually:
- Open the deal where you’d like to add collaborators.
- Go to the Collaborators section.
- Search for and select the internal teammate or partner contact you want to add OR
- Once added, they’ll start receiving automatic notifications whenever the deal is updated.
💡 Introw tip: Simply @mention a teammate or partner in the comment section to add them as a collaborator instantly.
### How to remove Collaborators
If a collaborator no longer needs visibility on a deal, you can easily remove them:
- Open the deal and go to the Collaborators section.
- Select the collaborator you want to remove.
- Click the bin icon and confirm the deletion.
They’ll no longer receive notifications or have access to updates for that deal.
No worries, you can always add them back later to keep them updated again.
- Collaborate on a deal or any other CRM object
- Collaborate from inside your HubSpot deals
- Share a deal to partners via Introw's app card in HubSpot
- Deal visibility restrictions for partner contacts
- How does the integration with Microsoft Teams work?

---

## Partner engagement reporting in HubSpot with Introw app events
Source: https://support.introw.io/en/articles/12499113-partner-engagement-reporting-in-hubspot-with-introw-app-events

Introw enables users to track and report on partner engagement directly in HubSpot using a new data source called App Events . As an official HubSpot app, Introw sends key partner engagement data so you can create dashboards and reports on how your partners interact with your portal and content. 
With the App Events data source, you can build reports and dashboards for:
- Partner portal visits to see how often each partner logs in.
- Assets viewed to track which content, resources, or documents your partners engage with the most.
- Activity over time to analyze trends and identify highly active or inactive partners.
These insights help you understand partner behavior, optimize engagement, and measure the impact of your programs.
### Step 1: Include App event data in HubSpot reports
- Go to Reports → Reports → Create custom report .
- Select Create report on your own .
- Add more data sources and include App Events
💡 Introw : The App Events source will include the partner interactions with Introw such as portal visits , assets viewed , comments made, forms submitted and objects updated .
### Step 2: Build your Partner engagement report
- Add the events you want to track, such as Event Count , Event Type , or Event Date .
- Filter by partner, partner type, or time range to focus on the insights that matter.
- Visualize trends using line charts, bar charts, or tables to see engagement over time.
### Step 4: Create Dashboards
- Save your custom report to a dashboard for ongoing visibility.
- Combine multiple partner engagement reports in one dashboard to get a complete view of portal activity.
- Share dashboards with internal teams or managers to track partner ecosystem performance.
App Events cover portal activity like visits, asset views, and form submissions, but partner engagement goes further than that. Introw also syncs course enrollment and certificate data to HubSpot as app objects , giving you a complete picture of how engaged your partners really are.
With the Introw app cards added to your HubSpot records, you can track partner engagement across learning and enablement:
- Course enrollments to see which partners are enrolled, in progress, or have completed training. Spot partners who haven't started onboarding courses or who dropped off mid-way.
- Certificates earned to identify which contacts are fully certified and ready to sell, support, or deliver on your behalf.
Combining App Events reporting with course and certificate tracking gives you a full view of partner engagement, from portal adoption to training completion, all inside HubSpot.
👉 Learn how to set up the Introw course and certificate cards in HubSpot
- Share a deal to partners via Introw's app card in HubSpot
- Introw workflow actions in HubSpot
- Partner activity events in your HubSpot timeline
- Automating workflow actions in HubSpot using Introw App events
- Show Introw course enrollments and certificates in HubSpot

---

## Automating workflow actions in HubSpot using Introw App events
Source: https://support.introw.io/en/articles/12499910-automating-workflow-actions-in-hubspot-using-introw-app-events

With Introw, you can leverage App Events as a trigger for HubSpot workflows. This allows you to automate actions based on partner interactions in your portal, such as portal visits, asset views, or other engagement events.
### How to set it up
##### Create a workflow triggered by App Events
- Go to Automation → Workflows → Create workflow in HubSpot.
- Select Partner or Deal-based workflow , depending on which record type you want to update.
- Under Enrollment triggers , choose App Events .
- Select the specific event type you want to trigger the workflow Introw App events (tracked at both partner company Level and partner contact Level) Portal Visit Triggered when a partner contact logs into or navigates through their dedicated partner portal. Example: A partner sales rep signs in to check the latest partner resources or news  Asset Viewed Captures when a partner contact opens or engages with shared content such as presentations, playbooks, datasheets, or case studies. Example: A partner marketing contacts views a new product brochure before sharing it with their internal sales team.  Form Submitted Recorded whenever a partner contact fills out and submits a form within the platform. A partner sales rep submits a deal registration form for a new opportunity, or a partner BDR completes a lead referral form to pass a prospect over to your sales team.  Deal Closed Won Logged when a partner successfully closes a deal and marks it as “Won.” Example: A partner sales executive reports the successful closure of a customer opportunity, which is then synced to the vendor’s CRM.  Object Updated Tracked when a partner contact edits or updates a shared object such as a deal, ticket, lead, or other collaborative record. Example: A partner adjusts the deal stage from “Negotiation” to “Closed Won” or updates a customer support ticket with additional details.
- Portal Visit Triggered when a partner contact logs into or navigates through their dedicated partner portal. Example: A partner sales rep signs in to check the latest partner resources or news 
- Triggered when a partner contact logs into or navigates through their dedicated partner portal. Example: A partner sales rep signs in to check the latest partner resources or news 
- Asset Viewed Captures when a partner contact opens or engages with shared content such as presentations, playbooks, datasheets, or case studies. Example: A partner marketing contacts views a new product brochure before sharing it with their internal sales team. 
- Captures when a partner contact opens or engages with shared content such as presentations, playbooks, datasheets, or case studies.
- Example: A partner marketing contacts views a new product brochure before sharing it with their internal sales team. 
- Form Submitted Recorded whenever a partner contact fills out and submits a form within the platform. A partner sales rep submits a deal registration form for a new opportunity, or a partner BDR completes a lead referral form to pass a prospect over to your sales team. 
- Recorded whenever a partner contact fills out and submits a form within the platform.
- A partner sales rep submits a deal registration form for a new opportunity, or a partner BDR completes a lead referral form to pass a prospect over to your sales team. 
- Deal Closed Won Logged when a partner successfully closes a deal and marks it as “Won.” Example: A partner sales executive reports the successful closure of a customer opportunity, which is then synced to the vendor’s CRM. 
- Logged when a partner successfully closes a deal and marks it as “Won.”
- Example: A partner sales executive reports the successful closure of a customer opportunity, which is then synced to the vendor’s CRM. 
- Object Updated Tracked when a partner contact edits or updates a shared object such as a deal, ticket, lead, or other collaborative record. Example: A partner adjusts the deal stage from “Negotiation” to “Closed Won” or updates a customer support ticket with additional details.
- Tracked when a partner contact edits or updates a shared object such as a deal, ticket, lead, or other collaborative record.
- Example: A partner adjusts the deal stage from “Negotiation” to “Closed Won” or updates a customer support ticket with additional details.
#### Examples
- Triggers for Marketing & Enablement If a partner views a marketing asset , automatically enroll them in the next marketing sequence If a partner hasn’t visited the portal in 60+ days, start a nurture workflow with fresh content. 
- If a partner views a marketing asset , automatically enroll them in the next marketing sequence
- If a partner hasn’t visited the portal in 60+ days, start a nurture workflow with fresh content. 
- Trigger Onboarding Workflow Enroll the new customer in your onboarding sequence (e.g., welcome email series, training invitations, setup guides).
- Enroll the new customer in your onboarding sequence (e.g., welcome email series, training invitations, setup guides).
- Share a deal to partners via Introw's app card in HubSpot
- Introw workflow actions in HubSpot
- Partner activity events in your HubSpot timeline
- Partner engagement reporting in HubSpot with Introw app events
- Show Introw course enrollments and certificates in HubSpot

---

## Introw product update - October 2025
Source: https://support.introw.io/en/articles/12534233-introw-product-update-october-2025

### Introw AI: ecosystem-wide partner insights
Meet Introw AI, the assistant for partner, channel, and RevOps teams, delivering instant insights across your partner ecosystem. Prepare QBRs in seconds, monitor partner activity and view partner attribution across tiers. All powered by real-time CRM and partner portal data in Introw. Learn more
### Introw app events in HubSpot
We’ve added Introw app events in HubSpot enabling you to track how partners are engaging with your portal and build reports or dashboards to monitor adoption trends. You can also trigger HubSpot workflows automatically based on partner actions done in Introw. Learn more
### Re-engage sleeping deals automatically
With sleeping deal notifications , you no longer need to manually chase stalled opportunities. Introw sends automated, timely notifications to partners when a deal drifts without activity, nudging them to re-engage or take next steps. This helps maintain momentum, keep your pipeline active, and ensure that no deal gets left behind. Learn more

### Additional improvements
Thanks to your continued feedback, Introw is making small but impactful updates that improve performance, usability, and the overall experience
 Show the role of the partner You can show the role your partner is playing on the CRM object by displaying the attribution of the partner (like the role they play).
Resellers and distributors Automatically link HubSpot deals to resellers and distributors with Introw ensuring accurate partner attribution and shared portal visibility without manual updates.  Learn more
Dynamic asset filters Show the right assets automatically to the right partners based on attributes like partner tier, phase, or role and ensure partners always see the right content at the right time .  Learn more
- Introw product update - June 2025
- Introw product update - July 2025
- Introw product update - August 2025
- Introw product update - November 2025
- Introw Product update - December 2025

---

## Tracking Partner involvement on deals
Source: https://support.introw.io/en/articles/12538260-tracking-partner-involvement-on-deals

Introw helps you easily understand and visualize how partners are involved in your deals by re-using the partner attribution setup you’ve already configured in your CRM.
In many CRMs, partner attribution can be configured in several ways, for example, through a property (dropdown, lookup field) such as “Sourcing Partner” or "Partner account" , an association label like “Reseller” or “Partner Influenced” , or a relationship table in Salesforce that defines the role a partner plays, such as “VAR, Reseller, Distributor.” Learn more about partner attribution.  Introw takes this existing data and makes it more intuitive and accessible, transforming these property values into clear partner involvement that both your team and your partners can easily interpret.
### How to do this
Connect Introw to your CRM and configure how your partner attribution is setup within your CRM.  Learn more about partner attribution.
- Re-use your existing setup: Within your Introw integration page you can configure the attribution from your CRM and give it a display name (see video below) 
- Display this on your deals (or any other shared CRM object) Within a deal pipeline overview (in the general overview or within the experience builder) you can visualize the display name of the attribution (see video below). In this example we rename our CRM attribution to "Involvement".
This keeps your existing CRM structure intact while giving partners a more user-friendly and transparent view of how they contribute to each deal.
### Partner Roles & Attribution (Sourced, Influenced, and Beyond)
Introw fully supports multi-partner attribution on Salesforce opportunities, including the common "sourced by one partner, influenced by another" scenario.
Under the hood, this maps to Salesforce's native Opportunity Partner junction object, each partner is linked to the opportunity as a separate record with its own role (e.g. Sourcing Partner, Influencing Partner, Implementation Partner). Introw writes directly to this junction object, so attribution lives natively in Salesforce and flows into your existing reports, commission logic, and forecasting.
On a closed-won opportunity, this means:
- Partner A (sourced the deal) and Partner B (influenced it) are both attached to the same opportunity with their respective roles
- Each partner sees the opportunity in their portal, scoped to the role they played
- Commissions, MDF, and reporting can be split or attributed per role
- New deals or leads submitted via Introw automatically get the correct partner + role written to the junction object
Example of a Salesforce opportunity showing the different roles (attribution) partners played on it.
### Why partner involvement matters
Partner attribution help internal teams and partners alike understand who is involved and how . Examples include:
- Sourced Partner to Introduced the opportunity.
- Influencing Partner to Provided advisory or technical influence.
- Reseller to Selling directly to the customer.
- Technology Partner to Enhances the offer through integration.
By making this information clear and consistent across Introw it enables:
- Better visibility into each partner’s contribution.
- More accurate insights on partner influence and revenue attribution.
- Improved partner experience through transparent, contextual insights.
- How partner deal data syncs to your CRM
- Configure the deal name of your partner deals.
- Deal visibility restrictions for partner contacts
- Automatically attribute resellers and distributors in two-tier channel deals
- Partner Connect: a 2-way CRM integration with HubSpot

---

## My partner does not receive any emails
Source: https://support.introw.io/en/articles/12549379-my-partner-does-not-receive-any-emails

If your partners aren’t receiving emails or notifications from Introw PRM, it’s usually because their email provider or company security settings are filtering them out, sometimes into Spam , Junk , or Promotions folders. 
### Why this happens
Introw PRM automatically sends notifications to partners to keep them engaged, such as portal invites, announcements, comments, or CRM updates.
These notifications are sent from: 📧 [email protected]
Depending on the recipient’s email system, messages can:
- Be marked as spam or promotional
- Be blocked by corporate filters
- Require the domain introw.io to be whitelisted
- Or, in some cases, the partner may have unsubscribed from Introw emails
### How to solve this
##### Step 1: Ask your partner to check their Spam or Junk folder
- Have your partner open their Spam or Junk folder.
- Ask them to look for messages from [email protected] .
- If they find one, they should click “Not spam” or move it back to their inbox.
💡 Gmail often shows a banner that says:  “Why is this message in spam? Similar to messages that were identified as spam.”
(Insert mockup image here to Gmail spam banner with an Introw email)
##### Step 2: Ask them to whitelist Introw’s email address
Whitelisting ensures future messages always arrive safely. 
For Gmail users
- Open Gmail.
- Click the ⚙️ Settings icon → See all settings → Filters and Blocked Addresses .
- Click Create a new filter . 
- In the From field, enter: [email protected]
- Click Create filter .
- Check “Never send it to Spam.”
- Save the filter.
##### For company or organization email systems
If your partner uses a business domain (e.g., Google Workspace, Microsoft 365, or a custom mail server), their IT department may need to whitelist:
introw.io
and specifically:
[email protected]
This ensures Introw messages are trusted and not blocked by company firewalls or security software.
##### Step 3: Check Promotions or Other tabs
In Gmail and Outlook, automated messages can sometimes appear under Promotions or Other tabs. Partners can move one of these messages to their Primary inbox to train their filter to recognize it next time.
##### Step 4: Confirm the partner has not unsubscribed
Sometimes, a partner may have intentionally unsubscribed from Introw notifications in the past. When this happens, we can’t deliver any further messages to that email address until they resubscribe.
If all the previous steps haven’t helped, the partner (or you on their behalf) should contact our support team at: 📩 [email protected]
We can check the subscription status and help restore email delivery if needed.
- Send notifications from your own email domain

---

## Partner detail
Source: https://support.introw.io/en/articles/12622728-partner-detail

The Partner Detail view provides a complete and actionable overview of each partner, from performance metrics to attributed deals, task progress, and collaboration. Designed as an operational hub for partner managers, it centralizes everything needed to manage partners efficiently without switching contexts
### A more insightful general page
The General tab now gives a clear snapshot of your partner’s performance and engagement. You’ll find the most relevant, actionable information surfaced in one place, including:
- Revenue: Track the partner’s contribution to your business.
- Engagement: Understand how actively the partner is collaborating and driving activity.
- Inactive or Overdue Deals: Identify deals that need attention and keep pipeline momentum on track.
- Task Progress: Monitor ongoing initiatives and follow up on what’s next.
These updates align the Partner Detail with the Home experience, offering a consistent and focused view of partner performance across the platform. 
### Manage and collaborate on all partner attributed CRM Objects
You no longer need to enter the partner portal to see which CRM objects are shared or attributed to a partner. From the Partner Detail , you can now view and collaborate on all linked CRM objects, not just deals and opportunities but also leads, contacts, and tickets, all in one place.
The Deal tab and other attributed CRM objects display everything attributed to the partner, including key details such as for example:
- Name and status
- Owner
- Amount
- Close date
- Last activity
The properties shown for each object are configured through the general CRM object overview (e.g., Deals, Leads, Contacts, Tickets) and apply automatically to all partners. 
### Quick actions
In addition to insights and deal visibility, the partner detail now includes Quick Actions to help you take immediate action with your partners:
- Send a Message: Reach out directly to the partner from the partner detail page.
- Add a Task: Create new tasks to track follow-ups or next steps.
- Add a Note: Capture important context or updates in one place.
- Invite to Portal: Quickly send an invitation for the partner to join the portal.
These actions let you manage communication, tasks, and onboarding without leaving the Partner Detail, keeping all partner-related activity centralized and accessible.
- Share a deal to partners via Introw's app card in HubSpot
- Partner notifications
- Save time with Introw’s AI Agent
- AI agents that actually take action for your partners
- Partner Connect: a 2-way CRM integration with HubSpot

---

## Create and manage views in the partner overview
Source: https://support.introw.io/en/articles/12634126-create-and-manage-views-in-the-partner-overview

The Partner overview gives you a complete picture of all your partners. To make it easier to focus on what matters most, you can use Views which is a saved combination of filters that you can save and access anytime.
### How to create a view
- Go to your Partner Overview .
- Use the filter options at the top (e.g., Tier, Country, Experience) to narrow down the partners you want to see.
- Once your filters are set, click Create view . 
- Give your view a clear name (e.g., “Gold Partners” or “EMEA Partners”). 
- Choose whether you want to save it as: Private View to visible only to you. Shared View to shared with all partner managers in your organization.
- Private View to visible only to you.
- Shared View to shared with all partner managers in your organization.
- Click Save .
Your new view will now appear in the Views tabs for quick access.
### Updating a View
You can change an existing view anytime:
- Open the view.
- Add, remove, or adjust filters as needed.
- Click Save View to update it.
For example, you can add Type = reseller to your “Gold Partners” view and save it again. 
### Managing Your Views
Click the three dots next to any view name to:
- Rename the view
- Duplicate it (create a copy including all filters)
- Remove it if you no longer need it
- Segment based access control
- Managing partner contacts
- Create and configure partner goals
- Create and manage views in the Deal Overview
- How to create a dashboard?

---

## Introw product update - November 2025
Source: https://support.introw.io/en/articles/12752596-introw-product-update-november-2025

### New partner detail
The new Partner detail view gives you a complete snapshot of every partner from recent activity and open deals to shared assets and performance metrics. No more jumping to their portal as you can now easily spot stalled deals , see where partners are falling behind on tasks , and keep every partnership moving forward, all in one place. Learn more
### Saved views on partners overview
Tired of re-applying filters every time you check your partners? With Views , you can now save your preferred filters in the partners overview. Whether it’s a list of inactive partners, gold-tier partners, or partners by region, your custom views are just one click away, making it easier to stay organized and focused on what matters most. Learn more
### Configurable dashboard sections
We’ve added new configuration options to Introw’s dashboard section, giving you full control over how partnership performance is shared with your partners. Introw pulls data directly from your CRM and turns it into meaningful metrics that match your partnership goals. Choose which pipelines or deals to include, set default time ranges, and define how results are aggregated, by Deal Amount, ARR, or any key deal property. You can even add multiple dashboard sections to tailor each partner portal to your needs. Learn more
### Additional improvements
Thanks to your continued feedback, Introw is making small but impactful updates that improve performance, usability, and the overall experience
 AI Agent Integrations via MCP Extend Introw’s AI Agent by connecting it with external knowledge bases and tools via an MCP server (Model Context Protocol). Learn more
 Internal collaborators are also notified whenever a comment is added to a deal or a deal is updated, keeping everyone in the loop and on track.
 
- Introw product update - October 2024
- Introw product update - March 2025
- Introw product update - May 2025
- Introw product update - October 2025
- Introw product update - March 2026

---

## Create dynamic partner conversion links
Source: https://support.introw.io/en/articles/12919444-create-dynamic-partner-conversion-links

Introw enables partners to receive a dynamic conversion link that can be used to track signups, trials, or demo bookings at scale. This feature removes lots of manual work, reduces data-entry errors, and ensures every lead or signup can be accurately associated with the correct partner record through your CRM workflow.
### What is a dynamic conversion link?
A dynamic conversion link is a customizable URL that partners can use in campaigns, emails, social media posts, website buttons, or landing pages. These links are automatically populated with partner-specific identifiers, such as UTM parameters or other tracking tags, so that when a prospect clicks the link and completes an action (e.g., signing up or booking a demo), the source partner can be accurately captured by your tracking systems.
This enables:
- Reliable partner attribution using your existing analytics or CRM workflows
- Reduced manual data entry , since partner identifiers are embedded directly in the link
- Cleaner reporting and routing , based on consistent tracking data
- More scalable co-marketing and demand-generation programs , because each partner can use a unique, trackable link 
### How It Works
Inside Introw’s link builder, you define a base URL (e.g. signup or demo booking page) with fixed parameters or include variable attributes such as: Partner Id, Partner Name, Contact Email or Partner CRM ID (which corresponds with the object ID of your partner in your CRM system). 
Introw replaces these placeholders with the correct values for each partner. 
Each partner will get that fully generated, ready-to-share version of the link complete with their specific attributes included.
#### Supported dynamic attributes include:
1. Partner Name
- Automatically inserts the partner’s name.
- Helpful for readability and campaign personalization.
2. Partner CRM ID (CRM Object Record ID)
- Inserts the exact CRM company record ID for the partner.
- Extremely powerful as it ensures incoming conversions contain the necessary data so they can be tied to the correct CRM partner account via your workflow.
3. Partner Contact Email
- Adds the partner contact's email address.
- Enables advanced routing, notifications, and tracking based on contact-level attribution.
4. Partner ID
- Inserts the partner’s unique identifier within Introw.
- Provides an additional, system-native tracking mechanism that can be used for attribution, reporting, and internal workflows independent of CRM configuration.
- Partner journeys
- Introw product update - October 2025
- Automatically attribute resellers and distributors in two-tier channel deals
- Linking deals to leads via Introw
- Affiliate link management in Introw

---

## Partner goals
Source: https://support.introw.io/en/articles/12975803-partner-goals

Introw’s Goals feature allows you to easily set, track, and manage objectives for your partners. These goals help align partner efforts with your strategic priorities, monitor progress over time, and provide partners with clear milestones to work toward.
📹 Learn more in this quick walk through video ⬇️ 
#### What are Partner Goals?
Introw's partner goals are performance targets that update automatically using real-time data from your connected CRM (such as HubSpot or Salesforce). Instead of asking partners or partners managers to report progress manually, Introw pulls the latest data directly from your CRM and displays them in your partner’s goals overview.
These goals can help you measure:
- Referrals submitted
- Qualified leads created
- Revenue sourced or influenced
- Tickets resolved
- etc .
Because the data comes directly from your CRM, it’s always accurate, up-to-date, and standardized across all partners.
#### How to create Partner goals
- Define what you want to measure Set the core details of your goal: its name, visibility, and the CRM object or metric to track, such as revenue, pipeline, or activities. Refine what counts toward the goal by choosing which partner attributions to include, how progress is calculated (count or sum), which date property determines eligibility, and any filters that narrow the data to what truly matters. 
- Select a timeframe Define how often the goal is defined by choosing a custom, monthly, quarterly, or annual frequency.
- Choose who the goal applies to Decide whether the target type  should be partner specific or defaulted for an an entire tier of partners.
- Set the target Enter the numerical target you want partners to reach, whether that’s a revenue amount, the number of sourced opportunities, or activity-based metrics. You can set a default value for all new partners that get the goal assigned or set values for each partner that override the default value. 
- Assign the goal Once assigned, partners can view their progress in real time on their Introw portal, automatically updated from your CRM. You can assign goals in bulk based on experience, tier, partner manager, phase or partner category.
- You can assign goals in bulk based on experience, tier, partner manager, phase or partner category.
- Track performance of the goal You can monitor goal progress both from the main goals overview and within each partner’s detail page. Introw users can see exactly which CRM records contribute to a partner’s progress, ensuring full transparency into how results are calculated. 
- Clicking on any goal card opens a detailed view showing the underlying records, allowing you to quickly validate performance and understand what is driving the numbers. 
### How the partner goal status is calculated
Goal status shows how your partners are progressing toward the targets you’ve set. It compares their actual progress to what they are expected to achieve at that point in time:
- Not started to The goal hasn’t started yet.
- On track to The partner is meeting or exceeding expected progress.
- Behind to The partner is slightly behind schedule (less than 50% behind expected progress).
- Critical to The partner is 50% or more behind expected progress.
- Achieved to The goal has been fully completed.
- Ended to The goal period has ended without being fully achieved.
For example, if a partner has a monthly goal of $100k in ARR and it’s the 14th (halfway through the month), they would be expected to have closed about $50k :
- $50k or more → On track
- Slightly under $50k → Behind
- $25k or less → Critical
This gives you a clear view of which partners are on pace and where additional support may be needed. 
- Partner Tiers
- Partner training courses
- Create and configure partner goals
- Edit the goals of your partner
- Everything Your Partners Can Do in Introw

---

## Partner training courses
Source: https://support.introw.io/en/articles/12976763-partner-training-courses

Introw courses give you a powerful, built-in LMS to train, enable, and certify your partners. With AI-generated course content, quizzes, and certification tools, you can deliver structured learning experiences that help partners better understand your product, processes, and value proposition. 
Introw courses lets you create and deliver organized training content directly inside the Introw partner platform. Whether you need a simple onboarding module or a full certification pathway, Introw Courses gives you the tools to design, publish, and measure training at scale without relying on external LMS systems.
### Introw courses (LMS) module includes:
- AI-Driven Course Builder
- Module & Lesson Creation
- Quiz & Assessment Tools
- Certificates for Partner Completion
- Partner Progress Tracking
Courses are delivered entirely within Introw, making training accessible to partners without additional logins or systems.
Create high-quality courses in a few seconds. Enter a topic, goal, or outline, and the AI builder will generate:
- A clear course structure
- Modules and chapters
- Draft content
- Suggested quiz questions
Courses aren't only generated by AI, they can also be edited via the AI agent . Instead of changing each block manually, just describe what you want in natural language and the agent updates your course for you. Everything the AI agent produces stays fully editable, so you can review and refine it at any time. With the AI agent you can:
- Edit lesson and chapter content via chat prompts
- Add, reorder, rename, or remove modules and chapters
- Generate or revise multiple-choice and conversational AI quizzes
- Create and edit visuals such as images
For an even richer and more authentic learning experience, Introw offers AI-powered conversational assessments or quizzes . Instead of only selecting answers from a predefined list of options, partners can interact naturally to your AI agent that simulates real learner interactions. The system evaluates understanding based on clarity, accuracy, and confidence allowing partners to prove their knowledge in a dynamic, scenario-based format.
Introw provides complete visibility into how partners engage with your training. 
Administrators can track individual and team-level progress across every course, including enrollment status, lesson completion, quiz performance, conversational-quiz outcomes and certification achievements.
Award certificates automatically when partner contacts:
- Complete all lessons
- Pass all required quizzes
Certificates can be downloaded and stored in their partner profile.
Courses in Introw have two statuses: Draft and Active . A course is shown as Active only when at least one learner is enrolled in it. There is no separate "deactivate" option, but you can effectively move a course back to Draft status by unenrolling all its learners.
To unenroll a learner from a course:
- Open the course and go to the Enrolled tab.
- Click the three-dot menu (⋮) next to the learner you want to remove.
- Select Unenroll .
Once all learners have been unenrolled, the course will return to Draft status and will no longer be visible to partners.
- How to use Introw's course builder
- Course Settings
- Partner certificates
- Using the AI Conversational Quiz
- Build a training curriculum with sequential courses

---

## How to use Introw's course builder
Source: https://support.introw.io/en/articles/12976824-how-to-use-introw-s-course-builder

Our AI Course Builder makes it easy to create a complete course outline in minutes. Whether you're starting from scratch or refining an existing structure, you can generate, review, and customize every part of your course. This guide walks you through each step.
Go to Portal → Courses and click Create Course . You'll be prompted to pick one of two paths:
Introw course builder
SCORM Import
Best for
Building a course from scratch or a prompt
Reusing content built in Storyline, Rise, Captivate, etc.
How it works
AI generates a full outline you can edit freely
Upload a .zip package, it runs as a full embedded LMS experience
Assessments
Multiple choice & Conversational AI quizzes
Managed inside your SCORM package, not tracked in Introw
Progress tracking
Full tracking, course progress, quiz results & scores
Enrollment status only (Not Started, In Progress, Completed)
Both options live inside the same Courses module, so your partners access everything from one place, regardless of how the course was built.
Our AI Course Builder makes it easy to create a complete course outline in minutes. Whether you're starting from scratch or refining an existing structure, you can generate, review, and customize every part of your course.
### Step 1: Create a course
- Go to Portal → Courses
You can choose between:
- A predefined AI course prompt (Sales training, technical support, product training) which you can adjust to your liking.
- Start from scratch
🤖 Introw AI tip: Provide clear context and a defined role , break down complex tasks into sequential steps , and specify the desired output format and constraints .
The AI course builder will generate a full course outline, but you can freely edit everything after generation. A default Introw course outline will contain:
- 6 modules each containing 3 chapters
- Lesson content within each chapter
- Assessments (Quiz) as the third chapter of each module
You can freely adjust the prompt to include more or fewer modules, chapters, or assessments, or edit everything after generation.
### Edit courses with the AI agent (for Introw courses only)
Beyond the manual editing tools, you can change any Introw-built course simply by asking the built-in AI agent . Describe what you want in plain language and the agent applies the changes directly to your course, no need to edit each block by hand. Everything the AI agent produces stays fully editable, so you can always review and fine-tune it afterwards. 
With the AI agent you can:
- Edit content via chat prompts to Ask the agent to rewrite, expand, shorten, or reword lesson and chapter content in natural language. 
- Add & restructure modules and chapters to Have the agent add, reorder, rename, or remove modules and chapters to reshape your course outline. 
- Generate & edit quizzes to Create new multiple-choice or conversational AI quiz questions, or revise existing ones, on request. 
- Create & edit visuals to Generate or update images and other visuals directly within your chapters. 
### Step 2: Review your course outline
A course outline is structured into modules , each with its own title, and every module contains a series of chapters , each with a chapter name. This hierarchy helps learners clearly understand how the course is organized and how each chapter fits into the bigger picture.
By default, every chapter content page displays a header that includes the module name , the chapter name , and the learner's progress within that module . This built-in navigation ensures a consistent, intuitive learning experience, helping learners stay oriented, track their progress, and easily follow the intended flow of the course.
After generating your course outline, you can quickly customize each module or chapter using the three-dot menu to:
- Add Chapter to Insert a new chapter directly below the selected one.
- Colorize to Choose a background color to personalize that chapter.
- Rename to Update the chapter title anytime.
- Duplicate - Save time by duplicating a chapter or module to keep the same structure within your course.
- Delete to Remove the chapter from your course.
You can also drag and reorder chapters or modules to create the perfect learning flow.
### Option B: Import a SCORM File
Already have training content built in tools like Articulate Storyline, Rise, Adobe Captivate, or iSpring? You can import it directly into Introw as a SCORM package. The entire experience is embedded and runs natively inside Introw's LMS, your partners never leave the portal.
#### Step 1: Upload your SCORM package
- Click Create Course and select Import SCORM
- Upload your .zip SCORM package (SCORM 1.2 and SCORM 2004 are supported)
Introw will process and validate your package automatically. Once uploaded, it will appear as a course in your Courses list.
#### Step 2: Configure your course settings
Once imported, you can configure the same course settings available for AI-generated courses:
- Course Name & Description to Set a clear title and summary.
- Thumbnail to Add a cover image to represent your course.
- Due dates to Set a deadline for completing the course.
- Enrollment Filters to Control which partners can access the course.
- Certificates to Enable automatic certificates upon course completion.
Note: SCORM courses run as a self-contained experience. The navigation, interactions, and assessments are all driven by your SCORM package itself, Introw handles the embedding and enrollment tracking.
#### Step 3: Track learner progress
Introw tracks each partner's progress through their SCORM course journey. You can see the following statuses from the Courses dashboard:
- Not Started to The partner has been enrolled but hasn't opened the course yet.
- In Progress to The partner has started but not yet completed the course.
- Completed to The partner has finished the course.
To create a new chapter, open the three-dot menu on any existing chapter and select Add Chapter . A list of predefined chapter sections will appear, allowing you to choose the layout that best fits your content. 
Examples of predefined content blocks within a chapter
#### Text & Images
Create rich, engaging chapters with a combination of text blocks and images. This section is ideal for explanations, storytelling, visual walkthroughs, or showcasing examples that support your lesson.
#### Collapsible Content, Product Overviews & Call-to-Action Buttons
Use collapsible sections to present information in a structured, easy-to-navigate way. perfect for FAQs, detailed breakdowns, or step-by-step guides. Add product overview modules to highlight key features or benefits, and include call-to-action buttons to guide learners toward next steps or external resources.
#### Multi-Column Layout (Image & Text)
Present content side-by-side with a clean multi-column layout. Pair an image with text for comparisons, instructions, feature highlights, or any scenario where visuals and explanations work best together.
#### Video
Add dynamic learning experiences by embedding videos from platforms like YouTube, Vimeo, or Loom. You can also upload your own videos directly with a limit of 2GB per file. This course section is perfect for demonstrations, lectures, walkthroughs, or personal introductions.
### Assessment or Quiz options
Standard Quiz (Multiple Choice with AI Feedback): Include interactive multiple-choice questions, supported by AI-generated feedback to help learners understand correct answers and reinforce learning. 
Conversational AI Quiz (Open-Ended Questions): Engage learners with open-ended assessments where AI provides conversational, personalized feedback. This format encourages deeper thinking and meaningful reflection. 
Limit question attempts:
- Multiple Choice: Set the number of times learners can retry each question.
- Conversational AI: Define the number of messages a learner can send to the AI agent.
This ensures learners have guided opportunities to practice and reinforce their understanding while staying within the intended limits.
### Edit chapter content
You can replace placeholder elements with your own text, images, or videos, and adjust the layout as needed. Every chapter is fully editable, giving you flexibility to refine your content, update materials, or restructure sections at any time as your course develops.
Whether you used the AI builder or imported a SCORM file, you can configure the course settings to control how learners experience your course.
For a full guide on all course settings, including detailed explanations and advanced tips, see our separate article: Course Settings
 Basic Settings
- Thumbnail to Add an image that represents your course. The aspect ratio for course thumbnails is 3/1 (so for example 3000x1000 would be a good resolution)
 Advanced Settings
- Due dates & Passing Score to Control how learners complete assessments.
- Button Labels to Customize action buttons (e.g., "Start Course," "Next Lesson") to fit your course style.
- Enrollment Filters to Manage which partners can access the course.
- Certificates to Enable automatic certificates for course completion.
- AI Features to Set a personalized Agent welcome message.
Can I export an Introw course as a SCORM file? No. Introw supports importing SCORM files only. Introw content cannot be exported as SCORM.
Can I add additional content to a SCORM module? No. Content inside a SCORM module is fully controlled by the SCORM file itself. You cannot add Introw blocks or other content within the same module. If you need additional content alongside a SCORM file, put it in a separate Introw module.
My SCORM file isn't displaying correctly. What should I check?
- Confirm the file was published as SCORM 1.2 or SCORM 2004 (not xAPI/cmi5)
- Confirm you're uploading the .zip file directly, do not unzip it first
- Check that the zip file includes an imsmanifest.xml at the root level; if it doesn't, the package wasn't exported correctly
- If published from Articulate, re-export using the LMS output type and re-upload
- Partner training courses
- Course Settings
- Show Introw course enrollments and certificates in HubSpot
- Show Introw course enrollments and certificates in Salesforce
- SCORM Files & Introw Courses

---

## How to create a partner certificate
Source: https://support.introw.io/en/articles/12976845-how-to-create-a-partner-certificate

Certificates allow you to officially recognize partners who complete your training or master the needed skills to sell or support your product or service. You can enable certification for any course and set the criteria required to earn it.
### Create a certificate
Click Create Certificate and define the following:
- Certificate Name Example: "Certified Product Specialist"
- Validity Period Example: valid for 1 year
- Issued by Example: dynamic person like the partner manager or a specific person who always appears as the certificate issuer, for example: Head of partnerships, CEO, etc.
Once the certificate is created, you can update its description or branding at any time. This includes:
- Editing the certificate description
- Updating branding elements such as: Background color Custom background image
- Background color
- Custom background image
Edits take effect immediately and will appear on all newly issued certificates.
Note : Previously issued certificates are not updated retroactively.
### How certification works
Partners can receive a certificate when they:
- Complete a course
- Pass all required quizzes
- Get one assigned manually via the peopel list on the partner detail page.
Certificates are generated automatically and stored in the partner's dashboard.
### Give certificates
- Go to Portal > Certificates
- Choose your certificate
- Give them to uncertified partner contacts
Issue and notify the partner contacts about the certificate
Once issued, partners can access it from the partner portal or download it directly from the certification email. 
Once your partner has earned a certificate, they can share it directly from your partner portal to LinkedIn. This is a quick way to showcase their achievement, highlight expertise, and celebrate their partnership with your brand.
#### How it works:
- Your partner logs into the portal you provide.
- They navigate to their certificate and click Share on LinkedIn . 
- LinkedIn opens with a pre-filled post including the certificate image. 
- They can customize the message and publish it to their network.
Sharing certificates helps increase visibility for both your partners and your brand while making it easy for partners to promote their success.
### Adding the issuing organisation's logo on LinkedIn
Introw sends the issuing organisation name to LinkedIn when a certificate is shared. However, LinkedIn does not automatically display the organisation's logo based on the name alone.
To have the logo appear on the certificate in LinkedIn, your partner can follow these steps:
- Go to their LinkedIn profile and open the Licenses & Certifications section.
- Click on the certificate they just added.
- In the Issuing organization field, search for and select your company from LinkedIn's suggestions.
- Once selected, LinkedIn automatically populates the certificate entry with your organisation's logo.
Tip : Make sure your company has an active LinkedIn Company Page with a logo uploaded. LinkedIn pulls the logo directly from your Company Page, so it needs to be set up for the logo to appear.
- Create partner portal from within HubSpot
- Create a Partner portal experience
- Create new partners via Introw
- Introw workflow actions in HubSpot
- Partner certificates

---

## Enrolling partners into courses
Source: https://support.introw.io/en/articles/12981492-enrolling-partners-into-courses

Quickly add partner contacts and notify them about courses they need to take. Courses can be ready in the portal and enrolled ahead of time without notifying partners, giving you the flexibility over when notifications are sent. 
### Enrollment from within the course
Step 1: Open the course detail and click Enroll 
Step 2: Select the users you want to enroll
- Individual partner contacts
- Entire sets of partner contacts based on filters like: Partner tiers - learn more Specific partner roles (e.g., sales, technical, onboarding) - learn more
- Partner tiers - learn more
- Specific partner roles (e.g., sales, technical, onboarding) - learn more
Step 3: Enroll and notify (optional) the selected partner contacts
- Enroll and notify partner contacts they are enrolled in the selected course.
- Notifying contacts is optional because you can enroll all partner contacts before launching their partner portal. This allows courses to be available in the portal without sending emails in advance, giving you the flexibility to control when contacts are notified. 
### Enrollment from within the partner detail
You can enroll partner contacts into courses directly from a partner’s detail page, making it easy to manage each partner individually. This approach allows you to select specific courses for a partner and optionally notify them immediately, keeping course assignments organized and streamlined. It also provides the flexibility to prepare content in advance, so partners have everything ready when they access their portal.
Step 1: Select the partner contacts you want to enroll 
Step 2: Select which course you want to enroll your partner in
- Enroll and notify the partner contacts they are enrolled in the selected course.
- Notifying contacts is optional because you can enroll all partner contacts before launching their partner portal. This allows courses to be available in the portal without sending emails in advance, giving you the flexibility to control when contacts are notified.
You get a notification email when a partner contact effectively starts the course
- Partner training courses
- Course Settings
- Show Introw course enrollments and certificates in HubSpot
- Show Introw course enrollments and certificates in Salesforce
- Build a training curriculum with sequential courses

---

## Create and configure partner goals
Source: https://support.introw.io/en/articles/12982099-create-and-configure-partner-goals

When creating a new goal in Introw, you define exactly what you want to measure, how it should be counted, and who can see it. Goals are powered directly by your CRM data and can track any object, metric, or partner-related activity available in your CRM. 
#### Step 1: Name and describe our Goal
Give your goal a clear and meaningful name and an optional description. Examples:
- Revenue target 2025: Amount of revenue to be closed won via partners
- X-mas lead goal: Register 5 new leads before Christmas
The name appears in all overviews, details, and partner views (if visible externally).
#### Step 2: Set the visibility
Choose who should be able to see the goal:
- Public This goal is visible to Introw users and partners via a goal section in the partner experience . Learn more
- This goal is visible to Introw users and partners via a goal section in the partner experience . Learn more
- Internal This goal is for internal team use only and will not be visible to the partner .
- This goal is for internal team use only and will not be visible to the partner .
Visibility can be changed later without affecting the goal’s data.
##### Step 3: Select the attributed CRM object you want to track
Select the CRM object that is attributed to partners and you want to measure.
By default Introw will include all attributions but if you want you can create a goal that only takes into account specific attributed deals for example.
- Deals or opportunities
- Leads
- Tickets or cases
- Any custom object in your CRM
#### Step 3: Configure how the goal is calculated
Here you define what and how goals gets counted , which date determines inclusion , and which records qualify . These three settings work together to define exactly which records count toward your goal. 
- Aggregation method ( how progress is measured Count : Number of objects (e.g. Leads registered this quarter) Sum : Total of a numeric field (e.g., deal amount) 
- Count : Number of objects (e.g. Leads registered this quarter)
- Sum : Total of a numeric field (e.g., deal amount) 
- Date property ( which timestamp to evaluate ) The date property determines which date field of your object is used to determine when a record falls inside your goal ’s timeframe. E.g. Created Date, Close date (“deals closed this month”)
- The date property determines which date field of your object is used to determine when a record falls inside your goal ’s timeframe. E.g. Created Date, Close date (“deals closed this month”)
- E.g. Created Date, Close date (“deals closed this month”)
- Filters ( which records qualify) Apply filters to include only relevant items, such as: E.g. Deal Stage = Closed Won E.g. Opportunity type = New opportunity 
- Apply filters to include only relevant items, such as: E.g. Deal Stage = Closed Won E.g. Opportunity type = New opportunity 
- E.g. Deal Stage = Closed Won
- E.g. Opportunity type = New opportunity 
- Aggregation property ( which property to use for the aggregation of data) Choose which numeric property Introw should use to calculate a sum. Examples: E.g. Deal Amount E.g. ARR E.g. Number of subscriptions
- Choose which numeric property Introw should use to calculate a sum. Examples: E.g. Deal Amount E.g. ARR E.g. Number of subscriptions
- E.g. Deal Amount
- E.g. ARR
- E.g. Number of subscriptions
#### Step 4: Choose a frequency and time range
Select a frequency and time range to define how often the goal repeats and which records count toward achieving it.
Frequency
Set a recurring frequency to quickly create recurring goals at scale, such as:
- Monthly goals
- Quarterly goals
- Annual goals
Example: “Partners must register 3 new leads every month.”
This is ideal for partner performance rhythms and automated recurring measurement.
Time Range
Defines when a record must fall with the previously selected date property to count toward the goal. Also determines when a goal is considered Not started, On track, Behind 
Example: “Track all partner-sourced created deals between Jan 1 and Mar 31.”
#### Step 5. Define the target type and values
Choose how targets are assigned:
- Tier-Based Target: Apply the same target to all partners in a tier (e.g., all Gold partners must achieve 10 deals per quarter).
- Partner-Specific Target: Each partner has their own personalized target. You can also define a default target for new partners automatically.
- Adding a partner override : For partner-specific goals, you can adjust the default targets individually for each partner.
- Example: Most partners have a target of 10 deals, but Partner X has a target of 15 deals due to higher capacity or a better joint value proposition or co-marketing activities.
- This allows scaling personalized goals while still managing them efficiently.
### How the partner goal status is calculated
Goal status shows how your partners are progressing toward the targets you’ve set. It compares their actual progress to what they are expected to achieve at that point in time:
- Not started to The goal hasn’t started yet.
- On track to The partner is meeting or exceeding expected progress.
- Behind to The partner is slightly behind schedule (less than 50% behind expected progress).
- Critical to The partner is 50% or more behind expected progress.
- Achieved to The goal has been fully completed.
- Ended to The goal period has ended without being fully achieved.
For example, if a partner has a monthly goal of $100k in ARR and it’s the 14th (halfway through the month), they would be expected to have closed about $50k :
- $50k or more → On track
- Slightly under $50k → Behind
- $25k or less → Critical
This gives you a clear view of which partners are on pace and where additional support may be needed.
- Partner Tiers
- Partner notifications
- Tracking Partner involvement on deals
- Partner goals
- Edit the goals of your partner

---

## Edit the goals of your partner
Source: https://support.introw.io/en/articles/12982846-edit-the-goals-of-your-partner

You can view and modify a partner’s goals directly on the Goals Detail page. Adjusting partner goals lets you update target values to reflect changes throughout the year, such as marketing campaigns, additional resource allocation, or enhancements to the joint value proposition. Note that only partner-specific goals can be edited, while partner tier goals apply to multiple partners and cannot be changed individually.
Navigate to the Goals page
- Go to your goals list and select which goal you want to review.
View a specific goal
- In the Goal Detail page, locate the Partner and select them.
- With our Partner access permission , you can allow Introw users to only see the goals of their assigned partners. Learn more
💡 Introw tip : With our Partner access permission , you can allow Introw users to only see the goals of their assigned partners. Learn more
Edit the target values
- Update the target values as needed to reflect changes in your strategy or partnership, such as: Launching a marketing campaign Allocating additional resources to the partner Improved integration that enhances the joint value proposition
- Launching a marketing campaign
- Allocating additional resources to the partner
- Improved integration that enhances the joint value proposition
Save changes
- After updating the values, click Save changes to apply your changes. The partner’s goals are now updated with the new targets.
- Add your partners to Introw
- Managing partner contacts
- Partner goals
- Partner training courses
- Create and configure partner goals

---

## Course Settings
Source: https://support.introw.io/en/articles/12988061-course-settings

In the top-right corner of the course builder, access the main course settings. After creating your outline and content, configure these settings to control learner experience, track progress, and manage certifications. The AI Course Builder makes it easy to set up both basic and advanced options for a professional, engaging course. 
- Go to Portal → Courses .
- Open the course you want to configure.
- Click Configure ( represented by the gear icon).
Here, you can adjust everything from the course title and description to advanced features like AI guidance and enrollment filters.
These settings help you define and showcase your course so learners can quickly understand and access it. The title, description, and thumbnail will appear in the portal, course catalog, and email notifications .
- Course name: Clear and concise, appears in catalog, dashboards, and notifications.
- Description: Brief, engaging, learner-focused; include prerequisites or audience.
- Thumbnail: High-quality image representing the course. For the best result in the partner portal, use a 4:1 ratio.
These settings allow you to control course deadlines and assessment requirements , helping ensure learners complete courses on time and achieve the intended learning outcomes. 
 Due Dates to Set deadlines for course completion:
- Relative Date: Specify a number of days after a learner enrollment.
- Fixed Date: Set a specific calendar date that applies to all learners.
Minimum Passing Score to Define the minimum score required to pass each quiz or the overall course.
- Ensures learners meet the learning objectives before progressing.
- If not enabled, no minimum score will be required.
Customize the text displayed on key action buttons throughout the course.
Personalizing button labels helps align the course interface with your tone or branding.  Tip: Use clear, action-oriented labels to guide learners naturally through the course. 
- Examples include: "Finish Course" to Finalize the last lesson or module of a course "Next Section" to Move to the next chapter "Submit Answer" to Submit an answer to an assessment
- "Finish Course" to Finalize the last lesson or module of a course
- "Next Section" to Move to the next chapter
- "Submit Answer" to Submit an answer to an assessment
Control which partner users are eligible to enroll in courses automatically based on defined filters.
Filters can be set using CRM and Introw properties such as Tier, Phase, Experience, Country, Language , and more. Partner users who match these filters will see the relevant courses dynamically appear in their portal and will be automatically eligible to enroll. 
💡 Introw: Note that learners must still click "Enroll" to begin a course; the filters only determine which courses are visible and available for enrollment.
Enable certificates to automatically issue upon course completion and customize certificate details via the certification module - Learn more
- Certificates provide recognition and motivate learners to complete the course.
AI-powered learning assistance for a personalized experience as our AI agent makes your course interactive and responsive to learner progress via:
- AI-generated feedback on quizzes
- Conversational guidance through chapters
- After configuring your course, click Save Settings to apply changes.
- Settings can be updated anytime, giving you flexibility to adjust course requirements, features, or certificates as your course evolves.
- Partner training courses
- How to use Introw's course builder
- Show Introw course enrollments and certificates in HubSpot
- Introw Product update - January 2026
- Show Introw course enrollments and certificates in Salesforce

---

## Partner certificates
Source: https://support.introw.io/en/articles/12991031-partner-certificates

Introw's Partner Certificates feature allows you to easily create, manage, and distribute certificates for your partners. These certificates help validate partner qualifications, track completed training, and provide partners with downloadable proof of their certifications.
📹 Learn more in this quick walk through video ⬇️
Partner Certificates are automatically generated documents that Introw dynamically fills with real partner data.
- Description: Provides information about the certificate and the achievements or entitlements it represents. Partner Contact Name: The recipient of the certificate. Issue Date: Automatically filled with the date the certificate is issued to the partner contact. Issued By: Can be a fixed issuer or dynamically set based on the partner manager. Validity: Sets the expiration date of the certificate, options include yearly, monthly, weekly, or lifetime. Branding Options: Customize the certificate's background and text colors to match your brand.
- Certificate numbe r: A unique identifier for the certificate, used for verification and tracking purposes.
Certificates can be given in two ways:
- Ad Hoc Assignment Introw users can create and assign certificates directly to a partner contact whenever needed, perfect for one-off validations or manual certification processes. 
- E.g. Already certified partners do not need to retake courses. If they are already recognized as certified in your system, you can assign certificates directly without requiring course completion again and select to not notify them when granting the certificate. 
- Through the Courses Module Certificates can also be automatically issued when a partner completes a course in Introw's Courses module. Learn more This streamlines training workflows and ensures partners receive the right certification the moment they finish required learning. 
Partners can view all their certified colleagues directly inside the Partner Portal .
For this to be present in the partner portal you need to add the smart section " certificates " within the experience builder. 
Within the partner portal, partners can:
- Download certificates at any time
- Share certificates on LinkedIn
- Access expiry information and verification details
- See a list of all earned certificates
This gives partners full visibility and easy access to their certifications and an overview of all their certified employees. 
### Sharing a Partner Certificate on LinkedIn
Once your partner has earned a certificate, they can share it directly from your partner portal to LinkedIn . This is a quick way to showcase their achievement, highlight expertise, and celebrate their partnership with your brand.
How it works:
- Your partner logs into the portal you provide.
- They navigate to their certificate and click Share on LinkedIn .
- LinkedIn opens with a pre-filled post including the certificate image.
- They can customize the message and publish it to their network.
Sharing certificates helps increase visibility for both your partners and your brand while making it easy for partners to promote their success.
### Adding the issuing organisation's logo on LinkedIn
Introw sends the issuing organisation name to LinkedIn when a certificate is shared. However, LinkedIn does not automatically display the organisation's logo based on the name alone.
To have the logo appear on the certificate in LinkedIn, your partner can follow these steps:
- Go to their LinkedIn profile and open the Licenses & Certifications section.
- Click on the certificate they just added.
- In the Issuing organization field, search for and select your company from LinkedIn's suggestions.
- Once selected, LinkedIn automatically populates the certificate entry with your organisation's logo.
Tip : Make sure your company has an active LinkedIn Company Page with a logo uploaded. LinkedIn pulls the logo directly from your Company Page, so it needs to be set up for the logo to appear.
#### Partner detail
Within each Partner Contact record, Introw users (eligible to see partners) can:
- View all certificates assigned to that contact
- Check expiration dates
- Issue new certificates or decertify (revoke) old ones
This makes certification tracking simple and centralized for your entire partner ecosystem.
#### Certificate overview
For a broader view, admins can access the certificates overview which provides key metrics at a glance such as the total number of certified users, certified partners, and upcoming or expiring certifications. 
 This centralized dashboard makes it easy to track, manage, and maintain all partner certifications efficiently, ensuring compliance and visibility across your partner ecosystem. 
### Benefits of Partner Certificates
- Automate the recognition process for partner training and achievements
- Provide partners with downloadable proof of their certifications
- Maintain consistent branding across all certificates
- Reduce administrative workload for partner managers
- Keep track of all certified contacts in one place
- Partner engagement reporting in HubSpot with Introw app events
- Partner training courses
- How to create a partner certificate
- Show Introw course enrollments and certificates in HubSpot
- Show Introw course enrollments and certificates in Salesforce

---

## Using the AI Conversational Quiz
Source: https://support.introw.io/en/articles/12994618-using-the-ai-conversational-quiz

Our AI Conversational Quiz is a new interactive learning tool that transforms traditional assessments into realistic, dialogue-based practice. Instead of selecting answers from simple options, learners engage in a natural conversation with your AI guide helping them think, apply knowledge, and learn more effectively.
### What Is the AI Conversational Quiz?
The AI Conversational Quiz is an assessment that can be embedded directly within your training course. Partners answer open-ended questions conversationally, just as they might with an instructor or colleague. The AI evaluates their understanding, provides tailored feedback, and encourages deeper reflection.
This feature is designed to mimic real-world communication, allowing partners to demonstrate not just what they know, but how they think. 
### Why conversational assessments are more effective
Traditional quizzes often rely on right-or-wrong checkboxes, which measure recall but not comprehension. Conversational learning goes further: 
- Encourages critical thinking: learners explain ideas in their own words, strengthening understanding and revealing gaps that multiple-choice questions may miss.
- Reduces guessing: there’s no “lucky click”; learners must demonstrate real knowledge instead of selecting from preset options.
- Builds real-world communication skills: dialogue mirrors workplace situations where explaining concepts matters more than picking an answer.
- Provides personalized feedback: AI offers immediate guidance, clarifications, and follow-up questions that help learners improve quickly.
- Increases engagement: the human-like conversational flow feels more dynamic, making learning more enjoyable and memorable.
### How to add an Conversational quiz in a course
Within your course builder you can add an assessment block called AI Conversational Quiz. Introw will provide you with an open question example that you can edit if necessary. 
You can provide the answer or context that the AI agent has to take into account whenever the course taker provides an answer.
- Partner training courses
- How to use Introw's course builder
- Course Settings
- Segment use cases
- AI course builder and live tutor

---

## Introw Product update - December 2025
Source: https://support.introw.io/en/articles/13035409-introw-product-update-december-2025

### Partner Goals
Track performance goals for each partner, driven directly by CRM data . Whether you want to track sourced pipeline, closed revenue, partner-influenced deals, or any custom metric. Partner Goals gives you a clear view of who is performing, who needs support, and where to double down. Real-time progress dashboards keep you and your partners aligned and accountable. Learn more 
### Partner Training and Certification
Give your partners a seamless, world-class learning experience with Introw courses. From teaching product fundamentals to guiding them through your sales process, everything happens in one place and all fully integrated into your CRM . Partners can complete courses, earn certificates , and you get instant visibility into who’s certified, making it easy to enable, recognize, and grow your partner ecosystem.
Introw’s AI Agent transforms traditional assessments into realistic, conversational quizzes . Partners engage in natural conversations, applying knowledge in context and learning more effectively, making training interactive, engaging, and memorable.
🎥 Watch this quick overview video on Introw courses and certificates
### Dynamic Partner Links
Make referrals effortless for your partners with Dynamic Partner Links. Each partner gets a unique, trackable link they can share and every conversion can be attributed in your CRM, giving you full visibility into partner-sourced pipeline. Learn more
### Additional improvements
Thanks to your continued feedback, Introw is making small but impactful updates that improve performance, usability, and the overall experience
Display Goals in Tiers Make your Tiers section more engaging and add real-time partner goals to your requirements to give partners a clearer path to progress. Learn more
 Test announcements You can now test exactly how your announcements will appear to partners, including all personalized variables. Learn more
 Multi-attribution for CRM Deals With multi-attribution, you can define exactly which partner attributions (like partner type or role) Introw applies when creating a deal, lead or any other attributed object in your CRM. Learn more
- Introw product update - October 2025
- Introw product update - November 2025
- Introw Product update - January 2026
- Introw product update - March 2026
- Introw product update - April 2026

---

## How to set a fiscal startdate
Source: https://support.introw.io/en/articles/13193635-how-to-set-a-fiscal-startdate

### How to set a custom fiscal year start date in Introw
Introw allows you to define a custom fiscal year start date so your dashboards and analytics reflect your internal reporting periods. This ensures time ranges like “This fiscal year” and “This fiscal quarter” align with how your business actually operates.
### Why this matters
Some organizations don’t follow a January-December calendar year for their finacial reporting. By setting your fiscal start date, Introw will:
- Align dashboards and analytics with your internal reporting
- Make pipeline, revenue, and partner performance easier to compare period over period
### How to configure your fiscal year start date
- Go to Settings in Introw
- Navigate to Company settings 
- Configure your Fiscal year start date Select the date your fiscal year begins (e.g. 1th of April, July, October)
- Save your changes
Once saved, Introw automatically shows fiscal-based time ranges within the Time range selectors. 
### Where this setting is applied
After configuring your fiscal year start date, it will be used across:
- Dashboards
- Analytics pages
- Additional Time ranges will be present : This fiscal year, This fiscal quarter Next fiscal year Next fiscal quarter
- This fiscal year,
- This fiscal quarter
- Next fiscal year
- Next fiscal quarter
### Important notes
- Changes apply going forward and update all fiscal-based views automatically
- Calendar-based ranges (e.g. “Last 30 days”) remain unchanged
- All users in your organisation will see the same fiscal year configuration
- Partner engagement reporting in HubSpot with Introw app events
- Multi-Currency: localise the partner portal experience
- How to create a report
- How to create a dashboard?
- How to embed a report or dashboard in your partner portal

---

## Partner profile section
Source: https://support.introw.io/en/articles/13212973-partner-profile-section

The Partner Profile section allows you to display and manage partner information directly inside your partner portal. This smart section is powered by data from your CRM and Introw, giving partners visibility into their own details and the ability to keep that information up to date. 
### What is the Partner Profile?
The Partner Profile is a configurable section in your partner portal that shows key information about each partner, such as:
- Company (partner) name
- Website
- Logo
- Partner tier
- CRM properties like type, industry, country, or region
All information is sourced from your CRM and Introw, ensuring consistency between your internal systems and what partners see in the portal.
### How it works
- Add the Partner Profile to the experience You can add the Partner Profile as a Smart section in your partner experience. Once published, the partner portal automatically displays partner-specific data based on the logged-in partner. 
- Choose which partner properties to show You can configure, at scale, which properties are visible in the Partner Profile section across the partner portals. This allows you to tailor the experience without creating custom profiles for each partner.  These partner properties can include: Introw properties (Logo, Tier, Partner manager, Partner champion) Any synced CRM properties (for example: industry, country, employee count, description, etc.)
- Introw properties (Logo, Tier, Partner manager, Partner champion)
- Any synced CRM properties (for example: industry, country, employee count, description, etc.)
- Allow partners to edit properties For each property, you remain in full control and can decide which fields partners are allowed to edit. Read-only fields can never be edited by partners. When a partner updates an editable field:
- The change is reflected in Introw
- The updated value is synced back to your CRM
This ensures your CRM stays current without requiring internal teams to manage routine updates. 
Below an example if a partner is allowed to edit certain properties like their logo, industry and their website for example.
### Limit who can edit the Partner Profile
You can take this a step further by restricting which partner contacts are allowed to edit the Partner Profile, based on Introw segments . For example, only contacts with a specific role (like Admin) or partner type can update editable fields, while other contacts see the profile in read-only mode. 
For more details on how to set up segments based on partner or contact properties, check out the Segments article .
The Partner Profile helps you:
- Give partners transparency into the information you have on them
- Reduce manual updates and back-and-forth with partners
- Keep your CRM data accurate and up to date
- Scale partner data management across your entire ecosystem
- How to personalize your partner portal?
- Partner Tiers
- Show commissions to your partners
- Managing partner contacts
- Build a partner directory powered by Introw

---

## Automatically attribute resellers and distributors in two-tier channel deals
Source: https://support.introw.io/en/articles/13293870-automatically-attribute-resellers-and-distributors-in-two-tier-channel-deals

In complex two-tier channel deals , a sale often involves more than one partner such as a Reseller bringing in the lead and a Distributor handling the fulfillment. Usually, deal registration forms only credits the partner who clicks "submit," leaving you to manually link other partners later. Introw solves this by allowing you to capture secondary partner attribution at the point of entry.
By adding a dynamic dropdown to your registration form, you allow partners to tag their collaborators from a pre-filtered list synced with your CRM. This ensures every stakeholder is fully attributed and visible the moment a deal submission is approved. 
### Video walkthrough
Watch the video below to see how to set up a secondary partner attribution and how it simplifies the registration process for your partners.
### How it works
When a deal is registered via an Introw form, you can configure multiple partner attributions simultaneously:
- Default Attribution: The submitting partner is by default linked to the deal based on your specific CRM attribution settings.
- Secondary Attribution: If enabled on the form, the submitter can select an additional partner from a dynamic dropdown. For example, a Reseller can tag their Distributor , or vice versa.
- Dynamic Filtering: The list of available secondary partners is filtered in real-time using your CRM or Introw data, ensuring only eligible partners are selectable.
- Automated Attribution: Introw applies the correct attribution to both partners, ensuring they both have visibility into the deal within their respective partner portals.
### How to set it up
#### Step 1: Add a secondary partner field on your form
Navigate to the Forms section and open your deal registration form builder. Add a new field and select either Distributor or Reseller from the available field options. This field will appear to the partner as a searchable dropdown populated with eligible partners.
- The field will render as a dropdown populated with eligible partners based on the applied filters (see step 2).
#### Step 2: Configure which partners appear in the dropdown
To ensure data quality, Introw can automatically make sure the correct partners appear in the dropdown:
- Set your filters Use CRM or Introw data such as company or account type (e.g., "Distributor") or partner tier (e.g., "Gold") to decide which partners should be included in the list. This ensures the dropdown only shows partners that are actually eligible.
- Preview the list Before saving, use the audience preview to see exactly how many partners match your filters (e.g., "9 partners match your filters"). This helps you verify that the correct partners will be selectable. 
- Set the Attribution method Define how the selected partner should be linked in your CRM. This ensures the secondary partner is attributed consistently according to your CRM setup.
Secondary partner attribution follows the same logic as default attribution and is also visible within the form's automation steps, ensuring it is applied consistently. 
#### Step 3: Save the form
Save your changes to the form. Whether you add the form to a Partner Experience , share it via a direct link , or embed it on an external website, Introw ensures the correct attribution is applied automatically upon submission. All partner attributions are set instantly into your CRM, so no manual updates are ever required.
### From form submission to CRM sync
After a partner submits a deal, Introw processes the attribution once the form submission is approved. This ensures your CRM only receives verified, high-quality data:
- Review and Approval: Whether you use manual approval or auto-approval, the automated data-sync begins as soon as the form submission is approved.
- Default partner attribution: Introw instantly links the default partner to the new deal or opportunity in your CRM.
- Secondary partner attribution: The partner selected in the dropdown is simultaneously linked to the same deal record, ensuring both parties are fully attributed and have immediate visibility in their partner portals.
### How it looks in your CRM
Once the deal submission is approved, both partners appear instantly on the deal or opportunity record in your CRM, no manual entry required. Your team can see the full two-tier channel picture at a glance.
HubSpot
Salesforce
In both CRMs, each partner is attributed with their correct role, Reseller and Distributor, automatically from the moment the form submission is approved.
### Key Benefits
- Zero Manual Entry: Both the default and secondary partners are attributed automatically once the submission is approved.
- Flexible partner roles: Easily track complex two-tier (2-tier) relationships, such as Reseller-Distributor pairings, without any manual CRM updates.
- Dynamic accuracy: Use real-time CRM data to ensure partners only select from an eligible, pre-filtered list.
- Full attribution: Ensure your deal records are 100% accurate from day one, reflecting the true involvement of your entire channel.
- How partner deal data syncs to your CRM
- How to use Introw forms
- Share a deal to partners via Introw's app card in HubSpot
- AI detected channel conflict resolution
- Tracking Partner involvement on deals

---

## Create and manage pipeline views in the portal experience builder
Source: https://support.introw.io/en/articles/13367569-create-and-manage-pipeline-views-in-the-portal-experience-builder

The Portal Experience builder lets you allow to add a pipeline section and configure which pipeline to display, which deal properties to show, and provides pre-configured views to help you quickly focus on deals that matter. You can now create your own views, rename them, and apply custom filters to tailor the pipeline to your needs.
#### The deal pipeline section
When you open the pipeline section in the Experience Builder, 4 default views are available:
- All: Shows all deals in the selected pipeline.
- Due: Deals that need to close this week.
- Overdue: Deals that should have been closed before today.
- Inactive: Deals that are not closed and have not had any activity in the last month.
These views provide a quick way to monitor deal health, deadlines, and engagement but you can edit them however you want by adjusting the filters, renaming them or creating new views.
#### How to create a new view
- Navigate to Portal Experience → Pipeline section in the Experience Builder.
- Click configure ⚙️ and navigate to Configure views 
- Click Add View . Give your view a clear name (you can rename it later for language reasons). Use the filter options to narrow down the deals you want to see. Examples can be: Created date or close date (with a rolling date range like This quarter, this month, etc..) Deal owner or deal stage (e.g., New, In Progress, Won, Lost) Deal Type or Size Region or Country Any deal property you have in your CRM.
- Give your view a clear name (you can rename it later for language reasons).
- Use the filter options to narrow down the deals you want to see. Examples can be: Created date or close date (with a rolling date range like This quarter, this month, etc..) Deal owner or deal stage (e.g., New, In Progress, Won, Lost) Deal Type or Size Region or Country Any deal property you have in your CRM.
- Created date or close date (with a rolling date range like This quarter, this month, etc..)
- Deal owner or deal stage (e.g., New, In Progress, Won, Lost)
- Deal Type or Size
- Region or Country
- Any deal property you have in your CRM.
- Click Save . Your new view now appears in the Views tab.
- How to create a partner portal experience
- How to setup shared sales pipelines
- What does “No portal yet" and "No deal embed yet” mean?
- Create and manage views in the Deal Overview
- How to embed a report or dashboard in your partner portal

---

## Show Introw course enrollments and certificates in HubSpot
Source: https://support.introw.io/en/articles/13375419-show-introw-course-enrollments-and-certificates-in-hubspot

### Overview
The Introw app cards allow you to view and manage Introw's partner course enrollments and certificates directly inside HubSpot. By adding these cards to your HubSpot record layouts, you can quickly see a contact’s learning progress and earned certificates without leaving HubSpot.
### Before you start
- You must have the Introw app installed in HubSpot Introw installations created before January 1, 2026 must be reconnected to enable the new course enrollment and certificate cards. Reconnecting the app grants the additional HubSpot scopes required for these cards to function correctly. New installations made on or after January 1, 2026 already include the required permissions. Learn more about installing or reconnecting the Introw app 
- Introw installations created before January 1, 2026 must be reconnected to enable the new course enrollment and certificate cards.
- Reconnecting the app grants the additional HubSpot scopes required for these cards to function correctly.
- New installations made on or after January 1, 2026 already include the required permissions.
- Learn more about installing or reconnecting the Introw app 
- You need permission to customize HubSpot record views This is required to add or replace Introw app cards in your HubSpot sidebars.
- This is required to add or replace Introw app cards in your HubSpot sidebars.
Reconnecting ensures HubSpot can securely access the data needed to show Introw course enrollments and certificates inside your records.
### Add the Introw course cards to HubSpot
You’ll need to add the Introw app cards to each HubSpot view where you want them to appear (for example: Contacts, Companies, Deals, or custom objects).
- In HubSpot, go to Settings
- Navigate to Objects and select the object you want to customize (e.g. Companies)
- Open Record customization
- Select the view you want to edit
- In the right sidebar or middle panel layout  click Add card  
- Select the Introw Course Enrollments and/or Introw Certificates app cards
- Save your changes
💡 Introw Tip : Repeat these steps for each object and view where you want the Introw cards to appear.
Example of adding the Introw cards on the middle panel in the company record in HubSpot.
Example of adding the Introw cards on the right panel in the company record in HubSpot. 
### What you’ll see in HubSpot
You can view Introw course enrollment and certificate data on multiple HubSpot objects. This setup allows you to track learning progress both at a high level (per company) and at a detailed level (per partner contact and per course), giving your sales, support, and partner teams visibility into training and certification status directly inside HubSpot.
- Company object: See which courses are associated with the company and track overall partner learning activity.
- Introw Course Enrollments app object: Get a detailed view of enrollments, including: Which users are enrolled in a course Who has completed the course Which partner or company each enrollment belongs to
- Which users are enrolled in a course
- Who has completed the course
- Which partner or company each enrollment belongs to
- Contact record: See individual users’ certifications and which certificates they have earned.
On the Company object, you can see both course enrollments and certificates for the company’s partner contacts. Each enrollment is shown for every partner contact, and each certificate reflects every certified contact within the company. This gives you a complete overview of your partners’ learning activity and certification status at the company level.
In addition, the Introw Course Enrollments app object provides a more detailed view. On this object, you can see:
- Which partner or company the enrollment belongs to
On the Contact record in HubSpot, you can track individual users’ certifications, making it easy to see who is certified and which certificates they’ve earned. Additionally, course enrollments are also visible on the Contact record, giving your team a complete view of each user’s learning progress and achievements. 
Start exploring courses now and unlock the full potential of your partner network. Empower your partners and team members to grow their skills and earn certifications, directly from HubSpot. Add the Introw cards to your records, track enrollments, and celebrate achievements as they happen.
- Show the Introw card inside HubSpot
- Introw workflow actions in HubSpot
- Partner engagement reporting in HubSpot with Introw app events
- Automating workflow actions in HubSpot using Introw App events
- Show Introw course enrollments and certificates in Salesforce

---

## What does “No portal yet" and "No deal embed yet” mean?
Source: https://support.introw.io/en/articles/13385268-what-does-no-portal-yet-and-no-deal-embed-yet-mean

### Overview
When you connect your CRM to Introw, we automatically sync all your deal and partner data. This data powers partner portal experiences, including embedded deal pipelines.
In the general deal overview , Introw users may see one of the following messages when opening a deal:
- No portal yet
- No deal embed yet
Both messages are informational and expected. Below we explain exactly what each one means and what to do next.
### No portal yet
#### What this means
No portal yet means that the partner linked to this deal does not have a portal experience assigned .
Because of that:
- No partner portal exists for this partner
- Deals cannot be embedded yet
- Partners cannot view or collaborate on deals
The deal itself is correctly synced from your CRM and remains fully visible to Introw users. 
#### What you can do
- ✅ View all deal details
- ❌ Collaborate on the deal with the partner
This is expected until a portal experience is assigned. 
#### How to make the deal show up in the partner portal
- Go to the Experience Builder
- Create or select a partner portal experience (that includes a pipeline embed)
- Assign the experience to the partner
Once assigned, Introw can start showing embedded content, such as deal pipelines, for that partner.
👉 For step-by-step instructions, see How to set up a deal pipeline embed in the Experience Builder .
### No deal embed yet
No deal embed yet means that the partner does have a portal experience , but:
- There is no deal pipeline embed in that portal yet, or
- The portal includes a deal embed, but it’s configured for a different pipeline than this deal belongs to.
In other words, the portal exists, but this deal doesn’t match any embedded pipeline. 
- ✅ View the deal details
- ❌ Partners cannot yet see or collaborate on this deal
This ensures partners only see deals that are intentionally included via pipeline embeds. 
To include the deal in an embedded pipeline:
- Create or edit the partner’s portal experience
- Add a deal pipeline embed section You can add the pipeline section into your layout and configure it
- You can add the pipeline section into your layout and configure it
- Assign that experience to the partner
Once that’s done, Introw will automatically populate the embed with the right deals based on CRM attribution, no extra work for you.
- How to create a partner portal
- Partner performance dashboard
- Create a Partner portal experience
- Embed Introw forms
- How to embed a report or dashboard in your partner portal

---

## Monthly partner engagement summary email
Source: https://support.introw.io/en/articles/13427907-monthly-partner-engagement-summary-email

The Monthly Partner Engagement Summary is an automated email sent to active Introw users who have this notification enabled . It provides an overview of partner engagement and activity over the last 30 days , helping users stay informed about how partners are interacting with their partner portal. 
### What’s included in this email
#### Engagement Metrics
The email includes key partner engagement metrics collected from the past 30 days, such as:
- Touchpoints to Interactions between partners and the platform
- Portal Visits to Number of partner visits to the portal
- Due Tasks to Open or completed tasks assigned to partners
- Form Submissions to Submitted deal registrations or other forms
- Announcement Views to Views of published announcements
- Asset Views to Engagement with shared assets and resources
These metrics provide a high-level view of partner activity and engagement. 
#### Top 3 Most Engaged Partners
A list of the top three most engaged partners based on their activity during the last 30 days. This helps identify partners who are highly active and engaged. 
#### Highlights From the Last 30 Days
A summary of notable engagement trends and key activities from the past month, such as increased portal usage, strong interaction with content, or a rise in submissions.
- Get a quick overview of partner engagement
- Identify highly engaged partners
- Monitor engagement trends over time
- Take informed actions to improve partner participation
This email is sent automatically first weekday of the month and is available to all active users who have enabled the notification in their settings.
### Who will receive this email?
The Monthly Partner Engagement Summary email is sent to active Introw users who have a valid email address and are not designated as a CRM user. The email is delivered by default unless the user has explicitly disabled the Periodic Engagement Updates notification. It is sent every first weekday of the month. Users with access restricted to their own partners will still receive the email, with all data limited to the partners they manage.
- Partner Engagement Tracking
- Partner Analytics
- Partner engagement reporting in HubSpot with Introw app events
- Send dedicated partner announcements
- How to embed a report or dashboard in your partner portal