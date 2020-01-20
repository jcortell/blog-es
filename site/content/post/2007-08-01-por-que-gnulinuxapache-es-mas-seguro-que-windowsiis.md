---
id: 911
title: Por qué GNULinux+Apache es más seguro que Windows+IIS
date: 2007-08-01T13:00:29+00:00
author: Jorge Cortell
layout: post
guid: http://www.cortell.net/2007/08/01/por-que-gnulinuxapache-es-mas-seguro-que-windowsiis/
permalink: /2007/08/01/por-que-gnulinuxapache-es-mas-seguro-que-windowsiis/
categories:
  - CiberDerechos
  - Copyfight
  - Free Software
  - General
  - Noticias
  - Rants
  - Technology
---
Por si alguien lo dudaba, aquí­ podemos ver gráficamente por qué GNULinux+Apache es más seguro que Windows+IIS. Es una cuestión de complejidad (los gráficos representan las llamadas que hace el sistema al servir una página HTML con una imagen).
  
En la primera vemos GNULinux+Apache:

<a target="_blank" title="Zoom" href="http://blogs.zdnet.com/images/SysCallApache.jpg"><img alt="GNULinux+Apache" title="GNULinux+Apache" src="http://blogs.zdnet.com/images/SysCallApachesmall.jpg" /></a>

En la segunda Windows+IIS:

<a target="_blank" title="Zoom" href="http://blogs.zdnet.com/images/SysCallIIS.jpg"><img alt="Windows+IIS" title="Windows+IIS" src="http://blogs.zdnet.com/images/SysCallIISsmall.jpg" /></a>

Fuente: <a target="_blank" title="artí­culo" href="http://blogs.zdnet.com/threatchaos/?p=311">ZDNet</a>

Y por si te quedan dudas, Google ha publicado un estudio de 80 millones de servidores de dominio que demuestra que hay el doble de posibilidades de que un malware venga de IIS que de Apache: el 49% de los servidores de malware son IIS â€”el mismo porcentaje que Apache. ("Otros": 2%.) Pero en total sólo el 23% de los servidores web analizados son IIS comparado con el 66% de Apache. O sea, un total de (49% contra 23%).
  
Fuente: <a target="_blank" title="Google" href="http://googleonlinesecurity.blogspot.com/2007/06/web-server-software-and-malware.html">Google</a>