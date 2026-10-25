<div align="center">
    
> Étudiant BTS SIO SISR | Passionné réseau, cloud et électronique embarquée
> Je bricole du homelab depuis 2 ans — version actuelle refaite en 2026
> 
# 🏠 Homelab — Tom MAUDET

![Proxmox](https://img.shields.io/badge/Proxmox-E57000?style=for-the-badge&logo=proxmox&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Home Assistant](https://img.shields.io/badge/Home%20Assistant-41BDF5?style=for-the-badge&logo=homeassistant&logoColor=white)
![Cloudflare](https://img.shields.io/badge/Cloudflare-F38020?style=for-the-badge&logo=cloudflare&logoColor=white)

> Homelab personnel évolutif combinant virtualisation, réseau, IoT et automatisation cloud.

</div>

---

## 📍 État actuel

| Élément | Détail |
|---|---|
| Hyperviseur | Proxmox VE — installé ✅ |
| CPU / RAM | Xeon E3-1241 v3 / 16 Go |
| Stockage | 1 × HDD 1 To (extension prévue) |
| Réseau | Bridge `vmbr0` |
| NAS | Projet séparé — 5 × HDD 1 To |

---

## 🎯 Architecture cible

> Ce que le homelab doit devenir. Avancement détaillé dans la roadmap.

```
Internet
    │
Cloudflare Zero Trust (tunnel chiffré)
    │
Serveur — Proxmox
    ├── VM pfSense        → Routeur/Firewall — VLANs
    ├── LXC Pi-hole       → DNS filtering
    ├── LXC Home Assistant + Node-RED → Domotique & automatisation
    ├── LXC Grafana       → Monitoring
    └── LXC Docker        → Services conteneurisés
         │
    ESP32 (MQTT)
    ├── Volets connectés custom
    └── Capteurs environnementaux
```

---

## ⚙️ Services

| Service | Rôle | État |
|---|---|---|
| Docker | Socle des conteneurs | 🔜 à installer |
| Pi-hole | DNS local + blocage pub réseau entier | 🔜 à installer |
| Home Assistant | Domotique | 🔜 à installer |
| Node-RED | Automatisations (flows MQTT, webhooks) | 🔜 à installer |
| Grafana + Prometheus | Monitoring CPU, RAM, réseau | 🔜 à installer |
| pfSense | Routeur/Firewall, VLANs | 🔜 à installer |
| Cloudflare Tunnel + Access | Exposition sécurisée Zero Trust, HTTPS auto | 🔜 à installer |

---

## 🔌 IoT & Embarqué — 🔄 en cours

**Volets connectés custom**
- ESP32 programmé en C++ (Arduino/PlatformIO)
- Soudure en cours de finition
- Prévu : communication MQTT vers Home Assistant, automatisations Node-RED (horaires, capteurs)

**Capteurs environnementaux**
- ESP32 + DHT22 (température/humidité)
- Prévu : données remontées via MQTT → Grafana

---

## 🚧 Roadmap

- [x] Proxmox VE installé
- [ ] Docker
- [ ] Pi-hole
- [ ] Home Assistant + Node-RED
- [ ] Grafana + Prometheus
- [ ] pfSense — segmentation VLANs complète
- [ ] Cloudflare Tunnel + Access
- [ ] ESP32 — finir la soudure des volets et des capteurs
- [ ] GitHub Actions — CI/CD pipeline

---

## 📚 Stack technique

`Proxmox` `pfSense` `Docker` `Home Assistant` `Node-RED` `Grafana`
`Cloudflare` `ESP32` `MQTT` `Python`
