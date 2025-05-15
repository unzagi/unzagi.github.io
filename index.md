---

## 2025-05-15 - Update

Back in February, I spec’d a new PC to dive into AI/LLMs and sharpen my networking skills during a career break. By May, I’d spun up a full observability stack, built version control, hosted internal DNS, deployed Docker and LXC services, and explored a suite of self-hosted tools — with ChatGPT as my hands-on assistant and research partner throughout.

What began as a modest AI lab has evolved into a production-grade home infrastructure — reconnecting me with my sysadmin roots while pushing into automation, AI integration, and modern networking.

Next up: populating NetBox as the single source of truth for my network, laying the groundwork for LLM-powered querying and infrastructure automation.

Here’s a snapshot of what I’ve built so far, and a preview of the topics I’ll dive into in upcoming posts.

---

## Work Completed

### Lab Rig
- Chosen Spec specifically to support a medium LLMs
- Dual-boot Linux/Windows
- Geforce 4070 Ti Super
- 128GB RAM
- Containerlab installed
- First tests with LLM images completed

### OpnSense Firewall
- Rebuilt a 2016 gaming PC into a dedicated OpnSense box
- Configured WireGuard VPN
- Added 10G NIC to Firewall to Juniper EX2300
- Fully migrated from ISP CPE to OpnSense

### Mon1 – Docker Monitoring Host
- Dockerized:
  - Grafana
  - Prometheus
  - cAdvisor
  - Portainer
  - Node_Exporter
  - Junos_Exporter
  - InfluxDB
  - Technitium DNS (DNS1)
  - GitLab
  - ELK Stack: Elasticsearch, Logstash, Kibana, Filebeat, Elastalert
  - Maltrail, Zenarmor Cloud, CrowdSec
- Home Assistant data exported to InfluxDB
- IDS enabled on OpnSense
- Built Mon1 dashboards in Grafana
- Temporarily crashed due to RAM pressure from GitLab + Security stack
- Upgraded to 32GB RAM, resumed services
- Slack & Telegram alert testing with Grafana
- Added Homarr dashboard
- Backup scripts using Python + crontab

### Mon2 – Jellyfin + Docker Server
- Jellyfin media server
- Dockerized DNS 2 with Technitium
- DNS1 & DNS2 in HA failover config
- Dockerized:
  - cAdvisor
  - Node_Exporter
  - Portainer
  - NTP
- Grafana dashboards for Mon2

###  eBay Box → Proxmox Server
- Purchased additional PC for Proxmox
- Installed 10G NIC and uplinked to EX2300

### Mon3 – Docker VM on Proxmox
- Mailu server deployed for internal mail notifications (e.g., GitLab over TLS)

###  Mon4 – Docker Host
- Experimented with `step-ca` + `acme.sh`
- Moved back to OpenSSL for internal CA
- Dockerized GitLab Mirror
- Configured repo mirroring between GitLab (Mon1) and GitLab-Mirror (Proxmox)

###  Proxmox Services
- Second Grafana + Prometheus instance on Proxmox
- Backup/Dev platform for monitoring
- NetBox VM installed
- Initial Ansible scripts built for host config (Mon1, Mon2, Lab Windows)

###  Home Assistant
- Built a VoIP phone that connects directly to LLM
- Using HA's private voice assistant stack  
  [Home Assistant Voice](https://www.home-assistant.io/voice_control/worlds-most-private-voice-assistant/)

### Gitlab Pages
- Building out this blog in Jekyll
- Mirroring a Gitlab Pages version internally

---

##  Future Work - Not in Order

### NetBox
- Build Ansible playbooks to automate population
- Use it as a source of truth for LLM queries
- Model Docker containers and services
- Document IoT fleet inside Home Assistant

### Documentation
- Visio-style network/environment diagrams

### Containerlab
- Juniper EVPN/VXLAN topologies

### LLM Research
- Explore running MCP locally
- Follow work by [John Capobianco](https://www.linkedin.com/in/john-capobianco-644a1515/)

### Alerting
- Create unified alerting across:
  - Email
  - Telegram
  - Home Assistant VoIP phone

### Backups
- Finalize and document backup strategy
