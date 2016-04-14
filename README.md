Jarves Standard Edition
========================

Jarves standard edition is a Symfony standard edition 3.0 + Jarves installed.

All you need to do to run Jarves is:

```
git clone git@github.com:jarves/jarves-standard.git
cd jarves-standard

composer install

php bin/console propel:model:build #build base model

php bin/console propel:migration:diff #generates a database schema diff
php bin/console propel:migration:up #upgrade the database schema

### Installs demo data

php bin/console jarves:install:demo 127.0.0.1 /
``` 

### Run

`php bin/console server:run`


open http://127.0.0.1:8000/jarves.

