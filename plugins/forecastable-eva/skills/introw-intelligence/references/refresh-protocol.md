# Introw Intelligence: Monthly Refresh Protocol

Cadence: monthly, first week. Writes to the Project at `claude/introw/`. Never edits a customer tenant.

1. **Release notes.** Read the newest monthly release note on docs.introw.io (release notes section)
   and the Product Updates collection on support.introw.io. Add each shipped item to section 5
   (Changelog) with month and source tag. If an item changes a limit, a plan inclusion, a menu path or
   a gotcha in sections 2 to 8 or 12, edit that line too and keep the old value in a
   "Superseded 2026-MM" note.
2. **Pricing page.** Re-read introw.io pricing. Update section 1.6 plan table; log any change.
3. **Docs index.** Pull the docs.introw.io page index (llms.txt). Diff against last month. Read new
   pages that touch CRM sync, attribution, permissions, forms, commissions, MCP, API or Crossbeam.
4. **Integrations.** Re-check HubSpot Marketplace and Salesforce AppExchange listings (version, rating,
   scopes). Re-check the Crossbeam integration docs for plan requirements (resolve the open CONFLICT).
5. **Live check (when a customer session is available and the customer agrees).** Walk section 12.1
   routes read-only; update the route table and section 12.3 corrections. Never copy customer data.
6. **Content and competitors.** Scan the Introw blog and video library for new material; add notable
   items to section 9. Label any competitor claim.
7. **Open items to resolve each cycle:** Crossbeam plan requirement (record exports vs Supernode);
   free plan goal limit; CRM User role on Salesforce; Pipedrive depth; webhooks (Coming soon as of
   2026-09-29); MCP tool names; hyperscaler (ACE) sync claim.
8. **Bump the version date** at the top of `introw-intelligence.md`, run the no-em-dash scrubber, and
   post a five-line summary of what changed to the project.
