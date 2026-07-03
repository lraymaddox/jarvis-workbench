# Jarvis Workbench

Public systems-engineering workbench: AI-assisted infrastructure, agentic orchestration, and build artifacts.

## Stack
- Mixed: Bash scripts, Python utilities, Markdown ADRs, dotfiles
- No build system — each directory is self-contained
- Not a deployable service — documentation and tooling artifacts

## Structure
- `adr/`: Architecture Decision Records
- `dotfiles/`: Shell configs and editor settings
- `hermes-orchestration/`: Hermes fleet orchestration scripts and patterns
- `inference-bench/`: LLM inference benchmarking scripts
- `s6-supervision/`: s6-overlay service supervision configs
- `vault-ingestion/`: Obsidian vault ingestion pipeline scripts

## Rules
- This is a public repo — no secrets, no private fleet details
- ADRs use the MADR format (Markdown Any Decision Records)
- Scripts are standalone — each has a shebang and is executable

## Boundaries
- Never commit private fleet data (API keys, account IDs, internal hostnames)
- Vault scripts reference iCloud paths — test locally before committing
