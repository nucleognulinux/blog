---
title: "Guía Markdown"
date: 2020-08-09T21:03:58-04:00
description: "Esta es una guía breve de Markdown"
categories: ["markdown", "guia"]
dropCap: true
displayInMenu: false
displayInList: true
draft: false
resources:
- name: featuredImage
  src: "MarkdownLogo.png"
  params:
    description: ""
---

"Si no documentas tu codig, no eres choquito"

# Cabeceras
Al igual que en HTML el markdown nos permite tener 6 niveles de cabeceras equivalentes a los h1 hasta el h6.

Lista de cabeceras

------

# Cabecera 1
## Cabecera 2
### Cabecera 3
#### Cabecera 4
##### Cabecera 5
###### Cabecera 6

# texto
**negrilla**
_cursiva_
~~tachado~~
# tablas
| nro | nombre |
| ---: | ----: |
| 1 | Juan carlos|
| 2 | Carlos perez |
| 3 | Maria perez |

# enlaces
**[mi pagina](http://google.com/)**

# Imágenes
![mi imagen](https://www.google.com/images/branding/googlelogo/1x/googlelogo_color_272x92dp.png)

# código

```shell
echo "HOLA MUNDO"
```

```javascript
const request = () => {
  return 'ABC';
}

```
Ejemplo en Python:
```python
print("hola mundo")
```
