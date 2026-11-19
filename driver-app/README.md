# Driver App

**Geofood Drivers: planning, availability, work hours and fleet management**

The Driver App connects driver planning and administration with the operational Taskboard. The deployed admin interface is visible in user-provided screenshots; actual driver phone screens remain to be captured.

> **Updated verification notice (19 November 2026):** The uploaded screenshots **confirm a working deployed Chauffeurs administration interface** with tabs for planning, requests, replacements, drivers/logins, hours, vehicles, dossiers, notifications/audit, go-live and settings. Earlier text claiming no driver admin interface could be verified was incomplete. The dedicated screens are still **not found in the reviewed `carnivale-b2b` main branch**, so their source branch/deployment needs reconciliation. A driver-facing phone interface has **not** been shown. Several feature switches were off in the captured settings screen, so a visible tab is not proof its operations are enabled.

## On this page

Select a section to jump directly to it.

- [Choose a guide](#choose-a-guide)
- [Feature areas represented in the backend](#feature-areas-represented-in-the-backend)
- [What is not a promised live feature?](#what-is-not-a-promised-live-feature)
- [Before the guide is released to drivers](#before-the-guide-is-released-to-drivers)

## Choose a guide

| Audience | Guide |
| --- | --- |
| Drivers | [Driver guide: planned workflow and features](driver-guide.md) |
| Administrators, operations planners and HR | [Driver App administrator guide](admin-guide.md) |
| Admin navigation and all 10 tabs | [Admin feature reference](admin-navigation.md) |
| Driver profiles, route knowledge, logins | [Drivers and logins](drivers-and-logins.md) |
| Monthly planning and route patterns | [Planning and routes](planning-and-routes.md) |
| Leave, availability and replacement calls | [Requests and replacements](requests-and-replacements.md) |
| Hours, payroll, vehicles, dossiers | [Hours, vehicles and dossiers](hours-vehicles-dossiers.md) |
| Settings, privacy, incidents, go-live | [Settings and go-live](settings-and-go-live.md) |
| Screenshot and verification needs | [Screenshot checklist](../SCREENSHOTS.md) |

## Feature areas represented in the backend

| Area | Overview | Current documentation confidence |
| --- | --- | --- |
| Driver profile and access | Employee linkage, profile, reviewed login creation | Backend documented; UI needs verification |
| Availability and leave | Driver requests and management decisions | Backend documented; UI needs verification |
| Monthly plans | Suggested assignments, review, publication, shadow plans | Backend documented; UI needs verification |
| Replacements | Replacement call, response, reminders and escalation | Backend documented; UI needs verification |
| Workdays and hours | Time capture, corrections, disputes, payroll month close | Backend documented; UI needs verification |
| Vehicles | Assignment, vehicle readiness and maintenance | Backend documented; UI needs verification |
| Odometer and damage | Departure photos, reported damage and evidence | Backend documented; UI needs verification |
| Driver dossier | Fines, disputes, manuals and route information sheets | Backend documented; UI needs verification |
| Notifications | In-app messages and optional email; push needs controlled enablement | Backend documented; live delivery needs verification |

## What is not a promised live feature?

- Camera OCR for odometer reading has no configured OCR provider by default.
- Departure GPS capture is off by default.
- Routific API integration and temperature registration are deferred in the source specification.
- Offline uploading of damage and fine photos is not supported as an offline queue.
- Push notification behavior requires an actual mobile-device test before activation.

## Before the guide is released to drivers

1. Confirm that the application is enabled and the required function switches have been approved.
2. Verify the actual phone URLs and screens, and update the guides to match the UI.
3. Test with one non-admin driver account and one administrator account.
4. Add screenshots taken with test data.
5. Obtain operational and privacy approval.

[Documentation home](../README.md)
