## 2026-09-03 15:38:53 UTC [target] (model bigpickle)
[PRIO] api.hypofriend.de,9.2,attack_surface=9 business_value=10 tech_exposure=8 gate_ease=10 cloud_surface=8 freshness=9
[PRIO] admin.hypofriend.de,8.8,attack_surface=9 business_value=9 tech_exposure=9 gate_ease=7 cloud_surface=8 freshness=9
[PRIO] auth.hypofriend.de,8.5,attack_surface=8 business_value=10 tech_exposure=8 gate_ease=5 cloud_surface=8 freshness=9
[PRIO] core-api.hypofriend.de,8.3,attack_surface=8 business_value=9 tech_exposure=8 gate_ease=6 cloud_surface=8 freshness=9
[PRIO] staging.hypofriend.de,7.8,attack_surface=8 business_value=7 tech_exposure=7 gate_ease=9 cloud_surface=7 freshness=9
[PRIO] documents.hypofriend.de,7.5,attack_surface=7 business_value=8 tech_exposure=7 gate_ease=6 cloud_surface=7 freshness=9
[HYP] API versioning/bypass on api.hypofriend.de
class: MISCONFIG
asset: api.hypofriend.de
confidence: 68
reasoning: Versioned API endpoints (/api/v1, /api/v2, /api/beta, /api/internal) often expose legacy or privileged endpoints. Target is explicitly "api". No prior probes on this host.
evidence_needed: Response from GET /api/, /api/v1/, /api/v2/, /api/beta/, /api/internal/, /api/swagger, /api/openapi.json, /api/docs
verify_steps: GET https://api.hypofriend.de/, GET https://api.hypofriend.de/api/, GET https://api.hypofriend.de/api/v1/, GET https://api.hypofriend.de/api/v2/, GET https://api.hypofriend.de/api/beta/, GET https://api.hypofriend.de/api/internal/, GET https://api.hypofriend.de/api/swagger, GET https://api.hypofriend.de/api/openapi.json, GET https://api.hypofriend.de/api/docs
impact: Information disclosure, legacy endpoint access, potential privilege escalation. Severity: MEDIUM
testability: PASSIVE
[HYP] GraphQL introspection on core-api.hypofriend.de
class: MISCONFIG
asset: core-api.hypofriend.de
confidence: 62
reasoning: GraphQL endpoints often left open for introspection, exposing entire schema. "core-api" suggests backend service. Financial recommendation engine likely uses GraphQL for complex queries.
evidence_needed: Response from POST /graphql with introspection query, GET /graphql
verify_steps: GET https://core-api.hypofriend.de/graphql, POST https://core-api.hypofriend.de/graphql with {"query":"{__schema{types{name,fields{name}}}}"}
impact: Full schema disclosure, potential mutation access to financial data. Severity: HIGH
testability: PASSIVE
[HYP] Admin panel exposure on admin.hypofriend.de
class: MISCONFIG
asset: admin.hypofriend.de
confidence: 65
reasoning: Admin portals often have weaker access controls, debug endpoints, or default credentials. "admin" subdomain likely internal tooling exposed to internet.
evidence_needed: Login page, API endpoints, debug endpoints (/admin/api, /admin/debug, /admin/health)
verify_steps: GET https://admin.hypofriend.de/, GET https://admin.hypofriend.de/api, GET https://admin.hypofriend.de/debug, GET https://admin.hypofriend.de/health
impact: Administrative access to platform, customer data, financial systems. Severity: CRITICAL
testability: AUTH_HELPED
[PARKED] API versioning/bypass on api.hypofriend.de: Confidence 68 > 40, class MISCONFIG not REJECTED. Verified.
[PARKED] GraphQL introspection on core-api.hypofriend.de: Confidence 62 > 40, class MISCONFIG not REJECTED. Verified.
[PARKED] Admin panel exposure on admin.hypofriend.de: Confidence 65 > 40, class MISCONFIG not REJECTED. Verified.
[FINAL] Survivors ranked:
[NEXT] PROBE: GET https://api.hypofriend.de/, GET https://api.hypofriend.de/api/, GET https://api.hypofriend.de/api/v1/, GET https://api.hypofriend.de/api/v2/, GET https://api.hypofriend.de/api/beta/, GET https://api.hypofriend.de/api/internal/, GET https://api.hypofriend.de/api/swagger, GET https://api.hypofriend.de/api/openapi.json, GET https://api.hypofriend.de/api/docs (passive, ≤1 rps)
[LEARN] ACCEPTED MISCONFIG @ api.hypofriend.de: Versioned API endpoints are common misconfiguration, high business value.
[LEARN] ACCEPTED MISCONFIG @ admin.hypofriend.de: Admin portals often exposed with weak controls.
[LEARN] ACCEPTED MISCONFIG @ core-api.hypofriend.de: GraphQL introspection is common misconfiguration.
[RISK] hypofriend: 75 High business value (financial platform), moderate attack surface, API-focused target. SSRF/IDOR on financial flows would be critical.
## 2026-09-03 18:53:43 UTC [target] (model bigpickle)
[PRIO] api.hypofriend.de,9.2,attack_surface=9 business_value=10 tech_exposure=8 gate_ease=10 cloud_surface=8 freshness=9
[PRIO] admin.hypofriend.de,8.8,attack_surface=9 business_value=9 tech_exposure=9 gate_ease=7 cloud_surface=8 freshness=9
[PRIO] auth.hypofriend.de,8.5,attack_surface=8 business_value=10 tech_exposure=8 gate_ease=5 cloud_surface=8 freshness=9
[PRIO] graph.hypofriend.de,8.5,attack_surface=8 business_value=9 tech_exposure=10 gate_ease=7 cloud_surface=8 freshness=9
[PRIO] core-api.hypofriend.de,8.3,attack_surface=8 business_value=9 tech_exposure=8 gate_ease=6 cloud_surface=8 freshness=9
[HYP] API versioning/bypass on api.hypofriend.de
class: MISCONFIG
asset: api.hypofriend.de
confidence: 68
reasoning: Versioned API endpoints (/api/v1, /api/v2, /api/beta, /api/internal) often expose legacy or privileged endpoints. Target is explicitly "api". No prior probes on this host.
evidence_needed: Response from GET /api/, /api/v1/, /api/v2/, /api/beta/, /api/internal/, /api/swagger, /api/openapi.json, /api/docs
verify_steps: GET https://api.hypofriend.de/, GET https://api.hypofriend.de/api/, GET https://api.hypofriend.de/api/v1/, GET https://api.hypofriend.de/api/v2/, GET https://api.hypofriend.de/api/beta/, GET https://api.hypofriend.de/api/internal/, GET https://api.hypofriend.de/api/swagger, GET https://api.hypofriend.de/api/openapi.json, GET https://api.hypofriend.de/api/docs
impact: Information disclosure, legacy endpoint access, potential privilege escalation. Severity: MEDIUM
testability: PASSIVE
[HYP] Admin panel exposure on admin.hypofriend.de
class: MISCONFIG
asset: admin.hypofriend.de
confidence: 65
reasoning: Admin portals often have weaker access controls, debug endpoints, or default credentials. "admin" subdomain likely internal tooling exposed to internet.
evidence_needed: Login page, API endpoints, debug endpoints (/admin/api, /admin/debug, /admin/health)
verify_steps: GET https://admin.hypofriend.de/, GET https://admin.hypofriend.de/api, GET https://admin.hypofriend.de/debug, GET https://admin.hypofriend.de/health
impact: Administrative access to platform, customer data, financial systems. Severity: CRITICAL
testability: AUTH_HELPED
[HYP] OAuth redirect_uri manipulation on auth.hypofriend.de
class: OATH
asset: auth.hypofriend.de
confidence: 60
reasoning: Auth endpoints often have OAuth flows with redirect_uri parameters that may be misvalidated, leading to code theft or open redirect.
evidence_needed: OAuth endpoints, redirect_uri parameter behavior.
verify_steps: GET https://auth.hypofriend.de/.well-known/openid-configuration, GET https://auth.hypofriend.de/authorize?response_type=code&client_id=test&redirect_uri=https://example.com&scope=openid
impact: Account takeover via OAuth code interception. Severity: HIGH
testability: PASSIVE
[PARKED] API versioning/bypass on api.hypofriend.de: Confidence 68 > 40, class MISCONFIG not REJECTED. Verified.
[PARKED] Admin panel exposure on admin.hypofriend.de: Confidence 65 > 40, class MISCONFIG not REJECTED. Verified.
[PARKED] OAuth redirect_uri manipulation on auth.hypofriend.de: Confidence 60 > 40, class OATH not REJECTED. Verified.
[FINAL] Survivors ranked:
[NEXT] PROBE: GET https://api.hypofriend.de/, GET https://api.hypofriend.de/api/, GET https://api.hypofriend.de/api/v1/, GET https://api.hypofriend.de/api/v2/, GET https://api.hypofriend.de/api/beta/, GET https://api.hypofriend.de/api/internal/, GET https://api.hypofriend.de/api/swagger, GET https://api.hypofriend.de/api/openapi.json, GET https://api.hypofriend.de/api/docs (passive, ≤1 rps)
[LEARN] ACCEPTED MISCONFIG @ api.hypofriend.de: Versioned API endpoints are common misconfiguration, high business value.
[LEARN] ACCEPTED MISCONFIG @ admin.hypofriend.de: Admin portals often exposed with weak controls.
[LEARN] ACCEPTED MISCONFIG @ core-api.hypofriend.de: GraphQL introspection is common misconfiguration.
[RISK] hypofriend: 75 High business value (financial platform), moderate attack surface, API-focused target. SSRF/IDOR on financial flows would be critical.
