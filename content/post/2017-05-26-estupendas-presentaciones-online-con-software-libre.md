---
id: 6096
title: Estupendas presentaciones online con software libre
date: 2017-05-26T09:05:16+00:00
author: Jorge Cortell
layout: post
guid: https://blog.cortell.net/es/?p=6096
permalink: /2017/05/26/estupendas-presentaciones-online-con-software-libre/
categories:
  - ¿Por qué no? ¿Utopías?
  - Copyfight
  - Free Software
  - Geek Fun
  - General
  - Hacking
  - Placeres de la vida
  - Sociedad y polí­tica
  - Technology
  - Technolust
---
Ha pasado ya tiempo desde que escribí un tutorial de _Compartir la riqueza – STW_, así que ya es hora de compartir algunos conocimientos prácticos (aunque sean básicos) más allá de la publicación de un enlace.

Durante años he tenido un proyecto en la lista "por hacer": crear presentaciones sin la necesidad de software dedicado, sea privativo (como PowerPoint o Keynote), o libre (como LibreOffice u OpenOffice). De esa manera podría evitar traer mi computadora a una conferencia, y no preocuparme acerca de qué sistema informático estará disponible en el auditorio. Mientras haya conexión a Internet o un puerto USB, puedo llevar una URL y un USB como copia de seguridad, y funcionará.

También quería una funcionalidad mínima como:

<li style="list-style-type: none">
  <ul>
    <li>
      Ser capaz de imprimir la presentación o exportarla a PDF
    </li>
    <li>
      Controles de teclado (incluida vista resumen)
    </li>
    <li>
      Barra de progreso
    </li>
    <li>
      Se ajusta a cualquier dispositivo
    </li>
    <li>
      Transiciones y efectos
    </li>
    <li>
      Reproducible en cualquier navegador sin la necesidad de ningún plug-in o software adicional
    </li>
    <li>
      Ventana del presentador con la siguiente diapositiva, notas y cuenta atrás
    </li>
    <li>
      Todo en un formato de archivo fácil de usar, como HTML o Markdown
    </li>
  </ul>
</li>

Por supuesto, tus deseos serán atendidos por los dioses del Software Libre. He aquí la librería JavaScript sin dependencias  [Reveal.js](https://github.com/hakimel/reveal.js) .Pero para hacer la presentación realmente impresionante, había algunas cosas más que necesitaba hacer, como incorporarla en mi flujo de trabajo de Git (para tener las ramas, versiones y todas esas ventajas git) y hospedarlo.

Déjame guiarte por el proceso, para que también puedas preparar presentation alucinantes en muy poco tiempo:

Primero, crea un nuevo repositorio en GitHub o GitLab (si no sabes lo que es, primero debes leer otros tutoriales). Para este tutorial, utilizaré GitHub, aunque en la oficina utilizamos Gitlab.

Da a tu presentación un nombre, como "MyPresentation".

Clónala en tu máquina local. Puedes utilizar la aplicación GUI (me gusta la nueva versión beta basada en Electron) o utilizar el CLI ("Terminal" para usuarios de Apple OSX):

 `git clone git@github.com: yourusername/MyPresentation.git`
  
[Nota obvia: sustituye "yourusername" por tu nombre de usuario]

Clona reveal.js en tu máquina local. Esta vez:
  
 `git clon git@github.com: hakimel/reveal.js.git` 

Ve al sistema de archivos ("Finder" en OSX), busca tu directorio ("Carpeta" en OSX) de trabajo Git y mueve (o copia) el contenido del directorio "reveal.js" a la carpeta "MyPresentation".

Modifica el archivo index.html. Aquí es donde va tu contenido de presentación y formato. Echa un vistazo al  [este detallado tutorial](https://github.com/hakimel/reveal.js) .

Una vez hecho esto, "sube" el proyecto modificado a tu Git. Si utilizas la CLI:
  
 `git push` 

Si quieres usa Grunt para servir dinámicamente en local. Algunas personas incluso utilizan generator-reveal, un generador Yeoman, para que cada diapositiva sea un archivo HTML o Markdown individual.

Si estás utilizando GitHub, ahora, "automágicamente", tus diapositivas se publican en yourusername.github.io/MyPresentation

Un detalle más: si deseas acceder a los diapositivas en sí (para una presentación remota o alojada) en lugar del "repo" (repositorio de todos los archivos que acabas de "subir"), tienes que ir a GitHub y activar "GitHub pages" en este repositorio en particular. Simplemente ve a la página index.html del repositorio en GitHub y selecciona el ícono de menú de flecha abajo en la parte superior derecha (junto a "insights") "settings > pages" y activa las páginas de GitHub para ese repo.

Además, hay muchos plug-ins que puedes usar con reveal.js, como  [kreator](https://github.com/hakimel/reveal.js/wiki/Plugins,-Tools-and-Hardware) . ¡A disfrutar!