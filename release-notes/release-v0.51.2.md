### Release Notes - v0.51.2

Features
- Added a numbered overview of the issuance steps before the consent screen
- Added a consent screen after the card read, listing the credential, its issuer and the PID data
- Applied the final designs across the PID issuance, wallet code and consent screens
- Added explanation sheets for the eID function, the card PIN and the card PIN letter
- Closing the issuance flow, or rejecting the consent, now asks for confirmation
- The card is read on its own screen, with a progress sheet and an animation matching where the device's NFC antenna sits
- The privacy policy now opens without leaving the app
- The wallet locks itself and wipes its data when the account is revoked
- Added the Common Codes EUDI Hub sandbox trust anchors

Fixes
- Re-issuing a credential from the same issuer now replaces the existing one instead of storing both
- Issuance and DPoP metadata are now encrypted on the device
- Entered PINs can no longer be pasted in, captured in screenshots, or left behind in memory
- The wallet no longer opens links sent by other apps that it does not own
- Screen readers now announce the card reader steps, the claims card and the toolbar actions correctly
- Long credential names are no longer cut off on the credential card

Known issues
- PID credentials are displayed incorrectly or not at all (issue #18)
