# AWS creator and source registry
Version: 2026.09 (built 2026-09-26). Walked monthly by the refresh task.
Rules: rank by usefulness to a partner team turning this hyperscaler into pipeline, not audience size.
Two consecutive empty checks move a creator to Dormant (checked quarterly). New creators need one
substantive, current, program-specific item and a stated reason. Label: OFFICIAL, VENDOR, INDEPENDENT,
CREATOR. "Last checked" is the date actually fetched.

Companion file: `aws-intelligence.md` (source tags [A1] to [A123]).

## Tier 0: official change feeds (check every month, first)

| # | Feed | What changes there | Exact URL | Feed / RSS | Last checked | Last new item |
|---|---|---|---|---|---|---|
| 0.1 | AWS What's New (filter for "Partner Central", "Marketplace", "Partner Revenue") | Launch announcements with dates; fastest signal for Partner Central agents, Marketplace fees, PRM | https://aws.amazon.com/about-aws/whats-new/recent/ | https://aws.amazon.com/about-aws/whats-new/recent/feed/ (verified 200 OK) | 2026-09-26 | 2026-09-09 (Marketplace request leads); 2026-09-01 (0% services fee in bundles) |
| 0.2 | AWS Partner Network (APN) Blog, Announcements category | Program changes (ISVA benefits, BOX, BVR, monthly Competency lists, awards) | https://aws.amazon.com/blogs/apn/category/post-types/announcements/ | https://aws.amazon.com/blogs/apn/feed/ (verified 200 OK) | 2026-09-26 | 2026-09-22 (Grow your services business through AWS Marketplace) |
| 0.3 | AWS Marketplace Blog | Seller features, private offers, Concurrent Agreements, SaaS integration guides | https://aws.amazon.com/blogs/awsmarketplace/ | https://aws.amazon.com/blogs/awsmarketplace/feed/ (verified 200 OK) | 2026-09-26 | 2026-06 (Concurrent Agreements upgrade guide) |
| 0.4 | Partner Central Getting Started Guide, Document history | Managed policies, console features, migration, channel management | https://docs.aws.amazon.com/partner-central/latest/getting-started/doc-history.html | none; diff page | 2026-09-26 | 2026-03-16 |
| 0.5 | Partner Central Sales Guide, Document history | ACE opportunity flow, agents, lead enrichment, RA IDs, deal sizing | https://docs.aws.amazon.com/partner-central/latest/sales-guide/doc-history.html | none; diff page | 2026-09-26 | 2026-06-30 (Revenue Attribution ID) |
| 0.6 | AWS Partner CRM Connector release notes | Salesforce connector versions, known issues, S3-to-API migration | https://docs.aws.amazon.com/partner-central/latest/crm/crm-connector-release-notes.html | none | 2026-09-26 | 2026-07-17 (v3.20) |
| 0.7 | Partner Central API Reference (Selling, Account, Benefits, Channel, Revenue Measurement, MCP server) | New API actions, quotas, MCP tools | https://docs.aws.amazon.com/partner-central/latest/APIReference/Welcome.html and https://docs.aws.amazon.com/partner-central/latest/selling-api/partner-central-mcp-server.html | TOC JSON: https://docs.aws.amazon.com/partner-central/latest/APIReference/toc-contents.json | 2026-09-26 | 2026-08-20 (MCP OAuth) |
| 0.8 | Partner Central Builder Guide | Solutions, FTR prerequisites, PSF | https://docs.aws.amazon.com/partner-central/latest/builder-guide/requesting-ftr.html | none | 2026-09-26 | 2026-06 (streamlined FTR) |
| 0.9 | PRM onboarding guide | Tagging, User Agent, Marketplace metering methods, FAQs | https://docs.aws.amazon.com/PRM/latest/aws-prm-onboarding-guide/getting-started.html | PDF: https://docs.aws.amazon.com/pdfs/PRM/latest/aws-prm-onboarding-guide/aws-prm-onboarding-guide.pdf | 2026-09-26 | 2026-04 (Marketplace metering) |
| 0.10 | AWS Marketplace Seller Guide (listing fees page and TOC) | Fees, private offers, CPPO, payment terms, AI-assisted listing | https://docs.aws.amazon.com/marketplace/latest/userguide/listing-fees.html | TOC JSON: https://docs.aws.amazon.com/marketplace/latest/userguide/toc-contents.json (doc-history page redirects in a loop; use TOC and What's New) | 2026-09-26 | 2026-09-01 (0% services in bundles) |
| 0.11 | ISV Accelerate program page | ISVA thresholds and benefits (verify monthly) | https://aws.amazon.com/partners/programs/isv-accelerate/ | none | 2026-09-26 | Thresholds as of 2026-09-26 |
| 0.12 | Services Partner Tiers page | Tier thresholds and fee | https://aws.amazon.com/partners/services-tiers/ | none | 2026-09-26 | n/a |
| 0.13 | AWS Specialization (Competencies) page | Competency list, Service Delivery/Ready deprecation (2027-06-01) | https://aws.amazon.com/partners/programs/competencies/ | none | 2026-09-26 | Deprecation notice live |
| 0.14 | Co-Sell with AWS page and ACE page | Co-sell program framing | https://aws.amazon.com/partners/co-sell-with-aws/ and https://aws.amazon.com/partners/programs/ace/ | none | 2026-09-26 | n/a |
| 0.15 | AWS Partner Network YouTube | Partner stories; occasional program explainers (for example PRM) | https://www.youtube.com/@AWSPartnerNetwork | https://www.youtube.com/feeds/videos.xml?channel_id=UC5jiGyfEcnFJNjtyS40c3Zg | 2026-09-26 | 2026-09-24 (HCLTech on Partner Revenue Measurement with Brian Bohan, AWS) |
| 0.16 | AWS Events YouTube (re:Invent partner sessions, Partner Summit) | Session recordings, PEX/PRT tracks | https://www.youtube.com/@AWSEventsChannel | https://www.youtube.com/feeds/videos.xml?channel_id=UCdoadna9HFHsxXWhafhNvKw | 2026-09-26 | not checked for partner items |
| 0.17 | re:Invent 2026 | Main annual partner announcements | https://aws.amazon.com/events/reinvent/ | none | 2026-09-26 | Event November 30 to December 4, 2026 |
| 0.18 | AWS re:Post (Partner Central, Marketplace tags) | Practitioner Q&A, AWS staff answers on fees and APN renewals | https://repost.aws/ (search "Partner Central", "APN fee", "AWS Marketplace seller") | per-tag RSS on re:Post | 2026-09-26 | not walked this cycle |
| 0.19 | Omdia AWS Partner Ecosystem Multiplier reports (hosted by AWS) | Services multiplier ($7.13 per $1 in 2025) and revenue timing | https://aws.amazon.com/resources/analyst-reports/omdia/global-whitepaper-ardm-25-partner-ecosystem-multiplier-the-aws-opportunity | none | 2026-09-26 | 2025-12 global; 2026 APJ edition exists |
| 0.20 | Login-gated (cannot be fetched, check manually) | Partner Funding Benefits Guide, MDF Guide, ACE FAQ, ISVA program guide, Partner Scorecard | Partner Central (console) > Guides | n/a | n/a | n/a |

## Tier 1: primary creators (check every month)

| # | Creator | Role / affiliation | Label | Where to look (exact URLs) | Good for | Last checked | Last new item |
|---|---|---|---|---|---|---|---|
| 1 | Andrew Morris and Michael Musselman (Beyond Co-Sell) | Morris: AWS Marketplace expert, author of "ALIGNED: The Playbook for Accelerating AWS Partnerships". Musselman: co-founder Partner Cloud Alliance Network (PCAN), ex-Lacework alliances | CREATOR | YouTube https://www.youtube.com/@beyondcosell (RSS https://www.youtube.com/feeds/videos.xml?channel_id=UCWTcJxEYlfX0DE1bAVpIKCw); LinkedIn https://www.linkedin.com/in/andrewmorris and https://www.linkedin.com/in/michaelmusselman; PCAN https://www.pcan.cloud/ | Ground truth on how ACE Opportunity Quality Score and co-sell motions behave in practice; PPA/SCA negotiation; Marketplace incrementality; listing-score skepticism | 2026-09-26 | 2026-09-15 "AWS Marketplace Listing Score: Basic to Top Tier, No Proven ROI" |
| 2 | Sabrina Xie (Suger) | Content lead at Suger, a Marketplace/co-sell integration vendor | VENDOR | Author page https://www.suger.io/resources/blog/author/sabrina-xie/ ; blog https://www.suger.io/resources/blog/ | Current, dated, source-linked explainers: Partner Central migration, Software Path, funding programs, ACE leads | 2026-09-26 | 2026-09-24 "AWS Partner Central Leads from Salesforce Accounts" |
| 3 | Jen Letourneau (AWS) | Global Leader, Partner Journey, AWS | OFFICIAL | APN Blog https://aws.amazon.com/blogs/apn/get-ready-to-sell/ ; APN blog author search | Onboarding changes (registered to ready-to-sell agents, FTR streamlining, List and Sell) | 2026-09-26 | 2026-06-16 "New agentic capabilities to take you from registered to ready-to-sell in days" |
| 4 | Cara Bohmann (AWS) with Charlene Vela, Eduardo Estrada, Patricia Kim | Sr. Co-Sell Initiative Managers, AWS | OFFICIAL | https://aws.amazon.com/blogs/apn/new-aws-isv-accelerate-benefits-unlock-the-co-sell-advantage/ | ISV Accelerate benefit changes (MDF, workshops) | 2026-09-26 | 2026-03-16 "New AWS ISV Accelerate benefits: Unlock the co-sell advantage" |
| 5 | Tom Thayer (AWS) and Partner Central product team (Nicole Schreiber, Prachi Bhopatkar, Raj Kandaswamy) | Partner Central agents product leads | OFFICIAL | https://aws.amazon.com/blogs/apn/sell-smarter-with-aws/ ; https://aws.amazon.com/blogs/apn/introducing-aws-partner-central-agents/ | Opportunity Quality Score, co-sell motions, lead propensity, MCP server | 2026-09-26 | 2026-06-16 "Sell smarter with AWS" |
| 6 | Jen Dawson (SaaSNova) | Founder and CEO, SaaSNova; host of The Jen GTM Show | CREATOR | Show https://www.saasnova.ai/show ; YouTube https://www.youtube.com/@SaaSNovaGTM ; newsletter "The Nova Brief" https://www.saasnova.ai/newsletter | Why listings do not create pipeline; field dynamics; ISV visibility to AWS | 2026-09-26 | Episode 7 "Why Your AWS Listing Isn't Generating Pipeline" (date not shown on page); interview on Inside Partnering 2026-02-03 |
| 7 | Trunal Bhanse (Clazar) | CEO, Clazar; host of Clazar Podcast | VENDOR | Guide https://clazar.io/guides/co-selling-with-aws ; report https://clazar.io/blog/state-of-cloud-marketplace-and-co-sell-report-insights ; podcasts https://clazar.io/podcasts ; YouTube https://www.youtube.com/@GetClazar | Survey data on marketplace revenue share and co-sell cadence; how-to guides | 2026-09-26 | 2025-04-24 State of Cloud Marketplaces and Co-Sell report (guides updated 2026, undated) |
| 8 | Chris Grusz (AWS) | Managing Director, Technology Partnerships (AWS Marketplace and ISV), AWS | OFFICIAL | theCUBE interviews (YouTube search "Chris Grusz"); LinkedIn https://www.linkedin.com/in/chris-grusz-03b855/ ; Tidemark Platform Journey ep. 12 https://theplatformjourney.tidemarkcap.com/episodes/12-chris-grusz-of-aws-the-powerhouse-marketplace | Marketplace strategy direction straight from the business owner; re:Invent framing | 2026-09-26 | re:Invent 2025 theCUBE interview with Snowflake (about 2025-12) |
| 9 | Chris Buckel (flashdba) | Independent writer on hyperscaler GTM | INDEPENDENT | https://flashdba.com/hyperscaler-gtm/co-sell/aws/ | Clear model of ACE, ISVA, seller quota, specialization renewals | 2026-09-26 | 2026-06-17 (reviewed 2026-09-02) |

## Tier 1B: Cloud GTM vendors (deep-mined 2026-09-26, check every month)

Full profiles, extracted facts, conflicts, content inventories and per-vendor people and discovery
queries: `vendors/{tackle,clazar,suger,workspan}-intelligence.md`; comparison in `vendors/cloud-gtm-vendors.md`.
Every claim is VENDOR and is checked against this cloud's intelligence file before use.

| # | Vendor | Label | Where to look | Good for | Last checked | Last new item |
|---|---|---|---|---|---|---|
| V1 | Tackle (AppDirect) | VENDOR | https://tackle.io/blog/ ; https://tackle.io/sitemap.xml ; help center ; YouTube https://www.youtube.com/@tackleio (Cloud GTM XP sessions) ; State of Cloud GTM report | Hyperscaler executive talks, survey data, rep-led co-sell patterns | 2026-09-26 | 2026-09 (blog) |
| V2 | Clazar | VENDOR | https://clazar.io/blog ; https://clazar.io/guides ; https://help.clazar.io ; https://clazar.io/podcasts ; YouTube (search Clazar) | Help-center rule detail, AWS credits, Microsoft deal registration checks, MCP server | 2026-09-26 | 2026-09-11 (blog) |
| V3 | Suger | VENDOR | https://www.suger.io/resources/blog/ ; https://www.suger.io/sitemap.xml ; guides ; YouTube @suger-io | Near-daily edge cases, OQS data, private offer failures, PDM webinars | 2026-09-26 | 2026-09 (near daily) |
| V4 | WorkSpan | VENDOR | https://www.workspan.com/blog ; https://www.workspan.com/sitemap.xml ; https://support.workspan.com ; YouTube (WorkSpan, Partner Signal Live) | AWS deadline notices, Microsoft field-comp quotes, rejection-message checklist, HubSpot referral sync | 2026-09-26 | 2026-09 |

## Tier 2: specialists (monthly, expect gaps)

| # | Creator | Role / affiliation | Label | Where to look | Good for | Last checked | Last new item |
|---|---|---|---|---|---|---|---|
| 10 | Tyler Althoff (AWS) | Sr. Partner Business Development Manager, AWS | OFFICIAL | https://aws.amazon.com/blogs/apn/best-practices-for-developing-an-aws-co-sell-program/ ; https://aws.amazon.com/blogs/apn/how-aws-partners-can-optimize-gtm-strategy-with-the-co-sell-development-framework/ | Co-sell program design (Educate, Enable, Engage; enablement and mapping ratios) | 2026-09-26 | 2023-09-21 (evergreen; no newer post found, candidate for Dormant) |
| 11 | Soumya Vanga (AWS) | AWS Marketplace solutions architect | OFFICIAL | https://aws.amazon.com/blogs/awsmarketplace/best-practices-receiving-accepting-distributing-private-offers-aws-marketplace/ | Buyer-side private offer mechanics (management vs member accounts, License Manager distribution) | 2026-09-26 | 2023-07-28 (evergreen; no newer post found) |
| 12 | Kaley Edmonds (Tackle) | Cloud GTM Coach, Tackle | VENDOR | https://tackle.io/blog/how-to-achieve-aws-saas-co-sell-benefit-and-maximize-co-sell-success/ ; LinkedIn https://www.linkedin.com/in/kmedmonds | SaaS Co-Sell Benefit steps and requirements | 2026-09-26 | 2025-04-24 |
| 13 | Tackle (company content; acquired by AppDirect, reported December 2025) | Marketplace and co-sell platform | VENDOR | Blog https://tackle.io/blog/ ; reports https://tackle.io/resources-category/reports/ ; State of Cloud GTM 2025 https://state-of-cloud-gtm-report-2025.tackle.io/ ; YouTube https://www.youtube.com/@tackleio | Annual State of Cloud GTM survey (committed spend, PDM access, channel share); monthly product updates reveal AWS feature timing | 2026-09-26 | 2026-03-18 March product updates; 2025-12-17 State of Cloud GTM 2025 |
| 14 | Samhita Suresh (Labra) | Content, Labra | VENDOR | https://labra.io/aws-partner-programs-guide/ ; https://labra.io/aws-reinvent-2025-recap/ ; help center https://helpcenter.labra.io/ | Program roundups and re:Invent recaps; ACE eligibility help articles | 2026-09-26 | 2026-03-02 "The Complete Guide to AWS Partner Programs in 2026" |
| 15 | Shirley Guo and Stacy Wu (Suger) | Suger content | VENDOR | https://www.suger.io/resources/blog/ | Fee math, EDP drawdown sourcing, Seller Prime | 2026-09-26 | 2026-08-06 "What a Marketplace Dollar Actually Costs You" |
| 16 | Amit Sinha (WorkSpan) | WorkSpan | VENDOR | https://www.workspan.com/blog/free-aws-partner-console-migration ; API guide https://support.workspan.com/hc/en-us/articles/47607948575379-AWS-Partner-Central-3-0-API-Guide | Partner Central 3.0 migration and API change impact (note: claimed June 30, 2026 deadline conflicts with AWS) | 2026-09-26 | 2025-11-30 |
| 17 | Omdia (Alastair Edwards, Peter Bryant; Canalys now part of Omdia) | Analyst firm | INDEPENDENT | https://omdia.tech.informa.com/blogs/2026/jan/aws-launches-its-partners-into-the-era-of-ai-at-reinvent-2025 | Partner Ecosystem Multiplier, re:Invent partner analysis, incentive restructuring (New Customer Incentives), Tackle acquisition | 2026-09-26 | 2026-01-09 |

## Tier 3: diligence and critics (quarterly)

| # | Creator | Role / affiliation | Label | Where to look | Good for | Last checked | Last new item |
|---|---|---|---|---|---|---|---|
| 18 | Corey Quinn (Duckbill) | Cloud economist | INDEPENDENT | https://www.duckbillhq.com/blog/new-aws-marketplace-rules/ ; newsletter Last Week in AWS | Critical read on Marketplace commit rules ("Deployed on AWS") | 2026-09-26 | 2025-10-29 update |
| 19 | nOps | FinOps vendor | VENDOR | https://www.nops.io/blog/aws-saas-marketplace-policy-changes-for-may-2025/ | Buyer-side view of commit retirement history (50% to 100% to deployed-on-AWS) | 2026-09-26 | 2025-04-03 |
| 20 | Automatum (Aein Eskandari) | Marketplace vendor | VENDOR | https://www.automatum.io/blog-posts/state-of-cloud-marketplaces-2026 | Cross-cloud GMV context | 2026-09-26 | 2026-05-07 |
| 21 | Working Backwards / Amazon operating cadence writers | Ex-Amazon authors | INDEPENDENT | https://workingbackwards.com/concepts/amazon-operating-cadence/ | OP1/OP2 timing for planning asks to AWS | 2026-09-26 | undated evergreen |

## Watchlist: new finds (promote after one more substantive item)

| # | Creator | Label | Where | Why added | First item | Last checked |
|---|---|---|---|---|---|---|
| W1 | Roman Kirsanov, Partner Insight newsletter | CREATOR | https://newsletter.partnerinsight.io/ | Seller-comp neutrality and ACE submission quality advice tied to AWS | 2025-11-18 "7 Seller Coaching Tactics to Convert $531B Cloud Commits" | 2026-09-26 |
| W2 | Chip Rodgers, Inside Partnering (Substack) | CREATOR | https://insidepartnering.substack.com/ | Long-form interviews with AWS-focused operators (Jen Dawson) | 2026-02-03 | 2026-09-26 |
| W3 | Juhi Saha, Partner1 | VENDOR | https://www.partner1.io/partner-blog/ | Partner-side re:Invent recaps | 2025-12-18 re:Invent 2025 recap | 2026-09-26 |
| W4 | Todd R. Weiss, ChannelE2E | INDEPENDENT | https://www.channele2e.com/ | Channel press coverage of AWS partner strategy (BVR Competency MDF) | 2026-06-29 | 2026-09-26 |
| W5 | PartnerCloud YouTube | CREATOR | https://www.youtube.com/@partnercloud | Explainer channel on AWS partner programs and funding; tiny audience, verify substance | Channel found 2026-09-26 | 2026-09-26 |
| W6 | Brian Bohan (AWS), Director Partner Strategy and Growth | OFFICIAL | https://www.youtube.com/watch?v=KB1Ruz2noDY | PRM strategy from AWS side | 2026-09-24 HCLTech PRM conversation | 2026-09-26 |
| W7 | Nikolay Nikolaev (Nascent, ex-Progress) | CREATOR | Beyond Co-Sell guest; LinkedIn | ACE Quality Score reverse-engineering (five-part submission) and incrementality data | 2026-08-18 | 2026-09-26 |
| W8 | Invisory blog | VENDOR | https://invisory.co/resources/blog/ | ISVA and Marketplace incentive explainers | 2025-04-15 update | 2026-09-26 |
| W9 | Pete Goldberg (via Clazar Podcast) | CREATOR | https://clazar.io/podcasts | Ex-AWS alliances view on "earned not given" co-sell and back-office readiness | 2024-03-28 (old; needs a current item) | 2026-09-26 |

New additions this pass (not in Alex's brief): Tom Thayer and the Partner Central product team; Chris Buckel (flashdba); Kaley Edmonds; Tackle State of Cloud GTM; Samhita Suresh (Labra); Shirley Guo and Stacy Wu (Suger); Amit Sinha (WorkSpan); Omdia analysts; Corey Quinn (Duckbill); nOps; Automatum; Roman Kirsanov; Chip Rodgers; Juhi Saha; Todd Weiss; Brian Bohan; Nikolay Nikolaev; plus Tier 0 feeds (What's New RSS, APN and Marketplace blog RSS, doc histories, CRM release notes, APN YouTube RSS).

## Discovery queries (run monthly, last 45 days)

1. Web: `site:aws.amazon.com/about-aws/whats-new/2026 "Partner Central"` and `site:aws.amazon.com/about-aws/whats-new/2026 "AWS Marketplace"` (swap year as needed).
2. Web: `"ISV Accelerate" 2026 requirements OR benefits -site:aws.amazon.com` (catch vendor reads of changes).
3. Web: `"Opportunity Quality Score" AWS ACE` (practitioner experience with scoring and motions).
4. Web: `"Partner Revenue Measurement" OR "Revenue Attribution ID" AWS partner` (PRM adoption stories and gotchas).
5. YouTube (TranscriptAPI search_youtube, upload_date=month): `AWS co-sell ACE`, `AWS Marketplace private offer`, `AWS Partner Central agents`.
6. YouTube channel RSS: @beyondcosell, @AWSPartnerNetwork, @SaaSNovaGTM, @tackleio, @GetClazar.
7. LinkedIn (manual): posts by Andrew Morris, Michael Musselman, Jen Dawson, Kaley Edmonds; search "ISV Accelerate" and "ACE score" sorted by latest.
8. Substack/Medium: `AWS Marketplace co-sell substack 2026`, `AWS partner central medium 2026`.
9. Podcasts: `"AWS Marketplace" podcast episode 2026` (Clazar Podcast, The Jen GTM Show, Partnership Leaders, Tackle Cloud GTM content).
10. Events: `re:Invent 2026 partner session PEX` and AWS Summit partner keynote recaps (November to December priority).
11. Analyst: `Omdia AWS partner ecosystem 2026`, `Canalys AWS co-sell study`, `Forrester AWS Marketplace TEI`.
12. re:Post: search "APN fee", "Partner Central migration", "Marketplace seller disbursement" sorted by newest.

## Dormant

| Creator | Reason | Recheck |
|---|---|---|
| (none yet) | Althoff (#10) and Vanga (#11) have no post newer than 2023; move to Dormant after the next empty check | 2026-10 |

## Change log

- 2026-09-26: created from Alex's creator research brief plus this research pass. Verified: Beyond Co-Sell (active, weekly), Sabrina Xie (active, weekly), Jen Letourneau (2026-06-16 post), Cara Bohmann (2026-03-16 post), Jen Dawson (show live; dates not on page), Trunal Bhanse (report 2025-04-24), Chris Grusz (re:Invent 2025 interview), Tyler Althoff and Soumya Vanga (posts real but 2023). Added 17 new creators and 20 Tier 0 feeds.
- 2026-09-26: Tackle, Clazar, Suger and WorkSpan deep-mined (blogs, guides, help centers, reports, YouTube transcripts) and added as Tier 1B.
