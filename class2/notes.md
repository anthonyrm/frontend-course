# HTML
- Lenguaje de Marcado para Hipertextos (HyperText Markup Language)
- Es un lenguaje de marcado, usa etiquetas para estructurar el contenido de una web (no su apariencia ni su funcionalidad)

## HTML 5
Es la ultima version de HTML que ofrece nuevos elementos
Es más semántico es decir sus etiquetas cuentan co  mejor significado que describen su contenido
Buen soporte para multimedia para el uso de audio y video

## Estructura
Ver structure.html
Datos importantes:
- lo que esta dentro del head se conoce como metadatos del documento
- lo que esta dentro del body es lo qu se ve en la pantalla

## Etiquetas importantes
html
head
title
link
script
body
header
footer
nav
section
article
h1
p
hr
br
ul
li
strong
img
iframe
video
table
form
input
button
select
textarea

## Formularios
Ver form.html
Datos importantes:
- action => a donde envia los datos
- method => que metodo usara al enviar
- submit => el boton que al presionarlo enviará los datos
- name => si el input no tiene name no se enviará ese valor
- Ahora no se suele usar action ni method en un formulario, solo el click del boton ejecuta una funcion que prepara los datos y los envia por otros mecanismos

## Template engines
Existen librerías en js que convierten cierto código en html para facilitar el desarrollo como por ejemplo PUG antes llamado Jade

### Ejemplo
Pug
```
doctype 5
html(lang=”es”)
 head
  title Template Pug 
 body
  h1#encabezado Hola Mundo!
  p.centrar Ingresa tu información
  input(type="text", placeholder="ingresa tu nombre")
```
Resultado en Html
```
<!DOCTYPE html>
<html lang="es">
  <head>
    <title>Template Pug</title>
  </head>
  <body>
  <h1 id="encabezado"> Hola Mundo!</h1>
  <p class="centrar">Ingresa tu información</p>
  <input type="text" placeholder="ingresa tu nombre">
  </body>
</html>

```
## Tarea
- Arma una estructura básica html de una web que ofrece noticias que contenga los siguientes elementos:
- Header con el titulo del diario
- Menu con las categorias de noticias (Mundo, Tecnologia, Arte, Política)
- Titulo de una noticia 
- Descripción de una noticia
- Un formulario para suscribirse a newsletter que solicite:
  - el email => maximo 100 caracteres
  - el nombre => maximo 50 caracteres
  - un boton de registrarse
- Footer de la página
Nota: no se calificara css solo la estructura de las etiquetas html

## Links
HTML => https://developer.mozilla.org/es/docs/Web/HTML
HTML 5 => https://developer.mozilla.org/es/docs/HTML/HTML5
Etiquetas => https://developer.mozilla.org/es/docs/HTML/HTML5/HTML5_lista_elementos
Pug, Template engines => https://medium.com/laboratoria-how-to/conoce-todo-sobre-pug-1ba98496191a