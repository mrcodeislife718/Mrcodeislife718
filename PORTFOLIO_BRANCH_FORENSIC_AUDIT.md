# Portfolio Branch Forensic Audit

**Started:** 2026-08-22

This is the canonical branch-aware audit for the active portfolio. JiffyLaundry is excluded from the active portfolio by owner directive.

## Why this exists

The earlier scoreboard was default-branch biased. It remains a provisional evidence snapshot until each repository has passed this audit. No multi-branch repository may be declared incomplete, production-ready, or commercially mature from the default branch alone.

## Required audit sequence

For every active repository:

1. Identify the actual default/canonical branch.
2. Enumerate every branch.
3. Compare each non-canonical branch against the canonical branch.
4. Record ahead/behind/diverged ancestry.
5. Identify unique implementation, tests, failure tests, benchmarks, security, deployment, operations, billing, analytics, and commercial evidence.
6. Distinguish stale/absorbed branches from unique recovery candidates.
7. Detect overlapping/divergent feature lines that need reconciliation.
8. Decide preserve / merge / cherry-pick / archive / delete-after-verification.
9. Run the canonical verification suite after reconciliation.
10. Only then update `PORTFOLIO_SCOREBOARD.md`.

## Branch classifications

- **SINGLE** — only the canonical branch exists; branch-recovery audit complete.
- **ABSORBED** — non-canonical branch is behind canonical with no unique commits.
- **UNIQUE** — branch is ahead with unique work and canonical is not ahead.
- **DIVERGED** — both branch and canonical contain unique commits; requires reconciliation.
- **FIX** — small targeted repair branch; inspect before deciding whether already superseded.
- **RECOVERY-CANDIDATE** — substantial unique implementation/proof is stranded off canonical.
- **STAGED-LADDER** — multiple branches may represent sequential capability generations; compare branch-to-branch as well as against canonical.

## Inventory status

The active portfolio branch inventory has been completed. Repositories with only one branch can be audited directly on their canonical branch; multi-branch repositories are undergoing ancestry comparison.

### Confirmed single-branch repositories

applied-ai-erp-agent, Bio-Gene-v.1.0, Cannon-Plus, cli-calculator, cli-expense-tracker, cli-todo-app, Concord, cradleos-v0, Einstein, Hired-Ai, IPX, Knowledge-Base-Ai, Measure, No-Cap, Nova, Parallel, phmf-v1-, Syncio, Teamwork-Data, Teamwork-Release, Teamwork-Test. `skill-x` is also single-branch but uses `master` rather than `main`.

### Confirmed multi-branch repositories

Axion, Boop, Branded, Cadence-, Cannon, Chronos, Codeable, Cognified, Cortex, Dev-Zero-, ECA-1-, Epiphany-, Focus, G.A.I.A, GigFlow, J.A.R.V.I.S, JobFlow-, Maestro, Muze, Nearby, OverDrive, Plasma, Prism, Scout, Sessions-, Sprout, The-Vigilante-, VaultRam, Velocity, Watchable, WorkForce-.

## Verified high-impact findings so far

### Sessions

`launch/sessions-production` is DIVERGED: **401 commits ahead / 4 behind main**. It contains major unique production work including CI and commercial qualification workflows, auth/billing/Stripe, API/runner/CLI/MCP/desktop/mobile/web surfaces, hosted repository services, PostgreSQL production migrations, Docker production topology, backup/restore/rollback/deploy scripts, SLO/config checks, tenancy/team-auth qualification, native collaboration, security tests, billing/lifecycle qualification, and recovery scoring. This is a major RECOVERY-CANDIDATE.

`test/runtime-integration` is also DIVERGED: **132 commits ahead / 4 behind main**, containing a substantial earlier integrated runtime line. It must be compared against `launch/sessions-production` to determine subsumption and any unique tests/assets.

### Codeable

`codeable-production-completion` is DIVERGED: **83 commits ahead / 9 behind main**. It includes production CI, production gate, agent-core, executor and tool registry hardening, MCP, memory, repo indexer, safety, LLM routing, computer-use, voice, autoresearch, dashboard, command runtime, and broad test coverage. This is a major RECOVERY-CANDIDATE.

`codeable-end-to-end-builder-complete` and `codeable-auto-repair-runtime` are already behind main with no unique commits, showing that branch names cannot be used as maturity evidence without ancestry comparison.

### JobFlow

`launch/jobflow-production` is ABSORBED/STALE: 0 ahead / 5 behind main.

`agent/production-app` is DIVERGED: **13 ahead / 4 behind main**, with receptionist, reminders, waitlist, web handler, recovery and restart tests.

`commercial/reliability-hardening` is DIVERGED: **15 ahead / 4 behind main**, adding the production-app work plus store concurrency hardening. This is currently the stronger recovery candidate.

`implementation/core-runtime` is DIVERGED but small: **1 ahead / 5 behind main**.

### WorkForce

`feature/universal-digital-employee-deployment` is DIVERGED: **150 ahead / 7 behind main**. It contains connectors, credential/network controls, deployment tokens, runtime jobs, approvals, billing, subscriptions, telemetry, capability broker/job runner, deployment service, store catalog, authentication, purchase flow, deployment wizard, connections UI, migrations and CI. This is a major RECOVERY-CANDIDATE.

### MUZE

`build/commercial-foundation` is DIVERGED: **164 ahead / 4 behind main**. It contains rights/identity, DDEX, royalty and settlement logic, billing/provider normalization, monetization, reporting, resilience, security, media pipelines, consumer streaming, artist migration, paid-beta/completion gates, extensive tests, Prisma schema/migrations, Docker, API/web surfaces and commercial/legal operating documentation. This is a major RECOVERY-CANDIDATE.

### Watchable

`launch/watchable-tv` is DIVERGED: **43 ahead / 4 behind main**. It includes Docker/compose, auth, billing, database, ingest, DVR, content-package configuration, web/mobile/TV/streamer surfaces, go-live/security/commercial docs and verification workflow. This is a recovery candidate, but many UI/client files are still thin and must not be mistaken for production completeness.

### OverDrive / Prism / VaultRam

Each `launch/production` branch is behind main with no unique commits (0 ahead / 4 behind). Their current missing benchmark/proof work is not hiding in those branches.

## Scoreboard rule during audit

Until a multi-branch repository has completed ancestry comparison and reconciliation planning, its existing scoreboard values are **provisional**. Evidence found on a non-canonical branch may raise the demonstrated maturity of the asset but does not automatically make the canonical release production-ready. Branch recovery and canonicalization are separate gates.

## Reconciliation safety rule

No large recovery branch will be force-merged blindly. We first determine which branch is the latest coherent line, compare overlapping branches, preserve unique evidence, run tests, then merge/cherry-pick into a canonical release branch. Stale branches are only candidates for archival/deletion after their useful history is proven preserved.
