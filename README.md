# AE Floristería y Eventos

## 1. Descripción del proyecto

AE Floristería y Eventos es un sitio web desarrollado para promocionar servicios de arreglos florales, decoración y organización de eventos especiales.

El sitio fue construido utilizando HTML5 y CSS3, aplicando principios de diseño responsive, accesibilidad, estructura semántica y buenas prácticas de desarrollo web.

Los servicios principales ofrecidos son:

- Arreglos florales personalizados.
- Decoración de bodas.
- Decoración para quince años.
- Fiestas infantiles.
- Celebraciones familiares y eventos especiales.

---

# 2. Estructura del proyecto

```text
ae-floristeriayeventos
│
├── capturas
│
├── css
│   └── styles.css
│
├── imagenes
│   ├── arreglo-floral.jpg
│   ├── bodas.jpg
│   ├── bodas2.jpg
│   ├── fiestas.jpg
│   ├── fiestas2.jpg
│   ├── ramos.jpg
│   └── ramos2.jpg
│
├── video
│   └── videoevento.mp4
│
├── index.html
├── servicios.html
└── README.md
```
# 3. Sistema visual

Para el diseño del sitio se utilizó una combinación de colores relacionada con la naturaleza, las flores y las celebraciones.

## Variables CSS utilizadas

```css
:root{
    --color-principal:#4f6f52;
    --color-secundario:#c9a227;
    --color-fondo:#faf8f3;
    --color-blanco:#ffffff;
    --color-texto:#333333;
    --color-borde:#e2d6b5;
}
```

## Tipografía

```css
font-family: Georgia, serif;
```

Esta tipografía fue seleccionada porque transmite elegancia y profesionalismo, características asociadas a una floristería y organización de eventos.

---

# 4. Estructura semántica

Para organizar adecuadamente el contenido se utilizaron las siguientes etiquetas semánticas:

```html
<header>
<nav>
<main>
<section>
<article>
<aside>
<footer>
```

También se emplearon otras etiquetas semánticas y de contenido:

```html
<blockquote>
<cite>
<strong>
<em>
<s>
<abbr>
```

Estas etiquetas permiten una mejor organización, accesibilidad y significado del contenido.

---

# 5. Selectores CSS utilizados

Durante el desarrollo se utilizaron diversos tipos de selectores CSS.

## Selector de clase

```css
.servicios__tarjeta{
    padding:1.5rem;
}
```

## Selector de atributo

```css
a[target="_blank"]{
    color:var(--color-principal);
}
```

## Combinador hijo

```css
.servicios__tarjeta > p{
    text-align:justify;
}
```

## Pseudoclase estructural

```css
.servicios__tarjeta:nth-child(2){
    border:2px solid var(--color-secundario);
}
```

---

# 6. Herencia en CSS

La herencia permite que algunos estilos definidos en un elemento padre sean transmitidos a los elementos hijos.

Ejemplo:

```css
body{
    color:var(--color-texto);
    font-family:Georgia, serif;
}
```

Gracias a esto, todos los textos del sitio heredan automáticamente la tipografía y el color definidos en el elemento `body`, salvo cuando son sobrescritos por reglas más específicas.

---

# 7. Modelo de cajas

Todos los elementos HTML se comportan como una caja compuesta por:

- Contenido (content).
- Relleno (padding).
- Borde (border).
- Margen (margin).

Ejemplo:

```css
.servicios__tarjeta{
    padding:1.5rem;

    border-top:3px solid var(--color-secundario);
    border-right:1px solid var(--color-borde);
    border-bottom:1px solid var(--color-borde);
    border-left:1px solid var(--color-borde);

    margin:1rem;
}
```

### Explicación

- El contenido corresponde a la información mostrada.
- El padding genera espacio interno.
- El border delimita el elemento.
- El margin genera separación externa respecto a otros elementos.

---

# 8. Diseño Responsive

El sitio fue desarrollado bajo el enfoque Responsive Design para adaptarse a dispositivos móviles y de escritorio.

Se implementó la siguiente Media Query:

```css
@media (max-width:360px){
    .nav__lista{
        flex-direction:column;
    }
}
```

## Adaptaciones implementadas

- Menú adaptable para dispositivos móviles.
- Imágenes responsivas.
- Video adaptable.
- Mapa adaptable.
- Tarjetas de servicios adaptables.
- Espaciado optimizado para pantallas pequeñas.

---

# 9. Conflictos de especificidad CSS

Durante el desarrollo se realizaron pruebas para comprender cómo funciona la especificidad en CSS.

## Conflicto 1 - Clase contra clase

```css
.servicios__tarjeta p{
    color:black;
}
```

```css
.servicios__tarjeta--destacada p{
    color:green;
}
```

### Resultado

Gana la segunda regla porque tiene mayor especificidad.

### Evidencia

Insertar captura del Inspector del navegador.

---

## Conflicto 2 - Mismo selector

```css
.footer a{
    color:red;
}
```

```css
.footer a{
    color:white;
}
```

### Resultado

Gana la segunda regla porque aparece después dentro de la hoja de estilos.

### Evidencia

Insertar captura del Inspector del navegador.

---

## Conflicto 3 - Etiqueta contra clase

```css
article p{
    font-size:1rem;
}
```

```css
.servicios__tarjeta p{
    font-size:1.05rem;
}
```

### Resultado

Gana la segunda regla porque utiliza una clase y tiene mayor especificidad.

### Evidencia

Insertar captura del Inspector del navegador.

---

# 10. Problemas encontrados y soluciones

## Problema 1

Las imágenes de los servicios tenían tamaños diferentes.

### Solución

Se aplicó:

```css
object-fit:cover;
height:320px;
```

para uniformar el tamaño de las imágenes.

---

## Problema 2

El video no tenía una presentación visual atractiva.

### Solución

Se creó un contenedor decorativo utilizando:

```css
.video-marco
```

incorporando gradientes, sombras y bordes redondeados.

---

## Problema 3

La navegación no se adaptaba correctamente a dispositivos móviles.

### Solución

Se implementó una Media Query para pantallas de 360 píxeles.

---

# 11. Evidencias

Todas las capturas se encuentran dentro de la carpeta:

```text
capturas/
```

## Captura 1 - Página principal

![Pturas/01-index.png

Se muestra la página principal del sitio web con el encabezado, menú de navegación, presentación del negocio y video decorativo.

---

## Captura 2 - Servicios

capturas/02-servicios.png

Se observan las tarjetas de servicios con sus respectivas imágenes.

---

## Captura 3 - Video decorativo

capturas/03-video.png

Se evidencia el contenedor personalizado del video utilizando gradientes, bordes redondeados y sombras.

---

## Captura 4 - Opiniones de clientes

capturas/04-opiniones.png

Se muestran las opiniones utilizando las etiquetas semánticas `blockquote` y `cite`.

---

## Captura 5 - Ubicación y contacto

capturas/05-ubicacion.png

Se visualiza el mapa, los datos de contacto y los enlaces externos.

---

## Captura 6 - Página servicios.html

capturas/06-servicios-html.png

Vista general de la segunda página.

---

## Captura 7 - Tabla de precios

capturas/07-tabla.png

Tabla de precios utilizando `colspan`.

---

## Captura 8 - Formulario

![Formularioformulario.png

Formulario de contacto con diferentes tipos de campos.

---

## Captura 9 - Diseño responsive

capturas/09-responsive.png

Visualización del sitio en una pantalla de 360 píxeles de ancho.

---

## Captura 10 - Conflicto de especificidad 1

capturas/10-conflicto-1.png

Conflicto entre:

```css
.servicios__tarjeta p
```

y

```css
.servicios__tarjeta--destacada p
```

---

## Captura 11 - Conflicto de especificidad 2

capturas/11-conflicto-2.png

Conflicto entre:

```css
.footer a{
    color:red;
}
```

y

```css
.footer a{
    color:white;
}
```

---

## Captura 12 - Conflicto de especificidad 3

![Confas/12-conflicto-3.png

Conflicto entre:

```css
article p
```

y

```css
.servicios__tarjeta p
```

---

## Captura 13 - Inspector del navegador

capturas/13-inspector.png

Visualización del Inspector de elementos mostrando la regla CSS que prevalece según la especificidad.


# Conclusiones

El desarrollo de AE Floristería y Eventos permitió aplicar conceptos fundamentales de HTML5 y CSS3, incluyendo estructura semántica, accesibilidad, diseño responsive, modelo de cajas, selectores avanzados y especificidad CSS.

El resultado es un sitio web funcional, visualmente atractivo y adaptable a diferentes dispositivos, orientado a la promoción de servicios de decoración floral y organización de eventos.