# Screenshot capture, phase 2 (admin screens): status

Drafts for Jo to accept or reject. Images only: no guide text was changed. The manifest (`SCREENSHOT_CAPTURE_MANIFEST.md`) has no status column, so the status is kept here. Captured read-only on production on 2026-11-23, Desk and Taskboard admin screens, masked with solid opaque rectangles, checked with OCR (tesseract eng+nld) and visually.

Status key: DONE, PARTIAL (real screen, but empty state or partial content), BLOCKED (cannot be captured or the supplied file does not show the requested screen), HOLD (not captured).

| ID | Target file | Status | Note |
| --- | --- | --- | --- |
| B2B-01 | `b2b-order-app/images/admin-customer-portal-users.png` | DONE | From the `B2B-01alt` capture. The file named `B2B-01.png` shows B2B Settings, not the customer, so it was not used |
| B2B-02 | `b2b-order-app/images/admin-customer-delivery-days.png` | BLOCKED | The file named `B2B-02.png` shows the empty B2B Delivery Rule list, not the Customer delivery_days table |
| B2B-03 | `b2b-order-app/images/admin-item-catalog.png` | BLOCKED | The file named `B2B-03.png` shows the B2B Order Request list, not an Item |
| B2B-04 | `b2b-order-app/images/admin-item-price-b2b.png` | BLOCKED | The file named `B2B-04.png` shows the B2B Cart list, not an Item Price |
| B2B-05 | `b2b-order-app/images/admin-b2b-settings.png` | DONE | From the `_clean` capture (no "Not Saved" badge) |
| B2B-06 | `b2b-order-app/images/admin-delivery-rule.png` | BLOCKED | No B2B Delivery Rule records exist |
| B2B-07 | `b2b-order-app/images/admin-sales-order-review.png` | DONE | Draft Sales Order of the test customer, order type Shopping Cart |
| B2B-08 | `b2b-order-app/images/admin-import-dry-run.png` | HOLD | Not captured |
| CRM-01 | `CRM-DAYBOARD/images/manager-daily-review.png` | DONE | Only the "Items With No Owner" block is visible |
| CRM-02 | `CRM-DAYBOARD/images/overdue-followups.png` | PARTIAL | Empty state ("Nothing to show") |
| CRM-03 | `CRM-DAYBOARD/images/needs-review-queue.png` | PARTIAL | Empty state |
| CRM-04 | `CRM-DAYBOARD/images/data-quality-queue.png` | DONE | Customer column masked |
| CRM-05 | `CRM-DAYBOARD/images/duplicate-override-audit.png` | PARTIAL | Empty state |
| CRM-06 | `CRM-DAYBOARD/images/contact-moments-log.png` | PARTIAL | Empty state; this is the Commercial Contact Moment list view, smaller capture (1095 x 549) |
| CRM-07 | `CRM-DAYBOARD/images/generate-today-preview.png` | PARTIAL | Preview toast ("Preview only - no changes made") only; no counts from the preview itself |
| CRM-08 | `CRM-DAYBOARD/images/prospect-onboarding-dayboard.png` | HOLD | Not captured |
| CRM-09 | `CRM-DAYBOARD/images/commercial-pipeline.png` | DONE | The form (Monthly Call) |
| CRM-10 | `CRM-DAYBOARD/images/pipeline-membership.png` | DONE | Customer column masked |
| CRM-11 | `CRM-DAYBOARD/images/pipeline-status-transition.png` | HOLD | Not captured |
| CRM-12 | `CRM-DAYBOARD/images/customer-ownership-contact.png` | DONE | Test customer "Silvano Test"; Customer Owner masked |
| CRM-13 | `CRM-DAYBOARD/images/customer-consent.png` | PARTIAL | Shows the Do Not Contact reason field only; the WhatsApp permission fields are not shown |
| CRM-14 | `CRM-DAYBOARD/images/contact-outcome-config.png` | PARTIAL | List view only; the status effect and follow-up default fields are not shown |
| CRM-15 | `CRM-DAYBOARD/images/commercial-settings.png` | DONE | A help-text line that names an internal document was masked |
| CRM-16 | `CRM-DAYBOARD/images/whatsapp-template.png` | PARTIAL | Empty list, no template open |
| CRM-17 | `CRM-DAYBOARD/images/dayboard-item-detail.png` | HOLD | Not captured |
| CRM-18 | `CRM-DAYBOARD/images/duplicate-followup-warning.png` | HOLD | Not captured |
| TB-09 | `taskboard/images/admin-report-filters.png` | DONE | |
| DR-09 | `driver-app/images/admin-add-driver.png` | HOLD | No capture of the add-driver form. The supplied drivers list shows only the "Chauffeur toevoegen" button and real names, so it was not used |
| DR-11 | `driver-app/images/admin-replacements.png` | PARTIAL | Empty state ("Geen open oproepen") |
| DR-16 | `driver-app/images/admin-readiness.png` | DONE | The "Wie" column (people) masked |

## Masked in every Desk or Taskboard capture

The logged-in user block (name and e-mail, or avatar) in the sidebar and top bar. Also masked where visible: real customer names (CRM-01, CRM-04, CRM-07, CRM-10), the portal user e-mail and Customer Owner (B2B-01, CRM-12), Rate and Amount values and exchange rates (B2B-07), the people named in the "Wie" column (DR-16). The test customer "Silvano Test" is not masked.

## Not used

- `B2B-01.png`, `B2B-02.png`, `B2B-03.png`, `B2B-04.png`: show other screens (see the table).
- `B2B-05-b2b-settings.jpg`: shows a "Not Saved" badge (the `_clean` one was used).
- `B2B-07.png`: Sales Order list with customer names and totals (the draft form was used).
- `CRM-07a_generate-dialog_mode-Create-Missing-NOT-RUN.jpg`: default mode screenshot, not to be published.
- `CRM-09_commercial-pipeline-list.jpg`: the manifest has no name for a list image.
- `CRM-12alt_customer-contact_silvano-test.jpg`: alternative, not needed.
- `CRM-dayboard_REAL-DATA.jpg`: not to be published.
- `DR-weekplan-admin.jpg`: no matching manifest row (an existing `admin-month-plan.png` covers monthly planning).
- `DR-drivers-list-REAL-NAMES.jpg`: real names; does not match DR-09 (form).
- `TB-holidays-admin.jpg`: not in the manifest.
