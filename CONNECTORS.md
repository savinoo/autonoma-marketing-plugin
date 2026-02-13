# Connectors

This plugin can integrate with the following external tools via MCP (Model Context Protocol). Each connector is optional — the plugin works without any of them, but adding connectors enhances capabilities.

## Available Connectors

| Connector | Purpose | MCP URL |
|-----------|---------|---------|
| **Slack** | Share content drafts, get team feedback, post updates | `https://mcp.slack.com/mcp` |
| **Notion** | Store content calendar, briefs, brand guidelines | `https://mcp.notion.com/mcp` |
| **Canva** | Create visual assets for social posts | `https://mcp.canva.com/mcp` |
| **HubSpot** | CRM integration, lead tracking, email campaigns | `https://mcp.hubspot.com/anthropic` |
| **Amplitude** | Content performance analytics | `https://mcp.amplitude.com/mcp` |

## Setup

Connectors are configured in `.mcp.json`. To add or remove a connector, edit that file. Each connector will prompt for authentication on first use.

## Without Connectors

All core features work without connectors:
- Content generation with quality gates
- Peer review with 6-dimension scoring
- Editorial calendar planning
- SEO research (uses web search)
- Trend detection (uses web search)

Connectors add distribution, analytics, and collaboration capabilities on top of the core pipeline.
