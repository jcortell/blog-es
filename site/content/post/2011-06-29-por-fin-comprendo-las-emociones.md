---
id: 3292
title: ¡Por fin comprendo las emociones!
date: 2011-06-29T19:26:34+00:00
author: Jorge Cortell
layout: post
guid: https://cortell.net/blog/?p=3292
permalink: /2011/06/29/por-fin-comprendo-las-emociones/
wpsd_autopost:
  - "1"
categories:
  - Geek Fun
  - General
  - Otras cosas
  - Personal
  - Psicología
  - Sociedad y polí­tica
  - Technology
---
<img class="aligncenter" src="https://farm6.static.flickr.com/5139/5468624509_125233a614.jpg" alt="emociones según Plutchik" />

Si ya lo decía yo, lo único que me hacía falta era una taxonomía bien definida (y a ser posible que se convierta en un estándar y en un lenguaje bien estructurado y definido como el [EML](https://www.w3.org/2005/Incubator/emotion/XGR-emotionml-20081120/)), que permita expresiones y procesos del tipo:

<emotionml xmlns=“https://www.w3.org/2011/06/emotionml”>
  
<metadata>
  
<name>Jorge example</name>
  
</metadata>

<!– Appraised value of incoming event –>
  
<emotion>
  
<modality mode="senses"/>
  
<appraisals set="scherer\_appraisals\_checks">
  
<novelty value="0.8" confidence="0.4"/>
  
<intrinsic-pleasantness value="-0.5" confidence="0.8"/>
  
</appraisals>
  
</emotion>

<!– Jorges current internal state configuration –>
  
<emotion>
  
<modality mode="internal"/>
  
<dimensions set="arousal\_valence\_potency">
  
<arousal value="0.3"/>
  
<valence value="0.9"/>
  
<potency value="0.8"/>
  
</dimensions>
  
</emotion>

<!– Jorges output action tendencies –>
  
<emotion>
  
<modality mode="body"/>
  
<action-tendencies set="myActionTendencies">
  
<charge-energy value="0.9"/>
  
<seek-shelter value="0.7"/>
  
<pickup-object value="-0.2"/>
  
</action-tendencies>
  
</emotion>

<!– Jorges facial gestures –>
  
<emotion>
  
<modality mode="face"/>
  
<category set="ekman_universal" name="joy"/>
  
<link role="expressedBy" start="0" end="5s" uri="smile.xml"/>
  
</emotion>
  
</emotionml>

y un [estudio](https://wefeelfine.org/book/) estadístico amplio y actual presentado de forma visual:

<img class="aligncenter" src="https://wefeelfine.org/book/pages/236-237.jpg" alt="pp 236-237" />
  
<img class="aligncenter" src="https://wefeelfine.org/book/pages/242-243.jpg" alt="242-243" />
  
<img class="aligncenter" src="https://wefeelfine.org/book/pages/244-245.jpg" alt="244-245" />

**¿Te ríes? Me alegro de que las emociones estuviesen en tu _firmware_ de origen.**