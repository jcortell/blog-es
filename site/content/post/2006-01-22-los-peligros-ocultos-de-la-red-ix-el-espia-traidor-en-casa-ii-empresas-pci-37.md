---
id: 237
title: 'Los peligros ocultos de la Red IX: El espí­a traidor en casa II (empresas) (PC&amp;I 37)'
date: 2006-01-22T02:56:50+00:00
author: Jorge Cortell
layout: post
guid: http://www.cortell.net/2006/01/22/los-peligros-ocultos-de-la-red-ix-el-espia-traidor-en-casa-ii-empresas-pci-37/
permalink: /2006/01/22/los-peligros-ocultos-de-la-red-ix-el-espia-traidor-en-casa-ii-empresas-pci-37/
categories:
  - 'Artí­culos escritos para la revista PC&amp;I'
  - CiberDerechos
  - Copyfight
  - Free Software
  - General
  - Privacidad
  - Rants
---
Si el mes anterior [hablábamos](http://www.cortell.net/2006/01/05/los-peligros-ocultos-de-la-red-ix-el-espia-traidor-en-casa-i-gobiernos-pci-36/) del spyware distribuí­do o esponsorizado por gobiernos, en esta ocasión vamos a hablar del que distribuyen las empresas por iniciativa propia. Los ejemplos, por desgracia, son más abundantes de lo que a priori se podrí­a pensar veamos un par (hay docenas).

Microsoft fue la primera (que yo sepa), cómo no, en cometer este abuso, y que quedase suficientemente documentado. En verano de 2002, tal y como se denunció en la web BSDVault.net, en la Licencia de Usuario (EULA) de una actualización de seguridad de su Windows Media Player 6.4, decí­a: "Acepta que para proteger la integridad del contenido y software protegido por DRM ("Contenido Seguro"), Microsoft puede proporcionar actualizaciones de seguridad al Sistema Operativo que serán automáticamente instalados en su ordenador. Estas actualizaciones de seguridad eliminarán su capacidad de copiar y/o ejecutar Contenido Seguro y usar otro software en su ordenador. Si proporcionamos tal actualización de seguridad, haremos esfuerzos razonables por comunicarlo en una web".

O sea, que se autoasignan la potestad de entrar en tu ordenador, instalar lo que quieran, no permitirte emplear el software que quieras... y ni te avisarán, ni te darán la oportunidad de comprobar lo que han hecho, ni podrás negarte.

Pero lo que comenzó como un abuso, y que proliferó por la inconsciencia de usuarios ignorantes y confiados que aceptaban EULAS sin leerlas, y empleaban software privativo (y lleno de errores, lento, vulnerable, caro, etc) como si no hubiese otra alternativa, se ha convertido en actividades delictivas descaradas.

Un ejemplo reciente, famoso y bien documentado es el de Sony-BMG (Bertelsmann), la multinacional discográfica (aunque no es la única). Pese a que muchos habréis leido la noticia, pocos sabréis el alcance real de la misma. Permitidme resumirla:

Sony-BMG, como la mayorí­a de discográficas y suciedades de gestión, obsesionadas con la proliferación de copias de sus discos (que por cierto, son absoluta y completamente legales según la legislación española vigente), introdujo sistemas de Gestión de Restricciones Digitales (DRM) ya en 2003. Desde entonces emplea el MediaMax de SunnComm, que se instala en el ordenador sin permiso ni notificación, sin desistalador (o el cual no funciona), y que transmite información del ordenador del usuario a SunnComm pese a que en el EULA dice lo contrario. Y se instala aunque el EULA se rechace.

Pero no contentos con esto, a principios de noviembre de este mismo año se supo que Sony-BMG también empleaba la tecnologí­a XCP (el rootkit Aries.sys) de First4Internet, que hací­a lo mismo que el MediaMax, pero además era mucho más difí­cil de detectar y desinstalar, y causaba un agujero de seguridad que han aprovechado desde virus hasta hackers (incluso contra el sistema anti trampas del juego online World of Warcraft).

Ante el lógico revuelo mediático que esto causó, Sony-BMG retiró 52 discos (Ray Charles, Frank Sinatra, Louis Armstrong, Celine Dion, etc), y proporcionó un desinstalador. Parecí­a una buena reacción. Lo malo es que justificaban sus acciones ("lo venimos haciendo desde hace tiempo", "es normal", etc), sigue habiendo muchos discos en el mercado con esas tecnologí­as, y para conseguir el desinstalador hay que conectarse a tres webs, dar tus datos dos veces, aceptar que los usen para enviarte spam, y todo para un desinstalador que se ha demostrado que puede romperte el sistema y/o borrar tus datos del ordenador. Además han mentido pues aseguraron que el XCP no enviaba datos del usuario a Sony, y se ha demostrado que sí­ lo hace.

Computer Associates calificó esta tecnologí­a de Spyware y de Malware. El Fiscal General de Texas puso una denuncia a Sony-BMG en noviembre, y otro en diciembre, en la que pedí­a a Sony-BMG 100.000 dólares por cada vulneración de la ley (con 20 millones de Cds portando MediaMax y 2 millones con XCP eso podrí­a suponer miles de millones de dólares) más los costes del juicio e investigación. En California la Electronic Frontier Foundation les puso una denuncia similar, y una asociación de consumidores otra. Y tanto en el Congreso de EEUU como otros 12 estados están estudiando aprobar leyes anti-spyware como la de California.

Al final Sony-BMG ha decidido ofrecer un acuerdo a los consumidores (acuerdo que ha sido en principio aceptado por un juez de Nueva York) en el que ofrecen 7‘50 dólares y la descarga gratuita de uno de los 200 álbumes de su colección, o tres álbumes (en vez de dinero). Además se comprometen a dejar de fabricar CDs con esa tecnologí­a y a ofrecer a los afectados un desinstalador del DRM que funcione.

DirectRevenue ya fue condenado por instalar Spyware por el juez Robert Gettleman en Illinois (EEUU), bajo cargos de allanamiento, fraude al consumidor, negligencia, y manipulación informática. Esperemos que a todos los apuestan por este tipo de medidas (incluí­dos el Ministerio Español de Cultura, y la SGAE) la ley les ponga en su lugar y paguen por la desfachatez de abusar de la confianza de los consumidores y restringir nuestros derechos.

Lo curioso es que con la legislación española (y la norteamericana) en la mano, cualquier consumidor que se vea afectado por este abuso criminal de restricción de sus derechos no puede tomar medidas para contrarrestar sistemas como MediaMax, XCP, o Macrovision. La mera posesión de tecnologí­a que lo permitiese está penado en el Código Penal español con hasta 2 años de cárcel. Es más, la ingenierí­a inversa de ese spyware está prohibida, incluso para su investigación.

> Algo falla en la ley y en las grandes corporaciones: ni entienden la tecnologí­a ni les importan los derechos de los ciudadanos/consumidores. En vez de buscar nuevos modelos de negocio, pretenden aferrarse al pasado mediante leyes absolutamente abusivas y prácticas criminales. 

Pero aun hay algo que me preocupa más: existiendo muchí­simas alternativas libres (Software Libre como Linux y miles de programas más, y millones de discos libros y pelí­culas libres o bajo licencias menos restrictivas que el copyright como Creative Commons, etc) la mayorí­a de ciudadanos/consumidores sigen permitiendo abusos contra sus derechos fundamentales. **-¡Qué cara sale la ignorancia, la sumisión, y el inmovilismo! Moraleja: emplea herramientas libres, disfruta de contenidos libres, y no permitas que abusen de tus derechos -¡y además te cobren por ello!**

[<img src="http://tira.escomposlinux.org/ecol-227.png" alt="tira es.comp.os.linux" border="0" />](http://tira.escomposlinux.org)