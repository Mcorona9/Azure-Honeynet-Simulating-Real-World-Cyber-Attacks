  <p align="center">


# Azure-Honeynet & SOC (Live Traffic)
</p>

  <p align="center">
<img src="https://i.imgur.com/JZRjPfT.png" height="80%" width="80%" alt="Sentinel logo"/>

## Introduction
My objective for this project is to create a customized honeynet on Microsoft Azure. The honeynet will be strategically designed to entice attackers, allowing for comprehensive logging and monitoring of malicious traffic. Additionally, I will implement incident response protocols and robust hardening measures to ensure the utmost security of the environment."

## Objective  
"After creating Windows and Linux virtual machines, I intentionally configured the firewall and network gateway settings to allow unrestricted traffic from all ports. Furthermore, I disabled all features in Microsoft Defender Firewall. As a result, I have intentionally created a vulnerable internet-facing environment designed to attract potential attackers

## Technologies, Regulations, and Azure Components Employed:
- Azure Virtual Network (VNet)
- Azure Network Security Group (NSG)
- Virtual Machines (2x Windows, 1x Linux)
- Log Analytics Workspace with Kusto Query Language (KQL) Queries
- Azure Key Vault for Secure Secrets Management
- Azure Storage Account for Data Storage
- Microsoft Sentinel for Security Information and Event Management (SIEM)
- Microsoft Defender for Cloud to Protect Cloud Resources
- Windows Remote Desktop for Remote Access
- Command Line Interface (CLI) for System Management
- PowerShell for Automation and Configuration Management
- NIST SP 800-53 Revision 4 for Security Controls
- NIST SP 800-61 Revision 2 for Incident Handling Guidance

## 
  <p align="center">
<img src="https://i.imgur.com/LUAvrtd.png" height=50%" width="50%" alt="Disk Sanitization Steps"/>

##
  <p align="center">
<img src="https://i.imgur.com/owwop2p.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>


## Attack Maps Before Hardening/ Security Controls
<p align="center">
 <b> This attack map highlights the repercussions of leaving the Network Security Group (NSG) exposed, enabling unrestricted passage of malicious traffic. This visualization emphasizes the significance of enforcing effective security measures, such as imposing restrictions on NSG rules, to thwart unauthorized access and mitigate potential threats.

##
   <p align="center">
<img src="https://i.imgur.com/j0Ih9Qk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <p align="center">
     The attack map reveals a multitude of syslog authentication failures encountered by the Linux server I implemented, signaling unauthorized access attempts originating externally. This underscores the significance of fortifying Linux servers with robust authentication mechanisms and vigilantly monitoring system logs to detect indicators of intrusion attempts, serving as a pertinent reminder of their importance.
 ##
   <p align="center">
<img src="https://i.imgur.com/ApgwnXn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> 
 <p align="center">
The attack map presents a vivid display of numerous RDP and SMB failures, highlighting the continuous endeavors of potential attackers to exploit these protocols. This visualization underscores the imperative of safeguarding remote access and file sharing services to shield against unauthorized entry and mitigate potential cyber threats
 ##
   <p align="center">
<img src="https://i.imgur.com/HsYV1z2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> 


   <p align="center">
This dynamic world map provides a comprehensive visualization of the relentless attacks directed towards the MSSQL Server across various geographical locations
##
   <p align="center">
<img src="https://i.imgur.com/CZlc8sd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> 

## Analysis & Incident Assessment 

   <p align="center">
During the 24-hour duration of running the vulnerable environment, I evaluated multiple incidents. For each incident, I meticulously scrutinized details concerning the entities behind these attacks, including their IP addresses, employed tactics and techniques, the type of attack executed, and the timeline of each occurrence. Additionally, I conducted in-depth investigations into the IP addresses of these entities, thoroughly examining any associated alerts to ascertain whether each incident constituted a true positive or a false positive.

 <p align="center">
 <img src="https://i.imgur.com/udWy7sk.png" height="90%" width="90%" alt="Disk Sanitization Steps"/> 

  <p align="center">
 <img src="https://i.imgur.com/FA2Akqm.png" height="50%" width="50%" alt="Disk Sanitization Steps"/> 

 <p align="center">
 <img src="https://i.imgur.com/ptdb21g.png" height="50%" width="50%" alt="Disk Sanitization Steps"/> 

  ## 
  Metrics Before Hardening / Security Controls

 
   <p align="center">
  
  | Metric                          |   Count
| ------------------------        |   -----
| SecurityEvent                   |   27052
| Syslog                          |   7003
| SecurityAlert                   |   9
| SecurityIncident                |   265
| AzureNetworkAnalytics_CL        |   689



<p align="center">
 
  | Metric                          |   Count
| ------------------------        |   -----
| SecurityEvent                   |   11490
| Syslog                          |   30
| SecurityAlert                   |   0
| SecurityIncident                |   13
| AzureNetworkAnalytics_CL        |   11
