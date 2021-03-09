Fertig compilierte Grbl_ESP32 Firmware mit allen zugehörigen Dateien.

Erstellung eines Releases
- git switch main (mein Grbl_Esp32 Repository, Branch "main")
- git fetch origin --tags (mein Repository)
- git fetch upstream --dry-run (das Repository von Bart Dring, erstmal Trockenübung)
  Änderungen anschauen
- git fetch upstream  (das Repository von Bart Dring, erstmal Trockenübung)
- git log --oneline BartMain main
- Compilieren
  - "Build env:release" in VSCode
- Testen
- Dateien aus dem WebUI in das Verzeichnis "JH_Release" kopieren oder hier anpassen
  - macrocfg.json
  - preferences.json
  - firmware.bin aus „.pio\build\release\firmware.bin“
- Anpassen dieser readme.txt mit neuer Versionsgeschichte
- git add -A (alle Änderungen integrieren)
- git merge BartMain (mein lokales Repository und das von Bart GitHub mergen)
  Merge "bdring/Grbl_Esp32, Branch main" in mein GitHub Repository "JensInternal/Grbl_Esp32, Branch main"
- git tag -a v2.6.z -m "Release note" (die Versionen fangen immer mit 2.6. an, solange die Hardware identisch bleibt)
- git commit -am "Release Notes"
- git push origin --tags
- Firmware hochladen (OTA durch den Button PlatformIO:Upload) und macrocfg.json/preferences.json über das WebUI in den ESP32 hochladen

Welche extra Dateien gehören zu diesem Release?
- GitHub Repository "JensInternal/Grbl_Esp32, Branch main", Tag v.2.6.1 mit allen Dateien des Releases
- index.html.gz (die Datei ist im Projektordner unter "Grbl_Esp32/data/index.html.gz")
- firmware.bin („.pio\build\release\firmware.bin“)
- JH_Release/macrocfg.json (manuell runter- / hochladen über das WebUI)
- JH_Release/preferences.json (manuell runter- / hochladen über das WebUI)
- JH_Release/readme.txt (diese Datei)

Versionsgeschichte
- v2.6      22.02.2021 Initiales Release mit Ordner "JH_Release" und allen relevanten config-Dateien
  Sorotec Z Probe von 40.8mm auf 40.9mm
- v2.6.0.1  23.02.2021 Sorotec Z Probe läuft 2x, schnell u. dann langsam
- v2.6.0.2  09.03.2021 Akt. Merge mit Bart, M30=Z up