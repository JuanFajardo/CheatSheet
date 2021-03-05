# MySQL


__mysqld__ 	El executable del servidor

__mysql__	Es la linea de comandos del cliente

__mysqladmin__	Es una utilidad de mantenimiento o administracion



## Basico

__Mostrar Base de Datos__

```sql
> show databases;
```

__Crear una Base de Datos__

```> create database baseDatos;```

__Crear una Tabla__

```>  create table autor(id int primary key auto_increment, autor varchar(50));```

```> insert into autor values('', 'Julio Verne');```

```> select * from autor;```

__Crear una Tabla con Cable Foreanea__

```>  create table libro( id  int primary key auto_increment, libro varchar(50), autor_id int, foreign key (autor_id) references autor(id_autor) );```



## Usuarios

__Crear un usuario__

```> CREATE USER 'bett0'@'localhost' IDENTIFIED BY '123';```


__Privilegio a nivel de base de datos__

```> grant select,insert,update on db.* to bett0@'192.168.70.60' identified by '123';```

__Privilegio a nivel de tabla__

```> grant select on db.libro to bett1@'%'  identified by '123';```

__Privilegio a nivel de columna__

```> grant update(autor) on db.autor to bett2@'localhost' identified by '123';```



__Asignar a un usuario límites__

```sql
> GRANT ALL ON test.* TO 'prueba'@'localhost'
       WITH MAX_QUERIES_PER_HOUR 100
       MAX_UPDATES_PER_HOUR 50
       MAX_CONNECTIONS_PER_HOUR 100
       MAX_USER_CONNECTIONS 20;
```

__Modificar límites de un usuario__

```> GRANT USAGE ON *.* TO 'prueba'@'localhost'```
      ```WITH MAX_QUERIES_PER_HOUR 50;```


__Eliminar un límite (poner a 0)__

```> grant usage on *.* to 'bett0'@'localhost' with max_queries_per_hour 0;```

__Poner a 0 los contadores a nivel general__

```> flush user_resources;```

```> flush privileges;```



## Reset 

__Resetear contraseña de mysql Windows__

```$ mysqld_safe --skip-grant-tables &```

```$ mysqld --skip-grant-tables &```

```$ mysql -u root mysql```

```> update user SET password=PASSWORD("123") WHERE user="root"; $ FLUSH PRIVILEGES;```



## Exportar e Importar

__Exportar Base Datos__

```$ mysqldump -u bett0 -p  -h 192.168.1.69 [db] > archivo.sql ```

__Importar A una base de datos__

```$ mysql -u bett0 -p  -h 192.168.1.69 [db] < archivo.sql```



## Mysql Errores 

__Aria engine is not enabled...__ 

```$ cd /var/lib/mysql```

```$ mv aria_log_control aria_log_control.moved```


## Mysql Servidor no levanta(estamos fregados - MySQL (MariaDB) Not Starting [closed])

```bash
# cd /var/lib/mysql

# ls

# rm -r *

# mysql_install_db --user=mysql --basedir=/usr --datadir=/var/lib/mysql

# systemctl start mysqld

# systemctl start mysql.service

# systemctl start mariadb

# mysql
```
