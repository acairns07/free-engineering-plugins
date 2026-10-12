# Review lenses

Correctness: invariants, ordering, consistency, idempotency and transaction scope.
Security: authentication versus authorisation, explicit ownership checks, trust crossing, secrets and minimised privileges.
Data: purpose, ownership, schema evolution, retention, deletion, backup and restored integrity.
Resilience: bounded timeouts, retry budgets, overload behaviour, recovery and dependency isolation.
Operations: deployment repeatability, rollback compatibility, useful telemetry and on-call ownership.
Economics: dominant storage/egress/compute costs and a measurable trigger for scaling.
Architecture: cohesion, coupling, boundaries, alternatives and reversibility.

Severity describes plausible impact plus exposure, not how much effort a fix requires. Unknown evidence should create a verification action; it is not proof that a control is absent. Compliance is not established by an architecture diagram.
