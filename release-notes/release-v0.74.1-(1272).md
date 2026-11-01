### Release Notes - v0.74.1 (1272)

**Features**
- An expired Digital ID is now treated as missing, presentations are blocked without a valid one, and a single missing-credential screen is shown.
- Added a blocking screen for a locked Digital ID, and aligned the verification denied screens with the blocking design.
- Added timeout and expired-session dialogs during PID issuance, and timeout and rate-limit dialogs on startup.
- HTTP 408 and 429 responses now produce dedicated errors.
- OpenID4VP errors are now reported to all verifiers (dev and sandbox builds only).

**Fixes**
- Improved recovery when reading the eID card: reading starts when the card is on the reader, you are asked again if the card is lifted, and you can retry or contact the citizen's office.
- Fixed the read progress and PID issuance after a PIN change, and the eID authentication now ends before the PIN change.
- Returning to the transport PIN after entering the CAN now works.
- The wallet now waits for a cancelled eID flow to finish before re-issuing the PID.
- The wallet PIN success step is now shown only after issuance completes.
- The personal data screen is now built from the issuer metadata.
- Credential response encryption is now supported but no longer required.
- Wallet instance attestation now comes from the wallet backend, with a local key check first.
- Certificate revocation lists (CRLs) are now cached between validations.
- Password managers are kept away from PIN entry.
- App data is now excluded from cloud backup and device transfer.
- Changed how the wallet PIN key is derived.
- The setup illustration now keeps a 16:9 ratio.
- The DPoP-Nonce is no longer required on the finish-authorization redirect.

**Known issues**
- PID credentials are displayed incorrectly or not at all (issue #18).
