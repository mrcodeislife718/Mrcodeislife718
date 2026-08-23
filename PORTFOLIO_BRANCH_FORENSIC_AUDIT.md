# Portfolio Branch Forensic Audit

**Started:** 2026-08-22  
**Ancestry pass:** COMPLETE across the active portfolio  
**Scope:** 53 active project repositories. JiffyLaundry is excluded by owner directive.

## Purpose

The earlier portfolio scoreboard was default-branch biased. This audit corrects that by treating the repository as the union of its reachable development branches, then separating **asset maturity** from **canonical-release maturity**.

A capability found on a non-default branch counts as existing engineering work, but it does not make `main` production-ready until that work is reconciled, verified, and promoted to the canonical release line.

## Permanent audit sequence

Before building a capability that appears missing:

1. Identify the actual canonical/default branch (`skill-x` currently uses `master`; most others use `main`).
2. Enumerate every branch.
3. Compare every non-canonical branch with the canonical branch.
4. Record ancestry: ahead, behind, diverged, or equal.
5. Identify unique implementation, tests, failure tests, benchmarks, security, deployment, operations, billing, analytics, and commercial evidence.
6. Compare overlapping branches directly when branch-vs-main is insufficient.
7. Classify each branch as absorbed, selective-recovery, major-recovery, staged/parallel research, or archive candidate.
8. Preserve unique work before deleting or rebuilding anything.
9. Reconcile onto a clean candidate release branch.
10. Run the repository's complete verification, failure, security, benchmark, and deployment gates.
11. Promote only verified work to the canonical branch.
12. Update `PORTFOLIO_SCOREBOARD.md` only from the reconciled evidence.

## Branch classifications

- **SINGLE** — only the canonical branch exists; branch-recovery audit is complete.
- **ABSORBED** — branch is behind canonical with no unique commits.
- **SELECTIVE** — small unique fix/capability should be cherry-picked or manually reconciled after verification.
- **RECOVERY-CANDIDATE** — substantial implementation/proof is stranded off canonical.
- **CUMULATIVE** — one branch demonstrably contains the useful history of earlier development branches.
- **PARALLEL/STAGED** — multiple branches contain non-subsumed capability lines and require a synthesis branch.

## Branch inventory

### Single-branch repositories

applied-ai-erp-agent, Bio-Gene-v.1.0, Cannon-Plus, cli-calculator, cli-expense-tracker, cli-todo-app, Concord, cradleos-v0, Einstein, Hired-Ai, IPX, Knowledge-Base-Ai, Measure, No-Cap, Nova, Parallel, phmf-v1-, Syncio, Teamwork-Data, Teamwork-Release, Teamwork-Test. `skill-x` is also single-branch but its canonical branch is `master`.

These repos have no hidden branch implementation to recover; remaining gaps must be searched on the canonical branch or built/proven anew.

### Multi-branch repositories

Axion, Boop, Branded, Cadence-, Cannon, Chronos, Codeable, Cognified, Cortex, Dev-Zero-, ECA-1-, Epiphany-, Focus, G.A.I.A, GigFlow, J.A.R.V.I.S, JobFlow-, Maestro, Muze, Nearby, OverDrive, Plasma, Prism, Scout, Sessions-, Sprout, The-Vigilante-, VaultRam, Velocity, Watchable, WorkForce-.

Every non-canonical branch above has now been compared against the canonical branch. High-impact overlapping branches have also received direct branch-to-branch lineage checks.

## Recovery map

| Project | Forensic result | Recovery source / unique branch | Required action |
|---|---|---|---|
| Sessions- | **Major CUMULATIVE recovery** | `launch/sessions-production` — 401 ahead / 4 behind `main`; directly contains `test/runtime-integration`, `fix/native-repository-async-default`, and `fix/repository-hygiene` | Build a release/reconciliation branch from the production line, incorporate the 4 canonical-only commits, run full production/commercial/security/recovery qualification, then promote |
| Codeable | **Major recovery** | `codeable-production-completion` — 83 ahead / 9 behind `main` | Reconcile this one branch with canonical; 15 other non-main branches checked are already absorbed and become archive candidates after verification |
| JobFlow- | **CUMULATIVE recovery** | `commercial/reliability-hardening` — 15 ahead / 4 behind `main`; 2 commits ahead of and fully contains `agent/production-app` | Reconcile reliability-hardening with canonical; preserve receptionist/reminders/waitlist/recovery plus concurrency hardening; rerun application/restart/concurrency tests |
| WorkForce- | **Major CUMULATIVE recovery + one parallel UX line** | `agent/market-control-plane` — 172 ahead / 7 behind `main`; fully contains dynamic-store → universal-deployment and adds 22 control/economics commits | Use market-control-plane as primary recovery source; separately inspect/preserve unique premium-store UX commits before canonicalization; verify runtime, policy, billing, deployment, auth, telemetry and recovery |
| Muze | **Major recovery** | `build/commercial-foundation` — 164 ahead / 4 behind `main` | Reconcile commercial foundation with canonical; run rights/DDEX/royalty/settlement/security/monetization/provider/paid-beta/production-readiness tests before promotion |
| Watchable | **Major recovery** | `launch/watchable-tv` — 43 ahead / 4 behind `main` | Reconcile launch branch; preserve separate brand asset if desired; verify real auth/billing/content ingest/DVR/deployment paths and replace thin client placeholders before claiming production completion |
| Axion | **Recovery candidate** | `agent/production-app` — 11 ahead / 4 behind `main` | Reconcile auth/passport/service/store/web/tests; older launch/core-registry branches are stale or tiny |
| G.A.I.A | **Recovery candidate** | `implementation/core-runtime-v1` — 5 ahead / 6 behind `main` | Reconcile Python autonomous runtime/execution protocol/CLI/tests; older core-runtime branch is absorbed |
| GigFlow | **Recovery candidate** | `agent/production-app` — 11 ahead / 4 behind `main` | Reconcile service/store/http/web/estimates/tests; older core-runtime branch is absorbed |
| J.A.R.V.I.S | **Major PARALLEL/STAGED recovery** | v0.1–v0.7 build branches | Do not promote a branch pointer. Synthesize a clean candidate that preserves governed core + PKM + infrastructure admin + analytics + business/content + customer support + biomedical modules and all migrations/tests; branch contents are increasingly cumulative, but Git history is divergent |
| Epiphany- | **Major PARALLEL research synthesis** | capability-development, continuous-development, production-hardening, Aquarius foundation/autonomy/native-completion, developmental-closure, developmental-constitution | Do not choose one branch as “the winner.” Create a synthesis branch, port unique mechanisms in dependency order, run regression/authority/governance/development validations after each tranche, and treat AGI/capability claims as unproven until empirical evidence exists |
| Cannon | **SELECTIVE recovery** | `agent/cannon-language-core` — 7 ahead / 14 behind `main` | Reconcile semantic analyzer/parser/compiler/lexer changes and tests selectively |
| Scout | **SELECTIVE recovery** | `agent/scout-universal-interop` — 26 ahead / 24 behind `main` | Reconcile parser/tokenizer/language-service/spec changes and tests; verify compatibility against current main |
| ECA-1- | **SELECTIVE repair** | `fix/strict-types` — 1 ahead / 5 behind `main` | Reapply/verify strict typing fixes across deployment/hardware/recovery/integration and tests |
| Cognified | **SELECTIVE repair** | `fix/portable-test-runner` — 1 ahead / 5 behind `main` | Reconcile portable test-runner package change if still needed |
| Cadence- | **SELECTIVE tiny recovery** | `implementation/runtime-v1` — 1 ahead / 17 behind `main` | Inspect tiny runtime/test delta; preserve only if current main lacks equivalent behavior |
| Velocity | **SELECTIVE tiny recovery** | `implementation/runtime-v1` — 1 ahead / 22 behind `main` | Inspect tiny runtime/test delta; preserve only if not superseded |
| Boop | **ABSORBED** | implementation branch 0 ahead / 4 behind | No branch recovery required |
| Branded | **ABSORBED** | runtime branch 0 ahead / 4 behind | No branch recovery required |
| Chronos | **ABSORBED** | runtime branch 0 ahead / 17 behind | No branch recovery required |
| Cortex | **ABSORBED** | runtime branch 0 ahead / 16 behind | No branch recovery required |
| Dev-Zero- | **ABSORBED** | core-runtime branch 0 ahead / 4 behind | No branch recovery required |
| Focus | **ABSORBED** | launch branch 0 ahead / 4 behind | No branch recovery required; benchmark/proof gap is real on canonical |
| Maestro | **ABSORBED** | launch branch 0 ahead / 4 behind | No branch recovery required; benchmark/proof gap is real on canonical |
| Nearby | **ABSORBED** | runtime branch 0 ahead / 4 behind | No branch recovery required |
| OverDrive | **ABSORBED** | launch branch 0 ahead / 4 behind | No branch recovery required; integrated empirical benchmark remains a real gap |
| Plasma | **ABSORBED** | runtime branch 0 ahead / 14 behind | No branch recovery required |
| Prism | **ABSORBED** | launch branch 0 ahead / 4 behind | No branch recovery required; packed-execution/resource benchmark remains a real gap |
| Sprout | **ABSORBED** | runtime branch 0 ahead / 17 behind | No branch recovery required |
| The-Vigilante- | **ABSORBED** | production-tracker branch 0 ahead / 4 behind | No branch recovery required |
| VaultRam | **ABSORBED** | launch branch 0 ahead / 4 behind | No branch recovery required; oversized-workload/tiering benchmark remains a real gap |

## Major findings

### 1. The portfolio is materially more implemented than the default branches suggested

The largest understated assets are Sessions, Codeable, WorkForce, MUZE, Watchable, J.A.R.V.I.S, Epiphany, JobFlow, Axion, G.A.I.A and GigFlow. Substantial implementation, tests, production infrastructure, security, billing, migrations, runtime logic, or domain logic exist outside canonical branches.

### 2. Branch sprawl is often historical rather than true parallel unfinished work

Several intimidating branch sets collapse cleanly after ancestry checks. Codeable is the clearest example: 15 of its 16 non-main branches are already fully absorbed into `main`; only `codeable-production-completion` carries major unique work. Sessions also collapses to one dominant production line because `launch/sessions-production` fully contains its older integration/fix branches.

### 3. Some repositories genuinely require synthesis rather than merge

J.A.R.V.I.S and Epiphany are the strongest examples. Their branches carry substantial overlapping capability generations with divergent Git ancestry. They need explicit synthesis, regression verification and canonicalization rather than a blind merge or branch-pointer promotion.

### 4. The OverDrive family does not have hidden benchmark work

OverDrive, Prism, VaultRam, Focus and Maestro launch branches are all stale/absorbed. Their outstanding empirical proof requirements are genuine: baseline comparisons, real resource telemetry, oversized-workload completion, quality/performance measurements and integrated ablations still need to be executed and preserved as evidence.

### 5. Canonicalization is now a first-class completion gate

A repository is not considered operationally complete while its strongest implementation is stranded hundreds of commits away from the default branch. For major recovery assets, the immediate engineering order is:

`identify dominant branch -> preserve parallel unique work -> reconcile canonical-only commits -> run full verification -> promote -> archive stale branches -> then continue proof/deployment/customer work`

## High-priority canonicalization order

1. Sessions- — dominant branch already proven to subsume older non-main lines.
2. JobFlow- — reliability-hardening cleanly supersedes production-app.
3. WorkForce- — market-control-plane is the dominant cumulative product line; preserve premium UX delta separately.
4. Codeable — one major production-completion branch, most branch noise already absorbed.
5. Muze — commercial foundation contains substantial product/legal/economic runtime work.
6. Watchable — launch line contains the real app/deployment surface but still needs implementation hardening.
7. Axion / G.A.I.A / GigFlow — smaller, bounded recovery candidates.
8. J.A.R.V.I.S — staged synthesis.
9. Epiphany- — research synthesis with regression/governance gates.
10. Cannon / Scout / ECA-1 / Cognified / Cadence / Velocity — selective recovery.

## Scoreboard rule

`PORTFOLIO_SCOREBOARD.md` remains an evidence scoreboard, but any value based only on a default-branch read must be treated as provisional for repositories listed as RECOVERY-CANDIDATE or PARALLEL/STAGED above.

Branch evidence may demonstrate that an asset exists. **Canonical release maturity is a separate gate.** A project receives production/deployment/commercial credit only after the recovered line is verified in its intended environment and the required external evidence exists.

## Reconciliation safety rule

No major branch is force-merged blindly. We preserve unique work, account for canonical-only commits, run tests and qualification gates on a candidate release line, and only then promote. Stale branches become archive/deletion candidates only after their useful history is demonstrably preserved.
