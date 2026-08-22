# Portfolio Completion Standard

Every project in this portfolio follows the same evidence-first progression:

Architecture -> Working implementation -> Tests -> Adversarial/failure tests -> Benchmarks -> Empirical proof -> Deployment -> Real usage -> Commercial validation where applicable -> Continuous improvement.

## Definition of done

A project is not complete because its architecture is documented. It is complete when its claimed capability exists, survives testing, produces reproducible evidence, operates in its intended environment, and—when commercial—creates enough real value that users adopt it and customers are willing to pay for it.

## Required evidence gates

Each repository is evaluated against these gates:

1. **Implementation** — core claimed capability exists as executable software or, for research architecture, as a runnable experiment.
2. **Tests** — correctness tests cover the intended path and important edge cases.
3. **Failure testing** — fault injection, adversarial tests, malformed inputs, dependency failure, degraded resources, rollback/recovery, and abuse cases are exercised where applicable.
4. **Benchmarks** — explicit baseline, workload, hardware/environment, measurement method, raw result, and reproducibility command.
5. **Proof** — every material README/marketing claim maps to an artifact, test, benchmark, deployment, or user result.
6. **Security** — threat model, authorization boundaries, secrets handling, tenant isolation, dependency risk, abuse controls, and incident/recovery procedures appropriate to the project.
7. **Deployment** — repeatable deployment path, configuration contract, health checks, observability, rollback, backups/recovery, and production-readiness evidence where deployment applies.
8. **Users** — real usage evidence where the system is user-facing; synthetic usage is never mislabeled as user validation.
9. **Revenue** — payment, retention, unit economics, and repeatable acquisition evidence where the project is commercial.
10. **Documentation** — architecture, setup, operations, limitations, evidence, and known failure modes remain current.

## Commercial product chain

Working product -> Deployable -> Production -> Customer onboarding -> Payment -> Customer usage -> Retention -> Measurable customer value -> Repeatable acquisition.

No stage may be marked complete without an evidence artifact.

## Research / infrastructure chain

Hypothesis -> Baseline -> Experiment -> Reproducible measurement -> Comparison -> Failure analysis -> Limitations -> Independent reproduction where feasible.

Research claims must distinguish design intent, implementation state, measured result, and unverified hypothesis.

## Claim-to-evidence rule

Material claims must be mechanically traceable to evidence. Examples:

- "reduces memory" -> benchmark showing baseline and measured memory reduction;
- "production-ready" -> deployment, health, rollback, and operational checks;
- "fault tolerant" -> fault-injection result and recovery evidence;
- "secure" -> scoped security controls and adversarial/security tests;
- "faster" -> reproducible latency/throughput benchmark;
- "used by customers" -> real usage evidence;
- "commercially validated" -> payment/retention evidence.

Unsupported adjectives are not proof.

## Evidence states

A gate can only be one of:

- **PROVEN** — artifact exists and supports the claim.
- **PARTIAL** — some evidence exists but the gate is incomplete.
- **UNPROVEN** — no sufficient evidence has been verified.
- **N/A** — genuinely not applicable to this project.

Percent-complete estimates are not accepted as substitutes for evidence.

## Required repository record

Every project repository must maintain `PORTFOLIO_PROOF.md` containing:

- project track;
- intended user / workload;
- core claims;
- gate status;
- exact evidence paths/commands;
- current blockers;
- next falsifiable experiment or commercial proof;
- known limitations;
- last verification date.

## Portfolio prioritization

Finish the closest-to-value commercial products first while continuously advancing deeper research and infrastructure systems. Priority is driven by evidence gap, customer value, time to deployment, strategic differentiation, and dependency value to other projects.

## Permanent rule

**Here is the code. Here are the tests. Here is the benchmark. Here are the failures we discovered. Here is what we fixed. Here is the deployment. Here is what happened when real people used it. Here is the evidence supporting every major claim.**
