# Humanloop Automation via Rube MCP

This document provides guidance for automating Humanloop tasks through Composio's toolkit using Rube MCP integration.

## Key Requirements

The setup necessitates three elements: Rube MCP connectivity, an active Humanloop connection, and adherence to a discovery-first approach. As stated, users must "Always call `RUBE_SEARCH_TOOLS` first to get current tool schemas."

## Core Workflow

The recommended pattern involves three sequential steps:

1. **Discovery**: Use `RUBE_SEARCH_TOOLS` to identify available tools and their schemas
2. **Verification**: Confirm connection status via `RUBE_MANAGE_CONNECTIONS`
3. **Execution**: Deploy tools through `RUBE_MULTI_EXECUTE_TOOL` with discovered parameters

## Critical Guidance

The documentation emphasizes several important constraints. "Tool schemas change. Never hardcode tool slugs or arguments without calling `RUBE_SEARCH_TOOLS`" represents a fundamental principle. Additionally, users should "Always include `memory` in `RUBE_MULTI_EXECUTE_TOOL` calls, even if empty."

## Setup Process

Rube MCP configuration requires adding a specific endpoint to your client without additional API keys. Users should verify availability, establish the Humanloop connection through provided authentication flows, and confirm active status before workflow execution.
