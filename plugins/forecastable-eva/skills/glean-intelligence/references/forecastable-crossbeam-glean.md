# Forecastable + Crossbeam + Glean

Version: 2026.09 (built 2026-09-26). How Eva and Alex make the three systems work together for a
customer that runs Glean. Source tags point to `glean-intelligence.md`.

## 1. One sentence each

- **Crossbeam tells you who.** Which partners overlap which accounts, who at the partner knows the
  buyer, what the partner is sharing. Numbers come from Crossbeam.
- **Glean tells you what we already know.** What was said internally about the account or partner,
  who inside the company knows them, which assets and past wins exist, whether a commitment was
  actually kept. Context comes from Glean, permission-trimmed to the acting user.
- **Forecastable makes it happen.** Partner plans, goals, milestones, dated tasks, relationship maps,
  commitments, drafts, and the accountability that chases them. Execution lives in Forecastable.

Eva is the accountability layer across all three. Alex is the judgment layer. Neither holds the
relationship.

## 2. Division of truth (never cross these lines)

| Question | Source of truth | Never from |
|---|---|---|
| Overlap counts, shared contacts, partner metrics | Crossbeam MCP | Glean documents, memory |
| Pipeline amounts, stages, dates, counts | CRM via Forecastable MCP (or Salesforce SOQL tool in Glean) | Glean summaries of documents [D39] |
| Plans, commitments, owners, due dates | Forecastable MCP | Glean, Slack |
| What was said, decided, promised; who knows whom internally; which assets exist | Glean (`search`, `read_document`, `meeting_lookup`, `employee_search`, `gmail_search`) | Recollection |
| Glean admin facts and how-to | `glean-intelligence.md`, verified live via Glean Docs MCP [D60] | Guesswork |

## 3. Topology

### 3.1 From Claude (where Eva and Alex run)

```
Claude (Eva / Alex, forecastable plugin)
  |-- Forecastable MCP   app.forecastable.com/mcp        plans, accounts, tasks, calendar, action items
  |-- Crossbeam MCP      mcp.crossbeam.com/mcp            overlaps, partner contacts (Supernode and up)
  |-- Glean MCP          {tenant}-be.glean.com/mcp/{path} internal context, permission-trimmed
```

Setup the customer's Glean admin does once [D53] [D54] [D56]:

1. Enable Glean OAuth (Users & permissions, Third-party access) and the MCP server.
2. Create a job-shaped server, e.g. **"Glean - Partnerships"** at `/mcp/partnerships`, with `search`,
   `chat`, `read_document`, `employee_search`, `meeting_lookup`, `gmail_search` or `outlook_search`,
   `user_activity`, `memory`. No write tools on this server.
3. Allow Anthropic IP ranges through any firewall in front of Glean.
4. In Claude admin settings, add the server URL as an org integration; each user signs in with Glean
   OAuth.
5. Validate: in Claude, "Search Glean for our last QBR with [partner]."

Each call runs as the acting user. Eva sees what that person can see in Glean, nothing more.

### 3.2 Inside Glean (for customers who live in Glean)

- Add **Crossbeam** as a remote MCP server (it is in Glean's supported list) with **OAuth User** auth,
  so each rep's own Crossbeam permissions apply [D51] [D52]. Crossbeam's MCP needs a Full Access or
  Sales seat and burns Crossbeam credits [A18].
- Forecastable MCP as a custom remote MCP server inside Glean: supported pattern in principle, not yet
  tested (section 23 of the intelligence file). Do not promise it.
- Salesforce customers: Glean indexes plus SOQL tools and opportunity updates [D23]. **Red-list partner
  economics fields** (margin, referral fee, MDF) because FLS is not enforced [D23]. <!-- VALIDATE-OK[economics]: names customer CRM fields to red-list in Glean, not Forecastable economics -->
- HubSpot customers: Glean indexes only Contacts, Companies, Deals, Tickets. Partner custom objects and
  Leads are invisible to the index; use HubSpot's remote MCP or rely on Forecastable for partner data
  [D25].
- Partner Slack Connect channels cannot fire Glean content triggers [D38]. Slack results require each
  user's own Slack authorization [D26].
- Glean agents with write tools cannot be exposed to Claude over MCP; keep anything Eva calls
  read-only and under 30 seconds [D57].

### 3.3 Cost awareness

Three meters run at once: Crossbeam MCP credits (annual, no rollover), Glean FlexCredits (agent runs
7 to 114 credits, Client API and MCP calls metered) and model tokens [A18] [D66]. Eva prefers one
Glean `search` plus targeted `read_document` over repeated `chat` calls, and one Crossbeam account
lookup over broad ecosystem scans.

## 4. The plays

Each play names the trigger, the three-system path, the output and the approver. None sends anything.

### L1. Partner-aware account brief (strengthens Eva Job A)

- Trigger: an account-planning session or partner meeting on the calendar.
- Forecastable: account, plan, open tasks, relationship map, last meeting action items.
- Crossbeam: `get_account_context`, `find_overlapping_partners`, `find_partner_shared_contacts`.
- Glean: `search` the account and partner names (last 90 days), `meeting_lookup` for prior meetings,
  `employee_search` for internal owners, `read_document` on the two or three most relevant hits.
- Output: one-page brief with cited internal context, partner overlap, who knows whom, open
  commitments, and the one ask for the meeting.
- Approver: the partner manager running the meeting.

### L2. Who-knows-who internal path (strengthens Job B persona pairing)

- Crossbeam gives the partner-side person; Glean `employee_search` and `search` find our people who
  worked the account, the partner or the persona before (emails, meeting notes, Slack threads).
- Output: the internal owner for the intro and the evidence trail. Never states the data source in
  partner-facing copy (Eva guardrail 11).

### L3. Real assets only (strengthens Job B handoff)

- Before drafting a ghostwritten handoff, Glean `search` for existing case studies, value stories,
  joint wins, battlecards and one-pagers with this partner or persona. Cite what exists; if nothing
  exists, say so and log the gap as a task. Never invent an asset.

### L4. Evidence before a chase (strengthens Job C)

- Before any rung of the chase ladder, check Glean for evidence the commitment was already kept:
  `gmail_search` or `outlook_search` for the sent intro, `meeting_lookup` for the follow-up meeting,
  `search` for the shared doc.
- Found: mark the Forecastable task done with the evidence link, do not chase. Not found: chase as
  normal. This is "evidence beats recollection" applied to the chase itself; a chase for something
  already done spends relationship credit for nothing.

### L5. Deal qualification context (strengthens Job G)

- Job G reads Crossbeam only; that rule stands. After Job G ranks deals, Glean adds internal context on
  the top deals (last call notes, stakeholder mentions, blockers) in a separate, labeled section.
  Glean never changes a Job G score.

### L6. Partner QBR and exec update pack

- Forecastable: plan progress (milestones done, missed, next), commitments kept and slipped.
- Crossbeam: `get_partner_context` metrics with their window.
- Glean: joint wins, escalations, quotes from internal meeting notes, cited.
- Output: content for the executive deck (routes to `executive-updates-as-decks`). Numbers keep their
  source and window.

### L7. Glean setup audit for the partner team (advisory)

A checklist Eva runs with the customer's Glean admin, proposing every change, making none:

1. Is there a job-shaped Glean MCP server for partnerships, read-only, with the tools in 3.1?
2. Is Crossbeam connected in Glean with OAuth User auth, and in Claude?
3. Salesforce: are partner economics fields red-listed? HubSpot: does the team know partner objects are
   not indexed?
4. Are partner channels in Slack authorized per user; are Slack Connect limits understood?
5. Is there a knowledge profile for shared partner-program agents so everyone gets the same answer
   [D43]?
6. Go links and Answers for the partner program: `go/partners`, `go/cosell`, `go/partner-plans`,
   "How do I register a partner deal?"
7. Usage limits on any partner-team agents; content triggers filtered [D67] [D38].
8. Default Member permissions and agent publishing approval set deliberately [D40].

Output: numbered proposals, each with an owner on the customer side. The customer's admin approves and
makes each change.

### L8. Glean agent specs for the partner team (built by the customer in Glean)

Eva writes the spec; the customer's builder builds it. Every spec states goal, trigger, knowledge scope,
tools, output, owner, run limit and approval path.

| Agent | Trigger | Knowledge and tools | Output |
|---|---|---|---|
| Partner account snapshot | Chat message: account name | Company search, CRM connector, Gong, Crossbeam MCP `get_account_context` | Snapshot with overlapping partners and internal context |
| Pre-meeting partner brief | Google Calendar "before the event starts", filtered to partner domains | Calendar, email, CRM, Crossbeam | Brief DM'd to the attendee |
| Gong call partner mentions | Gong new call, filtered to partner or co-sell calls | Gong transcript | List of partner commitments with owner and date, for the rep to log in Forecastable |
| Partner QBR prep | Chat message: partner name | Collections for the partner, Slack channel, CRM | QBR draft with citations |
| Partner program answers | Auto-routed chat agent with a knowledge profile | Partner program docs only | Consistent answers on registration, rules of engagement, MDF |

Constraints: agents that write cannot be called from Claude [D57]; unscoped triggers burn quota [D38];
Crossbeam credits cap run frequency [A18].

### L9. Glean admin advisory (any customer asking about Glean)

Eva answers Glean administration and usage questions from `glean-intelligence.md`, labels vendor
claims, gives the version date, and tells the person which facts to confirm in their own tenant.
Judgment calls about whether to buy, expand or cut Glean go to the partnerships lead or Alex, not Eva.

## 5. Guardrails specific to Glean

1. Glean content is internal. Before anything leaves the building, run Eva's outbound check and strip
   internal context, pricing posture and anything a partner was never meant to see.
2. Never widen access. Eva never asks someone to share, re-permission or export Glean content so Eva
   can see it. If the acting user cannot see it, Eva does not have it.
3. Never compute numbers from Glean documents. Numbers come from Crossbeam, the CRM or Forecastable.
4. Never change a customer's Glean configuration. Propose; the customer's admin decides and acts.
5. Cite Glean evidence with the document title and link the acting user can open.
6. A Glean miss is not a finding. "Glean returned nothing" can mean no content, no permission, Slack
   not authorized, or not yet indexed. Say which, or say it is unknown (Eva guardrail 12).
7. Respect the meters: prefer `search` plus `read_document`; avoid `chat` loops; say when a job will
   spend Crossbeam credits or FlexCredits.
