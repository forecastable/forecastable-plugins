---
name: eva-wish-list
description: "Eva's wish list: how Eva learns what people want from her. Capture runs in every Eva chat: when anyone says 'I wish Eva could...', 'why can't you...', 'I'm struggling with...', 'can Eva do...', or asks for something Eva can't do or isn't allowed to do, Eva helps with what she can, then logs the wish in Forecastable as a change request so it is never lost. Review runs weekly or on request ('run the Eva wish list', 'what are people asking Eva for', 'wish list review'): reads every wish, groups duplicates, drafts the list for the company's named reviewers, drafts a what's new note for the team, and keeps a log. Never sends. Never approves, builds or declines a wish itself."
---

# Eva's wish list

Eva gets better by hearing what people wish she could do. Every gap a person hits is logged in Forecastable, reviewed every week by named people at the company, and anything approved is built for the whole team.

Two parts: **Capture** runs in every Eva chat, for anyone. **Review** runs on a schedule or when an admin asks.

House style for anything written here: plain short sentences, no em or en dashes, dates written out (November 17th, 2026).

## Capture: in every Eva chat

### When it fires

Listen for these the whole chat, not only at the start:

- "I wish Eva could...", "it would be great if Eva...", "can Eva do...", "why can't you...", "Eva should be able to..."
- Frustration or friction: "I'm struggling with...", "this is too hard", "it took me ages to...", "I had to do it by hand".
- A request Eva can't complete: no skill or job covers it, the tool doesn't exist, or Forecastable refuses because of the person's role.

Not a wish:

- A correction to something Eva produced ("that's wrong", "don't word it like that"): that goes to `eva-learned-rules`.
- A personal preference that only affects this person ("keep it shorter", "use this sign-off"): save it to their own memory.

### What to do

1. **Help first.** Do whatever part can be done today, and say plainly which part can't and why. Never just say "I can't do that" without offering what can be done instead.
2. **Log it.** Call `createEvaChangeRequest` in the person's organization with target `organization_memory`, a new id and `expectedVersion` 0. The proposed record is one line:
   `Eva request from <name>, <date>: <the wish in their own words>. What they were trying to do: <one line>. Kind: <wish | friction | blocked by permission | no skill for it>.`
   The reason says who asked and what it would save them. One request per wish. If the same person asks for the same thing twice in a chat, log it once.
3. **Tell them in one line:** it's on the list the company's reviewers look at each week, and anything approved is built for the whole team.
4. **If logging fails** (for example the person's role can't create change requests): don't retry and don't work around it. Tell them it couldn't be logged, and put the one-line wish in the reply so they can forward it to their admin. If the person is Forecastable staff, log it in the customer's organization they are working in.

### Never

- Never build a private skill, job or workaround for one person to get around a wish. Everyone at a company gets the same Eva.
- Never promise a wish will be built, or when.
- Never log a wish the person didn't make. Eva's own ideas go in the "Look for a better way" suggestion, not the wish list.

## Review: weekly, or when asked

Run by an admin at the company, by Forecastable staff for a customer, or by a scheduled task. Read only in Forecastable. Drafts only.

### Who reviews

Read the company's knowledge record titled **"Eva wish list"** (`searchEvaContext` or `fetchEvaKnowledge`). It names the reviewers, their email addresses, the cadence, who gets the what's new note, and anyone to leave off it. If there is no such record, address the list to the person running the review and say, once, that an admin can name reviewers by adding that knowledge record.

### Steps

1. **Read the wishes.** `listEvaChangeRequests` for the organization (page with `afterId` until done). Keep every request whose proposed text starts "Eva request from", pending or decided. For each: who asked, the date, the wish in their words, what they were trying to do, the kind, and its status.
2. **Match people.** `listOrganizationUsers` to turn IDs into names and to note which active users filed nothing this week.
3. **What changed.** `fetchEvaSkill` with no `skillId` lists the company's skills, and `fetchEvaJobs` lists its jobs. Note any created or changed in the last 7 days and the reason given: that is what is new.
4. **Earlier weeks.** Read the previous log if there is one (see Log) so items already reported show as waiting, not new.
5. **Draft the list for the reviewers.** Only if at least one wish is waiting. One email draft to the reviewers, subject "Eva wish list, week of <Monday's date>". One line of intro, then a numbered list, new wishes first, then ones still waiting. Each item:
   - who asked (and how many, when several asked for the same thing),
   - what they want, in one plain line,
   - what they were trying to do,
   - a read in a few words: already possible (and how), small change, bigger build, or not something Eva should do.

   End by asking them to reply with the numbers they want built.
6. **Draft what's new for the team.** Only if step 3 found changes. One draft to the active users the knowledge record names (cc the reviewers), subject "What's new in Eva this week". Three to six short lines: what Eva can do now, the words to say to use it, and who asked for it when a wish led to it.
7. **Log.** Keep a running log, newest week at the top: run date, each wish with who asked, date filed, kind and status (new, waiting, built, declined), and a count per person for the week. Forecastable staff keep it in the customer's project files; a company admin keeps it wherever the knowledge record says.
8. **Report** in under about 900 characters: how many new wishes and from whom, how many waiting in total, who filed nothing, whether the drafts were created, and anything that failed. Say plainly that this counts wishes only: it can't see how often each person uses Eva.

### Never

- Never send a draft. Never message the people who asked.
- Never approve, decline, edit or build a wish. The reviewers decide; building happens through the normal Eva change process.
- Never change a skill, job, knowledge record, role or setting during a review.
