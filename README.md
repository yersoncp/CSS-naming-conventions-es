# Convención de nombres CSS
Estructura modular CSS y convención de nombres que uso en mis proyectos

## Componentes
En esta vida (al 2018) todo se basa en componentes:
Sintaxis: `<componente>[-elemento][--modificador]`

Esto tiene varios beneficios el escribir código:
* Ayuda a distinguir las clases de los componentes, los elementos descendientes y los modificadores.
* Evita el fuerte acoplado el HTML y especificación excesiva de selectores.

### Nombre de componente
El nombre del componente se escribe bajo de convención 'Pascal Case'.

```css
.MiComponente { /* … */ }
```

```html
<article class="MiComponente">
  …
</article>
```

### Elemento o componente descendiente
Un componente descendiente es una clase que está asociada a un componente. Deben escribirse en 'Camel Case'.

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
Un modificador de componente es una clase que modifica la presentación del componente base de alguna forma (por ejemplo, para una determinada configuración del componente). Los nombres de los modificadores se escriben en 'Camel Case' y se deben separar del nombre del componente con dos guiones.

```css
.Button {
   /* … */
}
.Button--primary {
   /* … */
}
```

```html
<button class="Button Button--primary" type="button">…</button>
```

## Recursos y fuentes
Ésta guia de una recopilación de diversos fuentes y adaptaciones hechas por mi en base a mi experiencia en diversos proyectos frontend.

* [SUIT CSS naming conventions](https://github.com/suitcss/suit/blob/master/doc/naming-conventions.md)
* [BEM Methodoloy](http://getbem.com/naming/)
* [Modular CSS naming conventions](http://thesassway.com/advanced/modular-css-naming-conventions)
* [CSS Naming Conventions that Will Save You Hours of Debugging](https://medium.freecodecamp.org/css-naming-conventions-that-will-save-you-hours-of-debugging-35cea737d849)
* [Bulma CSS Framework](https://github.com/jgthms/bulma)

### Copyright and license

Drive with Love. Copyright 2018 Yerson Carhuallanqui. [MIT License](https://github.com/yersoncp/CSS-naming-conventions-es/blob/master/LICENSE)
