# Validated findings (running count 0)

- 1 lead(s) marked VALID at 2026-09-04 14:11:03 UTC
  - | **VALID** | GraphQL BOLA/IDOR on `favoritedExposes`/`favoriteExpose` — arbitrary leadId read+write with no auth, exposing cross-tenant PII (broker phone/email/surname) on a financial mortgage platfo

- 4 lead(s) marked VALID at 2026-09-07 17:48:26 UTC
  - | Q7 Reasonable | **Yes** — auth-free R/W BOLA over customer-scoped IDs on a mortgage platform is a textbook valid bug |
  - **VERDICT: VALID**
  - | Q2 Reachable | **Partially** — endpoint returns 401, but no valid credentials confirmed |
  - | 1 | GraphQL BOLA/IDOR (favoritedExposes/favoriteExpose) | **VALID** | 8.6 | bugs.olivermaicher.eu |
