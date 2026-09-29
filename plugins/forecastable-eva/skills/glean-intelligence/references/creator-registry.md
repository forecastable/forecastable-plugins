# Glean creator registry

Version: 2026.09 (built 2026-09-26). Updated monthly by the `glean-intelligence-refresh` task.

Purpose: the list of people and organizations whose Glean content feeds `glean-intelligence.md`, what
each is good for, where to look for new material, and when it was last checked. The monthly refresh
walks this file top to bottom, then runs the discovery queries at the end to add new creators.

Rules for this file:

- Rank by usefulness to a Glean admin or a revenue team using Glean, not by audience size.
- A creator stays on the list only while it publishes Glean-specific substance. Two consecutive empty
  checks move it to Dormant. Dormant creators are checked quarterly, not monthly.
- A new creator is added only with at least one substantive Glean-specific item and a stated reason.
- Label bias on every row: VENDOR, PARTNER, INDEPENDENT, COMPETITOR.
- "Last checked" is the date the refresh actually fetched the source, not the date it was listed.

## Tier 1: primary sources (check every month)

| # | Creator | Label | Where to look | Good for | Last checked | Last new item |
|---|---|---|---|---|---|---|
| 1 | Glean docs | VENDOR | https://docs.glean.com/llms.txt (full index, about 1,430 pages); https://docs.glean.com/release-notes/ ; Glean Docs MCP https://docs.glean.com/mcp | Ground truth for every setting, limit, role, connector, MCP and pricing fact | 2026-09-26 | 2026-09-24 (Flex pricing page) |
| 2 | Glean blog, product drops and press | VENDOR | https://www.glean.com/blog ; monthly "drop" posts (e.g. /blog/mcp-mar-drop-2026) ; /press | Launches, benchmarks, customer numbers, partner program | 2026-09-26 | 2026-09-02 (enterprise context post) |
| 3 | Glean YouTube (@gleanwork) | VENDOR | https://www.youtube.com/@gleanwork/videos (about 300 videos, 8.3K subs) | Glean:GO sessions, monthly drops, webinars (Token Economy, Managing AI, Skills) | 2026-09-26 | 2026-09 (Glean:GO sessions) |
| 4 | Arvind Jain (CEO) interviews | VENDOR on host channels | Search YouTube and podcasts for "Arvind Jain" monthly (Canva Prompted, Composio, TechCrunch Equity, Greylock, FirstMark MAD, 20VC) | Strategy, architecture, agent sprawl, token economics, open models | 2026-09-26 | 2026-09 (Canva Prompted, Composio) |
| 5 | Alchemy Technology Group | PARTNER | https://alchemytechgroup.com/blog ; https://www.youtube.com/@alchemytechgroup | Deployment failure modes, permission hygiene, pilot design, cost tiering, custom connectors | 2026-09-26 | 2026-09-24 (Glean:GO recap) |
| 6 | KK Ashisuto | PARTNER | https://www.ashisuto.co.jp/glean_blog/ (Japanese; translate) | Hard adoption numbers from a 1,300-person customer-zero; builder governance | 2026-09-26 | 2026-09-04 (Glean Memory) |
| 7 | AHEAD | PARTNER | https://www.ahead.com/resources/ ; /news/ | Training-gated licensing, champion network charters, maturity model | 2026-09-26 | 2026-08-27 (award) |
| 8 | Crossbeam product updates and help center | PARTNER | https://www.crossbeam.com/product-updates ; https://help.crossbeam.com (search "MCP", "Glean") | Crossbeam MCP clients, tools, credits; the Crossbeam plus Glean path | 2026-09-26 | 2026-09-01 (MCP server) |

## Tier 2: specialist and ecosystem (check every month, expect gaps)

| # | Creator | Label | Where to look | Good for | Last checked | Last new item |
|---|---|---|---|---|---|---|
| 9 | EggNest.ai | PARTNER | https://www.eggnest.ai (services, press) | Service ladder (Assess, Launch, Expand), custom connector scope | 2026-09-26 | 2026-02-04 |
| 10 | Databricks | PARTNER | Data + AI Summit sessions; https://docs.databricks.com/aws/en/ingestion/lakeflow-connect/glean | Structured vs unstructured routing, Genie, exporting Glean Insights | 2026-09-26 | 2026-09-22 (Lakeflow doc) |
| 11 | Arize AI | INDEPENDENT host | Arize Observe talks on YouTube | Agent evals, production trust, permissions stories from Glean engineers | 2026-09-26 | 2026-07-01 |
| 12 | Carahsoft | PARTNER | https://www.carahsoft.com/glean | Public sector framing; gated Glean PDFs | 2026-09-26 | undated |
| 13 | Cloud Ace | PARTNER | https://www.youtube.com/@cloudace ; https://cloud-ace.jp/service/glean/ | Hands-on tests (Japanese) | 2026-09-26 | 2026-07 |
| 14 | Gartner (Darin Stewart, Jed Cawthorne) | INDEPENDENT | https://www.gartner.com/en/documents (search Glean); Peer Insights | CIO framing; free abstracts; user likes and dislikes | 2026-09-26 | 2026-08-28 |
| 15 | Forrester | VENDOR-commissioned | https://tei.forrester.com/go/Glean/workAIplatform/ | ROI framework only (dated 2024) | 2026-09-26 | 2024-09 |
| 16 | FirstMark MAD, Greylock, TechCrunch Equity, Canva Prompted, Composio | INDEPENDENT hosts | Their YouTube channels | Long-form Glean executive interviews | 2026-09-26 | 2026-09 |
| 17 | NVIDIA | PARTNER | https://blogs.nvidia.com (search Glean, Nemotron) | Open models, Waldo | 2026-09-26 | 2026-07-14 |
| 18 | Deloitte | PARTNER | Glean:GO sessions; press room | Operating-model framing; no Glean alliance content found | 2026-09-26 | 2026-09-01 (fireside, no transcript) |
| 19 | Bain & Company | INDEPENDENT | https://www.bain.com/insights/ | Agent factory and AI-native frameworks (no Glean mentions) | 2026-09-26 | 2026-08-06 |

## Tier 3: buyer diligence and critics (check quarterly unless something breaks)

| # | Creator | Label | Where | Good for | Last checked |
|---|---|---|---|---|---|
| 20 | Vendr, Sentra/Metronome | INDEPENDENT | vendr.com/marketplace/glean ; sentra.app/articles/glean-pricing | Price benchmarks | 2026-09-26 |
| 21 | G2, AWS Marketplace reviews | INDEPENDENT | g2.com ; aws.amazon.com/marketplace reviews | Real complaints | 2026-09-26 |
| 22 | DiscoverAI, SaaS Expert, Cybernews | INDEPENDENT | review articles | Buyer checklists, who should not buy | 2026-09-26 |
| 23 | Guru, Moveworks/ServiceNow, GoSearch | COMPETITOR | comparison blogs | Tests easy to miss in demos | 2026-09-26 |
| 24 | Caylent | PARTNER | caylent.com/blog | Architecture partner; almost no Glean content | 2026-09-26 |

## Watchlist: new creators found 2026-09-26 (promote after one more substantive item)

| Creator | Label | URL | Why |
|---|---|---|---|
| Generation Digital (gend.co) | PARTNER | https://www.gend.co/blog | Recurring Glean feature explainers: Insights chat, Admin chat, autonomous agents, sales agents |
| Glean Community | VENDOR community | https://community.glean.com | Real admin questions; timelines; mine monthly |
| gleanwork GitHub | VENDOR | https://github.com/gleanwork/claude-plugins ; /indexing-api-connectors | Canonical MCP tool names and Claude setup |
| Knostic | security vendor | https://www.knostic.ai/blog/glean-data-security | "Can access" vs "need to know"; red-team prompts |
| Bridge IT Consulting | PARTNER | https://www.bridgeitconsulting.com/insights | Published custom connector build notes |
| WWT | PARTNER | https://www.wwt.com/blog/why-wwt-for-glean | Large integrator practice; "20 primary use cases" |
| JOURN3Y (Australia) | PARTNER | https://www.journ3y.com.au/platforms/glean | APAC partner; marketing stats unverified |
| The Ravit Show | INDEPENDENT | https://www.theravitshow.com | Glean:GO feature status labels |
| Ken Yeung, The Letter Two | INDEPENDENT | https://thelettertwo.com | Keynote live blogs (fetch was rate limited) |
| StackOne | COMPETITOR-adjacent | https://www.stackone.com/blog/best-mcp-gateway-for-glean/ | MCP host coverage and action gaps |
| Nightfall AI | security vendor | https://www.nightfall.ai/blog | DLP framing for Glean plus agent hosts |
| Spinach.ai | vendor | https://www.spinach.ai/blog/glean-agents-conversation-data-spinach | Meeting data into Glean agents |
| Basis | PARTNER | AWS Marketplace listing | Packaged implementation offer |
| Inco (LATAM), Softcat (EMEA) | PARTNER | glean.com/blog/2026-glean-partner-award-winners | Regional partners of the year; no content checked yet |

## Discovery queries (run every month, last 45 days only)

1. `"Glean" admin OR deployment OR rollout OR connector -job -hiring` (web, news)
2. `"Glean" agents OR "agent builder" OR "Glean MCP" site:linkedin.com/pulse OR site:medium.com OR site:substack.com`
3. YouTube search: `Glean enterprise AI`, `Glean agents tutorial`, `Glean MCP Claude`, `Glean admin`
4. `"Glean" Crossbeam OR "co-sell" OR "partner ecosystem" OR PRM`
5. `"Glean" Salesforce OR HubSpot agent revenue team`
6. `site:community.glean.com` newest threads
7. Glean partner directory (partners.glean.com) for newly accredited partners that publish content
8. `"Glean:GO"` or Glean event names for new session recordings

Promotion rule: a watchlist creator moves to Tier 2 after two substantive Glean-specific items within
six months, or one item that changes an admin recommendation.

## Dormant

None yet.

## Change log

- 2026-09-26: registry created from the 25-creator research brief plus three research passes (official,
  implementation partners, analysts and ecosystem). 24 ranked creators, 14 on the watchlist.
