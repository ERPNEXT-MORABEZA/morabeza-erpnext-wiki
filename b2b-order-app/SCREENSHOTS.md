# B2B Order App screenshot checklist

The customer and administrator guides contain **inline Markdown image references immediately after the instructions they illustrate**. Each image has an explanatory caption.

**Status:** Nine user-supplied screenshots were reviewed on 19 November 2026 and mapped to filenames below. A sanitized image pack is prepared separately. The actual PNGs are not yet committed to the GitHub repository, so GitHub may show a broken-image placeholder until they are uploaded.

## On this page

- [Captures already supplied](#captures-already-supplied)
- [Capture still needed for the ERPNext administrator guide](#capture-still-needed-for-the-erpnext-administrator-guide)
- [Image upload rules](#image-upload-rules)

## Captures already supplied

| Exact destination path | Illustration used in the guide | Page |
| --- | --- | --- |
| `b2b-order-app/images/customer-home.png` | Customer home, quick actions and promotion cards | [Customer guide](customer-guide.md) |
| `b2b-order-app/images/customer-catalog.png` | Full catalog with collections, sorting and product cards | [Customer guide](customer-guide.md) |
| `b2b-order-app/images/customer-preorder-filters.png` | Yellow pre-order filter, active chips, collection selection | [Customer guide](customer-guide.md) |
| `b2b-order-app/images/customer-cart.png` | Basket with item notes, quantities and indicative total | [Customer guide](customer-guide.md) |
| `b2b-order-app/images/customer-delivery.png` | Selecting available delivery dates | [Customer guide](customer-guide.md) |
| `b2b-order-app/images/customer-review-order.png` | Delivery instructions, checkbox and final review | [Customer guide](customer-guide.md) |
| `b2b-order-app/images/customer-order-history.png` | Historical orders, status and Repeat Order | [Customer guide](customer-guide.md) |
| `b2b-order-app/images/customer-favorites-lists.png` | Favorites and saved order lists | [Customer guide](customer-guide.md) |
| `b2b-order-app/images/admin-share-links.png` | Staff list creation, share options and link table | [Shared Links guide](shared-links-guide.md) |

## Capture still needed for the ERPNext administrator guide

Screenshots of these **actual ERPNext Desk forms** were not supplied and are not fabricated:

- Customer record with approved Portal Users and delivery weekdays, using a fictional customer.
- Item record with enabled/catalog group, brand, image, labels and units.
- Item Price entry for B2B EUR and a controlled example of a link price list.
- B2B Settings flags, with clearly marked test values.
- B2B Delivery Rule, territory weekdays, cutoff, exceptions and Holiday List.
- Sales Order draft, review and submission controls, using a fictitious order.
- B2B import dry-run summary, when an approved operator can capture it.

## Image upload rules

1. Review the screenshots and **remove** customer names, staff identities, email addresses, order identifiers, active tokens and confidential price values.
2. Upload the PNGs to the exact folder `b2b-order-app/images/`.
3. Keep the filenames exactly as shown in the table. No Markdown edits are needed once the image files are uploaded.
4. Prefer a focused crop that keeps the relevant button and surrounding context visible.
5. Check the rendered GitHub page afterward and ensure the screenshot appears beside the correct instruction.
6. If an image contains information that cannot be safely obscured, do not publish it in this public wiki. Keep the placeholder instead.

[Documentation home](../README.md) | [B2B Order App contents](README.md)
