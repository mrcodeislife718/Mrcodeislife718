# Portfolio Completion Standard

Every project in this portfolio follows the same evidence-first progression:

Architecture -> Working implementation -> Tests -> Adversarial/failure tests -> Benchmarks -> Empirical proof -> Deployment -> Real usage -> Commercial validation where applicable -> Continuous improvement.

For products intended to disrupt a market, technical completion alone is insufficient. They also follow:

Existing spend -> incumbent baseline -> valuable weakness -> measurable superiority target -> switching incentive -> moat -> deployable product -> customer onboarding -> payment -> usage -> retention -> measurable customer value -> repeatable acquisition.

## Definition of done

A project is not complete because its architecture is documented. It is complete when its claimed capability exists, survives testing, produces reproducible evidence, operates in its intended environment, and—when commercial—creates enough real value that users adopt it and customers are willing to pay for it.

A commercial project is not considered disruptive merely because it is different. A disruption claim requires evidence that the product materially outperforms incumbent alternatives on dimensions customers value enough to adopt, switch, or pay for.

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

## Required vertical-disruption gates

Commercial products and platform businesses must additionally track:

1. **Existing spend** — evidence that the target customer already spends money, time, labor, risk budget, or opportunity cost solving the problem.
2. **Incumbent benchmark** — named incumbent or current workflow plus measurable baseline for cost, speed, reliability, accuracy, setup burden, lock-in, trust, usability, or another economically relevant dimension.
3. **Measurable superiority target** — a falsifiable target such as 50% lower cost, 2x faster completion, fewer failures, faster onboarding, higher automation, better verification, or materially better ownership/control.
4. **Switching incentive** — explicit reason a customer would endure migration or behavior change. Feature parity is not a switching incentive.
5. **Moat** — durable advantage such as proprietary workflow data, network effects, protocol/ecosystem position, accumulated evidence, integration depth, switching costs created by value, specialized infrastructure, or brand/distribution.
6. **Acquisition path** — concrete route to initial and repeat customers, including channel, target buyer, offer, conversion event, and economics.
7. **Customer value proof** — measured evidence that use of the product improves an outcome the customer cares about.

These gates are evidence states too: PROVEN, PARTIAL, UNPROVEN, or N/A.

## Commercial product chain

Working product -> Deployable -> Production -> Customer onboarding -> Payment -> Customer usage -> Retention -> Measurable customer value -> Repeatable acquisition.

No stage may be marked complete without an evidence artifact.

## Research / infrastructure chain

Hypothesis -> Baseline -> Experiment -> Reproducible measurement -> Comparison -> Failure analysis -> Limitations -> Independent reproduction where feasible.

Research claims must distinguish design intent, implementation state, measured result, and unverified hypothesis.

For research systems, the disruption equivalent is **scientific/engineering superiority**: the repository must identify the strongest relevant baseline and prove a meaningful improvement, new capability, or previously unavailable tradeoff.

## Claim-to-evidence rule

Material claims must be mechanically traceable to evidence. Examples:

- "reduces memory" -> benchmark showing baseline and measured memory reduction;
- "production-ready" -> deployment, health, rollback, and operational checks;
- "fault tolerant" -> fault-injection result and recovery evidence;
- "secure" -> scoped security controls and adversarial/security tests;
- "faster" -> reproducible latency/throughput benchmark;
- "better than incumbent X" -> same-workload comparison against X;
- "customers will switch" -> interviews, migrations, pilots, conversion, or other adoption evidence;
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
- incumbent/current-workflow baseline where applicable;
- measurable superiority target;
- switching incentive where applicable;
- moat hypothesis;
- acquisition path where applicable;
- current blockers;
- next falsifiable experiment or commercial proof;
- known limitations;
- last verification date.

Machine-readable claim ledgers must never promote a claim merely because implementation exists. Implementation, proof, deployment, customer value, and commercial validation are separate facts.

## Portfolio prioritization

Finish the closest-to-value commercial products first while continuously advancing deeper research and infrastructure systems. Priority is driven by evidence gap, customer value, time to deployment, strategic differentiation, dependency value to other projects, and probability that the next experiment will change a major gate from UNPROVEN/PARTIAL to PROVEN.

Use three execution lanes:

- **Finish & monetize now** — products near deployment, users, and revenue.
- **Produce hard engineering proof** — infrastructure/research where benchmarks and reproducibility create the asset value.
- **Incubate strategically** — important assets whose next major proof depends on earlier technical or market work.

## Permanent rule

**Here is the code. Here are the tests. Here is the benchmark. Here are the failures we discovered. Here is what we fixed. Here is the deployment. Here is what happened when real people used it. Here is the incumbent baseline. Here is our measured advantage. Here is why customers switch. Here is the evidence supporting every major claim.**
