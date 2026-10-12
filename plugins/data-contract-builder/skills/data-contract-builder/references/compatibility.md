# Compatibility guidance

Potentially breaking changes: removing or renaming a field, narrowing a type/range, changing units or timezone, changing key meaning, strengthening nullability, reusing an enum value or changing event-order guarantees.

Additive does not always mean safe: consumers with closed schemas may reject unknown fields; a new enum member may break exhaustive switches. Test actual consumer contracts.

Version policy proposal: major for incompatible semantics/contracts, minor for compatible additions, patch for clarification that changes no behaviour. Agree support periods with owners instead of inventing dates.

Data rules need a denominator and time window. "99% complete" must identify which fields, eligible records and period. Delete propagation must cover derived copies and backups according to the retention policy. Do not promise instantaneous erasure from immutable backups unless implemented.
