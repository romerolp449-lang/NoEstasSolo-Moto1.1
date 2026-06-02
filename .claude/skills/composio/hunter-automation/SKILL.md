# Hunter Automation Overview

Hunter Automation integrates Hunter.io's email intelligence capabilities through the Composio MCP server, enabling users to discover, verify, and manage email addresses via natural language commands.

## Key Capabilities

The toolkit provides six primary functions:

1. **Domain Email Search** – Locate publicly available email addresses for companies with filtering by department, seniority, and type
2. **Individual Email Finding** – Infer likely email addresses for specific people using name and company/domain
3. **Email Verification** – Validate deliverability and assess risk for target addresses
4. **Email Volume Estimates** – Check Hunter's database size for a domain (free operation)
5. **Lead Management** – Create or update prospect records via single upsert calls
6. **Account Monitoring** – Review plan details and remaining API quotas

## Setup Requirements

Users must add the Composio MCP server endpoint and authenticate with a Hunter.io API key to begin operations.

## Important Constraints

The documentation emphasizes several limitations: free/basic plans restrict domain searches to 10 results per request, email counts represent approximations rather than guaranteed retrievable numbers, and pagination requires manual offset handling. Authentication failures return HTTP 401 errors, while empty result sets should not be treated as system failures.
