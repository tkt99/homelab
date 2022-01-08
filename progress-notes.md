# Learning Journey

This document will be keep track of my troubleshooting processes and learning as my home lab evolves. (WIP)

## Starting out/Planning
### pfSense setup (WAN/LAN)
### pihole (DNS)
### OpenVPN
Setting up OpenVPN took a few attemps. At first, I could only get the pfSense OpenVPN server set up, and was not able to connect to it with the client. Eventually, I decided to use Wireshark on the client and the server to really see what was going on behind the scenes. I had Wireshark capture packets on the server as well as on the client right after I run the "openvpn" command to connect to the server. I found out the server was not receiving anything from my "WAN" network and only showed LAN network communication. On the client, I see that it was sending out OpenVPN packets, but not receiving anything from my server network. This is what told me that I forgot to open the correct ports on the client due to OpenVPN being a TCP connection. 

## Self-hosting services
### Port-forwarding and its implications


## Network and Server Security
### "Flat network" vs. DMZ's and Reverse Proxies
### Network forensics

## Home Lab vs. Home Server
### Future Plans and Direction of Home Lab evolution
