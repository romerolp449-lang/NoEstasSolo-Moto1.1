# Lemlist Automation Integration

This documentation covers automating Lemlist multichannel outreach through Composio's MCP integration, enabling campaign management, lead enrollment, personalization, data export, and unsubscribe handling.

## Key Capabilities

The toolkit provides seven primary tools for workflow automation:

1. **Campaign Discovery** – List campaigns by status with pagination
2. **Campaign Details** – Retrieve specific campaign configuration
3. **Lead Enrollment** – Add leads with enrichment options (email finding, phone lookup, LinkedIn data)
4. **Variable Enrichment** – Attach custom personalization fields to enrolled leads
5. **Lead Lookup** – Resolve internal lead IDs from email addresses
6. **Data Export** – Download campaign leads with state filtering
7. **Unsubscribe Management** – Remove leads from campaigns

## Critical Implementation Notes

The documentation highlights several common failures to avoid:

- Campaign list responses may be nested under a `campaigns` key rather than returned as flat arrays
- Bulk operations should be chunked to approximately 50 leads per batch with progress checkpoints
- Lead variable operations require the internal Lemlist ID, not email addresses
- Variable additions are not upserts—duplicate keys trigger errors
- Cross-campaign deduplication can cause HTTP 500 errors; disable when intentional overlap is needed
