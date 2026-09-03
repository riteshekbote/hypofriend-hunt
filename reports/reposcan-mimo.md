# Repository Scan Findings - mimo-v2.5-free
## Date: 2026-09-03

## Executive Summary

Scanned 44 public repositories in HypoFriend GitHub organization. Found 2 non-fork repositories (HypoFriend/advisor-couching, HypoFriend/browserUtils). browserUtils is empty. No hardcoded secrets, API keys, or credentials were found. One informational finding regarding a Google Cloud Project number.

---

## Findings

### [HYP] Google Cloud Project Number Exposed
- **class:** OTHER
- **asset:** HypoFriend/advisor-couching/main.js:17
- **confidence:** 20
- **reasoning:** Hardcoded `CLOUD_PROJECT_NUMBER = "910242124570"` found in main.js. This is a GCP project number (not a secret key), used for Google Meet Add-on integration. Project numbers are semi-public and can be found via GCP APIs, but exposure here reduces attack surface for reconnaissance.
- **impact:** Low - Informational. Project numbers alone don't grant access but can be used for enumeration of GCP resources.
- **verify_steps:** Passive - Check if this project number is associated with active Hypofriend GCP resources via Google APIs or public datasets.

---

## Repositories Scanned (Non-Fork)

| Repository | Status | Notes |
|------------|--------|-------|
| HypoFriend/advisor-couching | Contains code | Google Meet Add-on, hardcoded GCP project number |
| HypoFriend/browserUtils | Empty | No content |

## Repositories Scanned (Forks - No Findings)

All forked repositories (44 total) were scanned for:
- AWS access keys (AKIA pattern)
- Google API keys (AIza pattern)
- GitHub PATs (ghp_ pattern)
- Stripe keys (sk_live_, sk-us patterns)
- Private keys (BEGIN RSA/EC/OPENSSH PRIVATE)
- Hardcoded passwords, API keys, secrets, tokens
- AWS S3 bucket references
- Google Cloud Storage URLs
- Azure endpoints

**Result:** No secrets or hardcoded credentials found in any repository.

## Environment Variable Usage (Good Practice)

The following repos correctly use environment variables for secrets:
- HypoFriend/slack-pull-reminder: `SLACK_API_TOKEN`, `GITHUB_API_TOKEN` via `os.environ`
- HypoFriend/ecs-deploy: AWS credentials via GitHub Action inputs
- HypoFriend/gulp-cloudfront-invalidate-aws-publish: `process.env.AWS_SECRET_ACCESS_KEY`

---

## Conclusion

No actionable security findings (SECRETS, MISCONFIG, IDOR, SSRF) were identified in the public GitHub repositories. The only finding is informational: a hardcoded GCP project number in advisor-couching that could aid reconnaissance but does not directly compromise security.

**Recommendation:** Consider using environment variables for the GCP project number in advisor-couching if it should remain private, though project numbers are generally not considered sensitive.
