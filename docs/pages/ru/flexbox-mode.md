---
title: Режим Flexbox
description: Для браузеров с поддержкой передовых технологий, некоторые компоненты Foundation могут быть преобразованы в компоненты с использованием flexbox.
sass:
  - scss/components/_flex.scss
  - scss/util/_flex.scss
---

## Режим Flexbox

Компоненты Foundation используют комбинацию плавающих элементов, вертикального выравнивания, таблиц и различных других хаков CSS для получения необходимого внешнего вида. Но в наши дни есть более эффективный способ, если только у вас нет какой-то причины в поддержке интерфейса для устаревших версий браузеров.

Включение **режима flexbox** заменяет все эти хаки использованием свойств flex контейнеров, что делает макеты более упорядоченными, и методы определения размеров и выравнивания элементов становятся намного проще.

Режим Flexbox поддерживается в следующих браузерах:

- Последние версии Chrome и Firefox
- Safari 6+
- IE/Edge 10+
- iOS 7+
- Android 4.4+

---

## Включение режима Flexbox

Если вы используете CSS версию Foundation, вы можете сгенерировать <a href="https://foundation.zurb.com/sites/download">свою сборку Foundation</a> с включенным режимом flexbox. Если вы используете Sass версию Foundation, вы можете включить режим flexbox двумя путями:

Если вы используете миксин `foundation-everything()` в вашем главном Sass файле, передайте ему параметр `true` для включения режима flexbox.

```scss
@include foundation-everything(true);
```

Если вы импортируете каждый компонент отдельно (как делают шаблоны наших стартовых проектов), откройте ваш файл настроек (базовый шаблон: scss/_settings.scss, шаблон ZURB: src/assets/scss/_settings.scss), установите значение переменной `$global-flexbox` в `true`, удалите `@include` для плавающей (float) сетки и замените на `@include` для flex сетки, а также для вспомогательных классов (базовый шаблон: scss/app.scss, шаблон ZURB: src/assets/scss/app.scss):

```scss
$global-flexbox: true;

// @include foundation-grid;
@include foundation-flex-grid;
@include foundation-flex-classes;
```

---

## Поддерживаемые компоненты

Помимо самой flex сетки, режим flexbox поддерживают следующие компоненты:

- [Группа кнопок (Button group)](button-group.html)
- [Группа ввода (Input group) - (Формы)](forms.html#inline-labels-and-buttons)
- [Меню](menu.html)
- [Топ-бар (Top bar)](top-bar.html)
- [Медиа объекты (Media object)](media-object.html)
- [Тайтл-бар (Title bar)](off-canvas.html#title-bar)
- [Карточка (Card)](card.html)

В основной части, в режиме flexbox, все компоненты работают также как в основном. Однако, некоторые из них требуют небольших изменений классов CSS. Обратитесь к документации каждого из них, чтобы узнать, что именно меняется.
