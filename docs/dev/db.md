# Base de données
!!! warning "Warning"

    Operations carried out on the database can have **irreversible consequences** in the event of incorrect handling.  
    Please perform these actions knowingly or if it has been clearly indicated by the SABU development team.

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
!!! danger "Danger"

    This operation should only be carried out in the event of a major problem with the database.  
    **All data will be deleted**.

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