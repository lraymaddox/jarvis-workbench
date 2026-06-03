# jarvis-workbench

> Public systems-engineering workbench: AI-assisted infrastructure, agentic orchestration, and the artifacts that fall out of building alongside [Jarvis](https://github.com/lraymaddox) on a daily basis.

This is **not** a polished library. It is a working journal of how I (Lamar Maddox) build and operate AI/ML infrastructure in production — with a personal AI agent as a constant collaborator. The code is real, the bugs are real, the trade-offs are documented, and the commits are the receipts.

## What's Here

| Area | What lives here |
|------|-----------------|
| [`inference-bench/`](./inference-bench/) | Self-hosted LLM inference benchmarking harness — tokens/sec, cold-start, VRAM efficiency across backends (vLLM, llama.cpp, Ollama). The flagship project. |
| [`vault-ingestion/`](./vault-ingestion/) | Pipeline for ingesting research → guides → atomic wiki entries. Multi-agent validation. Ties into the [RayRay](https://github.com/lraymaddox) Obsidian vault. |
| [`hermes-orchestration/`](./hermes-orchestration/) | Multi-agent delegation patterns, cron-driven research loops, subagent protocols I've validated. |
| [`s6-supervision/`](./s6-supervision/) | Container supervision patterns — s6-overlay, health gates, restart policies. |
| [`adr/`](./adr/) | Architecture Decision Records from active projects. Why we picked X over Y. |
| [`dotfiles/`](./dotfiles/) | Refreshed terminal/dev environment. Mirror of [lraymaddox/mydotfiles](https://github.com/lraymaddox/mydotfiles), kept in sync. |

## How This Repo Is Built

Every commit in this repository is the output of a real session — either a hands-on build, a debugging investigation, or a multi-agent orchestration. I do not stage commits to manufacture activity. The contribution graph is what it is.

**Operating principles:**
- **Ship, don't polish.** Working code with a clear README beats a perfect library with no users.
- **Document trade-offs, not just decisions.** Every non-obvious choice lives in an ADR.
- **Tests where they earn their keep.** Benchmarking code has assertions. Glue code is allowed to be light.
- **Public from day one.** Mistakes stay visible. The audit trail is the point.

## Featured Projects

- **inference-bench** — a reproducible harness for measuring LLM serving performance on commodity and accelerator hardware. Designed to be the companion to my [AI Infrastructure](https://youtube.com/@aiDotEngineering) YouTube series.
- **vault-ingestion** — closes the loop between research agents and a personal knowledge base, with adversarial validation to prevent hallucinated entries.
- **hermes-orchestration** — production patterns for AI-agent swarms: who delegates to whom, who validates, who escalates.

## Context

I'm a senior SRE/AI engineer working toward a role as an AI engineer. My [YouTube channel](https://youtube.com/@aiDotEngineering) covers AI infrastructure, GPU orchestration, and the engineering behind running LLMs at scale. This repo is the public, verifiable counterpart to that content — every claim I make in a video should be reproducible from code in this workbench.

## Ask Me About

- Self-hosted LLM inference (vLLM, llama.cpp, Ollama, model quantization trade-offs)
- Multi-agent orchestration patterns and failure modes
- GPU infrastructure on shared HPC (HiPerGator / SLURM-style)
- Vault pipelines for research agents
- Container supervision and graceful-shutdown semantics
- Anything tagged `adr/` — the reasoning is documented and I enjoy the debate

## License

MIT for code. Documentation (ADRs, READMEs) is CC-BY-4.0 — fork, remix, attribute.

---

*Work in progress. Pull requests welcome on anything that has a clear `TODO(human)` or `TODO(jarvis)` marker. Issues are open.*
