# WohnGefühl – Infoseite für GitHub Pages

Statische Seite ohne JavaScript, Cookies, Tracking oder externe Schriften.
Sie dient als Website- und Datenschutz-URL für den Pinterest-Developer-Antrag.

## Live

- Startseite: https://verengy.github.io/wohngefuehl/
- Datenschutz: https://verengy.github.io/wohngefuehl/datenschutz.html
- Impressum: https://verengy.github.io/wohngefuehl/impressum.html
- Repository: https://github.com/Verengy/wohngefuehl

## Angaben

Impressum und Datenschutz enthalten aktuell:

- Matthias Kaufmann
- Breiteweg 20
- 39387 Oschersleben
- matzek22@icloud.com

Bei einer Änderung beide Dateien (`datenschutz.html`, `impressum.html`) anpassen.

## Änderungen veröffentlichen

Dieser Ordner ist die Arbeitskopie. Das öffentliche Repo ist eine Kopie davon.
Nach Änderungen:

```bash
rsync -a --delete --exclude .git site/ /tmp/opencode/wohngefuehl-publish/
cd /tmp/opencode/wohngefuehl-publish
git add -A
git commit -m "Infoseite aktualisieren"
git push origin main
```

GitHub Pages baut danach automatisch neu (ca. 1–2 Minuten).

## Erstmalige Einrichtung (falls das Repo neu aufgesetzt werden muss)

1. Öffentliches Repo `wohngefuehl` anlegen
2. Dateien aus diesem Ordner hochladen
3. **Settings → Pages** → Source: **Deploy from a branch**
4. Branch `main`, Ordner `/ (root)` → **Save**

## Rechtlicher Hinweis

Die Seite enthält eine Datenschutzerklärung und ein Impressum. Die Angaben
müssen wahr und vollständig sein. Diese Vorlage ersetzt keine Rechtsberatung.

Die geprüften Produktbilder liegen lokal unter `images/products/`, damit die
Empfehlungsseiten auch bei blockierten externen Bildservern vollständig laden.
