<h1> <b>Implementing-a-SOC-and-Honeynet-in-Azure </b> </h1>
<h2>Description</h2>
This is a portfolio that shows my skill in using <b>Microsoft Sentinel</b>. In the project, the use of different Microsoft Azure packages were used such as Active Directory, Log Analytics workspace, Sentinel, Key Vault, Microsoft Defender for Cloud, Virtual Machines, collection rule (windows and Linux), Alert creation (Manual and automatic), workbook(shows map). <br/>

<br/>
In this project, I build a mini honeynet in Azure and ingest log sources from various resources into a Log Analytics workspace, which is then used by Microsoft Sentinel to build attack maps, trigger alerts, and create incidents. I measured some security metrics in the insecure environment for 24 hours, applied some security controls to harden the environment, measured metrics for another 24 hours, and then showed the results below. The metrics we will show are:

- SecurityEvent (Windows Event Logs)
- Syslog (Linux Event Logs)
- SecurityAlert (Log Analytics Alerts Triggered)
- SecurityIncident (Incidents created by Sentinel)
- AzureNetworkAnalytics_CL (Malicious Flows allowed into our honeynet)
<br />

<h2>Languages and Utilities Used</h2>

- <b>Google Chrome</b> 
- <b>Azure Microsoft Sentinel</b>
- <b>Azure Active directory</b>
- <b>Azure Microsoft defender for cloud</b>

<h2>Environments Used </h2>

- <b>Windows 10 PC</b>

<h2>Program walk-through:</h2>

<p align="center">
## Brief Diagram showing the entire project <br/>
<img src="https://i.imgur.com/2eaRuI2.png" height="80%" width="80%" alt="Implementing-a-SOC-and-Honeynet-in-Azure"/>
<br />
<br />

<h2>Architecture Before Harding / Security Controls</h2>
<p align="center">
<img src="https://i.imgur.com/8dlXyCE.png" height="80%" width="80%" alt="Implementing-a-SOC-and-Honeynet-in-Azure"/>
<h2>Architecture After Hardening / Security Controls</h2>
<p align="center">
<img src="https://i.imgur.com/BMS073z.png" height="80%" width="80%" alt="Implementing-a-SOC-and-Honeynet-in-Azure"/> <br>

 The architecture of the mini honeynet in Azure consists of the following components:
- Virtual Network (VNet)
- Network Security Group (NSG)
- Virtual Machines (2 Windows, 1 Linux)
- Log Analytics Workspace
- Azure Key Vault
- Azure Storage Account
- Microsoft Sentinel

For the "BEFORE" metrics, all resources were originally deployed, and exposed to the internet. The Virtual Machines had both their Network Security Groups and built-in firewalls wide open, and all other resources are deployed with public endpoints visible to the Internet; aka, no use for Private Endpoints.

For the "AFTER" metrics, Network Security Groups were hardened by blocking ALL traffic except my admin workstation, and all other resources were protected by their built-in firewalls as well as Private Endpoint

## Attack Maps Before Hardening / Security Controls
<h3>NSG Allowed Inbound Malicious Flows</h3>
<p align="center">
<img src="https://i.imgur.com/Jls4anR.png" height="80%" width="80%" alt="Implementing-a-SOC-and-Honeynet-in-Azure"/>
<h3>Linux Syslog Auth Failures</h3>
<p align="center">
<img src="https://i.imgur.com/UYP68Nm.png" height="80%" width="80%" alt="Implementing-a-SOC-and-Honeynet-in-Azure"/>
<h3>Windows RDP/SMB Auth Failures</h3>
<p align="center">
<img src="https://i.imgur.com/gifXZnN.png" height="80%" width="80%" alt="Implementing-a-SOC-and-Honeynet-in-Azure"/> <br>
<br>

## Metrics Before Hardening / Security Controls

The following table shows the metrics we measured in our insecure environment for 24 hours:
Start Time 2023-12-25 13:15:44
Stop Time 2023-12-26T13:15:44

| Metric                   | Count
| ------------------------ | -----
| SecurityEvent            | 25102
| Syslog                   | 4227
| SecurityAlert            | 1
| SecurityIncident         | 180
| AzureNetworkAnalytics_CL | 2240

## Attack Maps Before Hardening / Security Controls

```All map queries returned no results due to no instances of malicious activity for the 24-hour period after hardening.```

## Metrics After Hardening / Security Controls

The following table shows the metrics we measured in our environment for another 24 hours, but after I applied security controls:
Start Time 2023-12-28 00:06:44
Stop Time	2023-12-28 00:06:44

| Metric                   | Count
| ------------------------ | -----
| SecurityEvent            | 13023
| Syslog                   | 10
| SecurityAlert            | 0
| SecurityIncident         | 9
| AzureNetworkAnalytics_CL | 0

## Conclusion

In this project, a mini honeynet was constructed in Microsoft Azure and log sources were integrated into a Log Analytics workspace. Microsoft Sentinel was employed to trigger alerts and create incidents based on the ingested logs. Additionally, metrics were measured in the insecure environment before security controls were applied, and then again after implementing security measures. It is noteworthy that the number of security events and incidents were drastically reduced after the security controls were applied, demonstrating their effectiveness.

It is worth noting that if the resources within the network were heavily utilized by regular users, it is likely that more security events and alerts may have been generated within the 24-hour period following the implementation of the security controls.
<br />
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
