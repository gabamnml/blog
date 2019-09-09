---
layout: post
title: "COMANDOS MÁS FRECUENTES PARA UTILIZAR GIT"
date: 2019-09-04
author: gabamnml
tags:
  - git
  - github
  - productividad
  - comandos git
category: blog
blog: true
---

En esta ocasión quiero traerles los “comandos” más típicos o más necesitados en la comunidad para trabajar con **GIT** el ya Mega archi reconocido controlador de versiones. Sin mas preámbulo vamos con ello

### Como deshacer el commit mas reciente localmente en git
```
git reset --hard HEAD~1
```

### Como borrar una rama local y remota
###### Remoto
```
git push origin --delete <tu_rama> 
```
###### Local
```
git branch -D <tu_rama>
```

### Como renombrar una rama
```
git branch -m <viejonombre> <nuevonombre>
```

### Como deshacer un `git add <archivo>`
```
git reset <archivo>
```

### Como borrar archivos locales que no estan "trackeados" en Git
```
git clean -f
```
pd: ten cuidado al utilizar este comando ya que perderias dichos archivos.

### Como forzar un `git pull`
###### Primero me traigo la informacion
```
git fetch --all
```
###### Fuerzo el contenido que quiero remplazar
```
git reset --hard origin/<nombre_rama>
```

### Como forzar un `git push`
```
git push --force
```


Este contenido se va a ir actualizando con el tiempo.
Si te gusto por favor compartelo :)
