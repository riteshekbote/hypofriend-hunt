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
