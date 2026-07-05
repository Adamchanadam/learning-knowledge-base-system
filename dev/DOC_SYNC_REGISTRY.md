# Doc Sync Registry

Purpose: map change types to documents and checks. Keep this as rows, not long prose.

## Status Vocabulary

Use: `confirmed`, `unverified`, `pending`, `blocked`, `not_applicable`.

| Change type | Also check/update | Verification |
|---|---|---|
| New file or directory | `dev/PROJECT_INDEX.md` Directory Map | path listed |
| Generated Markdown or durable artifact | `dev/PROJECT_INDEX.md` Directory Map / Fact Base / Entry Points, and this registry when future updates need sync | artifact classified as indexed / synced / temporary / one-time evidence; duplicate source-of-truth risk checked |
| Public install behavior | `README.md`, `dev/PROJECT_INDEX.md` Tool Operation References | README remains the single public source; official Agent Handoff Kit install page checked; doctor run |
| Public upgrade behavior | `README.md`, `dev/PROJECT_INDEX.md` Tool Operation References | README remains the single public source; official Agent Handoff Kit install page checked; dry-run rule preserved |
| Public boundary behavior | `PUBLICATION_BOUNDARY.md`, `README.md`, `docs/README.md`, `examples/README.md`, `skill/README.md` | privacy scan confirms no OPS/private data imported |
| Stack or command change | `dev/PROJECT_INDEX.md` Stack / Entry Points / Tool Operation References | command verified or marked unverified |
| Public behavior change | README, public docs, PUBLICATION_BOUNDARY.md release notes format | docs mention current behavior |
| Public version bump | `VERSION`, `README.md`, `PUBLICATION_BOUNDARY.md`, `dev/PROJECT_INDEX.md` Stack | same version appears in all version-bearing public surfaces; release notes use fixed user-benefit format |
| API or SDK behavior change | API docs, examples, tests | tests or documented reason |
| Runbook change | runbook path in `PROJECT_INDEX.md` | procedure still executable |
| Governance rule change | relevant pack/core, registry, README if public-facing | complexity budget checked |
| Closeout/startup contract change | `AGENTS.md`, `dev/SESSION_HANDOFF.md`, `dev/SESSION_LOG.md`, `dev/PROJECT_INDEX.md`, README quick usage | opening message schema + workspace identity present |
| Workspace identity change | `dev/SESSION_HANDOFF.md`, `dev/PROJECT_INDEX.md` | root/branch/commit/status recorded or marked unverified |
| OPS-to-PUBLIC release sync | README.md, PUBLICATION_BOUNDARY.md, affected public product files | OPS candidate classified; private/internal material removed; PUBLIC doctor/privacy/diff checks pass |
| Release | release notes, README version, VERSION, PUBLICATION_BOUNDARY.md | release pack checklist; explicit user authorization required |

## Registry Rule

If a change has no matching row, add a row before closeout or record why no durable sync rule is needed. At closeout, record sync status for every row touched by the session.
