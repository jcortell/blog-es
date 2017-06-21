---
id: 303
title: Cómo tumbar un servidor como el de la SGAE
date: 2006-02-24T14:42:41+00:00
author: Jorge Cortell
layout: post
guid: http://www.cortell.net/2006/02/24/como-tumbar-un-servidor-como-el-de-la-sgae/
permalink: /2006/02/24/como-tumbar-un-servidor-como-el-de-la-sgae/
categories:
  - CiberDerechos
  - Copyfight
  - General
  - Hacking
  - Noticias
---
Hace un mes hckrs.org propuso en KernelPanic una Ciberprotesta contra la SGAE.

No he querido comentarlo antes para que no se me acuse de &#8220;fomentar hostilidades&#8221; o nada parecido. Ya tengo bastante con el comentario de un abogado amigo mí­o &#8220;-¡Cómo <s>te atreves</s> se te ocurre llamar &#8220;mafia&#8221; a la SGAE!&#8221;, o con el de un periodista de una conocida radio &#8220;a mí­ me ha amenazado, pero a tí­ te partirán las piernas&#8221;. Así­ que lo dicho, la violencia es algo que ejercen &#8220;ellos&#8221;, no &#8220;nosotros&#8221; (lo pongo entre comillas porque parece que haya dos bandos, cuando todos somos lo mismo: seres humanos que necesitamos acceso a la cultura y que queremos que se fomente la creación de la misma, y lo poco que nos diferencia es el cómo hacer esto). Pero, eso no significa que la propuesta carezca de interés, aunque sea desde un punto de vista teórico.

Bueno, a lo que iba, el mensaje era el siguiente:

_Entre el 22 y el 27 de febrero de 2006, se llevará a cabo una nueva
  
versión del certamen musical más importante de habla hispana: el Festival
  
Internacional de la Canción de Viña del Mar.</p> 

Es una fiesta para la SGAE, con la que celebran el canon a modo de arancel
  
que nos han impuesto a todos en cada cd virgen que compramos, es por ello
  
que hay organizada una SENTADA VIRTUAL a modo de ciberprotesta contra la
  
página oficial de la SGAE.

-¿COMO PARTICIPO?

Es muy fácil, tán solo tienes que descomprir un programa y el se encargará
  
de todo, podrás hacer lo que tu quieras a la vez que protestas por una
  
buena causa

-¿CUANDO ES?

Es el dia 22 de febrero a las 20:00 y terminará a las 00:00</em>

[Nota: el certamen sigue en marcha 😉 ;-)]
  
_
  
-¿DONDE CONSIGO EL PROGRAMA?</p> 

La herramienta se encuentra en el siguiente link
  
http://www.hckrs.org/proyectosabiertos/Acomodador-SGAE.zip tambien puedes
  
encontrarla en cualquier red P2P como es eMule

-¿COMO SE USA?

Es muy sencillo, te descargas el programa &#8220;acomodador-SGAE.zip&#8221;, lo
  
descomprimes (es un archivo .zip) y abres con tu navegador la web
  
acomodador.html (viene dentro de la carpeta que has descomprimido), te
  
lees las instrucciones y advertencias para comprender todo correctamente,
  
y él solo se pondrá a recargar repetidas veces la página web de la SGAE
  
con objetivo de ralentizarla.

-¿FUNCIONA REALMENTE?

Piensa que al igual que tú miles de personas estarán haciendo multitud de
  
peticiones de recarga de la Web, con lo que la ralentización se multiplica

-¿ES DELITO?

Para nada, simplemente estamos visitando su página web muchas veces a la
  
vez, no estamos hackeando ni rompiendo nada, es un modo de protesta
  
pací­fica y ordenada</em>

[Nota.- En [esta entrevista](http://www.puntog.com.mx/2001/050101/REA050101-02.htm) al hacktivista Ricardo Domí­nguez se comenta la legalidad o no de este tipo de prupuestas]

_DESDE LA DIRECCií–N DE HCKRS.ORG PEDIMOS A LOS GRUPOS QUE COMPARTEN MATERIA NOS AYUDEN CON LA CIBERPROTESTA, REUNIENDO GENTE Y APORTANDO TODA LA INFORMACIí–N QUE CONSIDEREN NECESARIA&#8230; SE ADMITE CUALQUIER TIPO DE SUGERENCIA EN EL SIGUIENTE LINK:</p> 

<http://www.setbb.com/hckrs/viewtopic.php?t=31&mforum=hckrs>

Gracias por compartir vuestro tiempo
  
HCKRS.org</em>

A esto respondió Luis:

_be, sembla que volen fer una &#8220;protesta comode&#8221;, implicacions i discussions
  
a part, no he mirat el fitxer, pero suposo que es per windows, aixi que
  
aqui teniu com fer-ho amb el vostre ordinador 😉_

\# aptitude install privoxy
          
\# echo &#8220;forward-socks4a / localhost:9050 .&#8221; >> /etc/privoxy/config
            
[ millor si ho poseu dins la seccio 5.2, per tenir-ho ordenat&#8230;]

$ export http_proxy=localhost:8118
          
$ while [ : ] ; do wget -O /dev/null ; done

_aixo si, com ja he dit, tingueu en compte que aixo es com dir que es
  
participa en una manifestacio pq es parla per telefon amb algu que esta en
  
ella&#8230; 😉_

Ceritium, por su parte, propuso un scrip en bash:

`#!/bin/bash</p>
<p>mkdir SGAE<br />
while [ 1 ]<br />
do<br />
wget http://www.sgae.es/sgae.inm?selectedMenu=-1 -O /dev/null<br />
done`

Y Locovich propuso un [Acomodador en Javascript](http://locovich.webcindario.com).

Pues bien, se emplee un modo u otro (en el fondo lo mismo), esto es lo que harí­a falta para &#8220;conseguir el objetivo&#8221;, según un análisis de [LordEpsylon](http://www.setbb.com/hckrs/viewtopic.php?t=31&mforum=hckrs).

El cálculo sencillo de cuántas conexiones son necesarias para superar una tasa de transferencia de 5Gb (es la más normal en servidores como el de la SGAE) es el siguiente:

http://www.sgae.es ocupa aprox. 29 kb

29Kb x 3 frames de recarga son = 87 Kb

La recarga se produce cada 5 segundos que en 1 hora son = 720 recargas

87Kb x 720 recargas son = 62.640 Kb por persona (1hora)

En el perí­odo entre las 20:00 y las 00:00, suponiendo una media de 2 horas por persona (hay un porcentaje de gente dispuesta a permanecer las 4 horas para cubrir las carencias de los otros): 62.640 kb x 2 horas son = 125.280kb por persona (2 horas)

1 GB son = 1.048.576 Kb

por lo tanto 1.048.576 Kb x 5 son = 5.242.880 kb

5.242.880 kb / 125.280kb por persona (2 horas) son = 42 conexiones

10 Gb de transferencia serán por tanto 84 conexiones aprox.

A todo esto, Anarkogeek ha propuesto esta imagen para el evento:
  
![boicotsgae](http://www.labuenanoticia.com/files/boicotsgae_g.png)

Así­ que ahora ya lo sabéis. Cada cual que haga lo que crea que debe de hacer. Yo ya lo he hecho 😉