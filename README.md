<h1> <b>Implementing-a-SOC-and-Honeynet-in-Azure </b> </h1>
<h2>Description</h2>
This is a portfolio that shows my skill in using <b>Microsoft Sentinel</b>. In the project, the use of different Microsoft Azure packages was used such as Active Directory, Log Analytics workspace, Sentinel, Key Vault, Microsoft Defender for Cloud, Virtual Machines, collection rule (windows and Linux), Alert creation (Manual and automatic), workbook(shows map). 

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
Brief Diagram showing the entire project <br/>
<img src="https://i.imgur.com/RrBNnfz.png" height="80%" width="80%" alt="Microsoft Sentinel SIEM Steps"/>
<br />
<br />
Github profile to deploy Azure (https://github.com/Azure/Azure-Sentinel/tree/master/Tools/Sentinel-All-In-One)  <br/>
<img src="https://i.imgur.com/Jsmrq5T.png" height="80%" width="80%" alt="Microsoft Sentinel SIEM Steps"/>
<br />
<br />
Custom deployment configuration <br/>
<img src="https://i.imgur.com/nK1qtb6.png" height="80%" width="80%" alt="Microsoft Sentinel SIEM Steps"/>
<br />
<br />
Diagnostic Settings <br/>
<img src="https://i.imgur.com/U4Fy88k.png" height="80%" width="80%" alt="Microsoft Sentinel SIEM Steps"/>
<br />
<br />
Sentinel Analytic rules  <br/>
<img src="https://i.imgur.com/CC664dt.png" height="80%" width="80%" alt="Microsoft Sentinel SIEM Steps"/>
<br />
<br />
Setting up User Entity behavior <br/>
<img src="https://i.imgur.com/8soDNdU.png" height="80%" width="80%" alt="Microsoft Sentinel SIEM Steps"/>
<br />
<br />
Creating watchlist for  <br/>
<img src="https://i.imgur.com/GgIis0h.png" height="80%" width="80%" alt="Microsoft Sentinel SIEM Steps"/>
<br />
<br /> 
Creating an Analytic Scheduled Rule using KQL <br/>
<img src="https://i.imgur.com/fbAnegq.png" height="80%" width="80%" alt="Microsoft Sentinel SIEM Steps"/>
<br />
<br />
Alert Enrichment <br/>
<img src="https://i.imgur.com/422hjIQ.png" height="80%" width="80%" alt="Microsoft Sentinel SIEM Steps"/>
<br />
<br />
Custom and Alert Information <br/>
<img src="https://i.imgur.com/vtiQ3XD.png" height="80%" width="80%" alt="Microsoft Sentinel SIEM Steps"/>
<br />
<br />
Query Scheduling <br/>
<img src="https://i.imgur.com/PAadSOC.png" height="80%" width="80%" alt="Microsoft Sentinel SIEM Steps"/>
<br />
<br />
Incident Setting <br/>
<img src="https://i.imgur.com/QXPiu8p.png" height="80%" width="80%" alt="Microsoft Sentinel SIEM Steps"/>
<br />
<br />
Disabling Security Features <br/>
<img src="https://i.imgur.com/Qq0GOnM.png" height="80%" width="80%" alt="Microsoft Sentinel SIEM Steps"/>
<br />
<br />
creating a new user <br/>
<img src="https://i.imgur.com/N8Dz4S0.png" height="80%" width="80%" alt="Microsoft Sentinel SIEM Steps"/>
<br />
<br />
Assigning roles to the new user <br/>
<img src="https://i.imgur.com/WEwZ6AL.png" height="80%" width="80%" alt="Microsoft Sentinel SIEM Steps"/>
<br />
<br />
 New User Password Update  <br/>
<img src="https://i.imgur.com/SdxkiLC.png" height="80%" width="80%" alt="Microsoft Sentinel SIEM Steps"/>
<br />
<br />
Logging into the new user settings to perform an attack <br/>
<img src="https://i.imgur.com/SsiEdDs.png" height="80%" width="80%" alt="Microsoft Sentinel SIEM Steps"/>
<br />
<br />
Changing user's password for exploitation <br/>
<img src="https://i.imgur.com/EEP0pIt.png" height="80%" width="80%" alt="Microsoft Sentinel SIEM Steps"/>
<br />
<br /> 
Disabling and deleting Diagnostic settings <br/>
<img src="https://i.imgur.com/V3TiyeE.png" height="80%" width="80%" alt="Microsoft Sentinel SIEM Steps"/>
<br />
<br />
Disabling health monitoring <br/>
<img src="https://i.imgur.com/a8k417M.png" height="80%" width="80%" alt="Microsoft Sentinel SIEM Steps"/>
<br />
<br />
Generated incident Detected by Sentinel <br/>
<img src="https://i.imgur.com/EMLUxb1.png" height="80%" width="80%" alt="Microsoft Sentinel SIEM Steps"/>
<br />
<br />
Successful sign-in from Tor <br/>
<img src="https://i.imgur.com/1r4NTmL.png" height="80%" width="80%" alt="Microsoft Sentinel SIEM Steps"/>
<br />
<br />
Sentinel showing Logged activity by attacker  <br/>
<img src="https://i.imgur.com/ZDSqLjn.png" height="80%" width="80%" alt="Microsoft Sentinel SIEM Steps"/>
<br />
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
