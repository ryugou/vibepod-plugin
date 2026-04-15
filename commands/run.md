---
description: "Run a task inside a vibepod sandbox container (wraps `vibepod run`)"
argument-hint: "[--lang <rust|go|node|python|java>] [--mode impl|review] --prompt \"...\""
---

Execute the `vibepod` CLI with the user's arguments to launch a sandboxed Claude Code session.

Run this command in the current shell:

```bash
vibepod run $ARGUMENTS
```

Notes:
- `--lang` selects the official bundle (auto-detected from `Cargo.toml` / `go.mod` / `package.json` / `pyproject.toml` / `pom.xml` if omitted).
- `--mode impl` (default) enables Edit/Write; `--mode review` denies mutators via `permissions.deny`.
- `--template <name>` is for custom templates at `~/.config/vibepod/templates/<name>/` and is mutually exclusive with `--mode review`.
- If `vibepod` is not installed, instruct the user to install it via `brew install ryugou/tap/vibepod` or `cargo install vibepod`, then run `vibepod init`.
