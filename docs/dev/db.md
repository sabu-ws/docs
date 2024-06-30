# Base de données

## Init DB
```
cd /sabu
source sabu-venv/bin/activate
export FLASK_APP=/sabu/server/server.py
flask db init
```

## Update DB
```
cd /sabu/server
source /sabu/sabu-venv/bin/activate
flask db upgrade
```

## Erase and create DB
Erase
```
service sabu stop
su - postgres
psql
drop database sabu_db;
quit
```
Create
```
createdb sabu_db -O sabu_sql
service sabu start
```