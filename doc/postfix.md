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
- [x] Keine Konfiguration
- [ ] Internet-Site
- [ ] Internet mit Smwarthost
- [ ] Satellitensystem
- [ ] Nur lokal

## Konfiguration
### /etc/mailname
Sicherstellen, dass die Datei `/etc/mailname` den richtigen Eintrag hat.
Hier wird der hintere Teil nach dem `@` Zeichen festgelegt.

> Als Beispiel foo.bar  
> Eine Mail-Adresse würde dadurch dann "email@foo.bar" lauten.

---
### /etc/postfix/main.cf
Hat man bei der Installation `Keine Konfiguration` ausgewählt so kann man sich
die Grundkonfiguration aus `/usr/share/postfix/` kopieren.
```bash
cp /usr/share/postfix/main.cf.debian /etc/postfix/main.cf
```

## Tools
Für die Verwaltung von Postfix.

### Installation
Management der Queue.
```bash
sudo -E apt-get install pmailq
```
Dadurch installiert sich `postqueue` mit dem man sich eine Liste der Mails, die
noch nicht weggeschickt wurden, anzeigen lassen und diese Mails erneut
versenden kann.
```bash
sudo postqueue -p
sudo postqueue -f
```
E-mail aus der Queue löschen:
```bash
sudo postsuper -d QUEUEID
```
