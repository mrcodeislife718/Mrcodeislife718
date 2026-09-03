# Portfolio Economic Operating System

## Objective

Maximize the economic value of the portfolio as a whole. Repositories are not required to monetize independently. Each project must be assigned the economic role that creates the greatest total portfolio value.

Engineering work is a means, not the objective. Tests, benchmarks, documentation, refactors, branch cleanup, production hardening, and architecture work are funded by their ability to increase revenue, deal velocity, pricing power, customer trust, licensing value, adoption, defensibility, strategic leverage, or portfolio optionality.

## Decision loop

For every serious repository:

1. What does this repository actually do today?
2. Who values it enough to pay, adopt, integrate, license, or depend on it?
3. Which economic role maximizes portfolio value?
4. What is the immediate blocker to that outcome?
5. What is the smallest highest-value action that removes that blocker?
6. What should explicitly NOT be built yet?

## Economic roles

### 1. Already sellable
Treat the repository as a business. Priority order: customer acquisition, payment/contract path, onboarding, delivery, retention, support, expansion, and only then engineering that materially improves those outcomes.

### 2. Nearly sellable
Close only the gaps preventing safe transactions, deployment, onboarding, payment, legal delivery, or customer success. Do not overbuild for hypothetical scale.

### 3. Strategic infrastructure
Optimize for cross-portfolio leverage, licensing, OEM/enterprise integration, open-core distribution, standards influence, defensible IP, or reduced operating cost across commercial products.

### 4. Research / option value
Preserve the project and its IP while constraining engineering spend until a credible customer, licensing, strategic, or adoption path emerges.

## Required economic map

Each serious repo should maintain an economic record containing:

- economic role
- target customer / adopter
- painful problem solved
- current sellable capability
- distribution channel
- monetization mechanism
- pricing / deal shape hypothesis
- moat / defensible IP
- dependencies on other portfolio repos
- immediate revenue or adoption blocker
- next highest-value action
- explicit not-now work
- evidence required to unlock a real economic event

## Capital-allocation rules

- If a benchmark can unlock or materially improve a real sale, licensing deal, enterprise evaluation, or adoption decision, run it.
- If additional benchmarking will not change a buyer or partner decision, stop and move toward distribution or sales.
- If production hardening is necessary to serve the next customer safely, harden it.
- If the system can already serve the next cohort, do not build for million-user scale before demand exists.
- If open source materially increases distribution or ecosystem power without destroying the moat, use it strategically.
- If open source would give away the core licensing or IP advantage, protect the core and expose only the adoption layer.
- If payment, contracting, onboarding, deployment, or sales collateral is the only blocker between a usable product and revenue, that blocker outranks additional architecture work.
- No repository receives engineering work solely because more engineering is possible.

## Economic evidence standard

Evidence exists to unlock an economic event. Acceptable evidence includes customer outcomes, paid usage, signed contracts, conversion, retention, deployment reliability, benchmark wins that buyers care about, cost reductions, integration proof, licensing interest, adoption, contributor/ecosystem growth, or measurable cross-portfolio leverage.

The question is never merely “is this tested?” It is “what economically meaningful decision does this evidence enable?”

## Portfolio priority function

Rank work by expected portfolio value:

`priority = economic_upside × probability_of_unlock × strategic_leverage × urgency / effort`

Use judgment rather than false precision. The formula exists to prevent low-value engineering activity from outranking work that can produce revenue, adoption, licensing, or defensibility now.

## Stop conditions

Pause or defer work when:

- the next engineering increment does not improve a real economic outcome;
- no credible customer/adopter/licensing path exists yet;
- another repo has a materially higher expected portfolio return;
- the work is premature scaling;
- evidence already meets the decision threshold;
- the feature is technically attractive but economically irrelevant to the current stage.

## Portfolio mandate

The portfolio is the product. Some repositories should generate direct revenue. Some should create licensing/IP revenue. Some should drive adoption. Some should reduce infrastructure cost. Some should become standards or ecosystem anchors. Some should remain protected strategic options.

The governing objective is to compound the economic value of the entire system rather than maximize activity inside any single repository.
