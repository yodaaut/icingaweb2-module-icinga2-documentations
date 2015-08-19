# Postfix
`Postfix` ist ein Mailserver basierend auf Linux.
Im weiteren Verlauf wird Postfix auf `Debian 8.1` installiert.

[//]: # (die Liste stimmt noch nicht ganz, sollte angepasst werden!)
Im Prinzip gibt es 2 Möglichkeiten einen Mailserver aufzusetzen.
* als Mail-Relay
* oder als Eigenständigen Mailserver

## Installation
Zuerst bringen wir das Debian System auf aktuellen Stand und installieren
anschliessend `postfix` aus dem Debian Repository
```bash
sudo -E apt-get update
sudo -E apt-get upgrade
sudo -E apt-get install postfix
```
> `sudo -E` wird deshalb verwendet, damit die `Environment-Variables`
> (Umgebungsvariablen) übernommen werden.
> Das macht zb. Sinn bei `Proxy Konfigurationen`

### Installationsparameter
Bevor die Installation beginnt muss man eine der `E-Mail-Server-Konfigurationen`
auswählen.
[] Keine Konfiguration
[] Internet-Site
[] Internet mit Smwarthost
[x] Satellitensystem
[] Nur lokal
> Durch Auswahl des Satellitensystem versendet Postfix E-Mails mittels externen
> SMTP

Als nächstes wird die FQDN für E-Mail-Adressen erfragt.
> Im Beispiel foo@bar.com wäre der FQDN
> bar.com

Als nächstes wird der `SMTP-Relay-Server` angegeben.

## Konfiguration
