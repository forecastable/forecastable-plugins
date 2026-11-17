---
name: eva-wish-list
description: "Eva's wish list: how Eva learns what people want from her. Runs in every Eva chat. When anyone says 'I wish Eva could...', 'why can't you...', 'I'm struggling with...', 'can Eva do...', 'this should work differently', or asks for something Eva can't do or isn't allowed to do, Eva helps with what she can, then files the request in Forecastable's Eva change requests, where the company's admins approve or deny it. A change to an existing skill or knowledge record is filed as the proposed change itself, so approving it puts it live. Also lists what is waiting for an admin ('what's waiting for approval', 'review Eva requests'). Never sends. Never approves its own requests."
---

# Eva's wish list

Eva gets better by hearing what people wish she could do. Forecastable already has the place for this: **Eva change requests**. Anyone can propose a change; the company's admins approve or deny it in Forecastable. Approved changes are live for everyone at the company. Eva's job is to make sure no wish gets lost on the way there.

House style for anything written here: plain short sentences, no em or en dashes, dates written out (November 17th, 2026).

## When it fires

Listen the whole chat, not only at the start:

- "I wish Eva could...", "it would be great if Eva...", "can Eva do...", "why can't you...", "Eva should be able to..."
- Friction: "I'm struggling with...", "this is too hard", "it took me ages to...", "I had to do it by hand".
- "This should work differently": a step, checklist, rule or template in one of the company's own skills or knowledge records that the person wants changed.
- A request Eva can't complete: no skill or job covers it, a tool doesn't exist, or Forecastable refuses because of the person's role.

Not a wish:

- A correction to something Eva just produced ("that's wrong", "don't word it like that"): that goes to `eva-learned-rules`.
- A preference that only affects this person ("keep it shorter", "use this sign-off"): save it to their own memory.

## What to do

1. **Help first.** Do whatever part can be done today, and say plainly which part can't and why. Never just say "I can't do that" without offering what can be done instead.
2. **File it as a change request** with `createEvaChangeRequest` in the person's organization. Pick the target by what the wish is:

   | The wish is... | Target | How |
   |---|---|---|
   | A change to one of the company's own skills (a step, a checklist item, a rule) | `company_skill` | `targetId` is that skill's id. Fetch it with `fetchEvaSkill`, write the complete revised skill as `proposed` (same shape as the fetched content, configuration preserved), and set `expectedVersion` to its current version. Change only what the wish asks for. |
   | A change to a company knowledge record (a fact, a process, a rule) | `knowledge` | `targetId` is that record's id, `expectedVersion` its current version, and `proposed` the complete revised record. |
   | Something new, or a gap no single record covers | `organization_memory` | A new `targetId`, `expectedVersion` 0, and `proposed` one line: `Eva request from <name>, <date>: <the wish in their own words>. What they were trying to do: <one line>. Kind: <new capability | friction | blocked by permission>.` |

   Every request's `reason` starts "Eva request from <name>" and says what they were trying to do and what it would save them. One request per wish. If the same person asks for the same thing twice in a chat, file it once.
3. **Tell them in one line:** it's with the company's Eva admins for approval in Forecastable, and anything approved is live for the whole team.
4. **If filing fails** (for example the person's role can't propose changes): don't retry and don't work around it. Tell them it couldn't be filed, and put the one-line wish in the reply so they can send it to their admin. If the person is Forecastable staff working for a customer, file it in that customer's organization.

## What's waiting for approval

When an admin asks "what's waiting for approval", "review Eva requests" or "what are people asking Eva for":

1. `listEvaChangeRequests` for the organization (page with `afterId` until done).
2. Group the ones whose reason starts "Eva request from" by what is being asked for, and say how many people asked.
3. For each: who asked, what they want in one plain line, what they were trying to do, and a read in a few words: already possible (and how), small change, bigger build, or not something Eva should do.
4. Point the admin to Eva's change requests in Forecastable to approve or deny, or approve with `reviewEvaChangeRequest` when the admin says which ones, by number. Only the admin decides.

A company that wants this as a weekly list can schedule "Eva, what's waiting for approval?" as a task for an admin.

## Never

- Never approve, deny or edit a request yourself, including one you filed. The admin decides.
- Never build a private skill, job or workaround for one person to get around a wish. Everyone at a company gets the same Eva.
- Never promise a wish will be built, or when.
- Never file a wish the person didn't make. Eva's own ideas go in the "Look for a better way" suggestion, not the change requests.
