# Taskboard troubleshooting

**Audience:** Employees and Taskboard administrators.

## On this page

Select a section to jump directly to it.

- [Access and account problems](#access-and-account-problems)
- [Task action problems](#task-action-problems)
- [Planning and reports](#planning-and-reports)
- [Attendance](#attendance)
- [When to escalate](#when-to-escalate)

## Access and account problems

**The page says I am not authorized.** Sign in with your assigned account. Ask the administrator to check that your user has the correct operational role and is linked to an active Employee record. The employee page and admin page have different access gates.

**I can open the employee board but not the management page.** This is normal unless you have **Operational Team Leader** or **Operational Admin** access. Do not share an administrator account.

**I cannot see the task I expected.** Check the date, department grouping, whether the week has been generated, and **Verberg afgerond**. An unassigned team task may be visible even when you cannot complete it.

## Task action problems

**The checkbox is disabled.** Completion can be restricted because the date is not today, the task is informational, it belongs to another team, or the original task was moved. Administrators and leaders also have server-side restrictions.

**I marked a task Not Done by mistake.** On an eligible task, select **Ongedaan maken** and choose the correct state. If a change is blocked, ask your manager.

**I moved a task to the wrong date.** Employees cannot reverse their own move. Tell the team leader or admin which task, original date and intended new date are involved.

**I cannot add a library task.** Check whether the template is active, the day is a permitted working day, and the target week has been generated.

**I added a task but it is not on today's list.** A future-dated task is displayed on the selected date; a past-dated open task may show as carried over. Use date navigation to verify.

**A task's preparation did not move with it.** Linked preparation and production tasks are not automatically rescheduled as a pair. Review the related task separately.

## Planning and reports

**No tasks were generated for an expected day.** Check active templates, recurrence rules, manual calendar closures and the **Niet automatisch ingepland** list. Flexible recurring tasks require placement by a planner.

**I cannot edit a validated week.** Open the management page and use **Heropenen**, if authorized. Review consequences before changing an already communicated plan.

**The percentage looks too low.** Confirm that future dates are excluded from the desired report period. Open tasks on future dates count in the selected period. Informational, skipped and moved originals are excluded.

**I cannot filter reports by employee.** Only **Operational Admin** can use person-level filtering and metrics.

**Reports are unavailable on this server.** Frontend and backend versions may be out of sync. Contact the technical administrator.

## Attendance

**The QR scanner cannot start.** Check browser camera permission, network access and whether a photo fallback is offered.

**The QR code is rejected.** Use the current code displayed at the workplace entrance. A reissued QR version invalidates previous printed copies.

**The admin does not see a downloadable QR.** Confirm Operational Admin access and that check-in is enabled.

## When to escalate

Send the administrator a short report with the screen, approximate time, task title, expected behavior and actual error message. Include a screenshot with names and sensitive information obscured. Never include your password, session cookies, live QR code or tokens.

[Taskboard contents](README.md) | [Employee guide](employee-guide.md) | [Administrator guide](admin-guide.md)
