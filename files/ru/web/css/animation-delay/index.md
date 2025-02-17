---
title: animation-delay
slug: Web/CSS/animation-delay
tags:
  - CSS
  - CSS-анимации
  - CSS-свойства
translation_of: Web/CSS/animation-delay
---
{{CSSRef}}{{SeeCompatTable}}

## Описание

[CSS](/ru/docs/CSS "CSS") свойство **`animation-delay`** определяет время задержки перед стартом анимации.

{{EmbedInteractiveExample("pages/css/animation-delay.html")}}

Значение 0s, которое является значением по умолчанию, указывает на то, что анимация должна начаться непременно. В противном случае, старт анимации будет отложен на указанное время.

При указании отрицательного значения, анимация также начнётся непременно, но её воспроизведение начнётся не с первого ключевого кадра, а так, будто часть анимации уже была показана. Например, если вы укажете значение -1s, анимация будет начата с ключевого кадра, когда 1 секунда анимации уже была воспроизведена.

{{cssinfo}}

## Синтаксис

```css
animation-delay: 3s;
animation-delay: 2s, 4ms;
```

### Значения

- `<time>`
  - : Время задержки перед стартом анимации. Может быть определено в секундах (s), либо в миллисекундах (ms). Если вы не укажите единицу измерения, свойство будет недействительным.

### Формальный синтаксис

{{csssyntax}}

## Примеры

Посмотрите [CSS-анимации](/ru/docs/CSS/CSS_animations "CSS/CSS_animations") для примера.

## Спецификации

{{Specifications}}

## Совместимость с браузерами

{{Compat}}

## Смотрите также

- [Использование CSS-анимаций](/ru/docs/CSS/Tutorials/Using_CSS_animations "Tutorial about CSS animations")
- {{domxref("AnimationEvent", "AnimationEvent")}}
