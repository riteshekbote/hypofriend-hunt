# Hypotheses (ranked)

## RANKED HYPOTHESES 2026-09-02 21:35:39 UTC

## RANKED HYPOTHESES 2026-09-02 23:33:09 UTC

## RANKED HYPOTHESES 2026-09-03 01:30:17 UTC

## RANKED HYPOTHESES 2026-09-03 06:29:54 UTC

## RANKED HYPOTHESES 2026-09-03 11:43:38 UTC

## RANKED HYPOTHESES 2026-09-03 15:49:44 UTC
- [70] graph.hypofriend.de: GraphQL Introspection & Field-Level Auth Bypass (from art/lead_nemotron3.txt)
- [68] api.hypofriend.de: API versioning/bypass on api.hypofriend.de (from art/lead_bigpickle.txt)
- NEXT(hypotheses-nemotron3.txt): PROBE: GET https://graph.hypofriend.de/graphql?query=%7B__schema%7Btypes%7Bname%2Cfields%7Bname%7D%7D%7D%7D
- NEXT(hypotheses-bigpickle.txt): PROBE: GET https://api.hypofriend.de/, GET https://api.hypofriend.de/api/, GET https://api.hypofriend.de/api/v1/, GET https://api.hypofriend.de/api/v2/, GET htt
- LEARN: FIRST_RUN — no prior hypotheses to accept/reject; baseline established from passive DNS/CT inventory
- LEARN: ACCEPTED MISCONFIG @ api.hypofriend.de: Versioned API endpoints are common misconfiguration, high business value.
- LEARN: ACCEPTED MISCONFIG @ admin.hypofriend.de: Admin portals often exposed with weak controls.
- LEARN: ACCEPTED MISCONFIG @ core-api.hypofriend.de: GraphQL introspection is common misconfiguration.

## RANKED HYPOTHESES 2026-09-03 19:11:58 UTC
- [68] api.hypofriend.de: API versioning/bypass on api.hypofriend.de (from art/lead_bigpickle.txt)
- [65] hypofriend.de/api/v3/advisors: HTTP Basic Auth Credential Reuse on Advisors API (from art/lead_nemotron3.txt)
- NEXT(hypotheses-bigpickle.txt): PROBE: GET https://api.hypofriend.de/, GET https://api.hypofriend.de/api/, GET https://api.hypofriend.de/api/v1/, GET https://api.hypofriend.de/api/v2/, GET htt
- NEXT(hypotheses-nemotron3.txt): PROBE: GET https://o128333.ingest.sentry.io/api/0/projects/ with Authorization: DSN from window.__NUXT__ (public key only)
- LEARN: ACCEPTED MISCONFIG @ api.hypofriend.de: Versioned API endpoints are common misconfiguration, high business value.
- LEARN: ACCEPTED MISCONFIG @ admin.hypofriend.de: Admin portals often exposed with weak controls.
- LEARN: ACCEPTED MISCONFIG @ core-api.hypofriend.de: GraphQL introspection is common misconfiguration.
- LEARN: REJECTED MISCONFIG @ api.hypofriend.de: Versioned API endpoints (api.hypofriend.de/api/v1 etc.) do not exist — subdomain unresponsive (000), not a misconfigurat
- LEARN: REJECTED MISCONFIG @ admin.hypofriend.de: Admin portal returns 503, not exposed with weak controls
- LEARN: REJECTED MISCONFIG @ core-api.hypofriend.de: GraphQL introspection not accessible — endpoint returns 503
- LEARN: ACCEPTED MISCONFIG @ hypofriend.de: Client-side secret exposure in Nuxt payload (Sentry DSN, Amplitude key, Flagsmith env ID) — high business value, passive tes

## RANKED HYPOTHESES 2026-09-03 21:38:24 UTC
- [70] hypofriend.de/api/v3/advisors: Broken authentication on /api/v3/advisors endpoint (from art/lead_bigpickle.txt)
- [60] hypofriend.de/api/v3/advisors: HTTP Basic Auth Weak/Default Credentials on Advisors API (from art/lead_nemotron3.txt)
- NEXT(hypotheses-nemotron3.txt): PROBE: GET https://o128333.ingest.sentry.io/api/0/projects/ with Authorization: DSN <public_key_from_window.__NUXT__>
- NEXT(hypotheses-bigpickle.txt): PROBE: GET https://auth.hypofriend.de/.well-known/openid-configuration, GET https://auth.hypofriend.de/authorize?response_type=code&client_id=test&redirect_uri=
- LEARN: REJECTED MISCONFIG @ api.hypofriend.de: Versioned API endpoints (api.hypofriend.de/api/v1 etc.) do not exist — subdomain unresponsive (timeout), not a misconfig
- LEARN: REJECTED MISCONFIG @ admin.hypofriend.de: Admin portal returns 503, not exposed with weak controls
- LEARN: REJECTED MISCONFIG @ core-api.hypofriend.de: GraphQL introspection not accessible — endpoint returns 503/timeout
- LEARN: REJECTED MISCONFIG @ graph.hypofriend.de: GraphQL introspection not accessible — endpoint returns 503
- LEARN: ACCEPTED MISCONFIG @ hypofriend.de: Client-side secret exposure in Nuxt payload (Sentry DSN, Amplitude key, Flagsmith env ID) — high business value, passive tes
- LEARN: ACCEPTED ENDPOINT @ hypofriend.de/api/v3/advisors: Live HTTP Basic auth endpoint confirmed (401), only active API surface on main domain
- LEARN: ACCEPTED MISCONFIG @ hypofriend.de: Client-side secret exposure in Nuxt payload (Sentry DSN, Amplitude key, Flagsmith env ID) — high business value, passive tes
- LEARN: REJECTED MISCONFIG @ api.hypofriend.de: Versioned API endpoints (api.hypofriend.de/api/v1 etc.) do not exist — subdomain unresponsive (000), not a misconfigurat
- LEARN: REJECTED MISCONFIG @ admin.hypofriend.de: Admin portal returns 503, not exposed with weak controls.
- LEARN: REJECTED MISCONFIG @ core-api.hypofriend.de: GraphQL introspection not accessible — endpoint returns 503.

## RANKED HYPOTHESES 2026-09-03 23:35:33 UTC
- [75] hypofriend.de/property-search-api: GraphQL IDOR on Property Search API via expose/exposes/leadId (from art/lead_nemotron3.txt)
- [60] auth.hypofriend.de: OAuth redirect_uri open-redirect / code-interception on auth.hypofriend.de (from art/lead_bigpickle.txt)
- NEXT(hypotheses-nemotron3.txt): PROBE: POST https://hypofriend.de/property-search-api {"query":"{ exposes(id: \"1\", limit: 20) { id title price city address } }"} — enumerate expose IDs 1-100
- NEXT(hypotheses-bigpickle.txt): PROBE: GET https://auth.hypofriend.de/.well-known/openid-configuration ; GET https://auth.hypofriend.de/authorize?response_type=code&client_id=test&redirect_uri
- LEARN: ACCEPTED MISCONFIG @ hypofriend.de/property-search-api: GraphQL introspection enabled on production mortgage search API — high business value, passive testable
- LEARN: REJECTED MISCONFIG @ api.hypofriend.de: Versioned API endpoints (api.hypofriend.de/api/v1 etc.) do not exist — subdomain unresponsive (timeout/000), not a misco
- LEARN: REJECTED MISCONFIG @ admin.hypofriend.de: Admin portal returns 503, not exposed with weak controls
- LEARN: REJECTED MISCONFIG @ core-api.hypofriend.de: GraphQL introspection not accessible — endpoint returns 503/timeout
- LEARN: REJECTED MISCONFIG @ graph.hypofriend.de: GraphQL introspection not accessible — endpoint returns 503
- LEARN: ACCEPTED ENDPOINT @ hypofriend.de/api/v3/advisors: Live HTTP Basic auth endpoint confirmed (401), only active API surface on main domain
- LEARN: ACCEPTED MISCONFIG @ hypofriend.de: Client-side secret exposure in Nuxt payload (Sentry DSN, Amplitude key, Flagsmith env ID) — high business value, passive tes
- LEARN: REJECTED MISCONFIG @ graph.hypofriend.de: GraphQL introspection not accessible — endpoint returns 503/timeout (confirmed prior).

## RANKED HYPOTHESES 2026-09-04 01:25:05 UTC
- [82] hypofriend.de/property-search-api: GraphQL IDOR/BOLA on favoritedExposes(leadId) — cross-user favorites enumeration (from art/lead_bigpickle.txt)
- [75] hypofriend.de/property-search-api: GraphQL IDOR on Property Search API via expose/exposes/leadId (from art/lead_nemotron3.txt)
- NEXT(hypotheses-nemotron3.txt): PROBE: POST https://hypofriend.de/property-search-api {"query":"{ exposes(id: \"1\", limit: 20) { id title price city address } }"} — enumerate expose IDs 1-100
- NEXT(hypotheses-bigpickle.txt): PROBE: POST https://hypofriend.de/property-search-api {"query":"{exposeSeen(leadId:\"00000000-0000-0000-0000-000000000000\",exposeId:\"1\"){seen}}"} and {"query
- LEARN: ACCEPTED MISCONFIG @ hypofriend.de/property-search-api: GraphQL introspection enabled on production mortgage search API — high business value, passive testable
- LEARN: REJECTED MISCONFIG @ api.hypofriend.de: Versioned API endpoints (api.hypofriend.de/api/v1 etc.) do not exist — subdomain unresponsive (timeout/000), not a misco
- LEARN: REJECTED MISCONFIG @ admin.hypofriend.de: Admin portal returns 503, not exposed with weak controls
- LEARN: REJECTED MISCONFIG @ core-api.hypofriend.de: GraphQL introspection not accessible — endpoint returns 503/timeout
- LEARN: REJECTED MISCONFIG @ graph.hypofriend.de: GraphQL introspection not accessible — endpoint returns 503
- LEARN: ACCEPTED ENDPOINT @ hypofriend.de/api/v3/advisors: Live HTTP Basic auth endpoint confirmed (401), only active API surface on main domain
- LEARN: ACCEPTED MISCONFIG @ hypofriend.de: Client-side secret exposure in Nuxt payload (Sentry DSN, Amplitude key, Flagsmith env ID) — high business value, passive tes
- LEARN: ACCEPTED IDOR @ hypofriend.de/property-search-api: `favoritedExposes(leadId)` resolver returns data for arbitrary unauthenticated leadId (200, no auth), exposin
- LEARN: ACCEPTED MISCONFIG @ hypofriend.de/property-search-api: Full GraphQL introspection enabled in production (Ruby, graphql-2.5.26) — schema + stack traces exposed;
- LEARN: REJECTED OATH @ auth.hypofriend.de: OAuth/OpenID author from auth.hypofriend.de returns 503 (3 probes); not reachable passively, hypothesis parked not confirmed

## RANKED HYPOTHESES 2026-09-04 06:05:04 UTC
- [88] hypofriend.de/property-search-api: GraphQL BOLA/read+write on property-search-api favoritedExposes/favoriteExpose — arbitrary leadId, no auth (from art/lead_bigpickle.txt)
- [82] hypofriend.de/property-search-api: GraphQL IDOR/BOLA on Property Search API via favoritedExposes(leadId) and expose/exposes IDs (from art/lead_nemotron3.txt)
- NEXT(hypotheses-nemotron3.txt): PROBE: POST https://hypofriend.de/property-search-api {"query":"{ exposes(id: \"1\", limit: 20) { id title price city address } }"} — enumerate expose IDs 1-100
- NEXT(hypotheses-bigpickle.txt): PROBE: (read-only, ≤1 rps every few sec) POST https://hypofriend.de/property-search-api {"query":"{exposes(id:\"1\",limit:1){...}}"} to learn expose-id format f
- LEARN: ACCEPTED MISCONFIG @ hypofriend.de/property-search-api: GraphQL introspection enabled on production mortgage search API — high business value, passive testable
- LEARN: ACCEPTED IDOR @ hypofriend.de/property-search-api: `favoritedExposes(leadId)` resolver returns data for arbitrary unauthenticated leadId (200, no auth), exposin
- LEARN: ACCEPTED MISCONFIG @ hypofriend.de/property-search-api: Full GraphQL introspection enabled in production (Ruby, graphql-2.5.26) — schema + stack traces exposed;
- LEARN: ACCEPTED MISCONFIG @ hypofriend.de: Client-side secret exposure in Nuxt payload (Sentry DSN, Amplitude key, Flagsmith env ID) — high business value, passive tes
- LEARN: ACCEPTED ENDPOINT @ hypofriend.de/api/v3/advisors: Live HTTP Basic auth endpoint confirmed (401), only active API surface on main domain
- LEARN: REJECTED MISCONFIG @ api.hypofriend.de: Versioned API endpoints (api.hypofriend.de/api/v1 etc.) do not exist — subdomain unresponsive (timeout/000), not a misco
- LEARN: REJECTED MISCONFIG @ admin.hypofriend.de: Admin portal returns 503, not exposed with weak controls
- LEARN: REJECTED MISCONFIG @ core-api.hypofriend.de: GraphQL introspection not accessible — endpoint returns 503/timeout
- LEARN: REJECTED MISCONFIG @ graph.hypofriend.de: GraphQL introspection not accessible — endpoint returns 503
- LEARN: REJECTED OATH @ auth.hypofriend.de: OAuth/OpenID author from auth.hypofriend.de returns 503 (3 probes); not reachable passively, hypothesis parked not confirmed
- LEARN: CONFIRMED IDOR @ hypofriend.de/property-search-api: `favoritedExposes(leadId)` resolves for arbitrary unauthenticated leadId (200, both zero-UUID and random-UUI
- LEARN: CONFIRMED IDOR @ hypofriend.de/property-search-api: `favoriteExpose(leadId,exposeId)` mutation executes a real write handler for arbitrary leadId with no auth (
- LEARN: CONFIRMED MISCONFIG @ hypofriend.de/property-search-api: `meta(id)` with bogus/nil leak returns full Ruby backtrace (graphql-2.5.26, puma-7.2.0, rack-cors-3.0.0
- LEARN: CONFIRMED IDOR @ hypofriend.de/property-search-api: `favoritedExposes(leadId)` resolves for arbitrary unauthenticated leadId (200, zero-UUID and random-UUID acc
- LEARN: CONFIRMED IDOR @ hypofriend.de/property-search-api: `favoriteExpose(leadId,exposeId)` mutation executes a real write handler for arbitrary leadId with no auth (
- LEARN: CONFIRMED MISCONFIG @ hypofriend.de/property-search-api: `meta(id)` with nil leaks full Ruby backtrace (graphql-2.5.26, puma-7.2.0, rack-cors-3.0.0, sentry-ruby
- LEARN: REJECTED OATH @ auth.hypofriend.de: OAuth/OpenID author returns 503 (multiple probes); not reachable passively.

## RANKED HYPOTHESES 2026-09-04 11:31:13 UTC
- [88] hypofriend.de/property-search-api: GraphQL BOLA/IDOR on property-search-api via favoritedExposes/favoriteExpose — arbitrary leadId read+write (from art/lead_nemotron3.txt)
- NEXT(hypotheses-nemotron3.txt): PROBE: POST https://hypofriend.de/property-search-api {"query":"{ exposes(id: \"1\", limit: 20) { id title price city address } }"} — enumerate expose IDs 1-100
- LEARN: ACCEPTED MISCONFIG @ hypofriend.de/property-search-api: GraphQL introspection enabled on production mortgage search API — high business value, passive testable
- LEARN: ACCEPTED IDOR @ hypofriend.de/property-search-api: `favoritedExposes(leadId)` resolver returns data for arbitrary unauthenticated leadId (200, no auth), exposin
- LEARN: ACCEPTED MISCONFIG @ hypofriend.de/property-search-api: Full GraphQL introspection enabled in production (Ruby, graphql-2.5.26) — schema + stack traces exposed;
- LEARN: ACCEPTED MISCONFIG @ hypofriend.de: Client-side secret exposure in Nuxt payload (Sentry DSN, Amplitude key, Flagsmith env ID) — high business value, passive tes
- LEARN: ACCEPTED ENDPOINT @ hypofriend.de/api/v3/advisors: Live HTTP Basic auth endpoint confirmed (401), only active API surface on main domain
- LEARN: CONFIRMED IDOR @ hypofriend.de/property-search-api: `favoritedExposes(leadId)` resolves for arbitrary unauthenticated leadId (200, zero-UUID and random-UUID acc
- LEARN: CONFIRMED IDOR @ hypofriend.de/property-search-api: `favoriteExpose(leadId,exposeId)` mutation executes a real write handler for arbitrary leadId with no auth (
- LEARN: CONFIRMED MISCONFIG @ hypofriend.de/property-search-api: `meta(id)` with nil leaks full Ruby backtrace (graphql-2.5.26, puma-7.2.0, rack-cors-3.0.0, sentry-ruby
- LEARN: REJECTED MISCONFIG @ api.hypofriend.de: Versioned API endpoints (api.hypofriend.de/api/v1 etc.) do not exist — subdomain unresponsive (timeout/000), not a misco
- LEARN: REJECTED MISCONFIG @ admin.hypofriend.de: Admin portal returns 503, not exposed with weak controls
- LEARN: REJECTED MISCONFIG @ core-api.hypofriend.de: GraphQL introspection not accessible — endpoint returns 503/timeout
- LEARN: REJECTED MISCONFIG @ graph.hypofriend.de: GraphQL introspection not accessible — endpoint returns 503
- LEARN: REJECTED OATH @ auth.hypofriend.de: OAuth/OpenID author returns 503 (multiple probes); not reachable passively

## RANKED HYPOTHESES 2026-09-04 15:22:38 UTC
- [70] graph.hypofriend.de: GraphQL Introspection & Field-Level Auth Bypass (from art/lead_nemotron3.txt)
- NEXT(hypotheses-nemotron3.txt): PROBE: GET https://graph.hypofriend.de/graphql?query=%7B__schema%7Btypes%7Bname%2Cfields%7Bname%7D%7D%7D%7D
- LEARN: FIRST_RUN — no prior hypotheses to accept/reject; baseline established from passive DNS/CT inventory
- LEARN: REJECTED MISCONFIG @ api.hypofriend.de: Versioned API endpoints (api.hypofriend.de/api/v1 etc.) do not exist — subdomain unresponsive (000), not a misconfigurat
- LEARN: REJECTED MISCONFIG @ admin.hypofriend.de: Admin portal returns 503, not exposed with weak controls
- LEARN: REJECTED MISCONFIG @ core-api.hypofriend.de: GraphQL introspection not accessible — endpoint returns 503
- LEARN: ACCEPTED MISCONFIG @ hypofriend.de: Client-side secret exposure in Nuxt payload (Sentry DSN, Amplitude key, Flagsmith env ID) — high business value, passive tes
- LEARN: REJECTED MISCONFIG @ api.hypofriend.de: Versioned API endpoints (api.hypofriend.de/api/v1 etc.) do not exist — subdomain unresponsive (timeout), not a misconfig
- LEARN: REJECTED MISCONFIG @ admin.hypofriend.de: Admin portal returns 503, not exposed with weak controls
- LEARN: REJECTED MISCONFIG @ core-api.hypofriend.de: GraphQL introspection not accessible — endpoint returns 503/timeout
- LEARN: REJECTED MISCONFIG @ graph.hypofriend.de: GraphQL introspection not accessible — endpoint returns 503
- LEARN: ACCEPTED MISCONFIG @ hypofriend.de: Client-side secret exposure in Nuxt payload (Sentry DSN, Amplitude key, Flagsmith env ID) — high business value, passive tes
- LEARN: ACCEPTED ENDPOINT @ hypofriend.de/api/v3/advisors: Live HTTP Basic auth endpoint confirmed (401), only active API surface on main domain
- LEARN: ACCEPTED MISCONFIG @ hypofriend.de/property-search-api: GraphQL introspection enabled on production mortgage search API — high business value, passive testable
- LEARN: REJECTED MISCONFIG @ api.hypofriend.de: Versioned API endpoints (api.hypofriend.de/api/v1 etc.) do not exist — subdomain unresponsive (timeout/000), not a misco
- LEARN: REJECTED MISCONFIG @ admin.hypofriend.de: Admin portal returns 503, not exposed with weak controls
- LEARN: REJECTED MISCONFIG @ core-api.hypofriend.de: GraphQL introspection not accessible — endpoint returns 503/timeout
- LEARN: REJECTED MISCONFIG @ graph.hypofriend.de: GraphQL introspection not accessible — endpoint returns 503
- LEARN: ACCEPTED ENDPOINT @ hypofriend.de/api/v3/advisors: Live HTTP Basic auth endpoint confirmed (401), only active API surface on main domain
- LEARN: ACCEPTED MISCONFIG @ hypofriend.de: Client-side secret exposure in Nuxt payload (Sentry DSN, Amplitude key, Flagsmith env ID) — high business value, passive tes
- LEARN: ACCEPTED MISCONFIG @ hypofriend.de/property-search-api: GraphQL introspection enabled on production mortgage search API — high business value, passive testable
- LEARN: REJECTED MISCONFIG @ api.hypofriend.de: Versioned API endpoints (api.hypofriend.de/api/v1 etc.) do not exist — subdomain unresponsive (timeout/000), not a misco
- LEARN: REJECTED MISCONFIG @ admin.hypofriend.de: Admin portal returns 503, not exposed with weak controls
- LEARN: REJECTED MISCONFIG @ core-api.hypofriend.de: GraphQL introspection not accessible — endpoint returns 503/timeout
- LEARN: REJECTED MISCONFIG @ graph.hypofriend.de: GraphQL introspection not accessible — endpoint returns 503
- LEARN: ACCEPTED ENDPOINT @ hypofriend.de/api/v3/advisors: Live HTTP Basic auth endpoint confirmed (401), only active API surface on main domain
- LEARN: ACCEPTED MISCONFIG @ hypofriend.de: Client-side secret exposure in Nuxt payload (Sentry DSN, Amplitude key, Flagsmith env ID) — high business value, passive tes
- LEARN: ACCEPTED MISCONFIG @ hypofriend.de/property-search-api: GraphQL introspection enabled on production mortgage search API — high business value, passive testable
- LEARN: ACCEPTED IDOR @ hypofriend.de/property-search-api: `favoritedExposes(leadId)` resolver returns data for arbitrary unauthenticated leadId (200, no auth), exposin
- LEARN: ACCEPTED MISCONFIG @ hypofriend.de/property-search-api: Full GraphQL introspection enabled in production (Ruby, graphql-2.5.26) — schema + stack traces exposed;
- LEARN: ACCEPTED MISCONFIG @ hypofriend.de: Client-side secret exposure in Nuxt payload (Sentry DSN, Amplitude key, Flagsmith env ID) — high business value, passive tes
- LEARN: ACCEPTED ENDPOINT @ hypofriend.de/api/v3/advisors: Live HTTP Basic auth endpoint confirmed (401), only active API surface on main domain
- LEARN: REJECTED MISCONFIG @ api.hypofriend.de: Versioned API endpoints (api.hypofriend.de/api/v1 etc.) do not exist — subdomain unresponsive (timeout/000), not a misco
- LEARN: REJECTED MISCONFIG @ admin.hypofriend.de: Admin portal returns 503, not exposed with weak controls
- LEARN: REJECTED MISCONFIG @ core-api.hypofriend.de: GraphQL introspection not accessible — endpoint returns 503/timeout
- LEARN: REJECTED MISCONFIG @ graph.hypofriend.de: GraphQL introspection not accessible — endpoint returns 503
- LEARN: REJECTED OATH @ auth.hypofriend.de: OAuth/OpenID author from auth.hypofriend.de returns 503 (3 probes); not reachable passively, hypothesis parked not confirmed
- LEARN: ACCEPTED MISCONFIG @ hypofriend.de/property-search-api: GraphQL introspection enabled on production mortgage search API — high business value, passive testable
- LEARN: ACCEPTED IDOR @ hypofriend.de/property-search-api: `favoritedExposes(leadId)` resolver returns data for arbitrary unauthenticated leadId (200, no auth), exposin
- LEARN: ACCEPTED MISCONFIG @ hypofriend.de/property-search-api: Full GraphQL introspection enabled in production (Ruby, graphql-2.5.26) — schema + stack traces exposed;
- LEARN: ACCEPTED MISCONFIG @ hypofriend.de: Client-side secret exposure in Nuxt payload (Sentry DSN, Amplitude key, Flagsmith env ID) — high business value, passive tes
- LEARN: ACCEPTED ENDPOINT @ hypofriend.de/api/v3/advisors: Live HTTP Basic auth endpoint confirmed (401), only active API surface on main domain
- LEARN: CONFIRMED IDOR @ hypofriend.de/property-search-api: `favoritedExposes(leadId)` resolves for arbitrary unauthenticated leadId (200, zero-UUID and random-UUID acc
- LEARN: CONFIRMED IDOR @ hypofriend.de/property-search-api: `favoriteExpose(leadId,exposeId)` mutation executes a real write handler for arbitrary leadId with no auth (
- LEARN: CONFIRMED MISCONFIG @ hypofriend.de/property-search-api: `meta(id)` with nil leaks full Ruby backtrace (graphql-2.5.26, puma-7.2.0, rack-cors-3.0.0, sentry-ruby
- LEARN: REJECTED MISCONFIG @ api.hypofriend.de: Versioned API endpoints (api.hypofriend.de/api/v1 etc.) do not exist — subdomain unresponsive (timeout/000), not a misco
- LEARN: REJECTED MISCONFIG @ admin.hypofriend.de: Admin portal returns 503, not exposed with weak controls
- LEARN: REJECTED MISCONFIG @ core-api.hypofriend.de: GraphQL introspection not accessible — endpoint returns 503/timeout
- LEARN: REJECTED MISCONFIG @ graph.hypofriend.de: GraphQL introspection not accessible — endpoint returns 503
- LEARN: REJECTED OATH @ auth.hypofriend.de: OAuth/OpenID author returns 503 (multiple probes); not reachable passively
- LEARN: ACCEPTED MISCONFIG @ api.hypofriend.de: Versioned API endpoints are common misconfiguration, high business value.
- LEARN: ACCEPTED MISCONFIG @ admin.hypofriend.de: Admin portals often exposed with weak controls.
- LEARN: ACCEPTED MISCONFIG @ core-api.hypofriend.de: GraphQL introspection is common misconfiguration.
- LEARN: ACCEPTED MISCONFIG @ api.hypofriend.de: Versioned API endpoints are common misconfiguration, high business value.
- LEARN: ACCEPTED MISCONFIG @ admin.hypofriend.de: Admin portals often exposed with weak controls.
- LEARN: ACCEPTED MISCONFIG @ core-api.hypofriend.de: GraphQL introspection is common misconfiguration.
- LEARN: ACCEPTED MISCONFIG @ hypofriend.de: Client-side secret exposure in Nuxt payload (Sentry DSN, Amplitude key, Flagsmith env ID) — high business value, passive tes
- LEARN: REJECTED MISCONFIG @ api.hypofriend.de: Versioned API endpoints (api.hypofriend.de/api/v1 etc.) do not exist — subdomain unresponsive (000), not a misconfigurat
- LEARN: REJECTED MISCONFIG @ admin.hypofriend.de: Admin portal returns 503, not exposed with weak controls.
- LEARN: REJECTED MISCONFIG @ core-api.hypofriend.de: GraphQL introspection not accessible — endpoint returns 503.
- LEARN: REJECTED MISCONFIG @ graph.hypofriend.de: GraphQL introspection not accessible — endpoint returns 503/timeout (confirmed prior).
- LEARN: ACCEPTED IDOR @ hypofriend.de/property-search-api: `favoritedExposes(leadId)` resolver returns data for arbitrary unauthenticated leadId (200, no auth), exposin
- LEARN: ACCEPTED MISCONFIG @ hypofriend.de/property-search-api: Full GraphQL introspection enabled in production (Ruby, graphql-2.5.26) — schema + stack traces exposed;
- LEARN: REJECTED OATH @ auth.hypofriend.de: OAuth/OpenID author from auth.hypofriend.de returns 503 (3 probes); not reachable passively, hypothesis parked not confirmed
- LEARN: CONFIRMED IDOR @ hypofriend.de/property-search-api: `favoritedExposes(leadId)` resolves for arbitrary unauthenticated leadId (200, both zero-UUID and random-UUI
- LEARN: CONFIRMED IDOR @ hypofriend.de/property-search-api: `favoriteExpose(leadId,exposeId)` mutation executes a real write handler for arbitrary leadId with no auth (
- LEARN: CONFIRMED MISCONFIG @ hypofriend.de/property-search-api: `meta(id)` with bogus/nil leak returns full Ruby backtrace (graphql-2.5.26, puma-7.2.0, rack-cors-3.0.0
- LEARN: CONFIRMED IDOR @ hypofriend.de/property-search-api: `favoritedExposes(leadId)` resolves for arbitrary unauthenticated leadId (200, zero-UUID and random-UUID acc
- LEARN: CONFIRMED IDOR @ hypofriend.de/property-search-api: `favoriteExpose(leadId,exposeId)` mutation executes a real write handler for arbitrary leadId with no auth (
- LEARN: CONFIRMED MISCONFIG @ hypofriend.de/property-search-api: `meta(id)` with nil leaks full Ruby backtrace (graphql-2.5.26, puma-7.2.0, rack-cors-3.0.0, sentry-ruby
- LEARN: REJECTED OATH @ auth.hypofriend.de: OAuth/OpenID author returns 503 (multiple probes); not reachable passively.
- LEARN: ACCEPTED MISCONFIG @ hypofriend.de/property-search-api: GraphQL introspection enabled on production mortgage search API — high business value, passive testable
- LEARN: ACCEPTED IDOR @ hypofriend.de/property-search-api: `favoritedExposes(leadId)` resolver returns data for arbitrary unauthenticated leadId (200, no auth), exposin
- LEARN: ACCEPTED MISCONFIG @ hypofriend.de/property-search-api: Full GraphQL introspection enabled in production (Ruby, graphql-2.5.26) — schema + stack traces exposed;
- LEARN: ACCEPTED MISCONFIG @ hypofriend.de: Client-side secret exposure in Nuxt payload (Sentry DSN, Amplitude key, Flagsmith env ID) — high business value, passive tes
- LEARN: ACCEPTED ENDPOINT @ hypofriend.de/api/v3/advisors: Live HTTP Basic auth endpoint confirmed (401), only active API surface on main domain
- LEARN: CONFIRMED IDOR @ hypofriend.de/property-search-api: `favoritedExposes(leadId)` resolves for arbitrary unauthenticated leadId (200, zero-UUID and random-UUID acc
- LEARN: CONFIRMED IDOR @ hypofriend.de/property-search-api: `favoriteExpose(leadId,exposeId)` mutation executes a real write handler for arbitrary leadId with no auth (
- LEARN: CONFIRMED MISCONFIG @ hypofriend.de/property-search-api: `meta(id)` with nil leaks full Ruby backtrace (graphql-2.5.26, puma-7.2.0, rack-cors-3.0.0, sentry-ruby
- LEARN: REJECTED MISCONFIG @ api.hypofriend.de: Versioned API endpoints (api.hypofriend.de/api/v1 etc.) do not exist — subdomain unresponsive (timeout/000), not a misco
- LEARN: REJECTED MISCONFIG @ admin.hypofriend.de: Admin portal returns 503, not exposed with weak controls
- LEARN: REJECTED MISCONFIG @ core-api.hypofriend.de: GraphQL introspection not accessible — endpoint returns 503/timeout
- LEARN: REJECTED MISCONFIG @ graph.hypofriend.de: GraphQL introspection not accessible — endpoint returns 503
- LEARN: REJECTED OATH @ auth.hypofriend.de: OAuth/OpenID author returns 503 (multiple probes); not reachable passively

## RANKED HYPOTHESES 2026-09-04 18:34:20 UTC
- [85] hypofriend.de/property-search-api: Unauth'd expose(id) returns full PII of any enumerated listing (provider phone/email, owner surname, companies) (from art/lead_bigpickle.txt)
- [85] hypofriend.de/property-search-api: GraphQL BOLA/IDOR on property-search-api via expose/exposes — unauthenticated PII enumeration (from art/lead_nemotron3.txt)
- NEXT(hypotheses-bigpickle.txt): HUMAN: authorize one PII-field read (providerEmail, propertyOwnerLastName, cellPhoneNumber, ownerCompany) on a single real enumerated expose UUID (e.g. ad1d572e
- NEXT(hypotheses-nemotron3.txt): PROBE: POST https://hypofriend.de/property-search-api {"query":"{ expose(id: \"1\") { id title price city propertyOwnerLastName providerEmail providerCompany ce
- LEARN: CONFIRMED IDOR @ hypofriend.de/property-search-api: `expose(id)` resolver returns live listing data (200) for enumerated real expose UUID with NO auth and NO le
- LEARN: ACCEPTED MISCONFIG @ hypofriend.de/property-search-api: entire search lifecycle (propertySearch mutation, exposes listing) is unauthenticated, turning searchId 
- LEARN: ACCEPTED MISCONFIG @ hypofriend.de/property-search-api: GraphQL introspection enabled on production mortgage search API — high business value, passive testable
- LEARN: ACCEPTED IDOR @ hypofriend.de/property-search-api: `favoritedExposes(leadId)` resolver returns data for arbitrary unauthenticated leadId (200, no auth), exposin
- LEARN: ACCEPTED MISCONFIG @ hypofriend.de/property-search-api: Full GraphQL introspection enabled in production (Ruby, graphql-2.5.26) — schema + stack traces exposed;
- LEARN: ACCEPTED MISCONFIG @ hypofriend.de: Client-side secret exposure in Nuxt payload (Sentry DSN, Amplitude key, Flagsmith env ID) — high business value, passive tes
- LEARN: ACCEPTED ENDPOINT @ hypofriend.de/api/v3/advisors: Live HTTP Basic auth endpoint confirmed (401), only active API surface on main domain
- LEARN: CONFIRMED IDOR @ hypofriend.de/property-search-api: `favoritedExposes(leadId)` resolves for arbitrary unauthenticated leadId (200, zero-UUID and random-UUID acc
- LEARN: CONFIRMED IDOR @ hypofriend.de/property-search-api: `favoriteExpose(leadId,exposeId)` mutation executes a real write handler for arbitrary leadId with no auth (
- LEARN: CONFIRMED MISCONFIG @ hypofriend.de/property-search-api: `meta(id)` with nil leaks full Ruby backtrace (graphql-2.5.26, puma-7.2.0, rack-cors-3.0.0, sentry-ruby
- LEARN: REJECTED MISCONFIG @ api.hypofriend.de: Versioned API endpoints (api.hypofriend.de/api/v1 etc.) do not exist — subdomain unresponsive (timeout/000), not a misco
- LEARN: REJECTED MISCONFIG @ admin.hypofriend.de: Admin portal returns 503, not exposed with weak controls
- LEARN: REJECTED MISCONFIG @ core-api.hypofriend.de: GraphQL introspection not accessible — endpoint returns 503/timeout
- LEARN: REJECTED MISCONFIG @ graph.hypofriend.de: GraphQL introspection not accessible — endpoint returns 503
- LEARN: REJECTED OATH @ auth.hypofriend.de: OAuth/OpenID author returns 503 (multiple probes); not reachable passively

## RANKED HYPOTHESES 2026-09-04 21:05:40 UTC
- [95] hypofriend.de/property-search-api: GraphQL BOLA/IDOR on property-search-api via expose/exposes — unauthenticated PII enumeration (from art/lead_nemotron3.txt)
- NEXT(hypotheses-nemotron3.txt): PROBE: POST https://hypofriend.de/property-search-api {"query":"{ expose(id: \"ad1d572e-...\") { id title price city propertyOwnerLastName providerEmail provide
- LEARN: ACCEPTED MISCONFIG @ hypofriend.de/property-search-api: Full search lifecycle (propertySearch mutation, exposes listing) is unauthenticated, turning searchId in
- LEARN: CONFIRMED IDOR @ hypofriend.de/property-search-api: `expose(id)` resolver returns live listing data (200) for enumerated real expose UUID with NO auth and NO le
- LEARN: ACCEPTED MISCONFIG @ hypofriend.de/property-search-api: Expose type PII surface confirmed on auth-free object — cellPhoneNumber, phoneNumber, propertyOwnerLastN

## RANKED HYPOTHESES 2026-09-04 23:06:55 UTC
- [98] hypofriend.de/property-search-api: GraphQL BOLA/IDOR on property-search-api via expose/exposes/propertySearch chain — unauthenticated PII enumeration at scale (from art/lead_nemotron3.txt)
- [90] hypofriend.de/property-search-api: Auth-free expose(id) returns full broker/owner PII for any enumerated listing (from art/lead_bigpickle.txt)
- NEXT(hypotheses-bigpickle.txt): HUMAN: authorize the single PII-field read on ad1d572e-8c01-5d07-a8ff-14b1a3af7d21 — `{expose(id:"ad1d572e-8c01-5d07-a8ff-14b1a3af7d21"){id title price provider
- NEXT(hypotheses-nemotron3.txt): PROBE: POST https://hypofriend.de/property-search-api {"query":"{ expose(id: \"ad1d572e-...\") { id title price city propertyOwnerLastName providerEmail provide
- LEARN: ACCEPTED IDOR @ hypofriend.de/property-search-api: `expose(id)` resolver returns live listing data (200) for enumerated real expose UUID with NO auth and NO lea
- LEARN: ACCEPTED MISCONFIG @ hypofriend.de/property-search-api: Full search lifecycle (propertySearch mutation, exposes listing) is unauthenticated, turning searchId in
- LEARN: ACCEPTED MISCONFIG @ hypofriend.de/property-search-api: Expose type PII surface confirmed on auth-free object — cellPhoneNumber, phoneNumber, propertyOwnerLastN
- LEARN: ACCEPTED MISCONFIG @ hypofriend.de/property-search-api: GraphQL introspection enabled on production mortgage search API — high business value, passive testable
- LEARN: CONFIRMED IDOR @ hypofriend.de/property-search-api: `favoritedExposes(leadId)` resolves for arbitrary unauthenticated leadId (200, zero-UUID and random-UUID acc
- LEARN: CONFIRMED IDOR @ hypofriend.de/property-search-api: `favoriteExpose(leadId,exposeId)` mutation executes a real write handler for arbitrary leadId with no auth (
- LEARN: CONFIRMED MISCONFIG @ hypofriend.de/property-search-api: `meta(id)` with nil leaks full Ruby backtrace (graphql-2.5.26, puma-7.2.0, rack-cors-3.0.0, sentry-ruby
- LEARN: REJECTED MISCONFIG @ api.hypofriend.de: Versioned API endpoints (api.hypofriend.de/api/v1 etc.) do not exist — subdomain unresponsive (timeout/000), not a misco
- LEARN: REJECTED MISCONFIG @ admin.hypofriend.de: Admin portal returns 503, not exposed with weak controls
- LEARN: REJECTED MISCONFIG @ core-api.hypofriend.de: GraphQL introspection not accessible — endpoint returns 503/timeout
- LEARN: REJECTED MISCONFIG @ graph.hypofriend.de: GraphQL introspection not accessible — endpoint returns 503
- LEARN: REJECTED OATH @ auth.hypofriend.de: OAuth/OpenID author returns 503 (multiple probes); not reachable passively

## RANKED HYPOTHESES 2026-09-05 01:04:07 UTC
- [98] hypofriend.de/property-search-api: GraphQL BOLA/IDOR on property-search-api via expose/exposes/propertySearch chain — unauthenticated PII enumeration at scale (from art/lead_nemotron3.txt)
- [90] hypofriend.de/property-search-api: Auth-free expose(id) returns full broker/owner PII for any enumerated listing (from art/lead_bigpickle.txt)
- NEXT(hypotheses-bigpickle.txt): HUMAN: authorize the single PII-field read on ad1d572e-8c01-5d07-a8ff-14b1a3af7d21 — `{expose(id:"ad1d572e-8c01-5d07-a8ff-14b1a3af7d21"){id title price provider
- NEXT(hypotheses-nemotron3.txt): PROBE: POST https://hypofriend.de/property-search-api {"query":"{ expose(id: \"ad1d572e-8c01-5d07-a8ff-14b1a3af7d21\") { id title price city propertyOwnerLastNa
- LEARN: CONFIRMED IDOR @ hypofriend.de/property-search-api: `expose(id)` resolver returns live listing data (200) for enumerated real expose UUID with NO auth and NO le
- LEARN: ACCEPTED MISCONFIG @ hypofriend.de/property-search-api: entire search lifecycle (propertySearch mutation, exposes listing) is unauthenticated, turning searchId 
- LEARN: ACCEPTED IDOR @ hypofriend.de/property-search-api: expose(id) resolver returns live listing data (200) for enumerated real expose UUID with NO auth and NO leadI
- LEARN: ACCEPTED MISCONFIG @ hypofriend.de/property-search-api: Full search lifecycle (propertySearch mutation, exposes listing) is unauthenticated, turning searchId in
- LEARN: ACCEPTED MISCONFIG @ hypofriend.de/property-search-api: Expose type PII surface confirmed on auth-free object — cellPhoneNumber, phoneNumber, propertyOwnerLastN
- LEARN: ACCEPTED MISCONFIG @ hypofriend.de/property-search-api: GraphQL introspection enabled on production mortgage search API — high business value, passive testable
- LEARN: CONFIRMED IDOR @ hypofriend.de/property-search-api: favoritedExposes(leadId) resolves for arbitrary unauthenticated leadId (200, zero-UUID and random-UUID accep
- LEARN: CONFIRMED IDOR @ hypofriend.de/property-search-api: favoriteExpose(leadId,exposeId) mutation executes a real write handler for arbitrary leadId with no auth (er
- LEARN: CONFIRMED MISCONFIG @ hypofriend.de/property-search-api: meta(id) with nil leaks full Ruby backtrace (graphql-2.5.26, puma-7.2.0, rack-cors-3.0.0, sentry-ruby-6
- LEARN: ACCEPTED MISCONFIG @ hypofriend.de: Client-side secret exposure in Nuxt payload (Sentry DSN, Amplitude key, Flagsmith env ID) — high business value, passive tes
- LEARN: ACCEPTED ENDPOINT @ hypofriend.de/api/v3/advisors: Live HTTP Basic auth endpoint confirmed (401), only active API surface on main domain
- LEARN: REJECTED MISCONFIG @ api.hypofriend.de: Versioned API endpoints (api.hypofriend.de/api/v1 etc.) do not exist — subdomain unresponsive (timeout/000), not a misco
- LEARN: REJECTED MISCONFIG @ admin.hypofriend.de: Admin portal returns 503, not exposed with weak controls
- LEARN: REJECTED MISCONFIG @ core-api.hypofriend.de: GraphQL introspection not accessible — endpoint returns 503/timeout
- LEARN: REJECTED MISCONFIG @ graph.hypofriend.de: GraphQL introspection not accessible — endpoint returns 503
- LEARN: REJECTED OATH @ auth.hypofriend.de: OAuth/OpenID author returns 503 (multiple probes); not reachable passively

## RANKED HYPOTHESES 2026-09-05 06:00:39 UTC
- [99] hypofriend.de/property-search-api: GraphQL BOLA/IDOR via expose/exposes/propertySearch chain — unauthenticated PII enumeration at scale (from art/lead_nemotron3.txt)
- [90] hypofriend.de/property-search-api: Auth-free expose(id) returns full broker/owner PII for any enumerated listing (from art/lead_bigpickle.txt)
- NEXT(hypotheses-bigpickle.txt): HUMAN: authorize the single PII-field read on ad1d572e-8c01-5d07-a8ff-14b1a3af7d21 — `POST https://hypofriend.de/property-search-api {"query":"{expose(id:\"ad1d
- NEXT(hypotheses-nemotron3.txt): PROBE: POST https://hypofriend.de/property-search-api {"query":"mutation{propertySearch(city:\"MUNICH\",propertyType:APARTMENT){searchId}}"} → enumerate exposes
- LEARN: ACCEPTED IDOR @ hypofriend.de/property-search-api: expose(id) returns live PII (200) for enumerated UUIDs with NO auth/leadId — full-DB auth-free read oracle; I
- LEARN: ACCEPTED MISCONFIG @ hypofriend.de/property-search-api: Full search lifecycle (propertySearch, exposes) unauthenticated — searchId is public enumeration primiti
- LEARN: ACCEPTED MISCONFIG @ hypofriend.de/property-search-api: Expose type PII surface confirmed — cellPhoneNumber, phoneNumber, propertyOwnerLastName, providerEmail, 
- LEARN: ACCEPTED MISCONFIG @ hypofriend.de/property-search-api: GraphQL introspection enabled in production (graphql-2.5.26)
- LEARN: CONFIRMED IDOR @ hypofriend.de/property-search-api: favoritedExposes(leadId) resolves for arbitrary unauthenticated leadId (200) — auth-free read oracle
- LEARN: CONFIRMED IDOR @ hypofriend.de/property-search-api: favoriteExpose(leadId,exposeId) executes write handler for arbitrary leadId (error proves code path) — cross
- LEARN: CONFIRMED MISCONFIG @ hypofriend.de/property-search-api: meta(id) with bogus leaks full Ruby backtrace (graphql-2.5.26, puma-7.2.0, rack-cors-3.0.0, sentry-ruby
- LEARN: CONFIRMED MISCONFIG @ hypofriend.de/property-search-api: informationRequest missing advisor_email leaks /app/app/mutations/information_request.rb:53 backtrace
- LEARN: ACCEPTED MISCONFIG @ hypofriend.de: Client-side secret exposure in Nuxt payload (Sentry DSN, Amplitude key, Flagsmith env ID) — passive testable
- LEARN: ACCEPTED ENDPOINT @ hypofriend.de/api/v3/advisors: Live HTTP Basic auth (401), only active API surface on main domain
- LEARN: REJECTED MISCONFIG @ api.hypofriend.de/core-api.hypofriend.de/graph.hypofriend.de/auth.hypofriend.de/admin.hypofriend.de/portal.hypofriend.de/dashboard.hypofrie

## RANKED HYPOTHESES 2026-09-05 09:51:38 UTC
- [99] hypofriend.de/property-search-api: GraphQL BOLA/IDOR via expose/exposes/propertySearch chain — unauthenticated PII enumeration at scale (from art/lead_nemotron3.txt)
- [90] hypofriend.de/property-search-api: Auth-free expose(id) returns full broker/owner PII for any enumerated listing (from art/lead_bigpickle.txt)
- NEXT(hypotheses-bigpickle.txt): HUMAN: authorize the single PII-field read on ad1d572e-8c01-5d07-a8ff-14b1a3af7d21 — `POST https://hypofriend.de/property-search-api {"query":"{expose(id:\"ad1d
- NEXT(hypotheses-nemotron3.txt): PROBE: POST https://hypofriend.de/property-search-api {"query":"mutation{propertySearch(city:\"HAMBURG\",propertyType:APARTMENT){searchId}}"} → enumerate expose
- LEARN: ACCEPTED IDOR @ hypofriend.de/property-search-api: expose(id) returns live PII (200) for enumerated UUIDs with NO auth/leadId — full-DB auth-free read oracle; I
- LEARN: ACCEPTED MISCONFIG @ hypofriend.de/property-search-api: Full search lifecycle (propertySearch, exposes) unauthenticated — searchId is public enumeration primiti
- LEARN: ACCEPTED MISCONFIG @ hypofriend.de/property-search-api: Expose type PII surface confirmed — cellPhoneNumber, phoneNumber, propertyOwnerLastName, providerEmail, 
- LEARN: ACCEPTED MISCONFIG @ hypofriend.de/property-search-api: GraphQL introspection enabled in production (graphql-2.5.26)
- LEARN: ACCEPTED MISCONFIG @ hypofriend.de: Client-side secret exposure in Nuxt payload — passive testable
- LEARN: ACCEPTED ENDPOINT @ hypofriend.de/api/v3/advisors: Live HTTP Basic auth (401), only active API surface on main domain
- LEARN: CONFIRMED IDOR @ hypofriend.de/property-search-api: favoritedExposes(leadId) resolves for arbitrary unauthenticated leadId (200) — auth-free read oracle
- LEARN: CONFIRMED IDOR @ hypofriend.de/property-search-api: favoriteExpose(leadId,exposeId) executes write handler for arbitrary leadId (error proves code path) — cross
- LEARN: CONFIRMED MISCONFIG @ hypofriend.de/property-search-api: meta(id) with bogus leaks full Ruby backtrace (graphql-2.5.26, puma-7.2.0, rack-cors-3.0.0, sentry-ruby
- LEARN: CONFIRMED MISCONFIG @ hypofriend.de/property-search-api: informationRequest missing advisor_email leaks /app/app/mutations/information_request.rb:53 backtrace
- LEARN: REJECTED MISCONFIG @ api.hypofriend.de/core-api.hypofriend.de/graph.hypofriend.de/auth.hypofriend.de/admin.hypofriend.de/portal.hypofriend.de/dashboard.hypofrie
- LEARN: ACCEPTED IDOR @ hypofriend.de/property-search-api: expose(id) returns live PII (200) for enumerated UUIDs with NO auth/leadId — full-DB auth-free read oracle; I
- LEARN: ACCEPTED MISCONFIG @ hypofriend.de/property-search-api: Full search lifecycle (propertySearch, exposes) unauthenticated — searchId is public enumeration primiti
- LEARN: ACCEPTED MISCONFIG @ hypofriend.de/property-search-api: Expose type PII surface confirmed — cellPhoneNumber, phoneNumber, propertyOwnerLastName, providerEmail, 
- LEARN: ACCEPTED MISCONFIG @ hypofriend.de/property-search-api: GraphQL introspection enabled in production (graphql-2.5.26)
- LEARN: CONFIRMED IDOR @ hypofriend.de/property-search-api: favoritedExposes(leadId) resolves for arbitrary unauthenticated leadId (200) — auth-free read oracle
- LEARN: CONFIRMED IDOR @ hypofriend.de/property-search-api: favoriteExpose(leadId,exposeId) executes write handler for arbitrary leadId (error proves code path) — cross
- LEARN: CONFIRMED MISCONFIG @ hypofriend.de/property-search-api: meta(id) with bogus leaks full Ruby backtrace (graphql-2.5.26, puma-7.2.0, rack-cors-3.0.0, sentry-ruby
- LEARN: CONFIRMED MISCONFIG @ hypofriend.de/property-search-api: informationRequest missing advisor_email leaks /app/app/mutations/information_request.rb:53 backtrace
- LEARN: ACCEPTED MISCONFIG @ hypofriend.de: Client-side secret exposure in Nuxt payload (Sentry DSN, Amplitude key, Flagsmith env ID) — passive testable
- LEARN: ACCEPTED ENDPOINT @ hypofriend.de/api/v3/advisors: Live HTTP Basic auth (401), only active API surface on main domain
- LEARN: REJECTED MISCONFIG @ api.hypofriend.de/core-api.hypofriend.de/graph.hypofriend.de/auth.hypofriend.de/admin.hypofriend.de/portal.hypofriend.de/dashboard.hypofrie
- LEARN: REJECTED OATH @ auth.hypofriend.de: OAuth/OpenID author returns 503 (multiple probes); not reachable passively
