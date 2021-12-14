# Evermos-Flutter Documentation
This project is depend on :
- [Dart SDK >=2.12.0 <3.0.0](https://dart.dev/get-dart)
- [Flutter module package](https://github.com/evermos/flutter-module)
- [Dio Package](https://pub.dev/packages/dio)


## **Another documentation**
- [Flutter CI/CD with Jenkins, MacOS and fastlane](https://github.com/evermos/evermos-flutter/wiki/Flutter-CI-CD)

## **Test account**

- Write username & password for test account

## **Environment**

- Google play
- Appstore

## Requirements
- Flutter SDK 2.5.3
- Android with Minimum SDK Version 16
- iOS with Minimum OS Version 10
- Chrome to running this application on web
- Flutter Plugin
- Dart Plugin

## Configuration
To run this application, you need setup [launch.json](https://github.com/evermos/evermos-flutter/wiki/Configuration) to apply the configuration easy. But, if you a Android Studio user, you still can use that IDE with different configuration. You need to add configuration at run configuration with same args `flavor` and `dart-define` as you can found in launch.json.

## Git Branch Strategy
This application implemented using [Trunk Based Development](https://trunkbaseddevelopment.com/) for Git Branch Strategy with `main` as `trunk`. We as engineer can't direct / force push to main, we need create a pull request (PR) with [format applied](https://github.com/evermos/evermos-flutter/blob/main/.github/pull_request_template.md). Another engineer will review then approve the PR. After PR approved with another engineer, we can merged the PR to main.

## Architechture
This project implemented with [Clean Architecture](https://blog.cleancoder.com/uncle-bob/2012/08/13/the-clean-architecture.html), further [developed](https://github.com/ResoCoder/flutter-tdd-clean-architecture-course) from the [Reso Coder TDD example](https://resocoder.com/flutter-clean-architecture-tdd). Click [here](https://github.com/evermos/evermos-flutter/wiki/Clean-Architecture) to learn more about this project architecture.

# Running
If you want to running this project without IDE that support flutter and dart plugin. You can run this project using command
```
flutter run --flavor $flavorType --dart-define=FLAVOR_TYPE=$flavorType
```

### Staging
```
flutter run --flavor staging --dart-define=FLAVOR_TYPE=staging
```

### Preview
```
flutter run --flavor preview --dart-define=FLAVOR_TYPE=preview
```

### Production
Add args `release` for production. Please note, you can't apply this command to run in simulator. Because Apple not give permission to us install production in simulator.
```
flutter run --flavor production --release --dart-define=FLAVOR_TYPE=production
```

## Build
To build this project as APK, AppBundle, App or web you can use same command structure with run the project. But, you need replace from run to build. Then, specific type result what you want for example apk, appbundle, ios, and etc. For example, you can use this command:
```
flutter build apk --flavor staging --release --dart-define=FLAVOR_TYPE=staging
```