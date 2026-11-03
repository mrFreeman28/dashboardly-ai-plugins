---
name: get-started
description: Review a Dashboardly connection when the user asks to connect, choose a shop, identify account access or understand available capabilities.
---

# Get started with Dashboardly

Read [analysis rules](../../references/analysis-rules.md) before using this skill.

1. Call the Dashboardly connector's `get_connection_context` with the current schema. If unavailable or disconnected, explain the connection state and the host's OAuth connection step. Do not claim the endpoint is deployed or approved from the package alone.
2. Show the effective organization label, connection state and returned capability limits. Do not expose grants, client secrets or inaccessible accounts.
3. If the user needs a shop, call `list_shops`. Follow pagination only as needed for selection, within its limits. Name a sole available shop; ask for an explicit choice when multiple shops are plausible. Never imply the first page is the complete universe if a cursor remains.
4. Offer only workflows both bundled in this installed package and available in the live connection. A capability appearing on the server does not install a missing skill, and an installed skill does not grant access.
5. State the chosen shop and next action. If data is not ready, distinguish missing access from source readiness. Do not describe a subscription purchase as the connection recovery step.

Output a short connection summary: account, selected/available shops, supported task, unmet prerequisite, next step. A successful installation is not proof of successful OAuth, current financial data or publication in a directory.
