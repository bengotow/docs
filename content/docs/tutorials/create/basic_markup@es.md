---
$title: Crea tu página AMP HTML
---

El siguiente marcado es un punto de partida o código estándar aceptable.
Cópialo y guárdalo en un archivo con extensión .html.

[sourcecode:html]
<!doctype html>
<html amp lang="es">
  <head>
    <meta charset="utf-8">
    <script async src="https://cdn.ampproject.org/v0.js"></script>
    <title>Hola, AMP</title>
    <link rel="canonical" href="http://example.ampproject.org/article-metadata.html" />
    <meta name="viewport" content="width=device-width,minimum-scale=1,initial-scale=1">
    <script type="application/ld+json">
      {
        "@context": "http://schema.org",
        "@type": "NewsArticle",
        "headline": "Open-source framework for publishing content",
        "datePublished": "2015-10-07T12:02:41Z",
        "image": [
          "logo.jpg"
        ]
      }
    </script>
    <style amp-boilerplate>body{-webkit-animation:-amp-start 8s steps(1,end) 0s 1 normal both;-moz-animation:-amp-start 8s steps(1,end) 0s 1 normal both;-ms-animation:-amp-start 8s steps(1,end) 0s 1 normal both;animation:-amp-start 8s steps(1,end) 0s 1 normal both}@-webkit-keyframes -amp-start{from{visibility:hidden}to{visibility:visible}}@-moz-keyframes -amp-start{from{visibility:hidden}to{visibility:visible}}@-ms-keyframes -amp-start{from{visibility:hidden}to{visibility:visible}}@-o-keyframes -amp-start{from{visibility:hidden}to{visibility:visible}}@keyframes -amp-start{from{visibility:hidden}to{visibility:visible}}</style><noscript><style amp-boilerplate>body{-webkit-animation:none;-moz-animation:none;-ms-animation:none;animation:none}</style></noscript>
  </head>
  <body>
    <h1>Bienvenido a la web móvil</h1>
  </body>
</html>
[/sourcecode]

El contenido del cuerpo, hasta ahora, es bastante sencillo. Sin embargo, hay mucho más código en la etiqueta `<head>` de la página que podría no ser evidente de inmediato. Analicemos el marcado obligatorio.

## Marcado obligatorio

Los documentos AMP HTML DEBEN:

  - Comenzar con el tipo de documento `<!doctype html>`.
  - Contener la etiqueta `<html ⚡>` en el nivel superior (también se acepta `<html amp>`).
  - Contener las etiquetas `<head>` y `<body>` (opcionales en HTML).
  - Contener la etiqueta `<meta charset="utf-8">` como el primer hijo de su etiqueta `<head>`.
  - Contener la etiqueta `<script async src="https://cdn.ampproject.org/v0.js"></script>` como el segundo hijo de su etiqueta `<head>` (esto incluye y carga la biblioteca AMP JS).
  - Contener una etiqueta `<link rel="canonical" href="$SOME_URL" />` en la etiqueta `<head>` orientada a la versión de HTML común del documento de AMP HTML o a sí misma si no existiera dicha versión de HTML.
  - Contener una etiqueta `<meta name="viewport" content="width=device-width,minimum-scale=1">` en la etiqueta `<head>`. También se recomienda incluir initial-scale=1.
  - Contener lo siguiente en su etiqueta `<head>`:
    `<style amp-boilerplate>body{-webkit-animation:-amp-start 8s steps(1,end) 0s 1 normal both;-moz-animation:-amp-start 8s steps(1,end) 0s 1 normal both;-ms-animation:-amp-start 8s steps(1,end) 0s 1 normal both;animation:-amp-start 8s steps(1,end) 0s 1 normal both}@-webkit-keyframes -amp-start{from{visibility:hidden}to{visibility:visible}}@-moz-keyframes -amp-start{from{visibility:hidden}to{visibility:visible}}@-ms-keyframes -amp-start{from{visibility:hidden}to{visibility:visible}}@-o-keyframes -amp-start{from{visibility:hidden}to{visibility:visible}}@keyframes -amp-start{from{visibility:hidden}to{visibility:visible}}</style><noscript><style amp-boilerplate>body{-webkit-animation:none;-moz-animation:none;-ms-animation:none;animation:none}</style></noscript>`

## Meta datos opcionales

Además de los requisitos básicos, en nuestro ejemplo también se incluye una definición Schema.org en el `<head>`, que no es un requisito estricto para AMP, pero es un requisito para poder distribuir tu contenido en determinados sitios. Por ejemplo, en la [demostración del carrusel de novedades sobre Búsqueda de Google (pruébalo en tu teléfono)](https://g.co/ampdemo).

Para obtener más información acerca de todos los metadatos que necesitarás en muchos otros entornos (por ejemplo, Twitter), [explora nuestros ejemplos](https://github.com/ampproject/amphtml/tree/master/examples/metadata-examples). Para obtener información específica sobre AMP en la Búsqueda de Google, consulta [Historias principales con AMP](https://developers.google.com/structured-data/carousels/top-stories).

<hr>

¡Buenas noticias! Eso es todo lo que necesitamos para crear nuestra primera página AMP, aunque por supuesto aún no hay demasiadas noticias respecto del `<body>`. En la próxima sección, veremos la manera de agregar componentes básicos, como imágenes, elementos de AMP personalizados, de dar estilo a tu página y de definir un diseño responsivo.

<a class="go-button button" href="/es/docs/tutorials/create/include_image.html">Continuar con el paso 2</a>