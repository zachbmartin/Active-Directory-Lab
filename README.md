<h1>Active Directory and Splunk Lab</h1>

<h2>Description</h2>
Created lab environment in Oracle VM's to conduct a brute-force attack on Active Directory user. Splunk is installed and configured to view telemetry.
<br />


<h2>Utilities Used</h2>

- <b>Splunk</b> 
- <b>Sysmon</b>

<h2>Environments Used </h2>

- <b>Windows 10</b> 
- <b>Kali Linux</b>
- <b>Ubuntu</b>

 
<h2>Program walk-through:</h2>

<p align="center">
Project Diagram: <br/>
<img src="https://imgur.com/YbRxmuJ.png" height="80%" width="80%" alt="ADproject"/>
<br />
<br />
Account for User "Jenny Smith" created in AD:  <br/>
<img src="https://imgur.com/X620lTq.png" height="80%" width="80%" alt="ADprojects"/>
<br />
<br />
20 random passwords to be ran for attack + actual password added at the bottom (assume it was acquired by some means of reconaissance): <br/>
<img src="https://imgur.com/Smhb06h.png" height="80%" width="80%" alt="ADproject"/>
<br />
<br />
Utilizing crowbar in Kali to conduct brute-force attack on user "jsmith":  
 <br/>
"RDP-success" inidicating succesful remote log in
<img src="https://imgur.com/15f0XnM.png" height="80%" width="80%" alt="ADproject"/>
<br />
<br />
Event ID 4625 (account failed to log on) has 20 attempts, matching with the password list
<br />
Event ID 4624 (account successfully logged on) has 1 attempt, matching with the successful attack from Linux machine  <br/>
<img src="https://imgur.com/uZ8hYNR.png" height="80%" width="80%" alt="ADproject"/>
<br />
<br />
Confirmed attack from Kali Linux machine:  <br/>
<img src="https://imgur.com/T1MkZeu.png" height="80%" width="80%" alt="ADproject"/>
<br />
<br />


<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
