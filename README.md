# Home Lab

Hardware: HP Pavillion g6 laptop (connected via ethernet to a switch which is connected to the modem/router in my home)

OS: [Proxmox Virtual Environment](https://www.proxmox.com/en/proxmox-ve) (Type 1 Hypervisor built within a Debian Linux distro)

Purpose: To segment my own network (intranet) within my home network for tinkering and learning

Goals/Projects:
- Control every service from one place ([Heimdall](https://heimdall.site/))
- Host a web application securely so that my home network can access it without needing a VPN
  - Firewall rules/configuration
  - Reverse Proxy?
  - web applications managed by Docker

### Proxmox VE

- [X] [pfsense](https://www.pfsense.org/)
  - [X] router/firewall 
  - [X] DHCP
  - [X] OpenVPN server (for remote access from my PC within my home network)
  - [ ] Wireguard setup to replace OpenVPN
  
- [X] [pihole](https://pi-hole.net/) (Filters and blocks DNS according to block list)
  - [X] Main DNS server pointing to public DNS servers
  - [ ] Internal DNS

- [ ] Docker VM (running docker-compose files for now will switch to Portainer):
  - [X] [BookStack](https://www.bookstackapp.com/) for self-hosted documentation/wiki (VPN access only)
   
- [ ] Minecraft Server LXC
- [ ] Dashboard to access all web interfaces in one place (Heimdall)
- [ ] Network statistics/logging (WireShark through ssh X forwarding?)

* within my home network, but not inside the internal pfsense network


# TODO:

- port-forward web traffic to Docker VM and test if IP reached the VM
- test if web traffic can reach BookStack
- configure BookStack to work nginx

