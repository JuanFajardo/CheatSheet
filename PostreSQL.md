# Postgres


## Archivos de configuracion

__Herramienta de conexion listen_addresses__


```bash
postgres@localhost$ vim /etc/postgres/N.N/main/postgresql.conf
```

__Administracion de login de BaseDeDatos__

```bash
postgres@localhost$ vim /etc/postgres/N.N/main/pg_hba.conf
```


__Exportar Una BaseDeDatos__

```bash
postgres@localhost$ g_dump -U bett0 -W -h loclahost baseDatos > /tmp/baseDatos.sql
```


__Exportar Todas BaseDeDatos__
```bash
postgres@localhost$ pg_dumpall -U postgres > pg_todo.sql
```

__Importar BaseDeDatos__
```bash
postgres@localhost$ psql -U bett0 baseDeDatos < /tmp/baseDatos.sql > pg_mibd.log 2>&1
```

