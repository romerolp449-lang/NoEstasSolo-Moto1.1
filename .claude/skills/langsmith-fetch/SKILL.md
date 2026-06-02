---
name: langsmith-fetch
description: Debug LangChain and LangGraph agents by retrieving execution traces from LangSmith Studio. Use when debugging agents, investigating failures, or analyzing performance bottlenecks.
---

# LangSmith Fetch

This skill provides a CLI tool for debugging LangChain and LangGraph agents by retrieving execution traces from LangSmith Studio.

## When to Use

Activate this skill when users mention:
- "Debug my agent"
- "Show me recent traces"
- "Why did it fail?"

## Key Features

Four primary workflows:

1. **Quick Debug** - Fetches recent activity:
   ```
   langsmith-fetch traces --last-n-minutes 5 --limit 5
   ```

2. **Deep Dive Analysis** - Examines specific traces:
   ```
   langsmith-fetch trace <trace-id>
   ```

3. **Session Export** - Saves debugging sessions with timestamps and creates organized folders

4. **Error Detection** - Searches for failures and generates error reports with frequency analysis

## Setup Requirements

```bash
pip install langsmith-fetch
```

Environment variables required:
- `LANGSMITH_API_KEY` - authentication credential
- `LANGSMITH_PROJECT` - target project identifier

## Common Use Cases

- Unresponsive agents
- Incorrect tool selection
- Memory operation failures
- Performance bottlenecks

## Output Formats

| Format | Use Case |
|--------|----------|
| `pretty` | Visual inspection |
| `json` | Detailed analysis |
| `raw` | Command piping |

## Pre-Use Checklist

1. Verify tracing is enabled in your agent
2. Confirm `LANGSMITH_PROJECT` matches your project
3. Check `LANGSMITH_API_KEY` is valid
4. Review available traces before deep analysis
