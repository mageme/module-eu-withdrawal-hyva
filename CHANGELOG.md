## 1.0.9

+ New: The return summary now lists the items you selected, fully translated and matching the standard theme, and a bundle returned as one item shows what is inside it with the quantity to send back for each part — on the selection step, on the review step and in your order view.
+ New: The confirmation page now repeats what was requested — the items, their quantities and the total refund — matching the standard theme.
+ New: A part of a bundle that is a download or a service is marked "Nothing to send back" instead of a quantity.
- Fix: When no line of an order can be withdrawn any more, the return summary explains why instead of showing an empty panel.
* Other: The "Select items to return" heading now reads "Items to return" when there is nothing to pick.
* Other: A bundle that can only be returned whole no longer shows a price beside each of its parts on the selection step, so nothing suggests a single part could be sent back on its own for that amount.
* Other: This version uses new Tailwind classes — rebuild your theme's Tailwind bundle after updating, or the return summary will render unstyled.

## 1.0.8

- Fix: A bundle returned as a single unit now asks whether the seal is intact once for the whole bundle, instead of repeating the question for every sealed part.
- Fix: When the only item on an order is set aside because its seal was opened, the refund summary no longer shows the "your refund will be issued" note while there is nothing to refund.
* Other: In whole-order mode, the "this request covers all returnable items / contact us for a partial return" note now sits in a tidy bordered info box instead of loose text under the last item.

## 1.0.7

+ New: Bundle contents are now grouped under the bundle they belong to, each part showing the amount it contributed to the price, instead of appearing as a flat list of unrelated products.
- Fix: On orders paid with a discount code, the withdrawal form now shows the amount actually paid for each line instead of the price before the discount.
- Fix: On stores that display prices without tax, the withdrawal form quoted each line without VAT while the confirmation page and the receipt showed the amount including VAT; every screen now shows the amount that will actually be refunded.
- Fix: When a discount code also reduced the delivery charge, the refund summary quoted the undiscounted delivery and hid the difference in an "Order Adjustment" line.
- Fix: The refund summary no longer offers delivery that a credit memo had already refunded.
- Fix: A sealed hygiene or media item bought as a variant of a configurable product now shows the seal question on the withdrawal form, the same as a standalone sealed item.
- Fix: A bundle that contains a sealed hygiene or media component now asks whether that component's seal is intact; declaring it opened excludes the whole bundle from the return, matching the Luma storefront.
* Other: The refund preview reconstructs each line the way the server does, so it can no longer drift from the recorded refund on large quantities.
* Other: The VAT line in the refund summary now always breaks the tax out of the amounts above it instead of being added on top of them.
* Other: The item table's quantity columns are now labelled simply "Purchased" and "Returned".

## 1.0.6

+ New: The refund summary now shows VAT in line with your store's tax-display setting - gross prices with an "Of which VAT" note, or net prices with an added VAT line.
+ New: The withdrawal form now follows your Hyva theme's accent colour instead of a fixed blue, so it matches your storefront palette.
- Fix: Orders blocked from withdrawal no longer show their items as returnable on the Hyva storefront.

## 1.0.5

- Fix: The withdrawal page no longer errors when running on an older base module version.

## 1.0.4

* Other: Internal cleanup of the withdrawal form's inline-script handling.

## 1.0.3

+ New: Full order selection mode support in the withdrawal form
- Fix: final confirmation button now renders the legally required "Confirm withdrawal" label in the customer's language instead of "Submit return request"
+ New: Extension points for the Pro photo evidence step on the withdrawal form
* Other: Mobile layout polish on the withdrawal form (full-bleed cards, tighter spacing)

## 1.0.2

- Fix: The withdrawal refund summary now reflects order-level discounts and other custom totals.

## 1.0.1

+ New: "Show more" in the order picker — load more eligible orders on demand.

## 1.0.0

+ New: First public release. Hyva theme compatibility for the EU Withdrawal customer flow — the lookup form, the four-step withdrawal flow, the customer-account "Withdrawal requests" section, and the order-view withdraw button, all rebuilt with Tailwind and Alpine.js.
