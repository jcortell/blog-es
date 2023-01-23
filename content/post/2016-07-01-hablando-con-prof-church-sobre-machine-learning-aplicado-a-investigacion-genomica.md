---
id: 5836
title: Hablando con Prof. Church sobre machine learning aplicado a investigación genómica
date: 2016-07-01T13:22:59+00:00
author: Jorge Cortell
layout: post
guid: https://blog.cortell.net/es/?p=5836
permalink: /2016/07/01/hablando-con-prof-church-sobre-machine-learning-aplicado-a-investigacion-genomica/
categories:
  - ¿Por qué no? ¿Utopías?
  - Ciencias
  - Geek Fun
  - General
  - Hacking
  - Personal
  - Placeres de la vida
---
Durante mi vuelo a Boston leí "Regenesis" el interesante libro de genómica del Profesor George Church, regalo de mi amigo el Dr. Raminderpal Singh.

<img class="aligncenter" src="https://c3.staticflickr.com/8/7288/27881551722_868f869297.jpg" alt="George, Raminder and Jorge 2016 Boston" width="500" height="375" />

El miércoles por la tarde tuve una conversación muy interesante en Boston con los dos. Ninguno de ellos necesita una introducción en el mundo de la genómica, pero para aquellos que no son del sector:

  * Raminder es vicepresidente en Eagle Genomics y Asesor en Kanteron Systems. Anteriormente fue Director de Estrategia de Medicina Genómica en IBM, donde fue responsable del proyecto Watson Genomics.
  * George es escritor, catedrático de Genética de la Facultad de Medicina de Harvard y profesor de Ciencias de la Salud y Tecnología de la Universidad de Harvard y el MIT. Su doctorado llevó a la primera secuencia del genoma y ha contribuido a casi todos los métodos de secuenciación de ADN de "nueva generación".

Ya que el trabajo del laboratorio de George gira en torno a chip de síntesis de ADN, la edición de genes, ingeniería de células madre, super-resolución, computación molecular, la materia oscura y temas similares, y puesto que él tiene estudiantes de doctorado de la Universidad de Harvard, MIT, Boston U., y Cambridge, durante la conversación no pude resistir la oportunidad y le pregunté sobre el descubrimiento computacional de novo de secuencias.

Es una idea que tuve hace un par de semanas mientras navegaba desde San Petersburgo a Helsinki: ¿y si aplicamos algoritmos de _machine learning_ (ya sea _Random Forests_ o Memoria Temporal Jerárquica), o mejor incluso computación cuántica, para buscar "motivos" (_motifs_) de secuencia (nucleótido o patrón de secuencia de aminoácidos) para ayudar a predecir y construir motivos estructurales (moléculas biológicas en forma de cadena)? Podríamos empezar con los relacionados con la unión y plegado, lo que podría conducir a un avance exponencial en el campo del almacenamiento de la información y la biología sintética. Pero eso sería sólo el principio. Las posibilidades y las consecuencias podrían ser mucho mayores. Sería desbordar el SFLD 😉

En esencia (ejemplo gráfico simple y chorra), facilitaría mucho pasar de:
  
<img class="aligncenter" src="https://upload.wikimedia.org/wikipedia/commons/thumb/5/5c/G-quadruplex.svg/400px-G-quadruplex.svg.png" width="400" height="240" />a:

<img class="aligncenter" src="https://upload.wikimedia.org/wikipedia/commons/a/aa/Telomer-structure.gif" width="400" height="348" />

Y no sólo describir, sino también entender y facilitar su aplicación en la ingeniería de novo.

Hay más de 100 programas de software que intentan conseguir esto de modo programático (MEME, EXTREME, AlignAce, Amadeus, CisModule, FIRE, Gibbs Motif Sampler, PhyloGibbs, SeSiMCMC, ChIPMunk, Weeder, SCOPE, MotifVoter, MProfiler…). _Weirauch et al._ evaluaron muchos de ellos en una comparativa en 2013. Pero lo que propongo es mucho más potente, versátil, y rápido que cualquier otra cosa que se haya hecho hasta ahora (que yo sepa).

Mencionó algunas de las investigaciones en las que su esposa (la Profesora de Harvard Ting Wu, a quien también conocí en Boston) participa actualmente sobre super-resolución de imagen para el plegamiento de la cromatina, y la conservación evolutiva, y me dijo "**tu idea es realmente interesante**".

> Realmente, por lo general me importa muy poco lo que otros piensan de mis ideas (soy un científico, valoro pruebas y datos, no "creencias" o "juicios"), pero personalmente admiro y respeto su trabajo, y estoy muy de acuerdo con sus puntos de vista , especialmente sobre el intercambio libre de conocimientos y la edición del genoma humano, por lo que su comentario me alegró el día y me animó a proseguir con esa hipótesis ... algún día. En este momento en mi tiempo libre estoy rediseñando una interfaz de múltiples flujos de datos de sensores para la NASA (pro-bono, no solicitado ... pero esa es mi idea de diversión!).