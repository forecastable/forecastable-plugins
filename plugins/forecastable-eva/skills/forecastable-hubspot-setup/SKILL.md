---
name: "forecastable-hubspot-setup"
description: "Standard for configuring a HubSpot portal that Forecastable syncs from: the associated company carries the prospect, a property carries the referring partner, lead source is mirrored on the Lead and Deal objects with one internal name, sync filters match the records meant to sync, domains are verified before they are written, and live properties are changed by a protocol rather than by hand. Load on any HubSpot setup, audit or property change for an organization that uses Forecastable, and on any task that prepares HubSpot leads or deals for the Forecastable sync. Trigger on 'set up HubSpot for Forecastable', 'HubSpot integration settings', 'lead source', 'referring partner', 'partner attribution', 'associated company', 'is our HubSpot configured', or any HubSpot property edit on a portal Forecastable reads. Verified against a live portal on September 15th, 2026."
---

# HubSpot setup for Forecastable

The standard for configuring a HubSpot portal that Forecastable reads from. It is written to be
handed to a customer's HubSpot admin as-is, and for Eva to apply without re-deriving it. Every line
was verified against a live portal on September 15th, 2026, unless it says otherwise.

Load a learned-rules skill alongside this if one is installed. Load
`forecastable-controlled-vocabulary` for the Forecastable side of any write. General HubSpot doctrine
from a sales-ops corpus applies too, read with the caveat in section 2.

## The rule in one paragraph

The associated company on a lead or deal is the **prospect**. The **partner** who referred it lives
in a property. Lead source is a custom picklist that exists identically on the Lead and Deal objects.
Partners are identified by Company type = Partner. And the portal is the truth: before claiming a
property exists, does not exist, or must be built, search the portal.

---

## 1. How Forecastable reads HubSpot

In Forecastable: Settings, Integrations, HubSpot. Two tabs, in order. Lead settings first, then
Account syncs; the Account tab is gated until Lead settings are complete.

| Step | Setting | What it means |
|---|---|---|
| 1 | Partner Company Mapping | Which HubSpot companies count as partners. PARTNER mode: any company with type Partner syncs automatically. |
| 2 | Lead Mapping | Which object is a lead (the Lead object, not Contact), how a lead is tied to its partner (Company associations or Partner property), and a property filter for which leads sync. |
| 3 | Deal Mapping | Any deal associated to a synced company syncs. Hard-coded today. A Partner property option and a property filter are on the request list. |
| 4 | Sync Companies | Manual selection of which companies sync. |

**Step 2 is the decision that matters.** Company associations and Partner property read like two ways
to do the same job. They are not.

- **Company associations**: Forecastable reads the lead's associated company as the partner. The
  prospect is then only the free-text lead name, with no domain, so communication tracking has
  nothing to match on.
- **Partner property**: the associated company is the prospect and carries the domain. The partner
  is a dropdown on the record.

The HubSpot Lead object has one company association slot, a free-text name and no domain field. That
slot cannot be both prospect and partner. Use Partner property. (Design confirmed September 15th,
2026, with the reference portal being switched to it that day.)

**The sync filter must match the records you intend to sync.** A filter inherited from an earlier
setup, for example `Lead Type = Re-attempting`, silently excludes every new-business lead, so nothing
syncs and it looks like the integration is broken. Filter on `lead_source = Partner Referral`, or
whatever property actually separates partner-sourced records from the rest.

---

## 2. The property standard

### Lead source: custom picklist, both objects, same internal name

| | Lead object | Deal object |
|---|---|---|
| Internal name | `lead_source` | `lead_source` |
| Label | Sales Lead Source | Lead Source |
| Type | Dropdown select | Dropdown select |
| Values | identical | identical |

Never use HubSpot's standard `hs_lead_source` for this. It is an analytics picklist (Organic Search,
Paid Search, Email Marketing, Organic Social, Referrals, Other Campaigns, Direct Traffic, Offline
Sources, Paid Social, AI Referrals), it is locked, and its Referrals value means web referral traffic,
not a partner. On the Lead object it owns the label Lead Source and cannot be relabeled, which is why
the custom property carries a different label there. The internal name is the contract. The label is
cosmetic.

Reference value list, in order: Renewal, Customer Referral, Prospect Referral, Personal Network,
Web - Inbound, LinkedIn - Inbound, Cold Outbound, Event, Partner Referral, Advisor Referral,
Employee Referral.

The principles behind the list: a source is a channel. It is not a deal type (Expansion is a deal
type), not a program (a cohort is a program), and not a venue variant (one Event value covers in
person and virtual). No person's name in a value.

### Referring partner: a dropdown keyed to company records

`partner_source`, label Referring Partner, on the Deal object. A dropdown whose stored values are
HubSpot **company record IDs** and whose labels are the partner company names. That is what makes it
an account lookup rather than free text: the value resolves to a real company record.

Conditional logic on Deal: Lead Source is equal to Partner Referral shows Referring Partner. The
Required box is a deliberate decision, not a default. Required makes API writes fail the same way any
conditional requirement does, so leave it unchecked while the integration is under test and decide it
afterwards, with whoever owns the integration.

Known gap: `partner_source` exists on Deal only. A lead can say Partner Referral and has nowhere to
name the partner. Whether the integration creates the Lead-side field or it is built by hand is a
question for the integration owner. Building it alone risks a duplicate the integration ignores or
fights with.

### Why a dropdown and not an association label

General HubSpot doctrine says a string cannot roll up, so partner attribution should be an
association with a label. That rule assumes HubSpot owns partner reporting. On a Forecastable
customer it does not: Forecastable computes sourced pipeline, closing ratio and the leaderboard. Once
the rollup argument is gone, the deciding fact is that **HubSpot conditional logic can require a
property and cannot require an association**. A dropdown is enforceable natively with zero workflows.
An association needs a workflow-set flag, a tag and a stage gate to get the same effect. PRMs that
ship a HubSpot integration use the same architecture for the same reason.

Teach it as a conditional: dropdown when a PRM owns partner reporting, association labels when
HubSpot does.

### Everything else

- Company type = Partner identifies partners. Step 1 depends on it.
- Open-text detail fields (for example `lead_source_details` on Deal, or the integration's own
  `forecastable_lead_source_detail` on Lead) hold narrative, not attribution. Never parse them for a
  partner.
- Never delete the integration's own `forecastable_*` properties. They are its namespace, they show
  Created by: Unknown user because the API made them, and the integration may write to them on every
  sync. Demote instead: take them off the create record form so reps stop typing attribution into
  free text.
- Five referral values, one structured referrer. Customer, Prospect and Partner Referral point at a
  company. Advisor and Employee Referral point at a person. One field cannot cover all five, so decide
  the shape before adding a second.

---

## 3. Domains

Forecastable tracks communications by domain. A wrong domain does not error; it silently tracks
nothing, or tracks the wrong company.

- Verified means seen in a real address on a real thread or invite. Inferred from the company name is
  a hypothesis. Name-alikes are the trap: two companies sharing a word are not the same company. Do
  not fill a domain until the entity is confirmed.
- Existing company records are usually inconsistent on the `www.` prefix. Whether the sync normalizes
  it is a question for the integration owner. Until answered, write bare domains on new records and
  flag the mixed ones.
- Never guess an address or a domain from an apparent pattern. `UNKNOWN`, plus who can confirm it.

---

## 4. Change protocol for a live portal

1. **Search before you claim.** Search the object's properties, then read the property's Usage
   panel, before saying a property exists, does not exist, or must be built. Documentation describes
   what an integration intends to create. The portal shows what is there. A field declined on
   doc-derived reasoning while it already sat in the portal costs the person who built it an hour of
   confusion.
2. **Read Usage first.** The property editor's Usage panel lists reports, views, conditional logic as
   controlling and as dependent, create record forms and property cards. Know what a change touches
   before making it.
3. **Picklist edits.** The Field type tab shows a With value count per option. Rename by editing the
   label only; the internal value stays and every record keeps its data. Delete only at zero records,
   then search records for the deleted value to prove there are no orphans. Apply the identical edit
   to both objects in the same pass so they stay in parity.
4. **Standard properties cannot be relabeled.** A HubSpot-provided property takes a focused cursor
   and rejects typed input, and the banner says so. Do not fight it. Take the internal name you need
   on a custom property and vary the label.
5. **Conditional requirements bite the API.** A conditional Required fails writes with
   `Property validation failed: X is required based on the values of other properties`. Do not null a
   required field to tidy up; remap to a real value. Do not flip Required while anyone is testing the
   integration; write up the ask.
6. **Nothing written to records until the integration owner says go.** Configuration changes with
   zero-record impact are fine. Record loads wait.
7. **Coordinate.** If someone is mid-test on the integration, do not touch `forecastable_*`
   properties, sync filters or Required flags. Produce the ask instead.
8. **Report the audit, not reassurance.** After any change: what changed, what was checked, with
   counts.

---

## Checklist before any HubSpot change on a Forecastable-synced portal

- [ ] Searched the object's properties and read Usage for everything I am about to touch
- [ ] The association carries the prospect; the partner is in `partner_source` or its equivalent
- [ ] `lead_source` exists on Lead and Deal with the same internal name and identical values, and `hs_lead_source` is untouched
- [ ] Every picklist option I am deleting shows zero records, and I searched for the value afterwards
- [ ] Every rename was label-only
- [ ] The sync filter matches the records that are meant to sync
- [ ] Domains on new records are verified or marked inferred, and bare of `www.` unless the integration owner says otherwise
- [ ] Nothing integration-namespaced was deleted or made required
- [ ] The integration owner has said go before any record is written
