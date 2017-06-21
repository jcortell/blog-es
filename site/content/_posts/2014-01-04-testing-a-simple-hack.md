---
id: 5049
title: Testing a simple hack
date: 2014-01-04T14:51:25+00:00
author: Jorge Cortell
layout: post
guid: http://cortell.net/blog/?p=5049
permalink: /2014/01/04/testing-a-simple-hack/
categories:
  - Geek Fun
  - General
  - Hacking
  - Personal
  - Technology
---
Uso _qtranslate_ como plugin multi-idioma para mi blog. Es una estupenda solución, pero el problema es que cada vez que se actualiza Word Press, al autor del plugin le lleva días o incluso semanas actualizarlo.

Así que, cansado de esperar, he encontrado un _hack_ simple y rápido para la actualización a WP 3.8: edita en qtranslate.php

> define(&#8216;QT\_SUPPORTED\_WP_VERSION&#8217;, &#8216;3.8&#8217;);

De nada 😉