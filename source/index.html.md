---
title: Compendio de buenas prácticas SEO

language_tabs: # must be one of https://git.io/vQNgJ
  - html
  - javascript
  - php

toc_footers:
  - Para contribuir con este compendio 
  - enviar un email a 
  - bastian@mitocondria.cl

includes:
  - links

search: true
---

# Introducción

EL rol de este compendio es entregar directrices y guiar acerca de la buena construcción SEO para un sitio web, siendo este una guía elaborada en base a la investigación constante, al conocimiento colectivo, el estudio y debate del tema entre los participantes, y las propias experiencias de aquellos que han contribuido en mejorar el posicionamiento, la calidad y la optimización de nuestros sitios web en [Mitocondria](https://www.mitocondria.cl). 

Esta documentación esta escrita en Markdown utilizando el framework [Slate](https://github.com/lord/slate), sientete libre de explorar sus secciones y de contribuir, conversando con el equipo tu investigación y entregandola en el formato Markdown (MD) a [bastian@mitocondria.cl](mailto:bastian@mitocondria.cl).

# Cómo utilizar esta documentación

> Ejemplos de código:

```html
<img data-src="/wp-content/themes/mitocondria/assets/img/imagen_a.jpg" title="Testing" alt="Testing" />
```

```javascript
var mailto = 'bastian@mitocondria.cl';
jQuery(document).ready(function(){
    $('#inputMail').append('<a href="mailto:'+mailto+'">Enviar mail a Bastián: '+mailto+'</a>');
});
```

```php
<?php
$hola = 'Hola mundo';
echo $hola;
?>
```

> Algunos tips serán entregados en este sector.

Esta documentación tiene la posibilidad de adjuntar trozos de HTML, Javascript, PHP según sea el caso. así podremos ver ejemplos para cada ámbito, lo importante es ir destacando lo relevante, cada caso debe ser explicado detalladamente, la idea es resolver dudas de cualquier tipo, con el foco en SEO, con aspectos básicos de jerarquía de construcción, o hasta optimización de carga en server.


<aside class="notice">
Si tienes dudas o problemas con la documentación no olvides conversarlo con el equipo, recolectar investigación y presentarla de manera clara para poder debatir estos temas con fundamentación ya que este compendio no es solo una guía, si no una regla de cómo llevar a cabo las cosas.
</aside>

# Construcción

## Fundamentos SEO

Entendamos que el SEO (Search engine optimization) consta de dos partes que deben ser complemento para que todo vaya bien y los buscadores puedan indexar nuestros sitios con mejor valoración y obteniendo toda la data necesaria: nos referimos al **contenido** y a la **construcción de nuestro sitio web**.

De estos dos aspectos podríamos decir que el más importante es el contenido, ¡SI!, es lo más importante, debido a que ello es lo que vamos a posicionar, un sitio sin contenido, nunca ocupará un lugar en los buscadores, debido a que no entregará información relevante para los potenciales visitantes. Los contenidos deben ser **relevantes, originales, útiles, con apoyo de multimedia y respaldo de entidades o personas que tengan ingerencia en el tema**, bien dicho esto, nos enfocaremos y profundizaremos más adelante en esto, ya que por ahora nos centraremos en la construcción de nuestro sitio web.

Para ello vamos a pasar por lo más básico de un sitio web, hablamos del **HTML**, la base de todo sitio web.

Nuestro HTML debe ser jerárquico, debe estar construido y pensado para que cada página de nuestros sitios web cuente con la estructura necesaria para poder comenzar a poblarlo de contenidos, este debe poder soportar muchas variantes, desde un título en la etiqueta html correspondiente, imagenes con información en sus atributos, parrafos, columnas, meta datos, etc.

OK... *¿pero por qué?* 🤔

*Si, es una pregunta que todos nos podemos hacer en algún momento, ¿por qué no simplemente escribo mi HTML dentro de `<div>DIVS que sirven para todo</div>` y me olvido del tema?.*

<div class="tenor-gif-embed" data-postid="4515277" data-share-method="host" data-width="100%" data-aspect-ratio="1.5961538461538465"><a href="https://tenor.com/view/whynot-jimmy-fallon-shrug-idont-know-idk-gif-4515277">Why Not GIF</a> from <a href="https://tenor.com/search/whynot-gifs">Whynot GIFs</a></div>

¡Error! 😤

HTML es un lenguaje de etiquetas rico en distintas opciones semanticas que se puede adaptar perfectamente a nuestro contenido para poder hacerlo más expresivo no tan solo para el lector si no para las máquinas, ya que para que ellas puedan interpretar nuestros contenidos pueden apoyarse de esto, con etiquetas como:

`<strong> <meta> <img> <h1> <h2> <h3> <h4> <h5> <h6> <p> <header> <footer> <aside> <table> <article> <nav> <main> <address> <a> <sub> <sup> <video>` y muchas otras más que puedes encontrar [acá](https://developer.mozilla.org/en-US/docs/Web/HTML/Element).

Los buscadores entienden estas etiquetas y pueden estructurar la información que proviene se los sitios web. Si estas etiquetas son utilizadas correctamente, los buscadores entenderán de mejor manera que intentamos decirle a los usuarios.

## Estructura básica de un contenido HTML
> Ejemplo de estructura html válida:

```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width">
    <meta name="description" content="Escribiendo html semántico correctamente">
    <title>¿Cómo escribir una página html?</title>
  </head>
  <body>
    <article class="containerArticle">
      <h1>¿Cómo escribir una página html?</h1>
      <h2>Escribiendo html semántico correctamente</h2>
      <p>
        Phasellus luctus purus justo, in egestas ipsum interdum vitae. 
        Aliquam ultricies nisi et pulvinar imperdiet. Cras ac <strong>fermentum elit</strong>, 
        vel scelerisque lectus. Class aptent taciti sociosqu ad litora torquent per conubia nostra, 
        per inceptos himenaeos. Cras sit amet dui ut ante rhoncus vestibulum elementum eu tortor. 
      </p>
      <img src="/images/imagen1.jpg" alt="Imagen que muestra un trozo html" title="Trozo html" />
    </article>
  </body>
</html>
```

Toda página web debe al menos contar con estas etiquetas según sea el contenido que se presentará.

Etiqueta | Tipo | Valor
--------- | ------- | -----------
`<h1>` | Título | Toda página HTML debe tener una etiqueta `<h1>`y **SOLO UNA ÚNICAMENTE** ya que representa el título principal de la página, no debe ser el nombre del sitio, si no el título del contenido.
`<h2>` | Título | Esta etiqueta se utiliza para un título con segunda posición jerárquica en la página y debe existir también **SOLO UNA ÚNICAMENTE**.
`<h3>...<h6>`| Título | También es un título pero a diferencia de las anteriores si podemos utilizarlas más de una vez.
`<p>`| Párrafo | Nuestros contenidos deben estar insertos en etiquetas de tipo párrafo, ya que así los buscadores pueden entender que este es nuestro contenido relevante, separandolo de otros sectores del html que pueden hablar de tópicos y contextos completamente distintos.
`<strong>`| Negrita | Nuestros contenidos pueden ser destacados a través de esta etiqueta, es importante utilizarla y no solo con CSS destacar nuestra información, recordemos, **HTML semántico**.
`<img>`| Imagen | Esta etiqueta esta encargada de adjuntar imagenes, fotografías, recursos gráficos, etc. es de gran valor pero por si sola los buscadores no podrán entender que intenta decirnos, para eso deberemos contar con dos atributos estrictamente necesarios `alt` y `title`, siendo el texto alternativo en caso de que la imagen no pueda ser mostrada (por x motivo) y el título de nuestra imagen respectivamente.
`<meta>`| Meta datos | Puede ser utilizada con varios fines, pero esta no está inmersa dentro del contenido, si no que pertenece a la cabecera de nuestro HTML, dentro de `<head>` esta puede representar una descripción, datos para redes sociales, keywords, en fin, información acerca de nuestra data, más información [acá](https://www.w3schools.com/tags/tag_meta.asp).

Ya teniendo como mínimo estas simples etiquetas podremos entregarle información a los buscadores de una manera mucho más eficiente y correcta.

<aside class="warning">Existen algunas etiquetas HTML que pueden contener otras como un árbol, pero otras como los títulos no pueden contener párrafos dentro, este markup no es correcto acorde a la W3C.</aside>

## Frameworks CSS

Los Frameworks CSS son una buena herramienta para poder construir rápidamente un sitio web olvidandonos de normalizar nuestros estilos, dejandonos paso abierto a desarrollar lo importante, tipografías, columnas, grillas, formularios, etc. Esto lo sabemos de antemano por que siempre utilizamos alguno para comenzar algún proyecto, y es cierto, agiliza mucho nuestro trabajo y ahorra tiempo en nuestras destinadas en desarrollo que son innecesarias de invertir todo el tiempo. 

Siempre debemos pensar en ahorrar tiempo, para cada cosa que necesitemos hacer, debemos disponer del tiempo como un recurso valioso y fácilmente agotable, es por eso que los frameworks CSS son muy necesarios....¿ pero esta ahorrandole tiempo al usuario 🤔 ?

Pensemos que cada recurso que vamos a utilizar en nuestro sitio web, es un peso más en nuestro paquete de entregas a cliente. Cada elemento aporta con más peso a la petición de recursos hacia el servidor y esto se traduce en tiempos de descarga, mientras más se tarde el sitio en cargar, más impacto va a tener nuestro sitio web en un buen SEO ranking.

Los frameworks CSS son pesados, ya que tienen mucha información para hacerlo todo y en la mayoría de los casos, llegamos a utilizar a lo más el 30% de las prestaciones que nos ofrece, así que debemos ser cautos e utilizar lo que realmente vamos a necesitar de estos frameworks.

Si podemos nombrar frameworks que aprendieron de esto, podemos ver a Bootstrap, que te permite escoger si utilizar solo ciertos componentes y partes de su framework o usarlos por completo. Esto tiene un gran impacto en la velocidad, por que lo más probable es que solo quisieramos usar su grilla, y nosotros hacer a mano cada componente, cada formulario, botón o cualquier recurso gráfico.

## Frameworks JS

Los frameworks JS hoy en día en internet abundan, todos puedes hacer lo mismo o pueden tener focos distintos, Javascript hoy tiene un rol muy importante para todo lo que envuelve el desarrollo de sitios web, aplicaciones para Desktop, para internet, para mobile, para lo que sea. Pudiendo incluso ser utilizado fuera de un navegador (Node).

Si paramos a mirar la cantidad de frameworks que hoy existen para desarrollar aplicaciones web, probablemente nos vamos a perder si realmente no sabemos que queremos realizar, siendo un real dolor de cabeza escoger el que va a ser efectivo para nuestro cometido.

Pero sabiendo que vamos a construir un sitio web, un framework JS puede hecharnos abajo todo nuestro posible posicionamiento, *si....¡TODO!* 😱

<div class="tenor-gif-embed" data-postid="5546494" data-share-method="host" data-width="100%" data-aspect-ratio="1.4678899082568808"><a href="https://tenor.com/view/wat-what-monkey-wow-wtf-gif-5546494">Wat What GIF</a> from <a href="https://tenor.com/search/wat-gifs">Wat GIFs</a></div>

Si bien es cierto **algunos buscadores pueden interpretar Javascript**, no lo pueden hacer de manera tan efectiva como quisieramos, y como los frameworks modernos muchas veces se encargan de realizar mucho trabajo a nivel de como funciona el renderizado de un aplicación, siendo estos incluso los encargados de realizarlo por completo, lo hacen on the fly, dejando de lado el verdadero código fuente que van a explorar los buscadores, siendo este, inexistente para abrir paso a los Virtual DOMs, **por ende no son indexables**.

Supuestamente Google, Bing y Baidu pueden entender el HTML renderizado desde lado cliente, pero hasta que esta información no salga de boca de ellos, y mientras los FW actuales esten pensando en el renderizando en servidor de los DOMs generados por estos mismos, vamos a quedarnos con la idea de que no los realizan de forma correcta y dejar abierto el debate.

Es por eso que debemos tener cuidado y pensar en las desiciones ténicas que vamos a tomar según el verdadero cometido de nuestros proyectos, pensar siempre en todos los casos y como dato extra utilizar algun framework que haga también el trabajo de realizar [SSR](https://lemoncode.net/lemoncode-blog/2018/5/13/server-side-rendering-i-conceptos) ( server side rendering ).

<aside class="notice">
Como dice la introducción de este compendio, las técnicas utilizadas en esta documentación son fruta del estudio de Mitocondria y sus colaborados en estos ámbitos, si tienes información o novedades sobre estos puntos, demuestralos reuniendo la información necesaria y abre camino al debate, siempre es buen seguir actualizandonos 🤓.
</aside>

## Schemma.org

> Horarios con Schemma.org

```html
<!-- Markup sin Microdata -->


<h1>Disneyland Paris</h1>
<div>It's an amusement park in Marne-la-Vallée, near Paris, in France.</div>
<div>Hours: Mo-Fr 10am-7pm Sa 10am-22pm Su 10am-21pm</div>
<div>Entrance: with ticket</div>
<div>Currency accepted: Euro</div>
<div>Payment accepted: Cash, Credit Card</div>
<div>Website:
  <a href="http://www.disneylandparis.it/">www.disneylandparis.it</a>
</div>


<!-- Markup con Microdata -->


<div itemscope itemtype="http://schema.org/AmusementPark http://schema.org/TouristAttraction">
  <h1><span itemprop="name">Disneyland Paris</span></h1>
  <div>
    <span itemprop="description">It's an amusement park in Marne-la-Vallée, near Paris, in France and is the most visited theme park in all of France and Europe.</span>
  </div>
  <div>Hours: Mo-Fr 10am-7pm Sa 10am-22pm Su 10am-21pm
    <meta itemprop="openingHours" content="Mo-Fr 10:00-19:00"/>
    <meta itemprop="openingHours" content="Sa 10:00-22:00"/>
    <meta itemprop="openingHours" content="Su 10:00-21:00"/>
  </div>
  <div>
    <meta itemprop="isAccessibleForFree" content="false"/>Entrance: with ticket
  </div>
  <div>
    <meta itemprop="currenciesAccepted" content="EUR"/>Currency accepted: Euro
  </div>
  <div>
    <meta itemprop="paymentAccepted" content="Cash, Credit Card"/>Payment accepted: Cash, Credit Card
  </div>
  <div>Website:
    <a href="http://www.disneylandparis.it/" itemprop="url">www.disneylandparis.it</a>
  </div>
</div>
```

Schemma.org es una comunidad colaborativa, con la misión de entregar, crear,mantener y promocionar esquemas para la data estrcturada en internet, sitios web, emails y más.

La idea es ayudar a los buscadores a entender el contexto real de lo que intentan comunicar los sitios web extendiendo su vocabulario, por ejemplo, quisieramos ayudar a entender que una sección de un sitio web habla acerca de los horarios de funcionamiento de los locales físicos que posee, su número de telefono, su dirección, etc. Con Schemma.org podemos estructurar esta información colcando microdata para cada caso, así los buscadores comprenderían de que se trata ese contenido y lo sabrán guiar mejor.

Este proyecto esta fundado por Google, Microsoft, Yahoo y Yandex.

Para obtener más información y documentación de como realizar Microdata estructurada visitar el sitio web de [Schemma.org](https://schema.org/).

**¡Muy interesante y útil!**

<div class="tenor-gif-embed" data-postid="4540781" data-share-method="host" data-width="100%" data-aspect-ratio="1.456140350877193"><a href="https://tenor.com/view/batman-thinking-contemplating-pondering-chin-gif-4540781">Batman Thinking GIF</a> from <a href="https://tenor.com/search/batman-gifs">Batman GIFs</a></div>

## Taskrunners

> gulpfile.js

```javascript
gulp.task('vendors-js', function() {
	return gulp.src([
    './vendors-js/bootstrap.bundle.min.js',
    './vendors-js/owlcarousel.min.js',
    './vendors-js/simple-lightbox.min.js',
    './vendors-js/countUp.min.js',
    './vendors-js/jquery.visible.min.js',
    './vendors-js/vanilla-tilt.min.js',
    './vendors-js/lazyload.min.js'
	])
	.pipe(concat('vendors-js.js'))
	.pipe(uglify())
	.pipe(gulp.dest('./dist/'));
});
```
Una buena herramienta para agilizar el trabajo son los ejecutores de tareas recurrentes, por ejemplo podemos trabajar el CSS de nuestro sitio web, y cada vez que realicemos cambios podemos hacer **minificación, concatenación y compresión de nuestras hojas de estilos**, y también podemos ver los cambios en el momento, sin necesidad de refrescar el navegador.

También podemos trabajar con Preprocesadores como LESS o SASS, esto agiliza aún más el desarrollo y la mantenibilidad de nuestro trabajo.

También podemos hacer *linting* de nuestros JS y alertarnos cuando cometamos algún error de script y nos puede ayudar a resolver el problema indicandonos algunas pistas de que puede estar pasando.

Hay muchas tareas que podemos llevar a cabo, ya que existen muchos plugins para los taskrunners, en el caso de **gulp** podemos encontrar una gran cantidad en el repositorio de [NPM](https://www.npmjs.com) (node package manager), pero debemos tener en cuenta que tenemos que tener instalado en nuestros computadores [NodeJS](https://nodejs.org/en/), NodeJS es un runtime javascript construido en base al motor javascript [V8](https://developers.google.com/v8/) de Chrome.


<aside class="success">Si deseas ver un ejemplo de Minificación y concatenación de archivos JS utilizando GULP, revisa la pestaña de <strong>Javascript</strong>.</aside>

## Minificar y concatenar

Minificar y concatenar es una tarea que siempre debemos tener en nuestra mente, debido a la importancia que hoy en día tienen la velocidad de los sitios web para los buscadores y la forma en que indexan, clasifican y rankean nuestros sitios web.

Todo esto se traduce en menos impacto de carga en el servidor, ya que minificar, concatenar y comprimir disminuye el peso de nuestros archivos y las llamadas a servidor. También puede ayudar a que el renderizado de la página sea mucho más rápido y eso da puntos al momento de que los buscadores indexen nuestros sitios con una mejor valorización en ranking.

## Orden de dependencias

Cuando hablamos de orden de dependencias no solamente hablamos del orden lógico de las cosas, OK...si, se nos enseña que lo común es que tengamos CSS y JS externos y locales en el header.

... Pero no 😤...
<div class="tenor-gif-embed" data-postid="12298561" data-share-method="host" data-width="100%" data-aspect-ratio="1.7647058823529411"><a href="https://tenor.com/view/shannon-sharpe-shay-nope-nah-nuhuh-gif-12298561">Shannon Sharpe Shay GIF</a> from <a href="https://tenor.com/search/shannonsharpe-gifs">Shannonsharpe GIFs</a></div>

Hay varias cosas que tomar en cuenta.

* El peso de nuestras dependencias.
* Que nuestras scripts se carguen una vez que las propias dependencias ya esten disponibles.
* Que nuestras dependencias puedan recurrir a sus propias dependencias ya cargadas.
* Que nuestras dependencias **no bloqueen el renderizado de nuestro sitio web**.
* Utilizar solamente lo necesario.
* No llamar mil dependencias si no las vamos a ocupar.
* No sobrecargarnos de plugins.
* Si ya no vamos a utilizar plugins no dejarlos cargados en caso de usarlos en futuro, si no se necesitan... **se eliminan**.
* **No repeternirnos a nosotros mismos**.
* Utilizar las versiones minificadas de nuestras dependencias.

Pero no solamente eso...

Hay algunas dependencias como lo es el caso de *Bootstrap*, que es mejor **no llamarlas como hoja externa**, si no que dejarlo escrito **directamente en el html**, pare ser más específicos, en el **header de nuestro sitio**.

Espera...
<div class="tenor-gif-embed" data-postid="4246579" data-share-method="host" data-width="100%" data-aspect-ratio="1.9753086419753088"><a href="https://tenor.com/view/wut-himym-barneystinson-neilpatrickharris-what-gif-4246579">Wut GIF</a> from <a href="https://tenor.com/search/wut-gifs">Wut GIFs</a></div>

¡Sí!

La razón es que **Bootstrap** es una librería muy grande, incluso si solo utilizamos un par de componentes del mismo, entonces, al ser Bootstrap nuestra librería de grilla, al ser llamada externamente debemos esperar a que este listo y descargado para poder utilizarle, por ende más tiempo le toma a renderizar el contenido correctamente. Y al tomarse más tiempo, algunos buscadores como Google toman esta variable para puntuar y rankear nuestros sitios web, podemos fijarnos en una de las herramientas que Google nos provee: **[Pagespeed](https://developers.google.com/speed/pagespeed/insights/)**, aquí podemos ver muchas posibilidades para poder optimizar nuestro sitio web, pero vamos a profundizar en este tema más [adelante](#pagespeed).

Entonces, al disponer esta librería directamente en el html, este no será problema de carga externa, ni tendrá impacto en server, por ende es una gran ayuda en el ambito de la velocidad y renderizado de nuestro sitio web, este experimento fue descubierto acá en **Mitocondria**, puedes probarlo por tí mismo, es un gran tip.
<div class="tenor-gif-embed" data-postid="13216220" data-share-method="host" data-width="100%" data-aspect-ratio="1.7777777777777777"><a href="https://tenor.com/view/high-five-nailed-it-snow-white-gif-13216220">High Five Nailed GIF</a> from <a href="https://tenor.com/search/highfive-gifs">Highfive GIFs</a></div>

# Profundidad

Para que un sitio web tenga un buen ranking en los buscadores, este debe tener buenos contenidos, a su vez deben ser interesantes....OK eso ya lo sabemos 🤦‍♂️, pero debemos tener en cuenta que cada tópico que iremos contando en nuestros sitios web, aporta con SEO, ya que estamos ofreciendole contenido a nuestros visitantes, pero de nada sirve si nuestro contenido esta desparramado sin un orden lógico, es por eso que debemos tener **niveles**, para navegar nuestro sitio web debemos pensar en una arquitectura de información que posea un buen nivel de usabilidad e interacción.

## Niveles

Cuando hablamos de niveles debemos pensar en una piramide, en la cima encontramos a nuestro home, esta es nuestra puerta de entrada a todos los contenidos, categorías y secciones a los cuales podemos llegar, en la base tenemos cada post y cada página que termina nuestro ciclo. Lo importante es que a través de cada página podamos seguir interactuando con nuestro sitio web, sea donde nos encontremos no podemos perder el foco de navegación, esto sería muy perjudicial para nuestros visitantes, ya que si tenemos una navegación que dificulta su experiencia, lograremos desviar su atención e interés y puede que termine abandonando el sitio web prematuramente o incluso irse sin obtener la información que necesitaba.

Lo ideal en un sitio web es no tener más de tres clicks para poder llegar a la información que el usuario necesita, tres niveles de navegación son más que suficientes para cualquier interacción en un sitio web.

Un ejemplo:

* Home => Categoría => Post

* Home => Sección => Post

Mientras más contenidos y páginas tengamos en nuestro sitio web, siendo estos, originales, consisos, al grano, relevantes, interesantes, y lo que hemos venido hablando, mejor va a ser nuestra oportunidad de ser bien rankeados 💪.

## Breadcrumbs

Podemos hacer que la estructura de información sea aún más clara si disponemos de breadcrumbs al sitio, esto nos va a entregar una ruta visible de los niveles que fuimos explorando para llegar a nuestro destino. Nos entregan una mejor experencia de usuario, por tanto, también potencia el SEO de nuestro sitio web.

## One-Page

Los One-Page son sitios web que exploran todo su contenido en una sola página, lo cual en algunos casos es muy útil y tienden a tener un excelente acabado de diseño, rico en tablas, gráficos animados, ilustraciones animadas, exponiendo toda la información de forma que la experiencia de los usuarios sea muy buena, subdiviviendo todos sus contenidos en seccciones, y llamando la atención del visitante para que no se vaya sin al menos haber obtenido más información de la que un sitio común podría haber hecho.

El problema que radica en estos sitios, es que no poseen profundidad, es decir... una página para mostrarlo todo, eso nos trae el primer dilema:

*¿Voy a rankear un sitio completo, con todas sus palabras claves en una sola página?* 😩 

Eso, es muy dificil, pero si se puede lograr, algunos tips:

* Optimizar por sección
    - Palabras claves por cada una de estas secciones
    - Separar el html en `<section>` para poder lograr el cometido
    - Etiquetas `<h1>` para cada sección...eso significa más de 1 etiqueta y esta mal, pero bueno, así se penso, nada que hacer.
* Optimizar velocidad
* Contenidos realmente acertivos, y efectivos
* Analytics

Para más información revisa este [link](https://yoast.com/one-page-website-seo/).


# Homepage

Nuestro home como hablamos en el tópico anterior, es la parte principal de nuestra piramide, este ser un conductor de navegación para nuestros visitantes, es decir desde esta parte debemos dar caminos, poner rutas hacia los distintos contenidos, ¡ 🙌 pero HEY 🙌!  no debemos abusar, ya que si lo hacemos vamos a hacer un desorden, y eso no guía a nadie.

Si bien es la cabeza de nuestro sitio, nosotros no queremos realmente hacer SEO con nuestro home page (así como tampoco quisieramos posicionar la página de contacto 🤷‍♂️), lo realmente de posicionar son nuestros post o páginas internas, aquellas que hablen de un tópico específico, ya que será por lo que nos vayan a buscar nuestros visitantes, según las palabras claves que utilicemos dentro del mismo, debemos tomar en cuenta muchos factores relacionados con la intención e interacción del contenido que estamos generando. De nada sirve hablar un artículo completo sin un estudio del foco informativo de nuestro contenido y podemos irnos fácilmente por las ramas. Habiendo dicho esto, si debemos trabajar en un buen nivel de su finalidad real y convertirlo en un gran conductor de las páginas que realmente si queremos posicionar.

Por eso es importante fijar varios factores como un *must*: la velocidad, la experiencia de usuario y las redes sociales deben tomar buen papel aquí. Algunos puntos a destacar para mejorar esto es:

* Asegurarse de que el título de la página sea fácil de ver.
* Tener un logo reconocible en la esquina superior (ojalá a la izquierda).
* Tener un **call-to-action** que llame la atención
* Un menú correctamente estructurado en niveles.
* Proveer de OpenGraph y Twitter Cards para una correcta disposición de la información al momento de compartirla en redes sociales.
* No abusar de links en la página, ni el Footer.
* Disponer información de contacto.
* Si aplica, disponer un buscador.

# Optimización de carga

```javascript
<script src="demo_async.js" async></script>
```
Optimizar la carga de nuestro sitio web es algo demasiado importante como para dejarlo pasar así como así, *Mitocondria* tiene el deber de entregar sitios con un alto grado de optimización, hoy en día es uno de los factores más relevantes a la hora de construir un sitio, ¿la razón?, **Mobile**.

No es necesario nombrar que la proliferación hoy en día de el uso de smartphones es inmensa, incluso llegando a frases y movimientos como el "*mobile first*". Ecommerces, Sitios web, Web apps, etc. todos deben empezar a contar con una adaptación hacia mobile. Los smartphones y tablets han sobrepasado el uso de la itnernet versus desktop, desde el 2016.

Como nuestros dispositivos mobile funcionan con conexión a internet mobile, este se ve afectada por distintos factores que influyen en una buena experiencia, lo primero, es tener conexión, y no en todos lados vamos a tener una buena calidad de conexión, incluso hoy que tenemos muchas redes, y la otra es la velocidad de conexión que tienen niveles según la disponibilidad, en Chile estamos en 4G y 4G+ y [vamos en camino a 5G](#bibliografia).

No vamos a hablar de estudios de cual es el impacto de los smartphones en la actualidad de la internet, así que pasemos a alunos tips para optimizar la carga de nuestros sitios web desde la perspectiva de los buscadores.

Google quiere que todos nuestros sitios sean muy rápidos, cómo lograrlo:

1- Optimizando nuestras dependencias
* Tamaño
* Entrega
* Utilidad
* Minificado
* Concatenado
* Si puedes hacerlo, que sean [*async*](https://www.w3schools.com/tags/att_script_async.asp)

2- Caché
Debes tratar de lograr que tu sitio utilice un buen nivel de caché, por que no es necesario que el servidor procese las peticiones que se lo soliciten, ejecutando scripts en backend para entregar las páginas, utilizando un buen nivel de cache, puedes dejar las páginas estáticas generandolas una sola vez, eso reduce el impacto en servidor y puede entregar el contenido anuestros visitantes con mayor velocidad.

<aside class="notice">
Un buen plugin para cache en wordpress es <a href="https://cl.wordpress.org/plugins/wp-super-cache/" target="_blank">WP super cache</a>.
</aside>

3- Tamaño de imagenes
* Comprimir las imagenes con algún compresor como: Imageoptim, TinyPNG, Shortpixel.
* Tener las imagenes a un tamaño para que en pantalas retina se puedan apreciar bien.

4- Servidor de calidad

5- Comprimir la página web
* Minificar el html
* Concatenar el html
* Eliminar los comentarios html
* Eliminar los espacios dobles

6- Evitar errores de sintaxis

7- Revisar que todos los request sean validos y no existan links rotos

8- Evitar la sobre población de nodos en nuestro DOM

9- Evitar la sobre carga de dependencias JS y CSS (máximo 5 o 6 por cada uno)

10- Utilizar un CDN para entregar todo lo que puedas.
* Pueden proveer de cache
* Pueden proveer la carga de las imagenes aislando ese trabajo del servidor
* Pueden proveer de seguridad anti-hacking anti DDoS
* Aumentan la performance de nuestros sitios web
* Pueden proliferar nuestro sitio web por varios servidores en el mundo, acelerando así el proceso de entrega a nuestros visitantes.

<aside class="notice">
Uno de los CDN que utilizamos acá en Mitocondria es <a href="https://www.cloudflare.cl">Cloudflare</a>.
</aside>

Puede ser complicado en algún momento, e incluso puede ser muy trabajoso lograr optimizar una sitio web, si lo haces bien, Google te lo recompensará.

<div class="tenor-gif-embed" data-postid="10657915" data-share-method="host" data-width="100%" data-aspect-ratio="1.7857142857142858"><a href="https://tenor.com/view/leonardo-dicaprio-cheers-gif-10657915">Leonardo Dicaprio Cheers GIF</a> from <a href="https://tenor.com/search/leonardodicaprio-gifs">Leonardodicaprio GIFs</a></div>


# Pagespeed

[Pagespeed](https://developers.google.com/speed/pagespeed) es la herramienta de Google la cual nos va a dar dolores de cabeza, pero nos va a dar todas las pautas para tener un sitio realmente optimizado y con un buen nivel de SEO si llegamos a seguir todas sus reglas, cuenta con una auditoría realmente muy completa, analizando aspectos desde:

* Renderizado
* Carga de imagenes
* Render Blocking
* Interactividad
* Latencia
* Timing
* Diagnósticos

Esto es solo la punta del iceberg, dado que la herramienta no solo analiza el impacto en desktop si no que también en mobile, y es mucho más severo y estricto el análisis que nos ofrece, es importante saber esto no es trabajo fácil, y que nos va a llevar mucho tiempo, trabajo y estudio lograr un buen puntaje para ambos dispositivos, hay que estudiar bien cada punto por que la velocidad para Google es un punto...muy importante.

<aside class="success">Un buen plugin para Wordpress que resuelve muchos de pagespeed es <a href="https://wordpress.org/plugins/psn-pagespeed-ninja/" target="_blank"> Pagespeed ninja</a>, pero ojo, <strong>desactivar rápidamente la compresión de imagenes</strong>, debido a que esta teniendo problemas y deja las imagenes en blanco, lo demás es ensayo y error, pero si quieries basarte en configuraciones ya probadas, intenta con la del sitio de Mitocondria, también lo tiene 😉.</aside>


<div class="tenor-gif-embed" data-postid="3512096" data-share-method="host" data-width="100%" data-aspect-ratio="1.6666666666666667"><a href="https://tenor.com/view/typing-jim-carey-funny-workhard-gif-3512096">Working Hard GIF</a> from <a href="https://tenor.com/search/typing-gifs">Typing GIFs</a></div>

# Saludos

Espero hayan podido resolver algunas dudas, esta primera primera versión abarca todo lo que he podido ir aprendiendo en el camino, como podrán saber, todo esto a sido frutp de la investigación constante en estos puntos, de la ayuda que hemos tenido entre todos y de las ganas de seguir aprendiendo.

Bastián Hidalgo

# Versiones
Fecha | Versión | Autor
---------- | ------- | -------
10-01-2019 | 1era versión | Bastián Hidalgo, [bastian@mitocondria.cl](mailto:bastian@mitocondria.cl).

<script type="text/javascript" async src="https://tenor.com/embed.js"></script>