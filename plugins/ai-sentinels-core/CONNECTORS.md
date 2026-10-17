<!-- from productivity -->
# Connectors

## How tool references work

Plugin files use `~~category` as a placeholder for whatever tool the user connects in that category. For example, `~~project tracker` might mean Asana, Linear, Jira, or any other project tracker with an MCP server.

Plugins are **tool-agnostic** — they describe workflows in terms of categories (chat, project tracker, knowledge base, etc.) rather than specific products. The `.mcp.json` pre-configures specific MCP servers, but any MCP server in that category works.

## Connectors for this plugin

| Category | Placeholder | Included servers | Other options |
|----------|-------------|-----------------|---------------|
| Chat | `~~chat` | Slack | Microsoft Teams, Discord |
| Email | `~~email` | Gmail | Microsoft 365 |
| Calendar | `~~calendar` | Google Calendar | Microsoft 365 |
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
# Optional: interactive PDF viewer

The `/open`, `/annotate`, `/fill-form` and `/sign` commands and the **view-pdf** skill need a local PDF server. **It is not switched on by default**, because it runs on your own computer through Node.js, and the AI Sentinels workshop does not ask anyone to install Node.js.

Without it, Claude can still read, summarise and extract text and tables from PDFs you upload or keep in your working folder. Only the live viewer (highlighting, stamping, filling form fields and placing signatures on the page) is unavailable.

| Category | Server | How it runs |
|----------|--------|-------------|
| PDF viewer & annotator | `@modelcontextprotocol/server-pdf` | Local stdio via `npx` (optional, not pre-configured) |

### Turning it on (optional)

Requirements: Node.js 18 or later, and your IT team's approval to run local tools. Then add this server in Claude's connector settings (or to your own MCP configuration):

```json
"pdf": {
  "command": "npx",
  "args": ["-y", "@modelcontextprotocol/server-pdf", "--stdio"]
}
```

No API keys or sign-in are needed. Internet access is only used for remote PDFs (arXiv, bioRxiv and similar).
