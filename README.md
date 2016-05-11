Jarves Standard Edition
========================

Jarves standard edition is a Symfony standard edition 3.0 + Jarves installed.

All you need to do to run Jarves is:

```
git clone git@github.com:jarves/jarves-standard.git
cd jarves-standard

composer install

php bin/console propel:model:build #build base model

vim app/config/config.jarves.xml #change database settings and `groupOwner`
# make sure your database exists (CREATE DATABASE foobar)

php bin/console propel:migration:diff #generates a database schema diff
php bin/console propel:migration:up #upgrade the database schema

### Installs demo data

php bin/console jarves:install:demo 127.0.0.1 /
``` 

### Install dependencies

#### SCSS

If not already installed (type `sass` on your console), you need to install sass: http://sass-lang.com/install

1. osx: sudo gem install sass
2. linux: sudo su -c "gem install sass"
3. windows: see http://sass-lang.com/install

If Jarves can not find the sass binary (by having wrong PATH variable set, that does not contain the path of `sass`, see `which sass`) the administration will be unstyled.

### Run

`php bin/console server:run`


open http://127.0.0.1:8000/jarves.

