# PostgreSQL
Erklärung zu diversen Datenbank Themen.

## Anlegen eines neuen Clusters
Bei PostgreSQL ist es möglich mehrere "Datenbanken" in unterschiedlichen
Speicherorten abzulegen; Diese werden dann als "Cluster" bezeichnet.
Im Prinzip kann man sagen, dass pro Cluster mehrere Datenbanken eingerichtet
werden können.
Interessant wird die Sache, falls man die Version von Postgres updaten will und
vorher prüfen möchte, ob alles noch in der neuen Version funktioiert.

Aber nun zum Eigentlichen...

### Übersicht der Cluster
```bash
pg_lsclusters
```

### neuen Cluster anlegen
```bash
pg_createcluster -d /pfad/zur/datenbank/lokation VERSION NAME
```

Die Konfigurationsdateien befinden sich dann unter `/etc/postgresql/VERSION/NAME`

### Cluster starten/stoppen/status
```bash
pg_ctlcluster VERSION NAME start
pg_ctlcluster VERSION NAME stop
pg_ctlcluster VERSION NAME restart
pg_ctlcluster VERSION NAME reload
pg_ctlcluster VERSION NAME status
```
