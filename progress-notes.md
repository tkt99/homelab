# Learning Journey

This document will be keep track of my troubleshooting processes and learning as my home lab evolves. (WIP)


## Starting out/Planning
Prior to starting a home lab, I had little to no knowledge of how networking really works in the real-world. The only networking knowledge I had was from an Introduction to Networking course. Starting out and establishing an initial topology along with defining what components control different parts of the networking definitely made me more familiar with the big picture of how everything is structured.

### pfSense setup (WAN/LAN)
- Situation: Initially, I wanted to create a segmented network within my home network so that I can set up and install anything I wanted without affecting the network of those that I live with. I did not know that I would install in my home lab at this point, but I knew I wanted to start with a pfSense firewall/router and try out pihole as the first software to install. After watching Youtube tutorials on installing pfSense, a lot of them mentioned that I needed at least two ethernet ports on my machine. I did not have that, so I was confused for a while on how I would go about segmenting a network. 

- Action: Eventually I found a video that the network bridges can be created within the Proxmox software itself, which would allow the physical ethernet port to act as a "WAN" (WAN network is my home network's LAN), and a Proxmox network bridge (vmbr01) as my segmented network's LAN. 

- Result: After setting pfSense up and setting it as a DHCP server, any future virtual machines or linux containers within Proxmox will be assigned an IP address separate to my home network's LAN.

### pihole (DNS)
### OpenVPN
- Situation: Setting up OpenVPN took a few attemps. At first, I could only get the pfSense OpenVPN server set up, and was not able to connect to it with the client which as a PC on my home network. 

- Action: Eventually, I decided to use Wireshark on the client and the server to really see what was going on behind the scenes. I had Wireshark capture packets on the server as well as on the client right after I run the "openvpn" command to connect to the server. I found out the server was not receiving anything from my "WAN" network and only showed LAN network communication. On the client, I see that it was sending out OpenVPN packets, but not receiving anything from my server network. 

- Result: With Wireshark, I concluded that I did not open the correct inbound ports on the client due to OpenVPN requiring TCP connection. After opening those ports with ufw, I was finally able to establish an OpenVPN tunnel and connect to my internal network from my PC in my home network. 

## Self-hosting services
### Port-forwarding and its implications


## Network and Server Security
### "Flat network" vs. DMZ's and Reverse Proxies
### Network forensics

## Home Lab vs. Home Server
### Future Plans and Direction of Home Lab evolution
After setting up services, I realized that there was a difference between a "home lab" and a "home server." Setting up and self hosting services was out of the question due to the security implications of hosting from my home router. Additionally, there aren't many things I wish to do in terms of self-hosting. If I want this project to continue, I knew I had to decide on which direction to take in terms of expanding. Since the main purpose of this lab is to learn technologies, I will continue it without enphasizing too much on hosting services, and emphasize it on the basis of a segmented network where I can set up and bring down services just for the sake of learning how it works. The areas of focus of these technologies will depend on what my interest it at the moment, and at the moment I would like to explore Network security and forensics in particular.

History of Interests:
1. Self-hosting
2. Network Security and forensics
