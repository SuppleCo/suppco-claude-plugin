---
name: supplement-research
description: Look up what published research says about a supplement or nutrient with SuppCo. Use when the user asks what a supplement does, what studies say about it, typical intake ranges or upper limits for a nutrient, or for a supplement protocol for a goal such as sleep, energy or focus.
---

Use the SuppCo connector's research tools. None of them need the user to sign in.

1. For "what does research say about X" or "does X help with Y", call `suppco_search_effects` with `supplement_name` and, if the user named one, `health_condition` for the wellness area.
2. For what a nutrient is, its forms, typical intake ranges and upper limits, call `suppco_get_nutrient_info` with `nutrient_name`.
3. For a routine aimed at a goal, call `suppco_search_protocols` with the goal as `query`. If the user is signed in and asks about protocols they already follow, call `suppco_get_my_protocols`.

Report findings with the evidence grade SuppCo returns, and say when evidence is limited or mixed. Present intake ranges as published reference values, not as a recommendation for this user.

Only repeat what SuppCo returns. Do not diagnose, do not say a supplement treats, cures or prevents a disease, and do not compare supplements with prescription medications. If the user mentions a medical condition, pregnancy or prescription medication, suggest they talk to their clinician.
