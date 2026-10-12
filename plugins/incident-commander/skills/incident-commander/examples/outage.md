# Example: intermittent checkout errors

14:05Z: synthetic checkout failures rise; support reports affected customers. Impact extent unknown. 14:07Z: new release deployed at 13:58Z, but causation is unconfirmed. Database connections are near their configured limit.

Hypotheses: connection leak in the release; traffic burst; slow downstream payment responses holding connections. Read-only discriminators: active/idle connection counts, request volume, latency by dependency and comparison with the previous release window.

Proposed mitigation: route traffic to the previous version only after confirming schema compatibility. Stop if payment duplication or error rate worsens. Authorisation and execution remain pending.

Recovery: successful synthetic and representative customer journeys, stable connection count and error rate, reconciliation of unknown payment outcomes. A green homepage alone is insufficient.
