# Project Index

Purpose: give a stateless AI a compact map of the PUBLIC project before it reads or edits files.

## Stack

| Field | Value | Last verified |
|---|---|---|
| Agent Handoff Kit template version | 0.3.36 | 2026-07-05 |
| Public product version | 0.1.0 | 2026-07-05 |
| Product identity | 意脈系統 | 2026-07-05 rename correction |
| Runtime | Public Markdown scaffold + local Agent Handoff Kit governance | 2026-07-05 |
| Framework | Not applicable — public product scaffold | 2026-07-05 |
| Package manager | Not yet defined for the product; npm package / CLI still pending | 2026-07-05 positioning correction |
| Test command | `npx --yes @adamchanadam/agent-handoff-kit@latest doctor --root .` for governance health only | 2026-07-05 |
| Build command | Not configured | 2026-07-05 |
| Deploy command | Not configured; release/deploy requires explicit authorization | 2026-07-05 |

## Directory Map

| Path | Role | Read when |
|---|---|---|
| `README.md` | public product entrypoint: what 意脈系統 is, who it serves, and current status | public-facing docs or onboarding change |
| `PUBLICATION_BOUNDARY.md` | public/private boundary and product-vs-governance separation source of truth | before importing, publishing, syncing, or documenting content |
| `docs/README.md` | public product documentation index | public docs change |
| `docs/releases/` | public release notes written for product readers, not internal development logs | release |
| `examples/README.md` | public reproducible examples placeholder and constraints | adding or changing examples |
| `skill/README.md` | future 意脈系統 skill/package placeholder and constraints | adding or changing skill package content |
| `VERSION` | public product version source until package metadata exists | version bump |
| `AGENTS.md` | Agent Handoff Kit entry and startup contract for AI collaborators, not ordinary public product docs | session startup |
| `CLAUDE.md` | Claude Code bridge to the same startup path | Claude Code startup |
| `GEMINI.md` | Google Antigravity CLI / Gemini CLI migration bridge to the same startup path | Antigravity / Gemini startup |
| `START_NEXT_SESSION_PROMPT.txt` | auto-generated stateful startup prompt for the next local-agent session; `dev/SESSION_HANDOFF.md` remains authoritative | next session startup |
| `dev/` | Agent Handoff Kit governance state for PUBLIC only | startup, closeout, governance changes |

## Entry Points

| Entry | Path | Notes |
|---|---|---|
| Public product reading | `README.md` | Start here for public understanding of the product |
| Boundary guide | `PUBLICATION_BOUNDARY.md` | Must be read before adding public content |
| Public docs | `docs/README.md` | Documentation index |
| Public examples | `examples/README.md` | Future reproducible examples |
| Future skill/package | `skill/README.md` | Future product capability packaging |
| AI agent startup | `AGENTS.md` | For agent continuity only; not the product value proposition |
| Next-session prompt | `START_NEXT_SESSION_PROMPT.txt` | Convenience copy; `dev/SESSION_HANDOFF.md` remains authoritative |

## Fact Base

Reachable means the source can be found. It does not mean the source has been read in this session.

| Source | Role | Required before | Access method | Last verified |
|---|---|---|---|---|
| `README.md` | public product positioning and current public status | public docs, onboarding, version summary | local file | 2026-07-05 positioning correction |
| `PUBLICATION_BOUNDARY.md` | source of truth for what PUBLIC may contain and how to keep product-vs-governance separation | importing content, publishing, release, examples, skill packaging | local file | 2026-07-05 positioning correction |
| `VERSION` | public product version source until package metadata exists | public version bump | local file | 2026-07-05 |
| `docs/README.md` | public docs boundary placeholder | adding public docs | local file | 2026-07-05 positioning correction |
| `docs/releases/v0.1.0.md` | public release notes for v0.1.0 | GitHub Release v0.1.0 | local file | 2026-07-05 release preparation |
| `examples/README.md` | examples boundary placeholder | adding examples | local file | 2026-07-05 positioning correction |
| `skill/README.md` | product skill/package boundary placeholder | adding public skill package content | local file | 2026-07-05 positioning correction |

## External Sources

| Source | Role | Required before | Access method | `via` | Write-back rule | Last verified |
|---|---|---|---|---|---|---|
| `https://github.com/Adamchanadam/agent-handoff-kit` | Agent Handoff Kit reference for governance-layer behavior only | changing Agent Handoff Kit governance claims | browser / manual web read | manual paste | no write | 2026-07-05 |
| `https://adamchanadam.github.io/agent-handoff-kit/agent-handoff-kit-ai-install.html` | Agent Handoff Kit install/upgrade reference for governance-layer maintenance only | changing Agent Handoff Kit runtime maintenance commands | browser / manual web read | manual paste | no write | 2026-07-05 |

> Agent Handoff Kit external sources must not be used as the product install truth for `意脈系統`. Product package / CLI / deployment sources are not defined yet.

## Installed Integrations

> **Credential Separation Principle**: this section records only project usage and public reference coordinates. It must never record API keys, OAuth tokens, or credential values.

> Purpose: a new AI session reads this section to understand declared external-tool capabilities and their project roles. Every entry must include `Declared` and `Last Verified` fields so stale capability assumptions can be detected.

### Connectors

| Tool | Project Usage | Access Scope | Specific Instance | Credential Reference (no value) | Declared | Last Verified |
|------|---------------|--------------|-------------------|---------------------|----------|---------------|
| None declared | Not applicable | not_applicable | not_applicable | not_applicable | 2026-07-05 | 2026-07-05 |

### MCPs

| Server | Source | Project Usage | Credential Reference (no value) | Declared | Last Verified |
|--------|--------|---------------|---------------------|----------|---------------|
| None declared | Not applicable | not_applicable | not_applicable | 2026-07-05 | 2026-07-05 |

### Plugins

| Name | Bundle Content (Skills + MCP + hooks) | When Triggered | Last Verified |
|------|----------------------------------------|----------------|---------------|
| None declared | not_applicable | not_applicable | 2026-07-05 |

### Skills

| Name | Source | When Triggered | Last Verified |
|------|--------|----------------|---------------|
| Agent Handoff Kit runtime skills | `@adamchanadam/agent-handoff-kit` generated files | startup, closeout, governance, safety, docs, release-sensitive work | 2026-07-05 |

### Source-of-truth Architecture

| Layer | Surface (specific instance) | Role | Write Direction |
|-------|--------------------------|------|-----------------|
| Public product truth | `README.md`, `docs/`, `examples/`, `skill/`, future package files | 意脈系統 positioning, public docs, examples, and product packaging | Agent may edit local files after reading boundary and with normal safety checks |
| Boundary truth | `PUBLICATION_BOUNDARY.md` | Public/private separation and product-vs-governance separation | Agent updates when public boundary changes |
| Index | `dev/PROJECT_INDEX.md` | File map, commands, and durable artifact registration | Agent updates when durable files, commands, or entrypoints change |
| Governance state | `dev/SESSION_HANDOFF.md`, `dev/SESSION_LOG.md`, `dev/DOC_SYNC_REGISTRY.md` | PUBLIC current state, trace evidence, and sync obligations | Agent updates per Agent Handoff Kit rules |
| Governance dependency reference | official Agent Handoff Kit GitHub and install page | Agent Handoff Kit runtime maintenance source only | Read only; no write-back; not product install truth |

## Tool Operation References

Use this section for project-local runbooks or verified procedures for runtime-controlled tools.

| Tool / operation | Reference path or URL | Required before | Source and version/date | Scope and known limits | Last verified |
|---|---|---|---|---|---|
| Agent Handoff Kit governance maintenance | `https://adamchanadam.github.io/agent-handoff-kit/agent-handoff-kit-ai-install.html` | changing Agent Handoff Kit generated governance files or runtime maintenance commands | official AI install page, package used v0.3.36 | Applies only to AI collaboration / governance layer; not the product package | 2026-07-05 |

## Local QC Commands

| Check | Command | Run before | Last verified |
|---|---|---|---|
| Agent Handoff Kit doctor | `npx --yes @adamchanadam/agent-handoff-kit@latest doctor --root .` | closeout / governance changes / generated Markdown artifact checks | 2026-07-05 |
| Positioning pollution scan | search public and governance docs for phrases that present Agent Handoff Kit as the product body or install target | before commit, push, release, or publishing public docs | 2026-07-05 positioning correction validated |
| Public privacy scan | search for private local paths, OPS internal paths, credentials, private knowledge-base identifiers, and unapproved outputs | before commit, push, release, or publishing public docs | 2026-07-05 |
| Public-reader pollution scan | search README and release notes for obsolete private-tool names, internal governance lists, release-operation reminders, and maintainer action-list headings such as `## 下一步` that do not belong in public product copy | before commit, push, release, or publishing public docs | 2026-07-05 |
| Project governance check | Check newly created Markdown / durable artifacts against `dev/PROJECT_INDEX.md` and `dev/DOC_SYNC_REGISTRY.md`; register, sync, consolidate, or explicitly classify as temporary / one-time evidence | closeout / durable file changes | 2026-07-05 |

## Workspace Identity

Record this at closeout so the next AI can detect wrong-root or workspace drift.

| Field | Value | Last verified |
|---|---|---|
| Expected project root | `<PUBLIC repo root>` | 2026-07-05 |
| Git root | `<PUBLIC repo root>` | 2026-07-05 |
| Branch / commit | `main` / `90ab4b3` product rename pushed | 2026-07-05 |
| Worktree or parallel workspace | PUBLIC workspace only; separate from OPS | 2026-07-05 |
| Uncommitted change summary | PUBLIC positioning correction across README, boundary docs, docs/examples/skill placeholders, and governance files | 2026-07-05 |

## Change Hotspots

| Change type | Likely files | Required checks |
|---|---|---|
| Public product positioning | `README.md`, `PUBLICATION_BOUNDARY.md`, `docs/README.md`, `examples/README.md`, `skill/README.md`, `dev/SESSION_HANDOFF.md`, `dev/PROJECT_INDEX.md` | positioning pollution scan + privacy scan + diff check |
| Public product package / CLI | future package files, `README.md`, `docs/`, `examples/`, `skill/` | product tests + public docs + privacy scan |
| Public version bump | `VERSION`, `README.md`, `PUBLICATION_BOUNDARY.md`, `dev/PROJECT_INDEX.md` Stack | version consistent across files + user-facing release notes format applied |
| Public boundary behavior | `PUBLICATION_BOUNDARY.md`, `README.md`, `docs/README.md`, `examples/README.md`, `skill/README.md` | privacy scan + no OPS data imported |
| Governance behavior | `AGENTS.md`, `dev/*` | doctor + doc sync registry |
| Generated Markdown or durable artifact | `docs/`, root Markdown files, `examples/`, `skill/` | classify as indexed / synced / temporary / one-time evidence; update `dev/PROJECT_INDEX.md` or `dev/DOC_SYNC_REGISTRY.md` when durable |
| Closeout/startup contract | `AGENTS.md`, `START_NEXT_SESSION_PROMPT.txt`, `dev/SESSION_HANDOFF.md`, `dev/SESSION_LOG.md`, `dev/PROJECT_INDEX.md` | opening message present + workspace identity current + prompt file regenerated from handoff at closeout |
| OPS-to-PUBLIC release sync | README.md, PUBLICATION_BOUNDARY.md, public product files added later | OPS candidate reviewed, private data removed, PUBLIC checks passed |
| Release or publish | README, VERSION, PUBLICATION_BOUNDARY.md, docs, GitHub release/tag/package metadata if added later | explicit user approval + privacy scan + doctor |

## External Services

| Service | Scope | Verification source | Last verified |
|---|---|---|---|
| GitHub repository `Adamchanadam/learning-knowledge-base-system` | public repo remote | `git remote -v` | 2026-07-05 |
| Agent Handoff Kit GitHub Pages install page | governance maintenance instruction source | browser read | 2026-07-05 |

## Maintenance Rule

Update this file when stack, commands, directory roles, entry points, external services, runtime-controlled tool operation references, workspace identity, durable runbooks, or governance file map changes.
