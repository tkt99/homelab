# Home Lab

Hardware: HP Pavillion g6 laptop (connected via ethernet to a switch which is connected to the modem/router in my home)

OS: [Proxmox Virtual Environment](https://www.proxmox.com/en/proxmox-ve) (Type 1 Hypervisor built within a Debian Linux distro)

Purpose: To isolate a own network within my home network for tinkering and learning fun

Goals:
- Control every service from one place
- Have an organized system so that I can add services in the future in an easier manner (Ansible?)
- See and understand how everything communicates with each other under the hood for learning and curiosity

### Proxmox VE

- [X] [pfsense](https://www.pfsense.org/)
  - router/firewall 
  - DHCP
  - OpenVPN server (for remote access from my PC within my home network)
  - [ ] Wireguard setup to replace OpenVPN

- [X] [pihole](https://pi-hole.net/)
  - Main DNS server pointing to public DNS servers
  - Internal DNS
  - Filters DNS 

- [ ] Docker VM (running docker-compose files for now will switch to Portainer):
  - [X] [BookStack](https://www.bookstackapp.com/) for self-hosted documentation/wiki (VPN access only)
  - [ ] BookStack with [DuckDNS](https://www.duckdns.org/) and [NGINX Proxy Manager](https://nginxproxymanager.com/) (public access with HTTPS to replace this)

- [ ] Minecraft Server LXC
- [ ] Dashboard to access all web interfaces in one place (Heimdall)
- [ ] Network statistics/logging (WireShark through ssh X forwarding?)

