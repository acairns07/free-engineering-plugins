# Example: daily order totals

Producer: order service. Consumer: finance aggregation. Contract status: proposed. Primary key: order_id, immutable. total_minor is an integer in the currency's minor units; currency is a separate ISO currency code. Do not assume all currencies have two decimal places. created_at is an RFC 3339 UTC instant, distinct from business_date in the agreed accounting timezone.

Proposed quality: order_id is unique within the delivered snapshot; total_minor is non-negative unless record_type explicitly denotes a refund. Exact reconciliation tolerance and accounting cutoff require finance-owner approval.

Late correction: republish a record with the same order_id and an increasing revision, with consumers applying only newer revisions. A batch-complete marker distinguishes a complete zero-row delivery from a failed extract. Changing totals from minor units to decimals is a breaking semantic change even if the field remains numeric.
