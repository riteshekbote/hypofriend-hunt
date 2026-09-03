## 2026-09-03 15:49:33 UTC [target] (model nemotron3)
[NEW] api.hypofriend.de — primary API endpoint unprobed
[NEW] core-api.hypofriend.de — internal/core API unprobed
[NEW] graph.hypofriend.de — GraphQL endpoint unprobed
[NEW] graph-rates.hypofriend.de — GraphQL rates API unprobed
[NEW] v3.hypofriend.de — versioned API unprobed
[NEW] auth.hypofriend.de — auth/OAuth endpoint unprobed
[NEW] login.hypofriend.de — login endpoint unprobed
[NEW] sso.hypofriend.de — SSO endpoint unprobed
[NEW] admin.hypofriend.de — admin panel unprobed
[NEW] admin.app.hypofriend.de — admin app unprobed
[NEW] portal.hypofriend.de — customer portal unprobed
[NEW] dashboard.hypofriend.de — dashboard unprobed
[NEW] billing.hypofriend.de — billing/financial API unprobed
[NEW] offer.hypofriend.de — mortgage offer API unprobed
[NEW] documents.hypofriend.de — document API unprobed
[NEW] my.hypofriend.de — user portal unprobed
[NEW] profile.hypofriend.de — profile API unprobed
[NEW] account.hypofriend.de — account API unprobed
[CHANGED] bonava.hypofriend.de, myne.hypofriend.de, evernest.hypofriend.de — confirmed live (200) but CNAME to Heyflow (marketing), not core API
[PRIO] graph.hypofriend.de,8.25,attack_surface=9,business_value=9,tech_exposure=10,gate_ease=6,cloud_surface=7,freshness=6
[PRIO] api.hypofriend.de,8.0,attack_surface=9,business_value=10,tech_exposure=8,gate_ease=5,cloud_surface=7,freshness=6
[PRIO] core-api.hypofriend.de,7.5,attack_surface=8,business_value=9,tech_exposure=9,gate_ease=4,cloud_surface=7,freshness=6
[PRIO] auth.hypofriend.de,7.45,attack_surface=8,business_value=8,tech_exposure=8,gate_ease=7,cloud_surface=6,freshness=6
[PRIO] graph-rates.hypofriend.de,7.4,attack_surface=8,business_value=9,tech_exposure=9,gate_ease=5,cloud_surface=7,freshness=6
[PRIO] v3.hypofriend.de,7.2,attack_surface=8,business_value=8,tech_exposure=8,gate_ease=5,cloud_surface=7,freshness=6
[PRIO] admin.hypofriend.de,6.7,attack_surface=7,business_value=9,tech_exposure=7,gate_ease=3,cloud_surface=6,freshness=6
[PRIO] billing.hypofriend.de,6.5,attack_surface=7,business_value=9,tech_exposure=7,gate_ease=4,cloud_surface=6,freshness=6
[HYP] GraphQL Introspection & Field-Level Auth Bypass
class: MISCONFIG
asset: graph.hypofriend.de
confidence: 70
reasoning: GraphQL endpoints often have introspection enabled in non-prod; financial rates API may expose sensitive pricing logic; field-level auth often missing on derived/computed fields
evidence_needed: Introspection query returns full schema; sensitive fields (pricing, user data, internal IDs) accessible without proper auth
verify_steps: GET https://graph.hypofriend.de/graphql with introspection query; POST https://graph.hypofriend.de/graphql with mutation probes; Test field-level access on User/Offer types
impact: Full schema dump -> enumerate all mutations/queries -> IDOR/BOLA on financial data -> PII exposure -> pricing manipulation
testability: PASSIVE
[HYP] JWT Algorithm/Key Confusion on Primary API
class: AUTH
asset: api.hypofriend.de
confidence: 60
reasoning: Mortgage platform APIs typically use JWT for stateless auth; RS256->HS256 confusion common; JWKS endpoint may be exposed; algorithm not validated
evidence_needed: JWKS endpoint accessible; token validation accepts HS256 when RS256 expected; public key usable as HMAC secret
verify_steps: GET https://api.hypofriend.de/.well-known/jwks.json; Capture valid JWT from login flow; Test alg confusion with public key as HS256 secret
impact: Token forgery -> ATO on any user -> mortgage data access -> financial fraud
testability: AUTH_HELPED
[HYP] IDOR/BOLA on Core API Offer/User Endpoints
class: IDOR
asset: core-api.hypofriend.de
confidence: 65
reasoning: Core API likely serves mortgage offers, user profiles, documents; sequential UUIDs or integer IDs common; tenant isolation often missing in multi-tenant mortgage platforms
evidence_needed: Authenticated access to /offers/{id} or /users/{id} returns other users' data; cross-tenant access possible
verify_steps: Enumerate API endpoints via OPTIONS/swagger on core-api.hypofriend.de; Test sequential ID access on offers/users/documents with two test accounts
impact: Cross-user mortgage data access -> PII, financial data, documents -> regulatory violation (GDPR, financial regs)
testability: AUTH_HELPED
[FINAL] 1. GraphQL Introspection & Field-Level Auth Bypass (graph.hypofriend.de) — confidence 70, PASSIVE testable
[FINAL] 2. IDOR/BOLA on Core API Offer/User Endpoints (core-api.hypofriend.de) — confidence 65, AUTH_HELPED
[FINAL] 3. JWT Algorithm/Key Confusion on Primary API (api.hypofriend.de) — confidence 60, AUTH_HELPED
[NEXT] PROBE: GET https://graph.hypofriend.de/graphql?query=%7B__schema%7Btypes%7Bname%2Cfields%7Bname%7D%7D%7D%7D
[LEARN] FIRST_RUN — no prior hypotheses to accept/reject; baseline established from passive DNS/CT inventory
[RISK] hypofriend: 75 — High-value mortgage/financial platform with unprobed API surface (api.*, core-api.*, graph.*) handling sensitive PII and financial data; GraphQL and JWT attack surface likely; Heyflow subdomains indicate marketing funnel separation but core APIs untested
