# Dashboardly 1.1.0

Ask about your authorized shop's sales, profit, P&L, daily financial trends and imported advertising performance. The connected reporting workflow reads canonical Dashboardly results; separate offer and CRO workflows model supplied assumptions and draft improvements.

## Included workflows

- **Connection context:** Review the authorized account, shops and connection capabilities.
- **Shop Sales, Profit & Advertising:** Read authorized shop sales, profit and advertising results with reporting context, evidence and data limitations.
- **Offer & Profit Checker:** Compare modeled offer contribution using explicit costs and assumptions.
- **Video to Product Page CRO:** Compare supplied creative and product-page evidence and draft a testable improvement.

## Connect and select a shop

Install and enable the bundle through your Claude host's supported plugin flow. In Claude Code, open `/mcp` and authenticate `plugin:dashboardly:dashboardly`. For a terminal without automatic browser opening, use `claude mcp login plugin:dashboardly:dashboardly --no-browser` in a project where the plugin is enabled, then follow the displayed browser link. The connector is bundled; do not add a duplicate manually configured server. Installation alone does not authorize shop access. Sign in with your Dashboardly account, choose the intended shops and review the access shown before consenting. Never paste credentials into a conversation. Ask which account and shops this connection can use before analysis. An installed skill does not broaden the connection's capabilities.

## Ask a reporting question

Choose an authorized shop and the reporting dates. Ask for a sales/profit summary, a P&L breakdown, a daily trend or imported advertising performance. Financial reports use the returned saved/applied reporting context; caller-supplied timezone, reporting basis and merchant overrides are not supported. Summary requests are limited to 366 inclusive days; daily/P&L-day requests to 90 days, P&L-week requests to 184 days and coarser P&L requests to 366 days. A limit is not permission to silently shorten your requested period.

## Read the result with its limits

Preserve returned currency, dates, effective timezone, applied settings, evidence and source quality. Missing costs, unknown metrics and daily gaps remain unavailable, not zero. A response timestamp is not a source-data watermark; an incomplete or preliminary result does not prove final profit. Daily values follow the shared metricDefinitions order; null means unavailable and a returned zero remains zero. Whole-range totals are canonical, not reconstructed from displayed days. Do not reconstruct missing totals or average returned ratios.

Advertising reads cover at most 90 days of imported campaign facts and use their advertiser reporting calendar and verified currency. Campaign gross spend before credits differs from the financial report's net/cash ad spend; attributed revenue is a subset and must not be added to total shop sales. Campaign summaries do not establish whole-shop billed spend. Pending, stale, missing attribution and mixed/unknown currency remain explicit. This workflow does not trigger imports or fetch live TikTok reports.

Offer contribution is hypothetical and uses explicit supplied costs; it is not realized shop profit. CRO uses supplied evidence, does not fetch arbitrary URLs and does not claim verified conversion lift. The bundle does not expose buyer contacts, addresses, tracking or order-level personal data, or change costs, listings, orders, ads or access. Reports and recommendations are drafts; no sending, saving, publishing, purchases or profit guarantees. Stop when a required capability or source is unavailable.

## Disconnect and support

Disconnect Dashboardly in your assistant and revoke the connection through the available Dashboardly account controls to stop access. An expired or revoked connection uses the host's normal reconnect flow; never copy tokens or broaden access. Setup and troubleshooting: https://help.dashboardly.io/.

## Rights and terms

Copyright 2026 DASHBOARDLY INC. All rights reserved. Use of Dashboardly is governed by https://www.dashboardly.io/terms-of-service and https://www.dashboardly.io/privacy-policy. This notice does not grant an open-source license or permission to redistribute the bundle outside an owner-approved provider distribution.

## Availability

This 1.1.0 bundle is a separate provider-review preparation. It does not replace the existing 1.0.0 submission automatically. A local build does not establish deployed financial parity, client acceptance, owner distribution approval, provider approval, a public listing or installation from a directory.
