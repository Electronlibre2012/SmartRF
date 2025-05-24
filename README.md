


![RF](https://github.com/user-attachments/assets/95b5dfa9-f58b-4ff1-9496-08268a6b96a2)

# SmartRF

SmartRF est une version dérivée de [SmartIR](https://github.com/smartHomeHub/SmartIR), adaptée pour les appareils RF avec une structure de fichier JSON **plate**.

SmartRF is a fork of [SmartIR](https://github.com/smartHomeHub/SmartIR), tailored for RF devices with a **flat** JSON file structure.
---

## 🔧 Fonctionnalités

- Structure JSON simplifiée (sans arborescence imbriquée)
- Support RF via `remote.send_command` (Broadlink, Sonoff RF Bridge, etc.)
- Compatible Home Assistant
- Facile à étendre pour d'autres protocoles (MQTT, ESPHome, etc.)

---

## 📁 Structure du fichier JSON

```json
{
  "manufacturer": "ExempleCo",
  "supportedModels": ["Model-X1"],
  "supportedController": "RF",
  "commandsEncoding": "Base64",
  "minTemperature": 16.0,
  "maxTemperature": 30.0,
  "precision": 1.0,
  "operationModes": ["cool", "dry"],
  "fanModes": ["low", "mid", "high"],
  "commands": {
    "off": "b64:Base64Code",
    "cool_low_22": "b64:Base64Code",
    "cool_low": "b64:Base64Code",
    "cool": "b64:Base64Code",
    "22": "b64:Base64Code"
  }
}

## Installation

Copiez ce dépôt dans `custom_components/smartrf/` de votre configuration Home Assistant.

ou ajouter le dépôt personnalisé "https://github.com/Electronlibre2012/SmartRF" dans HACS
