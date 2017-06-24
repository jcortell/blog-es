---
date: 2017-06-22T10:24:16-04:00
title: Nuevo Blog
---

Como resultará evidente, he cambiado de blog.  
No por una cuestión de estilo, sino por dos motivos técnicos:
  
1. Mi blog anterior estaba basado en WordPress, un CMS (Sistema de Gestión de Contenidos) que generaba el blog desde una base de datos. Eso hacía que la gestión de los datos fuese mucho más engorrosa y poco trasparente de lo que me gusta
2. El rendimiento y la seguridad de un blog basado en base de datos es MUY inferior comparado con uno como el que he montado (este), basado en un "Generador Estático"

Para hacerse una idea, el blog anterior obtenía en los tests de rendimiento un 38/100, y este obtiene un 99/100:

- Tiempo de inicio de carga de 428ms a 21ms
- Tiempo completo de carga de 741ms a 21ms
- Ahora tiene HTTPS (lo voy a añadir), HTTP2 y certificado SSL

Además ahora está hospedado en un CDN (Red de Servidor de Contenido) con lo que carga más deprisa en todo el mundo.

Por supuesto no lo he hecho por mi propio blog (ni miro cuante gente lo lee), sino por aprender, y por probar alternativas para los sistemas de mi empresa.

Así que después de trastear con Jekyll, GitHub pages, Nikola, Octopress, y varias alternativas más, me he decidido por Hugo con Gulp, Webpack, y Netlify, manteniendo el contenido en formato de archivos de texto plano (markdown) bajo sistema de versioneado de GitHub.

Por cierto, migrar miles de posts de mi blog anterior ha sido cuestión de minutos, con sólamente un pequeño error en una línea.

¡Una maravilla!

 