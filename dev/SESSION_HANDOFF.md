# Session Handoff

Last Updated: 2026-07-05

<!-- ack:section:durable-anchors -->
## Durable Anchors

Stable facts that should survive across sessions. Update only when they change, but verify they still match reality at closeout.

1. Project root and boundary: `<PUBLIC repo root>`; public-facing workspace, not an OPS mirror.
2. Product/system identity: `學習型知識庫系統 PUBLIC` v0.1.0, a public release scaffold for install, upgrade, docs, examples, and future cleaned skill packaging.
3. Governance model: Agent Handoff Kit v0.3.36 installed as the PUBLIC local agentic-AI operating layer.
4. Source-of-truth ownership: PUBLIC docs and `dev/` files describe only this public repo. OPS data, OPS handoff history, internal research outputs, private Notion data, credentials, and local private paths are excluded.
5. Release / publish boundary: commit, push, tag, release, package publish, and deploy need explicit user authorization.
6. Installed Integrations registry: `dev/PROJECT_INDEX.md` `## Installed Integrations` section is the project's authoritative declaration of installed Connectors / MCPs / Plugins / Skills + Source-of-truth Architecture sub-table. New AI session must read it after governance reads and run availability probe per `runtime-core/AGENTS.core.md` Section 1. Credential values never appear here or in any `dev/*` file — only credential references such as AI tool secure storage, OS credential store, tool config, user-managed secret store, or env var name may be recorded.

<!-- ack:section:closeout-reconciled-state -->
## Closeout-Reconciled State

This is the current-state area. At every full closeout, rewrite or explicitly confirm every section below. Do not append a new state snapshot under an old one.

<!-- ack:section:current-baseline -->
## Current Baseline

1. Project root: `<PUBLIC repo root>`.
2. Product/system state: public release scaffold with Agent Handoff Kit bottom layer installed; not yet a complete public product release.
3. Governance state: Agent Handoff Kit v0.3.36 installed; public docs now define install, upgrade, and boundary rules.
4. Source-of-truth notes: `README.md` is the single public truth for install/upgrade behavior; `PUBLICATION_BOUNDARY.md` is the public/private boundary and OPS-to-PUBLIC release-flow truth.

<!-- ack:section:task-understanding-summary -->
## Task Understanding Summary

<!-- ack:field:user-intent -->
- User intent: Make the PUBLIC repo easy for users to install and upgrade through agentic AI, using the same Agent Handoff Kit bottom mechanism as OPS without importing OPS data.
<!-- ack:field:task-essence -->
- Task essence: Fresh-install Agent Handoff Kit into PUBLIC, then document user-facing install and upgrade flows.
- User value: A public repo that can be operated by AI agents consistently across sessions without exposing private OPS material.
<!-- ack:field:success-criteria -->
- Success criteria: PUBLIC has Agent Handoff Kit files, README-based install/upgrade guidance, OPS-to-PUBLIC release-flow guidance, v0.1.0 version bump, and user-facing changelog, registered durable artifacts, passing doctor, and a private-data scan showing no leaked OPS/private content beyond boundary warnings.
- Key background already read: PUBLIC `README.md`, `PUBLICATION_BOUNDARY.md`, `docs/README.md`, official Agent Handoff Kit GitHub repo, official AI install page.
- Background still unread or blocked: none for current integration; future product docs and examples still need design.
- Non-goals / boundaries: Do not copy OPS `dev/`, `outputs/`, session logs, internal decisions, private Notion identifiers, credentials, local private paths, or unlicensed third-party material into PUBLIC.

<!-- ack:section:active-objective -->
## Active Objective

Run final health checks and prepare PUBLIC changes for a commit decision.

<!-- ack:section:completed-this-session -->
## Completed This Session

Record only work actually completed in the current session.

1. PUBLIC current-state governance and public documentation updates are recorded. Detailed trace evidence is in `dev/SESSION_LOG.md`.

<!-- ack:section:next-priorities -->
## Next Priorities

Recommended next step: after this authorized commit and push, continue with the first public product/package structure decision — reason: tag, GitHub release, npm publish, and deploy are still separate release actions.

1. Commit and push the authorized PUBLIC v0.1.0 changes.\r\n2. Do not tag, create a GitHub release, publish to npm, or deploy without separate explicit user authorization.\r\n3. Next product step: decide the first public package structure and user-facing minimum viable example.

<!-- ack:section:next-task-required-reading -->
## Next Task Required Reading

Before acting on the next task, read or mark blocked:

| Source | Why required | Status |
|---|---|---|
| `PUBLICATION_BOUNDARY.md` | Defines what PUBLIC may and may not contain | required |
| `README.md` | Public user entrypoint, install/upgrade single source, OPS/PUBLIC role split, release sync flow, and version summary | required |
| `CHANGELOG.md` | User-facing Traditional Chinese release notes | required before public release notes or version bump |
| `VERSION` | Public product version source until package metadata exists | required before version bump |
| `dev/PROJECT_INDEX.md` | PUBLIC file map and governance registry | required before file changes |
| `dev/DOC_SYNC_REGISTRY.md` | Sync obligations for docs, governance, and release boundaries | required before file changes or closeout |

<!-- ack:section:risks-blockers -->
## Risks / Blockers

1. Main risk: accidentally importing OPS data or private local material into PUBLIC.
2. Release risk: installing/upgrading Agent Handoff Kit is not authorization to push, tag, release, package publish, or deploy.
3. Documentation risk: user-facing install/upgrade guidance must stay aligned with the official Agent Handoff Kit install page.

<!-- ack:section:validation-qc -->
## Validation / QC

- Checks run this session: initial doctor after install ran and correctly flagged unregistered durable docs; follow-up validation pending after governance updates.
- Checks not run and why: final doctor and privacy scan pending until all docs/index updates are complete.
- Handoff evidence location: this file and `dev/SESSION_LOG.md` current entry.

<!-- ack:section:workspace-identity -->
## Workspace Identity

Expected project root: `<PUBLIC repo root>`
Git root: `<PUBLIC repo root>`
Branch: `main`
Commit: `c38a104 Initialize public release scaffold`
Worktree / parallel workspace status: PUBLIC root only; separate from OPS workspace.
Uncommitted changes summary: Agent Handoff Kit fresh install plus README-centered public install/upgrade, OPS/PUBLIC role split, release-flow governance updates, v0.1.0 bump, and changelog.

<!-- ack:section:sync-status -->
## Sync Status

Use statuses from `dev/DOC_SYNC_REGISTRY.md`: `confirmed`, `unverified`, `pending`, `blocked`, `not_applicable`.

- Project index: pending final validation.
- Doc sync registry: pending final validation.
- Public docs / README: pending final validation.
- External knowledge tools: not_applicable.

<!-- ack:section:state-reconciliation-check -->
## State Reconciliation Check

At full closeout, complete this check after updating the state sections below.

- Reconciled at: pending full closeout
<!-- ack:field:state-sections-rewritten-or-confirmed -->
- State sections rewritten or confirmed current: current sections updated for PUBLIC integration during active task; full closeout pending.
<!-- ack:field:stale-snapshots-left -->
- Stale snapshots left in this handoff: no known stale snapshot after current update.
<!-- ack:field:lifecycle-conflicts-resolved -->
- Completed / pending / risk / opening-message lifecycle conflicts resolved or explicitly reclassified: yes; completed work is recorded as current state and trace evidence, and this turn is authorized to commit and push PUBLIC main.
<!-- ack:field:persistence-routing-checked -->
- Persistence routing checked: public docs in `README.md`, `PUBLICATION_BOUNDARY.md`, and `docs/`; current state in this handoff; trace evidence in `dev/SESSION_LOG.md`; file map in `dev/PROJECT_INDEX.md`.
<!-- ack:field:recommended-next-step-explicit -->
- Recommended next step is explicit and reasoned: yes, run final checks and diff review before commit.
<!-- ack:field:opening-message-matches-current-state -->
- Opening message matches current state: yes, mirrored to `START_NEXT_SESSION_PROMPT.txt` during this task.
<!-- ack:field:next-ai-can-continue -->
- Next AI can continue from `AGENTS.md`, this handoff, `dev/PROJECT_INDEX.md`, and needed rule packs without searching old log history: yes.

If any answer is no, blocked, or uncertain, fix this handoff before declaring handoff ready.

Lifecycle consistency rule: compare `Completed This Session`, `Validation / QC`, `Next Priorities`, `Risks / Blockers`, and `Next Session Opening Message`. A completed or verified item must not remain as an unresolved next priority, active risk, or startup instruction unless it is explicitly reclassified as monitor-only, follow-up scope, blocked, or reopened with the missing evidence or trigger condition stated. Recommended next-step rule: `Next Priorities` must name the single recommended next action and a short reason before listing additional options, unless the next action is blocked or genuinely requires a user decision. Persistence routing rule: one-time delivery instructions, historical validation evidence, old hashes, old version facts, and incident notes must stay in trace evidence unless they still affect the next action.

<!-- ack:section:handoff-sufficiency-check -->
## Handoff Sufficiency Check

Can the next AI continue from `AGENTS.md`, this handoff, `dev/PROJECT_INDEX.md`, and needed rule packs without searching old log history?

Answer: yes.
If no, update this handoff before closeout.

Continuity rule: this file carries current state and next action. `dev/SESSION_LOG.md` carries recent evidence only. Archive old detail only when needed; do not create an archive directory by default.

<!-- ack:section:next-session-opening-message -->
## Next Session Opening Message

This fenced block is the authoritative agent-managed startup content. At closeout, regenerate `START_NEXT_SESSION_PROMPT.txt` from this block. If the two differ, trust this block and rewrite the convenience copy. User-facing closeout output should show `Start Agent Handoff` / `開工` as the primary next-session entry, plus the path-bearing fallback when the next AI is not yet pointed at this project root; do not hand-write a separate stateful prompt in the final response.

📋 Next session: agent-managed startup content below

```text
Work in <PUBLIC repo root>.

Read in order:
1. AGENTS.md
2. dev/SESSION_HANDOFF.md
3. dev/SESSION_LOG.md
4. dev/PROJECT_INDEX.md
5. dev/RULE_PACKS.md

Read dev/DOC_SYNC_REGISTRY.md before file changes or closeout.

If this root does not match the expected project root, stop and ask for confirmation.

Current state: PUBLIC repo is at public product version v0.1.0 and uses Agent Handoff Kit v0.3.36 as its local agentic-AI operating layer. This repo is public-facing and must not import OPS data, OPS handoff history, internal research outputs, private Notion data, local private paths, credentials, or unlicensed third-party material.

Recommended next step: after the authorized commit and push, decide the first public package structure and minimum viable public example. Do not tag, create a GitHub release, publish to npm, or deploy without separate explicit user authorization.
```
