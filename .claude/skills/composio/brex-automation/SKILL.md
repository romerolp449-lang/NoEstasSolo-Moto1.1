# Brex Automation via Rube MCP

This documentation describes how to automate Brex operations using Composio's toolkit through the Rube MCP server.

## Key Requirements

The setup necessitates three components: Rube MCP connectivity, an active Brex connection, and the practice of "Always call `RUBE_SEARCH_TOOLS` first to get current tool schemas."

## Implementation Approach

The workflow follows a structured three-step pattern:

1. **Tool Discovery** — Use `RUBE_SEARCH_TOOLS` to identify available tools and their schemas
2. **Connection Verification** — Confirm Brex connection status is ACTIVE via `RUBE_MANAGE_CONNECTIONS`
3. **Execution** — Run tools with `RUBE_MULTI_EXECUTE_TOOL` using discovered schemas

## Critical Guidelines

The documentation emphasizes several important practices: avoid hardcoding tool slugs without fresh searches, always verify connection status beforehand, maintain schema compliance with exact field names, include the memory parameter in all tool executions, and handle pagination tokens in responses.

The resource provides a quick reference table linking common operations to their corresponding Rube MCP functions, helping users select the appropriate approach for their specific automation needs.
