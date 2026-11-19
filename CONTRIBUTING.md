# Maintaining the ERPNext user guides

All user-facing documentation in this repository is written in **English Markdown**.

## Publishing rules

1. Document only behavior found in the current code or demonstrated in a verified environment.
2. Separate **implemented backend behavior** from **available live UI behavior**.
3. Include the audience, documentation status and last review date when changing a guide.
4. Use the real interface label in **bold**, then explain it in English if it is Dutch.
5. Make steps executable for non-technical readers. Avoid API names and code unless needed for troubleshooting.
6. Keep operational and security-sensitive data out of this public repository.
7. Keep screenshot requirements in [SCREENSHOTS.md](SCREENSHOTS.md) and an inline Markdown image reference directly below the relevant instructions. Upload screenshots to the exact linked paths, so no future guide edit is necessary.
8. Confirm role/permission differences with an ordinary employee or driver account, not only an admin login.
9. Never turn on a production feature, modify employee data or change app settings as part of documentation review.
10. Keep the root README and subsection indexes linked to every new guide.

## Source review

For Taskboard, cross-check:
- Employee and admin web pages in the Carnivale B2B frontend.
- Backend task instance, template, week generation, calendar, attendance and reporting modules in Carnivale Operations.
- Role gates and current production deployment.

For Driver App, cross-check:
- Driver modules and Driver App technical specification in Carnivale Operations.
- Actual live driver and admin frontend screens. The current B2B main branch does not establish those screens.
- Feature-switch states, notifications and device-specific workflows in staging or production.

## Recommended change workflow

1. Update the Markdown guide.
2. Confirm every user step against a running build.
3. Add sanitized screenshots to the exact `images/` path already referenced inside each guide, if available.
4. Check relative Markdown links.
5. Have an operational owner approve the content.
6. Publish with a short changelog in the commit message.

## Guide status labels

- **Source-verified:** Confirmed in checked-in code, not necessarily enabled.
- **Live-verified:** Exercised in an agreed environment with the stated role.
- **Draft:** Based on technical specification or incomplete implementation.
- **Not yet available:** Not supported by the currently reviewed release.

[Documentation home](README.md)
