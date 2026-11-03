### Release Notes - v0.74.1 (1272)

**Features**
- If a credential is expired, presentations for that credential are blocked, and a single missing-credential screen is shown.
- Added a blocking screen for a locked Digital ID, and updated designs of the verification denied screens.
- Added timeout and expired-session dialogs during PID issuance, and timeout and rate-limit dialogs on startup.
- HTTP 408 and 429 responses now produce dedicated errors.
- OpenID4VP errors are now reported to all verifiers.

**Fixes**
- Improved recovery when reading the eID card.
- Fixed the read progress and PID issuance after a PIN change, and the eID authentication now ends before the PIN change.
- Returning to the transport PIN after entering the CAN now works.
- The wallet now waits for a cancelled eID flow to finish before re-issuing the PID.
- The wallet PIN success step is now shown only after issuance completes.
- The personal data screen is now built from the issuer metadata.
- Credential response encryption is now supported but no longer required. (Fixes issue #32)
- Wallet instance attestation for EAA issuers is now provided.
- Certificate revocation lists (CRLs) are now cached between validations.
- Password managers are kept away from PIN entry.
- App data is now excluded from cloud backup and device transfer.
- Changed how the wallet PIN key is derived.
- The setup illustration now keeps a 16:9 ratio.
- The DPoP-Nonce is no longer required on the finish-authorization redirect.
- PID credentials are now displayed correctly (Fixes issue #18).
