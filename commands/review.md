---
description: "Run a review-mode vibepod sandbox (wraps `vibepod run --mode review`)"
argument-hint: "[--lang <rust|go|node|python|java>] --prompt \"...\""
---

Execute the `vibepod` CLI in review mode. The container bundle's `settings.json` `permissions.deny` blocks Edit/Write/NotebookEdit and destructive git/build-tool/filesystem mutators; `--dangerously-skip-permissions` is NOT passed.

Run this command in the current shell:

```bash
vibepod run --mode review $ARGUMENTS
```

Notes:
- `--lang` is auto-detected from the project file if omitted.
- `--template <name>` is rejected in review mode — review templates are official-only (`--lang <lang>`), or use `generic` as a fallback.
