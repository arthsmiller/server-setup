# HOW TO SETUP DEBIAN SERVER

first, update and get some basic packages that may or not may be already installed:

> apt update && apt upgrade -y
> 
> apt install sudo fail2ban git curl nginx gpg neofetch htop tree certbot net-tools -y
> 
> shutdown -r now

change root password

> passwd

https://docs.docker.com/engine/install/debian/

https://www.passbolt.com/ce/debian

https://github.com/searxng/searxng-docker

if you have any subusers

> chsh -s /bin/bash username

## PHP

For php8.1 with extensions, use this link, or google

https://techlabs.blog/categories/debian-linux/install-php-8-1-for-nginx-on-debian-11

> apt install php-pgsql

optional (php installs apache2)

> systemctl disable apache2
> 
> apt remove apache2

## POSTGRES

postgres -> https://www.postgresql.org/download -> https://www.postgresql.org/docs/current/tutorial.html

> su postgres
> 
> psql
> 
> ALTER USER postgres PASSWORD 'pw';
> 
> CREATE DATABASE XXX;
>
> create new databse user with pw
> 
> grant all privileges to user to db

*or create the DB later*

## MISC

composer -> https://getcomposer.org/

node -> https://github.com/nodesource/distributions/blob/master/README.md

symfony-cli -> https://symfony.com/download

# in project: 

git clone your project, or create it

> chown -R www-data:www-data folderName

nginx conf -> symfony docs (change domain, root dir and php-fpm socket!)

## .env

> APP_ENV=dev
> 
> DATABASE_URL="postgres://db_user:db_pw@127.0.0.1:5432/db_name"

> composer install

make migrations and migrate them

> npm -g install yarn
>
> yarn install
>
> yarn add some packages
> 
>> copy packages to assets folder & import in app.js
>
> yarn watch
