---
layout: post
title: "Hoy presento mi navaja suiza de teclado en MacOS (A.K.A OSX)"
date: 2019-09-01
author: gabamnml
tags:
  - Productivity
  - utilities
  - keyboard pro
category: blog
blog: true
---

- Cambias varios teclados distintos en un misma computadora?
- Creas atajos de teclado?
- Usas varios monitores?
- Cambias la distribución de ventanas?

En mas de alguna seguro te identificas no?
Por eso te traigo una utilidad que para mi al menos la veo como una navaja suiza porque realmente si te pones creativo y a programar lo puedes hacer todo. Y su nombre es **Hammerspon**.

**Hammerspon** en su [web](http://www.hammerspoon.org) se auto describe como: 
*Una poderosa herramienta para la automatización de OS X. Un puente entre el sistema operativo y un motor de scripting en Lua (SI! en Lua! si nunca lo usaste o no lo conoces no te asustes es muy fácil de leer y escribir). Un conjunto de extensiones que exponen piezas específicas de la funcionalidad del sistema, para el usuario.
*
Ahora bien, que podemos hacer con todo esto? por lo que ellos responden:
*Reaccionar y/o manipular aplicaciones, ventanas, punteros del mouse, sistema de archivos, dispositivos de audio, baterías, pantallas, teclado de bajo nivel / eventos de mouse, portapapeles, servicios de localización, wifi, y mucho más.*

Suena bien no? pero… que utilidad diaria podríamos darle?
Y ahí como respuesta entran todas las preguntas que hice al comienzo del post.


Antiguamente para el manejo de ventanas (re ordenar, dimensionar, foco) ![](http://i.imgur.com/MVRHA5y.gif)

Usaba el poderoso pero antiguo [Slate](https://github.com/jigish/slate) su falta de actualización consiguió que me ponga a buscar alguna alternativa mas novedosa y ahí entre distintas pruebas encontré Hammerspon y por su versatilidad, simpleza y actualización constante decidí quedarme con el.

Cabe destacar que a nivel de manejo de ventanas prácticamente ambos son similares vas a poder re dimesionarlas, cambiarlas de pantalla, etc… pero la ventaja que logras con **Hammerspon** es que no es solo un windows manager entonces se abre foco completamente a la versatilidad como por ejemplo: Puedo detectar a que **WiFi** estoy conectado y si por ejemplo cumple la regla de que me encuentro usando el de la oficina asignar automáticamente que me genere una distribución de ventanas para el monitor del escritorio con ciertas proporciones según que aplicaciones tengo corriendo.
O algo totalmente distinto como por ejemplo subir el volumen del computador al llegar a casa o ponerlo en 0 al irme. Y todo esto es tan simple escribiendo las siguientes lineas de código en Lua

    local wifiWatcher = nil
    local homeSSID = "WifiDeCasa"
    local lastSSID = hs.wifi.currentNetwork()
    
    function ssidChangedCallback()
        newSSID = hs.wifi.currentNetwork()
    
        if newSSID == homeSSID and lastSSID ~= homeSSID then
            -- We just joined our home WiFi network
            hs.audiodevice.defaultOutputDevice():setVolume(25)
        elseif newSSID ~= homeSSID and lastSSID == homeSSID then
            -- We just departed our home WiFi network
            hs.audiodevice.defaultOutputDevice():setVolume(0)
        end
    
        lastSSID = newSSID
    end
    
    wifiWatcher = hs.wifi.watcher.new(ssidChangedCallback)
    wifiWatcher:start()

Volviendo al tema del manejo de ventanas lo que siempre por ejemplo uso es poder dividir la pantalla en 2 para trabajar al mismo tiempo con 2 aplicaciones distintas y lo puedes obtener escribiendo algo como esto en Lua:

    hs.hotkey.bind({"cmd", "ctrl"}, ",", function()
      local win = hs.window.focusedWindow()
      local f = win:frame()
      local screen = win:screen()
      local max = screen:frame()
    
      f.x = max.x
      f.y = max.y
      f.w = max.w / 2
      f.h = max.h
      win:setFrame(f)
    end)
    
    hs.hotkey.bind({"cmd", "ctrl"}, ".", function()
      local win = hs.window.focusedWindow()
      local f = win:frame()
      local screen = win:screen()
      local max = screen:frame()
    
      f.x = max.x + (max.w / 2)
      f.y = max.y
      f.w = max.w / 2
      f.h = max.h
      win:setFrame(f)
    end)
    
    hs.hotkey.bind({"cmd", "ctrl"}, "/", function()
      local win = hs.window.focusedWindow()
      local f = win:frame()
      local screen = win:screen()
      local max = screen:frame()
    
      f.x = max.x
      f.y = max.y
      f.w = max.w
      f.h = max.h
      win:setFrame(f)
    end)

Lo que estoy haciendo acá es básicamente enlazar un atajo de teclado en particular a cada cambio de tamaño por ejemplo “CMD + Ctrl + ,” lo que hace es dividir en la mitad mi ventana y llevarla al lado izquierdo de la pantalla el otro atajo hace lo mismo hacia el lado derecho y el otro hace cubrir toda la pantalla con la ventana actual.

Algo que por ejemplo me resolvió totalmente mi día a día fue un script que escribí que se los dejo a continuación. 

    local usbWatcher = nil
    
    function usbDeviceCallback(data)
        if (data["productName"] == "USB Keyboard") then
            if (data["eventType"] == "added") then
                hs.execute('/Applications/Karabiner.app/Contents/Library/bin/karabiner select 1')
            elseif (data["eventType"] == "removed") then
                hs.execute('/Applications/Karabiner.app/Contents/Library/bin/karabiner select 0')
            end
        end
    end
    
    usbWatcher = hs.usb.watcher.new(usbDeviceCallback)
    usbWatcher:start()

Lo que hace es revisar si se agrego un teclado externo USB al laptop y cambia mi perfil en **Karabiner** (Aplicación que uso para re mapear mis teclados) y si lo desenchufo vuelve al perfil por defecto, de esta forma cambio rápidamente mi configuración de teclado si es que utilizo mi teclado externo y de esta forma no tener que cambiar el perfil a mano cada vez que quiero usarlo. Ejemplo: De la casa a la oficina.
 
Mirando la documentación se puede fácilmente lograr todo esto y mucho mas y ni siquiera hace falta que sepas Lua ves? 

Espero que te sirva y haga de tu vida como desarrollador mas productiva y/o entretenida.
Si tienes dudas respecto al uso de **Hammerspon** o como programar en **Lua** no dudes en escribirme, estaré feliz de ayudar.