```sh
flutter create --platforms ios -i objc fire_bug ## create a new project
cd ./fire_bug/ios && pod install ## install pods
flutter run ## run the app
```

Output:

```sh
Uncategorized (Xcode): Command CompileSwift failed with a nonzero exit code


Swift Compiler Error (Xcode): Value of optional type 'HeartbeatsBundle?' must be unwrapped to refer to member 'makeHeartbeatsPayload' of wrapped base type 'HeartbeatsBundle'
/Users/kennethjones/Code/firebase_ios_flutter_bug/ios/Pods/FirebaseCoreInternal/FirebaseCore/Internal/Sources/He
artbeatLogging/HeartbeatController.swift:109:13


Could not build the application for the simulator.
Error launching application on iPhone 13.
```
```sh
flutter doctor
```

```
flutter doctor
Doctor summary (to see all details, run flutter doctor -v):
[✓] Flutter (Channel stable, 3.0.4, on macOS 12.3.1 21E258 darwin-arm, locale en-US)
[!] Android toolchain - develop for Android devices (Android SDK version 31.0.0)
    ✗ cmdline-tools component is missing
      Run `path/to/sdkmanager --install "cmdline-tools;latest"`
      See https://developer.android.com/studio/command-line for more details.
    ✗ Android license status unknown.
      Run `flutter doctor --android-licenses` to accept the SDK licenses.
      See https://flutter.dev/docs/get-started/install/macos#android-setup for more details.
[✓] Xcode - develop for iOS and macOS (Xcode 13.4.1)
[✓] Chrome - develop for the web
[✓] Android Studio (version 2021.1)
[✓] VS Code (version 1.69.0)
[✓] Connected device (3 available)
[✓] HTTP Host Availability

! Doctor found issues in 1 category.
```


