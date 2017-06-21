---
id: 4013
title: Is your Mac infected? Find out (and fix it if it is)!
date: 2012-04-06T17:05:06+00:00
author: Jorge Cortell
layout: post
guid: http://cortell.net/blog/?p=4013
permalink: /2012/04/06/is-your-mac-infected-find-out-and-fix-it-if-it-is/
wpsd_autopost:
  - "1"
categories:
  - Geek Fun
  - General
  - Hacking
  - Noticias
  - Technology
---
<a title="http://arstechnica.com/apple/news/2012/04/flashback-trojan-reportedly-controls-half-a-million-macs-and-counting.ars" href="http://arstechnica.com/apple/news/2012/04/flashback-trojan-reportedly-controls-half-a-million-macs-and-counting.ars" target="_blank">Más de 600,000 Macs están infectados con el Troyano FlashBack Trojan</a>. ¿Es el tuyo uno de ellos? Vamos a ver lo.

Abre el Terminal (venga, no seas vago, sé un hacker) y escribe:

<pre>defaults read /Applications/Safari.app/Contents/Info LSEnvironment</pre>

Si dice:

> `The domain/default pair of (/Applications/Safari.app/Contents/Info, LSEnvironment) does not exist`

significa que tu Mac por ahora va bien (de lo contrario <a title="https://www.f-secure.com/v-descs/trojan-downloader_osx_flashback_i.shtml" href="https://www.f-secure.com/v-descs/trojan-downloader_osx_flashback_i.shtml" target="_blank">ve aquí</a>). 

Luego escribe:

<pre>defaults read ~/.MacOSX/environment DYLD_INSERT_LIBRARIES</pre>

si dice:

> `The domain/default pair of (/Users/[your user name here]/.MacOSX/environment, DYLD_INSERT_LIBRARIES) does not exist`

significa que tu Mac no está infectado (de lo contrario ve aquí <a title="https://www.f-secure.com/v-descs/trojan-downloader_osx_flashback_i.shtml" href="https://www.f-secure.com/v-descs/trojan-downloader_osx_flashback_i.shtml" target="_blank">ve aquí</a>). 

Fuente FSecure via Ars <a title="http://arstechnica.com/apple/news/2012/04/flashback-trojan-reportedly-controls-half-a-million-macs-and-counting.ars" href="http://arstechnica.com/apple/news/2012/04/flashback-trojan-reportedly-controls-half-a-million-macs-and-counting.ars" target="_blank">Technica</a>.