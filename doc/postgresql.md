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
