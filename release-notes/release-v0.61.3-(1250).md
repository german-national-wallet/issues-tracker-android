### Release Notes - v0.61.3 (1250)

Features
- Added the settings screen, including the revocation code
- Added the new PID credential card design on the dashboard, consent and wallet code screens
- Enforced signed Issuer metadata, removed old trust anchors
- Presentation requests are refused when the relying party is not registered to ask for the data
- Improved UI on EAA issuance
- Moved the EAA issuance consent in Authorization Code Flow after the browser session
- Distinguish trust anchors per app environment
- Updated the OpenID4VCI and RASP libraries

Fixes
- Presentation that are unsatisfiable or declined by the user redirect to the redirect_uri if provided by the Relying Party
- Wallet Instance Attestation is send depending on the EAA Provider's metadata
- Allow retrying after entering a wrong transaction code
- No dialog appeared when the splash screen had no internet
- Technical fields such as expiry_date are removed from the Credential's details view
- Fixed the wrong number of selectively-disclosed claims shown in the Presentation consent headline
- SBOMs named the wrong supplier for packages that do not name one

Known issues
- PID credentials are displayed incorrectly or not at all (issue #18)