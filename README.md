# issues-tracker-android

A public repository for issues management and bug reporting for Germany's Android Wallet Application

Current version: [v0.51.2](/release-notes/release-v0.51.2.md)

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
| OpenID4VCI / OpenID4VP | Present a credential during issuance of another credential | ✅ | 0.29.0 |
| OpenID4VCI | Send Key Attestations to the Credential Endpoint of a PID Provider | ✅ | 0.25.13 |
| OpenID4VCI | Re-issue credentials using refresh tokens | ✅ | 0.25.13 |
| OpenID4VCI | Encrypt credential issuance request | ✅ | 0.25.13 |

## Upcoming features

| Area | Feature | Expected |
|---|---|---|
| OpenID4VCI | Validate signed issuer metadata | August 2026 |
| OpenID4VCI | Obtain information about the issuer using Issuers' Registration Certificates included in the issuer metadata | August 2026 |
| OpenID4VCI | Support non key-bound EAAs | September 2026 |
| OpenID4VCI | Send Key Attestations during Key-bound EAA Issuance | September 2026 |
| OpenID4VCI | Encrypt credential issuance responses | September 2026 |
| OpenID4VP | Prevent overasking using RP Registration Certificates included in the presentation requests | Q3 2026 (Conditional to Reference Implementation's implementation) |
| OpenID4VP | Present credentials through the browser or OS Digital Credentials API (only Android due to iOS lack of support) | August 2026 |
