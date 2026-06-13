# HOME REARED MEAT – Loud Enough to Kill (Android)

> Die Android-Version des Brotato-artigen Roguelite-Rhythm-Games. Entwickelt mit Godot 4.6.

Der vollständige Quellcode liegt im Haupt-Repo: [home-reared-meat-loud-enough-to-kill](https://github.com/nimraseflor84/home-reared-meat-loud-enough-to-kill). Die Android-App wird aus diesem Hauptprojekt exportiert.

---

## Download und Installieren

Neueste Version: [Release v1.2.0-mobile](https://github.com/nimraseflor84/home-reared-meat-mobile/releases/tag/v1.2.0-mobile)

Direkter Download: [HRM-v1.2.0-android.apk](https://github.com/nimraseflor84/home-reared-meat-mobile/releases/download/v1.2.0-mobile/HRM-v1.2.0-android.apk) (rund 110 MB)

1. Falls eine ältere Version installiert ist: zuerst deinstallieren (gleicher Paketname, sonst gibt es einen Konflikt).
2. APK auf dem Handy herunterladen.
3. Beim Öffnen die Installation aus unbekannten Quellen für den Browser oder die Dateien-App erlauben.
4. Installieren und starten.

Sauberer, signierter Build mit dem Compatibility-Renderer (OpenGL ES 3, läuft auf praktisch jedem Android-Gerät).

---

## Neu in v1.2.0: Signature-Waffen

Jeder Charakter schaltet eine besondere zweite Waffe frei, wenn man den Story-Mode mit ihm auf dem zweitschwersten Grad (Drink Fight Die!) oder höher durchspielt. Im Charakter-Auswahlbildschirm lässt sich dann zwischen Standard- und Signature-Waffe wählen. Jede Waffe ist ein eigener Spielstil, kein reiner Stärke-Boost (z. B. Armin "Standing Wave", Andz "Sweep Picking", Maik "Feedback Drone").

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

Ein Wave-Survival-Roguelite, in dem du als Mitglied der Metal-Band Home Reared Meat im Takt der Musik gegen Wellen von Feinden kämpfst. 15 Story-Wellen rund um den Konzern SoundCorp und seinen Chef Dr. Victor Stille, dazu Endless-Mode, 6 spielbare Charaktere, 10 Maps und 5 Sprachen. Volle Beschreibung im [Haupt-Repo](https://github.com/nimraseflor84/home-reared-meat-loud-enough-to-kill).

---

## Easter Eggs und Geheimnisse

Zwei versteckte Charaktere, zwei Geheim-Maps, die Signature-Waffen und zufällige Spott-Sprüche beim Tod. Vor der Freischaltung tauchen sie nicht auf.

<details>
<summary><b>Spoiler: So schaltest du alles frei</b></summary>

- **Pimmel (Merch-Mann):** Freischaltung: in einem Run 12 Upgrades nehmen.
- **Theo (Stagehand):** Freischaltung: eine Boss-Welle ohne Treffer überstehen.
- **Map Nikolausdorf:** 1.000 Kills insgesamt, oder im Dezember spielen.
- **Map Der Strand:** das Spiel 30-mal pausieren.
- **Signature-Waffen:** Story-Mode mit dem jeweiligen Charakter auf Drink Fight Die! oder höher durchspielen.
- **Spott-Sprüche:** beim Tod erscheint einer von 10 Sprüchen.

</details>

---

## Android selbst bauen

Die APK wird aus dem Hauptprojekt exportiert. Kurz: Godot 4.6, Renderer für Mobile auf Compatibility (in der project.godot bereits gesetzt), Android-Export-Templates plus Android SDK und JDK 17 einrichten, dann Project, Export, Preset Android, Export Project. Headless geht auch:
```bash
godot --headless --path "<Projektordner>" --export-debug "Android" "HRM.apk"
```

*Home Reared Meat, Loud Enough to Kill, Copyright 2026 Armin Rolfes / Home Reared Meat*
