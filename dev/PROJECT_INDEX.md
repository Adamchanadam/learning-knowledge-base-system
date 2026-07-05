# Project Index

Purpose: give a stateless AI a compact map of the project before it reads or edits files.

## Stack

| Field | Value | Last verified |
|---|---|---|
| Agent Handoff Kit template version | 0.3.36 | 2026-07-05 |
| Public product version | 0.1.0 | 2026-07-05 |
| Runtime | Markdown + Agent Handoff Kit | 2026-07-05 |
| Framework | Not applicable — public documentation scaffold | 2026-07-05 |
| Package manager | npx for Agent Handoff Kit install/upgrade commands | 2026-07-05 |
| Test command | `npx --yes @adamchanadam/agent-handoff-kit@latest doctor --root .` | 2026-07-05 |
| Build command | Not applicable | 2026-07-05 |
| Deploy command | Not configured; release/deploy requires explicit authorization | 2026-07-05 |

## Directory Map

| Path | Role | Read when |
|---|---|---|
| `AGENTS.md` | primary Agent Handoff Kit entry and startup contract | session startup |
| `CLAUDE.md` | Claude Code bridge to the same startup path | Claude Code startup |
| `GEMINI.md` | Google Antigravity CLI / Gemini CLI migration bridge to the same startup path | Antigravity / Gemini startup |
| `START_NEXT_SESSION_PROMPT.txt` | auto-generated stateful startup prompt for the next local-agent session; `dev/SESSION_HANDOFF.md` remains authoritative | next session startup |
| `README.md` | public repo entrypoint, install/upgrade single source of truth, OPS-to-PUBLIC release flow, version summary, and boundary summary | public-facing docs or onboarding change |
| `VERSION` | public product version source for this repo until a package manifest exists | version bump |
| `PUBLICATION_BOUNDARY.md` | public/private boundary source of truth | before importing, publishing, syncing, or documenting content |
| `docs/README.md` | public documentation index | public docs change |
| `examples/README.md` | public examples placeholder and constraints | adding or changing examples |
| `skill/README.md` | future public skill/package placeholder and constraints | adding or changing skill package content |
| `dev/` | Agent Handoff Kit governance state for PUBLIC only | startup, closeout, governance changes |

## Entry Points

| Entry | Path | Notes |
|---|---|---|
| AI agent startup | `AGENTS.md` | Use `Start Agent Handoff` or `開工` after installation |
| Next-session prompt | `START_NEXT_SESSION_PROMPT.txt` | Convenience copy; `dev/SESSION_HANDOFF.md` remains authoritative |
| Public docs | `README.md` | Main public entrypoint |
| Boundary guide | `PUBLICATION_BOUNDARY.md` | Must be read before adding public content |
| Generated artifact review | `dev/PROJECT_INDEX.md` + `dev/DOC_SYNC_REGISTRY.md` | After creating Markdown docs, generated outputs, specs, runbooks, checklists, or research artifacts, classify each artifact as indexed / synced / temporary / one-time evidence before completion |

## Fact Base

Reachable means the source can be found. It does not mean the source has been read in this session.

| Source | Role | Required before | Access method | Last verified |
|---|---|---|---|---|
| `README.md` | public entrypoint and current public status | public docs, onboarding, install/upgrade wording, version summary | local file | 2026-07-05 |
| `VERSION` | public product version source until package metadata exists | public version bump | local file | 2026-07-05 |
| `PUBLICATION_BOUNDARY.md` | source of truth for what PUBLIC may contain | importing content, publishing, release, examples, skill packaging | local file | 2026-07-05 |
| `examples/README.md` | examples boundary placeholder | adding examples | local file | 2026-07-05 |
| `skill/README.md` | skill package boundary placeholder | adding public skill package content | local file | 2026-07-05 |

## External Sources

| Source | Role | Required before | Access method | `via` | Write-back rule | Last verified |
|---|---|---|---|---|---|---|
| `https://github.com/Adamchanadam/agent-handoff-kit` | official Agent Handoff Kit repository | changing install/upgrade claims | browser / manual web read | manual paste | no write | 2026-07-05 |
| `https://adamchanadam.github.io/agent-handoff-kit/agent-handoff-kit-ai-install.html` | official AI-readable install and upgrade page | changing install/upgrade commands | browser / manual web read | manual paste | no write | 2026-07-05 |

> `via` column discipline: every External Sources row must reference an entry name under `## Installed Integrations`, such as `Notion Connector` or `Google Drive Connector`, so the access path is explicit. Sources without a declared integration use `manual paste`. Doctor and release QA enforce cross-section consistency.

## Installed Integrations

> **Credential Separation Principle**: this section records only project usage and public reference coordinates such as Notion database names, URLs, or folder paths. It must never record API keys, OAuth tokens, or credential values. Credentials belong in AI runtime secure storage, OS credential stores, tool configuration, or user-managed secret stores. If an environment variable is used, record only the environment variable name, never the value. Before writing this section, self-check that no credential value is being persisted. Doctor scans this section, `SESSION_HANDOFF`, and `SESSION_LOG` for common credential prefixes such as `sk-`, `ntn_`, `ya29.`, `xoxp-`, `ghp_`, `sl.`, `AKIA`, and `AIza`.

> Purpose: a new AI session reads this section to understand declared external-tool capabilities and their project roles. Declarations persist across sessions. Every entry must include `Declared` and `Last Verified` fields so stale capability assumptions can be detected.

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

> When a project uses several integrations as a source-of-truth system, for example Notion index + local primary sources + Google Drive reference mirror, this table records each layer's role so agents do not cross write boundaries.

| Layer | Surface (specific instance) | Role | Write Direction |
|-------|--------------------------|------|-----------------|
| Source of truth | local PUBLIC repo files | Public docs, boundary rules, README install/upgrade guidance, and release-flow guidance | Agent may edit local files after reading boundary and with normal safety checks |
| Index | `dev/PROJECT_INDEX.md` | File map, commands, and durable artifact registration | Agent updates when durable files, commands, or entrypoints change |
| Governance state | `dev/SESSION_HANDOFF.md`, `dev/SESSION_LOG.md`, `dev/DOC_SYNC_REGISTRY.md` | PUBLIC current state, trace evidence, and sync obligations | Agent updates per Agent Handoff Kit rules |
| External reference | official Agent Handoff Kit GitHub and install page | Install/upgrade behavior source | Read only; no write-back |

## Tool Operation References

Use this section for project-local runbooks or verified procedures for runtime-controlled tools such as browser validation, screenshots, DevTools, Playwright, crawlers, notebooks, desktop app automation, MCP/plugin helpers, or raw CLI/SDK operations.

Do not store credential values or machine-private paths here. Local machine-only references may be listed only when the project explicitly depends on them, and the scope / limits must say they are not portable.

| Tool / operation | Reference path or URL | Required before | Source and version/date | Scope and known limits | Last verified |
|---|---|---|---|---|---|
| Agent Handoff Kit install/upgrade | `https://adamchanadam.github.io/agent-handoff-kit/agent-handoff-kit-ai-install.html` | changing install or upgrade commands | official AI install page, v0.3.34 page; package used v0.3.36 | AI-readable operational page; verify current page before changing commands | 2026-07-05 |
| Agent Handoff Kit package | `https://github.com/Adamchanadam/agent-handoff-kit` | changing product claims, install method, or upgrade method | official repository | Public repo; package latest may advance after this date | 2026-07-05 |

## Local QC Commands

| Check | Command | Run before | Last verified |
|---|---|---|---|
| Agent Handoff Kit doctor | `npx --yes @adamchanadam/agent-handoff-kit@latest doctor --root .` | closeout / governance changes / generated Markdown artifact checks | 2026-07-05 |
| Public privacy scan | search for private local paths, OPS internal paths, credentials, Notion IDs, and unapproved outputs | before commit, push, release, or publishing public docs | 2026-07-05 |
| Project governance check | Check newly created Markdown / durable artifacts against `dev/PROJECT_INDEX.md` and `dev/DOC_SYNC_REGISTRY.md`; register, sync, consolidate, or explicitly classify as temporary / one-time evidence | closeout / durable file changes | 2026-07-05 |

## Workspace Identity

Record this at closeout so the next AI can detect wrong-root or workspace drift.

| Field | Value | Last verified |
|---|---|---|
| Expected project root | `<PUBLIC repo root>` | 2026-07-05 |
| Git root | `<PUBLIC repo root>` | 2026-07-05 |
| Branch / commit | `main` / `c38a104 Initialize public release scaffold` | 2026-07-05 |
| Worktree or parallel workspace | PUBLIC workspace only; separate from OPS | 2026-07-05 |
| Uncommitted change summary | Agent Handoff Kit install plus README-centered public install/upgrade, OPS/PUBLIC release flow, v0.1.0 bump, and user-facing release notes format correction | 2026-07-05 |

## Change Hotspots

| Change type | Likely files | Required checks |
|---|---|---|
| Public install behavior | `README.md`, `dev/PROJECT_INDEX.md` Tool Operation References | official install page read + doctor |
| Public version bump | `VERSION`, `README.md`, `PUBLICATION_BOUNDARY.md`, `dev/PROJECT_INDEX.md` Stack | version consistent across files + user-facing release notes format applied |
| Public upgrade behavior | `README.md`, `dev/PROJECT_INDEX.md` Tool Operation References | official install page read + dry-run guidance checked |
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
| Agent Handoff Kit GitHub Pages install page | install/upgrade instruction source | browser read | 2026-07-05 |

## Maintenance Rule

Update this file when stack, commands, directory roles, entry points, external services, runtime-controlled tool operation references, workspace identity, durable runbooks, or governance file map changes.
