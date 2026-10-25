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
| VM | Debian, avec Docker et Portainer |

## ⚙️ Services

| Service | Rôle | État |
|---|---|---|
| Docker + Portainer | Conteneurs et interface graphique | ✅ installé |
| Home Assistant | Domotique et dashboard | ✅ installé |
| Node-RED | Automatisations | ✅ installé, relié à Home Assistant |
| Pi-hole | DNS local et blocage de pubs | 🔜 à installer |
| Grafana | Monitoring | 🔜 à installer |

## 🚧 Roadmap

- [x] Proxmox VE
- [x] VM Debian + Docker + Portainer
- [x] Home Assistant et Node-RED, reliés entre eux
- [ ] Google Home dans Home Assistant (test vocal)
- [ ] Flow Node-RED : brief du matin lu par le Google Home
- [ ] Dashboard Home Assistant sur la tablette
- [ ] Pi-hole
- [ ] Grafana
