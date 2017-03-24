**Investigar Viewport**

Viewport es todo lo que vemos dentro de una pagina web.

```
<meta name="viewport" content="width=device-width, user-scalable=no">
```

- width controla el tamaño del viewport.
- el width puede definirse en pixeles o con device-width que es equivalente al ancho de la pantalla.

```
initial-scale
```

- Controla el nivel de zoom cuando la pantalla de carga por primera vez.

```
maximum-scale, minimum-scale, y user-scalable
```

- controlan la forma en que se permite a los usuarios aumentar o disminuir el zoom de la pagina.

```
<meta name="viewport" content="width=500, initial-scale=1">
```

- La escala inicial o maxima se traduce en que la propiedad width pasa a ser el ancho minimo en viewport, en el ejemplo anterior si la pantalla tiene un ancho mayor a 500 px, el navegador extendera el viewport, en lugar de acerca el zoom

**valores semanticos html**

```
<section></section>:
```

- se utiliza para representar una sección "general" dentro de un documento o aplicación, como un capítulo de un libro.

```
<article></article>
```

-  Es utilizado en las paginas web, para los elementos que puedan ser repetidos o reutilizados en su caso en foros, una revista o un un articulo de periodico.

```
<aside></aside>
```

- representa una sección de la página que abarca un contenido relacionado con el contenido que lo rodea, por lo que se le puede considerar un contenido independiente, comunmente usado en barras laterales o grupos de elementos de la navegacion.

```
<header></header>
```

- contiene por lo general la cabecera de la sección (un elemento h1-h6 o un elemento hgroup), pero no es necesario.

```
<nav></nav>
```

- Representa una sección de una página que enlaza a otras páginas o a otras partes dentro de la página.

```
<footer></footer>
```

- representa el pie de una sección, con información acerca de la página/sección que poco tiene que ver con el contenido de la página, como el autor, el copyright o el año.

```
<hgroup></hgroup>
```

- Representa el encabezado de una sección. El elemento se utiliza para agrupar un conjunto de elementos h1-h6 cuando el título tiene varios niveles, tales como subtítulos o títulos alternativos.

```
<time>
```

- Representa una hora (en formato de 24 horas), o una fecha precisa en el calendario gregoriano, opcionalmente con un tiempo y un desplazamiento de zona horaria.

**estructura html5**
![estructura html5](html5.png)

**flex-box**

- estos componentes estan declarados para la posicion
de los elementos dentro de una caja, la caja estara compuesta por display: flex  y dentro de la caja estaran todos los items .flex-item {   }

- La propiedad flex-direction especifica la direccion de los elementos flexibles dentro del contenedor de flexion, el valor prederterminado de la direccion de flexion es fila (puede ser de izquierda a derecha, arriba o abajo).

**Ejemplo**

```
.flex-container {
    display: -webkit-flex;
    display: flex;
    -webkit-flex-direction: row-reverse;
    flex-direction: row-reverse;
    width: 400px;
    height: 250px;
    background-color: lightgrey;
}
```
**Ejemplo Usando columnas**

```
.flex-container {
    display: -webkit-flex;
    display: flex;
    -webkit-flex-direction: column;
    flex-direction: column;
    width: 400px;
    height: 250px;
    background-color: lightgrey;
}
```
**Ejemplo usando columnas inversas**


```
.flex-container {
    display: -webkit-flex;
    display: flex;
    -webkit-flex-direction: column-reverse;
    flex-direction: column-reverse;
    width: 400px;
    height: 250px;
    background-color: lightgrey;
}
```

**Justificar el contenido**

- Justificar todos los items horizontalmente

- Ejemplo usando flex-end


```
.flex-container {
    display: -webkit-flex;
    display: flex;
    -webkit-justify-content: flex-end;
    justify-content: flex-end;
    width: 400px;
    height: 250px;
    background-color: lightgrey;
}
```
- Ejemplo usando center


```
.flex-container {
    display: -webkit-flex;
    display: flex;
    -webkit-justify-content: center;
    justify-content: center;
    width: 400px;
    height: 250px;
    background-color: lightgrey;
}
```

- Alinear los items hasta abajo


```
.flex-container {
    display: -webkit-flex;
    display: flex;
    -webkit-align-items: flex-end;
    align-items: flex-end;
    width: 400px;
    height: 250px;
    background-color: lightgrey;
}
```

**Flex-wrap**


Especifica los elementos flex y que se deben envolver o no, si no hay espacio para ellos en una linea flex.


```
.flex-container {
    display: -webkit-flex;
    display: flex;
    -webkit-flex-wrap: nowrap;
    flex-wrap: nowrap;
    width: 300px;
    height: 250px;
    background-color: lightgrey;
}
```


**Tabla de propiedades**


| propiedades    | Descripcion    |
| :------------- | :------------- |
| display        | Especifica el tipo de cuadro para el elemento |
| flex-direction | Especifica la dirección de los elementos flexibles dentro la caja |
| justify-content| horizontalmente alinea los elementos |
| align-items    | verticalmente alinea los elementos |
| flex-wrap      | especifica si los elementos deben ser envueltos o no |
| align-content  | es similar a alinear los elementos, pero en lugar de alinear elementos flexibles, alinea lineas flexibles |
| flex-flow      | una propiedad abreviada para flex direction y flex-wrap |
| order          | Especifica el orden de un elemento flexible con el resto de los elementos flexibles dentro de el mismo contenedor |
| align-self     | anula la propiedad align-items del contenedor |
| flex           | Especifica la longitud de un elemento flex |


**Sass version Sass**

- dispone de dos formatos diferentes para la sintaxis el .sass y el .scss

- Una de las reglas de su sintaxis es que no usan ; ni llaves

-al igual se pueden declarar variables, mayormente utilizadas para colores o tambien breakpoints.


**colores**
```
$brand: #F98355;
body{
color:$brand;
}
```


**breakpoints**
```
$tablet-landscape-desktop: '(min-width: 768px) and (max-width: 979px)';
```

**Ejemplo de sass**

```
$font-stack:    Helvetica, sans-serif
$primary-color: #333

body
  font: 100% $font-stack
  color: $primary-color

```

**crear una variable**


Todas las variables empiezan con $

Por ejemplo $width : 100%


**Utilizando los mixins**

- Para crearlos debemos utilizar al signo de arroba (@) seguido de la palabra clave mixin y por último el nombre que queramos darle al mixin. Luego, para declararlo dentro de un componente, usamos la palabra clave @include, seguido de un espacio, el nombre y por último entre paréntesis () escribimos los argumentos requeridos por nuestro Mixin. Los argumentos son opcionales.


```
@mixin sizes($width, $height: $width)
  height: $height
  width: $width

.box
  @include sizes(200px)

```
