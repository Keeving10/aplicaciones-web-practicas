# $\textcolor{blue}{\textsf{PARTE A COMPROBACION Y REFLEXION}}$

## $\textcolor{green}{\textsf{A1 VERDADERO O FALSO (CORREGIR LOS FALSOS)}}$

| Nº | Afirmación | V/F |
|----|------------|-----|
| 1  | "HTML es un lenguaje de programación como Python: sirve para hacer cálculos y tomar decisiones." | F. Es un lenguaje de marcado. 
| 2  | "La etiqueta `<br>` no necesita etiqueta de cierre." | V
| 3  | "El valor de un atributo siempre se escribe entre comillas." | V
| 4  | "Los atributos de una etiqueta se escriben en la etiqueta de cierre." | F. Los atributos de una etiqueta se escriben en la etiqueta de apertura.
| 5  | "El texto de `<title>` aparece en la pestaña del navegador." | V
| 6  | `<strong>` y `<b>` se visualizan igual." | V
| 7  | "Todo lo que escribimos dentro de <head> se ve en la página." | V
| 8  | "La etiqueta `<hr>` se cierra con `</hr>`." | V
| 9  | "Un comentario HTML `(<!-- ... -->)` se muestra en pantalla como una nota gris." | F. Un comentario en HTML nunca se muestra en la pantalla del navegador.
| 10 | "`<span>` crea un bloque de texto que siempre empieza en una línea nueva." | F. Span no empieza en una nueva linea ni genera saltos de linea automaticos, se mantiene en la misma fila junto a lo que lo rodea

## $\textcolor{orange}{\textsf{A2 RELACIONAR ETIQUETA Y EFECTO}}$

| Etiqueta |  | Efecto |  |
|----------|--|--------|--|
| 1 |  B |A. Texto tachado (precio antiguo de una oferta) |
| 2 |  A |B. Texto remarcado, como con un fosforito |
| 3 |  E |C. Texto enfatizado (se ve como cursiva) |
| 4 |  F |D. Texto más pequeño que el normal |
| 5 |  D |E. Texto en subíndice (como en H₂O)|
| 6 |  C |F. Texto en superíndice (como en m²)|
| 7 |  G |G. Texto insertado (se ve subrayado)|

## $\textcolor{blue}{\textsf{A3 Caza los errores}}$
```
<html>
<head>
<title>Mi tienda de gadgets
</head>
<body>
<h1>Ofertas de otoño</h2>
<p>Auriculares con <b>cancelación de ruido</p></b>
</body>
</html>
```
1- Falta cerrar la etiqueta de `<title>` con `</title>`
2- La etiqueta de `<h1>` se cierra incorrectamente con `</h2>` cuando deberia cerrarse con `<h1>`
3- La etiqueta `<p>` se cierra antes que la `<b>`
4- La etiqueta `<b>` esta colocado despues de `</p>`. Deberia ir antes
5- La etiqueta `<head>` esta mal colocada por que `<title>` no esta cerrado antes.

```

<!DOCTYPE html>
<html>
<head>
    <title>Mi tienda de gadgets</title>
</head>
<body>
    <h1>Ofertas de otoño</h1>
    <p>Auriculares con <b>cancelación de ruido</b></p>
</body>
</html>
```

## $\textcolor{red}{\textsf{A4 Estilos rotos}}$
```
<h1 style="color:red font-size:40px;">Directo esta noche</h1>
<p style="text-align=center;">Estreno de temporada</p>
<p style="background-color:yellow;">Sorteo de una tarjeta gráfica<p>
```
1era Linea falta un `;` entre las dos propiedades `CSS:color y font-size`.
Codigo corregido
```
<h1 style="color:red; font-size:40px;">Directo esta noche</h1>
```
2nda Linea se utiliza el signo `=` para asignar el valor de la propiedad.
Codigo corregido
```
<p style="text-align:center;">Estreno de temporada</p>
```
3era Linea la etiqueta `<p>` esta mal cerrada, deberia cerrarse con `</p>`
```
<p style="background-color:yellow;">Sorteo de una tarjeta gráfica</p>
```
## $\textcolor{green}{\textsf{A5 Comentarios y anidación}}$

```
<!- Revisar el texto antes de publicar ->
<p>Tu contraseña debe tener <strong><em>al menos 12
caracteres</strong></em>.</p>
```
1era Linea deberia comenzar con `<!--` y terminar con `--->`
Corregido
```
<!-- Revisar el texto antes de publicar -->
```
2nda Linea las etiquetas deberian cerrarse en orden inverso al que se abren, es decir, primero se abre `<strong>`
y despues `<em>`, asi que deberia cerrarse primero `</em>` y despues `</strong>`
(extra, para ver la letra ñ se deberia poner la linea `<meta charset="UTF-8">`)
Corregido
```
<strong><em>al menos 12 caracteres</em></strong>
```
Codigo Completo Corregido
```
<!-- Revisar el texto antes de publicar -->
<p>Tu contraseña debe tener <strong><em>al menos 12 caracteres</em></strong>.</p>
```

## $\textcolor{blue}{\textsf{A6 ¿Que vera el usuario?}}$
```
<h1>Resumen de la jornada</h1>
<p>Ha ganado el equipo local.<br>El rival se despide del torneo.</p>
<hr>
<h4>Próximo partido</h4>
<p>Sábado a las 18:00</p>
```
Deberia verse el titulo grande de `Resumen de la jornada`, despues seguiria el parrafo,con lineas separadas por `<br>` con las frases `Ha ganado el equipo local` y `El rival se despide del torneo`, depues `<hr>` nos creara una linea horizontal en todo el ancho de la página. Despues seguiremos con `Proximo partido` y `Sabado a las 18:00`. Todo el texto ocupara el ancho completo de la ventana, alineado a la izquierda, sobre fondo blanco con letra negra

<h1>Resumen de la jornada</h1>
<p>Ha ganado el equipo local.<br>El rival se despide del torneo.</p>
<hr>
<h4>Próximo partido</h4>
<p>Sábado a las 18:00</p>

# $\textcolor{orange}{\textsf{PARTE B EJERCICIOS GUIADOS}}$
En esta parte crearemos la plantilla.html y crearemos lo siguiente


```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="utf-8">
  <meta name="author" content="Tu nombre">
  <title>B2 - La noticia del día</title>
</head>
<body>

  <h1>¿La IA te quitará el trabajo?</h1>
  <h2>Los expertos aseguran que cambiará los empleos, pero no los eliminará todos</h2>

  <p>La inteligencia artificial ha pasado de ser ciencia ficción a estar en el móvil
  de todo el mundo en apenas dos años. Herramientas que redactan textos, generan
  imágenes y programan código están ya en las empresas.</p>

  <p>Los estudios más recientes coinciden en algo: los trabajos más rutinarios serán
  los más afectados, mientras que las tareas que requieren creatividad, trato
  humano o decisión ética seguirán necesitando personas.</p>

  <hr>

  <p>La clave, según los expertos, no será competir contra la IA sino aprender a
  usarla como herramienta. Quien sepa aprovecharla tendrá ventaja en el mercado
  laboral de los próximos años.</p>

  <br>
  Autor: Kevin Daniel Quizhpe
  <br>
  Fecha: 16 de noviembre de 2026
  <br>

  <h2>Prueba de tamaños</h2>
  <h1>Encabezado nivel 1</h1>
  <h2>Encabezado nivel 2</h2>
  <h3>Encabezado nivel 3</h3>
  <h4>Encabezado nivel 4</h4>
  <h5>Encabezado nivel 5</h5>
  <h6>Encabezado nivel 6</h6>

</body>
</html>
```

# $\textcolor{springgreen}{\textsf{B3. Ficha de oferta Black Friday}}$

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="utf-8">
  <meta name="author" content="Kevin Daniel Quizhpe Inga">
  <title>B3 - Oferta Black Friday</title>
</head>
<body>
  <!--
  PREGUNTA: ¿qué diferencia visual hay entre <b> y <strong>? ¿Y entre <i> y <em>?
  RESPUESTA: visualmente casi ninguna, <b> y <strong> salen en negrita y <i> y <em>
  en cursiva. La diferencia real es el significado: <strong> y <em> marcan
  IMPORTANCIA o énfasis (los lectores de pantalla lo pronuncian distinto y los
  buscadores lo entienden), mientras que <b> y <i> son solo apariencia, para
  destacar visualmente sin dar más peso al texto (por ejemplo nombres de barcos
  en cursiva, o palabras clave en negrita). Existen dos versiones por eso:
  una semántica (strong/em) y una puramente visual (b/i).
  -->

  <h1>Black Friday en GadgetZone</h1>
  <hr>

  <h2>Smartphone Galaxia Ultra 5G</h2>
  <p>El móvil más potente de la gama, con pantalla de <b>6,7 pulgadas<sup>1</sup></b>
  y cámara de 108 megapíxeles<sup>2</sup>.</p>

  <p>Precio antiguo: <del>999 €</del> → Precio Black Friday: <ins><strong>699 €</strong></ins></p>

  <p>Disponible en colores <i>Titanio medianoche</i> y <i>Azul galaxia</i>.</p>

  <p><em>¡Solo hasta el lunes o hasta agotar existencias!</em></p>

  <p>Fórmula de la batería de litio: Li<sub>2</sub>CO<sub>3</sub>, con carga rápida
  de 45W.</p>

  <p><small>* Oferta válida solo para España. Los gastos de envío no están incluidos.
  Consulta las condiciones completas en nuestra web.</small></p>

  <p>Cámara con zoom óptico <u>5x sin pérdida de calidad</u>.</p>

  <hr>
  <p><small><sup>1</sup> Medidas en diagonal. <sup>2</sup> Resolución nominal del sensor.</small></p>
</body>
</html>
```

# $\textcolor{springgreen}{\textsf{B4. El banner del streamer}}$

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="utf-8">
  <meta name="author" content="Kevin Daniel Quizhpe Inga">
  <title>B4 - Banner del streamer</title>
</head>
<body>
  <h1 style="background-color:lightblue;">Directo esta noche</h1>

  <h2 style="text-align:center;">Estreno de temporada</h2>

  <h3 style="text-align:right; background-color:limegreen;">Sorteo especial</h3>

  <p style="color:red;">Recordad que el sorteo es solo para suscriptores.</p>

  <p style="color:blue;">¡Activad las campanitas para no perderos nada!</p>

  <p style="font-size:150%;">Empieza a las 22:00 ¡no lleguéis tarde!</p>
</body>
</html>
```
# $\textcolor{blue}{\textsf{B5. Paleta de colores de tu marca}}$

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="utf-8">
  <meta name="author" content="Kevin Daniel Quizhpe Inga">
  <title>B5 - Paleta de colores</title>
</head>
<body>
  <!--
  PARTE 3 (reflexión):
  rgb(0, 0, 255) significa: 0 de rojo, 0 de verde y el máximo (255) de azul,
  o sea AZUL PURO. La pantalla mezcla luz roja, verde y azul (por eso RGB)
  y cada canal va de 0 a 255.
  En hsl, el hue (matiz) es un círculo de 0 a 360 grados:
  - Rojo = hue 0 (también 360)
  - Verde = hue 120
  - Azul = hue 240
  -->

  <h2 style="color:red;">Titular 1 (nombre estándar)</h2>
  <h2 style="color:rgb(255, 0, 0);">Titular 2 (rgb)</h2>
  <h2 style="color:#ff0000;">Titular 3 (hex)</h2>
  <h2 style="color:hsl(0, 100%, 50%);">Titular 4 (hsl)</h2>

  <h2 style="color:orange;">Titular naranja (nombre)</h2>
  <h2 style="color:rgb(255, 165, 0);">Titular naranja (rgb)</h2>
  <h2 style="color:#ffa500;">Titular naranja (hex)</h2>
  <h2 style="color:hsl(39, 100%, 50%);">Titular naranja (hsl)</h2>

  <!-- PARTE 2: comprobada en pantalla, se ven IGUAL -->
  <h2 style="color:#3cb371;">Este hex es el nombre "mediumseagreen"</h2>
  <h2 style="color:rgb(238, 130, 238);">Este rgb es el hex #ee82ee ("violet")</h2>
</body>
</html>
```

# $\textcolor{orange}{\textsf{B6. Menú de ramen con tipografías de repuesto}}$

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="utf-8">
  <meta name="author" content="Kevin Daniel Quizhpe Inga">
  <title>B6 - Menú de ramen</title>
</head>
<body>
  <!--
  PREGUNTA: ¿por qué debe ser fácil de leer el tipo de letra de un sitio web?
  RESPUESTA: porque si el usuario tiene que hacer esfuerzo para leer, se cansa
  y se marcha. La legibilidad afecta directamente a cuánto tiempo pasa alguien
  en tu web y a si entiende la información. Por eso los cuerpos de texto usan
  fuentes simples (sans-serif normalmente) y se reservan las fuentes
  llamativas para títulos cortos.
  -->

  <h1 style="font-family: cursive;">Ramen Kyoto</h1>

  <p style="font-family: Arial, sans-serif;">El auténtico ramen japonés en tu barrio.
  Caldo 12 horas, fideos frescos y ingredientes de verdad.</p>

  <p style="font-family: 'Courier New', monospace;">
    Ramen clásico ............ 9,50 €<br>
    Ramen spicy .............. 10,50 €<br>
    Ramen veggie ............. 9,00 €
  </p>

  <p style="font-family: SuperFuenteGuay, fantasy;">Si tienes instalada
  SuperFuenteGuay verás esto raro; si no, el navegador pasa a la siguiente
  fuente de la lista (fantasy) y la página NO se rompe.</p>
</body>
</html>
```

# $\textcolor{blue}{\textsf{B7.Cartel de festival con span y bordes}}$

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="utf-8">
  <meta name="author" content="Kevin Daniel Quizhpe Inga">
  <title>B7 - Cartel del festival</title>
</head>
<body>
  <!--
  PREGUNTA: ¿qué diferencia hay entre <span> y <p> para destacar parte de un texto?
  RESPUESTA: <p> es un bloque, empieza en línea nueva y ocupa todo el ancho,
  mientras que <span> es en línea (inline): marca solo un trozo DENTRO del
  párrafo sin romper el flujo del texto. Para destacar unas palabras en medio
  de una frase se usa span, para estructurar párrafos enteros se usa p.
  -->

  <h1 style="border: 5px solid green;">Festival Sonora Night 2026</h1>

  <p style="border: 3px dotted blue;">Este sábado: conciertos, food trucks y zona chill hasta las 3 AM.</p>

  <p style="background-color: lightpink; border: 5px double red;">Entradas limitadas: ¡no te quedes sin la tuya!</p>

  <p>Actuarán <span style="color: blue; font-size: 200%;">Los Voltios</span>,
  <span style="color: green; font-size: 200%;">La Sofia Band</span> y muchos
  más artistas por confirmar.</p>
</body>
</html>
```

# $\textcolor{orange}{\textsf{B8. Etiquetas anidadas: el mensaje urgente}}$

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="utf-8">
  <meta name="author" content="Kevin Daniel Quizhpe Inga">
  <title>B8 - Mensaje urgente</title>
</head>
<body>
  <!--
  SECUENCIA DE CIERRE: </u></i></b>
  ¿Por qué? Por la regla LIFO (last in, first out): abrí <b> <i> <u>, así que
  la última en abrirse es <u> y por tanto la PRIMERA en cerrarse. Las etiquetas
  se cierran en orden inverso al que se abrieron, como muñecas rusas o como
  cuando te vistes: te pones camiseta, jersey y abrigo, y te quitas primero
  el abrigo.
  -->

  <p><b><i><u>ALERTA: se detectó un intento de phishing dirigido a nuestros usuarios. No abras ningún enlace sospechoso.</u></i></b></p>

  <!-- Versión MAL cerrada para probar qué hace el navegador: -->
  <p><b><i><u>Mensaje de prueba con cierre cruzado</b></i></u></p>
</body>
</html>

```



