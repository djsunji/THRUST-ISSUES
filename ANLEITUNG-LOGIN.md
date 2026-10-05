# Login mit Apple, Google, Microsoft und Facebook einrichten

JetQ nutzt dafür Firebase Authentication (kostenlos im Spark-Plan). Solange `firebase-config.json` leer ist, zeigen die Buttons einen Hinweis und die Anmeldung mit Name und E-Mail funktioniert wie bisher.

## 1. Firebase-Projekt
1. https://console.firebase.google.com öffnen, "Projekt hinzufügen", z.B. `jetq`.
2. Projektübersicht, Web-App hinzufügen (Symbol `</>`). Die angezeigten Werte `apiKey`, `authDomain`, `projectId`, `appId` in `firebase-config.json` eintragen. Diese Werte sind öffentlich gedacht, kein Geheimnis.
3. Authentication, Einstellungen, Autorisierte Domains: deine GitHub-Pages-Domain hinzufügen (z.B. `deinname.github.io`).

## 2. Anbieter aktivieren (Authentication, Sign-in method)
- **Google**: nur aktivieren, fertig.
- **Microsoft**: in https://portal.azure.com eine App-Registrierung anlegen (Kontotypen: alle Microsoft-Konten). Redirect-URI = die Callback-URL, die Firebase anzeigt. Client-ID und ein Client-Secret in Firebase eintragen.
- **Facebook**: unter https://developers.facebook.com eine App (Typ Consumer) mit Facebook Login anlegen. App-ID und App-Secret in Firebase eintragen, die Firebase-Callback-URL bei Facebook als gültige OAuth-Redirect-URI eintragen. App auf "Live" schalten.
- **Apple**: braucht ein kostenpflichtiges Apple Developer Konto (99 USD/Jahr). Services ID und Key mit "Sign in with Apple" erstellen, Domain und Firebase-Callback-URL eintragen, Team-ID, Key-ID und privaten Schlüssel in Firebase hinterlegen.

## 3. Hochladen
`firebase-config.json` mit den Werten ins Repository hochladen. Nach dem nächsten Laden der Seite funktionieren die Buttons unter Profil.

Hinweis: Der Fortschritt wird in der GitHub-Version weiterhin im Browser gespeichert. In claude.ai erkennt JetQ dich automatisch über dein Claude-Konto, dort sind die Anbieter-Buttons nur Hinweis.
