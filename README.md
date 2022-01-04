# Home Lab
### Purpose: To segment my own network (intranet) within my home network for tinkering and learning

Hardware: HP Pavillion g6 laptop 
- CPU: Intel Core i5-2430M @ 2.4GHz, 4 cores
- RAM: 6 GB
- Storage: 600 GB
- Connection: via ethernet to a switch connected to the modem/router in my home

OS: [Proxmox Virtual Environment](https://www.proxmox.com/en/proxmox-ve) (Type 1 Hypervisor built within a Debian Linux distro)


# Proxmox Current Setup

[pfsense](https://www.pfsense.org/) (FreeBSD VM)
- router/firewall 
- DHCP
- OpenVPN server
  
[pihole](https://pi-hole.net/) (Debian LXC)
- Main DNS server pointing to public DNS servers
- Filters and logs DNS queries

# Experimental/Learning

- [X] = Succeeeded
- [ ] = Attempted/Planned

- [X] web app through HTTP and port-forwarding ([wiki.js](https://www.vultr.com/docs/install-wiki-js-with-node-js-postgresql-and-nginx-on-ubuntu-20-04-lts/) on Debian LXC)

- [ ] web app through HTTPS (on Alpine Linux VM)
  - [X] [BookStack](https://github.com/linuxserver/docker-bookstack) self-hosted web application
  - [ ] NGINX proxy manager with Let's Encrypt SSL certificate
  - [ ] Access through DuckDNS

- [ ] Minecraft Server
  - [X] Host port-forwarded minecraft server
  - [X] Use [Waterfall](https://github.com/PaperMC/Waterfall) to act as a proxy to the Minecraft server
  - [ ] Mask IP address


  


# Current TODO:

General:
- Automate package installs with each new created Linux container
- Centralized logging (SEIM + packet analysis)
- Setup Wireguard or automate the way I connect with OpenVPN (OpenVPN connected through command line from PC within my home LAN)

Web Apps:
- Access every web interface from one place ([Heimdall](https://heimdall.site/))
- Configure DNS to avoid typing in IP addresses within my intranet
- Configure reverse proxy with NGINX for web apps

P2P:
- Play around with P2P networking and decentralized applications to learn its concepts
