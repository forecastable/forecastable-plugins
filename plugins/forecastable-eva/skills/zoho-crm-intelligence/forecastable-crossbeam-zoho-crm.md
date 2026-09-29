# Forecastable, Crossbeam and Zoho CRM

Version: 2026-09-29. Companion to `zoho-crm-intelligence.md` (source tags refer to its section 14).

In a Zoho stack, Zoho CRM holds leads, deals and revenue, and usually the customer's mailboxes run through
Zoho Mail. Forecastable holds the partner relationships, relationship maps, partner and personal plans,
and partner email activity. Today most Forecastable customers on Zoho have no system integration: the two
meet on email addresses and domains, and on monthly pulls of Zoho outcomes into Forecastable plans. This
file is how Eva does that well, and how she audits a Zoho org for partner readiness.

## 1. Division of truth

| Question | System of record | Why |
|---|---|---|
| Who is a partner, partner tier, relationship map, owner | Forecastable | Partner work happens there (OURS) |
| A referred lead or appraisal, its source and referring partner | Zoho Lead (source picklists plus a partner lookup, or a custom module) | Zoho is where the lead is created |
| Deal value, stage, close date, won or lost | Zoho Deal (or the customer's custom deal module) | [A42] |
| Partner-sourced revenue per partner and per BDM for plans | Forecastable plan goals, fed from Zoho | OURS: Zoho stores the events, Forecastable turns them into attribution and plan actuals with history |
| Calls and meetings | Zoho Calls and Events when telephony or calendar sync is on; otherwise nowhere reliable | [B30][Y:_Dn2IF2DVQM 33:06] |
| Partner emails | Forecastable (email integration) and Zoho (mailbox integration), each matching by email address | Both read the same mailbox independently |
| Account overlap with partners (B2B customers) | Crossbeam, if the customer uses it | Whether Crossbeam offers a native Zoho CRM data source is UNVERIFIED; check the customer's Crossbeam data sources, otherwise a CSV or warehouse source |

## 2. Zoho org audit checklist (partner readiness)

Pass, fail or unknown per item, with evidence. Run read-only.

### A. Access and plumbing
1. Edition, data center, time zone. Where: `Get_Organization` or Setup > Company Details.
2. Eva's path works: Zoho CRM connector or custom read-only MCP server, as which user. The user's profile
   has Zoho CRM API Access [B10].
3. The Eva user's role sees all partner-relevant records (compare a COQL count with an admin's count).
4. API credits headroom: Setup > Developer Hub > APIs and SDKs > Credits [B28].
5. Sandbox exists for testing changes [B41].

### B. Data model for partner attribution
6. One field or lookup identifies the referring partner on Leads, and it carries to Deals on conversion
   (lead conversion mapping) [Y:m588QX4WmYA 60:02].
7. Partner records in Zoho (custom module or Accounts with a type) carry a website or domain field for
   matching to Forecastable.
8. Lead Source values describe the motion (Referral, Proactive, Event), and any second source picklist has
   defined values and a rule for when to use it [Y:m588QX4WmYA 38:52].
9. A clear "won" definition: the stage value (or custom module status) that means closed won, and the
   date field that dates it.
10. Stage history is available (Timeline API or picklist history tracking) [A29][Y:m588QX4WmYA 56:01].
11. Duplicate partners or contacts in Zoho that would break email matching (same email on two records).

### C. Activity capture
12. Share of BDMs with their mailbox integrated and sharing set to public [Y:_Dn2IF2DVQM 30:56].
13. Telephony: PhoneBridge or Zoho Voice installed, or calls only logged from the mobile app [B35][B30].
14. Calendar sync on for meetings [Y:Ngm045YcMgc 25:13].

### D. Reporting
15. Reports exist for partner-sourced deals opened and won by month, with partner name and domain as
    columns, and they reconcile with a COQL pull.
16. Dashboards the partner lead reads weekly.

### E. Governance
17. Profiles: mass delete and setup rights not on everyday BDM profiles [Y:0m05tx5_fVU 19:43].
18. MCP servers: only read tools for AI use; delete tools disabled; auth on demand [Y:325hWpN_lEs 04:50].
19. Blueprint or validation rules that would block any write-back Forecastable plans to do.

## 3. Monthly pull into Forecastable plans (OURS)

Run in the first business days of each month, and on demand before plan reviews.

1. **Load the customer map** from `customers/<customer>.md` (module and field API names, won stage,
   partner lookup, source picklists, BDM user ids). If missing, run SKILL section 2 discovery first.
2. **Pull with COQL** for the period, with the customer's offset:
   - Deals Opened: deals created in the period with a partner source.
   - Deals Won (or the customer's unit, for example keys): deals moved to won in the period with a partner
     source, dated by close date (or stage-change date from Timeline when the customer defines it so).
   - Leads or appraisals by source picklists, split by motion.
   Each row: Zoho id, name, owner, partner id and name, partner website or domain, source values, date,
   amount.
3. **Match to Forecastable partners.** Order: partner domain to Forecastable account domain; then contact
   email domain; then normalized partner name (strip "Pty Ltd", "Real Estate", punctuation). Mark every
   match as domain, email or name. Unmatched go to a list for the partner lead; never create Forecastable
   accounts without a yes.
4. **Roll up** per BDM (Zoho owner mapped to Forecastable user by email) and per partner.
5. **Write actuals** to the matching Forecastable personal and partner plan goals through the Forecastable
   MCP, with the Zoho ids in the note, only after the user confirms the table. Flag first-ever deals per
   partner (a common tier-promotion signal).
6. **Report:** totals vs goals, new first-time partners, unmatched rows, and data quality issues (missing
   partner lookup, wrong source picklist).

## 4. Recommendation plays (OURS)

1. **One partner field end to end.** A partner lookup on Leads that maps through conversion to Deals, so
   every won deal carries its partner without manual copying.
2. **Domain on the partner record.** A website or domain field on the Zoho partner record makes
   Forecastable matching exact instead of fuzzy.
3. **Two-level source, fixed values.** Keep Lead Source for the motion and one secondary picklist for the
   sub-motion, with values agreed with the partner lead and documented; no free text.
4. **A saved report and a COQL twin.** For each monthly number, a Zoho report the business trusts and a
   COQL query that returns the same count, so Eva can pull it without a human export.
5. **Read-only AI access.** A custom Zoho MCP server with read tools plus COQL, auth on demand, and API
   access only on the profiles that need it.
6. **Capture calls properly or not at all.** If calls matter to partner scoring, use telephony (Zoho Voice
   or PhoneBridge); mobile app logging misses iPhone inbound calls.
7. **Integration when the pull becomes weekly.** When manual monthly pulls turn weekly, scope a
   Forecastable to Zoho integration (deals, calendar, calls) with Alex.

## 5. What Eva does with Zoho each week (OURS)

1. Pull new partner-sourced leads and deals since last week; post to the partner lead with partner and BDM.
2. Flag won deals missing a partner lookup or with a source that contradicts the partner field.
3. List partners with a Zoho lead or deal but no Forecastable account (unmatched domains).
4. Check first-time won deals per partner and suggest tier changes to the partner lead.
5. Count BDM calls and meetings logged in Zoho if telephony or calendar sync is on; otherwise say that
   the data is not captured.
All reads through the connector, custom MCP or browser as the agreed user; no Zoho writes without an
explicit yes.
