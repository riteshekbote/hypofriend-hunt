## REPOSCAN 2026-09-03 15:10:34 UTC
TARGET_ORG not configured for hypofriend; skipping public-org deep scan.
## REPOSCAN 2026-09-03 18:42:05 UTC
TARGET_ORG not configured for hypofriend; skipping public-org deep scan.
## REPOSCAN 2026-09-03 21:35:56 UTC
TARGET_ORG not configured for hypofriend; skipping public-org deep scan.
## REPOSCAN 2026-09-03 23:32:09 UTC
[HYP] Google Cloud Project Number Exposed in advisor-couching
class: OTHER
asset: HypoFriend/advisor-couching/main.js:17
confidence: 20
reasoning: Hardcoded CLOUD_PROJECT_NUMBER = "910242124570" found in main.js. This is a GCP project number (not a secret key) used for Google Meet Add-on integration. Project numbers are semi-public but exposure reduces attack surface for reconnaissance.
impact: Low - Informational. Project numbers alone don't grant access but can aid enumeration of GCP resources.
verify_steps: Passive - Verify if this project number maps to active Hypofriend GCP resources via public GCP APIs or datasets.
TARGET_ORG not configured for hypofriend; skipping public-org deep scan.
## REPOSCAN 2026-09-04 01:22:12 UTC
TARGET_ORG not configured for hypofriend; skipping public-org deep scan.
