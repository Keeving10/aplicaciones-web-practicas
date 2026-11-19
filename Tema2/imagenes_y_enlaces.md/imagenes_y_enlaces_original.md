# $\textcolor{orange}{\textsf{NIVEL 2 — IMÁGENES Y ENLACES}}$

## $\textcolor{orange}{\textsf{PARTE A. COMPROBACIÓN Y REFLEXIÓN (SIN ORDENADOR)}}$

# $\textcolor{yellow}{\textsf{A1. Verdadero o falso (corrige las falsas)}}$

| Num | Afirmacion | V/F |
|-----|------------|-----| 
| 1 | "La etiqueta <img> se cierra con </img>." | F. img no se cierra con / img. Es una etiqueta vacia como br o hr 
| 2 | "El atributo alt muestra un texto si la imagen no se puede cargar." | V 
| 3 | "Para dar ancho y alto a una imagen se recomienda usar style en lugar de width y height." | V 
| 4 | "La propiedad float permite que una imagen flote a la izquierda o a la derecha del texto, o que no flote." | V 
| 5 | "El rótulo de un enlace solo puede ser un texto." | F.Puede ser texto o una imagen, incluso varias.
| 6 | "target=\"_blank\" hace que el enlace se abra en una ventana (pestaña) nueva." | V 
| 7 | "Por defecto, un enlace ya visitado se ve azul y uno por visitar, morado." | F. Esta al reves, un enlace por visitar se ve azul y uno YA VISITADO, morado 
| 8 | "Un enlace relativo escribe la URL completa, incluido el dominio." | F. Eso es un enlace ABSOLUTO. Un enlace relativo escribe la ruta respecto a la ubicación del archivo actual. 

# $\textcolor{green}{\textsf{A2. Relaciona atributo y función}}$

| Elemento | Descripción |
|----------|-------------|
| 1.src | D. Ruta del archivo de imagen |
| 2. alt | G. Texto que se muestra si la imagen no carga |
| 3. href | B. Indica el destino del enlace |
| 4. target | F. Indica dónde se abrirá el destino del enlace |
| 5. id | A. Crea un marcador (bookmark) dentro de la página |
| 6. float | E. Propiedad CSS para que la imagen flote junto al texto |
| 7. _blank | C. Valor de target que abre una pestaña nueva |

# $\textcolor{yellow}{\textsf{A3. ¿Absoluto o relativo?}}$

| URL | Tipo |
|-----|------|
| `1. https://www.w3.org/` | Absoluto |
| `2. paginas/contacto.html` | Relativo |
| `3. /css/default.asp` | Relativo |
| `4. https://www.google.com/` | Absoluto |
| `5. ./apuntes.pdf` | Relativo |
| `6. imagenes/logo.png` | Relativo |

# $\textcolor{blue}{\textsf{A4. Formatos de imagen}}$

| Abreviatura | Nombre completo | Extensión |
|-------------|-----------------|-----------|
| GIF | Graphics Interchange Format | .gif |
| JPEG | Joint Photographic Experts Group | .jpg/.png |
| PNG | Portable Network Graphics | .png |
| SVG | Scalable Vector Graphics | .svg |
| ICO | Icon format | .ico |
| APNG | Animated Portable Network Graphics | .png |

# $\textcolor{green}{\textsf{A5. Caza los errores de la galería (hay al menos 5)}}$
- El primer `<img>` tiene el src FUERA de la etiqueta: `<img>src="playa.jpg"... → el atributo va dentro: <img src="playa.jpg">`.
- Se usa `</img>` y esa etiqueta de cierre NO existe.
- El segundo `<img>` no tiene alt (obligatorio en el boletín y por accesibilidad).
- En el style se usa = en vez de : — en CSS es width: 300px;.
- El href va sin comillas: al tener un espacio después, el navegador interpreta mal el valor. Siempre href="https://...".
- El enlace nunca se cierra: falta el </a>.

Versión corregida:

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="utf-8">
  <meta name="author" content="Kevin Daniel Quizhpe Inga">
  <title>Mi galería</title>
</head>
<body>
  <h1>Mi viaje de fin de curso</h1>
  <img src="playa.jpg" alt="Playa al atardecer">
  <img src="monte.jpg" alt="Montaña del viaje" style="width:300px; height:200px;">
  <a href="https://www.wikipedia.org" target="_blank">Más información sobre el destino</a>
</body>
</html>
```
# $\textcolor{yellow}{\textsf{A6. Rutas que no funcionan}}$
| Linea | Funciona | Correcion |
|-------|----------|-----------|
| `<img src="logo.png">` | NO | `imagenes/logo.png (el logo está en la subcarpeta)` |
| `<img src="imagenes/equipo.jpg">` | SI |  |
| `<a href="Contacto.html">>` | NO | `contacto.html` (en servidores mayúsculas y minúsculas NO son lo mismo) |
| `<a href="apuntes.pdf">">` | SI |  |
| `<a href="imagenes/apuntes.pdf">">` | NO | `apuntes.pdf` (está en la raíz, no en imagenes) |
| `<img src="imagenes/equipo.png">">` | NO | `imagenes/equipo.jpg` (extensión equivocada) |

# $\textcolor{yellow}{\textsf{A7. ¿Qué verá el usuario?}}$

(a) La imagen del gato flota a la DERECHA `(float: right)` y el texto del párrafo rodea su lado izquierdo.

(b) Si `gato.jpg` no existe, se muestra el texto del alt: "Gato durmiendo" (normalmente acompañado de un icono de imagen rota).

(c) Al hacer clic en el logo se abre `https://www.w3.org/` en una PESTAÑA NUEVA, porque el enlace lleva `target="_blank"` y su rótulo es la imagen.

# $\textcolor{springgreen}{\textsf{PARTE B. EJERCICIOS GUIADOS}}$

## $\textcolor{blue}{\textsf{B1. Galería de tu setup}}$

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="utf-8">
  <meta name="author" content="Kevin Daniel Quizhpe Inga">
  <title>B1 - Galería de mi setup</title>
</head>
<body>
  <!--
  PREGUNTA: ¿por qué se recomienda style frente a width y height?
  RESPUESTA: porque style (CSS) es la forma moderna y más potente: con la
  propiedad style puedes controlar muchas más cosas (bordes, márgenes,
  max-width...), mantener el aspecto en un solo sitio y es lo que se usa
  en el mundo real. Los atributos width y height del HTML solo aceptan
  medidas en píxeles y se consideran anticuados para dar estilo.
  -->

  <h1>Galería de mi setup</h1>

  <p>Tamaño original:</p>
  <img src="imagenes/setup.jpg" alt="Mi setup a tamaño original">

  <p>Redimensionada con style (200 × 150 px):</p>
  <img src="imagenes/setup.jpg" alt="Mi setup reducida con style" style="width:200px; height:150px;">

  <p>Redimensionada con width y height (200 × 150 px):</p>
  <img src="imagenes/setup.jpg" alt="Mi setup reducida con atributos" width="200" height="150">

  <p>Prueba con src roto a propósito:</p>
  <img src="imagenes/setu.jpg" alt="Imagen rota: aquí se ve el texto alt en lugar de la foto">
</body>
</html>
```

# $\textcolor{yellow}{\textsf{B2. Perfil de una red social}}$
```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="utf-8">
  <meta name="author" content="Kevin Daniel Quizhpe Inga">
  <title>B2 - Perfil de red social</title>
</head>
<body>
  <!--
  PREGUNTA: ¿qué diferencia visual hay entre left, right y none?
  RESPUESTA: con float:left la imagen se coloca a la IZQUIERDA y el texto
  fluye por su derecha; con float:right la imagen va a la DERECHA y el
  texto la rodea por la izquierda; con float:none la imagen NO flota:
  se queda en su sitio dentro del flujo normal de la página y el texto
  no la rodea, continúa debajo.
  -->

  <h1>Kevin Daniel Quizhpe Inga</h1>

  <img src="imagenes/perfil.jpg" alt="Foto de perfil de Kevin Daniel Quizhpe Inga"
       style="float:right; border:5px solid green; width:200px;">

  <p>Hola, soy Kevin Daniel Quizhpe Inga, estudiante de 2.º SMR y aficionado
  a la tecnología desde siempre. Me encanta trastear con ordenadores y aprender
  cómo funcionan las webs por dentro.</p>

  <p>En mi tiempo libre juego al baloncesto, monto mi setup poco a poco y sigo
  canales de informática. Este curso estoy aprendiendo HTML y CSS y me está
  gustando mucho más de lo que esperaba.</p>

  <p> Mi objetivo es seguir en el mundo de los sistemas y las redes, así que
  apunto todo lo que aprendo para no olvidarlo. ¡Bienvenido a mi perfil!</p>

  <img src="imagenes/setup.jpg" alt="Foto de mi setup"
       style="float:left; border:3px dotted blue; width:250px;">

  <p>Esta es mi zona de estudio: dos pantallas, teclado mecánico y muchas
  pestañas abiertas. El borde punteado azul la distingue de la foto de perfil.</p>

  <img src="imagenes/mascota.jpg" alt="Mi mascota"
       style="float:none; width:250px;">

  <p>Y esta es la mascota de la casa, sin flotar y sin borde, como pide el
  ejercicio: una imagen tranquila dentro del flujo normal.</p>
</body>
</html>
```

# $\textcolor{orange}{\textsf{B3. ¿Qué formato elijo?}}$
```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="utf-8">
  <meta name="author" content="Kevin Daniel Quizhpe Inga">
  <title>B3 - Qué formato elijo</title>
</head>
<body>
  <h1>¿Qué formato de imagen elijo?</h1>

  <p>Para una <strong>foto de vacaciones con muchos colores usaré JPEG (.jpg)</strong>,
  porque comprime muy bien las fotografías y soporta millones de colores
  manteniendo el archivo ligero.</p>

  <p>Para un <strong>logo con fondo transparente usaré PNG (.png)</strong>,
  porque admite transparencia real sin bordes feos alrededor del logo.</p>

  <p>Para un <strong>icono nítido a cualquier tamaño usaré SVG (.svg)</strong>,
  porque es vectorial: por mucho que lo amplíes nunca se pixela.</p>

  <p>Para una <strong>animación corta tipo meme usaré GIF (.gif)</strong>,
  el clásico formato de animación en bucle que funciona en todas partes.</p>

  <p>Para el <strong>icono de la pestaña del navegador usaré ICO (.ico)</strong>,
  el formato pensado para el favicon de una web.</p>

  <p>Dos ejemplos reales de formatos distintos:</p>
  <img src="imagenes/foto-vacaciones.jpg" alt="Ejemplo de foto JPEG">
  <img src="imagenes/icono.svg" alt="Ejemplo de icono SVG">
</body>
</html>
```

# $\textcolor{blue}{\textsf{B4. Mis enlaces favoritos}}$
```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="utf-8">
  <meta name="author" content="Kevin Daniel Quizhpe Inga">
  <title>B4 - Mis enlaces favoritos</title>
</head>
<body>
  <!--
  PREGUNTA: ¿de qué color se ve por defecto un enlace por visitar y uno ya visitado?
  RESPUESTA: por visitar se ve AZUL y si ya lo has visitado se ve MORADO.
  Lo pinta así el navegador por defecto, sin que nosotros hagamos nada.
  -->

  <h1>Mis enlaces favoritos</h1>

  <p><a href="https://www.w3.org/">Web oficial del W3C (misma ventana)</a></p>

  <p><a href="https://www.google.com/" target="_blank">Google (se abre en pestaña nueva)</a></p>

  <p><a href="https://www.wikipedia.org/" target="_blank" style="color:tomato;">Wikipedia (pestaña nueva y en otro color)</a></p>
</body>
</html>
```

# $\textcolor{springgreen}{\textsf{B5. Enlaces con imagen}}$
```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="utf-8">
  <meta name="author" content="Kevin Daniel Quizhpe Inga">
  <title>B5 - Enlaces con imagen</title>
</head>
<body>
  <!--
  IDENTIFICACIÓN DE LOS ENLACES:

  Enlace 1:
  - Destino: https://www.w3.org/ (web externa)
  - Rótulo: solo una imagen (logo.png)
  - Objetivo: abrir la web del W3C en una pestaña nueva al hacer clic en la imagen

  Enlace 2:
  - Destino: https://es.wikipedia.org/ (web externa)
  - Rótulo: una imagen Y un texto a la vez (el logo + el texto "Ir a la Wikipedia")
  - Objetivo: abrir la Wikipedia en una pestaña nueva; como ambos elementos están
    dentro del <a>, se puede clicar en cualquiera de los dos
  -->

  <h1>Enlaces con imagen</h1>

  <p>Enlace 1 (rótulo solo imagen):</p>
  <a href="https://www.w3.org/" target="_blank">
    <img src="imagenes/logo.png" alt="Logo que enlaza al W3C">
  </a>

  <p>Enlace 2 (rótulo imagen + texto):</p>
  <a href="https://es.wikipedia.org/" target="_blank">
    <img src="imagenes/icono.svg" alt="Icono de la Wikipedia"> Ir a la Wikipedia
  </a>
</body>
</html>
```

# $\textcolor{springgreen}{\textsf{B6. Mini web de tres páginas}}$

## index . html
```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="utf-8">
  <meta name="author" content="Kevin Daniel Quizhpe Inga">
  <title>Mini web - Inicio</title>
</head>
<body>
  <h1>Página de inicio</h1>

  <p>
    <a href="index.html">Inicio</a> |
    <a href="sobre-mi.html">Sobre mí</a> |
    <a href="contacto.html">Contacto</a>
  </p>

  <img src="imagenes/logo.png" alt="Logo de la mini web">

  <p>Bienvenido a mi primera mini web de tres páginas conectadas con
  enlaces relativos.</p>
</body>
</html>
```
## sobre-mi . html

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="utf-8">
  <meta name="author" content="Kevin Daniel Quizhpe Inga">
  <title>Mini web - Sobre mí</title>
</head>
<body>
  <h1>Sobre mí</h1>

  <p>
    <a href="index.html">Inicio</a> |
    <a href="sobre-mi.html">Sobre mí</a> |
    <a href="contacto.html">Contacto</a>
  </p>

  <p>Soy Kevin Daniel Quizhpe Inga, estudiante de 2.º SMR. Esta página
  forma parte de mi práctica de enlaces relativos.</p>
</body>
</html>
```

## contacto . html

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="utf-8">
  <meta name="author" content="Kevin Daniel Quizhpe Inga">
  <title>Mini web - Contacto</title>
</head>
<body>
  <h1>Contacto</h1>

  <p>
    <a href="index.html">Inicio</a> |
    <a href="sobre-mi.html">Sobre mí</a> |
    <a href="contacto.html">Contacto</a>
  </p>

  <p>Puedes escribirme a kevin12.kd89@gmail.com o visitarme en el instituto primera planta.</p>

  <p>Enlace absoluto a una web externa:
  <a href="https://www.w3.org/" target="_blank">W3C</a></p>
</body>
</html>
```
## Pregunta: 
- ¿Qué enlaces dejarían de funcionar si movieras contacto.html a otra carpeta?
  Si moviese contacto.html a otra carpeta, dejarian de funcionar sus enlaces relativos por que estas se calculan desde la unbicación del archivo actual. El enlace absoluto funcionaria ya que estos no dependen de donde vive el archivo.

# $\textcolor{blue}{\textsf{B7. Tu propia chuleta}}$

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="utf-8">
  <meta name="author" content="Kevin Daniel Quizhpe Inga">
  <title>B7 - Mi chuleta</title>
</head>
<body>
  <h1>Mi chuleta de HTML y CSS</h1>

  <p><a href="chuleta.pdf">Abrir la chuleta en PDF (misma ventana)</a></p>

  <p><a href="chuleta.pdf" target="_blank">Abrir la chuleta en PDF (pestaña nueva)</a></p>

  <p><a href="https://www.w3.org/" target="_blank">Recurso externo: web del W3C</a></p>
</body>
</html>
```
Pregunta: ¿qué pasa si borras el PDF de la carpeta? El enlace se romperia saldria el error 404 de archivo no encontrado.
