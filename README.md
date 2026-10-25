# 🏠 Homelab

![Proxmox](https://img.shields.io/badge/Proxmox-E57000?style=for-the-badge&logo=proxmox&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Home Assistant](https://img.shields.io/badge/Home%20Assistant-41BDF5?style=for-the-badge&logo=homeassistant&logoColor=white)

Homelab personnel, refait de zéro en octobre 2026.

## 🎯 Objectif

Un dashboard Home Assistant sur une tablette, et un brief lu à voix haute chaque matin par un Google Home. Le tout fait partie d'une suite d'automatisations Node-RED, avec tout sous Docker.

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
| Grafana | Monitoring | 🔜 à installer |

Intégrations Home Assistant en place : Google Cast, Google Translate text-to-speech, HACS, Node-RED Companion.

## 🚧 Roadmap

- [x] Proxmox VE
- [x] VM Debian + Docker + Portainer
- [x] Home Assistant et Node-RED, reliés entre eux
- [x] Google Home et voix ajoutés dans Home Assistant
- [ ] Test vocal du Google Home
- [ ] Flow Node-RED : brief du matin lu par le Google Home
- [ ] Dashboard Home Assistant sur la tablette
- [ ] Pi-hole
- [ ] Grafana
