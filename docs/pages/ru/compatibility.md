---
title: Совместимость
description: Foundation тестируется на многих браузерах и устройствах и имеет обратную совместимость вплоть до IE9 и Android 2.
tags:
  - поддержка
  - браузер
---

## Обзор

<table class="docs-compat-table">
  <tr>
    <td>Chrome</td>
    <td class="works" rowspan="7">Последние две версии</td>
  </tr>
  <tr><td>Firefox</td></tr>
  <tr><td>Safari</td></tr>
  <tr><td>Opera</td></tr>
  <tr><td>Mobile Safari<sup>1</sup></td></tr>
  <tr><td>IE Mobile</td></tr>
  <tr><td>Edge</td></tr>
  <tr>
    <td>Internet Explorer</td>
    <td class="works">Версии 9+</td>
  </tr>
  <tr>
    <td>Android Browser</td>
    <td class="works">Версии 4.4+</td>
  </tr>
</table>

<sup>1</sup>iOS 7+ активно поддерживается, но с некоторыми известными багами.

---

## Что не работает в более старых версиях?

- **Сетка:** Сетка Foundation использует `box-sizing: border-box` для реализации полей в колонках, но это свойство не поддерживается в IE8.
- **Десктопные стили:** Т.к. фреймворк написан по технологии mobile-first, браузеры, которые не поддерживают медиа запросы, будут всегда отображать мобильные стили.
- **JavaScript:** Плагины Foundation используют ряд удобных возможностей ECMAScript 5, которые не поддерживаются в IE8.
