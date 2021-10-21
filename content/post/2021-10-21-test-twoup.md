---
author: ""
date: "2021-10-21T04:00:24+02:00"
draft: false
title: "Probando TwoUp"
tags: ["personal", "tecnología"]
images: "https://res.cloudinary.com/jcortell/image/upload/v1634282494/Personal/blurredCLItxpower.png"
comments: false     # set false to hide Disqus comments
share: true        # set false to share buttons
thumbnailImagePosition: left
thumbnailImage: https://res.cloudinary.com/jcortell/image/upload/v1634282494/Personal/blurredCLItxpower.png
coverImage: https://res.cloudinary.com/jcortell/image/upload/v1634282494/Personal/blurredCLItxpower.png
metaAlignment: center
coverMeta: out
---

GoogleChromeLabs ha sacado un interesante componente para comparar dos elementos del DOM: [two-up](https://github.com/GoogleChromeLabs/two-up). Vamos a probarlo.

<!--more-->

A ver si Hugo renderiza el HTML inline correctamente, o tengo que añadir una plantilla de *shortcode* para que inserte HTML en bruto dentro del *markdown* de la entrada:

{{< rawhtml >}}

<script src="https://unpkg.com/two-up-element@1"></script>

<two-up>
  <div><img src="https://lh3.googleusercontent.com/t-t_jepUsuxueR9K1FIYOybuiefOriG6fCrxBJSHWs56dPvztmrcknPmkemzQSlr38T9HJC6LwOfaVD0yLmpaB0ydCLHqwv8jfaJ9V50OWNORczRJjgD5uoAt1VQZ1BWLX3ueEq3NeU=w1920-h1080" alt="before"></div>
  <div><img src="https://lh3.googleusercontent.com/DBgFrRegPOAmVbaDj_ecDZdn5nJ5B_YeTtj3YtO2gMMgPC5hIqk2m-fVfjWOPj7hG0-C7A6FxQcqILUSR0hM98uKuxwWJHA6mVGZEsgwqzeqLowftjeUnfNp10xS6bzQ7IDUoDl6Mq4=w1920-h1080" alt="after"></div>
</two-up>

{{< /rawhtml >}}
