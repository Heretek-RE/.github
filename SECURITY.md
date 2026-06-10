# Security Policy

## Supported versions

The Heretek-RE public org is best-effort supported. We commit to applying
security fixes to the `main` branch of each repo.

| Repo | Supported |
|---|---|
| Heretek-RE/RE-Library | ✅ |
| Heretek-RE/Android-RE | ✅ |
| Heretek-RE/RE-UNLEASHED | ✅ |
| Heretek-RE/RE-AI | ✅ |
| Heretek-RE/RE-BREAKER | ✅ |
| Heretek-RE/re-* (per-MCP) | ✅ |
| Heretek-RE/.github | ✅ |

## Reporting a vulnerability

**Do not file a public issue for security vulnerabilities.** Use GitHub's
private vulnerability disclosure workflow:

1. Go to the repo's **Security** tab.
2. Click **"Report a vulnerability"**.
3. Fill in the advisory form with the details below.

We will respond within 7 days. We may ask for clarification or for a private
patch.

### What to include

- A clear description of the vulnerability
- The affected repo + version (or commit SHA)
- A reproducer (script, screenshot, or step-by-step)
- The impact (data exposure, RCE, etc.) and your assessment of severity

## What we will do

- Acknowledge receipt within 7 days.
- Triage the report within 14 days.
- Issue a fix or document a mitigation within 30 days for high-severity
  issues. Lower-severity issues may take longer.
- Credit you in the fix's release notes (unless you prefer to remain anonymous).
- Coordinate disclosure timing with you.

## Out-of-scope vulnerabilities

The following are explicitly out of scope for security advisories:

- **Vulnerabilities in vendor protection schemes.** This is research tooling.
  If you find a vulnerability in a commercial DRM or anti-tamper system, do
  not disclose it via this org. Disclose to the vendor per their security
  policy (or per coordinated disclosure norms for the relevant protection).
- **Vulnerabilities in third-party libraries** that the org's repos depend on.
  Report those upstream; the org will bump dependencies in response.
- **Bypass of the `--license-acknowledge` CLI gate** or removal of the
  `LICENSE-OFFENSIVE.md` terms. These are intentional design choices, not
  vulnerabilities.
- **Theoretical vulnerabilities** without a working reproducer.

## Scope of the offensive-research-use clause

The `LICENSE-OFFENSIVE.md` terms in the bypass-adjacent repos (RE-BREAKER and
the seven bypass-adjacent per-MCP repos) limit the authorized use of those
tools. If you believe a user is violating those terms, file a public issue in
the relevant repo with the violation details. The maintainers will review.
