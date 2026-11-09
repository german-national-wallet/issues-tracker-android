### Release Notes - v0.74.1 (1272)

**Features**
- If a credential is expired, presentations for that credential are blocked, and a single missing-credential screen is shown.
- Improved the UX after blocking the Digital ID code due to too many failed times. The presentation request is declined and the user is prompted to re-add their ID.

**Fixes**
- Improved recovery when reading the eID card.
- Fixed the transport PIN change during PID issuance: the running eID authentication is now ended first, and after the new PIN is set the app continues with the issuance instead of showing a blank screen. The scanning progress screen now accurately shows the scan status.
- Fixed continuing with the transport PIN after entering the CAN.
- The Digital ID Code success step is now shown only after issuance completes.
- The Credential details screen uses information from the issuer metadata.
- Credential response encryption is now supported but no longer required. (Fixes issue #32)
- WWallet Instance Attestation(WIA) is now provided in the EAA issuance.
- Certificate revocation lists (CRLs) are now cached between validations.
- Password managers are kept away from Digital ID Code entry.
- App data is now excluded from cloud backup and device transfer.
- Changed how the Digital ID Code key is derived.
- The setup illustration now keeps a 16:9 ratio.
- The DPoP-Nonce is no longer required on the finish-authorization redirect.
- PID credentials are now displayed correctly (Fixes issue #18).
