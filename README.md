# SB Admin in Angular8 and Bootstrap 4

* [SB Admin v8.0](https://github.com/start-angular/SB-Admin-BS4-Angular-8) - это простое приложение Dashboard-админки, созданное с использованием: `Angular 8` и `Bootstrap 4`
  > Быстрый, надежный и расширяемый стартер для разработки Angular проектов

* Этот проект был создан с помощью [Angular CLI версии 8.0.0](https://github.com/angular/angular-cli)
* Демо: [SB Admin BS4 Angular5](http://rawgit.com/start-angular/SB-Admin-BS4-Angular-6/master/dist/) **(** [StartAngular](http://startangular.com/) и [StrapUI](http://strapui.com/) **)**

* Ссылка на статью с хорошим описанием, примером и исходниками проекта:
  * статья [Angular Reactive (ngrx) Authentication](https://brianflove.com/2017/04/10/angular-reactive-authentication/)
  * исходный код [Angular Reactive (ngrx) Authentication](https://github.com/ngrx/example-app/tree/master/src/app)  **(** https://github.com/blove/angular-reactive-authentication/archive/master.zip **)**
  * демо [Angular Reactive (ngrx) Authentication](https://brianflove.com/examples/angular-reactive-authentication/users/sign-in) **(** `foo@test.com` | `password` **)**

### Структура проекта

    .
    └── src                                     # Папка исходников
        │
        │
        ├── app                                 # Серверная часть приложения
        │   ├── app.component.ts                # Общие настройки для механизма комуникации между компонентами внутри веб-приложения
        │   ├── app.component.css
        │   ├── app.component.html
        │   ├── app.component.spec.ts
        │   ├── app-routing.module.ts
        │   ├── app.module.ts                   # import (декларация) всех компрнентов и пакетов приложения
        │   ├── app.reducers.ts                 # роутинг (перенаправления) - описание коммуникации внутри приложения...
        │   ├── core                            # Ядро - собраны все функции и методы для использования приложением...
        │   │   ├── models                      # Entity (сущности)
        │   │   │   └── user.model.ts
        │   │   ├── services
        │   │   │   ├── api.service.ts (rest)
        │   │   │   ├── data.service.ts (storage)
        │   │   │   └── user.service.ts
        │   │   └── util.ts
        │   ├── layout                          # Страницы представленные пользователю...
        │   │   ├── components                  # Общие элементы для каждой страницы...
        │   │   │   ├── header
        │   │   │   ├── sidebar
        │   │   │   └── footer
        │   │   ├── dashboard-1
        │   │   ├── dashboard-2
        │   │   ├── dashboard-3
        │   │   ├── layout.component.html
        │   │   ├── layout.component.css
        │   │   └── layout.component.ts
        │   ├── users                           # Специальные страницы...
        │   │   ├── account
        │   │   │   ├── account.component.html (представление)
        │   │   │   ├── account.component.scss
        │   │   │   ├── account.component.spec.ts
        │   │   │   └── account.component.ts (контроллер)
        │   │   ├── sign-in (login)
        │   │   │   ├── sign-in.component.html (представление)
        │   │   │   ├── sign-in.component.scss
        │   │   │   ├── sign-in.component.spec.ts
        │   │   │   └── sign-in.component.ts (контроллер)
        │   │   ├── sign-out (logout)
        │   │   │   ├── sign-out.component.html (представление)
        │   │   │   ├── sign-out.component.scss
        │   │   │   ├── sign-out.component.spec.ts
        │   │   │   └── sign-out.component.ts (контроллер)
        │   │   ├── sign-up (registration)
        │   │   │   ├── sign-up.component.html (представление)
        │   │   │   ├── sign-up.component.scss
        │   │   │   ├── sign-up.component.spec.ts
        │   │   │   └── sign-up.component.ts (контроллер)
        │   │   ├── users-routing.module.ts
        │   │   ├── users.actions.ts
        │   │   ├── users.effects.ts
        │   │   ├── users.module.ts
        │   │   └── users.reducers.ts
        │   ├── shared
        │   │   └── authenticated.guard.ts
        │   └── not-found
        │       ├── not-found.component.html
        │       ├── not-found.component.css
        │       └── not-found.component.ts
        ├── assets                              # Ресурсы (картинки,языки)
        │   ├── i18n
        │   │   └── en.json
        │   ├── images
        │   │   └── logo.png
        ├── styles                              # Стили
        │   ├── bootstrap
        │   │   └── *.css
        │   └── main.css                        # Основной стиль для всего приложения
        └── index.html                          # Главная страница

### Introduction

*   Developed using boostrap-v4.0.0
*   angular-v8.0.0
*   angular/cli-v8.0.0
*   [ng-bootstrap-v4.0.0](https://github.com/ng-bootstrap/)
*   [ngx-translate-v11.0.0](https://github.com/ngx-translate)
*   Following the best practices.
*   Ahead-of-Time compilation support.
*   Official Angular i18n support.
*   Production and development builds.
*   Tree-Shaking production builds.

### How to start

**Note** that this seed project requires **node >=v8.9.0 and npm >=4**.

In order to start the project use:

```bash
$ git clone https://github.com/start-angular/SB-Admin-BS4-Angular-6.git
$ cd SB-Admin-BS4-Angular-6
# install the project's dependencies
$ npm install
# watches your files and uses livereload by default run `npm start` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.
$ ng serve
# or `npm start`
# prod build, will output the production application in `dist`
# the produced code can be deployed (rsynced) to a remote server
$ npm run build
```

### Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive/pipe/service/class/module`.

### Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

### Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).
Before running the tests make sure you are serving the app via `ng serve`.

### Developer

1. Создать новый проект ```ng new angular-reactive-authentication```
2. Установить нужные пакеты для работы приложения ```npm install @angular/flex-layout @angular/material @angular/animations @ngrx/core @ngrx/store @ngrx/effects @ngrx/router-store ngrx-store-freeze reselect --save```
3. Создать новую модель в проекте ```ng g module users/users```
4. Создать новый сервис в проекте ```ng g service core/services/user```
   - (позволяет нам защищать маршруты путем реализации интерфейсов CanActivate и CanLoad) ```ng g guard shared/authentication```
5. Создать новый компонент ```ng g component users/sign-in```
6. One helpful tool for debugging is the Redux DevTools Google Chrome browser extension ```npm install @ngrx/store-devtools --save```
