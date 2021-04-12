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
postgres@localhost$ pg_dump -U bett0 -W -h loclahost baseDatos > /tmp/baseDatos.sql

postgres@localhost$ pg_dump -U bett0 -W -h 192.168.69.69 --table public.tabla baseDatos > /tmp/baseDatos.sql
```

__Exportar Una Tabla__

```bash
pg_dump --host localhost --port 5432 --username postgres --format plain --verbose --file "<abstract_file_path>" --table public.tablename dbname                                                               
```

__Importar BaseDeDatos__
```bash
postgres@localhost$ psql -U bett0 baseDeDatos < /tmp/baseDatos.sql > pg_mibd.log 2>&1

postgres@localhost$ psql -U bett0 -W -h 192.168.69.69 --table public.tabla baseDatos < /tmp/baseDatos.sql
```

