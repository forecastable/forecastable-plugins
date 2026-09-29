# Monthly refresh protocol

Runs once a month from the `Glean intelligence monthly refresh` scheduled task (cloud). Writes only to
the claude.ai Project "AI Alex & Eva Build". Never edits the shipped skill directly; the Monday plugin
release copies the approved files into `Skills/glean-intelligence/`.

## Inputs

- Project doc `claude/glean/glean-intelligence.md` (current master)
- Project doc `claude/glean/creator-registry.md`
- Project doc `claude/glean/forecastable-crossbeam-glean.md`
- The previous `claude/glean/whats-new-YYYY-MM.md`, if any

## Steps

1. **Read** the three files above. Note the version date and every "Last checked" date.
2. **Glean docs delta.** Fetch `https://docs.glean.com/llms.txt` and `https://docs.glean.com/release-notes/`
   (or use the Glean Docs MCP `docs_search`). List pages new or changed since the last version date.
   For every fact tagged `[D..]` in sections 0, 2, 5, 10 to 13 and 21, re-fetch the page as raw
   Markdown (URL plus `.md`) when the release notes touch it. Fix anything that changed.
3. **Walk the registry.** For each Tier 1 and Tier 2 creator, check the listed locations for items
   published since its "Last new item" date. YouTube: list the latest videos and pull transcripts for
   Glean-specific ones (TranscriptAPI). Extract only admin, usage, governance, cost, adoption, agent,
   MCP and partner-team substance. Skip marketing without substance. Tier 3 only in Jan, Apr, Jul, Oct.
4. **Discover.** Run the discovery queries at the end of the registry for the last 45 days. Add real
   finds to the Watchlist with a reason. Promote per the promotion rule. Move creators with two empty
   checks to Dormant.
5. **Resolve conflicts and unverified items** in section 23 where new evidence settles them. Move
   settled items into the body with a source.
6. **Update the master file.** Edit in place, keep the section structure, keep source tags, add new
   tags at the end of the right table. Bump the version to `YYYY.MM` and the built date. Do not
   delete facts that are still true; replace facts that changed and note the old value in the
   what's-new file.
7. **Update the plays file** only if a change affects Forecastable, Crossbeam or partner-team use
   (for example a new Crossbeam MCP tool, a HubSpot connector change, a new MCP limit).
8. **Write `claude/glean/whats-new-YYYY-MM.md`:** changed facts (old, new, source), new features,
   new creators, promotions and demotions, anything that changes an Eva or customer recommendation,
   and items needing a human decision.
9. **Quality gates** before writing:
   - Zero em dashes and en dashes in every file (scrub with a script).
   - Every new fact has a source tag that resolves in the Sources table.
   - Vendor benchmarks labeled VENDOR.
   - No customer names, internal pricing or internal economics in any file.
   - Keep every `VALIDATE-OK` annotation on the line it covers. The customer plugin build gate needs
     them, and they must move with the line if the line is edited.
   - The master file still opens with the version line and the twelve things.
10. **Write** the updated files back to the same Project paths with `project_write`.
11. **Tell Alex** in one short Slack DM to self (or the run summary if Slack is unavailable): version,
    top three changes, new creators, anything needing a decision, and the line "Ships at the next
    Monday release after approval." Draft only; the DM to self is the only message sent.

## What the refresh never does

- Never pushes to GitHub or edits the plugin source.
- Never sends anything to a customer or partner.
- Never removes a guardrail or a section 23 caveat without new evidence.
- Never adds a creator on the strength of one marketing post.
