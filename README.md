# Home Lab
### Purpose: To segment my own network (intranet) within my home network for tinkering and learning

Hardware: HP Pavillion g6 laptop 
- CPU: Intel Core i5-2430M @ 2.4GHz, 4 cores
- RAM: 6 GB
- Storage: 600 GB
- Connection: via ethernet to a switch connected to the modem/router in my home

OS: [Proxmox Virtual Environment](https://www.proxmox.com/en/proxmox-ve) (Type 1 Hypervisor built within a Debian Linux distro)

- [X] = Succeeeded
- [ ] = Planned
-     = Attempted


# Proxmox Projects


## Management: 


- [ ] [pfsense](https://www.pfsense.org/) (FreeBSD VM)
  - [X] router/firewall 
  - [X] DHCP
  - [X] OpenVPN server
  - [ ] Wireguard


- [ ] Access every web interface from one place ([Heimdall](https://heimdall.site/))
- [ ] Centralized logging (SEIM + packet analysis)

## Internal: 

- [ ] [pihole](https://pi-hole.net/) (Debian LXC)
  - [X] Main DNS server pointing to public DNS servers
  - [ ] Internal DNS

- [ ] Automate package installs with each new created Linux container
- [ ] Configure DNS to avoid typing in IP addresses within my intranet

## Services: 

- [X] web app through HTTP and port-forwarding ([wiki.js](https://www.vultr.com/docs/install-wiki-js-with-node-js-postgresql-and-nginx-on-ubuntu-20-04-lts/) on Debian LXC)

- [ ] web app through HTTPS (Docker on Alpine Linux VM)
  - [X] [BookStack](https://github.com/linuxserver/docker-bookstack) self-hosted web application
  - NGINX proxy manager with Let's Encrypt SSL certificate
  - Access through DuckDNS

- [ ] Minecraft Server (Debian LXC)
  - [X] Host port-forwarded minecraft server
  - [X] Use [Waterfall](https://github.com/PaperMC/Waterfall) to act as a proxy to the Minecraft server
  - [ ] Mask IP address


## Experimental/Leanring:

- [ ] Play around with P2P networking and decentralized applications to learn its concepts
