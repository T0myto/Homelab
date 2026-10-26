# 🏠 Homelab

![Proxmox](https://img.shields.io/badge/Proxmox-E57000?style=for-the-badge&logo=proxmox&logoColor=white)
![Debian](https://img.shields.io/badge/Debian-A81D33?style=for-the-badge&logo=debian&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Portainer](https://img.shields.io/badge/Portainer-13BEF9?style=for-the-badge&logo=portainer&logoColor=white)
![Home Assistant](https://img.shields.io/badge/Home%20Assistant-41BDF5?style=for-the-badge&logo=homeassistant&logoColor=white)
![Node-RED](https://img.shields.io/badge/Node--RED-8F0000?style=for-the-badge&logo=nodered&logoColor=white)
![Tuya](https://img.shields.io/badge/Tuya-FF4800?style=for-the-badge&logo=tuya&logoColor=white)
![Spotify](https://img.shields.io/badge/Spotify-1DB954?style=for-the-badge&logo=spotify&logoColor=white)

Homelab personnel, refait de zéro en octobre 2026.

## 🎯 Objectif

Un dashboard Home Assistant sur une tablette, et un brief lu à voix haute chaque matin par un Google Home. Le tout fait partie d'une suite d'automatisations Node-RED, avec tout sous Docker.

## 🧰 Technologies utilisées

| Domaine | Technologie | Rôle | État |
|---|---|---|---|
| Virtualisation | Proxmox VE | Hyperviseur du serveur | ✅ en service |
| Système | Debian 13 | Système de la VM `docker-host` | ✅ en service |
| Conteneurs | Docker | Fait tourner les services | ✅ en service |
| Conteneurs | Portainer CE | Interface graphique de Docker | ✅ en service |
| Domotique | Home Assistant | Cœur de la maison connectée et dashboard | ✅ en service |
| Domotique | HACS (Mushroom, card-mod, kiosk-mode, thème Catppuccin) | Extensions et apparence du dashboard | ✅ en service |
| Automatisation | Node-RED | Brief du matin, écran de la tablette, alertes | ✅ en service |
| Objets connectés | Tuya (lampes LSC Smart Connect) | Lumières, via le cloud Tuya | ✅ en service |
| Audio | Google Home / Google Cast, Google Translate TTS | Fait parler le Google Home | ✅ en service |
| Audio | Spotify | Lecteur dans le dashboard | ✅ en service |
| Données | Google Agenda (lien iCal), Met.no | Agenda du jour et météo | ✅ en service |
| Tablette | Huawei MediaPad M5 lite, application Home Assistant, ADB (Android Debug Bridge) | Affichage mural, écran éteint la nuit | ✅ en service |
| Réseau | Pi-hole | DNS local et blocage de pubs | 🔜 à installer |
| Réseau | VPN | Accès sécurisé à distance (solution à déterminer) | 🔜 à choisir |
| Monitoring | Grafana | Tableaux de bord de supervision | 🔜 à installer |

## 📍 État actuel

| Élément | Détail |
|---|---|
| Hyperviseur | Proxmox VE |
| CPU / RAM | Xeon E3-1241 v3 / 16 Go |
| Stockage | 1 × HDD 1 To |
| Réseau | Bridge `vmbr0` |
| VM | `docker-host` : Debian 13, 2 CPU, 6 Go de RAM, Docker 29 |

## ⚙️ Services

Tous tournent en conteneurs Docker dans la VM, gérés avec Portainer.

| Service | Rôle | État |
|---|---|---|
| Portainer CE 2.45 | Interface graphique de Docker | ✅ installé |
| Home Assistant 2026.10 | Domotique et dashboard | ✅ installé |
| Node-RED | Automatisations | ✅ installé, relié à Home Assistant |
| Pi-hole | DNS local et blocage de pubs | 🔜 à installer |
| VPN | Accès sécurisé à distance | 🔜 solution à déterminer |
| Grafana | Monitoring | 🔜 à installer |

Intégrations Home Assistant en place : Tuya, Google Cast, Google Translate text-to-speech, Spotify, Calendrier distant (Google Agenda), Met.no, Android Debug Bridge, HACS, Node-RED Companion.

## ⏰ Brief du matin

Un seul brief vocal par jour de cours, 35 min avant le premier cours : date, météo, cours du jour et événements de l'agenda du jour. Rien le week-end ni pendant les vacances.

| Jour | Début des cours | Brief |
|---|---|---|
| Lundi | 10h00 | 9h25 |
| Mardi | 8h50 | 8h15 |
| Mercredi | 13h20 | 12h45 |
| Jeudi | 8h25 | 7h50 |
| Vendredi | 8h00 | 7h25 |

## 🚧 Roadmap

- [x] Proxmox VE
- [x] VM Debian + Docker + Portainer
- [x] Home Assistant et Node-RED, reliés entre eux
- [x] Google Home et voix ajoutés dans Home Assistant
- [x] Test vocal du Google Home
- [x] Flow Node-RED : un brief vocal par jour de cours, 35 min avant le premier cours (`node-red/brief-du-matin.json`)
- [x] Dashboard Home Assistant « Maison » en paysage (`home-assistant/dashboard-maison.json`)
- [x] Afficher le dashboard sur la tablette (application Home Assistant)
- [x] Écran de la tablette éteint de 23h à 7h15 par ADB (`node-red/ecran-tablette.json`)
- [x] Lampes Tuya dans Home Assistant et dans le dashboard
- [ ] Finir le module des volets, puis l'ajouter au dashboard
- [ ] Pi-hole
- [ ] VPN (solution à déterminer)
- [ ] Grafana
