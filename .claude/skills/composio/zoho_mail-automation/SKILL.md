# Zoho Mail Automation via Rube MCP

This documentation guides users through automating Zoho Mail operations using Composio's toolkit integrated with Rube MCP.

## Key Requirements

The system demands three prerequisites: Rube MCP connectivity, an active Zoho Mail connection, and adherence to a discovery-first pattern. As stated, users should "Always call `RUBE_SEARCH_TOOLS` first to get current tool schemas."

## Setup Process

Configuration involves three steps: verifying Rube MCP availability, establishing a Zoho Mail connection via `RUBE_MANAGE_CONNECTIONS`, and confirming the connection reaches ACTIVE status before workflow execution.

## Essential Pattern: Tool Discovery

Rather than hardcoding operations, the workflow emphasizes querying available tools first. The documentation warns that "Tool schemas and available operations may change. Never hardcode tool slugs without first discovering them via `RUBE_SEARCH_TOOLS`."

## Execution Framework

Once tools are discovered, operations execute through `RUBE_MULTI_EXECUTE_TOOL` with schema-compliant arguments. Complex workflows chain multiple steps, with responses flowing between sequential operations.

## Critical Safeguards

The documentation highlights several protection measures: validating connection status before execution, respecting rate limits, ensuring strict schema compliance, and implementing error handling that re-authenticates when tokens expire.
