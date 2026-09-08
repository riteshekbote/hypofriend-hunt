# Validated findings (running count 0)

- 1 lead(s) marked VALID at 2026-09-04 14:11:03 UTC
  - | **VALID** | GraphQL BOLA/IDOR on `favoritedExposes`/`favoriteExpose` — arbitrary leadId read+write with no auth, exposing cross-tenant PII (broker phone/email/surname) on a financial mortgage platfo

- 4 lead(s) marked VALID at 2026-09-07 17:48:26 UTC
  - | Q7 Reasonable | **Yes** — auth-free R/W BOLA over customer-scoped IDs on a mortgage platform is a textbook valid bug |
  - **VERDICT: VALID**
  - | Q2 Reachable | **Partially** — endpoint returns 401, but no valid credentials confirmed |
  - | 1 | GraphQL BOLA/IDOR (favoritedExposes/favoriteExpose) | **VALID** | 8.6 | bugs.olivermaicher.eu |

- 14 lead(s) marked VALID at 2026-09-08 08:58:20 UTC
  - **Verdict: VALID** — Read-only proof: POST introspection query. **Impact: Medium** (enabler). **CVSS 3.1: 5.3 (Medium)**. **Report via:** bugs.olivermaicher.eu
  - **Verdict: VALID** — Read-only: execute GraphQL queries as shown. **Impact: CRITICAL**. **CVSS 3.1: 8.6 (High)**. **Report via:** bugs.olivermaicher.eu
  - **Verdict: VALID** — Read-only: call mutation with arbitrary leadId, observe error differential. **Impact: High**. **CVSS 3.1: 8.1 (High)**. **Report via:** bugs.olivermaicher.eu
  - | Q3 Impact? | YES | Returns appointment data for arbitrary lead_id; zero-UUID returns `[]` but valid UUIDs may return booked appointment details |
  - **Verdict: VALID** — Read-only: POST with zero-UUID. **Impact: Medium-High**. **CVSS 3.1: 6.5 (Medium)**. **Report via:** bugs.olivermaicher.eu
  - **Verdict: VALID** — Read-only: OPTIONS request with custom Origin. **Impact: High** (session hijack if authenticated users exist). **CVSS 3.1: 8.1 (High)**. **Report via:** bugs.olivermaicher.eu
  - **Verdict: VALID** — Read-only: `curl -I` to origin vs edge. **Impact: Medium**. **CVSS 3.1: 5.3 (Medium)**. **Report via:** bugs.olivermaicher.eu
  - **Verdict: HOLD** — Needs active validation to confirm takeover is possible. Risk of false positive if ngrok re-registers. **Impact: Medium if confirmed**. **CVSS 3.1: 6.5 (Medium)** if valid.
  - | 1 | GraphQL introspection enabled | **VALID** | 5.3 (M) | Enabler for PII leak |
  - | 2 | Unauthenticated PII enumeration | **VALID** | 8.6 (H) | Direct customer data exposure |
  - | 3 | Cross-tenant write via `favoriteExpose` | **VALID** | 8.1 (H) | IDOR write + oracle |
  - | 4 | BOLA on `already_booked_appointments` | **VALID** | 6.5 (M) | Unauth appointment data |
  - | 5 | Open credentialed CORS on `/q` | **VALID** | 8.1 (H) | Session hijack vector |
  - | 7 | Direct-origin CloudFront bypass | **VALID** | 5.3 (M) | WAF/security-header bypass |
