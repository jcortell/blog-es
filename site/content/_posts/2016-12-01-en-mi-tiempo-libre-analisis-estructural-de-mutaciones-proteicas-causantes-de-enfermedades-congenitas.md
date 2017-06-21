---
id: 5973
title: 'En mi tiempo libre: análisis estructural de mutaciones protéicas causantes de enfermedades congénitas'
date: 2016-12-01T09:22:51+00:00
author: Jorge Cortell
layout: post
guid: http://blog.cortell.net/es/?p=5973
permalink: /2016/12/01/en-mi-tiempo-libre-analisis-estructural-de-mutaciones-proteicas-causantes-de-enfermedades-congenitas/
categories:
  - ¿Por qué no? ¿Utopías?
  - Ciencias
  - Geek Fun
  - General
  - Hacking
  - Humor y curiosidades
  - Personal
  - Placeres de la vida
  - Technology
---
La mayoría de la gente que conozco no consideraría el análisis estructural de mutaciones protéicas causantes de enfermedades congénitas &#8220;diversión del tiempo libre&#8221;. Por otra parte, la mayoría de la gente que conozco no piensa que soy como la mayoría de la gente que conocen.

Esta semana soy un &#8220;padre soltero&#8221;, ya que mi esposa está de viaje. Con lo que mi tiempo libre ahora es casi inexistente. Sin embargo, la idea de transformar una Prolina en una Glicina en la posición 22 me intrigó, así que pasé unos minutos simulándolo. Esto es lo que descubrí:<section> 

### Método

La estructura 3D de mi proteína objetivo la obtuve de la base de datos UniProt empleando Reprof. La información estructural la obtuve del análisis de PDB: [3NIR](http://pdb.rcsb.org/pdb/explore/explore.do?structureId=3NIR). Las anotaciones las obtuuve de UniProt [CRAM_CRAAB](http://www.uniprot.org/uniprot/CRAM_CRAAB).</section> <section> 

### Amino Ácidos

Me interesaba la mutación de <span>una Prolina en una Glicina en la posición 22</span>.

La figura más abajo muestra la estructura esquemática del amino ácido original (izquierda) y mutante (derecha). El esqueleto, que es el mismo para cada amino ácido, se muestra de color rojo. La cadena lateral, única para cada amino ácido, de color negro.

![](http://www.cmbi.ru.nl/hope/static/images/aa/pro.jpg) muta a ![](http://www.cmbi.ru.nl/hope/static/images/aa/gly.jpg)

Cada amino ácido tiene su propio tamaño, carga, y valor de hidrofobicidad. El resíduo original y el mutante difieren en dichas propiedades: el resíduo mutante es más pequeño que el original, mientras que el original es más hidrofóbico que el mutante.</section> <section> 

### Variantes

Existe una mutación conocida a &#8220;S&#8221; en dicha posición, que difiere de la mutación que yo había simulado. El efecto de dicha variante está anotada como: _In isoform SI_.</section> <section> 

### Conservación

El resíduo original no se conserva en esta posición. Otro tipo de resíduo se observa más a menudo en esta posición en otras secuencias homólogas. Esto significa que otras proteínas homólogas existen con ese otro tipo de resíduo más que con el original de mi secuencia, pero el otro tipo de resíduo no es similar a mi mutación. Por lo tanto la mutación es probablemente patogénica.</section> <section> 

### Dominios

Este resíduo es parte de un dominio de interpro llamado: _Thionin [IPR001010](http://www.ebi.ac.uk/interpro/entry/IPR001010)_

El resíduo mutado está ubicado en la superficie de un dominio sin función conocida. El resíduo no parece estar en contacto con otros dominios con función conocida en la estructura definida. No obstante, el contacto con otras moléculas o dominios es posible y puede ser afectado por esta mutación.</section> <section> 

### Propiedades de Amino Ácido

El amino ácido original y el mutante difieren en tamaño. El resíduo mutante es más pequeño que el original. Esto causará una posible pérdida de interacciones externas.

La hidrofobia del original y el mutante también difieren. La mutación puede causar pérdida de interacciones hidrofóbicas con otras moléculas en la superficie de la proteína.</section> <section> 

### Imágenes

![](http://www.cmbi.ru.nl/hope/yasara/0fc26700-bbb3-4a1c-85a9-b6a3b0f5e997/22GLY_overview.png/)Vista general de la proteína en forma de diagrama de Richardson. La proteína está coloreada por elemento; α-hélice=azul, β-filamento = rojo, giro=verde, y bobina aleatoria=cián.

![](http://www.cmbi.ru.nl/hope/yasara/0fc26700-bbb3-4a1c-85a9-b6a3b0f5e997/22GLY_overview_grey.png/)

Aquí la proteína está coloreada en gris, la cadena lateral del resíduo mutado está coloreada magenta y se muestra como pequeñas bolas.

![](http://www.cmbi.ru.nl/hope/yasara/0fc26700-bbb3-4a1c-85a9-b6a3b0f5e997/22GLY_zoom.png/)

Vista cercana de la mutación. La proteína está coloreada gris, ambas cadenas (original y mutada) se muestran en verde y rojo respectivamente.

![](http://www.cmbi.ru.nl/hope/yasara/0fc26700-bbb3-4a1c-85a9-b6a3b0f5e997/22GLY_zoom2.png/)

Desde un ángulo diferente.

![](http://www.cmbi.ru.nl/hope/yasara/0fc26700-bbb3-4a1c-85a9-b6a3b0f5e997/22GLY_zoom3.png/)

Desde otro ángulo</section> <section> 

### Animado

![](http://www.cmbi.ru.nl/hope/yasara/6c11cb58-f112-43f9-9f7a-4d907c84c268/22GLY_turning.gif/)Animación rotatoria con mismo esquema de colores.

![](http://www.cmbi.ru.nl/hope/yasara/6c11cb58-f112-43f9-9f7a-4d907c84c268/22GLY_morphing.gif/)

Animación con mismo esquema de colores.</section> <section> 

### Cita

Protein structure analysis of mutations causing inheritable diseases. DOI: [10.1186/1471-2105-11-548.](http://dx.doi.org/10.1186/1471-2105-11-548) PubMed: [21059217](http://www.ncbi.nlm.nih.gov/pubmed/21059217)<a href="http://www.cmbi.ru.nl/hope/report/583f164001ca360009798abb/" target="_blank">.</a></section>