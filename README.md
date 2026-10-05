# ATOSS / ASES Dienstplan Converter PWA

Diese Progressive Web App (PWA) konvertiert Dienstplan-PDFs aus dem Krankenhaussystem ATOSS / ASES vollständig offline in das iCalendar-Format (`.ics`) für iOS und Android.

## Features
- **100% Offline & DSGVO-sicher:** Die PDF-Verarbeitung erfolgt ausschließlich lokal im Browser-RAM mittels Mozilla PDF.js. Keine Daten verlassen das Gerät.
- **PWA Ready:** Installierbar auf iOS (via "Zum Home-Bildschirm hinzufügen") und Android/Desktop (via Browser-Prompt).
- **Intelligente Schichterkennung:** Erkennt Tagesschichten, Nachtschichten und Schicht-Überschneidungen automatisch.
- **Benutzerdefinierte Erinnerungen:** Ermöglicht das Setzen von Vorab-Alarmen/Erinnerungen für Schichten.
- **Modernes UI:** iOS-orientiertes Bento-Grid-Design mit vollem Dark-Mode-Support.

## Deployment auf GitHub Pages
Dieses Projekt ist darauf ausgelegt, direkt als statische Website gehostet zu werden.

1. Erstelle ein neues, leeres Repository auf GitHub.
2. Lade alle Dateien aus diesem Verzeichnis (`index.html`, `manifest.json`, `sw.js`, `icon.svg`, `README.md` sowie den `lib`-Ordner) in das Repository hoch.
3. Gehe in deinem GitHub-Repository zu **Settings > Pages**.
4. Wähle unter **Source** den Branch `main` (oder `master`) und als Ordner `/ (root)` aus.
5. Klicke auf **Save**. Deine App ist in wenigen Minuten unter `https://<dein-nutzername>.github.io/<repo-name>/` erreichbar.

## Lokale Entwicklung
Um die PWA lokal zu testen, starte einen simplen Webserver im Projektverzeichnis, z.B. mit Python oder Node.js:
- Python 3: `python -m http.server 8000`
- Node.js (http-server): `npx http-server -p 8000`

## Architektur & Bibliotheken
- **PDF-Parsing:** [PDF.js](https://mozilla.github.io/pdf.js/) von Mozilla (lokal eingebunden in `/lib`).
- **Styling:** Vanilla CSS (CSS Variables, Flexbox, Grid)
- **App-Logik:** Vanilla JavaScript (ES6+ Modules, File API, LocalStorage API, Service Worker API).
