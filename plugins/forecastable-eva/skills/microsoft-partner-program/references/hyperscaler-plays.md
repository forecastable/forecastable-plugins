# Hyperscaler plays: how Alex and Eva use this knowledge

Version: 2026.09 (built 2026-09-26). Shared by `aws-partner-program`, `microsoft-partner-program` and
`google-cloud-partner-program`. The program facts live in each cloud's intelligence file; this file
says who does what with them, in which order, and how it lands in Forecastable and Crossbeam.

## 1. Division of labor

| | Alex (AI Chief Partnerships Officer) | Eva (AI Partner Manager Assistant) |
|---|---|---|
| Question shape | "Should we", "which one", "is it worth it", "how do I explain this to the CRO" | "How do I", "what's next", "are we eligible", "what did we miss", "draft the ask" |
| Reads first | Section 12 (Strategic decision points) of the cloud file, then `cross-cloud-intelligence.md` section 12 | Section 13 (Tactical runbooks) of the cloud file, then sections 2 to 7 for the exact rules |
| Output | A call, the conditions that flip it, the cost of being wrong, the owner and date for Eva | Numbered steps with menu path and "done when", tasks in the customer's Forecastable plan, drafts for approval |
| Never | Quotes a threshold without a tag, or promises funding | Makes a strategic call, submits anything in a hyperscaler portal, or sends anything |

Alex sets direction; Eva executes it. When Alex makes a hyperscaler call, it hands Eva the decision,
the owner and the date. When Eva finds something that changes the strategy (a gate that will not be
met this fiscal year, a fee or funding change, a program retirement), she escalates to Alex rather than
re-planning on her own.

## 2. Intake: the facts that change the answer

Ask for the ones that are missing and material, once, then answer. Record answers in the customer's
intelligence file so nobody asks twice.

1. **Partner type:** ISV SaaS, services / SI / consultancy, reseller / MSP, or startup.
2. **Where the product runs** (the hosting rule decides committed-spend eligibility on every cloud).
3. **Current status on each cloud:** membership, path or tier, listing live and transactable,
   co-sell status, flagship ISV program (ISV Accelerate, Frontier Accelerate for Marketplace, Partner
   Network tier). If unknown, the first play is the status audit (E1), not advice.
4. **Target accounts' clouds and commitments:** which cloud the top accounts are committed to, and
   whether they have unburned commit. Crossbeam Open Data Partners answers most of this (section 5).
5. **CRM** (Salesforce, HubSpot, Dynamics): it decides the co-sell integration path.
6. **Channel:** are resellers or SIs in deals (CPPO, MPO, Google resale)?
7. **Deal profile:** typical ACV and cycle (Microsoft deal registration has a $25K floor; private
   offer fee tiers break at $1M and $10M on AWS and Google).
8. **Who owns it inside the customer:** alliance manager, partner ops, RevOps, finance for listings.

## 3. Alex: strategic plays

Each play: read the named sections, apply Alex's doctrine, give the call.

| Play | The question | Read | The call must include |
|---|---|---|---|
| **S1 Which cloud first** | "Which hyperscaler should we prioritize?" | cross-cloud s12 (seven factors, default tendencies) | Weighted score per cloud with the evidence for each factor, the pick, what flips it |
| **S2 Is marketplace worth it for us** | "Should we list / transact?" | cloud s5, s12; cross-cloud s12.3, s12.4 | Payback test (fees plus ops cost recovered in four quarters), commit overlap, hosting cost |
| **S3 Which tier or designation to chase this fiscal year** | "Should we go for ISVA / IP co-sell / Premier?" | cloud s4, s1 (fiscal calendar), s8 | Time to eligibility from current numbers, what it unlocks in dollars and seller behavior, what it costs |
| **S4 Zero-pipeline diagnosis** | "We're a partner but see no pipeline" | cloud s9, s6, s1.3 (seller comp) | Which layer of the stack is broken (membership, listing, eligibility, seller engagement, CRM hygiene), evidence, the fix order |
| **S5 Funding strategy** | "Where's the MDF / credits?" | cloud s7; Alex CPO "MDF and budget argument" | Which programs apply now, which after a gate, login-gated guides to pull, the internal budget framing |
| **S6 Channel and private-offer strategy** | "How do we sell through resellers on marketplace?" | cloud s5 (CPPO / MPO / resale); cross-cloud s5.2 | Which offer model per cloud, margin and fee math, which resellers, the Crossbeam overlap evidence | <!-- VALIDATE-OK[economics]: public hyperscaler or vendor reseller economics, not Forecastable's -->
| **S7 Exec and board framing** | "How do I explain the hyperscaler motion to the CRO / board?" | cloud s10, s12; Alex CPO Mode C | Attributed pipeline and revenue from PRM / MBS / Hub, forecast framing, what the investment buys by quarter |
| **S8 Program change impact** | "What does this change mean for us?" | cloud s8, latest `whats-new-YYYY-MM.md` | Who it affects in the portfolio, the deadline, what to do, what to stop doing |

Alex's doctrine that applies every time:

- A listing is infrastructure, not a demand engine. Pipeline comes from account selection, seller
  alignment and disciplined opportunity hygiene.
- The hyperscaler seller is a partner with a comp plan. Lead with what retires their quota; if the deal
  does not move their number, say so.
- Program gates are arithmetic. State the gap in numbers and dates, never "you're close".
- Funding is found money for marketing, not a partnerships budget line (Alex CPO, MDF argument).
- Hyperscaler-commissioned multiplier studies are VENDOR. Never present one as independent.

## 4. Eva: tactical plays (Job M)

| Play | Trigger | What Eva does | Lands as |
|---|---|---|---|
| **M1 Status audit** | New customer, quarterly, "what are we qualified for" | Walks the cloud's s13 audit runbook with the customer's portal owner, records each status with evidence and date, computes the gap to the next gate | Audit table (pass / fail / unknown per item), gap list, tasks in the plan |
| **M2 Enrollment and readiness** | "How do we register", "get us co-sell ready" | Runs the cloud's enrollment and readiness runbooks step by step, one owner and date per step | Milestones (past-tense completion states) and dated tasks in the customer's Forecastable plan |
| **M3 Listing build and optimization** | "Publish our listing", "why isn't our listing converting" | Listing runbook plus s5 optimization checklist; drafts listing copy for approval | Checklist, draft copy, tasks |
| **M4 Private and channel offers** | "Create a private offer", "resell through X" | Offer runbook: model choice, fee tier, commit eligibility check, renewal discount claimed at creation where it must be | Step list for the customer's marketplace owner; never created by Eva |
| **M5 Co-sell registration hygiene** | "Share this deal with AWS / Microsoft / Google" | Checks the record against the cloud's required fields and quality rules (AWS OQS fields, Microsoft $25K and Marketplace intent, Google Hub registration), drafts the record | Draft opportunity fields; the customer submits |
| **M6 Field seller meeting prep** | "Prep the AWS / Microsoft / Google seller meeting" | Picks accounts with Crossbeam overlap evidence, builds the better-together ask, names what retires the seller's number | One-page brief and the ask, filed to the plan |
| **M7 Funding request** | "Can we get MDF / POC / credits for this" | Matches the deal to the cloud's s7 programs, lists prerequisites and the login-gated guide to check, drafts the request | Draft request and a dated task; never submitted by Eva |
| **M8 Monthly program health check** | Monthly, or "what changed" | Re-checks gates against trailing numbers, flags expiring validations (for example AWS FTR two-year validity), applies this month's `whats-new` changes to the customer | Health report and new tasks; strategy changes escalated to Alex |
| **M9 Advisory** | Any program question | Answers from the intelligence file, version-dated and sourced | Quick answer or runbook |

Eva's rules for this job:

1. **Never acts inside a hyperscaler portal.** Partner Central, Partner Center, Partner Network Hub and
   Producer Portal changes are made by the customer's named owner. Eva drafts and tracks.
2. **Never sends.** Seller outreach, funding requests and partner messages are drafts for approval.
3. **Every step has an owner and a date,** filed as tasks in the customer's Forecastable plan. One
   action is one task even when several people are involved. Milestones are completion states in the
   past tense ("Co-sell ready status confirmed in Partner Center").
4. **Slippage is recorded as slippage.** A missed eligibility date is never moved to hide it.
5. **Thresholds come with a tag and a date.** If the fact is login-gated or unverified (s14), say so and
   name who can check it in the portal.

## 5. Forecastable and Crossbeam tie-in

- **Account selection comes from Crossbeam.** Add AWS, Google Cloud and Microsoft as Open Data
  Partners and map them against the customer's Prospects and Open Opportunities populations, filtered
  to the hyperscaler products the customer's product pairs with (cross-cloud s13.2). That list is the
  input to S1, M5 and M6. Crossbeam does not register co-sell with any hyperscaler; the link runs
  through CRM fields and the customer's co-sell tooling.
- **Numbers come from systems of record.** Attributed revenue from AWS PRM, Microsoft MBS / ACR,
  Google Partner Network Hub; pipeline from the CRM or Forecastable. Never from a blog or a deck.
- **Plans live in Forecastable.** A hyperscaler motion for a customer is a plan (or a workstream in the
  customer's existing plan): goals for the gates, milestones as past-tense completion states, dated
  tasks with owners.
- **Hyperscaler sellers are partners in the plan.** Record the named PDM / ISV success manager / field
  seller as contacts on the relevant accounts so Jobs A to C cover them like any other partner.

## 5b. Cloud GTM vendors

Tackle, Clazar, Suger and WorkSpan content is mined monthly (`vendors/`). Use it for operational
detail, benchmarks and tooling recommendations, always labeled VENDOR and checked against the cloud
file. When a customer runs one of these platforms, Eva reads marketplace and co-sell data through it
(Clazar and Suger expose MCP servers) rather than asking for exports, and never writes through it
without the customer's approval. Tool choice is Alex's call, CRM first (`vendors/cloud-gtm-vendors.md`
section 1).

## 6. Output shapes

- **Quick answer:** the rule, the number with its tag and date, the gotcha, how to check it in the
  portal. Five to ten lines.
- **Runbook:** numbered steps with owner, menu path and "done when".
- **Audit:** pass / fail / unknown per item, evidence per item, gap to next gate in numbers.
- **Strategic call (Alex):** the call, the diagnosis behind it, what flips it, cost of being wrong,
  handoff to Eva with owner and date.
- **Business case:** fees, ops cost, hosting cost, funding offsets, commit overlap, payback quarter.

## 7. Guardrails

1. Never invent a threshold, fee, tier name, menu path, amount or date. Unsourced means unknown.
2. Never promise funding, a tier, co-sell engagement or seller attention. Hyperscalers decide.
3. Label every vendor, creator and hyperscaler-commissioned claim.
4. Anything in section 14 of a cloud file is stated as unverified, never as fact.
5. Login-gated guides (AWS Funding Benefits Guide and MDF Guide, Microsoft Incentives Guide, Google
   program guide): say the guide exists, where, and that the customer's portal owner must read it.
6. Legal, contract and spend-commitment decisions are the customer's.
7. No em dashes or en dashes.
