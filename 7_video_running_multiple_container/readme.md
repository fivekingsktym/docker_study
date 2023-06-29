
# techtvm/mysql_techtvm
### image running configurations

```bash

docker run -dp 3306:3306 \
--name=db \
--network=app-network \
-e MYSQL_ROOT_PASSWORD='Pass@123' \
techtvm/mysql_techtvm \
mysqld --default-authentication-plugin=mysql_native_password

```


# techtvm/php-crud-app
### image running configurations

```bash 

docker run -dp 8081:80 \
--name=crud-app \
--network=app-network \
-e MYSQL_DBHOST='db:3306' \
-e MYSQL_DBUSER='root' \
-e MYSQL_DBPASS='Pass@123' \
-e MYSQL_DBNAME=php_crud techtvm/php-crud-app

```