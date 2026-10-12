# Worked example: shared meeting-room bookings

Evidence: supplied office-manager note says conflicting reservations require manual resolution. No conflict rate has been measured. Outcome proposal: reduce confirmed double bookings to zero; collect a one-week baseline first.

Scope: authenticated staff reserve one room for one interval and cancel their own reservation. Recurring reservations and catering are deferred.

R-001: a staff member can reserve a free room for a future start/end time. R-002: concurrent requests for overlapping intervals cannot both succeed. R-003: staff can cancel only their own bookings; managers have explicitly audited override permission.

R-002-A: Given two users submit overlapping reservations concurrently, when both are processed, exactly one succeeds and the other receives the current availability without losing their selected time. R-003-B: Given a booking owned by another staff member, when cancellation is requested, access is denied and that booking remains active.

Unknowns: office timezone, maximum duration and manager role source. These are decisions, not facts. A proposed 500 ms response target requires measurement before release. This example is illustrative, not evidence of a deployed system.
