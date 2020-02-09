---
id: 3514
title: Poesía en el código
date: 2011-09-18T10:09:47+00:00
author: Jorge Cortell
layout: post
guid: https://cortell.net/blog/?p=3514
permalink: /2011/09/18/poesia-en-el-codigo/
wpsd_autopost:
  - "1"
categories:
  - Arte
  - Free Software
  - Geek Fun
  - General
  - Hacking
  - Placeres de la vida
  - Technology
  - Technolust
---
Algunas de las líneas de código más interesantes y poéticas que uno puede encontrar:

Cabecera C autoejecutable (explicado <a title="https://gist.github.com/448040" href="https://gist.github.com/448040" target="_blank">aquí</a>):`<br />
//&>/dev/null;x="${0%.*}";[ ! "$x" -ot "$0" ]||(rm -f "$x";cc -o "$x" "$0")&&exec "$x" "$@"<br />
` 

Para cuando te sientes nihilista...

<pre>rm -rf *.*</pre>

o bien

<pre>rm -rf /</pre>

o la bomba de <a title="https://www.p0es1s.net/en/projects/jaromil.html" href="https://www.p0es1s.net/en/projects/jaromil.html" target="_blank">Jaromil</a>, pura poesía (con espacios extra añadidos para evitar cambiar la configuración por defecto de WP para la autodetección de smilies :-):

<pre>: ( ) {  : | : &  } ; :</pre>

que en el shell de Windows sería

<pre>%0|%0
</pre>

Y el más hermoso, este código:`<br />
main(){float A,B,P,Q,X,Y,d;int i,D=80,n=3120;for(X=-2.,Y=-1.5,d=6./D;B=2*A<br />
*B+Y,A=P-Q+X,n;((P=A*A)+(Q=B*B)>4||++i>D)&&putchar(*((n--%D?X+=d/2,i :11:(X=-2.0,Y+=d,12))+"Mandelbrot! n"))&&(A=B=P=Q=i=0));}<br />
` 

hace esto (set de Mandelbrot, para los que... olvídalo):

    ~~~~~~~~~~~~~}}}}}}}}}}}}}}}}}}}}||||||||{{{zyvrwuW{|||||}}}}}}~~~~~~~~~~~~
    ~~~~~~~~~~}}}}}}}}}}}}}}}}}}}}|||||||||{{{zyxwoaqwxz{{{|||||}}}}}}~~~~~~~~~
    ~~~~~~~~}}}}}}}}}}}}}}}}}}}|||||||||{{zzzyxvn    Knwyz{{{{||||}}}}}}~~~~~~~
    ~~~~~~}}}}}}}}}}}}}}}}}}||||||||{{zyxuxxxwvuq     svwwyzzzyr{||}}}}}}}~~~~~
    ~~~~}}}}}}}}}}}}}}}}}|||||{{{{{zzzxt>  qf             pttfqeqz{|}}}}}}}}~~~
    ~~~}}}}}}}}}}}}}}|||{{{{{{{{{zzzywotn                     atyz{||}}}}}}}}~~
    ~~}}}}}}}}}||||{{zwvyyyyyyyyyyyxvsP                        swvz{||}}}}}}}}~
    ~}}}}|||||||{{{{zyxvpN[ur]spvwwvi                           qxz{|||}}}}}}}}
    ~}||||||||{{{{{zyytun         qq                            avz{|||}}}}}}}}
    ~||||||{zzzzyyxtroqb           a                            xz{{|||}}}}}}}}
    ~@G::# 6# (                                              pvxyz{{||||}}}}}}}
    ~||||||{zzzzyyxtroqb           a                            xz{{|||}}}}}}}}
    ~}||||||||{{{{{zyytun         qq                            avz{|||}}}}}}}}
    ~}}}}|||||||{{{{zyxvpN[ur]spvwwvi                           qxz{|||}}}}}}}}
    ~~}}}}}}}}}||||{{zwvyyyyyyyyyyyxvsP                        swvz{||}}}}}}}}~
    ~~~}}}}}}}}}}}}}}|||{{{{{{{{{zzzywotn                     atyz{||}}}}}}}}~~
    ~~~~}}}}}}}}}}}}}}}}}|||||{{{{{zzzxt>  qf             pttfqeqz{|}}}}}}}}~~~
    ~~~~~~}}}}}}}}}}}}}}}}}}||||||||{{zyxuxxxwvuq     svwwyzzzyr{||}}}}}}}~~~~~
    ~~~~~~~~}}}}}}}}}}}}}}}}}}}|||||||||{{zzzyxvn    Knwyz{{{{||||}}}}}}~~~~~~~
    ~~~~~~~~~~}}}}}}}}}}}}}}}}}}}}|||||||||{{{zyxwoaqwxz{{{|||||}}}}}}~~~~~~~~~
    ~~~~~~~~~~~~~}}}}}}}}}}}}}}}}}}}}||||||||{{{zyvrwuW{|||||}}}}}}~~~~~~~~~~~~
    ~~~~~~~~~~~~~~~~~}}}}}}}}}}}}}}}}}}}}}|||||{zmt{{{||||}}}}}~~~~~~~~~~~~~~~~
    

<pre>/* no comment */</pre>

😉