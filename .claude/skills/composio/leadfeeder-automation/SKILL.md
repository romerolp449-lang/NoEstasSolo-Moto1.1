# Leadfeeder Automation via Rube MCP

This documentation outlines how to automate Leadfeeder tasks using Composio's toolkit through Rube MCP.

## Key Requirements

The setup requires three components: Rube MCP connectivity, an active Leadfeeder connection, and adherence to a discovery-first approach. As the guide emphasizes, "Always call `RUBE_SEARCH_TOOLS` first to get current tool schemas."

## Workflow Overview

The automation follows a three-step pattern:

1. **Tool Discovery** – Query available tools using `RUBE_SEARCH_TOOLS` with your specific use case
2. **Connection Verification** – Confirm active status via `RUBE_MANAGE_CONNECTIONS`
3. **Execution** – Run tools through `RUBE_MULTI_EXECUTE_TOOL` with discovered parameters

## Critical Implementation Notes

The documentation stresses avoiding hardcoded tool slugs, emphasizing that "Tool schemas change. Never hardcode tool slugs or arguments without calling `RUBE_SEARCH_TOOLS`." Additional safeguards include verifying connection status, maintaining schema compliance, including memory parameters in requests, and managing pagination in responses.

This approach prioritizes dynamic tool discovery over static configuration, ensuring workflows remain compatible as the Leadfeeder toolkit evolves.
