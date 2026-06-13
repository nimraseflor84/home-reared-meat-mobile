# HOME REARED MEAT – Loud Enough to Kill (Android)

> Die Android-Version des Brotato-artigen Roguelite-Rhythm-Games. Entwickelt mit Godot 4.6.

Dies ist das Mobile-Repo. Der vollständige Quellcode des Spiels liegt im Haupt-Repo: [home-reared-meat-loud-enough-to-kill](https://github.com/nimraseflor84/home-reared-meat-loud-enough-to-kill). Die Android-App wird aus diesem Hauptprojekt exportiert.

---

## APK installieren

Den fertigen Build findest du unter [Releases](https://github.com/nimraseflor84/home-reared-meat-mobile/releases).

1. Auf dem Handy die `HRM Loud enough to Kill.apk` herunterladen (das ist der vollständige Build, rund 190 MB).
2. Beim Öffnen fragt Android nach der Erlaubnis, Apps aus unbekannten Quellen zu installieren. Diese für den Browser oder die Dateien-App erlauben.
3. Installieren und starten.

> Die kleine `Home reared Meat.apk` (rund 26 MB) ist ein leerer Test-Build und zeigt nur das Godot-Logo. Nimm sie nicht. Sie wird aus dem Release entfernt.

---

## Wenn nur das Godot-Logo erscheint

Das ist ein bekanntes Problem dieses ersten Builds und hat zwei mögliche Ursachen:

1. **Falsche APK installiert.** Die kleine 26-MB-Datei stammt aus einem leeren Projekt ohne Hauptszene und zeigt deshalb nur das Godot-Symbol. Nutze die große `HRM Loud enough to Kill.apk`.

2. **Renderer.** Das Hauptprojekt rendert mit "Forward Plus" (Vulkan, für den Desktop). Viele Android-Geräte unterstützen das nicht. Die App startet dann bis zum Godot-Boot-Logo und bleibt dort hängen. Lösung: die Android-Version muss mit dem **Compatibility-Renderer** (OpenGL ES 3) gebaut werden. Das ist im Haupt-Repo jetzt vorbereitet (siehe unten).

---

## Android-Version selbst bauen

Die saubere Lösung. Du baust die APK aus dem **Hauptprojekt**, nicht aus diesem Repo (dieses Repo enthält nur die Verteilung und Doku).

### Voraussetzungen (einmalig)
- **Godot 4.6**
- **Android Build Templates** in Godot: Editor, Manage Export Templates, Download
- **Android SDK** plus ein **Debug-Keystore**. Godot richtet beides über Editor, Editor Settings, Export, Android weitgehend automatisch ein (OpenJDK und Android SDK lassen sich von dort installieren).

### Schritte
1. Das Hauptprojekt in Godot öffnen.
2. **Renderer auf Compatibility stellen:** Project, Project Settings, Rendering, Renderer, Rendering Method. Den Wert für **Mobile** auf **Compatibility** setzen. (Im Haupt-Repo ist `renderer/rendering_method.mobile="gl_compatibility"` bereits in der `project.godot` eingetragen, dieser Schritt ist dann nur noch eine Kontrolle.)
3. Project, Export. Das **Android**-Preset ist bereits angelegt (arm64-v8a, Paket "HRM Loud enough to Kill", Icons, Debug-Keystore).
4. Auf **Export Project** klicken und als `HRM Loud enough to Kill.apk` speichern.
5. APK aufs Handy übertragen und installieren, oder das Handy per USB mit aktiviertem USB-Debugging anschließen und in Godot auf das kleine Android-Play-Symbol (One-Click-Deploy) klicken.

> Touch-Steuerung ist im Spiel bereits enthalten (`scripts/ui/touch_controls.gd`): ein virtueller Joystick links plus Buttons für Dash und Ultimate. Der Angriff läuft automatisch.

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

Ein Wave-Survival-Roguelite, in dem du als Mitglied der Metal-Band Home Reared Meat im Takt der Musik gegen Wellen von Feinden kämpfst. 15 Story-Wellen rund um den Konzern SoundCorp und seinen Chef Dr. Victor Stille, dazu Endless-Mode, 6 spielbare Charaktere, 10 Maps und 5 Sprachen (Deutsch, Englisch, Französisch, Spanisch, Ukrainisch).

Die volle Beschreibung der Charaktere, Modi, Bosse und der kompletten Spielmechanik steht im Haupt-Repo: [home-reared-meat-loud-enough-to-kill](https://github.com/nimraseflor84/home-reared-meat-loud-enough-to-kill).

---

## Easter Eggs und Geheimnisse

Das Spiel hat zwei versteckte Charaktere, zwei Geheim-Maps und zufällige Spott-Sprüche beim Tod. Sie tauchen vor der Freischaltung nicht auf. Wer sich überraschen lassen will, klappt den Spoiler nicht auf.

<details>
<summary><b>Spoiler: So schaltest du alles frei</b></summary>

- **Pimmel (Merch-Mann):** Bumerang-Merch-Shirts, Becher-Ultimate, heilt alle 6 Kills. Freischaltung: in einem Run 12 Upgrades nehmen.
- **Theo (Stagehand):** Gaffa-Tape-Waffe, PA-Box-Ultimate, Kills verkürzen den Cooldown. Freischaltung: eine Boss-Welle ohne Treffer überstehen.
- **Nikolausdorf (Map):** verschneites Weihnachtsdorf. Freischaltung: 1.000 Kills insgesamt, oder im Dezember spielen.
- **Der Strand (Map):** die Pausen-Strand-Szene als Map, mit Fahrstuhl im Sand. Freischaltung: das Spiel 30-mal pausieren.
- **Spott-Sprüche:** beim Tod erscheint einer von 10 Sprüchen rund um die Spielwelt und die Easter Eggs.

</details>

---

## Hinweise

- Speichern, Bestenliste und alle Inhalte sind identisch zur Desktop-Version, da Android aus demselben Hauptprojekt exportiert wird.
- Musik (MP3) ist aus urheberrechtlichen Gründen eventuell nicht im Build enthalten. Soundeffekte werden prozedural erzeugt und funktionieren immer.

*Home Reared Meat, Loud Enough to Kill, Copyright 2026 Armin Rolfes / Home Reared Meat*
