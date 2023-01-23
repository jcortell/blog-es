---
author: ""
date: "2020-02-02T01:00:24+02:00"
draft: false
title: "Procesando miles de archivos con un comando de terminal"
tags: ["tecnología", "trabajo", "geek"]
images: "https://p1.pxfuel.com/preview/595/744/913/monitor-screen-browser-computer.jpg"
comments: false     # set false to hide Disqus comments
share: true        # set false to share buttons
thumbnailImagePosition: left
thumbnailImage: https://p1.pxfuel.com/preview/595/744/913/monitor-screen-browser-computer.jpg
coverImage: https://p1.pxfuel.com/preview/595/744/913/monitor-screen-browser-computer.jpg
metaAlignment: center
coverMeta: out
---

¿Cómo solucionar un problema que afecta a más de dos mil archivos sin pasar días con un procesador de textos? CLI al rescate.

<!--more-->

Tener un *stack* JAM[^jam] con un generador de CMS[^cms] estático bajo control de versiones en Git con CI/CD[^cid] automatizado a través de un CDN[^cdn] global es excelente por muchas razones (velocidad, seguridad, escalabilidad ...) pero ¿qué sucede cuando una nueva versión decide cambiar qué letras son aceptadas en la compilación y cuáles se consideran inválidas? Entonces tienes un problema que en mi caso afecta a más de dos mil archivos.  

No tengo tanto dominio del CLI[^cli] como mis amigos Álvaro o Santiago. Pero me encanta aprender nuevos trucos y disfrutar del poder del terminal.

En este caso, tuve que localizar una cantidad de "letras ofensivas" (restos de una migración anterior del motor de blog, que manejaba la codificación de texto de manera diferente) en miles de archivos, y luego hacer un "reemplazo con" en todos ellos a la vez.

Esto es lo que monté gracias a los tutoriales de CLI Magic, Winaero, Linuxize y Maketecheasier:

Primero, identifique qué archivos estaban causando problemas. Después de todo, si solo fueran uno o dos, podría solucionarlo manualmente. Entonces ejecuto (en el directorio que contiene todas mis publicaciones de blog):

```
grep -iRl "&#"
```

Estos son los argumentos:
-i: ignora las mayúsculas
-R: búsqueda recursiva de archivos en subdirectorios
-l: muestra los nombres de archivo en lugar de las porciones de contenido del archivo

La razón por la que usé "& #" es porque la codificación del texto ofensivo siempre incluía esa cadena parcial.

Una vez que me di cuenta de que estábamos hablando de más de dos mil archivos, decidí usar el CLI para sustituir las cadenas ofensivas. No los enumeraré a todos, así que no revelaré pistas y vulnerabilidades, pero el comando general que utilicé es:

```
find . -type f -exec sed -i 's/&#8230;/.../g' {} +
```

Y, como por arte de magia, en un abrir y cerrar de ojos, todas las ocurrencias ofensivas de `&#8230;` se convierten en `...`.

Eso es, en esencia, lo que yace en el fondo del software moderno y la transformación de datos. Unix sigue tan brillante medio siglo después.

[^jam]: JavaScript, APIs, y Markup
[^cms]: SIstema de Gestión de Contenidos
[^cid]: Integración Contínua / Entrega Contínua
[^cdn]: Plataforma de Suministro de Contenidos
[^cli]: Interfaz de Línea de Comandos
