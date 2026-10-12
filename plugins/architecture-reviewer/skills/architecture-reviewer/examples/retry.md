# Finding example

Evidence: design section 4 retries a payment-provider request three times after timeout, with no documented idempotency key. Code and provider contract were not inspected.

AR-01 — High, pending contract verification: the provider may commit a charge before the client times out; retrying a new request could duplicate the charge. Confirm the provider's idempotency semantics and use a stable key for one business operation. Keep a durable operation identifier and reconcile an unknown result before trying a distinct operation.

Verification: simulate provider commit followed by client timeout; repeat the request and demonstrate one business effect. This is a proposed test, not a passed result. An alternative is to stop automatic retry and require reconciliation, trading throughput for simpler failure handling.
