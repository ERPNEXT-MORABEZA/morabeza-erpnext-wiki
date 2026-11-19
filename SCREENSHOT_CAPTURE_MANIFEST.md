# Carnivale ERPNext: AI screenshot capture manifest

**Canonical, single-file inventory** for screenshots in the public [`morabeza-erpnext-wiki`](https://github.com/KingSolomun79/morabeza-erpnext-wiki) documentation repository. Prepared from the wiki's existing guides and screenshot inventories on **19 November 2026**. This is a **capture plan**, not evidence that unverified or disabled screens work.

**Baseline:** 35 images already uploaded; **51 further captures identified** (15 gated/conditional). Capture status must be checked again against the repository tree before beginning. Existing files are **not** to be overwritten by default.

## Quick navigation

- [Copy-paste instruction for the AI capture agent](#copy-paste-instruction-for-the-ai-capture-agent)
- [Safety and capture procedure](#safety-and-capture-procedure)
- [Confirmed navigation entry points](#confirmed-navigation-entry-points)
- [A. Taskboard screenshots to capture](#a-taskboard-screenshots-to-capture)
- [B. Driver App screenshots to capture](#b-driver-app-screenshots-to-capture)
- [C. B2B Order App screenshots to capture](#c-b2b-order-app-screenshots-to-capture)
- [D. CRM Dayboard screenshots to capture](#d-crm-dayboard-screenshots-to-capture)
- [Already uploaded: do not duplicate](#already-uploaded-do-not-duplicate)
- [Embedding, QA and completion report](#embedding-qa-and-completion-report)

## Copy-paste instruction for the AI capture agent

```text
OBJECTIVE: Populate the existing Carnivale ERPNext public documentation wiki with all safely obtainable screenshots listed in SCREENSHOT_CAPTURE_MANIFEST.md.
TARGET REPOSITORY: https://github.com/KingSolomun79/morabeza-erpnext-wiki
MANIFEST FILE: SCREENSHOT_CAPTURE_MANIFEST.md (repository root).
APP: Authorized Carnivale ERPNext instance and related /taskboard and /b2b portal pages, using an authorized browser session.
READ FIRST: This entire manifest, plus the target guide for each image. Use the exact filename and folder listed in the manifest.
WORKFLOW: Confirm the current repository tree; skip images already present; obtain authorized read-only staging/demo access and fictional data; navigate by the verified labels; capture the correct state; sanitize BEFORE writing any file in the public repo; save approved PNG to exact repo-relative path; ensure every new image is referenced in the appropriate guide; validate the preview and privacy; prepare a reviewable pull request, not a direct production data change.
CONSTRAINTS: Do not edit application code or ERP settings. Do not enable disabled driver features. Do not create/change real tasks, users, orders, customers, drivers, schedules, attendance, sales outcomes, messages, pricing, payroll or records. Do not send WhatsApp/email, accept replacement offers, publish plans, finalize orders, trigger imports or confirm a live attendance scan. Opening a form or harmless Preview is allowed when permissions permit. Use an approved test environment for any action requiring state.
SAFETY: The wiki is PUBLIC. No real people, email/phone/WhatsApp contacts, employee IDs, customer/order data, prices, active QR codes, cookies, secrets, private messages, fines, salary information or live tokenized share links. Use fictional records or irreversible solid-mask redaction; inspect browser URL, notifications and background panels. Never upload raw originals. Do not invent any UI or fake a successful operation. If a screen does not exist or is disabled, mark BLOCKED with evidence and move on.
ACCEPTANCE: Each new screenshot is a real capture from the correct page, named exactly as specified, cleanly cropped, private data removed, placed in the correct images/ directory, linked with meaningful alt text from the correct Markdown guide, and rendered successfully in GitHub. Report completed/blocked/remaining by ID, exact paths, application version if known, and a pull request URL or the reason no PR could be created.
```

## Safety and capture procedure

1. **Start with repository and environment inspection.** Work in an authorized checkout of this wiki. If no local checkout is available, select/clone into an approved workspace. Do not assume a local Windows directory. This is the **documentation repo**; application repositories remain read-only.
2. **Use an authorized demonstration environment.** Prefer staging and synthetic accounts with the minimum role needed. A production session may be inspected read-only, but do not alter real data just to produce a screenshot. If no harmless sample exists, mark the requested image **BLOCKED**.
3. **Capture only the real UI.** Standard desktop capture around 1440×900 for Desk/admin and 390×844 for driver/employee mobile. Crop to the relevant control and its screen title; do not resize text to illegibility. Use PNG with a descriptive alt label. Multiple captures are permissible for different states, but do not silently substitute a different feature.
4. **Redact irreversibly before adding files to the wiki.** Use solid opaque masks or approved fictitious test records, not transparent overlays or light blur. Include headers, browser tabs, URL paths containing tokens, notification toasts, sidebar identities and photos in the inspection. Completely obscure all **live attendance QR codes**, not merely their center.
5. **Respect feature gates and human approval.** The Driver App phone UI was not verified in the prior source review; hours, vehicles, dossiers and some mobile/offline capabilities were disabled in the captured settings. Open and report what exists, but never change switches just for a screenshot. Use **Preview**, not Generate/Publish/Rebuild/Save when this changes records.
6. **Save in the exact repository-relative directory.** For example: `taskboard/images/employee-not-done.png`, `driver-app/images/admin-requests.png`, `b2b-order-app/images/admin-b2b-settings.png`, or `CRM-DAYBOARD/images/commercial-settings.png`. Do not create alternative filenames such as `Screenshot (3).png`, do not put files under the application source repositories, and do not add unsafe unredacted assets to commits.
7. **Mark an image done only after checking** real content, the exact path, an actual Markdown inline reference near the relevant step, and GitHub rendering. Newly requested B2B Desk and CRM management images may lack inline placeholders; add references to the listed guide after the capture passes review. Keep existing `## On this page` jump links valid. Do not rename historical image assets.
8. **Submit a reviewable PR and completion table.** Separate already-uploaded, newly captured, unavailable/disabled and waiting-for-test-data counts. Images that could not safely be captured remain in the manifest as pending, not fake images or broken instructions.

**Status key:** `P1` = highest-value missing capture, try first on an authorized account. `P2` = useful follow-up/secondary screen. `HOLD` = requires evidence of real enabled UI and/or synthetic test state before capture. These are capture priorities, **not claims about the feature being released**.

## Confirmed navigation entry points

| Application | Starting point | Notes |
| --- | --- | --- |
| Taskboard employee | <https://carnivale.frappe.cloud/taskboard> | Linked operational Employee and role required |
| Taskboard management | <https://carnivale.frappe.cloud/taskboard/admin> | Team Leader / Operational Admin permissions |
| Driver App admin | Operations sidebar → **Chauffeurs**, then the named tab | Deployed admin navigation verified in screenshots; exact URL and driver mobile URL not verified |
| B2B portal | <https://carnivale.frappe.cloud/b2b> | Customer test account, portal rather than ERPNext Desk |
| B2B catalog | <https://carnivale.frappe.cloud/b2b/catalog> | Customer filtering and ordering |
| B2B staff Links | <https://carnivale.frappe.cloud/b2b/links> | Restricted staff view; shared token URL must not appear in captures |
| B2B administrator | ERPNext **Desk** search for Customer / Item / Item Price / B2B Settings / B2B Delivery Rule / Sales Order | Different roles see different controls |
| CRM Dayboard | ERPNext **Desk** → **Commercial Control Tower** workspace | Select Today's Dayboard, Manager Daily Review, reports and Commercial Config in the sidebar |
| CRM configuration | ERPNext **Desk** search for Commercial Pipeline, Commercial Pipeline Membership, WhatsApp Template, Commercial Contact Outcome, Commercial Settings | Restrict to authorized commercial admin |

## A. Taskboard screenshots to capture

**9 missing captures.** Real employee actions require a staging task. The five Taskboard management screenshot variants already uploaded below should not be replaced. For `employee-add-task.png`, if the library and own-task form cannot fit readably in one image, capture the primary view and note the second missing state for a follow-up.

| ID | Priority / role | Screen to open | What the screenshot must demonstrate | Exact PNG destination | Add inline in guide |
| --- | --- | --- | --- | --- | --- |
| **TB-01** | P1, Employee | `/taskboard`, **Vandaag** | Date, grouped task cards, progress and status; use fictional tasks | `taskboard/images/taskboard-overview.png` | `taskboard/README.md` |
| **TB-02** | P1, Employee | Sign-in page before entering credentials | Login form and sign-in controls, empty inputs; use separate browser session | `taskboard/images/employee-sign-in.png` | `taskboard/employee-guide.md` |
| **TB-03** | P1, Employee | `/taskboard`, **Vandaag** | Date arrows, eligible versus read-only task cards, grouping and progress | `taskboard/images/employee-today.png` | `taskboard/employee-guide.md` |
| **TB-04** | P1, Employee | Open a test task, **Niet uitgevoerd** | Reason selector and note input, before saving; no operational mutation | `taskboard/images/employee-not-done.png` | `taskboard/employee-guide.md` |
| **TB-05** | P1, Employee | Eligible test task, **Verplaatsen** | Destination date, any maximum-date explanation and confirmation, before saving | `taskboard/images/employee-move.png` | `taskboard/employee-guide.md` |
| **TB-06** | P1, Employee | **Taak toevoegen** / add own task | Task-library picker and own-task inputs; use one or two safe crops only if both views exist | `taskboard/images/employee-add-task.png` | `taskboard/employee-guide.md` |
| **TB-07** | P1, Employee | `/taskboard`, **Tijdsregistratie** | **Registreren** and **Mijn registraties** tabs with camera-scan control; exclude live QR | `taskboard/images/attendance-employee.png` | `taskboard/attendance.md` |
| **TB-08** | HOLD, Employee + test attendance | Attendance QR scan result in approved test environment | Real successful *test* scan confirmation, without any QR/token, ID or private attendance history | `taskboard/images/attendance-scan-result.png` | `taskboard/attendance.md` |
| **TB-09** | P1, Team Leader / Admin | `/taskboard/admin` → **Rapporten** | From/through dates, department, assignment/status filters and CSV export control | `taskboard/images/admin-report-filters.png` | `taskboard/reports.md` |

## B. Driver App screenshots to capture

**16 missing captures, many gated.** `Chauffeurs` tabs are verified on the deployed admin site, but **the mobile driver interface has not been verified** and some administrative features were off. Record actual visibility before trying each capture. Do not enable any feature switch or invent mobile URLs.

| ID | Priority / role | Screen to open | What the screenshot must demonstrate | Exact PNG destination | Add inline in guide |
| --- | --- | --- | --- | --- | --- |
| **DR-01** | HOLD, Driver test account | Verified driver mobile dashboard URL, not yet established | Actual phone home/navigation; do not infer mobile UI from backend | `driver-app/images/driver-home.png` | `driver-app/driver-guide.md` |
| **DR-02** | HOLD, Driver test account | Mobile published schedule / plan | Published date, route and start time with fictional assignment | `driver-app/images/driver-published-plan.png` | `driver-app/driver-guide.md` |
| **DR-03** | HOLD, Driver test account | Mobile availability / leave request | Request form and Submitted/Pending/Approved state in a safe test | `driver-app/images/driver-availability.png` | `driver-app/driver-guide.md` |
| **DR-04** | HOLD, Driver test account | Mobile replacement offer | Fictional offer, accept/decline controls and response; no replaced colleague name | `driver-app/images/driver-replacement.png` | `driver-app/driver-guide.md` |
| **DR-05** | HOLD, Driver test account | Mobile workday / time registration | Test clock-in/out, start/end and correction action, if feature enabled | `driver-app/images/driver-workday.png` | `driver-app/driver-guide.md` |
| **DR-06** | HOLD, Driver test account | Mobile odometer / departure evidence | Numeric mileage, photo input and test vehicle, with plates obscured | `driver-app/images/driver-odometer.png` | `driver-app/driver-guide.md` |
| **DR-07** | HOLD, Driver test account | Mobile damage/incident form | Fictional incident description and non-identifying sample photo | `driver-app/images/driver-damage.png` | `driver-app/driver-guide.md` |
| **DR-08** | HOLD, Driver test account | Mobile logistics manual / dossier reading | Fictional manual version and acknowledgment state | `driver-app/images/driver-manual.png` | `driver-app/driver-guide.md` |
| **DR-09** | P1, Operations Admin | **Chauffeurs** → **Chauffeurs en logins** → **Chauffeur toevoegen** | Actual new-driver form and readiness validation; do not save a real employee | `driver-app/images/admin-add-driver.png` | `driver-app/drivers-and-logins.md; driver-app/admin-guide.md` |
| **DR-10** | P1, Operations Admin | **Chauffeurs** → **Aanvragen** | Pending fictional leave/availability request and approve/reject controls | `driver-app/images/admin-requests.png` | `driver-app/requests-and-replacements.md; driver-app/admin-guide.md` |
| **DR-11** | P1, Operations Admin | **Chauffeurs** → **Vervangingen** | Test replacement call, candidate/response status and assignment state | `driver-app/images/admin-replacements.png` | `driver-app/requests-and-replacements.md; driver-app/admin-guide.md` |
| **DR-12** | HOLD, Operations Admin / HR | **Chauffeurs** → **Uren**, when enabled | Workday and correction/approval queue using fabricated records | `driver-app/images/admin-hours.png` | `driver-app/hours-vehicles-dossiers.md; driver-app/admin-guide.md` |
| **DR-13** | HOLD, Authorized payroll admin | **Chauffeurs** → **Uren** → month close/payroll, if exposed | Closed month/export version only; mask compensation, personnel, hours | `driver-app/images/admin-payroll.png` | `driver-app/hours-vehicles-dossiers.md; driver-app/admin-guide.md` |
| **DR-14** | HOLD, Operations Admin | **Chauffeurs** → **Voertuigen**, when enabled | Fictitious fleet readiness, assignments, warnings; no registration plates | `driver-app/images/admin-vehicles.png` | `driver-app/hours-vehicles-dossiers.md; driver-app/admin-guide.md` |
| **DR-15** | HOLD, Authorized admin | **Chauffeurs** → **Dossiers**, when enabled | Only mock dossier categories and read acknowledgments; no real fines or damage reports | `driver-app/images/admin-dossiers.png` | `driver-app/hours-vehicles-dossiers.md; driver-app/admin-guide.md` |
| **DR-16** | P1, Operations Admin | **Chauffeurs** → **Go-live** | Readiness checklist and blockers; mask internal contact information | `driver-app/images/admin-readiness.png` | `driver-app/settings-and-go-live.md; driver-app/admin-guide.md` |

## C. B2B Order App screenshots to capture

**8 additional ERPNext Desk admin captures.** All nine original customer/Links screenshots already exist. These newly named Desk images are **proposed destinations**, not existing image references. After safe capture, add each to the corresponding subsection of `b2b-order-app/admin-guide.md`. Import dry-run is gated and not necessarily a graphical UI.

| ID | Priority / role | Screen to open | What the screenshot must demonstrate | Exact PNG destination | Add inline in guide |
| --- | --- | --- | --- | --- | --- |
| **B2B-01** | P1, ERPNext authorized Customer admin | Desk search → **Customer**, open fictional customer | Customer document and linked portal users; redact real addresses and email | `b2b-order-app/images/admin-customer-portal-users.png` | `b2b-order-app/admin-guide.md` |
| **B2B-02** | P1, ERPNext authorized Customer admin | Desk **Customer** → **delivery_days** child table | Weekdays, delivery type and cutoff fields for sample customer | `b2b-order-app/images/admin-customer-delivery-days.png` | `b2b-order-app/admin-guide.md` |
| **B2B-03** | P1, B2B Catalog Manager | Desk search → **Item**, use test Item in **Carnivale Products** tree | Enabled state, group, brand, image, units, category/labels, without confidential prices | `b2b-order-app/images/admin-item-catalog.png` | `b2b-order-app/admin-guide.md` |
| **B2B-04** | P1, B2B Catalog Manager | Desk search → **Item Price**, authorized test Item | Price List **B2B EUR**, currency/unit/effective dates; redact price figures if sensitive | `b2b-order-app/images/admin-item-price-b2b.png` | `b2b-order-app/admin-guide.md` |
| **B2B-05** | P1, System Manager | Desk search → **B2B Settings** | Delivery-rule, unit, per-product delivery and new-product switches; no change | `b2b-order-app/images/admin-b2b-settings.png` | `b2b-order-app/admin-guide.md` |
| **B2B-06** | P1, Sales Manager / System Manager | Desk search → **B2B Delivery Rule** | Territory, enabled flag, deadline, weekday list, closed/extra exceptions | `b2b-order-app/images/admin-delivery-rule.png` | `b2b-order-app/admin-guide.md` |
| **B2B-07** | P1, Authorized Sales user | Desk search → **Sales Order**, safe B2B test draft | Shopping Cart order type, delivery/items, draft versus submitted controls; no real order | `b2b-order-app/images/admin-sales-order-review.png` | `b2b-order-app/admin-guide.md` |
| **B2B-08** | HOLD, Authorized import operator | Approved staging import dry-run, only if UI/approved report exists | Summary of proposed create/update/conflict counts; never run production import | `b2b-order-app/images/admin-import-dry-run.png` | `b2b-order-app/admin-guide.md` |

## D. CRM Dayboard screenshots to capture

**18 additional CRM manager/sales captures.** The nine prior CRM screenshots are already in GitHub. These newly named files are **proposed destinations** and require a Markdown embed beside the relevant guide subsection once captured. Use safe sample customers and avoid real WhatsApp drafts or consent history.

| ID | Priority / role | Screen to open | What the screenshot must demonstrate | Exact PNG destination | Add inline in guide |
| --- | --- | --- | --- | --- | --- |
| **CRM-01** | P1, Commercial Manager | Desk **Commercial Control Tower** → **Manager Daily Review** | Fallback owner items, duplicate overrides, cancellations, stale drafts (mock data) | `CRM-DAYBOARD/images/manager-daily-review.png` | `CRM-DAYBOARD/manager-admin-guide.md` |
| **CRM-02** | P1, Commercial Manager | Commercial Control Tower → **Overdue Followups** | Due dates, filters, ownership and statuses using test customers | `CRM-DAYBOARD/images/overdue-followups.png` | `CRM-DAYBOARD/reports.md` |
| **CRM-03** | P1, Commercial Manager | Commercial Control Tower → **Needs Review Queue** | Open review cases, filters and safe status/owner columns | `CRM-DAYBOARD/images/needs-review-queue.png` | `CRM-DAYBOARD/reports.md` |
| **CRM-04** | P1, Commercial Manager | Commercial Control Tower → **Data Quality Queue** | Missing/invalid contact data rules and resolution context with mock records | `CRM-DAYBOARD/images/data-quality-queue.png` | `CRM-DAYBOARD/reports.md` |
| **CRM-05** | P1, Commercial Manager | Commercial Control Tower → **Duplicate Override Audit** | Override reason and date, test entry and audit columns | `CRM-DAYBOARD/images/duplicate-override-audit.png` | `CRM-DAYBOARD/reports.md` |
| **CRM-06** | P2, Commercial Manager | Commercial Control Tower → **Contact Moments Log** or Desk report search | Historical contact-channel, outcome and owner columns; masked details | `CRM-DAYBOARD/images/contact-moments-log.png` | `CRM-DAYBOARD/reports.md` |
| **CRM-07** | P1, Commercial Sales User | **Today's Dayboard** → **Generate Today** → **Preview** | Date, board type, preview counts and available modes; do not run regenerate | `CRM-DAYBOARD/images/generate-today-preview.png` | `CRM-DAYBOARD/manager-admin-guide.md` |
| **CRM-08** | P2, Commercial Sales User | **Today's Dayboard** → select **Prospect Onboarding** | Board-type selection and staged onboarding items using demo prospects | `CRM-DAYBOARD/images/prospect-onboarding-dayboard.png` | `CRM-DAYBOARD/sales-user-guide.md` |
| **CRM-09** | P1, Commercial Admin | Desk search → **Commercial Pipeline** | Name, type, cadence, owner, channel, priority, enabled state | `CRM-DAYBOARD/images/commercial-pipeline.png` | `CRM-DAYBOARD/manager-admin-guide.md` |
| **CRM-10** | P1, Commercial Admin | Desk search → **Commercial Pipeline Membership** | Customer and pipeline relation, ownership override and membership status using test data | `CRM-DAYBOARD/images/pipeline-membership.png` | `CRM-DAYBOARD/manager-admin-guide.md` |
| **CRM-11** | P2, Commercial Admin | Open test membership → guided status transition | Available transition controls, reason/note and confirmation (before applying) | `CRM-DAYBOARD/images/pipeline-status-transition.png` | `CRM-DAYBOARD/manager-admin-guide.md` |
| **CRM-12** | P2, Commercial Manager | Desk **Customer** / **Contact** and pipeline owner rule | Configured contact selection and ownership fields, without real identity/contact data | `CRM-DAYBOARD/images/customer-ownership-contact.png` | `CRM-DAYBOARD/manager-admin-guide.md` |
| **CRM-13** | P1, Commercial Admin | Desk **Customer** / **Contact** commercial consent section | WhatsApp permission, do-not-contact and permitted channel indicators using demo account | `CRM-DAYBOARD/images/customer-consent.png` | `CRM-DAYBOARD/manager-admin-guide.md` |
| **CRM-14** | P1, Commercial Admin | Desk search → **Commercial Contact Outcome** | Status effect, follow-up defaults, destructive/notes and membership effects | `CRM-DAYBOARD/images/contact-outcome-config.png` | `CRM-DAYBOARD/manager-admin-guide.md` |
| **CRM-15** | P1, Commercial Admin | Commercial Control Tower → **Commercial Config** / **Commercial Settings** | Fallback owner, warning window, manual regeneration and policy fields; no edits | `CRM-DAYBOARD/images/commercial-settings.png` | `CRM-DAYBOARD/manager-admin-guide.md` |
| **CRM-16** | P1, Commercial Sales User / Admin | Desk search → **WhatsApp Template** | Demo template body, editable fields and metadata, no real message/contact | `CRM-DAYBOARD/images/whatsapp-template.png` | `CRM-DAYBOARD/whatsapp-workflow.md; CRM-DAYBOARD/manager-admin-guide.md` |
| **CRM-17** | P2, Commercial Sales User | **Today's Dayboard** → open a customer card | Dayboard Item detail, multiple reasons, owner and next actions, demo customer | `CRM-DAYBOARD/images/dayboard-item-detail.png` | `CRM-DAYBOARD/sales-user-guide.md` |
| **CRM-18** | HOLD, Commercial Sales User | Approved staging scenario triggering duplicate-follow-up warning | Duplicate matches, override reason and safe cancel path; do not create duplicate in production | `CRM-DAYBOARD/images/duplicate-followup-warning.png` | `CRM-DAYBOARD/sales-user-guide.md` |

## Already uploaded: do not duplicate

**Existing asset registry:** these exact PNG paths were verified in the wiki Git tree at manifest creation. They may be re-captured only if screenshots are demonstrably outdated and an approved replacement has passed redaction review. The filenames below must stay stable.

| Existing PNG destination | What it shows |
| --- | --- |
| `taskboard/images/admin-week-not-generated.png` | Week not generated, Generate action |
| `taskboard/images/admin-week-to-plan.png` | Draft week, schedule/skip flexible tasks |
| `taskboard/images/admin-week-calendar.png` | Calendar columns and completion summary |
| `taskboard/images/admin-week-calendar-detail.png` | Lower calendar and department legend |
| `taskboard/images/attendance-admin-qr-redacted.png` | Attendance administration, QR fully masked |
| `taskboard/images/attendance-registrations.png` | My registrations empty demonstration |
| `taskboard/images/admin-library.png` | Task template search/list |
| `taskboard/images/admin-template-editor.png` | Task main edit form |
| `taskboard/images/admin-template-fields.png` | Task advanced settings |
| `taskboard/images/admin-holidays.png` | Holiday calendar and sync |
| `taskboard/images/admin-calendar-day-form.png` | Manual calendar-day form |
| `taskboard/images/admin-report-summary.png` | Report totals and department progress |
| `driver-app/images/admin-drivers-overview.png` | Driver roster and availability, anonymized |
| `driver-app/images/admin-route-knowledge.png` | Route-knowledge matrix, anonymized |
| `driver-app/images/admin-login-review.png` | Reviewed login statuses, anonymized |
| `driver-app/images/admin-settings.png` | Feature switches, retention and incident/export |
| `driver-app/images/admin-month-plan.png` | Monthly planning, shadow plan, route patterns |
| `b2b-order-app/images/customer-home.png` | Customer home and shortcuts |
| `b2b-order-app/images/customer-catalog.png` | Catalog and category filters |
| `b2b-order-app/images/customer-preorder-filters.png` | Pre-order product quick filters |
| `b2b-order-app/images/customer-cart.png` | Cart, quantities, item notes |
| `b2b-order-app/images/customer-delivery.png` | Available delivery-day selector |
| `b2b-order-app/images/customer-review-order.png` | Review and delivery instructions |
| `b2b-order-app/images/customer-order-history.png` | Previous orders and reorder |
| `b2b-order-app/images/customer-favorites-lists.png` | Favorites and saved order lists |
| `b2b-order-app/images/admin-share-links.png` | Staff Links page, product lists and link statuses |
| `CRM-DAYBOARD/images/dayboard-overview.png` | Daily sales board and counters |
| `CRM-DAYBOARD/images/outcome-picker.png` | Set Outcome options |
| `CRM-DAYBOARD/images/log-call.png` | Log Call dialog |
| `CRM-DAYBOARD/images/log-email.png` | Log Email dialog |
| `CRM-DAYBOARD/images/item-more-actions.png` | More: Snooze/Cancel |
| `CRM-DAYBOARD/images/whatsapp-draft-review.png` | Manual WhatsApp draft review |
| `CRM-DAYBOARD/images/whatsapp-draft-status.png` | Draft status report |
| `CRM-DAYBOARD/images/pipeline-health.png` | Pipeline membership report |
| `CRM-DAYBOARD/images/contact-outcomes-report.png` | Contact outcomes report |

## Embedding, QA and completion report

**Embed rule:** For every newly approved image in the table, open its listed Markdown guide and place `![Meaningful UI description](images/<exact-file-name>.png)` immediately after the relevant procedure or subheading. The path is relative to the guide. Where a guide **already** has a matching image tag, upload the image only: do not add a duplicate tag. If an image is blocked, leave the placeholder/guide truthful and do not publish a misleading mockup. Reconcile the top-level `SCREENSHOTS.md` and per-app `SCREENSHOTS.md` inventories only when actually completing a capture batch.

**Check before requesting review:**
- [ ] Every new image originates from the actual authorized application screen, not an AI-generated rendering.
- [ ] Exact filename, case and path match the manifest; PNG is readable.
- [ ] All private content and tokens are irreversibly removed; QR codes are fully hidden.
- [ ] No production writes, sends, imports, login creation, schedule publication or feature-toggle changes were performed.
- [ ] No image from a disabled/absent screen is falsely presented as available.
- [ ] All inline Markdown paths resolve to existing files and the appropriate section.
- [ ] Existing image filenames, existing content and `On this page` jump anchors remain intact.
- [ ] Each guide renders correctly on GitHub; screenshots are contextual and not giant full-page exports.
- [ ] Final report records capture date, environment (production read-only / staging), app build if available, saved paths, and any blockers.

**Completion reporting template:**

| ID | Result: captured / blocked / already present | Exact saved path | Guide embedded? | Screenshot UI verified? | Blocker or note |
| --- | --- | --- | --- | --- | --- |
| TB-01 | … | `taskboard/images/taskboard-overview.png` | … | … | … |

**Escalation rule:** If the screenshot requires generating real customer/driver/attendance data or turning on a module, **stop that row, mark it blocked and request an approved staging/test scenario**. Do not improvise or bypass role permissions. Never use real customer/employee data to make documentation prettier.

[Main wiki](README.md) | [Existing Taskboard and Driver checklist](SCREENSHOTS.md) | [B2B screenshot checklist](b2b-order-app/SCREENSHOTS.md) | [CRM screenshot checklist](CRM-DAYBOARD/SCREENSHOTS.md)
