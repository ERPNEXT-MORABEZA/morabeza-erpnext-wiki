# CRM Dayboard: Troubleshooting

**Audience:** Sales users, managers and support staff.  
Use the Dayboard's own status and error messages as the first source of truth.

## On this page

- [Dayboard generation and visibility](#dayboard-generation-and-visibility)
- [Contact and WhatsApp errors](#contact-and-whatsapp-errors)
- [Calls, email and outcomes](#calls-email-and-outcomes)
- [Report and configuration confusion](#report-and-configuration-confusion)
- [Reporting a bug safely](#reporting-a-bug-safely)

## Dayboard generation and visibility

**No Dayboard appears for today.** Check the date, **Active Sales / Prospect Onboarding** board type and generation status. For ordinary cases, an authorized user can use **Generate Today → Preview / Create Missing**. Stronger modes require a manager.

**Items seem missing.** The Dayboard initially hides some statuses. Check **Assigned To**, **Status**, **Priority**, **Pipeline**, and any active chips. Select **Show all** when the page reports hidden open items.

**There is no owner.** An item may be assigned to the configured Fallback Owner, so its technical `assigned_to` is not empty. Use **No owner / Fallback** and the Manager Daily Review queue.

## Contact and WhatsApp errors

**WhatsApp Draft cannot be created.** Verify the intended contact's phone number, general WhatsApp consent **Yes**, pipeline permission and the customer's do-not-contact/closure rules. Never bypass these checks.

**Approve & Copy succeeded but nothing was sent.** That is expected. It copies text only. Send through an approved external WhatsApp channel and select **Mark Sent** after actual sending.

**The phone number changed after draft creation.** Use the preflight mismatch warning to resolve the correct recipient. Do not select **Send Anyway** unless the actual external send and recipient are consistent and authorized.

**Skip did not remove a draft.** This matches the current implementation: Skip records a reason and keeps the record in Draft, leaving the Dayboard status alone. Handle the work item separately.

**An edited WhatsApp text was not saved.** The reviewed Draft Review UI's **Edit** button focuses the textarea, and **Approve & Copy** copies it; neither saves that manual edit to the stored Draft. Confirm exact audit requirements with a manager.

## Calls, email and outcomes

**No phone or email appears.** Correct the customer Contact in ERPNext. Do not fabricate an address or phone number to close the work.

**A contact was logged but no follow-up was created.** Check the selected outcome, its follow-up policy, and whether duplicate warning protection was triggered.

**A duplicate warning appears.** Open the existing contact/follow-up first. Continuing is allowed only with a legitimate override reason; **Other** requires a note.

**A Done/Cancelled item cannot be reopened by staff.** These are terminal states in the normal flow. A manager should review the audit trail and approved correction path.

## Report and configuration confusion

**Pipeline Health does not match today's call count.** It counts membership statuses, not today's eligible contacts. Check cadence, suppressed customers and pipeline rules.

**Order Verification says Not integrated.** A commercial outcome is not tied to a confirmed ERPNext Sales Order, even when it says **Besteld**.

**Changing generation time in settings did nothing.** The settings value is informational. The scheduled job uses the fixed **04:00** entry in the ERPNext site's timezone.

**Permissions missing.** Sales users can operate the Dayboard; manager actions need **Commercial Manager**, **Commercial Admin** or a native system role. Have an authorized administrator check the role rather than sharing privileged credentials.

## Reporting a bug safely

Share the page, role, selected date/board type, button used, non-sensitive error text and expected result. Do **not** post customer names, contact details, WhatsApp drafts, real telephone/email data or access tokens in a public issue.

[CRM Dayboard contents](README.md) | [Sales User Guide](sales-user-guide.md) | [Manager Guide](manager-admin-guide.md)
