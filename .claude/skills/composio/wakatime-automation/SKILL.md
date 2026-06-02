# Wakatime Automation via Rube MCP

This documentation describes automating Wakatime tasks through Composio's toolkit via Rube MCP integration.

## Key Requirements

The setup necessitates three components: Rube MCP connectivity with `RUBE_SEARCH_TOOLS` available, an active Wakatime connection established through `RUBE_MANAGE_CONNECTIONS`, and always searching for current tool schemas first.

## Workflow Process

The recommended approach follows three steps: discovering available tools using `RUBE_SEARCH_TOOLS` with specific use cases, verifying connection status shows "ACTIVE" via `RUBE_MANAGE_CONNECTIONS`, then executing operations through `RUBE_MULTI_EXECUTE_TOOL` with discovered tool identifiers.

## Critical Guidelines

Several practices prevent common failures. Tool schemas should never be hardcoded since they change—always call the search function. The memory parameter must be included in execution calls. Session IDs should be reused within workflows but generated fresh for new ones. Additionally, responses should be checked for pagination tokens to ensure complete data retrieval.

## Additional Resources

For bulk operations and comprehensive schema details, the documentation references `RUBE_REMOTE_WORKBENCH` and `RUBE_GET_TOOL_SCHEMAS` respectively. Complete toolkit documentation is available at composio.dev/toolkits/wakatime.
