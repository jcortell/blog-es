---
id: 3315
title: Anatomía de un hackeo newbie de bajo nivel con el navegador
date: 2011-07-19T15:05:27+00:00
author: Jorge Cortell
layout: post
guid: https://cortell.net/blog/?p=3315
permalink: /2011/07/19/anatomia-de-un-hackeo-newbie-de-bajo-nivel-con-el-navegador/
wpsd_autopost:
  - "1"
categories:
  - ¿Por qué no? ¿Utopías?
  - CiberDerechos
  - Copyfight
  - Geek Fun
  - General
  - Hacking
  - Personal
  - Propuestas equilibradoras
  - Rants
  - Sociedad y polí­tica
  - Technology
---
Me entristece que los DRM y las políticas de miras cerradas de algunas instituciones priven a los usuarios/clientes/ciudadanos de sus derechos. Pero no tenemos por qué quedarnos de brazos cruzados. Un ejemplo:

Estoy haciendo un curso online (institución y temática no vienen a cuento).
  
Por el motivo que sea (me imagino la desgastada colección de excusas que se suelen emplear en estos casos) la institución que me ofrece esta formación, no considera, pese a que haya pagado por ello, que la información en la que se basa el curso sea algo que yo quiera mantener para futura revisión y estudio. Por lo tanto el acceso y los materiales (principalmente vídeo) están disponibles temporalmente, en streaming, y con contraseña.
  
Esto es una injusta barrera, y genera unas restricciones y un estrés innecesarios, al tener que ceñirse a los límites (temporales, de formas de acceso, etc) que impone arbitrariamente la institución, en sí misma influenciada y presionada por entidades de gestión colectiva, grupos de presión, y demás parásitos de miras cortas.
  
Pero ¿qué hacer si quiero ver esos vídeos en mi reproductor portátil, el año que viene, en vez de tener que verlos este mes, y en mi ordenador?
  
Pues para el neófito no hay forma, para el experto hay mil formas. A mí se me ocurren algunas, y esta que os muestro es una de las más sencillas y que se puede hacer sin equipamiento externo. Simplemente con un navegador (en este caso Google Chrome, aunque se puede hacer con casi cualquier navegador, y en casi cualquier plataforma).

a) Navegar hasta la página del curso que contiene el/los recursos que queramos descargar. Generalmente un vídeo en  streaming o animación multimedia embutido.

b) Ir a "ver>opciones para desarrolladores>herramientas para desarrolladores". Esto nos abrirá un panel en la parte inferior de la ventana. Hacer click en "recursos".

c) Si la página es muy larga, el código es complicado, hay muchos recursos, está bien ofuscado, etc, lo más práctico y directo es emplear la búsqueda, y utilizar un término que nos destaque lo que buscamos por formato de archivo (.avi, .mp4, .flv, etc), por almacenamiento externo (amazon, youtube, etc), o por ser la palabra que aparece justo antes del recurso necesitado (en la captura de pantalla adjunta, yo buscaba un vídeo que estaba tras la palabra "collection").

<img class="aligncenter" src="https://farm7.static.flickr.com/6005/5954546312_4afe8f92bb_z.jpg" alt="screenshot" />

d) Copiamos la URL del recurso, e intentamos descargarla (botón derecho>guardar como, CURL en la consola/terminal, o cualquier programa de descarga específico, desde el más sencillo hasta jDownloader). En caso de no poder, analizar si requiere algún tipo de autorización adicional (no debería, si tenéis acceso a la página que lo muestra), restricción (¿vía cookies, IP, u otra?), etc.

e) A veces puede ir en un contenedor (Widget, via Java, etc). La señal de alarma de acceso a recurso no seguro de la esquina inferior derecha nos dará directamente el acceso al código que el contenedor pretende mostrar. En ese caso lo mejor es abrir el recurso en una ventana a parte (simplificaremos el análisis del código), y ¡a leer líneas! Pronto os daréis cuenta de que, por ejemplo, en un archivo XML aparece
  
`This XML file does not appear to have any style information associated with it. The document tree is shown below.<br />
<data><br />
<assetURL><br />
<![CDATA[<br />
https://`

f) Una vez descargado, asegurarse del formato, ya que por lo general hay que modificar el nombre del archivo (añadiendo .avi, .mp4, .flv, o lo que sea). ¡Y a disfrutar de tu libertad espacio-temporal!