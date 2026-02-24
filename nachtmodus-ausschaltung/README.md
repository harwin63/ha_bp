# 🌙 Nachtmodus Auto-Ausschaltung (Werktag)

Schaltet einen Nachtmodus-Toggle automatisch zu einer konfigurierbaren Uhrzeit ab – aber nur an Werktagen, geprüft über den Home Assistant Workday-Sensor. Ideal als Ergänzung zur Schlafzimmer-Beleuchtung.

[![Import Blueprint](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https://raw.githubusercontent.com/harwin63/ha_bp/main/nachtmodus-ausschaltung/blueprint_nachtmodus_ausschalt.yaml)

---

## ✅ Voraussetzungen

- Ein `input_boolean` als Nachtmodus-Toggle (kann der gleiche wie bei der Schlafzimmer-Beleuchtung sein)
- [Workday-Integration](https://www.home-assistant.io/integrations/workday/) in Home Assistant eingerichtet  
  **Einstellungen → Geräte & Dienste → Integration hinzufügen → Workday**

---

## 🔧 Einmalige Vorbereitung

Falls noch kein Nachtmodus-Toggle vorhanden:

**Einstellungen → Geräte & Dienste → Helfer → Helfer erstellen → Schalter (input_boolean)**

| Feld | Wert |
|---|---|
| Name | `Nachtmodus` |
| Icon | `mdi:moon-waning-crescent` |

> 💡 Dieser Toggle wird auch vom Blueprint **Schlafzimmer Beleuchtung** genutzt – einmal anlegen, in beiden Blueprints verwenden.

---

## ▶️ Blueprint einrichten

1. Blueprint importieren (Badge oben oder Raw-URL manuell eingeben)
2. **Einstellungen → Automationen → Blueprints → Blueprint verwenden**
3. Felder ausfüllen:

| Feld | Beschreibung |
|---|---|
| Nachtmodus-Toggle | Der `input_boolean` der den Nachtmodus repräsentiert |
| Arbeitstag-Sensor | Der Workday-Sensor (`binary_sensor.workday_sensor` o.ä.) |
| Ausschalt-Zeit | Uhrzeit zu der der Nachtmodus abgeschaltet wird (Standard: 06:20) |

---

## ⚙️ Wie es funktioniert

```
Täglich um die eingestellte Uhrzeit:
  → Ist der Nachtmodus-Toggle AN?
  → Ist heute ein Werktag (Workday-Sensor = on)?
      Ja zu beiden  →  Nachtmodus-Toggle wird ausgeschaltet
      Nein          →  Nichts passiert (Wochenende / Feiertag)
```

---

## 🔗 Raw-URL für manuellen Import

```
https://raw.githubusercontent.com/harwin63/ha_bp/main/nachtmodus-ausschaltung/blueprint_nachtmodus_ausschalt.yaml
```
