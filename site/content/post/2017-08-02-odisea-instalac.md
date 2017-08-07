---
author: ""
date: "2017-08-02T18:54:24+02:00"
draft: false
title: "Lecciones de una odisea de instalación de software"
tags: ["geek","FLOSS","personal"]
image: "https://farm5.staticflickr.com/4326/35919108670_f5e1f6b067_z.jpg"
comments: true     # set false to hide Disqus comments
share: true        # set false to share buttons
thumbnailImagePosition: left
thumbnailImage: //farm5.staticflickr.com/4326/35919108670_f5e1f6b067_z.jpg
coverImage: //farm5.staticflickr.com/4326/35919108670_f5e1f6b067_z.jpg
metaAlignment: center
coverMeta: out
---
Vamos a instalar un nuevo sistema operativo GNU / Linux en dos ordenadores viejos para darles una nueva vida. Después de todo, ¿qué podría salir mal? ...

<!--more-->

En mi empresa siempre estamos utilizando diferentes ordenadores, dispositivos y sistemas operativos para probar escenarios, UX y alternativas. Así que cuando uno de los desarrolladores dijo: "Necesito una máquina con Ubuntu Server LTS para probar una nueva característica", le dije, "¿por qué no usar este viejo MacPro 1,1 que está en un rincón recogiendo polvo?".

Todo el mundo parecía estar de acuerdo con la idea, y ya que lo sugerí yo y todo el mundo sabe que me gusta 'trastear' con las máquinas ... me encargaron esa la responsabilidad.

"Ya que estoy haciendo esto, también podría actualizar el viejo iMac que también tenemos por ahí", pensé. Después de todo, he instalado sistemas GNU / Linux un montón de veces, y aunque en el pasado solía ser un desafío, en los últimos años se ha vuelto cada vez más fácil hasta el punto de ser un placer aburrido.

Pero no tenía IDEA de en lo que me estaba metiendo.

Primero probé el iMac. Voy a tratar de resumir una historia muy larga, enumerando los pasos de locura, los errores y las lecciones aprendidas:

1. Llave USB con el instalador no reconocida. ¿Podría ser la llave? Hagamos otra.
2. La llave del USB no arrancable. Vaya, error mío, hagamos otra.
3. La llave del USB no reconocida ... hmmm, esto es extraño. Tal vez sea el puerto USB, vamos a comprobarlo.
4. No se reconoce el instalador. ¿Ahora qué? Oh, veo en los registros que el cargador de arranque (*bootloader*) antiguo del iMac no arrancará desde USB para un instalador que no sea de OSX. Bueno, ojalá supiera eso antes. Intentemos con un CD.
5. CD no legible. Bueno, eso es normal, todos sabemos que los medios ópticos fallan. Intentemos otro.
6. OS debe ser de 32 bits. Ooops, me olvidé de comprobar, después de tanto jugar con periféricos y unidades. Vamos a quemar otro.
7. CD no arrancable. ¿Qué? OK, voy a revisar mi colección de "CDs oficiales", que he usado en el pasado y sé que funcionan:
	a. Fedora
	b. Debian
	c. RedHat
	d. Solaris
	f. Sabanyon
	g. ¡Incluso YellowDog!
	h. Aquí está: Ubuntu ... 7.0.4. Oh, bueno, siempre puedo actualizar más tarde
8. Por último, el CD instalador se carga ... sólo para mostrar un mensaje de error ilegible en multi-tecno-color. Pero he estado allí antes: es la tarjeta gráfica. Así que vamos a repetir, en modo compatibilidad (extra lento).
9. Error: /vmlinuz no encontrado. Compruebo el contenido del CD. El archivo está allí, pero tiene un .efi al final. Los foros en línea sugieren usar USB y borrar el apéndice del archivo. Pero eso no es una opción para mí. Así que tengo que meterme con el contenido ISO, y quemar otro CD. Oh, que alegría.
10. ¡Tachín! Funcionó. Ahora podemos actualizar. Siguiente disponible: 7.10. Aceptar, no hay problema, incluso si se tarda 10 actualizaciones, voy a llegar a la versión actual con tiempo ...
11. ¿Qué? ¿Error? Pero...¿? Vamos a investigar en línea: veo que el único problema no resuelto con los viejos actualizadores de Ubuntu es: 7.0.4 a 7.10 en iMacs. ¡Tienes que estar bromeando!
12. Espera, ahora que tenemos el cargador de arranque GNU / Linux, tal vez pueda saltar adelante a una nueva versión instalando de nuevo sobre él, ¿verdad? ¡Trae el CD Linux Mint 17!
13. ¡Éxito! Después de sólo un sinnúmero de horas de golpear mi cabeza contra los foros de novatos y techno-blogs expertos esotéricos, llegué a donde quería.

Valió completamente la pena. La sensación de domesticar a la bestia, de superar desafíos. ¡Me encanta!

Ahora, el MacPro. Estoy seguro de que no puede ser peor, ¿verdad?

1. Llave del USB con el instalador no reconocida. ¿Podría ser la llave? Hagamos otra.
2. La llave del USB no reconocida ... hmmm, esto es extraño. Tal vez sea el puerto USB, vamos a comprobarlo. Lo es. Mierda. Oh, bueno, siempre puedo usar el CD.
3. CD no legible. Bueno, eso es normal, todos sabemos que los medios ópticos fallan. Intentemos otro.
4. Nuevamente.
5. Una vez más. Esto no es normal.
6. Leo en línea que el cargador de arranque MacPro no me permite hacer lo que quiero. Así que a instalar rEFInd.
7. El nuevo gestor de arranque funciona, pero no arranca mis USB (en absoluto) o CD (los reconoce, pero no los carga).
8. Estoy investigando un poco más: ese MacPro particular es 64bit, PERO el bootloader es 32bit. Así que, lo que quería hacer nunca iba a funcionar!
9. Mientras voy opciones encontrando (algunas muy complejas y extravagantes), mis colegas mencionan que no lo necesitan después de todo.

Podría haberme frustrado, o enojado, o tercamente tratar de hacer que suceda de todos modos ... pero estoy demasiado ocupado, y mi orgullo no se confunde más por mi ego (o eso creo), así que decido pasar a otros proyectos, y aprender las muchas lecciones. ¿La principal? 
 **Revisa por triplicado lo que asumes**.

<div id="flickrembed"></div><div style="position:absolute; top:-70px; display:block; text-align:center; z-index:-1;">></div><script src='https://flickrembed.com/embed_v2.js.php?source=flickr&layout=responsive&input=www.flickr.com/photos/jcortell/sets/72157687091650855&sort=5&by=album&theme=default&scale=fill&limit=5&skin=default&autoplay=true'></script>