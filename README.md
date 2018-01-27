[<img src="https://avatars2.githubusercontent.com/u/27778577?s=200&v=4" align="right" width="131" height="143">](https://github.com/ngx-kit)

# Angular ngx-kit  [![Angular-RU](https://img.shields.io/badge/Github:-ng_kit-35a9ff.svg?style=flat)](https://github.com/ngx-kit) [![npm version](https://badge.fury.io/js/%40ngx-kit%2Fcore.svg)](https://www.npmjs.com/@ngx-kit/core)

Приветсвую всех участников и гостей сообщества Angular-RU. На данной странице вы найдете информацию об [ngx-kit](https://ngx-kit.com) на русском языке.

Если вы активно работаете с Angular, то наверняка сталкивались с тем, что сторонний компонент не поддерживает какой-то функционал, работает неправильно или выглядит не совсем так, как того требует заказчик-дизайнер-бизнес.

Ngx-kit - это не классическая либа компонентов, а набор генераторов. Что дает возможность быстро добавить компоненты в проект, получив полный доступ к кастомизации.

### [@ngx-kit/core](https://ngx-kit.com/core/docs/OVERVIEW)

Ядро - самостоятельный пакет, который содержит сервисы для упрощения кода сгенерированных компонентов.

### [@ngx-kit/collection](https://ngx-kit.com/collection/docs/OVERVIEW)

Коллекция — это набор генераторов кода, который существенно ускоряет работу с ядром. За несколько секунд вы можете добавить любой компонент и потом быстро его модифицировать под свои нужды. Ознакомиться со списком существующих модулей можно [на сайте](https://ngx-kit.com/collection/docs/OVERVIEW). 


## Особенности

* Поддержка AOT
* Поддержка серверного рендеринга
* Поддержка OnPush стратегии обнаружения изменений
* Генерация кода с помощью Angular CLI


## Минимальные требования

* Angular ^5.0.0
* Angular-cli ^1.5.0


## Руководство:

[<img src="https://habrastorage.org/webt/9l/iw/vc/9liwvcbgmipvnird_12blxfohoy.png" align="center">](https://github.com/ngx-kit)

На видео показана быстрая установка пакетов, генерация кода дейт-пикера и его кастомизация.

* [Демо-ролик](https://www.youtube.com/watch?v=th9fhD1e3d4)
* [Код из демо-ролика (stackblitz)](https://stackblitz.com/edit/ngx-kit-date-picker-demo)


## Использование

#### Установка пакетов

```
npm i @ngx-kit/core --save
npm i @ngx-kit/collection @angular-devkit/core --save-dev
```

#### Импорт модулей

```typescript
import { KitRootModule, KitModule, KitPlatformBrowserModule } from '@ngx-kit/core';

@NgModule({
  ...
  imports: [
    ...
    KitRootModule,
    KitModule,
    KitPlatformBrowserModule,
```

#### Генерация кода с помощью Angular CLI

Пример генерации модуля для кнопки:

```
ng g ui-button -c=@ngx-kit/collection my-button
```

В данном примере я использвал итоговое имя `my-button`, но оно может быть любым на ваше усмотрение. Что позволяет один и тот же шаблон генерировать несколько раз в рамках одного проекта и модифицировать его под разные нужды.

#### Подключение сгенерированного модуля

```typescript
@NgModule({
  ...
  imports: [
    ...
    MyButtonModule,
```

#### Использование компонента

```html
<button myButton color="primary">Let's do it!</button>
```

#### Модификация кода

Только сложная (и стабильная) логика хранится в [Core-пакете] (https://ngx-kit.com/core), поэтому вы можете любым образом изменять сгенерированные шаблоны и стили.


## License

MIT
