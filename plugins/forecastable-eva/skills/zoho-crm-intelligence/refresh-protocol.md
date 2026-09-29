# Zoho CRM Refresh Protocol

Cadence: monthly. Current version: 2026-09-29. Next due: 2026-10-29.

## Steps

1. **API v8 docs.** Re-read the COQL Overview, Get Records through COQL, COQL Joins, Subquery and
   Limitations pages, Get Records, Search, Bulk Read limitations, API Limits and What's New in V8
   (sources A24, A33, A34, A35, A40, A41, A45). Record changes to limits, credits, new endpoints.
   Try to settle the section 13 CONFLICT rows on joins, rows per criteria and SELECT caps.
2. **Newer API version.** Check https://www.zoho.com/crm/developer/docs/api/ for a v9. If released, note
   what changed for reads and keep v8 examples until customers move.
3. **Zoho MCP and the Claude connector.** Re-read claude.com/connectors/zoho-crm (tool count, named tools,
   regional URLs), zoho.com/crm/developer/mcp.html, the MCP overview and Claude setup pages, zoho.com/mcp
   pricing. Check GitHub anthropics/claude-ai-mcp issue #311 for status of the data center bug.
4. **Help Center.** Profiles and Developer Permissions (API access), NextGen UI FAQ, Setup changes,
   mobile call logging (iPhone and Android), telephony, email configuration. Check the latest Zoho CRM
   Community Digest for shipped features.
5. **Kaizen.** Scan the Kaizen index for new COQL, Bulk, Timeline, MCP or Queries posts; add any that
   change guidance.
6. **Pricing and editions.** Re-read the comparison page and pricing data file; update section 11 (USD
   and AUD), custom module and field caps, credits per edition.
7. **Creators.** Run the discovery queries in `creator-registry.md`; recency-check the tier 1 and 2
   channels with TranscriptAPI `get_channel_latest_videos`. Pull transcripts for any new video on COQL,
   API, MCP, reports, Blueprint, telephony or Zia with real how-to content. Add notes with [Y:id mm:ss]
   tags and fold confirmed facts into the intelligence file. Move silent creators to Dormant after 12
   months.
8. **Live tenants.** If any customer session happened this month, move confirmed items (connector
   behavior, API permission fix, field names) into the body with an [L#] tag and a date. Customer-specific
   facts go only to `customers/<customer>.md`.

## Open items to resolve each cycle

- COQL join limit (2 vs 5 base / 15 select), rows per criteria (100,000 vs 10,000), SELECT cap (50 vs 500).
- Whether `COUNT(id)` works in COQL aggregates.
- `Crm_Implied_Api_Access` mapping to the Zoho CRM API Access toggle (confirm in a live fix).
- Directory connector data center bug and the AU custom URL workaround.
- The 17 unnamed tools in the Claude directory connector; whether any reads the Emails related list.
- Whether Crossbeam offers a native Zoho CRM data source.
- Notification channel expiry, Bulk Read download rate.
- Zia Chat general availability and AU data center availability of Zia agents.

## Version bump

1. Set the header of `zoho-crm-intelligence.md` to `Version: {today}.`
2. Update the version line in `forecastable-crossbeam-zoho-crm.md`, `creator-registry.md` and this file.
3. Add a change log row in `creator-registry.md`.

## Scrub

Before saving, count U+2013 and U+2014 in every file with a short Python script and replace hits with
commas, colons, parentheses or "to". Zero hits required. Also confirm no customer names appear in the
generic files (`grep -i` for each customer in `customers/`).
