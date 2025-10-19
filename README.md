# E-Paper 4-Quadranten Display Blueprint für Home Assistant

Ein flexibler Home Assistant Blueprint zur Anzeige von vier Sensoren in einem übersichtlichen 4-Quadranten-Layout auf E-Paper Displays (Open ePaper Link Integration).

[![hacs_badge](https://img.shields.io/badge/HACS-Custom-41BDF5.svg)](https://github.com/hacs/integration)
[![GitHub release](https://img.shields.io/github/release/meddatzk/epaper-4quadrant-blueprint.svg)](https://github.com/meddatzk/epaper-4quadrant-blueprint/releases)
[![License](https://img.shields.io/github/license/meddatzk/epaper-4quadrant-blueprint.svg)](LICENSE)

## 🚀 Quick Start

[![Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fmeddatzk%2Fepaper-4quadrant-blueprint%2Fblob%2Fmain%2Fepaper_4quadrant.yaml)

Klicke auf den Button oben, um den Blueprint direkt in deine Home Assistant Instanz zu importieren!

## 📋 Voraussetzungen

- Home Assistant (Core 2023.8 oder neuer empfohlen)
- [Open ePaper Link Integration](https://github.com/OpenEPaperLink/Home_Assistant_Integration)
- Ein kompatibles E-Paper Display

## ✨ Features

- **Vollständig konfigurierbar**: Alle Elemente können individuell angepasst werden
- **4-Quadranten-Layout**: Übersichtliche Darstellung von vier Sensoren
- **Flexible Icons**: Beliebige Material Design Icons (MDI) verwendbar
- **Schwellenwert-Warnung**: Automatische Farbänderung bei Unterschreitung von Grenzwerten
- **Anpassbare Farben**: Normale Farbe, Alarmfarbe und Trennlinien individuell einstellbar
- **Universell einsetzbar**: Für Pflanzen, Temperaturen, Batterien, Luftfeuchtigkeit, etc.

## 🎯 Anwendungsbeispiele

| Anwendung | Icon | Einheit |
|-----------|------|---------|
| 🌱 Pflanzenfeuchtigkeit | `mdi:sprout` | % |
| 🌡️ Temperatur | `mdi:thermometer` | °C |
| 💧 Luftfeuchtigkeit | `mdi:water-percent` | % |
| 🔋 Batteriestände | `mdi:battery` | % |
| 💡 Helligkeit | `mdi:brightness-6` | lx |
| 📊 CO₂ Werte | `mdi:molecule-co2` | ppm |

## 📥 Installation

### Methode 1: Automatischer Import (empfohlen)

1. Klicke auf den Import-Button oben
2. Bestätige den Import in Home Assistant
3. Erstelle eine neue Automatisierung basierend auf dem Blueprint

### Methode 2: Manuelle Installation

1. Kopiere die Datei `epaper_4quadrant.yaml` nach `/config/blueprints/automation/`
2. Gehe in Home Assistant zu: **Einstellungen** → **Automatisierungen & Szenen** → **Blueprints**
3. Klicke auf **Blueprint importieren** und wähle die Datei aus

### Methode 3: URL Import

1. Gehe zu **Einstellungen** → **Automatisierungen & Szenen** → **Blueprints**
2. Klicke auf **Blueprint importieren**
3. Füge folgende URL ein:
```
https://github.com/meddatzk/epaper-4quadrant-blueprint/blob/main/epaper_4quadrant.yaml
```

## ⚙️ Konfiguration

Nach dem Import kannst du folgende Parameter konfigurieren:

### Display Einstellungen
- **E-Paper Display**: Zielgerät auswählen
- **Display Titel**: Überschrift der Anzeige
- **TTL**: Aktualisierungsintervall (60-3600 Sekunden)

### Pro Sensor (4x)
- **Sensor Entity**: Der zu überwachende Sensor
- **Beschriftung**: Anzeigename für den Sensor
- **Icon**: Material Design Icon (z.B. `mdi:sprout`)

### Schwellenwerte & Einheiten
- **Unterer Schwellenwert**: Wert für Alarm-Farbwechsel
- **Einheit**: Anzeigeeinheit (%, °C, lx, etc.)

### Farben
- **Normale Farbe**: Farbe für OK-Zustand (schwarz/rot/weiß)
- **Alarm Farbe**: Farbe bei Unterschreitung (rot/schwarz/weiß)
- **Trennlinien Farbe**: Farbe der Quadranten-Trennlinien

## 📖 Verwendungsbeispiel

### Beispiel: Pflanzenüberwachung

1. Erstelle eine neue Automatisierung mit dem Blueprint
2. Konfiguriere wie folgt:
   - **Display Titel**: "Pflanzen Bodenfeuchtigkeit"
   - **Sensor 1**: `sensor.pflanze_wohnzimmer_feuchtigkeit`
   - **Beschriftung 1**: "Wohnzimmer"
   - **Icon 1**: `mdi:sprout`
   - **Schwellenwert**: 30
   - **Einheit**: %
   - **Alarm Farbe**: rot

3. Wiederhole dies für alle vier Sensoren
4. Speichere die Automatisierung

Das Display aktualisiert sich nun automatisch bei Sensoränderungen und warnt visuell bei niedrigen Werten!

## 🖼️ Vorschau

Das Display zeigt:
- Oben links: Sensor 1
- Oben rechts: Sensor 2
- Unten links: Sensor 3
- Unten rechts: Sensor 4

Jeder Quadrant enthält:
- Icon (farblich markiert bei Alarm)
- Beschriftung
- Sensorwert + Einheit (farblich markiert bei Alarm)

## 🤝 Beitragen

Contributions sind willkommen! Bitte erstelle einen Pull Request oder öffne ein Issue für Vorschläge und Fehlerberichte.

## 📝 Changelog

### Version 1.0.0 (2025-10-19)
- Initiales Release
- Vollständig konfigurierbares 4-Quadranten-Layout
- Unterstützung für beliebige MDI Icons
- Schwellenwert-basierte Farbwarnungen
- Anpassbare Farben für alle Elemente

## 📜 Lizenz

MIT License - siehe [LICENSE](LICENSE) Datei für Details

## 💬 Support

Bei Fragen oder Problemen:
- Öffne ein [GitHub Issue](https://github.com/meddatzk/epaper-4quadrant-blueprint/issues)
