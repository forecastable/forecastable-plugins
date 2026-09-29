# Introw docs (docs.introw.io): api-reference

Verbatim from docs.introw.io/llms-full.txt, fetched 2026-09-29. 23 pages.

# Record an affiliate conversion
Source: https://docs.introw.io/api-reference/affiliate/record-an-affiliate-conversion

/openapi.json post /api/v1/affiliate/conversions
Records an affiliate conversion and creates the campaign form submission it maps to.

**Attribution flow.** A partner shares an Introw affiliate link (`/r/{code}`). Introw logs a server-side click and redirects the visitor to your site with an opaque `irw_id` param. The `affiliate.js` snippet stores that id in a first-party, last-click `_introw_aff` cookie (90-day window). When the visitor converts, you send the cookie value as `clickId`. Because every conversion is anchored to a real server-side click and deduplicated, attribution can never be forged or inflated.

**Two authentication paths:**
- **Server-to-server** (recommended for backend conversions): send an `x-api-key` secret that holds the `affiliate:write` scope. No publishable key or Origin is required.
- **Browser** (via `affiliate.js`): send the campaign publishable key in the `x-introw-publishable-key` header (or the `publishableKey` body field). The request `Origin` must match the campaign's allowed-origins allowlist; an empty allowlist permits any origin.

**Responses are deliberately forgiving** so the browser snippet never surfaces errors on your page: an invalid, expired, or already-converted click returns `200` with `status: ignored`/`duplicate` rather than an error. A newly attributed conversion returns `201` with `status: recorded`.

---

# Redirect a legacy (PartnerStack) link
Source: https://docs.introw.io/api-reference/affiliate/redirect-a-legacy-partnerstack-link

/openapi.json get /api/v1/affiliate/legacy-redirect
Backwards-compatible redirect for links created in a previous affiliate tool (e.g. PartnerStack) that were migrated into Introw. During a migration every old link is mapped to its newly generated Introw affiliate link. Point your old links at this endpoint with a redirect rule on your side; Introw resolves the mapping and `302`-redirects to the matching Introw link (`/r/{code}`), which then records the click, sets the first-party `_introw_aff` attribution cookie, and forwards the visitor to the campaign destination.

**No key required.** The lookup is keyed by the globally-unique original URL, so no API key or publishable key is needed.

**How the original URL is captured**, in priority order:
1. The `u` query parameter (recommended): your redirect rule forwards the original absolute URL, e.g. `https://api.introw.io/api/v1/affiliate/legacy-redirect?u=https%3A%2F%2Fgo.acme.com%2Fabc`.
2. The `X-Original-URL` or `X-Forwarded-Uri` request header (reverse-proxy / CNAME setups).
3. The `Referer` header (fallback).

The captured URL is normalized before lookup (scheme and host lowercased, default ports and a trailing slash stripped, query params sorted; path and query values stay case-sensitive), so the value you forward does not need to match byte-for-byte.

---

# Create a portal session
Source: https://docs.introw.io/api-reference/auth/create-a-portal-session

/openapi.json post /api/v1/auth/session
Creates a pre-authenticated partner portal URL for a visitor email. This is the foundation of the **embedded portal experience**: show Introw directly inside your own product with one login and full branding.

**How to embed:**
1. Allow-list the domains that may embed Introw under **Settings → Developers → Embed** (only these domains can load the portal in an `<iframe>`).
2. From your backend, call this endpoint with the visitor's email and your secret API key (`portal-sessions:write` scope). Keep the key server-side and never call this from the browser.
3. Drop the returned `url` into an `<iframe>`. The URL carries a short-lived sign-in token, so the partner is logged in automatically with no login screen.

The visitor must already have portal access in the organisation resolved from the API key; otherwise the request returns `401`. Pass `roomId` to deep-link the visitor into a specific room (collaboration space) after authentication. Each URL is single-use and short-lived, so generate a fresh one per visitor session.

---

# Create a comment
Source: https://docs.introw.io/api-reference/collaboration/create-a-comment

/openapi.json post /api/v1/comments
Posts a comment on a partner's timeline: the same comment your team and partners see in the partner portal, the CRM embed, and email/Slack notifications. This is the in-app comment composer over the API: plain-text, Markdown, or HTML comments (HTML is converted server-side), `@Name` / `@email` mentions (or an explicit `mentions` array), internal (org-only) visibility, and thread replies.

**Where the comment lands** is resolved from the targets you pass:
- `partnerId`: the partner portal timeline. Accepts the Introw partner id or the partner's CRM external id.
- `crmObjectId` + `crmObjectType`: a deal, ticket, or other CRM object. Pass `crmObjectType` in your own CRM's wording (`Opportunity` or `Deal`, whichever your CRM uses). See [CRM object types](#crm-object-types). The partner is resolved from the object's partner attribution (or pass `partnerId` explicitly). The comment is also synced as a note to your CRM.
- `taskId`: a partner portal task.
- `formSubmissionId`: a form submission (deal registration, shared lead, MDF request, …).
- `commissionPayoutId`: a commission payout. Comments on payouts the partner cannot see yet are automatically kept internal.
- `threadId`: reply to an existing comment (use the `threadId` from the create response).

**Who it is posted as**: `authorEmail` must match an organisation team member or a partner portal member of the target partner. Only team-member authors may set `isInternal: true`. Internal comments stay hidden from partner-facing surfaces and never trigger partner notifications.

Notifications, workflow triggers, and CRM note sync behave exactly as if the comment was posted in the app.

**Comments forwarded out of your CRM**: send `metadata.source: "CRM"` when the comment is a note or Chatter post your HubSpot workflow or Salesforce flow is copying into Introw. The post already sits on the CRM record, so Introw puts the comment on the partner timeline and skips writing it back out as a second note. Without it, that forwarded comment returns to the record as a duplicate, and a flow that forwards every note on the record will loop.

### CRM object types

`crmObjectType` takes your CRM's own name for the object, case-insensitively. Introw translates it, so there is nothing to look up or map on your side:

- **Deal**: Salesforce `Opportunity`, HubSpot `Deal`
- **Company**: Salesforce `Account`, HubSpot `Company`
- **Ticket**: Salesforce `Case`, HubSpot `Ticket`
- **Contact**: `Contact` in both
- **Lead**: `Lead` in both

Introw's own type names (`DEAL`, `COMPANY`, `TICKET`, `CONTACT`, `LEAD`) and HubSpot object type ids (`0-3`, `0-2`, `0-5`, `0-1`, `0-136`) resolve to the same objects.

**Custom objects** are the one case where the exact name matters: pass the object's API name as your CRM shows it, for example `Partner_Program__c` in Salesforce or `p_partner_application` / `2-12345` in HubSpot. Custom types are used verbatim, not translated.

### More payloads

Comment on a deal (the partner is resolved from the deal's attribution):

```bash
curl -X POST "https://api.introw.io/api/v1/comments" \
  -H "x-api-key: $INTROW_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "comment": "Pricing approved on our side, over to you for the paperwork.",
    "authorEmail": "alex@vendor.example",
    "crmObjectId": "9840193344",
    "crmObjectType": "DEAL",
    "isInternal": false
  }'
```

Reply in an existing thread:

```bash
curl -X POST "https://api.introw.io/api/v1/comments" \
  -H "x-api-key: $INTROW_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "comment": "Signed order form is in the deal room, **we are good to go**.",
    "authorEmail": "jamie@partner.example",
    "formSubmissionId": "fsub_01HVK6Y8Z8Q7J8J8J8J8J8J8J8",
    "threadId": "cmt_01HVK6Y8Z8Q7J8J8J8J8J8J8J8"
  }'
```

Mention people with `@Name` / `@email` in the body and/or an explicit `mentions` array:

```bash
curl -X POST "https://api.introw.io/api/v1/comments" \
  -H "x-api-key: $INTROW_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "comment": "Can you take a look at the pricing on this deal @Alex?",
    "mentions": [
      "jamie@partner.example"
    ],
    "authorEmail": "alex@vendor.example",
    "crmObjectId": "9840193344",
    "crmObjectType": "DEAL"
  }'
```

Forward a note out of your CRM without it syncing back:

```bash
curl -X POST "https://api.introw.io/api/v1/comments" \
  -H "x-api-key: $INTROW_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "comment": "Checked with the end customer, they want the security review before signing.",
    "authorEmail": "jamie@partner.example",
    "crmObjectId": "9840193344",
    "crmObjectType": "DEAL",
    "metadata": {
      "source": "CRM"
    }
  }'
```

---

# Create a commission line
Source: https://docs.introw.io/api-reference/commission-lines/create-a-commission-line

/openapi.json post /api/v1/commission-lines
Creates a commission line for a partner. Omit `payoutId` to create a pending line that a future payout batch can pick up, or pass `payoutId` to attach the line to an existing payout immediately. Pass `idempotencyKey` to make retries return the existing line without overwriting it.

---

# Decline a commission line
Source: https://docs.introw.io/api-reference/commission-lines/decline-a-commission-line

/openapi.json post /api/v1/commission-lines/{id}/decline
Soft-deletes (voids) a commission line attached to a payout, with a categorised reason. If the payout becomes empty as a result, it is automatically declined. Returns 422 when the line is not attached to a payout.

---

# Detach a commission line
Source: https://docs.introw.io/api-reference/commission-lines/detach-a-commission-line

/openapi.json post /api/v1/commission-lines/{id}/detach
Detaches a commission line from its payout and returns it to the pending pool so it can be picked up by a future payout batch. Returns 422 when the line is not attached to a payout.

---

# Get a commission line
Source: https://docs.introw.io/api-reference/commission-lines/get-a-commission-line

/openapi.json get /api/v1/commission-lines/{id}
Returns a single commission line by id, scoped to the authenticated API key organisation.

---

# List commission lines
Source: https://docs.introw.io/api-reference/commission-lines/list-commission-lines

/openapi.json get /api/v1/commission-lines
Returns commission lines for the organisation resolved from the authenticated API key. Filter by partner, payout, or status.

---

# Update a commission line
Source: https://docs.introw.io/api-reference/commission-lines/update-a-commission-line

/openapi.json patch /api/v1/commission-lines/{id}
Updates a commission line's amount, currency, description, source amount, or internal note. Voided lines cannot be edited.

---

# Sync a CRM object
Source: https://docs.introw.io/api-reference/crm/sync-a-crm-object

/openapi.json post /api/v1/crm/objects/{objectType}/sync/{objectId}
**You usually do not need this.** Introw already syncs every connected CRM object automatically about every 15 minutes, so any change made in your CRM is reflected in Introw within the next sync window without any action on your part.

Use this endpoint only when a change must be reflected in Introw **immediately** rather than waiting for the next automatic sync. The typical case is a workflow that computes or mutates a value on the record and whose result must be persisted in Introw right away to keep data integrity. For example, an automation recalculates a field on a deal and that value has to be consistent in Introw at once for partner-facing views, commission calculations, or downstream logic, instead of up to ~15 minutes later.

It forces Introw to re-fetch the single object from your connected CRM (HubSpot or Salesforce) and re-ingest it on demand. `objectId` is that record's id in the CRM. The object is ingested in the context of your linked partners, so partner associations are resolved as part of the sync.

`objectType` takes your CRM's own name for the object, case-insensitively. Introw translates it, so there is nothing to look up or map on your side:

- **Deal**: Salesforce `Opportunity`, HubSpot `Deal`
- **Company**: Salesforce `Account`, HubSpot `Company`
- **Ticket**: Salesforce `Case`, HubSpot `Ticket`
- **Contact**: `Contact` in both
- **Lead**: `Lead` in both

Introw's own type names (`DEAL`, `COMPANY`, `TICKET`, `CONTACT`, `LEAD`) and HubSpot object type ids (`0-3`, `0-2`, `0-5`, `0-1`, `0-136`) resolve to the same objects. **Custom objects** are the one case where the exact name matters: pass the object's API name as your CRM shows it, for example `Partner_Program__c` in Salesforce or `p_partner_application` / `2-12345` in HubSpot. Custom types are used verbatim, not translated.

Authenticated by API key only: no specific scope is required. On success the endpoint returns `204 No Content` and does not return the synced object; read it back from the relevant resource if you need the ingested state.

---

# Get a form schema
Source: https://docs.introw.io/api-reference/forms/get-a-form-schema

/openapi.json get /api/v1/forms/{formId}/schema
Returns the form's submittable fields: the field id to use as the payload key, the label, whether the field is required, the value shape to send, and (for picklists) the allowed values. Call this before `POST /api/v1/forms/{formId}/submissions` instead of copying field ids out of the Introw UI by hand.

**Field ids.** `id` is the key to use in the submission's `fields` map. Ids are opaque, generated identifiers (for example `qkzv8h2m4t6r1yc9pd3sxf70`), never human-readable names, and unique per form. They are stable: a field keeps its id across form edits.

**Value shapes.** `dataType` is the one field to branch on: it tells you what to send, whether that is a string, a number, a `YYYY-MM-DD` date, a picklist value, or a file URL. Fields that differ only in how the portal draws them (a single-line text box versus a text area) share a data type; only the kinds that behave differently keep their own: `PARTNER_SELECT` picks an Introw partner, `QUOTE_SELECTOR` an Introw quote, and `BATCH_UPLOAD` carries no value at all (it is the portal's bulk-CSV control, so over the API you send one request per submission).

**Options.** `options` is present exactly when `dataType` is `DROPDOWN`, `DROPDOWN_MULTI`, or `PARTNER_SELECT`, and is resolved live: from the CRM picklist behind the field, the pipeline stages of the form's own CRM automation, the organisation's synced CRM owners, the partner audience of a partner-select field, or the builder's preset list. Options limited by the builder are already excluded. **Prefer sending `value`.** A `label` is also accepted and resolved to its value on submission (case-insensitively), so a payload built from human-readable names still lands correctly in the CRM; a value matching no option is passed through untouched rather than rejected, which is what keeps unrestricted picklists working. Send `DROPDOWN_MULTI` values joined with `;`. An empty array means the option set could not be resolved (for example the CRM property has not synced yet), which is a configuration problem to fix in Introw rather than something to work around in the payload.

Fetch this whenever the form may have changed rather than caching it indefinitely: adding a required field, or changing a picklist in the CRM, changes what a valid submission looks like.

---

# Submit a form
Source: https://docs.introw.io/api-reference/forms/submit-a-form

/openapi.json post /api/v1/forms/{formId}/submissions
Submits an Introw form (deal registration, lead share, onboarding, feedback, …) server-to-server. The payload is validated against the form's field definitions and runs the exact same pipeline as a partner filling in the form on the portal: CRM object automations, the form's acceptance flow, notifications, and timeline events.

Use this to register deals or share leads from your own systems (a partner-facing app, an internal tool, or another platform) without sending anyone to the form itself.

**Field ids.** `fields` is keyed by form field id. Field ids are opaque, generated identifiers (for example `qkzv8h2m4t6r1yc9pd3sxf70`). They are never human-readable names, and they are unique per form. Call `GET /api/v1/forms/{formId}/schema` for the exact list (every field id, its label, whether it is required, the value shape to send, and the allowed values of every picklist), or read it off the form's **Share → API** tab in Introw. Values are validated with the form's own rules; a payload that violates them (missing required fields, wrong formats) returns `422` with per-field details. Keys that don't match a form field are ignored.

**Picklists.** For a `DROPDOWN`, `DROPDOWN_MULTI` or `PARTNER_SELECT` field, send one of the option values the schema lists (join multiple with `;`). Option *labels* are accepted too and resolved to their value case-insensitively, so "Qualified to buy" and `qualifiedtobuy` both work, and a partner can be named rather than referenced by id. A value matching no option is passed through as sent, so an unrestricted picklist keeps accepting free text.

**Partner attribution.** Pass `partnerId` to relate the submission to a specific partner (the same guarantee as the form's partner-specific share link). It accepts either the Introw partner id or the partner's CRM external id, so you can key off whichever identifier your own systems already hold; an identifier that matches neither returns `404`. With only `email`, Introw makes a best effort to resolve the partner from the submitter, the same behaviour as the form's general share link.

**Status.** Forms without an acceptance flow auto-accept the submission and trigger their automation immediately (`AUTO_ACCEPTED`). Forms with an acceptance flow return `PENDING` until a teammate (or the AI acceptance agent) processes the submission.

---

# Create a partner
Source: https://docs.introw.io/api-reference/partners/create-a-partner

/openapi.json post /api/v1/partners
Creates a partner in the organisation resolved from the authenticated API key.

Beyond `name` and `domain`, you can set configuration in the same call: assign a `tierId`, set the lifecycle `phaseId`, designate a `partnerOwnerId`, and publish an `experienceTemplateId` (optionally scoping its portal access with `portalAccess`).

The endpoint is **create-or-update**: when a partner with the same name/domain already exists, it is patched with the supplied settings rather than duplicated. A freshly created partner returns `201`; a matched (updated) partner returns `200`.

---

# Get a partner
Source: https://docs.introw.io/api-reference/partners/get-a-partner

/openapi.json get /api/v1/partners/{id}
Returns a single partner, scoped to the authenticated API key organisation.

`id` accepts either the Introw partner id or the partner's CRM external id (`externalId`), so you can read a partner straight from the identifier your CRM already holds.

---

# List partners
Source: https://docs.introw.io/api-reference/partners/list-partners

/openapi.json get /api/v1/partners
Returns partners for the organisation resolved from the authenticated API key.

---

# Update a partner
Source: https://docs.introw.io/api-reference/partners/update-a-partner

/openapi.json patch /api/v1/partners/{id}
Updates allowed public partner fields in the authenticated API key organisation.

Patch the partner's `name` and `domain`, and adjust configuration: `tierId`, `phaseId`, `partnerOwnerId`, and `experienceTemplateId` (optionally scoped with `portalAccess`). Only the fields you supply are changed.

`id` accepts either the Introw partner id or the partner's CRM external id (`externalId`), so you can patch a partner straight from the identifier your CRM already holds.

---

# Create a payout
Source: https://docs.introw.io/api-reference/payouts/create-a-payout

/openapi.json post /api/v1/payouts
Opens a commission payout for one partner and one period, so your finance stack can assemble a payout end to end over the API. The payout is created empty by default: attach lines with POST /commission-lines using the returned payout id, then render the statement with POST /api/v1/payouts/{id}/statement. Set attachPendingLines to pull in the partner's pending lines for the period instead, the way creating a payout in the app does. Every payout belongs to a batch: pass batchId to put this partner on an existing run alongside others, or leave it out and the payout gets a batch of its own. Either way the id comes back on the payout as batchId. Answers 200 instead of 201 when the partner already had a payout on that batch, returning the one they have.

---

# Create a payout batch
Source: https://docs.introw.io/api-reference/payouts/create-a-payout-batch

/openapi.json post /api/v1/payout-batches
Opens a payout run for one period and, optionally, a draft payout for each partner on it. A batch is what the Payouts page lists as a period: it holds one payout per partner, and each partner gets their own commission statement. Use it when a run covers several partners, so they stay one batch instead of one batch each. Pass partnerIds to open every partner's payout in this call, or leave it out and add partners one at a time with POST /api/v1/payouts using the returned batch id. The payouts open empty unless attachPendingLines is set.

---

# Generate the commission statement
Source: https://docs.introw.io/api-reference/payouts/generate-the-commission-statement

/openapi.json post /api/v1/payouts/{id}/statement
Renders the payout's commission statement PDF and returns a pre-signed link to it. The PDF is rebuilt only when something on it changed - the commission lines, the PO number, the statement note, or the statement template - so calling this repeatedly is cheap and returns the same document. When someone has uploaded their own statement in the app, that PDF is returned untouched and isUploaded is true.

---

# Get a payout
Source: https://docs.introw.io/api-reference/payouts/get-a-payout

/openapi.json get /api/v1/payouts/{id}
Returns a single commission payout by id, scoped to the authenticated API key organisation.

---

# List payouts
Source: https://docs.introw.io/api-reference/payouts/list-payouts

/openapi.json get /api/v1/payouts
Returns commission payouts for the organisation resolved from the authenticated API key. Use filters to pull payouts ready for your finance workflow.

---

# Update a payout
Source: https://docs.introw.io/api-reference/payouts/update-a-payout

/openapi.json patch /api/v1/payouts/{id}
Update payout fields from your finance software. Set the stage to reflect your approval, scheduling, and payment workflow, attach a partner purchase order number, and write the free-text block that prints on the commission statement PDF.