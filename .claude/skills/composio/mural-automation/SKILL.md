# Mural Automation via Rube MCP

This documentation outlines how to automate Mural tasks using Composio's toolkit through the Rube MCP server. Here are the key points:

## Essential Requirements

You need three main components: Rube MCP connectivity, an active Mural connection, and discovery of current tool schemas before executing any workflows.

## Setup Process

The setup involves four steps: verify Rube MCP availability, establish the Mural connection, authenticate if needed, and confirm the connection reaches ACTIVE status.

## Workflow Approach

The recommended pattern follows three phases: discover available tools via `RUBE_SEARCH_TOOLS`, verify connection status through `RUBE_MANAGE_CONNECTIONS`, then execute tools using `RUBE_MULTI_EXECUTE_TOOL` with discovered tool slugs and schema-compliant arguments.

## Critical Guidelines

The documentation emphasizes: "Always search first: Tool schemas change. Never hardcode tool slugs or arguments" without calling the search function. Always include the memory parameter even when empty, reuse session IDs within workflows, and check responses for pagination tokens.

## Common Operations

Operations range from tool discovery and connection management to executing individual tools, running bulk operations via workbench, and retrieving complete schemas for tools with schema references.
