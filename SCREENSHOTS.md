# Screenshot capture checklist

This repository intentionally starts with **Markdown-only screenshot placeholders**. Images will be inserted after a live UI walkthrough. Do not commit active QR codes, passwords, customer details, real payroll data, live employee information, access tokens or real vehicle registration information.

## How to capture and submit

1. Use a test or demonstration account with fictitious employee names, dates and tasks.
2. Capture the application at desktop width for admin pages, and phone width for employee/driver screens where appropriate.
3. Include enough of the surrounding interface to identify the screen and action.
4. Save the file using the exact path in this checklist. Create the `images/` folders only when the first image is ready.
5. Check for sensitive data in the screenshot, including notifications and browser tabs.
6. Replace the visible screenshot placeholder in the relevant Markdown guide with standard Markdown, for example `![Employee task list](images/employee-today.png)`.
7. Record the deployed app version and capture date in the documentation update.

### Taskboard screenshots

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
| `taskboard/images/admin-week-overview.png` | Weekplanning | Week picker, draft status, To Plan |
| `taskboard/images/admin-week-calendar.png` | Week calendar | Department cards, details |
| `taskboard/images/admin-report-filters.png` | Reports filter bar | Date range, status, export |
| `taskboard/images/admin-report-summary.png` | Reports output | Summary and a harmless task |

### Driver App screenshots

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
