# B2B Order App troubleshooting

**Audience:** Customers, customer service and ERPNext administrators.  
**Use the exact message shown on the page when contacting support.**

## On this page

- [Login and customer account](#login-and-customer-account)
- [Searching, products and prices](#searching-products-and-prices)
- [Cart and delivery](#cart-and-delivery)
- [Checkout and order history](#checkout-and-order-history)
- [Favorites, lists and Links](#favorites-lists-and-links)
- [How to report a problem](#how-to-report-a-problem)

## Login and customer account

**Relevant screens:** [Sign in](https://carnivale.frappe.cloud/b2b/login) · [My account](https://carnivale.frappe.cloud/b2b/account) · [Help](https://carnivale.frappe.cloud/b2b/account/help).

**I can sign in but cannot place an order.** Your login may lack a linked ERPNext Customer record. Ask Carnivale to review the Customer portal user relationship, not to grant you an internal Desk role.

**The wrong customer shows in the yellow header.** Stop ordering. Sign out and ask Carnivale to verify your login-to-Customer linkage. Never place an order against another company's account.

## Searching, products and prices

**Open directly:** [Catalog and filters](https://carnivale.frappe.cloud/b2b/catalog) · [Pre-order selection](https://carnivale.frappe.cloud/b2b/catalog?is_pre_order=1).

**A product is missing.** Remove all filters, search by exact Item Code, then confirm it is part of the B2B assortment. If it is still missing, ask the catalog manager to review the Item's enabled state and Item Group.

**Price on request prevents checkout.** Such items are not orderable online in the normal flow. Remove them and request commercial confirmation from Carnivale.

**A price has changed since my previous purchase.** The portal uses currently valid pricing and availability. An old Sales Order is a record of a previous transaction, not a current price quotation.

## Cart and delivery

**Relevant screens:** [Cart](https://carnivale.frappe.cloud/b2b/cart) · [Delivery moment](https://carnivale.frappe.cloud/b2b/delivery).

**The cart changed after I added products.** Item units, prices and eligibility may have changed. Review any **Apply changes** notice, correct the basket, and retry.

**No delivery date is available.** Check whether you have a fixed delivery weekday and whether a product or holiday rule blocks the next 14-day window. Contact Carnivale if no date is feasible.

**My pre-order does not have a definite deadline.** The portal can display **to be confirmed** when rules or deadlines are not enforced/configured. Ask the sales team before relying on a provisional date.

**One checkout seems to produce several orders.** With per-product delivery enabled, the system can group different delivery dates into multiple Sales Orders. Compare the order references and delivery dates before reporting duplication.

## Checkout and order history

**Relevant screens:** [Checkout review](https://carnivale.frappe.cloud/b2b/checkout) · [Order history](https://carnivale.frappe.cloud/b2b/account/orders).

**Place order is greyed out.** Tick the final review checkbox, confirm a valid delivery moment, and resolve any removed/changed cart lines first.

**I clicked Place Order but do not see a confirmation.** Do not repeatedly place a new order. Refresh Order History and ask Carnivale to check the Sales Order and B2B Order Request records.

**Order status is Under review.** The created Sales Order is still a draft awaiting sales review, not a confirmed shipment or payment.

**Repeat Order skipped products.** The catalog rechecks current prices, allowed units and availability. Inspect the preview and cart and reselect any necessary replacements.

## Favorites, lists and Links

**Relevant screens:** [Customer favorites](https://carnivale.frappe.cloud/b2b/account/favorites) · [Saved order lists](https://carnivale.frappe.cloud/b2b/account/favorites#b2b-order-lists) · [Staff-only Links](https://carnivale.frappe.cloud/b2b/links).

**I cannot find Links.** It is a staff-only feature for B2B Catalog Manager or System Manager, not for ordinary customers. Customers should use Favorites or Order lists.

**A shared link no longer works.** It may have expired or been revoked. Ask the sender for a new link. The application intentionally does not disclose the precise reason.

**I lost a generated share link.** The URL is intentionally shown only once. Authorized staff must generate a new one.

## How to report a problem

Provide the page, approximate date/time, the action attempted and any non-sensitive error message. If relevant, give the order reference to Carnivale support privately, not in a public GitHub issue. Never send passwords, share tokens, customer price lists or personally identifiable screenshots.

[Customer guide](customer-guide.md) | [Administrator guide](admin-guide.md) | [B2B Order App contents](README.md)
