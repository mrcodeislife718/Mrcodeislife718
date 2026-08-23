# Portfolio Branch Recovery Plan

**Derived from:** `PORTFOLIO_BRANCH_FORENSIC_AUDIT.md`  
**Rule:** recover existing work before rebuilding missing capabilities.

## Release gate

A recovery candidate is not merged directly into `main`. For each repo:

`dominant branch -> reconciliation branch -> preserve canonical-only commits -> preserve parallel unique work -> install/run verification -> fix failures -> benchmark/security/deploy gates -> promote canonical -> archive absorbed branches`

A branch with a production-sounding name is not trusted because of its name. A branch is promoted only after its ancestry, unique files, tests, and operational evidence are verified.

## Tier A — dominant cumulative branches

These repos have a clear strongest source branch and should be canonicalized first.

| Repo | Dominant source | Why | Pre-promotion gate |
|---|---|---|---|
| Sessions- | `launch/sessions-production` | 401 commits ahead of main and directly subsumes all three other non-main lines | reconcile 4 main-only commits; typecheck/build; native/commercial/API/runner/security tests; Postgres qualification; billing/tenancy/auth/native-collaboration qualification; deploy/backup/restore/rollback/SLO checks |
| JobFlow- | `commercial/reliability-hardening` | fully contains `agent/production-app` and adds concurrency hardening | app/receptionist/reminder/waitlist/restart/recovery/concurrency tests; reconcile 4 main-only commits |
| WorkForce- | `agent/market-control-plane` | fully contains dynamic store and universal deployment, then adds policy/checkpoint/outcome/economics/control-plane work | reconcile 7 main-only commits; inspect premium-store parallel UX; runtime/policy/auth/billing/connectors/deployment/telemetry/recovery tests |
| Codeable | `codeable-production-completion` | only major unique Codeable line; 15 other non-main branches are absorbed | reconcile 9 main-only commits; full production gate, agent/executor/MCP/memory/indexer/safety/LLM/computer-use/voice/autoresearch/smoke tests |
| Muze | `build/commercial-foundation` | 164 commits of rights, DDEX, royalties, settlement, provider, media, consumer and commercial completion work | reconcile 4 main-only commits; rights/identity/DDEX/royalty/settlement/provider/security/resilience/monetization/paid-beta tests; migration integrity |
| Watchable | `launch/watchable-tv` | 43 unique product/deployment commits | reconcile 4 main-only commits; preserve brand asset; replace/verify thin clients; auth/billing/db/content-ingest/DVR/streaming/deployment tests |
| Axion | `agent/production-app` | strongest unique registry/product line | reconcile 4 main-only commits; auth/passport/service/store/application tests |
| G.A.I.A | `implementation/core-runtime-v1` | unique Python autonomous runtime + execution protocol + tests | reconcile 6 main-only commits; Python package/tests; causal baseline experiments after canonicalization |
| GigFlow | `agent/production-app` | unique service/store/http/web/estimates product line | reconcile 4 main-only commits; application/estimate tests and production hardening |

## Tier B — synthesis repositories

These cannot safely be recovered by promoting one branch.

### J.A.R.V.I.S

Build a clean synthesis candidate preserving:

1. governed core;
2. persistent PKM;
3. infrastructure administration;
4. governed analytics;
5. business/content operations;
6. customer support;
7. biomedical research;
8. migrations and integration tests from every stage.

The staged branch contents are increasingly cumulative, but their Git histories diverge. Validate database migration order, route registration, shared context/compiler behavior, security boundaries, and integration tests after each capability tranche.

### Epiphany-

Build a controlled research synthesis candidate. Preserve and independently validate unique mechanisms from:

- Aquarius foundation / continuity / bounded execution;
- production hardening;
- capability-development runtime;
- continuous-development runtime and developmental ledgers;
- depth/autonomy/evolution mechanisms;
- native-development completion / coherence;
- developmental closure;
- developmental constitution / closed-loop branch.

Do not infer AGI or general intelligence from branch names or architecture. Promotion requires regression, governance/authority, capability-preservation, adversarial, and empirical developmental tests.

## Tier C — selective recovery

- Cannon — reconcile language-core semantic/parser/compiler/lexer changes and tests.
- Scout — reconcile universal-interop parser/tokenizer/language-service/spec changes and tests.
- ECA-1- — reconcile strict type/recovery/deployment/hardware fixes and tests.
- Cognified — reconcile portable test-runner fix if still needed.
- Cadence- — inspect one tiny unique runtime commit; preserve only if not superseded.
- Velocity — inspect one tiny unique runtime commit; preserve only if not superseded.
- WorkForce premium-store branch — preserve only unique approved UX/presentation work not already represented by market-control-plane.
- Watchable brand branch — preserve brand asset/documentation if desired.

## Tier D — absorbed branch cleanup

No feature recovery is required from the checked non-canonical branches of:

Boop, Branded, Chronos, Cortex, Dev-Zero-, Focus, Maestro, Nearby, OverDrive, Plasma, Prism, Sprout, The-Vigilante-, VaultRam.

Their stale branches may be archived/deleted only after canonical history and any tags/releases are checked. Their remaining completion gaps must be solved on the canonical branch rather than rebuilt from those stale branches.

## Single-branch repos

applied-ai-erp-agent, Bio-Gene-v.1.0, Cannon-Plus, cli-calculator, cli-expense-tracker, cli-todo-app, Concord, cradleos-v0, Einstein, Hired-Ai, IPX, Knowledge-Base-Ai, Measure, No-Cap, Nova, Parallel, phmf-v1-, Syncio, Teamwork-Data, Teamwork-Release, Teamwork-Test, and skill-x (`master`).

These bypass branch recovery and proceed directly to canonical evidence-gap closure.

## Scoreboard interaction

The current scoreboard remains conservative until recovery candidates are canonicalized. Once a candidate passes its release gate:

1. update `PORTFOLIO_PROOF.md` and `evidence/claims.json` in that repo;
2. point claims to exact tests/benchmarks/deployments;
3. promote only supported gates in `PORTFOLIO_SCOREBOARD.md`;
4. then continue external proof: deployment, users, payment, retention, measurable superiority and acquisition.

## Definition of branch-audit completion

The branch audit is complete when every repo is in one of four states:

- single/canonical only;
- absorbed branches only;
- recovery branch identified with release gate;
- synthesis plan defined for genuinely parallel development.

That state is now established portfolio-wide. The next operation is canonicalization and verification, not another shallow inventory.
