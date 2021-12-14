This documentation will guide every team member to write code that effective, less redundant, readable, and easy to understand for every member. Also, this documentation should be updated when there is a more sophisticated workflow. The final goal of this documentation is to guide every member to follow `Defined & Approved Standard` that can make the code more Uniform for the rest of us. In order to keep everything applicable for everyone, it's important to Classificate the Guidelines into a multiple category

# Index

Fundamental guideline 
- [Effective Dart](https://dart.dev/guides/language/effective-dart)
- [Clean Architecture](https://blog.cleancoder.com/uncle-bob/2012/08/13/the-clean-architecture.html)
- [Project Structure](https://github.com/evermos/evermos-flutter/wiki/Code-Writing-Guideline#project-structure)
- [Evermos Flutter Best Practice 101](https://github.com/evermos/evermos-flutter/wiki/Code-Writing-Guideline#evermos-flutter-best-practice-101)

## Project structure

Keep project folders shallow and avoid deeply nested projects structure, depend on classification project folders under `/lib` :
### Level 1
this level should contain a big part of segregated code based on the Architectural view
  - common, this dir contain common files such an utils, extension class, or even a boilerplate class or function that created to be used from all project files.
  - const, this dir contain localization, values, constant, that needed to be wrote on file.
  - data, this dir contain data related files such an datasources, models, mappers, and repository implementations class.
  - domain, this dir contain client side converted / processed data including : entities, usecases, repository interfaces, and custom error handler / Exception class
  - presentation, this dir contain client side user interface related files including : state management files (get, bloc, provider, so on), pages, and widgets (small level components)

### Level 2
this level should contain files depend on the ancestor level, example : `data > datasources`. For full example please take a look to the full map

### level 3 (Optional)
This level should contain more categorized files example : `data > datasources > voucher`, but there is a criteria to create level 3. If the file amount inside level 2 is more than 10. **Important notes : Directory more than level 3 should be avoided because this will conflict with modularization purposes**

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

1. Avoid deeply nested project folder & files, because it's conflicting with modularization purpose
2. Ensure task classification before write everything to a module or even new module
3. Respect legacy code, refactor is the last thing to do. Patching & updating is the best way, unless the files & project structure or any fundamentals aren't referring to our standard
4. Avoid over engineering, sometimes it's hard to distinguish our motivation to write a robust, reusable yet reliable code. But sometimes **Just working fine & didn't cause any problematic** just more than enough. Because simplicity is everyone needed
5. Choose simplicity over complexity x time relativity, don't we need a polymorphic class to wrap everything dynamically ? yes we do need to reduce a lines of code, but not to mention we also have to dealing with timelines & avoid any premature optimization & chaotic approach from the fresh start
6. Prefer classificate & categorize our code into a segregated methods, class for more reusability, overrideable, and readable. within achieving the good amount of simplicity

PS : That's it, happy coding. Update this within the forum discussions. Our standard may be obsolete in the future, when it come we need to update this documentation.