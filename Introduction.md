# Introducción

## Bloques

### Nombres
El nombre del 'block' describe su propósito y no su apariencia.
Por ejemplo.

```html
<!-- correcto -->
<div class="error"></div>

<!-- incorrecto -->
<div class="red-text"><div>
```

### Geometría
El bloque no debe afectar a su entorno (externo), esto quiere decir que no debe llevar márgenes, ancho fijo o posicione absoluta.

### Clases
El bloque está definido por una clase, no se puede definir un bloque con un ID o haciéndo referencia a la etiqueta html directamente.

### Anindado o sub-bloques
Los bloques se pueden anidar sin límite.
```html
<!-- `header` block -->
<header class="header">
    <!-- Nested `logo` block -->
    <div class="logo"></div>

    <!-- Nested `search-form` block -->
    <form class="search-form"></form>
</header>
```

## Elementos

### Nombres
El nombre del bloque describe su propósito y no su apariencia.

### Anidado
Los elementos pueden estar unos dentro de otros sin límite, recordando que un elemento siempre es parte de un bloque y no de otro elemento.

```html
<!-- correcto, elementos dentro de elementos pero sin afectar al nombrado -->
<form class="search-form">
    <div class="search-form__content">
        <input class="search-form__input">
        <button class="search-form__button">Search</button>
    </div>
</form>

<!-- incorrecto -->
<form class="search-form">
    <div class="search-form__content">
        <!-- Recomendado: `search-form__input` o `search-form__content-input` -->
        <input class="search-form__content__input">
        <!-- Recomendado: `search-form__button` o `search-form__content-button` -->
        <button class="search-form__content__button">Search</button>
    </div>
</form>
```

## Modificadores

### Nombres
El nombre del modificador describe su apariencia o estado siempre intentando describir el propósito. Mejor button--error que button--red

Los modificadores no pueden usarse de forma aislada siempre tiene que ir junto al bloque o al elemento que modifican. Los modificadores deben MODIFICAR la apariencia, el comportamiento o el estado de la entidad (bloque o elemento) y no reemplazarla.

```html
<!-- correcto -->
<div class="button button--main"></div>

<!-- incorrecto -->
<div class="button--main"></div>
```

Existen dos tipos de mofificadores, booleano y key/value.

Booleano:

```css
.button--disabled {}
.button--focused {}
.button--main {}
.button--secondary {}
```

Key/value:

```css
.button--themeIsland {}
.button--themeMonocrhome {}
.button--sizeBig {}
.button--sizeSmall {}
```

## Mix

Los mix son una técnica que permite utilizar distintas entidades de BEM (bloques o elementos) en una misma etiqueta HTML.

En este caso estamos mezclando el estilo y comportamiento de logo con header__logo así podemos mantener la hoja de estilos de header mucho más clara.
```html
<div class="header">
    <div class="header__logo logo">...</div>
</div>
```

```css
/* con eso para "acceder" a logo desde header tendríamos */
.header__logo {}
/* en lugar de */
.header .logo {}
```
