# WohnGefühl – Infoseite für GitHub Pages

Statische Seite ohne JavaScript, Cookies, Tracking oder externe Schriften.
Sie dient als Website- und Datenschutz-URL für den Pinterest-Developer-Antrag.

## 1. Platzhalter ersetzen

In `datenschutz.html` und `impressum.html` diese vier Werte eintragen:

- `[[NACHNAME]]`
- `[[STRASSE HAUSNUMMER]]`
- `[[PLZ ORT]]`
- `[[E-MAIL]]`

Am schnellsten mit `sed` (Werte anpassen):

```bash
cd site
sed -i 's/\[\[NACHNAME\]\]/Mustermann/g; s/\[\[STRASSE HAUSNUMMER\]\]/Musterstraße 1/g; s/\[\[PLZ ORT\]\]/12345 Musterstadt/g; s/\[\[E-MAIL\]\]/kontakt@example.com/g' datenschutz.html impressum.html
```

Prüfen, ob nichts übrig ist:

```bash
grep -n "\[\[" datenschutz.html impressum.html || echo "alle Platzhalter ersetzt"
```

## 2. Öffentliches GitHub-Repo anlegen

Name z. B. `wohngefuehl`. Wichtig: **Public**, sonst funktioniert GitHub Pages
im kostenlosen Account nicht.

### Variante Web-Oberfläche

1. https://github.com/new → Repository `wohngefuehl`, **Public**, ohne README
2. Dateien aus diesem Ordner hochladen (Drag & Drop)
3. **Settings → Pages**
4. Source: **Deploy from a branch**
5. Branch: `main`, Ordner: `/ (root)` → **Save**
6. Nach 1–2 Minuten ist die Seite erreichbar unter
   `https://<DEIN-GITHUB-NAME>.github.io/wohngefuehl/`

### Variante Git

```bash
cd site
git init
git add .
git commit -m "WohnGefühl Infoseite"
git branch -M main
git remote add origin https://github.com/<DEIN-GITHUB-NAME>/wohngefuehl.git
git push -u origin main
```

Danach Pages wie oben aktivieren.

## 3. URLs für den Pinterest-Developer-Antrag

```
Website/App:        https://<DEIN-GITHUB-NAME>.github.io/wohngefuehl/
Datenschutz:        https://<DEIN-GITHUB-NAME>.github.io/wohngefuehl/datenschutz.html
```

Beide URLs vorher im Browser öffnen und prüfen, dass sie ohne Login laden.

## 4. Rechtlicher Hinweis

Die Seite enthält eine Datenschutzerklärung und ein Impressum. Die Angaben
müssen wahr und vollständig sein. Bei einer gewerblichen Tätigkeit kann eine
Steuerberatung sinnvoll sein. Diese Vorlage ersetzt keine Rechtsberatung.
