# Explore Network Sniffing and ARP Attacks

# AIM:

To explore network sniffing and ARP Attacks

## STEPS:

- `Step 1:` Install kali linux either in partition or virtual box or in live mode
- `Step 2:` Investigate on the various categories of tools as follows.
-  `Step 3:` Open terminal and try execute some kali linux commands

## ARP Attacks:  
ARP spoofing: A hacker sends fake ARP packets that link an attacker's MAC address with an IP of a computer already on the LAN. 

```
arpspoof -i eth0 -t <victim_IP> <gateway_IP>
```
## Tools Commonly Used:

**ARP Spoofing:** arpspoof, ettercap, bettercap

**Sniffing:** wireshark, tcpdump, dsniff
## Architecture Diagram
```
                     +-------------------+
                     |   Attacker (Kali) |
                     |  [ARP Spoof Tool] |
                     +---------+---------+
                               |
               +---------------+----------------+
               |                                |
       +-------v-------+              +---------v--------+
       | Victim Device |              | Gateway/Router   |
       | (e.g., Laptop)|              | (Default Gateway)|
       +---------------+              +------------------+
               |                                |
       ====== Normal ARP Traffic ===============|
               |                                |
               +---------> Internet             |
                         (DNS, HTTP, etc.)      |
                                                |
                  [Start ARP Spoofing/Poisoning]
                               |
                               v
               +-------------------------------+
               |  Attacker becomes MITM        |
               | (Man-in-the-Middle via ARP)   |
               +-------------------------------+
                               |
                     [Sniff Packets Using]
                 e.g., Wireshark, tcpdump, Ettercap

         +----------------------------------------------+
         | Captured Info:                               |
         |  - IP Addresses                              |
         |  - DNS Requests                              |
         |  - HTTP/HTTPS Data (if not encrypted)        |
         |  - Credentials (if sent in plain text)       |
         +----------------------------------------------+

```
## ARP Attacks:  
ARP spoofing: A hacker sends fake ARP packets that link an attacker's MAC address with an IP of a computer already on the LAN. 
Boot kali and Windows7 virtual machines.
In windows 7 give the command arp -a
## OUTPUT:
<img width="951" height="509" alt="image" src="https://github.com/user-attachments/assets/65c3b36a-756b-4f28-a605-9eb39acf774f" />



From weak website login to the website:
## OUTPUT:

<img width="963" height="657" alt="image" src="https://github.com/user-attachments/assets/a6117e0c-6923-4468-bc9b-f0289dbfd6ba" />



## OUTPUT:
<img width="952" height="688" alt="image" src="https://github.com/user-attachments/assets/93e75b67-6d20-4efe-a70b-fd63eb1aaaca" />



Now using kali linux open the wireshark and segerate the "http"  and see for the Get ip address and follow it oot the http stream
## OUTPUT:
<img width="958" height="890" alt="image" src="https://github.com/user-attachments/assets/a539631a-e9d6-43c0-8ad2-48d1e78ac263" />



## RESULT:
The kali linux tools for ARP Attack and Network Sniffing were identified successfully
