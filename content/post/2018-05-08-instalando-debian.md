---
author: ""
date: "2018-05-08T18:54:24+02:00"
draft: false
title: "Instalando Debian 9 en un Dell XPS13"
tags: ["personal","tecnología"]
image: "https://upload.wikimedia.org/wikipedia/commons/b/ba/Debian_Linux_Error_Photo1.jpg"
comments: false     # set false to hide Disqus comments
share: true        # set false to share buttons
thumbnailImagePosition: right
thumbnailImage: https://upload.wikimedia.org/wikipedia/commons/b/ba/Debian_Linux_Error_Photo1.jpg
coverImage: https://upload.wikimedia.org/wikipedia/commons/b/ba/Debian_Linux_Error_Photo1.jpg
metaAlignment: center
coverMeta: out
---

Tengo un portátil Dell XPS nuevo, así que decidí instalar Debian 9. Aquí van algunas lecciones aprendidas:

<!--more-->

>Advertencia: hay muchas variables involucradas en una configuración compleja. Si te encuentras en una situación similar, no asumas que lo que describo en este post necesariamente será aplicable a tus circunstancias.

Mi maravillosa esposa me regaló un nuevo Dell XPS 13 9365. Es un portátil elegante y de gran calidad. Desafortunadamente vino con Windows 10, así que, por supuesto, lo primero que tenía que hacer era instalar GNU / Linux como sistema operativo.

Siguiendo los consejos siempre sabios de mi amigo AndOr, decidí regresar, después de muchos años, a mi querido Debian. Esta vez con Wayland y Gnome.

Después de que la placa madre tuviera que ser reemplazada DOS VECES, bajo garantía, por Dell (soporte técnico *in situ*, increíble) aquí hay algunos pasos que tuve que dar para asegurarme de que todo funcionaba como se esperaba (Markdown es muy gracioso, escribo mi lista como 0,1, 2 ... y renderiza 1,2,3 ...):

0. Oprimiendo F12, entré en la BIOS y la actualicé (botón superior derecho) con el último archivo descargado de la web de Dell y cargado en un USB.
1. Reiniciando y volviendo a la BIOS, cambio:
  - Sistema conf. SATA cambia Raid a AHCI
  - Arranque seguro deshabilitado
  - Legacy ROM desactivado y clic en "Aplicar / Guardar". Tal vez debería haber cambiado (en Advanced BIOS Intel RapidStart a Off, para evitar bloqueos *sleep-wake*, pero más sobre eso más adelante).
2. Arranco el NetInstall de Debian 9 desde el USB, asegurándome de que el portátil estuviera conectado a internet a través de ethernet. Lo detectó automáticamente, así que no tuve que cambiar el orden de arranque ni nada.
3. No quería ni necesitaba ninguna partición con Windows o cualquier otra cosa, así que decidí borrar y realizar una instalación limpia.
4. En la configuración inicial, hay que omitir dar a root un nombre de usuario / contraseña y, en su lugar, hacerlo la primera vez que ejecute `sudo`. Otra opción más molesta sería agregar al usuario a `sudoers list` más tarde.
5. Acepta (lo siento mucho, Richard) repo no libre en APT, si quieres que tu tarjeta wifi funcione, e instala `firmware-iwlwifi`. Es posible que también necesites instalar `firmware-atheros.deb`.
6. Una cosa muy importante para verificar (a través de `top`, o tu comando de monitoreo favorito) si tu máquina comienza a trabajar demasiado duro es Tracker. En mi caso, traté de administrar las preferencias a través de `tracker-preferences` para reducir el consumo, pero fue en vano. Tuve que `tracker daemon-t` para matarlo, y finalmente desactivar cualquier actividad de indexación y búsqueda. Decidí probar con Synapse en su lugar. Veamos cómo va.
7. Nota adicional: la salida HDMI solo funciona en la última actualización del kernel de los *backports* (desde el kernel 4.13.0 en adelante, creo).

Después de una pequeña configuración y reinstalar algún software, como pasar de Thunderbird a Geary (en algunos casos, como Firefox, para obtener la última versión, necesitas `snap`), no podría estar más feliz. ¡Gracias cariño!
