# blog-nucleo


## Blog del Núcleo Gnu/Linux
En el blog de Nucleo compartiremos resúmenes de las charlas, tutoriales y muchas cosas más!!!

## Como funciona:
Los cambios que sean aprobado en la rama dev, estaran disponibles en: [betablog.nucleognulinux.org](betablog.nucleognulinux.org)  
Los cambios que sean aprobado en la rama master, estarán disponibles en: [blog.nucleognulinux.org](blog.nucleognulinux.org)


## Quiero contribuir, que necesito ?
1. Instalar git [Instalar git](https://www.atlassian.com/es/git/tutorials/install-git)
2. Instalar go [Instalar go](https://golang.org/doc/install)
3. Instalar hugo [Instalar Hugo](https://gohugo.io/getting-started/installing)
4. CLonar el repo
5. Listo!!!, ya tienes el proyecto, ahora a iniciar hugo.


Ejecuta el siguiente comando
```shell=
cd blog-nucleo
hugo server
```
Ahora abre el navegador y entra a **localhost:3000**

# Agregar contenido al blog
Para agregar contenido al blog, ejecute el siguiente comando.

```shell=
hugo new content/post/nombre-del-post/index.md
```
Una ves que tengas los cambios hecho solicita un PR, si no sabes como hacer un PR, te invitamos a que leas [Como hacer me primer PR ?](https://github.com/nucleognulinux/hacktoberFest2020/)