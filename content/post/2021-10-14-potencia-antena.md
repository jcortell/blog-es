---
author: ""
date: "2021-10-14T04:00:24+02:00"
draft: false
title: "Rebajando la potencia de la antena de mi portátil"
tags: ["personal", "tecnología"]
images: "https://res.cloudinary.com/jcortell/image/upload/v1634282494/Personal/blurredCLItxpower.png"
comments: false     # set false to hide Disqus comments
share: true        # set false to share buttons
thumbnailImagePosition: right
thumbnailImage: https://res.cloudinary.com/jcortell/image/upload/v1634282494/Personal/blurredCLItxpower.png
coverImage: https://res.cloudinary.com/jcortell/image/upload/v1634282494/Personal/blurredCLItxpower.png
metaAlignment: center
coverMeta: out
---

Un adaptador múltiple USB-C funcionaba mal. Parecía ser una interferencia de la antena de mi portátil. Así que decidí reducir la potencia de la antena. A continuación, te muestro un pequeño procedimiento para evitarte la molestia de horas perdidas en un proceso mal documentado.

<!--more-->

Los portátiles son cada vez más ligeros y compactos. La portabilidad es una gran ventaja, pero también hay algunos inconvenientes, como la capacidad de reparación o la posibilidad de interferencias.

Mi adaptador múltiple Dell DA200 USB-C nunca funcionó correctamente. Si conectaba todo (cable Ethernet, HDMI / VGA y USB), al menos dos de esas cosas no funcionaban. Durante mucho tiempo no me importó, ya que lo usaba de viaje y lo único que me importaba era hacer una presentación para un cliente o tener un ratón externo. Pero cuando traté de usarlo desde la oficina de casa, conectado al teclado y al monitor externo, me molestó. Así que recurrí a la amigable comunidad en línea para verificar las posibles causas de este mal funcionamiento.

Fue entonces cuando aprendí a regular la potencia de la antena del portátil. En teoría, la proximidad del adaptador a la antena es lo que estaba causando el mal funcionamiento.

> Dato curioso: los portátiles XPS de Dell tienen conectores USB-C en ambos lados de la máquina. Ambos pueden conectar el adaptador de corriente. Pero solo uno tiene un icono que indica carga de energía (⚡). ¿Por qué? Parafraseando a un ingeniero de Dell: 'si no colocáramos ningún icono en ninguno de los lados, la gente llamaría a soporte técnico para averiguar cómo cargar el portátil ... y si lo colocáramos en ambos lados, crearía confusión y la gente llamaría al soporte técnico para averiguar qué lado es el correcto, por lo que decidimos colocarlo en un lado arbitrario'.

Resultó no ser la causa del mal funcionamiento de mi DA200, y terminé comprando otro adaptador que me permite tener una configuración de monitor triple (¡bien!). Pero entré en la madriguera del conejo de potencia de la antena. Aquí está el resumen.

Larga historia corta:
* Modificar la potencia de la antena de tu portátil (dentro de ciertos límites) no tiene ningún efecto en su cobertura wifi.
* No debes **aumentar** la potencia de la antena de tu portátil, porque no obtienes nada y podría ser ilegal (cada país regula la potencia y las frecuencias de los equipos de telecomunicaciones).
* **Deberías reducir** la potencia de la antena de tu portátil, porque ahorrarás energía, lo cual es bueno para el medio ambiente, tu factura de electricidad y la batería de tu portátil.
* Los fabricantes no hacen que esa información esté fácilmente disponible en la mayoría de los casos. Y cuando lo hacen, asumen que usas un sistema operativo Microsoft Windows y quieren que te metas con el BIOS.

Entonces, ¿qué hacer si usas un sistema GNU/Linux, como yo?

4 sencillos pasos:

* Selecciona la interfaz correcta (y el nombre) abriendo el CLI y escribiendo `netstat -i`. En mi caso fue `wlp60s0`.
* Verifica los detalles, incluida la energía, escribiendo `iwconfig [nombre de interfaz]`. En mi caso fue Tx-Power = 22 dBm.
* Reduce la potencia, escribiendo `sudo iwconfig [nombre de interfaz] txpower [número deseado]`. En mi caso bajé a Tx-Power = 11 dBm. Introduce la contraseña para `sudo`.
* Verifica que funcionó escribiendo nuevamente (o usando la tecla de flecha para recorrer comandos recientes) `iwconfig [nombre de la interfaz]` y verificando el Tx-Power.
* El cambio no es permanente, por lo que cuando cierres la sesión y vuelvas a iniciarla, volverá a la configuración predeterminada. Hay varias formas de hacerlo permanente, pero lo dejo para que lo investigues, ya que está muy bien documentado en línea.
