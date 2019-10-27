# blog-nucleo

*Blog del Núcleo Gnu/Linux*

Necesitamos un blog, urgente para documentar todo de las clases de cero a produccion y como me gusta complicarme,
les cuento que momentaneamente (hasta que tengamos uno definitivo) busque un blog en GO usando HUGO (Hugo es uno de los generadores de sitios estáticos ),
el codigo que se hace en GO hay que "compilarlo" y eso genera unos archivos HTML que se puede llevar a cualquier parte.


El blog no lo hice, lo encontre en template en github y sobre eso agregue contenido del primer dia de clases de Sergio
pero como me gusta complicarme++ lo subi a gitlab para que funcione con Continous Integration, Continuos Delivery y Continuos Deployment.


*Como funciona:*

En el git hay dos ramas la  dev y master (en lo posible no hay que tocar).

1. Cada ves que se haga un git commit (un cambio) dentro la rama dev este automaticamente ejecutara pruebas
2. Si todo sale bien se "compilara"
3. Si la compilacion salio bien los archivos se enviaran al servidor

Los cambios se podran ver en esta parte *betablog.nucleognulinux.org*


Cada ves que se haga un git commit dentro la rama master, todo sera lo mismo, solo que los cambios se veran en blog.nucleognulinux.org

La rama master es la de produccion, esta la vera todo el mundo, asi hay que tener cuidado con lo que publicamos
La otra rama dev, es para hacer pruebas y demas, en teoria la veremos solo nosotros y podremos corregir y demas.

Quiero contribuir, que necesito ?

1. Instalar git
2. Instalar go
3. Instalar hugo
4. CLonar el repo git clone git@gitlab.com:starsaminf/blog-nucleo.git

```shell=
cd blog-nucleo
hugo server
```


Abre el navegador y entra a localhost:3000


Como agrego mas contenido ?

```shell=
hugo new content/post/devOps-sessions-2/index.md
```