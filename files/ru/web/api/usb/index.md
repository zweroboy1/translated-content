---
title: USB
slug: Web/API/USB
tags:
  - API
  - Interface
  - Reference
  - USB
  - WebUSB
  - WebUSB API
translation_of: Web/API/USB
---
{{APIRef("WebUSB API")}}{{SeeCompatTable}}{{securecontext_header}}

Интерфейс **`USB`** [WebUSB API](/ru/docs/Web/API/WebUSB_API) представляет атрибуты и методы для поиска и подключения USB устройств из WEB страницы.

## Свойства

Нет.

### Обработчики событий

- {{domxref("USB.onconnect")}}
  - : Обработчик событий вызывается всегда, когда ранее сопряжённое устройство подключается.
- {{domxref("USB.ondisconnect")}}
  - : Обработчик событий вызывается всегда, когда ранее сопряжённое устройство отключается.

## Методы

- {{domxref("USB.getDevices()")}}
  - : Возвращает {{jsxref("Promise")}}, который разрешается массивов объектов {{domxref("USBDevice")}} сопряжённых устройств.
- {{domxref("USB.requestDevice()")}}
  - : Возвращает {{jsxref("Promise")}}, который разрешается экземпляром {{domxref("USBDevice")}}, если указанное устройство найдено. Вызов этой функции запускает поток сопряжения агента пользователя.

## Спецификация

{{Specifications}}

## Совместимость с браузерами

{{Compat}}
