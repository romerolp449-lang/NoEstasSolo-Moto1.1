# Customer.io Automation via Composio

This documentation describes an MCP integration enabling programmatic control of Customer.io customer engagement operations.

## Key Capabilities

The toolkit provides six primary workflows:

1. **Broadcast Triggering** – "Manually fire a pre-configured broadcast to a specific audience with personalization data" using the `CUSTOMERIO_TRIGGER_BROADCAST` tool, with support for targeting by customer IDs, email addresses, or complex segment filters.

2. **Delivery Analytics** – Retrieve paginated metrics across message types (email, webhook, SMS, Slack, push, in-app) filtered by campaign, time window, and engagement actions like opens and clicks.

3. **Segment Management** – Access all audience segments defined in your workspace to enable targeted campaign distribution.

4. **Newsletter Discovery** – Browse newsletter metadata with cursor-based pagination for content tracking.

5. **Template Inventory** – List transactional message templates to identify IDs for API-based sending workflows.

6. **Trigger History** – Review and inspect individual broadcast execution records.

## Critical Constraints

The documentation emphasizes three operational boundaries:

- Audience selection requires exactly one targeting method; combining multiple approaches triggers errors
- Broadcasts enforce rate-limiting at one request per 10 seconds per campaign ID
- Time filtering expects Unix timestamp format rather than ISO strings

The integration requires initial authentication through the Composio MCP server before tool availability.
