---
title: "De cero a producción  Session1"
date: 2019-10-26T10:35:35-05:00
description: "DevOps es un término que engloba un grupo de conceptos, prácticas y técnicas que aunque no son todos nuevos, se están extendiendo por la comunidad del software.."
categories: ["DevOps"]
dropCap: true
displayInMenu: false
displayInList: true
draft: false
resources:
- name: featuredImage
  src: "devops.png"
---

El martes 22 de Octubre, nuestro buen amigo [Sergio](https://twitter.com/donkeysharp) miembro de la comunidad [Cloud La Paz](https://www.facebook.com/lapazcloud/), es el instructor de esta serie de clases *De Cero a Producción*.

Necesitamos instalar nodeJS

**Node.js v12.x**:

**Ubuntu**
```shell=
curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash -
sudo apt update
sudo apt install -y nodejs
```

**Debian**
```shell=
sudo bash
curl -sL https://deb.nodesource.com/setup_12.x | bash -
apt update
apt install -y nodejs
```

**Manjaro**
```shell=
yay -S npm nodejs 
```
**Git**

**Debian/Ubuntu**
```shell=
sudo apt install git
```

**Manjaro**
```shell=
yay -S git 
```

## Tarea 
El Señor Homero alias el desarrollador te dio este repo de GitHub
```sh
git clone https://github.com/sguillen-proyectos/le-challenge-app
```

El señor Homero no escribió la documentación del programa,
asi que tu tarea es hacer correr el programa.  

Éxitos joven!!!


## Solucion

<details>
<summary>Clic para ver la solución</summary>
<p>

```shell=
git clone https://github.com/sguillen-proyectos/le-challenge-app
cd le-challenge-app
npm install
apt install redis
```
</p>
</details>