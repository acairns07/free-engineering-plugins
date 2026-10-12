# Expiring access example

Requirement ACCESS-01: access is allowed only before expires_at. Fix the clock at 2030-01-01T12:00:00Z and create an active grant ending at that instant.

T-01: at 11:59:59Z the entitled operation succeeds. T-02: at 12:00:00Z it is denied. T-03: at 12:00:01Z it is denied. T-04: an unrelated user's grant does not permit this user. T-05: revocation denies access even before expiry. T-06: denied requests create no protected records and expose no private content.

Integration extension: two concurrent revoke/invoke requests have an explicitly documented transaction ordering; tests should not assume a guarantee the design does not provide. All cases above are proposed examples, not execution results.
