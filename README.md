# HOME REARED MEAT – Loud Enough to Kill (Android)

> Die Android-Version des Brotato-artigen Roguelite-Rhythm-Games. Entwickelt mit Godot 4.6.

Der vollständige Quellcode liegt im Haupt-Repo: [home-reared-meat-loud-enough-to-kill](https://github.com/nimraseflor84/home-reared-meat-loud-enough-to-kill). Die Android-App wird aus diesem Hauptprojekt exportiert.

---

## Download und Installieren

Neueste Version: [Release v1.3.0-mobile](https://github.com/nimraseflor84/home-reared-meat-mobile/releases/tag/v1.3.0-mobile)

Direkter Download: [HRM-v1.3.0-android.apk](https://github.com/nimraseflor84/home-reared-meat-mobile/releases/download/v1.3.0-mobile/HRM-v1.3.0-android.apk) (rund 110 MB)

1. Falls eine ältere Version installiert ist: zuerst deinstallieren (gleicher Paketname).
2. APK auf dem Handy herunterladen.
3. Beim Öffnen die Installation aus unbekannten Quellen erlauben.
4. Installieren und starten.

Sauberer, signierter Build mit dem Compatibility-Renderer (läuft auf praktisch jedem Android-Gerät).

---

## Neu in v1.3.0

- **Bonus für den schwersten Grad:** Wer den Story-Mode auf "Bolognese Bloodbath" durchspielt, schaltet einen geheimen Bonus-Charakter (Toxo, ein mutierter Toxic-Held) und die Bonus-Map "Giftstadt" frei.
- **Tod-Spruch fährt jetzt deutlich ins Bild** (von links, mit Einblenden und Pulsieren), damit man ihn bemerkt.

## Neu in v1.2.0

- **Signature-Waffen:** Jeder Charakter schaltet eine besondere zweite Waffe frei, wenn man ihn auf Drink Fight Die! (zweitschwerster Grad) oder höher durchspielt. Auswahl im Charakter-Bildschirm.
- Neue Credits.

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

Ein Wave-Survival-Roguelite, in dem du als Mitglied der Metal-Band Home Reared Meat im Takt der Musik gegen Wellen von Feinden kämpfst. 15 Story-Wellen rund um den Konzern SoundCorp und seinen Chef Dr. Victor Stille, dazu Endless-Mode, Charaktere, Maps und 5 Sprachen. Volle Beschreibung im [Haupt-Repo](https://github.com/nimraseflor84/home-reared-meat-loud-enough-to-kill).

---

## Easter Eggs und Geheimnisse

<details>
<summary><b>Spoiler: So schaltest du alles frei</b></summary>

- **Pimmel (Merch-Mann):** in einem Run 12 Upgrades nehmen.
- **Theo (Stagehand):** eine Boss-Welle ohne Treffer überstehen.
- **Map Nikolausdorf:** 1.000 Kills insgesamt, oder im Dezember spielen.
- **Map Der Strand:** das Spiel 30-mal pausieren.
- **Signature-Waffen:** mit dem Charakter auf Drink Fight Die! oder höher durchspielen.
- **Toxo + Giftstadt:** den schwersten Grad (Bolognese Bloodbath) durchspielen.
- **Spott-Sprüche:** beim Tod erscheint einer von 10 Sprüchen.

</details>

---

## Android selbst bauen

Aus dem Hauptprojekt exportieren: Godot 4.6, Renderer für Mobile auf Compatibility, Android-Export-Templates plus Android SDK und JDK 17, dann Project, Export, Preset Android. Headless:
```bash
godot --headless --path "<Projektordner>" --export-debug "Android" "HRM.apk"
```

*Home Reared Meat, Loud Enough to Kill, Copyright 2026 Armin Rolfes / Home Reared Meat*
