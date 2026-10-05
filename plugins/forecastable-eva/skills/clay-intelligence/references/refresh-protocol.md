# Clay and Events Refresh Protocol

Cadence: monthly. Current version 2026-10-04; next due 2026-11-04. Run an extra pass the week of
2026-10-12 to absorb Sculpt 2026 (2026-10-08) launches.

## 1. Surfaces to check each cycle

| Surface | URL | What to diff |
|---|---|---|
| Pricing | https://www.clay.com/pricing | Plans, monthly and annual prices, Actions and Data Credits per plan, rows per table, feature gates |
| Changelog | https://www.clay.com/changelog (and docs release notes) | Every weekly entry since last version; add to section 10 |
| MCP docs | Clay MCP pages on university.clay.com / docs | Tool names, deprecations, auth, clients, governance settings |
| Agent Plugin and CLI | https://github.com/clay-run/agent-plugins (releases) | CLI version, new commands, API capabilities, table write support |
| Public API docs | api.clay.com/public/v0 reference | Endpoints, quotas, rate limits, webhooks |
| Crossbeam integration | Clay Crossbeam doc, Crossbeam help article, Claybook | Plan gate (Supernode), limit, fields, any write-back |
| Event integrations | Clay integrations page; Sequel, Luma, Zuddl, Goldcast, Splash, Bizzabo docs | Any new native Clay integration; API and webhook changes |
| Templates and Claybooks | clay.com/templates, Claybooks | New event, partner or ELG templates |
| Trust center | Clay trust page | SOC 2, ISO, sub-processors, AI model providers |
| Partner program | https://www.clay.com/en/experts | Tier names, partner count, Elite Studios |
| Crossbeam case studies and resources | crossbeam.com/case-study, resources | Sculpt results follow-up; new event or Clay content |
| YouTube | `creator-registry.md` | Walk Tier 1 and 2, run discovery queries, pull transcripts for new substantive videos |
| Events benchmarks | sources in `events-intelligence.md` section 11 | Newer editions of Forrester, Bizzabo, Splash, Goldcast reports |

## 2. Open items to resolve (carry forward until closed)

1. Row limit conflict: pricing page (Growth and Enterprise unlimited) vs docs (50,000 all plans).
2. Crossbeam source: Clay plan requirement ("Clay Pro" legacy vs "All Plans"); Action and credit cost
   per import and per Partner Data lookup; whether the 1,000 limit is per source or per run.
3. Whether Free or Connector Crossbeam accounts have any sanctioned path into Clay.
4. Crossbeam MCP credit cost per tool (ask Crossbeam).
5. Clay MCP tool changes announced at Sculpt 2026; any table-write capability in CLI or API.
6. Clay trust center contents (did not load 2026-10-04).
7. Tyler Swanson title confirmed only via LinkedIn search result.
8. Sculpt 2026 event-overlap outcomes (meetings, pipeline) if Clay or Crossbeam publish them.
9. User roles, permissions and per-user credit limits: no video coverage; confirm from docs live.
10. US privacy (CAN-SPAM, CCPA) for partner attendee sharing: not yet researched.
11. Remaining items in `clay-intelligence.md` section 12 and `events-intelligence.md` section 12.

## 3. Steps

1. Fetch each surface (WebFetch; never curl or scripts on blocked domains). Note failures.
2. Update affected sections; add dated changelog rows; add new sources with read dates; close
   resolved open items.
3. If a price, plan gate, row limit, MCP tool or the Crossbeam plan gate changed, update `SKILL.md`
   section 1 and `forecastable-crossbeam-clay.md` sections 2 and 3.
4. YouTube: follow `creator-registry.md`; transcripts only (TranscriptAPI), never video files; add new
   takeaways to `youtube-digest.md` or `clay-admin-best-practices.md` with timestamps; flag pricing
   claims older than 2026-03-11 as stale.
5. Fold in live-workspace observations into section 12 (product behavior only, no customer data).
6. Bump version lines in every file touched.
7. Scrub dashes: `grep -nP '\x{2013}|\x{2014}' *.md` returns nothing.
8. Re-check labels: VENDOR, PARTNER, INDEPENDENT, COMPETITOR; OURS on every recommendation; no
   unsourced price or limit.
