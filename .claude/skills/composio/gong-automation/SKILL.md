# Gong Automation

Gong Automation enables natural language access to call intelligence through the Composio MCP integration. The platform lets users retrieve transcripts, analyze call data, access analytics, and manage workspaces.

## Key Capabilities

The toolkit provides six core workflows:

1. **Retrieve Call Transcripts by Date Range** — Extract transcripts from specified time periods using the `GONG_RETRIEVE_TRANSCRIPTS_OF_CALLS_V2_CALLS_TRANSCRIPT` tool, with optional filtering by call IDs or workspace.

2. **Get Specific Call Transcripts** — Fetch transcripts with speaker details and timestamps using `GONG_GET_CALL_TRANSCRIPT` by providing call IDs.

3. **List Calls by Date Range** — Obtain basic call metadata (participants, duration) within specified dates via `GONG_RETRIEVE_CALL_DATA_BY_DATE_RANGE_V2_CALLS`.

4. **Get Detailed Call Analytics** — Access extensive insights including highlights, key points, topics, trackers, and speaker statistics using `GONG_RETRIEVE_FILTERED_CALL_DETAILS`.

5. **Get Specific Call by ID** — Retrieve individual call data using `GONG_RETRIEVE_DATA_FOR_A_SPECIFIC_CALL_V2_CALLS_ID`.

6. **List Company Workspaces** — View all organization workspaces via `GONG_LIST_ALL_COMPANY_WORKSPACES_V2_WORKSPACES`.

## Important Constraints

Users must follow ISO-8601 date formatting (e.g., `2025-02-01T00:00:00Z`), handle pagination for large datasets, understand that media URLs expire after 8 hours, and verify appropriate API scopes are enabled for each endpoint.
