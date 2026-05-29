# Jura-Repetitor – Setup-Anleitung für Anja

## Einmalige Einrichtung (ca. 10 Minuten)

### Schritt 1: Repo forken

1. GitHub-Konto anlegen oder einloggen unter [github.com](https://github.com)
2. Original-Repo öffnen: [github.com/i-lynus/Jura-Repetitor](https://github.com/i-lynus/Jura-Repetitor)
3. Oben rechts auf **Fork** klicken → **Create fork**
4. Du hast jetzt eine eigene Kopie unter `github.com/DEIN-NAME/Jura-Repetitor`

---

### Schritt 2: Automatische Synchronisation einrichten

1. In deinem Fork auf **Add file → Upload files** klicken
2. Im Fork-Repo den Ordner `.github/workflows/` anlegen (einfach den Pfad beim Upload eingeben)
3. Die Datei `sync-upstream.yml` (aus diesem Ordner) dort hochladen
4. Commit bestätigen

Ab sofort synchronisiert GitHub Actions täglich um 06:00 UTC automatisch alle Updates vom Original-Repo in deinen Fork.

---

### Schritt 3: Streamlit Cloud einrichten

1. Öffne [app.streamlit.io](https://app.streamlit.io) und melde dich mit GitHub an
2. Klicke auf **New app**
3. Wähle: **GitHub → dein Fork → Branch: main → Datei: app.py**
4. Klicke auf **Advanced settings** und trage folgende Secrets ein:

| Secret-Name        | Wert                                      |
|--------------------|-------------------------------------------|
| `ANTHROPIC_API_KEY` | Dein API-Schlüssel von Anthropic         |
| `GITHUB_TOKEN`     | Dein persönlicher GitHub-Token            |
| `GITHUB_DATA_REPO` | z. B. `DEIN-NAME/jura-daten`             |
| `GITHUB_DATA_BRANCH` | z. B. `main`                            |
| `ADMIN_USER`       | Benutzername für den Admin-Bereich        |
| `ADMIN_PASSWORD`   | Passwort für den Admin-Bereich            |

5. Klicke auf **Deploy** – die App ist in wenigen Minuten erreichbar.

---

### Ab sofort: kein manuelles Hochladen mehr

- Updates vom Original kommen **automatisch jeden Tag** in deinen Fork.
- Streamlit Cloud erkennt die Änderungen und aktualisiert die App selbstständig.

---

### Manuelles Update sofort auslosen

Falls du nicht bis 06:00 UTC warten willst:

1. In deinem Fork auf **Actions** klicken
2. Links "**Sync from upstream (i-lynus/Jura-Repetitor)**" auswählen
3. **Run workflow** → **Run workflow** klicken
4. Nach ca. 1 Minute ist der Fork auf dem neuesten Stand.
