### Release Notes - v0.66.4 (1261)

**Features**
- Added a new activity log with an overview and detail screen.
- Improved app onboarding screens with new setup steps for privacy policy, notification consent, screen lock, and more general improvements.
- General improvements to the PID issuance screens.
- Trust anchors split into access and registration CAs, with CRLs checked with soft-fail.

**Fixes**
- A service rejection dialog is now displayed when the verifier rejects the response.
- Dashboard no longer flashes its loader on return.
- Purpose box title: [b7af33cec](https://github.com/german-national-wallet/android-wallet-app/commit/b7af33cec) (WD-4715)
- Show full-width scroll fades on setup and presentation screens.
- Removed unneeded Android permissions.
- Following the HAIP recommendation, every OpenID4VCI config now allows only ECDH-ES (P-256) as JWE alg and A256GCM/A128GCM as `enc`.
- Explicit AES key size (256) and secure hardware required.

Known issues
- PID credentials are displayed incorrectly or not at all (issue #18)