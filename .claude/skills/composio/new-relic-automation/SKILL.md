# New Relic Automation via Composio MCP

This documentation covers automating New Relic observability tasks through the Composio MCP integration.

## Key Capabilities

The toolkit enables management of alert policies, notification channels, alert conditions, and application monitoring. Setup requires adding the Composio MCP server and authenticating with a New Relic API key.

## Primary Tools

**Policy Management:** Tools allow creating, listing, and deleting alert policies. Policies must have unique names within an account and support three incident preference modes (PER_POLICY, PER_CONDITION, PER_CONDITION_AND_TARGET).

**Notification Channels:** The system supports email, Slack, webhook, PagerDuty, OpsGenie, and VictorOps. Each channel type requires different configuration parameters—for example, email needs recipients while PagerDuty requires a service key.

**Application Monitoring:** Separate endpoints list APM and browser-monitored applications with optional filtering by name, host, or ID.

## Important Considerations

The documentation highlights several implementation details: policy names must be unique, channel configuration varies by type, all list endpoints use pagination, and there's a type mismatch where one policy deletion tool expects strings while the conditions lookup expects integers. Additionally, creating a channel doesn't automatically link it to policies—that association requires separate configuration.
