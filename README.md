# Traffic Analysis using Security Onion

This repository documents a homelab project focused on enhancing threat detection and analysis knowledge using Security Onion. The project provides step-by-step instructions for setting up Security Onion, accessing it via SSH and web configuration page, importing PCAP files, and analyzing logs. 

## Table of Contents
- [Download Links](#download-links)
- [Security Onion VM Configuration](#security-onion-vm-configuration)
- [Security Onion Installation Points](#security-onion-installation-points)
- [Access Security Onion via SSH](#access-security-onion-via-ssh)
- [Firewall Allow Rule in Security Onion](#firewall-allow-rule-in-security-onion)
- [Access Security Onion Web Configuration Page](#access-security-onion-web-configuration-page)
- [Live Traffic in Future Lab Expansion](#live-traffic-in-future-lab-expansion)
- [Download PCAP for Malware Traffic Analysis](#download-pcap-for-malware-traffic-analysis)
- [Import Malware Traffic Analysis PCAP](#import-malware-traffic-analysis-pcap)
- [Analyzing Logs and Tools](#analyzing-logs-and-tools)

## Download Links
- VMware: [Download VMware Workstation](https://www.vmware.com/products/workstation-player/workstation-player-evaluation.html)
- Security Onion: [Download Security Onion ISO](https://securityonion.net/Download)

## Security Onion VM Configuration
Minimum required specs:

- 4GB RAM
- 2 CPU cores
- 200GB storage

Note: These specs are sufficient for PCAP import functionality. To perform more resource-intensive tasks or expand your lab, consider allocating additional resources accordingly.

- Use a Network Adapter in NAT connection

![image](https://github.com/Muneer44/Security-Onion-Traffic-Analysis/assets/117259069/e895b677-2d87-444a-8674-a2b77c13de5f)

## Security Onion Installation guide
<img src="https://github.com/Muneer44/Security-Onion-Traffic-Analysis/assets/117259069/59b85019-5742-4014-bf30-00cd3ca6f03b" width="450" height="300">

<img src="https://github.com/Muneer44/Security-Onion-Traffic-Analysis/assets/117259069/442f03cf-c84d-4008-bf5e-f66915124366" width="500" height="280">

Type 'yes' and create an admin username and password, which will be used to access your Security Onion console.

```
  ## Security Onion Installation Navigation:
  
  1. Start the Security Onion installation.
  2. ┌─> Choose the option to Install Security Onion.
  3. │ └─> Select "Import" as the installation type.
  4. │  └─> "AGREE" to the terms and conditions.
  5. │   └─> Confirm the minimum requirements popups.
  6. │    └─> Enter a hostname for your Security Onion instance.
  7. │     └─> Choose the desired network interface card (NIC) from the available options.
  8. │      └─> Select DHCP to automatically configure network settings.
  9. │       └─> Choose Yes to proceed with the selected network configuration.
 10. │        └─> Accept the default settings by selecting OK.
 11. │         └─> Select the Standard installation type.
 12. │          └─> Choose the Direct mode for packet capture.
 13. │           └─> Accept the defaults for log disk size and memory configuration.
 14. │            └─> Set an email and password for accessing the Security Onion web configuration. Note down this information for future use.
 15. │             └─> Choose IP to access the web interface.
 16. |              └─> Choose Yes to configure NTP server and keep the defaults.
 17. |               └─> Choose No to so-allow access to the web tools. (We will set this up later). 
 18. |                └─> Take note of the provided Access URL for accessing Security Onion web configuration.
 19. └─> Reboot and Login into your security onion machine
 ```
 <img src="https://github.com/Muneer44/Security-Onion-Traffic-Analysis/assets/117259069/65839efd-94c8-4950-b43a-8e655e8637fe" width="500" height="280">


## Access Security Onion via SSH

1. Open a terminal on your local machine.
   ```shell
   ssh <security-onion-username>@<security-onion-ip>
<img src="https://github.com/Muneer44/Security-Onion-Traffic-Analysis/assets/117259069/bce5306f-f4b7-4b2d-8e88-60b66dae5aca" width="500" height="280">
   
   
## Create Firewall Rule in Security Onion
_Give local machine access to Security Onion's web interface_
  ```shell
   - sudo so-allow 
   - Choose option '[a] - Analyst'
   - <IP-address of local machine>
  ```
 <img src="https://github.com/Muneer44/Security-Onion-Traffic-Analysis/assets/117259069/b880dc5a-95e3-4153-a558-d28be9e977bc" width="500" height="280">

## Access Security Onion Web Configuration Page
`- browse <Security-Onion-IP-address>`
  
<img src="https://github.com/Muneer44/Security-Onion-Traffic-Analysis/assets/117259069/439ff556-9318-4b05-b7d8-203aa78c09b5" width="500" height="280">
  

  <img src="" width="500" height="280">

## Live Traffic in Future Lab Expansion
...

## Download and Import PCAP for Malware Traffic Analysis

_Links: [Malware-Traffic-PCAP](https://github.com/pan-unit42/Wireshark-quizzes/blob/main/2023-04-Unit42-Wireshark-quiz.pcap.zip) and [Unzip Password](https://github.com/pan-unit42/Wireshark-quizzes/blob/main/README.md)_

_Use the following commands to import the PCAP file in Security Onion:_
   ```shell
   - wget <Malware-Traffic-PCAP-Link_address>
   - unzip <PCAP-filename>   #You can use 'ls' command to list the files
   - sudo so-import-pcap <PCAP-filename> 
   ```
---
<img src="https://github.com/Muneer44/Security-Onion-Traffic-Analysis/assets/117259069/4e8aff8b-5d98-436c-b42a-073bf7be7c17" width="850" height="280">
<img src="https://github.com/Muneer44/Security-Onion-Traffic-Analysis/assets/117259069/73fba7c3-655b-4567-b1f6-eaf8d9db39a4" width="550" height="150">
<img src="https://github.com/Muneer44/Security-Onion-Traffic-Analysis/assets/117259069/102efea2-5d89-4ecf-aead-ac247ae004d6" width="700" height="280">


## Analyzing Logs and exploring tools
Dashboard:
![image](https://github.com/Muneer44/Security-Onion-Traffic-Analysis/assets/117259069/40c84f4c-3572-40df-8278-c8bc6ff0f390)

Kabana/ Elastic: Elasticsearch serving as a distributed search and analytics engine, and Kibana providing a web-based visualization and exploration interface for analyzing the data stored in Elasticsearch.
![image](https://github.com/Muneer44/Security-Onion-Traffic-Analysis/assets/117259069/80de2d62-339f-4334-a142-5d126b61156f)

Grafana: A versatile data visualization and monitoring tool that enables users to create and explore interactive dashboards of different Security onion machines
![image](https://github.com/Muneer44/Security-Onion-Traffic-Analysis/assets/117259069/47f64462-38a6-4afe-9411-3eb1cbeb0ff6)

CyberChef: A web application for performing various cryptographic, encoding, and data manipulation tasks.
![image](https://github.com/Muneer44/Security-Onion-Traffic-Analysis/assets/117259069/8edaa5a9-4566-4357-86fd-7a5320383085)
![image](https://github.com/Muneer44/Security-Onion-Traffic-Analysis/assets/117259069/deecdb21-3ccb-4872-9f13-70a2561eebe6)


