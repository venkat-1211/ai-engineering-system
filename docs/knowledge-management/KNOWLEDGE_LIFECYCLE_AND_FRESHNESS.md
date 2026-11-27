# Knowledge Lifecycle and Freshness

Suggested lifecycle: `Draft → In review → Approved (if required) → Active → Review due/Stale → Updated or Superseded → Archived`.

Durable important records need an owner or `Unassigned`, and a review date or trigger. Review after relevant architecture, dependency, API, schema, policy, deployment, incident, or major release changes. Cadence must reflect volatility and risk, not an arbitrary universal expiry.

Preserve meaningful history. Mark replaced records `Superseded` and link replacements. Do not rewrite historical decisions as if they were always current. Follow retention policy. Remove secrets through approved processes rather than preserving them for history.

Agents may identify stale records and propose changes; they may not claim approval, archival, or deletion unless authorized action actually occurred.
