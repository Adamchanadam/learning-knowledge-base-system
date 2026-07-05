# Doc Sync Registry

Purpose: map change types to documents and checks. Keep this as rows, not long prose.

## Status Vocabulary

Use: `confirmed`, `unverified`, `pending`, `blocked`, `not_applicable`.

| Change type | Also check/update | Verification |
|---|---|---|
| New file or directory | `dev/PROJECT_INDEX.md` Directory Map | path listed |
| Generated Markdown or durable artifact | `dev/PROJECT_INDEX.md` Directory Map / Fact Base / Entry Points, and this registry when future updates need sync | artifact classified as indexed / synced / temporary / one-time evidence; duplicate source-of-truth risk checked |
| Public product positioning | `README.md`, `PUBLICATION_BOUNDARY.md`, `docs/README.md`, `examples/README.md`, `skill/README.md`, `dev/SESSION_HANDOFF.md`, `dev/PROJECT_INDEX.md` | public docs describe `個人知識與品味脈絡系統` as the product; Agent Handoff Kit appears only as underlying AI collaboration / governance layer |
| Public product package or 命令列入口 behavior | `README.md`, `docs/`, `examples/`, `skill/`, 套件中繼資料 when added, `dev/PROJECT_INDEX.md` | commands install or run 個人知識與品味脈絡系統 itself; dependency docs do not become product docs |
| Public boundary behavior | `PUBLICATION_BOUNDARY.md`, `README.md`, `docs/README.md`, `examples/README.md`, `skill/README.md` | privacy scan confirms no OPS/private data imported; positioning scan confirms no governance layer is presented as product body |
| Stack or command change | `dev/PROJECT_INDEX.md` Stack / Entry Points / Tool Operation References | command verified or marked unverified |
| Public behavior change | README, public docs, PUBLICATION_BOUNDARY.md 發佈說明s format | docs mention current behavior |
| Public version bump | `VERSION`, `README.md`, `PUBLICATION_BOUNDARY.md`, `dev/PROJECT_INDEX.md` Stack | same version appears in all version-bearing public surfaces; 發佈說明s use fixed user-benefit format |
| API or SDK behavior change | API docs, examples, tests | tests or documented reason |
| Runbook change | runbook path in `PROJECT_INDEX.md` | procedure still executable |
| Governance rule change | relevant pack/core, registry, README if public-facing | complexity budget checked |
| Closeout/startup contract change | `AGENTS.md`, `dev/SESSION_HANDOFF.md`, `dev/SESSION_LOG.md`, `dev/PROJECT_INDEX.md`, `START_NEXT_SESSION_PROMPT.txt` | opening message schema + workspace identity present + prompt mirrors handoff |
| Workspace identity change | `dev/SESSION_HANDOFF.md`, `dev/PROJECT_INDEX.md` | root/branch/commit/status recorded or marked unverified |
| OPS-to-PUBLIC release sync | README.md, PUBLICATION_BOUNDARY.md, affected public product files | OPS candidate classified; private/internal material removed; PUBLIC doctor/privacy/positioning/diff checks pass |
| Release | 發佈說明s, README version, VERSION, PUBLICATION_BOUNDARY.md | release pack checklist; explicit user authorization required |

## Registry Rule

If a change has no matching row, add a row before closeout or record why no durable sync rule is needed. At closeout, record sync status for every row touched by the session.
