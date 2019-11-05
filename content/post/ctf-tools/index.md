---
title: "Herramientas mas usadas en los CTFs"
date: 2019-10-28
description: "Herramientas mas usadas para los CTF o Wargames"
categories: ["ctfs","wargames","tools"]
dropCap: true
displayInMenu: false
displayInList: true
draft: false
resources:
- name: featuredImage
  src: "ctf.png"
---

## Rar
```bash
sudo pacman -S john
yay -S crunch
```
## Generar el diccionario de datos
```bash
crunch 5 5 60372 -d 5 -o /tmp/dic.txt
```  

```bash
5 min
5 max
60372 cadena donde se hace las permutaciones
-o archivo de salida
```
 
## Generar Hash
```bash
rar2john FILE.rar > hash.txt
# FILE.rar:$rar5$16$6e69d887fa5e43132cf5f470f1affa18$15$ab3cf14027e68a43fc4891514f068bca$8$a23564e68ac1d630
```
## Iniciamos el aque 
```bash
john hash.txt FILE.rar --wordlist=dic.txt --format=rar5
```

## Cuidado

* La primera vez generara la contraseña sera exitosamente, la segunda vez ya saldra error, para solucionarlo eliminar la carpeta `~/.john`


## Cracking
```bash
yay -S hexedit
```



## Esteganografia

Binwalk.- Herramienta para extraer archivos ocultos dentro de imagenes

Sacar los headers de una imagen
perl-image-exiftool 


binwalk Sirve para descubrir si hay archivos ocultos dentro de otro archivo

binwalk -e nombre_archivo


Steghide

Con steghide puedes encontrar archivos ocultos que hayan sido protegidos con contraseña. Veamos la siguiente imagen

continuara...
