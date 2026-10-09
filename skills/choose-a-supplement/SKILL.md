---
name: choose-a-supplement
description: Pick or compare supplement products with SuppCo. Use when the user asks which supplement, product or brand to buy, wants a high-quality option for a goal such as sleep or energy, asks how trustworthy a product or brand is, or wants to compare a product with alternatives.
---

Use the SuppCo connector's catalog tools. None of them need the user to sign in.

1. Find candidates with `suppco_find_products`. Put the user's words in `query` and pass any filters they gave: `form`, `brand`, `max_price`, `certifications`, `include_ingredients` or `exclude_ingredients`. Keep `limit` small (5 is usually enough).
2. When the user names a brand, call `suppco_get_brand_trust_score` with `brand_name`. When they name products, call `suppco_get_product_trust_score` or `suppco_get_product_info` with those products.
3. To compare one product with others in its category, call `suppco_compare_product_to_alternatives` with its `product_id_or_slug`, plus `priority` if the user cares most about price, quality or another factor.
4. If the user is signed in and asks what fits with what they already take, call `suppco_get_my_stack` first and avoid suggesting duplicates.

Reply with a short list: product name, brand, form, price if returned, and TrustScore. Explain a TrustScore with the factors SuppCo returns, such as testing, certifications and manufacturing. Link to the SuppCo product page when a URL is returned.

Only repeat what SuppCo's tools return. Do not say a product treats, cures or prevents any disease, and do not give personal dosing advice. If the user mentions a medical condition, pregnancy or prescription medication, suggest they check with their clinician before starting a supplement.
