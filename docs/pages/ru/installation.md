---
title: Установка
description: В этом разделе приведены основные способы установки Foundation.
#video: '6KwsGcEHVTE'
---

## Установка с помощью менеджера пакетов

Foundation доступен в репозитариях ряда менеджеров пакетов. Пакет содержит исходный код Sass и JavaScript, а также скомпилированный CSS и JavaScript, как в минифицированном, так и полном виде.

<div class="grid-x grid-margin-x">
  <div class="cell small-2 text-right">
    <a href="https://www.npmjs.com/package/foundation-sites">
      <img class="docs-install-vendor-icon" src="{{root}}assets/img/icons/logo-npm.svg" alt="NPM">
    </a>
  </div>
  <div class="cell small-10">
    <div class="docs-code">
      <code class="bash">
        npm install foundation-sites
      </code>
    </div>
  </div>

  <div class="cell small-2 text-right">
    <a href="https://www.npmjs.com/package/foundation-sites">
      <img class="docs-install-vendor-icon" src="{{root}}assets/img/icons/logo-pnpm.svg" alt="PNPM">
    </a>
  </div>
  <div class="cell small-10">
    <div class="docs-code">
      <code class="bash">
        pnpm install foundation-sites
      </code>
    </div>
  </div>

  <div class="cell small-2 text-right">
    <a href="https://yarnpkg.com/en/package/foundation-sites">
      <img class="docs-install-vendor-icon" src="{{root}}assets/img/icons/logo-yarn.svg" alt="Yarn">
    </a>
  </div>
  <div class="cell small-10">
    <div class="docs-code">
      <code class="bash">
        yarn add foundation-sites
      </code>
    </div>
  </div>

  <div class="cell small-2 text-right">
    <a href="https://bower.io/search/?q=foundation-sites">
      <img class="docs-install-vendor-icon" src="{{root}}assets/img/icons/logo-bower.svg" alt="Bower">
    </a>
  </div>
  <div class="cell small-10">
    <div class="docs-code">
      <code class="bash">
        bower install foundation-sites
      </code>
    </div>
  </div>

  <div class="cell small-2 text-right">
    <a href="https://rubygems.org/gems/foundation-rails">
      <img class="docs-install-vendor-icon" src="{{root}}assets/img/icons/logo-rubygems.svg" alt="Ruby Gems">
    </a>
  </div>
  <div class="column small-10">
    <div class="docs-code">
      <code class="bash">
        gem install foundation-rails
      </code>
    </div>
  </div>

  <div class="cell small-2 text-right">
    <a href="https://atmospherejs.com/zurb/foundation-sites">
      <img class="docs-install-vendor-icon" src="{{root}}assets/img/icons/logo-meteor.svg" alt="Meteor">
    </a>
  </div>
  <div class="cell small-10">
    <div class="docs-code">
      <code class="bash">
        meteor add zurb:foundation-sites
      </code>
    </div>
  </div>

  <div class="cell small-2 text-right">
    <a href="https://packagist.org/packages/zurb/foundation">
      <img class="docs-install-vendor-icon" src="{{root}}assets/img/icons/logo-composer.svg" alt="Composer">
    </a>
  </div>
  <div class="cell small-10">
    <div class="docs-code">
      <code class="bash">
        php composer.phar require zurb/foundation
      </code>
    </div>
  </div>

  <div class="cell small-2 text-right">
    <a href="https://www.nuget.org/packages/foundation-sites/">
      <img class="docs-install-vendor-icon" src="{{root}}assets/img/icons/logo-nuget.svg" alt="NuGet">
    </a>
  </div>
  <div class="cell small-10">
    <div class="docs-code">
      <code class="bash">
        Install-Package foundation-sites
      </code>
    </div>
  </div>
</div>

Содержимое пакета:

```
├─ scss       Исходные файлы Sass. Используйте эту директорию в качестве пути загрузки Sass.
├─ js         Исхожные файлы JavaScript. Если вы используете сборщик, обязательно загрузите файл `foundation.core.js` первым.
└─ dist       Скомпилированные файлы:
   ├─ css        * Скомпилированные файлы CSS. Включает минифицированные и неминифицированные версии.
   ├─ js         * Собранные файлы JavaScript. Включает минифицированные и неминифицированные версии.
   └─ plugins    * Автономные плагины JavaScript.
```

---

## Установка из командной строки с помощью Foundation CLI

С помощью NodeJS-утилиты Foundation CLI вы можете создать проект на основе одного из шаблонов.

Установка Foundation CLI:

```bash
npm install --global foundation-cli
# или sudo npm install --global foundation-cli
```

<div class="callout info">
  В зависимости от настроек вашей машины, команда может потерпеть неудачу с ошибкой `EACCESS`. Чтобы обойти эту проблему, сначала выполните команду с `sudo`.
</div>

Следующая команда создаст новый проект Foundation:

```bash
foundation new
```

После того как вы выберете "Foundation for Sites", Foundation CLI предложит на выбор шаблон проекта. Вы сможете выбрать между:

<div class="grid-x grid-margin-x">
  <div class="cell small-6">
    <h3>Basic</h3>
    <p>
      <b>Рекомендовано для новичков</b><br>
      Базовый шаблон для начала использования Foundation. Он включает:
      <ul>
        <li>
          Преднастроенный Foundation for Sites.
        </li>
        <li>
          Компилятор Sass<br>
          Инструмент для конвертации ваших SASS/SCSS файлов в CSS.
        </li>
        <li>
          Начальный файл HTML<br>
          Базовый файл, который поможет вам использовать базовые компоненты Foundation (включая новую сетку XY !)
        </li>
      </ul>
    </p>
  </div>

  <div class="cell small-6">
    <h3>ZURB</h3>
    <p>
      <b>Рекомендуется для опытных пользователей</b><br>
      Более продвинутый шаблон, включающий Foundation и сборщик:
      <ul>
        <li>Handlebars HTML-шаблоны с Panini</li>
        <li>Sass компилятор и автопрефиксер</li>
        <li>JavaScript сборщик webpack</li>
        <li>Встроенный BrowserSync</li>
        <li>Продакшн сборщик с CSS, Javascript и компрессией изображений</li>
      </ul>
    </p>
  </div>
</div>

<p class="text-center">
  <a href="starter-projects.html" class="button">Больше об установке Шаблонов</a>
</p>

<div class="callout info">
  <p><strong>Пользователи Foundation 5</strong>: Если на вашей машине уже установлен Foundation 5 CLI, вы сможете получить доступ только к некоторым командам, в зависимости от настроек окружения вашей командной строки.</p>

  <p>Для удаления Foundation 5 CLI, запустите <code>gem uninstall foundation</code>. После тестирования Foundation 6 CLI, если вы пожелаете удалить его для того, чтобы вернуться к старому CLI, запустите <code>npm uninstall foundation-cli --global</code>.</p>
</div>

<div class="callout info">
  <p><strong>Пользователи Windows</strong>: имейте ввиду, что в вашем node окружении должен быть доступен python v2.7, т.к. он требуется для node-gyp. Есть 2 способа обеспечить это</p>

  <ol>
    <li>Установить <a href="https://github.com/felixrieseberg/windows-build-tools">windows-build-tools</a> (рекомендуется) и после сделать Python доступным командой <code>npm config set python "%USERPROFILE%\.windows-build-tools\python27\python.exe"</code></li>
    <li>Установить <a href="https://www.python.org/downloads/">python</a> (не рекомендуется) и добавить его в переменные окружения вашей системы</li>
  </ol>
 
  <p>Первый способ рекомендуется в случае, если у вас не установлен python v2.7, т.к. такая установка не повлияет на вашу машину за пределами окружения node. В случае если у вас уже установлен python v2.7 вы можете сразу же начать использовать foundationc-cli.</p>
</div>

---

## Скачивание

<div class="grid-x grid-margin-x">
  <div class="cell">
    <p>
      Если вы не используете Sass, для вас есть стартовый шаблон с скомпилированным CSS и JavaScript и стартовым файлом `index.html` с примерами компонентов. Просто разархивируйте и начинайте работать!
    </p>
    <p class="text-center">
      <a href="http://foundation.zurb.com/sites/download" class="button">Скачать Foundation</a>
    </p>
  </div>
</div>

---

## Ссылки CDN

Ребята из [jsDelivr](https://www.jsdelivr.com) предоставили нам место для сжатого Foundation CSS и JavaScript. Просто скопируйте следующие тэги в ваш HTML:

```html
<!-- Сжатый CSS -->
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/foundation-sites@6.4.3/dist/css/foundation.min.css" integrity="sha256-GSio8qamaXapM8Fq9JYdGNTvk/dgs+cMLgPeevOYEx0= sha384-wAweiGTn38CY2DSwAaEffed6iMeflc0FMiuptanbN4J+ib+342gKGpvYRWubPd/+ sha512-QHEb6jOC8SaGTmYmGU19u2FhIfeG+t/hSacIWPpDzOp5yygnthL3JwnilM7LM1dOAbJv62R+/FICfsrKUqv4Gg==" crossorigin="anonymous">

<!-- Сжатый JavaScript -->
<script src="https://cdn.jsdelivr.net/npm/foundation-sites@6.4.3/dist/js/foundation.min.js" integrity="sha256-mRYlCu5EG+ouD07WxLF8v4ZAZYCA6WrmdIXyn1Bv9Vk= sha384-KzKofw4qqetd3kvuQ5AdapWPqV1ZI+CnfyfEwZQgPk8poOLWaabfgJOfmW7uI+AV sha512-0gHfaMkY+Do568TgjJC2iMAV0dQlY4NqbeZ4pr9lVUTXQzKu8qceyd6wg/3Uql9qA2+3X5NHv3IMb05wb387rA==" crossorigin="anonymous"></script>
```

Начиная с Foundation 6.4, flex используется по умолчанию и как следствие **доступна только новая XY Сетка**. Для обратной совместимости и использования в наиболее распространенных кейсах имеются другие прекомпилированные версии CSS. Для остальных случаев и расширенной кастомизации, мы рекомендуем собирать Foundation с собственными настройками (смотрите другие методы установки).

```html
<!-- foundation-float.min.css: Сжатый CSS с поддержкой плавающей сетки -->
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/foundation-sites@6.4.3/dist/css/foundation-float.min.css" integrity="sha256-TPcVVrzfTETpAWQ8HhBHIMT7+DbszMr5n3eFi+UwIl8= sha384-+aXh7XSzITwlvjelsNWuL1A9rT8pWGaiqMMeUjtKcsWIfzT1oV8Mp3oYxmjPK8Gv sha512-cArttU/Yh+PzfQ/dhCdfBiU9+su+fuCwFxLrlLbvuJE/ynUbstaKweVPs7Hdbok9jlv9cwt+xdk20wRz7oYErQ==" crossorigin="anonymous">

<!-- foundation-prototype.min.css: Сжатый CSS с классами прототипирования -->
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/foundation-sites@6.4.3/dist/css/foundation-prototype.min.css" integrity="sha256-JyhZsgvsqjrdl9GPOILi/zyc+z4dcwXiyP1Q7cwWlM0= sha384-GtUT6gOaCY/S1ggTUOnqe5CQAEAZ6oVTmMq3X4vfZrvp+tLgjBEmwVxJnukor+o0 sha512-x3+KBxBjFh8PGncrfDOsJhntYDBFdJxmpb211THYkQOaGWvk7ckZG6prGUpZqz85AXgiispjow06+bDnIxnWDQ==" crossorigin="anonymous">

<!-- foundation-rtl.min.css: Сжатый CSS с поддержкой rtl -->
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/foundation-sites@6.4.3/dist/css/foundation-rtl.min.css" integrity="sha256-Az+E7JXW71Srarkum5QPTdnobddg2GqI1i8+nMusgLk= sha384-eBKuNtkGVmsJD0uNnWoKYYVnzDT0PXV+XNyAgmmZwYVn7MSNcaR4i5HjOpSRd0o6 sha512-d0RjiDZM/0NlD+7Y2DhUGuAUdwDIL5lS3GPAD0HEayEcrhuLuRiPYOgFWZik+gsFzsykxSn0KO6jim7ev8kIig==" crossorigin="anonymous">
```

<div class="text-center">
  <a href="https://www.jsdelivr.com/package/npm/foundation-sites?path=dist" class="button" target="_blank">Смотреть все версии и файлы CDN</a>
</div>

---

## Стартовый шаблон HTML
Начните с использования этого шаблона HTML и адаптируйте его под свои нужды. Обратите внимание, что использование класса `.no-js` в тэге `html` обязательно. Добавление данного класса предотвращает возникновение эффекта [неоформленного контента (FOUC)](https://en.wikipedia.org/wiki/Flash_of_unstyled_content) для ряда компонентов foundation.

```html
<!doctype html>
<html class="no-js" lang="en">
  <head>
    <meta charset="utf-8" />
    <meta http-equiv="x-ua-compatible" content="ie=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Foundation Starter Template</title>
    <link rel="stylesheet" href="css/foundation.css" />
  </head>
  <body>
    <h1>Hello, world!</h1>

    <script src="js/vendor/jquery.js"></script>
    <script src="js/vendor/what-input.js"></script>
    <script src="js/vendor/foundation.min.js"></script>
    <script>
      $(document).foundation();
    </script>

  </body>
</html>

```

---

## Прочие интеграции

Сообщество Foundation помогло нам интегрировать фреймврок в Rails, WordPress, Django, и многие другие. Для поиска возможных вариантов использования Foundation, обратитесь к нашей [странице ресурсов](http://foundation.zurb.com/sites/resources).
