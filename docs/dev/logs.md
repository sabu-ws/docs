# Logs

## Format des logs
```
Format
[TYPE] DATE HOUR    HOST (EXEC BY) MODULE ACTION : MESSAGE

Example
[DEBUG] 18/03/2024 21:46:23 sabu-server01 (system) FILES EXEC-SCRIPT : remove_old_files.sh was started to remove files older 10 days for /data

Field details
TYPE
=> DEBUG, INFO, WARN, CRITICAL

DATE HOUR
=> dd/mm/yyyy hh:mm:ss

HOST
=> (output command hostname)

EXEC BY
=> system (sabu), username (mbinet)

MODULE
=> SETTINGS, FILES, ENDPOINT, etc

ACTION
=> Executed action

MESSAGE
=> Details informations
```