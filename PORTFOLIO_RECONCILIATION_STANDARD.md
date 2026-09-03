# Portfolio Reconciliation Standard

This is the mandatory preservation and canonicalization rule for the portfolio.

## Core invariant

**Branch ancestry is evidence, not proof of capability preservation.**

A branch is not considered reconciled merely because its head is an ancestor of `main`. Later commits can delete, disconnect, weaken, disable, or commercially orphan work that once existed in history.

A repository is canonical only after the current `main` tree is checked for surviving capability.

## Required sequence

For every repository:

1. **Branch history** — enumerate current branch heads and identify ancestor, ahead, diverged, alias, and historical heads.
2. **Tree content** — inspect the files actually present at each materially distinct head and in current `main`.
3. **Unique files and artifacts** — preserve unique source, tests, migrations, schemas, assets, docs, deployment files, workflows, and binary artifacts that still matter.
4. **Capability survival** — verify that the behavior represented by historical work still exists in current `main`; filename survival alone is not sufficient.
5. **Runtime wiring** — verify surviving capability is reachable through the current application/runtime/API/CLI/UI rather than merely present as dead code.
6. **Test and qualification survival** — verify regression coverage and qualification gates for the capability still exist or are superseded by stronger evidence.
7. **Commercial and operational survival** — for revenue-bearing products, verify pricing, billing, entitlements, onboarding, delivery, customer isolation, economic accounting, recovery, deployment, and production boundaries still represent the intended business model.
8. **Canonical main** — only after the above checks may a repository be called consolidated.

## Reconciliation outcomes

Each branch must resolve to one of these outcomes:

- **Contained:** branch capability survives in `main` and the branch is a strict ancestor or identical head.
- **Semantically superseded:** historical implementation differs, but every material capability survives in a stronger/evolved form in `main`.
- **Preserve artifact:** a unique file, test, migration, asset, proof, or other artifact must be copied or grafted into `main`.
- **Reconcile implementation:** unique live capability must be integrated onto current `main` without regressing newer architecture.
- **Intentionally external/private:** the repository is a controlled public/product surface and explicitly places production source elsewhere; do not fabricate missing code into the public repository.
- **Obsolete:** the historical implementation has no surviving product value and is intentionally not reintroduced, with its useful capability already replaced or no longer required.

## No-loss rule

The objective is **preserve capability, not preserve obsolete code**.

Do not blindly merge every branch. Do not overwrite newer implementations with older ones merely to simplify branch topology. Do not declare work preserved from commit topology alone. Do not invent a runtime because a README describes one. Do not call a repository complete when commercial or operational wiring is absent from a revenue-bearing product.

## Economic completion rule

Additional engineering is justified only when it directly improves one or more of:

**REVENUE → CONVERSION → DELIVERY → RETENTION → EXPANSION → MARGIN → DISTRIBUTION → DEFENSIBILITY → REQUIRED RISK REDUCTION**

For commercial products, Stripe or another provider is a financial rail, not the owner of product economics. Product identity, pricing intent, entitlements, customer state, delivery logic, invoices/receipts where applicable, and economic evidence remain product-owned.

## Canonical lifecycle

**BUILT + TESTED → RECONCILED → COMMERCIALIZED → SOLD → DELIVERED → RETAINED → SCALED**

A repository may be technically mature while still requiring commercial completion. It may also be strategically valuable without being a standalone subscription product. The economic role determines the correct completion work.