# ⚡ Home Assistant Blueprints

Eine Sammlung von Blueprints für Home Assistant Automationen – wiederverwendbar, flexibel konfigurierbar und direkt importierbar.

---

## 📦 Enthaltene Blueprints

| Blueprint | Beschreibung |
|---|---|
| [⚡ Energie-Ladetracker](#-energie-ladetracker) | Misst Verbrauch & Kosten beim Laden von Akkus |
| [🌙 Nachtmodus Auto-Ausschaltung](#-nachtmodus-auto-ausschaltung) | Schaltet den Nachtmodus an Werktagen automatisch ab |
| [💡 Beleuchtung Hybrid & Adaptive](#-beleuchtung-hybrid--adaptive) | Bewegungsgesteuerte Lichtsteuerung mit Adaptive Lighting |

---

## ⚡ Energie-Ladetracker

Misst automatisch Verbrauch und Kosten eines Ladevorgangs (Fahrradakku, E-Scooter, Laptop, ...) über einen Smartplug mit Energiemessung. Speichert das Ergebnis nach Ladeende und startet beim nächsten Laden neu bei 0.

➡️ [Zur Anleitung](energie-ladetracker/README.md)

[![Import Blueprint](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https://raw.githubusercontent.com/harwin63/ha_bp/main/energie-ladetracker/blueprint_ladetracker_vollstaendig.yaml)

---

## 🌙 Nachtmodus Auto-Ausschaltung

Schaltet einen Nachtmodus-Toggle an Werktagen automatisch zu einer konfigurierbaren Uhrzeit aus – abhängig vom Workday-Sensor. Ideal als Ergänzung zur Schlafzimmer-Beleuchtung.

➡️ [Zur Anleitung](nachtmodus-ausschaltung/README.md)

[![Import Blueprint](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https://raw.githubusercontent.com/harwin63/ha_bp/main/nachtmodus-ausschaltung/blueprint_nachtmodus_ausschalt.yaml)

---

## 💡 Beleuchtung Hybrid & Adaptive

Bewegungsgesteuerte Lichtsteuerung mit drei automatischen Modi: Morgen (gedimmt), Tagsüber (hell) und Abend (gedimmt). Einsetzbar in beliebigen Räumen. Integriert Adaptive Lighting und einen Nachtmodus-Schalter. Zeiten flexibel per Festwert oder Helfer/Sonnen-Template-Sensoren steuerbar.

➡️ [Zur Anleitung](beleuchtung-hybrid-adaptive/README.md)

[![Import Blueprint](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https://raw.githubusercontent.com/harwin63/ha_bp/main/beleuchtung-hybrid-adaptive/blueprint_beleuchtung_hybrid-steuerung.yaml)

---

## 🗂️ Empfohlene Ordnerstruktur

```
ha_bp/
├── README.md
├── energie-ladetracker/
│   ├── blueprint_ladetracker_vollstaendig.yaml
│   ├── lovelace_beispiel.yaml
│   └── README.md
├── nachtmodus-ausschaltung/
│   ├── blueprint_nachtmodus_ausschalt.yaml
│   └── README.md
└── beleuchtung-hybrid-adaptive/
    ├── blueprint_beleuchtung_hybrid-steuerung.yaml
    ├── helfer.yaml
    └── README.md
```

---

## 📥 Blueprint importieren

1. Auf den **"Import Blueprint"** Badge klicken  
   *oder* in Home Assistant: **Einstellungen → Automationen → Blueprints → Blueprint importieren** → Raw-URL einfügen
2. Helfer gemäß Anleitung anlegen (siehe jeweilige README)
3. Neue Automation aus Blueprint erstellen und konfigurieren

---

## 🤝 Feedback & Beiträge

Fehler gefunden oder Verbesserungsvorschläge? Gerne ein Issue öffnen!
