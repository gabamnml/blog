Migrando a vim de la costumbre de usar un IDE

No planeo hacer un “tutorial” paso a paso de como migrar a VIM porque en internet existen miles de ellos de todas formas y colores.
Pero si explicar en lo personal como lo fue para mi y que te animes después a tratar al menos de hacerlo.

Debo ser sincero y mencionar de primera instancia que no es muy fácil cuando uno ya tiene una costumbre de años utilizando un workflow al programar pero la motivación por ser mucho mas productivo aun, decidí por fin utilizar Vim en todo momento y no solo en la consola cuando accedo a un servidor o editar mi .zshrc.

Mis primeros pasos fueron un tanto caóticos ya que lo abría de vez en cuando tratando de forzar el uso y el estar acostumbrado a múltiples pestañas y ventanas con persistencia que nos proporcionan los IDE’s para continuar trabajando. En cambio en VIM tenia cada vez que lo utilizaba o cerraba algún proyecto tenia que iniciar todo nuevamente donde lo había dejado la ultima vez que trabaje sobre el.
Por lo que al final muchas veces me daba pereza comenzar de cero y terminaba al fin y al cabo volviendo a al IDE. 
Pero alguien vino al rescate, recordé que para la persistencia de Shell activas en servidores usaba TMUX y dije porque no usarlo con VIM  y me puse manos a la obra, al buscar por internet casi todo el mundo por no decir la mayoría usaba esta combinación perfecta de VIM + TMUX y con ello mil plugins y preferencias listas para usar y esto me cambio la vida. Ahora podía persistir sesiones junto con la gema tmuxinator para TMUX me daba la posibilidad de crear “workspaces” para cada uno de mis proyectos y no solo con VIM si no que cada uno podía tener pre cargado IRC con ciertos canales o lo que quisiera dependiendo del proyecto en el que este trabajando.

Pero no todo termino ahi, si bien ahora habia dejado por fin de usar mi IDE predilecto me sentia que algo faltaba como ‘tab completition’, syntax highlight, Navegar por el codigo, poder comentar multiples lineas de forma rapida o poder ver mi arbol de directorio de manera clara y rapida.
Y ahi llegaron los preciados plugins al rescate, hay miles por toda la web y muy bien documentados que solucionaron todas mis falencias para sentirme a gusto.
Si pero luego dices OK quiero instalar y cargar al menos 20 plugins que locura hacerlo a mano verdad?
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