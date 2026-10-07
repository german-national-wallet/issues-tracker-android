### Release Notes - v0.61.3 (1250)

Features
- Built the settings screen, including the revocation code
- Added the new PID credential card design on the dashboard, consent and wallet code screens
- Issuer metadata must now be signed, and is checked against bundled trust anchors
- Presentation requests are refused when the relying party is not registered to ask for the data
- Presentation errors are now shown in designed dialogs, with a specific message for each
- Finished the EAA issuance and credential offer screens, and EAA consent now comes after the browser sign-in
- Each app variant now bundles its own trust anchors
- Updated the OpenID4VCI and RASP libraries

Fixes
- Unsatisfiable presentation or declining one now notifies the verifier
- Added metadata-driven WIA decision for unknown EAA issuers
- Allow retrying after entering a wrong transaction code
- No dialog appeared when the splash screen had no internet
- Technical fields such as expiry_date were shown in the personal details
- The consent headline showed the wrong number of claims
- SBOMs named the wrong supplier for packages that do not name one

Known issues
- PID credentials are displayed incorrectly or not at all (issue #18)