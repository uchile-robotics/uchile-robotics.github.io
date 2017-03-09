# uchile-robotics.github.io
Web Page for uchile robotics projects

Intall Jekyll 3.2.1, Ruby 2.2.3 install on Ubuntu 14.04
=======================================================

```
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

Subir pagina

# crear servidor local
bundle exec jekyll serve

# compilar pagina en site_
bundle exec jekyll build

copiar/pegar archivos de _site en carpeta de pagina