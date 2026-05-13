# ARP Spoofing and Network Sniffing Experiment
# NAME : PRIYADARSHINI K
# REG NO : 212224100046
## AIM

To perform ARP spoofing attack simulation and observe network sniffing behavior using Ettercap and Wireshark in a controlled LAN environment.

## TOOLS USED
Kali Linux

Ettercap (GUI)

Wireshark

Two virtual machines (Target systems in same network: 10.0.2.2 and 10.0.2.3)
## PROCEDURE / STEPS
### Step 1: Network Setup

Two systems (victims) were connected in the same virtual network:

Target 1: 10.0.2.2
Target 2: 10.0.2.3
### Step 2: Host Discovery using Ettercap

Ettercap was launched and the network was scanned to identify active hosts in the LAN.

### Step 3: Selecting Targets

Both detected hosts were added as:

Target 1
Target 2
### Step 4: ARP Poisoning Attack

ARP spoofing (MITM simulation) was initiated so that traffic between both targets is intercepted by the attacker machine.

### Step 5: Packet Monitoring

Wireshark was used to capture and analyze ARP packets to observe spoofing behavior and network anomalies.

## OBSERVATIONS FROM SCREENSHOTS
### Screenshot 1: Ettercap Host Discovery
<img width="1600" height="1054" alt="image" src="https://github.com/user-attachments/assets/18a2a79d-cb2b-432b-85ca-a8908a62180a" />
<img width="1600" height="998" alt="image" src="https://github.com/user-attachments/assets/dfd83eea-e0fd-4369-b77c-29defcbacbf9" />

### Explanation:
The above screenshots show the Ettercap application running on Kali Linux inside Oracle VirtualBox. Ettercap is a cybersecurity and network analysis tool used for monitoring network traffic and performing security testing. In the first screenshot, the tool scans the local network and identifies active hosts along with their IP addresses and MAC addresses. Two systems with the IP addresses 10.108.238.5 and 10.108.238.15 are detected and selected as Target 1 and Target 2. The log section at the bottom confirms that both hosts were successfully added to the target list. In the second screenshot, Ettercap displays the selected systems under “ARP poisoning victims,” indicating that the systems are prepared for ARP spoofing or Man-in-the-Middle (MITM) testing. This type of setup is commonly used in cybersecurity labs to analyze network vulnerabilities, monitor traffic flow, and understand how packet interception works in a controlled environment.

### Understanding:
This step confirms that both target machines are active in the same network and can communicate, which is necessary for ARP spoofing to work.This is the core phase of a Man-in-the-Middle (MITM) attack where traffic between two systems is silently redirected through the attacker machine.

### Screenshot 2: Wireshark ARP Packet Capture
<img width="1600" height="997" alt="image" src="https://github.com/user-attachments/assets/bf2d8f7a-add3-4861-8252-12b73cec33a8" />

### Explanation:
In this screenshot, the filter arp is applied to display only ARP (Address Resolution Protocol) packets. The captured packets show communication between devices in the local network, including requests such as “Who has 10.108.238.15? Tell 10.108.238.5.” These messages indicate that a system is trying to discover the MAC address associated with a specific IP address. The packet details section at the bottom provides detailed information about the selected ARP packet, including Ethernet and protocol-level data. This type of packet capture is commonly used in cybersecurity and networking labs to analyze network communication, troubleshoot connectivity issues, and study ARP spoofing or Man-in-the-Middle (MITM) attack behavior in a controlled environment.

### Understanding:
These duplicate ARP entries confirm that the network is receiving conflicting MAC address information, which is typical during ARP poisoning attacks.

## RESULT
The ARP spoofing and network sniffing experiment was successfully performed using Ettercap and Wireshark. The attack was simulated in a controlled environment, and ARP poisoning behavior was observed clearly through packet analysis.
