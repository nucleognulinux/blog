---
title: "Integracion continua usando Gitlab CI"
date: 2020-01-29T00:32:00-00:00
description: "Integracion continua usando Gitlab CI "
categories: ["DevOps"]
dropCap: true
displayInMenu: false
displayInList: true
draft: false
resources:
- name: featuredImage
  src: "ci-cd-flow.png"
---
# ¿Qué es DevOps?

"DevOps es la union de personas, procesos y productos para lograr la entrega de valor continuo para los usuarios finales" Donovan Brown - Principal DevOps Manager Microsoft

# ¿Qué es Integración Contínua (CI)?

La Integración Continua (Continuous Integration CI) es una práctica que incrementa la eficacia y la eficiencia de los resultados del equipo de desarrolladores.

Consiste en combinar los cambios realizados en el código del proyecto, en un repositorio central de forma periódica, para luego ejecutar pruebas y detectar y reparar errores lo antes posible.
### Integración y entrega continuas (CI/CD)

La integración continua es una práctica de desarrollo de software en la que los desarrolladores fusionan mediante combinación los cambios de código en la rama de código principal con frecuencia. En la integración continua se utilizan pruebas automáticas, que se ejecutan cada vez que se hace “commit” de código nuevo. De este modo, el código de la rama principal siempre es estable.


# Objetivo
AL finalizar esta guia podras tener tus propio repositorio gitlab configurado para que cada vez que se haga un commit se ejecuten pruebas automaticas.

Revisa estos links si tienes dudas:
[Curso Udemy DevOps - Las Artes Marciales del Software ](https://www.udemy.com/course/devops-las-artes-marciales-del-software/)
[¿Qué es DevOps? Microsoft Azure](https://azure.microsoft.com/es-es/overview/what-is-devops/)

# Manos a la obra
+ Cuenta en gitlab.com (Con ella podrás ejecutar Gitlab CI hasta 2000 minutos al mes.)
+ Proyecto link_proyecto
+ Configuracion
 * Archivo .gitlab-ci.yml
+ Ejecutando las pruebas en Gitlab CI

## Configuración
Para hacer que Gitlab CI reconozca nuestras pruebas y las ejecute debemos configurar nuestro proyecto, agregando algunos archivos:

## Archivo .gitlab-ci.yml

.gitlab-ci.yml es un archivo de configuración YAML que debes crear en la raíz de tu proyecto.

```bash

image: node:13.7.0
stages:
    - test-dev

cache:
    paths:
        - node_modules

before_script:
  - npm install
  - npm install -g jest

test-dev:
    stage: test-dev
    script:
        - npm test
```

Analicemos un poco este archivo:

En image le indicamos cuál imagen de Docker usará Gitlab para ejecutar las pruebas.

stages es la secuencia de pasos en los que se ejecutaran los jobs.

Con la opción de cache podemos establecer cuales archivos y carpetas serán guardarán en cache.

En before_script definimos el conjunto de comandos que se ejecutarán antes de que las pruebas sean ejecutadas. Para nuestro proyecto de nodejs necesitamos instalar las dependencias de la aplicación y realizar las configuraciones necesarias para que la app funcione correctamente.

test-dev es el job o trabajo que se va a ejecutar en Gitlab Runner y los comandos están definidos en scripts.

[Documentacion Yaml](https://docs.gitlab.com/ce/ci/yaml/README.html)

# Ejecutando las pruebas en Gitlab CI

Ahora procede a hacer commit de los dos archivos y git push para subir los cambios al repositorio.
![](./images/1.png)

Puedes ver estado del pipeline desde la opción CI/CD -> Pipelines, veras algo como:
*Un pipeline es un flujo de trabajo
![](./images/2.png)

Si todo salio bien, veremos algo similar:
![](./images/3.png)

En caso de fallo, veremos algo similar:
![](./images/4.png)


Desarrollar usando integración continua en nuestros proyectos es realmente beneficioso pues no necesitarías dedicarle mucho tiempo a probar el código cada vez que integras una nueva funcionalidad. Es bastante útil cuando se trabaja en equipos de desarrollo donde sus integrantes pueden no estar al tanto de todos los cambios y características del proyecto.