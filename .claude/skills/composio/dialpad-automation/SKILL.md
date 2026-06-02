# Dialpad Automation via Rube MCP

This guide enables automation of Dialpad tasks through Composio's toolkit integrated via Rube MCP. The setup requires three key components: establishing a Rube MCP connection, activating Dialpad credentials, and discovering available tools before execution.

## Key Setup Steps

The process follows a structured approach: first verify Rube MCP availability, then authenticate the Dialpad connection through `RUBE_MANAGE_CONNECTIONS`, and confirm the connection reaches "ACTIVE" status before proceeding.

## Essential Workflow Pattern

Tool discovery comes first—always call `RUBE_SEARCH_TOOLS` with specific use cases to retrieve current schemas and tool slugs. As the documentation emphasizes, "Tool schemas change. Never hardcode tool slugs or arguments without calling" the search function.

The standard execution sequence involves three stages: discovering tools via search, checking connection status, and executing operations through `RUBE_MULTI_EXECUTE_TOOL` with schema-compliant arguments.

## Critical Reminders

Several pitfalls require attention: maintain session IDs across related operations, include the memory parameter in all tool calls (even if empty), verify schemas match exactly from search results, and handle pagination when responses contain multiple pages.

The documentation references [composio.dev/toolkits/dialpad](https://composio.dev/toolkits/dialpad) for complete toolkit documentation and emphasizes that no API keys are needed—only the MCP endpoint configuration.
