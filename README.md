[<img src="https://avatars2.githubusercontent.com/u/27778577?s=200&v=4" align="right" width="131" height="143">](https://github.com/ngx-kit)

# Angular ngx-kit  [![Angular-RU](https://img.shields.io/badge/Github:-ng_kit-35a9ff.svg?style=flat)](https://github.com/ngx-kit) [![npm version](https://badge.fury.io/js/%40ngx-kit%2Fcore.svg)](https://www.npmjs.com/@ngx-kit/core)

Начните быструю разработку с Angular. Любое конфигурирование компонентов должно быть простым и легким. Но сегодня, вы можете просто создавать свои компоненты используя коллекцию компонентов ngx-kit, а в последующем изменять их по своему усмотрению.

## Особенности

* Поддержка AOT
* Поддержка серверного рейтинга
* Поддержка стратегит обнаружения изменений OnPush

## Минимальные требования

* Angular ^5.0.0
* Angular-cli ^1.5.0


## Руководство:

[<img src="https://habrastorage.org/webt/9l/iw/vc/9liwvcbgmipvnird_12blxfohoy.png" align="center">](https://github.com/ngx-kit)

* [Обучающий ролик](https://www.youtube.com/watch?v=th9fhD1e3d4)
* [Demo DateTimePicker (stackblitz)](https://stackblitz.com/edit/ngx-kit-date-picker-demo)

## Использование

#### Установка пакетов

```
npm i @ngx-kit/core --save
npm i @ngx-kit/collection --save-dev
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

#### Автоматическое генерирование с помощью Angular CLI

Пример быстрого встраивания кнопки:

```
ng g ui-button -c=@ngx-kit/collection my-button
```

#### На выходе:

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

#### Модификация зависимостей

Только сложная (стабильная) логика хранится в [Core] (https://ngx-kit.com/core), поэтому вы можете любым образом изменять сгенерированные шаблоны и стили.


## License

MIT
