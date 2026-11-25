# GitHub-Seite für DotPresso – Ablauf

Dieser Ordner ist **nur für die Veröffentlichung**. Kein Quellcode, nichts aus `Projekt` und schon gar nichts aus `Lizenzverwaltung`.

```
GitHub\
  Hochladen.md        diese Anleitung (wird NICHT hochgeladen)
  Release-1.0.0.md    Text für die Release-Seite (wird eingefügt, nicht hochgeladen)
  DotPresso-1.0.0-Setup.exe   kommt als Datei an das Release (nicht ins Repository)
  repo\               genau das, was ins Repository kommt
    README.md         die Startseite
    bilder\           Fotos und Screenshots für die README
```

## Vorher erledigen
- [ ] `[KONTAKT EINTRAGEN]` in `repo\README.md` ersetzen (E-Mail oder Kaufseite)
- [ ] Bilder in `repo\bilder\` legen: `ausdruck.jpg`, `programm.png`; `BILDER_HIER.txt` löschen
- [ ] Kontaktzeile in `Projekt\Setup\Lizenzbedingungen.txt` ausfüllen und Setup neu bauen
- [ ] Setup mit Nuitka-EXE frisch bauen und einmal installieren/testen

## Auf github.com
1. Oben rechts **+** → **New repository**
   - Name: `DotPresso`
   - **Public**
   - kein README, keine Lizenz, kein .gitignore anhaken (das README bringen wir mit)
2. Im leeren Repository **uploading an existing file** → den **Inhalt** von `repo\` hineinziehen (README.md und Ordner bilder) → **Commit changes**
3. Rechts **Releases** → **Create a new release**
   - Tag: `v1.0.0`, Titel: `DotPresso 1.0.0`
   - Text aus `Release-1.0.0.md` einfügen
   - `GitHub\DotPresso-1.0.0-Setup.exe` in das Feld für Dateien ziehen
   - **Publish release**
4. **Settings** → **General** → **Features**: Issues anhaken (meist schon an), Wiki/Projects abhaken
5. Optional **Settings → Pages**: Source „Deploy from a branch“, Branch `main`, Ordner `/ (root)`
   → Seite unter `https://<name>.github.io/DotPresso/`

## Danach
- Link der Seite als `BUY_URL` in `DotPresso.py` eintragen? (zeigt „Pro kaufen…“ im Lizenzdialog)
- Links in Forenbeiträgen auf die Repository-Seite setzen, nicht direkt auf die .exe
