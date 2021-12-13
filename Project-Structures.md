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