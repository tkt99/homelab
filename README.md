# Home Lab
### <ins>Purpose</ins>: To segment my own network (intranet) within my home network for tinkering and learning
***Learning Goals\*:***
- Computer Networking
- System Administration
- Defensive Cyber Security
- Network and Endpoint Forensics

*\*I hope to gain practical skills in these areas through mini projects within this home lab*

*My learning and thought processes can be seen in [this document](progress-notes.md)*

---

<ins>Hardware</ins>: HP Pavillion g6 laptop 
- CPU: Intel Core i5-2430M @ 2.4GHz, 4 cores
- RAM: 6 GB
- Storage: 600 GB
- Connection: via ethernet to a switch connected to the modem/router in my home

<ins>OS</ins>: [Proxmox Virtual Environment](https://www.proxmox.com/en/proxmox-ve) (Type 1 Hypervisor built within a Debian Linux distro)

---

# Proxmox Projects


## <ins>*Management:*</ins>


- [pfsense](https://www.pfsense.org/) - Firewall and router(FreeBSD VM)
  - [X] NAT forward web traffic to proxy
  - [X] DHCP
  - [X] OpenVPN server

## *<ins>Internal:</ins>*

- [pihole](https://pi-hole.net/) - DNS (Debian LXC)
  - [X] Main DNS server pointing to public DNS servers
  - [X] Internal DNS

- Ansible - Automate package installs with each new created Linux container 
  - [ ] packages to install:
    - [ ] sudo
    - [ ] vim
  - [ ] update repo
  - [ ] set up user and add to sudo 
  - [ ] configure static IP address if needed


## *<ins>Self-hosted Services:</ins>*
*(Only for LAN network outside of pfsense)*

- NGINX Web Server - Used as a reverse proxy to these web servers: (Debain VM)
  - [ ] [Heimdall](https://heimdall.site/) - Access every web interface from one place (LXC behind NGINX)
  - [X] [wiki.js](https://www.vultr.com/docs/install-wiki-js-with-node-js-postgresql-and-nginx-on-ubuntu-20-04-lts/) web app (Debian LXC behind NGINX)
    - [X] postgresql setup
    - [X] systemd service for starting web app on boot

- [Waterfall](https://github.com/PaperMC/Waterfall) - Minecraft Reverse Proxy Server (with NGINX VM or separate VM)
  - [X] PaperMC instance #1 - Close friends Minecraft Server (Debian LXC behind Waterfall)
    - [ ] get server domain


## *<ins>Security/Foresnics:</ins>*

- [X] [SIFT Workstation](https://github.com/teamdfir/sift-cli#installation) - Forensics (Ubuntu VM)
- [ ] Centralized security monitoring and logging (VM) 


