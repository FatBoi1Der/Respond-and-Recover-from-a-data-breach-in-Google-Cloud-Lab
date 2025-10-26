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
<h2>Once this is done, click networking on the left hand side, click the Network tags box and type in cc. Then scroll down and click the drop down menu under network interfaces and that brings up the edit network interface menu. Scroll down and change the External IPv4 address from Ephermal to none so the address it has already doesn't change.</h2>
<img src="https://i.imgur.com/CBGWxSw.jpeg" height="85%" width="85%" alt="Configure network settings for VM"/>
<img src="https://i.imgur.com/5l1mQKj.jpeg" height="85%" width="85%" alt="Configure network settings for VM2"/>
<img src="https://i.imgur.com/iqPMJIW.jpeg" height="85%" width="85%" alt="Configure network settings for VM3"/>
<img src="https://i.imgur.com/wdAm39n.jpeg" height="85%" width="85%" alt="Configure network settings for VM4"/>
<h2>Next, click security on the left hand side. Under Service accounts, make sure you select the appropriate account, and then click create at the bottom of the screen. VM should populate in about 5 minutes or less.</h2>
<img src="https://i.imgur.com/QvFfSzG.jpeg" height="85%" width="85%" alt="Configure security settings"/>
<img src="https://i.imgur.com/NT3YXBg.jpeg" height="85%" width="85%" alt="Configure security settings2"/>
<img src="https://i.imgur.com/3rKtVDp.jpeg" height="85%" width="85%" alt="Configure security settings3"/>
<h2>Next up, I make sure I turn on secure boot for the new VM instance.</h2>
<img src="https://i.imgur.com/pD3BSfN.jpeg" height="85%" width="85%" alt="Turning on secure boot"/>
<img src="https://i.imgur.com/QulTEj8.jpeg" height="85%" width="85%" alt="Turning on secure boot2"/>
<img src="https://i.imgur.com/iWF6sxJ.jpeg" height="85%" width="85%" alt="Turning on secure boot3"/>
<img src="https://i.imgur.com/BLCH4e6.jpeg" height="85%" width="85%" alt="Turning on secure boot4"/>
<h2>Make sure to restart the new VM. Once that VM is up and running, the VM with the malware threat can be deleted.</h2>
<img src="https://i.imgur.com/LrNeCcb.jpeg" height="85%" width="85%" alt="Restart new VM"/>
<img src="https://i.imgur.com/6IkEJio.jpeg" height="85%" width="85%" alt="Remove old VM"/>
<img src="https://i.imgur.com/HHycM2Q.jpeg" height="85%" width="85%" alt="Remove old VM2"/>
<br />
<br />
<h2>Task 3: Fix Cloud Storage bucket permissions</h2>
<br />
<br />
<h3>In this task I revoke public access to the storage bucket and switch to uniform bucket-level access control, which significantly reduces the risk of data breaches. Removing all user permissions from the storage bucket prevents unauthorized access to the data stored in the bucket.</h3>

<p align="center">
<img src="https://i.imgur.com/8NCi4dk.jpeg" height="85%" width="85%" alt="Remove bucket permissions"/>
<h3>Click the name of the bucket you wish to change the access controls and permissions for.</h3>
<img src="https://i.imgur.com/yoAsfTQ.jpeg" height="85%" width="85%" alt="Remove bucket permissions2"/>
<img src="https://i.imgur.com/bYeG6mH.jpeg" height="85%" width="85%" alt="Remove bucket permissions3"/>
<h3>On the Bucket details page, click Permissions.</h3>
<img src="https://i.imgur.com/ZudsL0v.jpeg" height="85%" width="85%" alt="Remove bucket permissions4"/>
<h3>Click Prevent Public Access</h3>
<img src="https://i.imgur.com/apYoIJT.jpeg" height="85%" width="85%" alt="Remove bucket permissions5"/>
<img src="https://i.imgur.com/juZ6AnN.jpeg" height="85%" width="85%" alt="Remove bucket permissions6"/>
<h3>Change Access Control from Fine-Grained to Uniform</h3>
<img src="https://i.imgur.com/5KRzoVq.jpeg" height="85%" width="85%" alt="Remove bucket permissions7"/>
<h3>Check the box on All Users under Permissions at the bottom of the page, and then click Remove Access.</h3>
<img src="https://i.imgur.com/Ifs1Qw3.jpeg" height="85%" width="85%" alt="Remove bucket permissions8"/>
<br />
<br />
<h2>Task 4: Limit Cloud Firewall Port Access</h2>
<br />
<br />
<h3>Go to the main menu and scroll down to VPC Network, and then Firewall. Once on the Firewall page, click Create Firewall Rule. Configure the firewall to restrict SSH which is Port 22, on the source network. Also make sure the logging feature is turned on, so the new firewall rule will keep accurate logs moving forward.</h3>
<img src="https://i.imgur.com/wb3uA8r.jpeg" height="85%" width="85%" alt="Firewall fixes"/>
<img src="https://i.imgur.com/SlPOydq.jpeg" height="85%" width="85%" alt="Firewall fixes2"/>
<img src="https://i.imgur.com/NbK70AM.jpeg" height="85%" width="85%" alt="Firewall fixes3"/>
<img src="https://i.imgur.com/VhSkj8E.jpeg" height="85%" width="85%" alt="Firewall fixes4"/>
<h3>Once the new firewall rule is created, the misconfigured rules need to be removed. Especially the SSH rule, since we are limiting that port with the new rule.</h3>
<img src="https://i.imgur.com/MrndJ47.jpeg" height="85%" width="85%" alt="Firewall fixes5"/>
<br />
<h2>Task 5: Verify Compliance</h2>
<br />
<br />
<h3>To finish this task, go to Security Command Center and then Compliance and scroll down to PCI DSS 3.2.1. When you click on this compliance control, it shows the new compliance level rises.</h3>
<img src="https://i.imgur.com/NmP1P98.jpeg" height="85%" width="85%" alt="Firewall fixes6"/>

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
