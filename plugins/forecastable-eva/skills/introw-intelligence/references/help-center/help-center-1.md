# Introw help center (support.introw.io), part 1 of 4

Verbatim text of every public help article, fetched 2026-09-29. Older than docs.introw.io; where they disagree, prefer docs.introw.io and the release notes.

## Link your Custom Domain
Source: https://support.introw.io/en/articles/10010261-link-your-custom-domain

Linking a custom domain will allow you to use your own domain for hosting your partner portal and help you better integrate Introw into your brand.  For example...
- Instead of using the subdomain of Introw: “ yourcompanyname.introw.io ”
- your partner portal URL can be “ partners.yourdomain.com ” 
#### Connect a custom domain for your Introw partner portal
You must be on an Introw Pro plan to configure your own custom domain.
Make sure that the subdomain you are trying to add is not being used elsewhere.
Navigate to Portal > Portal settings , and click Configure your own domain.
Enter the domain URL you’d like to connect and use for your partner portal, e.g., partners.yourdomain.com . Click Next .
Go to the DNS page of your domain management platform and enter the TXT and CNAME records with the values provided. Click Finish
Note : It may take up to 24 hours for your DNS settings to become active worldwide, depending on your hosting provider.
Ensure Google Trust Services is whitelisted in SSL certificate authority
#### How to access the DNS settings of your domain
The following steps must be completed on your domain's DNS settings (not on your Introw account). We recommend contacting your hosting provider if you need help with these steps.
- Log in to your domain provider (usually on your hosting).
- Find the DNS settings for your domain. You can find instructions on this by searching “DNS settings” + your hosting provider's name on any search engine (such as Google).
- Create a DNS record with CNAME type and fill out the Name and TXT Value fields given to you on your Introw account.
Just to remind you, hosting providers may refer to the Name and Value TXTs differently. They can be referred to as:
- Name and Host
- Domain and Value
- Domain and Host
In some cases, the CNAME record might be referred to as the Domain Alias record.
##### Make sure your DNS is configured correctly!
- Check TXT (name + value)
- Ensure minimum TLS version is 1.3
- Ensure Google Trust Services is whitelisted in SSL certificate authority
- How to launch a partner portal
- Launch your partner portal
- Enable Single-Sign-On for Partners
- My partner does not receive any emails
- Send notifications from your own email domain

---

## Introw product update - September 2024
Source: https://support.introw.io/en/articles/10023271-introw-product-update-september-2024

### Partnership performance dashboard 🚀
Keep track of your partners' performance with a full overview of their contribution to your revenue. See clearly how much revenue they've generated, the size of the open pipeline, and start taking action to close deals faster by engaging with your partners on key opportunities.
### Partner detail upgrade ✨
Keep track of an individual partner's performance with detailed insights into their assigned deals. See how much revenue they've driven, the size of their open pipeline, and stay on top of opportunities by monitoring deal progress in real-time
### Integration with Slack 👬
Link your Introw partner portal to a shared Slack channel , or push all your partner portal notifications to a dedicated internal Slack channel to keep you and your partner team in sync, right where you work.
- Introw product update - October 2024
- Introw product update - October 2025
- Introw product update - November 2025
- Introw Product update - January 2026
- Introw product update - March 2026

---

## Connecting Salesforce to Introw
Source: https://support.introw.io/en/articles/10087572-connecting-salesforce-to-introw

#### Connect your Salesforce account
- Go to https://app.introw.io
- To get started, navigate to the Settings section of your navigation bar. From there, click on Integrations and click Connect on the Salesforce card 
- Enter your Salesforce login and choose the correct Salesforce account you would want to link to Introw.
- Click on ' Allow ' to proceed. 
### Choose how you store your partners in Salesforce.
To be able to import partners from your CRM, we need to know how you store them. This can be done as either as an account or as custom object. 
 In this example: we store our partners as regular Salesforce Accounts . 
### Find your partners in Salesforce.
Once we know how you store your partners in your CRM, we will try to find them by identifying them based on filters. This way you can decide to only import for example your Reseller partners or Integration partners by using the filters.
By default Introw will try to suggest partners from your Salesforce account by filtering with the Account type set for Partner . 
### Configure your partner attribution
Choose which objects you link to your partners and how you attribute partners to those objects. You can link opportunities, leads, accounts or cases to your partners. 
In this example we say that in our CRM we link our opportunities to our partner via a custom property . 
Select which object you use to link a partner to an opportunity via a relation table   In this example we say that in our CRM we link our opportunities to our partner via a relation table to the object " Opportunity partner"
- Identify the foreign key for the opportunity (in this example: Opportunity ID)
- Identify the foreign key for the partner (in this example Account ID)
### Attributing other Salesforce objects to partners
In Introw, you can configure how you link your partners in Salesforce to multiple objects like Opportunities , Cases , Leads, etc.
You can follow the same flow as described above and identify which object you attribute to partners and how that attribution is done within your Salesforce account.
Example: linking Salesforce opportunities to partners via a custom property (Partner Account Lookup field) 
### Finish the configuration
Make sure to Finish the configuration so Introw can start gathering all the data from your CRM and setup all your partners in no time.
Once this is done, Introw will automatically create your  opportunity or cases pipelines for your specific partners and keep them up-to-date in real-time without leaving your partner portal. 
- Connecting HubSpot to Introw
- Link your Salesforce opportunities to Introw via custom fields
- Link your Salesforce opportunities to Introw via a relation table
- Integrating Introw with Crossbeam
- How to use Introw forms with Salesforce

---

## Link your Salesforce opportunities to Introw via custom fields
Source: https://support.introw.io/en/articles/10102826-link-your-salesforce-opportunities-to-introw-via-custom-fields

Make sure you have connected your Introw account to the right Salesforce account. If not, please check out this article: connecting-salesforce-to-Introw
Navigate to Settings > Integrations a nd click on Configure. 

#### Step 1: How do you store your partners in Salesforce
Choose how you store your partners in Salesforce.   In this example: we store our partners as regular Salesforce Accounts .
#### Step 2: Find your partners in your CRM
By default Introw will try to suggest partners from your Salesforce account by filtering with the Account type set for Partner . In case you use a different configuration to identify a partner, simply adjust the filter. 
#### Step 3: Select which objects you link with partners
Choose which objects you link to your partners to attribute their influence. You can link opportunities, leads, accounts or cases to your partners.  In this example we say that in our CRM we link our opportunities to our partner accounts via a custom field called "Partner". 
In this example: we select the custom field " Partner " that is linked to the Opportunity object in Salesforce. 
#### Step 4: Click finish
When you click Finish , we will automatically create all the relevant Introw partners, give you a great overview on their performance and you are ready to start collaborating with them in dedicated partner portals.
 
- Link your HubSpot deals to Introw via custom properties
- Link your HubSpot deals to Introw via company associations
- Link your HubSpot deals to Introw via custom objects
- Connecting Salesforce to Introw
- Link your Salesforce opportunities to Introw via a relation table

---

## Link your Salesforce opportunities to Introw via a relation table
Source: https://support.introw.io/en/articles/10104772-link-your-salesforce-opportunities-to-introw-via-a-relation-table

Make sure you have connected your Introw account to the right Salesforce account. If not, please check out this article: connecting-salesforce-to-Introw
Navigate to Settings > Integrations a nd click on Configure.  

### Step 1: How do you store your partners in Salesforce
Choose how you store your partners in Salesforce.   In this example: we store our partners as regular Salesforce Accounts . 
### Step 2: Find your partners in your CRM
By default Introw will try to suggest partners from your Salesforce account by filtering with the Account type set for Partner . In case you use a different configuration to identify a partner, simply adjust the filter. 
You can adjust the filter and look up the right object or record type ID. 
### Step 3: Select which objects you link with partners
- Choose which objects you link to your partners to attribute their influence. You can link opportunities, leads, accounts or cases to your partners.  In this example we say that in our CRM we link our opportunities to our partner via a relation table. 
- Select which object you use to link a partner to an opportunity via a relation table  In this example we say that in our CRM we link our opportunities to our partner via a relation table to the object " Opportunity partner"
- Identify the foreign key for the opportunity (in this example: Opportunity ID)
- Identify the foreign key for the partner (in this example Account ID)
Make sure to click "Add opportunity attribution" so Introw can gather all relevant information from this attribution.
### Step 4: Click finish
When you click Finish , we will automatically create all the relevant Introw partners, give you a great overview on their performance and you are ready to start collaborating with them in dedicated partner portals.
 
- Link your HubSpot deals to Introw via custom properties
- Link your HubSpot deals to Introw via custom objects
- Connecting Salesforce to Introw
- Link your Salesforce opportunities to Introw via custom fields
- How to use Introw forms with Salesforce

---

## Introw product update - October 2024
Source: https://support.introw.io/en/articles/10114996-introw-product-update-october-2024

### Announcements 📢
Make announcements towards all your partners and stay top of mind!
Introw allows you to communicate multiple announcements with your partners by creating an announcement that can be send as mail and included in your partner portals.
Learn how

#### Customise and Brand Your Portal 🎨
You may want to customize your branding on Introw to improve the partner’s experience! Customise the portal to reflect your company’s branding, including logos, colors, and messaging. A consistent brand experience reinforces your company’s identity. Learn how
#### Link your Custom Domain 🌐
Linking a custom domain will allow you to use your own domain for hosting your partner portal and help you better integrate Introw into your brand. *This feature is part of our Introw Pro plan - Request more info
### Notifications 🔔
Keep everyone informed and up-to-date by managing default notifications across all partners, with the flexibility to customize them for specific partners. Learn how
#### Other improvements
- Attachments on a deal detail are synced to Hubspot
- Configure the deal name during deal registration 
- Introw product update - May 2025
- Introw product update - August 2025
- Introw product update - October 2025
- Introw product update - November 2025
- Introw product update - March 2026

---

## Announcements
Source: https://support.introw.io/en/articles/10115215-announcements

Keeping your partners informed has never been easier. With Introw, you can create announcements manually or with Introw AI , sharing product launches, webinars, blog posts, or other updates directly in their partner portal, via email, or through Slack. 
Say goodbye to the hassle of chasing partners for updates,  Introw AI generates polished announcements in seconds , letting you keep your partners up to date on autopilot. Track engagement in real time to see who's reading, clicking, and interacting, so you can measure impact and optimize your communications. 
The result? Faster time-to-value, stronger partner relationships, and a seamless way to keep your product or service top of mind,  all without lifting a finger .
Announcements help you keep partners informed, aligned, and engaged, without manual effort. With Introw's AI announcement generator , you can instantly turn your existing content into partner-ready announcements, ensuring your product or service always stays top of mind.
Instead of writing announcements from scratch, Introw uses AI to generate high-quality announcements from:
- Blog posts
- Webinar details
- Product update prompts
Once created, announcements can be shared directly in the partner portal and distributed via email or Slack to maximize reach and engagement. 

Introw makes it easy to create announcements in the way that works best for you:
- With Introw AI Select a predefined prompt, such as blog post , webinar announcement , or product update Introw AI drafts a polished announcement with key highlights and a partner-friendly tone Review and personalize before publishing
- Select a predefined prompt, such as blog post , webinar announcement , or product update
- Introw AI drafts a polished announcement with key highlights and a partner-friendly tone
- Review and personalize before publishing
- From Scratch Start with a blank canvas and write your announcement manually Add your own content, formatting, and style
- Start with a blank canvas and write your announcement manually
- Add your own content, formatting, and style
No matter which option you choose, your announcements can be shared via email, Slack, or displayed in the partner portal in just a few clicks.
Whether using Introw AI or writing manually, Introw streamlines the process so you can communicate updates efficiently and keep partners engaged.
Watch the video below ⬇️ to see how easy it is to create an announcement, either from scratch or with Introw AI, and send it to your partners in minutes.
### Configure your announcement
- Send from : You can choose who will be shown as the sender of your announcements. This can done by a specific person (like head of partner marketing) or dynamically based on the corresponding Partner Manager of the partner that is receiving the announcement.
- Audience : Select which partners the announcement applies to.
- Assign Replies To : You can choose who will be informed from partner replies in your announcements. These replies can be a addressed to a specific person or dynamically to the corresponding Partner Manager of the partner that is replying.
- Thumbnail (optional) : Add an appealing preview to grab your partner's attention when they visit their portal. For the best result, use a 16:9 ratio.
- Pop-up : Choose to display an in-app message when your partner visits their partner portal
### Test your announcement
In case you want to test it, click Test and enter an email on which you want to receive the announcement email you just made. 
After you have tested, you can easily nudge your partners by publishing an announcement into their portal and in addition sending them an email and/or slack notification. Introw will notify all relevant contacts of the selected partners via email and automatically display the announcement in the announcements section within their partner portal.
### Partner's announcement view
When you create an announcement, it can be displayed in the partner portal by including the announcement section in the experience builder. 
You can choose the layout of the announcement section being:
- List view
- Card view
- Posts
And you can limit the amount of announcements to show at first sight when partner visit the portall while they still have the option to click view more to see all your previous announcement. 
Example of a card layout
Example of a list layout
 Example of a posts layout
If multiple announcements are created, they will be displayed with the most recent appearing on top the list or as the first one in the cards and posts view.    Bonus : enabling the ' Show pop-up ' option ensures your partners see an in-app notification as soon as they visit their portal.
An In-app popup will allow you to create more engagement among your partners when they visit their partner portal.
### Remove announcements
To remove old announcements from the section in your partner experience, you have two options: delete them permanently or unpublish them without losing the content and engagement data. Deleting an announcement removes it entirely from your account, while unpublishing keeps it in your overview in case you want to edit the content and republish it later. 
### Track engagement of your announcements
Introw automatically tracks partner engagement to help you understand how actively your partners are interacting with your announcements. So you'll get a clear picture of how engaged each partner is, making it easier to identify if your content is relevant or you need to re-engage some partners.
- How does the integration with Slack work?
- How to invite Partners to your portal via Introw
- Partner notifications
- Send dedicated partner announcements
- Auto-generated partner announcements from your LinkedIn

---

## Brand your Introw partner portal
Source: https://support.introw.io/en/articles/10115469-brand-your-introw-partner-portal

Make your partner portal fully yours! Customize the entire portal experience, from the login screen to portal content and notifications, using your company’s logos, colors, and fonts. A consistent, on-brand experience helps partners feel connected and confident every time they interact with your portal. 
Navigate to Portal > Portal Settings
- Upload a portal image to reflect within the login page of your partner portal. The best ratio for the portal page image is 2304x2160 which is like the golden ratio.
Make your partner portal fully reflect your brand. The portal displays your company logo and can be styled throughout with your brand’s colors, fonts, and visual elements. From the login screen to the pages your partners interact with daily, you can customize background colors, buttons, text, page headers, and active tab colors to create a cohesive, on-brand experience that helps partners feel confident and connected.
### Adding a Custom Font
Custom fonts help reinforce your brand and create a consistent look across your partner portal and other brand touchpoints. This feature is available starting at 25 partners.
You can upload a variable font file (TTF), and Introw will apply it across all partner-facing experiences, including the portal, announcements, certificates, and email notifications. We recommend choosing a font that aligns with your brand guidelines and includes appropriate fallbacks to ensure accessibility and readability.
##### What Is a Variable Font?
A variable font is a single font file that supports multiple styles, such as different weights or widths, without needing separate files for each. Variable fonts are part of the OpenType standard and are supported by most modern browsers and operating systems. 
#### Configuring portal access methods
Define your partner portal access settings by allowing partners to login via email, social logins or your custom partner SSO (Learn more)
Choose the welcome message and copy of the login screen of your portal to make sure it  is aligned with your company's tone of voice.
#### Learn more on how to brand the experience for you partner.
For more detailed guidance on customizing your partner portal, including branding the login page, check out Best practices for a good partner experience . It provides step-by-step instructions and additional best practices for setting up the best partner experience.
- How to create a partner portal
- Best practices for a good partner experience
- Launch your partner portal
- Create a Partner portal experience
- How to invite Partners to your portal via Introw

---

## Collaborate from inside your HubSpot deals
Source: https://support.introw.io/en/articles/10175087-collaborate-from-inside-your-hubspot-deals

The Introw Collaboration card is your command center for deal collaboration with your partners, right inside HubSpot. Without leaving your deal or company record, you can ask AI for partner insights, collaborate with your partners, and access your partner portal in one click.
### Getting started
When a deal doesn't have an active collaboration yet, you can kick one off directly from the card. From there you can:
- Share the deal with a partner directly from within HubSpot
- Get an easy overview of who is managing the partner, who your champion is on the partner side, and which partner tier they are in (Gold, Silver, etc.)
- Add comments, share updates, and track deal progress, all without leaving HubSpot
- Stay synced: all updates are automatically reflected in the Introw platform, keeping everything in sync
#### How to use it
- Locate the Collaboration Card: In your HubSpot deal view, you'll see the Introw Collaboration Card. If not, check out this article !
- Ask AI: Get instant AI-powered insights about the deal and the partner involved. Ask questions like "What is the current status of this deal?" or "What are the next steps?", all without leaving HubSpot.
- Get an overview: See at a glance who is managing the partner, who your champion is on the partner side, and which partner tier they are in (Gold, Silver, etc.).
- Manage Collaborations: Add comments, share updates, and track deal progress, all within HubSpot.
- Stay Synced: All updates are automatically reflected in the Introw platform, keeping everything in sync.
#### Customizing the card position
You can move the Introw Collaboration card within the right-side column of your HubSpot deal or company record so it's easier to reference. To do this:
- Open a deal or company record in HubSpot.
- Click Customize in the right-side panel.
- Drag and drop the Introw Collaboration card to your preferred position.
- Save your layout.
Your customized layout will be saved for future visits to deal and company records.
Watch this video below ⬇️
- Show the Introw card inside HubSpot
- Collaborate from inside HubSpot tickets
- Partner Connect: a 2-way CRM integration with HubSpot
- Link an existing HubSpot deal to your vendor
- Register a new deal from your HubSpot

---

## Multiple partner portal access
Source: https://support.introw.io/en/articles/10192327-multiple-partner-portal-access

In case you have partners that need access to multiple partner portals. E.g: a distributor partner that has multiple reseller partners working for them. While each reseller only has access to their own partner portal, the distributor can get access to all their reseller portals.
With Introw, you can seamlessly access multiple partner portals using the same email address. By simply adding the email under the "People" tab in each partner’s detail, you ensure smooth collaboration across different portals without needing multiple accounts. 
The partner can still use one portal link and enter their email address. 
When your partner enters their email address through the portal link and Introw detects that this email address is linked to multiple partner portals, they will be prompted to select which portal they wish to access. 
We will keep making sure the partner verifies their email address before they are allowed to enter the portal.  

- How to launch a partner portal
- Launch your partner portal
- How to personalize your partner portal?
- Unlink or update an experience of your partner portal
- Invite and manage partner portal users as a partner

---

## Configure the deal owner of your partner deals
Source: https://support.introw.io/en/articles/10200408-configure-the-deal-owner-of-your-partner-deals

To make sure the deals registered by your partners are assigned to the right deal owner of your sales team, we allow to choose which deal owner is set during the automatic creation of a deal in your CRM.
#### How to set this up
- Go to your form and choose Configuration
- Select the automation " Deal automation "
- Go to "Default fields" and select Deal Owner as CRM property
- Configure the deal owner by selecting either a fixed individual or the dynamic Partner manager option. This ensures that the partner owner managing the partnership will be assigned as the deal owner in your CRM.  E.g. John Smith manages the partner Tesla, and Ricky Gervais manages the partner Amazon. If Amazon registers deals via your deal form, the system will automatically assign Ricky Gervais as the deal owner in your CRM. The same logic applies to Tesla, where John Smith is automatically assigned.
Whenever your partners register deals, Introw will make sure the right deal owner is set when creating the deal in your CRM.

- Configure the deal name of your partner deals.
- Configure which deal properties to share with your partner
- How to use Introw forms
- Deal visibility restrictions for partner contacts
- AI Deal Coach

---

## Partner notes
Source: https://support.introw.io/en/articles/10220987-partner-notes

You and your team members in your Introw account can use Partner Notes to add and manage notes about your partners. 
#### Creating a note
- Navigate to the Partners screen
- Drill down on the name of the partner to which the note applies.
- Go to Notes
- Click on Create note
- Once done, press Save
E.g.: Use notes to document key takeaways, action items, and insights from your QBR with your partner, ensuring all updates and discussions are easily accessible for your team. 
- Add your partners to Introw
- Using Introw AI across your partners
- Partner profile section
- Introw's AI Agent in Slack
- How does the integration with Microsoft Teams work?

---

## Partner Tiers
Source: https://support.introw.io/en/articles/10221007-partner-tiers

Introw supports multi-tiered partner structures , allowing you to create separate tiering plans for different partner types such as resellers, referral partners, technology partners or MSPs. 
This enables more precise alignment of incentives, enablement, and recognition. For example, a Gold Reseller and a Gold Referral Partner may share the same tier name but have different requirements and benefits. With this update, Introw makes it easier to scale and personalize your partner portal across a diverse ecosystem.
#### Link tiers to your CRM
These tiers can be synced directly with your CRM, ensuring partner data stays aligned across systems and enabling automated workflows, segmentation, and accurate reporting. If you don’t have partner tiers set up in your CRM yet, Introw can automatically generate them for you in just a few clicks.
Go to Tiers and click Sync on the top right. 
Make sure to link the right partner tier to the right property values in your CRM.

Below an example of a partner program and partner tier on the company record in HubSpot which are directly in sync with Introw. 
#### Setting Up Partner Tiers
Partner tiers allow you to organize your partners based on their performance, contributions, and engagement. Each tier can be tailored with unique benefits and requirements to encourage growth and strengthen collaboration within your program.
Follow the steps below to create and manage your partner tiers:
- Navigate to tiers In the left hand navigation click " Portal " and select the "Tiers" menu item. 
- Link your CRM Tiers Your tiers can be synced directly with your CRM to avoid manual work. If you don’t have partner tiers set up in your CRM yet, Introw can automatically generate them for you in just a few clicks. 
- Create a new tier Click "Create Tier" and enter your tier name (e.g. Reseller partners USA or Technology partners).
- Add levels to your tiering plan Click "Create level" and choose your a name and color. 
- Define requirements and benefits Specify the criteria for this tier, such as revenue targets, deal numbers, or certifications, and list the benefits partners will receive (e.g., discounts, dedicated support, or co-marketing opportunities).
- Add dynamic partner goals as a requirement Enhance each tier with dynamic Introw goal requirements that update automatically, giving partners clear visibility into what they need to achieve and how they are progressing in their current tier.  
- Add a badge (optional) You can add a badge to each partner tier, giving partners a way to showcase their achievement. These badges can be downloaded directly from the portal, reinforcing partner recognition and motivation.  
- Show and apply Once your tiers are set up, make sure they are included in your partner portals by adding the Smart section "Tiers" to the right partner experience.  When they visit their portal, Introw will automatically showcase their current tier and associated benefits. In case the partner has no Tier assigned yet for example newly signed partners, you can set up a fallback tier program. This ensures transparency and keeps your partners informed about their standing within their potential tier program.
Simply apply the corresponding tier level to your partner and Introw will make sure to highlight your partner's tier level when they visit their portal. 
Within the partner experience, your partner will be able to see which tier he is in as it will be highlighted and shown in the top right corner of his partner portal.
Partners will have the option to download the badge directly from the portal, reinforcing partner recognition and motivation. They can do this from the tier overview or from the top right corner.
Partners can also embed your partner tier badge on their website using our provided embeddable code snippet.
### Best Practices
- Avoid overcomplicating tier names. Stick to common labels (Gold, Silver, etc.) to reduce confusion.
- Clearly define tiering criteria per partner tiering plan.
- Ensure your Tiering structure can present both horizontal (partner type) and vertical (tier level) segmentation .
- In case you have a multi-tiering structure , you can choose which tiering plan and their responding levels will show in the partner portal. 
- Automatically attribute resellers and distributors in two-tier channel deals
- Send dedicated partner announcements
- Build a partner directory powered by Introw
- The Introw-Powered Partner: A Day in the Life
- What is Partner Connect?

---

## Integrating Introw with Crossbeam
Source: https://support.introw.io/en/articles/10227780-integrating-introw-with-crossbeam

Our Crossbeam integration enables you to seamlessly view partner account overlap data directly within Introw PRM. By linking your Crossbeam (Supernode plan) account, you can uncover where your accounts intersect with your partner helping you identify high-potential co-selling opportunities and streamline your go-to-market strategy.
#### Connect your Crossbeam account
- To get started, navigate to the Settings section of your navigation bar.
- Click on Integrations and click Connect on the Crossbeam card.
- Follow the authentication wizard and allow the connection between Crossbeam and Introw
#### Link partners leveraging Crossbeam.
On the Crossbeam integration page, you can see which Crossbeam plan you're on and how many unique record exports you have remaining. In the partner overview, you can also see which Crossbeam partner is linked to your Introw partner.
### Account overlap insights
Our integration with Crossbeam gives your internal partnership team visibility into overlapping account data across customers, prospects, and open opportunities directly within Introw. 
#### How does it work?
When a partner registers a deal or opportunity in Introw via a form submission, the system automatically checks for any overlap with your data in Crossbeam. This includes matching against all your populations being customers, prospects, and open opportunities. 
#### Identifying account overlap during deal and lead registration
When a partner registers a new lead or deal in Introw, the system automatically checks for account overlap with your Crossbeam data matching against your customers, prospects, and open opportunities. Any overlaps are flagged in the pending form view, helping you quickly identify co-sell opportunities or potential conflicts. 
#### Showing Crossbeam overlap within the deal pipeline
Introw automatically highlights account overlaps with partner data from Crossbeam in the shared pipeline. When an overlap is detected across customers, prospects, or open opportunities a Crossbeam section appears in the deal detail, helping you quickly identify co-sell opportunities or potential conflicts without leaving your workflow.

- Connecting HubSpot to Introw
- Connecting Salesforce to Introw
- AI detected channel conflict resolution
- How Introw keeps your CRM clean
- Everything Your Partners Can Do in Introw

---

## Embed your google calendar in Introw
Source: https://support.introw.io/en/articles/10256349-embed-your-google-calendar-in-introw

You can embed your google calendar link within Introw to keep your partners up-to-date on all partner related events.
Step 1 : Open your google calendar and select the calendar you want to share.  Step 2 : Click on the 3 dots and choose Settings and sharing.
Step 3: Select Integrate calendar and copy the public URL. 
Step 4 : Go to Introw and add a section in your experience builder and choose embed anything. 
Step 5 : Paste the public URL you copied from your google calendar and click Embed . 
Step 6 : Publish your experience to make sure your partner portals are updated and can see your shared calendar. 
- Embed your google appointment scheduler
- Create new partners via Introw
- Embed Introw in your product
- Embed Introw forms
- Embed Notion into Introw

---

## Show commissions to your partners
Source: https://support.introw.io/en/articles/10270915-show-commissions-to-your-partners

#### Assign the commission plan(s) to your partner
In Introw, you can link one or more commission plans to a partner to match your specific compensation structure. For example, you might assign a recurring commission plan that rewards the partner with a percentage of the deal’s MRR, and at the same time, a one-off incentive plan that provides a fixed payout when a deal is marked as closed-won. These are just examples - you're free to create and combine commission plans based on your partnership strategy.  

#### Show the commission in your shared deal pipeline
You can show the calculated commission within your shared deal pipeline by adding the commission property of Introw on to a deal card via the deal pipeline embed configuration within your partner experience. It is marked purple to indicate that this is the calculated commission from Introw and not a deal property from your CRM.
Within the deal details, your partner can see the expected commission for that deal. The commission status is color-coded: green indicates the commission is confirmed, while a yellow dot means it is pending until the deal is marked as closed-won.
You can embed a commission section into your partner portal to create transparency.
#### Embed a commission dashboard
Within your partner portal you are able show a commission dashboard by adding a rich section named "Commissions" into your partner portal experience. 
When your partner visits their partner portal they can get a clear overview on all the expected commission and where in the funnel it is located.  Partners are able to see all of the commission statements that are generated for them and can download them directly from within the partner portal. 
- Introw's commission module
- Partner Engagement Tracking
- Tracking Partner involvement on deals
- Commissions in Introw: a complete walkthrough
- What is Partner Connect?

---

## Introw's commission module
Source: https://support.introw.io/en/articles/10270932-introw-s-commission-module

Effective commission structures are the cornerstone of a successful partnership program. This guide outlines how to create, manage, and assign commission plans to ensure your partners are incentivized accurately and payouts remain transparent.
🎥 Watch the video below to see how commissions work in action and how Introw keeps everything clear for you and your partners.
### Creating a New Commission Plan
To establish a new incentive structure, navigate to Commission > Plans of your admin navigation.
- Define Plan Parameters: Select Create New Plan and provide a descriptive name (e.g., "Demo to deal bonus 2026").
- Establish triggers (filters): Specify the deals that are eligible for the commission, such as "Customer Payment Received" or "Contract Signed."
- Set Reward Logic: Choose between a percentage-based model (e.g., 15% of total contract value) or a flat-fee structure.
- Configure frequency: Determine if the commission is a one-time acquisition fee or a recurring percentage for the life of the subscription.
These flexible settings allow you to define how commissions are calculated while keeping all information visible and up to date for both your team and your partners.
### Bringing transparency to partners
Introw calculates and displays outstanding commissions for each partner once a deal reaches the relevant stage. This transparency helps partners clearly understand what they’ve earned and what they can invoice.
#### Here’s how it works
- Commission invoice generation to As deals progress, Introw calculates commission amounts based on your defined plan and displays them in the partner’s portal experience.
- Partner visibility to Partners can see all outstanding commissions, including details like deal name, value, and applicable percentage or fixed amount.
- Invoice upload to When ready, partners can upload their invoices directly to the related commission record within Introw.
- Linked documentation to Each invoice is automatically linked to the correct deal and commission entry, keeping your records organized and easy to trace.
This process reduces back-and-forth communication, prevents misalignment, and gives partners full confidence in the amounts they’re invoicing.
### Streamlining the flow to finance
While Introw doesn’t process payouts directly, it helps your finance team work more efficiently by connecting all relevant commission and invoice data in one place.
### Typical workflow
- Commission granted - when you create a Commission statement, we will inform your partner that they have earned commission. This is send to the partner finance email address entered on the commission statement. 
- Invoice submission to Once a partner uploads their invoice, Introw notifies your team for review. The partner can upload their invoice via the portal or by simply replying to the email and attaching the file in an attachment. The Owner of the statement and the internal finance team email will be notified. 
- Approval flow to The user can review each invoice against the commission data, approve or request clarification, and forward it to finance.
- Finance review to The finance team receives all approved invoices along with supporting deal and commission details, making reconciliation faster and clearer.
- Mark as paid to After payment is completed, the invoice can be marked as paid in Introw to maintain a full record of commission activity.   By guiding invoices through this built-in approval and tracking flow, Introw ensures every stakeholder partner, partner manager, and finance stays aligned on commission status. This creates a transparent, auditable process from deal to payment confirmation.
- Show commissions to your partners
- Commissions in Introw: a complete walkthrough
- The Introw API: connect your partner program to the rest of your stack
- Introw's Chargebee integration
- Introw's Stripe integration

---

## How to disconnect HubSpot
Source: https://support.introw.io/en/articles/10285312-how-to-disconnect-hubspot

- Go to https://app.introw.io
- To get started, navigate to the Settings section of your navigation bar. From there, click on Integrations , HubSpot (Configure) and click Disconnect on the HubSpot card
- Confirm to disconnect
- To disconnect an app from your HubSpot account: In your HubSpot account, navigate to Data Management > Integrations. Click Actions on the app you want to disconnect, then click Uninstall. In the dialog box, type “uninstall” in the text field and click Uninstall.
- In your HubSpot account, navigate to Data Management > Integrations.
- Click Actions on the app you want to disconnect, then click Uninstall.
- In the dialog box, type “uninstall” in the text field and click Uninstall.
When you disconnect Introw, rest assured that no data will be removed from your HubSpot account. Introw operates with read and write permissions only, ensuring that all your data in HubSpot remains untouched.
However, please note the following changes:
- The Introw CRM card within HubSpot will no longer function.
- There will no longer be any synchronization between Introw and HubSpot.
Your HubSpot data will remain intact and accessible, but the features and insights provided by Introw will no longer be available after disconnection.
- Link your HubSpot deals to Introw via custom properties
- Link your HubSpot deals to Introw via custom objects
- Create partner portal from within HubSpot
- Introw workflow actions in HubSpot
- Show Introw course enrollments and certificates in HubSpot

---

## Introw product update - November 2024
Source: https://support.introw.io/en/articles/10295136-introw-product-update-november-2024

#### Partner tiers 🎖️
Tiering is an important tool in incentivizing and managing partner engagement within Introw. The embeddable tiers sections allows to create a clear overview to your partners in which partner tier they are situated and to download their potential partner badge.  Learn how
#### Partner notes ✍️
On the partner detail page in Introw, you can create notes to document key partner insights, ensuring your team stays updated and aligned with all relevant information.  Learn how 
#### Commission automation 💰
No more manual commission calculations or spreadsheet updates! Introw automates the process, saving you time and ensuring transparency to your partners.  Learn how
#### Crossbeam ⚔️
Our Crossbeam integration allows you to share opportunities with partners in one-click based on Crossbeam overlap-data. Learn how 
- Introw product update - October 2024
- Introw product update - May 2025
- Introw product update - October 2025
- Introw product update - November 2025
- Introw Product update - December 2025

---

## Configure which deal properties to share with your partner
Source: https://support.introw.io/en/articles/10353727-configure-which-deal-properties-to-share-with-your-partner

The best way of engaging with your partners is by going over a shared sales pipeline.
Introw offers the functionality to create shared pipelines for Deals, Leads, Contacts, Companies and even support tickets all synced from your connected CRM. 
First check out how to setup a shared sales pipeline - here !
#### Configure which deal properties to share with your partner
Step 1: Add properties
Select Add property to add other properties from your CRM that you want to display on the deal card and deal detail within Introw.
Step 2: Configure which properties you like to make editable
Configure the deal properties you want your partner to edit (ex. deal stage, close date) so they can drive the deal and you receive updates on these changes automatically.
Step 3 (optional): Change the display name of the properties
You can change the display label of your CRM deal properties to make them more partner friendly or match with the language of your partners. 
Example: if your partners are based in France but your CRM is in English, Introw allows you to display the CRM properties in French by adjusting the display label. You can do this for any pipeline embed so you can create a French deal pipeline and a German deal pipeline all based on the same data from your CRM. 
##### Extra: Introw supports multi-currencies
Introw supports multi-currency deal amounts from your CRM and allows you to display other deal amount properties based on your company currency from Introw.  Ex. you want to show the forecasted amount of your deal to your partner in your company currency of Introw being EUR.
- How partner deal data syncs to your CRM
- Collaborate on a deal or any other CRM object
- Configure the deal name of your partner deals.
- Configure the deal owner of your partner deals
- Tracking Partner involvement on deals

---

## Add your team to Introw
Source: https://support.introw.io/en/articles/10373313-add-your-team-to-introw

#### Managing Your Team
You can easily manage your team from the Team page so follow these steps to keep your team organized, informed, and easy to collaborate with.   Add Team Members to Click the “Add Member” button and enter their email address to invite new members to your workspace.
 Set Profile Images to Personalize each team member’s profile by uploading a photo. Ideal dimensions are 512x512 pixels, square . This helps everyone quickly recognize who’s who.
 Manage Notification Settings to Adjust how team members receive notifications. You can turn alerts on or off, or choose specific types of updates for each member.
#### Introw User roles
Introw comes with 4 preconfigured user roles by default. You can customize these roles by renaming them or adjusting their permissions to suit your needs. Additionally, you have the flexibility to create your own roles and assign a specific set of permissions to match your workflow. 
Admin
As Admin you have full access to the platform, including managing users, configuring settings, editing content, and viewing all partner data and performance metrics.
Member
With this role, the user is able to access all partner portals but is not able to invite other team members or manage technical integrations like the CRM connection and SSO. 

CRM User
With this role, the user is only able to access Introw partner portals via the copilot card in your CRM. Learn more about our Copilot card. 
Partner manager
With this role, the user is restricted to managing only their assigned partners and related objects, such as specific tasks, form submissions, and CRM-linked items like deals, leads, and more. 
#### Remove Team members
You can deactivate team members by clicking on the 3 dots next to their name and "Deactivate" them. Once this is done, they will no longer be able to access Introw.  
- Add your partners to Introw
- Introw tasks
- Create new partners via Introw
- Roles and permissions
- Introw CPQ

---

## Add your partners to Introw
Source: https://support.introw.io/en/articles/10373923-add-your-partners-to-introw

Remark : when adding partners, we will not send emails to them. Adding your partners to Introw is designed to automatically gather all the information from your partners that is living inside your CRM
### Add your partners to Introw via your CRM integration
When you set up the integration between Introw and your CRM, you can import your partners directly from your CRM into Introw. 
#### Manual import
First, identify how your partners are stored within your CRM. You can then multi-select specific partners or select all, and import them into Introw. Once imported, you can start creating partner portals and collaborate with them immediately.
 Steps:
- Go to your CRM Integration - Configure
- Click Find Partners in your CRM .
- Select the partners you want to import.
- Continue with " Number” of partners .
#### Automated partner creation
Introw supports automated partner synchronisation. With this option, your partners are automatically synced from your CRM based on the filters you set. This ensures your partner list in Introw is always up-to-date without manual imports.
Steps:
- Click Sync on the top right
- Confirm to enable auto-sync .
### Add your partners to Introw via the partner overview
On the partner overview there is the option to " Create partner ", this will show a pop-up to select any account from your CRM that resembles your partner. 
Go to Partners > Create Partner 
Select which partner company from your CRM you want to add as a partner in Introw.
#### Show CRM info on the partner overview
Introw allows you to visualize any property from your CRM directly within the Partner Overview.
Each property is linked to the corresponding partner record property it represents in your CRM, giving you a clear, connected view of your data without needing to switch platforms.
💡 Introw Tip : Changes made in your CRM on the partner record and partner contacts are reflected within 15 minutes!
Changes on your CRM record are reflected within 15 minutes.
- Create new partners via Introw
- Managing partner contacts
- Introw CPQ
- How Introw keeps your CRM clean
- Build a partner directory powered by Introw

---

## Organising Assets
Source: https://support.introw.io/en/articles/10391863-organising-assets

Introw's asset library allows you to organise your assets with a two-level system via Folders & Categories.
- Folders are mostly used to organize content in terms of their topic
- Categories are like tags for assets that can be used to easily group them
You can use this system to organize your assets to the way you prefer
- By topic or team (e.g. Marketing, Sales, Case studies, Competition battlecards, ...)
- By use case (e.g. Resellers, Affiliates, Product Specs, Meeting links,...)
### Asset detail
When you are adding an asset to your library you can immediately create or select which category to apply to it.  
For files and folders that don't generate a preview (such as ZIP files, certain PDFs, or custom file types), you can upload a custom thumbnail to provide a visual reference. Thumbnails help partners quickly identify the content and improve the overall look and usability of the asset library.
Add a thumbnail to an asset
- Simply hover on the preview to add a thumbnail image. This image will appear in place of a preview and can be updated at any time to reflect the content more accurately.
Add a thumbnail to a folder
Adding a thumbnail to a folder is a great way to make your asset library more visually aligned with your brand and to help users quickly recognize and navigate content.
- Click on the 3 dots next to a folder and select Set folder thumbnail 
- Upload your thumbnail to be used when visualizing the folder in the partner portal. The maximum file size for a folder thumbnail is 20MB
When the asset library is displayed as cards in the partner experience, the thumbnail you upload will be used as the visual representation of the folder.
You now have the option to archive assets instead of permanently deleting them. Archiving helps you keep your asset library clean and organised while maintaining a safety net.
How it works:
- When you archive an asset, you can provide a reason for archiving. This helps your team keep track of who changed what and why.
- Archived assets are moved to a dedicated Archived tab in the asset library, making it easy to find and review all archived content in one place.
- Archived assets will be automatically deleted after 90 days . Until then, they remain available for review or restoration.
- If you need an archived asset back, you can restore it at any time before the 90-day window expires, and it will reappear in your active library.
💡 Tip: Use archiving instead of deleting to maintain a clear audit trail. The archiving reason helps your team understand why an asset was removed and makes it easier to decide whether to restore it later.
- Asset library
- Manage your assets in the asset library
- Share assets at scale
- Managing assets in multiple languages
- Governance and versioning

---

## Manage your assets in the asset library
Source: https://support.introw.io/en/articles/10391889-manage-your-assets-in-the-asset-library

### Uploading new assets
You can upload new assets to the library by following the steps below. 
Click Add Asset on the asset library screen and select if you want to:
- Upload one or multiple files
- Add a URL
- Create a folder
### Upload your assets
Uploading multiple files like images, PDFs, and presentations to your asset library makes key resources easily accessible within the partner portal. This ensures partners always have the most up-to-date materials at their fingertips. Whether it's a product brochure, logo, or sales deck, adding files helps streamline communication and support.
### Replace an asset
You can easily replace assets in Introw to keep your content up to date without needing to create new entries. This works like version control when you upload a new asset with the same name or ID as an existing one, it will automatically replace the original while maintaining all associated metadata and links. This ensures consistency across your materials and saves time by avoiding broken references or manual updates.
#### Add a URL
Adding URLs to your asset library allows you to link directly to important resources, such as training pages, product information, or external tools. These links can be embedded in the partner portal for easy access, helping partners find what they need without searching. 
### Import a folder or assets in bulk
You can add assets in bulk two ways: upload a folder with all its subfolders and files, or upload a ZIP. Either way, Introw keeps your folder structure intact, so everything appears exactly as you organized it, no need to recreate folders or re-sort afterward. 
#### Create a folder
Creating folders in your asset library helps keep your content organized and easy to find. By grouping assets by campaign, region, or content type, you can streamline access for your team and partners. This ensures everyone quickly finds the right materials when they need them. 
### Sharing permissions
Sometimes you'll want to control how widely an asset can travel. Introw gives you three sharing levels: Public , where partners can share the asset with anyone, a prospect, an outside consultant, or a broader audience; Portal restricted , where the asset stays inside the partner portal and can't be shared externally; and Segment based , where access is limited to the specific partner segments you choose.
### Adding thumbnails to your assets and folders
For files and folders that don't generate a preview (such as ZIP files, certain PDFs, or custom file types), you can upload a custom thumbnail to provide a visual reference. Thumbnails help partners quickly identify the content and improve the overall look and usability of the asset library.
Add a thumbnail to an asset
- Simply hover on the preview to upload a thumbnail image. This image will appear in place of a preview and can be updated at any time to reflect the content more accurately.
Add a thumbnail to a folder
Adding a thumbnail to a folder is a great way to make your asset library more visually aligned with your brand and to help users quickly recognize and navigate content.
- Hover on your folder detail to upload a thumbnail.
- Upload your thumbnail to be used when visualizing the folder in the partner portal.  The maximum file size for a folder thumbnail is 20MB and best results are achieved by using a thumbnail file ratio: 16:9
When the asset library is displayed as cards in the partner experience, the thumbnail you upload will be used as the visual representation of the folder.
### Archiving assets
You now have the option to archive assets instead of permanently deleting them. Archiving is a great way to clean up your asset library while keeping a safety net in case you need to bring something back. 
How it works:
- When you archive an asset, you can provide a reason for archiving. This helps your team keep track of who changed what and why.
- Archived assets are moved to a dedicated Archived tab in the asset library, making it easy to find and review all archived content in one place.
- Archived assets will be automatically deleted after 90 days . Until then, they remain available for review or restoration.
- If you need an archived asset back, you can restore it at any time before the 90-day window expires, and it will reappear in your active library.
💡 Tip: Use archiving instead of deleting to maintain a clear audit trail. The archiving reason helps your team understand why an asset was removed and makes it easier to decide whether to restore it later.
- Asset library
- Organising Assets
- Embed your asset library in your partner experience
- Creating Co-branded assets
- Managing assets in multiple languages

---

## Segment based access control
Source: https://support.introw.io/en/articles/10392711-segment-based-access-control

🗣️ We took role-based access control (RBAC) further. After building RBAC, we revisited the model to make access management more scalable, the result is segment-based access control. Instead of manually assigning roles, access is now granted automatically based on partner or contact attributes. Learn more
#### Use case
You may want to provide different levels of visibility to various individuals or partner organizations. With segment-based access control, you can manage access on a per-tab basis using segments defined by:
- Partner properties, e.g. tier = Gold
- Partner contact properties, e.g. contact role = Engineer
#### Tab access
You can manage access per tab in the experience builder. By default, partner contacts can view all tabs that have no access restrictions applied.
To limit access:
- In the experience builder, select the desired tab.
- Click the three dots and choose "Manage access" .
- Assign the tab to one or more segments. 
Only partners or partner contacts matching the segment criteria will be able to see the restricted tab. 
### Creating segments
Segments are evaluated dynamically, access updates automatically as partner or contact attributes change. You can create two types:
- Partner-based, target entire organizations (e.g. partner tier = Gold , partner region = EMEA )
- Partner contact-based, target specific individuals (e.g. contact role = Engineer , contact language = French )
To verify segment membership, navigate to the Segments tab. If someone is missing access, check that their attributes match the segment criteria.
- Asset library
- Managing partner contacts
- Share assets at scale
- Segment use cases
- Segments in Introw

---

## Embed your asset library in your partner experience
Source: https://support.introw.io/en/articles/10401828-embed-your-asset-library-in-your-partner-experience

Embed your assets
In your experience you can choose to embed your assets by adding the smart section called Asset Hub. 
Click Add Section - choose the Smart section called Asset Hub . 
##### Configure which assets to show
To create a nice experience for your partner, there are multiple configure options available to showcase your assets.
You can configure the layout of your asset hub by choosing between:
- Table view
- Thumbnail view
You can choose to show a search or filter option allowing your partner to search within all shared assets or to hide those options to create a clean look.
By clicking the 👁️  icon you can simply choose which content you want to display to your partners. Enabling this on a folder will make sure all nested files within that folder are available for your partner, speeding up the process of showing the right files.
Partner portal experience with a table view of asets 
Partner portal experience with a grid view of assets
- How to preview a partner portal?
- Asset library
- Embed tasks within your partner experience
- Partner Asset Hub
- How to embed a report or dashboard in your partner portal

---

## Introw tasks
Source: https://support.introw.io/en/articles/10410224-introw-tasks

Keeping your partners focused can be a challenge, but with Introw, you can create and assign Tasks to ensure they’re notified and stay on top of what’s essential for your partnership's success. To make this process more efficient and consistent, you can create Task Templates (predefined sets of tasks) that can be automatically applied to one or multiple partners.
The Tasks feature has been enhanced to give you better visibility, control, and efficiency when managing partner activities. With a structured, drill-down approach, you can now track progress from a high-level overview down to individual task details, all in just a few clicks.
### Task template overview
When you access the Tasks page, you’ll now land directly on the Task Template overview . This serves as your central hub for managing partner tasks.
Here you’ll see:
- A list of all your Task Templates
- Completion rate percentages for each template, showing how much progress your partners have made
- The number of partners linked to each template
This immediate visibility helps you quickly identify which processes are on track and which may need attention. 
### Standalone tasks
Standalone tasks are ad hoc tasks that are created outside of a Task Template. They are ideal for one-off requests or tasks that don’t follow a predefined process. With standalone tasks, you can:
- Create and manage tasks independently from task templates
- Handle unexpected or unique partner requests as they arise
- View standalone tasks alongside template-based tasks in the Tasks overview
- Filter tasks by assignee so each user can focus on the tasks relevant to them
This ensures flexibility in task management while maintaining clear ownership and visibility.
### Task detail
To manage a specific task, simply click on it from within the template detail view. You’ll be taken to the Task Detail page , where you can edit the task name, due date, assignee, visibility, actions, description and status.
##### Due Dates
When setting a due date for a task, you can choose between:
- Fixed Date to Select a specific calendar date for the task to be completed.
- Relative Date to Set the due date to occur a certain number of days after a the task (template) gets assigned to the partner. Use case: The due date of the Sign NDA task should be 3 day after you assign the task to your partner. If you assign the task to your partner on the 10th of January, the due date will be set on the 13th of January and your partner will be nudged to complete his task when the due date is reached
- Use case: The due date of the Sign NDA task should be 3 day after you assign the task to your partner. If you assign the task to your partner on the 10th of January, the due date will be set on the 13th of January and your partner will be nudged to complete his task when the due date is reached
##### Assignee
When creating or editing a task, you can control who can see it by setting its assignee.
- All Partner Contacts to The task will be visible to all contacts linked to the partner organization.
- Internal Team to Only your internal team members will be able to view the task.
- Specific Roles to You can choose a role to set as dynamic assignee, and only partner contacts assigned with that role will see the task.
##### Task Visibility
When creating or editing a task, you can decide who can see it by selecting one of the following options:
- Public to The task is visible to all relevant external contacts and your internal team.
- Internal to The task is visible only to your internal team members.
- Assignee to Only the person (or people) assigned to the task will be able to view it.
Selecting the right visibility ensures that sensitive information is only shared with the right audience while keeping everyone who needs to be informed in the loop.
##### Actions
You can now link automated actions to tasks such as:
- Viewing an asset (e.g., product video, case study, sales deck)
- Uploading a file , such as an NDA, contract, or a specific onboarding form
- Submitting an Introw form (e.g. registering their first partner lead or deal)
- Going to an external link outside Introw (e.g., Calendly, Typeform, or your website for booking a demo)
Once the partners completes the action, the associated task will be automatically marked as done , keeping your taks overview cleaner and your partners on track.
##### Description & files
Add a Description to give more context and guidance for completing the task. This can include background information, step-by-step instructions, or any other details that will help clarify expectations. You can also attach Files such as documents, images, or templates to provide reference materials or supporting resources. Keeping all relevant details and assets in one place makes it easier for assignees and viewers to understand the task and take action.
### Task progress
You can track how far along a task is by opening the task details within the task template and checking the overall Progress . This shows you the current stage of the task, such as To Do , In Progress , or Done .
Task progress can also be monitored across multiple partners, making it easy to see who’s on track, who needs support, and where deadlines may be at risk. This helps you quickly spot trends, address bottlenecks, and keep projects moving smoothly. 
#### Task Notifications
Introw provides automated notifications to ensure that partners and your internal team remains informed about their tasks. Notifications are sent when a task is assigned, reminding the assignee of their responsibilities. Additional reminders are issued as the due date approaches to support timely completion. If a task becomes overdue, an overdue notification is generated and delivered to the assignee.  These notifications help maintain accountability and reduce the risk of delays.
##### Task assignment
##### Task due
- Introw Agent
- Task templates
- Introw's AI Agent in Slack
- How does the integration with Microsoft Teams work?
- Build a mutual action plan with Tasks

---

## Partner journeys
Source: https://support.introw.io/en/articles/10410246-partner-journeys

Journeys are reusable collections of tasks designed to guide partners through specific processes, such as onboarding, training, campaign execution, or certification. Instead of manually creating tasks for each partner, you can save time by applying a journey with just a few clicks, or automatically enroll partners into the right journey based on their profile or activity. 
Each journey bundles a predefined set of tasks together, where each individual task can include its own due date, assignee, description, and actions. 
### Manage journeys
Manage your journeys within the Journeys navigation item and start adding those recurring tasks that your partners or your internal team need to accomplish.
Easily create a journey by clicking Add journey .
You can pick one of Introw's predefined journey templates, such as Partner Onboarding , Partner Activation , or Certification Journey, and adjust them to your needs, or start from scratch and build a custom journey step by step.
### Configure tasks within a journey
The due date and assignee are variable options that will be applied when enrolling a partner into the journey.
For example:
The due date of the Sign NDA task should be 3 days after you enroll the partner into the journey. If the partner is enrolled on the 10th of January, the due date will be set on the 13th of January and your partner will be nudged to complete the task when the due date is reached.
### Create actionable tasks
Task Actions in Introw are designed to help you streamline your partner onboarding workflows by linking actions to specific tasks . With this feature, you can automate task completion when partners view content, upload files, or take important steps like registering their first deal, all from within their partner portal. 
You can link automated actions to tasks such as:
- Viewing an asset (e.g., product video, case study, sales deck)
- Uploading a file , such as an NDA, contract, or a specific onboarding form
- Submitting an Introw form (e.g. registering their first partner lead or deal)
- Going to an external link outside Introw (e.g., Calendly, Typeform, or your website for booking a demo)
Once the partner completes the action, the associated task will be automatically marked as done . 
### Enroll partners into a journey
There are multiple ways to enroll a partner into a journey, giving you the flexibility to automate and scale your onboarding process.
##### Via the Partner Experience Builder
You can apply journeys directly through the Partner Experience Builder , making it easy to assign consistent, repeatable task flows to partners. This ensures every partner gets the right guidance, without manual setup each time.
Within the experience builder, add the journey section and configure which journey needs to be displayed. 
##### Via the partner detail
On the partner detail page, within the Tasks tab, you can assign a journey to a specific partner at any time by clicking Add task > Assign journey and selecting the relevant journey.
##### Via HubSpot Workflows
You can also enroll partners into a journey automatically using HubSpot Workflows . This is particularly useful when you want to trigger onboarding based on a CRM event, for example, when a deal reaches a certain stage, a partner property is updated, or a new partner is created in HubSpot. Learn more 

When a partner's status in HubSpot is updated to "Active," a workflow can automatically enroll that partner into your standard onboarding journey in Introw, ensuring no partner slips through the cracks and onboarding kicks off right away, without any manual intervention from your team. 
### Task collaboration and configuration
You are able to work with your partner on a table view of tasks or use the kanban board layout to use a project approach within the partner portal experience.
The partner will clearly see the action to take on tasks in case there is an action linked, like viewing a training video or uploading a document. 
Completed tasks can be archived automatically within a partner portal after a relative set of days has passed, to keep a clean and structured overview of outstanding tasks and avoid clutter of completed tasks. 
### Create a dynamic partner experience with segment-based tabs
Taking your onboarding a step further, you can combine Journeys with segment-based access control to create a truly dynamic partner portal experience, one that evolves as partners progress through their onboarding.
With segment-based tabs, specific tabs in the partner portal are only made visible to partners who match certain criteria. Because segments are evaluated dynamically , access updates automatically as partner properties change, no manual intervention needed.
- A new partner is invited to the portal and only sees the Getting Started tab.
- As part of the onboarding journey, they are asked to accept the Terms & Conditions by submitting an Introw form.
- Submitting that form updates the partner's phase property (e.g., from "Onboarding" to "Active" ).
- That property change triggers a segment update, which automatically unlocks new tabs, such as the Deal Registration tab, the Training Hub, or the Co-marketing Resources tab.
This approach removes friction for partners by only surfacing what's relevant at each stage, while ensuring your team doesn't need to manually manage access as partners move forward. The result is a cleaner, more guided onboarding experience that scales effortlessly across your entire partner base.
- Introw workflow actions in HubSpot
- Partner activity events in your HubSpot timeline
- Partner Connect: a 2-way CRM integration with HubSpot
- Build a mutual action plan with Tasks
- What is Partner Connect?

---

## Embed tasks within your partner experience
Source: https://support.introw.io/en/articles/10410373-embed-tasks-within-your-partner-experience

#### Overview
Keeping your partners focused can be a challenge, but with Introw, you can create and assign tasks to your partners or your internal partnership team to ensure they’re notified and stay on top of what’s essential for the partnership's success.
#### Embed a tasks section
In your partner portal experience you can embed Introw's task  or mutual action plan section by clicking add section and select the rich section named Tasks. 
This is a smart section indicating that Introw will dynamically fill in this information based on the partner that the portal experience is assigned to. 
The partner portal will show the tasks that are linked to the partner and you and your partner will have the option to update those tasks or create new tasks.
- How to create a partner portal experience
- Show commissions to your partners
- Unlink or update an experience of your partner portal
- Embed your Power BI reports
- Build a mutual action plan with Tasks

---

## Partner Asset Hub
Source: https://support.introw.io/en/articles/10410484-partner-asset-hub

#### Overview
Managing a growing partner network can get messy when you need to share unique documents like contracts or proposals with specific partners while also distributing generic assets like marketing materials or pricing sheets to all partners efficiently.
#### Embed Partner asset hub
Introw offers the rich section Partner asset hub to easily share partner specific files with your partners while keeping the scalability of your partner experience.  In the experience builder click Add section > Smart sections > Asset Hub > Partner Specific Asset Hub. 
This a rich section indicating that Introw will dynamically fill in this information based on the assets linked to the partner detail and marked to be included the portal. 
#### Adding assets to a specific partner
You are able to add an asset to a specific partner by going into the partner detail under the tab Assets. You can upload any asset you want to link to this partner and choose if you want to include it in their portal or not.  For example: you have an NDA agreement linked to the partner and can choose if you want to include this in their portal and in which tab it should show. 
### Partner experience
Your partner portal will contain a section that only shows the partner exclusive assets that want to share with the specific partner.
- Asset library
- How to personalize your partner portal?
- Show commissions to your partners
- Partner journeys
- Embed tasks within your partner experience

---

## Embed your google appointment scheduler
Source: https://support.introw.io/en/articles/10419542-embed-your-google-appointment-scheduler

You can embed your google appointment scheduler within Introw to allow your partners to book an appointment with you.
 Step 1 : Open your google appointment scheduler and copy the URL 
Step 2: In your experience builder select Add Section > Meeting > Other
Step 3 : Add your meeting link and make sure to click Embed meeting link.
Step 4: Make sure to Publish your experience for the changes to take place in your partner portals.
- Embed your google calendar in Introw
- Embed your Power BI reports
- Embed Introw forms
- Embed Notion into Introw
- What does “No portal yet" and "No deal embed yet” mean?

---

## Introw product update - January 2025
Source: https://support.introw.io/en/articles/10516533-introw-product-update-january-2025

Content Engagement Tracking Track how partners engage with your shared content and refine your resources based on data-driven insights to maximize partner success. Learn more  Role based partner access You may want to grant different levels of access to individuals from your partner organisations. To achieve this, you can manage access on a per-tab basis. Learn more Partner Asset Hub Managing a growing partner network becomes challenging when you need to share unique documents like contracts and co-branded marketing materials with specific partners. Introw's Partner Asset Hub allows you to easily share partner-specific files. Learn more
### Content Engagement Tracking
### Role based partner access
### Partner Asset Hub
- Introw product update - March 2025
- Introw product update - May 2025
- Introw product update - June 2025
- Introw product update - August 2025
- Introw Product update - January 2026

---

## Link partners to leads in HubSpot
Source: https://support.introw.io/en/articles/10546603-link-partners-to-leads-in-hubspot

Use custom properties in HubSpot to attribute partners to Leads
Within HubSpot go to the Lead Object and select Manage lead properties . In case you have not configured a property yet to attribute your partners to a lead, click add property and define a property with the possible property values. 

##### How to setup Lead attribution within your Introw form
- Make sure you identify how you attribute leads to partners via the CRM configuration panel. In this example we attribute partners to leads via a custom property called "Introw Partner" 
- Make sure to add the creation of leads within your form submissions. Within the form configuration, an automation to create a contact or company is required before you can add the "create lead" automation for HubSpot to accept it. 
- Click add automation and select "Create lead". Make sure that your necessary lead fields from HubSpot are filled in via the configuration panel like leadname, lead stage, pipeline and so on.  
- Make sure to embed the lead form within your partner portal experience similar as you do for a deal pipeline - learn more 
- Your partner will fill in the form and based on the configuration within Introw, a lead will be created and automatically attributed to your partner. 
How to Display Custom Lead Properties in Your HubSpot Leads List
If you're having trouble viewing your custom lead properties after creating them in HubSpot, you don't have to keep editing columns repeatedly. Instead, customize your Leads list view to make these properties easily accessible.  Here’s a quick step-by-step guide to get you set up:
- Access Your Leads List Navigate to your Lead Dashboard in HubSpot.
- Navigate to your Lead Dashboard in HubSpot.
- Edit columns In the Leads list view, click on the "Edit Columns" option in the top right corner of the table
- In the Leads list view, click on the "Edit Columns" option in the top right corner of the table
- Add your Custom Properties In the column editor, search for and select your custom properties.
- In the column editor, search for and select your custom properties.
- Click apply Once applied, these properties will now display directly in your Leads list view and you can inline edit the property in the leads overview.
- Once applied, these properties will now display directly in your Leads list view and you can inline edit the property in the leads overview.
- Connecting HubSpot to Introw
- Link your HubSpot deals to Introw via custom properties
- Link your HubSpot deals to Introw via custom objects
- Linking deals to leads via Introw
- How to use Introw forms with HubSpot

---

## Partner Portal login
Source: https://support.introw.io/en/articles/10561979-partner-portal-login

Partners access your portal via a secure, passwordless login flow . Authentication is handled primarily through One-Time Passcodes (OTP) sent via email. For organizations that require it, Single Sign-On (SSO) is also supported.
This approach ensures robust security while maintaining a frictionless experience for your external partners. 
### How partners log in
Partners can access the portal through several entry points. Regardless of how they arrive, the authentication process follows the same secure principles. 
#### Supported entry points
- Invitation Emails: Direct links sent when a partner is first invited.
- Portal Login Page: Your dedicated URL (e.g., partners.yourdomain.com ).
- Email Notifications: Direct links to specific deals, leads, tickets, or tasks.
- Slack Notifications: Real-time updates in shared channels.
### Authentication Methods
#### 1. Login via One-Time Passcode (OTP)
OTP is the default authentication method to login to the partner portal. 
Step 1: Initiation: The partner enters their email address on the login page or clicks a link in an invitation/notification email.
Via the partner portal invitation email
- Step 2: Verification Email: A unique six-digit passcode is sent to the partner’s work email.
- Step 3: Verification: The partner enters the passcode into the login screen.
- Step 4: Access Granted: The partner is securely logged into the portal.
❗ Remark: Each unique one-time passcode (OTP) is valid for 15 minutes and can only be used once. If a code expires, the partner must request a new one from the login screen.
#### 2. Single Sign-On (SSO)
If your portal is configured for SSO (default enabled for Google, Microsoft, or configured for a custom SSO ), partners can bypass the email verification flow. By selecting their provider on the login page, they are authenticated instantly through their organization's identity provider.
### Accessing via Notifications
##### Email Notifications
When partners receive updates on deals, leads, tasks, announcements or anything related to them from the partner portal, the process is streamlined. ( See notifications )
- Click: The partner clicks the "View Deal" (or similar) button in the email.
- Session Check: * If they have an active session , they are taken directly to the specific record and no verification flow is required. If their session has expired, they are prompted to authenticate via OTP or SSO .
- If their session has expired, they are prompted to authenticate via OTP or SSO .
- Redirect: After a successful login, they are automatically redirected to the exact page linked in the notification.
##### Slack Notifications
If you have the Slack integration enabled, partners can receive updates directly in linked channels.
- Click: The partner clicks the link within the Slack message.
- Access: Just like email notifications, if the partner is already logged in, they land directly on the relevant deal. If not, they will be asked to complete the quick OTP or SSO verification first. 
- How to launch a partner portal
- Launch your partner portal
- Brand your Introw partner portal
- Enable Single-Sign-On for Partners
- Off-portal collaboration in Introw

---

## Create a Partner portal experience
Source: https://support.introw.io/en/articles/10562182-create-a-partner-portal-experience

#### Personalised welcome message
Create a welcoming experience for your partners by making their portal feel familiar and inviting by using a personalised introduction section.
#### Actionable welcome message
Add clear call-to-action buttons within an introduction section to give a partner a direct link to what they want to do like registering a deal or following up on existing deals. 
#### Invite other partner users
Introw makes it easy for your partners to collaborate by allowing them to invite additional users to their partner portal. With this feature, partners can add colleagues from their organisation without needing your involvement. You can manage and control permissions to maintain oversight.
#### Announcements
Keeping your partner up to date on the latest news via announcements
#### Partner Deals
Embedding a deal pipeline in your partner portal enhances transparency, streamlines collaboration, and keeps partners engaged throughout the sales process. Partners gain real-time visibility into deal progress, upcoming actions, and potential bottlenecks, ensuring better alignment and faster deal closures. 
#### Partner Content
Ensure your partners have everything they need at their fingertips, from sales presentations and marketing collateral to videos and solution papers or co-branded partner assets. 
#### Partner Tiers
In case you use Introw's tiering feature, your partner will be able to download their badge and even copy the embeddable code they can use on their website or LinkedIn page. 
- How to create a partner portal
- How to preview a partner portal?
- How to invite Partners to your portal via Introw
- Partner Engagement Tracking
- What is Partner Connect?

---

## Unlink or update an experience of your partner portal
Source: https://support.introw.io/en/articles/10616459-unlink-or-update-an-experience-of-your-partner-portal

### How to unlink the experience from a partner portal?
A partner portal is linked to a partner experience and this defines the look and feel and which content or information will be present within the portal.  Once a partner portal is created, you can remove or unlink the partner experience.  If you want to start a partner portal from scratch for a partner you can delete the partner from Introw and re-add them so the portal link no longer exists. Make sure your partner is informed before you do this, in case you have already shared a partner portal link with them.
##### Via the partner overview
- Go to the partner overview and select your partners
- Click "Unlink experience" 
- Or click on the 3 dots on partner record and select "Unlink experience" 
- Confirm that you want to unlink the experience of the partner portal(s).
❗ Introw Tip: "Unlinking the experience will delete the partner portal and erase all activity and engagement data.
The partner info like CRM attribution, tier level, commission plan, tasks, etc. will be kept, but partner contacts will lose access to the partner portal.
### How to update the experience of a partner portal?
##### Via the experience builder overview
- Go to the experience builder overview and select your experience
- Click "Link Partners" via the link icon or the 3 dots.
- Choose which partners you want to link to that experience.
- Click on "Link Partners" and Introw will update their portals with the selected experience.
- Optionally, you can send a message to your partner to notify them that their partner portal has been updated.
#### Via the experience builder detail
- When you preview a partner portal
- Click on edit in the portal editor preview detail
- Select "Switch experience" 
- Choose the experience you want to apply to the partner portal. 
- How to preview a partner portal?
- Launch your partner portal
- Embed tasks within your partner experience
- Create a Partner portal experience
- How to embed a report or dashboard in your partner portal

---

## How to share a lead (and other CRM objects) with your partner
Source: https://support.introw.io/en/articles/10628194-how-to-share-a-lead-and-other-crm-objects-with-your-partner

Introw allows you to share any CRM object with your partners. A typical use case is a vendor sending a lead to a reseller.
Step 1: Click "Share"
Step 2: Decide which contact from your CRM you want to share
Provide some additional context for your partner in order for them to contact the end-customer in the best way.
Step 3: Decide to who you want to send the selected contact
Introw will automatically generate a professional e-mail which will be sent to the partner.
- Collaborate on a deal or any other CRM object
- How to use Introw forms
- Share a deal to partners via Introw's app card in HubSpot
- Tracking Partner involvement on deals
- What is Partner Connect?

---

## Create new partners via Introw
Source: https://support.introw.io/en/articles/10660509-create-new-partners-via-introw

#### Step 1: Make sure you create a form for new partners to sign-up.
Use the form builder of Introw to create the questions you need to ask a new partner when they sign up and map the fields against your CRM on the right side
Go to configuration to make sure that upon submission of the form the correct actions are performed in you CRM ( create company, create contact, set the right partner properties, etc..)  Learn more on how to configure your forms 
You can also add an acceptance flow s o that you can accept or reject partners applications before they are created as partners within your CRM. 
Click Save to make sure your form is created
#### Step 2: Share or embed the form link for new partners to sign-up.
Click " share form " and use the General link to embed it on your website or share it via email to partner prospects.
#### Step 3: Add your partners to Introw (via Introw)
When the form is submitted (and accepted), you can go to " partners " in the left navigation bar - Click in the top right on Create partner.   Learn more on adding partners to introw 
Search for your newly created partner in this dropdown list as the partner has been automatically added to your CRM via the Introw form. 
#### Step 3b: Add your partners to Introw (via Introw copilot in HubSpot)
Search for your newly created partner company in HubSpot and create a shared space via the Introw Copilot card.  In case you have not set the Copilot card on a company card, see here how to do this. 
#### Step 4: Create a portal for your partner
Now that your partner is created in Introw, you can decide if you want to create a partner portal for this partner. 
Learn more on how to create a partner portal experience. 
#### Extra: Add your partners to Introw (automatically)
You are able to create an automated flow via our Zapier integration for creating a new partner in Introw when you have accepted their Introw form submission.  
- Create partner portal from within HubSpot
- Add your partners to Introw
- How to use Introw forms
- Share a deal to partners via Introw's app card in HubSpot
- Linking deals to leads via Introw

---

## Enable Single-Sign-On for Partners
Source: https://support.introw.io/en/articles/10740664-enable-single-sign-on-for-partners

Introw Partner SSO allows your partner users to access the Introw portal through your identity provider instead of Introw's default email-verification flow.
Introw supports two authentication protocols for partner SSO, so you can connect with whichever your identity provider uses:
- SAML 2.0 to the established standard supported by virtually every identity provider.
- OpenID Connect (OIDC) to a modern, OAuth 2.0-based protocol, ideal for providers that prefer OIDC over SAML.
In addition, Introw supports SCIM 2.0 for automated partner provisioning and deprovisioning. See the SCIM section below.
Remark ! Reach out to [email protected] if you want to have this feature enabled .
Navigate to your Introw settings > Developers . You will see a navigation item Portal SSO which contains all the necessary information to configure either a SAML 2.0 or an OpenID Connect (OIDC) connection with your identity provider.
The service provider is already prepared by Introw and available on your subdomain or custom domain. Use the metadata URL from Introw to prepare your internal SAML connection. Once your identity provider is prepared, fill in the Metadata URL and Introw will finalise the connection.
To connect via OIDC, register Introw as an application (client) in your identity provider, then provide the connection details in the Portal SSO settings. You will typically exchange the following:
- Issuer URL (or discovery / .well-known endpoint) from your identity provider.
- Client ID and Client Secret generated when you register Introw as an application.
- Redirect / Callback URL to copy the value shown by Introw and add it to the allowed redirect URLs in your identity provider.
- Scopes to ensure openid , email , and profile are granted so Introw receives the required user attributes.
Once these values are filled in, Introw will finalise the connection.
Beyond just-in-time provisioning at login, Introw supports SCIM 2.0 so your identity provider can automatically keep partner users in sync. With SCIM enabled, Introw will:
- Provision new partner users automatically when they are assigned to Introw in your identity provider to no manual invite needed.
- Update user attributes (such as name or email) whenever they change in your directory.
- Deprovision users automatically to when someone is removed from Introw in your identity provider or leaves the organisation, their access to the partner portal is revoked, helping you stay secure and compliant.
To set this up, open your Introw settings > Developers and locate the SCIM configuration. Introw provides a SCIM Base URL and a bearer token . Enter these into the provisioning settings of your identity provider (for example Okta, Microsoft Entra, or OneLogin) to establish the connection. You can then map SCIM attributes and assign users or groups to control who is provisioned into the partner portal.
As soon as “Enable Partner SSO” is enabled the login experience will shift and your partners will only see a Login with SSO button (this copy can be changed in the tab - portal).
If your partners are already authenticated and they click on a link to Introw (from an email for example) they will automatically be logged into Introw and land on their partner portal.  When not authenticated , the partners will land on the login page of the partner portal with a clear CTA to be redirected to Single Sign On.
Partners will now login on your Identity Provider, after the authentication they are redirected back to the partner portal and land within their dedicated partner portal. This works the same way whether your connection uses SAML 2.0 or OIDC.
Example of OneLogin as identity provider 
- How to launch a partner portal
- Setup Single-Sign-On for Partners (SSO) via Auth0
- Enable Single-Sign-On for your team
- Introw product update - March 2025
- Managing partner contacts

---

## Use a Relation table in Salesforce to attribute partnership revenue
Source: https://support.introw.io/en/articles/10757123-use-a-relation-table-in-salesforce-to-attribute-partnership-revenue

Using a relation table in Salesforce to attribute partnership revenue can be done by the following options: use the standard Partner object of Salesforce or create your own custom object.
Use Salesforce standard Partner object
Within Salesforce there is a default Partner object which can be associated to an opportunity to indicate the attribution of the partner.
On the opportunity detail in SF, you can link partner by clicking on the related "Partners" card. 
You have the option to create a relation between the opportunity and multiple partners as well as the role the partner is playing on the opportunity like Distributor, Reseller and so on. 
- Link your Salesforce opportunities to Introw via a relation table
- Use a Relation Lookup field in Salesforce to attribute partnership revenue
- Use a Picklist in Salesforce to attribute partnership revenue
- Use a Custom object in Salesforce to attribute partnership revenue
- Salesforce integration overview

---

## Use a Relation Lookup field in Salesforce to attribute partnership revenue
Source: https://support.introw.io/en/articles/10757124-use-a-relation-lookup-field-in-salesforce-to-attribute-partnership-revenue

Using a lookup relation field to Accounts in Salesforce to attribute partnership revenue can be done by following the next steps.
You prefer looking at a video instead of reading a text? ⬇️ This is for you.
##### Create a custom property (on opportunity level) with a lookup relation as data type
Step 1: Go to Setup , > Object Manager , > Opportunity
Step 2: Click on Fields & Relationships
Step 3: Create a new field
- Data Type : Lookup Relationship
- Field Label : This is up to you to decide, we’ve gone for “ Partner ”
- Related to : Account
 Attribute the right partner(s) to the right opportunities
Add your custom property (Partner in this example) to your opportunity page layout.
Now you will be able to search for your partners (being stored as Accounts in your Salesforce) and attribute them to the opportunity.
- Link your Salesforce opportunities to Introw via a relation table
- Use a Relation table in Salesforce to attribute partnership revenue
- Use a Picklist in Salesforce to attribute partnership revenue
- Use a Custom object in Salesforce to attribute partnership revenue
- How to use Introw forms with Salesforce

---

## Collaborate from inside HubSpot tickets
Source: https://support.introw.io/en/articles/10762826-collaborate-from-inside-hubspot-tickets

Introw's Copilot card integrates directly into your HubSpot ticket view, enabling you to:
- Collaborate with partners : Assign and manage tickets with partners directly from HubSpot.
- Streamline workflows : Eliminate the need to switch between Introw and HubSpot.
- Enhance communication : Track ticket updates and partner interactions effortlessly.
How to Use It:
- Locate the Copilot Card : In your HubSpot ticket view, you’ll see the Introw Copilot Card. If not, check out this article !
- Share and collaborate : Share tickets and collaborate with partners with a simple click straight from HubSpot.
- Off portal partner experience: Your partner can provide updates directly from his inbox and is not required to go into the partner portal.
All comments made by you or your partner on the ticket detail in Introw are synced instantly as notes in HubSpot .
Check out the video below on how your team can collaborate with your partners on support tickets and how your partners can provide off-portal updates to reduce the friction of logging into the partner portal.  
##### Integrate Introw with Slack and stay updated seamlessly
All updates on tickets can be pushed into your linked Slack channels so you don't need to leave your favourite communication tool. Learn more about how to set this up in this article. 
- Show the Introw card inside HubSpot
- Create partner portal from within HubSpot
- Collaborate from inside your HubSpot deals
- Share a deal to partners via Introw's app card in HubSpot
- Partner Connect: a 2-way CRM integration with HubSpot

---

## Use a Picklist in Salesforce to attribute partnership revenue
Source: https://support.introw.io/en/articles/10766417-use-a-picklist-in-salesforce-to-attribute-partnership-revenue

Using a picklist field in Salesforce to attribute partnership revenue can be done by following the next steps.
You prefer looking at a video instead of reading a text? ⬇️ This is for you.
#### Create a custom property (on opportunity level) with a picklist as data type
Step 1: Go to Setup , > Object Manager , > Opportunity
Step 2: Click on Fields & Relationships
Step 3: Create a new field
Step 4 : Choose data type: Picklist or Picklist (Multi-select*) 
*In case you want to attribute multiple partners to the same opportunity we advice to choose a Picklist (Multi-select).
Step 5: Name your customfield and assign values
- Field Label : This is up to you to decide, we’ve gone for “ Reseller ”
- Values : Add the custom property values that you relate with your partners 
Introw Tip: Make sure to add the custom field to the opportunity page layout.
Start attributing your partners to your opportunities
Within the opportunity you link your partners via the picklist values and Introw will automatically link them to the correct partner accounts.

- Connecting Salesforce to Introw
- Use a Relation table in Salesforce to attribute partnership revenue
- Use a Relation Lookup field in Salesforce to attribute partnership revenue
- Use a Custom object in Salesforce to attribute partnership revenue
- How to use Introw forms with Salesforce

---

## Use a Custom object in Salesforce to attribute partnership revenue
Source: https://support.introw.io/en/articles/10769562-use-a-custom-object-in-salesforce-to-attribute-partnership-revenue

You can use custom objects in Salesforce to attribute partnership revenue by doing  following the next steps.
You prefer looking at a video instead of reading a text? ⬇️ This is for you.
You want to take your time and go through the steps in detail?
Below you can find a detailed description of all the steps you need to take.
Create a custom object
- Go to Setup > Object manager
- Create custom object
Create a relation table between your object and opportunities
- Add a look up relation field on your custom object to link to another object (e.g. Opportunity )  
- Adjust your opportunity layout to show the new custom object. Go to the opportunity Object > Page Layout Select Related Lists and move the custom object to where you want to display it within an opportunity detail. Save the page layout
- Go to the opportunity Object > Page Layout
- Select Related Lists and move the custom object to where you want to display it within an opportunity detail.
- Save the page layout
Start attributing your partners to your opportunities
Within the opportunity you can now link your partners via the custom object.

- How to attribute revenue to partners in HubSpot?
- Use a Relation table in Salesforce to attribute partnership revenue
- Use a Relation Lookup field in Salesforce to attribute partnership revenue
- Use a Picklist in Salesforce to attribute partnership revenue
- How to use Introw forms with Salesforce

---

## How to share Co-branded assets with partners?
Source: https://support.introw.io/en/articles/10807736-how-to-share-co-branded-assets-with-partners

Cobranding in Introw allows you to create sales or marketing collaterals only once and generate them effortlessly with the right partner information at scale or ad hoc by your partner themselves. 
#### Watch this video below! 🚀
#### How to create co-brandable assets?
When selling through your ecosystem, your partners represent your brand but many lack the resources to create professional collateral. This often leaves your team handling the time-consuming task of customizing cobranded content for them.
Learn more on how to easily create co-brandable assets via Adobe acrobat.
https://support.introw.io/en/articles/10807750-creating-co-branded-assets
- Partner Asset Hub
- Create a Partner portal experience
- Creating Co-branded assets
- Share assets at scale
- Partner training courses

---

## Creating Co-branded assets
Source: https://support.introw.io/en/articles/10807750-creating-co-branded-assets

When selling through your ecosystem, partners represent your brand, but many lack the resources to create professional collateral themselves. Instead of customising documents one by one, you can prepare your existing PDF with a few placeholder fields and upload it to Introw's asset library. From there, Introw takes care of the rest.  When a partner downloads the asset, their logo and name are automatically inserted into the predefined fields in the PDF, no manual work required on your end.
### What you'll need
- Adobe Acrobat (Standard paid plan or higher) to prepare your PDF template
- Your existing sales or marketing PDF
- Partner logos in Introw (auto-captured from your CRM, enrichment tools, or uploaded manually)
#### Step 1, Open your PDF in Adobe Acrobat
- Open Adobe Acrobat and go to All Tools .
- Select Prepare a Form .
- Open your PDF file.
❗ Important: When the form editor opens, make sure to disable the "Automatically detect form fields" setting. This prevents Acrobat from adding unwanted fields to your document.
#### Step 2, Add placeholder fields
Place form fields wherever you want partner information to appear, typically where a logo or partner name would sit.
##### Partner Logo
- Insert an Image field component at the desired position.
- Open Properties and set: Name: Introw.partner.logo
- Name: Introw.partner.logo
- Open the Options tab and set: Default Value: LOGO HERE
- Default Value: LOGO HERE
##### Partner Name
- Insert a Text field component at the desired position.
- Open Properties and set: Name: Introw.partner.name
- Name: Introw.partner.name
- Open the Options tab and set: Alignment: Center Default Value: PARTNER NAME
- Alignment: Center
- Default Value: PARTNER NAME
💡 Introw Tip: The default values ("LOGO HERE" / "PARTNER NAME") act as visible placeholders in the asset preview, so partners immediately understand where their information will appear before downloading.
#### Step 3, Save and upload your PDF
Once your fields are in place:
- Save your PDF.
- Go to your Asset Library in Introw and upload the PDF.
Introw will automatically detect the Introw.partner.logo and Introw.partner.name fields and replace them with the correct partner information when the asset is downloaded.
#### Supported field names
Field name
What it inserts
Introw.partner.logo
Partner's logo (image)
Introw.partner.name
Partner's display name (text)
#### Example use cases
- Sales one-pagers → Generate a co-branded version for each reseller with their logo and name pre-filled.
- Event collateral → Produce partner-specific brochures or flyers ahead of joint events.
- Marketing kits → Let partners download ready-to-use materials without needing design resources.
### Related articles
- Asset Library
- Manage your assets in the Asset Library
- How to share co-branded assets with partners
- Share assets at scale
- Create a Partner Portal experience

- Asset library
- Manage your assets in the asset library
- How to share Co-branded assets with partners?
- Managing assets in multiple languages

---

## Embed your Power BI reports
Source: https://support.introw.io/en/articles/10809685-embed-your-power-bi-reports

Effortlessly deliver data-driven insights to your partner ecosystem with our Power BI embedding feature! Seamlessly integrate Power BI reports into Introw, providing your partners with real-time access to essential metrics and performance data , all within their Introw partner portal
### Connect Introw to Power BI
Make sure to connect Introw to Power BI before you can go the next steps. 
#### Create the right role (audience) for your partner reports
- Go to your dataset (Semantic model) that is used in a report and select Open Data Model.
- Click on Manage roles and add a new role to identify your partner. In the example below I created roles for each of my partners like Amazon_role, Microsoft_role.  PS: You are free to choose the naming of those roles, it is adviced to make some link to the partner as you will use this role in the next step within Introw.
- Go to Introw > Settings > Integrations and click Connect on the Power BI integration.
- Click "Add Power BI Embed"
- Paste the link of your Power BI report into Introw.
### Configure which partner is linked to which Power BI embed role
Within Introw you can configure which partner is allowed to see which Power BI dashboard/report based on the role you configured in Power BI. This ensures that the dataset assigned to a specific role is used exclusively to display the report for that particular partner.
### Embed the Power BI report in your partner portal
To visualize the power BI report towards your partner, you need to make sure to add the Power BI section in your partner experience. 
- Click add section > Power BI
- Select the report of your Power BI you want to embed.
- Make sure to publish the experience and check the result by using the preview option
Below you see the example of a power BI report embedded in the partner portal. It wil only show the data for the partner portal that you are viewing (in this case Microsoft). 
- Embed your google calendar in Introw
- Embed Introw in your product
- Link Introw to Power BI
- What does “No portal yet" and "No deal embed yet” mean?
- How to embed a report or dashboard in your partner portal

---

## Setup Single-Sign-On for Partners (SSO) via Auth0
Source: https://support.introw.io/en/articles/10820542-setup-single-sign-on-for-partners-sso-via-auth0

To setup Single Sign-On (SSO) via Auth0 please follow the instructions below 
Step 1 : Create a “Regular Web Applications” application in Auth0
Step 2 : In the Addons tab of the application enable SAML2 WEB APP
Step 3 : Define the correct nameIdentifier fields
Configure the necessary nameIdentifier fields:
- nameId
- emailAddress
- name
{ "nameIdentifierFormat": "urn:oasis:names:tc:SAML:1.1:nameid-format:emailAddress", "nameIdentifierProbes": [ "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/emailaddress", "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/nameidentifier", "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/name" ] }
Step 4 : Get the metadata endpoint of Auth0 from Application > Settings > Advance Settings > Endpoints > SAML section > SAML Metadata URL.
Step 5. Enter the SAML Metadata URL into Introw SSO configuration page.
Once your identity provider is prepared, fill in the Metadata URL and Introw will finalise the connection.
- Enable Single-Sign-On for Partners
- Enable Single-Sign-On for your team

---

## Enable Single-Sign-On for your team
Source: https://support.introw.io/en/articles/10829581-enable-single-sign-on-for-your-team

💡 Introw Tip : Reach out to [email protected] if you want to have this feature enabled .
Introw's Internal SSO allows your team to securely access the platform through your company's identity provider, seamlessly integrating with your existing Single Sign-On (SSO) system like Okta, OneLogin, Microsoft Entra (AD), and more. This ensures a streamlined login experience while maintaining security and compliance across your organisation.
Introw supports two authentication protocols, so you can connect with whichever your identity provider uses:
- SAML 2.0 to the established standard supported by virtually every identity provider.
- OpenID Connect (OIDC) to a modern, OAuth 2.0-based protocol, ideal for providers that prefer OIDC over SAML.
In addition, Introw supports SCIM 2.0 for automated user provisioning and deprovisioning. See the SCIM section below.
Navigate to your Introw settings > Developers .
In the Internal SSO settings you can find all the necessary information to configure either a SAML 2.0 or an OpenID Connect (OIDC) connection with your identity provider.
### Option A · SAML 2.0
The service provider is already prepared by Introw. Utilize the metadata URL to prepare your SAML connection in your identity provider. Once your identity provider is prepared, fill in the Metadata URL and Introw will finalise the connection.
### Option B · OpenID Connect (OIDC)
To connect via OIDC, register Introw as an application (client) in your identity provider, then provide the connection details in the Internal SSO settings. You will typically exchange the following:
- Issuer URL (or discovery / .well-known endpoint) from your identity provider.
- Client ID and Client Secret generated when you register Introw as an application.
- Redirect / Callback URL to copy the value shown by Introw and add it to the allowed redirect URLs in your identity provider.
- Scopes to ensure openid , email , and profile are granted so Introw receives the required user attributes.
Once these values are filled in, Introw will finalise the connection.
You can configure the mapping of the personal identification properties (email, first name, last name, and user ID) that Introw will use. Introw expects the claim values provided by your identity provider for these attributes. This means you specify the claim names from your identity provider (for example: email , given_name , family_name , oid ), and Introw will automatically read the corresponding claim values for each user during authentication. This mapping applies to both SAML 2.0 and OIDC connections.
Beyond just-in-time provisioning at login, Introw supports SCIM 2.0 so your identity provider can automatically keep team members in sync. With SCIM enabled, Introw will:
- Provision new users automatically when they are assigned to Introw in your identity provider to no manual invite needed.
- Update user attributes (such as name or email) whenever they change in your directory.
- Deprovision users automatically to when someone is removed from Introw in your identity provider or leaves your organisation, their access is revoked, helping you stay secure and compliant.
To set this up, open your Introw settings > Developers and locate the SCIM configuration. Introw provides a SCIM Base URL and a bearer token . Enter these into the provisioning settings of your identity provider (for example Okta, Microsoft Entra, or OneLogin) to establish the connection. You can then map SCIM attributes and assign users or groups to control who is provisioned into Introw.
To log in via Single Sign-On (SSO), team members should begin by accessing the standard Introw login page at https://app.introw.io/login and entering their email address. Upon clicking "Log in with email," Introw's authentication system will automatically determine if the user should be redirected to the organisation's SSO provider for authentication. This works the same way whether your connection uses SAML 2.0 or OIDC.
When the user is authenticated through the Single-Sign-On service they are redirected back to Introw.
### User provisioning
If the user was not yet invited to the team in Introw they are provisioned with the expected default role that was configured previously. When SCIM is enabled, users can also be provisioned in advance directly from your identity provider.
- Add your team to Introw
- Enable Single-Sign-On for Partners
- Setup Single-Sign-On for Partners (SSO) via Auth0
- How does the integration with Microsoft Teams work?
- Microsoft Teams - Link private and shared channels🔒

---

## Introw's Zapier Integration
Source: https://support.introw.io/en/articles/10839375-introw-s-zapier-integration

Connect Introw with Zapier to effortlessly automate partner creation and management. With this integration, you can seamlessly sync data from your CRM, forms, or other tools to automatically create new partners in Introw, saving time and ensuring consistency across your partner ecosystem 🚀 .
#### How to set it up?
Go to Integrations > Zapier and click Connect
Copy the API key generated by Introw as that will be needed for setting up the zap connection in Zapier. 
Once you have accepted the Zapier invite from Introw you can use our integration within your Zaps. 
To connect your Account to Zapier you need to enter the API key that you can copy from your integration screen in Introw and your Introw domain (like for example: acme.introw.io ).
### Introw's Zapier events
Introw has multiple Zapier events that you can leverage.
##### Trigger Events
- New Partner Triggers when a new partner is created in Introw.
- Triggers when a new partner is created in Introw.
- Access Change Triggers when partner portal access has been granted or revoked.
- Triggers when partner portal access has been granted or revoked.
- Portal visit Triggers when your partner contact visits their partner portal. 
- Triggers when your partner contact visits their partner portal. 
##### Action events
- Create Partner Will create a new partner within Introw
- Will create a new partner within Introw
##### Managing Partner portal access
You can automatically manage access to the partner portal saving time and ensuring only the right partner people get in.
This event allows you to change partner portal access based on actions, such as completing a purchase, reaching a milestone, or updating their subscription. Simply connect your CRM, payment platform, or any other supported app via Zapier, and let automation handle the rest.
##### Creating partners in Introw
In this example, I have a Typeform that is capturing data and that data is pushed to create a partner in Introw. 
In this example, I have a new company record created in HubSpot and based on some conditions (depending they are a good partner fit for example), the zap will create a partner in Introw.
#### Partner creation taking place in Introw
With the Zapier integration, you can automatically notify other systems whenever a new partner is created in Introw.  In this example, I have a new notion record be created whenever a new partner is added to Introw. 
- Integrating Introw with Crossbeam
- Add your team to Introw
- Create new partners via Introw
- Embed Introw in your product
- Introw workflow actions in HubSpot

---

## Introw product update - March 2025
Source: https://support.introw.io/en/articles/10854679-introw-product-update-march-2025

#### Single-Sign-On
Introw offers Single-Sign-On for both your internal team as your partner users to access the Introw portal. Enabling single sign-on allows you or your partners to access Introw without having to verify their email.  Learn more
Single-Sign-On for your team Introw's Internal SSO allows your team to securely access the platform through a SAML 2.0 authentication mechanism, seamlessly integrating with your company’s Single Sign-On (SSO) system.
Single-Sign-On for Partners Introw Partner SSO will allow your partner users to access the Introw portal through a SAML 2.0 authentication mechanism instead of Introw's default email-verification flow.
### Co-branded assets
Customizing and co-branding content for each partner can be a time-consuming task. With Introw's Co-Branded Asset feature , you can easily create sales and marketing materials, generating them seamlessly with the right partner details, whether at scale or on demand by your partners themselves.
Check out this video on how to share co-branded assets with ease!
### Power BI integration
Effortlessly deliver data-driven insights to your partner ecosystem with our Power BI embedding feature! Seamlessly integrate Power BI reports into Introw, providing your partners with real-time access to essential metrics and performance data , all within their Introw partner portal. Learn more
- Introw product update - May 2025
- Introw product update - August 2025
- Introw product update - October 2025
- Introw Product update - January 2026
- Introw product update - March 2026

---

## How to use Introw forms
Source: https://support.introw.io/en/articles/11092789-how-to-use-introw-forms

Introw forms give you the flexibility to create forms for your partners to fill in for any use case you might have and to use them inside or even outside your partner portal while automating the creation towards your CRM and giving you the ability to collaborate on your partners forms submisisons. 
### How to create a 'deal' form
Go to the "Form Builder" in the navigation menu to access an overview of suggested forms provided by Introw. You can also create a form from scratch.  We recommend starting with Introw’s preconfigured deal form and adjusting it to your needs. 
The Form Builder is a fully flexible form editor that lets you seamlessly link form fields to your CRM properties, such as Pipeline, Deal amount, Close date, Deal stage, and more. Any object or property in your CRM can be connected to fields in your Introw form, all without any coding required. 
Not every field has to be linked to your CRM. Alongside CRM-mapped fields, you can add standalone fields, such as free text , dropdown lists , and multi-select lists , that aren't connected to any CRM property.
These are useful for capturing extra context you need to review and manage the submission itself, like a partner's notes, a reason for the request, or a category selection, without adding new properties to your CRM. 
### Automatic CRM data validation
Introw automatically validates form submissions against your CRM’s property rules, no additional setup required.
When a partner submits a form, all mapped fields are checked against the validation rules defined in your CRM (such as phone number formats, ZIP/postal code patterns, required formats, numeric ranges, or custom property rules). If a value doesn’t meet your CRM’s requirements, the submission is blocked and the partner is prompted to correct the field.
Because validation is driven directly by your CRM configuration, your existing data rules are always enforced, ensuring clean, consistent data and protecting the integrity of your CRM out of the box.
### How to automate the partner attribution towards your CRM
When a partner shares a deal with you via the Introw form, either directly from the portal or through off-portal collaboration ( learn more here ) the deal or other object you are creating with the Introw form is automatically attributed to them using the method configured in your CRM integration. This simple flow requires no special setup and ensures every deal is tracked correctly.

With the multi-selector , you can credit partners for multiple roles on the same deal. For example, a partner can be marked as the partner-sourced partner while also being recognized for their role as a reseller.  You can configure forms so that deals submitted through one form are automatically attributed to resellers, while another form can automatically credit distributors. You can select from different attribution methods in your CRM ( all configured in the integration page ) giving you full flexibility to capture every partner’s attribution. 
You can also enhance the Introw form with additional automation steps to create any object you need such as contacts, companies, notes, tickets or custom objects and link them to the appropriate partner when required.
### Approval workflows
When you require a review before a submission becomes a record in your CRM, Introw supports multi-step approvals with optional AI assistance.
- AI pre-check before human review Introws AI agent can evaluate the submission against your criteria and gives the reviewer a recommendation plus partner-ready communication, so the human approver always has context before clicking Accept or Decline. 
- Multi-step (sequential) approval Chain multiple approvers on a single form. Each step must be approved before the next approver is notified, so reviews always happen in the order you define.
For details on configuring approvers and acting on submissions, see How to manage form submissions .
#### CRM Object create automation
Introw can automatically create any CRM object based on form submitted information like deals, contact, companies, tickets, cases etc. Basically any default and custom objects from your CRM.   Deduplication logic
Introw matches existing company records on any form fields to prevent duplicates and detect channel conflicts. Leave the defaults (company name, domain) or pick your own fields. 
#### Relative-date default values
Default values for date fields can be expressed relative to the form submission date, the approval date, or another date field on the form, instead of as fixed calendar dates. For example, set a deal's Close date to default to 30 days after the form is approved, or take the partner's selected Kick-off date and add 14 days on top. 
You'll find this option when configuring default values on date fields in the form's automation step. See How partner deal data syncs to your CRM for the full mapping flow.
#### Advanced automation options
Each automation step includes an Advanced section with extra control over how Introw handles created objects in your CRM.
- Disable net new company creation When enabled, Introw will only attach the object if it already exists in your CRM and never create new records. 
- Custom association labels for company relations Override the default association labels used when linking other created objects to this company. Use the Contact to Company association label option to select a label like "End Customer" or "Billing Contact". This way when a lead or deal comes in the prospects user information will be linked to the prospect company with that particular label.
### The result in your CRM
Below is an example of a deal submitted by my partner, Microsoft, which was automatically created in my HubSpot account with the correct partner attribution (in this case, using the association label “Partner”). 
All actions are logged in HubSpot’s activity timeline events and notes, including the full details of the form submission. 
- How partner deal data syncs to your CRM
- Embed Introw forms
- Linking deals to leads via Introw
- How to use Introw forms with HubSpot
- How to use Introw forms with Salesforce

---

## How to invite Partners to your portal via Introw
Source: https://support.introw.io/en/articles/11105067-how-to-invite-partners-to-your-portal-via-introw

Welcoming partners to your new portal is quick and simple with Introw Announcements . Make sure your partner contacst have their portal access enabled before sending them any announcements.
### Make sure Partner access is enabled
Before you send an announcement, confirm that your partner contacts have their portal access enabled .
- Go to the Partners / Contacts section.
- Check that each recipient has access enabled.
- Enable access for anyone who doesn’t already have it. 
### Create an announcement
- Go to the Announcements section.
- Click New Announcement and give it a clear title, such as Welcome Email .
- Use the full editor to customize your message. You can: Insert variables for personalization Add bullet points for clarity Embed images or videos Include call-to-action buttons (e.g., Visit Portal )
- Insert variables for personalization
- Add bullet points for clarity
- Embed images or videos
- Include call-to-action buttons (e.g., Visit Portal )
### Define your audience
- Select the group of partners who should receive the announcement.
- Assign where replies should go to (e.g., a specific team member).
- Choose the channels for sending (email, in-app, slack.).
### Send the announcement
- Review your announcement and test it.
- Send it out and your partners will now get a professional, branded invitation with a direct link to your portal and or introduction video's.
✅ Tip: You can also use call-to-action buttons to direct partners to onboarding materials or introduction videos.
- Launch your partner portal
- Brand your Introw partner portal
- Add your partners to Introw
- Create a Partner portal experience
- Invite and manage partner portal users as a partner

---

## Introw Agent
Source: https://support.introw.io/en/articles/11107074-introw-agent

The Introw AI Agent is designed to provide your partners with real-time, 24/7 support directly from the partner portal. This smart agent helps partners find the information they need quickly, whether it’s guidance on registering deals, understanding their partner tier, commission plan or providing information from your shared assets.
### How to Configure the AI Agent
- Go to Engage → AI Agent Open the Configure & Test menu item
Personalize the Agent Setup the AI Agent to reflect your brand and define how it should behave:
- Avatar to Upload an image to represent the agent.
- Display Name to Choose a name that aligns with your brand.
- Welcome Message to Set the greeting partners will see when the agent starts a conversation.
- Agent Instructions to Define how the agent should respond to partners. Use this field to: Specify tone of voice and communication style Instruct the agent to respond only within the correct partner context Clarify how the agent should handle missing or unclear information Guide the agent on what it should or should not answer
- Specify tone of voice and communication style
- Instruct the agent to respond only within the correct partner context
- Clarify how the agent should handle missing or unclear information
- Guide the agent on what it should or should not answer
These instructions control the agent’s behavior and ensure consistent, accurate responses.
💡 Introw tip Provide clear context and a defined role, break down complex tasks into sequential steps, and specify the desired output format and constraints.

- Define Your Knowledge Base The Introw AI Agent uses multiple knowledge sources to answer partner questions and always responds within the correct partner context.
❗ Partner-specific access only ❗ When a partner asks a question, Introw’s AI agent only accesses and processes data that is available for that specific partner . It never references, compares, or exposes information from other partners, accounts, or organizations
- Partner portal data (enabled by default). Announcements to Updates and messages shared directly with partners. Goals to Partner-specific performance goals and progress. Tiers to Current tier status, benefits, and requirements. Commissions to Only partner assigned commission plans and statements. Assets to Portal shared assets and partner-specific assets Attributed CRM objects to Deals, leads, and any CRM records attributed to each partner. 
- Announcements to Updates and messages shared directly with partners.
- Goals to Partner-specific performance goals and progress.
- Tiers to Current tier status, benefits, and requirements.
- Commissions to Only partner assigned commission plans and statements.
- Assets to Portal shared assets and partner-specific assets
- Attributed CRM objects to Deals, leads, and any CRM records attributed to each partner. 
- Websites Public URLs that you add for Introw to securely crawl and index relevant information. These sources allow the agent to answer questions using approved public-facing content such as documentation, pricing pages, or partner enablement sites.
- Public URLs that you add for Introw to securely crawl and index relevant information. These sources allow the agent to answer questions using approved public-facing content such as documentation, pricing pages, or partner enablement sites.
- Snippets Custom Q&A logic that allows you to intercept, override, or tailor AI responses.Snippets are ideal for enforcing specific phrasing, handling sensitive questions, or ensuring consistent answers to common partner inquiries.
- Custom Q&A logic that allows you to intercept, override, or tailor AI responses.Snippets are ideal for enforcing specific phrasing, handling sensitive questions, or ensuring consistent answers to common partner inquiries.
- Documents (Internal / Non-Partner-Facing) Internal documents that partners do not directly see or need to have in their portal experience, but that provide structured knowledge to improve the Agent's  responses. Examples include: Training materials or certification outlines Sales methodologies or best-practice documents A predefined QBR structure PDF Strategy decks or internal FAQs This allows you to enrich the agent’s intelligence without exposing internal content directly to partners. How the AI can use these documents: Generate partner-specific courses or training paths based on selected content Create QBR summaries automatically using a predefined QBR structure
- Examples include: Training materials or certification outlines Sales methodologies or best-practice documents A predefined QBR structure PDF Strategy decks or internal FAQs This allows you to enrich the agent’s intelligence without exposing internal content directly to partners.
- Training materials or certification outlines
- Sales methodologies or best-practice documents
- A predefined QBR structure PDF
- Strategy decks or internal FAQs
- How the AI can use these documents: Generate partner-specific courses or training paths based on selected content Create QBR summaries automatically using a predefined QBR structure
- Generate partner-specific courses or training paths based on selected content
- Create QBR summaries automatically using a predefined QBR structure
- MCP Server Extend the AI Agent with your own external knowledge bases or tools via MCP (Model Context Protocol). This enables advanced use cases such as live system lookups, proprietary data access, or custom workflows. Learn more.
- Extend the AI Agent with your own external knowledge bases or tools via MCP (Model Context Protocol). This enables advanced use cases such as live system lookups, proprietary data access, or custom workflows. Learn more.
### Test your Introw Agent
You can easily test your AI Agent directly in the name of your partner to see how it responds to common questions. This allows you to fine-tune the knowledge base and ensure the answers reflect your tone, branding, and partner expectations, before going live.
### Conversation Insights & History
Introw gives you a complete overview of all the interactions your partners have had with your AI Agent. You can review individual conversations, see what questions were asked, how the agent responded, and evaluate the overall quality and outcome of each chat. These insights help you understand partner needs, identify common questions, and continuously improve your knowledge base and agent responses.
### How partners experience it
Once activated, your partners will see the AI Agent in the bottom-right corner of their portal. They can ask questions in natural language and receive helpful answers instantly. If needed, they can still reach out to a human contact.
### Stay notified
When a partner reaches out to the agent, the partnership manager is promptly notified to ensure seamless communication and timely response. This helps maintain strong relationships and ensures the partner's needs are addressed efficiently. The notification allows the manager to stay informed and take the necessary actions to support both the partner and the agent.
- Using Introw AI across your partners
- Install the Claude connector of Introw
- Introw + Claude: use cases & what's possible
- Introw's AI Agent in Slack
- How Introw Solves TCMA for Vendors

---

## Embed Introw in your product
Source: https://support.introw.io/en/articles/11122927-embed-introw-in-your-product

Remark : the Embed Introw feature is only available when you have a custom domain setup. Learn more and contact us if you want to explore this.
Seamlessly integrate your partner portal into your existing product or platform with just a few lines of code so your partners stay in your ecosystem while enjoying the full power of Introw.

💡 Boost engagement with a fully embedded experience Run our solution directly inside your own platform, no redirects, no extra passwords, no context switching. 
🔗 Keep the journey seamless within your product Partners stay active and focused, whether they’re in your dashboard, portal, or product. 
🛠️ Zero extra effort, everything syncs as usual Embedded usage still triggers all the same CRM workflows, automations, and data syncs.
### How does it work?
- Configure your custom domain Before embedding Introw, ensure that your custom domain is properly set up. This allows for a fully branded experience within your own platform. Learn more
- Retrieve and secure your API key Access your API key from your Settings > Developers > API Key. This key is essential for authenticating requests to Introw, so be sure to store it securely and never share it publicly. 
- Generate a partner session Create a session by making a simple API call to our session endpoint using the partner’s email. This will authenticate the user and generate a session token required for embedding. More info 
- Embed Introw in your platform Use an iframe to display the authenticated PRM session directly inside your platform. This seamless integration keeps partners within your interface while giving them full access to Introw’s features.
- Embed your google calendar in Introw
- Introw's Zapier Integration
- Embed Introw forms
- Introw workflow actions in HubSpot
- Embed Notion into Introw

---

## Embed Introw forms
Source: https://support.introw.io/en/articles/11130706-embed-introw-forms

Remark: a custom domain is required to embed the form on your website. Learn more
You can now embed the Introw forms directly into your website, making it easier than ever to capture new leads, deals, or even partner sign-ups without asking them to leave your site.

💡 Streamlined experience means higher conversion rates Make it easy for partners or leads to take action without jumping through hoops. 
🔗 Keep the journey seamless across your site Partners stay engaged, whether they’re on your homepage, a landing page, or deep in your docs. 
🛠️ No extra work, everything still syncs with your CRM Submissions trigger the same workflows, automations, and data mapping as always. 
🎯 Perfect for lead capture, partner sign-ups, or gated content Use it for demo requests, program applications, or anything else that feeds your pipeline.
### Introw forms
Inside the Introw partner portal, you can already build forms that push data straight into your CRM, like:
- A lead form that creates a new contact and deal
- A sign-up form that registers a new partner
- A deal form that starts off a deal registration
Now, with the Embed option, you can take those same forms and drop them into your own website, landing page, or help center, wherever you want to meet your audience
#### How to Embed a Form
- Go to Forms → Select the Form You Want to Embed
- Click the Share button and select Embed
- Copy the auto-generated HTML snippet
- Paste it into your website (anywhere that accepts HTML, like a CMS, landing page builder, or custom site)
That’s it. The form will appear on your website just like it does in your portal, and every submission will still trigger the same workflows in Introw and towards your CRM. 
- Create new partners via Introw
- How to use Introw forms
- Introw forms are protected from spam
- Linking deals to leads via Introw
- How to use Introw forms with HubSpot

---

## Roles and permissions
Source: https://support.introw.io/en/articles/11136281-roles-and-permissions

Introw offers role-based access control (RBAC), allowing you to manage user permissions based on their responsibilities within your partner program. Introw comes with three preconfigured roles by default: Admin , Partnership Manager , and CRM User , each designed to streamline access and maintain control across your partnership ecosystem.
You can find all roles under Settings > Team > Roles . From here you can see each role's name, the number of assigned users, and when it was created or last updated. 
You can customize these roles by renaming them or adjusting their permissions to suit your needs. Additionally, you have the flexibility to create your own roles and assign a specific set of permissions to match your workflow.
#### Access types
When editing a role, Introw lets you choose from four access types that determine the baseline level of access for that role:
Admin Grants all permissions on all Introw settings. Users with this access type have full control over every feature and setting across the platform.
Custom Allows you to manually configure individual permissions. Choose exactly which features a user can access by toggling each permission on or off.
Partner Manager Limits the user to managing only their assigned partners. This restricts visibility and actions to relevant partner data.
CRM Only User Limits users to managing their partners through the CRM with no configuration options. This role is ideal for users who only need access to Introw via the CRM card integration. Learn more
### Permissions
For each access type, you can toggle individual permissions on or off to control what team members can see and manage within Introw.
Each permission maps directly to a section in the navigation, so you can grant or restrict access at a granular level per access type.
Portal Manage access to different modules of Introw.
- Portal, Control access to portal configuration, including branding and access settings.
- Experiences, Create and manage experiences for partner interactions, such as forms, emails, and workflows.
Settings Manage team members and their access permissions.
- Integrations, Configure and oversee third-party integrations, API connections, and data sharing across systems.
- Team, Add, remove, and manage team members and define their access levels within the platform.
- Billing, Access billing information, payment methods, and invoice history.
### Notifications
Introw allows you to configure email notifications on a per-role basis. Navigate to the Notifications tab when editing a role to choose which email notifications users with that role receive.
Notifications are organized by category (e.g. Deals). For each notification type such as Deal updates, New deal, Sleeping deal, or Deal closed won, you can choose from four options:
- All partners : Receive notifications for activity across all partners.
- Own partners : Only receive notifications related to partners assigned to the user.
- Collaborating only : Only receive notifications for partners the user is collaborating with.
- Disabled : Turn off notifications entirely for that type of notification.
Not all options are available for every notification type. Some notifications, such as portal visits or form submissions, only support a subset of these options. 
You can also use the toggle at the top of each category to enable or disable all notifications within that group at once.
- Add your team to Introw
- Introw workflow actions in HubSpot
- CRM User
- Tracking Partner involvement on deals
- How does the integration with Microsoft Teams work?

---

## Introw product update - May 2025
Source: https://support.introw.io/en/articles/11170409-introw-product-update-may-2025

The latest Introw product updates from April (last month) are here! 🚀
- Role based access control: enhance security and streamline access for your team and partners.
- Introw Embed: run Introw directly inside your own platform for a seamless journey for your partners,  no redirects, no extra passwords, no context switching.
- Introw Agent: an AI Agent designed to provide your partners with real-time, 24/7 support directly from the partner portal based on your content
- UI/UX enhancements : a fresh new navigation layout , expanded branding options, and a more personalized experience across the platform.
### Role based access control
Introw offers role-based access control (RBAC), allowing you to manage user permissions based on their responsibilities within your partner program.  Learn more 
### Introw Embed
Seamlessly integrate your partner portal into your existing product or platform with just a few lines of code so your partners can have seamless journey within your application while enjoying the full power of Introw. Learn more
### Introw AI Agent
The Introw AI Agent is designed to provide your partners with real-time , 24/7 support directly from the partner portal based on your knowledge base. This smart agent helps partners find the information they need quickly, whether it’s guidance on registering deals , understanding their partner tier, commission plan or providing information from your shared assets. Learn more
### Improved partner experience
We've given Introw a fresh upgrade ! Here's what's new:
- ✨ New navigation layout, making it easier and faster to find what you need.
- 🎨 Expanded branding options, tailor the platform even more to your company's identity.
- 🏠 Dynamic personalization, a dynamic home page and navigation for partnership manager to only see data related to their partners and a dynamic partner introduction section for a smoother partner experience.
- Introw product update - March 2025
- Introw product update - June 2025
- Introw product update - August 2025
- Introw product update - October 2025
- Introw Product update - December 2025

---

## Share a deal to partners via Introw's app card in HubSpot
Source: https://support.introw.io/en/articles/11383276-share-a-deal-to-partners-via-introw-s-app-card-in-hubspot

Introw allows you to share deals with your partners straight from within HubSpot via our Collaboration card feature and will automatically set the right attribution. More info on our Introw HubSpot card feature  Imagine a sales rep working in HubSpot who identifies a deal that could benefit from partner collaboration, whether for co-selling, local support, or additional services. Instead of switching tools or manually informing the partner, the rep uses the "Share Deal" option in the Introw Collaboration card card directly within HubSpot. 
Step 1: Click "Share deal" on the Introw Collaboration card in HubSpot 
 Step 2: Decide which partner you want to share it with With just a few clicks, the rep selects the partner, adds optional context or notes, and shares the deal securely.
Step 3: Decide to who you want to share the selected deal
The partner is immediately notified and can view the deal in their partner portal, along with all relevant details or comment on it via the off-portal collaboration feature of Introw.
Step 4: Let Introw handle the rest  Once the deal is shared, Introw automatically attributes it to the right partner, keeps them engaged with real-time updates, and enables seamless collaboration directly within HubSpot.
 This seamless workflow boosts speed, ensures consistent information, and strengthens partner engagement, right from the CRM where your sales team already works.
- Link your HubSpot deals to Introw via custom properties
- Link your HubSpot deals to Introw via custom objects
- Show the Introw card inside HubSpot
- Partner Connect: a 2-way CRM integration with HubSpot
- Link an existing HubSpot deal to your vendor