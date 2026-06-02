# Yelp Automation via Rube MCP

This guide enables automation of Yelp tasks using Composio's toolkit through Rube MCP integration.

## Key Requirements

The setup requires three components: Rube MCP connectivity, an active Yelp connection, and proper tool discovery before execution.

## Setup Process

First, add the Rube MCP server endpoint to your client configuration. Then verify the connection is operational by testing `RUBE_SEARCH_TOOLS`. Finally, establish your Yelp connection through `RUBE_MANAGE_CONNECTIONS` and confirm the status shows active.

## Essential Workflow Steps

The recommended approach involves three phases: discovering available tools specific to your task, verifying the Yelp connection remains active, and executing the selected tools with schema-compliant parameters.

Tool discovery is emphasized as critical: "Always search first: Tool schemas change. Never hardcode tool slugs or arguments without calling `RUBE_SEARCH_TOOLS`"

## Important Practices

Several practices prevent common issues. Always include the memory parameter in execution calls, reuse session IDs within workflows, and check responses for pagination tokens when dealing with multiple result pages. The documentation stresses schema compliance and connection verification before attempting any operations.

The guide provides reference implementations for tool discovery, connection management, and bulk operations through the designated MCP functions.
