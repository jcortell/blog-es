---
id: 2077
title: Hackeando pantallas remotas
date: 2009-07-30T08:37:40+00:00
author: Jorge Cortell
layout: post
guid: http://cortell.net/blog/?p=2077
permalink: /2009/07/30/hackeando-pantallas-remotas/
categories:
  - Geek Fun
  - General
  - Hacking
  - Humor y curiosidades
  - Placeres de la vida
  - Technology
---
El otro día volví a ver _The Matrix_ por enésima vez. Y me gustó la cara que pone el Sr. Anderson cuando ve aparecer "Wake up Neo" en su monitor. Así que me puse a buscar, y esto es lo que encuentro que se puede hacer si te apetece jugar a Trinity con el usuario dormido de turno.

1. Lo primero es logearte como root remotamente de una de estas dos formas:

  * SSH (Trinity emplea SSH en _Matrix:Reloaded_) con un shell y encontrar un exploit local para conseguir privilegios de root
  * Emplear directamente un exploit remoto para conseguir un shell root

2. Ejecutar ‘ps aux | grep X‘ (sustituir "X" por "windowserver" si es un MacOSX, "x.org" o la versión que sea si es GNU/Linux, etc) para ver los procesos, y poder encontrar así el X server. Apuntar el PID (que correrá en /dev/tty1).

3. Kill el proceso del X, dejando el terminal en blanco (negro).

4. Ejecutar ‘echo "Wake up, Neo." > /dev/tty1‘.

5. Seguir así con el resto ("The Matrix has you", "Follow the white rabbit", "Knock knock", "You have been onwed", "Pillao" o cualquiera que te apetezca), ejecutando ‘clear > /dev/tty1‘ para limpiar la pantalla entre mensajes.

Se admiten sugerencias, correcciones, y mejoras. Incluso el enlace a un scrip, que seguro que ya existe.