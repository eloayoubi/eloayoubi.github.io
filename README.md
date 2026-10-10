# eloayoubi.github.io

GitHub-Pages-Seite für die App **MyBoo** (Code im privaten Repo `eloayoubi/MyBoo`).

| Pfad | Zweck |
|---|---|
| `myboo/` | Landingpage der Einladungslinks `https://eloayoubi.github.io/myboo/?invite=<CODE>`. Mit installierter App öffnet iOS den Link direkt in MyBoo (Universal Link), sonst zeigt die Seite den Code und leitet einmal in den Store weiter. „In MyBoo öffnen“ nutzt `de.eloayoubi.myboo://join?invite=<CODE>`. |
| `.well-known/apple-app-site-association` | Erlaubt der App (`GYJLSZ9DRM.de.eloayoubi.myboo`) Links unter `/myboo/*` mit `invite`-Parameter. Apple lädt die Datei über sein CDN; Änderungen kommen mit Verzögerung bei den Geräten an. |
| `.nojekyll` | Ohne Jekyll liefert GitHub Pages auch den Ordner `.well-known` aus. |

Store-Ziele stehen oben im Skript von `myboo/index.html` (`TESTFLIGHT_URL`, `APP_STORE_URL`, `PLAY_URL`). Bis zum Release zeigt iOS auf den öffentlichen TestFlight-Link, danach `TESTFLIGHT_URL` leeren.

Android-App-Links bräuchten zusätzlich `.well-known/assetlinks.json` mit dem SHA-256 des Release-Schlüssels; bis dahin öffnet Android die Seite im Browser.
