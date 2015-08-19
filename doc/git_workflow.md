# Git Workflow

Neues Git-Verzeichnis anlegen
```bash
git init "neuesVerzeichnis"
```
oder ein bestehendes Git-Verzeichnis `clonen`
```bash
git clone http://foo/bar.git
```

In das neu angelegte Verzeichnis wechseln, neue Dateien anlegen und diese dann `hinzufügen` und `commiten`
```bash
cd "neuesVerzeichnis"
touch "neueDatei"
git add "neueDatei"
git commit "neueDatei" -m "Nachricht: zb.: Neue Datei angelegt"
```

Möchte man in einem neuen `Branch` weiter arbeiten, muss zuerst einer angelegt werden. Gewechselt wird zwischen den `Branches` mit `checkout`.
```bash
git branch "neuerBranch"
git checkout "neuerBranch"
```

