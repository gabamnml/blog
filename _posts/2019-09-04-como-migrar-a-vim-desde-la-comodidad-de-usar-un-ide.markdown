---
layout: post
title: "Como migrar a VIM desde la comodidad de usar un IDE"
date: 2019-09-04
author: gabamnml
tags:
  - Vim
  - ide
  - productividad
  - vim plugins
category: blog
blog: true
---

No planeo hacer un tutorial paso a paso de como migrar o instalar VIM. En internet existen miles de ellos en todas las formas y colores.
Si no que me enfocare en contar mi experiencia personal para que luego tu puedas animarte a hacerlo y dar el salto.

Debo ser honesto y mencionar de primera instancia que no es muy sensillo cuando ya tienes el habito de años con cierto flujo de trabajo al escribir codigo pero la motivacion de ser aun mucho mas productivo finalmente decidi usar VIM todo el tiempo y no solo en la consola cuando acceso a un servidor remoto o para editar mi .zshrc.

Mis primeros pasos fueron un poco caoticos, usaba vim forzozamente ocacionalmente ya que estaba acostumbrado a mi IDE donde tenia todo listo con la persistencia de las ventanas del trabajo del dia anterior para continuar con mi labor sin embargo esto no sucedia con VIM cada vez tenia que volver a inicializar todas las ventanas de trabajo y recordar en que estaba una y otra vez. Me frustraba por lo que volvia a usar mi IDE predilecto.
  
Pero alguien vino al rescate, recordé que para la persistencia de Shell activas en servidores usaba [TMUX](https://tmux.github.io) y dije porque no usarlo con VIM  y me puse manos a la obra, al buscar por internet casi todo el mundo por no decir la mayoría usaba esta combinación perfecta de VIM + TMUX y con ello mil plugins y preferencias listas para usar y esto realmente me cambio la vida. Ahora podía persistir sesiones junto con la gema [tmuxinator](https://github.com/tmuxinator/tmuxinator) para TMUX me daba la posibilidad de crear “workspaces” para cada uno de mis proyectos de manera muy facil y no solo con VIM si no que cada uno de estos proyectos podía tener pre cargado IRC (Si! aun lo uso) con ciertos canales o lo que quisiera dependiendo del proyecto en el que este trabajando.

Pero no todo termino ahí, si bien ahora había dejado por fin de usar mi IDE predilecto me sentía que algo faltaba como ‘auto completado’, resaltado de sintaxis, Navegar por el código, poder comentar múltiples lineas fácilmente o poder ver mi árbol de directorio de manera clara y rápido.
Y ahi llegaron los preciados plugins, hay miles por toda la web y muy bien documentados que solucionaron todas mis falencias para sentirme a gusto.
Luego dices OK quiero instalar y cargar al menos 20 plugins que locura hacerlo a mano verdad?
Buscando sobre como optimizar la tarea de instalar/actualizar y cargar los plugins en VIM me encontré con **Pathogen**, Existen varios plugins managers algunos con mas ventajas que otros pero este es el que a mi al menos me acomodo en términos de puesta en marcha y uso.

Te preguntaras porque aun no mencione nada al respecto de lo tedioso de tener que trabajar todo el tiempo con shortcuts de teclado ya que no existe mouse?
Pues bien quería dejarlo para el final.
Una vez que estuve 100% a gusto con todo lo necesario para poder usar VIM me tocaba la parte de aprender esos atajos de teclado aparte del clásico “i” para editar “:q” para salir o “:w” para guardar (ah me olvidaba tengo un plugin que hace auto guardado)
que fueron con los que me había manejado toda mi vida a la hora de usar VIM en servidores como le sucede a la mayoría y que no utiliza el horroroso NANO si eres uno de esos por favor te ruego que lo dejes de lado.
Y en verdad fue muy simple comienza por esos y de a poco ve averiguando atajos que vayas necesitando usar no te vuelvas loco aprendiéndotelos todos porque es imposible lo único que conseguirás es frustrarte.
Veras como a cabo de unos días ya te vas a sentir que es tu lugar de trabajo ideal y mucho mas productivo.


No se tu pero yo soy fanático del terminal y el no tener que salir de ahí para nada lo encuentro increíble ya que evita distracciones de otras aplicaciones al cambiar de foco, porque navego por directorios, levanto servidores locales, escribo código y un sin fin de tareas sin salir del terminal. Ah! y ahorras recursos de RAM y CPU :)

Se que mucha gente te hablara de que VIM es fantástico por su poder de sintaxis para manipular y navegar en texto y esto sin duda es increíble pero en lo personal son muchos mas los beneficios que obtienes al usarlo, que dejare por tu cuenta a que los descubras.

Espero al menos haberte levantado la curiosidad por usar VIM ojalá sea así.

PD: Si bien mi VIM tiene muchos plugins instalados y aveces los necesitaría en un servidor remoto igual es completamente placentero usar un mismo editor en cualquier parte se siente como en casa estés donde estés. 
La dependencia es muy baja a no ser que te conviertas en un adicto a los plugins. =P

PD2: ![](http://i.imgur.com/Fx1FXhQ.png)