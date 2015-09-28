# Wartung
Für eventuelle Serverwartungen, wie 
* Update von Icinga
* Update des Betriebssystem 
* Erstellen von Snapshots (Falls der Server innerhalb einer VM betrieben wird)
befindet sich unter `/usr/local/custom/` einmal eine `maintenance.motd` und
einmal eine `empty.motd`.

Um diese jeweils zu aktivieren:
```bash
% sudo ln -sf /usr/local/custom/maintenance.motd
# oder
% sudo ln -sf /usr/local/custom/empty.motd
```
