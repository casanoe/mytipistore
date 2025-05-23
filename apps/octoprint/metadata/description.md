# OctoPrint

![OctoPrint Logo](https://octoprint.org/assets/img/logo.png)

**OctoPrint** est une interface web puissante pour le contrôle à distance et en temps réel de vos **imprimantes 3D**. Elle permet de gérer vos impressions, de surveiller l’état de l’imprimante et d’automatiser votre flux de travail.

---

## 🔧 Fonctionnalités principales

- 🖨️ Contrôle complet de l’imprimante 3D via interface web
- 📦 Téléversement de fichiers G-code
- 🔁 Suivi en temps réel de l’impression (température, progression)
- 📹 Intégration de caméra (MJPG-Streamer)
- ⚙️ Système de plugins très riche (thèmes, intégrations, automatisations)
- 🔐 Authentification utilisateur et gestion des accès
- 🔄 API REST pour intégration avancée (Home Assistant, scripts…)

---

## 🖼️ Aperçu visuel

### Tableau de bord d'impression

![Dashboard OctoPrint](https://octoprint.org/assets/img/screenshots/octoprint-01.png)

---

### Visualisation G-code intégrée

![Visualiseur G-code](https://octoprint.org/assets/img/screenshots/octoprint-03.png)

---

### Interface plugin manager

![Plugin Manager](https://octoprint.org/assets/img/screenshots/octoprint-06.png)

---

## 📂 Où sont stockées les données ?

Les données (config, fichiers, plugins…) sont stockées dans un volume Docker monté dans `/octoprint`. Ce volume est persistant même en cas de redémarrage du conteneur.

---

## ⚠️ Pré-requis matériel

- Un Raspberry Pi (ou autre machine) connecté en USB à votre imprimante
- Un port série disponible, ex. : `/dev/ttyUSB0` ou `/dev/ttyACM0`
- Facultatif : une caméra compatible MJPG

---

## 🔗 Ressources utiles

- [Documentation officielle](https://docs.octoprint.org/)
- [Forum de la communauté](https://community.octoprint.org/)
- [Dépôt GitHub](https://github.com/OctoPrint/OctoPrint)

---

> 📌 Conseil : OctoPrint est souvent utilisé avec OctoPi, mais cette image Docker est une alternative légère, parfaite pour Runtipi.

