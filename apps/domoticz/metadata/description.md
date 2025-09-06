# Domoticz

![Domoticz Logo](https://www.domoticz.com/images/logo.png)

**Domoticz** est une solution **domotique open-source légère et puissante**, idéale pour centraliser, automatiser et surveiller vos équipements connectés (éclairage, chauffage, capteurs, caméras, énergie, météo…).  
Son interface web simple et efficace en fait un excellent choix pour les environnements **Runtipi**.

---

## 🔧 Fonctionnalités principales

- 🏠 Supervision complète de votre maison connectée  
- 📡 Compatible avec de nombreux protocoles : Z-Wave, Zigbee (via passerelles), MQTT, RFXCOM, 433 MHz, Philips Hue, etc.  
- 📊 Dashboards personnalisables avec graphiques et historiques  
- 🔄 Automatisations et scénarios avancés (blocs visuels, Lua, Python, DzVents)  
- 📲 Notifications vers vos applis préférées (Pushover, Telegram, email…)  
- 🔐 Gestion multi-utilisateurs et API REST/JSON intégrée  
- ⚙️ Léger, rapide et idéal pour Raspberry Pi comme pour serveur dédié  

---

## 🖼️ Aperçus

![Dashboard Domoticz](https://www.domoticz.com/images/screenshots/dashboard.png)  
*Tableau de bord personnalisable*  

---

![Graphiques énergie](https://www.domoticz.com/images/screenshots/usage.png)  
*Suivi consommation & capteurs*  

---

![Devices Domoticz](https://www.domoticz.com/images/screenshots/devices.png)  
*Gestion des périphériques connectés*  

---

## 📂 Données & persistance

- Les données sont stockées dans : `/opt/domoticz/userdata`  
- Contient la config (`domoticz.db`) et les historiques  
- Volume persistant même après mise à jour ou redémarrage du conteneur  

---

## ⚠️ Pré-requis

- Une machine hôte (Raspberry Pi, serveur Linux, macOS ou Windows)  
- Selon vos périphériques : clé USB Z-Wave, dongle Zigbee, RFXCOM, broker MQTT…  
- Port web : `8080` (par défaut, modifiable)  

---

## 🚀 Exemple de configuration Docker (Runtipi)

```yaml
services:
  domoticz:
    image: domoticz/domoticz:latest
    container_name: domoticz
    restart: unless-stopped
    ports:
      - "8080:8080"
    volumes:
      - ./domoticz_data:/opt/domoticz/userdata
    devices:
      - /dev/ttyUSB0:/dev/ttyUSB0   # Exemple pour dongle USB (Z-Wave, RFXCOM…)