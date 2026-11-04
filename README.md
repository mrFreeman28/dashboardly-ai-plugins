# Dashboardly AI plugins

This repository contains only Dashboardly plugin distribution files. It does not contain Dashboardly service source, customer data, credentials, build dependencies or production keys. Version 1.1.0 is prepared for provider review. A repository, scan or local build does not establish a live directory listing or installation from a catalogue.

## Workflows

Use your authorized Dashboardly connection to read shop sales, profit, P&L, daily financial trends and imported advertising performance. Financial reports preserve the returned reporting dates, currency, applied settings, evidence and data limitations. Advertising facts use their advertiser reporting calendar; campaign gross spend and attributed revenue must not be confused with financial net/cash ad spend or total shop sales.

The other workflows review connection and shop access, model offers from explicit manual inputs, and compare supplied creative and product-page evidence. Offer calculations are hypothetical and CRO recommendations are drafts. The bundle does not fetch arbitrary URLs, start imports, change shop data, send messages or make purchases. Missing data remains unavailable rather than zero.

## Claude Code setup

Add this existing distribution repository with `/plugin marketplace add mrFreeman28/dashboardly-ai-plugins`, then install with `/plugin install dashboardly@dashboardly`. The available version depends on the selected repository reference and provider publication state. Open `/mcp` and authenticate the bundled `plugin:dashboardly:dashboardly` through the normal Dashboardly OAuth flow. Review the intended shops and read-only permissions before consenting. Installation does not grant shop access. Do not add a duplicate manually configured MCP server or paste credentials into chat.

The plugin folder is `plugins/dashboardly`. Its README documents report limits, disconnection, privacy and support. `plugins/dashboardly/LICENSE` contains the DASHBOARDLY INC proprietary distribution notice and links to the existing Dashboardly terms. This is not an open-source grant.
