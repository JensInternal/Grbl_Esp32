22.02.2021 v2.6.1

Fertig compilierte Grbl_ESP32 Firmware mit allen zugehörigen Dateien.

Erstellung eines Releases
- git switch main (mein Grbl_Esp32 Repository, Branch "main")
- git fetch upstream --dry-run (das Repository von Bart Dring, erstmal Trockenübung)
  Änderungen anschauen
- git fetch upstream  (das Repository von Bart Dring, erstmal Trockenübung)
- git log --oneline BartMain main
- Compilieren
  - "Build env:release" in VSCode
- Testen
- Dateien aus dem WebUI in das Verzeichnis "JH_Release" kopieren
  - macrocfg.json
  - preferences.json
- Anpassen dieser readme.txt
- git add -A (alle Änderungen integrieren)
- git merge BartMain (mein lokales Repository und das von Bart GitHub mergen)
  Merge "bdring/Grbl_Esp32, Branch main" in mein GitHub Repository "JensInternal/Grbl_Esp32, Branch main"
- git tag -a v2.6.z -m "Version note" (die Versionen fangen immer mit 2.6. an, solange die Hardware identisch bleibt)
- git commit -am "Release Notes"
- git push origin

Was macht dieses Release aus?
GitHub Repository "JensInternal/Grbl_Esp32, Branch main", Tag v.2.6.1 mit allen Dateien des Releases
- index.html.gz       (die Datei ist ebenfalls im Projektordner unter "Grbl_Esp32/data/index.html.gz")

Versionsgeschichte
- v2.6.1 22.02.2021 Initiales Release