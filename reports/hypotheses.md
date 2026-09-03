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
