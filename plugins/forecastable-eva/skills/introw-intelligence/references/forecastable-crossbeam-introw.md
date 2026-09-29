# Introw with Forecastable and Crossbeam

Version: 2026-09-29. Sources: `introw-intelligence.md` tags, plus Forecastable's own recommendations
(labeled OURS).

## 1. Division of truth

| Question | System of record | Why |
|---|---|---|
| Which accounts overlap with which partner | Crossbeam | Introw only reads Crossbeam overlaps one way, for records worked in Introw [S45] |
| Deal amount, stage, close date | The CRM | Introw is CRM-native; it mirrors the CRM, it does not hold its own pipeline [S38] |
| Which partner is attached to a deal, and in which role | The CRM, written by Introw | Attribution lives in CRM properties, association labels, junction roles or custom objects [S34][S36] |
| Partner portal, registrations, enablement, payouts | Introw | Workflow and partner experience layer |
| Whether the partner actually changed the outcome, and the forecast | Forecastable | Introw records named attributions; it has no built-in sourced vs influenced model or forecast [S94] |

OURS: Introw's named attributions ("Sourced by", "Influenced by", "Reseller") are the right raw
material. Forecastable reads them, applies the customer's own sourced and influenced definitions from
their stack profile, and keeps the history. Never let Eva report Introw's revenue tiles as sourced
revenue; they count any deal with a partner attached.

## 2. Tenant health audit (run on first connection, then quarterly)

Pass, fail or unknown per item with the evidence. Route in brackets is the page to read [L1].

**A. Plumbing (P1: everything downstream depends on these)**
1. CRM tile is Connected, not Interrupted, Needs attention or Update available [`/settings/integrations`]. No email alert fires when it breaks [S40].
2. The CRM on the tile is one the plan includes (Pro is HubSpot only) [S2].
3. Salesforce: connection authenticates as a dedicated integration user, not an admin [S37][S23].
4. Deal attribution is configured in Object Linking; sourced and influenced are separate named attributions [S34][S36].
5. Opportunities overview count roughly matches partner-attached deals in the CRM [`/overview/DEAL`].
6. Crossbeam tile: connected by whom, record export usage percentage versus days to reset [`/settings/integrations` > Crossbeam].
7. Slack or Teams not showing "Update available".

**B. Partner coverage**
8. Share of partners with a published experience (portal) versus "Upgrade plan" or blank [`/partners`].
9. Share with Tier, Manager and Champion set.
10. Share "Inactive" in Engagement; last activity dates.
11. Partner Connect onboarded for partners who live in their own CRM or Slack [partner detail].

**C. Deal flow**
12. Submissions: pending age, share Auto accepted, last submission date [`/submissions`].
13. Forms: seeded defaults (owner Introw, 0 submissions) still live; approval gate mode set (Manual, AI Assisted, Autonomous) [`/forms`][S22].
14. Partners with submissions but Revenue $0 and 0 Opportunities (loop not closing) [partner detail].
15. Sleeping deal and closed won notifications actually sending [`/settings/notifications`].

**D. Enablement and engagement**
16. Announcements: unpublished AI Generated drafts; date of last published one [`/announcements`].
17. Goals, Courses, Certificates, Journeys, Deal Coaching, AI Agent in use or empty state.
18. Assets: views per asset; stale assets.

**E. Governance and risk**
19. Team: stale "Invite sent" users; Admin count [`/settings/team`].
20. CPQ: test products or deep discounts "Available to all partners" [`/products`].
21. Segments: override segments and who they widen access for (most permissive wins) [S56].
22. API credits meter and keys in use [`/settings/developers/api-keys`].

Report the top three fixes ranked by revenue impact, each with owner and "done when". Offer
Forecastable's help executing them, focused on the customer's stated priority partners.

## 3. Crossbeam inside Introw: what to watch

- The integration consumes the customer's Crossbeam record-export allowance [S45][S46]. The Introw
  Crossbeam page shows the meter. If usage is high relative to days left in the term, say so, name
  Introw as one consumer, and suggest the customer check what else is exporting before they run out.
  OURS: frame it as optimizing usage, never as blaming either vendor.
- Overlap flags on pending submissions check customers, prospects and open opportunities [S48]. They
  are a signal for the reviewer, not a verdict; channel conflict still needs the rules of engagement.
- Introw's "Crossbeam Co-Sell Partner Finder" skill [S47] overlaps with Eva's Crossbeam work. OURS:
  Eva's version reads Crossbeam through the browser first to save the customer's MCP credits and
  record exports, and writes the outcome into Forecastable so the attribution has history.

## 4. Recommendation plays (OURS unless sourced)

1. **Fix the plumbing before the program.** A broken CRM connection makes every Introw number stale.
   First recommendation in any audit where A fails.
2. **Name the attributions the way the customer defines partner impact.** Separate "Sourced by" and
   "Influenced by" (association labels on HubSpot Pro+, OpportunityPartner roles on Salesforce)
   [S34][S36]. Mirror the exact definitions from the Forecastable stack profile.
3. **Put a review gate on deal registration.** Auto accept is only safe for conflict-free lead
   shares. For deals use AI Assisted at minimum; accepted is final [S55][S22].
4. **Meet partners where they work.** Low portal engagement is normal; Partner Connect, Slack or
   Teams channels and the partner MCP are Introw's answer [S82][S79]. Recommend them before more
   portal content.
5. **Publish or delete the AI drafts.** Unpublished auto-announcements are a sign nobody owns partner
   comms. Assign an owner and a cadence; Eva drafts, a human publishes.
6. **Tier with goals, not labels.** Link tier requirements to goals so progress is live [S57].
   Promotions stay human-reviewed.
7. **Clean CPQ visibility.** Restrict discounts and test SKUs by segment or deal filter.
8. **Use workflows for the chase, Eva for the judgment.** Introw workflows handle deterministic
   nudges (task due, journey step) [S84]; Eva handles the cross-system follow-ups Introw cannot see.

## 5. What Eva does with Introw each week (OURS)

- Pull new and pending submissions and any in Error; chase the reviewer, never accept on their behalf.
- Pull deals with partner attribution changed this week; reconcile against Forecastable records.
- Flag sleeping partner deals and partners gone inactive among the priority partners.
- Check the CRM and Crossbeam tiles; alert on any status other than Connected or on record exports
  above 80 percent with more than 60 days left.
- Log confirmed partner touches to Forecastable through `eva-partner-influence`.
