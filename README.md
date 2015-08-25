# MySQL plugin for Dokku

## Installation

```
cd /var/lib/dokku/plugins
git clone https://xxxx mysql
dokku plugins-install
```


init)
mysql="mysql -u root --password=$admin_pw mysql"

_mysql "CREATE USER 'root'@'localhost' IDENTIFIED BY '$admin_pw'; FLUSH PRIVILEGES;" "$mysql"
_mysql "GRANT ALL PRIVILEGES ON *.* to 'root'@'localhost' IDENTIFIED BY '$admin_pw' WITH GRANT OPTION; FLUSH PRIVILEGES;" "$mysql"
_mysql "CREATE USER 'root'@'%' IDENTIFIED BY '$admin_pw'; FLUSH PRIVILEGES;" "$mysql"
_mysql "GRANT ALL PRIVILEGES ON *.* to 'root'@'%' IDENTIFIED BY '$admin_pw' WITH GRANT OPTION; FLUSH PRIVILEGES;" "$mysql"
;;

## Commands
```
$ dokku help
    mysql:create   <database>               Create a MySQL database
    mysql:delete   <database>               Delete specified MySQL database
    mysql:url      <database>               Get DATABASE_URL for <database>
    mysql:console  <database>               Launch a MySQL console for a given database
    mysql:dump     <database> > <filename>  Dump database to SQL format
    mysql:restore  <database> < <filename>  Restore database from SQL format
```
