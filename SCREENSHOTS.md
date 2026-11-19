# Screenshot capture checklist

Each guide now contains **inline Markdown image references** at the exact position where its screenshots belong. Seventeen sanitized screenshots have been uploaded and placed at the correct paths. Other planned screenshot slots still show missing-image previews until their images are added. Uploading the PNG to the listed path makes it appear automatically, without editing the guide. Do not commit active QR codes, passwords, customer details, real payroll data, live employee information, access tokens or real vehicle registration information.

## On this page

Select a section to jump directly to it.

- [How to capture and submit](#how-to-capture-and-submit)
- [Captures supplied on 19 November 2026](#captures-supplied-on-19-november-2026)
- [Taskboard screenshots](#taskboard-screenshots)
- [Driver App screenshots](#driver-app-screenshots)
- [Do not capture](#do-not-capture)

## How to capture and submit

1. Use a test or demonstration account with fictitious employee names, dates and tasks.
2. Capture the application at desktop width for admin pages, and phone width for employee/driver screens where appropriate.
3. Include enough of the surrounding interface to identify the screen and action.
4. Save the file using the exact path in this checklist. Create the `images/` folders only when the first image is ready.
5. Check for sensitive data in the screenshot, including notifications and browser tabs.
6. Upload the approved PNG to the **exact filename and folder** below, for example `taskboard/images/employee-today.png`. Each guide already includes an inline image tag such as `![Employee Today](images/employee-today.png)`. **No Markdown change is needed** to display it.
7. Record the deployed app version and capture date in the documentation update.

## Captures supplied on 19 November 2026

**17 real screenshots were reviewed and mapped to the guides.** A sanitized image bundle has been prepared with staff names/IDs/email addresses and the live attendance QR masked. **All 17 PNG files are now present in GitHub at their expected paths.** Other screenshot slots remain deliberately unfilled until the UI and safe examples can be captured.

| Image path expected in the wiki | What it shows | Asset status |
| --- | --- | --- |
| `taskboard/images/admin-week-not-generated.png` | Ungenerated weekly plan and Generate action | Uploaded, linked |
| `taskboard/images/admin-week-to-plan.png` | Draft week, flexible task day selector, Schedule/Skip | Uploaded, linked |
| `taskboard/images/admin-week-calendar.png` | Week calendar and execution summary | Uploaded, linked |
| `taskboard/images/admin-week-calendar-detail.png` | Additional daily tasks and department color legend | Uploaded, linked |
| `taskboard/images/attendance-admin-qr-redacted.png` | Admin attendance card with QR code obscured | Uploaded, linked |
| `taskboard/images/attendance-registrations.png` | My registrations tab, empty sample history | Uploaded, linked |
| `taskboard/images/admin-library.png` | Task library search and filters | Uploaded, linked |
| `taskboard/images/admin-template-editor.png` | Task editor, primary fields | Uploaded, linked |
| `taskboard/images/admin-template-fields.png` | Task editor, advanced flags | Uploaded, linked |
| `taskboard/images/admin-holidays.png` | Holiday calendar and sync action | Uploaded, linked |
| `taskboard/images/admin-calendar-day-form.png` | Manual calendar-day form | Uploaded, linked |
| `taskboard/images/admin-report-summary.png` | Report overview and open-task follow-up | Uploaded, linked |
| `driver-app/images/admin-drivers-overview.png` | Driver readiness and availability, identities obscured | Uploaded, linked |
| `driver-app/images/admin-route-knowledge.png` | Route familiarity matrix, identities obscured | Uploaded, linked |
| `driver-app/images/admin-login-review.png` | Driver login status, personal fields obscured | Uploaded, linked |
| `driver-app/images/admin-settings.png` | Feature switches, retention, incidents, export | Uploaded, linked |
| `driver-app/images/admin-month-plan.png` | Driver month planning, shadow plan and route patterns | Uploaded, linked |

The 17 supplied screenshots are in `taskboard/images/` and `driver-app/images/`. The remaining items below are planned captures. Before adding further images, check for private information and live QR tokens.

## Taskboard screenshots

| File path | Screen to capture | Include |
| --- | --- | --- |
| `taskboard/images/taskboard-overview.png` | Employee Today page | Navigation, tasks by department, progress |
| `taskboard/images/employee-sign-in.png` | Sign-in form | Email/password fields, no entered credentials |
| `taskboard/images/employee-today.png` | Employee task list | Date arrows, status, read-only vs editable tasks |
| `taskboard/images/employee-not-done.png` | Not Done form | Reason selector, note field, Save |
| `taskboard/images/employee-move.png` | Move task | Date picker and limit |
| `taskboard/images/employee-add-task.png` | Add task | Ad hoc library and own-task options |
| `taskboard/images/attendance-employee.png` | Attendance | Register and My registrations tabs |
| `taskboard/images/attendance-scan-result.png` | Check-in result | Success state only, no token |
| `taskboard/images/attendance-admin-qr-redacted.png` | Admin QR card | Download control; QR image fully obscured |
| `taskboard/images/admin-holidays.png` | Admin calendar | Year, official sync, sample closure |
| `taskboard/images/admin-library.png` | Task templates | Filters, search, edit/deactivate |
| `taskboard/images/admin-template-editor.png` | Task template form | Planning type, flags, assignments |
| `taskboard/images/admin-week-to-plan.png` | Weekplanning | Week picker, draft status, To Plan |
| `taskboard/images/admin-week-calendar.png` | Week calendar | Department cards, details |
| `taskboard/images/admin-report-filters.png` | Reports filter bar | Date range, status, export |
| `taskboard/images/admin-report-summary.png` | Reports output | Summary and a harmless task |

## Driver App screenshots

**Hold these until the dedicated frontend and deployed feature switches are confirmed.** A backend model is not evidence that a specific screen exists.

| File path | Screen to verify and capture | Include |
| --- | --- | --- |
| `driver-app/images/driver-home.png` | Phone dashboard | Test driver and visible navigation |
| `driver-app/images/driver-published-plan.png` | Driver schedule | Published date, route, start |
| `driver-app/images/driver-availability.png` | Availability/leave request | Form and approval status |
| `driver-app/images/driver-replacement.png` | Replacement offer | Accept/decline and outcome |
| `driver-app/images/driver-workday.png` | Workday registration | Start, end, correction |
| `driver-app/images/driver-odometer.png` | Odometer photo | Reading and anonymized test photo |
| `driver-app/images/driver-damage.png` | Damage report | Description and sample evidence |
| `driver-app/images/driver-manual.png` | Logistics manual | Version and read confirmation |
| `driver-app/images/admin-add-driver.png` | New driver | Test employee creation and readiness |
| `driver-app/images/admin-login-review.png` | Login review | Separate user creation controls |
| `driver-app/images/admin-month-plan.png` | Month plan | Shadow/published state and conflicts |
| `driver-app/images/admin-requests.png` | Requests queue | Pending review and decision controls |
| `driver-app/images/admin-replacements.png` | Replacement calls | Candidate / response progression |
| `driver-app/images/admin-hours.png` | Time corrections | Fictitious exception |
| `driver-app/images/admin-payroll.png` | Payroll | Close/export controls, all private data hidden |
| `driver-app/images/admin-vehicles.png` | Fleet | Baseline, vehicle status, warnings |
| `driver-app/images/admin-dossiers.png` | Dossiers | Categories, permissions, confirmations |
| `driver-app/images/admin-readiness.png` | Readiness | Red/green checklist with no personal data |

## Do not capture

- Real attendance QR codes, even if they appear permanent.
- Authentication cookies, API keys, passwords or login invitation URLs.
- Personal employee or driver dossiers, home addresses, phone numbers, payroll amounts or fine details.
- Live customer/supplier order data.

If safe staging data is not available, **leave the placeholder in Markdown** and ask the app owner for an approved demo environment.

[Documentation home](README.md)
