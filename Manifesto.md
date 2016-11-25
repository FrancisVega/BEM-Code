# CSS

## Componible
Un componente siempre tiene que ser ["componible"](http://dle.rae.es/?id=A2BkG2M) y para ello debe estar libre de las propiedades: width, position, transform, float y margin.
Usaremos componentes de alto nivel (grids) para encajar el componente en un contexto específico.

## Dirección del margen
Los márgenes siempre deberán ir en una misma dirección:
- **margin-left** para "mover" horizontalmente un elemento
- **margin-bottom** para "mover" verticalmente un elemento

Beneficios:
- Es más fácil definir un ritmo vertical.
- Menos sorpresas a la hora de añadir o eliminar componentes de una página.
- Más libertar para cambiar de orden los componentes dentro de una misma página.
- Evitamos preocuparnos por el [Margin Collapse](https://developer.mozilla.org/es/docs/Web/CSS/CSS_Modelo_Caja/Mastering_margin_collapsing)
