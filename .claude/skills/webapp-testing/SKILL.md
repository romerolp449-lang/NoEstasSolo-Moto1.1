---
name: webapp-testing
description: Test local web applications through native Python Playwright scripts. Supports both static HTML and dynamic server-backed apps. Use for automated UI testing, visual regression testing, and end-to-end workflow validation.
---

# Webapp Testing

This skill enables testing of local web applications through native Python Playwright scripts.

## Decision Framework

Determine your target type first:
- **Static HTML**: Read directly from filesystem
- **Dynamic app**: Requires server management via `scripts/with_server.py`

## Key Resources

The `scripts/with_server.py` helper manages server lifecycle for single or multiple services.

Always run scripts with `--help` first to understand usage before attempting customization.

## Core Workflow

The reconnaissance-then-action pattern:
1. Navigate and wait for `networkidle`
2. Capture screenshots or inspect DOM to identify selectors
3. Execute actions using discovered selectors

**Critical reminder**: Do not inspect the DOM before waiting for `networkidle` on dynamic apps - this common mistake causes automation failures.

## Implementation

Use `sync_playwright()` for synchronous automation. The helper manages server startup automatically, so your Playwright script focuses solely on browser interaction logic.

### Example Server Launch

```bash
python scripts/with_server.py --server "npm run dev" --port 5173 -- python your_automation.py
```

## Examples

The `examples/` directory demonstrates:
- Element discovery patterns
- Static HTML automation
- Console logging patterns
- Screenshot capture

## Supported Test Types

- UI interaction testing
- Visual regression testing
- Form submission testing
- Navigation flow testing
- Console error monitoring
