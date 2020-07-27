---
author: ""
date: "2020-01-02T18:54:24+02:00"
draft: false
title: "Horas de análisis de código para arreglar una errata"
tags: ["geek", "tecnología"]
images: "https://cdn.pixabay.com/photo/2016/11/18/00/32/programming-1833058_960_720.png"
comments: false     # set false to hide Disqus comments
share: true        # set false to share buttons
thumbnailImagePosition: right
thumbnailImage: https://cdn.pixabay.com/photo/2016/11/18/00/32/programming-1833058_960_720.png
coverImage: https://cdn.pixabay.com/photo/2016/11/18/00/32/programming-1833058_960_720.png
metaAlignment: center
coverMeta: out
---

Hace tiempo noté que cuando compartía las publicaciones de mi blog en las redes sociales, la imagen de la publicación no aparecía. Finalmente decidí investigarlo ... ¡no sabía en qué agujero negro me estaba metiendo!

<!--more-->

Para resumir una historia larga, y para que no sea demasiado técnica, mi blog está escrito usando varias tecnologías diferentes, la principal es [Hugo](https://gohugo.io/).

Hugo es un blog estático y generador de webs escrito en el lenguaje Go. Go es un lenguaje fundado por Google de tipeado estático. Hugo es el más rápido y no tiene dependencias como Octopress o Hexo. Estoy muy contento con él y con toda la configuración que he tenido durante años (control de versiones de Git en GitHub, implementación de Netlify, CDN Cloudinary, etc.).

Cuando comencé a investigar por qué cuando compartía las publicaciones de mi blog en las redes sociales, la imagen de la publicación no aparecía, TODOS los resultados de búsqueda que encontré apuntaban en la dirección del funcionamiento interno de Hugo. Cuanto más leía, más tenía que profundizar en su funcionamiento interno, lidiar con las Plantillas Parciales Internas y tener que revisar y volver a codificar y parchear muchos elementos de su estructura interna. Adelante, busca y verás. Es una locura. La mayoría de las publicaciones y tutoriales sobre el tema dicen que tienes que lidiar con el diseño base, parcial, meta, open graph, tarjeta Twitter y configuración.

Sugieren añadir y modificar código como este para Open Graph:

```javascript
<meta property="og:title" content="{{ .Title }}" />
<meta property="og:description" content="{{ with .Description }}{{ . }}{{ else }}{{if .IsPage}}{{ .Summary }}{{ else }}{{ with .Site.Params.description }}{{ . }}{{ end }}{{ end }}{{ end }}" />
<meta property="og:type" content="{{ if .IsPage }}article{{ else }}website{{ end }}" />
<meta property="og:url" content="{{ .Permalink }}" />
<meta property="og:image" content="{{ with .Param "lua.image" }}{{ .url | absURL }}{{ else }}{{ with .Site.Params.image }}{{ .url | absURL }}{{ end }}{{ end }}" />
{{ with .Site.Language }}<meta property="og:locale" content="{{ .Lang }}" />{{ end }}
{{ with .Site.Params.facebook.appid }}<meta property="fb:app_id" content="{{ . }}" />{{ end }}
```

O este para Twitter Card:

```javascript
<meta name="twitter:title" content="{{ .Title }}"/>
<meta name="twitter:description" content="{{ with .Description }}{{ . }}{{ else }}{{if .IsPage}}{{ .Summary }}{{ else }}{{ with .Site.Params.description }}{{ . }}{{ end }}{{ end }}{{ end -}}"/>
{{ if .IsHome -}}
  {{ if ge .Site.Params.image.width 300 -}}
<meta name="twitter:card" content="summary_large_image"/>
<meta name="twitter:image" content="{{ .Site.Params.image.url | absURL }}"/>
  {{- else -}}
<meta name="twitter:card" content="summary"/>
<meta name="twitter:image" content="{{ with .Site.Params.image }}{{ .url | absURL }}{{ else }}{{ with .Site.Params.logo }}{{ .url | absURL }}{{ end }}{{ end }}" />
  {{- end }}
{{- else -}}
  {{ if ge (.Param "lua.image.width") 300 -}}
<meta name="twitter:card" content="summary_large_image"/>
<meta name="twitter:image" content="{{ .Param "lua.image.url" | absURL }}"/>
  {{- else -}}
<meta name="twitter:card" content="summary"/>
<meta name="twitter:image" content="{{ with .Param "lua.image" }}{{ .url | absURL }}{{ else }}{{ with .Site.Params.logo }}{{ .url | absURL }}{{ end }}{{ end }}" />
  {{- end }}
{{- end }}
{{ with .Site.Params.twitter -}}
<meta name="twitter:site" content="@{{ .username }}"/>
{{- end }}
```

O estas metatags para la cabecera de HTML:

```javascript
<meta name="title" content="Page Title for Search Engines Results | Website Name" />
<meta name="description" content="Page Description for Search Engine Results" />
<meta property="og:title" content="Page Title for Facebook" />
<meta property="og:description" content="Page Description for Facebook" />
<meta property="og:image" content="https://www.sitename.com/image-for-facebook.png" />
<meta property="twitter:card" content="summary" />
<meta property="twitter:description" content="Page Description for Twitter." />
<meta property="twitter:title" content="Page Title for Twitter" />
<meta property="twitter:image" content="https://www.sitename.com/image-for-twitter.png" />
```

Mientras programaba, volvía a programar y parcheaba ... todo me pareció extraño y excesivo. Tenía que haber una mejor manera. La mayoría de las personas que usan Hugo para blogs no tienen el conocimiento técnico para hacer todo esto, sin embargo, no tienen el mismo problema con sus imágenes cuando comparten una publicación, por lo que tenía que ser otra cosa.

Efectivamente, cuando presté más atención a las estructuras y códigos de otras personas, y lo comparé con el mío, noté algo.

*Front matter* permite mantener los metadatos adjuntos a una instancia de un tipo de contenido, es decir, incrustado dentro de un archivo de contenido, y es una de las muchas características que le da fuerza a Hugo. Hugo permite agregar *front matter* en yaml, toml o json a sus archivos de contenido.

Noté que en mi *front matter*, en la línea 7, después de *title* y *tags* y antes de *comments*, tenía *image*, mientras que todos los demás tenían *images*. Una letra. Una errata de cuando configuré toda la estructura. ¿Podría ser eso?

Efectivamente, seguí adelante y lo probé en [FaceBook OpenGraph Debugger](https://developers.facebook.com/tools/debug/og/object/) y [Twitter Card Validator](https://cards- dev.twitter.com/validator).

Horas "invertidas" (nunca "desperdiciadas"). Una errata. Odio el código Me encanta el código.
