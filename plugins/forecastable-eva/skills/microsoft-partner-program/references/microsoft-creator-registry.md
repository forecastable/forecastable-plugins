# Microsoft creator and source registry
Version: 2026.09 (built 2026-09-26). Walked monthly by the refresh task.
Rules: rank by usefulness to a partner team turning this hyperscaler into pipeline, not audience size.
Two consecutive empty checks move a creator to Dormant (checked quarterly). New creators need one
substantive, current, program-specific item and a stated reason. Label: OFFICIAL, VENDOR, INDEPENDENT,
CREATOR. "Last checked" is the date actually fetched.

Fetch notes for the refresh agent: partner.microsoft.com and www.microsoft.com use a Microsoft TLS ECC Root G2 chain; if WebFetch fails with a certificate error, fetch with curl using a CA bundle that appends the "Microsoft TLS ECC Root G2 - xsign" certificate (from www.microsoft.com/pkiops/certs/) to the proxy bundle. Microsoft Learn pages fetch cleanly (the `updated_at` meta tag gives the page date). Tech Community pages render client-side; use the board RSS feeds below, which include full post bodies. The FY27 incentives guide requires sign-in.

## Tier 0: official change feeds (check every month, first)

| # | Feed | What to extract | URL (and feed) | Last checked | Last new item |
|---|---|---|---|---|---|
| 0.1 | Partner Center announcements (monthly page) | Every dated change: co-sell, Marketplace, designations, benefits, incentives, CSP, API retirements. Highest-signal single source | https://learn.microsoft.com/en-us/partner-center/announcements/2026-september (pattern: /announcements/YYYY-month) | 2026-09-26 | 2026-09-25 ("new Copilot"); 2026-09-23 growth margin API | <!-- VALIDATE-OK[economics]: public hyperscaler or vendor reseller economics, not Forecastable's -->
| 0.2 | Monthly Microsoft AI Cloud Partner Program update (inside 0.1, Membership workspace) | Designation, specialization, certification retirements, badge changes | Same pages; search "Monthly Microsoft AI Cloud Partner Program update" | 2026-09-26 | 2026-08-13 |
| 0.3 | Frontier Accelerate for Marketplace docs | Tiers, eligibility, sponsorship policy, migration rules | https://learn.microsoft.com/en-us/partner-center/frontier-accelerate-marketplace/overview (and /faq, /grow/azure-sponsorship) | 2026-09-26 | 2026-09-16 |
| 0.4 | Co-sell requirements and status pages | Threshold changes (USD 100K), status names, emerging criteria | https://learn.microsoft.com/en-us/partner-center/referrals/co-sell-requirements ; /co-sell-status ; /register-deals | 2026-09-26 | 2026-08-18 (overview); requirements last 2025-09-25 |
| 0.5 | Marketplace transact capabilities (fees) and agency fee discount | Fee changes (3 percent, renewal 50 percent discount) | https://learn.microsoft.com/en-us/partner-center/marketplace-offers/marketplace-commercial-transaction-capabilities-and-considerations ; /agency-fee-discount-for-renewals | 2026-09-26 | 2026-08-18 |
| 0.6 | MPO and REO overview pages | Country list changes | https://learn.microsoft.com/en-us/partner-center/marketplace-offers/multiparty-private-offers-overview ; /resale-enabled-offers-overview | 2026-09-26 | 2026-07-22 (MPO), 2026-08-18 (REO) |
| 0.7 | Solutions Partner and certified software requirement pages | PCS thresholds, cert lists, CSD thresholds | https://learn.microsoft.com/en-us/partner-center/membership/partner-capability-score ; /membership/solutions-partner-azure ; /referrals/solutions-partner-certified-software-solution-area | 2026-09-26 | 2026-08-31 (Security) |
| 0.8 | Microsoft Partner blog | FY-level policy (MCAPS Start, Marketplace, incentives, Ignite) | https://partner.microsoft.com/en-us/blog (author pages below; no RSS confirmed) | 2026-09-26 | 2026-09-03 (Deggans) |
| 0.9 | Tech Community Marketplace blog (includes monthly Microsoft Marketplace Partner Digest, App Advisor guidance, partner guest posts) | New features, events, office hours, guest practitioner playbooks | https://techcommunity.microsoft.com/category/marketplace ; RSS https://techcommunity.microsoft.com/t5/s/gxcuf89792/rss/board?board.id=marketplace-blog | 2026-09-26 | 2026-09-25 |
| 0.10 | Tech Community Partner News (monthly "What's new for partners in Azure / Security / AI Business Solutions", MSP updates, partner blog mirrors) | Solution-area newsletters, co-sell skilling | RSS https://techcommunity.microsoft.com/t5/s/gxcuf89792/rss/board?board.id=partnernews | 2026-09-26 | 2026-09-25 |
| 0.11 | Microsoft AI Cloud Partner Program YouTube (@msPartner) | Program briefings (FAM briefing 2026-09-10), Titan Co-Sell Execution Engine series, benefits ROI | https://www.youtube.com/@msPartner ; RSS https://www.youtube.com/feeds/videos.xml?channel_id=UCsSMyUhJpfSsVw9KDw0XYlQ | 2026-09-26 | 2026-09-13 |
| 0.12 | Microsoft Tech Community YouTube (@MicrosoftTechCommunity), Marketplace office hours | Monthly Marketplace office hours (private offers, MPO, REO, channel playbooks) | https://www.youtube.com/@MicrosoftTechCommunity ; RSS https://www.youtube.com/feeds/videos.xml?channel_id=UCdaBIk_axiNLfdCCGWiHwgg | 2026-09-26 | ~2026-07 (MPO Australia office hour) |
| 0.13 | Microsoft Marketplace community (discussion board, office hours calendar) | Q&A with Microsoft staff; event calendar | https://aka.ms/community/marketplace | 2026-09-26 (via RSS) | 2026-09-21 digest |
| 0.14 | Microsoft Commercial Partner Incentives Guide (FY27) | Incentive rates, engagements, co-op guidance | https://incentiveguide.partner.microsoft.com/ (login required) | 2026-09-26 (shell only) | n/a (gated) |
| 0.15 | Azure IP co-sell resources collection | FY27 IP co-sell program guide, one-pager, FAQ | https://partner.microsoft.com/en-us/asset/collection/microsoft-azure-ip-co-sell-resources | 2026-09-26 (assets JS-rendered) | Collection modified 2026-08-11 |
| 0.16 | Frontier Accelerate partner sites (AI Business Solutions, Security) | Engagement lists, partner guides and FAQs | https://microsoftpartners.microsoft.com/abs/fa/ ; https://microsoftpartners.microsoft.com/Microsoft-Security-Partners/Frontier-Accelerate-for-Security/ | 2026-09-26 | 2026 FY27 content |
| 0.17 | Events | MCAPS Start for Partners on demand; FY27 GTM Kickoff; Microsoft Ignite (Nov 17 to 20, 2026) session catalog | https://events.microsoft.com/flow/microsoft/startpartners27/home/page/home ; https://microsoftpartners.microsoft.com/abs/gtm-event/ ; https://ignite.microsoft.com/ | 2026-09-26 (via blog links) | 2026-09-22 Ignite catalog live |
| 0.18 | Partner Skilling Hub | Partnering for Success Together (monthly, from 2026-09-23); Co-Sell Execution Engine series; Titan paths | https://www.skilling-hub.com/ ; https://www.skilling-hub.com/collection/co-sell-execution-engine-video-series | 2026-09-26 (via links) | 2026-09-23 |
| 0.19 | Mastering the Marketplace (Microsoft learning series on GitHub) | Offer-type technical how-tos, SaaS Accelerator | https://microsoft.github.io/Mastering-the-Marketplace/ | 2026-09-26 (search result) | not dated |
| 0.20 | Microsoft for Startups benefits | Credits tiers; Azure IP Co-sell Acceleration | https://learn.microsoft.com/en-us/startups/benefits ; /startups/benefits/gtm-benefits/azure-ipcs | 2026-09-26 | 2026-06-16 |

## Tier 1: primary creators (check every month)

| # | Creator | Role / affiliation | Label | Where to look (exact URLs) | Good for | Last checked | Last new item |
|---|---|---|---|---|---|---|---|
| 1 | Nicole Dezen | Chief Partner Officer and CVP, Global Channel Partner Sales, Microsoft | OFFICIAL | https://partner.microsoft.com/en-us/blog/author/nicole-dezen | FY-level program direction: MCAPS Start FY27 post (investments, co-sell stats, incentives framework), Marketplace launch, MPO expansion, Ignite recaps | 2026-09-26 | 2026-07-22 "MCAPS Start for Partners FY27: Powering Frontier Transformation together" |
| 2 | Heather Deggans | VP, Global Partner Go-To-Market, Programs, Operations, Microsoft | OFFICIAL | https://partner.microsoft.com/en-us/blog/author/heather-deggans | Where FY27 resources live (playbooks, co-op guide, Forrester TEI numbers, Core and Frontier conversations) | 2026-09-26 | 2026-09-03 "Back at your desk? Start FY27 with the resources that matter most" |
| 3 | Cyril Belikoff | VP, Commercial Cloud and AI, Microsoft | OFFICIAL | https://partner.microsoft.com/en-us/blog/author/cyril-belikoff ; Azure blog | Azure partner incentives lineage (Azure Accelerate to Frontier Accelerate for Azure), Azure GTM priorities; quoted on Marketplace-first co-sell | 2026-09-26 | 2026-09-02 "FY27 is the year to execute on AI" |
| 4 | Mira Ayad (NEW) | General Manager, Global Marketplace, Microsoft | OFFICIAL | https://partner.microsoft.com/en-us/blog/article/marketplace-business-priorities-fy27 (author page: https://partner.microsoft.com/en-us/blog/author/mira-ayad) | Marketplace strategy: MACC 100 percent match reaffirmed, channel activation, IP Co-sell Acceleration, 141 markets | 2026-09-26 | 2026-07-28 "Built to grow together: The FY27 Microsoft Marketplace opportunity" |
| 5 | Mason McCoy | Director of Partner Experiences, Microsoft (Marketplace) | OFFICIAL | https://partner.microsoft.com/en-us/blog/author/mason-mccoy | "Capturing the marketplace opportunity" series (parts 1 to 4, Feb to May 2025), channel ecosystem, Omdia profitability multiplier; co-sell best practices with quota-credit framing | 2026-09-26 | 2026-02-03 "Unlocking the profitability multiplier" (no newer post; watch) |
| 6 | Jason Rook | Microsoft Marketplace channel leader (hosts channel-led office hours and Ignite channel sessions) | OFFICIAL | Tech Community office hours on https://www.youtube.com/@MicrosoftTechCommunity ; Ignite 2025 channel session via https://www.youtube.com/watch?v=5iq8PPuXE1k ; campaign kit aka.ms/channel-led-ciab | MPO vs REO decision rules, channel campaign in a box, seller motivation for channel deals | 2026-09-26 | ~2026-06 "The Marketplace playbook for channel-led sales" (https://www.youtube.com/watch?v=_jdhmL3jgCk). Brief's "offer transfer" video not located |
| 7 | Reis Barrie | Founder and CEO, Carve Partners (Microsoft co-sell and Marketplace advisory) | VENDOR | https://techcommunity.microsoft.com/t5/marketplace-blog/four-things-leading-partners-teach-their-sellers-to-turn-a/ba-p/4552398 ; https://www.carvepartners.com/resources/understanding-the-azure-ip-co-sell-incentive-benefit ; Carve Partner Center guide https://carvepartners.com/partner-center-guide/ | Seller enablement for Marketplace co-sell (MACC discovery questions, CRM signals, incentive programs); Sept 10, 2026 Marketplace community session | 2026-09-26 | 2026-09-02 Tech Community post |
| 8 | Sabrina Xie | Suger (cloud marketplace platform) | VENDOR | https://www.suger.io/resources/blog/microsoft-ip-co-sell-how-it-works/ ; https://www.suger.io/resources/blog/ | IP co-sell mechanics, deal registration rules, FY27 changes | 2026-09-26 | 2026-08-18 "Microsoft IP co-sell: how it works" |
| 9 | Jason Matthew Smith | Tackle | VENDOR | https://tackle.io/blog/co-selling-with-microsoft/ ; Tackle YouTube https://www.youtube.com/@tackleio | Microsoft co-sell primer, MPO 101, Cloud GTM XP sessions | 2026-09-26 | 2026-04-17 update of "Co-selling with Microsoft" |
| 10 | Darren Sharpe (NEW) | Marketplace Partner Leader, Microsoft UK | OFFICIAL (personal channel) | https://www.youtube.com/@MarketplaceSharpe (RSS channel_id UC8u4kzNNr6kfuSbD5c-50kw) | REO and private offer operational walkthroughs in Partner Center, procurement-facing Marketplace webinars, UK and EMEA channel | 2026-09-26 | 2026-09-24 "The Modern Procurement Advantage for Public Sector Customers" |
| 11 | Microsoft Marketplace Partner Digest (NEW, recurring) | Monthly digest by Microsoft Marketplace team (posted by community staff) | OFFICIAL | Tech Community Marketplace blog (RSS 0.9); September 2026 edition https://techcommunity.microsoft.com/t5/marketplace-blog/microsoft-marketplace-partner-digest-september-2026/ba-p/4555004 | Monthly feature changes and upcoming office hours | 2026-09-26 | 2026-09-21 |

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
| 1 | Trunal Bhanse | Co-founder and CEO, Clazar | VENDOR | https://clazar.io/guides/co-selling-with-azure ; https://clazar.io/blog/azure-co-sell-vs-ip-co-sell-eligible-guide ; podcast ep. https://theultimatepartner.com/227-how-clazar-is-revolutionizing-cloud-gtm-amp-democratizing-access-for-all/ | Azure co-sell status ladder, operational co-sell practice (sub-4-hour referral response) | 2026-09-26 | Guide labelled 2026, updated after Nov 2025 (exact date not shown); author not attributed on page |
| 2 | Kevin Flitcroft (NEW) | Spektra Systems / SaaSify | VENDOR | https://techcommunity.microsoft.com/t5/marketplace-blog/from-co-sell-ready-to-closed-won-a-practical-playbook-for-your/ba-p/4554512 ; Oct 7, 2026 Marketplace community session | 90-day co-sell ready to closed-won framework, five co-sell KPIs, private offer timing | 2026-09-26 | 2026-09-17 |
| 3 | Samantha Ho (NEW) | Suger | VENDOR | https://www.suger.io/resources/blog/azure-marketplace-fy27-changes-for-isvs ; https://www.suger.io/resources/blog/what-is-a-macc-azure-committed-spend-explained | FY27 Marketplace changes for ISVs, MACC explainer, request private offer, custom contract lengths | 2026-09-26 | 2026-08-18 |
| 4 | Vince Menzione (NEW) | Host, Ultimate Partner podcast and YouTube | CREATOR | https://www.youtube.com/@ultimatepartner (RSS channel_id UCzf3hClCIz3TxeQdp2jUwLQ) ; https://theultimatepartner.com/ | Interviews with Microsoft Marketplace leaders (Mira Ayad, Erwin Visser) and distributors on REO, ASPX, agent stores | 2026-09-26 | 2026-09-21 episode; 2026-09-08 "The Agent 365 Announcement You Can't Afford to Miss" with Mira Ayad |
| 5 | Sian Herrington (NEW) | Noteworthy (Microsoft incentives consultancy) | VENDOR | https://noteworthy.support/news-and-insights/marketplace-funding-frontier-accelerate-fy27 ; https://noteworthy.support/news-and-insights/ | FY27 engagement amounts behind the gated incentives guide (assessment, migration, Build and Publish tiers, governance ratios) | 2026-09-26 | 2026-09-08 |
| 6 | Cloud Factory blog (Jacob V. Schaumann Schmidt) (NEW) | Cloud Factory (Nordic CSP distributor) | VENDOR | https://blog.cloudfactorygroup.com/posts/microsoft-fy27-partner-incentives-what-changed-and-how-to-get-paid-now ; https://blog.cloudfactorygroup.com/posts/fy27-kicks-in-every-partner-center-change-from-july-2026-that-moves-your-pipeline | CSP incentive changes (growth margins, rebate retirement), Partner Center change roundups | 2026-09-26 | 2026-07-19 | <!-- VALIDATE-OK[economics]: public hyperscaler or vendor reseller economics, not Forecastable's -->
| 7 | Jay McBain (NEW) | Chief Analyst, Omdia (formerly Canalys) | INDEPENDENT | Ignite 2025 channel session https://www.youtube.com/watch?v=5iq8PPuXE1k ; Omdia research cited by Microsoft (USD 163B marketplace by 2030; USD 300B partner services opportunity; 59 percent partner-funded transactions by 2030) | Market sizing, channel-led marketplace forecasts | 2026-09-26 | 2025-12-17 (session upload); Omdia commissioned study Dec 2025 |
| 8 | Justin Royal (NEW) | Community manager, Microsoft Marketplace community | OFFICIAL | https://aka.ms/community/marketplace ; office hours on @MicrosoftTechCommunity | Monthly office-hour schedule, Q&A routing | 2026-09-26 | ~2026-06 office hour host |
| 9 | Kyle Richardson and Zach Vote (NEW) | Microsoft MAICPP team, Frontier Accelerate for Marketplace owners | OFFICIAL | https://www.youtube.com/watch?v=htJsG9deae4 | FAM sponsorship amounts (USD 400K, 2.1M, 200K channel), migration cohorts, CSD criteria change Jan 1, 2027 | 2026-09-26 | 2026-09-10 briefing |
| 10 | Steve Thomas (NEW) | Director, Partner Programs and Experiences, Microsoft | OFFICIAL | https://partner.microsoft.com/en-us/blog/article/benefits-renewal (author page https://partner.microsoft.com/en-us/blog/author/steve-thomas) | Benefits packages changes, redemption process | 2026-09-26 | 2026-01-22 |
| 11 | Brady-B (App Advisor posts) (NEW) | Microsoft Marketplace team (Tech Community handle) | OFFICIAL | Tech Community Marketplace blog RSS (0.9) | App Advisor guidance for private offers, MPO, REO and negotiated deals | 2026-09-26 | 2026-09-25 "Scale repeatable channel sales with REO and App Advisor" |
| 12 | Maven Collective Marketing (NEW) | Microsoft partner marketing agency | VENDOR | https://mavencollectivemarketing.com/insights/blog/ ; https://mavencollectivemarketing.com/insights/media/ | FY playbook changes for partner marketers, Azure Accelerate to Frontier Accelerate lineage, list of Microsoft partner media | 2026-09-26 | 2026-08-18 update |

## Tier 3: diligence and critics (quarterly)

| # | Source | Label | Where | Good for | Last checked | Last new item |
|---|---|---|---|---|---|---|
| 1 | Channel Dive (Matt Ashare) | INDEPENDENT | https://www.channeldive.com/news/microsoft-marketplace-isv-partners-co-selling/825104/ | Independent reporting on policy shifts (Marketplace-first co-sell, one-year transition) | 2026-09-26 | 2026-07-13 |
| 2 | Redmond Channel Partner | INDEPENDENT | https://rcpmag.com/blogs/rcp-channel-briefing/2025/07/microsoft-azure-accelerate-launch.aspx | Channel press view of program consolidations | 2026-09-26 (search result) | 2025-07 |
| 3 | AI Cloud Partners guides | INDEPENDENT (unknown ownership; verify claims) | https://www.aicloudpartners.com/guides/microsoft-partner-program-roles.html ; /guides/microsoft-partner-incentives.html | Role descriptions (PDM, PTS, PMA), incentive explainers | 2026-09-26 | 2026-04-12 |
| 4 | WeTransact blog | VENDOR | https://www.wetransact.io/blog/fy26-microsoft-incentives-fast-track-to-1m-in-benefits-for-isvs | ISV incentive sequencing claims (quota relief at USD 100K MBS); treat as unverified | 2026-09-26 | FY26 (undated) |
| 5 | Pax8 blog | VENDOR | https://www.pax8.com/blog/microsoft-incentives-fy27-updates/ | CSP-side FY27 incentive interpretation | 2026-09-26 (search result) | 2026 |
| 6 | Work 365 | VENDOR | https://resources.work365apps.com/blog/microsoft-fy27-csp-incentives-whats-changing-for-partners | CSP billing and incentive changes | 2026-09-26 (search result) | 2026 |
| 7 | Partner1 | VENDOR | https://www.partner1.io/partner-blog/mcaps-start-2026-fy27-microsoft ; podcast https://www.partner1.io/podcast | MCAPS Start interpretation | 2026-09-26 (search result) | 2026-07 |
| 8 | Forrester TEI studies (Microsoft-commissioned) | INDEPENDENT (commissioned) | https://tei.forrester.com/go/microsoft/azureservicespartner2026/ | Azure services partner economics (SMB USD 23,278 vs 95,000; enterprise USD 3.0M vs 5.7M) | 2026-09-26 (via Deggans post) | 2026-06 |
| 9 | IDC (Steve White, Program VP Channels and Alliances) | INDEPENDENT (commissioned) | https://www.youtube.com/watch?v=BcBLxW6woh8 | Benefits package ROI assessment | 2026-09-26 | 2026-07-30 |

## Watchlist: new finds (promote after one more substantive item)

| Candidate | Label | Where | Why watch | First seen |
|---|---|---|---|---|
| Julie Sanford (VP GTM, Programs and Operations, Global Partner Solutions, per 2025 materials) | OFFICIAL (status uncertain) | https://ignite.microsoft.com/en-US/sessions/PBRK417 ; https://partner.microsoft.com/en-gb/blog/author/julie-sanford | Ignite 2025 co-sell session "Connect, Plan, Win" (PBRK417) and program session (PBRK415); a LinkedIn result shows a Stripe profile, so confirm she is still at Microsoft before promoting | 2026-09-26 |
| Microsoft Events YouTube (@events_msft) | OFFICIAL | https://www.youtube.com/@events_msft | Ignite Marketplace breakouts (for example BRK213 on Marketplace) | 2026-09-26 |
| Tackle Cloud GTM XP sessions | VENDOR | https://www.youtube.com/@tackleio | "How the Microsoft Marketplace drives channel-led cloud growth" (~2026-07) | 2026-09-26 |
| Carve Partners Partner Center guide | VENDOR | https://carvepartners.com/partner-center-guide/grow/criteria-azure-ip-co-sell-eligible/ | Step-by-step Partner Center guides | 2026-09-26 |
| Miguel Arcilla, "Learning in Public Journal" | CREATOR | https://blog.miguelarcilla.com/2025/08/22/Primer-Marketplace-Rewards.html | Marketplace Rewards primer (pre-FAM); check for FAM update | 2026-09-26 |
| Microsoft partner podcast series on Tech Community (for example Ep 37 on partner valuation) | OFFICIAL | https://techcommunity.microsoft.com/blog/partnernews/ep-37--how-microsoft-partners-can-maximize-valuation-in-2026-insights-from-tim-m/4504509 | Possible recurring Microsoft partner podcast; identify series name | 2026-09-26 |
| M365 FM Podcast, partner strategy category | CREATOR | https://www.m365.fm/categories/microsoft-strategy-partner-marketing/ | Microsoft partner strategy episodes | 2026-09-26 |
| Kevin Peterson, Anthony Robbins style Microsoft partner voices | n/a | Not verified in this pass | Brief suggested; no current program-specific item found | 2026-09-26 |
| Heather Gordon, Frontier Forward: Asia Edition | OFFICIAL | https://partner.microsoft.com/en-sg/blog/author/heather-gordon ; @msPartner series | Asia partner co-sell stories | 2026-09-26 |
| Microsoft Partner Center "Pitch Maker Agent" and ASPX content | OFFICIAL | Partner Center announcements | CSP-side seller tooling | 2026-09-26 |

## Discovery queries (run monthly, last 45 days)

1. Partner Center announcements current month page: search titles containing "co-sell", "Marketplace", "private offer", "designation", "specialization", "Frontier Accelerate", "incentive".
2. Tech Community RSS (marketplace-blog, partnernews): new posts by non-staff authors (guest practitioners) and any "Partner Digest".
3. YouTube search, upload date this month: "Microsoft Marketplace private offer", "multiparty private offer", "resale enabled offer", "Azure IP co-sell", "Frontier Accelerate for Marketplace".
4. YouTube channel RSS pulls: @msPartner, @MicrosoftTechCommunity, @MarketplaceSharpe, @ultimatepartner, @tackleio, @events_msft.
5. Web search: "Azure IP co-sell" FY27 OR "Marketplace-first" site:partner.microsoft.com OR site:techcommunity.microsoft.com.
6. Web search: "Frontier Accelerate" incentives FY27 engagement amounts (vendor analyses: Noteworthy, Cloud Factory, Pax8, Maven).
7. Web search: "Microsoft Marketplace" "MACC" OR "cloud consumption commitment" change 2026.
8. LinkedIn search (posts, past month): "Microsoft Marketplace" "co-sell" from Microsoft employees titled Marketplace, ISV, PDM; plus Reis Barrie, Jason Rook, Darren Sharpe, Mira Ayad.
9. Substack and Medium: "Microsoft co-sell" OR "Azure Marketplace" newsletter posts (for example Partner Insight, Inside Partnering).
10. Podcasts: "Microsoft partner" podcast episode co-sell OR marketplace (Ultimate Partner, Partner1, M365 FM, Tackle, Clazar).
11. Analyst: Omdia (Jay McBain) hyperscaler marketplace research; IDC channels and alliances; Forrester TEI Microsoft partner studies.
12. Events: Microsoft Ignite partner (PBRK) session list for November 2026; Marketplace community office hours calendar.

## Dormant

| Source | Reason | Last substantive item | Recheck |
|---|---|---|---|
| ISV Success pages and FAQs (Learn, partner.microsoft.com) | Program consolidated into Frontier Accelerate for Marketplace (September 2026) | 2026 pre-FAM | Quarterly, for migration notes only |
| Marketplace Rewards pages (Learn) | Consolidated into FAM; Learn page stale | 2026-07-23 | Quarterly |
| Azure Expert MSP pages | Program retiring (no new enrollments from 2026-09-15) | 2026-08-19 | Quarterly until January 2027 |
| Microsoft Inspire | Event discontinued; replaced by MCAPS Start for Partners | 2023 | None |

## Change log
- 2026-09-26: created from Alex's creator research brief plus this research pass. Verified: Nicole Dezen, Heather Deggans, Cyril Belikoff, Mason McCoy (last post 2026-02-03), Jason Rook, Reis Barrie, Sabrina Xie, Jason Matthew Smith, Trunal Bhanse (Clazar guide, author not attributed on page). Not located: Jason Rook "offer transfer" video. Uncertain: Julie Sanford (moved to watchlist). Added 12 new sources: Mira Ayad, Darren Sharpe, Microsoft Marketplace Partner Digest, Kevin Flitcroft, Samantha Ho, Vince Menzione, Sian Herrington (Noteworthy), Cloud Factory, Jay McBain (Omdia), Justin Royal, Kyle Richardson and Zach Vote (FAM briefing), Steve Thomas, Brady-B App Advisor posts, Maven Collective, plus Tier 0 feeds (Partner Center announcements, Tech Community RSS, @msPartner and @MicrosoftTechCommunity YouTube RSS, Skilling Hub, Mastering the Marketplace).
- 2026-09-26: Tackle, Clazar, Suger and WorkSpan deep-mined (blogs, guides, help centers, reports, YouTube transcripts) and added as Tier 1B.
