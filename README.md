# uchile-robotics.github.io
Web Page for uchile robotics projects

## Descripción

Este repositorio mantiene el código de la página oficial del equipo UChile Homebreakers y el equipo UChile Peppers.

La página es hosteada en dos servidores:

- [Servidor de Desarrollo](https://uchile-robotics.github.io/): GitHub Pages. Contiene la última versión de la página, tal como está hosteada en GitHub.
- [Servidor Oficial](http://robotica-uchile.amtc.cl/): Hosteado en la AMTC. Contiene un snapshot del repositorio, en algún commit considerado *oficial*.


## Desarrollo de la página

La página se desarrolla de acuerdo a los requerimientos de [GitHub Pages](https://pages.github.com/), por lo que sólo contiene código estático: html, css y javascript; además de utilizar [Jekyll](https://jekyllrb.com/) como framework para generar la página estática.

### Prerequisitos

#### Intall Jekyll 3.2.1 and Ruby 2.2.3 on Ubuntu 14.04

```bash
cd
git clone git://github.com/sstephenson/rbenv.git .rbenv
echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.bashrc
echo 'eval "$(rbenv init -)"' >> ~/.bashrc
git clone git://github.com/sstephenson/ruby-build.git ~/.rbenv/plugins/ruby-build
echo 'export PATH="$HOME/.rbenv/plugins/ruby-build/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc 
rbenv install -v 2.2.3
rbenv global 2.2.3
ruby -v
echo "gem: --no-document" > ~/.gemrc
gem install bundler
gem install jekyll
ruby -v
gem -v
``` 

#### Descargar este repositorio

Debes descargar este repositorio para poder aplicar cambios en la página. Por defecto, el repositorio es descargado al instalar **uchile_ws**, en el directorio: `<uchile_ws>/misc/webpage`


### Desarrollo y test

Cada commit subido (push) al repositorio será automáticamente compilado por GitHub pages. Los cambios se podrán ver en la página de desarrollo unos minutos tras el commit.

Para evitar realizar commits constantemente, se recomienda fuertemente el uso de un servidor local de desarrollo, basado en Jekyll. Para ver el resultado de los cambios, se puede utilizar:

```bash
cd <uchile_ws>/misc/webpage
bundle exec jekyll serve
```

Con lo esto, tendrán corriendo una versión local del servidor, el que compilará y se actualizará automátimente con todos los cambios realizados en los archivos. Generalmente, la URL de la página local será `http://127.0.0.1:4000/`.


## Servidor oficial

Para acceder al servidor oficial se recomienda el uso de un gestor FTP, como FileZilla.

- En primer lugar se debe compilar la página web mediante Jekyll (es automático la usar `jekyll serve`).
- Los archivos a subir ar servidor se encuentran en `<uchile_ws>/misc/webpage/_site`. Se deben copiar todos los contenidos de la carpeta al servidor oficial.

Notar que el servidor oficial además puede contener otros directorios con archivos subidos manualmente, que no son parte del repositorio, tal como archivos multimedia.

## Consideraciones IMPORTANTES

- Evitar a toda costa subir archivos que no sean código a la página web: imágenes, video, pdfs, etc. Especialmente si éstos pesan más de 1MB. Los archivos son hosteados en el servidor oficial y deben ser subidos manualmente mediante FTP.


## Troubleshooting

jekyll 3.3.1 | Error:  Could not find a JavaScript runtime. See https://github.com/rails/execjs for a list of available runtimes.
```
gem install execjs
sudo apt-get install nodejs

```
