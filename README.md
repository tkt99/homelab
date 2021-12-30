# Home Lab

Hardware: HP Pavillion g6 laptop (connected via ethernet to a switch which is connected to the modem/router in my home)

OS: [Proxmox Virtual Environment](https://www.proxmox.com/en/proxmox-ve) (Type 1 Hypervisor built within a Debian Linux distro)

Purpose: To segment my own network (intranet) within my home network for tinkering and learning

## Proxmox Current Setup

### Active:


[pfsense](https://www.pfsense.org/) (FreeBSD VM from custom ISO)
- router/firewall 
- DHCP
- OpenVPN server
  
[pihole](https://pi-hole.net/) (Debian LXC)
- Main DNS server pointing to public DNS servers

[wiki.js](https://www.vultr.com/docs/install-wiki-js-with-node-js-postgresql-and-nginx-on-ubuntu-20-04-lts/) (Debian LXC)



### Inactive (Experimentation):

Docker (Alpine Linux VM)
  Attempted:
  - [BookStack](https://github.com/linuxserver/docker-bookstack) self-hosted web application
  - NGINX proxy manager with SSL certificate
  - DuckDNS
  

# TODO:

General:
- Host a minecraft server
- Centralized logging (SEIM + packet analysis)
- Automate package installs with every new Linux container

Web Apps:
- Access every web interface from one place ([Heimdall](https://heimdall.site/))
- Configure DNS to avoid typing in IP addresses within my intranet
- Harden wiki.js HTTP access for a more secure connection
- Configure reverse proxy with NGINX for web apps
