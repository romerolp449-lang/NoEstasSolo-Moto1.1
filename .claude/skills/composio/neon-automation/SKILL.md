# Neon Automation Integration Guide

The Neon Automation toolkit enables management of serverless Postgres operations through Composio's MCP integration. Here's what you need to know:

## Key Setup Steps

Connect via the Composio MCP server at `https://rube.app/mcp`, authenticate with your Neon API key, and you're ready to automate database workflows.

## Primary Operations

The toolkit provides nine core tools for managing Neon infrastructure:

- **Project management**: List all projects and retrieve individual project details
- **Branch operations**: Enumerate development branches within projects
- **Database inventory**: Discover databases on specific branches
- **Connection strings**: Generate Postgres URIs with embedded credentials
- **Role & database inspection**: Verify available roles and database metadata
- **Organization management**: Access org details and create API keys

## Critical Security Considerations

As stated in the documentation: "The returned URI includes credentials. Treat it as a secret -- do not log or share it." Connection strings should be handled as sensitive data throughout your workflows.

## Common Implementation Issues

The `org_id` parameter is mandatory when using personal API keys for project listing. Pagination requires iterating through cursor values to capture complete result sets. Rate limiting may occur during bulk operations, necessitating request throttling. Invalid role-database pairings will return authentication errors—validate roles first using the dedicated roles tool.
