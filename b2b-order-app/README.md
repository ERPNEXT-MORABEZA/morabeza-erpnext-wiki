# Carnivale B2B Order App

English-language user documentation for the professional customer ordering portal and ERPNext staff administration.

**Application:** [Carnivale B2B portal](https://carnivale.frappe.cloud/b2b)  
**Source repository:** [ERPNEXT-MORABEZA/carnivale-b2b](https://github.com/ERPNEXT-MORABEZA/carnivale-b2b)  
**Reviewed implementation:** `b2b-v5-release-2` branch plus the nine screenshots supplied on 19 November 2026.

> The screenshots show delivery selection, final checkout and staff Links. Those pages exist on the reviewed release branch, **not on the older source repository main branch**. This is a documentation-of-the-shown-release guide, not a claim about current production flags or a guarantee that every source branch is deployed.

## On this page

- [Start here](#start-here)
- [How the B2B portal works](#how-the-b2b-portal-works)
- [Languages, roles and confidentiality](#languages-roles-and-confidentiality)
- [Current guide coverage](#current-guide-coverage)

## Start here

**Open directly:** [B2B Home](https://carnivale.frappe.cloud/b2b) · [Shop the catalog](https://carnivale.frappe.cloud/b2b/catalog) · [Pre-order products](https://carnivale.frappe.cloud/b2b/catalog?is_pre_order=1) · [Cart](https://carnivale.frappe.cloud/b2b/cart) · [Choose delivery](https://carnivale.frappe.cloud/b2b/delivery) · [Order history](https://carnivale.frappe.cloud/b2b/account/orders) · [Favorites and lists](https://carnivale.frappe.cloud/b2b/account/favorites) · [My account](https://carnivale.frappe.cloud/b2b/account) · [Staff Links](https://carnivale.frappe.cloud/b2b/links). The checkout pages require a valid customer session and cart.

| Reader | Guide |
| --- | --- |
| **Customer / buyer** | [Customer user guide](customer-guide.md), from login to repeat ordering |
| **Administrator / sales manager** | [Administrator guide](admin-guide.md), products, customer access, delivery settings, Sales Orders, imports |
| **Staff member creating product shares** | [Shared Links guide](shared-links-guide.md), prices, expiration and revocation |
| **Anyone with a problem** | [Troubleshooting](troubleshooting.md) |
| **Documentation editor** | [Screenshots and capture checklist](SCREENSHOTS.md) |

## How the B2B portal works

1. **Browse:** Customers find products using search, categories, filters, favorites and saved lists.
2. **Prepare:** Customers add products and quantities to the cart, then review per-item comments, unit availability and the indicative ex-VAT total.
3. **Schedule:** Customers select an available delivery date, subject to the configured deadline and delivery rules.
4. **Review:** Customers confirm their items, delivery instructions and selected delivery moment.
5. **Submit:** ERPNext creates a Sales Order (or multiple orders where delivery per product is enabled), for sales-team review.
6. **Follow up:** Customers view statuses, order details and previous purchases under Order History.

The staff-only **Links** feature creates read-only product shares; it does not grant customer checkout access.

## Languages, roles and confidentiality

The portal has NL, FR and EN language options; the screenshots happen to use Dutch. In these guides, exact Dutch control labels appear in **bold** with an English explanation.

Customer accounts are tied to ERPNext **Customer** records. The **B2B Catalog Manager** role is deliberately restricted to selected catalog and price operations, while ERPNext sales administrators handle order review. Global B2B Settings are managed by an authorized System Manager.

This wiki is **public**. Do not upload real customer identities, order references, staff email addresses, private prices or live share tokens. All nine sanitized screenshots have been uploaded in `b2b-order-app/images/` and are embedded in context. ERPNext Desk screenshots for the administrator workflows are still to be captured.

## Current guide coverage

| Area | Source / screenshot basis |
| --- | --- |
| Home, search, categories, pre-order, filters | Screenshot + release branch |
| Cart, quantity, item comments, delivery selection, final review | Screenshot + release branch |
| Order history, repeat order, favorites and order lists | Screenshot + release branch |
| Staff Links page | Screenshot + permission-enforced release branch |
| Catalog Item and Item Price maintenance | ERPNext Desk/permission source; no Desk screenshot supplied |
| B2B Settings, delivery rules and holiday integration | ERPNext DocTypes and source; no Desk screenshot supplied |
| Customer onboarding, Sales Order review and data imports | Source and ERPNext conventions; confirm exact company Desk permissions locally |

[Back to main wiki](../README.md)
