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

<img width="1919" height="1012" alt="Screenshot 2025-09-20 084305" src="https://github.com/user-attachments/assets/f2f54546-ecca-4988-9d53-aba58a6f7662" />


## OUTPUT:
<img width="1867" height="1084" alt="Screenshot 2025-09-20 090559" src="https://github.com/user-attachments/assets/ed1d5200-cbf5-4d37-8d15-54eb157e7be3" />


Now using kali linux open the wireshark and segerate the "http"  and see for the Get ip address and follow it oot the http stream
## OUTPUT:
<img width="1918" height="1118" alt="Screenshot 2025-09-20 093232" src="https://github.com/user-attachments/assets/0763dbf6-115e-4c50-afef-4b3eb7bb73f4" />


## RESULT:
The kali linux tools for ARP Attack and Network Sniffing were identified successfully
