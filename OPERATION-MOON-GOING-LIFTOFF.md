# OPERATION MOON — GOING LIFTOFF

Status date: 2026-09-16
Release candidate: BonBazaar / Abonazaar v0.7.3

## Mission phase

Project Moon has entered the Operation Moon Going Liftoff phase.

## Verified launch gates

### Windows
- Source reconstruction: PASS
- Dependency install: PASS
- Automated tests: PASS (12/12)
- Native NSIS build: PASS
- Silent installer test: PASS
- Installed product version: 0.7.3.0
- Application launch smoke test: PASS
- Runtime process alive after 8 seconds: PASS
- Launch evidence artifact: PASS

### Android
- Source reconstruction: PASS
- Node setup: PASS
- Java setup: PASS
- Android SDK setup blocker fixed
- Android SDK 36 setup: PASS
- Final dependency/test/native APK gate: IN PROGRESS

## Liftoff rule

GO ONLINE is declared only when the final Android v0.7.3 job also completes successfully and the release artifacts are published from the verified commit. No older v0.7.0 installer may be presented as the v0.7.3 launch build.

## Launch sequence

GREEN LIGHT -> LAUNCH -> GO ONLINE

The launch source of truth is the verified v0.7.3 release commit and its CI artifacts.
