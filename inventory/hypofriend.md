# Hypofriend GmbH inventory (discovery seed 2026-09-02)
# NOTE: hosts below are discovery candidates from passive DNS/CT; confirm in-scope vs program scope before active testing.
a.hypofriend.de
accentro.hypofriend.de
account.hypofriend.de
admin.app.hypofriend.de
admin.hypofriend.de
api.hypofriend.de
app.hypofriend.de
appointments.app.hypofriend.de
auth.hypofriend.de
berater-suche.hypofriend.de
billing.hypofriend.de
blog-admin.hypofriend.de
blog.hypofriend.de
bonava.hypofriend.de
bot.hypofriend.de
cdn.hypofriend.de
core-api.hypofriend.de
core.hypofriend.de
dashboard.hypofriend.de
demo.hypofriend.de
dev.hypofriend.de
dev1.hypofriend.de
dns.hypofriend.de
documents.hypofriend.de
email.m.hypofriend.de
email.m2.hypofriend.de
evernest.hypofriend.de
experiments.hypofriend.de
frontend.app.hypofriend.de
funnels.hypofriend.de
graph-rates.hypofriend.de
graph.hypofriend.de
heyflow.hypofriend.de
hypofriend.de
images.hypofriend.de
jenkins.hypofriend.de
kajsa.local.hypofriend.de
kubernetes.hypofriend.de
landingpage.hypofriend.de
laurence.local.hypofriend.de
listings.hypofriend.de
local.hypofriend.de
login.hypofriend.de
m2.hypofriend.de
mail.hypofriend.de
mobile.hypofriend.de
my.hypofriend.de
myne.hypofriend.de
news.hypofriend.de
newsletter.hypofriend.de
offer.hypofriend.de
pavel.local.hypofriend.de
pipedrive-sync.hypofriend.de
portal.hypofriend.de
profile.app.hypofriend.de
profile.hypofriend.de
relay.m.hypofriend.de
root.hypofriend.de
secure.hypofriend.de
sofia.local.hypofriend.de
sparplan.hypofriend.de
sso.hypofriend.de
staging.hypofriend.de
support.hypofriend.de
test.hypofriend.de
tiago.local.hypofriend.de
uploader.app.hypofriend.de
v3.hypofriend.de
web.hypofriend.de
wildcard.hypofriend.de
www.hypofriend.de

## PASSIVE RECON 2026-09-02 (read-only, non-intrusive)

> Recon observations only. These are NOT confirmed vulnerabilities; ownership/in-scope of each host must be confirmed against the program scope before any active testing. Hosts resolve + serve HTTP — investigation requires scoped authorization.

**Probed:** 71 hosts | **Live HTTP:** 10

| Host | Status | Server/Tech |
|---|---|---|
| `kajsa.local.hypofriend.de` | 404 | - |
| `laurence.local.hypofriend.de` | 404 | - |
| `email.m.hypofriend.de` | 404 | - |
| `pavel.local.hypofriend.de` | 404 | - |
| `tiago.local.hypofriend.de` | 404 | - |
| `sofia.local.hypofriend.de` | 404 | - |
| `email.m2.hypofriend.de` | 404 | - |
| `bonava.hypofriend.de` | 200 | Server: cloudflare; Via: 1.1 google |
| `myne.hypofriend.de` | 200 | Server: cloudflare; Via: 1.1 google |
| `evernest.hypofriend.de` | 200 | Server: cloudflare; Via: 1.1 google |

**CNAME review signals (14):**
- `accentro.hypofriend.de` -> `flow.heyflow.domains`
- `berater-suche.hypofriend.de` -> `flow.heyflow.domains`
- `kajsa.local.hypofriend.de` -> `jtkfqjar.cname.eu.ngrok.io`
- `laurence.local.hypofriend.de` -> `jtkfqjar.cname.eu.ngrok.io`
- `email.m.hypofriend.de` -> `eu.mailgun.org`
- `pavel.local.hypofriend.de` -> `jtkfqjar.cname.eu.ngrok.io`
- `heyflow.hypofriend.de` -> `flow.heyflow.domains`
- `sparplan.hypofriend.de` -> `flow.heyflow.domains`
- `tiago.local.hypofriend.de` -> `jtkfqjar.cname.eu.ngrok.io`
- `sofia.local.hypofriend.de` -> `jtkfqjar.cname.eu.ngrok.io`
- `email.m2.hypofriend.de` -> `eu.mailgun.org`
- `bonava.hypofriend.de` -> `flow.heyflow.domains`
- `myne.hypofriend.de` -> `flow.heyflow.domains`
- `evernest.hypofriend.de` -> `flow.heyflow.domains`

## DEEP SERVICE SCAN 2026-09-02 (read-only connect+banner)
**Host:** `bonava.hypofriend.de` | **Ports:** [80, 443, 2082, 2083, 2086, 2087, 8080, 8443]
**Non-web ports observed:** [2082, 2083, 2086, 2087, 8080, 8443]
> NOTE: repeated identical non-web port sets (e.g. 2082,2083,2086,2087,8080,8443) across many hosts and wide port sets are likely a shared edge/proxy answering EOF, NOT confirmed real services. Verify with a proper port scanner (e.g. nmap) under authorization before treating as real. These are surface-map hints only, not findings.

## DEEP SERVICE SCAN 2026-09-02 (read-only connect+banner)
**Host:** `email.m.hypofriend.de` | **Ports:** [80, 443]
**Web surface only:** [80, 443]

## DEEP SERVICE SCAN 2026-09-02 (read-only connect+banner)
**Host:** `email.m2.hypofriend.de` | **Ports:** [80, 443]
**Web surface only:** [80, 443]

## DEEP SERVICE SCAN 2026-09-02 (read-only connect+banner)
**Host:** `evernest.hypofriend.de` | **Ports:** [80, 443, 2082, 2083, 2086, 2087, 8080, 8443]
**Non-web ports observed:** [2082, 2083, 2086, 2087, 8080, 8443]
> NOTE: repeated identical non-web port sets (e.g. 2082,2083,2086,2087,8080,8443) across many hosts and wide port sets are likely a shared edge/proxy answering EOF, NOT confirmed real services. Verify with a proper port scanner (e.g. nmap) under authorization before treating as real. These are surface-map hints only, not findings.

## DEEP SERVICE SCAN 2026-09-02 (read-only connect+banner)
**Host:** `kajsa.local.hypofriend.de` | **Ports:** [80, 443]
**Web surface only:** [80, 443]

## DEEP SERVICE SCAN 2026-09-02 (read-only connect+banner)
**Host:** `laurence.local.hypofriend.de` | **Ports:** [80, 443]
**Web surface only:** [80, 443]

## DEEP SERVICE SCAN 2026-09-02 (read-only connect+banner)
**Host:** `myne.hypofriend.de` | **Ports:** [80, 443, 2082, 2083, 2086, 2087, 8080, 8443]
**Non-web ports observed:** [2082, 2083, 2086, 2087, 8080, 8443]
> NOTE: repeated identical non-web port sets (e.g. 2082,2083,2086,2087,8080,8443) across many hosts and wide port sets are likely a shared edge/proxy answering EOF, NOT confirmed real services. Verify with a proper port scanner (e.g. nmap) under authorization before treating as real. These are surface-map hints only, not findings.

## DEEP SERVICE SCAN 2026-09-02 (read-only connect+banner)
**Host:** `pavel.local.hypofriend.de` | **Ports:** [80, 443]
**Web surface only:** [80, 443]

## DEEP SERVICE SCAN 2026-09-02 (read-only connect+banner)
**Host:** `sofia.local.hypofriend.de` | **Ports:** [80, 443]
**Web surface only:** [80, 443]

## DEEP SERVICE SCAN 2026-09-02 (read-only connect+banner)
**Host:** `tiago.local.hypofriend.de` | **Ports:** [80, 443]
**Web surface only:** [80, 443]

## 2026-09-02 21:35:39 UTC

## 2026-09-02 23:33:09 UTC

## 2026-09-03 01:30:17 UTC

## 2026-09-03 06:29:54 UTC

## 2026-09-03 11:43:38 UTC

## 2026-09-03 15:49:44 UTC
- NEW api.hypofriend.de — primary API endpoint unprobed
- NEW core-api.hypofriend.de — internal/core API unprobed
- NEW graph.hypofriend.de — GraphQL endpoint unprobed
- NEW graph-rates.hypofriend.de — GraphQL rates API unprobed
- NEW v3.hypofriend.de — versioned API unprobed
- NEW auth.hypofriend.de — auth/OAuth endpoint unprobed
- NEW login.hypofriend.de — login endpoint unprobed
- NEW sso.hypofriend.de — SSO endpoint unprobed
- NEW admin.hypofriend.de — admin panel unprobed
- NEW admin.app.hypofriend.de — admin app unprobed
- NEW portal.hypofriend.de — customer portal unprobed
- NEW dashboard.hypofriend.de — dashboard unprobed
- NEW billing.hypofriend.de — billing/financial API unprobed
- NEW offer.hypofriend.de — mortgage offer API unprobed
- NEW documents.hypofriend.de — document API unprobed
- NEW my.hypofriend.de — user portal unprobed
- NEW profile.hypofriend.de — profile API unprobed
- NEW account.hypofriend.de — account API unprobed
- CHANGED bonava.hypofriend.de, myne.hypofriend.de, evernest.hypofriend.de — confirmed live (200) but CNAME to Heyflow (marketing), not core API

## 2026-09-03 19:11:58 UTC
- NEW hypofriend.de — Primary API surface consolidated on main domain (Nuxt SPA), subdomain APIs (api.*, core-api.*, graph.*) returning 503/000
- NEW /api/v3/advisors — Live endpoint requiring HTTP Basic auth (401), only confirmed API endpoint
- NEW Exposed Nuxt config — Sentry DSN, Amplitude key, Flagsmith env, GTM, FB Pixel, advisorEndpoint in window.__NUXT__
- CHANGED api.hypofriend.de, core-api.hypofriend.de, graph.hypofriend.de, graph-rates.hypofriend.de — Previously unprobed, now confirmed unresponsive (503/000)
- CHANGED login.hypofriend.de, sso.hypofriend.de, portal.hypofriend.de, dashboard.hypofriend.de, billing.hypofriend.de, offer.hypofriend.de, documents.hypofriend.de, my.hypofriend.de, profile.hypofriend.de, acc

## 2026-09-03 21:38:24 UTC
- NEW hypofriend.de — Primary API surface consolidated on main domain (Nuxt SPA); subdomain APIs (api.*, core-api.*, graph.*) confirmed dead (503/000/timeout)
- NEW /api/v3/advisors — Live endpoint requiring HTTP Basic auth (401), only confirmed API endpoint; `www-authenticate: Basic realm="Application"` header present
- NEW Exposed Nuxt config in `window.__NUXT__` — Sentry DSN (o128333.ingest.sentry.io), Amplitude API key, Flagsmith env ID (cqupGKF7Y3f5i2g62Zwbsv), GTM, FB Pixel, `advisorEndpoint: "/api/v3/advisors"`
- NEW /property-search-api — Returns HTTP 400 (expects parameters), dedicated API per Nuxt config
- CHANGED api.hypofriend.de, core-api.hypofriend.de, graph.hypofriend.de, graph-rates.hypofriend.de — Previously unprobed, now confirmed unresponsive (timeout/503/000)
- CHANGED login.hypofriend.de, sso.hypofriend.de, portal.hypofriend.de, dashboard.hypofriend.de, billing.hypofriend.de, offer.hypofriend.de, documents.hypofriend.de, my.hypofriend.de, profile.hypofriend.de, acc

## 2026-09-03 23:35:33 UTC
- NEW hypofriend.de/property-search-api — GraphQL endpoint with full introspection enabled; rich schema (Query/Mutation/Expose/Lead types); `expose(id: ID!)`, `exposes(id: ID!)`, `favoritedExposes(leadId: I
- CHANGED hypofriend.de/property-search-api — Previously "400 expects parameters"; now confirmed GraphQL with introspection, not REST

## 2026-09-04 01:25:05 UTC

## 2026-09-04 06:05:04 UTC

## 2026-09-04 11:31:13 UTC

## 2026-09-04 15:22:38 UTC
- NEW api.hypofriend.de — primary API endpoint unprobed
- NEW core-api.hypofriend.de — internal/core API unprobed
- NEW graph.hypofriend.de — GraphQL endpoint unprobed
- NEW graph-rates.hypofriend.de — GraphQL rates API unprobed
- NEW v3.hypofriend.de — versioned API unprobed
- NEW auth.hypofriend.de — auth/OAuth endpoint unprobed
- NEW login.hypofriend.de — login endpoint unprobed
- NEW sso.hypofriend.de — SSO endpoint unprobed
- NEW admin.hypofriend.de — admin panel unprobed
- NEW admin.app.hypofriend.de — admin app unprobed
- NEW portal.hypofriend.de — customer portal unprobed
- NEW dashboard.hypofriend.de — dashboard unprobed
- NEW billing.hypofriend.de — billing/financial API unprobed
- NEW offer.hypofriend.de — mortgage offer API unprobed
- NEW documents.hypofriend.de — document API unprobed
- NEW my.hypofriend.de — user portal unprobed
- NEW profile.hypofriend.de — profile API unprobed
- NEW account.hypofriend.de — account API unprobed
- CHANGED bonava.hypofriend.de, myne.hypofriend.de, evernest.hypofriend.de — confirmed live (200) but CNAME to Heyflow (marketing), not core API
- NEW hypofriend.de — Primary API surface consolidated on main domain (Nuxt SPA), subdomain APIs (api.*, core-api.*, graph.*) returning 503/000
- NEW /api/v3/advisors — Live endpoint requiring HTTP Basic auth (401), only confirmed API endpoint
- NEW Exposed Nuxt config — Sentry DSN, Amplitude key, Flagsmith env, GTM, FB Pixel, advisorEndpoint in window.__NUXT__
- CHANGED api.hypofriend.de, core-api.hypofriend.de, graph.hypofriend.de, graph-rates.hypofriend.de — Previously unprobed, now confirmed unresponsive (503/000)
- CHANGED login.hypofriend.de, sso.hypofriend.de, portal.hypofriend.de, dashboard.hypofriend.de, billing.hypofriend.de, offer.hypofriend.de, documents.hypofriend.de, my.hypofriend.de, profile.hypofriend.de, acc
- NEW hypofriend.de — Primary API surface consolidated on main domain (Nuxt SPA); subdomain APIs (api.*, core-api.*, graph.*) confirmed dead (503/000/timeout)
- NEW /api/v3/advisors — Live endpoint requiring HTTP Basic auth (401), only confirmed API endpoint; `www-authenticate: Basic realm="Application"` header present
- NEW Exposed Nuxt config in `window.__NUXT__` — Sentry DSN (o128333.ingest.sentry.io), Amplitude API key, Flagsmith env ID (cqupGKF7Y3f5i2g62Zwbsv), GTM, FB Pixel, `advisorEndpoint: "/api/v3/advisors"`
- NEW /property-search-api — Returns HTTP 400 (expects parameters), dedicated API per Nuxt config
- CHANGED api.hypofriend.de, core-api.hypofriend.de, graph.hypofriend.de, graph-rates.hypofriend.de — Previously unprobed, now confirmed unresponsive (timeout/503/000)
- CHANGED login.hypofriend.de, sso.hypofriend.de, portal.hypofriend.de, dashboard.hypofriend.de, billing.hypofriend.de, offer.hypofriend.de, documents.hypofriend.de, my.hypofriend.de, profile.hypofriend.de, acc
- NEW hypofriend.de/property-search-api — GraphQL endpoint with full introspection enabled; rich schema (Query/Mutation/Expose/Lead types); `expose(id: ID!)`, `exposes(id: ID!)`, `favoritedExposes(leadId: I
- CHANGED hypofriend.de/property-search-api — Previously "400 expects parameters"; now confirmed GraphQL with introspection, not REST

## 2026-09-04 18:34:20 UTC
- CHANGED hypofriend.de/property-search-api `expose(id)` resolver: previously boundary-only ("99999999 -> not found"); NOW confirmed live on a real enumerated expose UUID (200, returns title/price/street/proper
- NEW hypofriend.de/property-search-api: full search lifecycle is auth-free — `propertySearch(city:BERLIN,propertyType:APARTMENT)` returns searchId UUID with zero credentials; `exposes(id:<searchId>)` retur
- NEW Expose type PII surface confirmed on same auth-free object: cellPhoneNumber, phoneNumber, propertyOwnerLastName, providerEmail, ownerCompany, providerCompany (all String scalars)
