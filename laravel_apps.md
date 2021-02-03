# Windows 10 for Laravel Development

## Requirements

- choco
- code

## Install PHP and Composer

`sudo choco install php`

`sudo choco install composer`

- add to path

```
C:\tools\php80
C:\ProgramData\ComposerSetup\bin
C:\Users\masterpowers\AppData\Roaming\Composer\vendor\bin
```

## Install Laravel 

`composer global require laravel/installer`

## Install Laravel Valet

`composer global require cretueusebiu/valet-windows`

## Install Laravel Expose

`composer global require beyondcode/expose`

## to edit php.ini

locate the file with

`php --ini`

results:

```
Configuration File (php.ini) Path:
Loaded Configuration File:         C:\tools\php80\php.ini
Scan for additional .ini files in: (none)
Additional .ini files parsed:      (none)
```

edit it
code `C:\tools\php80\php.ini`

## Enable Extensions

```
extension=php_curl.dll
extension=php_fileinfo.dll
extension=php_mbstring.dll
extension=exif      ; Must be after mbstring as it depends on it
extension=php_mysqli.dll
extension=php_openssl.dll
extension=php_pdo_sqlite.dll
extension=php_sqlite3.dll
```

## Install MYSQL

`sudo choco install mysql`

`sudo choco install mysql.workbench`

- add to path

```
C:\Program Files\MySQL\MySQL Server 8.0\bin
C:\Program Files\MySQL\MySQL Shell 8.0\bin
C:\Program Files\MySQL\MySQL Workbench 8.0 CE\
```

## Install postgresql

`sudo choco install postgresql`

## Install Sqlite3

`sudo choco install SQLite`



