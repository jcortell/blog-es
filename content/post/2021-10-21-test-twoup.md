---
author: ""
date: "2021-10-21T04:00:24+02:00"
draft: false
title: "Probando Two-Up en Hugo"
tags: ["personal", "tecnología"]
images: "https://c0.wallpaperflare.com/preview/524/860/912/screen-code-coding-programming.jpg"
comments: false     # set false to hide Disqus comments
share: true        # set false to share buttons
thumbnailImagePosition: left
thumbnailImage: https://c0.wallpaperflare.com/preview/524/860/912/screen-code-coding-programming.jpg
coverImage: https://c0.wallpaperflare.com/preview/524/860/912/screen-code-coding-programming.jpg
metaAlignment: center
coverMeta: out
---

GoogleChromeLabs ha sacado un interesante componente para comparar dos elementos del DOM: [two-up](https://github.com/GoogleChromeLabs/two-up). Vamos a probarlo.

<!--more-->

Lo primero es hacer que [Hugo](https://gohugo.io) (el generador estático que empleo en este blog) renderice el HTML *inline* correctamente, lo cual se consigue añadiendo una plantilla de [shortcode](https://gohugo.io/templates/shortcode-templates/) para que inserte HTML en bruto dentro del *markdown* de la entrada (gracias por la idea, [Ana Ulin](https://anaulin.org/blog/hugo-raw-html-shortcode/)) simplemente añadiendo una plantilla de *shortcode* llamada `rawhtml.html` en `layouts/shortcodes/rawhtml.html` de tu instalación de Hugo. O sea, crea un documento HTML con ese nombre, en ese directorio, con este contenido:

`<!-- raw html -->
{{.Inner}}
`

Ahora ya sólo queda escribir el código HTML dentro de la entrada en *markdown* de Hugo empleando este *shortcode*:

`{{< rawhtml >}}
    Pon aquí tu HTML
{{< /rawhtml >}}
`

Y, para probar el Two-up, ¿cuál es el código HTML que hay que emplear (usando el JS externo)? ¡Muy sencillo!

`<script src="https://unpkg.com/two-up-element@1"></script>

<two-up>
  <div><img src="https://lh3.googleusercontent.com/t-t_jepUsuxueR9K1FIYOybuiefOriG6fCrxBJSHWs56dPvztmrcknPmkemzQSlr38T9HJC6LwOfaVD0yLmpaB0ydCLHqwv8jfaJ9V50OWNORczRJjgD5uoAt1VQZ1BWLX3ueEq3NeU=w1920-h1080" alt="before"></div>
  <div><img src="https://lh3.googleusercontent.com/DBgFrRegPOAmVbaDj_ecDZdn5nJ5B_YeTtj3YtO2gMMgPC5hIqk2m-fVfjWOPj7hG0-C7A6FxQcqILUSR0hM98uKuxwWJHA6mVGZEsgwqzeqLowftjeUnfNp10xS6bzQ7IDUoDl6Mq4=w1920-h1080" alt="after"></div>
  `

Perdón por las fotos, pero son las primeras que he encontrado en mi colección. Ahora imagina la de usos que le puedes dar (comparar niveles de compresión, modificaciones, versiones...):

{{< rawhtml >}}

<script src="https://unpkg.com/two-up-element@1"></script>

<two-up>
  <div><img src="https://lh3.googleusercontent.com/t-t_jepUsuxueR9K1FIYOybuiefOriG6fCrxBJSHWs56dPvztmrcknPmkemzQSlr38T9HJC6LwOfaVD0yLmpaB0ydCLHqwv8jfaJ9V50OWNORczRJjgD5uoAt1VQZ1BWLX3ueEq3NeU=w1920-h1080" alt="before"></div>
  <div><img src="https://lh3.googleusercontent.com/DBgFrRegPOAmVbaDj_ecDZdn5nJ5B_YeTtj3YtO2gMMgPC5hIqk2m-fVfjWOPj7hG0-C7A6FxQcqILUSR0hM98uKuxwWJHA6mVGZEsgwqzeqLowftjeUnfNp10xS6bzQ7IDUoDl6Mq4=w1920-h1080" alt="after"></div>
</two-up>

{{< /rawhtml >}}
