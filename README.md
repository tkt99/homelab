# Home Lab

Hardware: HP Pavillion g6 laptop (connected via ethernet to a switch which is connected to the modem/router in my home)

OS: [Proxmox Virtual Environment](https://www.proxmox.com/en/proxmox-ve) (Type 1 Hypervisor built within a Debian Linux distro)

Purpose: To segment my own network (intranet) within my home network for tinkering and learning

## Proxmox VE setup

- [X] [pfsense](https://www.pfsense.org/)
  - [X] router/firewall 
  - [X] DHCP
  - [X] OpenVPN server
  - [ ] Wireguard (replaces OpenVPN)
  
- [X] [pihole](https://pi-hole.net/)
  - [X] Main DNS server pointing to public DNS servers
  - [ ] Internal DNS

- [X] wiki.js LXC
- [ ] Minecraft Server LXC
- [ ] Dashboard to access all web interfaces in one place (Heimdall)
- [ ] Network statistics/logging (WireShark through ssh X forwarding?)


# TODO:

- Host a minecraft server
- Configure DNS to avoid typing in IP addresses within my intranet
- Centralized logging
- Access every service from one place ([Heimdall](https://heimdall.site/))
- Harden wiki.js access to secure connection
