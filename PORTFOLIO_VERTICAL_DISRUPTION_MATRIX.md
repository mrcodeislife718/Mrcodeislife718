# Portfolio Vertical Disruption Matrix

This file is the market/strategic operating layer paired with `PORTFOLIO_SCOREBOARD.md`.

The scoreboard answers **what is proven now**. This matrix answers **what advantage each asset must prove next**.

A disruption claim is never inferred from ambition. It requires a baseline, a measurable superiority target, and eventually adoption evidence.

## Priority closure tranche

| Project | Buyer / user | Incumbent / current workflow | Valuable weakness to attack | Measurable superiority target | Switching incentive | Moat hypothesis | Acquisition path | Current blocker | Next proof |
|---|---|---|---|---|---|---|---|---|---|
| Sessions | AI engineering teams, agent builders, developers | ad-hoc chat history, IDE state, issue trackers, generic memory layers | context loss, unverifiable completion, weak long-running continuity | survive realistic multi-session engineering workflows with materially less lost state and reproducible recovery | persistent execution history + evidence + resumability that reduces rework | accumulated workflow/evidence graph, integrations, long-lived state | developer-led pilots, AI engineering teams, technical demos | no real external usage/retention evidence yet | deploy production pilot and measure resume success, lost-context rate, recovery time, task completion |
| JobFlow | appointment/service businesses | human receptionist, answering services, basic voice bots, vertical SaaS front desks | missed calls, latency, incomplete booking, poor escalation, fragmented state | high successful-call handling and booking completion with low escalation and measurable labor savings | replaces/augments expensive front-desk labor while preserving continuity | workflow data, integrations, business-specific operating state, reliability evidence | local service-business pilots, direct outreach, vertical partnerships | no real business usage/payment evidence yet | deploy to first business and measure calls handled, bookings, escalations, failures, labor/time saved |
| Measure | AI/system vendors, buyers, evaluators | benchmark suites, vendor self-reported metrics, one-off eval consultancies | gaming, contamination, weak reproducibility, unverifiable claims | catch benchmark weaknesses ordinary suites miss while producing replayable evidence | trusted independent proof and benchmark auditing | verifier ecosystem, evidence ledger, certified evaluators, accumulated benchmark corpus | evaluate external systems, publish evidence-backed reports, enterprise audits | external evaluation and buyer validation still missing | evaluate a real external system/benchmark and document findings ordinary benchmark reporting misses |
| WorkForce- | companies deploying AI workers | fragmented agent frameworks, RPA, custom orchestration | weak persistence, collisions, opaque completion, lock-in | complete realistic multi-agent workflows with auditable state and lower coordination failure | persistent governed AI workforce with evidence and recovery | operational data, orchestration state, integrations, verification layer | design-partner deployments with ops-heavy businesses | insufficient external workload proof | run real workflow pilot and measure completion, intervention rate, collision/recovery events, cost |
| Jiffy-Laundry-App | laundry customers / operators | phone/text ordering, incumbent laundry apps | friction, status opacity, operational coordination | faster order flow, lower operator handling burden, higher successful pickup/delivery completion | simpler experience + better operator economics | local density, logistics history, customer/operator retention | local launch in constrained geography | usage exists only partially; commercial proof incomplete | instrument full order funnel and validate repeat paid orders |
| Muze | artists, managers, rights holders, fans | streaming/distribution/ticketing/merch platforms | fragmented economics, weak ownership/control, opaque payouts, disintermediation | faster transparent payouts and materially higher direct-fan/artist economic control | ownership + unified monetization + direct audience relationship | rights/identity graph, fan relationships, integrated economics | artist pilot cohorts, managers, indie labels, creator partnerships | licensing/rights and real artist onboarding/payment proof | onboard pilot artist with verified rights and complete one end-to-end paid fan transaction/payout |
| Watchable | households / content partners | cable, vMVPDs, streaming bundles | price, fragmentation, device friction | deliver target service at constrained household price with reliable playback and usable channel/content experience | lower total cost + simpler TV experience + optional hardware | distribution relationships, owned device/app experience, household bundle economics | local/segment launch, direct sales, referral residuals | content rights, production delivery, unit economics, real households | validate lawful content package + working production stream + first paid household |
| Codeable | developers / teams | IDE copilots, coding agents, manual debugging workflows | brittle edits, unverifiable completion, weak recovery | higher successful repair/task completion with deterministic validation and fewer regressions | safer autonomous code work with proof and retry/recovery | execution/evidence history, repair traces, integrations | developer demos, targeted engineering teams | benchmark and external usage evidence incomplete | benchmark against representative coding-agent workflow on repair success, regressions, time, retries |

## Hiring / engineering proof tranche

| Project | Strongest baseline | Advantage that must be proven | Next experiment |
|---|---|---|---|
| applied-ai-erp-agent | manual ERP operation + generic tool-using agent | safer governed enterprise actions with deterministic verification | fault-injected ERP scenarios; compare task completion, unsafe-write rate, recovery, evidence completeness |
| Prism | FP32/FP16/INT8 storage/execution path | real packed low-bit resource savings at bounded quality loss | same workload at baseline, 4-bit, 2-bit; record bytes, RSS, latency, throughput, quality |
| VaultRam | ordinary memory allocation / OS swap | larger useful workload completion with controlled tiering and acceptable slowdown | workload that OOMs baseline but completes under tiering; measure faults, I/O wait, effective capacity, throughput |
| Focus | static placement / naive recency | useful hotness prediction that reduces costly movement or misses | replay trace with/without Focus; measure hit rate, false prefetch, missed-hot cost, bytes moved, net benefit |
| Maestro | static scheduling | adaptive scheduling that reduces idle/I/O wait or improves throughput | identical workload static vs adaptive; measure completion time, utilization, wait, adaptation overhead |
| OverDrive | baseline runtime without coordinated layers | integrated constrained-hardware advantage greater than isolated components | ablation benchmark: baseline -> Prism -> +VaultRam -> +Focus -> +Maestro -> full stack |
| Hired-Ai | manual job search + generic automation | governed multi-agent workflow with better traceability and lower coordination failure | replay representative applications; measure completion, evidence, handoff errors, intervention rate |

## Research proof tranche

| Project | Research claim class | Required falsifiable proof | Current next step |
|---|---|---|---|
| Einstein | developmental synthetic cognition | individual mechanisms improve learning/generalization/stability without erasing prior capability | implement first minimal developmental experiments: belief versioning, consolidation, goal provenance, capability regression |
| Epiphany- | governed cognition / governed OS | governance preserves authority boundaries under adversarial capability growth | adversarial privilege/authority scenarios with immutable evidence and rollback |
| ECA-1- | embodied cognition | integrated perception/action loop outperforms disconnected control baseline on defined embodied tasks | choose simulated embodied task and establish baseline + recovery tests |
| G.A.I.A | causal intelligence | causal mechanism identifies interventions/counterfactuals better than correlational baseline | controlled causal worlds with hidden confounders and intervention scoring |
| Bio-Gene-v.1.0 | biomedical research platform | evidence system improves hypothesis quality/reproducibility without overstating biological claims | select bounded public dataset/question and run reproducible hypothesis-to-evidence pipeline |

## Platform ecosystem tranche

Scout, Cannon, Cannon-Plus, Nova, Parallel, Cadence-, Sprout, Velocity, Chronos, Syncio, Plasma, and Cortex are treated as one ecosystem for strategic evaluation even though each remains independently testable.

The ecosystem must eventually prove an end-to-end path:

`create project -> author -> compile/build -> execute -> persist data -> interoperate -> test -> release -> deploy -> observe -> recover`

The key disruption test is not whether every component exists. It is whether the integrated developer experience produces a measurable advantage over established toolchains in setup time, build/runtime performance, deployment reliability, cognitive burden, portability, or another customer-valued dimension.

**Next ecosystem proof:** choose one representative application and build/deploy it end-to-end through the native stack while capturing every failure, workaround, timing result, and external dependency.

## Incubation rule for remaining assets

Axion, Boop, Branded, Cognified, Concord, cradleos-v0, Dev-Zero-, GigFlow, IPX, J.A.R.V.I.S, Knowledge-Base-Ai, Nearby, No-Cap, phmf-v1-, skill-x, Teamwork-Data, Teamwork-Release, Teamwork-Test, The-Vigilante-, and other non-priority assets remain active but do not automatically consume equal execution time.

They are promoted when one of these is true:

- the core dependency chain is ready;
- an external customer/opportunity appears;
- the next experiment can cheaply resolve a high-value uncertainty;
- the asset materially strengthens a priority product;
- a market/technology change increases its immediate value.

## Commercial closure rule

For every commercial repo, the terminal evidence chain is:

`real buyer -> real problem -> existing spend -> incumbent baseline -> measurable superiority -> deployable product -> onboarding -> payment -> usage -> retained usage -> customer value -> repeatable acquisition`

Revenue without retained customer value is not commercial completion. Technical superiority without adoption is not disruption. Adoption without defensible value is not a durable business.
