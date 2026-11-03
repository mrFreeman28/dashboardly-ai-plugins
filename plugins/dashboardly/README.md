# Dashboardly 1.0.0

Review your authorized Dashboardly connection, model product offers using costs you supply, and compare supplied creative and product-page evidence. These workflows return read-only results and drafts.

## Included workflows

- **Connection context:** Review the authorized account, shops and connection capabilities.
- **Offer & Profit Checker:** Compare modeled offer contribution using explicit costs and assumptions.
- **Video to Product Page CRO:** Compare supplied creative and product-page evidence and draft a testable improvement.

## Connect

Install and enable the bundle through your Claude host's supported plugin flow. In Claude Code, open `/mcp` and authenticate `plugin:dashboardly:dashboardly`. For a terminal without automatic browser opening, use `claude mcp login plugin:dashboardly:dashboardly --no-browser` in a project where the plugin is enabled, then follow the displayed browser link. The connector is bundled; do not add a duplicate manually configured server. Installation alone does not authorize shop access. Sign in with your Dashboardly account, choose the intended shops and review the access shown before consenting. Never paste passwords or tokens into a conversation. Ask which account and shops the connection can use before analysis. Only the connection's permitted capabilities are available.

## Results and limits

Offer contribution is modeled from explicit inputs; it is not a connected financial report. CRO uses supplied evidence and does not fetch arbitrary URLs or claim verified conversion metrics. Missing costs remain unknown. Preserve the returned currency, assumptions, evidence and limitations. No profit or conversion uplift is guaranteed. The bundle does not send, schedule, save, publish, modify listings or ads, or make purchases. Stop if the required tool or permission is unavailable.

## Disconnect and support

Disconnect Dashboardly in your assistant and revoke the connection through the available Dashboardly account controls to stop access. An expired or revoked connection must use the host's normal reconnect flow; never copy tokens or broaden access. Setup and troubleshooting: https://help.dashboardly.io/.

## Rights and terms

Copyright 2026 DASHBOARDLY INC. All rights reserved. Use of Dashboardly is governed by https://www.dashboardly.io/terms-of-service and https://www.dashboardly.io/privacy-policy. This notice does not grant an open-source license or permission to redistribute the bundle outside an owner-approved provider distribution.

## Availability

This bundle is prepared for provider review. Its version and build do not establish owner distribution approval, provider acceptance, a public listing or a production-data guarantee.
