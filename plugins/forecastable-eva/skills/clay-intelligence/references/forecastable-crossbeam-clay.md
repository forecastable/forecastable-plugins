# Clay with Forecastable and Crossbeam

Version: 2026-10-04. Next refresh due: 2026-11-04 (with `clay-intelligence.md`).
Source tags `[C#]` resolve in `clay-intelligence.md` section 11, `[E#]` in `events-intelligence.md`
section 11. Recommendations are OURS unless sourced.

## 1. Where Clay sits

| Layer | Owner system | Eva's job there |
|---|---|---|
| Pipeline of record | CRM (HubSpot, Salesforce, Zoho) | Read amounts and owners; write only on a yes |
| Who overlaps with which partner | Crossbeam (MCP, shared lists, Clay source) | Overlap cuts, partner context, shared contacts |
| Who the people are and what they care about | Clay (MCP for 1 to 20, tables and Functions for volume) | Fill buying-committee gaps, score, research, route |
| Who is coming to the event | Event platform (Zuddl, Luma, Sequel, Splash, Bizzabo, CSV) | Registrant and check-in pull |
| What partners committed to and what it produced | Forecastable (plans, tasks, Engage lists, Events module) | Commitments ledger, follow-up, attribution |

Clay is a specialist executor. It is never a customer's Eva runtime and never
the place attribution lives. Clay writes nothing back to Crossbeam [C38].

## 2. Crossbeam plan decides the path

| Customer's Crossbeam plan | Native Clay "Import from Crossbeam" and Partner Data action | What Eva does instead |
|---|---|---|
| Free | No (Supernode minimum) [C39] | Crossbeam MCP in the customer's Claude for overlaps (50 MCP credits a year, Free sees up to 50 overlap records) [E19], Clay MCP for people. Small events only |
| Connector | No [C39] | Same, 500 MCP credits a year [E19]; or Crossbeam export into Clay by CSV (UNVERIFIED as a sanctioned path) |
| Supernode | Yes | One Crossbeam source per partner (limit 1,000 overlaps each), Partner Data action on every registrant domain, auto-update on [C38] [C40] |
| Enterprise | Yes | Same, plus room for warehouse-grade joins like Clay's own Sculpt build |

## 3. Workspace audit checklist

Run read-only. Pass, fail or unknown with evidence; top three fixes ranked by credit waste or revenue
impact.

1. Plan identified (modern Launch, Growth, Enterprise, or legacy). Legacy loses modern features,
   including MCP, on 2026-12-31 [C4].
2. Actions and Data Credits consumption for the last 30 days vs allowance; Actions do not roll over [C2].
3. Table-level auto-run off on every table not deliberately live [C51].
4. Every paid column has an "Only run if" condition [C51] [C52].
5. Auto-dedupe set on the key column of every source-fed table [C51].
6. No table within 10 percent of 50,000 rows; no webhook source near its 50,000 lifetime cap [C26] [C50].
7. Waterfalls ordered cheapest-valid-first; BYO keys understood to still cost Actions [C2].
8. CRM write-back uses lookup then update or upsert, never blind create; HubSpot custom-object scope
   not enabled on a non-Enterprise portal [C45].
9. Partner and attribution fields written by Clay match the CRM attribution design
   (`forecastable-hubspot-setup`); Clay never overwrites a partner-sourced field set by a human.
10. MCP: per-user credit limits set, allowed MCP clients listed, only reviewed Functions enabled for
    MCP, each with name, description and output column [C7] [C8].
11. Crossbeam connection (Supernode and up): one source per priority partner, auto-update on, Partner
    Data action used on inbound and event tables [C38].
12. Repeated chains packaged as Functions so Eva can call them through MCP [C28].

## 4. Eva Job O: partner event overlap (the Sculpt pattern for any customer)

**Trigger phrases:** "plan [event] with partners", "who should we invite", "which partners for the
dinner", "build a Sculpt-style dashboard", "event overlap for [event]", "follow up [event]".

**Inputs:** event name, date, format, region; registrant source (platform or CSV); CRM; Crossbeam
access level (section 2); Clay access (optional).

**Steps** (runbook detail in `events-intelligence.md` section 5):

1. **T-60 Pick co-hosts.** Score partners with the Event Partner Score (events file section 3, F1 to
   F7, gates G1 to G4). Two co-hosts maximum per dinner. Output: ranked list for the partner manager.
2. **T-45 Target list.** Three overlap cuts: registrants or invitees x partner customers; our open opps x
   partner customers or opps; partner customers not in our CRM (`find_new_accounts`). Report match rate
   and unmatched count.
3. **T-45 Contacts.** `find_partner_shared_contacts` first, Clay MCP for gaps (1 to 20 per run), a
   Clay table or Function for volume. Store as relationship maps or buying groups in Forecastable.
4. **T-30 Warm-intro asks.** One specific ask per overlap account with an open opp, named partner
   owner and due date, logged as tasks on the partner's Forecastable plan. Drafts only.
5. **T-14 and T-1 Refresh.** Pull registrants, rejoin, rescore, flag new warm targets; one brief per
   meeting.
6. **T-7 Partner page.** One private page per co-host: account, our status, partner status,
   registered or attended, our owner, partner owner, warm contact, ask. No ARR or pipeline figures on
   a partner page without the partnerships lead's yes. Prefer Crossbeam shared lists for account data.
7. **Post-event.** Tier-1 follow-up drafts within 24 hours, Clay enrichment and scoring of attendees
   and scans, attribution tags (event x partner, sourced vs influenced), T+30 and T+90 readouts per
   partner.

**Output:** grounding line, co-host ranking, target table with overlap type, asks with owners and
dates, partner pages, and the readout. Nothing sends.

**Self-check:** consent basis checked before any attendee data reached a partner; every number names
its field and source; match rate reported; no partner saw another partner's data.

## 5. When to use Clay vs not (OURS)

- Use Clay when the job is people and signals at volume: buying committees at 200 overlap accounts,
  registrant scoring, sponsor list enrichment, recurring Functions Eva calls by MCP.
- Skip Clay when Crossbeam shared contacts already cover the account, when the event is under about
  40 names, or when the customer has no Clay seat; Clay MCP and Crossbeam MCP in chat are enough.
- Practitioners are split on replacing Clay with Claude Code builds; the consensus keeps Clay for
  anything that writes to the CRM or sends (see `clay-admin-best-practices.md`, Conflicts).

## 6. Proof and timing

- Clay's own Solution Partners team built the pattern for Sculpt 2026 (2026-10-08); partners GoNimbly
  and demandDrive used it; no outcomes published yet [E1]. Check for a results follow-up after Sculpt.
