# Driver App administration: navigation and feature reference

**Audience:** Geofood operational administrators and managers.  
**Verification:** The supplied 19 November 2026 screenshots establish that the **Chauffeurs** management page and its tab navigation exist on the deployed site. Only some tab contents were captured. Backend capabilities are cross-checked with the Carnivale Operations source; noncaptured tabs must still be walked through live.

## On this page

- [Open the Chauffeurs module](#open-the-chauffeurs-module)
- [What each tab is for](#what-each-tab-is-for)
- [How to recognize disabled modules](#how-to-recognize-disabled-modules)
- [What remains to be verified](#what-remains-to-be-verified)

## Open the Chauffeurs module

**Direct links:** [Weekplanning](https://carnivale.frappe.cloud/taskboard/admin#drivers/plan) · [Aanvragen](https://carnivale.frappe.cloud/taskboard/admin#drivers/requests) · [Vervangingen](https://carnivale.frappe.cloud/taskboard/admin#drivers/replacements) · [Chauffeurs en logins](https://carnivale.frappe.cloud/taskboard/admin#drivers/drivers) · [Uren](https://carnivale.frappe.cloud/taskboard/admin#drivers/hours) · [Voertuigen](https://carnivale.frappe.cloud/taskboard/admin#drivers/vehicles) · [Dossiers](https://carnivale.frappe.cloud/taskboard/admin#drivers/dossiers) · [Meldingen en audit](https://carnivale.frappe.cloud/taskboard/admin#drivers/audit) · [Go-live](https://carnivale.frappe.cloud/taskboard/admin#drivers/golive) · [Instellingen](https://carnivale.frappe.cloud/taskboard/admin#drivers/settings). These hash routes are defined by the reviewed B2B release branch; role permissions and feature switches still apply.

Sign in to the operational administration area and choose **Chauffeurs** from the left-hand navigation. The screenshot shows the following tabs across the top:

**Weekplanning**, **Aanvragen**, **Vervangingen**, **Chauffeurs en logins**, **Uren**, **Voertuigen**, **Dossiers**, **Meldingen en audit**, **Go-live**, **Instellingen**.

The tab names are in Dutch; this wiki explains them in English while preserving exact on-screen labels.

## What each tab is for

| Tab | English meaning | Verified visual content / source-backed capability |
| --- | --- | --- |
| **Weekplanning** | Driver planning | Screenshot: month navigation, generation, shadow month, coverage, route patterns and holidays. [Planning guide](planning-and-routes.md) |
| **Aanvragen** | Requests | Backend: leave and availability-change requests, admin decisions. Screen content not captured. [Requests and replacements](requests-and-replacements.md) |
| **Vervangingen** | Replacements | Backend: replacement calls, accept/decline, reminders/escalation. Screen content not captured. [Requests and replacements](requests-and-replacements.md) |
| **Chauffeurs en logins** | Driver administration | Screenshots: driver list, availability, route knowledge and login-management table. [Drivers and logins](drivers-and-logins.md) |
| **Uren** | Hours | Backend: workday registrations, adjustments, month close/payroll; screenshot tab only. [Hours, vehicles and dossiers](hours-vehicles-dossiers.md) |
| **Voertuigen** | Vehicles | Backend: vehicle availability, assignments, baseline, odometer, maintenance; screenshot tab only. [Hours, vehicles and dossiers](hours-vehicles-dossiers.md) |
| **Dossiers** | Driver dossiers | Backend: damage, fines, logistics manual, route sheets; screenshot tab only. [Hours, vehicles and dossiers](hours-vehicles-dossiers.md) |
| **Meldingen en audit** | Notifications/audit | Backend: in-app/email notices, delivery status and admin audit; screenshot tab only. [Settings and go-live](settings-and-go-live.md) |
| **Go-live** | Readiness | A readiness count is shown in the tab. Detailed checklist is source-backed; screen itself not captured. [Settings and go-live](settings-and-go-live.md) |
| **Instellingen** | Settings | Screenshot: timezone, deadlines, retention proposals, feature switches, incidents and emergency export. [Settings and go-live](settings-and-go-live.md) |

## How to recognize disabled modules

A visible tab is **not proof that the associated workflow is enabled**. In the supplied settings capture, several components are marked **Uit** (off), while offline read-only copy is marked **Aan** (on). Use the real status on your deployed instance when deciding which processes staff should use.

The presence of the module in a screenshot supersedes the earlier wiki wording that no driver administration interface existed. The **mobile driver interface** remains unverified from the screenshots provided.

## What remains to be verified

Screenshots are still needed for the actual content of **Aanvragen**, **Vervangingen**, **Uren**, **Voertuigen**, **Dossiers**, **Meldingen en audit**, **Go-live** and the **driver phone interface**. The wiki intentionally does not invent their buttons.

[Driver App contents](README.md) | [Driver administrator guide](admin-guide.md)
