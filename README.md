# Dashboardly AI plugins

This repository contains only the Dashboardly plugin distribution files. It does not contain the Dashboardly service source, customer data, credentials, build dependencies, or production keys. The 1.0.0 bundle is prepared for provider review; a repository or successful build does not establish a live directory listing.

## Workflows

Review authorized connection and shop access, model product offers from explicit manual inputs, and compare supplied creative and product-page evidence. These workflows produce read-only results and drafts. They do not fetch arbitrary URLs, report connected financial performance, or modify shop data.

## Claude Code setup

Once this distribution repository is publicly released, use `/plugin marketplace add mrFreeman28/dashboardly-ai-plugins`, then `/plugin install dashboardly@dashboardly`. Open `/mcp` and authenticate the bundled `plugin:dashboardly:dashboardly` through the normal Dashboardly OAuth flow. Review the intended shops and permissions before consenting. Do not add a duplicate manually configured MCP server or paste credentials into chat.

The plugin folder is `plugins/dashboardly`. Its README describes limitations, disconnection, privacy and support. `plugins/dashboardly/LICENSE` contains the DASHBOARDLY INC proprietary distribution notice and links to the existing Dashboardly terms. This is not an open-source grant.
