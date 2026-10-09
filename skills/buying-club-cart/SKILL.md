---
name: buying-club-cart
description: Shop the SuppCo Buying Club. Use when the user asks whether the Buying Club carries a product, wants a Buying Club alternative to something they take, or asks to add, change or remove items in their SuppCo cart or to check out.
---

Cart tools need the user to connect their SuppCo account. If a tool says sign-in is required, ask the user to connect SuppCo from the plugin's Connectors tab.

1. Find products with `suppco_find_buying_club_products`, using the user's words as `query`. To find a Buying Club alternative to a specific product, call `suppco_compare_to_buying_club` with its `product_id_or_slug`.
2. Add an item only when the user asks: call `suppco_add_to_cart` with the product's `product_id_or_slug`, and `quantity` if given. Ask whether they want a one-time purchase or a subscription only if they haven't said.
3. Use `suppco_update_cart_item` to set a new total quantity and `suppco_remove_from_cart` to remove an item.
4. Call `suppco_get_my_cart` to confirm the cart after a change. Report items, quantities, prices and subtotal as returned.
5. Call `suppco_get_checkout_url` only when the user asks to check out, then give them the link.

Never say a purchase was made. The checkout link opens SuppCo's own checkout, where the user reviews the order and pays. Treat the link as private to the user and don't repeat it later in the conversation.
