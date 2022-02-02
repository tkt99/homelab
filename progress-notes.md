_This document will be keep track of my thoughts as the home lab evolves._

# Learning Journey

**Self-hosting:**
Originally, I wanted to document my progress on a self-hosted wiki application, but having realized the security implications of self-hosting as well as keeping the documentation of the Home Lab on the Home Lab itself, I concluded that was not the best idea, and decided to scrap it.

**Network Security and forensics:**
Even though I won't self-host, I would still like to learn about how to secure my network if I were to self-host. Additionally for forensics and having some experience with Wireshark, I've always enjoyed diving into the details.

**Spyware Analysis:**
I tend to be paranoid of my data being tracked online and/or having the microphones and cameras on my devices being compromised, so this seems like a good opportunity to take the matters into my own hands and see under the hood while learning about forensics. I plan to execute malware such as spyware on the lab and observe what happens on the network through forensics.

**Threat Modeling:**
However, before diving deep into the tools and technology, I feel like it would be wise to take into consideration the actual threat I am defending from instead of taking action based on paranoia.

**Malware Analysis:**
Additionally, before I execute malware randomly, since I am on a network where others are on it as well, I want to be careful to properly segment my network so that no inbound or outbound connections can be made besides a VPN connection. I will need some guidance on this, so I will ask those in my network that has more experience than I do.

The next few sections will describe the troubleshooting and learning processes of each section of the lab.

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
After setting up services, I realized that there was a difference between a "home lab" and a "home server." Setting up and self hosting services was out of the question due to the security implications of hosting from my home router. Additionally, there aren't many things I wish to do in terms of self-hosting. If I want this project to continue, I knew I had to decide on which direction to take in terms of expanding. Since the main purpose of this lab is to learn technologies, I will continue it without enphasizing too much on hosting services, and emphasize it on the basis of a segmented network where I can set up and bring down services just for the sake of learning how it works. The areas of focus will depend on my interest at the moment which can be seen under the "Learning Journey" section.



