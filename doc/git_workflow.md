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
Alternativ kann man auch einen `leeren` Branch anlegen.
```bash
git checkout --orphan "leererBranch"
git rm -rf .
touch "neue_Datei_im_leeren_branch"
git add -A
git commit -a -m "Leere Datei angelegt."
```

Kontrollieren, ob es ein neues Update des git-Verzeichnis gibt und anschliessend durchführen.
```bash
git remote -v update
git status -uno
git pull
```
