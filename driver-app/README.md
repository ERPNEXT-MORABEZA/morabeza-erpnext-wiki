# Driver App

**Geofood Drivers: planning, availability, work hours and fleet management**

The Driver App is designed to connect driver planning and administration with the operational Taskboard.

> **Important availability notice (19 November 2026):** The operations backend includes substantial Driver App functionality and automated tests. However, dedicated Driver App screens described in the technical specification were **not found in the current `carnivale-b2b` main branch**. Furthermore, the backend has feature switches that default to off. These documents explain intended and source-backed behavior, **not a confirmed live user interface**. Do not distribute these as finalized phone instructions until the screens, switches and permissions have been checked in staging or production.

## Choose a guide

| Audience | Guide |
| --- | --- |
| Drivers | [Driver guide: planned workflow and features](driver-guide.md) |
| Administrators, operations planners and HR | [Driver App administrator guide](admin-guide.md) |
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
