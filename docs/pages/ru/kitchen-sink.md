---
title: Элементы
description: Все элементы одной страницей.
---

## Валидатор (Abide)


<div class="docs-codepen-container" data-ks-codepen>
  <a class="codepen-logo-link" href="https://codepen.io/IamManchanda/pen/qmoKbK?editors=1000" target="_blank"><img src="{{root}}assets/img/logos/edit-in-browser.svg" class="" height="" width="" alt="редактировать на codepen"></a>
</div>

```html_example
<form data-abide novalidate>
  <div class="grid-x grid-margin-x">
    <div class="cell">
      <div data-abide-error class="alert callout" style="display: none;">
        <p><i class="fi-alert"></i> Есть некоторые ошибки в форме.</p>
      </div>
    </div>
  </div>
  <div class="grid-x grid-margin-x">
    <div class="cell small-12">
      <label>Требуется число
        <input type="text" placeholder="1234" aria-describedby="exampleHelpText" required pattern="number">
        <span class="form-error">
          Необходимо корректно заполнить это поле.
        </span>
      </label>
      <p class="help-text" id="exampleHelpText">Информационный текст к полю</p>
    </div>
    <div class="cell small-12">
      <label>Ничего не требуется!
        <input type="text" placeholder="Можно заполнить поле, а можно не заполнять" aria-describedby="exampleHelpTex" data-abide-ignore>
      </label>
      <p class="help-text" id="exampleHelpTex">Это поле игнорируется валидатором благодаря `data-abide-ignore`</p>
    </div>
    <div class="cell small-12">
      <label>Требуется пароль
        <input type="password" id="password" placeholder="yeti4preZ" aria-describedby="exampleHelpText" required >
        <span class="form-error">
          Меня необходимо заполнить!
        </span>
      </label>
      <p class="help-text" id="exampleHelpText">Введите пароль, пожалуйста.</p>
    </div>
    <div class="cell small-12">
      <label>Повтор пароля
        <input type="password" placeholder="yeti4preZ" aria-describedby="exampleHelpText2" required pattern="alpha_numeric" data-equalto="password">
        <span class="form-error">
         Пароли должны совпадать!
        </span>
      </label>
      <p class="help-text" id="exampleHelpText2">Это поле использует атрибут `data-equalto="password"`, что указывает на необходимость совпадения с полем password.</p>
    </div>
  </div>
  <div class="grid-x grid-margin-x">
    <div class="cell medium-6">
      <label>URL шаблон, не требует заполнения, но показывает ошибку в случае, если заполненное значение не соответсвует Регулярному выражению валидного URL.
        <input type="text" placeholder="http://foundation.narusskom.info" pattern="url">
      </label>
    </div>
    <div class="cell medium-6">
      <label>Европейские автомобили. Выберите один. Пустой вариант оставлять нельзя.
        <select id="select" required>
          <option value=""></option>
          <option value="volvo">Volvo</option>
          <option value="saab">Saab</option>
          <option value="mercedes">Mercedes</option>
          <option value="audi">Audi</option>
        </select>
      </label>
    </div>
  </div>
  <div class="grid-x grid-margin-x">
    <fieldset class="cell medium-6">
      <legend>Выберите любимый цвет. Выбор обязателен.</legend>
      <input type="radio" name="pokemon" value="Red" id="pokemonRed"><label for="pokemonRed">Красный</label>
      <input type="radio" name="pokemon" value="Blue" id="pokemonBlue" required><label for="pokemonBlue">Голубой</label>
      <input type="radio" name="pokemon" value="Yellow" id="pokemonYellow"><label for="pokemonYellow">Желтый</label>
    </fieldset>
    <fieldset class="cell medium-6">
      <legend>Выберите любимый цвет. Выбор не обязателен.</legend>
      <input type="radio" name="pockets" value="Red" id="pocketsRed"><label for="pocketsRed">Красный</label>
      <input type="radio" name="pockets" value="Blue" id="pocketsBlue"><label for="pocketsBlue">Голубой</label>
      <input type="radio" name="pockets" value="Yellow" id="pocketsYellow"><label for="pocketsYellow">Желтый</label>
    </fieldset>
    <fieldset class="cell medium-6">
      <legend>Один из вариантов обязательный. Угадайте какой!</legend>
      <input id="checkbox1" type="checkbox"><label for="checkbox1">Вариант 1</label>
      <input id="checkbox2" type="checkbox" required><label for="checkbox2">Вариант 2</label>
      <input id="checkbox3" type="checkbox"><label for="checkbox3">Вариант 3</label>
    </fieldset>
  </div>
  <div class="grid-x grid-margin-x">
    <fieldset class="cell medium-6">
      <button class="button" type="submit" value="Submit">Отправить</button>
    </fieldset>
    <fieldset class="cell medium-6">
      <button class="button" type="reset" value="Reset">Сбросить</button>
    </fieldset>
  </div>
</form>
```

---

## Аккордеон (Accordion)


<div class="docs-codepen-container" data-ks-codepen>
  <a class="codepen-logo-link" href="https://codepen.io/IamManchanda/pen/WjzKqa?editors=1000" target="_blank"><img src="{{root}}assets/img/logos/edit-in-browser.svg" class="" height="" width="" alt="редактировать на codepen"></a>
</div>

```html_example
<ul class="accordion" data-accordion>
  <li class="accordion-item is-active" data-accordion-item>
    <a href="#" class="accordion-title">Аккордеон 1</a>
    <div class="accordion-content" data-tab-content >
      <p>Панель 1. Lorem ipsum dolor</p>
      <a href="#">Некуда переходить</a>
    </div>
  </li>
  <li class="accordion-item" data-accordion-item>
    <a href="#" class="accordion-title">Аккордеон 2</a>
    <div class="accordion-content" data-tab-content>
      <textarea></textarea>
      <button class="button">Я ничего не делаю!</button>
    </div>
  </li>
  <li class="accordion-item" data-accordion-item>
    <a href="#" class="accordion-title">Аккордеон 3</a>
    <div class="accordion-content" data-tab-content>
      Наберите свое имя!
      <input type="text"></input>
    </div>
  </li>
</ul>
```


---

## Аккордеон Меню (Accordion Menu)


<div class="docs-codepen-container" data-ks-codepen>
  <a class="codepen-logo-link" href="https://codepen.io/IamManchanda/pen/XREPVK?editors=1000" target="_blank"><img src="{{root}}assets/img/logos/edit-in-browser.svg" class="" height="" width="" alt="редактировать на codepen"></a>
</div>

```html_example
<ul class="vertical menu" data-accordion-menu>
  <li>
    <a href="#0">Элемент 1</a>
    <ul class="menu vertical nested is-active">
      <li>
        <a href="#0">Элемент 1A</a>
        <ul class="menu vertical nested">
          <li><a href="#0">Элемент 1Ai</a></li>
          <li><a href="#0">Элемент 1Aii</a></li>
          <li><a href="#0">Элемент 1Aiii</a></li>
        </ul>
      </li>
      <li><a href="#0">Элемент 1B</a></li>
      <li><a href="#0">Элемент 1C</a></li>
    </ul>
  </li>
  <li>
    <a href="#0">Элемент 2</a>
    <ul class="menu vertical nested">
      <li><a href="#0">Элемент 2A</a></li>
      <li><a href="#0">Элемент 2B</a></li>
    </ul>
  </li>
  <li><a href="#0">Элемент 3</a></li>
</ul>
```

---

## Бейдж (Badge)


<div class="docs-codepen-container" data-ks-codepen>
  <a class="codepen-logo-link" href="https://codepen.io/IamManchanda/pen/JNvKZj?editors=1000" target="_blank"><img src="{{root}}assets/img/logos/edit-in-browser.svg" class="" height="" width="" alt="редактировать на codepen"></a>
</div>

```html_example
<span class="primary badge">1</span>
<span class="secondary badge">2</span>
<span class="success badge">3</span>
<span class="alert badge">A</span>
<span class="warning badge">B</span>
```

---

## Хлебные крошки (Breadcrumbs)


<div class="docs-codepen-container" data-ks-codepen>
  <a class="codepen-logo-link" href="https://codepen.io/IamManchanda/pen/MmGeMx?editors=1000" target="_blank"><img src="{{root}}assets/img/logos/edit-in-browser.svg" class="" height="" width="" alt="редактировать на codepen"></a>
</div>

```html_example
<nav aria-label="You are here:" role="navigation">
  <ul class="breadcrumbs">
    <li><a href="#0">Главная</a></li>
    <li><a href="#0">Возможности</a></li>
    <li class="disabled">Генная инженерия</li>
    <li>
      <span class="show-for-sr">Текущая: </span> Клонирование
    </li>
  </ul>
</nav>
```

---

## Кнопка (Button)


<div class="docs-codepen-container" data-ks-codepen>
  <a class="codepen-logo-link" href="https://codepen.io/IamManchanda/pen/ybjagd?editors=1000" target="_blank"><img src="{{root}}assets/img/logos/edit-in-browser.svg" class="" height="" width="" alt="редактировать на codepen"></a>
</div>

```html_example
<!-- Якоря (ссылки) -->
<a href="#0" class="button">Читать еще</a>
<a href="#features" class="button">Смотреть все варианты</a>

<!-- Кнопки (действия) -->
<button type="button" class="success button">Сохранить</button>
<button type="button" class="alert button">Удалить</button>

<a class="tiny button" href="#0">Крошечная</a>
<a class="small button" href="#0">Маленькая</a>
<a class="large button" href="#0">Большая</a>
<a class="expanded button" href="#0">На всю ширину</a>

<div class="button-group">
  <a class="button">Один</a>
  <a class="button">Два</a>
  <a class="button">Три</a>
</div>
```

---

## Выноска (Callout)


<div class="docs-codepen-container" data-ks-codepen>
  <a class="codepen-logo-link" href="https://codepen.io/IamManchanda/pen/XRqjxj?editors=1000" target="_blank"><img src="{{root}}assets/img/logos/edit-in-browser.svg" class="" height="" width="" alt="редактировать на codepen"></a>
</div>

```html_example
<div class="callout">
  <h5>Это выноска.</h5>
  <p>Ее визуальный стиль легко переопределяется.</p>
  <a href="#0">Ссылка</a>
</div>

<div class="callout primary">
   <h5>Это основная (primary) выноска.</h5>
   <p>Ее визуальный стиль легко переопределяется.</p>
   <a href="#0">Ссылка</a>
</div>

<div class="callout secondary">
   <h5>Это вторичная (secondary) выноска.</h5>
   <p>Ее визуальный стиль легко переопределяется.</p>
   <a href="#0">Ссылка</a>
</div>

<div class="callout success">
   <h5>Это подтверждающая (success) выноска.</h5>
   <p>Ее визуальный стиль легко переопределяется.</p>
   <a href="#0">Ссылка</a>
</div>

<div class="callout warning">
   <h5>Это предупеждающая (warning) выноска.</h5>
   <p>Ее визуальный стиль легко переопределяется.</p>
   <a href="#0">Ссылка</a>
</div>

<div class="callout alert">
   <h5>Это уведомляющая (alert) выноска.</h5>
   <p>Ее визуальный стиль легко переопределяется.</p>
   <a href="#0">Ссылка</a>
</div>
```

---

## Кнопка "закрыть" (Close Button)


<div class="docs-codepen-container" data-ks-codepen>
  <a class="codepen-logo-link" href="https://codepen.io/IamManchanda/pen/dWepJz?editors=1000" target="_blank"><img src="{{root}}assets/img/logos/edit-in-browser.svg" class="" height="" width="" alt="редактировать на codepen"></a>
</div>

```html_example
<div class="callout" data-closable>
  <button class="close-button" aria-label="Close alert" type="button" data-close>
    <span aria-hidden="true">&times;</span>
  </button>
  <p>Это пример кнопки "закрыть".</p>
</div>
```

---

## Меню углубления (Drilldown Menu)


<div class="docs-codepen-container" data-ks-codepen>
  <a class="codepen-logo-link" href="https://codepen.io/IamManchanda/pen/mmLrZz?editors=1000" target="_blank"><img src="{{root}}assets/img/logos/edit-in-browser.svg" class="" height="" width="" alt="редактировать на codepen"></a>
</div>

```html_example
<ul class="vertical menu" data-drilldown style="width: 200px" id="m1">
  <li>
    <a href="#0">Элемент 1</a>
    <ul class="vertical menu" id="m2">
      <li>
        <a href="#0">Элемент 1A</a>
        <ul class="vertical menu" id="m3">
          <li><a href="#0">Элемент 1Aa</a></li>
          <li><a href="#0">Элемент 1Ba</a></li>
          <li><a href="#0">Элемент 1Ca</a></li>
          <li><a href="#0">Элемент 1Da</a></li>
          <li><a href="#0">Элемент 1Ea</a></li>
        </ul>
      </li>
      <li><a href="#0">Элемент 1B</a></li>
      <li><a href="#0">Элемент 1C</a></li>
      <li><a href="#0">Элемент 1D</a></li>
      <li><a href="#0">Элемент 1E</a></li>
    </ul>
  </li>
  <li>
    <a href="#0">Элемент 2</a>
    <ul class="vertical menu">
      <li><a href="#0">Элемент 2A</a></li>
      <li><a href="#0">Элемент 2B</a></li>
      <li><a href="#0">Элемент 2C</a></li>
      <li><a href="#0">Элемент 2D</a></li>
      <li><a href="#0">Элемент 2E</a></li>
    </ul>
  </li>
  <li>
    <a href="#0">Элемент 3</a>
    <ul class="vertical menu">
      <li><a href="#0">Элемент 3A</a></li>
      <li><a href="#0">Элемент 3B</a></li>
      <li><a href="#0">Элемент 3C</a></li>
      <li><a href="#0">Элемент 3D</a></li>
      <li><a href="#0">Элемент 3E</a></li>
    </ul>
  </li>
  <li><a href='#0'>Элемент 4</a></li>
</ul>
```

---

## Низпадающее меню (Dropdown Menu)


<div class="docs-codepen-container" data-ks-codepen>
  <a class="codepen-logo-link" href="https://codepen.io/IamManchanda/pen/jmxVPP?editors=1000" target="_blank"><img src="{{root}}assets/img/logos/edit-in-browser.svg" class="" height="" width="" alt="редактировать на codepen"></a>
</div>

```html_example
<ul class="dropdown menu" data-dropdown-menu>
  <li>
    <a>Элемент 1</a>
    <ul class="menu">
      <li><a href="#0">Элемент 1A Длииинный</a></li>
      <li>
        <a href='#0'> Элемент 1 sub</a>
        <ul class="menu">
          <li><a href='#0'>Элемент 1 subA</a></li>
          <li><a href='#0'>Элемент 1 subB</a></li>
          <li>
            <a href='#0'> Элемент 1 subC</a>
            <ul class="menu">
              <li><a href='#0'>Элемент 1 subCA</a></li>
              <li><a href='#0'>Элемент 1 subCB</a></li>
            </ul>
          </li>
          <li>
            <a href='#0'> Элемент 1 subD</a>
            <ul class="menu">
              <li><a href='#0'>Элемент 1 subDA</a></li>
            </ul>
          </li>
        </ul>
      </li>
      <li><a href="#0">Элемент 1B</a></li>
    </ul>
  </li>
  <li>
    <a href="#0">Элемент 2</a>
    <ul class="menu">
      <li><a href="#0">Элемент 2A</a></li>
      <li><a href="#0">Элемент 2B</a></li>
    </ul>
  </li>
  <li><a href="#0">Элемент 3</a></li>
  <li><a href='#0'>Элемент 4</a></li>
</ul>
```

---

## Низпадающая панель (Dropdown Pane)


<div class="docs-codepen-container" data-ks-codepen>
  <a class="codepen-logo-link" href="https://codepen.io/IamManchanda/pen/QvrGGj?editors=1000" target="_blank"><img src="{{root}}assets/img/logos/edit-in-browser.svg" class="" height="" width="" alt="редактировать на codepen"></a>
</div>

```html_example
<button class="button" type="button" data-toggle="example-dropdown">Открыть/Закрыть панель</button>
<div class="dropdown-pane" id="example-dropdown" data-dropdown>
  Текст содержимого панели. Здесь может быть много текста. Столько, сколько надо.
</div>
```

---

## Эквалайзер (Equalizer)


<div class="docs-codepen-container" data-ks-codepen>
  <a class="codepen-logo-link" href="https://codepen.io/IamManchanda/pen/mmLBEa?editors=1000" target="_blank"><img src="{{root}}assets/img/logos/edit-in-browser.svg" class="" height="" width="" alt="редактировать на codepen"></a>
</div>

```html_example
<div class="grid-x grid-margin-x" data-equalizer data-equalize-on="medium" id="test-eq">
  <div class="cell medium-4">
    <div class="callout" data-equalizer-watch>
      <img src= "assets/img/generic/square-1.jpg">
    </div>
  </div>
  <div class="cell medium-4">
    <div class="callout" data-equalizer-watch>
      <p>Pellentesque habitant morbi tristique senectus et netus et, ante.</p>
    </div>
  </div>
  <div class="cell medium-4">
    <div class="callout" data-equalizer-watch>
      <img src= "assets/img/generic/rectangle-1.jpg">
    </div>
  </div>
</div>
```

---

## Плавающая Сетка (Flex Grid)


<div class="docs-codepen-container" data-ks-codepen>
  <a class="codepen-logo-link" href="http://codepen.io/ZURBFoundation/pen/dWmVax?editors=1000" target="_blank"><img src="{{root}}assets/img/logos/edit-in-browser.svg" class="" height="" width="" alt="редактировать на codepen"></a>
</div>

```html
<div class="row">
  <div class="small-6 columns">6 колонок</div>
  <div class="small-6 columns">6 колонок</div>
</div>
<div class="row">
  <div class="medium-6 large-4 columns">12/6/4 колонок</div>
  <div class="medium-6 large-8 columns">12/6/8 колонок</div>
</div>
```

<div class="row display">
  <div class="small-6 columns">6 колонок</div>
  <div class="small-6 columns">6 колонок</div>
</div>
<div class="row display">
  <div class="medium-6 large-4 columns">12/6/4 колонок</div>
  <div class="medium-6 large-8 columns">12/6/8 колонок</div>
</div>

---

## Адаптивное содержимое (Responsive Embed)


<div class="docs-codepen-container" data-ks-codepen>
  <a class="codepen-logo-link" href="https://codepen.io/IamManchanda/pen/MmGEbb?editors=1000" target="_blank"><img src="{{root}}assets/img/logos/edit-in-browser.svg" class="" height="" width="" alt="редактировать на codepen"></a>
</div>

```html_example
<div class="responsive-embed">
  <iframe width="420" height="315" src="https://www.youtube.com/embed/mM5_T-F1Yn4" frameborder="0" allowfullscreen></iframe>
</div>
```

---

## Флоат классы (Float Classes)


<div class="docs-codepen-container" data-ks-codepen>
  <a class="codepen-logo-link" href="https://codepen.io/IamManchanda/pen/zwjEPP?editors=1000" target="_blank"><img src="{{root}}assets/img/logos/edit-in-browser.svg" class="" height="" width="" alt="редактировать на codepen"></a>
</div>

```html_example
<div class="callout clearfix">
  <a class="button float-left">Левый</a>
  <a class="button float-right">Правый</a>
</div>
```

---

## Формы (Forms)


<div class="docs-codepen-container" data-ks-codepen>
  <a class="codepen-logo-link" href="https://codepen.io/IamManchanda/pen/jmxGGr?editors=1000" target="_blank"><img src="{{root}}assets/img/logos/edit-in-browser.svg" class="" height="" width="" alt="редактировать на codepen"></a>
</div>

```html_example
<form>
  <label>Ярлык поля ввода
    <input type="text" placeholder=".small-12.columns" aria-describedby="exampleHelpText">
  </label>
  <p class="help-text" id="exampleHelpText">Дополнительная информация для поля ввода.</p>
  <label>
    Сколько щенков?
    <input type="number" value="100">
  </label>
  <label>
   Какие книги вы прочитали за летние каникулы?
    <textarea placeholder="Никакие"></textarea>
  </label>
  <label>Меню выбора
    <select>
      <option value="husker">Husker</option>
      <option value="starbuck">Starbuck</option>
      <option value="hotdog">Hot Dog</option>
      <option value="apollo">Apollo</option>
    </select>
  </label>
  <div class="grid-x grid-margin-x">
    <fieldset class="cell large-6">
      <legend>Выберите цвет</legend>
      <input type="radio" name="pokemon" value="Red" id="formRed" required><label for="formRed">Красный</label>
      <input type="radio" name="pokemon" value="Blue" id="formBlue"><label for="formBlue">Синий</label>
      <input type="radio" name="pokemon" value="Yellow" id="formYellow"><label for="formYellow">Желтый</label>
    </fieldset>
    <fieldset class="cell large-6">
      <legend>Выберите</legend>
      <input id="formCheckbox1" type="checkbox"><label for="formCheckbox1">Вариант 1</label>
      <input id="formCheckbox2" type="checkbox"><label for="formCheckbox2">Вариант 2</label>
      <input id="formCheckbox3" type="checkbox"><label for="formCheckbox3">Вариант 3</label>
    </fieldset>
  </div>
  <div class="grid-x grid-margin-x">
    <div class="cell small-3">
      <label for="middle-label" class="text-right middle">Ярлык</label>
    </div>
    <div class="cell small-9">
      <input type="text" id="middle-label" placeholder="Поле ввода по правому краю">
    </div>
  </div>
  <div class="input-group">
    <span class="input-group-label">$</span>
    <input class="input-group-field" type="url">
    <div class="input-group-button">
      <input type="submit" class="button" value="Отправить">
    </div>
  </div>
</form>
```

---

## Сетка (Grid)


<div class="docs-codepen-container" data-ks-codepen>
  <a class="codepen-logo-link" href="https://codepen.io/IamManchanda/pen/rmvEBJ?editors=1000" target="_blank"><img src="{{root}}assets/img/logos/edit-in-browser.svg" class="" height="" width="" alt="редактировать на codepen"></a>
</div>

```html
<div class="row">
  <div class="small-2 medium-3 large-4 columns">2/3/4 колонок</div>
  <div class="small-4 medium-3 large-4 columns">4/3/4 колонок</div>
  <div class="small-6 large-4 columns">6/6/4 колонок</div>
</div>
<div class="row">
  <div class="large-3 columns">12/12/3 колонок</div>
  <div class="large-6 columns">12/12/6 колонок</div>
  <div class="large-3 columns">12/12/3 колонок</div>
</div>
<div class="row">
  <div class="small-6 large-2 columns">6/6/2 колонок</div>
  <div class="small-6 large-8 columns">6/6/8 колонок</div>
  <div class="small-12 large-2 columns">12/12/2 колонок</div>
</div>
<div class="row">
  <div class="small-3 columns">3 колонок</div>
  <div class="small-9 columns">9 колонок</div>
</div>
<div class="row">
  <div class="medium-8 large-4 columns">12/8/4 колонок</div>
  <div class="medium-4 large-8 columns">12/4/8 колонок</div>
</div>
```

<div class="row display">
  <div class="small-2 medium-3 large-4 columns">2/3/4 колонок</div>
  <div class="small-4 medium-3 large-4 columns">4/3/4 колонок</div>
  <div class="small-6 large-4 columns">6/6/4 колонок</div>
</div>
<div class="row display">
  <div class="large-3 columns">12/12/3 колонок</div>
  <div class="large-6 columns">12/12/6 колонок</div>
  <div class="large-3 columns">12/12/3 колонок</div>
</div>
<div class="row display">
  <div class="small-6 large-2 columns">6/6/2 колонок</div>
  <div class="small-6 large-8 columns">6/6/8 колонок</div>
  <div class="small-12 large-2 columns">12/12/2 колонок</div>
</div>
<div class="row display">
  <div class="small-3 columns">3 колонок</div>
  <div class="small-9 columns">9 колонок</div>
</div>
<div class="row display">
  <div class="medium-8 large-4 columns">12/8/4 колонок</div>
  <div class="medium-4 large-8 columns">12/4/8 колонок</div>
</div>

---

## Подстраивающееся содержимое (Interchange)


<div class="docs-codepen-container" data-ks-codepen>
  <a class="codepen-logo-link" href="https://codepen.io/IamManchanda/pen/xdjXYj?editors=1000" target="_blank"><img src="{{root}}assets/img/logos/edit-in-browser.svg" class="" height="" width="" alt="редактировать на codepen"></a>
</div>

```html_example
<img data-interchange="[assets/img/interchange/small.jpg, small], [assets/img/interchange/medium.jpg, medium], [assets/img/interchange/large.jpg, large]">
```

---

## Ярлык (Label)


<div class="docs-codepen-container" data-ks-codepen>
  <a class="codepen-logo-link" href="https://codepen.io/IamManchanda/pen/VbxMXq?editors=1000" target="_blank"><img src="{{root}}assets/img/logos/edit-in-browser.svg" class="" height="" width="" alt="редактировать на codepen"></a>
</div>

```html_example
<span class="primary label">Основной (primary) ярлык</span>
<span class="secondary label">Вторичный (secondary) ярлык</span>
<span class="success label">Успешный (success) ярлык</span>
<span class="alert label">Уведомляющий (alert) ярлык</span>
<span class="warning label">Предупреждающий (warning) ярлык</span>
```

---

## Магеллан навигация (Magellan)


<div class="docs-codepen-container" data-ks-codepen>
  <a class="codepen-logo-link" href="https://codepen.io/IamManchanda/pen/MmGEXo?editors=1000" target="_blank"><img src="{{root}}assets/img/logos/edit-in-browser.svg" class="" height="" width="" alt="редактировать на codepen"></a>
</div>

```html_example
<ul class="horizontal menu" data-magellan>
  <li><a href="#first">Первая секция</a></li>
  <li><a href="#second">Вторая секция</a></li>
  <li><a href="#third">Третья секция</a></li>
</ul>
<div class="sections">
  <section id="first" data-magellan-target="first">
    <h4>Первая секция</h4>
    <p>Duis scelerisque ligula ut metus rhoncus scelerisque. Integer ut egestas metus. Nulla facilisi. Aenean luctus magna lobortis ligula rhoncus, sit amet lacinia lorem sagittis. Sed ultrices at metus id aliquet. Vestibulum in condimentum quam, id ornare erat. Vivamus nec justo quis ex fringilla condimentum ac non quam.</p>
  </section>
  <section id="second" data-magellan-target="second">
    <h4>Вторая секция</h4>
    <p>Sed vulputate, felis interdum molestie viverra, neque urna placerat dui, ac efficitur est magna eu tellus. Nunc sodales consequat eros at bibendum. Vestibulum hendrerit gravida elit non eleifend. Nunc at vehicula ipsum. Vestibulum eu suscipit felis. Proin ipsum felis, consequat congue quam ac, efficitur tincidunt ex. Morbi accumsan sem iaculis nunc malesuada tincidunt.</p>
  </section>
  <section id="third" data-magellan-target="third">
    <h4>Третья секция</h4>
    <p>Aliquam orci orci, maximus a pulvinar id, tincidunt a neque. Suspendisse eros diam, finibus et faucibus ac, suscipit feugiat orci. Morbi scelerisque sem id blandit malesuada. Donec suscipit tincidunt dolor in blandit. Nam rhoncus risus vitae lacinia dictum. Cras lobortis, nulla non faucibus mattis, tellus nibh condimentum eros, posuere volutpat arcu risus vel ante. In ut ullamcorper eros, et vestibulum risus. Fusce auctor risus vitae diam viverra tincidunt.</p>
  </section>
</div>
```

---

## Медиа объект (Media Object)


<div class="docs-codepen-container" data-ks-codepen>
  <a class="codepen-logo-link" href="https://codepen.io/IamManchanda/pen/NjMaEr?editors=1000" target="_blank"><img src="{{root}}assets/img/logos/edit-in-browser.svg" class="" height="" width="" alt="редактировать на codepen"></a>
</div>

```html_example
<div class="media-object">
  <div class="media-object-section">
    <img src= "https://placeimg.com/200/200/people">
  </div>
  <div class="media-object-section">
    <h4>Мечты реальны пока мы в них.</h4>
    <p>В сердце каждого человека заложена сила, помогающая получить желаемое. Она не даст покоя, пока ты не дойдешь до той самой точки, к которой стремился. Все возможно при одном условии: по-настоящему хотеть того, к чему идешь.</p>
  </div>
</div>
```

---

## Меню (Menu)


<div class="docs-codepen-container" data-ks-codepen>
  <a class="codepen-logo-link" href="https://codepen.io/IamManchanda/pen/bWMMzZ?editors=1000" target="_blank"><img src="{{root}}assets/img/logos/edit-in-browser.svg" class="" height="" width="" alt="редактировать на codepen"></a>
</div>

```html_example
<ul class="menu">
  <li><a href="#0"><i class="fi-list"></i> <span>Один</span></a></li>
  <li><a href="#0"><i class="fi-list"></i> <span>Два</span></a></li>
  <li><a href="#0"><i class="fi-list"></i> <span>Три</span></a></li>
  <li><a href="#0"><i class="fi-list"></i> <span>Четыре</span></a></li>
</ul>
```

---

## Сдвиг холста (Off-canvas)


<div class="docs-codepen-container" data-ks-codepen>
  <a class="codepen-logo-link" href="https://codepen.io/IamManchanda/pen/oWdrLR?editors=1000" target="_blank"><img src="{{root}}assets/img/logos/edit-in-browser.svg" class="" height="" width="" alt="редактировать на codepen"></a>
</div>

```html_example
<!-- Настройки Off-canvas -->
<body>
  <div class="off-canvas-wrapper">
    <div class="off-canvas-wrapper-inner" data-off-canvas-wrapper>
      <div class="off-canvas position-left" id="offCanvasLeft" data-off-canvas>
        <!-- левая разметка off-canvas -->
      </div>
      <div class="off-canvas position-right" id="offCanvasRight" data-off-canvas data-position="right">
        <!-- правая разметка off-canvas -->
      </div>
      <div class="off-canvas-content" data-off-canvas-content>
        <!-- содержимое страницы -->
      </div>
    </div>
  </div>
</body>

<!-- Вызов Off-canvas -->
<button type="button" class="button" data-toggle="offCanvasLeft">Открыть меню</button>
```

---

## Слайдер Orbit


<div class="docs-codepen-container" data-ks-codepen>
  <a class="codepen-logo-link" href="https://codepen.io/IamManchanda/pen/zwjjgN?editors=1000" target="_blank"><img src="{{root}}assets/img/logos/edit-in-browser.svg" class="" height="" width="" alt="редактировать на codepen"></a>
</div>

```html_example
<div class="orbit" role="region" aria-label="Favorite Text Ever" data-orbit>
  <ul class="orbit-container">
    <button class="orbit-previous" aria-label="previous"><span class="show-for-sr">Предыдущий слайд</span>&#9664;</button>
    <button class="orbit-next" aria-label="next"><span class="show-for-sr">Следующий слайд</span>&#9654;</button>
    <li class="is-active orbit-slide">
      <div class="docs-example-orbit-slide">
        <p><strong>Первый</strong> Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
      </div>
    </li>
    <li class="orbit-slide">
      <div class="docs-example-orbit-slide">
        <p><strong>Второй</strong> Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
      </div>
    </li>
    <li class="orbit-slide">
      <div class="docs-example-orbit-slide">
        <p><strong>Третий</strong> Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
      </div>
    </li>
    <li class="orbit-slide">
      <div class="docs-example-orbit-slide">
        <p><strong>Четвертый</strong> Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
      </div>
    </li>
  </ul>
  <nav class="orbit-bullets">
    <button class="is-active" data-slide="0">
      <span class="show-for-sr">Первый слайд</span>
      <span class="show-for-sr" data-slide-active-label>Текущий слайд</span>
    </button>
    <button data-slide="1"><span class="show-for-sr">Второй слайд</span></button>
    <button data-slide="2"><span class="show-for-sr">Третий слайд</span></button>
    <button data-slide="3"><span class="show-for-sr">Четвертый слайд</span></button>
  </nav>
</div>
```

---

## Постраничная навигация (Pagination)


<div class="docs-codepen-container" data-ks-codepen>
  <a class="codepen-logo-link" href="https://codepen.io/IamManchanda/pen/BRxVmB?editors=1000" target="_blank"><img src="{{root}}assets/img/logos/edit-in-browser.svg" class="" height="" width="" alt="редактировать на codepen"></a>
</div>

```html_example
<ul class="pagination" role="navigation" aria-label="Pagination">
  <li class="disabled">Предыдущая <span class="show-for-sr">страница</span></li>
  <li class="current"><span class="show-for-sr">Вы на странице</span> 1</li>
  <li><a href="#0" aria-label="Page 2">2</a></li>
  <li><a href="#0" aria-label="Page 3">3</a></li>
  <li><a href="#0" aria-label="Page 4">4</a></li>
  <li class="ellipsis" aria-hidden="true"></li>
  <li><a href="#0" aria-label="Page 12">12</a></li>
  <li><a href="#0" aria-label="Page 13">13</a></li>
  <li><a href="#0" aria-label="Next page">Следующая <span class="show-for-sr">страница</span></a></li>
</ul>
```

---

## Прогресс-бар (Progress Bar)


<div class="docs-codepen-container" data-ks-codepen>
  <a class="codepen-logo-link" href="https://codepen.io/IamManchanda/pen/YVLvvB?editors=1000" target="_blank"><img src="{{root}}assets/img/logos/edit-in-browser.svg" class="" height="" width="" alt="редактировать на codepen"></a>
</div>

```html_example
<div class="primary progress" role="progressbar" tabindex="0" aria-valuenow="25" aria-valuemin="0" aria-valuetext="25 percent" aria-valuemax="100">
  <div class="progress-meter" style="width: 25%">
    <p class="progress-meter-text">25%</p>
  </div>
</div>

<div class="warning progress">
  <div class="progress-meter" style="width: 50%">
    <p class="progress-meter-text">50%</p>
  </div>
</div>

<div class="alert progress">
  <div class="progress-meter" style="width: 75%">
    <p class="progress-meter-text">75%</p>
  </div>
</div>

<div class="success progress" role="progressbar" tabindex="0" aria-valuenow="100" aria-valuemin="0" aria-valuetext="100 percent" aria-valuemax="100">
  <div class="progress-meter" style="width: 100%">
    <p class="progress-meter-text">100%</p>
  </div>
</div>
```

---

## Адаптивное меню (Responsive Menu)


<div class="docs-codepen-container" data-ks-codepen>
  <a class="codepen-logo-link" href="https://codepen.io/IamManchanda/pen/qmYKgJ?editors=1000" target="_blank"><img src="{{root}}assets/img/logos/edit-in-browser.svg" class="" height="" width="" alt="редактировать на codepen"></a>
</div>

```html_example
<ul class="vertical medium-horizontal menu">
  <li><a href="#0"><i class="fi-list"></i> <span>Один</span></a></li>
  <li><a href="#0"><i class="fi-list"></i> <span>Два</span></a></li>
  <li><a href="#0"><i class="fi-list"></i> <span>Три</span></a></li>
  <li><a href="#0"><i class="fi-list"></i> <span>Четыре</span></a></li>
</ul>
```

---

## Адаптивное переключение (Responsive Toggle)


<div class="docs-codepen-container" data-ks-codepen>
  <a class="codepen-logo-link" href="https://codepen.io/IamManchanda/pen/LymroM?editors=1000" target="_blank"><img src="{{root}}assets/img/logos/edit-in-browser.svg" class="" height="" width="" alt="редактировать на codepen"></a>
</div>

```html_example
<div class="title-bar" data-responsive-toggle="example-menu" data-hide-for="medium">
  <button class="menu-icon" type="button" data-toggle></button>
  <div class="title-bar-title">Меню</div>
</div>

<div class="top-bar" id="example-menu">
  <div class="top-bar-left">
    <ul class="dropdown menu" data-dropdown-menu>
      <li class="menu-text">Заголовок сайта</li>
      <li class="has-submenu">
        <a href="#0">Один</a>
        <ul class="submenu menu vertical" data-submenu>
          <li><a href="#0">Один</a></li>
          <li><a href="#0">Два</a></li>
          <li><a href="#0">Три</a></li>
        </ul>
      </li>
      <li><a href="#0">Два</a></li>
      <li><a href="#0">Три</a></li>
    </ul>
  </div>
  <div class="top-bar-right">
    <ul class="menu">
      <li><input type="search" placeholder="Поиск"></li>
      <li><button type="button" class="button">Поиск</button></li>
    </ul>
  </div>
</div>
```

---

## Переключатель отображения (Reveal)


<div class="docs-codepen-container" data-ks-codepen>
  <a class="codepen-logo-link" href="https://codepen.io/IamManchanda/pen/RVyBPw?editors=1000" target="_blank"><img src="{{root}}assets/img/logos/edit-in-browser.svg" class="" height="" width="" alt="редактировать на codepen"></a>
</div>

```html_example
<p><a data-open="exampleModal1">Кликни, чтобы показать модальное окно</a></p>

<div class="reveal" id="exampleModal1" data-reveal>
  <h1>Отлично!</h1>
  <p class="lead">Все получилось.</p>
  <p>Параграф текста модального окна.</p>
  <button class="close-button" data-close aria-label="Close reveal" type="button">
    <span aria-hidden="true">&times;</span>
  </button>
</div>
```

---

## Слайдер (Slider)


<div class="docs-codepen-container" data-ks-codepen>
  <a class="codepen-logo-link" href="https://codepen.io/IamManchanda/pen/xdjJVm?editors=1000" target="_blank"><img src="{{root}}assets/img/logos/edit-in-browser.svg" class="" height="" width="" alt="редактировать на codepen"></a>
</div>

```html_example
<div class="slider" data-slider data-initial-start="50" data-end="200">
  <span class="slider-handle"  data-slider-handle role="slider" tabindex="1"></span>
  <span class="slider-fill" data-slider-fill></span>
  <input type="hidden">
</div>

<div class="slider vertical" data-slider data-initial-start="25" data-end="200" data-vertical="true">
  <span class="slider-handle" data-slider-handle role="slider" tabindex="1"></span>
  <span class="slider-fill" data-slider-fill></span>
  <input type="hidden">
</div>

<div class="slider" data-slider data-initial-start="25" data-initial-end="75">
  <span class="slider-handle" data-slider-handle role="slider" tabindex="1"></span>
  <span class="slider-fill" data-slider-fill></span>
  <span class="slider-handle" data-slider-handle role="slider" tabindex="1"></span>
  <input type="hidden">
  <input type="hidden">
</div>
```

---

## Эффект приклеивания (Sticky)


<div class="docs-codepen-container" data-ks-codepen>
  <a class="codepen-logo-link" href="https://codepen.io/IamManchanda/pen/ZKodJR?editors=1000" target="_blank"><img src="{{root}}assets/img/logos/edit-in-browser.svg" class="" height="" width="" alt="редактировать на codepen"></a>
</div>

```html_example
<div class="row">
  <div class="columns small-6" id="example1" data-something>
    <p id="doodle">
      Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
    </p>
    <p>
      Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
    </p>
    <p>
      Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
    </p>
    <p>
      Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
    </p>
  </div>
  <div class="columns small-6 right" data-sticky-container>
    <div class="sticky" data-sticky data-margin-top="6" data-anchor="example1">
      <img class="thumbnail" src="assets/img/generic/rectangle-3.jpg">
    </div>
  </div>
</div>
```

---

## Переключатель (Switch)


<div class="docs-codepen-container" data-ks-codepen>
  <a class="codepen-logo-link" href="https://codepen.io/IamManchanda/pen/dWejpx?editors=1000" target="_blank"><img src="{{root}}assets/img/logos/edit-in-browser.svg" class="" height="" width="" alt="редактировать на codepen"></a>
</div>

```html_example
<div class="switch tiny">
  <input class="switch-input" id="tinySwitch" type="checkbox" name="exampleSwitch">
  <label class="switch-paddle" for="tinySwitch">
    <span class="show-for-sr">Выключатель 1</span>
  </label>
</div>

<div class="switch small">
  <input class="switch-input" id="smallSwitch" type="checkbox" name="exampleSwitch">
  <label class="switch-paddle" for="smallSwitch">
    <span class="show-for-sr">Выключатель 2</span>
  </label>
</div>

<div class="switch large">
  <input class="switch-input" id="largeSwitch" type="checkbox" name="exampleSwitch">
  <label class="switch-paddle" for="largeSwitch">
    <span class="show-for-sr">Выключатель 3</span>
  </label>
</div>
```

---

## Таблица (Table)


<div class="docs-codepen-container" data-ks-codepen>
  <a class="codepen-logo-link" href="https://codepen.io/IamManchanda/pen/eWrjQx?editors=1000" target="_blank"><img src="{{root}}assets/img/logos/edit-in-browser.svg" class="" height="" width="" alt="редактировать на codepen"></a>
</div>

```html_example
<table>
  <thead>
    <tr>
      <th width="200">Заголовок таблицы</th>
      <th>Заголовок таблицы</th>
      <th width="150">Заголовок таблицы</th>
      <th width="150">Заголовок таблицы</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Здесь контент</td>
      <td>Здесь более длинный контент Donec id elit non mi porta gravida at eget metus.</td>
      <td>Здесь контент</td>
      <td>Здесь контент</td>
    </tr>
    <tr>
      <td>Здесь контент</td>
      <td>Здесь более длинный контент Donec id elit non mi porta gravida at eget metus.</td>
      <td>Здесь контент</td>
      <td>Здесь контент</td>
    </tr>
    <tr>
      <td>Здесь контент</td>
      <td>Здесь более длинный контент Donec id elit non mi porta gravida at eget metus.</td>
      <td>Здесь контент</td>
      <td>Здесь контент</td>
    </tr>
  </tbody>
</table>
```

---

## Табы (Tabs)


<div class="docs-codepen-container" data-ks-codepen>
  <a class="codepen-logo-link" href="https://codepen.io/IamManchanda/pen/qmYygE?editors=1000" target="_blank"><img src="{{root}}assets/img/logos/edit-in-browser.svg" class="" height="" width="" alt="редактировать на codepen"></a>
</div>

```html_example
<ul class="tabs" data-tabs id="example-tabs">
  <li class="tabs-title is-active"><a href="#panel1" aria-selected="true">Таб 1</a></li>
  <li class="tabs-title"><a href="#panel2">Таб 2</a></li>
  <li class="tabs-title"><a href="#panel3">Таб 3</a></li>
  <li class="tabs-title"><a href="#panel4">Таб 4</a></li>
  <li class="tabs-title"><a href="#panel5">Таб 5</a></li>
  <li class="tabs-title"><a href="#panel6">Таб 6</a></li>
</ul>

<div class="tabs-content" data-tabs-content="example-tabs">
  <div class="tabs-panel is-active" id="panel1">
    <p>Один</p>
    <p>Проверьте меня! Я клевая Таб панель с текстовым контентом!</p>
  </div>
  <div class="tabs-panel" id="panel2">
    <p>Два</p>
    <img class="thumbnail" src="assets/img/generic/rectangle-7.jpg">
  </div>
  <div class="tabs-panel" id="panel3">
    <p>Три</p>
    <p>Проверьте меня! Я клевая Таб панель с текстовым контентом!</p>
  </div>
  <div class="tabs-panel" id="panel4">
    <p>Четыре</p>
    <img class="thumbnail" src="assets/img/generic/rectangle-2.jpg">
  </div>
  <div class="tabs-panel" id="panel5">
    <p>Пять</p>
    <p>Проверьте меня! Я клевая Таб панель с текстовым контентом!</p>
  </div>
  <div class="tabs-panel" id="panel6">
    <p>Шесть</p>
    <img class="thumbnail" src="assets/img/generic/rectangle-8.jpg">
  </div>
</div>
```

---

## Миниатюра (Thumbnail)


<div class="docs-codepen-container" data-ks-codepen>
  <a class="codepen-logo-link" href="https://codepen.io/IamManchanda/pen/EmLexY?editors=1000" target="_blank"><img src="{{root}}assets/img/logos/edit-in-browser.svg" class="" height="" width="" alt="редактировать на codepen"></a>
</div>

```html_example
<div class="grid-x grid-margin-x">
  <div class="cell small-4">
    <img class="thumbnail" src="assets/img/thumbnail/01.jpg" alt="Фотография Урана.">
  </div>
  <div class="cell small-4">
    <img class="thumbnail" src="assets/img/thumbnail/02.jpg" alt="Фотография Нептуна.">
  </div>
  <div class="cell small-4">
    <img class="thumbnail" src="assets/img/thumbnail/03.jpg" alt="Фотография Плутона.">
  </div>
</div>
```

---

## Тайтл-Бар (Title Bar)


<div class="docs-codepen-container" data-ks-codepen>
  <a class="codepen-logo-link" href="https://codepen.io/IamManchanda/pen/qmYMZZ?editors=1000" target="_blank"><img src="{{root}}assets/img/logos/edit-in-browser.svg" class="" height="" width="" alt="редактировать на codepen"></a>
</div>

```html_example
<div class="title-bar">
  <div class="title-bar-left">
    <button class="menu-icon" type="button"></button>
    <span class="title-bar-title">Foundation</span>
  </div>
  <div class="title-bar-right">
    <button class="menu-icon" type="button"></button>
  </div>
</div>
```

---

## Переключатель-туглер (Toggler)


<div class="docs-codepen-container" data-ks-codepen>
  <a class="codepen-logo-link" href="https://codepen.io/IamManchanda/pen/LymJLb?editors=1000" target="_blank"><img src="{{root}}assets/img/logos/edit-in-browser.svg" class="" height="" width="" alt="редактировать на codepen"></a>
</div>

```html_example
<p><a data-toggle="menuBar">Раздвинуть!</a></p>

<ul class="menu" id="menuBar" data-toggler=".expanded">
  <li><a href="#0"><i class="fi-list"></i> <span>Один</span></a></li>
  <li><a href="#0"><i class="fi-list"></i> <span>Два</span></a></li>
  <li><a href="#0"><i class="fi-list"></i> <span>Три</span></a></li>
  <li><a href="#0"><i class="fi-list"></i> <span>Четыре</span></a></li>
</ul>
```

---

## Подсказка (Tooltip)


<div class="docs-codepen-container" data-ks-codepen>
  <a class="codepen-logo-link" href="https://codepen.io/IamManchanda/pen/pPVOdm?editors=1000" target="_blank"><img src="{{root}}assets/img/logos/edit-in-browser.svg" class="" height="" width="" alt="редактировать на codepen"></a>
</div>

```html_example
<p><span data-tooltip aria-haspopup="true" class="has-tip" data-disable-hover="false" tabindex=1 title="Классное название для жука!">Скарабей</span> — один из самых почитаемых символов Древнего Египта. Считалось, что маленький жук повторяет путь Солнца: подобно тому, как Солнце совершает путешествие по небу, излучая свет и тепло, создавая условия для возрождения жизни во всём сущем, скарабей перекатывает свой шар с яйцами с востока на запад, пока зародыши не созреют и не родятся на свет.</p>
```

---

## Топ-Бар (Top Bar)


<div class="docs-codepen-container" data-ks-codepen>
  <a class="codepen-logo-link" href="https://codepen.io/IamManchanda/pen/eWrwKP?editors=1000" target="_blank"><img src="{{root}}assets/img/logos/edit-in-browser.svg" class="" height="" width="" alt="редактировать на codepen"></a>
</div>

```html_example
<div class="top-bar">
  <div class="top-bar-left">
    <ul class="dropdown menu" data-dropdown-menu>
      <li class="menu-text">Название сайта</li>
      <li class="has-submenu">
        <a href="#0">Один</a>
        <ul class="submenu menu vertical" data-submenu>
          <li><a href="#0">Один</a></li>
          <li><a href="#0">Два</a></li>
          <li><a href="#0">Три</a></li>
        </ul>
      </li>
      <li><a href="#0">Два</a></li>
      <li><a href="#0">Три</a></li>
    </ul>
  </div>
  <div class="top-bar-right">
    <ul class="menu">
      <li><input type="search" placeholder="Поиск"></li>
      <li><button type="button" class="button">Поиск</button></li>
    </ul>
  </div>
</div>
```

---

## Классы видимости (Visibility Classes)


<div class="docs-codepen-container" data-ks-codepen>
  <a class="codepen-logo-link" href="https://codepen.io/IamManchanda/pen/vmjqVG?editors=1000" target="_blank"><img src="{{root}}assets/img/logos/edit-in-browser.svg" class="" height="" width="" alt="редактировать на codepen"></a>
</div>

```html_example
<p>У вас экран размером от малого (small) и больше.</p>
<p class="show-for-medium">У вас экран размером от среднего (medium) и больше.</p>
<p class="show-for-large">У вас экран размером от большого (large) и больше.</p>
<p class="show-for-small-only">У вас <em>наверняка</em> малый (small) экран.</p>
<p class="show-for-medium-only">У вас <em>наверняка</em> средний (medium) экран.</p>
<p class="show-for-large-only">У вас <em>наверняка</em> большой (large) экран.</p>

<p class="hide-for-medium">У вас экран <em>не</em> среднего (medium) размера и больше.</p>
<p class="hide-for-large">У вас экран <em>не</em> большого (large) размера и больше.</p>
<p class="hide-for-small-only">У вас <em>наверняка не</em> малый (small) экран.</p>
<p class="hide-for-medium-only">У вас <em>наверняка не</em> средний (medium) экран.</p>
<p class="hide-for-large-only">У вас <em>наверняка не</em> большой (large) экран.</p>
<p class="hide">Не трогайте это.</p>

<p class="invisible">Я вижу это.</p>

<p class="show-for-landscape">У вас альбомная ориентация.</p>
<p class="show-for-portrait">У вас портретная ориентация.</p>

<p class="show-for-sr">Этот текст виден только скрин-ридерам.</p>
<p>Над этой строкой есть строка текста, просто вы ее не видите.</p>

<p aria-hidden="true">Этот текст видно, но не читается скрин-ридерами.</p>

<p><a class="show-on-focus" href="#mainContent">Перейти к содержанию (видно только при получении фокуса)</a></p>
<header id="header" role="banner">
</header>
<main id="mainContent" role="main" tabindex="0">
</main>
```
