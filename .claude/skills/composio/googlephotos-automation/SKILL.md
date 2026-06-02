# Google Photos Automation via Rube MCP

This documentation describes automation capabilities for Google Photos using Rube MCP (Composio). Here are the key points:

**Setup Requirements:**
The system requires Rube MCP connection with an active `googlephotos` toolkit. Users must verify availability through `RUBE_SEARCH_TOOLS` and complete authentication via `RUBE_MANAGE_CONNECTIONS` if needed.

**Main Operations:**
The toolkit supports six primary workflows: listing albums, creating new albums, uploading media files, batch operations, searching photos with filters, and organizing items into albums.

**Notable Features:**
- Upload support includes local files and direct URLs
- Batch operations allow multiple files in single requests
- Search functionality includes filtering by date ranges and content categories
- Album enrichments can add text overlays and location data

**Important Limitations:**
"GOOGLEPHOTOS_LIST_MEDIA_ITEMS is **deprecated** -- prefer GOOGLEPHOTOS_SEARCH_MEDIA_ITEMS" for retrieval tasks. File size restrictions apply: images up to 200MB and videos beyond that threshold will fail. Additionally, "Media items created via the API may not immediately appear in the Google Photos web UI due to processing delays."

**Key Constraint:**
Batch operations can "only add items to albums **created by the app** or albums the user owns," restricting organizational capabilities to owned or app-created collections.
