# vibepod-plugin

Claude Code plugin exposing slash commands that wrap the [`vibepod`](https://github.com/ryugou/vibepod) CLI.

## Commands

| Slash command | Wraps |
| --- | --- |
| `/vibepod:run` | `vibepod run $ARGUMENTS` |
| `/vibepod:review` | `vibepod run --mode review $ARGUMENTS` |
| `/vibepod:status` | `vibepod template status` |

## Prerequisites

- `vibepod` ≥ 1.6.0 on `PATH`
  - `brew install ryugou/tap/vibepod` or `cargo install vibepod`
- Run `vibepod init` once to clone the ECC cache into `~/.config/vibepod/ecc-cache/`.
- Docker Desktop (or compatible) running locally.

## Install

```
/plugin install ryugou/vibepod-plugin
```

## Usage

```
/vibepod:run --lang rust --prompt "add a smoke test for the CLI entrypoint"
/vibepod:review --lang rust --prompt "review the diff against main"
/vibepod:status
```

`--lang` is auto-detected from `Cargo.toml` / `go.mod` / `package.json` / `pyproject.toml` / `pom.xml` when omitted.

## License

MIT
