# MySQL


El executable del servidor

__mysqld__ 

Es la linea de comandos del cliente

__mysql__

Es una utilidad de mantenimiento o administracion

__mysqladmin__

### Basico

__Mostrar Base de Datos__

```> show databases;```

__Crear una Base de Datos__

```> create database baseDatos;```


### Usuarios

__Crear un usuario__

```> CREATE USER 'bett0'@'localhost' IDENTIFIED BY '123';```

__Asigna a un usuario límites__

```> GRANT ALL ON test.* TO 'prueba'@'localhost'```
       ```WITH MAX_QUERIES_PER_HOUR 100```
            ```MAX_UPDATES_PER_HOUR 50```
            ```MAX_CONNECTIONS_PER_HOUR 100```
            ```MAX_USER_CONNECTIONS 20;```

__Modificar límites de un usuario__

```> GRANT USAGE ON *.* TO 'prueba'@'localhost'```
      ```WITH MAX_QUERIES_PER_HOUR 50;```


__Eliminar un límite (poner a 0)__
```> grant usage on *.* to 'bett0'@'localhost' with max_queries_per_hour 0;```

__Poner a 0 los contadores a nivel general__

```> flush user_resources;```

```> flush privileges;```

__Resetear contraseña de mysql__

```$ mysqld_safe --skip-grant-tables &```

```$ mysql -u root mysql```

```> update user SET password=PASSWORD("123") WHERE user="root"; $ FLUSH PRIVILEGES;```

### Exportar e Importar

__Exportar Base Datos__
```$ mysqldump -u bett0 -p  -h 192.168.1.69 [db] > archivo.sql ```

__Importar A una base de datos__
```$ mysql -u bett0 -p  -h 192.168.1.69 [db] < archivo.sql```


## Mysql Errores 

__Aria engine is not enabled...__ 

```$ cd /var/lib/mysql```

```$ mv aria_log_control aria_log_control.moved```
