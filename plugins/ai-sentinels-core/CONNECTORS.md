<!-- from productivity -->
# Connectors

## How tool references work

Plugin files use `~~category` as a placeholder for whatever tool the user connects in that category. For example, `~~project tracker` might mean Asana, Linear, Jira, or any other project tracker with an MCP server.

Plugins are **tool-agnostic** — they describe workflows in terms of categories (chat, project tracker, knowledge base, etc.) rather than specific products. The `.mcp.json` pre-configures specific MCP servers, but any MCP server in that category works.

## Connectors for this plugin

| Category | Placeholder | Included servers | Other options |
|----------|-------------|-----------------|---------------|
| Chat | `~~chat` | Slack | Microsoft Teams, Discord |
| Email | `~~email` | Microsoft 365 | — |
| Calendar | `~~calendar` | Microsoft 365 | — |
| Knowledge base | `~~knowledge base` | Notion | Confluence, Guru, Coda |
| Project tracker | `~~project tracker` | Asana, Linear, Atlassian (Jira/Confluence), monday.com, ClickUp | Shortcut, Basecamp, Wrike |
| Office suite | `~~office suite` | Microsoft 365 | — |


---

<!-- from enterprise-search -->
# Connectors

## How tool references work

Plugin files use `~~category` as a placeholder for whatever tool the user connects in that category. For example, `~~chat` might mean Slack, Microsoft Teams, or any other chat tool with an MCP server.

Plugins are **tool-agnostic** — they describe workflows in terms of categories (chat, email, cloud storage, etc.) rather than specific products. The `.mcp.json` pre-configures specific MCP servers, but any MCP server in that category works.

This plugin uses `~~category` references extensively as source labels in search output (e.g. `~~chat:`, `~~email:`). These are intentional — they represent dynamic category markers that resolve to whatever tool is connected.

## Connectors for this plugin

| Category | Placeholder | Included servers | Other options |
|----------|-------------|-----------------|---------------|
| Chat | `~~chat` | Slack | Microsoft Teams, Discord |
| Email | `~~email` | Microsoft 365 | — |
| Cloud storage | `~~cloud storage` | Microsoft 365 | Dropbox |
| Knowledge base | `~~knowledge base` | Notion, Guru | Confluence, Slite |
| Project tracker | `~~project tracker` | Atlassian (Jira/Confluence), Asana | Linear, monday.com |
| CRM | `~~CRM` | *(not pre-configured)* | Salesforce, HubSpot |
| Office suite | `~~office suite` | Microsoft 365 | Google Workspace |


---

<!-- from pdf-viewer -->
# Connectors

## Local MCP Server

This plugin uses a **local MCP server** instead of a remote connector.
The PDF server runs on your machine via `npx`.

| Category | Server | How it runs |
|----------|--------|-------------|
| PDF viewer & annotator | `@modelcontextprotocol/server-pdf` | Local stdio via `npx` (auto-installed) |

### Requirements
- Node.js >= 18
- Internet access for remote PDFs (arXiv, bioRxiv, etc.)
- No API keys or authentication needed
