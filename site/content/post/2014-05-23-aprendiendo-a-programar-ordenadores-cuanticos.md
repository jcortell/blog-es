---
id: 5193
title: Aprendiendo a programar ordenadores cuánticos
date: 2014-05-23T11:38:19+00:00
author: Jorge Cortell
layout: post
guid: https://blog.cortell.net/es/?p=5193
permalink: /2014/05/23/aprendiendo-a-programar-ordenadores-cuanticos/
categories:
  - ¿Por qué no? ¿Utopías?
  - Geek Fun
  - General
  - Hacking
  - Personal
  - Placeres de la vida
  - Technology
  - Technolust
---
Ayer comencé a aprender y experimentar con programación de ordenadores cuánticos. No me es fácil expresar lo bien que me lo pasé y lo que me emocionó, pero lo intentaré:

<img class="aligncenter" src="https://www.extremetech.com/wp-content/uploads/2014/05/quantum-playground-640x353.jpg" alt="quantum computing simulator" width="640" height="353" />

Programar un ordenador cuántico es diferente de programar un ordenador "digital" binario (0 y 1). Para programar un sistema cuántico tienes que mapear un problema a la búsqueda del "punto más bajo" de una gran cantidad de opciones, que corresponde con el mejor resultado posible. El procesador considera todas las posibilidades simultáneamente para determinar **la menor energía requerida para formar esas relaciones**. Un ordenador cuántico es probabilístico, no determinístico, así que el ordenador produce las mejores respuestas de una forma muy rápida. Esto resulta no sólo en la solución óptima de una sola respuesta, sino en otras alternativas entre las que elegir.

> Por supuesto (_todavía_) no tengo acceso a un ordenador cuántico, así que he usado un simulador de ordenador cuántico con aceleración GPU y un interfaz de IDE simple, con su propio lenguaje de programación y _debugging_, y un visualizador de estado cuántico en 3D que permite simular eficientemente registros cuánticos de hasta 22 bits cuánticos (_qubits_), ejecutar algoritmos de Grover y Shor, y con una serie de puertas  lógicas cuánticas incorporadas.

Para usar un ordenador cuántico trasladas el problema a una ecuación cuyo objetivo es devolver los valores mínimos (soluciones óptimas). Se deben proveer dos valores – los "pesos" de los **qubits** (que existen en una superposición de estados 0 y 1, y son representados por números complejos) y las "fuerzas" de la interacción entre ellos. Cuando N qubits se superponen, se crea una combinación de 2^N estados.

**Las puertas lógicas cuánticas** son similares a las puertas lógicas empleadas en ordenadores digitales binarios. Con puertas cuánticas (que definen las operaciones más básicas que se pueden realizar con qubits) puedes construir algoritmos complejos, que por lo general culminan en una operación de medida que obtiene un valor clásico de qubits (bien 0 o 1, pero no una superposición).

Un grupo de  qubits llamado **registro cuántico** puede ser visualizado de varias formas, generalmente en un gráfico 2D o 3D, en el cual los puntos o barras representan el "**peso**" de superposición de qubits, mientras que el color o altura de la barra representa la "**fuerza**" (amplitud o fase) de una superposición dada.

> Una propiedad interesante de las puertas cuánticas es su reversibilidad, permitiendo la ejecución de los programas tanto hacia delante como a la inversa sin efectos secundarios.

El problema ya no es obtener la respuesta, sino hacer la pregunta correcta.

Procesado de Lenguaje Natural, Computación Cognitiva, Computación Cuántica... si no quieres temer a los nuevos amos que rápidamente se acercan, más te vale comenzar a aprender y a programarlos YA.

_La IA se acerca (AI is coming)_

&nbsp;