# Lever Automation Documentation Summary

This resource provides guidance for automating recruiting operations within Lever ATS using Claude Code and Composio integration.

## Key Setup Requirements

To begin, users must add the Composio MCP server endpoint and authenticate their Lever account via OAuth when first running a Lever command.

## Primary Capabilities

The toolkit enables six core recruiting workflows:

**Job Posting Management** – The `LEVER_LIST_POSTINGS` tool retrieves postings with filters for state, team, department, location, and commitment type, supporting pagination up to 100 results.

**Candidate Pipeline Tracking** – Users can list opportunities through `LEVER_LIST_OPPORTUNITIES`, with parameters for posting ID, stage ID, date ranges, and expandable related objects like contact details and stage history.

**Opportunity Details** – The `LEVER_GET_OPPORTUNITY` tool fetches comprehensive information about individual candidates, including sources and applications.

**Requisition Management** – Tools exist for creating, retrieving, updating, and deleting requisitions, though updates require all mandatory fields as "full replacements."

**Pipeline Stage Visibility** – `LEVER_LIST_STAGES` displays configured hiring stages.

**Tag Organization** – `LEVER_LIST_TAGS` lists categorization tags across candidates and opportunities.

## Critical Implementation Notes

The documentation emphasizes that pagination is essential for large datasets, the expand parameter format differs across tools (arrays versus comma-separated strings), and API token scopes must include write permissions for modification operations.
