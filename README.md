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
<h2>Go back to the main menu and click on Findings, and under Quick Filters, scroll down and check Google Cloud storage bucket. This shows all storage bucket findings, and the reason for the finding is located under Finding Class.</h2>
<img src="https://i.imgur.com/yWYEDBT.jpeg" height="85%" width="85%" alt="Findings page"/>
<img src="https://i.imgur.com/3EVoLTX.jpeg" height="85%" width="85%" alt="Quick filters then check Google Cloud storage bucket"/>
<h2>Uncheck Google Cloud, and then check Google Compute Instance. This selection will show all findings related to compute instances/virtual machines, and in this particular lab, it shows how this data breach took place. There is a malware threat finding which made the whole system vulnerable.</h2>
<img src="https://i.imgur.com/z86kZue.jpeg" height="85%" width="85%" alt="Quick filters then check Google Compute instance"/>
<h2>Uncheck Google Compute Instance and check Google Compute Firewall. This selection will show all findings related to firewall errors and misconfigurations.</h2>
<img src="https://i.imgur.com/x9Z2bsO.jpeg" height="85%" width="85%" alt="Quick filters then check Google Compute Firewall"/>
<br />
<br />
<h2>Task 2: Fix the Compute Engine vulnerabilities</h2>
<br />
<br />
<h2>Now that I've researched the breach and found the issues, it's time to start fixing them. </h2>

<p align="center">

<h2>Go to the main menu and scroll down to Compute Engine, then click VM instances</h2>
<img src="https://i.imgur.com/jMDzJuF.jpeg" height="85%" width="85%" alt="Compute Engine, VM instances"/>
<h2>Select the available instance, and click stop. This instance has the malware finding on it.</h2>
<img src="https://i.imgur.com/5g0fClP.jpeg" height="85%" width="85%" alt="Select active VM instance and click Stop"/>
<img src="https://i.imgur.com/8gmAic8.jpeg" height="85%" width="85%" alt="Select active VM instance and click Stop"/>
<h2>Once the instance stops, click create instance at the top of the screen</h2>
<img src="https://i.imgur.com/jnKZrND.jpeg" height="85%" width="85%" alt="Click Create Instance"/>
<h2>Configure new VM instance</h2>
<img src="https://i.imgur.com/mQduL35.jpeg" height="85%" width="85%" alt="Configure VM instance"/>
<img src="https://i.imgur.com/cAbtEmg.jpeg" height="85%" width="85%" alt="Configure VM instance2"/>
<img src="https://i.imgur.com/jW9WFmJ.jpeg" height="85%" width="85%" alt="Configure VM instance3"/>
<img src="https://i.imgur.com/BFsm4nS.jpeg" height="85%" width="85%" alt="Configure VM instance4"/>
<img src="https://i.imgur.com/axsmAsT.jpeg" height="85%" width="85%" alt="Configure VM instance5"/>
<h2>On the boot disk screen, make sure you click snapshots, and then select the last snapshot from the instance you stopped earlier. This insures the new VM instance is created with the same configuration/settings as the previous instance.</h2>
<img src="https://i.imgur.com/vUBy6TG.jpeg" height="85%" width="85%" alt="Ensure VM instance snapshot is selected"/>





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
