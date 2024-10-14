We use three versioning schemes for our projects:

- [**Semantic Versioning**](https://semver.org/) (_SemVer_) — for applications, demons and utilities;
- [**Intended Effort Versioning**](https://jacobtomlinson.dev/effver/) (_EffVer_) — for libraries and Golang packages;
- YOLO/zero versions — for all MVPs and prototypes.

### SemVer

Version name: **MAJOR.MINOR.PATCH**

- `MAJOR` version incremented if incompatible API changes were made or a significant part of the logic was changed;
- `MINOR` version incremented if new functionality was added in a backward-compatible way, or a small part of the logic was changed;
- `PATCH` version incremented if backward-compatible bug fixes have been made.

### EffVer

Version name: **MACRO.MESO.MICRO**

- `MAJOR` version incremented if user has to spend significant time to upgrade to this version;
- `MESO` version incremented if upgrading to this version may require some minor effort;
- `MICRO` version incremented if upgrading to this version doesn't require the user to do anything.

### YOLO versions

Version name: **0.MAJOR.MINOR**

YOLO versions, also known as zero versions, are used for the very first versions of software where almost everything can be changed completely or broken. It is strongly discouraged to use software with these versions in your production environment.

When the software becomes stable, we move from zero version to SemVer or EffVer schemes.
