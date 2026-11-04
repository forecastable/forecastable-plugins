---
name: partner-program-intelligence
description: "Research, store and keep current what a company needs to know about another company's partner program or ecosystem (tiers, requirements, benefits, funds, co-sell, marketplace, fees, people, deadlines), as company knowledge in Forecastable with a dated history of every change. Use for 'research the X partner program', 'track X's ecosystem for us', 'what changed in the X partner program', 'keep us updated on X', 'how has X changed since', or a monthly refresh of a tracked program. Checks Forecastable's global knowledge first. Never sends."
---

# Partner program intelligence

Companies work inside other companies' partner programs: a cloud marketplace, a CRM app ecosystem, a payroll platform's referral program. Forecastable maintains **global knowledge** for the big programs many customers share (AWS, Microsoft, Google Cloud, cross-cloud vendors, Crossbeam, Introw). Everything else a company tracks for itself as **company knowledge**, and Eva builds and maintains it.

Run the `use-eva` loop first. Writing knowledge follows "Changing Eva" there: an admin's record publishes after review, and a non-admin's goes in as a change request for an admin.

## 1. Check what already exists

1. Search Eva for the program by name and common aliases (`searchEvaContext`, then `fetchEvaKnowledge` with `query`). Global knowledge from Forecastable wins: use it, never copy it into company knowledge, and only add company-specific notes (their tier, their partner manager, their deal history) in a separate company record.
2. If a company record exists, read it and the newest dated update record. Answer from them, or refresh them (section 4).
3. If nothing exists, build it (section 2). If the program is large and likely shared by many companies, also tell the user they can ask Forecastable to maintain it as global knowledge.

## 2. Research

Work outward from the source of truth. Spend effort on substance, not volume: one official page beats ten recaps.

1. **Official program pages**: overview, tiers and requirements, benefits, terms, fee schedules, program guides, FAQs, release notes or changelogs, partner directory. Public pages only. Never log in to a partner portal, never ask the user for a password, and never state a login-gated detail as fact.
2. **Official blog, newsroom and events**: launches, policy changes, leadership moves, partner keynotes.
3. **Partners and vendors**: blogs from partners and service vendors in that ecosystem. Useful, often early, sometimes wrong.
4. **Creators and analysts**: people who cover the program regularly, newsletters, podcasts, LinkedIn posts with substance.
5. **YouTube**: search for the program name plus "partner program", "partner summit", "keynote" and "what's new". Read each video's title, description, chapters and any linked post or show notes.
   - **If a transcript tool is connected** (a YouTube transcript connector or API), pull transcripts for the few videos that matter and extract the program substance.
   - **Most companies won't have one.** Then work from the description, chapters and linked material only. Say plainly that the video itself wasn't watched, and never attribute a claim to a video you have no transcript for. Note it as a lead to verify, with the link.

Label every fact by source: **OFFICIAL** (the program owner's own page), **VENDOR** (a partner or vendor), **CREATOR**, or **INDEPENDENT** (press, analyst). A fact found only from a vendor or creator, or only behind a login, is **unverified** and is written that way. Keep the URL and the date you read it for every fact.

## 3. Store it

Write one master record and keep it current, plus one dated update record per refresh. The dated records are the history: never delete or overwrite them.

**Master record**, titled `Partner program: <Program name>`:

- First line: `Version: YYYY.MM (built <date>). Last checked: <date>.`
- What it is and who it's for, in two lines.
- Tiers and how to qualify.
- Benefits and funds (MDF, credits, sponsorships, discounts), with amounts and who approves them.
- Co-sell and deal registration: how, where, timelines, rules.
- Marketplace and fees, if any.
- People: program leaders and the roles a partner deals with.
- Deadlines and dates for the next 90 days.
- What this means for this company, in plain language.
- Open questions and unverified items.
- Where to look next time: the pages, blogs, creators and channels that proved useful, so the next refresh is fast.
- Sources table: tag, label, title, URL, date read.

**Dated update record**, titled `Partner program updates: <Program name>, <Month YYYY>`:

- Changed facts as a table: fact, old value, new value, date of change if known, source and label.
- What was checked and found unchanged.
- New programs, funds or rules. People moves.
- Deadlines in the next 90 days.
- What this changes for the company, and any decision a person needs to make.

Use `createEvaKnowledge` for a new record and `updateEvaKnowledge` for the master, with tags for the program name and `partner-program`. Records land in review until approved; tell the user so.

## 4. Refresh

On request, or monthly if the company wants it:

1. Read the master record, its version and "Last checked" date, and the newest dated update.
2. Re-check the "Where to look next time" list for anything published since then. Re-read the official pages behind the facts most likely to move: fees, funds, tiers, deadlines, people.
3. Write the new dated update record, even if little changed ("checked, no change" is history too).
4. Update the master in place: replace changed facts, keep true ones, bump the version and "Last checked".
5. If the company wants this regularly, offer to set up a monthly scheduled task in their Claude that runs this section and reports the top changes. The report is a draft for a person; nothing is sent to anyone else.

## 5. Answer questions about change

For "what changed in X" or "how has X changed since August": read the dated update records for that period in order, oldest first. For each change give the from, the to, when it changed and the source with its label. Say where the history starts, and don't guess before it. For "what should we do about it", tie each change to what it means for this company, using their own partners, deals and plans from Forecastable.

## Rules

- Global knowledge is Forecastable's. Never copy or edit it; add company notes in a separate record.
- Public sources only. No logins, no passwords, no scraping behind paywalls.
- Unverified stays labeled unverified until an official page confirms it.
- Never claim to have watched a video without a transcript.
- No em dashes or en dashes in anything written.
- Draft only. Nothing goes to a partner, the program owner or anyone outside the company.
