---
name: offer-profit-checker
description: Compare one to five proposed product offers when the user needs modeled contribution, cost gaps or a supported target cash-ad budget before a promotion.
---

# Offer & Profit Checker

Read [analysis rules](../../references/analysis-rules.md). This skill models supplied assumptions; it does not report realized shop Net Profit or start a promotion.

1. Establish the current connection with `get_connection_context`. This version supports `manual` scenarios with an explicit currency and supplied assumptions. Connected-product prefilling is unavailable. Do not fetch hidden shop economics, guess product identity or treat a client-supplied provenance label as a server-verified fact.
2. Collect 1–5 scenarios using the current `evaluate_offer` schema: quantity, unit price, seller discount, platform-funded product discount and each required cost. Seller amount-discount is the total for the modeled order. Product cost is per unit; shipping, platform fees, standard affiliate commission, Shop Ads commission, cash ads, samples and other costs are scenario totals. Keep standard and Shop Ads commissions distinct; do not double-count components.
3. Each cost must explicitly be included with an amount, unknown, or excluded where the schema allows it. Core costs cannot be excluded. An explicit confirmed zero is an assumption; an omitted cost is unknown. Optional excluded samples/other costs mean limited contribution. Do not invent market fee rates, tax treatment, cost bases, refunds or shipping subsidies. Request only missing inputs that change the answer.
4. Call `evaluate_offer` for deterministic results. Use server-returned normalized values, evidence, assumptions, exclusions, modeled contribution and margin. Preserve user overrides as assumptions; they do not update stored costs or prices. If total/margin is unavailable, show the known breakdown and the missing inputs rather than calculating a replacement.
5. Compare only scenarios the server marks comparable. Do not rank an incomplete scenario as more profitable. Do not rescale fixed expenses automatically for different quantities or mix currencies.
6. If the user requests a target margin, pass the supported target field. Echo a cash-ad cap only when returned as available, with all required fixed-input assumptions. A target-infeasible result is not a zero budget that achieves the target. A cap is a model boundary, not a spending recommendation or a ROAS promise. Maximum discount or commission searches are unavailable in this version.

Output: short modeled conclusion; table of scenarios, revenue basis, included/excluded costs, contribution and margin; supported target budget if requested; assumptions, evidence and missing inputs; one next verification step. Label every conclusion as modeled or limited contribution, never guaranteed profit.
