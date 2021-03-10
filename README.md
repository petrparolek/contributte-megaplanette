Pla.Nette
==========================

-----

This project is currently discontinued. Go to [blog.nette.org](http://blog.nette.org) or ask about more info at [@f3l1x](https://github.com/f3l1x) or [@chemix](https://github.com/chemix).

----

Note: Login page is : /sign/in and logout page /sign/out

Installation
------------

### 1) Get code

clone repository `git clone git@github.com:chemix/planette.git`


## 2) Composer

Install [Composer](http://getcomposer.org) and download dependencies via composer `composer.phar install`


### 3) Permissions

write for folders log and temp

```bash
chmod -R a+rw temp log
```

and for data

```bash
chmod -R a+rw www/data
```

### 4) App configuration

Copy file *app/config/config.local.template.neon* as *app/config/config.local.neon*
and update database credentials.

### 5) SQL init

default user is "architect" and password is "kreslo"

Run nextras migration script

```bash
./bin/console mig:res
```

### 6) Apache

update your file `etc/hosts` and add new line

`127.0.0.1 planette.loc`

apache/virtuals-list

```
<VirtualHost *:80>
    DocumentRoot "/Sites/planette/www/
    ServerName planette.loc
    ServerAlias plannete.192.168.1.111.xip.io
</VirtualHost>
```

For development
------------

### Node

install [Node](http://nodejs.org)

download dependencies via npm
```bash
npm install`
```

### Bower

install [Bower](http://bower.io)

download dependencies via composer
```bash
bower install`
```

### Grunt

install [Grunt](http://gruntjs.com)

build minimalized script file and stylesheets file
```bash
grunt
```

for development use

```bash```
grunt watch`
```
