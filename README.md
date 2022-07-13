```sh
## create a new project
flutter create --platforms ios -i objc fire_bug

## install dependencies
cd fire_bug
flutter pub add firebase_core
flutter pub add firebase_messaging

cd ios 

# edit Podfile
vi Podfile

## install pods
pod install

# run
flutter run ## run the app
```

## Podfile

```ruby
# Uncomment this line to define a global platform for your project
platform :ios, '12.0'
use_modular_headers!

# CocoaPods analytics sends network stats synchronously affecting flutter build latency.
ENV['COCOAPODS_DISABLE_STATS'] = 'true'
ENV['SWIFT_VERSION'] = '4'

project 'Runner', {
  'Debug' => :debug,
  'Profile' => :release,
  'Release' => :release,
}

def flutter_root
  generated_xcode_build_settings_path = File.expand_path(File.join('..', 'Flutter', 'Generated.xcconfig'), __FILE__)
  unless File.exist?(generated_xcode_build_settings_path)
    raise "#{generated_xcode_build_settings_path} must exist. If you're running pod install manually, make sure flutter pub get is executed first"
  end

  File.foreach(generated_xcode_build_settings_path) do |line|
    matches = line.match(/FLUTTER_ROOT\=(.*)/)
    return matches[1].strip if matches
  end
  raise "FLUTTER_ROOT not found in #{generated_xcode_build_settings_path}. Try deleting Generated.xcconfig, then run flutter pub get"
end

require File.expand_path(File.join('packages', 'flutter_tools', 'bin', 'podhelper'), flutter_root)

flutter_ios_podfile_setup

target 'Runner' do
  flutter_install_all_ios_pods File.dirname(File.realpath(__FILE__))
end


post_install do |installer|
  installer.pods_project.targets.each do |target|
    target.build_configurations.each do |config|
      config.build_settings['SWIFT_VERSION'] = '4.0'
      config.build_settings['IPHONEOS_DEPLOYMENT_TARGET'] = '12.0'
    end
    flutter_additional_ios_build_settings(target)
  end
end
```

## Error

```sh
Uncategorized (Xcode): Command CompileSwift failed with a nonzero exit code


Swift Compiler Error (Xcode): Value of optional type 'HeartbeatsBundle?' must be unwrapped to refer to member 'makeHeartbeatsPayload' of wrapped base type 'HeartbeatsBundle'
/Users/kennethjones/Code/firebase_ios_flutter_bug/ios/Pods/FirebaseCoreInternal/FirebaseCore/Internal/Sources/He
artbeatLogging/HeartbeatController.swift:109:13


Could not build the application for the simulator.
Error launching application on iPhone 13.
```
