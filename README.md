# HOME REARED MEAT – Loud Enough to Kill (Android)

> Die Android-Version des Brotato-artigen Roguelite-Rhythm-Games. Entwickelt mit Godot 4.6.

Der vollständige Quellcode liegt im Haupt-Repo: [home-reared-meat-loud-enough-to-kill](https://github.com/nimraseflor84/home-reared-meat-loud-enough-to-kill). Die Android-App wird aus diesem Hauptprojekt exportiert.

---

## Download und Installieren

Neueste Version: [Release v1.1.0-mobile](https://github.com/nimraseflor84/home-reared-meat-mobile/releases/tag/v1.1.0-mobile)

Direkter Download: [HRM-v1.1.0-android.apk](https://github.com/nimraseflor84/home-reared-meat-mobile/releases/download/v1.1.0-mobile/HRM-v1.1.0-android.apk) (rund 110 MB)

1. Falls eine ältere Version installiert ist: zuerst deinstallieren (gleicher Paketname, sonst gibt es einen Konflikt).
2. APK auf dem Handy herunterladen.
3. Beim Öffnen die Installation aus unbekannten Quellen für den Browser oder die Dateien-App erlauben.
4. Installieren und starten.

Diese Version ist ein sauberer, signierter Build mit dem Compatibility-Renderer (OpenGL ES 3, läuft auf praktisch jedem Android-Gerät) und enthält den kompletten aktuellen Stand: alle Easter Eggs, die vollständige Lokalisierung in 5 Sprachen und die Story-Überarbeitung.

---

## Steuerung (Touch)

| Aktion | Eingabe |
|--------|---------|
| Bewegen | Virtueller Joystick (linke Bildschirmhälfte) |
| Angriff | Automatisch |
| Dash | Touch-Button |
| Ultimate | Touch-Button |

---

## Worum geht es

Ein Wave-Survival-Roguelite, in dem du als Mitglied der Metal-Band Home Reared Meat im Takt der Musik gegen Wellen von Feinden kämpfst. 15 Story-Wellen rund um den Konzern SoundCorp und seinen Chef Dr. Victor Stille, dazu Endless-Mode, 6 spielbare Charaktere, 10 Maps und 5 Sprachen.

Die vollständige Beschreibung der Charaktere, Modi und Mechaniken steht im Haupt-Repo: [home-reared-meat-loud-enough-to-kill](https://github.com/nimraseflor84/home-reared-meat-loud-enough-to-kill).

---

## Easter Eggs und Geheimnisse

Zwei versteckte Charaktere, zwei Geheim-Maps und zufällige Spott-Sprüche beim Tod. Sie tauchen vor der Freischaltung nicht auf. Wer sich überraschen lassen will, klappt den Spoiler nicht auf.

<details>
<summary><b>Spoiler: So schaltest du alles frei</b></summary>

- **Pimmel (Merch-Mann):** Bumerang-Merch-Shirts, Becher-Ultimate, heilt alle 6 Kills. Freischaltung: in einem Run 12 Upgrades nehmen.
- **Theo (Stagehand):** Gaffa-Tape-Waffe, PA-Box-Ultimate, Kills verkürzen den Cooldown. Freischaltung: eine Boss-Welle ohne Treffer überstehen.
- **Nikolausdorf (Map):** verschneites Weihnachtsdorf. Freischaltung: 1.000 Kills insgesamt, oder im Dezember spielen.
- **Der Strand (Map):** die Pausen-Strand-Szene als Map, mit Fahrstuhl im Sand. Freischaltung: das Spiel 30-mal pausieren.
- **Spott-Sprüche:** beim Tod erscheint einer von 10 Sprüchen rund um die Spielwelt und die Easter Eggs.

</details>

---

## Android selbst bauen

Die APK wird aus dem Hauptprojekt exportiert, nicht aus diesem Repo. Kurz:

1. Hauptprojekt in Godot 4.6 öffnen.
2. Project, Project Settings, Rendering, Renderer: Rendering Method für Mobile auf Compatibility (in der `project.godot` bereits als `renderer/rendering_method.mobile="gl_compatibility"` gesetzt).
3. Einmalig Android-Export-Templates und Android SDK plus Debug-Keystore einrichten (Godot Editor: Manage Export Templates, und Editor Settings, Export, Android). Wichtig: sdkmanager braucht JDK 17.
4. Project, Export, Preset Android, Export Project.

Alternativ headless per Kommandozeile:
```bash
godot --headless --path "<Projektordner>" --export-debug "Android" "HRM.apk"
```

---

## Hinweise

- Speichern, Bestenliste und alle Inhalte sind identisch zur Desktop-Version, da Android aus demselben Hauptprojekt exportiert wird.
- Musik (MP3) ist aus urheberrechtlichen Gründen eventuell nicht im Build enthalten. Soundeffekte werden prozedural erzeugt und funktionieren immer.

*Home Reared Meat, Loud Enough to Kill, Copyright 2026 Armin Rolfes / Home Reared Meat*
