# Forecastable plugins

Partnerships and co-sell plugins for Claude, from [Forecastable](https://forecastable.com).

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
