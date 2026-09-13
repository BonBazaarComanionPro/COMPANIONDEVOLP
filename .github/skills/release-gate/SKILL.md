---
name: release-gate
description: Check BonBazaar release readiness. Use before internal beta or public release.
---

A release is GREEN only when:
- Target platform build succeeds.
- App launches on the target platform.
- Required automated tests pass.
- Privacy/memory isolation tests pass.
- No secrets are embedded in artifacts.
- Rollback is available.
- Version, hashes and release notes exist.
- Human creator explicitly approves release.
If any item is unproven, mark YELLOW or RED, never GREEN.
