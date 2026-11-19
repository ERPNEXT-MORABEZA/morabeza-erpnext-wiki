# Morabeza ERPNext User Guides

English-language help and operating instructions for the ERPNext apps developed for Carnivale and associated operations.

> **Documentation status:** These guides describe functionality found in the source repositories as of **19 November 2026**. A feature in code is not automatically enabled in production. Screen labels in the application may still be in Dutch. Screenshots and deployment-specific checks are being added.

## On this page

Select a section to jump directly to it.

- [Choose your application](#choose-your-application)
- [Open the applications directly](#open-the-applications-directly)
- [Quick links](#quick-links)
  - [Taskboard](#taskboard)
  - [Driver App](#driver-app)
  - [B2B Order App](#b2b-order-app)
  - [CRM Dayboard](#crm-dayboard)
  - [Shared resources](#shared-resources)
- [How to use these guides](#how-to-use-these-guides)
- [Documentation conventions](#documentation-conventions)
- [Source and maintenance](#source-and-maintenance)

## Choose your application

| Application | Who should read it | Guides |
| --- | --- | --- |
| **Taskboard** | Employees, team leaders, operations administrators | [Taskboard guides](taskboard/README.md) |
| **Driver App** | Drivers, dispatch / operations administrators, HR | [Driver App guides](driver-app/README.md) |
| **B2B Order App** | Professional customers, sales and catalog administrators | [B2B ordering guides](b2b-order-app/README.md) |
| **CRM Dayboard / Commercial Control Tower** | Commercial sales staff, managers and ERPNext administrators | [CRM Dayboard guides](CRM-DAYBOARD/README.md) |

## Open the applications directly

These links open the Carnivale instance at **https://carnivale.frappe.cloud**. Sign in first; the available screens depend on your role and enabled features.

| Application | Direct links |
| --- | --- |
| **Taskboard** | [Employee Today](https://carnivale.frappe.cloud/taskboard#vandaag) · [Attendance](https://carnivale.frappe.cloud/taskboard#tijdsregistratie) · [Weekplanning](https://carnivale.frappe.cloud/taskboard/admin#weekplanning) · [Task library](https://carnivale.frappe.cloud/taskboard/admin#templates) |
| **Driver App** | [Chauffeurs planning](https://carnivale.frappe.cloud/taskboard/admin#drivers/plan) · [Driver profiles](https://carnivale.frappe.cloud/taskboard/admin#drivers/drivers) · [Go-live](https://carnivale.frappe.cloud/taskboard/admin#drivers/golive) |
| **B2B Order App** | [Shop](https://carnivale.frappe.cloud/b2b/catalog) · [Cart](https://carnivale.frappe.cloud/b2b/cart) · [Order history](https://carnivale.frappe.cloud/b2b/account/orders) · [Favorites](https://carnivale.frappe.cloud/b2b/account/favorites) |
| **CRM Dayboard** | [Today's Dayboard](https://carnivale.frappe.cloud/app/dayboard) · [WhatsApp Draft Review](https://carnivale.frappe.cloud/app/whatsapp-draft-review) · [Manager Daily Review](https://carnivale.frappe.cloud/app/manager-review) · [Commercial Config](https://carnivale.frappe.cloud/app/commercial-config) |

**Route verification:** The links are derived from the application repository's defined web routes, URL hashes and ERPNext Desk page/report names. An authenticated live-browser walkthrough is still required to confirm permissions and that all release-branch features are deployed.

## Quick links

### Taskboard

- [Employee guide](taskboard/employee-guide.md)
- [Administrator guide](taskboard/admin-guide.md)
- [Attendance and QR check-in](taskboard/attendance.md)
- [Reports](taskboard/reports.md)
- [Detailed weekly planning](taskboard/week-planning.md)
- [Task templates and library](taskboard/task-library.md)
- [Holidays and closures](taskboard/holidays-and-closures.md)

### Driver App

- [Driver guide](driver-app/driver-guide.md)
- [Administrator guide](driver-app/admin-guide.md)
- [All administration tabs](driver-app/admin-navigation.md)
- [Monthly planning and routes](driver-app/planning-and-routes.md)
- [Driver profiles and logins](driver-app/drivers-and-logins.md)

### B2B Order App

- [Customer user guide](b2b-order-app/customer-guide.md)
- [Administrator guide](b2b-order-app/admin-guide.md)
- [Staff shared-product links](b2b-order-app/shared-links-guide.md)
- [Screenshots](b2b-order-app/SCREENSHOTS.md)

### CRM Dayboard

- [Sales user guide](CRM-DAYBOARD/sales-user-guide.md)
- [WhatsApp draft and send workflow](CRM-DAYBOARD/whatsapp-workflow.md)
- [Manager and administrator guide](CRM-DAYBOARD/manager-admin-guide.md)
- [Reports and monitoring](CRM-DAYBOARD/reports.md)
- [Troubleshooting](CRM-DAYBOARD/troubleshooting.md)
- [Screenshot inventory](CRM-DAYBOARD/SCREENSHOTS.md)

### Shared resources

- [AI screenshot capture manifest](SCREENSHOT_CAPTURE_MANIFEST.md)
- [Screenshot capture checklist](SCREENSHOTS.md)

## How to use these guides

1. Choose the application above.
2. Start with your role-specific guide.
3. Follow the steps in order. Dutch button labels are shown in **bold**, with an English explanation.
4. If a button is missing, check your access rights and whether that feature has been enabled by an administrator.
5. Consult the relevant troubleshooting section if something does not work.

## Documentation conventions

- **Verified in source**: the underlying feature and/or screen was found in the code on the stated branch.
- **Needs live verification**: the behavior has source support but was not confirmed by a hands-on production session.
- **Not yet available**: a planned feature or a screen not found in the current frontend source.
- **Screenshot to add**: a short description followed by an inline Markdown image reference in the appropriate guide. Upload the image to the specified path and it will appear there automatically. Until uploaded, GitHub may show a missing-image preview.
- Examples should use fictitious employees, customers, routes and tasks. Never upload private employee data, credentials, personal telephone numbers or access tokens.

## Source and maintenance

These are **user manuals**, not technical installation instructions.

Taskboard functionality is drawn from the `carnivale_operations` backend and the `carnivale_b2b` Taskboard frontend. Driver App information additionally comes from the Drivers App technical documentation and backend modules. The reviewed B2B frontend contains the Taskboard employee and admin pages; the Driver App admin interface is **also visible in screenshots from the deployed site**, and the reviewed `b2b-v5-release-2` source branch contains its Chauffeurs routes and driver page. Deployment and feature switches still require verification. Driver phone steps and disabled feature areas remain marked for verification. Seventeen supplied screenshots have now been uploaded to the matching `taskboard/images/` and `driver-app/images/` directories. Nine sanitized Commercial Control Tower screenshots have also been uploaded to `CRM-DAYBOARD/images/` and placed inline in its guides. Other inline image slots intentionally remain pending until their screenshots are captured.

Documentation owner: Morabeza. Please review the guides after each relevant application release, especially when screen labels, permissions or feature switches change.

See [Contributing and documentation checks](CONTRIBUTING.md) for the review process.
