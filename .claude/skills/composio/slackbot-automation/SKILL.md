# Slackbot Automation via Rube MCP

This documentation outlines how to automate Slackbot operations through Composio's toolkit using Rube MCP.

## Key Requirements

The setup necessitates an active Rube MCP connection with `RUBE_SEARCH_TOOLS` available and a functioning Slackbot connection established via `RUBE_MANAGE_CONNECTIONS`.

## Essential Workflow Steps

The recommended approach involves three phases: first, discover applicable tools using `RUBE_SEARCH_TOOLS` with your specific use case; second, verify connection status through `RUBE_MANAGE_CONNECTIONS`; and third, execute tools via `RUBE_MULTI_EXECUTE_TOOL` with the discovered tool slugs.

## Critical Guidelines

Documentation emphasizes that "tool schemas change. Never hardcode tool slugs or arguments" without performing a fresh search. Additionally, users must verify the connection displays an ACTIVE status prior to executing any operations, and should ensure the `memory` parameter is included in tool execution calls even when empty.

## Additional Resources

The complete toolkit documentation is available at composio.dev/toolkits/slackbot, and Rube MCP can be accessed by adding `https://rube.app/mcp` as an MCP server endpoint.
