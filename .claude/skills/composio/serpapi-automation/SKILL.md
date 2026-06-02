# Serpapi Automation via Rube MCP

This documentation outlines automating Serpapi operations through Composio's toolkit using Rube MCP. Here are the key points:

## Prerequisites & Setup
You'll need Rube MCP connected with an active Serpapi connection. The setup process involves adding the MCP server endpoint, verifying availability through `RUBE_SEARCH_TOOLS`, and confirming an active connection status via `RUBE_MANAGE_CONNECTIONS`.

## Essential Workflow
The recommended approach follows three steps: first discover available tools by querying Serpapi-specific use cases, then verify the connection is active, and finally execute tools with schema-compliant arguments. The documentation emphasizes that "Tool schemas change. Never hardcode tool slugs or arguments without calling `RUBE_SEARCH_TOOLS`."

## Important Guidelines
Several critical practices are highlighted, including always including the `memory` parameter (even if empty), reusing session IDs within workflows, and checking responses for pagination tokens to ensure complete data retrieval. Connection verification before tool execution is mandatory.

## Tool Discovery
Rather than assuming tool availability, the system requires dynamic schema discovery. This approach ensures compatibility as tools evolve and prevents errors from outdated hardcoded references.

The resource is powered by Composio and directs users to their toolkit documentation for detailed information.
