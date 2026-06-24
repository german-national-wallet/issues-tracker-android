# issues-tracker-android

A public repository for issues management and bug reporting for Germany's Android Wallet Application

Current version: 0.14.0

## Supported features

| Area | Feature | Status | Version |
|---|---|---|---|
| OpenID4VCI | Issue PID credentials in both mdoc and SD-JWT VC formats | ✅ | 0.14.0 |
| OpenID4VCI | Issue EAA credentials, in both mdoc and SD-JWT VC formats, both wallet initiated and issuer initiated flows | ✅ | 0.14.0 |
| OpenID4VCI | Resolve a Credential Offer, both by value and by reference | ✅ | 0.14.0 |
| OpenID4VCI | Use PAR Endpoint for issuance | ✅ | 0.14.0 |
| OpenID4VCI | Use DPoP to sender-constrain Access Tokens | ✅ | 0.14.0 |
| OpenID4VCI | Send Wallet Attestations | ✅ | 0.14.0 |
| OpenID4VCI | Deferred Issuance | ✅ | 0.14.0 |
| OpenID4VP | Present PID and EAA credentials to verifiers | ✅ | 0.14.0 |
| OpenID4VP | Verify the verifier identity, supported client_id_schemes are <ul><li>x509_san_dns</li> and <li>x509_hash</li></ul> | ✅ | 0.14.0 |
| OpenID4VP | Send encrypted presentation responses to verifiers | ✅ | 0.14.0 |

## Upcoming features

| Area | Feature | Expected |
|---|---|---|
| OpenID4VCI | Send Key Attestations for PID Issuance | June 2026 |
| OpenID4VCI | Re-issue credentials using refresh tokens | June 2026 |
| OpenID4VCI / OpenID4VP | Present a credential during issuance of another credential | June 2026 |
| OpenID4VCI | Validate signed issuer metadata | August 2026 |
| OpenID4VCI | Obtain information about the issuer using Issuers' Registration Certificates included in the issuer metadata | August 2026 |
| OpenID4VCI | Support non key-bound EAAs | September 2026 |
| OpenID4VCI | Send Key Attestations during Key-bound EAA Issuance | September 2026 |
| OpenID4VCI | Encrypt credential issuance requests and responses | September 2026 |
| OpenID4VP | Prevent overasking using RP Registration Certificates included in the presentation requests | Q3 2026 (Conditional to Reference Implementation's implementation) |
| OpenID4VP | Present credentials through the browser or OS Digital Credentials API (only Android due to iOS lack of support) | August 2026 |

## Changelog

### v0.14.0

- The first time you start this app version after updating from a previous version, the app will clear app data and shut down. Start it a second time to use the app.
- The app now checks the relying party Access Certificate during presentation (Sandbox reported bug, ticket ref. WD-2551). If you saw this bug before, please re test and let us know if the fix works for you.
- Instead of issuing a PID document in either mdoc or SD-JWT format, there is now a single option that issues both formats at once. Issuance succeeds only if credentials in both formats are issued.
- Internal change. Moved to new backend (rWSCD to rWSCA).
- Visual styling (colors, fonts) has changed. This is not the final design, expect future changes.
- EAA issuance (both auth code flow and pre auth code flow) now works.
