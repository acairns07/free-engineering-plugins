# Response guidance

Prioritise safety and containment, user impact reduction, evidence preservation, then diagnosis. Keep one shared timeline in UTC plus the user's local timezone where needed. Redact personal data and tokens before including observations.

Good mitigation: a bounded, reversible change with an owner and success/stop criteria. A rollback may be unsafe after a schema change; verify compatibility first. A restart can hide evidence or amplify recovery load; understand the failure and preserve useful diagnostics.

Good update: timestamp, current impact, what is known, action in progress, next update. Unknown cause is acceptable. Blame and speculation are not useful operational data.

Closure requires sustained user-journey success, normal error/latency signals, verified backlog/data state, removed temporary access and assigned residual work. Root cause may remain unresolved after service recovery.
