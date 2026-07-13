# issues-tracker-android

A public repository for issues management and bug reporting for Germany's Android Wallet Application

Current version: 0.25.13

## Supported features

| Area | Feature | Status | Version |
|---|---|---|---|
| OpenID4VCI | Issue PID credentials in both mdoc and SD-JWT VC formats | ✅ | 0.14.0 |
| OpenID4VCI | Issue EAA credentials, in both mdoc and SD-JWT VC formats, both wallet initiated and issuer initiated flows | ✅ | 0.14.0 |
| OpenID4VCI | Resolve a Credential Offer, both by value and by reference | ✅ | 0.14.0 |
| OpenID4VCI | Use PAR Endpoint for issuance | ✅ | 0.14.0 |
| OpenID4VCI | Use DPoP to sender-constrain Access Tokens | ✅ | 0.14.0 |
| OpenID4VCI | Send Wallet Attestations | ✅ | 0.14.0 |
| OpenID4VP | Present PID and EAA credentials to verifiers | ✅ | 0.14.0 |
| OpenID4VP | Verify the verifier identity, supported client_id_schemes are <ul><li>x509_san_dns</li> and <li>x509_hash</li></ul> | ✅ | 0.14.0 |
| OpenID4VP | Send encrypted presentation responses to verifiers | ✅ | 0.14.0 |
| OpenID4VP | Present multiple credentials together in one presentation | ✅ | 0.25.13 |
| OpenID4VCI | Send Key Attestations to the Credential Endpoint of a PID Provider | ✅ | 0.25.13 |
| OpenID4VCI | Re-issue credentials using refresh tokens | ✅ | 0.25.13 |
| Security | All wallet data stored encrypted on device using SQLCipher | ✅ | 0.25.13 |
| Security | Forced app update when installed version is below the required minimum | ✅ | 0.25.13 |
| Security | Automatic data wipe when the device's lock screen is removed | ✅ | 0.25.13 |
| Security | Certificate pinning for the Personal ID issuer on demo and pre-production servers | ✅ | 0.25.13 |
| Security | Google Play Integrity checks, configurable via a build setting | ✅ | 0.25.13 |

## Upcoming features

| Area | Feature | Expected |
|---|---|---|
| OpenID4VCI / OpenID4VP | Present a credential during issuance of another credential | June 2026 |
| OpenID4VCI | Validate signed issuer metadata | August 2026 |
| OpenID4VCI | Obtain information about the issuer using Issuers' Registration Certificates included in the issuer metadata | August 2026 |
| OpenID4VCI | Support non key-bound EAAs | September 2026 |
| OpenID4VCI | Send Key Attestations during Key-bound EAA Issuance | September 2026 |
| OpenID4VCI | Encrypt credential issuance requests and responses | September 2026 |
| OpenID4VP | Prevent overasking using RP Registration Certificates included in the presentation requests | Q3 2026 (Conditional to Reference Implementation's implementation) |
| OpenID4VP | Present credentials through the browser or OS Digital Credentials API (only Android due to iOS lack of support) | August 2026 |

## Changelog

### v0.25.13

- Present multiple credentials together in one presentation.
- Stacked credential cards on the dashboard, with a clear "no document" screen during presentation.
- Core engine upgraded, with tighter secure-key service handling and one-time codes wired into key creation.
- All wallet data on the device is now stored encrypted.
- Forced app update: if the installed version is below the required minimum, the app blocks use until updated.
- Automatic data wipe when the device's lock screen is removed.
- Credentials are refreshed when the remaining count is low after presentation (requires the Credential Issuer to provide a Refresh Token).
- Certificate pinning for the Personal ID issuer on demo and pre-production servers; root certificate pinned instead of the intermediate.
- Device validation renewal is now double-signed with a freshly generated key each time.
- Non-essential logging removed from release builds.
- Credential request encryption hardened, using a stronger algorithm and an encrypted request header.

### v0.14.0

- The first time you start this app version after updating from a previous version, the app will clear app data and shut down. Start it a second time to use the app.
- The app now checks the relying party Access Certificate during presentation (Sandbox reported bug, ticket ref. WD-2551). If you saw this bug before, please re test and let us know if the fix works for you.
- Instead of issuing a PID document in either mdoc or SD-JWT format, there is now a single option that issues both formats at once. Issuance succeeds only if credentials in both formats are issued.
- Internal change. Moved to new backend (rWSCD to rWSCA).
- Visual styling (colors, fonts) has changed. This is not the final design, expect future changes.
- EAA issuance (both auth code flow and pre auth code flow) now works.
