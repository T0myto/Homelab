<div align="center">
    
> Étudiant BTS SIO SISR | Passionné réseau, cloud et électronique embarquée
> Construit et maintiens une infrastructure homelab depuis 2 ans
> 
# 🏠 Homelab — Tom MAUDET

![Proxmox](https://img.shields.io/badge/Proxmox-E57000?style=for-the-badge&logo=proxmox&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Home Assistant](https://img.shields.io/badge/Home%20Assistant-41BDF5?style=for-the-badge&logo=homeassistant&logoColor=white)
![Cloudflare](https://img.shields.io/badge/Cloudflare-F38020?style=for-the-badge&logo=cloudflare&logoColor=white)
![Azure](https://img.shields.io/badge/Azure-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white)

> Homelab personnel évolutif combinant virtualisation, réseau, IoT et automatisation cloud.

</div>

---

## 🗺️ Architecture réseau

```
Internet
    │
Cloudflare Zero Trust (tunnel chiffré)
    │
Mini PC — Proxmox
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

## 🖥️ Infrastructure

| Composant | Technologie | Détail |
|---|---|---|
| Hyperviseur | Proxmox VE | VMs + conteneurs LXC sur Mini PC |
| Firewall/Routeur | pfSense | VLANs, règles firewall, DNS |
| Exposition sécurisée | Cloudflare Tunnel + Access | Zero Trust, HTTPS auto, auth |
| DNS local | Pi-hole | Blocage pub réseau entier |
| Monitoring | Grafana + Prometheus | CPU, RAM, réseau en temps réel |

---

## ⚙️ Services

| Service | Stack | Accès |
|---|---|---|
| Domotique | Home Assistant | homeassit.tom-maudet.fr |
| Automatisation | Node-RED | Flows MQTT, webhooks |
| Reverse proxy | Cloudflare Tunnel | SSL automatique |

---

## 🔌 IoT & Embarqué

**Volets connectés custom**
- ESP32 programmé en C++ (Arduino/PlatformIO)
- Communication MQTT vers Home Assistant
- Automatisations Node-RED (horaires, capteurs)

**Capteurs environnementaux**
- ESP32 + DHT22 (température/humidité)
- Données remontées via MQTT → Grafana

---

## 🎓 Certifications

- ✅ Cisco (Networking/Troubleshooting)
- ✅ Microsoft Azure
- ✅ Docker
- 🔄 Python — en cours
- 🔜 Terraform
- 🔜 Ansible

---

## 🚧 Roadmap

- [ ] pfSense — segmentation VLANs complète
- [ ] Ansible — automatisation config VMs
- [ ] Terraform — déploiement infra Azure
- [ ] GitHub Actions — CI/CD pipeline
- [ ] Azure IoT Hub — connexion ESP32 cloud
- [ ] AZ-220 Azure IoT Developer

---

## 📚 Stack technique

`Proxmox` `pfSense` `Docker` `Home Assistant` `Node-RED` `Grafana`
`Cloudflare` `ESP32` `MQTT` `Python` `Ansible` `Terraform` `Azure`
