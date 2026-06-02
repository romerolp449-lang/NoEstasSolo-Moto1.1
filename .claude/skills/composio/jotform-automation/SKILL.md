# Jotform Automation Overview

The Jotform Automation toolkit enables users to manage their Jotform accounts through natural language commands. It provides six primary capabilities:

**Core Functions:**
The toolkit supports form discovery and searching, user account inspection, activity auditing, folder/label organization, and plan limit verification. All operations are executed "through natural language" via the Rube MCP server integration.

**Key Tools:**
- `JOTFORM_GET_USER_FORMS` retrieves forms with search and filtering options
- `JOTFORM_GET_USER_DETAILS` displays account information and usage statistics
- `JOTFORM_GET_USER_HISTORY` tracks account activities with action and date filtering
- `JOTFORM_GET_USER_FOLDERS` manages the label structure
- `JOTFORM_GET_SYSTEM_PLAN` compares pricing tier features

**Setup Requirements:**
Integration requires adding the Rube MCP server and authenticating via Jotform API key through Composio.

**Important Considerations:**
The documentation notes that Jotform migrated from folders to labels, date filters require MM/DD/YYYY formatting, and plan name parameters are case-sensitive (`FREE`, `BRONZE`, `SILVER`, `GOLD`, `PLATINUM`). Pagination uses offset-based navigation rather than cursor or page-based systems.
