# JetQ – Refresher for Embraer Pilots

Selbsttest- und Lernseite für Pilotinnen und Piloten auf **Embraer E2** (E190-E2/E195-E2) und **Embraer E1** (E190/E195).
Alle Fragen, Fakten, Fachartikel und Memory Items stammen aus den Handbüchern (AFM, AOM, OM-A, OM-B, MEL), jeweils mit Fundstelle und Originalabschnitt.

## Inhalt

| Datei | Zweck |
|---|---|
| `index.html` | Die komplette Seite (HTML, CSS und JavaScript in einer Datei) |
| `fragen.json` | Fragenkatalog, Bibliothek, Fachartikel, Memory Items, Saisontests (DE/EN) |
| `aircraft-e1.jpg`, `aircraft-e2.jpg`, `cockpit-e1.jpg`, `cockpit-e2.jpg` | Fotos auf der Startseite |
| `jetq-logo-*.png` | Logo hell und dunkel, gross und klein |
| `.nojekyll` | Damit GitHub Pages die Dateien unverändert ausliefert |

## Veröffentlichen mit GitHub Pages

1. Neues Repository auf GitHub anlegen, am besten **privat** (siehe Hinweis unten).
2. Alle Dateien aus diesem Ordner hochladen (inklusive `.nojekyll`).
3. Unter **Settings → Pages** als Quelle den Branch `main` und den Ordner `/ (root)` wählen.
4. Nach etwa einer Minute ist die Seite unter `https://<benutzername>.github.io/<repository>/` erreichbar.

## Lokal testen

Die Seite lädt `fragen.json` per `fetch`, deshalb funktioniert ein Doppelklick auf `index.html` nicht. Stattdessen im Ordner einen kleinen Webserver starten:

```bash
python3 -m http.server 8000
```

und `http://localhost:8000` im Browser öffnen.

## Gut zu wissen

- **Profil und Statistik** werden ausserhalb von claude.ai im Browser gespeichert (localStorage), also pro Gerät und Browser. Eine echte Anmeldung (z. B. mit Apple, Google, Microsoft) braucht einen Dienst wie Firebase Authentication oder Auth0.
- Der Hinweis im Profil, dass die Anmeldung über das Claude-Konto läuft, gilt nur für die Version auf claude.ai.
- **Vertraulichkeit:** Die Inhalte zitieren firmeninterne Handbücher. Das Repository deshalb privat halten oder den Zugriff auf die Crew beschränken. GitHub Pages aus einem privaten Repository braucht einen kostenpflichtigen GitHub-Plan.
- Sprachen: Deutsch und Englisch, Umschaltung oben rechts. Tag- und Nachtmodus folgen dem System oder dem Schalter oben rechts.
