<!-- from finance -->
# Connectors

## How tool references work

Plugin files use `~~category` as a placeholder for whatever tool the user connects in that category. For example, `~~data warehouse` might mean Snowflake, BigQuery, or any other warehouse with an MCP server.

Plugins are **tool-agnostic** — they describe workflows in terms of categories (data warehouse, chat, project tracker, etc.) rather than specific products. The `.mcp.json` pre-configures specific MCP servers, but any MCP server in that category works.

## Connectors for this plugin

| Category | Placeholder | Included servers | Other options |
|----------|-------------|-----------------|---------------|
| Data warehouse | `~~data warehouse` | BigQuery | Snowflake\*, Databricks\*, Redshift, PostgreSQL |
| Email | `~~email` | Gmail, Microsoft 365 | — |
| Office suite | `~~office suite` | Microsoft 365 | — |
| Chat | `~~chat` | Slack | Microsoft Teams |
| ERP / Accounting | `~~erp` | — (no supported MCP servers yet) | NetSuite, SAP, QuickBooks, Xero |
| Analytics / BI | `~~analytics` | — (no supported MCP servers yet) | Tableau, Looker, Power BI |

\* Not pre-configured. Snowflake and Databricks MCP servers live at an address unique to your organisation's account (for example `https://<account>.snowflakecomputing.com/...` or `https://<workspace>.cloud.databricks.com/api/2.0/mcp/...`), so they cannot ship in this pack. Ask your data team for the address and add it as a custom connector in Claude.


---

<!-- from data -->
# Connectors

## How tool references work

Plugin files use `~~category` as a placeholder for whatever tool the user connects in that category. For example, `~~data warehouse` might mean Snowflake, BigQuery, or any other warehouse with an MCP server.

Plugins are **tool-agnostic** — they describe workflows in terms of categories (data warehouse, notebook, product analytics, etc.) rather than specific products. The `.mcp.json` pre-configures specific MCP servers, but any MCP server in that category works.

## Connectors for this plugin

| Category | Placeholder | Included servers | Other options |
|----------|-------------|-----------------|---------------|
| Data warehouse | `~~data warehouse` | BigQuery, Definite | Snowflake\*, Databricks\*, Redshift, PostgreSQL, MySQL |
| Notebook | `~~notebook` | Hex | Jupyter, Deepnote, Observable |
| Product analytics | `~~product analytics` | Amplitude | Mixpanel, Heap |
| Project tracker | `~~project tracker` | Atlassian (Jira/Confluence) | Linear, Asana |

\* Not pre-configured. Snowflake and Databricks MCP servers live at an address unique to your organisation's account (for example `https://<account>.snowflakecomputing.com/...` or `https://<workspace>.cloud.databricks.com/api/2.0/mcp/...`), so they cannot ship in this pack. Ask your data team for the address and add it as a custom connector in Claude.
