<h1>Respond and Recover from a data breach in Google Cloud Lab</h1>


<h2>Description</h2>
<b>In this Lab, I am responding and recovering from a data breach inside Google Cloud. This lab requires me to assess and fix a Compute Engine virtual machine, a Cloud Storage bucket, and a firewall vulnerability in relation to the data breach.
</b>
<br />
<br />
<h2>Task 1: Analyze the data breach and gather information</h2>
<br />
<br />

<p align="center">
<h2>Security Command Center Risk Overview</h2>
<img src="https://i.imgur.com/c3XaKLK.jpeg" height="85%" width="85%" alt="Security Command Center Risk Overview"/>
<h2>Vunlerabilities tab</h2>
<img src="https://i.imgur.com/QifG85h.jpeg" height="85%" width="85%" alt="Risk Overview Vulnerabilities tab"/>
<h2>From the Security Command Center menu click compliance and scroll down to PCI DSS 3.2.1 and click this</h2>
<img src="https://i.imgur.com/Mj5G5qJ.jpeg" height="85%" width="85%" alt="Google Cloud Compliance tab"/>
<img src="https://i.imgur.com/TfaIo8a.jpeg" height="85%" width="85%" alt="PCI DSS 3.2.1 Compliance detail"/>
<h2>Scroll down to the Control compliance status and sort by Findings</h2>
<img src="https://i.imgur.com/Qi3dORq.jpeg" height="85%" width="85%" alt="Compliance detail sorted by Findings"/>
<h2>Go back to the main menu and click on Findings, and under Quick Filters, scroll down and check Google Cloud storage bucket</h2>
<img src="https://i.imgur.com/yWYEDBT.jpeg" height="85%" width="85%" alt="Findings page"/>
<img src="https://i.imgur.com/3EVoLTX.jpeg" height="85%" width="85%" alt="Quick filters then check Google Cloud storage bucket"/>

</p>
<h2>Languages Used</h2>

- <b>PowerShell:</b> Extract RDP failed logon logs from Windows Event Viewer 

<h2>Utilities Used</h2>

- <b>ipgeolocation.io:</b> IP Address to Geolocation API

<h2>Attacks from China coming in; Custom logs being output with geodata</h2>

<p align="center">
<img src="https://i.imgur.com/LhDCRz4.jpeg" height="85%" width="85%" alt="Image Analysis Dataflow"/>
</p>

<h2>World map of incoming attacks after 24 hours (built custom logs including geodata)</h2>

<p align="center">
<img src="https://i.imgur.com/krRFrK5.png" height="85%" width="85%" alt="Image Analysis Dataflow"/>
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
