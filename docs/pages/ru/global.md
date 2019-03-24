---
title: Глобальные стили
description: CSS Foundation включает в себя ресеты, которые обеспечивают кроссбраузерную работу стилей.
sass: scss/_global.scss
---

## Размеры шрифтов

Размер основного шрифта по умолчанию установлен в 100% основного браузерного шрифта, который обычно составляет 16 пикселей. Это обеспечивает совместимость с браузерным зуммированием или собственными установками пользователей. Если вы используете Sass версию Foundation, вы можете изменить размер базового шрифта переопределив переменную `$global-font-size`. Значение может устанавливаться в процентах или пикселях.

---

## Цвета

Foundation по умолчанию имеет удобную палитру цветров. Приоритетный цвет (primary) используется для интерактивных элементов, таких как ссылки и кнопки. Вторичный (secondary), успешный (success), предупреждающий (warning) и уведомляющий (alert) цвета используются для обеспечения большего контекста для элементов и действий интерфейса.

<div class="grid-x grid-margin-x small-up-1 medium-up-3 large-up-5">
  <div class="cell">
    <div class="docs-color-block text-wrap">
      <div class="docs-color-block-primary"></div>
      <p>Приоритетный (primary)</p>
    </div>
  </div>
  <div class="cell">
    <div class="docs-color-block text-wrap">
      <div class="docs-color-block-secondary"></div>
      <p>Вторичный (secondary)</p>
    </div>
  </div>
  <div class="cell">
    <div class="docs-color-block text-wrap">
      <div class="docs-color-block-success"></div>
      <p>Успешный (success)</p>
    </div>
  </div>
  <div class="cell">
    <div class="docs-color-block text-wrap">
      <div class="docs-color-block-warning"></div>
      <p>Предупреждающий (warning)</p>
    </div>
  </div>
  <div class="cell">
    <div class="docs-color-block text-wrap">
      <div class="docs-color-block-alert"></div>
      <p>Уведомляющий (alert)</p>
    </div>
  </div>
  <div class="cell">
    <div class="docs-color-block text-wrap">
      <div class="docs-color-block-white"></div>
      <p>Белый (white)</p>
    </div>
  </div>
  <div class="cell">
    <div class="docs-color-block text-wrap">
      <div class="docs-color-block-light-gray"></div>
      <p>Светло-серый (light gray)</p>
    </div>
  </div>
  <div class="cell">
    <div class="docs-color-block text-wrap">
      <div class="docs-color-block-medium-gray"></div>
      <p>Серый (medium gray)</p>
    </div>
  </div>
  <div class="cell">
    <div class="docs-color-block text-wrap">
      <div class="docs-color-block-dark-gray"></div>
      <p>Темно-серый (dark gray)</p>
    </div>
  </div>
  <div class="cell">
    <div class="docs-color-block text-wrap">
      <div class="docs-color-block-black"></div>
      <p>Черный (black)</p>
    </div>
  </div>
</div>

---

### Изменение цветовой палитры

Если вы используете Sass версию Foundation, вы легко можете изменить цветовую палитру переопределив переменные в вашем фале настроек.

Семантические цвета (primary, secondary, success, warning, и alert) могут быть изменены в карте `$foundation-palette`. Ключи в этой карте используются для стилизации различных компонентов и конечных классов.

```scss
$foundation-palette: (
  primary: #1779ba,
  secondary: #767676,
  success: #3adb76,
  warning: #ffae00,
  alert: #cc4b37,
);
```

<div class="warning callout">
  <p>Если вы удалите дефолтный ключ из карты `$foundation-palette`, вам придется внести изменения в различные переменные Sass, использующие данный ключ.</p>
</div>

Именованные цвета (white, light gray, medium gray, dark gray, и black) могут быть изменены в соответствующих переменных

```scss
$light-gray: #e6e6e6;
$medium-gray: #cacaca;
$dark-gray: #8a8a8a;
$black: #0a0a0a;
$white: #fefefe;
```

Строка `@include add-foundation-colors;` в вашем файле настроек позволит вам использовать соответствующие переменные, ссылающиеся на *цвета по умолчанию* из палитры:

- `$primary-color`
- `$secondary-color`
- `$success-color`
- `$warning-color`
- `$alert-color`

Вы также можете использовать функцию Foundation `get-color()`, чтобы сослаться на *любой цвет* из палитры. Эта функция также дает доступ к пользовательским цветам, которые вы определили в палитре.

```scss
// Создание переменной собственного цвета
$custom-color: get-color(custom);
```
