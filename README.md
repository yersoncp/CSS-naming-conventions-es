# Convención de nombres CSS
Estructura modular CSS y convención de nombres que uso en mis proyectos. Las convenciones de nomenclaturas para las clases son la parte principal de lo que ofrece una metodología como [SMACSS](https://smacss.com/), [BEM](http://getbem.com/) u [OOCSS](http://oocss.org/).

## Componentes
Sintaxis: `<componente>[-elemento][--modificador]`

Esto tiene varios beneficios al escribir código:
* Ayuda a distinguir las clases de los componentes, los elementos descendientes y los modificadores.
* Evita el fuerte acoplado el HTML y especificación excesiva de selectores.

### Nombre de componente
El nombre del componente se escribe bajo de convención `PascalCase`.

```css
.MiComponente { /* … */ }
```

```html
<article class="MiComponente">
  …
</article>
```

### Elemento o componente descendiente
Un componente descendiente es una clase que está asociada a un componente. Deben escribirse en `camelCase`.

```html
<article class="Polygon">
   <header class="Polygon-header">
      <img class="Polygon-avatar" src="{{src}}" alt="{{alt}}">
      …
   </header>
   <div class="Polygon-bodyText">
      …
   </div>
</article>
```

### Modificador
Un modificador de componente es una clase que modifica la presentación del componente base de alguna forma (por ejemplo, para una determinada configuración del componente). Los nombres de los modificadores se escriben en `camelCase` y se deben separar del nombre del componente con dos guiones.

```css
.Card {
   /* … */
}
.Card--featured {
   /* … */
}
```

```html
<div class="Card Card-featured">…</div>
```

## Estado (is-state)
Refleja los cambios en el estado de un componente. Siempre deben usarse como una clase contigua acompañador de algún componente.

```css
.Polygon { /* … */ }
.Polygon.is-expanded { /* … */ }
```

```html
<article class="Polygon is-expanded">
  …
</article>
```

## JavaScript hooks
Evitar la vinculación de CSS y JavaScript en la misma clase. Llamados al DOM desde JavaScript pueden romper cualquier clase en CSS.

Recomiendo crear clases específicas para vincular con CSS usando el prefijo `js-`:

```html
<a class="link js-request-country">Request Country</a>
```

## Consideraciones adicionales
* Usar variables con guiones medios `$mi-variable` en lugar de `camelCase` o `snake_case`.
* Es posible usar guíon bajo como prefijo solo para variables dentro del mismo archivo: `$_mi-variable`.

## Recursos y fuentes
Esta guia es una recopilación de diversos fuentes y adaptaciones hechas por mi en base a mi experiencia en diversos proyectos frontend.

* [SUIT CSS naming conventions](https://github.com/suitcss/suit/blob/master/doc/naming-conventions.md)
* [BEM Methodoloy](http://getbem.com/naming/)
* [Modular CSS naming conventions](http://thesassway.com/advanced/modular-css-naming-conventions)
* [CSS Naming Conventions that Will Save You Hours of Debugging](https://medium.freecodecamp.org/css-naming-conventions-that-will-save-you-hours-of-debugging-35cea737d849)
* [Bulma CSS Framework](https://github.com/jgthms/bulma)
* [Airbnb CSS / Sass Styleguide](https://github.com/airbnb/css)

### Copyright and license

Drive with Love. Copyright 2018 Yerson Carhuallanqui. [MIT License](https://github.com/yersoncp/CSS-naming-conventions-es/blob/master/LICENSE)
