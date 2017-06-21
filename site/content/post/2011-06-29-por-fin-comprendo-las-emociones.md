---
id: 3292
title: ¡Por fin comprendo las emociones!
date: 2011-06-29T19:26:34+00:00
author: Jorge Cortell
layout: post
guid: http://cortell.net/blog/?p=3292
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
<img class="aligncenter" src="http://farm6.static.flickr.com/5139/5468624509_125233a614.jpg" alt="emociones según Plutchik" />

Si ya lo decía yo, lo único que me hacía falta era una taxonomía bien definida (y a ser posible que se convierta en un estándar y en un lenguaje bien estructurado y definido como el [EML](http://www.w3.org/2005/Incubator/emotion/XGR-emotionml-20081120/)), que permita expresiones y procesos del tipo:

<emotionml xmlns=“http://www.w3.org/2011/06/emotionml”>
  
<metadata>
  
<name>Jorge example</name>
  
</metadata>

<!&#8211; Appraised value of incoming event &#8211;>
  
<emotion>
  
<modality mode=&#8221;senses&#8221;/>
  
<appraisals set=&#8221;scherer\_appraisals\_checks&#8221;>
  
<novelty value=&#8221;0.8&#8243; confidence=&#8221;0.4&#8243;/>
  
<intrinsic-pleasantness value=&#8221;-0.5&#8243; confidence=&#8221;0.8&#8243;/>
  
</appraisals>
  
</emotion>

<!&#8211; Jorges current internal state configuration &#8211;>
  
<emotion>
  
<modality mode=&#8221;internal&#8221;/>
  
<dimensions set=&#8221;arousal\_valence\_potency&#8221;>
  
<arousal value=&#8221;0.3&#8243;/>
  
<valence value=&#8221;0.9&#8243;/>
  
<potency value=&#8221;0.8&#8243;/>
  
</dimensions>
  
</emotion>

<!&#8211; Jorges output action tendencies &#8211;>
  
<emotion>
  
<modality mode=&#8221;body&#8221;/>
  
<action-tendencies set=&#8221;myActionTendencies&#8221;>
  
<charge-energy value=&#8221;0.9&#8243;/>
  
<seek-shelter value=&#8221;0.7&#8243;/>
  
<pickup-object value=&#8221;-0.2&#8243;/>
  
</action-tendencies>
  
</emotion>

<!&#8211; Jorges facial gestures &#8211;>
  
<emotion>
  
<modality mode=&#8221;face&#8221;/>
  
<category set=&#8221;ekman_universal&#8221; name=&#8221;joy&#8221;/>
  
<link role=&#8221;expressedBy&#8221; start=&#8221;0&#8243; end=&#8221;5s&#8221; uri=&#8221;smile.xml&#8221;/>
  
</emotion>
  
</emotionml>

y un [estudio](http://wefeelfine.org/book/) estadístico amplio y actual presentado de forma visual:

<img class="aligncenter" src="http://wefeelfine.org/book/pages/236-237.jpg" alt="pp 236-237" />
  
<img class="aligncenter" src="http://wefeelfine.org/book/pages/242-243.jpg" alt="242-243" />
  
<img class="aligncenter" src="http://wefeelfine.org/book/pages/244-245.jpg" alt="244-245" />

**¿Te ríes? Me alegro de que las emociones estuviesen en tu _firmware_ de origen.**