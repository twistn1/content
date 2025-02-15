---
title: "ARIA-роль `alert`"
description: "Роль для важной информации, о которой скринридер расскажет пользователю сразу же."
authors:
  - doka-dog
keywords:
  - доступность
  - ARIA
  - ARIA-атрибут
  - live region
  - живая область
  - интерактивная область
related:
  - a11y/aria-intro
  - a11y/aria-roles
  - a11y/aria-live
tags:
  - doka
  - placeholder
---

## Кратко

[Роль изменяющихся областей](/a11y/aria-roles/#roli-izmenyayushchihsya-oblastey). Делает часть страницы live region или «живой» областью. `alert` нужна для важной в определённый момент времени информации.

## Пример

```html
<div role="alert">
  Сервер сейчас недоступен. Повторите попытку позже.
</div>
```

## Как пишется

Добавьте к тегу атрибут `role="alert"`. Роль можно использовать для всех тегов.

У `alert` по умолчанию есть свойства [`aria-live="assertive"`](/a11y/aria-live/) и [`aria-atomic="true"`](/a11y/aria-atomic/).

[Скринридер](/a11y/screenreaders/) объявит сообщение с ролью `alert` сразу же, как только оно появится.

Элементы с ролью `alert` не должны быть в порядке фокуса, а ещё не надо добавлять для них кнопку закрытия.

Важно, чтобы сообщение содержало только текст и появлялось на странице не сразу при загрузке, а динамически.

## Как понять

«Живая» область — это область страницы, в которой что-то постоянно обновляется из-за внешних событий. Например, появляется уведомление или ошибка, когда пользователь сделал что-то неправильно. Так пользователи скринридеров могут узнать об изменениях автоматически, без перехода к этой части страницы.

Роль `alert` пригодится для важного сообщения об ошибке или предупреждения. К примеру, когда пользователь ввёл неверные данные в поле, заканчивается время сессии или возникла северная ошибка и не сохранились данные, пропало интернет-соединение и подобное.
