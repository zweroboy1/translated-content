---
title: animation-play-state
slug: Web/CSS/animation-play-state
translation_of: Web/CSS/animation-play-state
---
{{CSSRef}}{{SeeCompatTable}}

##

## Resumen

La propiedad [CSS](/es/docs/CSS "CSS") **`animation-play-state`** determina si una animación está en ejecución o en pausa. Puede ser consultada para determinar si la animación se está ejecutando. Además, su valor se puede establecer para pausar y reanudar una animación.

Reanudando una animación pausada, ésta empezará en el punto en el que fue pausada, en vez de empezar desde el principio.

{{cssinfo}}

## Sintaxis

```css
/* Single animation */
animation-play-state: running;
animation-play-state: paused;

/* Multiple animations */
animation-play-state: paused, running, running;

/* Global values */
animation-play-state: inherited;
animation-play-state: initial;
animation-play-state: unset;
```

### Valores

- `running`
  - : La animación se está ejecutando.
- `paused`
  - : La animación está pausada.

### Syntax formal

    {{csssyntax}}

## Ejemplos

Visita [animaciones CSS](https://developer.mozilla.org/es/CSS/Usando_animaciones_CSS "en/CSS/CSS_animations") para ver algunos ejemplos.

## Especificaciones

| Especificación                                                                                               | Estado                               | Comentario        |
| ------------------------------------------------------------------------------------------------------------ | ------------------------------------ | ----------------- |
| {{SpecName('CSS3 Animations', '#animation-play-state', 'animation-play-state')}} | {{Spec2('CSS3 Animations')}} | Definición incial |

## Compatibilidad entre navegadores

{{Compat("css.properties.animation-play-state")}}

##

## Consulte también

- [Usando animaciones CSS](/es/docs/Web/CSS/CSS_Animations/Using_CSS_animations "CSS developer guide about CSS animations")
- {{domxref("AnimationEvent", "AnimationEvent")}}