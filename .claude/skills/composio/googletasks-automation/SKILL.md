# Google Tasks Automation via Rube MCP

This documentation describes a toolkit for automating Google Tasks operations through Rube MCP (Composio). Here are the key aspects:

## Core Capabilities
The toolkit enables users to "create, manage, organize, and bulk-operate on Google Tasks and task lists." Primary functions include creating tasks, listing task lists, updating task details, deleting tasks, and performing batch operations.

## Setup Requirements
Users must have Rube MCP connected and an active Google Tasks connection established through `RUBE_MANAGE_CONNECTIONS`. The documentation emphasizes always calling `RUBE_SEARCH_TOOLS` first to retrieve current tool schemas.

## Essential Tools
Key operations are available through tools like `GOOGLETASKS_INSERT_TASK` for creation, `GOOGLETASKS_UPDATE_TASK` for modifications, and `GOOGLETASKS_BULK_INSERT_TASKS` for batch operations. All date parameters require RFC3339 formatting.

## Critical Warnings
The documentation highlights important constraints: both task list ID and task ID are required for most operations, date formats must be strictly RFC3339 compliant, and the `GOOGLETASKS_CLEAR_TASKS` operation "permanently deletes all completed tasks from a list."

## Practical Workflow Pattern
The recommended approach involves first discovering available task lists, then retrieving specific task IDs before performing modifications—avoiding attempts to operate on tasks without knowing their parent list.
