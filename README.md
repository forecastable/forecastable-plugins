# Forecastable plugins

Partnerships and co-sell plugins for Claude, from [Forecastable](https://forecastable.com).

## Before you install

Eva works from your live Forecastable data, so two things need to be true first.

1. **You have a Forecastable account**, and you can sign in to it.
2. **The Forecastable connector is set up in Claude.** Eva reads your accounts,
   plans and calendar through it. Without it she can still talk, but she cannot
   tell you anything about your actual partners. If you are not sure whether it
   is connected, ask us and we will check with you.

Two things that are **optional**:

- **Crossbeam.** If your organization has it connected, Eva uses it for overlap
  and partner signals. If not, she says so and works without it.
- **A calendar connection.** This turns on the daily triage of action items into
  plans. Everything else works without it.

An administrator configures company skills, knowledge, and schedules in EVA. You do not need to put organization IDs or credentials in the plugin.

## Install

In Claude Code:

```
/plugin marketplace add forecastable/forecastable-plugins
/plugin install forecastable-eva@forecastable
```

If the install summary says `Run /reload-plugins to activate.`, run that command.

From the command line instead:

```bash
claude plugin marketplace add forecastable/forecastable-plugins
claude plugin install forecastable-eva@forecastable
```

## First run, about two minutes

### Database-backed company workspace

The updated EVA workspace adds company skills, a reviewed knowledge base, shared procedure
selection, and Claude cloud routine configuration. Connect the authenticated Forecastable
`/mcp` or `/mcp/integration` endpoint; the restricted `/mcp/public` endpoint does not expose
these company-management tools. Authorize the skill, knowledge, and schedule scopes appropriate
to the user's role. Missing tools can mean a deployment or connection-scope prerequisite.

An administrator creates or uploads skills and knowledge in EVA. MCP writes update existing
records only. Shared procedures remain separate from company instructions, and company learning
never changes the distributed plugin. Knowledge changes from an agent remain drafts or review
items until an authorized person publishes them.

For scheduled work, the customer signs in to Claude and creates a cloud routine with the
Forecastable MCP connector. EVA generates the saved prompt and stores the schedule. Link only
the routine's dedicated API trigger ID/token through EVA's schedule editor; never supply a
Claude account login token. Forecastable owns the cadence, so avoid a second schedule in Claude.
Trigger acceptance is distinct from completion; the agent reports each existing EVA run and its
draft artifacts through MCP. Communications still require human verification, approval, and sending.

The five Alloggio fixture workflows are explicitly synthetic. They verify scheduling, activity,
and draft review without reading customer accounts or claiming live business outcomes.

**Start a new chat.** Plugins load when a chat begins, so a chat you already had
open will not see Eva yet.

**Type this:**

```
Ask Eva what she can do.
```

That one sentence is the whole setup. Eva will:

1. Look at your Forecastable organization and count your partner accounts.
2. Check whether a calendar and Crossbeam are connected.
3. Write her own config file so you never have to.
4. Tell you what she can do **today**, using your real partner names and real
   numbers, not a feature list.

You should get back something shaped like: *"You have 41 partner accounts. 12
have a plan attached. I can prep your next partner meeting, tell you who owes
what, or sweep for partners going quiet. Your calendar isn't synced, so I can't
do the daily triage yet."*

If she reports something missing, that is normal and not an error. She will tell
you what each missing piece would unlock, and everything else still works.

## Your first real task

Pick whichever of these matches something you actually need. Plain language is
fine; you do not have to learn any commands.

| Say this | What you get |
|---|---|
| `Who owes what right now?` | Every open commitment, who owns it, how late it is |
| `Prep my next partner meeting.` | An agenda built from what happened last time |
| `What's gone stale?` | Partners going quiet, dead plays, commitments with no owner |
| `Draft the handoff for [account].` | A forwardable note their rep can send as-is |

**Eva never sends anything.** Every email, message and introduction is a draft
that waits for you to approve it. She will say so explicitly each time.

## Teaching her

When Eva gets something wrong, tell her in plain words: *"That should have gone
to the Acme plan, not the company-wide one."*

She fixes what she filed, writes the correction down, and applies it from then
on. Corrections outrank her defaults, so you should not have to give the same
one twice. If you ever do, tell us, because that is a bug on our side.

## If something looks wrong

**She says she cannot see any accounts.** Usually a permissions setting on your
Forecastable organization rather than an empty program. Ask us and we will look.

**She answers as though she is a different assistant.** You may have another
plugin installed that provides a similar assistant. Disable the other one and
start a new chat.

**She reports nothing to do, and you know that is wrong.** Say exactly that. Eva
is built to tell the difference between a quiet week and a connection that is not
working, and she will re-check rather than insisting.

## Updates

This marketplace declares a version for each plugin release. Refresh the marketplace to check for updates:

```
/plugin marketplace update forecastable
```

## What is in here

### Eva, AI Partner Manager Assistant (`forecastable-eva`)

Eva is the accountability layer for a partnership: she makes sure the people on
both sides who said they would do something actually do it, including the people
who report to neither party.

She handles meeting prep, play assignment and forwardable handoffs, partner
success plans, commitment tracking and chases, staleness sweeps, and a daily
triage of action items into plans.

Eva drafts everything for your approval. She never sends on your behalf, and she
escalates judgment calls to your partnerships lead rather than guessing.

Eva reads your live Forecastable workspace, and Crossbeam when your organization
has it connected.

### HubSpot setup for Forecastable (`forecastable-hubspot-setup`)

Ships inside the same plugin. The standard for configuring a HubSpot portal
that Forecastable syncs from: the associated company carries the prospect, a
property carries the referring partner, lead source is mirrored on the Lead and
Deal objects with one internal name, sync filters match the records meant to
sync, and live properties are changed by a protocol rather than by hand.

Hand it to your HubSpot admin as-is, or say `Is our HubSpot configured for
Forecastable?` and Eva audits the portal against it.

### Partner influence tracking (`eva-partner-influence`)

Measures partner impact beyond sourced and influenced without partner-washing.
Eva inventories your data sources, proposes a metric menu by lifecycle stage for
your approval, then logs confirmed partner touches and compares them against a
matched direct group.

### Hyperscaler partner programs (`aws-partner-program`, `microsoft-partner-program`, `google-cloud-partner-program`)

Sourced, dated knowledge of the AWS, Microsoft and Google Cloud partner
programs: tiers and criteria, marketplace listings and private offers, co-sell,
and funding. Ask `Are we eligible for ISV Accelerate?` or `Prep the Microsoft
seller meeting`, and Eva turns the answer into steps with owners in your plan.

### Glean (`glean-intelligence`)

Glean administration and use: connectors, permissions, agents, MCP and the
Claude integration, and how Glean works alongside Forecastable and Crossbeam for
partner teams.

## Support

Questions, problems, or requests: [forecastable.com](https://forecastable.com)
