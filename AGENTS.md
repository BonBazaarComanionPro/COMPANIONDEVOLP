# Pet BonBazaar / Abonazaar Agent Workflow

This repository is the shared source of truth for continued development.

## Collaboration model

- **Owner / product direction:** Yannis Peeters (`yannispeeters96`)
- **ChatGPT / OpenAI agent work:** implementation, review, integration, tests and release preparation through Git branches and pull requests.
- **Cloud / Claude work:** may contribute through its own Git branch or fork and submit pull requests into this repository.
- **Community contributors:** may fork the public repository and submit pull requests. Direct write access is not required.

## Branch policy

- `main`: stable integration target. Do not overwrite blindly.
- `agents/petbonbazaar-integration`: shared integration/work branch for reconstructing the current product and agent handoffs.
- Other agents should use branches such as `cloud/<feature>` or `contrib/<feature>`.

## Current priority

1. Get **Abonazaar** locally deployable on Samsung S25 through Capacitor/Android.
2. Reconcile the React/Vite-era BonBazaar source with the newer Cloud/Claude implementation.
3. Add CI once the complete source is present in GitHub.
4. Only label a release `Launch Ready` after reproducible build + runtime/device tests pass.

## Android local deployment target

- App name: **Abonazaar**
- Android application ID: `com.bonbazaar.abonazaar`
- Initial target: local debug APK for Samsung S25.
- Public distribution later requires a signed release APK/AAB and a protected signing-key workflow.

## Security

Do not commit owner registration codes, master keys, passwords, signing keys, API secrets or private QR credentials to this public repository.
