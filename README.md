# Morabeza ERPNext User Guides

English-language help and operating instructions for the ERPNext apps developed for Carnivale and associated operations.

> **Documentation status:** These guides describe functionality found in the source repositories as of **19 November 2026**. A feature in code is not automatically enabled in production. Screen labels in the application may still be in Dutch. Screenshots and deployment-specific checks are being added.

## Choose your application

| Application | Who should read it | Guides |
| --- | --- | --- |
| **Taskboard** | Employees, team leaders, operations administrators | [Taskboard guides](taskboard/README.md) |
| **Driver App** | Drivers, dispatch / operations administrators, HR | [Driver App guides](driver-app/README.md) |

## Quick links

- [Taskboard: employee guide](taskboard/employee-guide.md)
- [Taskboard: administrator guide](taskboard/admin-guide.md)
- [Taskboard: attendance and QR check-in](taskboard/attendance.md)
- [Taskboard: reports](taskboard/reports.md)
- [Driver App: driver guide](driver-app/driver-guide.md)
- [Driver App: administrator guide](driver-app/admin-guide.md)
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
- **[Screenshot needed]**: an image to add later. Each placeholder specifies the required screen, filename and what to show.
- Examples should use fictitious employees, customers, routes and tasks. Never upload private employee data, credentials, personal telephone numbers or access tokens.

## Source and maintenance

These are **user manuals**, not technical installation instructions.

Taskboard functionality is drawn from the `carnivale_operations` backend and the `carnivale_b2b` Taskboard frontend. Driver App information additionally comes from the Drivers App technical documentation and backend modules. The main frontend currently contains the Taskboard employee and admin pages, but no dedicated Driver App pages. Accordingly, Driver App user-facing steps are marked for live verification.

Documentation owner: Morabeza. Please review the guides after each relevant application release, especially when screen labels, permissions or feature switches change.

See [Contributing and documentation checks](CONTRIBUTING.md) for the review process.
