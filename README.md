# tools
Tools develop

Microsoft Visual C++ 2015
https://www.microsoft.com/en-us/download/details.aspx?id=53840

Install Apache2 as services

$>httpd.exe -k install -n "Apache2"

$>httpd.exe -k uninstall

------------------------------------------------------------------
Config php into apache2
httpd.conf

```bash
#
# PHP-Module setup
#
LoadFile "C:/php/php7ts.dll"
LoadModule php7_module "C:/php/php7apache2_4.dll"

<FilesMatch "\.php$">
    SetHandler application/x-httpd-php
</FilesMatch>
<FilesMatch "\.phps$">
    SetHandler application/x-httpd-php-source
</FilesMatch>
```

Install mongodb on windows

create

mongodb/bin/mongod.cnf

    systemLog:
        destination: file
        path: D:/www/mongodb/data/log/mongod.log
    storage:
        dbPath: D:/www/mongodb/data/db
    
mongodb/data/log
mongodb/data/db

Run command install mongodb as services (Administrative Privileges)

```
$>D:\www\mongodb\bin\mongod.exe --config D:\www\mongodb\bin\mongod.cfg --install
```

Install MySQL

    $>D:\www\MySQL\MySql\bin\mysqld --install MySQL 
