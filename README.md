# Leuchten Rundgang

Kleine Web-App für den Campus-Rundgang. Du fotografierst Leuchten oder Steckdosen, gibst die Nummer vom Plan ein, und die Nummer landet auf dem Bild und im Dateinamen.

## Funktionen

- Foto mit der Handykamera aufnehmen
- Nummer eingeben, einzeln (z. B. 7) oder als Bereich (z. B. 1-5)
- Nummer wird direkt ins Bild gebrannt (unten links, mit Rahmen)
- Nummer steht auch im Dateinamen, z. B. `Leuchte_1-5_20260916_142530.jpg`
- Umschalten zwischen Leuchte und Steckdose
- Auto +1: nach jedem Foto zählt die Nummer automatisch weiter
- Schnellbereiche 1-3, 1-5, 1-10 und ein Bereich-Knopf (macht aus 3 den Bereich 3-7)
- Standort (GPS) pro Foto: Koordinaten werden gespeichert, unten rechts ins Bild gebrannt und in der Galerie als Karten-Link (Google Maps) angezeigt. Schalter zum Ausschalten, Statusanzeige mit Genauigkeit.
- Galerie mit allen Fotos, gespeichert im Browser (IndexedDB, offline verfügbar)
- Einzelnes Foto speichern, teilen oder löschen
- Alle Fotos gesammelt teilen oder herunterladen

## So nutzt du sie

1. Lege die 4 Dateien (`index.html`, `manifest.json`, `sw.js`, `icon.svg`) auf einen HTTPS-Server. Ohne HTTPS gibt die Handykamera keinen Zugriff (Ausnahme: localhost am Rechner).
   - Schnell und gratis: GitHub Pages. Aktiviere Pages im Repo, dann öffnest du die Seite unter der Pages-URL.
2. Öffne die Seite auf dem Handy im Browser (iPhone: Safari, Android: Chrome).
3. Erlaube den Kamerazugriff.
4. Optional: über das Browser-Menü "Zum Home-Bildschirm" installieren, dann startet sie wie eine App.

## Bedienung

- Oben Leuchte oder Steckdose wählen.
- Nummer im Feld eintippen oder mit − und + anpassen. Bei einem Bereich wie 1-5 verschiebt + den ganzen Bereich auf 2-6.
- Auf den grossen weissen Knopf tippen: Foto wird aufgenommen und gespeichert.
- Reiter Galerie zeigt alle Fotos. Tippe ein Foto an zum Ansehen, Speichern, Teilen oder Löschen.

## Hinweise

- Für GPS musst du den Standortzugriff im Browser erlauben. Der erste Fix im Freien dauert wenige Sekunden, drinnen ist er ungenauer. Die Statusanzeige zeigt die Genauigkeit in Metern.
- Die Fotos liegen nur lokal im Browser. Lösche die Browserdaten nicht, bevor du sie exportiert hast.
- Zum Sichern: in der Galerie "Alle laden" nutzen und die Bilder ins Fotoalbum oder in einen Ordner übernehmen.
