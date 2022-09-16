## Instllation
https://www.youtube.com/watch?v=wTqosS71Dc4

## Set up on Heroku
https://dev.to/prisma/how-to-setup-a-free-postgresql-database-on-heroku-1dc1

## Commands from Terminal

### Creating user
```terminal
sudo -u postgres createuser <username>
```

### Creating database
```terminal
sudo -u postgres createdb <dbname>
```



## Commands in Postgres
### Setting user password
```postgres
psql=# alter user <username> with encrypted password '<password>';
```

### Granting privileges on database
```postgres
psql=# grant all privileges on database <dbname> to <username> ;
```
### List out users
```postgres
\du
```

### Connect to DB
```postgresql
psql postgres://[username]@localhost/5432/[db_name]
```

### Check where we are
```postgresql
\conninfo
```

### Quit
```
\q
```
