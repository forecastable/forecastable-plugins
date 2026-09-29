---
name: crossbeam-instance-audit
description: How Eva reads a customer's live Crossbeam instance in the browser, inventories what every partner shares down to the field, and turns it into specific partner asks. Companion to Job J (7d) and crossbeam-admin-reference.md. Built from live audits of three customer instances (a new small account, a young Connector account and a mature Supernode account), September 26th, 2026.
---

# Crossbeam instance audit: the field-level method

Job J (7d) says what to check. This file says how, in the customer's own Crossbeam in their browser,
and what the findings usually look like. Read it before any audit, data-mining pass or "what are our
partners sharing" question.

## 1. Why the browser first

The customer's browser session is the default path for audit work, on every plan.

- It shows things the MCP summary does not: field-level sharing per partner population, a partner's
  custom populations and their names, the customer's own population filters, the Plan & Billing
  breakdown of record exports and credits, and real rows with real values.
- It makes the best use of the plan's included MCP credits and record exports. Those allowances are
  worth keeping for the targeted lookups that need them (one account, one partner, a live deal).
- Reading a page never counts as an export.

When a question is better answered in the browser, suggest it and give the reason. Words that work:
"I can pull this straight from your Crossbeam in your browser. It shows every field each partner
shares, and it keeps your plan's included credits for the account-level lookups where they matter
most." Frame it as getting the most from the plan. Never frame it as avoiding Crossbeam's tools or
cost; Crossbeam is a partner and the MCP is the right tool for targeted lookups.

Use the MCP when: the customer is not at a browser, the question is one account or one partner, or a
job needs structured results across many accounts that the UI would only give page by page.

## 2. Where everything lives (UI map)

| What | Where |
|---|---|
| Plan, seats, credits, record exports | Settings, Plan & Billing. "See usage" under Record Export Summary breaks exports down by integration and by population and lists recent exports. "See usage" under Credit Usage does the same for credits |
| Data sources (CRM or CSV) | Data, Data Sources. CSV-built populations carry a warning that re-uploads count again |
| Own populations and their filters | Data, Populations. Open one to see its filter (for example Account Stage is Customer) |
| Default sharing and per-partner sharing | Partners, Sharing Dashboard (defaults and who is custom) |
| What a partner shares with the customer | Partner page, Settings, **Shared with You**. Each population shows its sharing level (Counts Only, Overlapping Accounts, All Accounts), a field count, and Request data or Pending. **Hover the field count to see every field, grouped by object** |
| What the customer shares with a partner | Partner page, Settings, Shared with Partner |
| Shortcut to a partner's sharing | The gear icon at the end of each row on the Partner List |
| Overlap counts by population | Partner page, Overview matrix. Rows are the customer's populations, columns the partner's |
| Real rows with partner fields | Click one matrix cell, then Columns, expand the partner and its objects, tick fields, Save. Do not save the list itself unless asked |
| All partners' shared populations at once | Account Mapping, the Partner Populations filter, expanded by type |
| Saved lists, owners, notifications | Lists |
| Installed integrations | Data, Integrations. A "Record Exports" badge means the integration can spend exports, not that it has |

Mechanics learned the hard way:

- Opportunity fields only unlock in a list with exactly one partner population. In multi-partner views
  they are greyed out ("Partner opportunity data can only be added when the report includes only 1
  partner population").
- The Shared with You hover list is the complete inventory. It includes Contact fields, which the
  Columns window never shows.
- The app is heavy. Partner pages and the partner list can take 20 to 60 seconds. A tab that is not in
  front may not render at all, so bring it to the front (a screenshot does this) before reading. Work
  one tab at a time; several Crossbeam tabs loading together slows every one of them. If a page stays
  blank, reload it once, then move on and come back.
- Read page text or the DOM rather than screenshots wherever possible. In the Columns window, tree
  nodes only expand on a real click.
- A narrow window swaps the app for a screen asking for a larger display. Ask the user to widen it.

## 3. The audit, in order

1. **Snapshot the instance.** Plan and renewal date, seats, credits used, record exports used and
   what spends them, data sources, populations with counts and filters, default sharing, integrations,
   tags, list count and owners, partner count split online and offline, and partners connected but
   sharing nothing.
2. **Ask the magic-button question** before looking at any partner (7d.5).
3. **Inventory every online partner** from Shared with You: sharing level per population, custom
   populations and their names, and the full field list. Then Shared with Partner for the other
   direction.
4. **Read real rows** for the two or three partners that matter most: fill rate ("--" counts), recency
   (close and last activity dates), and whether each population holds what its name says.
5. **Compare to the wishlist** and write the partner data map: Have, Gap, Unexpected gold, per partner.
6. **Recommend** under the rules in 7d.6, and report the budget (7d.7).

## 4. What to expect: patterns from live instances

**Three archetypes.** Place every customer first; the archetype decides which moves come first.

| | New and small | Young Connector | Mature Supernode |
|---|---|---|---|
| Typical shape | Handful of partners, several offline, CSV-heavy | CRM plus CSV, 10 to 20 partners, some connected but silent | CRM, 50 plus partners, custom populations, tags and tiers |
| Default sharing | Counts Only | Often Overlapping Accounts | Counts Only plus custom per partner |
| Tags and lists | None | None of their own, a few shared in by partners | A full taxonomy and a play-coded list set |
| Integrations | None | None, even ones the plan includes | Several, some broken |
| Budget pressure | None | Low | Record exports near the limit |
| First moves | Rep-contact plays with the richest partner | Get data to reps, wake silent partners, mine partner target lists | Mine hidden populations, surface partner signals in lists, protect the export budget |

**What partners share, by type.**

- CRM partners on Salesforce or HubSpot that share opportunities usually expose 20 to 24 fields:
  account firmographics, owner name, email and title, contacts (name, title, email, last activity) and
  opportunity name, stage, type, dates and won. The richest single source for rep routing and timing.
- Big platforms share the least about people and the most about product. Expect no owner names, but
  product footprint fields, product-tier custom populations (for example one per product edition),
  CSM coverage flags, third-party intent scores and conversion dates.
- Some platforms put their program in the population name ("... Help us and get 30%. Email
  included") and ship target lists as uploaded files with rep names, rep emails and company IDs. Read
  population names as briefs.
- Deal fields like Use Case and Use Case Detail are ready-made messaging.
- A partner whose data sits under a file name, not Account, User and Opportunity, uploaded a file
  instead of connecting a CRM. Expect a fixed field set and old data; check the date in the file name.
- A partner that shares populations but has no Partner Data under Columns is on Counts Only.
- A partner sharing All Accounts exposes accounts the customer does not have at all (Greenfield).
- A population's name does not guarantee its contents. An "Open Opportunities" population can hold
  closed deals from years ago. Always read real rows before acting.

**What the customer's own instance often shows.**

- A custom population hidden from every partner, often by accident. Former opportunities are the usual
  one, and the most valuable.
- A Customers population that includes partners. Sometimes a labeling issue, sometimes correct because
  partners buy and resell. Ask before judging (7d.6).
- A Prospects population in the tens of thousands, which drives most record exports when pushed to a
  CRM.
- Lists owned by deactivated users, integrations showing "Action needed", and included integrations
  never installed.
- Potential Revenue far above what the pipeline could be. Check how opportunity amounts are populated
  before quoting it; never present it as pipeline.

## 5. Budget reading

Record exports: each unique record counts once per term when it first leaves Crossbeam. The
breakdown names the integration (for example a CRM standard-object field push, a CRM custom object,
Pipeline Generation exports, list exports) and the populations behind the count. The biggest spender
is usually a CRM push fed by a very large Prospects population. Recommend narrowing what each
integration pushes before recommending more exports. At 100% every export-based integration pauses.

Credits: read used against included and the reset date. Zero used while the MCP shows recent activity
is worth a question, not a conclusion.

Report both in every audit (7d.7), with the integration or population to adjust first.
