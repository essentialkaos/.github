### Applications Update Feature

Some of our apps have a built-in update feature that lets users check for new versions and install them directly from the app. You can usually run it using the `-U` or `--update` command line option.

This feature lets users update their apps to the latest versions. It makes sure that users have access to the latest features, security updates, and performance enhancements.

#### How it works

1. The application downloads the latest version information from the ESSENTIAL KAOS app repository (`apps.kaos.st` _or_ `apps.kaos.ws`).
2. If a new version is available, the app will download the [ECDSA signature](https://en.wikipedia.org/wiki/Elliptic_Curve_Digital_Signature_Algorithm) and the new version of the app.
3. The application checks the signature to confirm that the downloaded file is real and hasn't been changed.
4. If the verification is successful, the application replaces the old version with the new one.

#### Security

The update process is designed with security in mind:
- The application verifies the ECDSA signature of the downloaded file to ensure it has not been tampered with.
- The update process is initiated by the user, ensuring that updates are not applied without user consent.
- The application checks for updates only from trusted sources (_the official ESSENTIAL KAOS app repository_).
- ECDSA public key is embedded in the application binary, ensuring that only verified updates can be applied.
- ECDSA private key is protected with a long passpahrase and presented only on build server.
