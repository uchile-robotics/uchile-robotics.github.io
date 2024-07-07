# uchile-robotics.github.io
Web Page for uchile robotics projects

## Descripción

Este repositorio mantiene el código de la página oficial del equipo UChile Homebreakers y el equipo UChile Peppers.

La página es hosteada en dos servidores:

- [Servidor de Desarrollo](https://uchile-robotics.github.io/): GitHub Pages. Contiene la última versión de la página, tal como está hosteada en GitHub.
- [Servidor Oficial](http://robotica-uchile.amtc.cl/): Hosteado en la AMTC. Contiene un snapshot del repositorio, en algún commit considerado *oficial* (actualmente no esta funcionando),


## Desarrollo de la página

La página se desarrolla de acuerdo a los requerimientos de [GitHub Pages](https://pages.github.com/), por lo que sólo contiene código estático: html, css y javascript; además de utilizar [Jekyll](https://jekyllrb.com/) como framework para generar la página estática.

### Prerequisitos

#### Instalar la última versión de ruby y jekyll.

#### Descargar este repositorio

Basta con clonar el repositorio y compilarlo como un espacio de trabajo de jekyll, esto es, correr el comando `bundle install` en la carpeta del repositorio.


### Desarrollo y test

Cada commit subido (push) al repositorio será automáticamente compilado por GitHub pages. Los cambios se podrán ver en la página de desarrollo unos minutos tras el commit.

Para evitar realizar commits constantemente, se recomienda fuertemente el uso de un servidor local de desarrollo, basado en Jekyll. Para ver el resultado de los cambios, se puede utilizar:

```bash
bundle exec jekyll serve
```

Con lo esto, tendrán corriendo una versión local del servidor, el que compilará y se actualizará automátimente con todos los cambios realizados en los archivos. Generalmente, la URL de la página local será `http://127.0.0.1:4000/`.


## Servidor oficial

Para acceder al servidor oficial se recomienda el uso de un gestor FTP, como FileZilla.

- En primer lugar se debe compilar la página web mediante Jekyll (es automático la usar `jekyll serve`).
- Los archivos a subir ar servidor se encuentran en `/_site`. Se deben copiar todos los contenidos de la carpeta al servidor oficial.

Notar que el servidor oficial además puede contener otros directorios con archivos subidos manualmente, que no son parte del repositorio, tal como archivos multimedia.

## Consideraciones IMPORTANTES

- Evitar a toda costa subir archivos que no sean código a la página web: imágenes, video, pdfs, etc. Especialmente si éstos pesan más de 1MB. Los archivos son hosteados en el servidor oficial y deben ser subidos manualmente mediante FTP.