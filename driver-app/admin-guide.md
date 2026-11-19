# Driver App administrator guide

**Audience:** Operational Admin, planner and HR/Payroll where explicitly permitted.  
**Status:** Backend and technical specification reviewed; the dedicated management frontend and actual enabled modules are **not verified on the B2B main branch**. Treat all click paths in the technical specification as provisional.

## 1. What an administrator manages

The backend has separate functions for driver profiles, availability, month plans, replacements, hours, vehicles, damages, fines, manuals, incident handling and exports. Rights are enforced server-side.

**Roles**

- **Operational Admin:** broad operational management and driver-specific administration.
- **Operational Driver:** own profile, own assignments and permitted own requests/records.
- **Operational HR Payroll:** restricted profile view and export access only when the relevant switch permits it.

## 2. Enabling the app safely

The documented **Geofood Driver Settings** include separate feature switches:

| Switch | Purpose / default |
| --- | --- |
| `enabled` | Master switch, off by default |
| `workday_enabled` | Hours and workday features, off by default |
| `vehicles_enabled` | Fleet features, off by default |
| `dossiers_enabled` | Driver dossier features, off by default |
| `push_enabled` | Push delivery, off by default |
| `offline_write` | Offline write queue, off by default |
| `payroll_export_hr` | Allow HR/Payroll to download exports, off by default |

**Do not enable everything together.** The production rollout requires a backup, compatible frontend/backend deployment, configuration of privacy settings and a staged acceptance process. No settings or switches are changed by this documentation.

## 3. Create or complete driver profiles

The backend specification describes an administrator **Add a driver** flow, including **New employee**.

A new employee/profile creation requires validated personnel and contract details. The application refuses duplicate identifiers and duplicate employee identities. It does **not** automatically create a User/login or supply missing availability.

For an existing employee who lacks personnel number or contract type, an approved fill-empty-only completion action is available in the backend. Existing values cannot silently be overwritten.

After profile creation:

1. Check whether contact details and availability are complete.
2. Resolve missing information before scheduling or creating login access.
3. Use the reviewed login-creation action separately.
4. Test the newly created driver account with driver-only access.

> **[Screenshot needed: `driver-app/images/admin-add-driver.png`]** Show the actual add-driver workflow with a fictitious employee and the incomplete-profile indicator.
>
> **[Screenshot needed: `driver-app/images/admin-login-review.png`]** Show the admin login preview and the separate creation action, with no real account details.

## 4. Prepare the monthly driver plan

The month planner supports:

- Fixed and flexible driver work patterns.
- Availability and approved leave.
- Route/driver familiarity, hard constraints and candidate scoring.
- Generated plans that can be reviewed, manually adjusted and published.
- A **shadow month** that remains invisible to drivers and does not trigger ordinary driver notices.

Recommended process:

1. Check current availability, leave and readiness of active profiles.
2. Generate the next period in **shadow** mode for a dry run.
3. Resolve hard constraints and conflicts, documenting any intentional override.
4. Confirm driver and route coverage.
5. Publish only after operational approval.
6. If appropriate, convert an approved shadow plan to a published plan.

> **[Screenshot needed: `driver-app/images/admin-month-plan.png`]** Show a fictional monthly driver plan with conflicts and publication state clearly visible.

## 5. Handle leave, availability and replacements

Availability changes and leave requests require a management decision. A replacement request triggered by an approved absence may be handled automatically under an enabled policy, but the administrator remains responsible for confirming the final plan.

Replacement calls can be offered to eligible drivers. The documented job handles first valid acceptance, reminders and escalation when no one accepts. Check the final assignment and notification status instead of relying on a phone call alone.

> **[Screenshot needed: `driver-app/images/admin-requests.png`]** Show the admin pending-request queue and an approval/rejection decision.
>
> **[Screenshot needed: `driver-app/images/admin-replacements.png`]** Show an active fictional replacement call and response trail.

## 6. Work hours and payroll

When workday tracking is enabled, the backend records working days for both fixed and flexi drivers, allows correction and dispute handling, and supports month close and versioned payroll exports.

- Review forgotten or disputed registrations before payroll close.
- Validate mapping to the approved payroll columns.
- Distinguish provisional exports from the confirmed mapping.
- Treat any correction after close as a versioned change with an audit trail.
- Restrict payroll export access to approved administrators and HR recipients.

The application does not replace the employer's payroll validation responsibilities.

> **[Screenshot needed: `driver-app/images/admin-hours.png`]** Show the workday exception/approval view with test records.
>
> **[Screenshot needed: `driver-app/images/admin-payroll.png`]** Show month close and export version, with compensation and personal data hidden.

## 7. Manage vehicles

The backend supports vehicle setup, assignment, service and maintenance checks, odometer history, departure evidence and damage baselines.

Before making a vehicle available, confirm its approved baseline and service data. A vehicle lacking the required baseline must not be allocated by the normal flow. Resolve unavailability and maintenance warnings before publication or dispatch.

> **[Screenshot needed: `driver-app/images/admin-vehicles.png`]** Show test vehicle readiness, maintenance warnings and assignment.

## 8. Manage driver dossiers

Administrators can review damage reports, fines and disputes, publish versions of the logistics manual, require read confirmations, and manage route information sheets. Drivers see only their authorized subsets.

Do not disclose a tentative fine or internal responsibility assessment to drivers before the workflow permits it. Do not upload sensitive dossier records to this public documentation repository.

> **[Screenshot needed: `driver-app/images/admin-dossiers.png`]** Show test dossier sections and a manual acknowledgment overview.

## 9. Incident, privacy and emergency operations

The backend includes:

- A critical-incident switch that stops affected functions until explicitly released.
- A restricted emergency export for planning continuity.
- An audit log for important actions.
- A retention policy owner who must approve data retention periods before automated cleanup.
- A go-live readiness checklist requiring separate sign-offs.

Changes to retention, payroll access and incident stops must be reviewed as operational controls, not treated as ordinary UI preferences.

> **[Screenshot needed: `driver-app/images/admin-readiness.png`]** Show a fictitious go-live checklist and unresolved items. Hide all internal contacts and private details.

## 10. Known limits and deferred functionality

- Dedicated driver/admin screens and actual navigation are still to be confirmed on the current deployed frontend.
- OCR for odometer readings has no provider configured by default.
- Departure GPS is off by default.
- Offline damage/fine photo submission is not queued.
- Push needs real-device acceptance.
- Temperature logging and Routific API are deferred in the source specification.

## Release gate before publishing end-user instructions

- [ ] Confirm compatible backend and frontend versions.
- [ ] Confirm enabled modules and roles.
- [ ] Check driver-only data isolation.
- [ ] Walk through the real phone application with a test account.
- [ ] Verify replacement, workday, vehicle and dossier flows on actual devices.
- [ ] Confirm privacy owner, retention policy, backups and incident process.
- [ ] Add sanitized screenshots, then mark the individual guides production-verified.

[Driver App contents](README.md) | [Driver guide](driver-guide.md)
