# CRM Dayboard: Manager and Administrator Guide

**Audience:** Commercial Manager, Commercial Admin, System Manager and authorized operational owners.  
**Source checked:** The repository's `main` branch, role gates, ERPNext DocTypes, manager page, generation code and the nine screen captures supplied on 19 November 2026.

This application sits inside **ERPNext Desk**. Management configuration is spread across **Commercial Config**, native Customer/Contact records and individual Commercial DocTypes. Do not expect a separate custom SPA administration area.

## On this page

- [Roles and responsibilities](#roles-and-responsibilities)
- [Review the day before taking action](#review-the-day-before-taking-action)
- [Generate and regenerate boards](#generate-and-regenerate-boards)
- [Configure commercial pipelines](#configure-commercial-pipelines)
- [Resolve customer ownership and contact selection](#resolve-customer-ownership-and-contact-selection)
- [Manage consent and reachability](#manage-consent-and-reachability)
- [Configure outcomes and follow-up policies](#configure-outcomes-and-follow-up-policies)
- [Set Commercial Settings](#set-commercial-settings)
- [Handle data quality and exceptions](#handle-data-quality-and-exceptions)
- [Import data safely](#import-data-safely)
- [Daily manager checklist](#daily-manager-checklist)

## Roles and responsibilities

| Role | Main capabilities |
| --- | --- |
| **Commercial Sales User** | Read and work the Dayboard, create drafts, log contacts, apply permitted outcomes, follow up |
| **Commercial Manager** | Sales actions plus manager review, sensitive cancellations, outcome reapplication, strong Dayboard regeneration and import tasks |
| **Commercial Admin** | Manager capabilities plus configuration and outcome maintenance |
| **System Manager / Administrator** | Native system administration and Commercial role gates |

There is **no separate implemented Sales Support or Commercial Owner role** in the source. Grant the narrowest role needed. Check each DocType's permissions as well as the API's manager gates.

## Review the day before taking action

Start with **Manager Daily Review**, **Today's Dayboard**, **Needs Review Queue** and **Overdue Followups**. The manager review page brings together:

- Items assigned to the configured **Fallback Owner**, meaning no real owner was resolved.
- Duplicate-follow-up warning overrides requiring review.
- Recent cancellations, limited in the source to the last seven days.
- WhatsApp Drafts unsent for more than two days.

Open an item to inspect the customer, reason, owner, contact and history before changing its status.

## Generate and regenerate boards

The source schedules **Active Sales** and **Prospect Onboarding** boards daily at **04:00 site time**. The Commercial Settings generation-time/timezone fields are informational; they do not reschedule the fixed job.

In **Today's Dayboard**, select **Generate Today**, confirm date and board type, then select the appropriate mode:

| Mode | Permission | Behavior |
| --- | --- | --- |
| **Preview** | Commercial user | Shows an estimate without writing changes |
| **Create Missing** | Commercial user | Creates missing work, preserving existing items |
| **Rebuild Open** | Manager or above | Reassesses open reasons; can reset manual priority overrides where selected |
| **Cancel and Regenerate** | Manager or above | Cancels open nonfinal items and recreates work; **confirmation note required** |

Use **Preview** or **Create Missing** for routine checks. Do not use destructive regeneration to hide overdue work, and never do so while sales staff are actively handling that day's queue without coordinating with them.

**Done**, **Cancelled** and **Carried Over** are excluded from ordinary open-item rebuild processing. After any generation, verify counts, exceptions, and errors in the appropriate log.

## Configure commercial pipelines

Open **Commercial Pipeline** from the Commercial Control Tower workspace or Desk search.

Each pipeline has a name, type, status, enabled flag, preferred contact channel, default priority, cadence, default owner and optional day-specific owners, WhatsApp template and holiday adjustment mode.

The source seeds examples such as **Onboarding**, **Monthly Call**, **Delivery-day Reminder** and **Pre-order Wednesday**. The report screenshot shows their membership counts on a sample day, which may differ today.

Common membership states include **Suggested**, **Active**, **Paused**, **Deactivation Suggested**, **Removed**, **Suggested Reactivation** and **Rejected**.

Add or change **Commercial Pipeline Membership** only after confirming the Customer, effective pipeline, status and reason. The guided status transitions are audited. **Do not manually remove memberships solely to decrease today's call total.**

## Resolve customer ownership and contact selection

The source's owner resolution evaluates a **day-specific pipeline owner**, then the **pipeline default owner**, a membership owner override, and finally **Commercial Settings.fallback_owner**.

The native `Customer.customer_owner` is only a reference field for this app, not an automatic fixed account manager.

Contact selection prioritizes a specific pipeline contact override, then eligible default commercial contact, then fallback commercial contact, and finally a preferred or otherwise eligible contact.

Because a fallback owner can make an item appear technically assigned, review **No owner / Fallback** rather than searching for a blank Assigned To field.

## Manage consent and reachability

Before automations generate eligible work, validate:

- **Customer.do_not_contact**, commercial status, holiday pause and closure period.
- The Customer's commercial contact, WhatsApp consent and contact-channel permission by pipeline.
- Commercial opening hours, delivery days and language.
- Whether a customer is Passive/Inactive and restricted to a reactivation pipeline.

The source suppresses work for restricted states, including **Geneutraliseerd** and **Failliet**. Missing data can create a separate Data Quality item instead of authorizing outreach.

When onboarding new accounts, enter correct master data and permission information first, then let the normal generation process create a relevant task.

## Configure outcomes and follow-up policies

**Commercial Contact Outcome** controls the user-facing **Set Outcome** options. Settings include:

- **Status Effect** such as Done, Waiting for Reply, Snoozed, Needs Review, Cancelled or In Progress.
- **Closes Item** and **Creates Follow Up**.
- **Follow Up Default Days**.
- **Membership Effect** such as Pause, Remove or Reactivate.
- **Sets Customer Do Not Contact**, **Signals Order Placed**, **Requires Note**, **Destructive**, **Allowed Channels**, and optional pipeline type.

Examples from the screenshot include **Niets nodig - herhaal in pijplijn**, **Niets nodig - verwijder van pijplijn**, **Besteld**, **Do Not Contact**, **No Answer**, **Unreachable**, **Needs Review**, **Follow-up Needed** and **Done - Ordered**.

Restrict destructive or channel-specific outcomes according to the approved policy. **Unreachable** is configured for phone-contact use, while **No Answer** is suitable for other unanswered contact attempts, subject to current setup.

**Signals Order Placed** does **not** verify a Sales Order in ERPNext. The outcome report explicitly shows **Not integrated**.

## Set Commercial Settings

Open **Commercial Config** or the **Commercial Settings** DocType in Desk. The source includes:

- **Fallback Owner** and **Default Team**.
- **Duplicate Followup Warning Window Days**, default **10**.
- **Follow-up Creates ToDo Mirror**.
- Generation locks and whether manual generation or rebuilding is allowed.
- **WhatsApp Web Base URL**, completion/cancellation note requirements.
- Passive-customer reactivation restrictions, contact frequency and follow-up windows.
- Import field ownership and optionally enabled Google Drive Links.
- An **Excluded Customers** list.

Changing these affects work-generation and reporting rules. Require an explicit business owner decision, a staging test, and a recorded configuration change. In particular, a setting that looks like a scheduler time is **informational only** in the current code.

## Handle data quality and exceptions

The Data Quality rules can flag missing primary contact, WhatsApp number, undecided consent, preferred language, owner, delivery day, opening hours, closures, and do-not-contact conflicts.

Use **Data Quality Queue**, **Needs Review Queue**, **Overdue Followups**, and **Duplicate Override Audit** to prioritize and investigate. Corrections should normally be made to the master record in ERPNext, not hidden by simply marking the data-quality item Done.

The Manager Daily Review also provides early warning about stale WhatsApp drafts and cancelled work.

## Import data safely

The repository includes controlled import scripts and **Commercial Settings → Import: fields Mappa may overwrite**.

By default, import rules should **only fill empty existing values**, not overwrite already enriched Customer/Contact fields. Before importing:

1. Confirm the approved input and data owner.
2. Run the documented dry-run/preview procedure.
3. Review additions, changes and conflicts with the sales owner.
4. Take an approved backup and confirm rollback requirements.
5. Run the authorized importer and inspect its change log.
6. Validate a sampling of Customers, Contacts and pipeline memberships in Desk.

Never paste a manual terminal command from a development README into production without an approved deployment procedure. The old repository README may still reference a former organization URL.

## Daily manager checklist

- [ ] Today's Active Sales and Prospect Onboarding boards generated and reconciled.
- [ ] Critical/High and overdue work have owners.
- [ ] Fallback-owned items claimed or assigned.
- [ ] Needs Review and Data Quality queues triaged.
- [ ] Drafts older than two days checked for legitimate pending sends.
- [ ] Duplicate overrides and sensitive cancellations reviewed.
- [ ] Pipeline memberships and contact permissions updated where approved.
- [ ] Follow-ups consistent with actual customer activity.
- [ ] Sales/order conversion numbers kept separate from verified ERP Sales Orders.

[CRM Dayboard contents](README.md) | [Sales User Guide](sales-user-guide.md) | [Reports](reports.md)
