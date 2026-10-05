# Partner and Ecosystem Events Intelligence

Version 2026-10-04 | Next refresh 2026-11-04 | Owner: Eva (Forecastable) | Scope: B2B events, partner and ecosystem events, and the Crossbeam + Clay data layer that plans, runs and measures them.

Conventions. Every factual claim carries a source tag [E#] (section 11). Anything marked OURS is a Forecastable recommendation, not a sourced fact. Source labels: VENDOR means the publisher sells an event, partner, data or services product that benefits from the claim (agencies included); INDEPENDENT means analyst, academic or press with no product stake in the number; INTERNAL means Forecastable's own verified notes. Self-reported survey numbers are flagged as such. Nothing here is legal advice.

---

## 1. Why events in ELG

**The macro case.**
- 88% of 1,058 US marketers call events a key revenue driver; 66% say in-person events generated the most revenue; 52% attribute at least half of 2024 closed-won deals to events; 72% say prospects close faster after attending (self-reported, Jan to Feb 2025) [E24].
- 78% of organizers call in-person conferences, summits and conventions their most impactful marketing channel [E20].
- Forrester (417 respondents, Jan to Feb 2026): 37% are increasing event budgets, 31% declining; budget splits 49% hosted vs 51% sponsoring third-party events; the top objective is net-new leads (73%) [E25].
- The format shift favors partner-sized events: 63% plan more hosted intimate networking, 52% more small in-person events under 200, 42% more webinars, only 18% more large events over 200 [E25]. In 2025, two-thirds of event teams had flat or declining budgets for the second year running, and only 12% planned more large gatherings [E26].
- Measurement is the weak point. Only 44% measure event impact (ROI/ROO) and 30% use many metrics but struggle to show impact [E25]. 40% of organizers report difficulty proving event ROI in 2026, down from 70% in 2025 [E20]. Fewer than one in five teams have integrated event platforms into the wider stack [E26].

**The partner multiplier.**
- In Crossbeam network data (as of 2024-10-28), involving partners lifted win rate 11.7% on average, rising to 37.1% for companies with 50+ connected partners and 58.6% where 75 to 100% of sales seats used Crossbeam [E17].
- Crossbeam's 2023 State of the Partner Ecosystem: deals are 53% more likely to close and close 46% faster when a partner is involved [E18].
- 48% of GTM teams aligned with partners report shorter sales cycles (PartnerStack/Wynter 2026) [E32].
- At the Nearbound Summit, Gainsight's field and partner marketing lead reported 50% of pipeline attributed (Q3) and a 3x pipeline increase from partner co-marketing events. These are speaker-reported, unaudited [E6].
- The ELG book lists "co-host events" as a core co-marketing motion for shared target accounts, and says to measure co-marketing campaigns on pipeline, engagement and win rate [E8][E9].

**The anchor proof (Clay, Sculpt 2026).** Clay's Head of Solution Partners, Tyler Swanson, built a per-partner event-strategy dashboard over one weekend. It combines Snowflake MCP (accounts, ARR, open opps), Crossbeam MCP (partner overlap), Clay MCP (contacts by role) and the Zuddl API (registration and ticket data). He built it in Claude Code, deployed it on Lovable, and gave each partner a password-protected link [E1]. Partners GoNimbly and demandDrive used it and gave positive feedback. Sculpt itself is a San Francisco GTM conference built around hands-on workshops where attendees build workflows [E2]. No outcome numbers were published, because the event (2026-10-08) had not happened when the study went out [E1]. Clay has about 150 partners and 500 to 1,000 employees [E1].

**OURS: the thesis for Eva.** Events are the one GTM moment where both partners' sellers, both partners' customers and shared prospects sit in the same place on the same day. Overlap data turns an event from a lead-capture exercise into a co-sell sprint. Eva's job is to make sure every seat, meeting and dinner chair maps to an overlap account and a named partner owner.

---

## 2. Event formats and when to use each

Cost bands are only shown where a source gives them. "Attend" is the sourced registration-to-attendance rate.

| Format | Primary goal | Partner role | Cost band (sourced) | Attend | Best metric |
|---|---|---|---|---|---|
| Co-hosted executive dinner (8 to 14 guests) | Advance named overlap opps; exec access | Co-host; each side brings 3 to 4 accounts; customers seated next to prospects [E29] | $300 to $1,500+ per head; 12-person standard dinner about $5k to $10k all-in [E29]; $1k to $3k per meeting [E28] | 70% exec dinners, 52% networking dinners [E27] | Opps advanced per seat; attendee to opp 30 to 50% [E28] |
| Roundtable (8 to 15) | Reference-led persuasion, discovery | Partner brings customers as peer voices [E29] | Same per-head tiers as dinners [E29] | 61% [E27] | Meetings booked within 30 days [E29] |
| Side event at a third-party conference (dinner, breakfast) | Borrow a conference's audience | Co-host splits the F&B minimum; partner invites its accounts | Venue often on a food-and-drink minimum; main cost is F&B [E30] | Over-invite: attendees are triple-booked [E30] | Overlap accounts in room |
| Co-hosted webinar | Top and mid-funnel education; integration launch | Co-presenter; co-promotes to its list | Not sourced | 40% avg (26,190 webinars) [E23] | Overlap-account registrants; on-demand completion (91%) [E23] |
| Workshop / working session (cohort) | Mid-funnel activation; use-case adoption | Co-teaches; funds or fills seats | Not sourced | Customer/partner events 62% [E27] | Accounts with a joint plan after the session (OURS) |
| Booth sharing / partner pavilion at a big trade show | Reach at scale | Shares the booth, staffs it, runs joint demos; Crossbeam invite-link QR codes on booth banners recruit new mapping partners on the spot [E15] | Tier 1 sponsorship $1.5k to $3k per meeting; mid-tier $2.5k to $5k [E28] | Booth meeting show rate 40 to 60% [E28]; vendor-owned conferences 19% [E27] | Cost per qualified meeting |
| Hospitality suite | Exec meetings off the floor | Co-host | $3k to $6k per meeting [E28] | n/a | Meeting to qualified opp 40 to 60% [E28] |
| Your user conference with partner sponsors | Monetize and activate the ecosystem; partner-sourced pipeline | Sponsors; speakers; buy packages | Paid events average about $84k revenue [E21] (ticketing, not sponsorship) | 52% avg across Bizzabo events [E21] | Partner-attributed pipeline per sponsor (OURS) |
| Partner's user conference (you sponsor) | Reach the partner's installed base | Host; you are the sponsor | Not sourced | n/a | Overlap customers met (OURS) |
| VIP / sport experience | Relationship, late-stage deals | Co-host | Not sourced | 86% [E27] | Late-stage opps influenced |

How to sequence the funnel: big conferences for top of funnel, use-case workshops for mid-funnel, curated in-person community events for bottom of funnel [E6]. For online formats, a speaker-recommended split is 20 minutes of thought leadership, 3 minutes of demo and 2 minutes of CTA [E6].

OURS rules of thumb:
- Under 30 overlap accounts with a partner: dinner or roundtable, not a webinar.
- Over 200 overlap accounts: webinar or workshop series, then dinners for the top decile.
- Never buy a booth for partner reasons alone. Buy it when your own ICP density at the show justifies it, then layer partner dinners on top.

---

## 3. Partner selection for events using overlap data

**Sourced inputs.** Pick co-hosts from the partners with the highest customer and prospect overlap, plus partners of partners who share your ICP. Pull candidate lists from Crossbeam, CRM and LinkedIn, then filter by tech stack, integration fit and economic value [E6]. The Crossbeam MCP exposes the signals needed:
- `get_partner_context`: overlap counts, open deals, potential revenue, partner score, win rate, deal size, recency.
- `find_overlapping_accounts_and_leads`: filter by partner, population, segment and partner score.
- `find_partner_shared_contacts`: decision makers, economic buyers and exec sponsors the partner shares.
- `find_overlapping_partners`: which partners have a given account.
- `get_ecosystem_activity`: partner deals opened, partner deals won, greenfield.
- `get_list_link`: a shareable list.

All of these come from [E3]. Per partner, `get_partner_context` also returns `total_overlap_count`, `shared_overlap_count`, `coverage_percentage`, `last_active` and `is_offline_partner` [E19].

**OURS: Event Partner Score (0 to 100).** Compute it per partner, per event. Here, "event target list" means your target accounts for this event: registrants, invitees, or ICP accounts in the event's region.

| # | Factor | Weight | How Eva measures it |
|---|---|---|---|
| F1 | Target overlap density | 25 | Event target accounts that are the partner's customers or open opps ÷ event target list size. Source: `find_overlapping_accounts_and_leads` filtered to the event population |
| F2 | Pipeline at stake | 20 | Your open-opp amount (or ARR for expansion events) on F1 accounts. Source: CRM, then intersect |
| F3 | Warm-path depth | 15 | Share of F1 accounts with at least one partner-shared contact at Director+ or buying role. Source: `find_partner_shared_contacts` |
| F4 | Data reciprocity | 10 | `shared_overlap_count` ÷ `total_overlap_count`. A partner showing counts only scores 0 here |
| F5 | Partner co-sell health | 10 | Partner win rate and `last_active` recency from `get_partner_context`, plus open joint deals |
| F6 | Audience pull | 10 | Whether the partner will invite its own customers: a named partner marketer and a list size commitment |
| F7 | Customer proof | 10 | Mutual customers willing to speak or attend (reference seats, per [E29]) |

Gates. A partner that fails any of these is not a co-host, whatever its score:
- G1: the partner shares at least Overlapping Accounts level on customers and opps.
- G2: there is a named partner AE or PM owner for the event.
- G3: the partner agrees to the attendee-data terms in section 6.
- G4: for Free-plan Crossbeam customers, the MCP credit budget covers the calls (Free 50 per year, Connector 500, Supernode 2,500, Enterprise 5,000; Free and Connector cannot buy packs) [E19].

Bands:
- 70 and up: co-host. Joint invite list, joint dinner, shared dashboard.
- 50 to 69: guest partner. Invited to bring 2 to 4 accounts to your dinner.
- Under 50: account-level asks only. Use warm intros on specific accounts, no co-hosting.

Cap co-hosts at 2 per dinner (OURS: more than 2 makes it a vendor parade). Re-score at T-14 once registration data is in.

**OURS: three overlap cuts to run per event.**
1. Registrants or invitees x partner customers. Who can the partner warm up?
2. Your open opps x partner customers or opps. Who needs a partner exec at the dinner?
3. Partner customers not in your CRM. Use `find_new_accounts` [E3] to find greenfield seats for the partner to fill.

---

## 4. The Sculpt 2026 pattern decomposed

What Clay built [E1]:
- **Data:** Snowflake MCP, Crossbeam MCP, Clay MCP and the Zuddl API.
- **Build and delivery:** a dashboard built in Claude Code, shipped on Lovable, with one password-protected link per partner.
- **Summary metrics:** overlap accounts, mutual customers, warm-intro targets, ARR in overlap, open pipeline, tickets used.
- **Account table:** filters by Clay status, partner status and event attendance.
- **Drill-down:** open opps, key contacts by role, registration status.

| Layer | Clay's tool | Question it answers | Forecastable / Eva equivalent (OURS) | Gaps and risks |
|---|---|---|---|---|
| 1. GTM system of record | Snowflake MCP: accounts, ARR, open opps [E1] | What is each account worth to us? | Customer's CRM through HubSpot MCP or Salesforce. For accounts already worked in Forecastable: `listAccounts`, `listOpportunities` | Most mid-market customers lack a warehouse, and ARR often is not a CRM field. Eva must state which amount field she used. ARR in overlap needs an ARR field or a defined proxy |
| 2. Ecosystem overlap | Crossbeam MCP [E1] | Which partners touch which accounts? | Same. `find_overlapping_accounts_and_leads`, `find_overlapping_partners`, `get_partner_context`, `get_ecosystem_activity` [E3] | MCP credits are capped by plan, and per-tool credit cost is not published [E19]. Free plan cannot create or save Lists and sees up to 50 overlap records [E19]. Sharing level limits what is visible |
| 3. Buying committee contacts | Clay MCP [E1] | Who do we invite and meet at each account? | `find_partner_shared_contacts` first: partner-sourced and already warm [E3]. Then Clay MCP for gaps, recommended for 1 to 20 contacts per task [E49]. Then a Clay table for volume. Store results as relationship maps or buying groups in Forecastable | Clay MCP credit use (500 free credits on first connect; admins set per-rep limits) [E49]. Contacts from a partner carry the partner's consent basis, not yours (section 6) |
| 4. Event registration | Zuddl API: registration and ticket data [E1] | Who is coming, and who used a ticket? | Event platform API or webhook (section 8), or a CSV export. Hold the invite and registrant list as an Engage list keyed to the event | Forecastable has no native event object. Ticket-used vs registered needs check-in data. Luma webhooks need Luma Plus [E43] |
| 5. Join and score | Claude Code logic [E1] | Which overlap accounts are registered, which are warm-intro targets? | Eva joins on domain: event registrant domain → CRM account → Crossbeam overlap → partner contacts. Score using section 3 F1 to F3 | Domain mismatches (subsidiaries, personal emails). Eva must report the match rate and the unmatched count |
| 6. Delivery to partners | Lovable app, password per partner [E1] | What does each partner see? | One private Artifact or doc per partner, or a Crossbeam shared list via `get_list_link` [E3]; Crossbeam Shared Lists auto-push updates to the partner [E14]. Joint plan per partner in Forecastable (plan, milestones, tasks) | Exposure risk: a per-partner page may show your ARR and pipeline, which Crossbeam sharing normally hides. Partners see only shared fields on matching records inside Crossbeam [E14]. A password link is shareable onward |
| 7. Metrics | Overlap, mutual customers, warm-intro targets, ARR, open pipe, tickets used [E1] | Is the event worth working with this partner? | Same six, plus OURS: meetings booked per partner, intros requested vs made, post-event opps by attribution cell (section 7) | Clay's view has no outcome layer yet (no results published [E1]). Eva must add T+30 and T+90 readouts |

Note: earlier Forecastable material lists older Crossbeam MCP tool names [E4]; use the current list in [E3]. Crossbeam's own 2026 programming is AI-and-signals webinars, not partner-event playbooks [E5].

**OURS: what Eva adds beyond Sculpt.**
1. A commitments ledger: every warm-intro target gets a named partner owner and a due date before T-7.
2. A consent flag per contact (section 6).
3. Post-event attribution in the 2x2 (section 7).
4. One-click drafts of invite and intro asks, drafts only, with a named human sender (house rule, INTERNAL [E55]).

**OURS: minimum viable Sculpt for a Forecastable customer with no warehouse.** CRM + Crossbeam MCP + event CSV, joined by Eva. Deliverable: one page per co-host partner with these columns:
- account
- our status
- partner status
- registered / attended
- our owner
- partner owner
- warm contact
- ask

Build time target: 1 working day per event once the event CSV exists.

---

## 5. Pre, during and post runbook

Owners:
- **PM:** customer's partner manager.
- **FM:** field or event marketer.
- **AE / SDR:** customer sellers.
- **PAE / PPM:** partner's AE and partner's PM.
- **RevOps:** customer's revenue operations.
- **Eva:** drafts and data.

Timings are relative to event day T. All outreach is drafted by Eva and sent by a named human (INTERNAL [E55]).

### 5.1 Pre-event

| When | Step | Owner | Done when |
|---|---|---|---|
| T-60 | Pick the format (section 2) and co-host partners (section 3 score, gates G1 to G4) | PM, FM; Eva scores | Co-host list signed off, at most 2 per dinner |
| T-60 | Sign the data terms with co-hosts: who controls the attendee data, what is shared, retention, opt-in wording (section 6) | PM, legal | Written terms exist; registration form carries a partner-named opt-in, not pre-ticked [E33][E34] |
| T-45 | Build the target account list: ICP x region x overlap cuts 1 to 3 (section 3) | Eva, RevOps | List with account, owner, partner, overlap type, amount; match rate reported |
| T-45 | Contacts per target account: partner-shared contacts first [E3], Clay to fill buying roles [E49][E48] | Eva | At least 2 named contacts per tier-1 account, or the gap flagged |
| T-40 | Invite math: dinners need about 3x headcount in named invitees (35 to 45 names for 12 seats), with a 25 to 40% invite-to-confirm rate and 15 to 25% final-week drop [E29]; size by format attendance (section 9) | FM | Invite list sized to the format's attend rate |
| T-35 | Personal invites from the AE and the partner AE, not marketing blasts; partner invites its own customers | AE, PAE; Eva drafts | Every tier-1 account has an invite from the person closest to it |
| T-30 | Warm-intro asks: for each overlap account with an open opp, a specific ask to the PAE ("intro to [name] before the dinner") | PM; Eva drafts | Ask logged with owner and due date in the commitments ledger |
| T-21 | Meeting booking for the conference: pre-booked meetings convert to qualified opps at 25 to 40% [E28] | SDR, AE | Meetings on calendars with an account brief attached |
| T-14 | Pull registrants via API or webhook (section 8); re-run overlap; re-score partners | Eva | Registrant x overlap table refreshed; new warm targets flagged |
| T-7 | Per-partner page (section 4 layer 6) and joint target list with "who meets whom" | Eva, PM | Each co-host has its page and its asks |
| T-5 | Co-hosted virtual sessions: rehearse with the partner, share draft decks and scripts, run tech tests days ahead, and assign a colleague to watch as an attendee [E7] | FM, PPM | Rehearsal held; run-of-show signed off |
| T-3 | Reminder cadence; executive dinners show 80 to 90% when meetings are confirmed [E28]. Fill dropouts from the waitlist | FM | Confirmations re-verified; waitlist promoted |
| T-1 | One-page brief per meeting: account, opp stage, partner relationship, contacts, ask | Eva | Brief in each owner's inbox |

### 5.2 During

| When | Step | Owner | Done when |
|---|---|---|---|
| T0 | Seating: mix customers and prospects half and half at roundtables [E29]; seat each PAE next to its overlap accounts (OURS) | FM, PM | Seating chart maps every overlap account to an owner |
| T0 | Meeting ops: check-ins captured in the event platform (Zuddl flips HubSpot status from RSVPed to Attended on check-in [E35]); log no-shows | FM | Attendance data in CRM the same day |
| T0 | Booth: badge scans or exhibitor leads API (Swapcard [E45]); tag each scan with the partner if the partner staffed the conversation (OURS) | FM | Every scan has a partner tag or "none" |
| T0 | Dinner capture: each host writes 3 lines per guest within 2 hours (what they said, next step, partner role) | AE, PAE | Notes in CRM or Forecastable |

### 5.3 Post-event

| When | Step | Owner | Done when |
|---|---|---|---|
| T+2h to T+24h | Tier-1 follow-up. Personal, references the conversation, makes promised intros now [E30][E29]. Speed matters: firms that contacted a lead within an hour were nearly 7x as likely to qualify it as those that waited longer, and over 60x versus 24+ hours (online leads, 2011) [E31] | AE, PAE | Every tier-1 contact has a sent personal message |
| T+24h | Tier-2 follow-up; tier-3 to nurture. A practitioner tiering model: score 8+ within 2h, 5 to 7 within 24h [E52] | SDR | Sequences enrolled; segments for attended vs registered no-show |
| T+48h | Enrich attendees and booth scans in Clay (title, seniority, company, signals), score, route to owner [E52][E48] | Eva, RevOps | Every lead has an owner and a score |
| T+3d | Partner sync: share the agreed overlap outcomes with co-hosts through Crossbeam shared lists, not raw spreadsheets (section 6) | PM | Partner sees the next step on its accounts |
| T+7d | Personal nurture touch on non-converted tier-1 [E29] | AE | Touch logged |
| T+14d | Attribution tagging: event-sourced vs influenced; partner-sourced vs influenced in the Crossbeam Attribute workspace [E10] | RevOps, PM | Every post-event opp has both tags |
| T+30d | Pipeline check: meetings held, opps created or advanced [E29] | Eva | 30-day readout per partner |
| T+90d | Pipeline readout vs cost. Target 3 to 5x all-in cost in 90-day attributed pipeline, best-in-class 10 to 15x (vendor benchmark) [E28] | Eva, RevOps | Readout delivered; decision to repeat or drop each partner |

### 5.4 Clay-specific event workflows

**Sourcing attendees.** Clay has no native attendee-list scraping feature, per a practitioner consultancy [E51]. Clay's own community answer on 2026 attendee lists could not be retrieved (open item). The working pattern:
- Scrape sponsor, exhibitor and speaker pages with Claygent or an Apify actor [E50][E48].
- Scrape LinkedIn event posts [E51].
- Enrich through waterfall providers [E48].

**Pre-event targeting.**
- Clay's event-leads tool defines an event and title target, searches its company database, and waterfalls 150+ providers for verified emails.
- Output goes to CSV, Salesforce, HubSpot or sequencers [E48].
- A Terrapinn case cut manual research from about two months to about ten minutes (vendor case) [E48].

**Trade-show intelligence.** An agency pattern:
- Scrape the event.
- Run an AI ICP fit check.
- Match personas.
- Enrich contacts.
- Generate a per-prospect outreach angle.
- Show it on a Claude Code dashboard.

The agency reported 415 ICP-matched companies across 21 events [E53].

**Post-event.**
1. Export attendees.
2. Import to Clay.
3. Enrich with Claygent.
4. Add signals.
5. Score.
6. Push by tier to the sequencer [E52].

**In-assistant.** Clay MCP works inside Claude, ChatGPT and Codex for 1 to 20 contacts per task. Use the full Clay platform for volume [E49].

**Ingest.** Clay community threads document webhook sources into Clay tables [E56]. OURS: use an event platform webhook (Zuddl, Luma Plus, Splash Simple Postback, Goldcast) pointing at a Clay webhook table for near-real-time registrant enrichment.

---

## 6. Data-sharing and privacy rules for attendee lists with partners

**Sourced.**
- **Crossbeam sharing.** Partners never see your full customer or pipeline lists, only the shared fields on matching records under your sharing configuration [E14]. Sharing is set per population at four levels: All Accounts, Overlapping Accounts, Counts Only, Hidden [E19].
- **CSV and offline lists.** Crossbeam CSV uploads are static, need Company Name and Website (Email for people), and are capped at 15 MB [E12]. Offline partners (partners not on Crossbeam) can be mapped from a CSV or Google Sheet; Free allows one [E13].
- **GDPR consent for partner email.** EU attendees must actively opt in, through a registration-form checkbox, to receive emails from sponsors or partners. Boxes cannot be pre-checked or bundled with terms [E34]. Receiving partners remain responsible for their own compliance [E34].
- **Lawful bases (UK/EU).** Consent must name which sponsors get the data, be a separate unticked box, and be withdrawable. Legitimate interest needs a balancing test plus transparency and an easy opt-out. Without the delegate's direct consent, sponsors cannot use PECR-regulated channels (email, SMS) for marketing. Joint organizers may share as joint controllers but need specialist advice [E33].
- **Consent age and contracts.** The ICO recommends not relying on consent older than six months for first contact. Use contracts that follow the ICO Data Sharing Code [E33].
- **Roles.** The organizer is the data controller; event tech vendors are processors that the controller must audit and document [E34].

**OURS: Eva's operating rules.** These are defaults, not legal advice; customer counsel overrides.
1. **Accounts over people.** Share account-level overlap through Crossbeam (shared lists, list links), not attendee spreadsheets. Crossbeam's field-level sharing is the privacy layer; raw lists bypass it.
2. **People only with a basis.** Share a named attendee with a partner only if the registration form carried a partner-named opt-in, or the partner co-hosted under written joint terms. Otherwise share the account name and "attended: yes" at most.
3. **Name the co-host on the form.** For co-hosted events, list the co-host by name in the opt-in text. "Our partners" is not specific enough under the sourced consent standard [E33].
4. **Field minimization.** Share name, title, company, attended or no-show, and the agreed next step. Never share session-level behavior, poll answers or dietary or accessibility data.
5. **Retention.** Partner deletes, or stops using for marketing, attendee personal data 90 days after the event unless an opp exists. EU contacts without consent go to account-level only.
6. **No laundering.** A partner-shared contact (from `find_partner_shared_contacts`) is used for warm-intro routing through the partner. It is never loaded into your cold outbound sequencer as a net-new lead without your own basis.
7. **Per-partner pages show only what Crossbeam sharing already exposes to that partner.** Your ARR and opp amounts appear only if the customer's partner manager approves it in writing for that partner. This is a stricter default than the Sculpt dashboard [E1].
8. **Log it.** Record what was shared, with whom, on what basis and when, on the partner's Forecastable plan.

---

## 7. Measurement and attribution

**Definitions.** Crossbeam's are sourced [E10]; the event ones are OURS.

| Term | Definition |
|---|---|
| Partner-sourced | Opp originated directly from a partner [E10] |
| Partner-influenced | A partner contributed after the opp was already in play [E10] |
| Event-sourced (OURS) | Opp created within 90 days after a contact's first attended event touch, where the account had no open opp and no active sales sequence at registration |
| Event-influenced (OURS) | An open opp, or one created within the window but failing the sourced test, where a contact on the opp attended or met at the event within 90 days before close or stage advance |

**The 2x2 Eva reports per event (OURS).** Each opp lands in exactly one cell per dimension.

| | Partner-sourced | Partner-influenced | No partner |
|---|---|---|---|
| Event-sourced | A | B | C |
| Event-influenced | D | E | F |

**Numbers to report.** Always as counts and amounts, with stated windows.
1. Overlap accounts in the room: attended, divided by targeted.
2. Meetings held, and meetings with a partner present.
3. Event-sourced pipeline: A + B + C.
4. Event-influenced pipeline: D + E + F.
5. Partner-involved event pipeline: A + B + D + E, by partner.
6. 90-day pipeline divided by all-in cost [E28].
7. Closed-won at 12 months divided by cost. Vendor benchmark: target 1 to 3x, best-in-class 5 to 10x [E28].
8. Missed coverage: event attendees at accounts with partner overlap but no partner engagement. This mirrors Crossbeam's "with coverage, no engagement" view [E16].

**Dedupe rules (OURS).**
- One opp counts once per dimension. Never add event-sourced and partner-sourced totals together.
- Report cell A explicitly: that is where the event team and the partner team will both claim credit.
- Sourced beats influenced in the same dimension. If an opp qualifies as event-sourced, it is not also event-influenced.
- Multi-partner opps: list every partner in Crossbeam attribution, which supports adding more than one partner [E10]. Credit the pipeline amount once in totals and per partner in the by-partner view, and label that by-partner view as non-additive.
- Multi-event opps: the first event that meets the sourced test owns "sourced"; later events can only be "influenced".
- Freeze windows: Crossbeam's Salesforce attribution push syncs every 12 hours [E11]. Take snapshots at least 24 hours after tagging.
- Model choice: one vendor recommends last-touch or W-shaped for conferences and multi-touch or time-decay for virtual events. W-shaped gives 30% each to first touch, lead creation and opp creation [E22]. OURS: report the 2x2 on rules first; show model-weighted dollars only as a secondary view. 42% of companies use multi-touch for partner attribution, 31% first-touch, 19% last-touch [E32].

**Where tags live.**
- Event platform → CRM: campaign or marketing event membership with status. Zuddl's HubSpot sync uses Marketing Event records and RSVPed/Attended statuses [E35]; Goldcast writes Salesforce custom activities [E41].
- Partner attribution: Crossbeam Attribute workspace and Salesforce attribution push, on the Supernode plan [E10][E11].
- Event-attribution fields: OURS proposal, `event_attribution` (sourced/influenced) and `event_id` on the opp, set by RevOps at T+14.

---

## 8. Event tech stack: APIs and integrations

The "getting registration data out" column gives the shortest path to a registrant file Eva can join to overlap data.

| Platform | API | Webhooks | CRM / MAP native | Getting registration data out | Sources |
|---|---|---|---|---|---|
| Zuddl | REST; API key in Authorization header; US `api.zuddl.com`, EU `api.eu.zuddl.com`; limits 10 req/s, 100 concurrent, 10,000/day (raise via CS) | Ticketing webhook reference exists in docs | HubSpot, bidirectional: registrants create or update contacts as RSVPed, check-in flips to Attended, no-shows stay Registered; engagement (polls, Q&A, booth scans, dwell) as timeline activities; uses HubSpot Marketing Event records. Salesforce integration documented | API pull or HubSpot Marketing Event membership. Clay's Sculpt build used the Zuddl API [E1] | [E35][E36][E37] |
| Bizzabo | REST at `api.bizzabo.com/v1`; registrations and contacts resources; Stoplight docs | Listed as an API feature | HubSpot app: registrations, attendee info and engagement into Contacts, timeline, lists, companies. Salesforce: guide exists, not verified here | API List Registrations, or HubSpot lists | [E38][E39] |
| Splash | API v2.2; OAuth 2.0 with client ID and secret from your CSM; Events, GroupContacts (guests), Contacts | "Simple Postback" outgoing webhook, configured in the UI at org or event level; does not count against API limits | Not detailed in sources fetched | Postback to a Clay webhook table, or GroupContacts API | [E40][E24] |
| Goldcast | Not detailed | Webhooks for event user activities | Salesforce (registrants, attendees, engagement as custom activities); HubSpot (dynamic lists, scoring, workflows); Marketo; Eloqua; Pardot; Slack and Slack + Salesforce alerts | CRM sync, or webhook | [E41] |
| Luma | Public API, e.g. `GET public-api.luma.com/v1/events/guests/list`; filter by approval_status; sort by registered_at or checked_in_at | Luma Plus only: Guest Registered, Guest Updated, Guest Refunded, Ticket Registered, event lifecycle | Not covered in sources | List Guests API, or webhook on Plus | [E43][E44] |
| Hubilo | Not specified | Not specified | Claims martech integrations and lead activity sync; names not given on the page fetched | Verify before committing (open item) | [E47] |
| Swapcard | Exhibitor Leads API: GraphQL at `developer.swapcard.com/exhibitor/graphql` for leads collected at events; webhook subscription docs exist | Yes (docs exist) | Not covered | Exhibitor Leads API is the booth-scan path for sponsors and co-exhibitors | [E45] |
| RainFocus | "Integration framework" API, two-way flow | Not specified | 40+ integrations: Salesforce app, Eloqua, Marketo, HubSpot | Salesforce app or API | [E46] |

OURS notes:
- **Data-out ladder.** Native CRM sync with attended status is best, then webhook into a Clay table, then API pull, then CSV export.
- **What the join needs.** Eva needs email, company domain, registration status, check-in timestamp and ticket type. Insist the customer's event platform exposes check-in, because without it "tickets used" (a Sculpt metric [E1]) cannot be computed.
- **Exhibitor-side data.** When the customer is a sponsor at someone else's conference, the only reliable people data is its own badge scans or exhibitor leads API (Swapcard pattern [E45]) plus the organizer's opt-in sponsor list, if one exists (section 6).
- **Integration debt.** 28% of larger organizations run six or more event platforms, and fewer than one in five have integrated them [E26]. Eva should ask "which platform owns this event" before anything else.

---

## 9. Benchmarks

| Metric | Value | Source | Date | Label |
|---|---|---|---|---|
| Avg registrations / attendees per event | 412 / 269 | Bizzabo platform data [E21] | 2025 data, pub 2026 | VENDOR |
| Avg attendance rate (all Bizzabo events) | 52% | [E21] | 2025 data | VENDOR |
| Visit-to-registration conversion | 21.5% overall; 24.4% dynamic flow vs 11.6% static | [E21][E20] | 2025 data | VENDOR |
| Format mix | 63% in-person, 33% virtual, 4% hybrid | [E21] | 2025 data | VENDOR |
| Webinar attendance rate | 40% (up from 33%); 251 registrants, 102 attendees avg; 26,190 webinars, 522 orgs | Goldcast [E23] | CY2025 | VENDOR |
| Webinar best attendance days | Monday 47.2%, Friday 46.9% | [E23] | CY2025 | VENDOR |
| On-demand vs live completion | 91% vs 74% | [E23] | CY2025 | VENDOR |
| Executive dinner attendance | 70% | Clutch, 191 events, 13,155 registrations [E27] | Feb 2025 to Mar 2026 | VENDOR |
| Roundtable / networking dinner / morning briefing | 61% / 52% / 45% | [E27] | Feb 2025 to Mar 2026 | VENDOR |
| Customer/partner events attendance | 62% | [E27] | Feb 2025 to Mar 2026 | VENDOR |
| Vendor-owned conference attendance | 19% | [E27] | Feb 2025 to Mar 2026 | VENDOR |
| Conference day-of no-show | 40%; only 22% cancel ahead. Roundtables: 11 of 12 no-shows cancel ahead | [E27] | Feb 2025 to Mar 2026 | VENDOR |
| Directors+ attendance | 62% | [E27] | Feb 2025 to Mar 2026 | VENDOR |
| Dinner invite-to-confirm | 25 to 40%; 15 to 25% final-week drop; invite about 3x headcount | Attendir [E29] | 2026 | VENDOR |
| Dinner cost per head | $300 to $500 lean, $400 to $800 standard, $800 to $1,500+ premium | [E29] | 2026 | VENDOR |
| Cost per meeting | Tier 1 sponsorship $1.5k to $3k; mid-tier $2.5k to $5k; dinner $1k to $3k; hospitality suite $3k to $6k | Vendelux [E28] | 2026-06 | VENDOR |
| Meeting to qualified opp | Pre-booked 25 to 40%; dinner attendee 30 to 50%; suite 40 to 60% | [E28] | 2026-06 | VENDOR |
| Meeting show rate | Booth 40 to 60%; exec dinner 80 to 90%; pre-event virtual 60 to 75% | [E28] | 2026-06 | VENDOR |
| Pipeline per event (target / best-in-class) | 90-day pipeline 3 to 5x / 10 to 15x all-in cost; 12-month won 1 to 3x / 5 to 10x | [E28] | 2026-06 | VENDOR |
| Lead response speed | Within 1 hour: about 7x as likely to qualify vs later; over 60x vs 24h+. Only 37% of 2,241 firms responded within an hour; 23% never did | HBR, Oldroyd et al. [E31] | 2011 | INDEPENDENT |
| Events as revenue driver | 88%; 52% attribute half or more of closed-won to events (self-reported) | Splash, n=1,058 [E24] | Jan to Feb 2025 | VENDOR |
| Event budget direction | 37% up, 31% down; 49% hosted / 51% sponsored | Forrester, n=417 [E25] | Q1 2026 | INDEPENDENT |
| Planned format growth | Intimate networking 63%; small under 200: 52%; webinars 42%; large over 200: 18% | [E25] | Q1 2026 | INDEPENDENT |
| Measure event impact | 44% | [E25] | Q1 2026 | INDEPENDENT |
| Difficulty proving ROI | 40% (2026) vs 70% (2025) | Bizzabo [E20] | 2026 | VENDOR |
| Event team size | 45% run with 1 to 3 people | [E20] | 2026 | VENDOR |
| Partner win-rate lift | +11.7% avg; +37.1% at 50+ partners | Crossbeam network [E17] | 2024-10-28 | VENDOR |
| Partner deal close likelihood / speed | 53% more likely; 46% faster | Crossbeam 2023 report via [E18] | 2023 | VENDOR |
| Partner attribution model in use | Multi-touch 42%, first 31%, last 19% | PartnerStack/Wynter [E32] | 2026 | VENDOR |

OURS reading:
- The independent evidence (Forrester) supports the shift to small hosted events and the measurement gap.
- Nearly every per-format and per-meeting number is vendor-sourced. Use those as planning ranges, not promises, and replace them with the customer's own actuals after 2 events.

---

## 10. Anti-patterns

1. **Co-hosting by logo, not overlap.** Choosing the biggest partner rather than the one with the highest target overlap density and shared data. The sourced practice is overlap-first selection [E6]; a counts-only partner fails gate G1.
2. **Raw attendee spreadsheets emailed to partners.** This bypasses Crossbeam's field-level sharing [E14] and fails the GDPR partner-named opt-in standard [E33][E34].
3. **Treating registrations as attendance.** Average attendance runs from 19% at vendor-owned conferences to 86% at VIP experiences [E27]. Plan headcount on the format's rate, and report "tickets used" from check-in data [E1][E35].
4. **Slow follow-up.** Response decay is steep [E31]; the warm-intro half-life is measured in days [E30]. Tier-1 follow-up after 24 hours is a failure (OURS).
5. **Double-counting credit.** Summing event-sourced and partner-sourced pipeline. Use the 2x2 and report cell A (section 7).
6. **Dashboards with no outcome layer.** Sculpt published no outcomes [E1]. Eva must ship the T+30 and T+90 readouts, or the dashboard is a planning toy.
7. **Over-inviting with no waitlist discipline.** Dinners need 35 to 45 names for 12 seats [E29], but filling seats with non-ICP guests to avoid empty chairs wastes the format (OURS).
8. **Partner contacts pushed into cold outbound.** This breaks rule 6 in section 6 and the partner's trust.
9. **Six event platforms, zero integration.** Common in larger organizations [E26]. Pick the system of record per event before building the join.
10. **Big-booth-first budgeting.** Large events are the declining format [E25][E26]. Lead with dinners and roundtables layered on top of conferences you already attend [E30].
11. **Running MCP-heavy builds on a Free Crossbeam plan.** 50 credits per year, no saved lists [E19]. Budget calls, or use CSV and offline paths [E12][E13].
12. **Using vendor benchmarks as targets in a customer SOW.** Label them VENDOR and set targets after the customer's own baseline (OURS).

---

## 11. Sources

All fetched or queried 2026-10-04 unless noted.

- [E1] Crossbeam, "How Clay's Solution Partners team used AI to solve event strategy for Sculpt 2026," case study. https://www.crossbeam.com/case-study/how-clays-solution-partners-team-used-ai-to-solve-event-strategy-for-sculpt-2026 (VENDOR)
- [E2] Clay, "How we designed Sculpt." https://www.clay.com/blog/how-we-designed-sculpt (VENDOR)
- [E3] Crossbeam Help Center, "Crossbeam MCP Server" (tool list), via Crossbeam knowledge search. https://help.crossbeam.com/en/articles/12601327-crossbeam-mcp-server (VENDOR)
- [E4] Forecastable, "Crossbeam MCP Server: 10 Plays for Partner Teams." https://forecastable.com/crossbeam-mcp-server-playbook/ (VENDOR; lists older tool names, superseded by E3)
- [E5] Crossbeam, Events page. https://www.crossbeam.com/resources/events (VENDOR)
- [E6] ELG Insider, "How to nail co-marketing events in 2024 with nearbound," Nearbound Summit session with Kate Hammit (Splash), Emily Wilkes (Gainsight), Justin Zimmerman. https://insider.crossbeam.com/entry/how-to-nail-co-marketing-events-in-2024-with-nearbound (VENDOR; speaker-reported numbers)
- [E7] ELG Insider, "Partnerships 101: How to Organize and Execute an Online Event With Your Partners," 2020-06-23. https://insider.crossbeam.com/entry/how-to-organize-and-execute-an-online-event-with-your-partners (VENDOR)
- [E8] Ecosystem-Led Growth book, Ch. 3 "Operationalizing Ecosystem GTM," via Crossbeam MCP `search_crossbeam_knowledge` (elg_book). (VENDOR)
- [E9] Ecosystem-Led Growth book, Ch. 4 "Ecosystem Metrics & Measurement," via the same search. (VENDOR)
- [E10] Crossbeam Help, "Understanding Attribution in Crossbeam." https://help.crossbeam.com/en/articles/11553885-understanding-attribution-in-crossbeam (VENDOR)
- [E11] Crossbeam Help, "Attribution for Salesforce Users" and "Crossbeam for Sales Attribution FAQs." https://help.crossbeam.com/en/articles/8042999-attribution-for-salesforce-users ; https://help.crossbeam.com/en/articles/9180987-crossbeam-for-sales-attribution-faqs (VENDOR)
- [E12] Crossbeam Help, "Upload a CSV File and Map Your Fields." https://help.crossbeam.com/en/articles/3160473-upload-a-csv-file (VENDOR)
- [E13] Crossbeam Help, "Offline Partners." https://help.crossbeam.com/en/articles/8799966-offline-partners (VENDOR)
- [E14] Crossbeam Help, "Data Privacy FAQ" and "Static Shared Lists." https://help.crossbeam.com/en/articles/13066154-data-privacy-faq ; https://help.crossbeam.com/en/articles/8345701-static-shared-lists (VENDOR)
- [E15] Crossbeam Help, "Invite Partners to Crossbeam with the Invite Link" (QR codes on booth banners). https://help.crossbeam.com/en/articles/3499611-invite-partners-to-crossbeam-with-the-invite-link (VENDOR)
- [E16] Crossbeam Help, "Crossbeam Performance Dashboard Guide." https://help.crossbeam.com/en/articles/10845010-crossbeam-performance-dashboard-guide (VENDOR)
- [E17] ELG Insider, "New Data: Involving Partners in Deals Increases Win Rate for Nearly Every Ecosystem Size and Type," data as of 2024-10-28. https://insider.crossbeam.com/entry/new-data-involving-partners-in-deals-increases-win-rate-for-nearly-every-ecosystem-size-and-type (VENDOR)
- [E18] ELG Insider, "Every Stat We Have That Proves The Value Of Partnerships," 2022-08-22, updated with the 2023 State of the Partner Ecosystem. https://insider.crossbeam.com/entry/every-stat-we-have-that-proves-the-value-of-partnerships (VENDOR)
- [E19] Crossbeam Help Center plan and credit articles and the live Crossbeam MCP tool schemas, read 2026-09-25: credits by plan, Free limits, sharing levels, `get_partner_context` fields. (VENDOR)
- [E20] Bizzabo, "The Events Industry's Top Marketing Statistics, Trends, and Benchmarks for 2026." https://www.bizzabo.com/blog/event-marketing-statistics (VENDOR)
- [E21] Bizzabo, "Event Program Benchmarks 2026." https://www.bizzabo.com/blog/event-program-benchmarks-2026 (VENDOR; sample size not disclosed)
- [E22] Bizzabo, "The Ultimate Guide to Event ROI and Marketing Attribution," 2026-08-24. https://www.bizzabo.com/blog/event-roi-marketing-attribution-guide (VENDOR)
- [E23] Goldcast, "2026 B2B Webinar Benchmark Report" (26,190 webinars, 522 orgs, CY2025). https://www.goldcast.io/reports/b2b-webinar-benchmark-report-2026 (VENDOR)
- [E24] Splash, "2025 Outlook on Events," BusinessWire, 2025-03-27 (n=1,058 US marketers). https://www.businesswire.com/news/home/20250327434693/en/ (VENDOR)
- [E25] Forrester, "Q1 2026 State Of B2B Events Survey" findings PDF (n=417, Jan to Feb 2026). https://cdn.prod.website-files.com/651d0b52d335df8b3a43d0f7/6a0acbdb703fe31852e6e33c_B2B%20Events%20Trends%20Survey%202026%20findings.pdf (INDEPENDENT; analyst, hosted copy)
- [E26] The B2B Marketer, "Forrester: B2B events struggle as budget pressures mount," 2025-08-22, summarizing Forrester Q1 2025 (250+ decision makers). https://theb2bmarketer.pro/forrester-b2b-events-struggle/ (INDEPENDENT; secondary)
- [E27] Clutch Events, "The State of Executive B2B Event Attendance" (191 events, 13,155 registrations, Feb 2025 to Mar 2026). https://report.clutchevents.co/ (VENDOR)
- [E28] Vendelux, "B2B Event Marketing Benchmarks: The Operator's Reference," modified 2026-06-16. https://vendelux.com/event-marketing/b2b-event-marketing-benchmarks (VENDOR)
- [E29] Attendir, "The B2B Executive Roundtable & VIP Dinner Playbook." https://attendir.com/blog/executive-roundtable-vip-dinner-playbook (VENDOR)
- [E30] 10times, "Host the dinner, not the booth: a side-event playbook." https://blog.10times.com/host-the-dinner-not-the-booth-a-side-event-playbook/ (VENDOR)
- [E31] Oldroyd, McElheran, Elkington, "The Short Life of Online Sales Leads," Harvard Business Review, March 2011. https://hbr.org/2011/03/the-short-life-of-online-sales-leads (INDEPENDENT; online leads, not event-specific)
- [E32] PartnerStack and Wynter, "The State of Partnerships in GTM 2026." https://partnerstack.com/resources/research-lab/the-state-of-partnerships-in-gtm-2026 (VENDOR)
- [E33] Guild, "How can event organisers give delegate data to sponsors and be GDPR and PECR compliant?" 2021-03-26, updated 2021-09-29. https://guild.co/blog/how-can-event-organisers-give-delegate-data-to-sponsors-and-be-gdpr-and-pecr-compliant/ (VENDOR; legal commentary, UK focus)
- [E34] Splash, "GDPR for Event Marketing: FAQs," 2024-03-04. https://splashthat.com/blog/gdpr-for-event-marketing (VENDOR)
- [E35] Zuddl docs, "HubSpot integration." https://docs.zuddl.com/integration/hubspot ; Salesforce: https://docs.zuddl.com/integration/salesforce (VENDOR)
- [E36] Zuddl docs, "Introduction to Zuddl APIs." https://docs.zuddl.com/api-reference/introduction (VENDOR)
- [E37] Zuddl docs, ticketing webhooks reference ("Add on modified activity"). https://docs.zuddl.com/api-reference/ticketingwebhooks/add-on-modified-activity (VENDOR; existence confirmed via search index only)
- [E38] HubSpot App Marketplace, Bizzabo listing. https://ecosystem.hubspot.com/marketplace/listing/bizzabo (VENDOR)
- [E39] API Evangelist, Bizzabo API profile, plus Bizzabo Stoplight docs. https://github.com/api-evangelist/bizzabo ; https://bizzabo.stoplight.io/docs/bizzabo-rest-api/ (INDEPENDENT third-party profile)
- [E40] Splash API v2.2 documentation. https://api-docs.splashthat.com/ (VENDOR)
- [E41] Goldcast Help, "Integrations." https://help.goldcast.io/en_US/eventintegrations (VENDOR)
- [E43] Luma Help, "Webhooks." https://help.luma.com/p/webhooks (VENDOR)
- [E44] Luma API, "List Guests." https://docs.luma.com/reference/get_v1-events-guests-list (VENDOR)
- [E45] Swapcard developer docs, "About the Leads API." https://swapcard.dev/leads-api/about-the-api ; webhooks: https://swapcard.dev/webhooks/using-webhooks/subscribe (VENDOR)
- [E46] RainFocus, "Seamless Event Integrations." https://www.rainfocus.com/streamlined-integrations/ (VENDOR)
- [E47] Hubilo, "Integrations." https://www.hubilo.com/integrations (VENDOR; no specifics on page)
- [E48] Clay, "How to Generate Event Leads with AI." https://www.clay.com/tools/generate-event-leads (VENDOR)
- [E49] Clay, "What Is Clay MCP?" 2026-06-14. https://www.clay.com/guides/clay-mcp (VENDOR)
- [E50] Clay Community, "Finding Trade Shows and Exhibitors Using Clay Tools." https://community.clay.com/x/tutorials/m2rq1hob1on4/finding-trade-shows-and-exhibitors-using-clay-tool (VENDOR community)
- [E51] Pipeline Factory, "Does Clay have the ability to pull the attendee list for events happening in 2026?" https://pipelinefactory.co/blog/clay-scrape-event-attendee-lists.html (VENDOR; agency)
- [E52] LinkedOtter, "How to Enrich Webinar Attendees with Clay After Your B2B Event." https://www.linkedotter.com/articles/enrich-webinar-attendees-clay-post-event-outbound-2026 (VENDOR; agency)
- [E53] Fractional Demand, "Clay Workflow Example: Trade Show Intelligence Dashboard." https://fractionaldemand.com/resources/blog/clay-workflow-trade-show-intelligence-dashboard (VENDOR; agency)
- [E55] Forecastable house rules for Eva: never auto-send, a named human approves and sends, drafts only, no em or en dashes. (INTERNAL)
- [E56] Clay Community threads on webhook sources into tables, e.g. "How to Import Data to Clay Using Webhooks in the New UI." https://community.clay.com/x/support/ax2sov05zmad/how-to-import-data-to-clay-using-webhooks-in-the-n (VENDOR community; thread content not retrievable, existence only)

---

## 12. Open items

1. **Sculpt outcomes.** The event is 2026-10-08 [E1]. At the 2026-11-04 refresh, check for a Crossbeam or Clay follow-up with results (meetings, pipeline, partner usage) and add them to sections 1 and 4.
2. **Crossbeam MCP per-tool credit cost** is unpublished [E19]. Confirm it with Crossbeam before quoting the MCP cost of a Sculpt-style build to Free or Connector customers.
3. **Unretrieved Crossbeam content:**
   - "The 3 Best Event Types for Driving Revenue" (Hammitt and Wilkes, 2023-11-07): page body not retrievable.
   - "How to use Reveal for Co-marketing Events" (2023-04-18).
   - Supernode 2023 session recordings.
   - Partnership Leaders community event threads: nothing citable found.
   Retry via Crossbeam Academy or the ELG Insider video transcripts.
4. **Clay's official answer on 2026 attendee lists** (community thread) was not retrievable. The only citation is a third-party claim [E51].
5. **Not verified:** Bizzabo's Salesforce integration, Hubilo's named integrations and API, and Goldcast and RainFocus public API docs. Fill in section 8 from vendor docs.
6. **US privacy rules not researched:** CAN-SPAM, CCPA/CPRA "sale or share" for attendee lists given to partners, and Canada's CASL. Section 6 is GDPR/PECR-only.
7. **Unverified statistic:** "80% of trade show leads are never followed up" circulates widely, but no primary source was found. Do not use it.
8. **No sourced cost bands** for webinars, workshops or sponsor packages at your own conference. Collect actuals from customers.
9. **Event-sourced and event-influenced definitions are OURS** (section 7). Align them with each customer's RevOps before the first readout, and add `event_attribution` and `event_id` fields through `forecastable-hubspot-setup` where approved.
