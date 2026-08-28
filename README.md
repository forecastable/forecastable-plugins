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

Nothing else to prepare. There is no configuration file to write, no IDs to look
up, and no setup form. Eva does that part herself on the first run.

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

Updates are automatic. This marketplace declares no plugin version, so Claude
Code resolves each plugin to its current commit and picks up new work in the
background. To refresh immediately:

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

## Support

Questions, problems, or requests: [forecastable.com](https://forecastable.com)
