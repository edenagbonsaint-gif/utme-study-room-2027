# 320+ Study Room for Android

This Android app packages the study website in a secure local WebView origin. The study plan, quizzes, and screens are included in the APK. The on-device AI tutor downloads its model the first time it is used, and partner chat needs an internet connection.

## Build

Build an installable debug APK with Android SDK, Java 17, and Gradle 8.9:

```sh
gradle --no-daemon assembleDebug
```

The APK is written to `app/build/outputs/apk/debug/app-debug.apk`. The repository workflow builds this APK and publishes it as a public GitHub Release asset.

## Notes

- Package ID: `com.utme.studyroom`
- Minimum Android version: Android 7.0 (API 24)
- The APK is debug-signed for direct installation and is not a Google Play release.
- The local tutor relies on the phone's Android System WebView, Android version, GPU, and available memory. If WebGPU is unavailable, the schedule, quizzes, and partner chat remain available.

