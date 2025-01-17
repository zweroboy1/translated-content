---
title: Date.now()
slug: Web/JavaScript/Reference/Global_Objects/Date/now
tags:
  - Date
  - JavaScript
  - Method
  - Reference
  - polyfill
translation_of: Web/JavaScript/Reference/Global_Objects/Date/now
---
{{JSRef("Global_Objects", "Date")}}

## Сводка

Метод **`Date.now()`** возвращает количество миллисекунд, прошедших с 1 января 1970 года 00:00:00 по UTC.

## Синтаксис

```
var timeInMs = Date.now();
```

### Параметры

Нет.

## Описание

Метод `now()` возвращает количество миллисекунд, прошедших с 1 января 1970 года 00:00:00 по UTC по текущий момент времени в качестве {{jsxref("Global_Objects/Number", "числа", "", 1)}}.

Поскольку метод `now()` является статическим методом объекта {{jsxref("Global_Objects/Date", "Date")}}, вы всегда должны использовать его как `Date.now()`.

## Полифил

Этот метод был стандартизирован в ECMA-262 5-го издания. Отсутствие этого метода в движках, которые не были обновлены для его поддержки, можно обойти следующей прокладкой:

```js
if (!Date.now) {
  Date.now = function now() {
    return new Date().getTime();
  };
}
```

## Спецификации

{{Specifications}}

## Совместимость с браузерами

{{Compat}}

## Смотрите также

- {{domxref("Performance.now()")}} — предоставляет временные метки с разрешением в доли миллисекунд для использования при измерении производительности веб-страницы
- {{domxref("console.time()")}} / {{domxref("console.timeEnd()")}}
