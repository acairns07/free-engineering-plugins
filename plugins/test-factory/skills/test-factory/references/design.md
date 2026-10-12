# Test design guidance

Boundary analysis: use immediately below, exactly at and immediately above a specified threshold. Ask which side is inclusive when the contract is ambiguous.
Decision tables: enumerate combinations where more than one condition controls an outcome, especially permissions and entitlement expiry.
State transitions: list legal/illegal transitions, repeated events and recovery after interruption.
Property checks: conservation, monotonicity, idempotency and isolation can detect more than a handful of example values.
Concurrency: coordinate starts with barriers or controlled scheduling; avoid fragile sleeps.
Security: a denied call must leave state unchanged and must not reveal another user's data.
Privacy: inspect persisted fields/logs using synthetic canaries; do not introduce real secrets in test fixtures.

Avoid snapshots of large generated text, timing assertions tied to workstation speed, live services in unit tests and unbounded retries. Record which external behaviour remains unverified behind mocks.
