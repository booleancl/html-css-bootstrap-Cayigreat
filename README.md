# HTML CSS BOOTSTRAP

Html Css y Javascript son los pilares de toda aplicación web
Cualquier cosa que funcione dentro de un navegador web (como chrome, mozzila o safari) utiliza estos pilares. Y no solo eso, hoy también se pueden hacer aplicaciones "nativas" con estas tecnologías.

## HTML 

Significa **Hyper Text Markul Language** en español sería como Lenguaje de marcado de hiper texto. Lenguaje de marcado es por las *Etiquetas*. Dependiendo de su etiqueta el navegador lo procesa de diferentes formas. Y el hiper texto se refiere a que estos documentos están enlazados por *links*.

Con HTML crearemos *documentos* estructurados que el navegador puede interpretar.

El documento principal de un sitio o aplicación se debe llamar **index.html**. Todo junto y en minúsculas.

### Un poquito de historia

HTML inicialmente estaba pensado para transmitir documentación científica. Y se necesitaba una forma de indicar que secciones del documento eran párrafos, imágenes, títulos y encabezados. Con este motivo nació HTML

### Doctype

Esta primera etiqueta indica al navegador la versión de HTML. En este caso indica que es la versión 5.
```html
<!DOCTYPE html>
```

### Html

Luego de eso viene la primera etiqueta que es parte del documento. La famosa etiqueta **html**:

```html
<html lang="es">
    ...
</html>  
```

Del ejemplo anterior vemos que esta etiqueta se compone de 2 partes principales. La etiqueta se compone de 2 partes principales. La etiqueta de apertura `<html>` y la de cierre `<html>`.

Entremedio de las etiquetas de apertura y cierre irá el contenido.

Además vemos que la etiqueta de apertura tiene el **atributo** `lang="es"`, lo que le indica al navegador en qué idioma está el contenidor del documento.

>**ATENCIÓN**: Solo las etiquetas de apertura pueden tener atributos, las etiquetas de cierre NO.

### head

A continuación viene la etiqueta `head`.
Esta etiqueta entrega información al **Navegador** sobre como visualizar el contenido que vendrá en las siguientes secciones. Por ejemplo, se indica mediante etiquetas "meta" el set de caracteres que utilizará la página.
Ejemplo:

```hmtl
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
```

La tercera etiqueta `meta` que tiene el atributo `name="viewport"` permite que el contenido se cargue inicialmente considerando el tamaño de pantalla disponible, desde grandes a muy pequeños.

Además dentro del head se encuentre la etiqueta `title`, que es la encargada de mostrar el sitio en la pestaña del navegador.

Por otra parte dentro del `head` podemos cargar otros recursos que utilizará el documento como por ejemplo hojas de estilo CSS o archivos Javascript.

### Estructura jerárquica 

Algo que es muy importante notar y que no es tan evidente, es que los documentos HTML forman una estructura jerárquica bien definida del tipo árbol.
Donde la etiqueta raíz es la etiqueta `html`. Lo podemos visualizar de la siguiente forma

```html
  <html>
    <head></head>
    <body></body>
  <html>    
```

Esto es muy importante de comprender ya que luego, manejaremos las etiquetas pensando en su ubicación relativa dentro del árbol. Y pensaremos que las etiquetas son ***nodos*** que tienen **nodos padre**, **nodos hermanos** y **nodos hijos**.


## Etiquetas principales

Podemos separar las etiquetas en 2 tipos: Semánticos y semánticos. (que tiene o no significado intrínseco)

### Títulos

Las etiquetas para hacer títulos son las etiquetas **h** con numeros del 1 al 6, Ejemplos:

```html

    <h1> Super título</h1>
    <h2>Super sub título</h2>
    <h3>Super sub sub título</h3>
    <h4>...</h4>
    <h5>...</h5>
    <h6>...</h6>
```

### Links

Los links son el corazón de internet y los crearemos frecuentemente. Se componen de el atributo `href` que indica el destino del link y su contenido, que es lo que se muestra al usuario

```html
 <a href="headings.html">Títulos</a>
 ```

 ### Imagénes

 Las imágenes sun una de las etiquetas que no requiere cierre ya que la imagen que se despliega se indica en el atributo `src` y en caso de que la imagen no esté disponible se despliega el texto indicado en el atributo `alt` conocido como texto alternativo.


### Listas

#### Ordenadas

```html  
  <ul> Días de la semana
    <li>Lunes</li>
    <li>Martes</li>
    <li>Miércoles</li>
    <li>Jueves</li>
    <li>Viernes</li>

```

#### No ordenadas

```html
   <ul>Pilares de la Web
     <li>HTML</li>
     <li>CSS</li>
     <li>Javascript</li>
   </ul>  
```

### Tablas
```html
 <table>
        <tr>
            <th>Italiano</th>
            <th>Chacarero</th>
        </tr>
        <tr>
            <td>Tomate</td>
            <td>Lechuga</td>
        </tr>
        <tr>
            <td>Palta</td>
            <td>Porotos</td>
        </tr>
        <tr>
            <td>Mayo</td>
            <td>Ají</td>
        </tr>
        
    </table> 

```

### Etiquetas no semánticas

Estas etiquetas no tienen un significado propio y sirven como contenedores para agrupar otras etiquetas

## div
El div es para separar y agrupar el contenido
```html
<div>
  <p>Hola mundo</p>
</div>
```

## span
La etiqueta span se puede usar dentro de un texto.

``html
<div>
  <p>Hola mundo</span></p>
</div>
```

La idea detrás de los elementos no semánticos es utilizar CSS para darles estilo.

Más adelante, en este módulo veremos lo frecuente de su uso con el marco de trabajo o framework Boostrap.

 
### Formularios
Contiene controles interactivos para ingresar información
```html
<form action='/search' method="get">
...    
</form>
```
Cuando enviamos el formulario mediante el método GET, los parámetros ingresados quedan reflejados en la URL después del signo '?' y separados por '&'


### CSS

Hojas de estilo en cascada (Cascade Style Sheets). CSS nos permite entregar al sitio el aspecto que queremos. Lo hace aplicando reglas de estilo  sobre los diferentes elementos del HTML.

Los navegadores tienen estilos predefinidos para mostrar las diferentes etiquetas.

Cuando el código CSS está definido dentro del mismo archivo html, se denomina css-inline, pero no es la mejor forma de definir los estilos que se van a utilizar en varias páginas. Para eso es mejor utilizar un archivo externo y vincularlo al html

### Síntaxis CSS

Las reglas CSS parten con un selector, luego dentro de las llaves se ingresan las propiedades junto con su valor.
Ejemplo:

```css

h2{
    color: blue;
    font-size: 24px;
    }

selector{
    propiedad: valor;
    propiedad: valor;
}    

p{
    color:red;
    text-align: center;
}
```

### Selectores

En el ejemplo anterior el selector era la  misma etiqueta, es decir, la regla de estilo aplica a TODAS las etiquetas de ese tipo. Tenemos otros 2 selectores muy frecuentes. El selector por 'id' y por 'clase'.

El 'id' es un atributo de las etiquetas HTML. Toda etiqueta HTML puede tener el atributo ''d' para diferenciarlo del resto. Y podemos usar ese atributo como selector CSS usando la notación '#'


Ejemplo de selector por id
```css
#fname{
    border-radius: 6px;
}
```

Ejemplo de selector por clase
```css
.some-class{
    border-radius: 6px;
}
```

CSS es muy flexible y permite combinar selectores. Ej:

```css
/* Esta regla aplica a los párrafos con clase centered */
p.centered{
    text-align: center;
    color: purple
}
```
Si tenemos reglas que se repiten. Ej:
```css

h1{
    text-align= center;
    color: blue
}

h2{
    text-align= center;
    color: blue
}
```

Podemos refactorizarlo en una sola regla

```css
h1, h2{
    text-align= center;
    color: blue
}
```

Selector | Ejemplo | Descripción
----- | ----- | -----
#id | #some-id | Selecciona el elemento con `id="some-id"`
.class | .some-class | Selecciona TODOS los elementos con clase `class="some-class"`
element.class | p.intro | Selecciona solo los `<p>` con clase `class="intro"`
element, element | div, p | Selecciona todos los elementos `<div>` y `<p>`

### Modelo de caja

En esencia cada elemento html está inserto dentro de una caja que consiste de: Margen, Borde, Padding y contenido.

![Box Model](img/box-model.png)

### Unidades de medidas

En general, no solo en el desarrollo web. Podemos clasificar las unidades de medidas en dos grupos:

- Unidades Absolutas: px
- Unidades Relativas: %, rem, em, vh, vw

#### rem
Es una unidad de medida relativa al font-size del elemento raíz

#### em
es relativa al font-size del mismo elemento

#### vh
Es relativo al 1% del alto de la pantalla (viewport)

#### vw
Es relativo al 1% del ancho de la pantalla(viewport)


### Tipos de diseños

- El diseño estático: sirve para un solo tamaño de pantalla

- El diseño fluído: se basa en porcentajes(%) dependiendo del tamaño de la pantalla

- Diseño responsivo: tiene puntos de quiebre( distintos tamaños) para aplicar diferentes estilos

### CSS MediaQueries


Utiliza la regla `@media` para incluir un bloque de propiedades CSS solo si la condición es verdadera. Ejemplo:

```CSS
/* si el tamaño de la pantalla es de 600px o menor, el color de fondo del body será verde*/
@media only screen and (max-width: 600px){
    body{
        background-color: green
    }
}
```

Existen ciertos tamaños de pantallas  más o menos estandarizados y estas serían sus respectivas media queries:

```css
/* Extra small devices (phones, 600px and down) */
@media only screen and (max-width: 600px) {...}

/* Small devices (portrait tablets and large phones, 600px and up) */
@media only screen and (min-width: 600px) {...}

/* Medium devices (landscape tablets, 768px and up) */
@media only screen and (min-width: 768px) {...}

/* Large devices (laptops/desktops, 992px and up) */
@media only screen and (min-width: 992px) {...}

/* Extra large devices (large laptops and desktops, 1200px and up) */
@media only screen and (min-width: 1200px) {...} 
```

### Display

```CSS
/* si el tamaño de la pantalla es de 600px o menor, el color de fondo del body será verde*/
@media only screen and (max-width: 600px){
    body{
        background-color: green
    }
    p{
        display: none;
    }
 /* display none, oculta los párrafos si la condición se cumple*/
}
```

El valor de la propiedad display modifica como el navegador posicionará la caja del elemento

La caja puede ser de lado a lado, en ese caso la propiedad display tendrá el valor block.
También podemos establecer el valor como inline y en ese caso, la caja será del menor tamaño posible. Ejemplo:


```CSS
.side-to-side{
    display: block;
    border: solid
}
.narrow{
    display: block;
    border: solid
    }
    
    ```
### Marcos de trabajo o Frameworks CSS

Los marcos de trabajo CSS traen hecho el css responsivo listo para ser utilizado. En general se utilizará mediante clases css. El framework define una serie de clases y utilidades que han sido diseñadas y probadas para cumplir con los requisitos de un diseño moderno y usable.

Uno de los más famosos es Bootstrap. Un marco de trabajo de codigo libre utilizado en millones de sitios y apps.

### Boopstrap

Boopstrap basa su enfoque en dividir el espacio disponible en una grilla de filas y columnas. Mediante las clases`row` y `col` .


Bootstrap es un framework orientado al desarrollo mobile, es decir, su principal preocupacion son los dispositivos pequeños. Se llama a sí mismo un framework "Mobile First"


### Contenedores


