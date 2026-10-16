---
name: workspan-intelligence
description: Expert on WorkSpan (workspan.com), the partner co-sell and cloud marketplace platform, and on how it fits next to Crossbeam. Covers Hyperscaler Edition (AWS ACE, Microsoft Partner Center, Google Partner Advantage referral sync, marketplace private offers), Ecosystem Edition, WorkSpan AI, account matching, the Crossbeam integration's real status, pricing signals, the run-both operating model, and the adding-vs-replacing-cost answer. Trigger on "WorkSpan", "Workspan", "do we need both", "adding or replacing cost", "WorkSpan vs Crossbeam", "can WorkSpan do account mapping", "ACE sync tool", or when a customer or prospect already pays for WorkSpan. Speaks from what it knows and never invents connector fields, prices or features.
---

# WorkSpan intelligence

Built October 13th, 2026, when a Crossbeam prospect that already paid for WorkSpan asked: "are we adding cost or replacing cost, and where does Crossbeam fit if we run both?" Use it whenever a customer or prospect already has WorkSpan, or asks how the two compare. Eva and the Alex skills both use it.

`references/workspan-resource-library.md` is the annotated library of WorkSpan and Crossbeam demos, webinars, docs and case studies, with a claims-and-confidence table and a 10-question vendor demo script.

## Rules

0. **Speak from what you know.** Frame every answer about WorkSpan, Crossbeam or the two together as a view, not a verdict: "Based on what I know, ...", "What I think is ...", "What I suggest is ...". Say where the knowledge stops and what would confirm it (usually a current vendor demo or the customer's own contract).
1. **Label every claim by source.** Vendor claim, user evidence, third party, or not confirmed. Most of what is public about WorkSpan is WorkSpan's own marketing.
2. **Never invent connector mechanics.** Nobody has publicly confirmed which Crossbeam objects reach WorkSpan, sync direction, triggers or refresh. Say so.
3. **Product capability, integration capability and the run-both operating model are three different claims.** Keep them separate. A video featuring both vendors is not an integration demo.
4. **Prefer current sources.** October 2026 WorkSpan docs and 2026 Crossbeam Help Center beat older webinars, whose UI and messaging have changed.
5. **Be honest when Crossbeam lacks something.** Crossbeam does not file hyperscaler registrations or run marketplace private offers.
6. **No pricing, competitor bashing or MDF in a customer email.** This is talk track and workshop material.

## What WorkSpan is

A partner revenue execution platform: it moves co-sell work across company boundaries and keeps systems in sync. Founded 2015, co-founder and CEO Amit Sinha. Positions itself as an AI-native partner revenue platform with a network of connected companies (vendor figures for network size and pipeline vary by page and are not independently verified).

**Editions**
- **Hyperscaler Edition.** The job most customers buy it for.
  - AWS: sends CRM opportunities to ACE with field mapping, brings inbound AWS referrals into the CRM, keeps stage and value in sync, creates and updates marketplace private offers from Salesforce. Launch partner for AWS's 2026 Partner Central API move.
  - Microsoft: Partner Center co-sell referral sync, marketplace private offers, MACC signals.
  - Google: submits opportunities to Partner Advantage and brings Google referrals back.
  - Works from Salesforce, Dynamics 365, HubSpot and, newest, ServiceNow CRM.
- **Ecosystem Edition.** Partner-to-partner co-sell with ISVs, GSIs, resellers and MSPs: referrals between partner CRMs, joint business plans, joint account plans, incentives and MDF (Cisco runs reseller incentive claims on it), attribution and QBR dashboards.
- **WorkSpan AI.** A Partner Advantage Card and per-partnership AI agents inside the CRM: tells the seller when to engage a cloud partner, incentive eligibility, the counterpart rep, drafts outreach, pre-fills referrals and private offers, flags stale deals.

**What the demos actually show.** Referral submission to ACE from Salesforce, inbound referral handling, private offers, AWS-supplied account signals on a Salesforce record, QBR dashboards. No reviewed demo shows WorkSpan discovering partner overlap. The only "matching" on screen is lining up an incoming referral with an account the receiver already has.

**Account mapping inside WorkSpan.** WorkSpan describes account matching inside a shared environment that both companies authorize for that partnership: each side uploads accounts and only matches show. Nothing public says the partner must be a WorkSpan customer, but everything implies a mutually authorized workspace (inference, consistent with the partnerships.ai comparison). For overlap with partners outside that, WorkSpan's own integration pages credit Crossbeam (and Reveal) with identifying overlaps.

**What users say (G2, about 4.3 from roughly 29 reviews; Crossbeam about 4.8).** Strong at automating hyperscaler registrations inside Salesforce (Postman: its channel lead stopped hand-keying AWS registrations). Many reviewers are Cisco resellers using it for incentive claims. Common complaints: hard to learn, slow screens, limited customization, Salesforce package gaps.

**Pricing signals (estimates, not published by WorkSpan).** Vendr buyer data: median about $48K a year, range roughly $20K to $64K; hyperscaler edition around $24K per cloud. Older list prices from about $990 a month. AWS Marketplace bundle up to about $52K. Compare Crossbeam: Free, Connector from $4,800 a year, Supernode and Enterprise quoted (Supernode about $39.9K plus seats on AWS Marketplace).

## The Crossbeam integration: what is actually true

- WorkSpan's integration directory lists Crossbeam for identifying and connecting overlapping accounts and opportunities.
- Its Crossbeam detail page has described logging into the Crossbeam portal from WorkSpan, partners signing up for Crossbeam from WorkSpan, and sharing leads through WorkSpan's own CRM plug-in. The same listing on its integrations subdomain has shown "Coming Soon", and the detail page has also returned 404. Status unverified.
- Crossbeam does not list WorkSpan on its integrations page and has no help article on it.
- No launch announcement, joint customer story or connector walkthrough found. Bob Moore and Amit Sinha have shared stages (Channel Partners 2024 panel; a 2025 joint webinar with Structured on partner-sourced revenue), which is strategy talk, not a product integration.
- **Practical answer:** the handoff is Salesforce. Crossbeam writes overlap and Deal Navigator signals onto the account or opportunity; the rep works the deal; WorkSpan's Salesforce app files the registration from the same opportunity.

## Where each one fits

| Job | Crossbeam | WorkSpan |
|---|---|---|
| Find which accounts overlap with which partner, including partners not on any shared tool | Core product | Only inside an authorized partnership, or via Crossbeam/Reveal |
| Rank deals by partner signal, warm paths, who knows the buyer | Deal Navigator, Lists, Copilot, MCP | WorkSpan AI, focused on cloud partners |
| Put partner context in front of sellers in Salesforce or Claude | Yes, CRM push and MCP | Yes, CRM card |
| File and sync AWS ACE, Microsoft and Google registrations | No | Core product |
| Marketplace private offers | No | Core product |
| Joint business plans, cross-company deal workflow, incentive claims | Light (lists, notes, Get Intel) | Core of Ecosystem Edition |
| Attribution | Partner influence on overlaps | Sourced and influenced across co-sell records |

They overlap at the edges and the overlap is growing: Crossbeam's Deal Navigator and co-selling automation act more like execution tools, and WorkSpan AI and account matching act more like intelligence. Don't reduce it to "Crossbeam finds, WorkSpan executes" without checking which edition and features the customer actually uses.

## Run-both operating model

1. **See the overlap** in Crossbeam: which accounts each partner already works.
2. **Pick the play**: which partner moves which deal, and why (Deal Navigator, Lists).
3. **Engage the partner** through the rep and partner manager.
4. **Register and transact** in WorkSpan when a hyperscaler is involved: ACE, Partner Advantage, Partner Center, private offers.
5. **Prove it** in Salesforce: sourced and influenced pipeline, with clear criteria so an overlap is never counted as influence by itself.

## Adding or replacing cost

| Customer situation | Answer |
|---|---|
| Uses WorkSpan only to sync hyperscaler registrations | Keep WorkSpan. Crossbeam is a new line item for a different job, not a second bill for the same one. |
| Was about to buy WorkSpan account-level data, account matching or an SOW to add overlap | That spend is the overlap. Crossbeam replaces it, with a far larger network and partners who haven't signed anything. |
| Runs WorkSpan Ecosystem Edition for ISV and GSI co-sell | Real overlap. Map feature by feature before claiming either replaces the other. |
| Only wants registrations filed | WorkSpan alone is enough. |
| Priority is partner-sourced pipeline and will register by hand or with a cheaper ACE tool | Crossbeam alone can be enough. |

## Discovery questions for a customer that has WorkSpan

1. Which WorkSpan edition and which clouds, and when does it renew?
2. What exactly does any planned WorkSpan SOW or add-on deliver, and what does it cost?
3. Which partners do you need overlap with, and are they on WorkSpan with you today?
4. Does account data refresh from the CRM, or is it uploaded?
5. Who decides what gets registered with AWS or Google, and how many inbound cloud referrals do you get a month?
6. Has WorkSpan presented its Crossbeam integration to you as live? What did they show?

## Objections

- **"WorkSpan already does account mapping."** Only inside a partnership you've both authorized there, and its own integration pages credit Crossbeam for finding overlap. Crossbeam maps against any partner on the network, plus offline partners from a spreadsheet.
- **"We can't pay for two tools."** Then decide by job: registration and marketplace stay in WorkSpan; overlap and play selection go to Crossbeam; any money earmarked for overlap inside WorkSpan moves to Crossbeam.
- **"WorkSpan has a Crossbeam integration."** It's listed, but its status is unclear and Crossbeam doesn't list it. Plan on Salesforce as the handoff and ask WorkSpan to demo it end to end.

## Vendor demo test (if a customer wants proof)

Ask WorkSpan to show one live flow: a Crossbeam overlap on an open Salesforce opportunity, through partner owner assignment, an intro or referral, joint updates, permissions, and attribution, stating at each step whether it is native, integration, custom or manual. The full 10-question script is in `references/workspan-resource-library.md`.

## Refresh

Recheck monthly or before any customer use: WorkSpan integrations directory and Crossbeam detail page status, doc.workspan.com (its llms.txt index lists every article), Crossbeam integrations page and Help Center, Vendr pricing, G2. Record changes with the date in `references/workspan-resource-library.md`.
