# Rocketlane Automation via Rube MCP

This documentation outlines how to automate Rocketlane tasks using Composio's toolkit through Rube MCP. Here are the key takeaways:

## Essential Setup Steps

The guide requires three prerequisites: active Rube MCP connection, Rocketlane toolkit configured via `RUBE_MANAGE_CONNECTIONS`, and always calling `RUBE_SEARCH_TOOLS` first for current schemas.

To get started, add `https://rube.app/mcp` as an MCP server endpoint (no API keys required), then verify Rube MCP availability and confirm the Rocketlane connection shows ACTIVE status.

## Workflow Pattern

The recommended approach follows three stages: discovering available tools using `RUBE_SEARCH_TOOLS`, verifying the connection is active, and executing tools through `RUBE_MULTI_EXECUTE_TOOL` with discovered slugs and schema-compliant arguments.

## Critical Reminders

As noted, users should "Always search first" since tool schemas change, and hardcoding tool information without discovery is problematic. The documentation emphasizes verifying connection status and maintaining session reuse within workflows rather than generating new sessions unnecessarily. Including the memory parameter in execution calls—even as an empty object—is mandatory.
