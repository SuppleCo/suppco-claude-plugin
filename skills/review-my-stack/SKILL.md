---
name: review-my-stack
description: Review or update the user's SuppCo supplement stack. Use when the user asks what is in their stack, how good their stack is, how to improve it, what their nutrient totals or nutrient plan are, when they take each product, or asks to add, remove, swap or reschedule a product.
---

These tools need the user to connect their SuppCo account. If a tool says sign-in is required, ask the user to connect SuppCo from the plugin's Connectors tab.

Reading the stack:
1. Call `suppco_get_my_stack` for the products and doses the user tracks.
2. For "how good is my stack" or "how can I improve it", call `suppco_get_stack_score`. Report the overall StackScore and its category ratings, then the recommendations SuppCo returns.
3. For nutrient questions, call `suppco_get_my_nutrient_totals` (what the current products provide, including amounts over upper limits) or `suppco_get_my_nutrient_plan` (SuppCo's personalized targets).
4. For timing, call `suppco_get_my_schedule`.

Changing the stack (only when the user asks):
- Add a product with `suppco_add_to_stack`, remove one with `suppco_remove_from_stack`, or replace one with `suppco_swap_products`. Use product IDs from SuppCo results; search with `suppco_find_products` first if you only have a name.
- Change when or how a product is taken with `suppco_update_product_schedule`.
- Before calling a tool that changes the stack, say which product and what change, and make it only once the user agrees.
- Call `suppco_refresh_stack_score` only when the user asks for an updated score. It recalculates in a few minutes.
- Save a preference with `suppco_save_memory` only when the user asks SuppCo to remember it.

Summarize results in plain language; don't paste raw tool output. Only repeat what SuppCo returns, make no disease or treatment claims, and suggest the user check with a clinician before changing supplements if they mention a medical condition or prescription medication.
