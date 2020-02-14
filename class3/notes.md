# CSS
- Hojas de Estilo en Cascada (del inglés Cascading Style Sheets)
- Da estilo a la página, describe la presentación del documento

## Sintaxis
Una declaración esta compuesta por:
- Propiedad
- Valor
Ejemplo:
```
background-color: red;
```
Las declaraciones se agrupan en un bloque con llaves
{
  background-color: red;
  border: 1px solid black;
}
A esto se le agregan los selectores

## Selectores
Elemento HTML al que se le aplicará el estilo

Nombre del selector           | Descripción | Ejemplo
------------------------------|-------------|--------
Selector de tipo              | Todas las etiquetas de ese tipo | p { }
Selector universal            | Aplica a todas las etiquetas | * { }
Selector de clase             | Las que tengan esa clase | .box { }
Selector de id                | Las que tengan ese id | #unique {}
Selector de atributo          | Las que tengan el atributo en corchetes | a[title] {  }
Selector de pseudo-clase      | Aplica elemento que se encuentre en el estado de la pseudo clase | p:first-child { }
Selector de pseudo-elemento   | Aplica al pseudo elemento de ese elemento | p::first-line { }
Selector descendiente         | Al elemento que cumpla ser descediente | article p
Selector hijo                 | Al elemento que cumpla ser hijo directo | article > p
Selector de hermano adyacente | Al elemento que es hermano adyacente | h1 + p
Selector general de hermano   | Al elemento que es hermano no necesariamente adyacente | h1 ~ p

## CSS3
Es la última evolución de css y traen muchas novedades como:
- Esquinas redondeadas
- Sombras
- Gradientes
- Transiciones o Animaciones
- Nuevos layouts (grid layout, flexbox)

## Metodologías
Ayudan a escribir código css más flexible, reutilizable, comprensible y manejable.

### OOCSS => Object-Oriented CSS 
- Separar la estructura del diseño (skin, piel).
Sin OOCSS
```
#button {
  width: 200px;
  height: 50px;
  padding: 10px;
  border: solid 1px #ccc;
  background: linear-gradient(#ccc, #aaa);
  box-shadow: rgba(0, 0, 0, .5) 2px 2px 5px;
}
#widget {
  width: 500px;
  min-height: 200px;
  overflow: auto;
  border: solid 1px #ccc;
  background: linear-gradient(#ccc, #222);
  box-shadow: rgba(0, 0, 0, .5) 2px 2px 5px;
}
```
Con OCCSS
```
.button {
  width: 200px;
  height: 50px;
  padding: 10px;
}
.widget {
  width: 500px;
  min-height: 200px;
  overflow: auto;
}
.skin {
  border: solid 1px #ccc;
  background: linear-gradient(#ccc, #aaa);
  box-shadow: rgba(0, 0, 0, .5) 2px 2px 5px;
}
```
- Separar contenedor del contenido.
Sin OOCSS
```
header h1 {
  font-family: 'Roboto', Helvetica, sans-serif;
  font-size: 2em;
  color: #F44;
}
/*mas código css...*/
footer h1 {
  font-family: 'Roboto', Helvetica, sans-serif;
  font-size: 1.5em;
  color: #F44;
  opacity: 0.5;
  filter: alpha(opacity = 50);
}
```
Con OOCSS
```
h1{
  font-family: 'Roboto', Helvetica, sans-serif;
  color: #F44;
}
/* ... */
h1, .h1-size { font-size: 2em;   }
h2, .h2-size { font-size: 1.8em; } 
h3, .h3-size { font-size: 1.5em; }
/* ... */
.transparente {
  opacity: 0.5;
  filter: alpha(opacity = 50);
}
```
### BEM => Block, Element, Modifier
- Bloques
Entidad independiente que tiene significado por sí misma. (header, container, menu, checkbox, input…)

- Elementos
Partes de un bloque que no tienen un significado independiente. Están semánticamente vinculados a su bloque. (elemento de un menú, elemento de una lista, titulo de un header, caption de un elemento picture, etc…)

- Modificadores
Indicadores de bloque o elemento. Utilizados para cambiar la apariencia o comportamiento. (disabled, highlighted, checked, fixed, size big, color yellow…)

Ejemplo
.bloque
.bloque--modificador
.bloque__elemento
.bloque__elemento--modificador

### SMACSS => Scalable and Modular Architecture for CSS
SMACSS funciona mediante organización de las reglas CSS en 5 categorías. (Base, Maquetación, Módulo, Estado y tema)

## Media Queries
Se utilizan para aplicar estilos segun el dispositivo, el tamaño de la resolución de pantalla o tamaño del viewport

Ejemplo
```
@media (max-width: 600px) {
  .facet_sidebar {
    display: none;
  }
}
```

## Modelo de caja
- Cajas en bloque
  - Su ancho ocupará el 100% de su contenedor
  - Fuerza el salto de línea
  - Se respeta el width y height
- Cajas en línea
  - No fuerza el salto de línea
  - No aplic width y height

### Contenido de una caja
 - Margin:
    - margin: 5px;
    - margin-left: 5px;
    - margin: 10px 5px;
    - margin: 5px 10px 4px 2px;
 - Border
    - border: 1px solid green;
    - border-width: 1px;
    - border-style: solid;
    - botder-color: green;
 - Padding
    - padding: 5px;
    - padding-left: 5px;
    - padding: 10px 5px;
    - padding: 5px 10px 4px 2px;
 - Content
## Pseudo clases
Se añade al selector para especificar un estado determinado de un elemento
```css
div:hover {
  background-color: #F89B4D;
}
```

Otras pseudo clases:
- active
- checked
- disabled
- first
- focus

Ver más en: https://developer.mozilla.org/es/docs/Web/CSS/Pseudo-classes
## Pseudo Elementos
Se añade al selector para añadir estilo a una parte concreta del documento
```css
p::after { margin-top: 5px; }
```

Otros pseudo elementos:
- ::before
- ::first-line
- ::selection

Ver más en: https://developer.mozilla.org/es/docs/Web/CSS/Pseudoelementos

## Sistema de grillas
Ejemplo de bootstrap
Nota: Falta Completar

## Flexbox
Ejemplo de bootstrap
Nota: Falta Completar

## Frameworks
- Bootstrap
- Semantic UI
- Skeleton
- Bulma

## Pre procesadores
- sass
- less
- stylus

### SASS
 
 - Variables

 ```scss
  $font-stack:    Helvetica, sans-serif;
  $primary-color: #333;

  body {
    font: 100% $font-stack;
    color: $primary-color;
  }
```

- Anidación

```scss
nav {
  ul {
    margin: 0;
    padding: 0;
    list-style: none;
  }

  li { display: inline-block; }

  a {
    display: block;
    padding: 6px 12px;
    text-decoration: none;
  }
}
```

- Mixins
```scss
@mixin transform($property) {
  -webkit-transform: $property;
  -ms-transform: $property;
  transform: $property;
}
.box { @include transform(rotate(30deg)); }
```
## Ejemplo
Ver style.css

## Links
Css básico => https://developer.mozilla.org/es/docs/Learn/Getting_started_with_the_web/CSS_basics
Metodologías css => https://www.espai.es/blog/2016/07/metodologias-css-oocss-bem-smacss/