# CRM Dayboard: Commercial Control Tower

English-language instructions for Carnivale's **Commercial Control Tower**, a Frappe/ERPNext v16 application supporting the daily commercial contact workflow.

**Source application:** [ERPNEXT-MORABEZA/ERPNEXT-MEAT-WHOLESALE-CUSTOM-APP](https://github.com/ERPNEXT-MORABEZA/ERPNEXT-MEAT-WHOLESALE-CUSTOM-APP).  
**Documentation basis:** The source repository's `main` branch and nine UI screenshots supplied 19 November 2026. Screenshots show one demonstration state; customer counts, pipeline membership and enabled configuration will change.  
**Audience:** Sales staff, commercial managers and system administrators. Screens shown in the source are mixed English/Dutch.

## On this page

- [Choose a guide](#choose-a-guide)
- [What this application does](#what-this-application-does)
- [How to begin](#how-to-begin)
- [Permissions and what is not automated](#permissions-and-what-is-not-automated)
- [Documentation maintenance](#documentation-maintenance)

## Choose a guide

**Open the actual application:** [Commercial Control Tower workspace](https://carnivale.frappe.cloud/app/commercial-control-tower) · [Today's Dayboard](https://carnivale.frappe.cloud/app/dayboard) · [WhatsApp Draft Review](https://carnivale.frappe.cloud/app/whatsapp-draft-review) · [Manager Daily Review](https://carnivale.frappe.cloud/app/manager-review) · [Commercial Config](https://carnivale.frappe.cloud/app/commercial-config). These are authenticated ERPNext Desk routes; your role determines what appears.

| Your role or need | Open |
| --- | --- |
| Sales user handling today's customer calls and follow-ups | [Sales User Guide](sales-user-guide.md) |
| Preparing and logging WhatsApp communication | [WhatsApp Draft Workflow](whatsapp-workflow.md) |
| Commercial Manager or Commercial Admin | [Manager and Administrator Guide](manager-admin-guide.md) |
| Reviewing pipeline health, contact outcomes, draft status and queues | [Reports and Monitoring](reports.md) |
| Problems and common questions | [Troubleshooting](troubleshooting.md) |
| Captured images and privacy requirements | [Screenshot Inventory](SCREENSHOTS.md) |

## What this application does

The Dayboard answers **who needs to be contacted today, why, through which channel, and what happens next**. A day may include normal pipeline contacts, overdue follow-ups and data quality tasks. A customer can appear with multiple reasons combined into one item.

The application includes separate **Active Sales** and **Prospect Onboarding** boards, daily generation, owner and priority filtering, call/email logging, manual WhatsApp drafts, outcome-driven follow-ups, manager review and reporting.

It is **not** a replacement for ERPNext Sales Orders, stock management, invoicing or order confirmation. In particular, **Besteld / Done - Ordered** is currently only a commercial outcome signal. The source's **Order Verification** field is **Not integrated**, so it does not prove an ERP order exists.

## How to begin

**Go directly to:** [Today's Dayboard](https://carnivale.frappe.cloud/app/dayboard) after signing in. For exceptions, use [Manager Daily Review](https://carnivale.frappe.cloud/app/manager-review) or [Overdue Followups](https://carnivale.frappe.cloud/app/query-report/Overdue%20Followups).

1. Sign in to Carnivale ERPNext Desk with the Commercial role assigned by the administrator.
2. Open the **Commercial Control Tower** workspace.
3. Select **Today's Dayboard**.
4. Confirm **Date** and **Board Type**.
5. Prioritize Critical/High items and overdue follow-ups.
6. Review all reasons for a customer, contact them through an approved channel, and immediately record the outcome.
7. Use the appropriate manager review or report for exceptions rather than manually maintaining duplicate spreadsheets.

The screenshot examples are redacted and placed at the corresponding step in each guide.

## Permissions and what is not automated

- **Commercial Sales User:** standard contact workflow.
- **Commercial Manager:** sales workflow plus manager review, sensitive cancellations, outcome reapplication and stronger regeneration modes.
- **Commercial Admin:** manager capabilities plus administrative settings and outcome configuration.
- **System Manager / Administrator:** native system-level roles.

WhatsApp messages are **never automatically sent** in this version. **Approve & Copy** only copies the message. The operator sends externally, then returns to record **Mark Sent**. **Skip** records a reason but does not finalize the draft.

The manager or administrator should verify the deployed site, permissions and any unresolved business decisions before treating all source-backed options as approved operating procedure.

## Documentation maintenance

The wiki is public. Do not add real customer names, phone numbers, WhatsApp numbers, email addresses, draft IDs, internal prices or client contact records to screenshots. Keep future images inside `CRM-DAYBOARD/images/` and update the matching guides when controls change.

[Back to main wiki](../README.md)
