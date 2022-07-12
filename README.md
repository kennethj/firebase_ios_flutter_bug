
```sh
cd ios && pod install
```

```sh
flutter run
```

Output
```
flutter run
Launching lib/main.dart on iPhone 13 in debug mode...
Running Xcode build...                                                  
 └─Compiling, linking and signing...                      2,392ms
Xcode build done.                                           12.2s
remote notifications are not supported in the simulator
[VERBOSE-2:ui_dart_state.cc(198)] Unhandled Exception: [core/not-initialized] Firebase has not been correctly initialized.

Usually this means you've attempted to use a Firebase service before calling `Firebase.initializeApp`.

View the documentation for more information: https://firebase.flutter.dev/docs/overview#initialization

#0      MethodChannelFirebase.initializeApp (package:firebase_core_platform_interface/src/method_channel/method_channel_firebase.dart:120:9)
<asynchronous suspension>
#1      Firebase.initializeApp (package:firebase_core/src/firebase.dart:40:31)
<asynchronous suspension>
#2      main (package:firebase_ios_flutter_bug/main.dart:6:3)
<asynchronous suspension>
Syncing files to device iPhone 13...                                60ms

Flutter run key commands.
r Hot reload. 🔥🔥🔥
R Hot restart.
h List all available interactive commands.
d Detach (terminate "flutter run" but leave application running).
c Clear the screen
q Quit (terminate the application on the device).

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

