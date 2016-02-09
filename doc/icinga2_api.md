# Icinga2 API

Hier wird im wesentlichen beschrieben, wie neue Hosts oder Services angelegt,
		 verändert oder gelöscht werden können.

Dazu wird eine Bash-Shell und das Programm `curl` benötigt.

neuen Host anlegen:
```bash
curl -k -s -u 'root' -H 'Accept: application/json' -X POST
'https://localhost:5665/v1/objects/hosts/NEUERHOST' -d '{ "templates": [
"generic-host" ], "attrs": { "address": "IP-ADRESSE", "check_command" :
				"hostalive", "vars.os" : "Linux" } }' | python -m json.tool
```

Zu Ändern sind natürlich die Begriffe `NEUERHOST` und `IP-ADRESSE`.
Erklärung zu den Parametern von curl:
Parameter | Erklärung
----------|-----------
-k				|	insecure: Erlaubt SSL Sites ohne gültigem Zertifikat.
-s				| silent: Unterdrück alle Ausgaben.
-u				| user: Username
-H				|	header LINE: Alternative "header Line" übergeben.
-X				| request: Welche Request-Methode soll benutzt werden.
-d				| data: HTTP-POST Daten anhängen.

angelegten Host ändern:
```bash
curl -k -s -u 'USER' -H ....
```

angelegten Host löschen:
```bash
curl -k -s -u 'USER' -H ....
```
