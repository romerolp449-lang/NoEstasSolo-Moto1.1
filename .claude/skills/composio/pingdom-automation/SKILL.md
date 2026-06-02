# Pingdom Automation via Rube MCP

This documentation describes automating Pingdom tasks through Composio's Pingdom toolkit via Rube MCP. The guide emphasizes a critical principle: "Always search tools first for current schemas" rather than hardcoding tool information.

## Key Requirements

The setup demands three prerequisites: Rube MCP connectivity, an active Pingdom connection through `RUBE_MANAGE_CONNECTIONS`, and consistently calling `RUBE_SEARCH_TOOLS` before executing workflows.

## Core Process

The recommended workflow follows three phases. First, discover available tools using `RUBE_SEARCH_TOOLS` with specific use cases. Second, verify connection status via `RUBE_MANAGE_CONNECTIONS` shows ACTIVE. Third, execute tools through `RUBE_MULTI_EXECUTE_TOOL` using discovered slugs and schema-compliant arguments.

## Critical Warnings

The documentation identifies several pitfalls to avoid: never hardcoding tool slugs without searching first, always verify active connection status, match exact field names from search results, include the memory parameter in execution calls, reuse session IDs within workflows, and handle pagination in responses.

## Access Method

Users can add `https://rube.app/mcp` as an MCP server without requiring API keys—only the endpoint configuration is necessary.
