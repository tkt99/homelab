# Home Lab
### Purpose: To segment my own network (intranet) within my home network for tinkering and learning

Hardware: HP Pavillion g6 laptop 
- CPU: Intel Core i5-2430M @ 2.4GHz, 4 cores
- RAM: 6 GB
- Storage: 600 GB
- Connection: via ethernet to a switch connected to the modem/router in my home

OS: [Proxmox Virtual Environment](https://www.proxmox.com/en/proxmox-ve) (Type 1 Hypervisor built within a Debian Linux distro)


# Proxmox Projects


## Management: 


- [ ] [pfsense](https://www.pfsense.org/) - Firewall and router(FreeBSD VM)
  - [X] NAT forward web traffic to proxy
  - [X] DHCP
  - [X] OpenVPN server
  - [ ] Wireguard to replace OpenVPN
  - [ ] Snort (Separate LXC?)

- [ ] [Heimdall](https://heimdall.site/) - Access every web interface from one place (LXC behind NGINX)
- [ ] Splunk or ELK Stack - centralized logging (LXC behind NGINX)

## Internal: 

- [ ] [pihole](https://pi-hole.net/) - DNS (Debian LXC)
  - [X] Main DNS server pointing to public DNS servers
  - [X] Internal DNS

- [ ] Ansible - Automate package installs with each new created Linux container 
- [ ] NGINX - Reverse Proxy (Debain VM)
- [ ] [Waterfall](https://github.com/PaperMC/Waterfall) - Minecraft Reverse Proxy Server (with NGINX VM or separate VM)

## Services: 

- [ ] [wiki.js](https://www.vultr.com/docs/install-wiki-js-with-node-js-postgresql-and-nginx-on-ubuntu-20-04-lts/) web app (Debian LXC behind NGINX)

- [X] PaperMC instance #1 - Close friends Minecraft Server (Debian LXC behind Waterfall)
  - [ ] Server domain


## Experimental/Leanring:

- [ ] Play around with P2P networking and decentralized applications to learn its concepts
