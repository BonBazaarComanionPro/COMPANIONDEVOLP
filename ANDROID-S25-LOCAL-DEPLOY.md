# Abonazaar Samsung S25 Local Deploy

## Status

The available BonBazaar HATCH source core was tested on 9 September 2026 with Node's built-in test runner.

- Tests: **12/12 passed**
- Android wrapper: **Capacitor**
- Local app identity: **Abonazaar**
- Application ID: `com.bonbazaar.abonazaar`
- First deployment target: **Samsung S25 via USB/ADB**

## Windows prerequisites

1. Install Node.js LTS.
2. Install Android Studio.
3. Open Android Studio once so the Android SDK, Platform Tools and bundled JDK are installed.
4. On Samsung S25 enable Developer options and USB debugging.
5. Connect the phone over USB and approve the RSA authorization prompt.

## Build flow

```text
npm install --no-audit --no-fund
npx cap add android        # only the first time
npx cap sync android
cd android
gradlew.bat assembleDebug
```

Expected APK:

```text
android/app/build/outputs/apk/debug/app-debug.apk
```

Install locally:

```text
adb install -r android/app/build/outputs/apk/debug/app-debug.apk
```

## Release boundary

This path produces a local **debug APK**. It is suitable for owner/device testing today. A public production launch requires a signed release APK/AAB, release signing keys stored outside Git, full runtime/device verification, and CI evidence.
