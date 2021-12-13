This documentation will guide every team member to write code that effective, less redundant, readable, and easy to understand for every member. Also, this documentation should be updated when there is a more sophisticated workflow. The final goal of this documentation is to guide every member to follow `Defined & Approved Standard` that can make the code more Uniform for the rest of us. In order to keep everything applicable for everyone, it's important to Classificate the Guidelines into a multiple category

# Classification

Fundamental guideline 
- [Effective Dart](https://dart.dev/guides/language/effective-dart)
- [Clean Architecture](https://blog.cleancoder.com/uncle-bob/2012/08/13/the-clean-architecture.html)
- [Project Structure](https://github.com/evermos/evermos-flutter/wiki/Code-Writing-Guideline#project-structure)
- [Evermos Flutter Best Practice 101](https://github.com/evermos/evermos-flutter/wiki/Code-Writing-Guideline#evermos-flutter-best-practice-101)

## Project structure
Our project structure is divided to 3 section :
1. `data` is stand for every data component as `datasources`, `mappers`, `repositories`
2. `domain` is stand for every component that relevant to the domain such as `entities`, `repositories` and `usecases`
3. `presentation` is stand for every UI component such as `state management folders like (get,bloc,provider, etc)`, `pages`, `widgets`, and `view_model`

here is the map : 
```
├── README.md
├── .vscode
├── example_module
│   ├── README.md
│   ├── .vscode
│   ├── android
│   ├── ios
│   ├── build
│   └── lib
│       ├── app_page.dart
│       ├── main_page.dart
│       ├── translation_service.dart
│       ├── example_page1.dart
│       ├── example_page2.dart
│       └── main.dart
├── assets
│   ├── fonts
│   │   ├── mitr
│   │   └── roboto
│   ├── icons
│   │   ├── 2.0x
│   │   ├── 3.0x
│   │   ├── 4.0x
│   │   └── icon.png
│   └── images
│       ├── 2.0x
│       ├── 3.0x
│       ├── 4.0x
│       └── image.png
├── lib
│   ├── consts
│   ├── data
│   │   ├── mappers
│   │   │   ├── converter_model_entity.dart
│   │   │   └── converter_model_entity.dart
│   │   ├── datasources
│   │   │   ├── local_datasource.dart
│   │   │   └── network_datasource.dart
│   │   ├── models
│   │   │  ├── model1.dart
│   │   │  └── model2.dart
│   │   └── repositories
│   │       ├── repository_impl1.dart
│   │       └── repository_impl2.dart
│   ├── domain
│   │   ├── entities
│   │   │   ├── custom_error1.dart
│   │   │   └── custom_error2.dart
│   │   ├── entities
│   │   │   ├── entity1.dart
│   │   │   └── entity2.dart
│   │   ├── usecases
│   │   │   ├── usecase1.dart
│   │   │   └── usecase2.dart
│   │   └── repositories
│   │       ├── repository1.dart
│   │       └── repository2.dart
│   └── presentation
│       ├── get
│       │   ├── binding.dart
│       │   ├── controller.dart
│       │   └── state.dart
│       ├── pages
│       │   ├── page1.dart
│       │   └── page2.dart
│       └── widgets
│           ├── widget1.dart
│           └── widget2.dart
├── changelog.md
├── pubspec.lock
├── pubspec.yaml
└── test
    ├── data
    │   ├── converters
    │   │   ├── converter1.dart
    │   │   └── converter2.dart
    │   ├── datasources
    │   │   ├── datasource1.dart
    │   │   └── datasource2.dart
    │   ├── models
    │   │   ├── model1.dart
    │   │   └── model2.dart
    │   └── repositories
    │       ├── repository_impl1.dart
    │       └── repository_impl2.dart
    ├── domain
    │   ├── entities
    │   │   ├── custom_error1.dart
    │   │   └── custom_error2.dart
    │   ├── entities
    │   │   ├── entity1.dart
    │   │   └── entity2.dart
    │   ├── usecases
    │   │   ├── usecase1.dart
    │   │   └── usecase2.dart
    │   └── repositories
    │       ├── repository1.dart
    │       └── repository2.dart
    ├── presentation
    │       ├── get
    │       │   ├── binding.dart
    │       │   ├── controller.dart
    │       │   └── state.dart
    │       ├── pages
    │       │   ├── page1.dart
    │       │   └── page2.dart
    │       └── widgets
    │           ├── widget1.dart
    │           └── widget2.dart
    └── main.dart
```

## Evermos Flutter Best Practice 101
In order to avoid `Premature Optimization` while breaking down software complexities, there is a things to follow so we don't get lost in the development process. We really respect the diversity of member individual thinking, but we can't implement all of them into the project, that's why this documentation & guidelines is created, to create a standard that everyone commit to agree & follow. 

Keep project folders shallow (Deep nested doesn't recommended), depend on classification project folders under `/lib` :
1. `Big chunk` this level should contain a big part of segregated code based on the Architectural view
  - common, this folder contain common files such an utils, extension class, or even a boilerplate class or function that created to be used from all project files.
  - const, this folder contain localization, values, constant, that needed to be wrote on file.
  - data, this folder contain data related files such an datasource class, model class, mapper class, and repository interface class.
  - domain
  - presentation
