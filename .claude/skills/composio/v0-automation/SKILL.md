# V0 Automation via Rube MCP

This documentation outlines automating V0 tasks through Composio's toolkit using Rube MCP.

## Key Requirements

The setup necessitates three components: Rube MCP connectivity, an active V0 connection, and "Always call `RUBE_SEARCH_TOOLS` first to get current tool schemas."

## Setup Process

Users should add `https://rube.app/mcp` as an MCP server, verify Rube MCP availability, establish the V0 connection, and confirm active status before proceeding with workflows.

## Workflow Approach

The documentation recommends a three-step pattern:

1. **Tool Discovery**: Use RUBE_SEARCH_TOOLS to identify available tools with current schemas
2. **Connection Verification**: Confirm active status via RUBE_MANAGE_CONNECTIONS
3. **Tool Execution**: Run RUBE_MULTI_EXECUTE_TOOL with discovered parameters

## Critical Cautions

The guide emphasizes avoiding hardcoded tool slugs, verifying connection status beforehand, ensuring schema compliance with exact field names, including the memory parameter in all execution calls, and reusing session IDs appropriately within workflows.
