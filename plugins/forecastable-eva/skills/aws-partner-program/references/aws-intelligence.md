# AWS partner program intelligence
Version: 2026.09 (built 2026-09-26). Refreshed monthly. Facts carry source tags; see Sources.

Scope: AWS Partner Network (APN), AWS Partner Central, ACE co-sell, AWS Marketplace, partner funding. Audience: Alex (strategy) and Eva (execution) serving B2B SaaS ISVs, services firms, agencies and resellers. Official sources are ground truth; VENDOR, CREATOR and INDEPENDENT claims are labeled inline where they carry a number or a judgment call.

## The twelve things that matter right now

1. **Partner Central now lives inside the AWS Management Console, and nothing new works until you migrate.** AWS launched Partner Central in the console on November 30, 2025 [A11][A4]. Migration is self-service, takes 2 to 6 hours, blocks all users during the window and cannot be reversed; after migration the linked AWS account is permanent and all ACE history is tied to it [A8][A112]. Partner Central agents, the funding agent, lead prospecting and the MCP server all require a migrated account [A43][A46][A78]. AWS publishes no hard cutoff date [A8][A11]; one vendor claimed June 30, 2026 [A102], another (August 2026) says no end-of-life date is published [A9]. Treat an unmigrated account as the first fix.

2. **ACE is now scored and triaged by AI, so "submit and wait for a rep" is dead.** Every open opportunity gets an Opportunity Quality Score (0 to 100) and one of three co-sell motions: AWS Field-engaged, Agent-engaged, or Partner-led [A3][A75]. AWS says a higher score "may increase the likelihood" of field engagement "but it does not guarantee" it [A3]. Practitioners report most scores landing under 40 and a record scoring 85 still routed Partner-led (CREATOR) [A87][A88]. The score rewards record quality (specific business problem, dated next step with owner, Pricing Calculator MRR, real AWS services, tagged solution) [A3][A43]. It does not replace a human relationship with the AWS account team.

3. **Partner Revenue Measurement (PRM) is the new currency.** PRM (GA January 30, 2026) attributes AWS consumption to your Marketplace product via resource tag `aws-apn-id = pc:<product-code>`, a User Agent string `APN_1.1/pc_<product-code>$`, or automatic Marketplace metering for AMI/ML [A12][A13][A14]. It gates the FTR (product must be PRM-enabled) [A49], the new ISV Accelerate MDF (enrolled after January 1, 2026 plus PRM plus co-sell criteria) [A6], and feeds the Attributed Revenue dashboard (data lands 17 days after month end) [A77]. Revenue Attribution IDs (`ra-` prefix, launched June 30, 2026) map that revenue to specific ACE opportunities and private offers [A50][A43].

4. **The FTR is now a minutes-long automated check, but the prerequisites catch people.** Submit a SOC 2 Type II or a Well-Architected Framework Review (PDF, max 3 MB) in Build > Solutions > Validation; approval or feedback comes back in minutes and lasts two years [A19][A49]. Checks run in sequence: solution linked to exactly one AWS Marketplace software product (SaaS, AMI, container or ML), no non-Marketplace products, an approved AWS-hosted architecture diagram, and PRM enabled (allow up to 7 days for data) [A49]. FTR moves a Software Path partner from Registered to Validated [A21].

5. **ISV Accelerate criteria (verified on the official page, September 2026):** GA software product in AWS Marketplace; ACE eligibility; Validated or Differentiated status; Amazon Payee Central set up; at least 5 launched opportunities (ACE or Marketplace private offers) and at least 15 qualified ACE opportunities in the past 12 months; at least 1 person through the Co-Selling with AWS learning module; at least $2,000 recognized AWS account revenue at enrollment [A1]. New March 2026 benefits: MDF (new ISVA enrollees after January 1, 2026 who implement PRM and meet co-sell engagement criteria), in-person partner workshops, and Partner Central agents [A6]. MDF amounts are not published (login-gated MDF Guide) [A6].

6. **Why an AWS seller cares: the SaaS Co-Sell Benefit.** Since January 2025 the SaaS revenue recognition benefit (formerly invite-only) covers all ISV Accelerate partners transacting in AWS Marketplace, including startups [A79]. Vendors describe it as quota retirement for AWS sellers when they co-sell SaaS through Marketplace private offers (VENDOR) [A37][A34]. Exact credit percentages are not published [A84]. Practical rule: an ISVA partner's private offer linked to an ACE opportunity is the transaction an AWS account manager gets paid on.

7. **Marketplace fees are low and falling.** Public SaaS 3%, public server (AMI, container, ML) 20%, private offers 3% under $1M TCV, 2% from $1M to under $10M, 1.5% at $10M or more, all renewals 1.5% (since January 5, 2024) [A24][A115]. CPPO adds 0.5% [A24]. Professional services private offers dropped from 2.5% to 0.5% on June 16, 2026 [A28] and to 0% when bundled in a qualifying multi-product solution with a paid product (September 1, 2026) [A29]. South Korea buyers add 1% (April 1, 2025) [A24].

8. **Committed-spend drawdown requires "Deployed on AWS", and even that is not a guarantee.** From May 1, 2025, only SaaS hosted entirely on AWS counts toward customer EDP/PPA commitments (INDEPENDENT and VENDOR reporting) [A38][A39]; AWS's own buyer FAQ says products "deployed on AWS typically qualify" and eligibility is per product [A60]; Suger (VENDOR) confirms "Deployed on AWS" is necessary but not sufficient, so check each product in the buyer FAQ terms before promising drawdown. The historic 25%-of-commitment cap on Marketplace retirement is a contract term, not a published rule; verify per customer [A38][A39].

9. **Every co-sell record now has to point at something AWS can see.** You must associate at least one solution or AWS Marketplace product to create an opportunity [A43]; since July 1, 2026 you can attach up to 10 Marketplace solutions and 10 Marketplace products directly, and an opportunity cannot move to Committed or Launched without one [A95]. API limit: 1 private offer per opportunity [A48]. Unlinked private offers are invisible pipeline.

10. **Funding is being automated and tied to outcomes.** The funding agent recommends programs and drafts fund requests from the opportunity page [A46][A15]. Marketplace Private Offer Promotion Program (MPOPP) delivers customer credits the next business day after offer acceptance, self-service, year-round [A31][A7]. New 2026 money: $25K extra MDF for agentic AI category validation [A73][A71], up to $50K MDF for Amazon Connect implementations, up to $50K industry MDF in BOX [A7], and Business Value Realization (June 16, 2026) paying services partners on customer-attested milestones [A98]. Dollar tables live in the login-gated AWS Partner Funding Benefits Guide.

11. **Marketplace is becoming a lead source, not only a procurement rail.** Since September 9, 2026, demo and private offer requests from listings arrive as qualified leads instantly instead of waiting for manual AWS qualification [A96]. Partner Lead Prospecting (July 9, 2026) generates sales plays, call scripts and email templates for ACE-eligible partners [A97]. Buyers now use agent mode (search, comparison and evaluation agents) [A62]. Storefront (GA June 16, 2026) gives no-code branded catalogs [A99]. Express private offers automate standard SaaS contract deals [A54].

12. **Specializations are consolidating around Competencies.** AWS Service Delivery and Service Ready specializations close to new applications now and are deprecated June 1, 2027 [A20]. Three agentic AI categories were added to the AI Competency (November 30, 2025) [A73], validation agents cut processing time up to 70% [A71], and specialization badges now appear in Marketplace search results [A71]. Plan badges around Competencies, not Service Ready.

## 0. Program map and vocabulary

### The layered model (AWS version)

| Layer | What it is at AWS | Where it lives | Gate to next layer |
|---|---|---|---|
| 1. Org membership | APN registration in Partner Central (console), identity and business verification, ACE and APN terms accepted | Partner Central > Get started [A44] | Paid AWS account in good standing, one Partner Central account per legal entity [A44] |
| 2. Path and stage | Path enrollment (Software, Services, Hardware, Training, Distribution); stages Registered, Validated, Differentiated [A18][A21] | Partner Scorecard [A45] | FTR (Software) or Select tier (Services) |
| 3. Solution and listing | Solutions (Build > Solutions) linked to Marketplace products; Partner Solutions Finder listing [A49] | Build menu; AMMP for listings [A45] | At least one Limited or Public solution to create an ACE opportunity [A43] |
| 4. Technical validation | FTR (2-year validity), Competencies, MSP, Qualified Software badge [A19][A20] | Solutions > Validation; Program Applications [A49][A45] | PRM enabled for FTR [A49] |
| 5. Co-sell eligibility | ACE eligibility (receive AWS referrals), ISV Accelerate [A1][A109] | Sell > Opportunities, Leads [A45] | ACE T&C plus eligibility criteria (FAQ is login-gated) |
| 6. Opportunity execution | ACE opportunities, Quality Score, co-sell motion, AWS referrals, multi-partner opportunities [A3][A43] | Sell > Opportunities | Approved review status |
| 7. Incentives and funding | MDF, POC, MAP, ISV WMP, MPOPP, BVR, BOX, PGP [A65][A7] | Funding Benefits > Funding dashboard, Wallets [A45] | Program eligibility plus linked opportunity |
| 8. Channel and private offers | Private offers, CPPO, selling authorizations, multi-product offer sets, Buy with AWS, Storefront [A52][A53][A99] | Sell > Private offers (redirects to AMMP) [A45] | Active public listing for private offers [A52] |

### What replaced what (retired names still on the web)

| Old name (still seen) | Current name / status | Source |
|---|---|---|
| APN Portal / legacy Partner Central (partnercentral.awspartner.com, email login) | AWS Partner Central in the AWS Console (IAM login), launched 2025-11-30 | [A11][A8] |
| AWS Marketplace Management Portal (AMMP) as separate place | Still exists; many console menu items "redirect to AMMP" | [A45] |
| ISV Partner Path / Technology Partner | Software Path | [A21] |
| Consulting Partner | Services Path (Select, Advanced, Premier tiers) | [A17][A18] |
| Registered / Select / Advanced / Premier Technology Partner tiers | Software Path stages Registered, Validated, Differentiated (tiers only on Services Path) | [A21] |
| Enterprise Discount Program (EDP) | Private Pricing Agreement (PPA); both terms used | [A89][A60] |
| SaaS Revenue Recognition program | Merged into SaaS Co-Sell Benefit for ISVA partners (January 2025) | [A37][A79] |
| Amazon S3-based CRM integration ("Sync with AWS", "Send to AWS") | Partner Central Selling API ("Share with AWS"); S3 closed to new users | [A47][A9] |
| Partner Growth Rebate credits | Partner Growth Discounts | [A45] |
| Partner Originated discount (resellers) | New Customer Incentives (re:Invent 2025) | [A92] |
| Service Delivery / Service Ready specializations | Closed to new applications; deprecated 2027-06-01 | [A20] |
| Solution IDs `S-xxxx` | New `soln-` format after console migration (CRM connector support lagged) | [A9][A47] |
| Partner Assistant chatbot | Amazon Q based Partner Assistant, plus Partner Central agents (March 2026) | [A4][A15] |

### Glossary

| Term | Meaning | Source |
|---|---|---|
| APN | AWS Partner Network. Joining is free; annual APN fee applies to paths and tiers ($2,500/year on Services tiers) | [A18][A17] |
| Partner Central | Partner portal, now an AWS Console service; IAM-based access | [A11] |
| AMMP | AWS Marketplace Management Portal, where listings, offers, agreements, selling authorizations are managed | [A45] |
| ACE | APN Customer Engagements: the co-sell pipeline program (opportunities, leads, referrals) | [A109] |
| ACE Pipeline Manager | UI for sharing opportunities, now Sell > Opportunities | [A2][A45] |
| Opportunity Quality Score | 0 to 100 AI score on each open opportunity, with trend indicator | [A3] |
| Co-sell motion | AWS Field-engaged, Agent-engaged, or Partner-led, assigned per opportunity | [A3] |
| Involvement type | API values `Co-Sell` or `For Visibility Only` | [A42] |
| Review status | Pending Submission, Submitted, In review, Action Required, Approved, Rejected | [A41] |
| Stage | Prospect, Qualified, Technical Validation, Business Validation, Committed, Launched, Closed Lost | [A41] |
| FTR | Foundational Technical Review, 2-year validity | [A19] |
| PRM | Partner Revenue Measurement | [A13] |
| RA ID | Revenue Attribution ID (`ra-` plus 13 chars), deal-level PRM overlay | [A50] |
| ISVA | ISV Accelerate, AWS's co-sell program for software partners | [A1] |
| SCB | SaaS Co-Sell Benefit, the seller-compensation benefit for ISVA partners | [A37] |
| CPPO | Channel Partner Private Offer: reseller extends an ISV's product under a selling authorization | [A53] |
| MPPO | Marketplace (seller-issued) private offer | [A55] |
| Selling authorization / resale authorization | ISV grant to a channel partner (by 12-digit AWS account ID) with wholesale price | [A53] |
| PPA / EDP | Customer committed-spend agreement with AWS | [A60] |
| MDF | Marketing Development Funds (cash or credits) | [A65] |
| MAP | Migration Acceleration Program (Assess, Mobilize, Migrate and Modernize) | [A66] |
| ISV WMP | ISV Workload Migration Program: credits for moving customer workloads to partner SaaS on AWS | [A68] |
| MPOPP | Marketplace Private Offer Promotion Program: customer credits on private offers | [A31] |
| BOX | Business Outcomes Xcelerator: multi-partner solution program | [A23][A7] |
| PGP | Partner Greenfield Program: new-to-AWS customer acquisition | [A69] |
| BVR | Business Value Realization: post-deployment adoption motion with milestone funding | [A98] |
| SCA | Strategic Collaboration Agreement: negotiated multi-year investment agreement | [A71][A46] |
| PDM / PDR | Partner Development Manager / Representative, owns your partnership | [A32][A43] |
| PSM / ISM | Partner Sales Manager / ISV Sales Manager, field-facing partner sellers | [A32] |
| PSA | Partner Solutions Architect, does technical approval on POC fund requests | [A46] |
| PSS | Partner Success Specialist (BVR reviewer) | [A98] |
| Payee Central | Amazon system for partner cash payouts (MDF, MAP claims, invoices) | [A1][A46] |
| Deployed on AWS | Marketplace badge for SaaS entirely hosted on AWS; drives commit eligibility | [A38] |
| PSF | Partner Solutions Finder, AWS's public partner directory | [A49] |

## 1. Fiscal calendar, org and where decisions get made

### Fiscal year and planning moments

| Item | Detail | Source |
|---|---|---|
| Fiscal year | Amazon reports on the calendar year (Q1 ends March 31; FY ends December 31) | [A110] |
| OP1 | Amazon's main annual operating plan, drafted roughly August to October, reviewed October to December | [A82] |
| OP2 | January adjustment of OP1 after the year closes | [A82] |
| Implication | Ask your PDM in August/September what your AWS team is writing into OP1 (target segments, named ISVs, SCAs). By January, headcount, territories and partner priorities are set for the year | [A82] (inference labeled) |
| re:Invent 2026 | November 30 to December 4, 2026, Las Vegas; partner program announcements cluster here (2025 partner recap blog published December 1) | [A94][A7] |
| AWS Partner Awards | 2026 nominations announced July 10, 2026; regional winners announced April 2026 | [A74] |
| Program-year changes | Many incentives reset January 1 (MSP incentives effective January 1, 2026; ISVA MDF for enrollees after January 1, 2026; Amazon Connect MDF launched January 2026) | [A92][A6][A7] |
| Monthly competency cadence | AWS posts new Competency/MSP partners monthly ("Say Hello to ..." posts) | [A74] |

### Field roles a partner deals with

| Role | What they do for you | Source |
|---|---|---|
| Account Manager (AM / AWS seller) | Owns the customer; named on referrals as "AWS Sales Rep" and "AWS Account Owner" | [A43][A32] |
| Partner Development Manager (PDM) / PDR | Owns your partnership, business plan, program nominations, funding sponsorship; consult on co-sell objectives | [A32][A43] |
| WWPS PDM | Public sector partner development manager | [A43] |
| Partner Success Manager / ISV Success Manager (PSM) | Named on AWS referrals; bridges partner and field | [A43] |
| ISV Sales Manager (ISM) / Partner Sales Manager (PSM) | Field-aligned partner sellers; key co-sell stakeholders | [A32] |
| Partner Solutions Architect (PSA) | Technical approval stage on POC fund requests | [A46] |
| AWS Reviewer / Business Approver / Finance | Fund request approval stages | [A46] |
| Marketplace Customer Advisors / Marketplace BD / Channel Account Managers | Marketplace and channel roles in the AWS sales org | [A32] |
| Partner Success Specialist (PSS) | Reviews BVR activity submissions | [A98] |
| Partner Territory Managers | SMB-focused (Small Business Acceleration Initiative, January 2025) | [A79] |
| AI agents | Agent-engaged motion: the Partner Central agent qualifies and enriches deals before any human | [A3] |

### How AWS sellers are compensated on partner and Marketplace deals

| Mechanism | What it means | Label and source |
|---|---|---|
| SaaS Co-Sell Benefit (SCB) | From January 2025, available to all ISVA partners transacting in Marketplace (previously invite-only); AWS sellers receive quota retirement when co-selling SaaS/PaaS via Marketplace private offers | OFFICIAL for expansion [A79]; VENDOR for quota wording [A37][A34] |
| ISV Accelerate "incentive structures for co-sell transactions" | Official page says ISVA partners appear in AM solution libraries and recommendation engines with incentive structures for co-sell transactions | OFFICIAL [A1] |
| Consumption | AWS sellers are paid on AWS consumption growth; PRM and "Deployed on AWS" connect your product to that number | VENDOR [A36]; OFFICIAL PRM [A13] |
| Earned, not given | Former alliance leader: field referrals and co-sell support from Marketplace are "earned, not gotten"; sellers favor ISVs showing AWS consumption growth and Marketplace wins (VENDOR interview) | [A83] |
| Customer commit burn-down | Customers can retire eligible PPA/EDP commitments with Marketplace purchases, which helps the AM hit commit targets | [A60][A38] |
| Co-sell recommendation score | AWS matching tools recommend partners to sellers based on listing quality, past opportunities, partnership progress, past performance | [A47][A71] |
| Not published | Exact quota credit percentages, accelerators, and SPIFF amounts | [A84] |

Why a seller cares, in one line: an AWS AM gets retirement credit and a commit burn-down when your deal closes as an ISVA private offer on a "Deployed on AWS" product that is linked to an ACE opportunity, and gets nothing extra when you sell direct.

### Where decisions get made

- Program membership, tiers, competencies: Partner Admin > Program Applications (still redirects to legacy experience) and Partner Scorecard [A45].
- Co-sell routing: an AI model assigns the motion; humans on the AWS side still decide whether to engage [A3][A87].
- Funding: stage-gated workflow (AWS Review, Tech Approval by PSA, Business Approval, Finance Approval) [A46].
- Strategic investments (SCA, co-investment): negotiated with PDM leadership; tied to AWS consumption give-and-get (CREATOR) [A89][A114].

## 2. Navigating the portal(s)

### Portals

| Portal | URL / access | Used for | Source |
|---|---|---|---|
| AWS Partner Central (console) | https://us-east-1.console.aws.amazon.com/partnercentral/home, IAM or SSO login into the linked AWS account | APN, ACE, funding, analytics, solutions | [A56][A11] |
| Legacy Partner Central | partnercentral.awspartner.com | Still used for case studies, badge manager, program applications, business plans, support, distributor requests, device listings | [A45] |
| AMMP | Redirect targets from console menus | Listings, offers, agreements, selling authorizations, file upload, refunds | [A45] |
| AWS Partner Funding Portal | Via Funding Benefits > Funding dashboard | Fund requests and claims | [A46] |
| Payee Central | Link from approved cash claims | Invoices and cash payouts | [A46] |
| Marketing Central | Go to Market > Marketing Central | Joint campaign assets | [A45] |
| Partner Central MCP server | JSON-RPC 2.0 over HTTPS, SigV4 or OAuth with AWS Sign-In (us-east-1, August 20, 2026) | Agents inside your own tools | [A48][A100] |

### Console navigation map (menu paths)

| Top menu | Items (N = native in console, R = redirect) | Source |
|---|---|---|
| Build | Solutions (N); AI agents and tools, SaaS products, Server products, ML products, AMI, Data products, Professional services, Requests, File upload (R to AMMP); Device listings (R legacy) | [A45] |
| Go to Market | Marketing Central (R); Case studies (R legacy); Badge manager (R legacy) | [A45] |
| Sell | Leads (N); Opportunities (N); Private offers, Public free trials, Agreements, Selling authorizations (R to AMMP) | [A45] |
| Funding Benefits | Funding dashboard (N); Wallets (N) | [A45] |
| Channel management | Channel partner management (N); Distribution engagement requests (R legacy) | [A45] |
| Account connections | Partner discovery (N); Partner connections (N) | [A45] |
| Partner analytics | At a Glance, Opportunities, Leads, Investments, Channel, Marketing Campaigns, Training and Certifications, Attributed Revenue | [A45][A77] |
| Marketplace insights | Agreements and renewals, Usage, Billed revenue, Collections and disbursements, Tax | [A45] |
| Partner admin | Program applications (R legacy); Business plan (R legacy); Profiles (N); User onboarding (R to IAM); Partner Central settings (N); Marketplace settings (R); Partner Central support (R legacy); Marketplace support (R); Marketplace refund support (R) | [A45] |

### Account linking

- Required if your company used legacy Partner Central with email credentials; not required if you registered directly in the console with an AWS account [A112].
- Linked account manages APN fee payments, solutions and ACE; resources cannot be transferred to another AWS account [A112].
- Starting November 15, 2025, APN fee billing is processed only for Partner Central accounts with a linked AWS account on a Paid plan at renewal [A112].
- Account must be paid (not Free Tier), company-owned (not a distributor's), able to onboard future users, and have a legal entity address matching your primary business location. Do not use developer, personal, or (not recommended) management/payer or Marketplace buyer accounts [A44][A112].
- Before migration you can unlink and relink; after migration the link is permanent [A112].
- Roles: IAM Administrator completes prerequisites; Alliance Lead (or delegated Cloud Admin) performs linking [A112].

### IAM managed policies (assign per user or role)

| Policy | Grants | Source |
|---|---|---|
| AWSPartnerCentralFullAccess | Everything: opportunities, leads, fund requests, settings, profiles, Marketing Central, channel, connections, business plans, scorecard, analytics, badges, Amazon Q, program applications, support | [A45] |
| AWSPartnerCentralOpportunityManagement | Opportunities and leads | [A45] |
| AWSPartnerCentralSandboxFullAccess | Sandbox catalog | [A45] |
| AWSPartnerCentralChannelManagement / ChannelHandshakeApprovalManagement | Channel program (Billing Transfer) | [A45][A4] |
| AWSPartnerCentralMarketingManagement | Marketing Central | [A45] |
| PartnerCentralIncentiveBenefitManagement | Funding and benefits | [A45] |
| AWSPartnerCentralRevenueAttributionManagement / AWSRevenueAttributionManagement | PRM Revenue Attribution IDs | [A45][A43] |
| PartnerCentralAccountManagementUserRoleAssociation | Cloud admin maps users to `PartnerCentralRoleFor*` roles | [A45] |
| AWSMarketplaceSellerFullAccess / AWSMarketplaceSellerOfferManagement | Marketplace seller actions; needed for registration and offer linking | [A44][A112] |

Registration error "Access denied" means the user lacks AWSPartnerCentralFullAccess plus AWSMarketplaceSellerFullAccess [A44]. Users needing only Skill Builder no longer need Partner Central access [A8].

### Subsidiary account connections

Account connections > connect subsidiary seller accounts. Level 1 (connection) consolidates PRM attribution; Level 2 (subsidiary chooses Associate qualifications) consolidates scorecard, recalculates tier eligibility, shares specializations and certifications, and rebrands the subsidiary "[Subsidiary] by [Primary]" [A112]. Without connections, seller-account revenue may not count toward attribution, funding eligibility or SCA compliance [A112].

## 3. Registration: step by step

### Prerequisites checklist

| Item | Why | Source |
|---|---|---|
| One AWS account on a Paid plan, in good standing, owned by your company, ideally a member account (not the payer) | Partner Central is provisioned in this account; all users get access to it | [A44] |
| Government photo ID and a smartphone camera for the registrant | Identity verification (selfie plus ID via QR code) | [A44] |
| Legal business name, country of incorporation, business tax ID (EIN, VAT, GST), state/province | Business verification; personal SSNs, sole proprietors without registration, students and non-commercial entities cannot verify | [A44] |
| Alliance lead contact (use a shared alias such as aws-partners@) and business email | APN communications and policy notices | [A44] |
| IAM admin available | Assign AWSPartnerCentralFullAccess and AWSMarketplaceSellerFullAccess | [A44] |
| Bank account that accepts USD, W-9 or W-8 tax form | Needed later for paid Marketplace listings and Payee Central | [A51][A56] |

### Steps (new partner, no legacy account)

1. Go to the APN page, choose **Become a partner**, sign in to the chosen AWS account. Done when you land on the AWS Console home in the right account [A44].
2. Console search > **AWS Partner Central** > **Get started**. Done when the pre-registration modal appears [A44].
3. **Identity verification**: Continue to Registration, scan QR code, complete selfie and ID on mobile. Usually under a minute; 3 attempts per 24 hours [A44].
4. **Business verification**: legal name, country, tax ID, state. Up to an hour; if it fails, supply the supplementary form (tax/VAT number, registration number, full incorporation address) [A44].
5. **Registration form**: alliance lead name, title, primary product or service type; verify business email with a code; optional tags (for example Region or Sector to restrict user access); accept APN Terms and **APN Customer Engagements (ACE) Terms**; Submit registration. Done when you are redirected to the Partner Central dashboard [A44].
6. **Onboarding agent**: use the Getting Started cards on the dashboard. The agent auto-populates the partner profile from your website, sets profile visibility (PUBLIC or PRIVATE), links training domains, runs the tax interview (W-9, W-8BEN, W-8BEN-E), explains banking and KYC/BAV, guides Marketplace seller (ESC catalog) registration, and checks or creates the `AWSServiceRoleForMarketplaceResaleAuthorization` service-linked role needed for CPPO [A45][A5].
7. **Enroll in a path** (Software, Services, Hardware, Training, Distribution) and track progress in the Partner Scorecard. Removing a path requires APN Support [A45].
8. **Pay the APN fee** from the linked account (fee billed to the linked account) [A8][A112].
9. **Create a solution** (Build > Solutions) and, for software, list on Marketplace, enable PRM, request FTR (see section 13 runbooks) [A49].

Time to complete: registration itself is same-day (verification minutes to an hour) [A44]. AWS's June 2026 messaging is "registered to actively selling" in days rather than weeks with agents [A5]; one partner launched four listings within an hour [A5]. Marketplace listing review is 7 to 10 business days per AWS with 2 to 4 weeks recommended end to end (VENDOR summary) [A25]; Clazar cites 3 to 10 business days for SaaS [A85].

### Existing partner (legacy account) steps

1. Do not register again; a new registration "will replace all of your historical partner data." "Domain in use" or "Not Registered" means you must migrate instead [A44].
2. Export legacy user list (Alliance Lead) and map roles to managed policies (Last Login Date helps prune) [A8].
3. IAM admin creates users or SSO permission sets with the policies [A8].
4. Link the AWS account (before migration you can still change it) [A112].
5. Alliance Lead or Cloud Admin opens the self-service migration tool, completes the pre-migration checklist and business verification, schedules a window (2 to 6 hours; off-hours) [A8][A10].
6. After the confirmation email, users sign in with IAM credentials [A8].
7. If you use a CRM integration on Amazon S3, move to the API (account linking is the only hard prerequisite; can be done before console migration) [A47].

### Common blockers

| Blocker | Fix | Source |
|---|---|---|
| "Partner Registration requires a paid AWS account in good standing" | Upgrade from Free Tier to Paid plan in Billing | [A44] |
| "Access denied" at verification | Attach AWSPartnerCentralFullAccess and AWSMarketplaceSellerFullAccess | [A44] |
| "Domain in use" | Company already has legacy account; migrate it | [A44] |
| Identity check fails | Use a photo ID with a recent picture; retry after 24 hours after 3 failures | [A44] |
| Business verification fails | Supplementary form with registration number and incorporation address | [A44] |
| Wrong account linked (payer or reseller's) | Unlink before migration; after migration it is permanent | [A112] |
| Firefox ESR | Not supported for account linking | [A112] |
| Agents missing | Account not migrated or IAM lacks `partnercentral:UseSession` | [A43] |

## 4. Tiers, paths, designations, competencies, badges: exact qualification criteria

### Paths

| Path | For | Validation mechanism | Source |
|---|---|---|---|
| Software | Software that runs on or integrates with AWS | Foundational Technical Review | [A18] |
| Services | Consulting, professional, managed, value-added resale services | Services Partner Tiers | [A18] |
| Hardware | Devices compatible with AWS | Device Qualification Program | [A18] |
| Training | Sell, deliver or embed AWS training | AWS Training Partner designation | [A18] |
| Distribution | Recruit and support resellers | AWS Authorized Distributor | [A18] |

A company can enroll in multiple paths (for example Software plus Services) [A45].

### Software Path stages

| Stage | Requirement | Unlocks | Source |
|---|---|---|---|
| Registered | APN registration, path enrolled | Partner Central, training; no commercial benefits | [A21] |
| Validated | Approved FTR (renew every 2 years or lose it) | Commercial programs: ISVA eligibility, ISV WMP, funding, Qualified Software badge, PSF listing | [A21][A19][A68] |
| Differentiated | Specialization (Competency, etc.) | Deeper field engagement, BOX, PGP (requires Differentiated) | [A21][A69] |

### Foundational Technical Review (FTR) detail

| Item | Current rule | Source |
|---|---|---|
| Evidence | SOC 2 Type II (third-party, covering the AWS-hosted workload) or WAFR report covering the primary AWS-hosted workload | [A49] |
| Report age | Less than one year old (VENDOR) | [A21] |
| Format | PDF, max 3 MB | [A49] |
| Prerequisite 1 | Solution linked to an AWS Marketplace product (requires account linking or console) | [A49] |
| Prerequisite 2 | Exactly one Marketplace product per solution | [A49] |
| Prerequisite 3 | No non-Marketplace products in the solution | [A49] |
| Prerequisite 4 | Product is software type: SaaS, AMI, Container, or ML (professional services not eligible) | [A49] |
| Prerequisite 5 | Approved AWS-hosted architecture diagram uploaded in AMMP ("deployed on AWS") | [A49] |
| Prerequisite 6 | PRM enabled; complete when product shows as onboarded in Attributed Revenue (up to 7 days) | [A49] |
| Turnaround | Minutes; result Approved or Action required with failed checks | [A49][A19] |
| Validity | 2 years | [A19] |
| Cost | Free | [A19] |
| Unlocks | Qualified Software badge, PSF listing, Competency access, ISVA eligibility, funding and marketing | [A19] |
| Launch | Streamlined FTR announced June 2026 | [A5] |
| FTR funding | Addressing at least 25% of high-risk items makes partners eligible for Well-Architected ISV promotional credits (VENDOR, date 2026-03) | [A16] |

### Services Path tiers (annual fee $2,500 per year at every tier)

| Requirement | Select | Advanced | Premier | Source |
|---|---|---|---|---|
| Accredited individuals | 4 (2 technical, 2 business) | 8 (4 technical, 4 business) | 20 (10 technical, 10 business) | [A17] |
| AWS Foundational certified | 2 | 4 | 10 | [A17] |
| AWS Technical certified | 2 | 6 (min 3 Professional or Specialty) | 25 (min 10 Professional or Specialty) | [A17] |
| Launched opportunities | 3, total MRR at least $1,500 | 20, total MRR at least $10,000 | 50, total MRR at least $50,000 | [A17] |
| Business plan | No | Partner Business Plan | Partner Business Plan plus Executive Business Review | [A17] |
| Competencies | None | None | 3 AWS Competencies, including MSP, DevOps or CloudOps | [A17] |
| Sustained | No | No | More than 6 months of sustained attainment | [A17] |
| 2024 change | CSAT and public reference requirements removed July 10, 2024; case studies emphasized | | | [A23] |

Launched opportunities are counted from ACE (stage Launched, AWS account ID attached) [A43]. Business Value Realization requires Advanced or Premier plus a qualifying domain competency [A98].

### ACE eligibility (receive AWS referrals)

Official: join APN, accept ACE T&C, share opportunities, update them regularly; eligibility details sit in the login-gated ACE FAQ [A109]. Vendor summary of the FAQ (undated, derived from a November 2023 FAQ) [A108]:

| Partner type | Criteria (VENDOR, verify in ACE FAQ) |
|---|---|
| Software Path | ACE T&C accepted; at least one solution; FTR passed (SaaS); at least 15 opportunities submitted and validated; active PSF listing |
| Services Advanced or Premier | ACE T&C; active PSF listing |
| Services Select | Above plus 10 AWS-validated opportunities plus one program designation (Competency, MSP, ISVA, Public Sector, Service Delivery, Well-Architected, Service Ready, or Global Startup) |

AWS referrals must be accepted within 5 business days or they disappear from Opportunity Invitations [A43]. Partner Lead Prospecting is available to all ACE-eligible partners [A97].

### ISV Accelerate (official, fetched 2026-09-26)

| Requirement | Threshold | How measured | Source |
|---|---|---|---|
| Marketplace product | 1 or more software products GA in AWS Marketplace | AMMP listing status | [A1] |
| ACE | ACE program eligibility | ACE status | [A1] |
| Stage | Validated or Differentiated | Partner Scorecard | [A1] |
| Payee | Amazon Payee Central account set up | Payee Central | [A1] |
| Launched opportunities | Minimum 5 in past 12 months (ACE or Marketplace private offers) | ACE Launched, accepted private offers | [A1] |
| Qualified opportunities | Minimum 15 qualified in ACE in past 12 months | ACE | [A1] |
| Training | At least 1 individual completed Co-Selling with AWS learning module | Skill Builder / training records | [A1] |
| AWS revenue | At least $2,000 recognized AWS account revenue at enrollment | Reported at enrollment | [A1] |
| Benefits | Visibility in AM solution libraries and recommendation engines with co-sell incentives; training/events; ISV funding including MPOPP and ISV WMP; MDF for new enrollees after 2026-01-01 with PRM; in-person workshops; agents | | [A1][A6] |
| Tackle note | Vendor guide also says to mark ACE opportunities "Co-sell Support Needed" for the 15 qualified | VENDOR | [A37] |

### Competencies, specializations, badges

| Item | Current state | Source |
|---|---|---|
| Specialization types | AWS Competency; AWS Service Specializations (Service Delivery, Service Ready: closed to new applications, deprecated 2027-06-01); MSP | [A20] |
| Competency count | 43+ competencies across industries, use cases, workloads | [A20] |
| Agentic AI categories (AI Competency) | Agentic AI Applications, Agentic AI Tools, Agentic AI Consulting Services; Validated or Differentiated members of Services or Software Path; $25K extra MDF on validation plus existing $50K for AI Specialization; 60 launch partners | [A73] |
| Other 2025 additions | Resilience Competency extended to Software Partners (3 categories); MSSP Competency (7 categories); Government Competency (3 categories); SMB Competency ($25K MDF) | [A71] |
| Validation agent | AI Competency validation automated, up to 70% faster, expanding through 2026 | [A71][A7] |
| Badges | Category-level badges; badges shown in Marketplace search results | [A71] |
| BVR Competency | $50,000 MDF annually (2026 to 2027) for partners achieving it (INDEPENDENT) | [A72] |
| Buyer weight | 87% of customers cite specializations as a top-3 selection criterion; 60% as primary factor (VENDOR citing AWS) | [A16] |
| Renewals | Partners report renewals now require launched ACE opportunities tied to the specialization's solutions over rolling 12 months (INDEPENDENT) | [A34] |
| Qualified Software | Badge earned through FTR | [A19] |

### Other programs and what they require

| Program | Eligibility | Source |
|---|---|---|
| ISV Workload Migration Program | Fully managed SaaS on AWS; FTR for the nominated workload; qualified migration use case; Software Path | [A68] |
| Partner Greenfield Program | Executive sponsorship; Differentiated; Services: Migration Competency plus Security or Generative AI Competency; Software: enrolled in ISVA; dedicated team with greenfield wins | [A69] |
| BOX | Validated or Differentiated (2024); expanded to business consulting and advisory partners March 19, 2026; 350+ solutions; up to $50K industry MDF | [A23][A74][A7] |
| BVR | Consulting, SI and MSP partners at Advanced or Premier with qualifying domain competency | [A98] |
| MSP | Three new MSP benefits for 2026; MSP incentives effective January 1, 2026 | [A7][A92] |

## 5. Marketplace

### Seller eligibility

| Seller type | Requirement | Source |
|---|---|---|
| All | AWS account in good standing; accept seller T&C; valid non-alias email; IAM roles recommended | [A51] |
| Free products | Production-ready, full-feature software; support process; patching | [A51] |
| Paid or BYOL | Resident or entity in eligible jurisdiction (Australia, Bahrain, Colombia, EU member states, Hong Kong SAR, India, Israel, Japan, New Zealand, Norway, Qatar, South Korea, Switzerland, UAE, UK, US); W-9 or W-8; bank account accepting USD; KYC for EMEA sales, Korea, or UK bank accounts; bank account verification | [A51] |
| Professional services | Complete DAC7 tax questionnaire | [A51] |
| USD disbursement | Mandatory for all sellers (public offers are USD only); India sellers use INR | [A56] |
| Private offers | At least one active public listing | [A52] |

### Listing types and pricing models

| Type | Notes | Source |
|---|---|---|
| SaaS subscription (PAYG) | Metered hourly via Metering Service; up to 200 dimensions; EventBridge replacing SNS notifications | [A57] |
| SaaS contract | Upfront or scheduled billing; entitlement checks via Entitlement Service; durations Monthly, 1, 2, 3 years; private offers up to 144 months; dimension API name max 15 characters, immutable | [A57] |
| SaaS contract with consumption | Contract plus metered overage | [A57] |
| AMI, container, ML | Server products (20% public fee) | [A24] |
| AI agents and tools | Category launched July 2025; API (vendor-hosted, including Bedrock AgentCore Gateway) or container (Bedrock AgentCore Runtime) deployment | [A27][A58] |
| Data (AWS Data Exchange) | 3% | [A24] |
| Professional services | 0.5% private offers (June 16, 2026); 0% in qualifying multi-product sets (September 1, 2026); variable payments (milestone, time and materials, contract caps) | [A28][A29][A76] |
| Multi-product solutions | Solution listings plus offer sets (group of private offers transacted together); private offer only | [A60] |
| Free trials | SaaS free trial 7 to 90 days; one per product per AWS account; token `x-amzn-marketplace-offer-type=free-trial` in registration redirect | [A57] |
| Pricing permanence | Pricing model selection is permanent once published (VENDOR) | [A25] |
| Concurrent Agreements | Multiple active agreements for the same SaaS or professional services product in one account (February 26, 2026); required for new SaaS products from June 1, 2026 | [A101] |

### Fees (effective since 2024-01-05 unless noted)

| Offer | Fee | Source |
|---|---|---|
| Public SaaS | 3% | [A24] |
| Public server (AMI, container, ML) | 20% | [A24] |
| AWS Data Exchange | 3% | [A24] |
| Private offer, TCV under $1M | 3% | [A24] |
| Private offer, $1M to under $10M | 2% | [A24] |
| Private offer, $10M or more | 1.5% | [A24] |
| All renewals | 1.5% | [A24] |
| CPPO uplift | +0.5%, charged to ISV, on the discounted (wholesale) price | [A24][A53] |
| Professional services private offer | 0.5% from 2026-06-16 (was 2.5%); existing offers keep original terms | [A28] |
| Professional services in qualifying multi-product set | 0% from 2026-09-01 (needs a paid non-services product and an active sibling agreement) | [A29][A24] |
| South Korea buyer | +1% from 2025-04-01 | [A24] |
| Worked example | $250,000 SaaS private offer: $7,500 fee; same as server product: $50,000. One $2M contract at 2% ($40,000) vs four $500K at 3% ($60,000) (VENDOR) | [A26] |

### Private offers

- Created in Partner Central > Private offers (Sell menu, redirects into AMMP flows); choose offer type, product type and product (cannot change later) [A52].
- Statuses: Draft, Active, Expired; accepted offers appear under Agreements [A52].
- Extend to the buyer's linked or management account; if the buyer uses a private marketplace, include the private marketplace admin account [A52]. Management-account offers are visible to all member accounts (OFFICIAL blog 2023) [A111].
- Geo-targeting by country; India sellers India-only [A52].
- Up to five custom EULA documents; BYOL not supported; installment plans; future-dated agreements; upgrades and renewals on SaaS contracts [A52].
- Net payment terms: Customer default, Net 15, 30, 45, 60, 90, 120; set before acceptance; invoice buyers only; AWS pays you after it collects [A55].
- Express private offers: rate cards for SaaS contract products auto-generate offers for standard deals; custom requests route to your team [A54]. AWS says more than 80% of Marketplace transactions are already self-service (VENDOR quoting AWS) [A93].
- Request buttons: ACE-eligible partners can add "Request private offer" and "Request demo" buttons; from September 9, 2026 these arrive as instantly qualified leads in Partner Central [A52][A96].
- Link each private offer to its ACE opportunity (1 private offer per opportunity via API) [A48][A47].

### Channel: CPPO and selling authorizations

| Step or rule | Detail | Source |
|---|---|---|
| Channel partner prerequisites | Paid seller registration; service-linked role; tax interview location matches business location; USD disbursement method | [A53] |
| ISV action | AMMP > Selling authorizations > Create; enter reseller's 12-digit AWS account ID; product; renewal flag; optional buyer account IDs; pricing model (contract with installments, contract upfront, usage); currency; duration; dimensions | [A53] |
| Discount types | Recurring (ongoing wholesale discount) or non-recurring (one buyer) | [A53] |
| Supported products | AMI, container, SaaS, professional services | [A53] |
| Money flow | Buyer pays AWS; AWS disburses to partner and ISV; ISV listing fee based on wholesale price plus 0.5% CPPO uplift | [A53][A24] |
| Currency | CPPO must use the currency set in the authorization | [A53] |
| Payment terms | ISV sets the maximum net terms the reseller may extend | [A55] |
| Market data | 27% of marketplace transactions involved channel partners, expected 37% next 12 months (VENDOR survey) | [A91] |
| Storefront | Resellers can run branded multi-vendor catalogs (GA 2026-06-16) | [A99] |
| Channel ROI claim | Forrester: 234% ROI, 50% faster deal closure, 4 to 5x richer deal sizes for channel partners using Marketplace (cited by AWS) | [A5] |

### Committed spend (PPA / EDP) drawdown

| Rule | Detail | Label / source |
|---|---|---|
| Official buyer guidance | Suger notes this FAQ is the only AWS doc naming the drawdown rule (VENDOR) [A35]. Committed spend can be used if products are eligible; "products deployed on AWS typically qualify"; eligibility determined per product | OFFICIAL [A60] |
| May 1, 2025 change | Only SaaS "hosted entirely on AWS" qualifies for commitment retirement; previously a portion hosted in a customer AWS account sufficed | INDEPENDENT [A38], VENDOR [A39] |
| Deployed on AWS badge | Introduced for eligible listings; sellers submit updated architecture diagrams in AMMP | [A38][A39] |
| Migration-tool exception | Clients/gateways may run outside AWS if app and control planes are on AWS and AWS is the only target | [A38] |
| History | 50% of Marketplace spend counted before 2022; 2022 to April 2025, 100% of eligible spend counted, capped at 25% of commitment | VENDOR [A39] |
| Professional services | Reported as not counting toward commitments | INDEPENDENT [A38] |
| Buyer motivation | 74% of surveyed sellers cite access to committed spend as a significant benefit | VENDOR [A91] |

### Payments and disbursement

- AWS bills, collects, then disburses; funds only after collection [A56].
- Daily (when positive balance) or monthly (day 1 to 28); arrives 1 to 2 business days after disbursement; dashboard updates 3 to 5 days after [A56].
- Currencies: USD, EUR, GBP, AUD, JPY, INR (India only); ACH is USD only, SWIFT for others [A56].
- Partial disbursements for partially paid invoices since May 2025; collection visibility reporting January 2026 (VENDOR) [A25].
- Tax management portal for sellers (May 7, 2026): view and download invoices, `ListInvoiceSummaries` API [A117]. Localized billing for professional services from AWS EMEA with SEPA direct debit (February 3, 2026) [A119].

### Listing optimization, reviews, analytics

| Lever | Detail | Source |
|---|---|---|
| AI-assisted product listing | Partner Assistant generates listing content from URL or docs, scores listing strength, gives field-level recommendations including SEO and GEO; announced June 2026 | [A64] |
| Listing score reality check | A listing moved from Basic to top-tier score with no measurable lift in trials or demand (CREATOR) | [A120] |
| Reviews | Verified reviews collected via PeerSpot; external G2 and PeerSpot reviews shown separately; email invite 30 days after purchase; data and professional services products do not support reviews | [A63] |
| Vendor Insights | Security and compliance dashboard for SaaS from self-assessment, CAIQ, ISO 27001 reports and live AWS Audit Manager / Config evidence | [A59] |
| Buy with AWS | CTAs on your own site: Buy with AWS, View offers on AWS, Try free with AWS, Request private offer, Request demo; supports SaaS subscriptions, contracts, contracts with consumption, free trials | [A61] |
| Agent mode (buyer side) | Search, Comparison and Evaluation agents; buyers can request demo or private offer from the flow | [A62] |
| Marketing | 180-day GTM Academy in Marketplace Resources; AWS reviews announcements (up to 10 business days); press release guidelines | [A64] |
| Dashboards | Search performance, listing performance, customer agreements, Buy with AWS dashboards; Marketplace insights menu for agreements, usage, billed revenue, disbursements, tax | [A45][A64] |
| Agreements API | Programmatic procurement and agreement management for buyers, usable by partners for custom storefronts (May 6, 2026, us-east-1) | [A118] |

### Marketplace incentives

| Incentive | Detail | Source / label |
|---|---|---|
| List and Sell Incentive | Offsets cost of first listing, new country expansion, or PLG/Buy with AWS; work through an approved integrator found in Partner Central; amounts not on public page | OFFICIAL [A30][A5]; $10,000 credits per VENDOR [A25] |
| MPOPP | AWS promotional credits to customers buying ISV private offers, based on TCV and program rates; new sellers and renewals; request in Partner Funding Portal; credits next business day after acceptance; fully automated approval | OFFICIAL [A31][A7] |
| Seller Prime | PLG guidance, $10K new-listing credit, up to $40K MDF for ISV-led campaigns; submit Seller Prime Strategy Document to PDM | VENDOR (2025-01) [A86][A85]; UNVERIFIED on AWS pages |
| ACE-CRM integration credits | $10,000 (VENDOR) | [A25] |
| Automation Incentive | Supports system integration and agentic workflows | OFFICIAL, amount unpublished [A5] |

### What makes a listing produce pipeline

1. Treat the listing as a procurement accelerator and co-sell attachment point, not a lead engine. CREATOR voices consistently say AWS amplifies existing demand [A106][A107]; one ISV attributes only about $1.5M of $10M Marketplace billings to genuinely incremental revenue (CREATOR) [A88].
2. Be "Deployed on AWS" so customers can burn commits [A38][A60].
3. Enable request buttons and work the instant leads in Sell > Leads [A96].
4. Put Buy with AWS CTAs and Storefront on your own site [A61][A99].
5. Enable PRM and link offers and opportunities so AWS sees your consumption impact [A13][A95].
6. Use private offers linked to ACE opportunities for the SaaS Co-Sell Benefit [A37][A79].
7. Collect verified reviews via PeerSpot and connect Vendor Insights for security reviews [A63][A59].

## 6. Co-sell

### Eligibility ladder

| Level | What you can do | Gate | Source |
|---|---|---|---|
| Registered, ACE T&C accepted | Create and share partner-originated opportunities (Co-Sell or For Visibility Only) | Registration | [A44][A42] |
| Solution in Limited or Public status | Required to create any opportunity | Build > Solutions | [A43] |
| ACE eligible | Receive AWS opportunity referrals and leads; Partner Lead Prospecting | ACE FAQ criteria (login-gated) | [A43][A97][A108] |
| ISV Accelerate | Seller incentives (SCB), AM solution libraries, ISVA MDF, workshops | Section 4 thresholds | [A1][A6] |
| Competency / Differentiated | Higher recommendation weight, badges in Marketplace search, PGP, BOX | Specialization | [A71][A69] |

### How to register and share an opportunity (console)

1. Sell > Opportunities > **Create opportunity** > Create using wizard or **Create using agent** (describe the deal or upload notes, proposal or transcript in PDF, DOCX, XLSX, TXT; agent extracts, enriches, you approve; status returns Pending Approval) [A43].
2. **Customer details**: all fields required except DUNS; website and postal code drive routing; Government vertical requires Classified National Security Information selection [A43].
3. **Project details**: specific customer business problem (not generic); accurate Use Case and Industry (not Other); select **Co-Sell with AWS** and one or more "Partner specific needs from AWS"; Opportunity Type (Net New, Expansion, Flat Renewal with optional parent ID); future Target Close Date (never submit Launched or Closed Won); associate at least one solution or Marketplace product; if sourced from marketing, answer the MDF question [A43].
4. **APN program**: select program (for example MAP, then workload, source, phase Assess/Mobilize/Migrate and Modernize/Manage, managed services Y/N, details) [A43].
5. **Deal sizing**: MRR estimate via AWS Pricing Calculator URL import or "Forecast MRR from TCV" (enter TCV and months); AI recommends AWS products and flags MAP eligibility [A43].
6. Submit. Record becomes read-only while Submitted and In review. Validation checks deal size, solution alignment and customer engagement status; the CRM guide states validation can take up to five business days [A43][A47].
7. If **Action Required**: Filter Action required > open > review Quality Score and AWS recommended actions > Edit > Save > Submit [A43].
8. If **Approved**: it enters the AWS seller's pipeline; you get a motion assignment and score. Add next steps (255 characters, action + deliverable + owner + date) at every stage change; next steps feed the score [A43][A3].
9. At close: move to **Launched** (attach customer AWS account ID; for Marketplace deals attach the offer) or **Closed Lost** (reason required) [A43][A47]. Committed or Launched requires an associated solution or Marketplace product [A95].

### What the field sees and does not see

- AWS referrals: before acceptance you see company, website, country, postal code, industry, opportunity fields, and AWS contacts (Sales Rep, Account Owner, PSM/ISV Success Manager, PDM/PDR, WWPS PDM); customer contacts are masked until you accept [A43][A47].
- AWS-side stage: when the AWS seller moves a deal to a terminal stage in AWS's CRM, you see AWS Stage, AWS Close Date, AWS Closed/Lost Reason in Additional Details [A43].
- Opportunities in terminal stages show no Quality Score or motion [A43].
- AWS Next Step field is visible read-only in the Salesforce connector since v3.19 (June 23, 2026) [A47].
- Visibility "Limited" restricts what AWS sales sees (API) [A42].

### Opportunity Quality Score and motions

| Item | Detail | Source |
|---|---|---|
| Range and display | 0 to 100, "[score] / 100", with up/down/flat trend, recalculated continuously | [A3] |
| Motions | AWS Field-engaged (matched with an AWS sales team; agent supports research and record upkeep); Agent-engaged (agent qualifies and enriches with you); Partner-led (you drive with agent sales plays and resources) | [A3][A75] |
| Official caveat | Higher score may increase likelihood of seller engagement; no guarantee | [A3] |
| Eight hygiene fields | Title (customer, workload, delivery model); customer business problem (why now, outcome); stage (move promptly to Launched or Closed Lost); next steps (action, owner, date); MRR from Pricing Calculator; industry and use case (not Other); AWS services the customer is adopting (not ones your product runs on); partner solution tag | [A3] |
| Practitioner data | Scores rarely above 40; very poor records around 5 route to an agent; resubmitting with more customer and AWS-revenue context rescored higher (CREATOR) | [A87] |
| Practitioner data | A five-part write-up (opportunity overview, customer outcomes, evaluation criteria, AWS asks, budget authority) lifted typical scores from 15 to 25 into 55 to 65; an 85 still routed Partner-led (CREATOR) | [A88] |
| Launch | Agents that qualify every opportunity in real time and the score announced June 16, 2026 | [A75][A121] |

### Referral flows

| Direction | Mechanism | SLA | Source |
|---|---|---|---|
| AWS to partner (opportunity) | AWS seller attaches partner in AWS CRM; you get an Engagement Invitation (Opportunity Invitations tab) | Accept or reject within 5 business days; reject requires reason and loses access | [A43][A40] |
| AWS to partner (lead) | Lead invitations tab; accept to see contacts; enrich and convert to opportunity | 5 business days | [A43] |
| Marketplace to partner | Demo and private offer requests arrive as qualified leads instantly (from 2026-09-09) | Immediate | [A96] |
| Partner to AWS | Partner-originated opportunity, Co-Sell or For Visibility Only | Validation up to 5 business days | [A42][A47] |
| Partner to AWS (leads) | AWS "doesn't support the Partner Shares Lead with AWS scenario"; qualify first, then submit as opportunity | n/a | [A47] |
| Partner to partner | Partner discovery and connections; multi-partner opportunities (December 2024) | n/a | [A45][A43] |
| Sync latency (CRM) | Each update can take up to one hour to sync (S3-era guidance) | n/a | [A47] |

### CRM integration and APIs

| Option | Detail | Source |
|---|---|---|
| AWS Partner CRM Connector (Salesforce only) | Launched with Marketplace support in November 2023 [A22]; free AppExchange managed package; two-way ACE sync, private offers, agreements, resale authorizations; latest v3.20 (July 17, 2026) | [A47] |
| Third-party (Tackle, Labra, Suger, Clazar, WorkSpan and others) | Supports other CRMs (HubSpot, Dynamics, Zoho); subscription cost; example: Tackle's Salesforce agent surfaces ACE insights and MAP/POC/MPOPP/WMP eligibility (March 2026) | [A47][A2][A105] |
| Custom | Partner Central APIs; 3 to 12 weeks to build, 2 to 3 weeks per quarter to maintain; no lead management | [A47] |
| Selling API endpoint | `partnercentral-selling.us-east-1.api.aws`; catalogs `AWS` and `Sandbox` | [A40] |
| Key actions | CreateOpportunity, UpdateOpportunity (must pass LastModifiedDate; optimistic locking), SubmitOpportunity (InvolvementType, Visibility), StartEngagementByAcceptingInvitationTask, RejectEngagementInvitation, AssociateOpportunity, GetAwsOpportunitySummary, ListSolutions, prospecting tasks | [A40][A42] |
| Events (EventBridge) | Opportunity Created, Opportunity Updated, Engagement Invitation Created/Accepted/Rejected | [A40] |
| Quotas | Reads 10/s and 100,000 per 24h; writes 1/s and 10,000 per 24h; CreateEngagement 15/s; per opportunity: 20 AWS products, 10 partner solutions, 10 Marketplace solutions, 10 Marketplace products, 1 private offer | [A48] |
| Other APIs | Account API (registration, profile, connections), Benefits API (benefit applications and allocations), Channel API, Revenue Measurement API (RA IDs) | [A48] |
| MCP server | Tools `sendMessage` and `getSession`; human approval required for writes; max 3 files per message (documents 4.5 MB, images 3.75 MB); SigV4 or OAuth (August 2026, us-east-1) | [A48][A100] |
| S3 to API upgrade | S3 deprecated and closed to new users; account linking is the only hard prerequisite; delete old scheduled jobs; deactivate legacy validation rules; backfill Last Modified Date; buttons change to "Share with AWS" | [A47][A9] |
| Known connector issue | Validation rules ACEOppNew_PreventUpdatesWhenPOSubmitted, ACEOpp_PreventUpdatesWhenPOSubmitted, ACEOppNew_MandatorySolutionOffered stay active after upgrades from 3.14 to 3.17; deactivate manually | [A47] |

### The seller engagement playbook that works

1. **Qualify before you submit.** Submit early (qualification or discovery) but with a specific business problem, dated next step and Pricing Calculator MRR [A43][A36]. Partner Insight recommends clear stage, deal size, timeline and 2 to 3 explicit asks (CREATOR) [A104].
2. **Name the AWS angle.** List the AWS services the customer adopts and quantify AWS consumption impact; AWS field teams prioritize ISVs that increase compute, storage or keep workloads on AWS (CREATOR) [A3][A106].
3. **Transact through a linked private offer** so the AM gets SCB credit and the customer burns commit [A37][A60].
4. **Do not wait for the agent to hand you a rep.** Find the AM from the referral contacts or via your PDM and run account mapping; Althoff's ratios: one formal enablement session per 20 co-sell engagements and one account mapping session per 10 (OFFICIAL blog, 2023) [A32].
5. **Educate, Enable, Engage** framework for your own sellers (OFFICIAL blog, 2023) [A33].
6. **Work the new lead sources**: Sell > Leads, Partner Lead Prospecting plays, Marketplace request leads [A97][A96].
7. **Close the loop**: update stage to Launched with the AWS account ID; launched opportunities count for ISVA, tiers and specialization renewals [A1][A17][A34].
8. **Negotiate SCA and PPA context together** when you are a large AWS consumer (CREATOR) [A89].

## 7. Incentives, funding and benefits (current published amounts)

Where the guide lives: the AWS Partner Funding Benefits Guide, MDF Guide and program guides are login-gated in Partner Central. Public pages rarely publish amounts. Everything below states what is public.

### How to request any fund (console)

Funding Benefits > Funding dashboard > **Create fund request** > pick program template [A46]. Or from an opportunity: Funding Recommendation widget > Get estimated funding / **Create fund request** (agent drafts, you submit in the Funding portal) [A46]. Funding agents covered four programs from March 2026 and all funding programs from July 20, 2026, including SCA funding and AWS Growth Initiative (AGI) funding [A122].

| Fund request stage | Meaning | Source |
|---|---|---|
| Created | Draft or rejected back to partner | [A46] |
| AWS Review | Sell (POC) and Miscellaneous (Jumpstart, ISV WMP) only | [A46] |
| Tech Approval | PSA checks SOW feasibility (POC) | [A46] |
| Business Approval | Program business approver | [A46] |
| Finance Approval | PO for cash, codes for credits | [A46] |
| Pre-Approval | Execute; credits stay here until redeemed (MAP skips this stage) | [A46] |
| Cash Claim | Submit actuals after completion; then invoice via Payee Central | [A46] |
| Completed | Done | [A46] |
| Expiry | Status Expired 30 days after delivery end date | [A46] |
| Attachments | Files with disallowed formulas get Quarantined; convert to PDF | [A46] |

### Program table

| Program | Who | Amount (public) | Claim | Source |
|---|---|---|---|---|
| MDF | Partners with Payee Central; eligibility tied to designations and tiers | Not published generally; ISVA MDF for new ISVA enrollees after 2026-01-01 with PRM; +$25K for agentic AI category; $25K for SMB Competency; up to $50K for Amazon Connect implementations (from January 2026); up to $50K industry MDF in BOX; $50K per year for BVR Competency (INDEPENDENT) | Funding Portal, reimbursement against proof of execution | [A65][A6][A73][A71][A7][A72][A114] |
| POC funding | Partners running customer proofs of concept | Not published; stages include PSA tech approval | Fund request (Sell motion) | [A46][A114] |
| MAP | Services partners (and ISVs with migration use cases) | Not published on AWS page; vendor figures: Assess about 5% of projected ARR, Mobilize about 20%, Migrate 15% to 25% of ARR in credits; MAP Lite minimum $100K ARR; max $2M; workloads must be tagged before migration (VENDOR, updated 2026-05) | Fund request with MAP template; opportunity must carry MAP program details | [A66][A113][A43] |
| ISV Workload Migration Program | SaaS on AWS with FTR and migration use case | Customer promotional credits; amounts in login-gated guide | Apply, then fund request (Miscellaneous) | [A68][A46] |
| MPOPP | ISVs selling via Marketplace private offers | Customer credits based on TCV and program rates; next business day after acceptance | Self-service in Funding Portal, year-round | [A31][A7] |
| List and Sell Incentive | First listing, new country, PLG | Offsets integrator cost; $10K credits (VENDOR) | Pick integrator in Partner Central | [A30][A25] |
| APN Innovation Sandbox Credits | APN members building solutions | Not published | Via Partner Development contact | [A65] |
| Training discounts and credits | APN members | Not published | Training and Certification Funding | [A65] |
| BVR | Advanced/Premier services partners with domain competency | Amount scales with opportunity size; auto-disbursed per pit stop | Nominate customer, define KPIs, complete pit stops | [A98] |
| BOX | Validated/Differentiated; now business consulting and advisory partners too | Cash and credits; up to $50K industry MDF | Apply | [A23][A7][A74] |
| Partner Greenfield Program | Differentiated with competency mix or ISVA | Practice funding, GTM funding, performance incentives (amounts unpublished) | Application form | [A69] |
| SCA | Strategic partners | Negotiated; budget allocation visible in funding widget; managed in Contract Central | PDM leadership | [A46][A71] |
| AWS Activate | Startups pre-Series B, founded within 10 years, paid account | Founders up to $5,000 (starts $1,000); Portfolio up to $200,000 with provider Org ID; AI startups $200,000+ (invite) | Apply; decision in 5 to 10 business days | [A67] |
| Generative AI Accelerator | Gen AI and agentic startups | Up to $1M credits; 2025 cohort applications June 10 to July 10, 2025, kickoff October 13 to 17, closing at re:Invent December 1 to 4, 2025 | Application | [A70] |
| Global Startup Program | Startups in APN | Free Kiro access, early Nova access, enhanced MDF wallets | Program | [A7] |
| MSP incentives | MSPs | Three new benefits effective January 1, 2026 | Program | [A7][A92] |
| Reseller incentives | Solution Provider / Distribution | New Customer Incentives replaced Partner Originated discount (re:Invent 2025); Partner Growth Discounts; CEI Grow; Public Sector Discounts | Channel analytics | [A92][A45] |
| AI investment context | All | $115M+ invested in partner AI since March 2024 | n/a | [A7] |

### Benefit-to-requirement map for an ISV

| Benefit | Requires |
|---|---|
| FTR | Marketplace product, deployed on AWS, PRM enabled [A49] |
| ISV WMP | FTR [A68] |
| ISVA | FTR (Validated), GA listing, ACE eligibility, 5 launched, 15 qualified, Payee Central, $2K revenue, training [A1] |
| ISVA MDF | Enrolled after 2026-01-01, PRM, co-sell engagement criteria [A6] |
| SCB (seller quota retirement) | ISVA plus Marketplace private offers [A79][A37] |
| MPOPP | Marketplace private offer [A31] |
| PGP (software) | ISVA plus Differentiated [A69] |

## 8. What changed in 2025 to 2026 and what is announced next

Newest first.

| Date | Change | Source |
|---|---|---|
| 2026-09-22 | APN blog "Grow your services business through AWS Marketplace": 0.5% services fee, 0% in multi-product solutions, variable payments, branded storefronts, agent mode | [A76] |
| 2026-09-09 | Marketplace demo and private offer requests delivered as instantly qualified leads | [A96] |
| 2026-09-01 | 0% listing fee for professional services in qualifying multi-product solutions | [A29] |
| 2026-08-20 | Partner Central agents MCP server supports OAuth with AWS Sign-In (us-east-1) | [A100] |
| 2026-07-20 | Partner Central funding agents expanded to all funding programs incl. SCA and AWS Growth Initiative (AGI) | [A122] |
| 2026-07-17 | CRM connector v3.20 | [A47] |
| 2026-07-10 | 2026 AWS Partner Award nominations announced | [A74] |
| 2026-07-09 | Partner Lead Prospecting (sales plays, call scripts, emails) for ACE-eligible partners | [A97] |
| 2026-07-01 | Marketplace listings attachable to co-sell opportunities (10 solutions and 10 products); association required for Committed or Launched | [A95] |
| 2026-06-30 | Partner Revenue Attribution ID feature and managed policies | [A43][A50] |
| 2026-06-30 | Forward Deployed Engineering for Partners introduced | [A74] |
| 2026-06-29 | Reported: BVR Competency with $50K MDF per year (2026 to 2027); agentic services package for MSPs (INDEPENDENT) | [A72] |
| 2026-06-23 | CRM connector v3.19 adds read-only AWS Next Step | [A47] |
| 2026-06-16 | Partner Central agents qualify every co-sell opportunity; Opportunity Quality Score; three co-sell motions; lead enrichment; ACE Resonate sales guide update | [A121][A75][A43] |
| 2026-06-16 | "Registered to ready-to-sell" agentic onboarding: profile auto-fill, listing generation, streamlined FTR (SOC 2 or WAFR in minutes), PRM guidance | [A5] |
| 2026-06-16 | BVR funding motion launched | [A98] |
| 2026-06-16 | Marketplace Storefront GA; AI-assisted product listing; professional services fee cut from 2.5% to 0.5% | [A99][A64][A28] |
| 2026-06-01 | Concurrent Agreements required for new SaaS products | [A101] |
| 2026-05-07 | Marketplace Tax management portal | [A117] |
| 2026-05-06 | Marketplace Agreements API | [A118] |
| 2026-04-21 | Attributed Revenue dashboard (Partner analytics) | [A77] |
| 2026-04-03 | PRM supports Marketplace metering for AMI and ML (EC2, SageMaker) | [A14] |
| 2026-03-31 | CRM connector v3.17: EUR for European Sovereign Cloud, S3-to-API backfill mode | [A47] |
| 2026-03-19 | BOX expanded to business consulting and advisory partners | [A74] |
| 2026-03-16 | Partner Central agents launched (pipeline insights, opportunity creation, funding recommendations, MCP) | [A15][A78] |
| 2026-03-16 | New ISVA benefits: MDF (new enrollees after 2026-01-01 with PRM), workshops, agents | [A6] |
| 2026-02-26 | Concurrent Agreements for SaaS and professional services | [A101] |
| 2026-02-11 | PartnerCentralIncentiveBenefitManagement policy; Amazon Q permissions | [A4] |
| 2026-02-03 | Localized EMEA billing for professional services | [A119] |
| 2026-01-30 | Partner Revenue Measurement GA; MAP opportunity data enrichments | [A12][A43] |
| 2026-01-29 | Skill Builder login method change for all companies (VENDOR) | [A10] |
| 2026-01-12 | Specialization program 2025 recap: validation agent, category badges, badges in Marketplace search, co-sell recommendation score dashboard | [A71] |
| 2026-01-01 | MSP incentives effective; Amazon Connect MDF program starts | [A92][A7] |
| 2025-12-11 | Tagging AWS partition (European Sovereign Cloud) on opportunities | [A43] |
| 2025-12-08 | Deal sizing on opportunity creation | [A43] |
| 2025-12 | New solution management using Marketplace solution workflow after migration | [A49] |
| 2025-12-01 | re:Invent 2025 partner announcements: $7.13 services multiplier (Partner1 recap [A103]), agentic AI categories, PGP, Small Business Acceleration global, Billing Transfer, MPOPP next-day credits, Marketing Central agents planned for 2026 | [A7][A92] |
| 2025-11-30 | Partner Central in the AWS Console; migration tool; agentic AI competency categories | [A11][A73] |
| 2025-11-19 | Channel Management (Billing Transfer) docs and policies | [A4] |
| 2025-11-15 | APN fee billing only for accounts with linked, paid AWS accounts at renewal | [A112] |
| 2025-11 | Express private offers | [A54][A93] |
| 2025-08-12 | MPOPP launched in Funding Portal | [A31] |
| 2025-07 | AI agents and tools category in Marketplace | [A27] |
| 2025-05-01 | "Deployed on AWS" rule for SaaS commit retirement | [A38][A39] |
| 2025-04-01 | South Korea +1% regional fee | [A24] |
| 2025-01 | SaaS Co-Sell Benefit extended to all ISVA partners; Small Business Acceleration Initiative | [A79][A37][A80][A81] |

### Announced or expected next

| Item | Date | Source |
|---|---|---|
| Service Delivery and Service Ready deprecation | 2027-06-01 (new applications already closed) | [A20] |
| Validation agent expansion beyond AI Competency | Throughout 2026 | [A71] |
| Marketing Central with AI agents | Planned for 2026 | [A7] |
| Lead propensity messaging (sales plays, scripts, templates) | Partly delivered July 2026 | [A75][A97] |
| S3 CRM backend end-of-life | AWS docs: not published, "as soon as possible" [A47]. WorkSpan customer notice (VENDOR): S3 sync ends 2026-09-30, bucket access revoked 2026-10-30, decommissioning from 2026-12-31 (see vendors/workspan-intelligence.md). Treat as urgent: move any S3 integration to the API now. | [A47] |
| re:Invent 2026 | November 30 to December 4, 2026: expect 2027 program changes | [A94] |

## 9. Diagnostics: why partners get zero pipeline, and the fix

| # | Failure mode | How to detect (where to look) | Fix | Source |
|---|---|---|---|---|
| 1 | Still on legacy Partner Central | Console dashboard shows "Not Registered"; no agents; "domain in use" on registration | Link account, map IAM, migrate in a quiet window | [A44][A8] |
| 2 | Wrong or unlinked AWS account | Partner Central settings; APN fee not billing; agents missing | Pick a paid, company-owned member account before migration; unlink/relink only pre-migration | [A112] |
| 3 | No solution or solution not Limited/Public | Build > Solutions status; cannot create opportunities | Create solution, link Marketplace product, publish to PSF | [A43][A49] |
| 4 | Stuck at Registered (no FTR) | Partner Scorecard; Solutions > Validation checklist shows blocked prerequisite | Fix prerequisites in order (Marketplace link, one product, software type, architecture diagram, PRM) then submit SOC 2 or WAFR | [A49] |
| 5 | PRM not implemented | Partner analytics > Attributed Revenue > Onboarding Status empty | Tag resources `aws-apn-id=pc:<code>` or add UA string; for AMI/ML it is automatic | [A13][A77] |
| 6 | Opportunities submitted "For Visibility Only" | Opportunity detail, involvement type | Resubmit as Co-Sell with explicit partner needs from AWS | [A42][A43] |
| 7 | Generic business problem, Other industry, guessed MRR | Low Quality Score; Action Required; Agent-engaged or Partner-led motion | Rewrite with customer-specific pain, why now, outcome; Pricing Calculator MRR; real AWS services | [A3][A87][A88] |
| 8 | Stale records | Next steps older than a stage; close dates in past; pipeline insights flags stalled deals | Weekly hygiene: dated next step with owner; close Launched/Closed Lost promptly | [A43] |
| 9 | Missed AWS referrals | Opportunity Invitations and Lead invitations tabs; items expire after 5 business days | Assign an owner to check daily; auto-accept via API/CRM with events | [A43][A40] |
| 10 | Deals not launched in ACE | Launched count below 5 in 12 months; tiers stall | Close out wins as Launched with AWS account ID and linked offer | [A1][A17][A47] |
| 11 | Selling direct, not via private offers | Marketplace insights > Agreements shows no private offers | Route ISVA deals through private offers linked to ACE for SCB | [A37][A79] |
| 12 | Product not "Deployed on AWS" | Listing lacks badge; customers say it does not burn commit | Submit architecture diagram; move hosting fully to AWS if feasible | [A38][A39] |
| 13 | Not in ISVA | Program applications; check 15 qualified / 5 launched / $2K | Build pipeline volume through qualified submissions, then apply | [A1] |
| 14 | Private offers not linked to opportunities | Opportunity has no associated offer; Revenue Attribution missing | Associate offer (1 per opportunity) and RA ID | [A48][A50] |
| 15 | CRM integration on S3 | Connector buttons still "Send to AWS"; duplicate opportunities | Upgrade to API; delete old APN jobs; deactivate legacy validation rules | [A47][A9] |
| 16 | Subsidiary seller accounts disconnected | Attributed revenue missing a product | Account connections Level 1 | [A112] |
| 17 | Expecting Marketplace to generate demand | Listing views without trials or requests | Use listing as procurement rail plus request buttons, Buy with AWS, and your own demand gen | [A88][A106][A96] |
| 18 | No relationship with PDM or AMs | No named AWS contacts on your opportunities; 46% of vendors call PDM access extremely challenging (VENDOR) | Business plan with PDM; target AMs from referral contacts; attend workshops | [A91][A6] |
| 19 | Funding never requested | Funding dashboard empty; Investments analytics shows no claims | Use Funding Recommendation widget on each opportunity | [A46] |
| 20 | Services partner without launched MRR | Tier requirements unmet (3 launched, $1,500 MRR for Select) | Log every AWS-consuming project as an ACE opportunity with AWS account ID | [A17] |

## 10. KPIs and operating cadence

### What to measure

| KPI | Definition | Target or benchmark | Source |
|---|---|---|---|
| Qualified ACE opportunities (trailing 12 months) | Opportunities in Qualified or later | At least 15 for ISVA | [A1] |
| Launched opportunities (T12M) | ACE Launched or accepted private offers | At least 5 for ISVA; 3/20/50 for Services tiers | [A1][A17] |
| Average Opportunity Quality Score | Mean score on open opportunities | Not published; practitioners see most under 40 (CREATOR) | [A87] |
| Motion mix | Share of opportunities Field-engaged vs Agent-engaged vs Partner-led | Track trend; not benchmarked | [A3] |
| Referral acceptance time | Hours from invitation to accept | Under 5 business days mandatory | [A43] |
| Validation cycle time | Submit to Approved | Up to 5 business days | [A47] |
| Market size context | Cloud marketplace GMV across AWS, Azure, GCP estimated above $45B a year, AWS largest by volume (VENDOR) | [A116] |
| Marketplace billed revenue / TCV | Agreements and billed revenue dashboards | Vendor survey: 41% of companies get under 5% of revenue from marketplaces; 22% get over 20% (VENDOR) | [A90] |
| Incremental vs rerouted Marketplace revenue | Deals that would not have closed without Marketplace | One ISV: about $1.5M of $10M (CREATOR) | [A88] |
| Attributed AWS revenue (PRM) | Partner analytics > Attributed Revenue | Monthly, 17 days after month end | [A77] |
| Co-sell win rate vs direct | Win rate of ACE-linked vs non-ACE deals | 59% report higher win rates (VENDOR); Canalys 2024: 65% higher close rates, 54% larger deals, 51% higher revenue growth (cited by AWS) | [A90][A75][A1] |
| Funding claimed vs available | Investments analytics | Track claim rate | [A45] |
| Private offer attach rate | Share of ACE Launched with linked offer | Internal | [A47] |

### Cadence

| Cadence | Activities |
|---|---|
| Daily | Check Opportunity Invitations and Lead invitations; work Marketplace request leads [A43][A96] |
| Weekly | Update next steps and stages on every open opportunity; review pipeline insights ("Ask about sales pipeline"); fix Action Required [A43]; internal co-sell stand-up |
| Monthly | Program health check (runbook 13.10); Attributed Revenue review [A77]; funding claims; Marketplace agreements and renewals; refresh this file |
| Quarterly | Business review with PDM (YTD goals, must-win deals, enablement) [A32]; recompute ISVA and tier thresholds; FTR expiry watch; account mapping sessions |
| Annually | OP1 input to AWS in August to October; SCA/PPA negotiation; APN fee renewal; re:Invent planning (Nov 30 to Dec 4, 2026) [A82][A94] |

## 11. By partner type

| Partner type | Path | First five moves | Watch-outs |
|---|---|---|---|
| B2B SaaS ISV (Series B to public) | Software Path | 1) Register or migrate and link account; 2) List SaaS contract product on Marketplace with Concurrent Agreements support; 3) Get "Deployed on AWS" and enable PRM; 4) FTR via SOC 2 Type II; 5) Build to 15 qualified / 5 launched and apply to ISVA [A1][A49][A101] | Pricing model is permanent (VENDOR) [A25]; do not rely on listing for demand [A88]; transact via linked private offers for SCB [A37] |
| ISV not hosted on AWS | Software Path | Decide whether to move hosting; without it, no commit burn-down and no FTR path (FTR requires AWS-hosted architecture) [A38][A49] | Marketplace still usable for procurement, but AWS sellers have little reason to engage |
| Services, SI, consultancy | Services Path | 1) Certifications and accreditations for Select (4 accredited, 2 foundational, 2 technical); 2) log 3 launched opportunities with $1,500 MRR; 3) Competency in a domain; 4) MAP, POC, BVR funding; 5) list professional services on Marketplace at 0.5% (0% in bundles) [A17][A28][A29][A98] | Service Delivery/Service Ready closing [A20]; Premier needs 3 Competencies incl. MSP, DevOps or CloudOps [A17] |
| Agency (marketing, RevOps) | Services Path (often Select) or referral partner to ISVs | Package services as Marketplace professional services in multi-product solutions with ISV partners (0% fee) [A29]; BOX now open to business consulting and advisory partners [A74] | Limited AWS consumption impact means limited seller attention |
| Reseller / MSP | Services Path plus Solution Provider / Distribution | CPPO resale authorizations; Storefront for curated catalogs; Channel Management with Billing Transfer; MSP program incentives from January 2026 [A53][A99][A4][A92] | New Customer Incentives replaced Partner Originated discount [A92]; CPPO uplift 0.5% is borne by the ISV [A24] |
| Startup | Software Path plus Activate / Global Startup Program | Activate credits (up to $200K via provider); Generative AI Accelerator (up to $1M); SCB also applies to eligible startups in ISVA [A67][A70][A79] | Activate eligibility: pre-Series B, founded within 10 years [A67] |

## 12. Strategic decision points (for Alex)

### 12.1 Should we invest in AWS at all this year?

Invest when at least two are true: the product runs entirely on AWS (commit burn-down and FTR path) [A38][A49]; target customers hold AWS PPAs; you can list a SaaS contract product and route enterprise deals through private offers; you can staff an alliance owner plus RevOps for ACE hygiene. Hold or go light when hosting is elsewhere, ACV is under typical private offer sizes, or no one can own weekly ACE upkeep. The call flips when a large customer asks to buy via their AWS commit.

### 12.2 Which tier or stage to chase

| Situation | Chase | Why |
|---|---|---|
| ISV with AWS-hosted product | Validated (FTR) now, ISVA within two quarters | ISVA is the stage where AWS sellers get paid (SCB) [A1][A79] |
| ISV with strong vertical wins | Competency (Differentiated) after ISVA | Badges in Marketplace search, PGP eligibility [A71][A69] |
| Services firm new to AWS | Select tier plus one Competency | ACE eligibility for Select requires a designation (VENDOR) [A108] |
| Services firm with volume | Advanced for BVR funding | BVR requires Advanced or Premier [A98] |
| Anyone on Service Ready/Service Delivery | Replace with Competency before 2027-06-01 | Deprecation [A20] |

### 12.3 Marketplace-first or not

Marketplace-first makes sense when enterprise buyers have AWS commits and procurement friction is the bottleneck: fees are 1.5% to 3% on private offers [A24], commit retirement requires "Deployed on AWS" [A38], and 74% of surveyed sellers name committed-spend access as a major benefit (VENDOR) [A91]. Expect Marketplace to accelerate and multiply, not create, demand (CREATOR) [A88][A106]. The call flips toward direct when the product is not on AWS, deals are small monthly PAYG with credit cards, or the customer's commit is already fully consumed.

### 12.4 When private offers beat direct

Use a private offer when: the customer has an AWS commit; the deal involves an AWS AM you want engaged (SCB credit); you want MPOPP customer credits [A31]; procurement is slow (AWS paper, standardized contract); or a reseller is involved (CPPO). Direct wins when the fee is not offset (rare at 1.5% to 3%) or the buyer refuses AWS billing. Consolidate multi-year deals into one offer above $1M or $10M thresholds to cut the fee (VENDOR worked example) [A26].

### 12.5 How to fund the motion

Stack: FTR (free) [A19]; List and Sell Incentive to offset integrator cost [A30]; MPOPP credits to close deals [A31]; ISV WMP credits for competitive migrations [A68]; ISVA MDF after enrollment with PRM [A6]; POC funds per opportunity [A46]; for services firms MAP, BVR, BOX [A66][A98][A7]. Large partners negotiate an SCA; CREATOR advice is to negotiate PPA and SCA together and expect a consumption give-and-get [A89].

### 12.6 Business case inputs

| Input | Where it comes from |
|---|---|
| Share of target accounts with AWS PPAs | Account mapping with AWS, customer interviews |
| Average deal size and expected fee tier | Marketplace fee table [A24] |
| Expected co-sell win-rate lift | Vendor and analyst studies (label them): 59% report higher win rates (VENDOR) [A90]; 65% higher close rates, 54% larger deals (Canalys 2024, cited by AWS) [A75] |
| Incrementality haircut | Plan conservatively; one ISV saw about 15% incremental (CREATOR) [A88] |
| Headcount | Alliance manager, RevOps/ACE owner, Marketplace ops; integrators or listing platforms |
| Funding offsets | Program table in section 7 |
| Time to value | Registration in a day; FTR in minutes once prerequisites met; ISVA needs 12-month trailing volume [A44][A49][A1] |

### 12.7 Conditions under which the calls flip

- AWS publishes an S3 CRM end-of-life date or a legacy portal cutoff: migration becomes urgent, not optional [A47].
- ISVA thresholds or MDF terms change (check official page monthly) [A1].
- Customer's PPA renewal: best moment to position your product for commit retirement [A89].
- AWS launches a competing native service: CREATOR "graduate" positioning advice (differentiate without partner conflict) [A120].
- re:Invent 2026 program changes (Nov 30 to Dec 4, 2026) [A94].

## 13. Tactical runbooks (for Eva)

Conventions: menu paths use the console Partner Central unless stated. "Done when" is the exit check. Never submit on a customer's behalf without the account owner's approval.

### 13.1 Enroll (new partner)

1. Confirm a paid, company-owned member AWS account exists (not payer, not personal, not developer). Done when IAM admin confirms account ID [A44].
2. IAM admin attaches AWSPartnerCentralFullAccess and AWSMarketplaceSellerFullAccess to the registrant. Done when user can open Partner Central [A44].
3. Console > AWS Partner Central > Get started > identity verification (QR, selfie, ID). Done when Verification Status = Complete [A44].
4. Business verification (legal name, country, tax ID, state). Done when green success bar appears [A44].
5. Registration form: alliance lead (shared alias), primary product/service, verify email, optional tags, accept APN and ACE terms, Submit. Done when dashboard loads [A44].
6. Dashboard Getting Started cards: let the onboarding agent fill profile, set PUBLIC visibility, link training domains, run tax interview. Done when profile approved and visible [A45].
7. Enroll in path(s) (Partner Scorecard). Done when path shows in scorecard [A45].
8. Pay APN fee from linked account. Done when fee shows paid [A112].

### 13.2 Migrate an existing legacy account

1. Alliance Lead exports user list; map each to a managed policy (drop inactive by Last Login Date) [A8].
2. IAM admin creates users/SSO permission sets [A8].
3. Link AWS account (Partner Central settings > account linking). Double-check selection: permanent after migration [A112].
4. If on S3 CRM integration: upgrade to API first or in parallel (runbook 13.12) [A47].
5. Open migration tool, complete checklist and business verification, schedule off-hours window; tell all users they will be locked out 2 to 6 hours [A8][A10].
6. Done when Alliance Lead receives completion email and a test user signs in with IAM and sees opportunities history [A8].

### 13.3 Get co-sell ready and eligible

1. Build > Solutions > create solution; status Limited or Public. Done when solution can be selected on an opportunity [A43][A49].
2. Link the Marketplace product (one per solution for FTR) [A49].
3. Upload AWS-hosted architecture diagram in AMMP; confirm "Deployed on AWS" [A49][A38].
4. Implement PRM (runbook 13.11). Done when product is "onboarded" in Attributed Revenue [A49].
5. Build > Solutions > [solution] > Validation > Request validation > SOC 2 or WAFR PDF (max 3 MB) > Request FTR. Done when status Approved with expiration date [A49].
6. Publish to Partner Solutions Finder [A49].
7. Confirm ACE eligibility (ACE FAQ in Partner Central; vendor summary: 15 validated opportunities for Software) [A108].
8. Track ISVA thresholds monthly; when met, Partner Admin > Program Applications > Create > Select Designation "ISV Accelerate" > agree > complete > Submit. Done when program shows Active [A45][A1].
9. Complete Co-Selling with AWS learning module for at least one person; set up Payee Central [A1].

### 13.4 Publish a Marketplace listing (SaaS)

1. Seller prerequisites: tax interview, USD bank account (disbursement method; wait up to 2 business days after profile), KYC/BAV if applicable [A51][A56].
2. Optional: ask the Partner Assistant "Help me build my product information from my website: [URL]" and "Score the quality of my listing" [A64].
3. Build > SaaS products (AMMP) > create SaaS contract or subscription; set dimensions (API name max 15 chars, immutable) [A57].
4. Integrate: registration URL, Entitlement/Metering APIs, EventBridge events; support Concurrent Agreements (required for new SaaS products since 2026-06-01) [A57][A101].
5. Submit for review; plan 7 to 10 business days of AWS review and 2 to 4 weeks end to end (VENDOR) [A25].
6. Add Buy with AWS CTAs and request buttons; enable free trial (7 to 90 days) if PLG [A61][A57].
7. Done when listing is Public and a test buyer can reach the fulfillment URL.

### 13.5 Create a private offer

1. Confirm at least one active public listing and IAM access to Private offers [A52].
2. Sell > Private offers > Create private offer > offer type, product type, product (cannot change later) [A52].
3. Offer info: name, details, purpose, expiration date; geo-targeting countries [A52].
4. Pricing and duration: dimensions, custom duration (SaaS contract up to 144 months), installment plan or upfront; payment terms (Net 15 to 120 or customer default) [A57][A55].
5. Legal: standard contract or custom EULA (up to five docs) [A52].
6. Buyer accounts: the buyer's account that will subscribe (plus private marketplace admin account if used) [A52].
7. Publish; send offer URL to the buyer [A52].
8. Link the offer to the ACE opportunity (Associate) and, if using RA IDs, add the offer to the attribution [A48][A50].
9. If eligible, request MPOPP credits in the Funding Portal [A31].
10. Done when the offer appears as Active and later as an Agreement after acceptance.

### 13.6 Create a channel (CPPO) offer

ISV side:
1. Get the reseller's 12-digit AWS account ID; confirm they are a paid seller with the service-linked role [A53].
2. AMMP > Selling authorizations > Create selling authorization > name, reseller ID, product type and product > details (description, renewal flag, optional buyer IDs) > pricing model, currency, duration, dimensions and wholesale price, maximum payment terms > review legal entity name > create [A53][A55].
3. Done when authorization shows Active for the reseller.
Reseller side:
4. Sell > Private offers > Create private offer > choose CPPO from resale authorization > ISV, product, authorization > mark up > buyer account > publish (same currency as authorization) [A52][A53].
5. Done when buyer accepts; both parties see the agreement; ISV fee includes +0.5% uplift [A24].

### 13.7 Register and share an opportunity

1. Sell > Opportunities > Create opportunity > Create using agent (upload call notes) or wizard [A43].
2. Fill: specific business problem; Use Case and Industry (not Other); Co-Sell with AWS plus partner needs; Opportunity Type; future Target Close Date; associate solution or Marketplace product; MAP details if migration [A43].
3. Deal sizing: import Pricing Calculator URL or TCV plus months [A43].
4. Submit. Done when status Submitted, then Approved (up to 5 business days) [A47].
5. If Action Required: follow AWS recommended actions, edit, resubmit [A43].
6. After approval: read the motion and score; if Field-engaged, contact named AWS rep within 48 hours; if Agent-engaged or Partner-led, use the agent's sales play and still ask your PDM for an AM intro [A3][A87].
7. Weekly: next step (action, owner, date) and stage; at close set Launched with AWS account ID and linked offer, or Closed Lost with reason [A43][A47].

### 13.8 Accept an AWS referral

1. Sell > Opportunities > Opportunity Invitations (or Leads > Lead invitations) daily [A43].
2. Open Opportunity ID to read pre-acceptance fields; decide within 5 business days [A43].
3. Accept Invitation (bulk allowed) or reject with reason [A43][A40].
4. Contact the AWS Sales Rep and PSM named on the record; log first next step [A43].
5. Done when opportunity is in the Opportunities tab with a dated next step.

### 13.9 Request and claim funding

1. Open the opportunity > Funding Recommendation widget > Get estimated funding > Create fund request (or Funding Benefits > Funding dashboard > Create fund request > program) [A46].
2. Complete template, attach SOW/plan as PDF (avoid spreadsheets with formulas) [A46].
3. Track stages: AWS Review, Tech Approval (PSA), Business Approval, Finance Approval, Pre-Approval [A46].
4. Execute only after Pre-Approval (MAP: Cash Claim stage signals pre-approval) [A46].
5. Submit claim actuals at completion; then invoice via Payee Central link [A46].
6. Watch expiry: 30 days after delivery end date [A46].
7. Done when stage Completed.

### 13.10 Audit current status (first call with a new customer)

| Check | Where | Pass condition |
|---|---|---|
| Console migration | Dashboard | No "Not Registered"; agents available [A44] |
| Linked account type | Partner Central settings / account linking | Paid, company-owned member account [A112] |
| IAM coverage | IAM | Named owners with correct policies [A45] |
| Paths and stage | Partner Scorecard | Validated or better [A45] |
| Solutions | Build > Solutions | At least one Public/Limited, linked to Marketplace product [A43] |
| FTR | Solutions > Validation | Approved, expiry more than 90 days out [A49] |
| PRM | Partner analytics > Attributed Revenue > Onboarding Status | Active per product [A77] |
| Listing | AMMP | Public; Deployed on AWS; request buttons on [A38][A52] |
| Pipeline | Sell > Opportunities | T12M qualified at least 15, launched at least 5; none For Visibility Only by mistake [A1] |
| Quality | Opportunity list | Average score trend; Action Required count zero [A3] |
| Invitations | Opportunity/Lead invitations | None older than 3 business days [A43] |
| Offers linked | Opportunities with Marketplace deals | Offer associated [A48] |
| Funding | Funding dashboard, Investments | Active requests; no expired [A46] |
| Programs | Program applications | ISVA status, competencies, renewal dates [A45] |
| CRM | Connector version / API | API-based, v3.20 or later [A47] |
| Subsidiaries | Account connections | All seller accounts connected [A112] |

### 13.11 Implement PRM

1. Get product code: AMMP > Products > product > Product Summary (use product code, not product ID) [A13].
2. Pick method: Marketplace metering (AMI/ML automatic), resource tagging, or User Agent [A13].
3. Tagging: key `aws-apn-id`, value `pc:<product-code>`, applied via IaC for managed resources (console/CLI tags cause drift) [A13].
4. User Agent: `sdk_ua_app_id=APN_1.1/pc_<product-code>$` in `~/.aws/config` or env var `AWS_SDK_UA_APP_ID`; at least one API call per resource per month [A13].
5. Validate in CloudTrail (userAgent field) [A13].
6. Done when product shows onboarded in Attributed Revenue (up to 7 days; monthly data 17 days after month end) [A49][A77].
7. Optional: create Revenue Attribution IDs per deal (`CreateRevenueAttribution`) and allocate by offer or opportunity per billing month [A50].

### 13.12 Upgrade CRM integration from S3 to API (Salesforce connector)

1. Confirm account linking (hard prerequisite) [A47].
2. Do it in a Salesforce sandbox first [A47].
3. Install latest connector from AppExchange; set up AWS infrastructure (IAM role) [A47].
4. Review mappings, add required fields and buttons ("Share with AWS") [A47][A9].
5. Disable S3 schedules; delete old APN scheduled jobs to avoid duplicates [A47][A9].
6. Deactivate legacy validation rules (Setup > Object Manager > ACE Opportunity > Validation Rules) [A47].
7. Backfill opportunities from AWS (Last Modified Date) [A47].
8. Monitor EventBridge events. Done when a test opportunity round-trips and AWS updates appear in Salesforce [A47].

### 13.13 Prep for a field seller meeting

1. Pull the AWS contacts from the opportunity (AM, PSM, PDM) [A43].
2. Refresh the record: score, next step, AWS services, Pricing Calculator MRR [A3].
3. Generate a sales play on the opportunity (Opportunity Insights > Generate sales play) and a customer profile [A43].
4. Prepare a one-page brief: customer problem and why now, AWS consumption impact (services and monthly spend), commit status, Marketplace path (private offer, Deployed on AWS), funding available (POC, MPOPP), 2 to 3 explicit asks [A104][A46].
5. Bring proof: case study, competency badge, Vendor Insights profile [A59].
6. After the meeting: next step with owner and date within 24 hours [A43].

### 13.14 Monthly program health check

1. Run 13.10 audit table.
2. Compute T12M qualified and launched counts vs ISVA and tier thresholds [A1][A17].
3. Review Quality Score distribution and motion mix [A3].
4. Attributed Revenue trend by product and service [A77].
5. Marketplace: new agreements, renewals due in 90 days, disbursements [A45].
6. Funding: open requests, claims due, expiring requests [A46].
7. Certifications and accreditations counts (Services) [A17].
8. Check official change feeds (Tier 0 in the creator registry) and log changes in section 8.
9. Done when a dated status note is filed with owners for each gap.

## 14. Unverified, conflicting or login-gated

| Item | Status | Detail |
|---|---|---|
| Legacy portal shutdown date | CONFLICTING | WorkSpan (2025-11-30) says migration must complete by June 30, 2026 [A102]; AWS migration docs and What's New state no deadline [A8][A11]; Suger (2026-08-24) says no end-of-life date published [A9]. Treat as unconfirmed. |
| MDF, POC, MAP, ISV WMP, MPOPP amounts and rates | LOGIN-GATED | AWS Partner Funding Benefits Guide and MDF Guide in Partner Central. MAP percentages in section 7 are VENDOR [A113], updated 2026-05. |
| ISVA MDF amount | NOT PUBLISHED | [A6] |
| SCB quota credit percentage | NOT PUBLISHED | Quota retirement wording is VENDOR [A37][A84] |
| ACE eligibility criteria | LOGIN-GATED | ACE FAQ; vendor summary [A108] derived from a November 2023 FAQ: `[UNVERIFIED, source dated 2023-11]` |
| 25% cap on Marketplace commit retirement | CONTRACT-SPECIFIC | VENDOR/INDEPENDENT [A38][A39]; AWS buyer FAQ only says eligible products deployed on AWS typically qualify [A60] |
| Seller Prime ($10K credit, up to $40K MDF) | UNVERIFIED | VENDOR only [A86][A85], source dated 2025-01; not found on current AWS pages |
| List and Sell $10K credits; ACE-CRM integration $10K credits | UNVERIFIED | VENDOR [A25]; official page gives no amount [A30] |
| APN fee $2,500 on Software Path | PARTLY VERIFIED | $2,500/year verified for Services tiers [A17]; Software Path figure is VENDOR [A16][A37]. Tackle says the fee is returned as $3,500 in credits (VENDOR, 2025-04) `[UNVERIFIED, source dated 2025-04]` |
| Services path fee at Registered stage | NOT CONFIRMED | Services tiers page lists $2,500 for Select, Advanced, Premier [A17] |
| Opportunity Quality Score thresholds for motion assignment | NOT PUBLISHED | CREATOR speculation that field assignment happens around 30 to 35 [A87]; an 85 routed Partner-led [A88] |
| Specialization renewals requiring launched ACE opportunities | INDEPENDENT only | [A34] |
| BVR Competency $50K MDF | INDEPENDENT only | [A72]; BVR What's New gives no amounts [A98] |
| Generative AI Accelerator 2026 cohort | NOT FOUND | Only 2025 cohort dates published [A70] |
| MAP 2026 changes | PARTIAL | MAP page lists phases, no amounts [A66]; January 2026 MAP data enrichments in ACE [A43] |
| Marketplace seller guide document history | FETCH BLOCKED | Page redirects in loop; rely on What's New and AppExchange release notes |
| Partner Scorecard metric definitions per tier | LOGIN-GATED | Partner Central |
| Tackle ownership | INDEPENDENT | Omdia reported AppDirect's acquisition of Tackle.io (December 2025) [A123]; relevant because Tackle is a major ACE/Marketplace integrator |


### 14.V Vendor-sourced items to verify (Tackle, Clazar, Suger, WorkSpan; added 2026-09-26)

All VENDOR. Detail and sources in `vendors/{vendor}-intelligence.md`. Official pages win on conflict.

| Item | Vendor claim | Official status | Action |
|---|---|---|---|
| S3 CRM sync end | Ends 2026-09-30; bucket access revoked 2026-10-30 (WorkSpan customer notice) | No AWS date published | Treat as urgent; move to Partner Central API now |
| Console migration final date | 2026-09-30 per AWS emails cited on a WorkSpan webinar; PDMs pushed 2026-06-30 | No AWS date published | Migrate now; do not wait for a published cutoff |
| ACE eligibility count | 10 validated opportunities (Tackle) vs 15 (our earlier vendor summary) | Login-gated ACE FAQ | Confirm in Partner Central |
| Referral response window | 72 hours (Clazar) | 5 business days [A43] | Use 5 business days; aim for same day |
| PRM deadline | 2026-07-31, or 2026-05-31 for AI Competency holders (Clazar, later called planning dates) | Not published | Enable PRM now regardless |
| $5K credit for 10+ opportunities updated via Partner Central MCP by 2026-12-01 | Clazar | Not on public AWS pages | Ask the PDM before counting on it |
| List & Sell and CRM-connect credits ($10K each) | Clazar: List & Sell needs $65K contract value or 10+ private offers in 12 months | Thresholds not published | Verify with PDM |
| Seller quota retirement on marketplace deals | "42% of our deal" (Qualtrics, WorkSpan webinar, 2025) | No rate published | Anecdote only, never a promise |
| Opportunity Quality Score behavior | Lowest bucket scores 0; template text in fields; PDM says scoring follows a MEDDPICC-like model and rewards a specific ask (Suger) | Criteria not published | Use as record-quality checklist in M5 |
| Solution Matching Engine | Internal AWS engine fed by ACE data recommends partners to sellers and Marketplace agent mode (PDM on Suger webinar) | Unofficial | Keep ACE data complete; context only |
| Vendor Insights | Automated assessments closed to new sellers (Suger) | Re-check [A59] | Do not recommend as a new-seller step until verified |
| Net payment terms | Net 30 to 90 (Suger) | Customer default and Net 15 to Net 120 (official, re-fetched 2026-09-26) | Official wins |
| MPOPP credit linkage | Accepted private offer must be linked to the opportunity at Launched (Tackle) | Consistent with [A31] | Add to M4 checklist |
| Rejection messages | WorkSpan's list of 56 AWS co-sell rejection messages | Vendor list | Use as pre-submission checklist in M5 |

## Sources

| Tag | Title | Publisher | Date | Label | URL |
|---|---|---|---|---|---|
| A1 | AWS ISV Accelerate Program | AWS | fetched 2026-09-26 | OFFICIAL | https://aws.amazon.com/partners/programs/isv-accelerate/ |
| A2 | Co-Sell with AWS | AWS | fetched 2026-09-26 | OFFICIAL | https://aws.amazon.com/partners/co-sell-with-aws/ |
| A3 | Co-sell engagement (Partner Central Sales Guide) | AWS Docs | fetched 2026-09-26 (feature 2026-06-16) | OFFICIAL | https://docs.aws.amazon.com/partner-central/latest/sales-guide/co-sell-engagement.html |
| A4 | Document history, Partner Central Getting Started Guide | AWS Docs | through 2026-03-16 | OFFICIAL | https://docs.aws.amazon.com/partner-central/latest/getting-started/doc-history.html |
| A5 | New agentic capabilities to take you from registered to ready-to-sell in days (Letourneau, Patel, Bar Lev) | AWS APN Blog | 2026-06-16 | OFFICIAL | https://aws.amazon.com/blogs/apn/get-ready-to-sell/ |
| A6 | New AWS ISV Accelerate benefits: Unlock the co-sell advantage (Bohmann, Vela, Estrada, Kim) | AWS APN Blog | 2026-03-16 | OFFICIAL | https://aws.amazon.com/blogs/apn/new-aws-isv-accelerate-benefits-unlock-the-co-sell-advantage/ |
| A7 | Powering Next-Level Partner Success: Innovations for Growth and Scale in 2026 (Bains) | AWS APN Blog | 2025-12-01, updated 2026-03-25 | OFFICIAL | https://aws.amazon.com/blogs/apn/powering-partner-success-2026-innovations/ |
| A8 | Migrating to Partner Central in the AWS Console | AWS Docs | fetched 2026-09-26 | OFFICIAL | https://docs.aws.amazon.com/partner-central/latest/getting-started/migrating-to-partner-central.html |
| A9 | Migrating to the New AWS Partner Central (ACE) (Sabrina Xie) | Suger | 2026-08-24 | VENDOR | https://www.suger.io/resources/blog/migrating-to-aws-partner-central/ |
| A10 | AWS Partner Central Migration Guide | Clazar Knowledge Base | about 2026-08 | VENDOR | https://help.clazar.io/articles/2549501160-aws-partner-central-migration-guide |
| A11 | AWS Partner Central is now available in the AWS Management Console | AWS What's New | 2025-11-30 | OFFICIAL | https://aws.amazon.com/about-aws/whats-new/2025/11/aws-partner-central-available-management-console |
| A12 | New Partner Revenue Measurement gives visibility into AWS service consumption | AWS What's New | 2026-01-30 | OFFICIAL | https://aws.amazon.com/about-aws/whats-new/2026/01/new-partner-revenue-measurement |
| A13 | AWS Partner Revenue Measurement onboarding guide (getting started, implementation methods, partner FAQ, automated user agent, manual tagging) | AWS Docs | fetched 2026-09-26 | OFFICIAL | https://docs.aws.amazon.com/PRM/latest/aws-prm-onboarding-guide/getting-started.html |
| A14 | Partner Revenue Measurement now supports AWS Marketplace Metering | AWS What's New | 2026-04-03 | OFFICIAL | https://aws.amazon.com/about-aws/whats-new/2026/04/partner-revenue-supports-mp-metering |
| A15 | Announcing AWS Partner Central agents to accelerate co-sell | AWS What's New | 2026-03-16 | OFFICIAL | https://aws.amazon.com/about-aws/whats-new/2026/03/aws-partner-central-agents-accelerate-co-sell/ |
| A16 | The Complete Guide to AWS Partner Programs in 2026 (Samhita Suresh) | Labra | 2026-03-02 | VENDOR | https://labra.io/aws-partner-programs-guide/ |
| A17 | AWS Services Partner Tiers | AWS | fetched 2026-09-26 | OFFICIAL | https://aws.amazon.com/partners/services-tiers/ |
| A18 | AWS Partner Paths | AWS | fetched 2026-09-26 | OFFICIAL | https://aws.amazon.com/partners/paths/ |
| A19 | AWS Foundational Technical Review | AWS | fetched 2026-09-26 | OFFICIAL | https://aws.amazon.com/partners/foundational-technical-review/ |
| A20 | AWS Specialization Program (Competencies) | AWS | fetched 2026-09-26 | OFFICIAL | https://aws.amazon.com/partners/programs/competencies/ |
| A21 | The AWS ISV Partner Path Is Now the Software Path (Sabrina Xie) | Suger | 2026-08-09 | VENDOR | https://www.suger.io/resources/blog/aws-isv-partner-path/ |
| A22 | More Value, Greater Profitability: 10 Enhancements to the AWS Partner Experience (Bains) | AWS APN Blog | 2023-11-29 | OFFICIAL | https://aws.amazon.com/blogs/apn/more-value-greater-profitability-10-enhancements-to-the-aws-partner-experience/ |
| A23 | New Programs, Benefits, and Tools: Empowering AWS Partners for Greater Profitability (Bains) | AWS APN Blog | 2024-07-09 | OFFICIAL | https://aws.amazon.com/blogs/apn/new-programs-benefits-and-tools-empowering-aws-partners-for-greater-profitability/ |
| A24 | Understanding listing fees for AWS Marketplace sellers | AWS Docs | fetched 2026-09-26 | OFFICIAL | https://docs.aws.amazon.com/marketplace/latest/userguide/listing-fees.html |
| A25 | Selling on AWS Marketplace: The Complete 2026 Guide | Suger | 2026-04-23, reviewed 2026-08-02 | VENDOR | https://www.suger.io/resources/guides/aws-marketplace/ |
| A26 | What a Marketplace Dollar Actually Costs You (Shirley Guo) | Suger | 2026-08-06 | VENDOR | https://www.suger.io/resources/blog/what-a-marketplace-dollar-costs-you/ |
| A27 | Introducing AI agents and tools in AWS Marketplace | AWS What's New | 2025-07 | OFFICIAL | https://aws.amazon.com/about-aws/whats-new/2025/07/ai-agents-tools-aws-marketplace |
| A28 | AWS Marketplace reduces listing fee for professional services to 0.5% | AWS What's New | 2026-06-16 | OFFICIAL | https://aws.amazon.com/about-aws/whats-new/2026/06/reduce-listing-fee-professional-services-aws-marketplace/ |
| A29 | AWS Marketplace reduces listing fee for professional services in multi-product solutions | AWS What's New | 2026-09-01 | OFFICIAL | https://aws.amazon.com/about-aws/whats-new/2026/09/aws-marketplace-fee-professional-services/ |
| A30 | AWS Marketplace List and Sell Program | AWS | fetched 2026-09-26 | OFFICIAL | https://aws.amazon.com/partners/saas-on-aws/mpls/ |
| A31 | Announcing new incentives for ISVs selling in AWS Marketplace (MPOPP) | AWS What's New | 2025-08-12 | OFFICIAL | https://aws.amazon.com/about-aws/whats-new/2025/08/aws-marketplace-private-offer-promotions/ |
| A32 | Best Practices for Developing an AWS Co-Sell Program (Tyler Althoff) | AWS APN Blog | 2023-07-20, updated 2023-09-21 | OFFICIAL | https://aws.amazon.com/blogs/apn/best-practices-for-developing-an-aws-co-sell-program/ |
| A33 | How AWS Partners Can Optimize GTM Strategy with the Co-Sell Development Framework (Tyler Althoff) | AWS APN Blog | 2023-09-21 | OFFICIAL | https://aws.amazon.com/blogs/apn/how-aws-partners-can-optimize-gtm-strategy-with-the-co-sell-development-framework/ |
| A34 | How to Co-Sell With AWS: ACE, ISV Accelerate and the Path to Partner-Led Growth (Chris Buckel) | flashdba | 2026-06-17, reviewed 2026-09-02 | INDEPENDENT | https://flashdba.com/hyperscaler-gtm/co-sell/aws/ |
| A35 | AWS EDP: What Marketplace Sellers Need to Know (Stacy Wu) | Suger | 2026-08-05 | VENDOR | https://www.suger.io/resources/blog/aws-edp-what-sellers-need-to-know/ |
| A36 | Co-selling with AWS guide | Clazar | 2026 (undated) | VENDOR | https://clazar.io/guides/co-selling-with-aws |
| A37 | How to Achieve AWS SaaS Co-Sell Benefit and Maximize Co-Sell Success (Kaley Edmonds) | Tackle | 2025-04-24 | VENDOR | https://tackle.io/blog/how-to-achieve-aws-saas-co-sell-benefit-and-maximize-co-sell-success/ |
| A38 | AWS Tightens the Reins: New AWS SaaS Marketplace Rules Will Impact Your Commitments (Corey Quinn) | Duckbill | 2025-02-06, updated 2025-10-29 | INDEPENDENT | https://www.duckbillhq.com/blog/new-aws-marketplace-rules/ |
| A39 | AWS SaaS Marketplace Policy Changes (Shouri Thallam) | nOps | 2025-04-03 | VENDOR | https://www.nops.io/blog/aws-saas-marketplace-policy-changes-for-may-2025/ |
| A40 | AWS Partner Central Selling API guide (reference, opportunities from AWS, best practices) | AWS Docs | fetched 2026-09-26 | OFFICIAL | https://docs.aws.amazon.com/partner-central/latest/selling-api/aws-partner-central-api-reference-guide.html |
| A41 | LifeCycle data type | AWS Docs | fetched 2026-09-26 | OFFICIAL | https://docs.aws.amazon.com/partner-central/latest/APIReference/API_LifeCycle.html |
| A42 | submit-opportunity (AWS CLI) | AWS Docs | fetched 2026-09-26 | OFFICIAL | https://docs.aws.amazon.com/cli/v1/reference/partnercentral-selling/submit-opportunity.html |
| A43 | AWS Partner Central Sales Guide (creating opportunity, review process, accepting, leads, updating, stage visibility, agents, doc history) | AWS Docs | through 2026-06-30 | OFFICIAL | https://docs.aws.amazon.com/partner-central/latest/sales-guide/creating-opportunity.html |
| A44 | Partner Central Getting Started: account selection, registration process, verification, registration form, FAQ | AWS Docs | fetched 2026-09-26 | OFFICIAL | https://docs.aws.amazon.com/partner-central/latest/getting-started/registration-process.html |
| A45 | Partner Central Getting Started: navigation sections, onboarding agent, managed policies, scorecard, program applications | AWS Docs | fetched 2026-09-26 | OFFICIAL | https://docs.aws.amazon.com/partner-central/latest/getting-started/navigate-partner-central.html |
| A46 | Partner Central funding: accessing funding, creating fund request, funding agent | AWS Docs | fetched 2026-09-26 | OFFICIAL | https://docs.aws.amazon.com/partner-central/latest/getting-started/create-fund-request.html |
| A47 | AWS Partner CRM integration guide (options, business flows, S3 to API upgrade, connector overview, release notes to v3.20) | AWS Docs | through 2026-07-17 | OFFICIAL | https://docs.aws.amazon.com/partner-central/latest/crm/upgrade-crm-api.html |
| A48 | Partner Central MCP server, tools reference, Selling API quotas | AWS Docs | fetched 2026-09-26 | OFFICIAL | https://docs.aws.amazon.com/partner-central/latest/selling-api/partner-central-mcp-server.html |
| A49 | Partner Central Builder Guide: What is a solution; Request Foundational Technical Review | AWS Docs | fetched 2026-09-26 | OFFICIAL | https://docs.aws.amazon.com/partner-central/latest/builder-guide/requesting-ftr.html |
| A50 | Working with your Revenue Attribution IDs | AWS Docs | fetched 2026-09-26 | OFFICIAL | https://docs.aws.amazon.com/partner-central/latest/selling-api/working-with-revenue-attribution.html |
| A51 | Seller eligibility requirements | AWS Docs | fetched 2026-09-26 | OFFICIAL | https://docs.aws.amazon.com/marketplace/latest/userguide/seller-eligibility.html |
| A52 | Preparing a private offer; Creating and managing private offers | AWS Docs | fetched 2026-09-26 | OFFICIAL | https://docs.aws.amazon.com/marketplace/latest/userguide/private-offers-overview.html |
| A53 | Channel Partner private offers; Creating a selling authorization as an ISV | AWS Docs | fetched 2026-09-26 | OFFICIAL | https://docs.aws.amazon.com/marketplace/latest/userguide/channel-partner-offers.html |
| A54 | Express private offers | AWS Docs | fetched 2026-09-26 | OFFICIAL | https://docs.aws.amazon.com/marketplace/latest/userguide/express-private-offers.html |
| A55 | Configuring net payment terms for private offers | AWS Docs | fetched 2026-09-26 | OFFICIAL | https://docs.aws.amazon.com/marketplace/latest/userguide/seller-net-payment-terms.html |
| A56 | Managing disbursements; Set disbursement preferences | AWS Docs | fetched 2026-09-26 | OFFICIAL | https://docs.aws.amazon.com/marketplace/latest/userguide/managing-disbursements.html |
| A57 | SaaS contracts, SaaS subscriptions, SaaS free trials | AWS Docs | fetched 2026-09-26 | OFFICIAL | https://docs.aws.amazon.com/marketplace/latest/userguide/saas-contracts.html |
| A58 | AI agent products | AWS Docs | fetched 2026-09-26 | OFFICIAL | https://docs.aws.amazon.com/marketplace/latest/userguide/ai-agents-tools.html |
| A59 | AWS Marketplace Vendor Insights | AWS Docs | fetched 2026-09-26 | OFFICIAL | https://docs.aws.amazon.com/marketplace/latest/userguide/vendor-insights.html |
| A60 | Multi-product solutions (seller) and Multi-Product Solutions buyer FAQ (EDP/PPA) | AWS Docs | fetched 2026-09-26 | OFFICIAL | https://docs.aws.amazon.com/marketplace/latest/buyerguide/multi-product-solutions-buyer-faq.html |
| A61 | Using Buy with AWS as a buyer | AWS Docs | fetched 2026-09-26 | OFFICIAL | https://docs.aws.amazon.com/marketplace/latest/buyerguide/buy-with-aws.html |
| A62 | Agent mode for AWS Marketplace | AWS Docs | fetched 2026-09-26 | OFFICIAL | https://docs.aws.amazon.com/marketplace/latest/buyerguide/agent-mode.html |
| A63 | Product reviews for items listed in AWS Marketplace | AWS Docs | fetched 2026-09-26 | OFFICIAL | https://docs.aws.amazon.com/marketplace/latest/buyerguide/buyer-product-reviews.html |
| A64 | AI-assisted product listing; Marketing your product | AWS Docs | fetched 2026-09-26 | OFFICIAL | https://docs.aws.amazon.com/marketplace/latest/userguide/ai-assisted-product-listing.html |
| A65 | AWS Partner Funding | AWS | fetched 2026-09-26 | OFFICIAL | https://aws.amazon.com/partners/funding/ |
| A66 | AWS Migration Acceleration Program | AWS | fetched 2026-09-26 | OFFICIAL | https://aws.amazon.com/migration-acceleration-program/ |
| A67 | AWS Activate credits | AWS | fetched 2026-09-26 | OFFICIAL | https://aws.amazon.com/startups/credits |
| A68 | AWS ISV Workload Migration Program | AWS | fetched 2026-09-26 | OFFICIAL | https://aws.amazon.com/partners/programs/isv-workload-migration/ |
| A69 | Partner Greenfield Program | AWS | fetched 2026-09-26 | OFFICIAL | https://aws.amazon.com/partners/programs/partner-greenfield/ |
| A70 | Generative AI Accelerator | AWS Startups | fetched 2026-09-26 (2025 cohort) | OFFICIAL | https://aws.amazon.com/startups/programs/generative-ai |
| A71 | AWS Specialization Program 2025 enhancements and looking ahead (Costlow, Butler, Erdem, Chatelain) | AWS APN Blog | 2026-01-12 | OFFICIAL | https://aws.amazon.com/blogs/apn/aws-specialization-program-2025-enhancements-and-looking-ahead |
| A72 | AWS builds new partner strategy around agentic AI outcomes (Todd R. Weiss) | ChannelE2E | 2026-06-29 | INDEPENDENT | https://www.channele2e.com/news/aws-builds-new-partner-strategy-around-agentic-ai-outcomes |
| A73 | New agentic AI categories for AWS AI Competency partners (Dally, Rojo, Butler) | AWS APN Blog | 2025-11-30 | OFFICIAL | https://aws.amazon.com/blogs/apn/new-agentic-ai-categories-for-aws-ai-competency-partners |
| A74 | APN Blog announcements index (pages 1 and 2) | AWS APN Blog | through 2026-09-22 | OFFICIAL | https://aws.amazon.com/blogs/apn/category/post-types/announcements/ |
| A75 | Sell smarter with AWS: New agentic capabilities accelerate time to revenue (Thayer, Kandaswamy) | AWS APN Blog | 2026-06-16 | OFFICIAL | https://aws.amazon.com/blogs/apn/sell-smarter-with-aws/ |
| A76 | Grow your services business through AWS Marketplace (Petit, Matz) | AWS APN Blog | 2026-09-22 | OFFICIAL | https://aws.amazon.com/blogs/apn/grow-your-services-business-through-aws-marketplace/ |
| A77 | Unlock revenue insights in the new Attributed Revenue Dashboard; Attributed Revenue docs | AWS APN Blog / Docs | 2026-04-21 | OFFICIAL | https://aws.amazon.com/blogs/apn/unlock-revenue-insights-in-the-new-attributed-revenue-dashboard/ |
| A78 | Introducing AWS Partner Central agents (Schreiber, Bhopatkar, Thayer) | AWS APN Blog | 2026-03-16 | OFFICIAL | https://aws.amazon.com/blogs/apn/introducing-aws-partner-central-agents/ |
| A79 | Accelerating AWS Partner Success: New Initiatives to Drive Customer Value in 2025 (Bains) | AWS APN Blog | 2024-12-04, modified 2025-06-12 | OFFICIAL | https://aws.amazon.com/blogs/apn/accelerating-aws-partner-success-new-initiatives-to-drive-customer-value-in-2025/ |
| A80 | AWS Driving Customer Value in 2025 with Partner Program Enhancements | Channel Insider | 2024-12 | INDEPENDENT | https://www.channelinsider.com/security/managed-services/aws-2025-partner-program-upgrades/ |
| A81 | A Guide to AWS Marketplace's New Incentives (Sienna Quirk) | Invisory | 2024-12-06, updated 2025-04-15 | VENDOR | https://invisory.co/resources/blog/a-guide-to-aws-marketplaces-new-incentives-2025/ |
| A82 | The Amazon Operating Cadence | Working Backwards | undated | INDEPENDENT | https://workingbackwards.com/concepts/amazon-operating-cadence/ |
| A83 | AWS Marketplace Partnerships: Strategies from Pete Goldberg | Clazar | 2024-11-22 | VENDOR | https://clazar.io/blog/hyperscaler-isv-relationships-aws-marketplace-pete-goldberg |
| A84 | Unlock Revenue Potential: AWS SaaS Revenue Recognition Program (Shirley Guo) | Suger | 2025-01-28 | VENDOR | https://www.suger.io/blog/aws-saas-revenue-recognition-program |
| A85 | How to Sell on AWS Marketplace: A Complete Guide (2026) | Clazar | 2026 (undated) | VENDOR | https://clazar.io/guides/aws-marketplace |
| A86 | 5 things you should know about AWS Marketplace Seller Prime (Stacy Wu) | Suger | 2025-01-15 | VENDOR | https://www.suger.io/resources/blog/aws-marketplace-seller-prime/ |
| A87 | My Quality Score Never Hit 40, Here's What I Learned (Andrew Morris, Michael Musselman) | Beyond Co-Sell (YouTube) | about 2026-07 | CREATOR | https://www.youtube.com/watch?v=XTw4NB4FRis |
| A88 | He Scored 85, AWS Still Didn't Send a Rep (with Nikolay Nikolaev) | Beyond Co-Sell (YouTube) | 2026-08-18 | CREATOR | https://www.youtube.com/watch?v=WBDi7UNkURA |
| A89 | Why You Should Negotiate Your AWS PPA and SCA at the Same Time | Beyond Co-Sell (YouTube) | 2026-09-03 | CREATOR | https://www.youtube.com/watch?v=ZFOIVuuYZ2E |
| A90 | State of Cloud Marketplaces and Co-Sell report insights (Trunal Bhanse) | Clazar | 2025-04-24 | VENDOR | https://clazar.io/blog/state-of-cloud-marketplace-and-co-sell-report-insights |
| A91 | State of Cloud GTM 2025 report (Alex Murdoch) | Tackle | 2025-12-17 | VENDOR | https://tackle.io/blog/state-of-cloud-gtm-2025-committed-spend-engagement-and-the-new-marketplace-landscape/ |
| A92 | AWS launches its partners into the era of AI at re:Invent 2025 (Alastair Edwards, Peter Bryant) | Omdia | 2026-01-09 | INDEPENDENT | https://omdia.tech.informa.com/blogs/2026/jan/aws-launches-its-partners-into-the-era-of-ai-at-reinvent-2025 |
| A93 | The AWS re:Invent 2025 Marketplace Breakdown (Samhita Suresh) | Labra | 2025-12-09 | VENDOR | https://labra.io/aws-reinvent-2025-recap/ |
| A94 | AWS re:Invent 2026 | AWS | fetched 2026-09-26 | OFFICIAL | https://aws.amazon.com/events/reinvent/ |
| A95 | AWS Partner Central now supports AWS Marketplace listings for co-selling | AWS What's New | 2026-07-01 | OFFICIAL | https://aws.amazon.com/about-aws/whats-new/2026/07/aws-marketplace-co-selling-support/ |
| A96 | AWS Marketplace sellers now receive qualified demo and private offer requests in minutes | AWS What's New | 2026-09-09 | OFFICIAL | https://aws.amazon.com/about-aws/whats-new/2026/09/aws-marketplace-demo-private-offer-requests-qualification/ |
| A97 | AWS Partner Central introduces Partner Lead Prospecting | AWS What's New | 2026-07-09 | OFFICIAL | https://aws.amazon.com/about-aws/whats-new/2026/07/aws-partner-central-prospecting/ |
| A98 | AWS Partner Central launches new funding benefits for Business Value Realization; BVR docs | AWS What's New / Docs | 2026-06-16 | OFFICIAL | https://aws.amazon.com/about-aws/whats-new/2026/06/aws-partner-business-value-realization/ |
| A99 | AWS Marketplace Storefront is now generally available | AWS What's New | 2026-06-16 | OFFICIAL | https://aws.amazon.com/about-aws/whats-new/2026/06/aws-marketplace-storefront/ |
| A100 | AWS Partner Central agents MCP Server now supports OAuth with AWS Sign-In | AWS What's New | 2026-08-20 | OFFICIAL | https://aws.amazon.com/about-aws/whats-new/2026/8/aws-partner-central-mcp/ |
| A101 | AWS Marketplace now supports multiple purchases of SaaS and Professional Services products (Concurrent Agreements) | AWS What's New | 2026-02-26 | OFFICIAL | https://aws.amazon.com/about-aws/whats-new/2026/02/concurrent-agreements-february |
| A102 | AWS Partner Central 3.0 Migration Guide (Amit Sinha) | WorkSpan | 2025-11-30 | VENDOR | https://www.workspan.com/blog/free-aws-partner-console-migration |
| A103 | The agentic era and the 7x multiplier: AWS re:Invent 2025 partner recap (Juhi Saha) | Partner1 | 2025-12-18 | VENDOR | https://www.partner1.io/partner-blog/aws-reinvent-2025 |
| A104 | 7 Seller Coaching Tactics to Convert $531B Cloud Commits into Marketplace Revenue (Roman Kirsanov) | Partner Insight newsletter | 2025-11-18 | CREATOR | https://newsletter.partnerinsight.io/p/7-seller-coaching-tactics-to-convert |
| A105 | March 2026 Product Updates (Ashley Stachura) | Tackle | 2026-03-18 | VENDOR | https://tackle.io/blog/cloud-gtm-product-updates-march-2026-tackle/ |
| A106 | Jen Dawson: why most ISVs misunderstand (Chip Rodgers) | Inside Partnering (Substack) | 2026-02-03 | CREATOR | https://insidepartnering.substack.com/p/jen-dawson-why-most-isvs-misunderstand |
| A107 | The Jen GTM Show | SaaSNova | fetched 2026-09-26 | CREATOR | https://www.saasnova.ai/show |
| A108 | Becoming ACE Eligible | Labra Help Center | undated (derived from 2023-11 ACE FAQ) | VENDOR | https://helpcenter.labra.io/hc/en-us/articles/32330411617171-Becoming-ACE-Eligible |
| A109 | APN Customer Engagements (ACE) Program | AWS | fetched 2026-09-26 | OFFICIAL | https://aws.amazon.com/partners/programs/ace/ |
| A110 | Amazon.com Q2 2025 results (fiscal quarter ended June 30, 2025) | Amazon / SEC | 2025-07-31 | OFFICIAL | https://www.sec.gov/Archives/edgar/data/0001018724/000101872425000084/amzn-20250630xex991.htm |
| A111 | Best practices for receiving, accepting, and distributing private offers in AWS Marketplace (Soumya Vanga) | AWS Marketplace Blog | 2023-07-28 | OFFICIAL | https://aws.amazon.com/blogs/awsmarketplace/best-practices-receiving-accepting-distributing-private-offers-aws-marketplace/ |
| A112 | Linking AWS Partner Central and AWS accounts (prerequisites, FAQ); Managing subsidiary account connections | AWS Docs | fetched 2026-09-26 | OFFICIAL | https://docs.aws.amazon.com/partner-central/latest/getting-started/account-linking.html |
| A113 | What Is AWS MAP? How to Maximize Migration Credits in 2026 (Cody Slingerland) | CloudZero | updated 2026-05-15 | VENDOR | https://www.cloudzero.com/blog/aws-map/ |
| A114 | AWS Partner Funding: POC, MDF, ISV Workload, PIF (Sabrina Xie) | Suger | 2026-08-06 | VENDOR | https://www.suger.io/resources/blog/aws-partner-funding-programs/ |
| A115 | AWS Marketplace announces simplified and reduced listing fees for sellers | AWS What's New | 2024-01 | OFFICIAL | https://aws.amazon.com/about-aws/whats-new/2024/01/aws-marketplace-simplified-reduced-listing-fees/ |
| A116 | State of Cloud Marketplaces 2026 (Aein Eskandari) | Automatum | 2026-05-07 | VENDOR | https://www.automatum.io/blog-posts/state-of-cloud-marketplaces-2026 |
| A117 | AWS Marketplace introduces Tax management portal for sellers | AWS What's New | 2026-05-07 | OFFICIAL | https://aws.amazon.com/about-aws/whats-new/2026/05/aws-marketplace-tax/ |
| A118 | AWS Marketplace now supports programmatic procurement with Agreements API | AWS What's New | 2026-05-06 | OFFICIAL | https://aws.amazon.com/about-aws/whats-new/2026/05/aws-marketplace-agreements-api/ |
| A119 | AWS Marketplace introduces localized billing for Professional Services from AWS EMEA | AWS What's New | 2026-02-03 | OFFICIAL | https://aws.amazon.com/about-aws/whats-new/2026/02/aws-marketplace-localized-billing-professional/ |
| A120 | AWS Marketplace Listing Score: Basic to Top Tier, No Proven ROI | Beyond Co-Sell (YouTube) | 2026-09-15 | CREATOR | https://www.youtube.com/watch?v=ow_F1uCqfrA |
| A121 | AWS Partner Central agents now accelerate co-selling on every deal | AWS What's New | 2026-06-16 | OFFICIAL | https://aws.amazon.com/about-aws/whats-new/2026/06/accelerate-co-selling-with-agents/ |
| A122 | AWS Partner Central agents expand funding guidance to all programs | AWS What's New | 2026-07-20 | OFFICIAL | https://aws.amazon.com/about-aws/whats-new/2026/07/aws-partner-central/ |
| A123 | AppDirect advances its Everything Store strategy with Tackle.io acquisition | Omdia | 2025-12 | INDEPENDENT | https://omdia.tech.informa.com/blogs/2025/dec/appdirects-advances-its-everything-etore-strategy-with-tackleio-acquisition |
