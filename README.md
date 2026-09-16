# Leuchten Rundgang

Kleine Web-App für den Campus-Rundgang. Du fotografierst Leuchten, Steckdosen oder Verteilungen, gibst die Nummer vom Plan ein, und die Nummer landet auf dem Bild und im Dateinamen.

## Funktionen

- Kamera-Ansicht ohne Scrollen: Sucher und Bedienung passen auf eine Handy-Seite
- Foto mit der Handykamera aufnehmen
- Nummer über ein Zahlenfeld eingeben (öffnet sich direkt beim Tippen), einzeln (z. B. 7) oder als Bereich (z. B. 1-5)
- Nummer wird direkt ins Bild gebrannt
- Nummer steht auch im Dateinamen, z. B. `GebaeudeA_Leuchte_1-5_20260916_142530.jpg`
- Umschalten zwischen Leuchte, Steckdose und Verteilung (jeweils eigene Nummer)
- Optionaler Ort / Gebäude, wird mit abgespeichert und ins Bild geschrieben
- Auto +1: nach einem Einzelbild +1, nach einem Bereich der nächste Block (1-5 → 6-10)
- Schnellbereiche 1-3, 1-5, 1-10 und +5
- Zoom (1× / 1,5× / 2× / 3×), Taschenlampe wenn das Handy sie anbietet
- Standort (GPS) pro Foto: Koordinaten werden gespeichert, ins Bild gebrannt und in der Galerie als Karten-Link angezeigt
- Galerie mit Filter, Teilen, CSV-Liste (Art, Nummer, Ort, GPS) und Löschen
- Letztes Foto rückgängig (kurz nach der Aufnahme)
- Einstellungen bleiben erhalten (Nummer, Art, Ort, GPS, Auto +1)
- Offline als PWA (IndexedDB, Service Worker)

## So nutzt du sie

1. Lege die Dateien (`index.html`, `manifest.json`, `sw.js`, `icon.svg`) auf einen HTTPS-Server. Ohne HTTPS gibt die Handykamera keinen Zugriff (Ausnahme: localhost am Rechner).
   - Schnell und gratis: GitHub Pages. Aktiviere Pages im Repo, dann öffnest du die Seite unter der Pages-URL.
2. Öffne die Seite auf dem Handy im Browser (iPhone: Safari, Android: Chrome).
3. Erlaube den Kamerazugriff.
4. Optional: über das Browser-Menü "Zum Home-Bildschirm" installieren, dann startet sie wie eine App.

## Bedienung

- Oben Leuchte, Steckdose oder Verteilung wählen.
- Auf das Nummernfeld tippen: das Zahlenfeld öffnet sich. Bereiche gehen mit − oder den Schnellknöpfen.
- Auf den grossen weissen Knopf tippen: Foto wird aufgenommen und gespeichert.
- Reiter Galerie zeigt alle Fotos. Tippe ein Foto an zum Ansehen, Speichern, Teilen oder Löschen.

## Hinweise

- Für GPS musst du den Standortzugriff im Browser erlauben. Der erste Fix im Freien dauert wenige Sekunden, drinnen ist er ungenauer.
- Die Fotos liegen nur lokal im Browser. Lösche die Browserdaten nicht, bevor du sie exportiert hast.
- Zum Sichern: in der Galerie "Fotos teilen" oder "Liste.csv" nutzen.
