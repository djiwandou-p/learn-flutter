# Getting Started
This Architecture contains several layer:
- [Const](https://github.com/evermos/evermos-flutter/wiki/Clean-Architecture#const)
- [Data](https://github.com/evermos/evermos-flutter/wiki/Clean-Architecture#data)
- [Domain](https://github.com/evermos/evermos-flutter/wiki/Clean-Architecture#domain)
- [Presentation](https://github.com/evermos/evermos-flutter/wiki/Clean-Architecture#presentation)
- [Util](https://github.com/evermos/evermos-flutter/wiki/Clean-Architecture#util)

## Const
Contains all constants value that needed by the project. This layer contains internationalization (i18n), for now, this project just support in English and Indonesian value. All translation value collect in `strings` file. As you can see, there is have different strings declaration in app and module. In module, we need to add prefix module name. For example in module we need declare `productTitle`, but in app we can declare `title`. Since, module included to the app, when found same const value the compiler will confused about string declaration. We split the module and app using prefix. Another const in this layer we can store endpoint class that contains all endpoint API needed by the project.

## Data
Contains class for managerial data from network or local. There are sub layer from data layer:
- [Datasource](https://github.com/evermos/evermos-flutter/wiki/Clean-Architecture#datasources)
- [Mappers](https://github.com/evermos/evermos-flutter/wiki/Clean-Architecture#mappers)
- [Models](https://github.com/evermos/evermos-flutter/wiki/Clean-Architecture#models)
- [Repositories Implementation](https://github.com/evermos/evermos-flutter/wiki/Clean-Architecture#repositories-implementation)

### Datasources
Low level to communication direct with client for network or local storage. There will abstract and implementation class. Abstract class used for testing.

### Mappers
Contains all class to map from models under data with entity under domain.

### Models
Contains class representation for data communication from network or local. Model class can contains another platform/third party.

### Repositories Implementation
Contains implementation class of repository as bridge communication from models to entity.

## Domain
Contains class for business rules or business proccess:
- [Entities](https://github.com/evermos/evermos-flutter/wiki/Clean-Architecture#entities)
- [Repositories](https://github.com/evermos/evermos-flutter/wiki/Clean-Architecture#repositories)
- [Usecases](https://github.com/evermos/evermos-flutter/wiki/Clean-Architecture#usecases)

### Entities
Contains class representation for business rules/proccess can't contains another platform/third party.

### Repositories
Contains abstract class for repositories. This will be plans for data communication. This class usually used for testing.

### Usecases
Contains class with specific job. Just execute single responsibilities. In this class can contains business logic.

## Presentation
Contains class for user interface:
- [State Management](https://github.com/evermos/evermos-flutter/wiki/Clean-Architecture#state-management)
- [Pages](https://github.com/evermos/evermos-flutter/wiki/Clean-Architecture#pages)
- [Widgets](https://github.com/evermos/evermos-flutter/wiki/Clean-Architecture#widgets)

### State Management
Contains class that used for state management stuff. This project use GetX as state management. So, the folder name is get. When you use another state management, for example bloc, you can give folder name as bloc.

### Pages
Contains class that build the user interface. In this class we will build UI component using method for overrideable UI when have child class.

### Widgets
Contains class that component widget to support composable user interface.

## Util
Contains all util class that can help development procces.