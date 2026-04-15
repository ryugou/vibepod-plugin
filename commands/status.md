---
description: "Show vibepod ECC cache status (wraps `vibepod template status`)"
---

Report the status of the local ECC (everything-claude-code) cache that vibepod uses as content source of truth.

Run this command in the current shell:

```bash
vibepod template status
```

The output shows the cache path, current ref, last-fetched timestamp, and whether an auto-refresh is due based on `refresh_ttl`.
