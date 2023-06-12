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
 18. └─> Take note of the provided Access URL for accessing Security Onion web configuration.
```
## Access Security Onion via SSH
...

## Firewall Allow Rule in Security Onion
...

## Access Security Onion Web Configuration Page
...

## Live Traffic in Future Lab Expansion
...

## Download PCAP for Malware Traffic Analysis
...

## Import Malware Traffic Analysis PCAP
...

## Analyzing Logs and Tools
...
