# Flutter CI/CD

This project has automatic CI/CD and testing, to reproduce what is already defined follow this step below.
Software requirement for CI/CD
* Jenkins
* Homebrew
* Cocoapods
* Fastlane
* Android-sdk
* Java Runtime

## Installation

**macOS environment setup**

Homebrew Installation
- Run this command to install homebrew <br>
`/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"`

Java Run Time Installation<br>
- To install java runtime run this command<br>
`brew install adoptopenjdk8 --cask`<br>
For the record now java runtime is already at 16 version<br>
- Add JAVA_HOME to the bash profile, for mac especially bigSur it’s on ~/.zshrc file, open and add this line bellow<br>
`export JAVA_HOME=/Library/Java/JavaVirtualMachines/adoptopenjdk-8.jdk/Contents/Home`<br>

Install Android-sdk (Optional)<br>
- Skip this step if you already installed Android studio (really). But don’t forget to check if Android-sdk is already registered on the home environment. If it doesn’t, add this line to your ~/.zshrc or bashprofile<br>
`export ANDROID_HOME=/wherever/your/android/sdk/path`<br><br>
- Then set it to flutter by running flutter config --android-sdk<br>
`flutter config --android-sdk $ANDROID_HOME`<br>

- Then doublecheck if your SDK is already contained by this platform-tools<br>

`sdkmanager platform-tools "build-tools;29.0.2"`<br>
`sdkmanager platform-tools "platforms;android-29"`<br>
`sdkmanager platform-tools "build-tools;28.0.3"`<br>
`sdkmanager platform-tools "platforms;android-28"`<br>
`sdkmanager platform-tools "extras;android;m2repository"`<br>

Install Ruby & Cocoapods
- `brew install ruby`
- `sudo gem install cocoapods`

Install Fastlane
- `brew install fastlane`

Initial fastlane in project<br>
1. For the android
- `cd android/`
- `fastlane init`

2. For the ios
- `cd ios/`
- `fastlane match init`
- `fastlane init`

Jenkins Installation (Local purpose only)
- `brew install jenkins-lts`
- `brew services start jenkins-lts`
- `cat /Users/administrator/.jenkins/secrets/initialAdminPassword`

Jenkins build rules
- Push to PR Branches : Generate (android: .apk staging), (iOS: .ipa staging)
- PR Merged to Master : Generate (android: .apk staging & preview), (iOS: .ipa staging & preview)
- Tag from master : Generate (android: .apk & .aab production), (iOS: .ipa production)

