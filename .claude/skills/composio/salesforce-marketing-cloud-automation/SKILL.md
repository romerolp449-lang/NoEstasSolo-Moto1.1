# Salesforce Marketing Cloud Automation via Rube MCP

This documentation outlines how to automate Salesforce Marketing Cloud operations through Composio's toolkit via Rube MCP.

## Key Requirements

The setup demands three components: Rube MCP connectivity (with RUBE_SEARCH_TOOLS available), an active Salesforce Marketing Cloud connection through RUBE_MANAGE_CONNECTIONS, and adherence to always searching for current tool schemas first.

## Essential Workflow Steps

The recommended approach follows three phases:

1. **Tool Discovery**: Call RUBE_SEARCH_TOOLS with your specific Salesforce Marketing Cloud use case to retrieve available tool slugs and input schemas
2. **Connection Verification**: Use RUBE_MANAGE_CONNECTIONS to confirm the toolkit connection shows ACTIVE status
3. **Tool Execution**: Run RUBE_MULTI_EXECUTE_TOOL with discovered tool slugs and schema-compliant arguments

## Critical Best Practices

The documentation emphasizes: "Always search first: Tool schemas change. Never hardcode tool slugs or arguments without calling RUBE_SEARCH_TOOLS." Additional safeguards include verifying connection status before execution, matching exact field names from search results, including the memory parameter in all tool calls, and reusing session IDs within workflows.

## Getting Started

Access Rube MCP by adding the endpoint `https://rube.app/mcp` to your client configuration without requiring API keys. The full toolkit documentation is available through Composio's official resources.
