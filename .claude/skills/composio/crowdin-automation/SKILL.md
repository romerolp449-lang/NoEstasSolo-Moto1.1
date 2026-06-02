# Crowdin Automation via Rube MCP

This documentation outlines automating Crowdin tasks through Composio's toolkit integrated with Rube MCP.

## Key Requirements

The setup demands three prerequisites: active Rube MCP connectivity, an established Crowdin connection through `RUBE_MANAGE_CONNECTIONS`, and adherence to searching tools before execution.

## Essential Process

The workflow follows a three-step pattern. First, discover available tools using `RUBE_SEARCH_TOOLS` with specific Crowdin use cases. Second, verify the connection status remains active via `RUBE_MANAGE_CONNECTIONS`. Third, execute the discovered tools through `RUBE_MULTI_EXECUTE_TOOL` using schemas returned from the search.

## Critical Guidelines

The documentation emphasizes: "Always search first: Tool schemas change. Never hardcode tool slugs or arguments without calling `RUBE_SEARCH_TOOLS`". Additionally, sessions should be reused within workflows, memory parameters must always be included in tool calls, and pagination tokens require checking for complete data retrieval.

## Quick Operations

Various Crowdin operations map to specific approaches—discovery uses `RUBE_SEARCH_TOOLS`, connection uses `RUBE_MANAGE_CONNECTIONS`, execution uses `RUBE_MULTI_EXECUTE_TOOL`, and bulk operations leverage `RUBE_REMOTE_WORKBENCH`.
