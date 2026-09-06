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

## 2026-09-04 21:05:40 UTC
- NEW hypofriend.de/property-search-api: `expose(id)` resolver confirmed live on real enumerated expose UUID (200, returns title/price/street/propertyOwnerLastName/providerEmail/providerCompany/cellPhoneNum
- NEW hypofriend.de/property-search-api: Full search lifecycle auth-free — `propertySearch(city:BERLIN,propertyType:APARTMENT)` returns searchId UUID with zero credentials; `exposes(id:<searchId>)` returns 
- NEW hypofriend.de/property-search-api: Expose type PII surface confirmed on auth-free object — cellPhoneNumber, phoneNumber, propertyOwnerLastName, providerEmail, ownerCompany, providerCompany (all String
- CHANGED hypofriend.de/property-search-api: Risk escalated from 88→92 (CRITICAL) — auth-free read (favoritedExposes, expose/exposes) + auth-free write (favoriteExpose, informationRequest) + Ruby stack-trace di

## 2026-09-04 23:06:55 UTC

## 2026-09-05 01:04:07 UTC
- CHANGED hypofriend.de/property-search-api: Confirmed real expose UUID (ad1d572e-8c01-5d07-a8ff-14b1a3af7d21) returns 200 with full PII (title, price, city, propertyOwnerLastName, providerEmail, providerCompan
- CHANGED hypofriend.de/property-search-api: Full search lifecycle auth-free confirmed — propertySearch mutation returns searchId; exposes(id:<searchId>) returns listing UUIDs; expose(id) returns PII for each —
- CHANGED hypofriend.de/property-search-api: Expose type PII surface confirmed — cellPhoneNumber, phoneNumber, propertyOwnerLastName, providerEmail, ownerCompany, providerCompany all accessible without auth
- NEW Inventory gap: 61/71 discovered subdomains unprobed since 2026-09-02 (only bonava/myne/evernest + 7 local.* confirmed live via Heyflow CNAME); api.*, core-api.*, graph.*, auth.*, admin.*, portal.*, da
- CHANGED hypofriend.de/api/v3/advisors: Only confirmed live API endpoint on main domain (401 Basic auth), advisorEndpoint exposed in Nuxt config
- CHANGED hypofriend.de: Nuxt config exposes Sentry DSN (o128333.ingest.sentry.io), Amplitude key, Flagsmith env ID (cqupGKF7Y3f5i2g62Zwbsv) — passive PII extraction via Sentry API possible

## 2026-09-05 06:00:39 UTC
- NEW hypofriend.de/property-search-api: Full enumeration chain validated — propertySearch→exposes→expose returns PII for 6+ listings in single city query; 2 real UUIDs confirmed with phone/email/surname/co
- NEW hypofriend.de/property-search-api: favoriteExpose mutation executes write handler for arbitrary leadId (error differs for exist vs non-exist exposeId) — cross-tenant write primitive confirmed
- NEW hypofriend.de/property-search-api: informationRequest mutation leaks full Ruby backtrace on missing advisor_email — additional stack-trace disclosure vector
- NEW hypofriend.de: Sentry DSN public key extracted (9ca05e60fc824941825aaeb8010b7e50@o128333.ingest.sentry.io/6376386) but API requires auth token, not DSN key — passive PII extraction blocked
- CHANGED api.hypofriend.de/core-api.hypofriend.de/graph.hypofriend.de/auth.hypofriend.de/admin.hypofriend.de/portal.hypofriend.de/dashboard.hypofriend.de/billing.hypofriend.de/offer.hypofriend.de/documents.hyp
- CHANGED app.hypofriend.de → Apple App Store (301), www.hypofriend.de → hypofriend.de (301)

## 2026-09-05 09:51:38 UTC
- CHANGED hypofriend.de/property-search-api: Full enumeration chain validated across cities — propertySearch→exposes→expose returns PII for 6+ listings per city; 2 real UUIDs confirmed with phone/email/surname/
- CHANGED hypofriend.de/property-search-api: favoriteExpose mutation error differentiates exist vs non-exist exposeId for arbitrary leadId — cross-tenant write primitive confirmed
- CHANGED hypofriend.de/property-search-api: informationRequest mutation leaks /app/app/mutations/information_request.rb:53 backtrace on missing advisor_email — additional stack-trace vector
- CHANGED hypofriend.de: Sentry DSN public key confirmed (9ca05e60fc824941825aaeb8010b7e50@o128333.ingest.sentry.io/6376386) but Sentry API requires auth token, not DSN key — passive PII extraction blocked

## 2026-09-05 13:23:35 UTC
- NEW core.hypofriend.de — LIVE Rails origin of main-domain app; direct backend without CloudFront edge; canonical redirect shell; 200 robots/sitemap; 401 /api/v3/advisors; 400 /property-search-api GraphQL
- NEW a.hypofriend.de — CloudFront→S3 (eu-central-1) closed bucket, 403 on all probed objects
- CHANGED blog.hypofriend.de — direct S3 403 AllAccessDisabled (confirms prior), HTTPS 000
- CHANGED m2.hypofriend.de — awselb/2.0 301 chain to https://hypofriend.de/en (inert)
- CHANGED hypofriend.de/property-search-api: Cross-city enumeration validated — propertySearch→exposes→expose returns 6+ listings PII per city (MUNICH, BERLIN, HAMBURG confirmed); 2 real UUIDs (ad1d572e-8c01-5d
- CHANGED hypofriend.de/property-search-api: favoriteExpose mutation error differentiates exist vs non-exist exposeId for arbitrary leadId — cross-tenant write primitive confirmed (error:"expose does not exist"
- CHANGED hypofriend.de/property-search-api: informationRequest missing advisor_email leaks /app/app/mutations/information_request.rb:53 backtrace — new stack-trace vector
- CHANGED hypofriend.de: Sentry DSN public key confirmed (9ca05e60fc824941825aaeb8010b7e50@o128333.ingest.sentry.io/6376386) but Sentry API requires auth token — passive PII extraction blocked

## 2026-09-05 16:26:50 UTC
- NEW core.hypofriend.de — Live Rails origin (direct, no CloudFront), canonical redirect shell, 200 robots.txt/sitemap.xml, 401 /api/v3/advisors Basic, 400 /property-search-api GraphQL
- NEW a.hypofriend.de — CloudFront→S3 (eu-central-1) closed bucket, 403 all objects (index.html, favicon.ico, images, robots, sitemap, assets)
- CHANGED hypofriend.de/property-search-api — Cross-city enumeration validated: propertySearch→exposes→expose returns 6+ listings PII per city (MUNICH, BERLIN, HAMBURG confirmed); 2 real UUIDs (ad1d572e-8c01-5d
- CHANGED hypofriend.de/property-search-api — favoriteExpose mutation error differentiates exist vs non-exist exposeId for arbitrary leadId — cross-tenant write primitive confirmed (error:"expose does not exist
- CHANGED hypofriend.de/property-search-api — informationRequest missing advisor_email leaks /app/app/mutations/information_request.rb:53 backtrace — new stack-trace vector
- CHANGED hypofriend.de — Sentry DSN public key confirmed (9ca05e60fc824941825aaeb8010b7e50@o128333.ingest.sentry.io/6376386) but Sentry API requires auth token — passive PII extraction blocked
- CHANGED blog.hypofriend.de — Direct S3 403 AllAccessDisabled (HTTP), HTTPS 000 — confirms prior
- CHANGED m2.hypofriend.de — awselb/2.0 301 chain (HTTP→HTTPS→https://hypofriend.de/en) — inert redirect edge
- CHANGED 503-fleet/.app-cluster/relay.m — Unchanged (503 HTTPS / 000 / 301 HTTP) — no new surface

## 2026-09-05 18:23:35 UTC
- NEW core.hypofriend.de — Live Rails origin (direct, no CloudFront), canonical redirect shell, 200 robots.txt/sitemap.xml, 401 /api/v3/advisors Basic, 400 /property-search-api GraphQL
- NEW a.hypofriend.de — CloudFront→S3 (eu-central-1) closed bucket, 403 all objects (index.html, favicon.ico, images, robots, sitemap, assets)
- CHANGED hypofriend.de/property-search-api — Cross-city enumeration validated: propertySearch→exposes→expose returns 6+ listings PII per city (MUNICH, BERLIN, HAMBURG confirmed); 2 real UUIDs (ad1d572e-8c01-5d
- CHANGED hypofriend.de/property-search-api — favoriteExpose mutation error differentiates exist vs non-exist exposeId for arbitrary leadId — cross-tenant write primitive confirmed (error:"expose does not exist
- CHANGED hypofriend.de/property-search-api — informationRequest missing advisor_email leaks /app/app/mutations/information_request.rb:53 backtrace — new stack-trace vector
- CHANGED hypofriend.de — Sentry DSN public key confirmed (9ca05e60fc824941825aaeb8010b7e50@o128333.ingest.sentry.io/6376386) but Sentry API requires auth token — passive PII extraction blocked
- CHANGED blog.hypofriend.de — Direct S3 403 AllAccessDisabled (HTTP), HTTPS 000 — confirms prior
- CHANGED m2.hypofriend.de — awselb/2.0 301 chain (HTTP→HTTPS→https://hypofriend.de/en) — inert redirect edge
- CHANGED 503-fleet/.app-cluster/relay.m — Unchanged (503 HTTPS / 000 / 301 HTTP) — no new surface
- NEW core.hypofriend.de — Live Rails origin (direct, no CloudFront), canonical redirect shell, 200 robots.txt/sitemap.xml, 401 /api/v3/advisors Basic, 400 /property-search-api GraphQL
- NEW a.hypofriend.de — CloudFront→S3 (eu-central-1) closed bucket, 403 all objects (index.html, favicon.ico, images, robots, sitemap, assets)
- CHANGED hypofriend.de/property-search-api — Cross-city enumeration validated: propertySearch→exposes→expose returns 6+ listings PII per city (MUNICH, BERLIN, HAMBURG confirmed); 2 real UUIDs (ad1d572e-8c01-5d
- CHANGED hypofriend.de/property-search-api — favoriteExpose mutation error differentiates exist vs non-exist exposeId for arbitrary leadId — cross-tenant write primitive confirmed (error:"expose does not exist
- CHANGED hypofriend.de/property-search-api — informationRequest missing advisor_email leaks /app/app/mutations/information_request.rb:53 backtrace — new stack-trace vector
- CHANGED hypofriend.de — Sentry DSN public key confirmed (9ca05e60fc824941825aaeb8010b7e50@o128333.ingest.sentry.io/6376386) but Sentry API requires auth token — passive PII extraction blocked
- CHANGED blog.hypofriend.de — Direct S3 403 AllAccessDisabled (HTTP), HTTPS 000 — confirms prior
- CHANGED m2.hypofriend.de — awselb/2.0 301 chain (HTTP→HTTPS→https://hypofriend.de/en) — inert redirect edge
- CHANGED 503-fleet/.app-cluster/relay.m — Unchanged (503 HTTPS / 000 / 301 HTTP) — no new surface

## 2026-09-05 20:49:06 UTC
- NEW core.hypofriend.de — Live Rails origin (direct, no CloudFront), canonical redirect shell, 200 robots.txt/sitemap.xml, 401 /api/v3/advisors Basic, 400 /property-search-api GraphQL
- NEW a.hypofriend.de — CloudFront→S3 (eu-central-1) closed bucket, 403 all objects (index.html, favicon.ico, images, robots, sitemap, assets)
- CHANGED hypofriend.de/property-search-api — Cross-city enumeration validated: propertySearch→exposes→expose returns 6+ listings PII per city (MUNICH, BERLIN, HAMBURG confirmed); 2 real UUIDs (ad1d572e-8c01-5d
- CHANGED hypofriend.de/property-search-api — favoriteExpose mutation error differentiates exist vs non-exist exposeId for arbitrary leadId — cross-tenant write primitive confirmed (error:"expose does not exist
- CHANGED hypofriend.de/property-search-api — informationRequest missing advisor_email leaks /app/app/mutations/information_request.rb:53 backtrace — new stack-trace vector
- CHANGED hypofriend.de — Sentry DSN public key confirmed (9ca05e60fc824941825aaeb8010b7e50@o128333.ingest.sentry.io/6376386) but Sentry API requires auth token — passive PII extraction blocked
- CHANGED blog.hypofriend.de — Direct S3 403 AllAccessDisabled (HTTP), HTTPS 000 — confirms prior
- CHANGED m2.hypofriend.de — awselb/2.0 301 chain (HTTP→HTTPS→https://hypofriend.de/en) — inert redirect edge
- CHANGED 503-fleet/.app-cluster/relay.m — Unchanged (503 HTTPS / 000 / 301 HTTP) — no new surface
- CHANGED core.hypofriend.de/property-search-api — Direct-origin full introspection CONFIRMED: identical schema to main domain (Query 12 resolvers, Mutation 3, Expose/ExposeSeen/FavoriteExposePayload/Informatio
- NEW property-search-api resolver map (from own introspection on direct origin): `exposes(id,offset,limit)`, `pagination(id,offset,limit)`, `exposesInBounds(id,bounds{north,east,south,west})`, `mapExposes(
- NEW core.hypofriend.de — Live Rails origin (direct, no CloudFront), canonical redirect shell, 200 robots.txt/sitemap.xml, 401 /api/v3/advisors Basic, 400 /property-search-api GraphQL
- NEW a.hypofriend.de — CloudFront→S3 (eu-central-1) closed bucket, 403 all objects (index.html, favicon.ico, images, robots, sitemap, assets)
- CHANGED hypofriend.de/property-search-api — Cross-city enumeration validated: propertySearch→exposes→expose returns 6+ listings PII per city (MUNICH, BERLIN, HAMBURG confirmed); 2 real UUIDs confirmed with ph
- CHANGED hypofriend.de/property-search-api — favoriteExpose mutation error differentiates exist vs non-exist exposeId for arbitrary leadId — cross-tenant write primitive confirmed
- CHANGED hypofriend.de/property-search-api — informationRequest missing advisor_email leaks /app/app/mutations/information_request.rb:53 backtrace — new stack-trace vector
- CHANGED hypofriend.de — Sentry DSN public key confirmed but Sentry API requires auth token — passive PII extraction blocked
- CHANGED blog.hypofriend.de — Direct S3 403 AllAccessDisabled (HTTP), HTTPS 000 — confirms prior
- CHANGED m2.hypofriend.de — awselb/2.0 301 chain (HTTP→HTTPS→https://hypofriend.de/en) — inert redirect edge
- CHANGED 503-fleet/.app-cluster/relay.m — Unchanged (503 HTTPS / 000 / 301 HTTP) — no new surface

## 2026-09-05 22:40:03 UTC
- NEW core.hypofriend.de/property-search-api — direct-origin full introspection CONFIRMED identical schema to main domain (Query 12 resolvers, Mutation 3, Expose/ExposeSeen/FavoriteExposePayload/Information
- NEW property-search-api resolver map expanded via direct-origin introspection: `exposes(id,offset,limit)`, `pagination(id,offset,limit)`, `exposesInBounds(id,bounds{north,east,south,west})`, `mapExposes(i
- NEW expose(id,leadId,saveExposeContact,returnMissing) signature confirmed — optional leadId/saveExposeContact/returnMissing args exposed auth-free (contact-save + delisted-record retrieval vectors)
- CHANGED hypofriend.de/property-search-api — cross-city enumeration validated across MUNICH, BERLIN, HAMBURG (6+ listings PII per city); 2 real UUIDs (ad1d572e-8c01-5d07-a8ff-14b1a3af7d21 + 1 more) confirmed w
- CHANGED favoriteExpose mutation — error differentiates exist vs non-exist exposeId for arbitrary leadId (`expose does not exist` vs `validation failed`) — cross-tenant write primitive confirmed
- CHANGED informationRequest missing advisor_email — leaks `/app/app/mutations/information_request.rb:53` backtrace (new stack-trace vector, distinct from meta)
- CHANGED Sentry DSN public key confirmed (9ca05e60fc824941825aaeb8010b7e50@o128333.ingest.sentry.io/6376386) but Sentry API requires auth token — passive PII extraction blocked
- CHANGED core.hypofriend.de — canonical redirect shell confirmed (root 302→/en, unknown 301→/), 200 robots.txt/sitemap.xml, 401 /api/v3/advisors Basic, 400 /property-search-api GraphQL
- CHANGED a.hypofriend.de — CloudFront→S3 (eu-central-1) closed bucket, 403 all objects (index.html, favicon.ico, images, robots, sitemap, assets)
- CHANGED blog.hypofriend.de — direct S3 403 AllAccessDisabled (HTTP), HTTPS 000 — confirms prior
- CHANGED m2.hypofriend.de — awselb/2.0 301 chain (HTTP→HTTPS→https://hypofriend.de/en) — inert redirect edge
- CHANGED 503-fleet/.app-cluster/relay.m — unchanged (503 HTTPS / 000 / 301 HTTP) — no new surface
- CHANGED dead fleet (api.*, core-api.*, graph.*, auth.*, admin.*, portal.*, dashboard.*, billing.*, offer.*, documents.*, my.*, profile.*, account.*) + graph-rates, v3, login, sso — all 503/000/timeout — no ne

## 2026-09-06 00:16:53 UTC
- NEW core.hypofriend.de/property-search-api — direct-origin hardening gap reconfirmed: OPTIONS 200 returns ONLY `date`/`content-length` (no `server`, no HSTS/X-Frame-Options/X-Content-Type-Options/nosniff,
- CHANGED none — all tracked hosts returned identical statuses to last cycle (hypofriend.de/en 200, both /property-search-api 400, core robots 200 / advisors 401, a. 403, m2 301, auth/admin 503, api/admin.app/b

## 2026-09-06 04:47:48 UTC

## 2026-09-06 09:11:25 UTC
