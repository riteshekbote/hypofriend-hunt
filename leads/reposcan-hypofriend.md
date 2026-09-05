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
## REPOSCAN 2026-09-04 06:04:33 UTC
[HYP] Hardcoded Google Cloud Project Number in advisor-couching
class: SECRET
asset: advisor-couching/main.js:17
confidence: 85
reasoning: CLOUD_PROJECT_NUMBER = "910242124570" is hardcoded in client-side JS. This is Hypofriend's own code (single commit from pavel@hypofriend.de, commit message "Add google project"). The GCP project number identifies the specific Google Cloud project backing their Google Meet add-on. An attacker can enumerate the project's services, IAM bindings, and API surfaces using this identifier. The value is also used in main.js:27 and main.js:43 to initialize the Meet addon session.
impact: Medium — enables targeted recon against the GCP project (enumerate APIs, service accounts, IAM policies via `gcloud projects describe 910242124570`). Not a direct credential leak, but a building block for further attacks.
verify_steps: 1) Visit https://github.com/HypoFriend/advisor-couching/blob/master/main.js line 17. 2) Confirm the number is real: run `gcloud projects describe 910242124570` (requires auth, passive). 3) Check if the GCP project hosts any live services by probing the Meet add-on URL https://hypofriend.github.io/advisor-couching/MainStage.html.
[HYP] Manager authorization bypass in voicemail-for-amazon-connect
class: IDOR
asset: voicemail-for-amazon-connect/aws-connect-vm-serverless/src/service/auth.service.js:120-122
confidence: 70
reasoning: The auth policy grants Managers full API access (policy.allowAllMethods()) despite a TODO comment indicating it should be restricted to "POST /manager/*" endpoints. This is a fork of an AWS sample, so the vulnerability is upstream, but if Hypofriend deployed this template without fixing the TODO, Managers can invoke all API endpoints including Admin-only routes. The code at line 120 shows: "// TODO: Allow only manager specific endpoints | policy.allowMethod("POST", "/manager/*"); policy.allowAllMethods();"
impact: Medium — Manager-role users could access Admin-only API endpoints (e.g., agent management, system settings) if deployed as-is. Depends on whether Hypofriend customized this before deployment.
verify_steps: 1) Check if Hypofriend's deployed voicemail portal has Manager-role users. 2) Attempt to call Admin-only endpoints with a Manager JWT. 3) Review if Hypofriend's deployment customized auth.service.js (requires access to their deployment, not passive).
[HYP] Hardcoded AWS Account ID in voicemail-for-amazon-connect mock data
class: OTHER
asset: voicemail-for-amazon-connect/aws-connect-vm-serverless/mock/voicemail-stream-completed.json:93
confidence: 30
reasoning: Mock data contains AWS account ID 439200502815 in DynamoDB stream ARNs. However, this is from the upstream AWS sample (author hdang), NOT Hypofriend's account. Out of scope per "known public files" exclusion.
impact: Low — upstream sample data, not Hypofriend's infrastructure.
verify_steps: N/A — this is upstream artifact, not Hypofriend-specific.
TARGET_ORG not configured for hypofriend; skipping public-org deep scan.
## REPOSCAN 2026-09-04 10:51:50 UTC
TARGET_ORG not configured for hypofriend; skipping public-org deep scan.
## REPOSCAN 2026-09-04 14:37:24 UTC
TARGET_ORG not configured for hypofriend; skipping public-org deep scan.
## REPOSCAN 2026-09-04 17:48:23 UTC
TARGET_ORG not configured for hypofriend; skipping public-org deep scan.
## REPOSCAN 2026-09-04 20:02:04 UTC
TARGET_ORG not configured for hypofriend; skipping public-org deep scan.
## REPOSCAN 2026-09-04 22:21:57 UTC
TARGET_ORG not configured for hypofriend; skipping public-org deep scan.
## REPOSCAN 2026-09-05 00:20:44 UTC
TARGET_ORG not configured for hypofriend; skipping public-org deep scan.
## REPOSCAN 2026-09-05 04:54:08 UTC
TARGET_ORG not configured for hypofriend; skipping public-org deep scan.
## REPOSCAN 2026-09-05 08:43:36 UTC
TARGET_ORG not configured for hypofriend; skipping public-org deep scan.
## REPOSCAN 2026-09-05 12:13:22 UTC
TARGET_ORG not configured for hypofriend; skipping public-org deep scan.
## REPOSCAN 2026-09-05 15:22:08 UTC
[HYP] Hardcoded GCP Project Number in Google Meet Add-on
class: SECRET
asset: HypoFriend/advisor-couching/main.js:17
confidence: 85
reasoning: CLOUD_PROJECT_NUMBER = "910242124570" is hardcoded in client-side JS committed by pavel@hypofriend.de (single commit "Add google project"). This is Hypofriend's OWN code (not a fork). The GCP project number identifies the specific Google Cloud project backing their Google Meet advisor-couching add-on. Used at lines 27 and 43 to initialize meet.addon.createAddonSession(). Enables targeted recon against the GCP project (enumerate APIs, service accounts, IAM bindings via gcloud CLI).
impact: Medium — enables targeted GCP project enumeration; not a direct credential leak but a building block for further attacks.
verify_steps: 1) Browse https://github.com/HypoFriend/advisor-couching/blob/master/main.js:17. 2) Passively confirm project existence: gcloud projects describe 910242124570 (requires auth). 3) Check if the Meet add-on is live at https://hypofriend.github.io/advisor-couching/MainStage.html.
[HYP] Manager-Role Auth Bypass (allowAllMethods) in Amazon Connect Voicemail
class: IDOR
asset: HypoFriend/voicemail-for-amazon-connect/aws-connect-vm-serverless/src/service/auth.service.js:119-121
confidence: 60
reasoning: The _generate() method grants Manager-role users full API access via policy.allowAllMethods() despite a TODO comment indicating it should be restricted to POST /manager/* endpoints. Code: "// TODO: Allow only manager specific endpoints | policy.allowMethod("POST", "/manager/*"); policy.allowAllMethods();". This is a FORK of amazon-connect/voicemail-for-amazon-connect (upstream author: Dave Lemons). If Hypofriend deployed this template without fixing the TODO, Manager users can invoke all API endpoints including Admin-only routes (agent management, global settings, contact flow building).
impact: Medium — Manager-role users could access Admin-only API endpoints if deployed as-is. Depends on whether Hypofriend customized auth.service.js before deployment.
verify_steps: 1) Check if Hypofriend has a live Amazon Connect voicemail deployment (probe for voicemail-related subdomains or paths). 2) If a Manager JWT can be obtained, attempt Admin-only endpoints (e.g., POST /global/settings, POST /contact/flow). 3) Review if Hypofriend's deployment customized auth.service.js (requires access to their deployment, not passive).
TARGET_ORG not configured for hypofriend; skipping public-org deep scan.
## REPOSCAN 2026-09-05 17:28:00 UTC
[HYP] Hardcoded GCP Project Number in Google Meet Add-on
class: MISCONFIG
asset: HypoFriend/advisor-couching/main.js:17
confidence: 35
reasoning: >-
impact: LOW — GCP project numbers are not secrets. No credential exposure.
verify_steps: >-
[HYP] Google Maps API Key in gmap-vue Documentation (Upstream Test Key)
class: OTHER
asset: HypoFriend/gmap-vue/packages/documentation/docs/vue-2-version/guide/*.md
confidence: 10
reasoning: >-
impact: INFO — Not a secret. Standard upstream example key.
verify_steps: N/A — Upstream documentation key, not actionable.
TARGET_ORG not configured for hypofriend; skipping public-org deep scan.
## REPOSCAN 2026-09-05 19:25:07 UTC
TARGET_ORG not configured for hypofriend; skipping public-org deep scan.
