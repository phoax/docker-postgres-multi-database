# PostgreSQL with multi databases and pgAdmin

A docker-compose file to setup a PostgreSQL database with pgAdmin4.

Database tables are declared in `docker_postgres_init.sql` and created at start up.

## Start containers

Execute:

```
docker-compose up
```

## pgAdmin

### Connect to pgAdmin

Got to:

```
http://localhost:5050/
```

Login on pgadmin with

| attribute | value                  |
| --------- | ---------------------- |
| login     | `postgres@pgadmin.org` |
| password  | `admin`                |

### Access database tables on pgAdmin

Click on `Add New Server`

On General, add:

| attribute | value       |
| --------- | ----------- |
| Name      | `mymultidb` |

On Connection, add:

| attribute            | value       |
| -------------------- | ----------- |
| Hostname/address     | `postgres`  |
| Port                 | `5432`      |
| Maintenance database | `postgres`  |
| Username             | `postgres`  |
| Password             | `Welcome01` |
| Save password?       | `checked`   |

## database connections

The two database connections are:

### mydb_1

| attribute | value       |
| --------- | ----------- |
| hostname  | `localhost` |
| database  | `mydb_1`    |
| port      | `5432`      |
| username  | `postgres`  |
| password  | `Welcome01` |

### mydb_2

| attribute | value       |
| --------- | ----------- |
| hostname  | `localhost` |
| database  | `mydb_2`    |
| port      | `5432`      |
| username  | `postgres`  |
| password  | `Welcome01` |
