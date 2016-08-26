# BEM-Code
Ejemplos de buenas vs malas prácticas en BEM

#### No más de un elementos por bloque

:see_no_evil:
```html
<div class="recipe">
  <div class="recipe__header">
    <div class="recipe__header__title">Tortilla de patatas.</div>
    <div class="recipe__header__subtitle">Rápida, fácil y sin utilizar huevo.</div>
  </div>
  <div class="recipe__content">
    <div class="recipe__content__section">
      <div class="recipe__content__section__heading">
        <ul class="recipe__content__section__heading__list">
          <li class="repice__content__section__heading__list__item">...</li>
        </ul>
      </div>
    </div>
  </div>
</div>
```
:smiley:
```html
<div class="recipe">
  <div class="recipe__header">
    <div class="recipe__title">Tortilla de patatas.</div>
    <div class="recipe__subtitle">Rápida, fácil y sin utilizar huevo.</div>
  </div>
  <div class="recipe__content">
    <div class="recipe__section">
      <div class="recipe__heading">
        <ul class="recipe__list">
          <li class="repice__item">...</li>
        </ul>
      </div>
    </div>
  </div>
</div>
```



#### Bloque y Elemento del mismo bloque no pueden estar juntos

:see_no_evil:
```html
<ul class="nav nav__list">
  <li class="nav__item"></li>
</ul>
```

:smiley:
```html
<div class="nav">
  <ul class="nav__list">
    <li class="nav__item"></li>
  </ul>
</div>
```

o

:smiley:
```html
<ul class="nav">
  <li class="nav__item"></li>
</ul>
```
