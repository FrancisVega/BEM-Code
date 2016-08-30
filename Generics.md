# Generics

### Elementos anidados.

Debemos buscar la forma de nombrar las clases de tal forma que solo tengamos un nivel de elemento por bloque. Si nos cuesta mucho o ciertamente vemos que queda muy raro y forzado es posible que ese elemento que quieres añadir sea realmente otro bloque.

:see_no_evil:
```html
<!-- Recipe Block -->
<div class="recipe">

  <!-- Header -->
  <div class="recipe__header">
    <div class="recipe__header__title">...</div>
    <div class="recipe__header__subtitle">...</div>
  </div>

  <!-- Content -->
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
<!-- / Recipe Block -->
```

:smiley:
```html
<!-- Recipe Block -->
<div class="recipe">

  <!-- Header -->
  <div class="recipe__header">
    <div class="recipe__title">...</div>
    <div class="recipe__subtitle">...</div>
  </div>

  <!-- Content -->
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
<!-- / Recipe Block -->
```



#### Bloque y Elemento del mismo bloque no pueden estar juntos

:see_no_evil:
```html
<!-- Nav Block  -->
<ul class="nav nav__list">
  <li class="nav__item"></li>
</ul>
<!-- / Nav Block  -->
```

:smiley:
```html
<!-- Nav Block  -->
<div class="nav">
  <ul class="nav__list">
    <li class="nav__item"></li>
  </ul>
</div>
<!-- / Nav Block  -->
```

:smiley:
```html
<!-- Nav Block  -->
<ul class="nav">
  <li class="nav__item"></li>
</ul>
<!-- / Nav Block  -->
```


### Modificadores
