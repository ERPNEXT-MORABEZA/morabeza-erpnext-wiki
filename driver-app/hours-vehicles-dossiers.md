# Driver hours, vehicles, dossiers and notifications

**Audience:** Operations administrators, with limited HR/Payroll access where enabled.  
**Verification:** The admin tab names appear in the uploaded screenshots, and the backend modules support the workflows below. Detailed tab panels were **not** captured. As seen under **Instellingen**, hours, vehicles and dossiers were marked **Uit** in the 19 November 2026 screenshot. Do not present these features as currently available to all users.

## On this page

- [Uren: time registration and corrections](#uren-time-registration-and-corrections)
- [Payroll close and export](#payroll-close-and-export)
- [Voertuigen: vehicle management](#voertuigen-vehicle-management)
- [Odometer and departure evidence](#odometer-and-departure-evidence)
- [Dossiers: damage, fines and manuals](#dossiers-damage-fines-and-manuals)
- [Meldingen en audit: notifications and audit trail](#meldingen-en-audit-notifications-and-audit-trail)
- [Evidence needed before publication](#evidence-needed-before-publication)

## Uren: time registration and corrections

**Open directly if enabled:** [Chauffeurs → Uren](https://carnivale.frappe.cloud/taskboard/admin#drivers/hours).

When enabled by the approved workday switch, the backend records driver start and end events, detects forgotten end registrations, and supports corrections and disputes. The registration and payroll logic is not split by **Vast** versus **Flexi** contract type.

Administrators should review incorrect or missing registrations, approved leave overlaps, requests for correction and the audit trail before month close.

> **Screenshot still needed:** `driver-app/images/admin-hours.png`, with fictional start/end and correction/approval states.
>
> ![Driver hours and correction queue pending capture](images/admin-hours.png)

## Payroll close and export

**Open directly if enabled:** [Uren, payroll and corrections](https://carnivale.frappe.cloud/taskboard/admin#drivers/hours), subject to Payroll/HR permissions.

The backend supports a closed monthly payroll period and an **SD Worx** export with versioning. A later correction after a month close creates a new version rather than silently changing an already downloaded file.

Mapping must be checked and confirmed before use. The HR/Payroll role can export only if the appropriate permission switch is enabled. The organization must still validate payroll calculations and personnel data before submission.

> **Screenshot still needed:** `driver-app/images/admin-payroll.png`, showing only anonymized mapping, close state and export version.
>
> ![Payroll month close pending capture](images/admin-payroll.png)

## Voertuigen: vehicle management

**Open directly if enabled:** [Chauffeurs → Voertuigen](https://carnivale.frappe.cloud/taskboard/admin#drivers/vehicles).

Vehicle management includes fleet profiles, route and driver preferences, assignments, temporary unavailability and service/maintenance warnings.

A vehicle assignment requires an approved baseline where the applicable readiness rule is active. An unavailable vehicle may lead to a proposed alternative, subject to manager review.

> **Screenshot still needed:** `driver-app/images/admin-vehicles.png`, showing a fictitious fleet table, readiness, alerts and assignments.
>
> ![Fleet management pending capture](images/admin-vehicles.png)

## Odometer and departure evidence

The backend supports departure odometer readings and associated photos. The default OCR provider is **none**, so a driver should enter and verify the actual reading. Default departure GPS capture is not enabled.

The driver phone screen and live upload behavior must be tested before adding step-by-step camera instructions.

## Dossiers: damage, fines and manuals

**Open directly if enabled:** [Chauffeurs → Dossiers](https://carnivale.frappe.cloud/taskboard/admin#drivers/dossiers).

Dossiers cover:

- Damage reports, photos, statuses and restricted responsibility decisions.
- Fines and fine disputes. A driver sees only **confirmed** fines permitted by their role.
- Logistics manual versions, publication and required read acknowledgments.
- Route information sheets attached to a driver's own assignments.

Do not include real license plates, fines or medical/personnel details in screenshots.

> **Screenshot still needed:** `driver-app/images/admin-dossiers.png`, with sample damage/fine/manual sections only.
>
> ![Driver dossiers pending capture](images/admin-dossiers.png)

## Meldingen en audit: notifications and audit trail

**Open directly:** [Chauffeurs → Meldingen en audit](https://carnivale.frappe.cloud/taskboard/admin#drivers/audit).

The backend includes in-app and email notification channels, optional push behavior, and an audit log of important administrative actions. An unread or failed notification must not be interpreted as proof a driver has accepted or seen a schedule.

Push requires an enabled switch and real-device testing. Audit details are restricted; avoid sharing logs or private staff data in this public documentation.

## Evidence needed before publication

- Capture the detailed **Uren**, **Voertuigen**, **Dossiers** and **Meldingen en audit** tabs.
- Confirm which modules are enabled in the environment intended for use.
- Test a non-admin driver session for isolation to the driver's own data.
- Check a versioned payroll correction and one vehicle/dossier example in staging.
- Update the screenshots and then promote these sections from backend-verified drafts to live-verified instructions.

[Driver App contents](README.md) | [Settings and go-live](settings-and-go-live.md)
